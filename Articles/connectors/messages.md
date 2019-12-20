---
title: /messages
description: Referenzartikel zur API zum Abfragen von Nachrichten, die von Ina Group gesendet werden
topic: Reference
author: nitinjms
ms.openlocfilehash: 64d694e067336a7da0c08ea116498086ee5650ce
ms.sourcegitcommit: 9e57984827280ed977019d33dd78b1ce5e3097fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2019
ms.locfileid: "40809431"
---
# <a name="messages"></a>/messages

API-Endpunkt zum Senden von Nachrichten an unterhaltungsgruppen in Kaizala.

## <a name="post-messages"></a>Post/Messages

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt. |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | Zeichenfolge | Nein | Wert: Application/JSON |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| message | String | Nein | Zu sendende Text Nachricht (maximale Grenze von 4000 Zeichen) |
| sendToAllSubscribers | Boolescher Wert | Ja | Default: false. Gilt nur für den Fall, dass die Gruppen-Nr zu einer öffentlichen Gruppe gehört. True, wenn die Textnachricht an alle Abonnenten gesendet werden soll, für die der Benutzer des Tokens Administrator der öffentlichen Gruppe sein muss. |
| Abonnenten | String [] | Ja | Jedes Element entspricht einer Mobiltelefonnummer (mit Landesvorwahl). EG. + 911999999999). Die Text Nachricht wird nur an die ausgewählten Abonnenten gesendet. Für die selektive Kommunikation mit Teilnehmern im Kontext einer öffentlichen Gruppe verwendet werden |

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
