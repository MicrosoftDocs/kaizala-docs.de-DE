---
title: /webhooks
description: Referenzartikel zur API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: e5064e88bbc492a21883ad813792a1d69f54769c
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535772"
---
# <a name="apis-to-register--manage-webhooks"></a>APIs zum Registrieren #a0 Verwalten von webhooks
## <a name="webhook"></a>/webhook
API-Endpunkt zum Verwalten von Abonnements für Ereignisse in Kaizala.

Webhooks ist ein leichtes http-Muster, das ein einfaches Publisher/Subscriber-Modell für die Verkabelung von webapis und Saas-Diensten bereitstellt. Wenn ein Ereignis in Kaizala erfolgt, wird eine Benachrichtigung in Form einer HTTP POST-Anforderung an registrierte Abonnenten gesendet. Die Post-Anforderung enthält Informationen über das Ereignis, das es dem Empfänger ermöglicht, entsprechend zu handeln.


Mithilfe von webhooks können Sie verschiedene Ereignisse abonnieren, die innerhalb eines unterhaltungsgruppen Kontexts in Kaizala auftreten.

### <a name="post-webhook"></a>Post/webhook

    POST {endpoint-url}/v1/webhook

Um sicherzustellen, dass Ihr webhook-Dienstendpunkt authentisch ist und funktioniert, überprüfen wir Ihre Rückruf-URL vor dem Erstellen des Abonnements. Zur Überprüfung senden wir Ihnen ein Validierungs Token, das Sie benötigen, um uns innerhalb von 5 Sekunden zurückzusenden. [Weitere Informationen](WebHookValidation.md)

#### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token || HTTP-Header | Content-Type | String | Nein | "application/json" |

#### <a name="request-body"></a>Anforderungstext

|  Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| objectId | String | Nein | Bezeichner, der das Objekt darstellt, in welchem Kontext die webhooks erstellt werden müssen. Für ObjectType = Group, den Bezeichner der Gruppe, für ObjectType = Action, seine Aktions-ID, für ObjectType = ActionPackage, dessen Aktionspaket-ID |
| objectType | String | Nein | Enum: "Group"/"action"/"ActionPackage" |
| eventTypes | Array | Nein | Array verschiedener Ereignistypen, für die Sie den webhook abonnieren müssen. Unterstützte Ereignisse sind: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Announcement", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved" |
| callBackUrl | String | Nein | HTTPS-URL, zu der die abonnierten Ereignisse benachrichtigt werden müssen |
| callBackToken | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, welcher im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird |
| callbackcontext | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als "Context" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird |
| Gültigkeit | Zeichenfolge | Ja | Gültigkeit, damit der webhook im Epoch-Format aktiv ist. Der Standardwert ist 2 Jahre. |


#### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| webhook-Verknüpfung | String | Bezeichner, der den erstellten webhook darstellt |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a>Anforderungstext – abonnieren aller Ereignisse auf Gruppenebene

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


Sie können das webhook-Antwortschema für registrierte Ereignisse in Kaizala [**hier**](EventSchema.md)finden.

> **Hinweis:** Kaizala garantiert mindestens einmal die Zustellung der webhook-Antwort. In bestimmten Fällen kann es vorkommen, dass Kaizala doppelte webhook-Antwort für dasselbe Ereignis senden kann.

### <a name="get-webhook"></a>/Webhook abrufen

    Get {Endpunkt-URL}/v1/webhook

#### <a name="request-parameters"></a>Anforderungsparameter


|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| Abfrageparameter | objectId | String | Nein | Bezeichner, der das Objekt darstellt, in welchem Kontext die webhooks erstellt werden müssen. Für ObjectType = Group, den Bezeichner der Gruppe, für ObjectType = Action, seine Aktions-ID, für ObjectType = ActionPackage, dessen Aktionspaket-ID |
| Abfrageparameter | objectType | String | Nein | Enum: "Group"/"action"/"ActionPackage" |

#### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| webhooks | JSON-Objekt Array | Array von webhooks, die für die ObjectID abonniert sind |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a>JSON-Struktur für jeden einzelnen webhook im Array webhooks []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| id | String | Webhook-Bezeichner |
| objectId | String | Objektbezeichner |
| objectType | Zeichenfolge | Enum: "Group"/"action"/"ActionPackage" |
| events | String [] | Ereignisliste mit jedem Wert als eine von "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Announcement", "MemberAdded", "MemberRemoved", "GroupAdded", " GroupRemoved" |
| callBackUrl | String | Rückruf-URL, zu der die abonnierten Ereignisse benachrichtigt werden müssen |
| callBackToken | String | Parameter, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird |
| callbackcontext | String | In der JSON-Nutzlast als "Context" gesendeter Parameter mit jedem Rückruf, der vom webhook vorgenommen wird |
| Gültigkeit | String | Gültigkeit, damit der webhook im Epoch-Format aktiv ist. |
| Active | Boolesch | True, wenn der Status von webhook aktiv ist |

##### <a name="sample-json-response"></a>JSON-Beispielantwort

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
            "active": true
        }
    ]
}
```

### <a name="delete-webhook"></a>/Webhook löschen

    DELETE {Endpunkt-URL}/v1/webhook

#### <a name="request-parameters"></a>Anforderungsparameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| Path-Parameter | webhook-Verknüpfung | String | Nein | Webhook-Bezeichner |

### <a name="put-webhook"></a>Put/webhook

    PUT {endpoint-url}/v1/webhook/{webhookId}

Jeder Parameter für den webhook kann aktualisiert werden. Der Anforderungstext kann bei Bedarf 1 oder mehr Parameter enthalten.

#### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| Path-Parameter | webhook-Verknüpfung | String | Nein | Webhook-Bezeichner |

#### <a name="request-body"></a>Anforderungstext

|  Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| objectId | Zeichenfolge | Ja | Bezeichner, der das Objekt darstellt, in welchem Kontext die webhooks erstellt werden müssen. Für ObjectType = Group, den Bezeichner der Gruppe, für ObjectType = Action, seine Aktions-ID, für ObjectType = ActionPackage, dessen Aktionspaket-ID |
| objectType | Zeichenfolge | Ja | Enum: "Group"/"action"/"ActionPackage" |
| eventTypes | Array | Ja | Array verschiedener Ereignistypen, für die Sie den webhook abonnieren müssen. Unterstützte Ereignisse sind: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Announcement", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved" |
| callBackUrl | Zeichenfolge | Ja | HTTPS-URL, zu der die abonnierten Ereignisse benachrichtigt werden müssen |
| callBackToken | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, welcher im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird |
| callbackcontext | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als "Context" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird |
| Gültigkeit | String | Ja | Gültigkeit, damit der webhook im Epoch-Format aktiv ist. Der Standardwert ist 2 Jahre. |
| Aktiv | Boolesch | Ja | Ändern des Status von webhook in "aktiv", wenn der Wert "true" lautet |


#### <a name="sample-request-body"></a>Beispiel Anforderungstext

````javascript
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
      "Active": "true" 
    } 

````

## <a name="auto-disable-of-webhooks"></a>Automatisches Deaktivieren von webhooks

Um die Zuverlässigkeit unserer webhooks zu verbessern, haben wir vor kurzem die Logik wiederholen und deaktivieren hinzugefügt. Die mit einem webhook registrierte Rückruf-URL/der Endpunkt, wenn Sie nicht erreichbar ist oder nicht mit einem anderen Statuscode als 2xx (>= 3xx) antwortet, versucht unser Dienst, ihn 6 Mal exponentiell innerhalb einer Spanne von 2 Tagen zu erreichen/wiederholen. 

Wenn es immer noch 2 Tage lang nicht funktioniert, wird der entsprechende webhook deaktiviert, und der Besitzer muss ihn mit der Put/webhook-API aktualisieren, bevor er wieder mit der Arbeit beginnt. Für z.b.

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a>Anforderungstext:
````javascript
{ 
  "Active": "true" 
} 
````
