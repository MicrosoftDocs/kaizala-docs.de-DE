---
title: /Reaction
description: Referenzartikel zur API zum Abfragen von Reaktionen auf alle in einer Gruppe gesendeten Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: a0c86aac9dd70e4c72e177f64c6e2dcaeeb8b41c
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33191302"
---
# <a name="reaction"></a>/Reaction
API-Endpunkt zum Abfragen von Reaktions Daten für alle in einer Gruppe gesendeten Aktionen.

## <a name="post-reaction"></a>POST/Reaction

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a>AnforderungsParameter

| | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---  | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/JSON |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| referenceId | String | Nein | GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt |
| sourceGroupId | String | Nein | GUID der Gruppe, in der die Aktion gesendet wurde. Bei Gruppen, bei denen es sich um eine Untergruppe einer anderen Gruppe handelt, kann dies von der im URL-Pfad-Parameter angegebenen Gruppierung|
| reactiontype | String | Nein | Enumerationswert: ' like '/' Comment '|
| comment | String | Nein | Kommentartext ist nur für reactiontype "comment" obligatorisch. Für "like" sollte dies ignoriert werden. |

#### <a name="sample-json-request"></a>JSON-Beispielanforderung

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Reaction-Nr. | String | GUID, die die ID der Reaktions Entität nach erfolgreichem Abschluss der Anforderung darstellt |

#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a>/Reaction-Zusammenfassung auf Aktionsebene abrufen

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| URL-Pfad Parameter | referenceId | String | Nein | GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt |
| URL-Pfad Parameter | sourceGroupId | String | Nein | GUID der Gruppe, in der die Aktion gesendet wurde. |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Zusammenfassung | JSON-Array | Array von JSON-Objekten, die die Zusammenfassung der Reaktionen für eine in einer Gruppe gesendete Aktion darstellen |

### <a name="response-body-summary-object"></a>Antworttext-Zusammenfassungs Objekt

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt |
| reactionsCountMap | JSON-Objekt | JSON-Objekt mit likes-und comments-Anzahl für diesen Verweistyp |


### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "summary": [
        {
            "referenceId": "4a44e62e-4b42-a980-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 1,
                "comment": 4
            }
        }
    ]
}
```

## <a name="get-reaction-summary-at-group-level"></a>/Reaction-Zusammenfassung auf Gruppenebene abrufen

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| URL-Pfad Parameter | sourceGroupId | String | Nein | GUID der Gruppe, in der die Aktion gesendet wurde. |
| URL-Pfad Parameter | Cursor | Zeitstempel | Nein | Zeitstempel, aus dem die Zusammenfassung berechnet werden muss. Standardwert 0 |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Cursor | Zeitstempel | Zeitstempel, bis die Zusammenfassung berechnet wurde. Nächster Satz von reactionSummary kann mit diesem Cursor Wert generiert werden. |
| Zusammenfassung | JSON-Array | Array von JSON-Objekten, die die Zusammenfassung der Reaktionen für eine in einer Gruppe gesendete Aktion darstellen |

#### <a name="response-body-summary-object"></a>Antworttext-Zusammenfassungs Objekt

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | String | GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt |
| reactionsCountMap | JSON-Objekt | JSON-Objekt mit likes-und comments-Anzahl für diesen Verweistyp |


#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "cursor": 636674054802000000,
    "summary": [
        {
            "referenceId": "4a44-51be-4b42-a980-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 1,
                "comment": 4
            }
        },
        {
            "referenceId": "4a44-51be-4b420-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 10,
                "comment": 14
            }
        }
    ]
}
```

## <a name="get-reaction-details-for-a-action"></a>Abrufen von/Reaction-Details für eine Aktion

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| URL-Pfad Parameter | sourceGroupId | String | Nein | GUID der Gruppe, in der die Aktion gesendet wurde. |
| URL-Pfad Parameter | referenceId | String | Nein | GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt |
| URL-Pfad Parameter | reactiontype | String | Nein | Enumerationswert: ' like '/' Comment '|
| URL-Pfad Parameter | Cursor | Zeitstempel | Nein | Zeitstempel, aus dem die Zusammenfassung berechnet werden muss. Standardwert 0 |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Cursor | Zeitstempel | Zeitstempel, bis zu dem reactionDetail bereitgestellt wurde. Nächster Satz von reactionDetails kann mit diesem Cursor Wert generiert werden. |
| reactionDetails | JSON-Array | Array von JSON-Objekten, die alle Reaktionen auf eine in einer Gruppe gesendete Aktion darstellen. |

#### <a name="response-body-summary-object"></a>Antworttext-Zusammenfassungs Objekt

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Reaction-Nr. | String | GUID, die die ID für die Reaktion darstellt, die auf einer Referenz erstellt wurde, die eine Aktion darstellt |
| userId | JSON-Objekt | UserId für den Benutzer, der die Reaktion auf eine Aktion erstellt hat |
| lastModifiedTime | Zeitstempel | Zeitstempel, an dem die Reaktion erstellt/aktualisiert wurde |


#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "cursor": 636674054802000000,
    "reactionDetails": [
        {
            "lastModifiedTime": 1529573303063,
            "reactionId": "4b2fb78b-b529-4fa1-acda-f670b491ebca",
            "userId": "72e29591-f391-4e7b-84eb-4e228406fb9b"
        },
        {
            "lastModifiedTime": 1529573313063,
            "reactionId": "4b2fb7529-4fa1-acda-f670b491ebca",
            "userId": "72e29591-f391-4eb-4e228406fb9b"
        }
    ]
}
```