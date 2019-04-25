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
# <a name="reaction"></a><span data-ttu-id="c8b91-103">/Reaction</span><span class="sxs-lookup"><span data-stu-id="c8b91-103">/reaction</span></span>
<span data-ttu-id="c8b91-104">API-Endpunkt zum Abfragen von Reaktions Daten für alle in einer Gruppe gesendeten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="c8b91-104">API end-point to query reactions data on any Action sent in a group.</span></span>

## <a name="post-reaction"></a><span data-ttu-id="c8b91-105">POST/Reaction</span><span class="sxs-lookup"><span data-stu-id="c8b91-105">POST /reaction</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a><span data-ttu-id="c8b91-106">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-106">Request Parameters</span></span>

| | <span data-ttu-id="c8b91-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-107">Parameter</span></span> | <span data-ttu-id="c8b91-108">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-108">Type</span></span> | <span data-ttu-id="c8b91-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="c8b91-109">Optional?</span></span> | <span data-ttu-id="c8b91-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-110">Description</span></span> |
| :---: | :---: | :---: | :---  | :--- |
| <span data-ttu-id="c8b91-111">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-111">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-112">groupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-112">groupId</span></span> | <span data-ttu-id="c8b91-113">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-113">String</span></span> | <span data-ttu-id="c8b91-114">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-114">No</span></span> | <span data-ttu-id="c8b91-115">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="c8b91-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c8b91-116">HTTP Header</span></span> | <span data-ttu-id="c8b91-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="c8b91-117">accessToken</span></span> | <span data-ttu-id="c8b91-118">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-118">String</span></span> | <span data-ttu-id="c8b91-119">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-119">No</span></span> | <span data-ttu-id="c8b91-120">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="c8b91-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="c8b91-121">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c8b91-121">HTTP Header</span></span> | <span data-ttu-id="c8b91-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c8b91-122">Content-Type</span></span> | <span data-ttu-id="c8b91-123">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-123">String</span></span> | <span data-ttu-id="c8b91-124">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-124">No</span></span> | <span data-ttu-id="c8b91-125">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="c8b91-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="c8b91-126">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="c8b91-126">Request body</span></span>

| <span data-ttu-id="c8b91-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-127">Parameter</span></span> | <span data-ttu-id="c8b91-128">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-128">Type</span></span> | <span data-ttu-id="c8b91-129">Optional?</span><span class="sxs-lookup"><span data-stu-id="c8b91-129">Optional?</span></span> | <span data-ttu-id="c8b91-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="c8b91-131">referenceId</span><span class="sxs-lookup"><span data-stu-id="c8b91-131">referenceId</span></span> | <span data-ttu-id="c8b91-132">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-132">String</span></span> | <span data-ttu-id="c8b91-133">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-133">No</span></span> | <span data-ttu-id="c8b91-134">GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-134">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="c8b91-135">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-135">sourceGroupId</span></span> | <span data-ttu-id="c8b91-136">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-136">String</span></span> | <span data-ttu-id="c8b91-137">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-137">No</span></span> | <span data-ttu-id="c8b91-138">GUID der Gruppe, in der die Aktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b91-138">GUID of the group in which the Action has been sent.</span></span> <span data-ttu-id="c8b91-139">Bei Gruppen, bei denen es sich um eine Untergruppe einer anderen Gruppe handelt, kann dies von der im URL-Pfad-Parameter angegebenen Gruppierung</span><span class="sxs-lookup"><span data-stu-id="c8b91-139">In case of groups which is a subgroup of another group, this may differ from 'groupId' provided in the url Path parameter</span></span>|
| <span data-ttu-id="c8b91-140">reactiontype</span><span class="sxs-lookup"><span data-stu-id="c8b91-140">reactionType</span></span> | <span data-ttu-id="c8b91-141">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-141">String</span></span> | <span data-ttu-id="c8b91-142">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-142">No</span></span> | <span data-ttu-id="c8b91-143">Enumerationswert: ' like '/' Comment '</span><span class="sxs-lookup"><span data-stu-id="c8b91-143">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="c8b91-144">comment</span><span class="sxs-lookup"><span data-stu-id="c8b91-144">comment</span></span> | <span data-ttu-id="c8b91-145">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-145">String</span></span> | <span data-ttu-id="c8b91-146">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-146">No</span></span> | <span data-ttu-id="c8b91-147">Kommentartext ist nur für reactiontype "comment" obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="c8b91-147">Comment text is mandatory only for reactionType 'Comment'.</span></span> <span data-ttu-id="c8b91-148">Für "like" sollte dies ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8b91-148">For 'Like', this should be ignored</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="c8b91-149">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="c8b91-149">Sample JSON Request</span></span>

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a><span data-ttu-id="c8b91-150">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c8b91-150">Response body</span></span>

| <span data-ttu-id="c8b91-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-151">Parameter</span></span> | <span data-ttu-id="c8b91-152">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-152">Type</span></span> | <span data-ttu-id="c8b91-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-154">Reaction-Nr.</span><span class="sxs-lookup"><span data-stu-id="c8b91-154">reactionId</span></span> | <span data-ttu-id="c8b91-155">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-155">String</span></span> | <span data-ttu-id="c8b91-156">GUID, die die ID der Reaktions Entität nach erfolgreichem Abschluss der Anforderung darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-156">GUID representing the id for reaction entity after successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="c8b91-157">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="c8b91-157">Sample JSON Response</span></span>

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a><span data-ttu-id="c8b91-158">/Reaction-Zusammenfassung auf Aktionsebene abrufen</span><span class="sxs-lookup"><span data-stu-id="c8b91-158">GET /reaction summary at Action level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a><span data-ttu-id="c8b91-159">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-159">Request Parameters</span></span>

|  | <span data-ttu-id="c8b91-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-160">Parameter</span></span> | <span data-ttu-id="c8b91-161">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-161">Type</span></span> | <span data-ttu-id="c8b91-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="c8b91-162">Optional?</span></span> | <span data-ttu-id="c8b91-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-163">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c8b91-164">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-164">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-165">groupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-165">groupId</span></span> | <span data-ttu-id="c8b91-166">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-166">String</span></span> | <span data-ttu-id="c8b91-167">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-167">No</span></span> | <span data-ttu-id="c8b91-168">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-168">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="c8b91-169">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-169">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-170">referenceId</span><span class="sxs-lookup"><span data-stu-id="c8b91-170">referenceId</span></span> | <span data-ttu-id="c8b91-171">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-171">String</span></span> | <span data-ttu-id="c8b91-172">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-172">No</span></span> | <span data-ttu-id="c8b91-173">GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-173">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="c8b91-174">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-174">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-175">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-175">sourceGroupId</span></span> | <span data-ttu-id="c8b91-176">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-176">String</span></span> | <span data-ttu-id="c8b91-177">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-177">No</span></span> | <span data-ttu-id="c8b91-178">GUID der Gruppe, in der die Aktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b91-178">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="c8b91-179">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c8b91-179">HTTP Header</span></span> | <span data-ttu-id="c8b91-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="c8b91-180">accessToken</span></span> | <span data-ttu-id="c8b91-181">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-181">String</span></span> | <span data-ttu-id="c8b91-182">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-182">No</span></span> | <span data-ttu-id="c8b91-183">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="c8b91-183">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="c8b91-184">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c8b91-184">Response body</span></span>

| <span data-ttu-id="c8b91-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-185">Parameter</span></span> | <span data-ttu-id="c8b91-186">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-186">Type</span></span> | <span data-ttu-id="c8b91-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-188">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c8b91-188">summary</span></span> | <span data-ttu-id="c8b91-189">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="c8b91-189">JSON Array</span></span> | <span data-ttu-id="c8b91-190">Array von JSON-Objekten, die die Zusammenfassung der Reaktionen für eine in einer Gruppe gesendete Aktion darstellen</span><span class="sxs-lookup"><span data-stu-id="c8b91-190">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

### <a name="response-body-summary-object"></a><span data-ttu-id="c8b91-191">Antworttext-Zusammenfassungs Objekt</span><span class="sxs-lookup"><span data-stu-id="c8b91-191">Response body summary object</span></span>

| <span data-ttu-id="c8b91-192">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-192">Parameter</span></span> | <span data-ttu-id="c8b91-193">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-193">Type</span></span> | <span data-ttu-id="c8b91-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-195">referenceId</span><span class="sxs-lookup"><span data-stu-id="c8b91-195">referenceId</span></span> | <span data-ttu-id="c8b91-196">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-196">String</span></span> | <span data-ttu-id="c8b91-197">GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-197">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="c8b91-198">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="c8b91-198">reactionsCountMap</span></span> | <span data-ttu-id="c8b91-199">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="c8b91-199">Json object</span></span> | <span data-ttu-id="c8b91-200">JSON-Objekt mit likes-und comments-Anzahl für diesen Verweistyp</span><span class="sxs-lookup"><span data-stu-id="c8b91-200">Json object containing Likes and comments count for that referenceId</span></span> |


### <a name="sample-json-response"></a><span data-ttu-id="c8b91-201">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="c8b91-201">Sample JSON Response</span></span>

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

## <a name="get-reaction-summary-at-group-level"></a><span data-ttu-id="c8b91-202">/Reaction-Zusammenfassung auf Gruppenebene abrufen</span><span class="sxs-lookup"><span data-stu-id="c8b91-202">GET /reaction summary at group level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="c8b91-203">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-203">Request Parameters</span></span>

|  | <span data-ttu-id="c8b91-204">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-204">Parameter</span></span> | <span data-ttu-id="c8b91-205">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-205">Type</span></span> | <span data-ttu-id="c8b91-206">Optional?</span><span class="sxs-lookup"><span data-stu-id="c8b91-206">Optional?</span></span> | <span data-ttu-id="c8b91-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-207">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c8b91-208">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-208">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-209">groupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-209">groupId</span></span> | <span data-ttu-id="c8b91-210">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-210">String</span></span> | <span data-ttu-id="c8b91-211">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-211">No</span></span> | <span data-ttu-id="c8b91-212">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-212">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="c8b91-213">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-213">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-214">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-214">sourceGroupId</span></span> | <span data-ttu-id="c8b91-215">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-215">String</span></span> | <span data-ttu-id="c8b91-216">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-216">No</span></span> | <span data-ttu-id="c8b91-217">GUID der Gruppe, in der die Aktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b91-217">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="c8b91-218">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-218">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-219">Cursor</span><span class="sxs-lookup"><span data-stu-id="c8b91-219">cursor</span></span> | <span data-ttu-id="c8b91-220">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c8b91-220">timeStamp</span></span> | <span data-ttu-id="c8b91-221">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-221">No</span></span> | <span data-ttu-id="c8b91-222">Zeitstempel, aus dem die Zusammenfassung berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8b91-222">timeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="c8b91-223">Standardwert 0</span><span class="sxs-lookup"><span data-stu-id="c8b91-223">Default value 0</span></span> |
| <span data-ttu-id="c8b91-224">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c8b91-224">HTTP Header</span></span> | <span data-ttu-id="c8b91-225">accessToken</span><span class="sxs-lookup"><span data-stu-id="c8b91-225">accessToken</span></span> | <span data-ttu-id="c8b91-226">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-226">String</span></span> | <span data-ttu-id="c8b91-227">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-227">No</span></span> | <span data-ttu-id="c8b91-228">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="c8b91-228">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="c8b91-229">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c8b91-229">Response body</span></span>

| <span data-ttu-id="c8b91-230">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-230">Parameter</span></span> | <span data-ttu-id="c8b91-231">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-231">Type</span></span> | <span data-ttu-id="c8b91-232">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-232">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-233">Cursor</span><span class="sxs-lookup"><span data-stu-id="c8b91-233">cursor</span></span> | <span data-ttu-id="c8b91-234">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c8b91-234">timeStamp</span></span> | <span data-ttu-id="c8b91-235">Zeitstempel, bis die Zusammenfassung berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b91-235">timeStamp till which summary has been calculated.</span></span> <span data-ttu-id="c8b91-236">Nächster Satz von reactionSummary kann mit diesem Cursor Wert generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8b91-236">Next set of reactionSummary can be generated using this cursor value</span></span> |
| <span data-ttu-id="c8b91-237">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c8b91-237">summary</span></span> | <span data-ttu-id="c8b91-238">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="c8b91-238">JSON Array</span></span> | <span data-ttu-id="c8b91-239">Array von JSON-Objekten, die die Zusammenfassung der Reaktionen für eine in einer Gruppe gesendete Aktion darstellen</span><span class="sxs-lookup"><span data-stu-id="c8b91-239">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="c8b91-240">Antworttext-Zusammenfassungs Objekt</span><span class="sxs-lookup"><span data-stu-id="c8b91-240">Response body summary object</span></span>

| <span data-ttu-id="c8b91-241">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-241">Parameter</span></span> | <span data-ttu-id="c8b91-242">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-242">Type</span></span> | <span data-ttu-id="c8b91-243">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-244">referenceId</span><span class="sxs-lookup"><span data-stu-id="c8b91-244">referenceId</span></span> | <span data-ttu-id="c8b91-245">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-245">String</span></span> | <span data-ttu-id="c8b91-246">GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-246">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="c8b91-247">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="c8b91-247">reactionsCountMap</span></span> | <span data-ttu-id="c8b91-248">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="c8b91-248">Json object</span></span> | <span data-ttu-id="c8b91-249">JSON-Objekt mit likes-und comments-Anzahl für diesen Verweistyp</span><span class="sxs-lookup"><span data-stu-id="c8b91-249">Json object containing Likes and comments count for that referenceId</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="c8b91-250">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="c8b91-250">Sample JSON Response</span></span>

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

## <a name="get-reaction-details-for-a-action"></a><span data-ttu-id="c8b91-251">Abrufen von/Reaction-Details für eine Aktion</span><span class="sxs-lookup"><span data-stu-id="c8b91-251">GET /reaction details for a Action</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="c8b91-252">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-252">Request Parameters</span></span>

|  | <span data-ttu-id="c8b91-253">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-253">Parameter</span></span> | <span data-ttu-id="c8b91-254">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-254">Type</span></span> | <span data-ttu-id="c8b91-255">Optional?</span><span class="sxs-lookup"><span data-stu-id="c8b91-255">Optional?</span></span> | <span data-ttu-id="c8b91-256">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c8b91-257">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-257">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-258">groupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-258">groupId</span></span> | <span data-ttu-id="c8b91-259">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-259">String</span></span> | <span data-ttu-id="c8b91-260">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-260">No</span></span> | <span data-ttu-id="c8b91-261">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-261">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="c8b91-262">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-262">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-263">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c8b91-263">sourceGroupId</span></span> | <span data-ttu-id="c8b91-264">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-264">String</span></span> | <span data-ttu-id="c8b91-265">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-265">No</span></span> | <span data-ttu-id="c8b91-266">GUID der Gruppe, in der die Aktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b91-266">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="c8b91-267">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-267">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-268">referenceId</span><span class="sxs-lookup"><span data-stu-id="c8b91-268">referenceId</span></span> | <span data-ttu-id="c8b91-269">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-269">String</span></span> | <span data-ttu-id="c8b91-270">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-270">No</span></span> | <span data-ttu-id="c8b91-271">GUID, die die ID für den Entitätsverweis darstellt, der eine Aktion darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-271">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="c8b91-272">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-272">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-273">reactiontype</span><span class="sxs-lookup"><span data-stu-id="c8b91-273">reactionType</span></span> | <span data-ttu-id="c8b91-274">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-274">String</span></span> | <span data-ttu-id="c8b91-275">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-275">No</span></span> | <span data-ttu-id="c8b91-276">Enumerationswert: ' like '/' Comment '</span><span class="sxs-lookup"><span data-stu-id="c8b91-276">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="c8b91-277">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-277">URL Path Parameter</span></span> | <span data-ttu-id="c8b91-278">Cursor</span><span class="sxs-lookup"><span data-stu-id="c8b91-278">cursor</span></span> | <span data-ttu-id="c8b91-279">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c8b91-279">TimeStamp</span></span> | <span data-ttu-id="c8b91-280">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-280">No</span></span> | <span data-ttu-id="c8b91-281">Zeitstempel, aus dem die Zusammenfassung berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8b91-281">TimeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="c8b91-282">Standardwert 0</span><span class="sxs-lookup"><span data-stu-id="c8b91-282">Default value 0</span></span> |
| <span data-ttu-id="c8b91-283">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c8b91-283">HTTP Header</span></span> | <span data-ttu-id="c8b91-284">accessToken</span><span class="sxs-lookup"><span data-stu-id="c8b91-284">accessToken</span></span> | <span data-ttu-id="c8b91-285">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-285">String</span></span> | <span data-ttu-id="c8b91-286">Nein</span><span class="sxs-lookup"><span data-stu-id="c8b91-286">No</span></span> | <span data-ttu-id="c8b91-287">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="c8b91-287">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="c8b91-288">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c8b91-288">Response body</span></span>

| <span data-ttu-id="c8b91-289">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-289">Parameter</span></span> | <span data-ttu-id="c8b91-290">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-290">Type</span></span> | <span data-ttu-id="c8b91-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-291">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-292">Cursor</span><span class="sxs-lookup"><span data-stu-id="c8b91-292">cursor</span></span> | <span data-ttu-id="c8b91-293">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c8b91-293">TimeStamp</span></span> | <span data-ttu-id="c8b91-294">Zeitstempel, bis zu dem reactionDetail bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b91-294">TimeStamp till which reactionDetail has been provided.</span></span> <span data-ttu-id="c8b91-295">Nächster Satz von reactionDetails kann mit diesem Cursor Wert generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8b91-295">Next set of reactionDetails can be generated using this cursor value</span></span> |
| <span data-ttu-id="c8b91-296">reactionDetails</span><span class="sxs-lookup"><span data-stu-id="c8b91-296">reactionDetails</span></span> | <span data-ttu-id="c8b91-297">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="c8b91-297">JSON Array</span></span> | <span data-ttu-id="c8b91-298">Array von JSON-Objekten, die alle Reaktionen auf eine in einer Gruppe gesendete Aktion darstellen.</span><span class="sxs-lookup"><span data-stu-id="c8b91-298">Array of JSON objects each representing reactions detail on an Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="c8b91-299">Antworttext-Zusammenfassungs Objekt</span><span class="sxs-lookup"><span data-stu-id="c8b91-299">Response body summary object</span></span>

| <span data-ttu-id="c8b91-300">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b91-300">Parameter</span></span> | <span data-ttu-id="c8b91-301">Typ</span><span class="sxs-lookup"><span data-stu-id="c8b91-301">Type</span></span> | <span data-ttu-id="c8b91-302">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b91-302">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c8b91-303">Reaction-Nr.</span><span class="sxs-lookup"><span data-stu-id="c8b91-303">reactionId</span></span> | <span data-ttu-id="c8b91-304">String</span><span class="sxs-lookup"><span data-stu-id="c8b91-304">String</span></span> | <span data-ttu-id="c8b91-305">GUID, die die ID für die Reaktion darstellt, die auf einer Referenz erstellt wurde, die eine Aktion darstellt</span><span class="sxs-lookup"><span data-stu-id="c8b91-305">GUID representing the id for reaction created on referenceId representing an Action</span></span> |
| <span data-ttu-id="c8b91-306">userId</span><span class="sxs-lookup"><span data-stu-id="c8b91-306">userId</span></span> | <span data-ttu-id="c8b91-307">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="c8b91-307">Json object</span></span> | <span data-ttu-id="c8b91-308">UserId für den Benutzer, der die Reaktion auf eine Aktion erstellt hat</span><span class="sxs-lookup"><span data-stu-id="c8b91-308">UserId for the user who has created the reaction on an Action</span></span> |
| <span data-ttu-id="c8b91-309">lastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="c8b91-309">lastModifiedTime</span></span> | <span data-ttu-id="c8b91-310">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c8b91-310">Timestamp</span></span> | <span data-ttu-id="c8b91-311">Zeitstempel, an dem die Reaktion erstellt/aktualisiert wurde</span><span class="sxs-lookup"><span data-stu-id="c8b91-311">Timestamp at which reaction was created/updated</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="c8b91-312">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="c8b91-312">Sample JSON Response</span></span>

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