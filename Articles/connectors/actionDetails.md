---
title: /Action-Details
description: Referenzartikel zur API zur Abfrage von Details zu Kaizala-Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: a0871eec8a0247cea122bd14f968dd1e16936101
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190724"
---
# <a name="get-details-for-an-action-in-a-group"></a>Abrufen von Details für eine Aktion in einer Gruppe
## <a name="get-actionsactionid"></a>/Actions/{actionId}/abrufen

AusChecken der API zum Abrufen der Liste der an eine Gruppe gesendeten Aktionsinstanzen mithilfe der [API für Get/actions here](actions_get.md). Sie können weitere Details zu einer bestimmten Aktionsinstanz abrufen, auf die durch eine Aktions-Nr verwiesen wird.

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| URL-Pfad Parameter | actionId | String | Nein | GUID, die die spezifische Aktionsinstanz darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| URL-Abfrage Parameter | getDetails | Boolean | Ja | Verwenden Sie, um Drilldown-Details der spezifischen Aktion zu erhalten. Der Standardwert ist false. |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionType | String | Typ der zurückgegebenen Aktion |
| actionDetails | JSON-Objekt | Spezifische JSON-onbject für Action Type |
| sender | String | Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet hat |
| sentAt | DateTime | Zeitpunkt, zu dem die Aktion in der Gruppe veröffentlicht wurde |

####  <a name="actiondetails-object-structure-for-the-action-job"></a>actionDetails-Objektstruktur für die Aktion ' Job ':

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| dueDate | DateTime | Fälligkeitsdatum für den Auftrag |
| title | String | Titel des Auftrags |
| status | Boolean | True, wenn alle Empfänger den Auftrag abgeschlossen haben |
| responseCount | Numeric | Anzahl der Empfänger, die den Auftrag markiert haben |
| assigneeCount | Numeric | Anzahl der Empfänger |
| Antworten | JSON-Array | JSON-Array der einzelnen Auftragsantworten |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a>actionDetails-Objektstruktur für die Aktion "Survey":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | String | GUID, die die spezifische Aktionsinstanz darstellt |
| title | String | Titel der Umfrage |
| responseCount | Numeric | Anzahl der Personen, die auf die Umfrage geantwortet haben |
| Ablaufdatum | DateTime | DateTime der Umfrage Ablaufzeit |

##### <a name="sample-json-response"></a>JSON-Beispielantwort:

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
