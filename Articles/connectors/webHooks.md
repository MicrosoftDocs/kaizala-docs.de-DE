---
title: /webhooks
description: Referenzartikel zur API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: a2cdb74284f6980644366cf3b61740ea46389512
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190732"
---
# <a name="apis-to-register--manage-webhooks"></a>APIs zum Registrieren von & Manage webhooks
## <a name="webhook"></a>/webhook
API-Endpunkt zum Verwalten von Abonnements für Ereignisse in Kaizala.

WebHooks ist ein leichtes HTTP-Muster, das ein einfaches Publisher/Subscriber-Modell für die Verbindung von Web-APIs und SaaS-Diensten bereitstellt. Wenn in Kaizala ein Ereignis auftritt, wird eine Benachrichtigung in Form einer HTTP-POST-Anforderung an registrierte Abonnenten gesendet. Die POST-Anforderung enthält Informationen über das Ereignis, mit denen der Empfänger entsprechend handeln kann.


Mit webHooks können Sie verschiedene Ereignisse abonnieren, die innerhalb eines unterhaltungsgruppen Kontexts in Kaizala auftreten.

### <a name="post-webhook"></a>POST/webhook

    POST {endpoint-url}/v1/webhook

Um sicherzustellen, dass Ihr webhook-Dienstendpunkt authentisch ist und funktioniert, überprüfen wir Ihre Rückruf-URL, bevor Sie ein Abonnement erstellen. Zur Überprüfung senden wir Ihnen ein Validierungs Token zu, das Sie innerhalb von 5 Sekunden zurücksenden müssen. [Weitere Informationen](WebHookValidaton.md)

#### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token || HTTP-Header | Content-Type | String | Nein | "application/json" |

#### <a name="request-body"></a>Anforderungstext

|  Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| objectId | String | Nein | Bezeichner, der das Objekt darstellt, in dem der Kontext der webhooks erstellt werden muss. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier |
| objectType | String | Nein | Enum: "Group"/"action"/"ActionPackage" |
| eventTypes | Array | Nein | Array unterschiedlicher Ereignistypen, für die Sie den webhook abonnieren müssen. Unterstützte Ereignisse sind folgende: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ansage", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved" |
| callBackUrl | String | Nein | HTTPS-URL, an die die abonnierten Ereignisse benachrichtigt werden müssen |
| callBackToken | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf des webHooks gesendet wird. |
| callBackcontext | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als ' context ' gesendet wird, bei jedem Rückruf, der vom webHook ausgeführt wird. |
| Gültigkeit | Zeichenfolge | Ja | Gültigkeit für die webHook-Aktivität im EPOCH-Format. Standardwert ist 2 Jahre |


#### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| webhook-Nr. | String | Bezeichner, der den erstellten webHook darstellt |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a>AnforderungsText – abonnieren aller Ereignisse auf Gruppenebene

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


Das webhook-Antwortschema für registrierte Ereignisse in Kaizala finden Sie [**hier**](EventSchema.md).

> **Hinweis:** Kaizala garantiert, dass die webhook-Antwort mindestens einmal bereitgestellt wird. In bestimmten Fällen kann es vorkommen, dass Kaizala doppelte webhook-Antwort für dasselbe Ereignis sendet.

### <a name="get-webhook"></a>/Webhook abrufen

    GET {Endpoint-URL}/v1/webhook

#### <a name="request-parameters"></a>AnforderungsParameter


|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| Abfrageparameter | objectId | String | Nein | Bezeichner, der das Objekt darstellt, in dem der Kontext der webhooks erstellt werden muss. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier |
| Abfrageparameter | objectType | String | Nein | Enum: "Group"/"action"/"ActionPackage" |

#### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| webhooks | JSON-Objekt Array | Array von webhooks, die für die objectId abonniert wurden |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a>JSON-Struktur für jeden einzelnen webhook im Array webhooks []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| id | String | Webhook-ID |
| objectId | String | Objektbezeichner |
| objectType | Zeichenfolge | Enum: "Group"/"action"/"ActionPackage" |
| events | String [] | Ereignisliste mit jedem Wert von "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ansage", "MemberAdded", "MemberRemoved", "GroupAdded"; " GroupRemoved " |
| callBackUrl | String | Rückruf-URL, an die die abonnierten Ereignisse benachrichtigt werden müssen |
| callBackToken | String | Parameter, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf des webHooks gesendet wird. |
| callBackcontext | String | Parameter, der in der JSON-Nutzlast als "Context" gesendet wird und jeder Rückruf durch den webHook erfolgt. |
| Gültigkeit | String | Gültigkeit für die webHook-Aktivität im EPOCH-Format. |
| Active | Boolean | True, wenn der Status von webhook aktiv ist |

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

    DELETE {Endpoint-URL}/v1/webhook

#### <a name="request-parameters"></a>AnforderungsParameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| Path-Parameter | webhook-Nr. | String | Nein | Webhook-ID |

### <a name="put-webhook"></a>PUT/webhook

    PUT {endpoint-url}/v1/webhook/{webhookId}

Jeder Parameter für den webhook kann aktualisiert werden. Der AnforderungsText kann je nach Bedarf 1 oder mehr Parameter enthalten.

#### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| Path-Parameter | webhook-Nr. | String | Nein | Webhook-ID |

#### <a name="request-body"></a>Anforderungstext

|  Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| objectId | Zeichenfolge | Ja | Bezeichner, der das Objekt darstellt, in dem der Kontext der webhooks erstellt werden muss. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier |
| objectType | Zeichenfolge | Ja | Enum: "Group"/"action"/"ActionPackage" |
| eventTypes | Array | Ja | Array unterschiedlicher Ereignistypen, für die Sie den webhook abonnieren müssen. Unterstützte Ereignisse sind folgende: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ansage", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved" |
| callBackUrl | Zeichenfolge | Ja | HTTPS-URL, an die die abonnierten Ereignisse benachrichtigt werden müssen |
| callBackToken | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf des webHooks gesendet wird. |
| callBackcontext | Zeichenfolge | Ja | Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als ' context ' gesendet wird, bei jedem Rückruf, der vom webHook ausgeführt wird. |
| Gültigkeit | String | Ja | Gültigkeit für die webHook-Aktivität im EPOCH-Format. Standardwert ist 2 Jahre |
| Aktiv | Boolean | Ja | Ändern Sie den Zustand der webhook in aktiv, wenn der Wert true ist |


#### <a name="sample-request-body"></a>Beispiel für AnforderungsText

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

## <a name="auto-disable-of-webhooks"></a>Automatische deAktivierung von webhooks

Zur Verbesserung der Zuverlässigkeit unserer webhooks haben wir vor kurzem die Wiederholungs-und deAktivierungs Logik hinzugefügt. Die mit einem webhook registrierte Callback-URL/-Endpunkt, wenn Sie nicht erreichbar ist oder nicht mit einem anderen Statuscode als 2xx (> = 3xx) antwortet, dann versucht unser Dienst, es sechs Mal exponentiell innerhalb einer Spanne von 2 Tagen zu erreichen. 

Wenn es noch 2 Tage fehlschlägt, wird der entsprechende webhook deaktiviert, und der Besitzer muss es mit der Put-/webhook-API aktualisieren, bevor es wieder beginnt zu arbeiten. Beispielsweise

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a>AnforderungsText:
````javascript
{ 
  "Active": "true" 
} 
````
