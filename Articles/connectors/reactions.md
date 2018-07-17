---
title: /Reaction
description: Referenzartikel für Reaktionen auf eine beliebige Aktion in einer Gruppe gesendet Abfrage-API
topic: Reference
author: nitinjms
ms.openlocfilehash: 4f2da7302133371dba5edd6035a57068e16aae63
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20425632"
---
# <a name="reaction"></a><span data-ttu-id="45b18-103">/Reaction</span><span class="sxs-lookup"><span data-stu-id="45b18-103">/reaction</span></span>
<span data-ttu-id="45b18-104">API-Endpunkt auf Abfrage Reaktionen Daten für alle Aktionen, die in einer Gruppe gesendet.</span><span class="sxs-lookup"><span data-stu-id="45b18-104">API end-point to query reactions data on any Action sent in a group.</span></span>

## <a name="post-reaction"></a><span data-ttu-id="45b18-105">POST-/reaction</span><span class="sxs-lookup"><span data-stu-id="45b18-105">POST /reaction</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a><span data-ttu-id="45b18-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="45b18-106">Request Parameters</span></span>

| | <span data-ttu-id="45b18-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-107">Parameter</span></span> | <span data-ttu-id="45b18-108">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-108">Type</span></span> | <span data-ttu-id="45b18-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="45b18-109">Optional?</span></span> | <span data-ttu-id="45b18-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-110">Description</span></span> |
| :---: | :---: | :---: | :---  | :--- |
| <span data-ttu-id="45b18-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-111">URL Path Parameter</span></span> | <span data-ttu-id="45b18-112">groupId</span><span class="sxs-lookup"><span data-stu-id="45b18-112">groupId</span></span> | <span data-ttu-id="45b18-113">String</span><span class="sxs-lookup"><span data-stu-id="45b18-113">String</span></span> | <span data-ttu-id="45b18-114">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-114">No</span></span> | <span data-ttu-id="45b18-115">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b18-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="45b18-116">HTTP Header</span></span> | <span data-ttu-id="45b18-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b18-117">accessToken</span></span> | <span data-ttu-id="45b18-118">String</span><span class="sxs-lookup"><span data-stu-id="45b18-118">String</span></span> | <span data-ttu-id="45b18-119">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-119">No</span></span> | <span data-ttu-id="45b18-120">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="45b18-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="45b18-121">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="45b18-121">HTTP Header</span></span> | <span data-ttu-id="45b18-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="45b18-122">Content-Type</span></span> | <span data-ttu-id="45b18-123">String</span><span class="sxs-lookup"><span data-stu-id="45b18-123">String</span></span> | <span data-ttu-id="45b18-124">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-124">No</span></span> | <span data-ttu-id="45b18-125">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="45b18-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="45b18-126">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="45b18-126">Request body</span></span>

| <span data-ttu-id="45b18-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-127">Parameter</span></span> | <span data-ttu-id="45b18-128">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-128">Type</span></span> | <span data-ttu-id="45b18-129">Optional?</span><span class="sxs-lookup"><span data-stu-id="45b18-129">Optional?</span></span> | <span data-ttu-id="45b18-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="45b18-131">referenceId</span><span class="sxs-lookup"><span data-stu-id="45b18-131">referenceId</span></span> | <span data-ttu-id="45b18-132">String</span><span class="sxs-lookup"><span data-stu-id="45b18-132">String</span></span> | <span data-ttu-id="45b18-133">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-133">No</span></span> | <span data-ttu-id="45b18-134">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-134">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="45b18-135">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="45b18-135">sourceGroupId</span></span> | <span data-ttu-id="45b18-136">String</span><span class="sxs-lookup"><span data-stu-id="45b18-136">String</span></span> | <span data-ttu-id="45b18-137">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-137">No</span></span> | <span data-ttu-id="45b18-138">Die GUID der Gruppe in der die Aktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="45b18-138">GUID of the group in which the Action has been sent.</span></span> <span data-ttu-id="45b18-139">Im Fall eines WAN-Gruppen, die eine Untergruppe einer anderen Gruppe ist, kann dies von 'GroupId' in der Url bereitgestellt abweichen Path-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-139">In case of groups which is a subgroup of another group, this may differ from 'groupId' provided in the url Path parameter</span></span>|
| <span data-ttu-id="45b18-140">reactionType</span><span class="sxs-lookup"><span data-stu-id="45b18-140">reactionType</span></span> | <span data-ttu-id="45b18-141">String</span><span class="sxs-lookup"><span data-stu-id="45b18-141">String</span></span> | <span data-ttu-id="45b18-142">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-142">No</span></span> | <span data-ttu-id="45b18-143">Enum-Wert: 'Like "/" abgeben'</span><span class="sxs-lookup"><span data-stu-id="45b18-143">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="45b18-144">comment</span><span class="sxs-lookup"><span data-stu-id="45b18-144">comment</span></span> | <span data-ttu-id="45b18-145">String</span><span class="sxs-lookup"><span data-stu-id="45b18-145">String</span></span> | <span data-ttu-id="45b18-146">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-146">No</span></span> | <span data-ttu-id="45b18-147">Kommentartext ist nur für ReactionType 'Comment' obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="45b18-147">Comment text is mandatory only for reactionType 'Comment'.</span></span> <span data-ttu-id="45b18-148">Für sollen "Like" dies ignoriert werden</span><span class="sxs-lookup"><span data-stu-id="45b18-148">For 'Like', this should be ignored</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="45b18-149">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="45b18-149">Sample JSON Request</span></span>

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a><span data-ttu-id="45b18-150">Antworttext</span><span class="sxs-lookup"><span data-stu-id="45b18-150">Response body</span></span>

| <span data-ttu-id="45b18-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-151">Parameter</span></span> | <span data-ttu-id="45b18-152">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-152">Type</span></span> | <span data-ttu-id="45b18-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-154">reactionId</span><span class="sxs-lookup"><span data-stu-id="45b18-154">reactionId</span></span> | <span data-ttu-id="45b18-155">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="45b18-155">String</span></span> | <span data-ttu-id="45b18-156">GUID, die die Id für Reaktion Entität nach dem erfolgreichen Abschluss der Anforderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-156">GUID representing the id for reaction entity after successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="45b18-157">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="45b18-157">Sample JSON Response</span></span>

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a><span data-ttu-id="45b18-158">/Reaction Aktion Ebene Zusammenfassung abrufen</span><span class="sxs-lookup"><span data-stu-id="45b18-158">GET /reaction summary at Action level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a><span data-ttu-id="45b18-159">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="45b18-159">Request Parameters</span></span>

|  | <span data-ttu-id="45b18-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-160">Parameter</span></span> | <span data-ttu-id="45b18-161">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-161">Type</span></span> | <span data-ttu-id="45b18-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="45b18-162">Optional?</span></span> | <span data-ttu-id="45b18-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-163">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="45b18-164">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-164">URL Path Parameter</span></span> | <span data-ttu-id="45b18-165">groupId</span><span class="sxs-lookup"><span data-stu-id="45b18-165">groupId</span></span> | <span data-ttu-id="45b18-166">String</span><span class="sxs-lookup"><span data-stu-id="45b18-166">String</span></span> | <span data-ttu-id="45b18-167">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-167">No</span></span> | <span data-ttu-id="45b18-168">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-168">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b18-169">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-169">URL Path Parameter</span></span> | <span data-ttu-id="45b18-170">referenceId</span><span class="sxs-lookup"><span data-stu-id="45b18-170">referenceId</span></span> | <span data-ttu-id="45b18-171">String</span><span class="sxs-lookup"><span data-stu-id="45b18-171">String</span></span> | <span data-ttu-id="45b18-172">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-172">No</span></span> | <span data-ttu-id="45b18-173">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-173">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="45b18-174">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-174">URL Path Parameter</span></span> | <span data-ttu-id="45b18-175">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="45b18-175">sourceGroupId</span></span> | <span data-ttu-id="45b18-176">String</span><span class="sxs-lookup"><span data-stu-id="45b18-176">String</span></span> | <span data-ttu-id="45b18-177">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-177">No</span></span> | <span data-ttu-id="45b18-178">Die GUID der Gruppe, in der die Aktion gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="45b18-178">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="45b18-179">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="45b18-179">HTTP Header</span></span> | <span data-ttu-id="45b18-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b18-180">accessToken</span></span> | <span data-ttu-id="45b18-181">String</span><span class="sxs-lookup"><span data-stu-id="45b18-181">String</span></span> | <span data-ttu-id="45b18-182">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-182">No</span></span> | <span data-ttu-id="45b18-183">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="45b18-183">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="45b18-184">Antworttext</span><span class="sxs-lookup"><span data-stu-id="45b18-184">Response body</span></span>

| <span data-ttu-id="45b18-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-185">Parameter</span></span> | <span data-ttu-id="45b18-186">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-186">Type</span></span> | <span data-ttu-id="45b18-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-188">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="45b18-188">summary</span></span> | <span data-ttu-id="45b18-189">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="45b18-189">JSON Array</span></span> | <span data-ttu-id="45b18-190">Array von JSON-Objekten jede Ereignisobjekten Reaktionen Zusammenfassung auf eine Aktion, die in einer Gruppe gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="45b18-190">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

### <a name="response-body-summary-object"></a><span data-ttu-id="45b18-191">Zusammenfassung Antwort Body-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-191">Response body summary object</span></span>

| <span data-ttu-id="45b18-192">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-192">Parameter</span></span> | <span data-ttu-id="45b18-193">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-193">Type</span></span> | <span data-ttu-id="45b18-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-195">referenceId</span><span class="sxs-lookup"><span data-stu-id="45b18-195">referenceId</span></span> | <span data-ttu-id="45b18-196">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="45b18-196">String</span></span> | <span data-ttu-id="45b18-197">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-197">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="45b18-198">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="45b18-198">reactionsCountMap</span></span> | <span data-ttu-id="45b18-199">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-199">Json object</span></span> | <span data-ttu-id="45b18-200">Mit "gefällt mir" und Kommentare Count für diese ReferenceId JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-200">Json object containing Likes and comments count for that referenceId</span></span> |


### <a name="sample-json-response"></a><span data-ttu-id="45b18-201">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="45b18-201">Sample JSON Response</span></span>

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

## <a name="get-reaction-summary-at-group-level"></a><span data-ttu-id="45b18-202">Abrufen einer Zusammenfassung /reaction auf Gruppenebene</span><span class="sxs-lookup"><span data-stu-id="45b18-202">GET /reaction summary at group level</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="45b18-203">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="45b18-203">Request Parameters</span></span>

|  | <span data-ttu-id="45b18-204">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-204">Parameter</span></span> | <span data-ttu-id="45b18-205">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-205">Type</span></span> | <span data-ttu-id="45b18-206">Optional?</span><span class="sxs-lookup"><span data-stu-id="45b18-206">Optional?</span></span> | <span data-ttu-id="45b18-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-207">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="45b18-208">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-208">URL Path Parameter</span></span> | <span data-ttu-id="45b18-209">groupId</span><span class="sxs-lookup"><span data-stu-id="45b18-209">groupId</span></span> | <span data-ttu-id="45b18-210">String</span><span class="sxs-lookup"><span data-stu-id="45b18-210">String</span></span> | <span data-ttu-id="45b18-211">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-211">No</span></span> | <span data-ttu-id="45b18-212">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-212">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b18-213">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-213">URL Path Parameter</span></span> | <span data-ttu-id="45b18-214">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="45b18-214">sourceGroupId</span></span> | <span data-ttu-id="45b18-215">String</span><span class="sxs-lookup"><span data-stu-id="45b18-215">String</span></span> | <span data-ttu-id="45b18-216">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-216">No</span></span> | <span data-ttu-id="45b18-217">Die GUID der Gruppe, in der die Aktion gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="45b18-217">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="45b18-218">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-218">URL Path Parameter</span></span> | <span data-ttu-id="45b18-219">Cursor</span><span class="sxs-lookup"><span data-stu-id="45b18-219">cursor</span></span> | <span data-ttu-id="45b18-220">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="45b18-220">timeStamp</span></span> | <span data-ttu-id="45b18-221">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-221">No</span></span> | <span data-ttu-id="45b18-222">Zeitstempel, aus denen die Zusammenfassung berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="45b18-222">timeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="45b18-223">Der Standardwert 0</span><span class="sxs-lookup"><span data-stu-id="45b18-223">Default value 0</span></span> |
| <span data-ttu-id="45b18-224">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="45b18-224">HTTP Header</span></span> | <span data-ttu-id="45b18-225">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b18-225">accessToken</span></span> | <span data-ttu-id="45b18-226">String</span><span class="sxs-lookup"><span data-stu-id="45b18-226">String</span></span> | <span data-ttu-id="45b18-227">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-227">No</span></span> | <span data-ttu-id="45b18-228">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="45b18-228">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="45b18-229">Antworttext</span><span class="sxs-lookup"><span data-stu-id="45b18-229">Response body</span></span>

| <span data-ttu-id="45b18-230">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-230">Parameter</span></span> | <span data-ttu-id="45b18-231">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-231">Type</span></span> | <span data-ttu-id="45b18-232">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-232">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-233">Cursor</span><span class="sxs-lookup"><span data-stu-id="45b18-233">cursor</span></span> | <span data-ttu-id="45b18-234">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="45b18-234">timeStamp</span></span> | <span data-ttu-id="45b18-235">Zeitstempel, bis die Zusammenfassung berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="45b18-235">timeStamp till which summary has been calculated.</span></span> <span data-ttu-id="45b18-236">Nächsten Satzes von ReactionSummary kann mit dieser Wert Cursor generiert werden</span><span class="sxs-lookup"><span data-stu-id="45b18-236">Next set of reactionSummary can be generated using this cursor value</span></span> |
| <span data-ttu-id="45b18-237">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="45b18-237">summary</span></span> | <span data-ttu-id="45b18-238">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="45b18-238">JSON Array</span></span> | <span data-ttu-id="45b18-239">Array von JSON-Objekten jede Ereignisobjekten Reaktionen Zusammenfassung auf eine Aktion, die in einer Gruppe gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="45b18-239">Array of JSON objects each representing reactions summary on a Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="45b18-240">Zusammenfassung Antwort Body-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-240">Response body summary object</span></span>

| <span data-ttu-id="45b18-241">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-241">Parameter</span></span> | <span data-ttu-id="45b18-242">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-242">Type</span></span> | <span data-ttu-id="45b18-243">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-244">referenceId</span><span class="sxs-lookup"><span data-stu-id="45b18-244">referenceId</span></span> | <span data-ttu-id="45b18-245">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="45b18-245">String</span></span> | <span data-ttu-id="45b18-246">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-246">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="45b18-247">reactionsCountMap</span><span class="sxs-lookup"><span data-stu-id="45b18-247">reactionsCountMap</span></span> | <span data-ttu-id="45b18-248">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-248">Json object</span></span> | <span data-ttu-id="45b18-249">Mit "gefällt mir" und Kommentare Count für diese ReferenceId JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-249">Json object containing Likes and comments count for that referenceId</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="45b18-250">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="45b18-250">Sample JSON Response</span></span>

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

## <a name="get-reaction-details-for-a-action"></a><span data-ttu-id="45b18-251">Hier erhalten Sie /reaction für eine Aktion</span><span class="sxs-lookup"><span data-stu-id="45b18-251">GET /reaction details for a Action</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a><span data-ttu-id="45b18-252">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="45b18-252">Request Parameters</span></span>

|  | <span data-ttu-id="45b18-253">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-253">Parameter</span></span> | <span data-ttu-id="45b18-254">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-254">Type</span></span> | <span data-ttu-id="45b18-255">Optional?</span><span class="sxs-lookup"><span data-stu-id="45b18-255">Optional?</span></span> | <span data-ttu-id="45b18-256">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="45b18-257">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-257">URL Path Parameter</span></span> | <span data-ttu-id="45b18-258">groupId</span><span class="sxs-lookup"><span data-stu-id="45b18-258">groupId</span></span> | <span data-ttu-id="45b18-259">String</span><span class="sxs-lookup"><span data-stu-id="45b18-259">String</span></span> | <span data-ttu-id="45b18-260">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-260">No</span></span> | <span data-ttu-id="45b18-261">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-261">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="45b18-262">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-262">URL Path Parameter</span></span> | <span data-ttu-id="45b18-263">sourceGroupId</span><span class="sxs-lookup"><span data-stu-id="45b18-263">sourceGroupId</span></span> | <span data-ttu-id="45b18-264">String</span><span class="sxs-lookup"><span data-stu-id="45b18-264">String</span></span> | <span data-ttu-id="45b18-265">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-265">No</span></span> | <span data-ttu-id="45b18-266">Die GUID der Gruppe, in der die Aktion gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="45b18-266">GUID of the group in which the Action has been sent</span></span> |
| <span data-ttu-id="45b18-267">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-267">URL Path Parameter</span></span> | <span data-ttu-id="45b18-268">referenceId</span><span class="sxs-lookup"><span data-stu-id="45b18-268">referenceId</span></span> | <span data-ttu-id="45b18-269">String</span><span class="sxs-lookup"><span data-stu-id="45b18-269">String</span></span> | <span data-ttu-id="45b18-270">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-270">No</span></span> | <span data-ttu-id="45b18-271">GUID, die die Id für die Entitätsverweis für eine Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-271">GUID representing the id for entity reference representing an Action</span></span> |
| <span data-ttu-id="45b18-272">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-272">URL Path Parameter</span></span> | <span data-ttu-id="45b18-273">reactionType</span><span class="sxs-lookup"><span data-stu-id="45b18-273">reactionType</span></span> | <span data-ttu-id="45b18-274">String</span><span class="sxs-lookup"><span data-stu-id="45b18-274">String</span></span> | <span data-ttu-id="45b18-275">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-275">No</span></span> | <span data-ttu-id="45b18-276">Enum-Wert: 'Like "/" abgeben'</span><span class="sxs-lookup"><span data-stu-id="45b18-276">Enum value: 'Like'/'Comment'</span></span>|
| <span data-ttu-id="45b18-277">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-277">URL Path Parameter</span></span> | <span data-ttu-id="45b18-278">Cursor</span><span class="sxs-lookup"><span data-stu-id="45b18-278">cursor</span></span> | <span data-ttu-id="45b18-279">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="45b18-279">TimeStamp</span></span> | <span data-ttu-id="45b18-280">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-280">No</span></span> | <span data-ttu-id="45b18-281">Zeitstempel, aus denen die Zusammenfassung berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="45b18-281">TimeStamp from which the summary needs to be calculated.</span></span> <span data-ttu-id="45b18-282">Der Standardwert 0</span><span class="sxs-lookup"><span data-stu-id="45b18-282">Default value 0</span></span> |
| <span data-ttu-id="45b18-283">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="45b18-283">HTTP Header</span></span> | <span data-ttu-id="45b18-284">accessToken</span><span class="sxs-lookup"><span data-stu-id="45b18-284">accessToken</span></span> | <span data-ttu-id="45b18-285">String</span><span class="sxs-lookup"><span data-stu-id="45b18-285">String</span></span> | <span data-ttu-id="45b18-286">Nein</span><span class="sxs-lookup"><span data-stu-id="45b18-286">No</span></span> | <span data-ttu-id="45b18-287">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="45b18-287">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="45b18-288">Antworttext</span><span class="sxs-lookup"><span data-stu-id="45b18-288">Response body</span></span>

| <span data-ttu-id="45b18-289">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-289">Parameter</span></span> | <span data-ttu-id="45b18-290">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-290">Type</span></span> | <span data-ttu-id="45b18-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-291">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-292">Cursor</span><span class="sxs-lookup"><span data-stu-id="45b18-292">cursor</span></span> | <span data-ttu-id="45b18-293">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="45b18-293">TimeStamp</span></span> | <span data-ttu-id="45b18-294">Zeitstempel, bis die ReactionDetail bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="45b18-294">TimeStamp till which reactionDetail has been provided.</span></span> <span data-ttu-id="45b18-295">Nächsten Satzes von ReactionDetails kann mit dieser Wert Cursor generiert werden</span><span class="sxs-lookup"><span data-stu-id="45b18-295">Next set of reactionDetails can be generated using this cursor value</span></span> |
| <span data-ttu-id="45b18-296">reactionDetails</span><span class="sxs-lookup"><span data-stu-id="45b18-296">reactionDetails</span></span> | <span data-ttu-id="45b18-297">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="45b18-297">JSON Array</span></span> | <span data-ttu-id="45b18-298">Array von JSON-Objekten jedes Ereignisobjekten Reaktionen Detail auf eine Aktion, die in einer Gruppe gesendet</span><span class="sxs-lookup"><span data-stu-id="45b18-298">Array of JSON objects each representing reactions detail on an Action sent in a group</span></span> |

#### <a name="response-body-summary-object"></a><span data-ttu-id="45b18-299">Zusammenfassung Antwort Body-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-299">Response body summary object</span></span>

| <span data-ttu-id="45b18-300">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b18-300">Parameter</span></span> | <span data-ttu-id="45b18-301">Typ</span><span class="sxs-lookup"><span data-stu-id="45b18-301">Type</span></span> | <span data-ttu-id="45b18-302">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b18-302">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="45b18-303">reactionId</span><span class="sxs-lookup"><span data-stu-id="45b18-303">reactionId</span></span> | <span data-ttu-id="45b18-304">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="45b18-304">String</span></span> | <span data-ttu-id="45b18-305">GUID, die die Id für die Reaktion auf ReferenceId für eine Aktion erstellt darstellt.</span><span class="sxs-lookup"><span data-stu-id="45b18-305">GUID representing the id for reaction created on referenceId representing an Action</span></span> |
| <span data-ttu-id="45b18-306">userId</span><span class="sxs-lookup"><span data-stu-id="45b18-306">userId</span></span> | <span data-ttu-id="45b18-307">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="45b18-307">Json object</span></span> | <span data-ttu-id="45b18-308">Benutzer-ID des Benutzers, der die Reaktion auf eine Aktion erstellt hat</span><span class="sxs-lookup"><span data-stu-id="45b18-308">UserId for the user who has created the reaction on an Action</span></span> |
| <span data-ttu-id="45b18-309">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="45b18-309">lastModifiedTime</span></span> | <span data-ttu-id="45b18-310">Timestamp</span><span class="sxs-lookup"><span data-stu-id="45b18-310">Timestamp</span></span> | <span data-ttu-id="45b18-311">Zeitstempel, an dem Reaktion erstellt/aktualisiert wurde</span><span class="sxs-lookup"><span data-stu-id="45b18-311">Timestamp at which reaction was created/updated</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="45b18-312">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="45b18-312">Sample JSON Response</span></span>

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