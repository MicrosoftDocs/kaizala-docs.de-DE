---
title: /Actions_post
description: Referenzartikel zur API zur Post-Aktion in einer Kaizala-Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 8a5e6e3c4d2f294e7c507e661ec8e5df7c717ec6
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535776"
---
# <a name="post-a-action-in-a-group"></a>Posten einer Aktion in einer Gruppe
## <a name="post-actions"></a>Post/Actions

    POST {endpoint-url}/groups/{groupId}/actions

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | Gruppenbezeichner |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/JSON |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| id | Zeichenfolge | ID des Kaizala-Aktionspakets. Entweder von Action Type oder ID sollte angegeben werden |
| actionType | String | Enum "Survey"/"Job". Entweder von Action Type oder ID sollte angegeben werden |
| actionBody | JSON-Objekt | Objekt, das für die jeweilige Aktion erforderliche Daten darstellt. Für jede der unterstützten Aktionen definierte Parameter. |


#### <a name="actionbody-for-an-announcement-action"></a>actionBody für eine Ankündigungs Aktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Ansage |
| MediaResources | String [] | Ja | Array von Medienressourcen |
| Nachricht | String | Nein | Nachrichtentext |

#### <a name="sample-json-request-for-an-announcement-action"></a>JSON-Beispielanforderung für eine Ankündigungs Aktion

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

#### <a name="actionbody-for-a-job-action"></a>actionBody für eine Auftragsaktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel des Auftrags |
| assignedTo | String [] | Nein | Titel des Auftrags |
| DueDate | long | Ja | Standard: 24 Stunden. Anzahl der Stunden vor dem Abschluss des Auftrags |

##### <a name="sample-json-request-for-a-job-action"></a>JSON-Beispielanforderung für eine Auftragsaktion

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

#### <a name="actionbody-for-a-poll-action"></a>actionBody für eine Abfrage Aktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| Frage | String | Nein | Umfrage Frage |
| Auswahlmöglichkeiten | JSON-Array | Nein | Verfügbare Auswahlmöglichkeiten für die Umfrage. Jede Auswahl ist Unterkomponente: <ol><li>Title (obligatorisch #a0 im Zeichenfolgenformat) </li><li>Image (optional)</li></ol> |
| expiryInHours | Ganze Zahl | Ja | Standard: 720. Anzahl der Stunden, in denen eine bestimmte Umfrage ablaufen würde |

##### <a name="sample-json-request-for-a-poll-action"></a>JSON-Beispielanforderung für eine Abfrage Aktion

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
#### <a name="actionbody-for-a-lets-meet-action"></a>actionBody für eine Let es Meet-Aktion

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Besprechungsanfrage  |
| Startzeit | DateTime | Nein | Startzeit für die Besprechung |
| DurationInMins | Ganze Zahl | Nein | Standard: 30 Minuten. Anzahl der Minuten, für die eine Besprechung durchgeführt wurde |
| Ort | JSON-Objekt | Ja | Besprechungs Standort. Enthält 3 Komponenten: Latitude, Längengrad, Name  |
| Agendas | String | Ja | Agenda für die Besprechung/Beschreibung für die Besprechung |
| isSenderOnly | Boolescher Wert | Ja | Damit nur Absender die Zusammenfassung von Let es Meet anzeigen können. Standard: false |

##### <a name="sample-json-request-for-a-lets-meet-action"></a>JSON-Beispielanforderung für eine Let es Meet-Aktion

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a>actionBody für eine Umfrageaktion oder eine Aktionspaket Instanz (ID):

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel des Auftrags |
| DueDate | long | Ja | Standard: 24 Stunden. Anzahl der Stunden vor dem Abschluss des Auftrags |
| isAnonymous | Boolescher Wert | Ja | Für das zulassen anonymer Umfrage Antworten. Standard: false |
| isSenderOnly | Boolescher Wert | Ja | Für die Möglichkeit, dass nur Absender die Umfragezusammenfassung anzeigen können. Standard: false |
| acceptMultipleResponses | Boolescher Wert | Ja | Für das Zulassen mehrerer Antworten von demselben Responder. Standard: false |
| Fragen | object[] | Nein | Jedes Element von Object [] wird im folgenden als Question-Objekt beschrieben. |
| properties | object[] | Nein | Jedes Element von Object [] wird im folgenden als Property-Objekt beschrieben. Nur gültig zum Erstellen einer Aktionspaket Instanz |

##### <a name="structure-for-question-object"></a>Struktur für Question-Objekt

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Frage |
| type | Zeichenfolge | Nein | Der Typ der Frage. Enumeration: SingleOption/multioption/Text/Image/numerisch/Datum/Ort/Anlage Liste |
| isunsichtbar | Boolescher Wert | Ja | Default: false. So steuern Sie die Sichtbarkeit der Frage |
| options | object[] | Ja | Obligatorisch für SingleOption und multioption-Fragentyp. jedes Element von Object [] wird im folgenden als Optionsobjekt beschrieben. |

###### <a name="structure-for-option-object"></a>Struktur für Optionsobjekt

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| title | String | Nein | Titel der Option |

###### <a name="structure-for-property-object"></a>Struktur für Property-Objekt

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| name | Zeichenfolge | Nein | Name der Eigenschaft |
| type | String | Nein | Typ der Eigenschaft. Enum: Text, numeric, Location, DateTime, stringlist, Attachment, stringset, attachmentlist |
| value | String | Nein | Wert der Eigenschaft |

##### <a name="sample-json-request-for-a-survey-action"></a>JSON-Beispielanforderung für eine Umfrageaktion

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

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | Anforderungs-ID |
| actionId | String | Aktions-ID |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
