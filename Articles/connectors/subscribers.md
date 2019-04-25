---
title: /Subscribers
description: Referenzartikel zur API zum Abrufen von Abonnentendaten für öffentliche Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190698"
---
# <a name="subscribers"></a>/Subscribers

API-Endpunkt zum Hinzufügen, Abrufen oder Löschen von Abonnenten aus verwalteter öffentlicher Gruppe.

## <a name="add-subscribers"></a>/Subscribers hinzufügen

    PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/add

### <a name="request-parameters"></a>AnforderungsParameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="request-body"></a>Anforderungstext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Abonnenten | String [] | Jede Zeichenfolge steht für eine Mobiltelefonnummer mit Landesvorwahl (zB. + 911111111111) |

#### <a name="sample-json-request"></a>JSON-Beispielanforderung
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | JSON-Objekt | Jeder Schlüssel dieses JSON-Objekts stellt die Mobiltelefonnummer dar, und value stellt das JSON-Objekt dar, das Erfolg oder Fehler mit Reason enthält. |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

## <a name="get-subscribers"></a>/Subscribers abrufen

    POST {Endpunkt-URL}/v1/groups/{groupId}/subscribers

### <a name="request-parameters"></a>AnforderungsParameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| Cursor | Zeichenfolge | Ja | Anfang des Resultsets. Zur Paginierung. Zurückgegeben im Antworttext |
| count | int | Ja | Standard: 50. Max: 50. Anzahl der Abonnenten, die in einem Resultset zurückgegeben werden sollen|

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Abonnenten | JSON-Array | Array von JSON-Objekten, die jeweils einen Teilnehmer der Gruppe darstellen |
| Cursor | String | Anfang des Resultsets. Zur Paginierung. Wird im Anforderungstext zum Abrufen des nächsten Resultsets verwendet. Wird nur dann als Antwort angezeigt, wenn ein gültiger nächster Resultset vorhanden ist. |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

## <a name="remove-subscribers"></a>/Subscribers entfernen

    PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/remove

### <a name="request-parameters"></a>AnforderungsParameter
|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="request-body"></a>Anforderungstext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Abonnenten | String [] | Jede Zeichenfolge steht für eine Mobiltelefonnummer mit Landesvorwahl (zB. + 911111111111) |

#### <a name="sample-json-request"></a>JSON-Beispielanforderung
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | JSON-Objekt | Jeder Schlüssel dieses JSON-Objekts stellt die Mobiltelefonnummer dar, und value stellt das JSON-Objekt dar, das Erfolg oder Fehler mit Reason enthält. |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

