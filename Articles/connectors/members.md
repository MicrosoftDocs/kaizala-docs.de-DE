---
title: /Members
description: Referenzartikel für Abfragen Gruppe Mitglieder von Daten-API
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905351"
---
# <a name="members"></a>/Members
Hinzufügen oder Löschen von Mitgliedern aus Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.

## <a name="get-members"></a>Abrufen von /members

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Elemente | JSON-Array | Array von JSON-Objekten jedes, ein Mitglied der Gruppe darstellt. |

#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
  "members": [
    {
      "id": "4deffa08-guid-4b87-8c2f-d944565f5f31",
      "role": "Admin",
      "mobileNumber": "+919652000000",
      "isProvisioned": true
    },
    {
      "id": "2e20e9ac-guid-47bd-abac-1f5236004684",
      "role": "Member",
      "mobileNumber": "+919652000001",
      "isProvisioned": false
    }
  ]
}
```

## <a name="put-members"></a>PLATZIEREN Sie /members

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/Json |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Elemente | Zeichenfolgenarray | Array von gut formatierte Telefonnummern der neuen Elemente hinzugefügt werden soll |

#### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | Boolean | True, wenn alle Rufnummer erfolgreich an die Gruppe hinzugefügt wurden |

#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a>/Members löschen

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Pfad-Parameter | memberId | String | Nein | GUID, die die MemberId des bestimmten Elements darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | Boolean | True, wenn das angegebene Element wurde erfolgreich aus der Gruppe entfernt |

#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "result": "true"
}
```
