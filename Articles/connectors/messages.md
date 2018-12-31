---
title: /Messages
description: Referenzartikel für API auf Abfragenachrichten gesendet, einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 58839035fca768f92eda40974029208eb31dda7f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/31/2018
ms.locfileid: "27465701"
---
# <a name="messages"></a>/Messages

Zum Senden von Nachrichten an Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.

## <a name="post-messages"></a>POST-/messages

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/Json |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| message | String | Nein | Textnachricht (Max 1.000 Zeichen begrenzt) gesendet werden |
| sendToAllSubscribers | Boolescher Wert | Ja | Standard: False. Gültige nur im Fall der GroupId öffentliche Gruppe gehört. True, um die Text-Nachricht an alle Abonnenten senden bewirkt, dass die das Token Benutzer Admin der Gruppe der öffentlich sein |
| Abonnenten | String] | Ja | Jedes Element entspricht einer Mobiltelefonnummer (mit Ländercode. EG. +911999999999). Textnachricht wird nur für die ausgewählten Abonnenten gesendet werden. Für selektive Kommunikation für Abonnenten im Kontext eines öffentliche Gruppe verwendet werden soll |

#### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | GUID, die den erfolgreichen Abschluss der Anforderung darstellt. |

#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
