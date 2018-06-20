---
title: /webhooks
description: Referenzartikel für API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: 8b78449ba41042de262bed7e3317771ef33c8031
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905388"
---
# <a name="apis-to-register--manage-webhooks"></a>APIs für das registrieren & Webhooks verwalten
## <a name="webhook"></a>/webhook
Zum Verwalten von Abonnements auf Ereignisse innerhalb Kaizala API-Endpunkt.

WebHooks besteht aus einem kompakten HTTP-Muster ein einfachen Publisher-Abonnent-Modells für Verdrahtung zusammen Web-APIs und SaaS Services bereitstellen. Wenn ein Ereignis in Kaizala passiert, wird eine Benachrichtigung in Form von HTTP POST-Anforderung an die registrierten Abonnenten gesendet. Die POST-Anforderung enthält Informationen über das Ereignis für den Empfänger an, entsprechend agieren kann.


WebHooks verwenden, können Sie verschiedene Abonnieren von Ereignissen, die innerhalb einer Unterhaltung Gruppe in Kaizala Kontext auftreten.

### <a name="post-webhook"></a>/Webhook buchen

    POST {endpoint-url}/v1/webhook

Um sicherzustellen, dass Ihr Dienstendpunkt Webhook authentisch und betriebsbereit ist wird wir Ihr Callback-URL überprüfen, bevor Abonnement erstellen. Zur Überprüfung werden wir Sie ein Token Validation senden, die Sie uns wieder innerhalb von 5 Sekunden senden müssen. [Erfahren Sie mehr](WebHookValidaton.md)

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt || HTTP-Header | Content-Type | String | Nein | "Application/Json" |

##### <a name="request-body"></a>Anforderungstext

|  Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| objectId | String | Nein | Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id |
| objectType | String | Nein | Enum: "Group" / "Aktion" / "ActionPackage" |
| eventTypes | Array | Nein | Array von verschiedenen Arten von Ereignissen, denen Sie die Webhook zu abonnieren müssen. Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved" |
| callBackUrl | String | Nein | HTTPS-URL, an die die abonnierten Ereignisse, gemeldet werden müssen |
| callBackToken | String | Ja | Ein optionaler Parameter können Sie festlegen, die im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird |
| callBackContext | String | Ja | Ein optionaler Parameter können Sie festlegen, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet wird |
| Gültigkeit | String | Ja | Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein. Der Standardwert lautet 2 Jahre |


##### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| webhookId | String | Bezeichner für die WebHook erstellt |

##### <a name="request-body---subscribe-to-all-events-at-group-level"></a>Anforderungstextkörper - alle Ereignisse auf Gruppenebene abonnieren

```javascript
{  
   "objectId":"74943849802190eaea3810",
   "objectType":"Group",
   "eventTypes":[
      "ActionCreated",
      "ActionResponse",
      "SurveyCreated",
      "JobCreated",
      "SurveyResponse",
      "JobResponse",
      "TextMessageCreated",
      "AttachmentCreated",
      "Announcement",
      "MemberAdded",
      "MemberRemoved",
      "GroupAdded",
      "GroupRemoved"
   ],
   "callBackUrl":"https://requestb.in/123",
   "callBackToken":"tokenToBeVerifiedByCallback",
   "callBackContext":"Any data which is required to be returned in callback"
}

```


Finden Sie Webhook Antwortschema für registrierte Ereignisse in Kaizala [**hier**](EventSchema.md).

### <a name="get-webhook"></a>Abrufen von /webhook

    GET {endpoint-url}/v1/webhook

##### <a name="request-parameters"></a>Anforderungsparameter


|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| Abfrageparameter | objectId | String | Nein | Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id |
| Abfrageparameter | objectType | String | Nein | Enum: "Group" / "Aktion" / "ActionPackage" |

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| webhooks | JSON-Objekt-Array | Array von Webhooks auf ObjectId abonniert |

######  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a>JSON-Struktur für jede einzelne Webhook in das Array Webhooks []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| id | String | Webhook-Bezeichner |
| objectId | String | Objekt-ID |
| objectType | String | Enum: "Group" / "Aktion" / "ActionPackage" |
| events | String] | Ereignisliste mit jedem Wert als eines der "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ankündigung", "MemberAdded", "MemberRemoved", "GroupAdded" " GroupRemoved" |
| callBackUrl | String | Callback-URL an die die abonnierten Ereignisse, gemeldet werden müssen |
| callBackToken | String | Parameter der im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird |
| callBackContext | String | Parameter, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet |
| Gültigkeit | String | Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein. |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "webhooks": [
        {
            "id": "dac6fccf-f2e9-4abc-94d7-793037e99da7",
            "objectId": "b21405d1-4b10-4c46-bfa9-8338592f3782",
            "objectType": "Group",
            "events": [
                "ActionCreated",
                "ActionResponse",
                "SurveyCreated",
                "JobCreated",
                "SurveyResponse",
                "JobResponse",
                "TextMessageCreated",
                "AttachmentCreated",
                "Announcement",
                "MemberAdded",
                "MemberRemoved",
                "GroupAdded",
                "GroupRemoved"
            ],
            "filters": [],
            "callbackUrl": "https://requestb.in/12786un1",
            "callbackToken": "tokenToBeVerifiedByCallback",
            "ts": 1505491564677,
            "validity": 1568605416677
        }
    ]
}
```

### <a name="delete-webhook"></a>/Webhook löschen

    DELETE {endpoint-url}/v1/webhook

##### <a name="request-parameters"></a>Anforderungsparameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| Pfadparameter | webhookId | String | Nein | Webhook-Bezeichner |
