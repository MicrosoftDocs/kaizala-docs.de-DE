---
title: /Reaction
description: Referenzartikel für Reaktionen auf eine beliebige Aktion in einer Gruppe gesendet Abfrage-API
topic: Reference
author: nitinjms
ms.openlocfilehash: 4f2da7302133371dba5edd6035a57068e16aae63
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20425632"
---
# <a name="reaction"></a>/Reaction
API-Endpunkt auf Abfrage Reaktionen Daten für alle Aktionen, die in einer Gruppe gesendet.

## <a name="post-reaction"></a>POST-/reaction

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a>Anforderungsparameter

| | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---  | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/Json |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :--- | :--- |
| referenceId | String | Nein | GUID, die die Id für die Entitätsverweis für eine Aktion darstellt. |
| sourceGroupId | String | Nein | Die GUID der Gruppe in der die Aktion gesendet wurde. Im Fall eines WAN-Gruppen, die eine Untergruppe einer anderen Gruppe ist, kann dies von 'GroupId' in der Url bereitgestellt abweichen Path-Parameter|
| reactionType | String | Nein | Enum-Wert: 'Like "/" abgeben'|
| comment | String | Nein | Kommentartext ist nur für ReactionType 'Comment' obligatorisch. Für sollen "Like" dies ignoriert werden |

#### <a name="sample-json-request"></a>Beispiel für JSON-Anforderung

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
| reactionId | Zeichenfolge | GUID, die die Id für Reaktion Entität nach dem erfolgreichen Abschluss der Anforderung darstellt. |

#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a>/Reaction Aktion Ebene Zusammenfassung abrufen

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Pfad-Parameter | referenceId | String | Nein | GUID, die die Id für die Entitätsverweis für eine Aktion darstellt. |
| URL-Pfad-Parameter | sourceGroupId | String | Nein | Die GUID der Gruppe, in der die Aktion gesendet wurde |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Zusammenfassung | JSON-Array | Array von JSON-Objekten jede Ereignisobjekten Reaktionen Zusammenfassung auf eine Aktion, die in einer Gruppe gesendet werden. |

### <a name="response-body-summary-object"></a>Zusammenfassung Antwort Body-Objekt

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | Zeichenfolge | GUID, die die Id für die Entitätsverweis für eine Aktion darstellt. |
| reactionsCountMap | JSON-Objekt | Mit "gefällt mir" und Kommentare Count für diese ReferenceId JSON-Objekt |


### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

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

## <a name="get-reaction-summary-at-group-level"></a>Abrufen einer Zusammenfassung /reaction auf Gruppenebene

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Pfad-Parameter | sourceGroupId | String | Nein | Die GUID der Gruppe, in der die Aktion gesendet wurde |
| URL-Pfad-Parameter | Cursor | Zeitstempel | Nein | Zeitstempel, aus denen die Zusammenfassung berechnet werden muss. Der Standardwert 0 |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Cursor | Zeitstempel | Zeitstempel, bis die Zusammenfassung berechnet wurde. Nächsten Satzes von ReactionSummary kann mit dieser Wert Cursor generiert werden |
| Zusammenfassung | JSON-Array | Array von JSON-Objekten jede Ereignisobjekten Reaktionen Zusammenfassung auf eine Aktion, die in einer Gruppe gesendet werden. |

#### <a name="response-body-summary-object"></a>Zusammenfassung Antwort Body-Objekt

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| referenceId | Zeichenfolge | GUID, die die Id für die Entitätsverweis für eine Aktion darstellt. |
| reactionsCountMap | JSON-Objekt | Mit "gefällt mir" und Kommentare Count für diese ReferenceId JSON-Objekt |


#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

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

## <a name="get-reaction-details-for-a-action"></a>Hier erhalten Sie /reaction für eine Aktion

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Pfad-Parameter | sourceGroupId | String | Nein | Die GUID der Gruppe, in der die Aktion gesendet wurde |
| URL-Pfad-Parameter | referenceId | String | Nein | GUID, die die Id für die Entitätsverweis für eine Aktion darstellt. |
| URL-Pfad-Parameter | reactionType | String | Nein | Enum-Wert: 'Like "/" abgeben'|
| URL-Pfad-Parameter | Cursor | TimeStamp | Nein | Zeitstempel, aus denen die Zusammenfassung berechnet werden muss. Der Standardwert 0 |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Cursor | TimeStamp | Zeitstempel, bis die ReactionDetail bereitgestellt wurde. Nächsten Satzes von ReactionDetails kann mit dieser Wert Cursor generiert werden |
| reactionDetails | JSON-Array | Array von JSON-Objekten jedes Ereignisobjekten Reaktionen Detail auf eine Aktion, die in einer Gruppe gesendet |

#### <a name="response-body-summary-object"></a>Zusammenfassung Antwort Body-Objekt

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| reactionId | Zeichenfolge | GUID, die die Id für die Reaktion auf ReferenceId für eine Aktion erstellt darstellt. |
| userId | JSON-Objekt | Benutzer-ID des Benutzers, der die Reaktion auf eine Aktion erstellt hat |
| ZuletztGeändertUm | Timestamp | Zeitstempel, an dem Reaktion erstellt/aktualisiert wurde |


#### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

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