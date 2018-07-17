---
title: /subGroups
description: Referenzartikel für Abfragen Untergruppe von Daten-API
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399367"
---
# <a name="subgroups"></a>/subGroups
API-Endpunkt zur Interaktion mit der Unterhaltung Unterseite innerhalb Kaizala gruppiert.

## <a name="get-subgroups"></a>Abrufen von /subGroups

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Abfrageparameter | fetchAllGroups | Boolean | Ja | Parameter, um anzugeben, wenn alle Untergruppen in der Hierarchie abgerufen werden soll. |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Gruppen | JSON-Objekt-Array | Array von Gruppen mit der Liste der Untergruppen, falls vorhanden |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | Zeichenfolge | GUID der Gruppe zugeordnete |
| groupName | Zeichenfolge | Der Name der Gruppe |
| groupImageURL | Zeichenfolge | Zeichenfolge, die die URL des Bilds Profil Gruppe angibt. |

#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "subGroups": [
          {
            "groupName": "Sample sub group name",
            "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
            "groupImageUrl": "{sample sub group image URL here}",
          }
      ]
    }
  ]
}
```

## <a name="post-subgroups"></a>POST-/subGroups

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |

### <a name="request-body"></a>Anforderungstext

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| groupName | String | Nein | Der Name der Gruppe "Sub" |
| groupImageURL | String | Ja | Media-URL des Bilds Gruppe; Bild muss durch den Pfad /media hochgeladen werden |
| Elemente | Array | Ja | Zeichenfolgenarray gut formatierte Telefonnummern |
| welcomeMessage | Array | Nein | Zeichenfolgenarray gut formatierte Telefonnummern  |
| addUserToGroup | Boolean | Ja | Auf False festgelegt, wenn der Benutzer standardmäßig nicht der Gruppe hinzugefügt werden soll  |


#### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | Zeichenfolge | Gruppen-ID. |
| groupName | Zeichenfolge | Name der Gruppe erstellt |


#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
