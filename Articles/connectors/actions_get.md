---
title: /Actions
description: Referenzartikel zur API zum Abrufen einer Liste von Aktionen in einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 717b91d38ed43c85c3511de84538bb357e799f9b
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190720"
---
# <a name="get-list-of-actions-in-a-group"></a><span data-ttu-id="662c3-103">Liste der Aktionen in einer Gruppe abrufen</span><span class="sxs-lookup"><span data-stu-id="662c3-103">Get list of Actions in a group</span></span>
## <a name="get-actions"></a><span data-ttu-id="662c3-104">/Actions abrufen</span><span class="sxs-lookup"><span data-stu-id="662c3-104">GET /actions</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/actions?actionType={action_Type}

### <a name="request-parameters"></a><span data-ttu-id="662c3-105">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="662c3-105">Request Parameters</span></span>

|  | <span data-ttu-id="662c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-106">Parameter</span></span> | <span data-ttu-id="662c3-107">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-107">Type</span></span> | <span data-ttu-id="662c3-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="662c3-108">Optional?</span></span> | <span data-ttu-id="662c3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="662c3-110">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-110">URL Path Parameter</span></span> | <span data-ttu-id="662c3-111">groupId</span><span class="sxs-lookup"><span data-stu-id="662c3-111">groupId</span></span> | <span data-ttu-id="662c3-112">String</span><span class="sxs-lookup"><span data-stu-id="662c3-112">String</span></span> | <span data-ttu-id="662c3-113">Nein</span><span class="sxs-lookup"><span data-stu-id="662c3-113">No</span></span> | <span data-ttu-id="662c3-114">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="662c3-114">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="662c3-115">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="662c3-115">HTTP Header</span></span> | <span data-ttu-id="662c3-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="662c3-116">accessToken</span></span> | <span data-ttu-id="662c3-117">String</span><span class="sxs-lookup"><span data-stu-id="662c3-117">String</span></span> | <span data-ttu-id="662c3-118">Nein</span><span class="sxs-lookup"><span data-stu-id="662c3-118">No</span></span> | <span data-ttu-id="662c3-119">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="662c3-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="662c3-120">URL-Abfrage Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-120">URL Query Parameter</span></span> | <span data-ttu-id="662c3-121">actionType</span><span class="sxs-lookup"><span data-stu-id="662c3-121">actionType</span></span> | <span data-ttu-id="662c3-122">String</span><span class="sxs-lookup"><span data-stu-id="662c3-122">String</span></span> | <span data-ttu-id="662c3-123">Nein</span><span class="sxs-lookup"><span data-stu-id="662c3-123">No</span></span> | <span data-ttu-id="662c3-124">Typ der abzurufenden Aktion</span><span class="sxs-lookup"><span data-stu-id="662c3-124">Type of action to retrieve</span></span> |
| <span data-ttu-id="662c3-125">URL-Abfrage Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-125">URL Query Parameter</span></span> | <span data-ttu-id="662c3-126">fromDate</span><span class="sxs-lookup"><span data-stu-id="662c3-126">fromDate</span></span> | <span data-ttu-id="662c3-127">DateTime (Epoche Zeit)</span><span class="sxs-lookup"><span data-stu-id="662c3-127">DateTime (epoch time)</span></span> | <span data-ttu-id="662c3-128">Ja</span><span class="sxs-lookup"><span data-stu-id="662c3-128">Yes</span></span> | <span data-ttu-id="662c3-129">Zeitpunkt, zu dem die Aktionen abgerufen werden müssen</span><span class="sxs-lookup"><span data-stu-id="662c3-129">Time from which the actions need to be retrieved</span></span> |
| <span data-ttu-id="662c3-130">URL-Abfrage Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-130">URL Query Parameter</span></span> | <span data-ttu-id="662c3-131">count</span><span class="sxs-lookup"><span data-stu-id="662c3-131">count</span></span> | <span data-ttu-id="662c3-132">number</span><span class="sxs-lookup"><span data-stu-id="662c3-132">number</span></span> | <span data-ttu-id="662c3-133">Ja</span><span class="sxs-lookup"><span data-stu-id="662c3-133">Yes</span></span> | <span data-ttu-id="662c3-134">Anzahl der zurückzugebenden einzelnen Aktionen; Standard = 30</span><span class="sxs-lookup"><span data-stu-id="662c3-134">Count of individual actions to be returned; Default = 30</span></span> |

### <a name="response-body"></a><span data-ttu-id="662c3-135">Antworttext</span><span class="sxs-lookup"><span data-stu-id="662c3-135">Response body</span></span>

| <span data-ttu-id="662c3-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-136">Parameter</span></span> | <span data-ttu-id="662c3-137">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-137">Type</span></span> | <span data-ttu-id="662c3-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-138">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-139">Aktionen</span><span class="sxs-lookup"><span data-stu-id="662c3-139">actions</span></span> | <span data-ttu-id="662c3-140">JSON-Objekt Array</span><span class="sxs-lookup"><span data-stu-id="662c3-140">JSON Object Array</span></span> | <span data-ttu-id="662c3-141">Array von Action-Objekten</span><span class="sxs-lookup"><span data-stu-id="662c3-141">Array of action objects</span></span> |
| <span data-ttu-id="662c3-142">hasMore</span><span class="sxs-lookup"><span data-stu-id="662c3-142">hasMore</span></span> | <span data-ttu-id="662c3-143">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="662c3-143">boolean</span></span> | <span data-ttu-id="662c3-144">Wenn die maximale Anzahl von Aktionen pro Antwort erreicht wurde, wird diese Variable auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="662c3-144">If the max count of actions per response has reached, this variable will be set to true</span></span> |

<span data-ttu-id="662c3-145">JSON-Struktur für jede einzelne Aktion im Array Actions []:</span><span class="sxs-lookup"><span data-stu-id="662c3-145">JSON structure for each individual action in the array actions[]:</span></span>

| <span data-ttu-id="662c3-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-146">Parameter</span></span> | <span data-ttu-id="662c3-147">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-147">Type</span></span> | <span data-ttu-id="662c3-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-149">referenceId</span><span class="sxs-lookup"><span data-stu-id="662c3-149">referenceId</span></span> | <span data-ttu-id="662c3-150">String</span><span class="sxs-lookup"><span data-stu-id="662c3-150">String</span></span> | <span data-ttu-id="662c3-151">Referenznummer für die Nachricht</span><span class="sxs-lookup"><span data-stu-id="662c3-151">referenceID for the message</span></span> |
| <span data-ttu-id="662c3-152">actionType</span><span class="sxs-lookup"><span data-stu-id="662c3-152">actionType</span></span> | <span data-ttu-id="662c3-153">String</span><span class="sxs-lookup"><span data-stu-id="662c3-153">String</span></span> | <span data-ttu-id="662c3-154">Typ der zurückgegebenen Aktion</span><span class="sxs-lookup"><span data-stu-id="662c3-154">Type of action being returned</span></span> |
| <span data-ttu-id="662c3-155">actionBody</span><span class="sxs-lookup"><span data-stu-id="662c3-155">actionBody</span></span> | <span data-ttu-id="662c3-156">Spezifisches JSON-Objektarray für Action Type</span><span class="sxs-lookup"><span data-stu-id="662c3-156">JSON object array specific to the actiontype</span></span> | <span data-ttu-id="662c3-157">Array mit spezifisch für den ActionType-Objekt</span><span class="sxs-lookup"><span data-stu-id="662c3-157">Array with objects specific to the actiontype</span></span> |
| <span data-ttu-id="662c3-158">sender</span><span class="sxs-lookup"><span data-stu-id="662c3-158">sender</span></span> | <span data-ttu-id="662c3-159">String</span><span class="sxs-lookup"><span data-stu-id="662c3-159">String</span></span> | <span data-ttu-id="662c3-160">Telefonnummer des Benutzers, der die Aktion an die Gruppe gesendet hat</span><span class="sxs-lookup"><span data-stu-id="662c3-160">Phone number of the user who sent the action to the group</span></span> |
| <span data-ttu-id="662c3-161">sentAt</span><span class="sxs-lookup"><span data-stu-id="662c3-161">sentAt</span></span> | <span data-ttu-id="662c3-162">DateTime</span><span class="sxs-lookup"><span data-stu-id="662c3-162">DateTime</span></span> | <span data-ttu-id="662c3-163">Zeitpunkt, zu dem die Aktion in der Gruppe veröffentlicht wurde</span><span class="sxs-lookup"><span data-stu-id="662c3-163">Time when the action was posted to the group</span></span> |

####  <a name="actionbody-object-structure-for-imagepicture-attachment"></a><span data-ttu-id="662c3-164">actionBody-Objektstruktur für Bild/Bild-Anlage:</span><span class="sxs-lookup"><span data-stu-id="662c3-164">actionBody object structure for image/picture attachment:</span></span>

| <span data-ttu-id="662c3-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-165">Parameter</span></span> | <span data-ttu-id="662c3-166">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-166">Type</span></span> | <span data-ttu-id="662c3-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-168">imageURL</span><span class="sxs-lookup"><span data-stu-id="662c3-168">imageURL</span></span> | <span data-ttu-id="662c3-169">String</span><span class="sxs-lookup"><span data-stu-id="662c3-169">String</span></span> | <span data-ttu-id="662c3-170">URL-Zeichenfolge für das Bild</span><span class="sxs-lookup"><span data-stu-id="662c3-170">URL string for the picture</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-171">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-171">Sample JSON Response:</span></span>

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

####  <a name="actionbody-object-structure-for-the-action-share-location"></a><span data-ttu-id="662c3-172">actionBody-Objektstruktur für die Aktion "Freigabespeicherort":</span><span class="sxs-lookup"><span data-stu-id="662c3-172">actionBody object structure for the action 'Share Location':</span></span>

| <span data-ttu-id="662c3-173">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-173">Parameter</span></span> | <span data-ttu-id="662c3-174">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-174">Type</span></span> | <span data-ttu-id="662c3-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-175">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-176">latitude</span><span class="sxs-lookup"><span data-stu-id="662c3-176">latitude</span></span> | <span data-ttu-id="662c3-177">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="662c3-177">Double</span></span> | <span data-ttu-id="662c3-178">Latitude-Koordinaten für den Standort</span><span class="sxs-lookup"><span data-stu-id="662c3-178">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="662c3-179">longitude</span><span class="sxs-lookup"><span data-stu-id="662c3-179">longitude</span></span> | <span data-ttu-id="662c3-180">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="662c3-180">Double</span></span> | <span data-ttu-id="662c3-181">Längenkoordinaten für den Standort</span><span class="sxs-lookup"><span data-stu-id="662c3-181">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-182">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-182">Sample JSON Response:</span></span>

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

#### <a name="actionbody-object-structure-for-the-action-photo-with-location"></a><span data-ttu-id="662c3-183">actionBody-Objektstruktur für die Aktion "Foto mit Speicherort":</span><span class="sxs-lookup"><span data-stu-id="662c3-183">actionBody object structure for the action 'Photo with Location':</span></span>

| <span data-ttu-id="662c3-184">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-184">Parameter</span></span> | <span data-ttu-id="662c3-185">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-185">Type</span></span> | <span data-ttu-id="662c3-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-187">imageURL</span><span class="sxs-lookup"><span data-stu-id="662c3-187">imageURL</span></span> | <span data-ttu-id="662c3-188">String</span><span class="sxs-lookup"><span data-stu-id="662c3-188">String</span></span> | <span data-ttu-id="662c3-189">URL-Zeichenfolge für das Bild</span><span class="sxs-lookup"><span data-stu-id="662c3-189">URL string for the picture</span></span> |
| <span data-ttu-id="662c3-190">latitude</span><span class="sxs-lookup"><span data-stu-id="662c3-190">latitude</span></span> | <span data-ttu-id="662c3-191">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="662c3-191">Double</span></span> | <span data-ttu-id="662c3-192">Latitude-Koordinaten für den Standort</span><span class="sxs-lookup"><span data-stu-id="662c3-192">Latitude coordinates for the location</span></span> |
| <span data-ttu-id="662c3-193">longitude</span><span class="sxs-lookup"><span data-stu-id="662c3-193">longitude</span></span> | <span data-ttu-id="662c3-194">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="662c3-194">Double</span></span> | <span data-ttu-id="662c3-195">Längenkoordinaten für den Standort</span><span class="sxs-lookup"><span data-stu-id="662c3-195">Longitude coordinates for the location</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-196">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-196">Sample JSON Response:</span></span>

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

####  <a name="actionbody-object-structure-for-the-action-job"></a><span data-ttu-id="662c3-197">actionBody-Objektstruktur für die Aktion ' Job ':</span><span class="sxs-lookup"><span data-stu-id="662c3-197">actionBody object structure for the action 'Job':</span></span>

| <span data-ttu-id="662c3-198">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-198">Parameter</span></span> | <span data-ttu-id="662c3-199">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-199">Type</span></span> | <span data-ttu-id="662c3-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-201">actionId</span><span class="sxs-lookup"><span data-stu-id="662c3-201">actionId</span></span> | <span data-ttu-id="662c3-202">String</span><span class="sxs-lookup"><span data-stu-id="662c3-202">String</span></span> | <span data-ttu-id="662c3-203">GUID, die die spezifische Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="662c3-203">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="662c3-204">title</span><span class="sxs-lookup"><span data-stu-id="662c3-204">title</span></span> | <span data-ttu-id="662c3-205">String</span><span class="sxs-lookup"><span data-stu-id="662c3-205">String</span></span> | <span data-ttu-id="662c3-206">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="662c3-206">Title of the Job</span></span> |
| <span data-ttu-id="662c3-207">assigneeCount</span><span class="sxs-lookup"><span data-stu-id="662c3-207">assigneeCount</span></span> | <span data-ttu-id="662c3-208">Numeric</span><span class="sxs-lookup"><span data-stu-id="662c3-208">Numeric</span></span> | <span data-ttu-id="662c3-209">Anzahl der Empfänger</span><span class="sxs-lookup"><span data-stu-id="662c3-209">Number of assignees</span></span> |
| <span data-ttu-id="662c3-210">responseCount</span><span class="sxs-lookup"><span data-stu-id="662c3-210">responseCount</span></span> | <span data-ttu-id="662c3-211">Numeric</span><span class="sxs-lookup"><span data-stu-id="662c3-211">Numeric</span></span> | <span data-ttu-id="662c3-212">Anzahl der Empfänger, die den Auftrag markiert haben</span><span class="sxs-lookup"><span data-stu-id="662c3-212">Number of assignees who have marked the job complete</span></span> |
| <span data-ttu-id="662c3-213">isCompleted</span><span class="sxs-lookup"><span data-stu-id="662c3-213">isCompleted</span></span> | <span data-ttu-id="662c3-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="662c3-214">Boolean</span></span> | <span data-ttu-id="662c3-215">True, wenn alle Empfänger den Auftrag abgeschlossen haben</span><span class="sxs-lookup"><span data-stu-id="662c3-215">True when all assignees have completed the job</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-216">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-216">Sample JSON Response:</span></span>

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
####  <a name="actionbody-object-structure-for-the-action-poll"></a><span data-ttu-id="662c3-217">actionBody-Objektstruktur für die Aktion "Umfrage":</span><span class="sxs-lookup"><span data-stu-id="662c3-217">actionBody object structure for the action 'Poll':</span></span>

| <span data-ttu-id="662c3-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-218">Parameter</span></span> | <span data-ttu-id="662c3-219">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-219">Type</span></span> | <span data-ttu-id="662c3-220">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-220">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-221">actionId</span><span class="sxs-lookup"><span data-stu-id="662c3-221">actionId</span></span> | <span data-ttu-id="662c3-222">String</span><span class="sxs-lookup"><span data-stu-id="662c3-222">String</span></span> | <span data-ttu-id="662c3-223">GUID, die die spezifische Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="662c3-223">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="662c3-224">Frage</span><span class="sxs-lookup"><span data-stu-id="662c3-224">question</span></span> | <span data-ttu-id="662c3-225">String</span><span class="sxs-lookup"><span data-stu-id="662c3-225">String</span></span> | <span data-ttu-id="662c3-226">Umfrage Frage</span><span class="sxs-lookup"><span data-stu-id="662c3-226">Poll Question</span></span> |
| <span data-ttu-id="662c3-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="662c3-227">isSenderOnly</span></span> | <span data-ttu-id="662c3-228">Boolean</span><span class="sxs-lookup"><span data-stu-id="662c3-228">Boolean</span></span> | <span data-ttu-id="662c3-229">True, wenn die Abstimmungs Zusammenfassung nur für Absender sichtbar ist</span><span class="sxs-lookup"><span data-stu-id="662c3-229">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="662c3-230">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="662c3-230">expiryDate</span></span> | <span data-ttu-id="662c3-231">DateTime</span><span class="sxs-lookup"><span data-stu-id="662c3-231">DateTime</span></span> | <span data-ttu-id="662c3-232">DateTime der Umfrage Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="662c3-232">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="662c3-233">Auswahlmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="662c3-233">Choices</span></span> | <span data-ttu-id="662c3-234">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="662c3-234">Json Array</span></span> | <span data-ttu-id="662c3-235">Liste der JSON-Objekte mit folgender Komponente</span><span class="sxs-lookup"><span data-stu-id="662c3-235">List of Json objects with following component</span></span> <ol><li><span data-ttu-id="662c3-236">Titel-Options Text</span><span class="sxs-lookup"><span data-stu-id="662c3-236">title - Option Text</span></span></li><li><span data-ttu-id="662c3-237">Image-Optionsbild</span><span class="sxs-lookup"><span data-stu-id="662c3-237">image - Option Image</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-238">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-238">Sample JSON Response:</span></span>

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
####  <a name="actionbody-object-structure-for-the-action-lets-meet"></a><span data-ttu-id="662c3-239">actionBody-Objektstruktur für die Aktion ' Let es Meet ':</span><span class="sxs-lookup"><span data-stu-id="662c3-239">actionBody object structure for the action 'Let's Meet':</span></span>

| <span data-ttu-id="662c3-240">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-240">Parameter</span></span> | <span data-ttu-id="662c3-241">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-241">Type</span></span> | <span data-ttu-id="662c3-242">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-242">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-243">actionId</span><span class="sxs-lookup"><span data-stu-id="662c3-243">actionId</span></span> | <span data-ttu-id="662c3-244">String</span><span class="sxs-lookup"><span data-stu-id="662c3-244">String</span></span> | <span data-ttu-id="662c3-245">GUID, die die spezifische Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="662c3-245">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="662c3-246">title</span><span class="sxs-lookup"><span data-stu-id="662c3-246">title</span></span> | <span data-ttu-id="662c3-247">String</span><span class="sxs-lookup"><span data-stu-id="662c3-247">String</span></span> | <span data-ttu-id="662c3-248">Titel der Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="662c3-248">Title of the Meeting request</span></span> |
| <span data-ttu-id="662c3-249">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="662c3-249">isSenderOnly</span></span> | <span data-ttu-id="662c3-250">Boolean</span><span class="sxs-lookup"><span data-stu-id="662c3-250">Boolean</span></span> | <span data-ttu-id="662c3-251">True, wenn die Abstimmungs Zusammenfassung nur für Absender sichtbar ist</span><span class="sxs-lookup"><span data-stu-id="662c3-251">True when Poll Summary is visible only to sender</span></span> |
| <span data-ttu-id="662c3-252">duration</span><span class="sxs-lookup"><span data-stu-id="662c3-252">duration</span></span> | <span data-ttu-id="662c3-253">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="662c3-253">Integer</span></span> | <span data-ttu-id="662c3-254">Dauer der Besprechung (in Minuten)</span><span class="sxs-lookup"><span data-stu-id="662c3-254">Duration of the meeting (in mins)</span></span> |
| <span data-ttu-id="662c3-255">Agendas</span><span class="sxs-lookup"><span data-stu-id="662c3-255">agenda</span></span> | <span data-ttu-id="662c3-256">String</span><span class="sxs-lookup"><span data-stu-id="662c3-256">String</span></span> | <span data-ttu-id="662c3-257">TagesOrdnungs Satz für die Besprechung</span><span class="sxs-lookup"><span data-stu-id="662c3-257">Agenda set for the meeting</span></span> |
| <span data-ttu-id="662c3-258">Startzeit</span><span class="sxs-lookup"><span data-stu-id="662c3-258">startingTime</span></span> | <span data-ttu-id="662c3-259">DateTime</span><span class="sxs-lookup"><span data-stu-id="662c3-259">DateTime</span></span> | <span data-ttu-id="662c3-260">DateTime der Umfrage Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="662c3-260">DateTime of the Poll expiry time</span></span> |
| <span data-ttu-id="662c3-261">Compliance</span><span class="sxs-lookup"><span data-stu-id="662c3-261">Place</span></span> | <span data-ttu-id="662c3-262">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="662c3-262">Json Object</span></span> | <span data-ttu-id="662c3-263">Standortdaten mit folgender Komponente</span><span class="sxs-lookup"><span data-stu-id="662c3-263">Location Data with following component</span></span> <ol><li><span data-ttu-id="662c3-264">Latitude</span><span class="sxs-lookup"><span data-stu-id="662c3-264">Latitude</span></span></li><li><span data-ttu-id="662c3-265">Längengrad</span><span class="sxs-lookup"><span data-stu-id="662c3-265">Longitude</span></span></li><li><span data-ttu-id="662c3-266">name</span><span class="sxs-lookup"><span data-stu-id="662c3-266">name</span></span></li></ol> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-267">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-267">Sample JSON Response:</span></span>

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


####  <a name="actionbody-object-structure-for-the-action-survey"></a><span data-ttu-id="662c3-268">actionBody-Objektstruktur für die Aktion "Survey":</span><span class="sxs-lookup"><span data-stu-id="662c3-268">actionBody object structure for the action 'Survey':</span></span>

| <span data-ttu-id="662c3-269">Parameter</span><span class="sxs-lookup"><span data-stu-id="662c3-269">Parameter</span></span> | <span data-ttu-id="662c3-270">Typ</span><span class="sxs-lookup"><span data-stu-id="662c3-270">Type</span></span> | <span data-ttu-id="662c3-271">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662c3-271">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="662c3-272">actionId</span><span class="sxs-lookup"><span data-stu-id="662c3-272">actionId</span></span> | <span data-ttu-id="662c3-273">String</span><span class="sxs-lookup"><span data-stu-id="662c3-273">String</span></span> | <span data-ttu-id="662c3-274">GUID, die die spezifische Aktionsinstanz darstellt</span><span class="sxs-lookup"><span data-stu-id="662c3-274">GUID representing the specific action instance</span></span> |
| <span data-ttu-id="662c3-275">title</span><span class="sxs-lookup"><span data-stu-id="662c3-275">title</span></span> | <span data-ttu-id="662c3-276">String</span><span class="sxs-lookup"><span data-stu-id="662c3-276">String</span></span> | <span data-ttu-id="662c3-277">Titel der Umfrage</span><span class="sxs-lookup"><span data-stu-id="662c3-277">Title of the Survey</span></span> |
| <span data-ttu-id="662c3-278">responseCount</span><span class="sxs-lookup"><span data-stu-id="662c3-278">responseCount</span></span> | <span data-ttu-id="662c3-279">Numeric</span><span class="sxs-lookup"><span data-stu-id="662c3-279">Numeric</span></span> | <span data-ttu-id="662c3-280">Anzahl der Personen, die auf die Umfrage geantwortet haben</span><span class="sxs-lookup"><span data-stu-id="662c3-280">Number of people who responded to the Survey</span></span> |
| <span data-ttu-id="662c3-281">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="662c3-281">expiryDate</span></span> | <span data-ttu-id="662c3-282">DateTime</span><span class="sxs-lookup"><span data-stu-id="662c3-282">DateTime</span></span> | <span data-ttu-id="662c3-283">DateTime der Umfrage Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="662c3-283">DateTime of the Survey expiry time</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="662c3-284">JSON-Beispielantwort:</span><span class="sxs-lookup"><span data-stu-id="662c3-284">Sample JSON Response:</span></span>

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

<span data-ttu-id="662c3-285">Als nächstes: Sie können weitere Details der einzelnen Aktionsinstanzen mit der entsprechenden Aktions-Nr. abrufen.</span><span class="sxs-lookup"><span data-stu-id="662c3-285">Next: You can retrieve further details of each action instance with the corresponding actionId.</span></span> [<span data-ttu-id="662c3-286">API zum Abrufen von Details zur Aktionsinstanz</span><span class="sxs-lookup"><span data-stu-id="662c3-286">API for retrieving Action instance Details</span></span>](actionDetails.md)
