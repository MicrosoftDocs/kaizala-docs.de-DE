---
title: -Details Aktion
description: Referenzartikel für API Fragen Details der Kaizala Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: a0871eec8a0247cea122bd14f968dd1e16936101
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905323"
---
# <a name="get-details-for-an-action-in-a-group"></a>Anzeigen der Details zu einer Aktion in einer Gruppe
## <a name="get-actionsactionid"></a>GET-/actions/ {ActionId} /

Auschecken Sie die API zum Abrufen der Liste der Action-Instanzen, die an eine Gruppe mithilfe der [API für erste /actions hier](actions_get.md)gesendet. Sie können weitere Details über eine bestimmte Aktion-Instanz, die durch ein ActionId abrufen.

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| URL-Pfad-Parameter | actionId | String | Nein | GUID, die bestimmte Aktionsinstanz darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| URL-Abfrageparameter | getDetails | Boolean | Ja | Nicht mit Drilldown-Details zu den speziellen Vorgang abzurufen. Standard ist False |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionType | String | Typ der Aktion zurückgegeben wird |
| actionDetails | JSON-Objekt | JSON Onbject speziell für die actiontype |
| sender | String | Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet |
| sentAt | DateTime | Wenn die Aktion in der Gruppe veröffentlicht wurde Zeit |

####  <a name="actiondetails-object-structure-for-the-action-job"></a>ActionDetails Objektstruktur für die Aktion "Job":

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| dueDate | DateTime | Fälligkeitsdatum für den Auftrag |
| title | String | Titel des Auftrags |
| status | Boolean | True, wenn alle "assignees" den Auftrag abgeschlossen haben |
| responseCount | Numerisch | Anzahl der "assignees", die den Auftrag abgeschlossen gekennzeichnet haben |
| assigneeCount | Numerisch | Anzahl der "assignees" |
| Antworten | JSON-Array | JSON-Array von einzelnen Auftragsantworten |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a>ActionDetails Objektstruktur für die Aktion "Umfrage":

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
