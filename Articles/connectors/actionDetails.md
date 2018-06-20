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
# <a name="get-details-for-an-action-in-a-group"></a><span data-ttu-id="56e9b-103">Anzeigen der Details zu einer Aktion in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="56e9b-103">Get details for an Action in a group</span></span>
## <a name="get-actionsactionid"></a><span data-ttu-id="56e9b-104">GET-/actions/ {ActionId} /</span><span class="sxs-lookup"><span data-stu-id="56e9b-104">GET /actions/{actionId}/</span></span>

<span data-ttu-id="56e9b-105">Auschecken Sie die API zum Abrufen der Liste der Action-Instanzen, die an eine Gruppe mithilfe der [API für erste /actions hier](actions_get.md)gesendet.</span><span class="sxs-lookup"><span data-stu-id="56e9b-105">Check-out the API for retrieving the list of action instances sent to a group using the [API for get /actions here](actions_get.md).</span></span> <span data-ttu-id="56e9b-106">Sie können weitere Details über eine bestimmte Aktion-Instanz, die durch ein ActionId abrufen.</span><span class="sxs-lookup"><span data-stu-id="56e9b-106">You can retrieve further details about a specific action instance referenced by an actionId.</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a><span data-ttu-id="56e9b-107">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-107">Request Parameters</span></span>

|  | <span data-ttu-id="56e9b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-108">Parameter</span></span> | <span data-ttu-id="56e9b-109">Typ</span><span class="sxs-lookup"><span data-stu-id="56e9b-109">Type</span></span> | <span data-ttu-id="56e9b-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="56e9b-110">Optional?</span></span> | <span data-ttu-id="56e9b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56e9b-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="56e9b-112">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-112">URL Path Parameter</span></span> | <span data-ttu-id="56e9b-113">groupId</span><span class="sxs-lookup"><span data-stu-id="56e9b-113">groupId</span></span> | <span data-ttu-id="56e9b-114">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-114">String</span></span> | <span data-ttu-id="56e9b-115">Nein</span><span class="sxs-lookup"><span data-stu-id="56e9b-115">No</span></span> | <span data-ttu-id="56e9b-116">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="56e9b-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="56e9b-117">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-117">URL Path Parameter</span></span> | <span data-ttu-id="56e9b-118">actionId</span><span class="sxs-lookup"><span data-stu-id="56e9b-118">actionId</span></span> | <span data-ttu-id="56e9b-119">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-119">String</span></span> | <span data-ttu-id="56e9b-120">Nein</span><span class="sxs-lookup"><span data-stu-id="56e9b-120">No</span></span> | <span data-ttu-id="56e9b-121">GUID, die bestimmte Aktionsinstanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="56e9b-121">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="56e9b-122">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="56e9b-122">HTTP Header</span></span> | <span data-ttu-id="56e9b-123">accessToken</span><span class="sxs-lookup"><span data-stu-id="56e9b-123">accessToken</span></span> | <span data-ttu-id="56e9b-124">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-124">String</span></span> | <span data-ttu-id="56e9b-125">Nein</span><span class="sxs-lookup"><span data-stu-id="56e9b-125">No</span></span> | <span data-ttu-id="56e9b-126">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="56e9b-126">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="56e9b-127">URL-Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-127">URL Query Parameter</span></span> | <span data-ttu-id="56e9b-128">getDetails</span><span class="sxs-lookup"><span data-stu-id="56e9b-128">getDetails</span></span> | <span data-ttu-id="56e9b-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="56e9b-129">Boolean</span></span> | <span data-ttu-id="56e9b-130">Ja</span><span class="sxs-lookup"><span data-stu-id="56e9b-130">Yes</span></span> | <span data-ttu-id="56e9b-131">Nicht mit Drilldown-Details zu den speziellen Vorgang abzurufen. Standard ist False</span><span class="sxs-lookup"><span data-stu-id="56e9b-131">Use to get drill-down details of the specific action; Default is False</span></span> |

### <a name="response-body"></a><span data-ttu-id="56e9b-132">Antworttext</span><span class="sxs-lookup"><span data-stu-id="56e9b-132">Response body</span></span>

| <span data-ttu-id="56e9b-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-133">Parameter</span></span> | <span data-ttu-id="56e9b-134">Typ</span><span class="sxs-lookup"><span data-stu-id="56e9b-134">Type</span></span> | <span data-ttu-id="56e9b-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56e9b-135">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="56e9b-136">actionType</span><span class="sxs-lookup"><span data-stu-id="56e9b-136">actionType</span></span> | <span data-ttu-id="56e9b-137">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-137">String</span></span> | <span data-ttu-id="56e9b-138">Typ der Aktion zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="56e9b-138">Type of action being returned</span></span> |
| <span data-ttu-id="56e9b-139">actionDetails</span><span class="sxs-lookup"><span data-stu-id="56e9b-139">actionDetails</span></span> | <span data-ttu-id="56e9b-140">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="56e9b-140">JSON object</span></span> | <span data-ttu-id="56e9b-141">JSON Onbject speziell für die actiontype</span><span class="sxs-lookup"><span data-stu-id="56e9b-141">JSON onbject specific to the actiontype</span></span> |
| <span data-ttu-id="56e9b-142">sender</span><span class="sxs-lookup"><span data-stu-id="56e9b-142">sender</span></span> | <span data-ttu-id="56e9b-143">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-143">String</span></span> | <span data-ttu-id="56e9b-144">Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet</span><span class="sxs-lookup"><span data-stu-id="56e9b-144">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="56e9b-145">sentAt</span><span class="sxs-lookup"><span data-stu-id="56e9b-145">sentAt</span></span> | <span data-ttu-id="56e9b-146">DateTime</span><span class="sxs-lookup"><span data-stu-id="56e9b-146">DateTime</span></span> | <span data-ttu-id="56e9b-147">Wenn die Aktion in der Gruppe veröffentlicht wurde Zeit</span><span class="sxs-lookup"><span data-stu-id="56e9b-147">Time when the action was posted to the group</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-job"></a><span data-ttu-id="56e9b-148">ActionDetails Objektstruktur für die Aktion "Job":</span><span class="sxs-lookup"><span data-stu-id="56e9b-148">actionDetails object structure for the action 'Job':</span></span>

| <span data-ttu-id="56e9b-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-149">Parameter</span></span> | <span data-ttu-id="56e9b-150">Typ</span><span class="sxs-lookup"><span data-stu-id="56e9b-150">Type</span></span> | <span data-ttu-id="56e9b-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56e9b-151">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="56e9b-152">dueDate</span><span class="sxs-lookup"><span data-stu-id="56e9b-152">dueDate</span></span> | <span data-ttu-id="56e9b-153">DateTime</span><span class="sxs-lookup"><span data-stu-id="56e9b-153">DateTime</span></span> | <span data-ttu-id="56e9b-154">Fälligkeitsdatum für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="56e9b-154">Due date for the Job</span></span> |
| <span data-ttu-id="56e9b-155">title</span><span class="sxs-lookup"><span data-stu-id="56e9b-155">title</span></span> | <span data-ttu-id="56e9b-156">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-156">String</span></span> | <span data-ttu-id="56e9b-157">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="56e9b-157">Title of the Job</span></span> |
| <span data-ttu-id="56e9b-158">status</span><span class="sxs-lookup"><span data-stu-id="56e9b-158">status</span></span> | <span data-ttu-id="56e9b-159">Boolean</span><span class="sxs-lookup"><span data-stu-id="56e9b-159">Boolean</span></span> | <span data-ttu-id="56e9b-160">True, wenn alle "assignees" den Auftrag abgeschlossen haben</span><span class="sxs-lookup"><span data-stu-id="56e9b-160">True when all assignees have completed the job</span></span> |
| <span data-ttu-id="56e9b-161">responseCount</span><span class="sxs-lookup"><span data-stu-id="56e9b-161">responseCount</span></span> | <span data-ttu-id="56e9b-162">Numerisch</span><span class="sxs-lookup"><span data-stu-id="56e9b-162">Numeric</span></span> | <span data-ttu-id="56e9b-163">Anzahl der "assignees", die den Auftrag abgeschlossen gekennzeichnet haben</span><span class="sxs-lookup"><span data-stu-id="56e9b-163">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="56e9b-164">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="56e9b-164">assigneeCount</span></span> | <span data-ttu-id="56e9b-165">Numerisch</span><span class="sxs-lookup"><span data-stu-id="56e9b-165">Numeric</span></span> | <span data-ttu-id="56e9b-166">Anzahl der "assignees"</span><span class="sxs-lookup"><span data-stu-id="56e9b-166">Number of assignees</span></span> |
| <span data-ttu-id="56e9b-167">Antworten</span><span class="sxs-lookup"><span data-stu-id="56e9b-167">responses</span></span> | <span data-ttu-id="56e9b-168">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="56e9b-168">JSON Array</span></span> | <span data-ttu-id="56e9b-169">JSON-Array von einzelnen Auftragsantworten</span><span class="sxs-lookup"><span data-stu-id="56e9b-169">JSON Array of individual Job responses</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a><span data-ttu-id="56e9b-170">ActionDetails Objektstruktur für die Aktion "Umfrage":</span><span class="sxs-lookup"><span data-stu-id="56e9b-170">actionDetails object structure for the action 'Survey':</span></span>

| <span data-ttu-id="56e9b-171">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e9b-171">Parameter</span></span> | <span data-ttu-id="56e9b-172">Typ</span><span class="sxs-lookup"><span data-stu-id="56e9b-172">Type</span></span> | <span data-ttu-id="56e9b-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56e9b-173">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="56e9b-174">actionId</span><span class="sxs-lookup"><span data-stu-id="56e9b-174">actionId</span></span> | <span data-ttu-id="56e9b-175">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-175">String</span></span> | <span data-ttu-id="56e9b-176">GUID, die bestimmte Aktionsinstanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="56e9b-176">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="56e9b-177">title</span><span class="sxs-lookup"><span data-stu-id="56e9b-177">title</span></span> | <span data-ttu-id="56e9b-178">String</span><span class="sxs-lookup"><span data-stu-id="56e9b-178">String</span></span> | <span data-ttu-id="56e9b-179">Titel der Umfrage</span><span class="sxs-lookup"><span data-stu-id="56e9b-179">Title of the Survey</span></span> |
| <span data-ttu-id="56e9b-180">responseCount</span><span class="sxs-lookup"><span data-stu-id="56e9b-180">responseCount</span></span> | <span data-ttu-id="56e9b-181">Numerisch</span><span class="sxs-lookup"><span data-stu-id="56e9b-181">Numeric</span></span> | <span data-ttu-id="56e9b-182">Anzahl der Personen, die auf die Umfrage geantwortet</span><span class="sxs-lookup"><span data-stu-id="56e9b-182">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="56e9b-183">ExpiryDate.</span><span class="sxs-lookup"><span data-stu-id="56e9b-183">expiryDate</span></span> | <span data-ttu-id="56e9b-184">DateTime</span><span class="sxs-lookup"><span data-stu-id="56e9b-184">DateTime</span></span> | <span data-ttu-id="56e9b-185">DateTime der Ablaufzeit der Umfrage</span><span class="sxs-lookup"><span data-stu-id="56e9b-185">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="56e9b-186">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="56e9b-186">Sample JSON Response:</span></span>

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
