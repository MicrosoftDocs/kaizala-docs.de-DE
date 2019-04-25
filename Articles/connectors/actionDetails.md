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
# <a name="get-details-for-an-action-in-a-group"></a><span data-ttu-id="34038-103">Abrufen von Details für eine Aktion in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="34038-103">Get details for an Action in a group</span></span>
## <a name="get-actionsactionid"></a><span data-ttu-id="34038-104">/Actions/{actionId}/abrufen</span><span class="sxs-lookup"><span data-stu-id="34038-104">GET /actions/{actionId}/</span></span>

<span data-ttu-id="34038-105">AusChecken der API zum Abrufen der Liste der an eine Gruppe gesendeten Aktionsinstanzen mithilfe der [API für Get/actions here](actions_get.md).</span><span class="sxs-lookup"><span data-stu-id="34038-105">Check-out the API for retrieving the list of action instances sent to a group using the [API for get /actions here](actions_get.md).</span></span> <span data-ttu-id="34038-106">Sie können weitere Details zu einer bestimmten Aktionsinstanz abrufen, auf die durch eine Aktions-Nr verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="34038-106">You can retrieve further details about a specific action instance referenced by an actionId.</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions/{actionId}/

### <a name="request-parameters"></a><span data-ttu-id="34038-107">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="34038-107">Request Parameters</span></span>

|  | <span data-ttu-id="34038-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-108">Parameter</span></span> | <span data-ttu-id="34038-109">Typ</span><span class="sxs-lookup"><span data-stu-id="34038-109">Type</span></span> | <span data-ttu-id="34038-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="34038-110">Optional?</span></span> | <span data-ttu-id="34038-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34038-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="34038-112">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-112">URL Path Parameter</span></span> | <span data-ttu-id="34038-113">groupId</span><span class="sxs-lookup"><span data-stu-id="34038-113">groupId</span></span> | <span data-ttu-id="34038-114">String</span><span class="sxs-lookup"><span data-stu-id="34038-114">String</span></span> | <span data-ttu-id="34038-115">Nein</span><span class="sxs-lookup"><span data-stu-id="34038-115">No</span></span> | <span data-ttu-id="34038-116">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="34038-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="34038-117">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-117">URL Path Parameter</span></span> | <span data-ttu-id="34038-118">actionId</span><span class="sxs-lookup"><span data-stu-id="34038-118">actionId</span></span> | <span data-ttu-id="34038-119">String</span><span class="sxs-lookup"><span data-stu-id="34038-119">String</span></span> | <span data-ttu-id="34038-120">Nein</span><span class="sxs-lookup"><span data-stu-id="34038-120">No</span></span> | <span data-ttu-id="34038-121">GUID, die die spezifische Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="34038-121">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="34038-122">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="34038-122">HTTP Header</span></span> | <span data-ttu-id="34038-123">accessToken</span><span class="sxs-lookup"><span data-stu-id="34038-123">accessToken</span></span> | <span data-ttu-id="34038-124">String</span><span class="sxs-lookup"><span data-stu-id="34038-124">String</span></span> | <span data-ttu-id="34038-125">Nein</span><span class="sxs-lookup"><span data-stu-id="34038-125">No</span></span> | <span data-ttu-id="34038-126">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="34038-126">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="34038-127">URL-Abfrage Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-127">URL Query Parameter</span></span> | <span data-ttu-id="34038-128">getDetails</span><span class="sxs-lookup"><span data-stu-id="34038-128">getDetails</span></span> | <span data-ttu-id="34038-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="34038-129">Boolean</span></span> | <span data-ttu-id="34038-130">Ja</span><span class="sxs-lookup"><span data-stu-id="34038-130">Yes</span></span> | <span data-ttu-id="34038-131">Verwenden Sie, um Drilldown-Details der spezifischen Aktion zu erhalten. Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="34038-131">Use to get drill-down details of the specific action; Default is False</span></span> |

### <a name="response-body"></a><span data-ttu-id="34038-132">Antworttext</span><span class="sxs-lookup"><span data-stu-id="34038-132">Response body</span></span>

| <span data-ttu-id="34038-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-133">Parameter</span></span> | <span data-ttu-id="34038-134">Typ</span><span class="sxs-lookup"><span data-stu-id="34038-134">Type</span></span> | <span data-ttu-id="34038-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34038-135">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="34038-136">actionType</span><span class="sxs-lookup"><span data-stu-id="34038-136">actionType</span></span> | <span data-ttu-id="34038-137">String</span><span class="sxs-lookup"><span data-stu-id="34038-137">String</span></span> | <span data-ttu-id="34038-138">Typ der zurückgegebenen Aktion</span><span class="sxs-lookup"><span data-stu-id="34038-138">Type of action being returned</span></span> |
| <span data-ttu-id="34038-139">actionDetails</span><span class="sxs-lookup"><span data-stu-id="34038-139">actionDetails</span></span> | <span data-ttu-id="34038-140">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="34038-140">JSON object</span></span> | <span data-ttu-id="34038-141">Spezifische JSON-onbject für Action Type</span><span class="sxs-lookup"><span data-stu-id="34038-141">JSON onbject specific to the actiontype</span></span> |
| <span data-ttu-id="34038-142">sender</span><span class="sxs-lookup"><span data-stu-id="34038-142">sender</span></span> | <span data-ttu-id="34038-143">String</span><span class="sxs-lookup"><span data-stu-id="34038-143">String</span></span> | <span data-ttu-id="34038-144">Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet hat</span><span class="sxs-lookup"><span data-stu-id="34038-144">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="34038-145">sentAt</span><span class="sxs-lookup"><span data-stu-id="34038-145">sentAt</span></span> | <span data-ttu-id="34038-146">DateTime</span><span class="sxs-lookup"><span data-stu-id="34038-146">DateTime</span></span> | <span data-ttu-id="34038-147">Zeitpunkt, zu dem die Aktion in der Gruppe veröffentlicht wurde</span><span class="sxs-lookup"><span data-stu-id="34038-147">Time when the action was posted to the group</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-job"></a><span data-ttu-id="34038-148">actionDetails-Objektstruktur für die Aktion ' Job ':</span><span class="sxs-lookup"><span data-stu-id="34038-148">actionDetails object structure for the action 'Job':</span></span>

| <span data-ttu-id="34038-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-149">Parameter</span></span> | <span data-ttu-id="34038-150">Typ</span><span class="sxs-lookup"><span data-stu-id="34038-150">Type</span></span> | <span data-ttu-id="34038-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34038-151">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="34038-152">dueDate</span><span class="sxs-lookup"><span data-stu-id="34038-152">dueDate</span></span> | <span data-ttu-id="34038-153">DateTime</span><span class="sxs-lookup"><span data-stu-id="34038-153">DateTime</span></span> | <span data-ttu-id="34038-154">Fälligkeitsdatum für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="34038-154">Due date for the Job</span></span> |
| <span data-ttu-id="34038-155">title</span><span class="sxs-lookup"><span data-stu-id="34038-155">title</span></span> | <span data-ttu-id="34038-156">String</span><span class="sxs-lookup"><span data-stu-id="34038-156">String</span></span> | <span data-ttu-id="34038-157">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="34038-157">Title of the Job</span></span> |
| <span data-ttu-id="34038-158">status</span><span class="sxs-lookup"><span data-stu-id="34038-158">status</span></span> | <span data-ttu-id="34038-159">Boolean</span><span class="sxs-lookup"><span data-stu-id="34038-159">Boolean</span></span> | <span data-ttu-id="34038-160">True, wenn alle Empfänger den Auftrag abgeschlossen haben</span><span class="sxs-lookup"><span data-stu-id="34038-160">True when all assignees have completed the job</span></span> |
| <span data-ttu-id="34038-161">responseCount</span><span class="sxs-lookup"><span data-stu-id="34038-161">responseCount</span></span> | <span data-ttu-id="34038-162">Numeric</span><span class="sxs-lookup"><span data-stu-id="34038-162">Numeric</span></span> | <span data-ttu-id="34038-163">Anzahl der Empfänger, die den Auftrag markiert haben</span><span class="sxs-lookup"><span data-stu-id="34038-163">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="34038-164">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="34038-164">assigneeCount</span></span> | <span data-ttu-id="34038-165">Numeric</span><span class="sxs-lookup"><span data-stu-id="34038-165">Numeric</span></span> | <span data-ttu-id="34038-166">Anzahl der Empfänger</span><span class="sxs-lookup"><span data-stu-id="34038-166">Number of assignees</span></span> |
| <span data-ttu-id="34038-167">Antworten</span><span class="sxs-lookup"><span data-stu-id="34038-167">responses</span></span> | <span data-ttu-id="34038-168">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="34038-168">JSON Array</span></span> | <span data-ttu-id="34038-169">JSON-Array der einzelnen Auftragsantworten</span><span class="sxs-lookup"><span data-stu-id="34038-169">JSON Array of individual Job responses</span></span> |

####  <a name="actiondetails-object-structure-for-the-action-survey"></a><span data-ttu-id="34038-170">actionDetails-Objektstruktur für die Aktion "Survey":</span><span class="sxs-lookup"><span data-stu-id="34038-170">actionDetails object structure for the action 'Survey':</span></span>

| <span data-ttu-id="34038-171">Parameter</span><span class="sxs-lookup"><span data-stu-id="34038-171">Parameter</span></span> | <span data-ttu-id="34038-172">Typ</span><span class="sxs-lookup"><span data-stu-id="34038-172">Type</span></span> | <span data-ttu-id="34038-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34038-173">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="34038-174">actionId</span><span class="sxs-lookup"><span data-stu-id="34038-174">actionId</span></span> | <span data-ttu-id="34038-175">String</span><span class="sxs-lookup"><span data-stu-id="34038-175">String</span></span> | <span data-ttu-id="34038-176">GUID, die die spezifische Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="34038-176">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="34038-177">title</span><span class="sxs-lookup"><span data-stu-id="34038-177">title</span></span> | <span data-ttu-id="34038-178">String</span><span class="sxs-lookup"><span data-stu-id="34038-178">String</span></span> | <span data-ttu-id="34038-179">Titel der Umfrage</span><span class="sxs-lookup"><span data-stu-id="34038-179">Title of the Survey</span></span> |
| <span data-ttu-id="34038-180">responseCount</span><span class="sxs-lookup"><span data-stu-id="34038-180">responseCount</span></span> | <span data-ttu-id="34038-181">Numeric</span><span class="sxs-lookup"><span data-stu-id="34038-181">Numeric</span></span> | <span data-ttu-id="34038-182">Anzahl der Personen, die auf die Umfrage geantwortet haben</span><span class="sxs-lookup"><span data-stu-id="34038-182">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="34038-183">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="34038-183">expiryDate</span></span> | <span data-ttu-id="34038-184">DateTime</span><span class="sxs-lookup"><span data-stu-id="34038-184">DateTime</span></span> | <span data-ttu-id="34038-185">DateTime der Umfrage Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="34038-185">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="34038-186">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="34038-186">Sample JSON Response:</span></span>

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
