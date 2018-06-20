---
title: / Actions_post
description: Referenzartikel für API-Aktion auf einer Gruppe Kaizala bereitstellen
topic: Reference
author: nitinjms
ms.openlocfilehash: 015a60bbef7be7108cc0edc10e81cc1f8b5636e2
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905329"
---
# <a name="post-a-action-in-a-group"></a>Eine Aktion nach der in einer Gruppe
### <a name="post-actions"></a>POST-/actions

    POST {endpoint-url}/groups/{groupId}/actions

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | Gruppen-ID. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/Json |

##### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| id | String | ID des Pakets Kaizala Aktion. Entweder ActionType oder Id muss angegeben werden |
| actionType | String | Enumeration "Umfrage" / "Job". Entweder ActionType oder Id muss angegeben werden |
| actionBody | JSON-Objekt | Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt. Parameter für die einzelnen unterstützten Aktionen beschrieben. |


###### <a name="actionbody-for-an-announcement-action"></a>ActionBody für eine Ankündigung-Aktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Ankündigung |
| MediaResources | String] | Ja | Array von Medienressourcen |
| Nachricht | String | Nein | Nachrichtentext |

###### <a name="sample-json-request-for-an-announcement-action"></a>Beispiel für eine Anforderung für eine Aktion Ankündigung JSON

```javascript
{
  "actionType" : "Announcement",
  "actionBody" : 
  {
    "Message":"Announcement from API Message text",
    "Title" : "Title text", 
    "MediaResources" : 
    [
      "eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNV","eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VE"
    ]
  }
}

```

###### <a name="actionbody-for-a-job-action"></a>ActionBody für eine Auftrags-Aktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel des Auftrags |
| assignedTo | String] | Nein | Titel des Auftrags |
| dueDate | long | Ja | Standard: 24 Stunden. Anzahl der Stunden, die vor denen Auftrag ausgeführt werden soll |

###### <a name="sample-json-request-for-a-job-action"></a>Beispiel für eine Anforderung für eine Aktion Auftrag JSON

```javascript
{
    actionType:"Job",
    actionBody: {
        title : "test job",
        assignedTo : ["+911111111111", "+911111111112"],
        dueDate : 10
    }
}

```

###### <a name="actionbody-for-a-poll-action"></a>ActionBody für eine Aktion eines Abrufs

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| question | String | Nein | Abstimmungsfrage |
| Choices | JSON-Array | Nein | Optionen für die Umfrage zur Verfügung. Jede Auswahl werden unter Komponente: <ol><li>Titel (obligatorisch & im Zeichenformat) </li><li>Bild (optional)</li></ol> |
| expiryInHours | Ganzzahl | Ja | Standard: 720. Anzahl der Stunden, in denen eine Umfrage Gven abläuft |

###### <a name="sample-json-request-for-a-poll-action"></a>Beispiel für eine Anforderung für eine Aktion Umfrage JSON

```javascript
{actionType:"Poll", actionBody:{question:"Do you find Kaizala extensibility easy to use?", 
    choices:
        [
        {title:"Yes",image:"eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNVcFRWRlZXVjFoWldtTmtaV1puYUdscWMzUjFkbmQ0ZVhxRGhJV0doNGlKaXBLVGxKV1dsNWlabXFLanBLV21wNmlwcXJLenRMVzJ0N2k1dXNMRHhNWEd4OGpKeXRMVDFOWFcxOWpaMnVIaTQrVGw1dWZvNmVyeDh2UDA5ZmIzK1BuNi84UUFId0VBQXdFQkFRRUJBUUVCQVFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSRUFBZ0VDQkFRREJBY0ZCQVFBQVFKM0FBRUNBeEVFQlNFeEJoSkJVUWRoY1JNaU1vRUlGRUtSb2JIQkNTTXpVdkFWWW5MUkNoWWtOT0VsOFJjWUdSb21KeWdwS2pVMk56ZzVPa05FUlVaSFNFbEtVMVJWVmxkWVdWcGpaR1ZtWjJocGFuTjBkWFozZUhsNmdvT0VoWWFIaUltS2twT1VsWmFYbUptYW9xT2twYWFucUttcXNyTzB0YmEzdUxtNndzUEV4Y2JIeU1uSzB0UFUxZGJYMk5uYTR1UGs1ZWJuNk9ucTh2UDA5ZmIzK1BuNi85b0FEQU1CQUFJUkF4RUFQd0N4UlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVsQUMwVW1hTTByZ0xSU1pvelJjQmFLVE5HYUxnTFJTWm96UmNCYUtUTkdhTGdMUlNab3pSY0JhS1ROR2FMb0JhS0tLWUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSWVsTFNIcFNld0MwVVVVd0NpaWs3MEFMUlNZb3hTMUFXaWt4UmlqVUJhS1RGR0tOUUZvcE1VWW8xQVdrUFNqRkJIRkR2WUJhS1RGR0tOUUZvcE1VWW8xQVdpa3hSaWpVQmFLVEZHS05RRm9wQlMwd0NpaWlnQW9vb29BS0tLS0FDaWlpZ0FwRDBwYVE5S1QyQVdpaWltQVVuZWxwTzlJQmFLS0tZQlJSUlFBVVVVVUFGRkZGQUJTSHBTMGg2VW5zQXRGRkZNQW9vb29BS0tLS0FDaWlpZ0JPOUxTZDZXa2dDaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFKaWpGTFJTc2dFeFJpbHBPOUZrQVlveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQlJSUlRBS0tLS0FDaWlpZ0Fvb29vQVR2UzBuZWxwSUFvb29wZ0ZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVuZWxwTzlMc0F0RkZGTUFvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FFNzB0SjNwYVNBS0tLS1lCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSjNwYVR2U0FXaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFDZDZXazcwdEpBRkZGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDa3BhS0FFeFJpbG9wV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDVXRGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdELzlrPSIsIkFjdGlvblR5cGUiOjMsIkZpbGVzIjpbeyJJZCI6ImU1Y2YyMWJmLWQ3OGItNGY4Yi1iYjY3LTM2NTJlNDk1ZDEyZSIsIk5hbWUiOiJ0ZXN0LnBuZyIsIlNpemUiOjQsIlVybCI6Imh0dHBzOi8vY2RuLmthc2NvcmUub3NpLm9mZmljZS5uZXQvNzVlOGU3YjYzZDJhNGMxMGNkYzMwMjA4YWEyN2YxYzI5ODdkODY4YTBlNzY0ZmM3NDJhOTRmNjU0OWQ4YmRiMi5wbmc/c3Y9MjAxNS0xMi0xMSZzcj1iJnNpZz00aXFzd2pGVll5cUdxeUtnNmNkTWRVUW1pQWV6OHNWOTUxVVNjVW1MekxrJTNEJnN0PTIwMTctMDUtMTdUMDclM0EwNCUzQTQxWiZzZT0yMjkxLTAzLTAyVDA4JTNBMDQlM0E0MVomc3A9ciJ9XX0="},
        {title:"No"},
        {title:"Not at all"}
        ],
    expiryInHours:10}}
```
###### <a name="actionbody-for-a-lets-meet-action"></a>ActionBody für eine wir erfüllen Aktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Besprechungsanfrage  |
| startingTime | DateTime | Nein | Die Startzeit für die Besprechung |
| DurationInMins | Ganzzahl | Nein | Standard: 30 Minuten. Anzahl der Minuten für die eine Besprechung durchgeführt werden würde |
| Platzieren | JSON-Objekt | Ja | Speicherort der Besprechung. 3-Komponenten enthält: Breitengrad, Längengrad, Name  |
| Tagesordnung | String | Ja | Tagesordnung für die Besprechung / Beschreibung für die Besprechung |
| isSenderOnly | Bool | Ja | Für das Zulassen nur Absender treffen wir uns Zusammenfassung anzeigen. Standard: false |

###### <a name="sample-json-request-for-a-lets-meet-action"></a>Beispiel von JSON-Anforderung für eine treffen wir uns Aktion

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

###### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a>ActionBody für eine Umfrage oder-Aktion Paket instance(id):

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel des Auftrags |
| dueDate | long | Ja | Standard: 24 Stunden. Anzahl der Stunden, die vor denen Auftrag ausgeführt werden soll |
| isAnonymous | Bool | Ja | Für anonyme Umfrageantworten zulassen. Standard: false |
| isSenderOnly | Bool | Ja | Für das Zulassen nur Absender Umfrage Zusammenfassung anzeigen. Standard: false |
| acceptMultipleResponses | Bool | Ja | Mehrere Antworten von den gleichen Responder zulässt. Standard: false |
| Fragen | object[] | Nein | Jedes Element des Object [] wird als Objekt "Question" unten erläutert. |
| properties | object[] | Nein | Jedes Element des Object [] wird als Property-Objekt unten beschrieben. Nur gültig für das Paket Aktionsinstanz erstellen |

###### <a name="structure-for-question-object"></a>Struktur für Objekt "Question"

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Frage |
| Typ | String | Nein | Typ der Frage. Enum: SingleOption/MultiOption/Text/Image/numerischen/Datum/Speicherort/AttachmentList |
| isInvisible | Bool | Ja | Standard: false. Um die Sichtbarkeit der Frage steuern |
| options | object[] | Ja | Obligatorisch für SingleOption und MultiOption Frage. jedes Element des Object [] wird als Optionsobjekt unten beschrieben. |

###### <a name="structure-for-option-object"></a>Struktur für Option-Objekt

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Option |

###### <a name="structure-for-property-object"></a>Struktur für Property-Objekt

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| name | String | Nein | Name der Eigenschaft |
| Typ | String | Nein | Typ der Eigenschaft. Enum: Text, Numeric, Position, DateTime, StringList, Attachment, StringSet, AttachmentList |
| Wert | String | Nein | Wert der Eigenschaft |

###### <a name="sample-json-request-for-a-survey-action"></a>Beispiel für eine Anforderung für eine Aktion Umfrage JSON

```javascript
{
  actionType: "Survey",
  actionBody: {
    isAnonymous:false,
    isSenderOnly:false,
    acceptMultipleResponses:true,
    dueDate:10,
    title: "A test survey!!",
    questions: [
        {
            title: "a test question written here",
            type: "Text"
        },
        {
            title: "Single select question",
            type: "SingleOption",
            options: [{title:"Opt1"},{title:"Opt2"}]
        },
        {
            title: "Multi select question",
            type: "MultiOption",
            options: [{title:"MOpt1"},{title:"MOpt2"},{title:"MOpt3"}]
        },
        {
            title: "Numeric question",
            type: "Numeric"
        },
        {
            title: "Location question",
            type: "Location"
        },
        {
            title: "DateTime question",
            type: "DateTime"
        },
        {
            title: "Image question",
            type: "Image"
        }
        ]
  }
}
```

###### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | Anforderungsbezeichner |
| actionId | String | Aktionsbezeichner |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
