---
title: /Messages
description: Referenzartikel für API auf Abfragenachrichten gesendet, einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 25e3a918c95bd045a374de0420eda6324d46046a
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905368"
---
# <a name="apis-to-query-messages-sent-in-a-group"></a>APIs für die von Abfragenachrichten in einer Gruppe
## <a name="messages"></a>/Messages
Zum Senden von Nachrichten an Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.

### <a name="post-messages"></a>POST-/messages

    POST {endpoint-url}/v1/groups/{groupId}/messages

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/Json |

##### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| message | String | Nein | Textnachricht (Max 1.000 Zeichen begrenzt) gesendet werden |
| sendToAllSubscribers | Bool | Ja | Standard: false. Gültige nur im Fall der GroupId öffentliche Gruppe gehört. True, um die Text-Nachricht an alle Abonnenten senden bewirkt, dass die das Token Benutzer Admin der Gruppe der öffentlich sein |
| Abonnenten | String] | Ja | Jedes Element entspricht einer Mobiltelefonnummer (mit Ländercode. EG. +911999999999). Textnachricht wird nur für die ausgewählten Abonnenten gesendet werden. Für selektive Kommunikation für Abonnenten im Kontext eines öffentliche Gruppe verwendet werden soll |

###### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | GUID, die nach erfolgreicher Abschluss der Anforderung darstellt. |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
