---
title: /Actions
description: Referenzartikel für API zum Abrufen der Liste der Aktionen in einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 717b91d38ed43c85c3511de84538bb357e799f9b
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905331"
---
# <a name="get-list-of-actions-in-a-group"></a>Hier finden Sie die Liste der Aktionen in einer Gruppe
## <a name="get-actions"></a>Abrufen von /actions

    GET {endpoint-url}/v1/groups/{groupId}/actions?actionType={action_Type}

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| URL-Abfrageparameter | actionType | String | Nein | Typ der abzurufenden Aktion |
| URL-Abfrageparameter | fromDate | DateTime (Epoche Zeit) | Ja | Zeit aus der die Aktionen benötigte abgerufen werden sollen |
| URL-Abfrageparameter | count | number | Ja | Die Anzahl der einzelnen Aktionen zu zurückgegeben werden soll; Default = 30 |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Aktionen | JSON-Objekt-Array | Array von Action-Objekten |
| hasMore | Boolean | Wenn die maximale Anzahl von Aktionen pro Antwort erreicht hat, wird diese Variable festlegen auf "true" |

JSON-Struktur für jede einzelne Aktion in das Array Aktionen []:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | ReferenceID für die Nachricht |
| actionType | String | Typ der Aktion zurückgegeben wird |
| actionBody | JSON-Objekt-Array speziell für die actiontype | Array mit Objekten, die speziell für die actiontype |
| sender | String | Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet |
| sentAt | DateTime | Wenn die Aktion in der Gruppe veröffentlicht wurde Zeit |

####  <a name="actionbody-object-structure-for-imagepicture-attachment"></a>ActionBody Objektstruktur für Bild/Bild Anlage:

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| imageURL | String | URL-Zeichenfolge für das Bild |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
  "actions": [
    {
      "referenceId": "8a93c6cc-8499-44b0-aa54-016648100080",
      "actionType": "Image",
      "sender": "+9196500000",
      "creationTime": 1481180806,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg"
      }
    }
]
}
```

####  <a name="actionbody-object-structure-for-the-action-share-location"></a>ActionBody Objektstruktur für die Aktion "Speicherort freigeben":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| latitude | Double | Breitengradkoordinaten für den Speicherort |
| longitude | Double | Längengradkoordinaten für den Speicherort |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

#### <a name="actionbody-object-structure-for-the-action-photo-with-location"></a>ActionBody Objektstruktur für die Aktion 'Foto mit Speicherort':

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| imageURL | String | URL-Zeichenfolge für das Bild |
| latitude | Double | Breitengradkoordinaten für den Speicherort |
| longitude | Double | Längengradkoordinaten für den Speicherort |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg",
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

####  <a name="actionbody-object-structure-for-the-action-job"></a>ActionBody Objektstruktur für die Aktion "Job":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | String | GUID, die bestimmte Aktionsinstanz darstellt. |
| title | String | Titel des Auftrags |
| assigneeCount | Numerisch | Anzahl der "assignees" |
| responseCount | Numerisch | Anzahl der "assignees", die den Auftrag abgeschlossen gekennzeichnet haben |
| isCompleted | Boolean | True, wenn alle "assignees" den Auftrag abgeschlossen haben |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
  "actions": [
    {
      "referenceId": "3214841c-eaa2-4bf3-a583-acc69d9279c4",
      "actionType": "Job",
      "sender": "+919910005",
      "creationTime": 1481179788,
      "actionBody": {
        "actionId": "f260dc09-f1f3-4305-84f6-6edbedb82fb7",
        "title": "Test",
        "assigneeCount": 1,
        "responseCount": 0,
        "isCompleted": false
      }
    }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-poll"></a>ActionBody Objektstruktur für die Aktion "Umfrage":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | String | GUID, die bestimmte Aktionsinstanz darstellt. |
| question | String | Abstimmungsfrage |
| isSenderOnly | Boolean | True, wenn die Umfrage Zusammenfassung nur Absender angezeigt wird. |
| ExpiryDate. | DateTime | DateTime der Ablaufzeit der Umfrage |
| Choices | JSON-Array | Liste der Json-Objekte mit folgenden-Komponente <ol><li>Titel - Option Text</li><li>Bild - Option</li></ol> |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
    "actions": [
        {
            "referenceId": "d4753fdc-13fe-4162-a48f-5bf071bfd380",
            "actionType": "Poll",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:33:51Z",
            "actionBody": {
                "actionId": "27c7dbcf-48bb-4523-8273-d53a3da2343b",
                "question": "Do you find Kaizala extensibility easy to use?",
                "isSenderOnly": false,
                "expiryDate": "2017-12-20T18:33:51Z",
                "choices": [
                    {
                        "title": "Yes",
                        "image": "https://cdn.kascore.osi.office.net/75e8e7b63d2a4c10cdc30208aa27f1c2987d868a0e764fc742a94f6549d8bdb2.png?sv=2015-12-11&sr=b&sig=4iqswjFVYyqGqyKg6cdMdUQmiAez8sV951UScUmLzLk%3D&st=2017-05-17T07%3A04%3A41Z&se=2291-03-02T08%3A04%3A41Z&sp=r"
                    },
                    {
                        "title": "No"
                    },
                    {
                        "title": "Not at all"
                    }
                ]
            }
        }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-lets-meet"></a>ActionBody Objektstruktur für die Aktion 'Treffen wir uns':

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | String | GUID, die bestimmte Aktionsinstanz darstellt. |
| title | String | Titel der Besprechungsanfrage |
| isSenderOnly | Boolean | True, wenn die Umfrage Zusammenfassung nur Absender angezeigt wird. |
| duration | Ganzzahl | Dauer der Besprechung (in Minuten) |
| Tagesordnung | String | Legen Sie für die Besprechung Tagesordnung |
| startingTime | DateTime | DateTime der Ablaufzeit der Umfrage |
| Ort | JSON-Objekt | Standortdaten mit folgenden-Komponente <ol><li>Latitude</li><li>Longitude</li><li>name</li></ol> |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
    "actions": [
        {
            "referenceId": "32d1e5ad-36ff-4237-a49c-4be95a10cd12",
            "actionType": "LetsMeet",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:55:04Z",
            "actionBody": {
                "actionId": "3c80f0f1-2b2f-460a-b760-ec10adb7dbb1",
                "title": "lets catch up?",
                "startingTime": "2018-01-01T00:00:00Z",
                "agenda": "no agenda",
                "duration": 30,
                "isSenderOnly": false,
                "place": {
                    "latitude": 15,
                    "longitude": 96,
                    "name": "MS Building 3"
                }
            }
        }
  ]
}
```


####  <a name="actionbody-object-structure-for-the-action-survey"></a>ActionBody Objektstruktur für die Aktion "Umfrage":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | String | GUID, die bestimmte Aktionsinstanz darstellt. |
| title | String | Titel der Umfrage |
| responseCount | Numerisch | Anzahl der Personen, die auf die Umfrage geantwortet |
| ExpiryDate. | DateTime | DateTime der Ablaufzeit der Umfrage |

##### <a name="sample-json-response"></a>Beispiel JSON-Antwort:

```javascript
{
  "actions": [
    {
      "referenceId": "88a93ddd-0349d-4d18-86ee-c0f8484728db",
      "actionType": "Survey",
      "sender": "+91960000",
      "creationTime": 1480931759,
      "actionBody": {
        "actionId": "8106b2bb-236c-4952-a554-2baadcbd49a0",
        "title": "Sample Survey",
        "responseCount": 1
      }
    }
]
}
```

Als Nächstes folgt: Sie können weitere Details jeder Aktion-Instanz mit den entsprechenden ActionId abrufen. [API zum Abrufen von Action Instanzdetails](actionDetails.md)
