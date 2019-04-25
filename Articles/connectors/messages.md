---
title: /Messages
description: Referenzartikel zur API zum Abfragen von Nachrichten, die an Ina Group gesendet wurden
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190712"
---
# <a name="messages"></a>/Messages

API-Endpunkt zum Senden von Nachrichten an unterhaltungsgruppen innerhalb von Kaizala.

## <a name="post-messages"></a>POST/Messages

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/JSON |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| message | String | Nein | Zu sendende Text Nachricht (maximale Grenze von 1000 Zeichen) |
| sendToAllSubscribers | Boolescher Wert | Ja | Standard: false. Gilt nur für den Fall, dass die Gruppen-zu einer öffentlichen Gruppe gehört. True, um die Textnachricht an alle Abonnenten zu senden, für die der Benutzer des Tokens als Administrator der öffentlichen Gruppe erforderlich ist. |
| Abonnenten | String [] | Ja | Jedes Element entspricht einer Mobiltelefonnummer (mit Landesvorwahl. EG. + 911999999999). Text Nachricht wird nur an die ausgewählten Abonnenten gesendet. Zur selektiven Kommunikation mit Abonnenten im Kontext einer öffentlichen Gruppe |

#### <a name="sample-json-request"></a>JSON-Beispielanforderung

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | GUID, die den erfolgreichen Abschluss der Anforderung darstellt |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
