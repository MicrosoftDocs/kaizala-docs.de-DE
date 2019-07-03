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
# <a name="get-details-for-an-action-in-a-group"></a><span data-ttu-id="0f21d-103">Abrufen von Details für eine Aktion in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="0f21d-103">Get details for an Action in a group</span></span>
## <a name="get-actionsactionid"></a><span data-ttu-id="0f21d-104">/Actions/{actionId}/abrufen</span><span class="sxs-lookup"><span data-stu-id="0f21d-104">GET /actions/{actionId}/</span></span>

<span data-ttu-id="0f21d-105">Checken Sie die API zum Abrufen der Liste der Aktionsinstanzen ein, die an eine Gruppe mithilfe der [API für Get/Actions hier](actions_get.md)gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0f21d-105">Check-out the API for retrieving the list of action instances sent to a group using the [API for get /actions here](actions_get.md).</span></span> <span data-ttu-id="0f21d-106">Sie können weitere Details zu einer bestimmten Aktionsinstanz abrufen, auf die durch eine Aktions-Nr verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0f21d-106">You can retrieve further details about a specific action instance referenced by an actionId.</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a><span data-ttu-id="0f21d-107">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-107">Request Parameters</span></span>

|  | <span data-ttu-id="0f21d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-108">Parameter</span></span> | <span data-ttu-id="0f21d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="0f21d-109">Type</span></span> | <span data-ttu-id="0f21d-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="0f21d-110">Optional?</span></span> | <span data-ttu-id="0f21d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f21d-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="0f21d-112">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-112">URL Path Parameter</span></span> | <span data-ttu-id="0f21d-113">groupId</span><span class="sxs-lookup"><span data-stu-id="0f21d-113">groupId</span></span> | <span data-ttu-id="0f21d-114">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-114">String</span></span> | <span data-ttu-id="0f21d-115">Nein</span><span class="sxs-lookup"><span data-stu-id="0f21d-115">No</span></span> | <span data-ttu-id="0f21d-116">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f21d-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="0f21d-117">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-117">URL Path Parameter</span></span> | <span data-ttu-id="0f21d-118">actionId</span><span class="sxs-lookup"><span data-stu-id="0f21d-118">actionId</span></span> | <span data-ttu-id="0f21d-119">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-119">String</span></span> | <span data-ttu-id="0f21d-120">Nein</span><span class="sxs-lookup"><span data-stu-id="0f21d-120">No</span></span> | <span data-ttu-id="0f21d-121">GUID, die die bestimmte Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="0f21d-121">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="0f21d-122">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="0f21d-122">HTTP Header</span></span> | <span data-ttu-id="0f21d-123">accessToken</span><span class="sxs-lookup"><span data-stu-id="0f21d-123">accessToken</span></span> | <span data-ttu-id="0f21d-124">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-124">String</span></span> | <span data-ttu-id="0f21d-125">Nein</span><span class="sxs-lookup"><span data-stu-id="0f21d-125">No</span></span> | <span data-ttu-id="0f21d-126">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="0f21d-126">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="0f21d-127">URL-Abfrage Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-127">URL Query Parameter</span></span> | <span data-ttu-id="0f21d-128">getDetails</span><span class="sxs-lookup"><span data-stu-id="0f21d-128">getDetails</span></span> | <span data-ttu-id="0f21d-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="0f21d-129">Boolean</span></span> | <span data-ttu-id="0f21d-130">Ja</span><span class="sxs-lookup"><span data-stu-id="0f21d-130">Yes</span></span> | <span data-ttu-id="0f21d-131">Wird verwendet, um Drilldown-Details der spezifischen Aktion abzurufen. Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="0f21d-131">Use to get drill-down details of the specific action; Default is False</span></span> |

### <a name="response-body"></a><span data-ttu-id="0f21d-132">Antworttext</span><span class="sxs-lookup"><span data-stu-id="0f21d-132">Response body</span></span>

| <span data-ttu-id="0f21d-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-133">Parameter</span></span> | <span data-ttu-id="0f21d-134">Typ</span><span class="sxs-lookup"><span data-stu-id="0f21d-134">Type</span></span> | <span data-ttu-id="0f21d-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f21d-135">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="0f21d-136">actionType</span><span class="sxs-lookup"><span data-stu-id="0f21d-136">actionType</span></span> | <span data-ttu-id="0f21d-137">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-137">String</span></span> | <span data-ttu-id="0f21d-138">Typ der zurückzugebenden Aktion</span><span class="sxs-lookup"><span data-stu-id="0f21d-138">Type of action being returned</span></span> |
| <span data-ttu-id="0f21d-139">actionDetails</span><span class="sxs-lookup"><span data-stu-id="0f21d-139">actionDetails</span></span> | <span data-ttu-id="0f21d-140">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="0f21d-140">JSON object</span></span> | <span data-ttu-id="0f21d-141">Für den Action Type spezifisches JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="0f21d-141">JSON object specific to the actiontype</span></span> |
| <span data-ttu-id="0f21d-142">sender</span><span class="sxs-lookup"><span data-stu-id="0f21d-142">sender</span></span> | <span data-ttu-id="0f21d-143">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-143">String</span></span> | <span data-ttu-id="0f21d-144">Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet hat</span><span class="sxs-lookup"><span data-stu-id="0f21d-144">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="0f21d-145">sentAt</span><span class="sxs-lookup"><span data-stu-id="0f21d-145">sentAt</span></span> | <span data-ttu-id="0f21d-146">DateTime</span><span class="sxs-lookup"><span data-stu-id="0f21d-146">DateTime</span></span> | <span data-ttu-id="0f21d-147">Zeitpunkt, zu dem die Aktion in der Gruppe veröffentlicht wurde</span><span class="sxs-lookup"><span data-stu-id="0f21d-147">Time when the action was posted to the group</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-job"></a><span data-ttu-id="0f21d-148">actionDetails-Objektstruktur für die Aktion "Auftrag":</span><span class="sxs-lookup"><span data-stu-id="0f21d-148">actionDetails object structure for the action 'Job':</span></span>

| <span data-ttu-id="0f21d-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-149">Parameter</span></span> | <span data-ttu-id="0f21d-150">Typ</span><span class="sxs-lookup"><span data-stu-id="0f21d-150">Type</span></span> | <span data-ttu-id="0f21d-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f21d-151">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="0f21d-152">DueDate</span><span class="sxs-lookup"><span data-stu-id="0f21d-152">dueDate</span></span> | <span data-ttu-id="0f21d-153">DateTime</span><span class="sxs-lookup"><span data-stu-id="0f21d-153">DateTime</span></span> | <span data-ttu-id="0f21d-154">Fälligkeitsdatum für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="0f21d-154">Due date for the Job</span></span> |
| <span data-ttu-id="0f21d-155">title</span><span class="sxs-lookup"><span data-stu-id="0f21d-155">title</span></span> | <span data-ttu-id="0f21d-156">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-156">String</span></span> | <span data-ttu-id="0f21d-157">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="0f21d-157">Title of the Job</span></span> |
| <span data-ttu-id="0f21d-158">status</span><span class="sxs-lookup"><span data-stu-id="0f21d-158">status</span></span> | <span data-ttu-id="0f21d-159">Boolesch</span><span class="sxs-lookup"><span data-stu-id="0f21d-159">Boolean</span></span> | <span data-ttu-id="0f21d-160">True, wenn alle Empfänger den Auftrag abgeschlossen haben</span><span class="sxs-lookup"><span data-stu-id="0f21d-160">True when all assignees have completed the job</span></span> |
| <span data-ttu-id="0f21d-161">responseCount</span><span class="sxs-lookup"><span data-stu-id="0f21d-161">responseCount</span></span> | <span data-ttu-id="0f21d-162">Numeric</span><span class="sxs-lookup"><span data-stu-id="0f21d-162">Numeric</span></span> | <span data-ttu-id="0f21d-163">Anzahl von Empfängern, die den Auftrag als abgeschlossen markiert haben</span><span class="sxs-lookup"><span data-stu-id="0f21d-163">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="0f21d-164">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="0f21d-164">assigneeCount</span></span> | <span data-ttu-id="0f21d-165">Numeric</span><span class="sxs-lookup"><span data-stu-id="0f21d-165">Numeric</span></span> | <span data-ttu-id="0f21d-166">Anzahl der Empfänger</span><span class="sxs-lookup"><span data-stu-id="0f21d-166">Number of assignees</span></span> |
| <span data-ttu-id="0f21d-167">Antworten</span><span class="sxs-lookup"><span data-stu-id="0f21d-167">responses</span></span> | <span data-ttu-id="0f21d-168">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="0f21d-168">JSON Array</span></span> | <span data-ttu-id="0f21d-169">JSON-Array einzelner Auftragsantworten</span><span class="sxs-lookup"><span data-stu-id="0f21d-169">JSON Array of individual Job responses</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a><span data-ttu-id="0f21d-170">actionDetails-Objektstruktur für die Aktion "Survey":</span><span class="sxs-lookup"><span data-stu-id="0f21d-170">actionDetails object structure for the action 'Survey':</span></span>

| <span data-ttu-id="0f21d-171">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f21d-171">Parameter</span></span> | <span data-ttu-id="0f21d-172">Typ</span><span class="sxs-lookup"><span data-stu-id="0f21d-172">Type</span></span> | <span data-ttu-id="0f21d-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f21d-173">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="0f21d-174">actionId</span><span class="sxs-lookup"><span data-stu-id="0f21d-174">actionId</span></span> | <span data-ttu-id="0f21d-175">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-175">String</span></span> | <span data-ttu-id="0f21d-176">GUID, die die bestimmte Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="0f21d-176">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="0f21d-177">title</span><span class="sxs-lookup"><span data-stu-id="0f21d-177">title</span></span> | <span data-ttu-id="0f21d-178">String</span><span class="sxs-lookup"><span data-stu-id="0f21d-178">String</span></span> | <span data-ttu-id="0f21d-179">Titel der Umfrage</span><span class="sxs-lookup"><span data-stu-id="0f21d-179">Title of the Survey</span></span> |
| <span data-ttu-id="0f21d-180">responseCount</span><span class="sxs-lookup"><span data-stu-id="0f21d-180">responseCount</span></span> | <span data-ttu-id="0f21d-181">Numeric</span><span class="sxs-lookup"><span data-stu-id="0f21d-181">Numeric</span></span> | <span data-ttu-id="0f21d-182">Anzahl der Personen, die auf die Umfrage geantwortet haben</span><span class="sxs-lookup"><span data-stu-id="0f21d-182">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="0f21d-183">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="0f21d-183">expiryDate</span></span> | <span data-ttu-id="0f21d-184">DateTime</span><span class="sxs-lookup"><span data-stu-id="0f21d-184">DateTime</span></span> | <span data-ttu-id="0f21d-185">DateTime der Vermessungs Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="0f21d-185">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="0f21d-186">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="0f21d-186">Sample JSON Response:</span></span>

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
