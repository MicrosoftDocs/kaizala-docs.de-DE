---
title: /Subscribers
description: Verweisen auf Artikel, um die API zum Abrufen von Abonnenten Daten für öffentliche Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: b026c8c38ce3cea600219a3e5713726013e62367
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905335"
---
# <a name="apis-to-query-subscribers-data-in-a-public-group"></a>APIs für das Abfragen von Daten in einer öffentlichen Gruppe-Abonnenten
## <a name="subscribers"></a>/Subscribers

API-Endpunkt hinzufügen, Abrufen oder Abonnenten von verwalteten öffentliche Gruppe löschen.

### <a name="add-subscribers"></a>/Subscribers hinzufügen

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add

##### <a name="request-parameters"></a>Anforderungsparameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

##### <a name="request-body"></a>Anforderungstext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Abonnenten | String] | Jede Zeichenfolge stellt Mobiltelefonnummer mit Ländercode (z. B.. +911111111111) |

###### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

##### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | JSON-Objekt | Jeder Schlüssel in Json-Objekt repräsentiert die Mobiltelefonnummer und Wert darstellt, enthält Erfolg oder Fehler mit Grund Json-Objekt |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "result": {
        "+911111111111": {
            "isAdded": true
        },
        "+911111111112": {
            "isAdded": true
        }
    }
}
```

### <a name="get-subscribers"></a>Abrufen von /subscribers

    POST {endpoint-url}/v1/groups/{groupId}/subscribers

##### <a name="request-parameters"></a>Anforderungsparameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

##### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| Cursor | String | Ja | Anfang des Resultset. Für die Paginierung. In Antworttext zurückgegeben |
| count | int | Ja | Standard: 50. Max: 50. Anzahl von Abonnenten in einem Resultset zurückgegeben werden soll|

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Abonnenten | JSON-Array | Array von JSON-Objekten jeder Teilnehmer an der Gruppe darstellt |
| Cursor | String | Anfang des Resultset. Für die Paginierung. Legen Sie für die nächste Ergebnis im Textkörper der Anforderung verwendet werden soll. Teilnehmende Antwort nur dann, wenn eine gültige nächste Resultset. |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "subscribers": [
        {
            "id": "e2238eb5-2f45-4783-8f4b-571549db86c0",
            "mobileNumber": "+91109999999",
            "name": "",
            "profilePic": "",
            "isProvisioned": false
        }
    ]
}
```

### <a name="remove-subscribers"></a>/Subscribers entfernen

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove

##### <a name="request-parameters"></a>Anforderungsparameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

##### <a name="request-body"></a>Anforderungstext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Abonnenten | String] | Jede Zeichenfolge stellt Mobiltelefonnummer mit Ländercode (z. B.. +911111111111) |

###### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

##### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | JSON-Objekt | Jeder Schlüssel in Json-Objekt repräsentiert die Mobiltelefonnummer und Wert darstellt, enthält Erfolg oder Fehler mit Grund Json-Objekt |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "result": {
        "+911111111111": {
            "isRemoved": true
        },
        "+911111111112": {
            "isRemoved": true
        }
    }
}
```

