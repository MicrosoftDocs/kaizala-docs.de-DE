---
title: Locations
description: Referenzartikel für API zum Abfrage Gruppieren von Daten
topic: Reference
author: nitinjms
ms.openlocfilehash: 010d6d30c72355e2575cda2f8104316a5a770ac4
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905341"
---
# <a name="apis-to-query-kaizala-groups"></a>APIs für die Abfrage Kaizala Gruppen
## <a name="groups"></a>Locations
Interaktion mit der Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.

### <a name="post-groups"></a>POST-Locations

    Post {endpoint-url}/v1/groups

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | "Application/Json" |

##### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| name | String | Nein | Gruppenname |
| welcomeMessage | String | Nein | Willkommensnachricht das neue Mitglied der Gruppe angezeigt wird |
| Elemente | String] | Ja | Die Mobiltelefonnummer (mit Ländercode) Mitglieder hinzugefügt werden soll. Standard: Zugangs-Token Benutzer wird als Administrator der Gruppe hinzugefügt werden |
| groupType | String | Ja | Enum: Gruppe/ConnectGroup. ConnectGroup werden verwaltete öffentliche Gruppe erstellen. Standard: Gruppe |

###### <a name="sample-json-request-for-create-group"></a>Beispiel für eine Anforderung für JSON Gruppe erstellen

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupName | String | Gruppenname |
| groupId | String | Gruppen-ID, die im weiteren API-Aufrufe verwendet werden können |
| membersAdded | bool | True, wenn alle Mitglieder sind erfolgreich hinzugefügt. |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


### <a name="get-groups"></a>Abrufen von Locations

    GET {endpoint-url}/v1/groups

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| Abfrageparameter | showDetail | bool | Ja | Standard: false. True, wenn Return Gruppe alle details |
| Abfrageparameter | fetchAllGroups | bool | Ja | Standard: false. True zurück, um alle übergeordneten und sub-Gruppen |

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Gruppen | JSON-Objekt-Array | Array von Gruppen, dass der Benutzer Zugriff auf mit der AccessToken hat. |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | String | Gruppen-ID. |
| groupName | String | Der Name der Gruppe |
| groupImageURL | String | Zeichenfolge, die die URL des Bilds Profil Gruppe angibt. |
| hasSubGroups | bool | True, wenn die Gruppe Untergruppen besitzt. |
| hasParentGroups | bool | True, wenn die Gruppe verfügt über die übergeordneten Gruppen |
| isMappedToTenant | bool | True, wenn die Gruppe Organisation Gruppe ist |
| groupType | String | Gruppe/ConnectGroup. ConnectGroup Wenn die Gruppe in der Gruppe Public verwaltet |
| userCount | Numerisch | Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie |
| currentLevelUserCount | Numerisch | Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": false,
      "hasParentGroups": false,
      "callerRole": "Admin",
      "currentLevelSubGroupCount": 0,
      "currentLevelParentGroupCount": 0,
      "userCount": 2,
      "uniqueUserCount": 0,
      "currentLevelUserCount": 2,
      "currentLevelUnProvisionedUserCount": 0,
      "unProvisionedUserCount": 0,
      "isMappedToTenant": false,
      "groupType": "Group",
      "isDuplicate": false,
      "isEditable": true,
      "isDetailsReadable": true
    }
  ]
}
```

### <a name="get-groupsgroupid"></a>Abrufen von /groups/ {GroupId}

Sie können die Details zu einer bestimmten Ressource Member (hier eine Gruppe) abrufen, indem der Bezeichner als URL Path-Parameter angeben

    GET {endpoint-url}/groups/{groupId}

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Gruppen | JSON-Objekt-Array | Array von Gruppen, dass der Benutzer Zugriff auf mit der AccessToken hat. |

JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | String | Gruppen-ID. |
| groupName | String | Der Name der Gruppe |
| groupImageURL | String | Zeichenfolge, die die URL des Bilds Profil Gruppe angibt. |
| hasSubGroups | bool | True, wenn die Gruppe Untergruppen besitzt. |
| hasParentGroups | bool | True, wenn die Gruppe verfügt über die übergeordneten Gruppen |
| isMappedToTenant | bool | True, wenn die Gruppe Organisation Gruppe ist |
| groupType | String | Gruppe/ConnectGroup. ConnectGroup Wenn die Gruppe in der Gruppe Public verwaltet |
| userCount | Numerisch | Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie |
| currentLevelUserCount | Numerisch | Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene |

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": true,
      "userCount": 200,
      "currentLevelUserCount": 10
    }
  ]
}
```

