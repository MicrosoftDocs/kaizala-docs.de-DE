---
title: /subGroups
description: Referenzartikel zur API zum Abfragen von Untergruppen Daten
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190688"
---
# <a name="subgroups"></a>/subGroups
API-Endpunkt für die Interaktion mit den Unterhaltungs-Untergruppen innerhalb von Kaizala.

## <a name="get-subgroups"></a>/SubGroups abrufen

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| URL-Abfrage Parameter | fetchAllGroups | Boolean | Ja | Parameter, mit dem angegeben wird, ob alle Untergruppen in der Hierarchie abgerufen werden sollen |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groups | JSON-Objekt Array | Array von Gruppen mit der Liste der Untergruppen, falls vorhanden |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>JSON-Struktur für jede einzelne Gruppe in den Array Gruppen []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | Zeichenfolge | Der Gruppe zugeordnete GUID |
| groupName | String | Der Name der Gruppe |
| groupImageURL | String | Zeichenfolge, die die URL des Gruppenprofil Bilds angibt |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

## <a name="post-subgroups"></a>POST/subGroups

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |

### <a name="request-body"></a>Anforderungstext

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| groupName | String | Nein | Name der Untergruppe |
| groupImageURL | Zeichenfolge | Ja | Medien-URL des Gruppen Bilds; Das Bild muss über den/Media-Pfad hochgeladen werden. |
| members | Array | Ja | Zeichenfolgenarray von formatierten Telefonnummern |
| welcomeMessage | Array | Nein | Zeichenfolgenarray von formatierten Telefonnummern  |
| addUserToGroup | Boolean | Ja | Wird auf false festgelegt, wenn der aufrufende Benutzer standardmäßig nicht der Gruppe hinzugefügt werden soll.  |


#### <a name="sample-json-request"></a>JSON-Beispielanforderung

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
| groupId | Zeichenfolge | Gruppenbezeichner |
| groupName | String | Name der erstellten Gruppe |


#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
