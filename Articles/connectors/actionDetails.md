---
title: /Action-Details
description: Referenzartikel zur API zur Abfrage bezüglich Details zu Kaizala-Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: edb02de0ab8d88e058dc2ad20be236986984226f
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535674"
---
# <a name="get-details-for-an-action-in-a-group"></a>Abrufen von Details für eine Aktion in einer Gruppe
## <a name="get-actionsactionid"></a>/Actions/{actionId}/abrufen

Checken Sie die API zum Abrufen der Liste der Aktionsinstanzen ein, die an eine Gruppe mithilfe der [API für Get/Actions hier](actions_get.md)gesendet wurden. Sie können weitere Details zu einer bestimmten Aktionsinstanz abrufen, auf die durch eine Aktions-Nr verwiesen wird.

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt. |
| URL-Pfad-Parameter | actionId | String | Nein | GUID, die die bestimmte Aktionsinstanz darstellt |
| HTTP-Header | accessToken | String | Nein | Vom auth-Endpunkt empfangenes Zugriffs Token |
| URL-Abfrage Parameter | getDetails | Boolesch | Ja | Wird verwendet, um Drilldown-Details der spezifischen Aktion abzurufen. Der Standardwert ist false. |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionType | String | Typ der zurückzugebenden Aktion |
| actionDetails | JSON-Objekt | Für den Action Type spezifisches JSON-Objekt |
| sender | String | Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet hat |
| sentAt | DateTime | Zeitpunkt, zu dem die Aktion in der Gruppe veröffentlicht wurde |

####  <a name="actiondetails-object-structure-for-the-action-job"></a>actionDetails-Objektstruktur für die Aktion "Auftrag":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| DueDate | DateTime | Fälligkeitsdatum für den Auftrag |
| title | String | Titel des Auftrags |
| status | Boolesch | True, wenn alle Empfänger den Auftrag abgeschlossen haben |
| responseCount | Numeric | Anzahl von Empfängern, die den Auftrag als abgeschlossen markiert haben |
| assigneeCount | Numeric | Anzahl der Empfänger |
| Antworten | JSON-Array | JSON-Array einzelner Auftragsantworten |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a>actionDetails-Objektstruktur für die Aktion "Survey":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | String | GUID, die die bestimmte Aktionsinstanz darstellt |
| title | String | Titel der Umfrage |
| responseCount | Numeric | Anzahl der Personen, die auf die Umfrage geantwortet haben |
| Ablaufdatum | DateTime | DateTime der Vermessungs Ablaufzeit |

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
