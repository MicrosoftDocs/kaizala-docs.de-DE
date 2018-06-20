---
title: /subGroups
description: Referenzartikel für Abfragen Untergruppe von Daten-API
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6d013b4d6657eaaaadb9fe3244c2d9383e56f6
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905328"
---
# <a name="apis-to-query-subgroups-within-a-group"></a>APIs für die Abfrage Untergruppen innerhalb einer Gruppe
## <a name="subgroups"></a>/subGroups
API-Endpunkt zur Interaktion mit der Unterhaltung Unterseite innerhalb Kaizala gruppiert.

### <a name="get-subgroups"></a>Abrufen von /subGroups

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Abfrageparameter | fetchAllGroups | Boolean | Ja | Parameter, um anzugeben, wenn alle Untergruppen in der Hierarchie abgerufen werden soll. |

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Gruppen | JSON-Objekt-Array | Array von Gruppen mit der Liste der Untergruppen, falls vorhanden |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | String | GUID der Gruppe zugeordnete |
| groupName | String | Der Name der Gruppe |
| groupImageURL | String | Zeichenfolge, die die URL des Bilds Profil Gruppe angibt. |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

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

### <a name="post-subgroups"></a>POST-/subGroups

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |

##### <a name="request-body"></a>Anforderungstext

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| groupName | String | Nein | Der Name der Gruppe "Sub" |
| groupImageURL | String | Ja | Media-URL des Bilds Gruppe; Bild muss durch den Pfad /media hochgeladen werden |
| Elemente | Array | Ja | Zeichenfolgenarray gut formatierte Telefonnummern |
| welcomeMessage | Array | Nein | Zeichenfolgenarray gut formatierte Telefonnummern  |
| addUserToGroup | Boolean | Ja | Auf False festgelegt, wenn der Benutzer standardmäßig nicht der Gruppe hinzugefügt werden soll  |


###### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | String | Gruppen-ID. |
| groupName | String | Name der Gruppe erstellt |


###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
