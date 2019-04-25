---
title: /Groups
description: Referenzartikel für API zum Abfragen von Gruppendaten
topic: Reference
author: nitinjms
ms.openlocfilehash: 6a0b56d36aef458b5a3d302235499f445ed134e6
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190716"
---
# <a name="groups"></a>/Groups
API-Endpunkt für die Interaktion mit den unterhaltungsgruppen in Kaizala.

## <a name="post-groups"></a>POST/Groups

    Post {endpoint-url}/v1/groups

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | "application/json" |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| name | String | Nein | Name der Gruppe |
| welcomeMessage | String | Nein | Willkommensnachricht, die dem neuen Gruppenmitglied angezeigt wird |
| members | String [] | Ja | Mobiltelefonnummer (mit Landesvorwahl) der hinzuzufügenden Mitglieder. Standard: der Benutzer des Zugriffstokens wird als Administrator der Gruppe hinzugefügt. |
| groupType | Zeichenfolge | Ja | Enum: Group/Connectgroup. Connectgroup erstellt eine verwaltete öffentliche Gruppe. Standard: Gruppe |

#### <a name="sample-json-request-for-create-group"></a>JSON-Beispielanforderung für Create Group

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupName | String | Name der Gruppe |
| groupId | Zeichenfolge | Gruppenbezeichner, der bei nachfolgenden API-Aufrufen verwendet werden kann |
| membersAdded | bool | True, wenn alle Elemente erfolgreich hinzugefügt werden |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


## <a name="get-groups"></a>/Groups abrufen

    GET {endpoint-url}/v1/groups

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| Abfrageparameter | showDetail | bool | Ja | Standard: false. True, um alle Gruppendetails zurückzugeben |
| Abfrageparameter | fetchAllGroups | bool | Ja | Standard: false. True, um alle über-und Untergruppen zurückzugeben |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groups | JSON-Objekt Array | Array von Gruppen, auf die der Benutzer mit der Access Token zugreifen kann |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a>JSON-Struktur für jede einzelne Gruppe in den Array Gruppen []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | Zeichenfolge | Gruppenbezeichner |
| groupName | String | Der Name der Gruppe |
| groupImageURL | String | Zeichenfolge, die die URL des Gruppenprofil Bilds angibt |
| hasSubGroups | bool | True, wenn die Gruppe Untergruppen hat |
| hasParentGroups | bool | True, wenn die Gruppe übergeordnete Gruppen hat |
| isMappedToTenant | bool | True, wenn die Gruppe Organisationsgruppe ist |
| groupType | String | Group/Connectgroup. Connectgroup wenn die Gruppe in verwalteter öffentlicher Gruppe |
| userCount | Numeric | Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie |
| currentLevelUserCount | Numeric | Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

## <a name="get-groupsgroupid"></a>/Groups/{groupId} abrufen

Sie können Details zu einem bestimmten Resource-Element (eine Gruppe hier) abrufen, indem Sie den Bezeichner als URL-Pfadparameter angeben.

    GET {endpoint-url}/groups/{groupId}

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groups | JSON-Objekt Array | Array von Gruppen, auf die der Benutzer mit der Access Token zugreifen kann |

JSON-Struktur für jede einzelne Gruppe in den Array Gruppen []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| groupId | Zeichenfolge | Gruppenbezeichner |
| groupName | String | Der Name der Gruppe |
| groupImageURL | String | Zeichenfolge, die die URL des Gruppenprofil Bilds angibt |
| hasSubGroups | bool | True, wenn die Gruppe Untergruppen hat |
| hasParentGroups | bool | True, wenn die Gruppe übergeordnete Gruppen hat |
| isMappedToTenant | bool | True, wenn die Gruppe Organisationsgruppe ist |
| groupType | String | Group/Connectgroup. Connectgroup wenn die Gruppe in verwalteter öffentlicher Gruppe |
| userCount | Numeric | Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie |
| currentLevelUserCount | Numeric | Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

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

