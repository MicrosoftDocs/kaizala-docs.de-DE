---
title: /Reaction
description: Referenzartikel für Reaktionen auf eine beliebige Aktion in einer Gruppe gesendet Abfrage-API
topic: Reference
author: nitinjms
ms.openlocfilehash: a0c86aac9dd70e4c72e177f64c6e2dcaeeb8b41c
ms.sourcegitcommit: 9ac64dcb3ef72a84589483e45ae8e528aaa5aa4c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2018
ms.locfileid: "20457304"
---
# <a name="reaction"></a><span data-ttu-id="bf161-103">/Reaction</span><span class="sxs-lookup"><span data-stu-id="bf161-103">/reaction</span></span>
<span data-ttu-id="bf161-104">API-Endpunkt auf Abfrage Reaktionen Daten für alle Aktionen, die in einer Gruppe gesendet.</span><span class="sxs-lookup"><span data-stu-id="bf161-104">API end-point to query reactions data on any Action sent in a group.</span></span>

## <a name="post-reaction"></a><span data-ttu-id="bf161-105">POST-/reaction</span><span class="sxs-lookup"><span data-stu-id="bf161-105">POST /reaction</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a><span data-ttu-id="bf161-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="bf161-106">Request Parameters</span></span>

| | <span data-ttu-id="bf161-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-107">Parameter</span></span> | <span data-ttu-id="bf161-108">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-108">Type</span></span> | <span data-ttu-id="bf161-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="bf161-109">Optional?</span></span> | <span data-ttu-id="bf161-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-110">Description</span></span> |
| :---: | :---: | :---: | :---  | :--- |
| <span data-ttu-id="bf161-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-111">URL Path Parameter</span></span> | <span data-ttu-id="bf161-112">groupId</span><span class="sxs-lookup"><span data-stu-id="bf161-112">groupId</span></span> | <span data-ttu-id="bf161-113">String</span><span class="sxs-lookup"><span data-stu-id="bf161-113">String</span></span> | <span data-ttu-id="bf161-114">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-114">No</span></span> | <span data-ttu-id="bf161-115">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="bf161-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="bf161-116">HTTP Header</span></span> | <span data-ttu-id="bf161-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="bf161-117">accessToken</span></span> | <span data-ttu-id="bf161-118">String</span><span class="sxs-lookup"><span data-stu-id="bf161-118">String</span></span> | <span data-ttu-id="bf161-119">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-119">No</span></span> | <span data-ttu-id="bf161-120">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="bf161-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="bf161-121">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="bf161-121">HTTP Header</span></span> | <span data-ttu-id="bf161-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bf161-122">Content-Type</span></span> | <span data-ttu-id="bf161-123">String</span><span class="sxs-lookup"><span data-stu-id="bf161-123">String</span></span> | <span data-ttu-id="bf161-124">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-124">No</span></span> | <span data-ttu-id="bf161-125">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="bf161-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="bf161-126">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="bf161-126">Request body</span></span>

| <span data-ttu-id="bf161-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-127">Parameter</span></span> | <span data-ttu-id="bf161-128">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-128">Type</span></span> | <span data-ttu-id="bf161-129">Optional?</span><span class="sxs-lookup"><span data-stu-id="bf161-129">Optional?</span></span> | <span data-ttu-id="bf161-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="bf161-131">referenceId</span><span class="sxs-lookup"><span data-stu-id="bf161-131">referenceId</span></span> | <span data-ttu-id="bf161-132">String</span><span class="sxs-lookup"><span data-stu-id="bf161-132">String</span></span> | <span data-ttu-id="bf161-133">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-133">No</span></span> | <span data-ttu-id="bf161-134">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-134">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="bf161-135">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bf161-135">sourceGroupId</span></span> | <span data-ttu-id="bf161-136">String</span><span class="sxs-lookup"><span data-stu-id="bf161-136">String</span></span> | <span data-ttu-id="bf161-137">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-137">No</span></span> | <span data-ttu-id="bf161-138">Die GUID der Gruppe in der die Aktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf161-138">GUID of the group in which the Action has been sent.</span></span> <span data-ttu-id="bf161-139">Im Fall eines WAN-Gruppen, die eine Untergruppe einer anderen Gruppe ist, kann dies von 'GroupId' in der Url bereitgestellt abweichen Path-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-139">In case of groups which is a subgroup of another group, this may differ from 'groupId' provided in the url Path parameter</span></span>|
| <span data-ttu-id="bf161-140">reactionType</span><span class="sxs-lookup"><span data-stu-id="bf161-140">reactionType</span></span> | <span data-ttu-id="bf161-141">String</span><span class="sxs-lookup"><span data-stu-id="bf161-141">String</span></span> | <span data-ttu-id="bf161-142">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-142">No</span></span> | <span data-ttu-id="bf161-143">Enum-Wert: 'Like "/" abgeben'</span><span class="sxs-lookup"><span data-stu-id="bf161-143">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="bf161-144">comment</span><span class="sxs-lookup"><span data-stu-id="bf161-144">comment</span></span> | <span data-ttu-id="bf161-145">String</span><span class="sxs-lookup"><span data-stu-id="bf161-145">String</span></span> | <span data-ttu-id="bf161-146">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-146">No</span></span> | <span data-ttu-id="bf161-147">Kommentartext ist nur für ReactionType 'Comment' obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="bf161-147">Comment text is mandatory only for reactionType 'Comment'.</span></span> <span data-ttu-id="bf161-148">Für sollen "Like" dies ignoriert werden</span><span class="sxs-lookup"><span data-stu-id="bf161-148">For 'Like', this should be ignored</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="bf161-149">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf161-149">Sample JSON Request</span></span>

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a><span data-ttu-id="bf161-150">Antworttext</span><span class="sxs-lookup"><span data-stu-id="bf161-150">Response body</span></span>

| <span data-ttu-id="bf161-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-151">Parameter</span></span> | <span data-ttu-id="bf161-152">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-152">Type</span></span> | <span data-ttu-id="bf161-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-154">reactionId</span><span class="sxs-lookup"><span data-stu-id="bf161-154">reactionId</span></span> | <span data-ttu-id="bf161-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf161-155">String</span></span> | <span data-ttu-id="bf161-156">GUID, die die Id für Reaktion Entität nach dem erfolgreichen Abschluss der Anforderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-156">GUID representing the id for reaction entity after successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="bf161-157">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="bf161-157">Sample JSON Response</span></span>

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a><span data-ttu-id="bf161-158">/Reaction Aktion Ebene Zusammenfassung abrufen</span><span class="sxs-lookup"><span data-stu-id="bf161-158">GET /reaction summary at Action level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a><span data-ttu-id="bf161-159">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="bf161-159">Request Parameters</span></span>

|  | <span data-ttu-id="bf161-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-160">Parameter</span></span> | <span data-ttu-id="bf161-161">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-161">Type</span></span> | <span data-ttu-id="bf161-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="bf161-162">Optional?</span></span> | <span data-ttu-id="bf161-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-163">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="bf161-164">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-164">URL Path Parameter</span></span> | <span data-ttu-id="bf161-165">groupId</span><span class="sxs-lookup"><span data-stu-id="bf161-165">groupId</span></span> | <span data-ttu-id="bf161-166">String</span><span class="sxs-lookup"><span data-stu-id="bf161-166">String</span></span> | <span data-ttu-id="bf161-167">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-167">No</span></span> | <span data-ttu-id="bf161-168">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-168">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="bf161-169">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-169">URL Path Parameter</span></span> | <span data-ttu-id="bf161-170">referenceId</span><span class="sxs-lookup"><span data-stu-id="bf161-170">referenceId</span></span> | <span data-ttu-id="bf161-171">String</span><span class="sxs-lookup"><span data-stu-id="bf161-171">String</span></span> | <span data-ttu-id="bf161-172">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-172">No</span></span> | <span data-ttu-id="bf161-173">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-173">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="bf161-174">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-174">URL Path Parameter</span></span> | <span data-ttu-id="bf161-175">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bf161-175">sourceGroupId</span></span> | <span data-ttu-id="bf161-176">String</span><span class="sxs-lookup"><span data-stu-id="bf161-176">String</span></span> | <span data-ttu-id="bf161-177">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-177">No</span></span> | <span data-ttu-id="bf161-178">Die GUID der Gruppe, in der die Aktion gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="bf161-178">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="bf161-179">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="bf161-179">HTTP Header</span></span> | <span data-ttu-id="bf161-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="bf161-180">accessToken</span></span> | <span data-ttu-id="bf161-181">String</span><span class="sxs-lookup"><span data-stu-id="bf161-181">String</span></span> | <span data-ttu-id="bf161-182">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-182">No</span></span> | <span data-ttu-id="bf161-183">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="bf161-183">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="bf161-184">Antworttext</span><span class="sxs-lookup"><span data-stu-id="bf161-184">Response body</span></span>

| <span data-ttu-id="bf161-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-185">Parameter</span></span> | <span data-ttu-id="bf161-186">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-186">Type</span></span> | <span data-ttu-id="bf161-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-188">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bf161-188">summary</span></span> | <span data-ttu-id="bf161-189">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="bf161-189">JSON Array</span></span> | <span data-ttu-id="bf161-190">Array von JSON-Objekten jede Ereignisobjekten Reaktionen Zusammenfassung auf eine Aktion, die in einer Gruppe gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf161-190">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

### <a name="response-body-summary-object"></a><span data-ttu-id="bf161-191">Zusammenfassung Antwort Body-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-191">Response body summary object</span></span>

| <span data-ttu-id="bf161-192">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-192">Parameter</span></span> | <span data-ttu-id="bf161-193">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-193">Type</span></span> | <span data-ttu-id="bf161-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-195">referenceId</span><span class="sxs-lookup"><span data-stu-id="bf161-195">referenceId</span></span> | <span data-ttu-id="bf161-196">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf161-196">String</span></span> | <span data-ttu-id="bf161-197">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-197">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="bf161-198">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="bf161-198">reactionsCountMap</span></span> | <span data-ttu-id="bf161-199">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-199">Json object</span></span> | <span data-ttu-id="bf161-200">Mit "gefällt mir" und Kommentare Count für diese ReferenceId JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-200">Json object containing Likes and comments count for that referenceId</span></span> |


### <a name="sample-json-response"></a><span data-ttu-id="bf161-201">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="bf161-201">Sample JSON Response</span></span>

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

## <a name="get-reaction-summary-at-group-level"></a><span data-ttu-id="bf161-202">Abrufen einer Zusammenfassung /reaction auf Gruppenebene</span><span class="sxs-lookup"><span data-stu-id="bf161-202">GET /reaction summary at group level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="bf161-203">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="bf161-203">Request Parameters</span></span>

|  | <span data-ttu-id="bf161-204">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-204">Parameter</span></span> | <span data-ttu-id="bf161-205">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-205">Type</span></span> | <span data-ttu-id="bf161-206">Optional?</span><span class="sxs-lookup"><span data-stu-id="bf161-206">Optional?</span></span> | <span data-ttu-id="bf161-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-207">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="bf161-208">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-208">URL Path Parameter</span></span> | <span data-ttu-id="bf161-209">groupId</span><span class="sxs-lookup"><span data-stu-id="bf161-209">groupId</span></span> | <span data-ttu-id="bf161-210">String</span><span class="sxs-lookup"><span data-stu-id="bf161-210">String</span></span> | <span data-ttu-id="bf161-211">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-211">No</span></span> | <span data-ttu-id="bf161-212">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-212">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="bf161-213">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-213">URL Path Parameter</span></span> | <span data-ttu-id="bf161-214">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bf161-214">sourceGroupId</span></span> | <span data-ttu-id="bf161-215">String</span><span class="sxs-lookup"><span data-stu-id="bf161-215">String</span></span> | <span data-ttu-id="bf161-216">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-216">No</span></span> | <span data-ttu-id="bf161-217">Die GUID der Gruppe, in der die Aktion gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="bf161-217">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="bf161-218">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-218">URL Path Parameter</span></span> | <span data-ttu-id="bf161-219">Cursor</span><span class="sxs-lookup"><span data-stu-id="bf161-219">cursor</span></span> | <span data-ttu-id="bf161-220">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="bf161-220">timeStamp</span></span> | <span data-ttu-id="bf161-221">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-221">No</span></span> | <span data-ttu-id="bf161-222">Zeitstempel, aus denen die Zusammenfassung berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="bf161-222">timeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="bf161-223">Der Standardwert 0</span><span class="sxs-lookup"><span data-stu-id="bf161-223">Default value 0</span></span> |
| <span data-ttu-id="bf161-224">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="bf161-224">HTTP Header</span></span> | <span data-ttu-id="bf161-225">accessToken</span><span class="sxs-lookup"><span data-stu-id="bf161-225">accessToken</span></span> | <span data-ttu-id="bf161-226">String</span><span class="sxs-lookup"><span data-stu-id="bf161-226">String</span></span> | <span data-ttu-id="bf161-227">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-227">No</span></span> | <span data-ttu-id="bf161-228">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="bf161-228">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="bf161-229">Antworttext</span><span class="sxs-lookup"><span data-stu-id="bf161-229">Response body</span></span>

| <span data-ttu-id="bf161-230">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-230">Parameter</span></span> | <span data-ttu-id="bf161-231">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-231">Type</span></span> | <span data-ttu-id="bf161-232">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-232">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-233">Cursor</span><span class="sxs-lookup"><span data-stu-id="bf161-233">cursor</span></span> | <span data-ttu-id="bf161-234">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="bf161-234">timeStamp</span></span> | <span data-ttu-id="bf161-235">Zeitstempel, bis die Zusammenfassung berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf161-235">timeStamp till which summary has been calculated.</span></span> <span data-ttu-id="bf161-236">Nächsten Satzes von ReactionSummary kann mit dieser Wert Cursor generiert werden</span><span class="sxs-lookup"><span data-stu-id="bf161-236">Next set of reactionSummary can be generated using this cursor value</span></span> |
| <span data-ttu-id="bf161-237">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bf161-237">summary</span></span> | <span data-ttu-id="bf161-238">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="bf161-238">JSON Array</span></span> | <span data-ttu-id="bf161-239">Array von JSON-Objekten jede Ereignisobjekten Reaktionen Zusammenfassung auf eine Aktion, die in einer Gruppe gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf161-239">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="bf161-240">Zusammenfassung Antwort Body-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-240">Response body summary object</span></span>

| <span data-ttu-id="bf161-241">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-241">Parameter</span></span> | <span data-ttu-id="bf161-242">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-242">Type</span></span> | <span data-ttu-id="bf161-243">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-244">referenceId</span><span class="sxs-lookup"><span data-stu-id="bf161-244">referenceId</span></span> | <span data-ttu-id="bf161-245">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf161-245">String</span></span> | <span data-ttu-id="bf161-246">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-246">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="bf161-247">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="bf161-247">reactionsCountMap</span></span> | <span data-ttu-id="bf161-248">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-248">Json object</span></span> | <span data-ttu-id="bf161-249">Mit "gefällt mir" und Kommentare Count für diese ReferenceId JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-249">Json object containing Likes and comments count for that referenceId</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="bf161-250">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="bf161-250">Sample JSON Response</span></span>

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

## <a name="get-reaction-details-for-a-action"></a><span data-ttu-id="bf161-251">Hier erhalten Sie /reaction für eine Aktion</span><span class="sxs-lookup"><span data-stu-id="bf161-251">GET /reaction details for a Action</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="bf161-252">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="bf161-252">Request Parameters</span></span>

|  | <span data-ttu-id="bf161-253">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-253">Parameter</span></span> | <span data-ttu-id="bf161-254">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-254">Type</span></span> | <span data-ttu-id="bf161-255">Optional?</span><span class="sxs-lookup"><span data-stu-id="bf161-255">Optional?</span></span> | <span data-ttu-id="bf161-256">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="bf161-257">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-257">URL Path Parameter</span></span> | <span data-ttu-id="bf161-258">groupId</span><span class="sxs-lookup"><span data-stu-id="bf161-258">groupId</span></span> | <span data-ttu-id="bf161-259">String</span><span class="sxs-lookup"><span data-stu-id="bf161-259">String</span></span> | <span data-ttu-id="bf161-260">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-260">No</span></span> | <span data-ttu-id="bf161-261">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-261">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="bf161-262">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-262">URL Path Parameter</span></span> | <span data-ttu-id="bf161-263">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bf161-263">sourceGroupId</span></span> | <span data-ttu-id="bf161-264">String</span><span class="sxs-lookup"><span data-stu-id="bf161-264">String</span></span> | <span data-ttu-id="bf161-265">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-265">No</span></span> | <span data-ttu-id="bf161-266">Die GUID der Gruppe, in der die Aktion gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="bf161-266">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="bf161-267">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-267">URL Path Parameter</span></span> | <span data-ttu-id="bf161-268">referenceId</span><span class="sxs-lookup"><span data-stu-id="bf161-268">referenceId</span></span> | <span data-ttu-id="bf161-269">String</span><span class="sxs-lookup"><span data-stu-id="bf161-269">String</span></span> | <span data-ttu-id="bf161-270">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-270">No</span></span> | <span data-ttu-id="bf161-271">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-271">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="bf161-272">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-272">URL Path Parameter</span></span> | <span data-ttu-id="bf161-273">reactionType</span><span class="sxs-lookup"><span data-stu-id="bf161-273">reactionType</span></span> | <span data-ttu-id="bf161-274">String</span><span class="sxs-lookup"><span data-stu-id="bf161-274">String</span></span> | <span data-ttu-id="bf161-275">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-275">No</span></span> | <span data-ttu-id="bf161-276">Enum-Wert: 'Like "/" abgeben'</span><span class="sxs-lookup"><span data-stu-id="bf161-276">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="bf161-277">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-277">URL Path Parameter</span></span> | <span data-ttu-id="bf161-278">Cursor</span><span class="sxs-lookup"><span data-stu-id="bf161-278">cursor</span></span> | <span data-ttu-id="bf161-279">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="bf161-279">TimeStamp</span></span> | <span data-ttu-id="bf161-280">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-280">No</span></span> | <span data-ttu-id="bf161-281">Zeitstempel, aus denen die Zusammenfassung berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="bf161-281">TimeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="bf161-282">Der Standardwert 0</span><span class="sxs-lookup"><span data-stu-id="bf161-282">Default value 0</span></span> |
| <span data-ttu-id="bf161-283">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="bf161-283">HTTP Header</span></span> | <span data-ttu-id="bf161-284">accessToken</span><span class="sxs-lookup"><span data-stu-id="bf161-284">accessToken</span></span> | <span data-ttu-id="bf161-285">String</span><span class="sxs-lookup"><span data-stu-id="bf161-285">String</span></span> | <span data-ttu-id="bf161-286">Nein</span><span class="sxs-lookup"><span data-stu-id="bf161-286">No</span></span> | <span data-ttu-id="bf161-287">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="bf161-287">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="bf161-288">Antworttext</span><span class="sxs-lookup"><span data-stu-id="bf161-288">Response body</span></span>

| <span data-ttu-id="bf161-289">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-289">Parameter</span></span> | <span data-ttu-id="bf161-290">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-290">Type</span></span> | <span data-ttu-id="bf161-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-291">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-292">Cursor</span><span class="sxs-lookup"><span data-stu-id="bf161-292">cursor</span></span> | <span data-ttu-id="bf161-293">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="bf161-293">TimeStamp</span></span> | <span data-ttu-id="bf161-294">Zeitstempel, bis die ReactionDetail bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf161-294">TimeStamp till which reactionDetail has been provided.</span></span> <span data-ttu-id="bf161-295">Nächsten Satzes von ReactionDetails kann mit dieser Wert Cursor generiert werden</span><span class="sxs-lookup"><span data-stu-id="bf161-295">Next set of reactionDetails can be generated using this cursor value</span></span> |
| <span data-ttu-id="bf161-296">reactionDetails</span><span class="sxs-lookup"><span data-stu-id="bf161-296">reactionDetails</span></span> | <span data-ttu-id="bf161-297">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="bf161-297">JSON Array</span></span> | <span data-ttu-id="bf161-298">Array von JSON-Objekten jedes Ereignisobjekten Reaktionen Detail auf eine Aktion, die in einer Gruppe gesendet</span><span class="sxs-lookup"><span data-stu-id="bf161-298">Array of JSON objects each representing reactions detail on an Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="bf161-299">Zusammenfassung Antwort Body-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-299">Response body summary object</span></span>

| <span data-ttu-id="bf161-300">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf161-300">Parameter</span></span> | <span data-ttu-id="bf161-301">Typ</span><span class="sxs-lookup"><span data-stu-id="bf161-301">Type</span></span> | <span data-ttu-id="bf161-302">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf161-302">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="bf161-303">reactionId</span><span class="sxs-lookup"><span data-stu-id="bf161-303">reactionId</span></span> | <span data-ttu-id="bf161-304">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf161-304">String</span></span> | <span data-ttu-id="bf161-305">GUID, die die Id für die Reaktion auf ReferenceId für eine Aktion erstellt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf161-305">GUID representing the id for reaction created on referenceId representing an Action</span></span> |
| <span data-ttu-id="bf161-306">userId</span><span class="sxs-lookup"><span data-stu-id="bf161-306">userId</span></span> | <span data-ttu-id="bf161-307">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf161-307">Json object</span></span> | <span data-ttu-id="bf161-308">Benutzer-ID des Benutzers, der die Reaktion auf eine Aktion erstellt hat</span><span class="sxs-lookup"><span data-stu-id="bf161-308">UserId for the user who has created the reaction on an Action</span></span> |
| <span data-ttu-id="bf161-309">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="bf161-309">lastModifiedTime</span></span> | <span data-ttu-id="bf161-310">Timestamp</span><span class="sxs-lookup"><span data-stu-id="bf161-310">Timestamp</span></span> | <span data-ttu-id="bf161-311">Zeitstempel, an dem Reaktion erstellt/aktualisiert wurde</span><span class="sxs-lookup"><span data-stu-id="bf161-311">Timestamp at which reaction was created/updated</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="bf161-312">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="bf161-312">Sample JSON Response</span></span>

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