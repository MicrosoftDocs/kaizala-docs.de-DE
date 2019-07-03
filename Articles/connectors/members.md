---
title: /members
description: Referenzartikel zur API für Abfragegruppen Mitgliederdaten
topic: Reference
author: nitinjms
ms.openlocfilehash: d4f71858cfd58a4d6dd33f3d3d14b5ac855a757a
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535774"
---
# <a name="members"></a>/members
API-Endpunkt zum Hinzufügen oder Löschen von Mitgliedern aus unterhaltungsgruppen in Kaizala.

## <a name="get-members"></a>/Members abrufen

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt. |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Elemente | JSON-Array | Array von JSON-Objekten, die jeweils ein Mitglied der Gruppe darstellen |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

## <a name="put-members"></a>Put/Members

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt. |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/JSON |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Elemente | Zeichenfolgenarray | Array mit gut formatierten Telefonnummern neuer Mitglieder, die hinzugefügt werden sollen |

#### <a name="sample-json-request"></a>JSON-Beispielanforderung

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
| result | Boolesch | True, wenn alle Telefonnummern erfolgreich der Gruppe hinzugefügt wurden |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt. |
| URL-Pfad-Parameter | memberId | String | Nein | GUID, die die Mitglieds-ID des bestimmten Members darstellt |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| result | Boolesch | True, wenn das angegebene Element erfolgreich aus der Gruppe entfernt wurde |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "result": "true"
}
```
