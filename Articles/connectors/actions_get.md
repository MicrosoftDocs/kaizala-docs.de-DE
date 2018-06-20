---
title: /Actions
description: Referenzartikel für API zum Abrufen der Liste der Aktionen in einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 717b91d38ed43c85c3511de84538bb357e799f9b
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905331"
---
# <a name="get-list-of-actions-in-a-group"></a><span data-ttu-id="411af-103">Hier finden Sie die Liste der Aktionen in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="411af-103">Get list of Actions in a group</span></span>
## <a name="get-actions"></a><span data-ttu-id="411af-104">Abrufen von /actions</span><span class="sxs-lookup"><span data-stu-id="411af-104">GET /actions</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions?actionType={action_Type}

### <a name="request-parameters"></a><span data-ttu-id="411af-105">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="411af-105">Request Parameters</span></span>

|  | <span data-ttu-id="411af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-106">Parameter</span></span> | <span data-ttu-id="411af-107">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-107">Type</span></span> | <span data-ttu-id="411af-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="411af-108">Optional?</span></span> | <span data-ttu-id="411af-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="411af-110">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-110">URL Path Parameter</span></span> | <span data-ttu-id="411af-111">groupId</span><span class="sxs-lookup"><span data-stu-id="411af-111">groupId</span></span> | <span data-ttu-id="411af-112">String</span><span class="sxs-lookup"><span data-stu-id="411af-112">String</span></span> | <span data-ttu-id="411af-113">Nein</span><span class="sxs-lookup"><span data-stu-id="411af-113">No</span></span> | <span data-ttu-id="411af-114">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="411af-114">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="411af-115">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="411af-115">HTTP Header</span></span> | <span data-ttu-id="411af-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="411af-116">accessToken</span></span> | <span data-ttu-id="411af-117">String</span><span class="sxs-lookup"><span data-stu-id="411af-117">String</span></span> | <span data-ttu-id="411af-118">Nein</span><span class="sxs-lookup"><span data-stu-id="411af-118">No</span></span> | <span data-ttu-id="411af-119">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="411af-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="411af-120">URL-Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="411af-120">URL Query Parameter</span></span> | <span data-ttu-id="411af-121">actionType</span><span class="sxs-lookup"><span data-stu-id="411af-121">actionType</span></span> | <span data-ttu-id="411af-122">String</span><span class="sxs-lookup"><span data-stu-id="411af-122">String</span></span> | <span data-ttu-id="411af-123">Nein</span><span class="sxs-lookup"><span data-stu-id="411af-123">No</span></span> | <span data-ttu-id="411af-124">Typ der abzurufenden Aktion</span><span class="sxs-lookup"><span data-stu-id="411af-124">Type of action to retrieve</span></span> |
| <span data-ttu-id="411af-125">URL-Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="411af-125">URL Query Parameter</span></span> | <span data-ttu-id="411af-126">fromDate</span><span class="sxs-lookup"><span data-stu-id="411af-126">fromDate</span></span> | <span data-ttu-id="411af-127">DateTime (Epoche Zeit)</span><span class="sxs-lookup"><span data-stu-id="411af-127">DateTime (epoch time)</span></span> | <span data-ttu-id="411af-128">Ja</span><span class="sxs-lookup"><span data-stu-id="411af-128">Yes</span></span> | <span data-ttu-id="411af-129">Zeit aus der die Aktionen benötigte abgerufen werden sollen</span><span class="sxs-lookup"><span data-stu-id="411af-129">Time from which the actions need to be retrieved</span></span> |
| <span data-ttu-id="411af-130">URL-Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="411af-130">URL Query Parameter</span></span> | <span data-ttu-id="411af-131">count</span><span class="sxs-lookup"><span data-stu-id="411af-131">count</span></span> | <span data-ttu-id="411af-132">number</span><span class="sxs-lookup"><span data-stu-id="411af-132">number</span></span> | <span data-ttu-id="411af-133">Ja</span><span class="sxs-lookup"><span data-stu-id="411af-133">Yes</span></span> | <span data-ttu-id="411af-134">Die Anzahl der einzelnen Aktionen zu zurückgegeben werden soll; Default = 30</span><span class="sxs-lookup"><span data-stu-id="411af-134">Count of individual actions to be returned; Default = 30</span></span> |

### <a name="response-body"></a><span data-ttu-id="411af-135">Antworttext</span><span class="sxs-lookup"><span data-stu-id="411af-135">Response body</span></span>

| <span data-ttu-id="411af-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-136">Parameter</span></span> | <span data-ttu-id="411af-137">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-137">Type</span></span> | <span data-ttu-id="411af-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-138">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-139">Aktionen</span><span class="sxs-lookup"><span data-stu-id="411af-139">actions</span></span> | <span data-ttu-id="411af-140">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="411af-140">JSON Object Array</span></span> | <span data-ttu-id="411af-141">Array von Action-Objekten</span><span class="sxs-lookup"><span data-stu-id="411af-141">Array of action objects</span></span> |
| <span data-ttu-id="411af-142">hasMore</span><span class="sxs-lookup"><span data-stu-id="411af-142">hasMore</span></span> | <span data-ttu-id="411af-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="411af-143">boolean</span></span> | <span data-ttu-id="411af-144">Wenn die maximale Anzahl von Aktionen pro Antwort erreicht hat, wird diese Variable festlegen auf "true"</span><span class="sxs-lookup"><span data-stu-id="411af-144">If the max count of actions per response has reached, this variable will be set to true</span></span> |

<span data-ttu-id="411af-145">JSON-Struktur für jede einzelne Aktion in das Array Aktionen []:</span><span class="sxs-lookup"><span data-stu-id="411af-145">JSON structure for each individual action in the array actions[]:</span></span>

| <span data-ttu-id="411af-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-146">Parameter</span></span> | <span data-ttu-id="411af-147">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-147">Type</span></span> | <span data-ttu-id="411af-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-149">referenceId</span><span class="sxs-lookup"><span data-stu-id="411af-149">referenceId</span></span> | <span data-ttu-id="411af-150">String</span><span class="sxs-lookup"><span data-stu-id="411af-150">String</span></span> | <span data-ttu-id="411af-151">ReferenceID für die Nachricht</span><span class="sxs-lookup"><span data-stu-id="411af-151">referenceID for the message</span></span> |
| <span data-ttu-id="411af-152">actionType</span><span class="sxs-lookup"><span data-stu-id="411af-152">actionType</span></span> | <span data-ttu-id="411af-153">String</span><span class="sxs-lookup"><span data-stu-id="411af-153">String</span></span> | <span data-ttu-id="411af-154">Typ der Aktion zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="411af-154">Type of action being returned</span></span> |
| <span data-ttu-id="411af-155">actionBody</span><span class="sxs-lookup"><span data-stu-id="411af-155">actionBody</span></span> | <span data-ttu-id="411af-156">JSON-Objekt-Array speziell für die actiontype</span><span class="sxs-lookup"><span data-stu-id="411af-156">JSON object array specific to the actiontype</span></span> | <span data-ttu-id="411af-157">Array mit Objekten, die speziell für die actiontype</span><span class="sxs-lookup"><span data-stu-id="411af-157">Array with objects specific to the actiontype</span></span> |
| <span data-ttu-id="411af-158">sender</span><span class="sxs-lookup"><span data-stu-id="411af-158">sender</span></span> | <span data-ttu-id="411af-159">String</span><span class="sxs-lookup"><span data-stu-id="411af-159">String</span></span> | <span data-ttu-id="411af-160">Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet</span><span class="sxs-lookup"><span data-stu-id="411af-160">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="411af-161">sentAt</span><span class="sxs-lookup"><span data-stu-id="411af-161">sentAt</span></span> | <span data-ttu-id="411af-162">DateTime</span><span class="sxs-lookup"><span data-stu-id="411af-162">DateTime</span></span> | <span data-ttu-id="411af-163">Wenn die Aktion in der Gruppe veröffentlicht wurde Zeit</span><span class="sxs-lookup"><span data-stu-id="411af-163">Time when the action was posted to the group</span></span> |

####  <a name="actionbody-object-structure-for-imagepicture-attachment"></a><span data-ttu-id="411af-164">ActionBody Objektstruktur für Bild/Bild Anlage:</span><span class="sxs-lookup"><span data-stu-id="411af-164">actionBody object structure for image/picture attachment:</span></span>

| <span data-ttu-id="411af-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-165">Parameter</span></span> | <span data-ttu-id="411af-166">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-166">Type</span></span> | <span data-ttu-id="411af-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-168">imageURL</span><span class="sxs-lookup"><span data-stu-id="411af-168">imageURL</span></span> | <span data-ttu-id="411af-169">String</span><span class="sxs-lookup"><span data-stu-id="411af-169">String</span></span> | <span data-ttu-id="411af-170">URL-Zeichenfolge für das Bild</span><span class="sxs-lookup"><span data-stu-id="411af-170">URL string for the picture</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-171">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-171">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "8a93c6cc-8499-44b0-aa54-016648100080",
      "actionType": "Image",
      "sender": "+9196500000",
      "creationTime": 1481180806,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg"
      }
    }
]
}
```

####  <a name="actionbody-object-structure-for-the-action-share-location"></a><span data-ttu-id="411af-172">ActionBody Objektstruktur für die Aktion "Speicherort freigeben":</span><span class="sxs-lookup"><span data-stu-id="411af-172">actionBody object structure for the action 'Share Location':</span></span>

| <span data-ttu-id="411af-173">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-173">Parameter</span></span> | <span data-ttu-id="411af-174">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-174">Type</span></span> | <span data-ttu-id="411af-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-175">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-176">latitude</span><span class="sxs-lookup"><span data-stu-id="411af-176">latitude</span></span> | <span data-ttu-id="411af-177">Double</span><span class="sxs-lookup"><span data-stu-id="411af-177">Double</span></span> | <span data-ttu-id="411af-178">Breitengradkoordinaten für den Speicherort</span><span class="sxs-lookup"><span data-stu-id="411af-178">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="411af-179">longitude</span><span class="sxs-lookup"><span data-stu-id="411af-179">longitude</span></span> | <span data-ttu-id="411af-180">Double</span><span class="sxs-lookup"><span data-stu-id="411af-180">Double</span></span> | <span data-ttu-id="411af-181">Längengradkoordinaten für den Speicherort</span><span class="sxs-lookup"><span data-stu-id="411af-181">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-182">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-182">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

#### <a name="actionbody-object-structure-for-the-action-photo-with-location"></a><span data-ttu-id="411af-183">ActionBody Objektstruktur für die Aktion 'Foto mit Speicherort':</span><span class="sxs-lookup"><span data-stu-id="411af-183">actionBody object structure for the action 'Photo with Location':</span></span>

| <span data-ttu-id="411af-184">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-184">Parameter</span></span> | <span data-ttu-id="411af-185">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-185">Type</span></span> | <span data-ttu-id="411af-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-187">imageURL</span><span class="sxs-lookup"><span data-stu-id="411af-187">imageURL</span></span> | <span data-ttu-id="411af-188">String</span><span class="sxs-lookup"><span data-stu-id="411af-188">String</span></span> | <span data-ttu-id="411af-189">URL-Zeichenfolge für das Bild</span><span class="sxs-lookup"><span data-stu-id="411af-189">URL string for the picture</span></span> |
| <span data-ttu-id="411af-190">latitude</span><span class="sxs-lookup"><span data-stu-id="411af-190">latitude</span></span> | <span data-ttu-id="411af-191">Double</span><span class="sxs-lookup"><span data-stu-id="411af-191">Double</span></span> | <span data-ttu-id="411af-192">Breitengradkoordinaten für den Speicherort</span><span class="sxs-lookup"><span data-stu-id="411af-192">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="411af-193">longitude</span><span class="sxs-lookup"><span data-stu-id="411af-193">longitude</span></span> | <span data-ttu-id="411af-194">Double</span><span class="sxs-lookup"><span data-stu-id="411af-194">Double</span></span> | <span data-ttu-id="411af-195">Längengradkoordinaten für den Speicherort</span><span class="sxs-lookup"><span data-stu-id="411af-195">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-196">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-196">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg",
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

####  <a name="actionbody-object-structure-for-the-action-job"></a><span data-ttu-id="411af-197">ActionBody Objektstruktur für die Aktion "Job":</span><span class="sxs-lookup"><span data-stu-id="411af-197">actionBody object structure for the action 'Job':</span></span>

| <span data-ttu-id="411af-198">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-198">Parameter</span></span> | <span data-ttu-id="411af-199">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-199">Type</span></span> | <span data-ttu-id="411af-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-201">actionId</span><span class="sxs-lookup"><span data-stu-id="411af-201">actionId</span></span> | <span data-ttu-id="411af-202">String</span><span class="sxs-lookup"><span data-stu-id="411af-202">String</span></span> | <span data-ttu-id="411af-203">GUID, die bestimmte Aktionsinstanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="411af-203">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="411af-204">title</span><span class="sxs-lookup"><span data-stu-id="411af-204">title</span></span> | <span data-ttu-id="411af-205">String</span><span class="sxs-lookup"><span data-stu-id="411af-205">String</span></span> | <span data-ttu-id="411af-206">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="411af-206">Title of the Job</span></span> |
| <span data-ttu-id="411af-207">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="411af-207">assigneeCount</span></span> | <span data-ttu-id="411af-208">Numerisch</span><span class="sxs-lookup"><span data-stu-id="411af-208">Numeric</span></span> | <span data-ttu-id="411af-209">Anzahl der "assignees"</span><span class="sxs-lookup"><span data-stu-id="411af-209">Number of assignees</span></span> |
| <span data-ttu-id="411af-210">responseCount</span><span class="sxs-lookup"><span data-stu-id="411af-210">responseCount</span></span> | <span data-ttu-id="411af-211">Numerisch</span><span class="sxs-lookup"><span data-stu-id="411af-211">Numeric</span></span> | <span data-ttu-id="411af-212">Anzahl der "assignees", die den Auftrag abgeschlossen gekennzeichnet haben</span><span class="sxs-lookup"><span data-stu-id="411af-212">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="411af-213">isCompleted</span><span class="sxs-lookup"><span data-stu-id="411af-213">isCompleted</span></span> | <span data-ttu-id="411af-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="411af-214">Boolean</span></span> | <span data-ttu-id="411af-215">True, wenn alle "assignees" den Auftrag abgeschlossen haben</span><span class="sxs-lookup"><span data-stu-id="411af-215">True when all assignees have completed the job</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-216">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-216">Sample JSON Response:</span></span>

```javascript
{
  "actions": [
    {
      "referenceId": "3214841c-eaa2-4bf3-a583-acc69d9279c4",
      "actionType": "Job",
      "sender": "+919910005",
      "creationTime": 1481179788,
      "actionBody": {
        "actionId": "f260dc09-f1f3-4305-84f6-6edbedb82fb7",
        "title": "Test",
        "assigneeCount": 1,
        "responseCount": 0,
        "isCompleted": false
      }
    }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-poll"></a><span data-ttu-id="411af-217">ActionBody Objektstruktur für die Aktion "Umfrage":</span><span class="sxs-lookup"><span data-stu-id="411af-217">actionBody object structure for the action 'Poll':</span></span>

| <span data-ttu-id="411af-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-218">Parameter</span></span> | <span data-ttu-id="411af-219">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-219">Type</span></span> | <span data-ttu-id="411af-220">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-220">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-221">actionId</span><span class="sxs-lookup"><span data-stu-id="411af-221">actionId</span></span> | <span data-ttu-id="411af-222">String</span><span class="sxs-lookup"><span data-stu-id="411af-222">String</span></span> | <span data-ttu-id="411af-223">GUID, die bestimmte Aktionsinstanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="411af-223">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="411af-224">question</span><span class="sxs-lookup"><span data-stu-id="411af-224">question</span></span> | <span data-ttu-id="411af-225">String</span><span class="sxs-lookup"><span data-stu-id="411af-225">String</span></span> | <span data-ttu-id="411af-226">Abstimmungsfrage</span><span class="sxs-lookup"><span data-stu-id="411af-226">Poll Question</span></span> |
| <span data-ttu-id="411af-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="411af-227">isSenderOnly</span></span> | <span data-ttu-id="411af-228">Boolean</span><span class="sxs-lookup"><span data-stu-id="411af-228">Boolean</span></span> | <span data-ttu-id="411af-229">True, wenn die Umfrage Zusammenfassung nur Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="411af-229">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="411af-230">ExpiryDate.</span><span class="sxs-lookup"><span data-stu-id="411af-230">expiryDate</span></span> | <span data-ttu-id="411af-231">DateTime</span><span class="sxs-lookup"><span data-stu-id="411af-231">DateTime</span></span> | <span data-ttu-id="411af-232">DateTime der Ablaufzeit der Umfrage</span><span class="sxs-lookup"><span data-stu-id="411af-232">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="411af-233">Choices</span><span class="sxs-lookup"><span data-stu-id="411af-233">Choices</span></span> | <span data-ttu-id="411af-234">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="411af-234">Json Array</span></span> | <span data-ttu-id="411af-235">Liste der Json-Objekte mit folgenden-Komponente</span><span class="sxs-lookup"><span data-stu-id="411af-235">List of Json objects with following component</span></span> <ol><li><span data-ttu-id="411af-236">Titel - Option Text</span><span class="sxs-lookup"><span data-stu-id="411af-236">title - Option Text</span></span></li><li><span data-ttu-id="411af-237">Bild - Option</span><span class="sxs-lookup"><span data-stu-id="411af-237">image - Option Image</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-238">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-238">Sample JSON Response:</span></span>

```javascript
{
    "actions": [
        {
            "referenceId": "d4753fdc-13fe-4162-a48f-5bf071bfd380",
            "actionType": "Poll",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:33:51Z",
            "actionBody": {
                "actionId": "27c7dbcf-48bb-4523-8273-d53a3da2343b",
                "question": "Do you find Kaizala extensibility easy to use?",
                "isSenderOnly": false,
                "expiryDate": "2017-12-20T18:33:51Z",
                "choices": [
                    {
                        "title": "Yes",
                        "image": "https://cdn.kascore.osi.office.net/75e8e7b63d2a4c10cdc30208aa27f1c2987d868a0e764fc742a94f6549d8bdb2.png?sv=2015-12-11&sr=b&sig=4iqswjFVYyqGqyKg6cdMdUQmiAez8sV951UScUmLzLk%3D&st=2017-05-17T07%3A04%3A41Z&se=2291-03-02T08%3A04%3A41Z&sp=r"
                    },
                    {
                        "title": "No"
                    },
                    {
                        "title": "Not at all"
                    }
                ]
            }
        }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-lets-meet"></a><span data-ttu-id="411af-239">ActionBody Objektstruktur für die Aktion 'Treffen wir uns':</span><span class="sxs-lookup"><span data-stu-id="411af-239">actionBody object structure for the action 'Let's Meet':</span></span>

| <span data-ttu-id="411af-240">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-240">Parameter</span></span> | <span data-ttu-id="411af-241">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-241">Type</span></span> | <span data-ttu-id="411af-242">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-242">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-243">actionId</span><span class="sxs-lookup"><span data-stu-id="411af-243">actionId</span></span> | <span data-ttu-id="411af-244">String</span><span class="sxs-lookup"><span data-stu-id="411af-244">String</span></span> | <span data-ttu-id="411af-245">GUID, die bestimmte Aktionsinstanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="411af-245">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="411af-246">title</span><span class="sxs-lookup"><span data-stu-id="411af-246">title</span></span> | <span data-ttu-id="411af-247">String</span><span class="sxs-lookup"><span data-stu-id="411af-247">String</span></span> | <span data-ttu-id="411af-248">Titel der Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="411af-248">Title of the Meeting request</span></span> |
| <span data-ttu-id="411af-249">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="411af-249">isSenderOnly</span></span> | <span data-ttu-id="411af-250">Boolean</span><span class="sxs-lookup"><span data-stu-id="411af-250">Boolean</span></span> | <span data-ttu-id="411af-251">True, wenn die Umfrage Zusammenfassung nur Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="411af-251">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="411af-252">duration</span><span class="sxs-lookup"><span data-stu-id="411af-252">duration</span></span> | <span data-ttu-id="411af-253">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="411af-253">Integer</span></span> | <span data-ttu-id="411af-254">Dauer der Besprechung (in Minuten)</span><span class="sxs-lookup"><span data-stu-id="411af-254">Duration of the meeting (in mins)</span></span> |
| <span data-ttu-id="411af-255">Tagesordnung</span><span class="sxs-lookup"><span data-stu-id="411af-255">agenda</span></span> | <span data-ttu-id="411af-256">String</span><span class="sxs-lookup"><span data-stu-id="411af-256">String</span></span> | <span data-ttu-id="411af-257">Legen Sie für die Besprechung Tagesordnung</span><span class="sxs-lookup"><span data-stu-id="411af-257">Agenda set for the meeting</span></span> |
| <span data-ttu-id="411af-258">startingTime</span><span class="sxs-lookup"><span data-stu-id="411af-258">startingTime</span></span> | <span data-ttu-id="411af-259">DateTime</span><span class="sxs-lookup"><span data-stu-id="411af-259">DateTime</span></span> | <span data-ttu-id="411af-260">DateTime der Ablaufzeit der Umfrage</span><span class="sxs-lookup"><span data-stu-id="411af-260">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="411af-261">Ort</span><span class="sxs-lookup"><span data-stu-id="411af-261">Place</span></span> | <span data-ttu-id="411af-262">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="411af-262">Json Object</span></span> | <span data-ttu-id="411af-263">Standortdaten mit folgenden-Komponente</span><span class="sxs-lookup"><span data-stu-id="411af-263">Location Data with following component</span></span> <ol><li><span data-ttu-id="411af-264">Latitude</span><span class="sxs-lookup"><span data-stu-id="411af-264">Latitude</span></span></li><li><span data-ttu-id="411af-265">Longitude</span><span class="sxs-lookup"><span data-stu-id="411af-265">Longitude</span></span></li><li><span data-ttu-id="411af-266">name</span><span class="sxs-lookup"><span data-stu-id="411af-266">name</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-267">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-267">Sample JSON Response:</span></span>

```javascript
{
    "actions": [
        {
            "referenceId": "32d1e5ad-36ff-4237-a49c-4be95a10cd12",
            "actionType": "LetsMeet",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:55:04Z",
            "actionBody": {
                "actionId": "3c80f0f1-2b2f-460a-b760-ec10adb7dbb1",
                "title": "lets catch up?",
                "startingTime": "2018-01-01T00:00:00Z",
                "agenda": "no agenda",
                "duration": 30,
                "isSenderOnly": false,
                "place": {
                    "latitude": 15,
                    "longitude": 96,
                    "name": "MS Building 3"
                }
            }
        }
  ]
}
```


####  <a name="actionbody-object-structure-for-the-action-survey"></a><span data-ttu-id="411af-268">ActionBody Objektstruktur für die Aktion "Umfrage":</span><span class="sxs-lookup"><span data-stu-id="411af-268">actionBody object structure for the action 'Survey':</span></span>

| <span data-ttu-id="411af-269">Parameter</span><span class="sxs-lookup"><span data-stu-id="411af-269">Parameter</span></span> | <span data-ttu-id="411af-270">Typ</span><span class="sxs-lookup"><span data-stu-id="411af-270">Type</span></span> | <span data-ttu-id="411af-271">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="411af-271">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="411af-272">actionId</span><span class="sxs-lookup"><span data-stu-id="411af-272">actionId</span></span> | <span data-ttu-id="411af-273">String</span><span class="sxs-lookup"><span data-stu-id="411af-273">String</span></span> | <span data-ttu-id="411af-274">GUID, die bestimmte Aktionsinstanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="411af-274">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="411af-275">title</span><span class="sxs-lookup"><span data-stu-id="411af-275">title</span></span> | <span data-ttu-id="411af-276">String</span><span class="sxs-lookup"><span data-stu-id="411af-276">String</span></span> | <span data-ttu-id="411af-277">Titel der Umfrage</span><span class="sxs-lookup"><span data-stu-id="411af-277">Title of the Survey</span></span> |
| <span data-ttu-id="411af-278">responseCount</span><span class="sxs-lookup"><span data-stu-id="411af-278">responseCount</span></span> | <span data-ttu-id="411af-279">Numerisch</span><span class="sxs-lookup"><span data-stu-id="411af-279">Numeric</span></span> | <span data-ttu-id="411af-280">Anzahl der Personen, die auf die Umfrage geantwortet</span><span class="sxs-lookup"><span data-stu-id="411af-280">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="411af-281">ExpiryDate.</span><span class="sxs-lookup"><span data-stu-id="411af-281">expiryDate</span></span> | <span data-ttu-id="411af-282">DateTime</span><span class="sxs-lookup"><span data-stu-id="411af-282">DateTime</span></span> | <span data-ttu-id="411af-283">DateTime der Ablaufzeit der Umfrage</span><span class="sxs-lookup"><span data-stu-id="411af-283">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="411af-284">Beispiel JSON-Antwort:</span><span class="sxs-lookup"><span data-stu-id="411af-284">Sample JSON Response:</span></span>

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

<span data-ttu-id="411af-285">Als Nächstes folgt: Sie können weitere Details jeder Aktion-Instanz mit den entsprechenden ActionId abrufen.</span><span class="sxs-lookup"><span data-stu-id="411af-285">Next: You can retrieve further details of each action instance with the corresponding actionId.</span></span> [<span data-ttu-id="411af-286">API zum Abrufen von Action Instanzdetails</span><span class="sxs-lookup"><span data-stu-id="411af-286">API for retrieving Action instance Details</span></span>](actionDetails.md)
