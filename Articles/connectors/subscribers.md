---
title: /Subscribers
description: Referenzartikel zur API zum Abrufen von Abonnentendaten für öffentliche Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190698"
---
# <a name="subscribers"></a><span data-ttu-id="886f2-103">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="886f2-103">/subscribers</span></span>

<span data-ttu-id="886f2-104">API-Endpunkt zum Hinzufügen, Abrufen oder Löschen von Abonnenten aus verwalteter öffentlicher Gruppe.</span><span class="sxs-lookup"><span data-stu-id="886f2-104">API end-point to add, get or delete subscribers from Managed Public group.</span></span>

## <a name="add-subscribers"></a><span data-ttu-id="886f2-105">/Subscribers hinzufügen</span><span class="sxs-lookup"><span data-stu-id="886f2-105">ADD /subscribers</span></span>

    <span data-ttu-id="886f2-106">PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/add</span><span class="sxs-lookup"><span data-stu-id="886f2-106">PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add</span></span>

### <a name="request-parameters"></a><span data-ttu-id="886f2-107">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="886f2-107">Request Parameters</span></span>
|  | <span data-ttu-id="886f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-108">Parameter</span></span> | <span data-ttu-id="886f2-109">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-109">Type</span></span> | <span data-ttu-id="886f2-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="886f2-110">Optional?</span></span> | <span data-ttu-id="886f2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="886f2-112">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-112">URL Path Parameter</span></span> | <span data-ttu-id="886f2-113">groupId</span><span class="sxs-lookup"><span data-stu-id="886f2-113">groupId</span></span> | <span data-ttu-id="886f2-114">String</span><span class="sxs-lookup"><span data-stu-id="886f2-114">String</span></span> | <span data-ttu-id="886f2-115">Nein</span><span class="sxs-lookup"><span data-stu-id="886f2-115">No</span></span> | <span data-ttu-id="886f2-116">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="886f2-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="886f2-117">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="886f2-117">HTTP Header</span></span> | <span data-ttu-id="886f2-118">accessToken</span><span class="sxs-lookup"><span data-stu-id="886f2-118">accessToken</span></span> | <span data-ttu-id="886f2-119">String</span><span class="sxs-lookup"><span data-stu-id="886f2-119">String</span></span> | <span data-ttu-id="886f2-120">Nein</span><span class="sxs-lookup"><span data-stu-id="886f2-120">No</span></span> | <span data-ttu-id="886f2-121">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="886f2-121">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="886f2-122">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="886f2-122">Request body</span></span>
| <span data-ttu-id="886f2-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-123">Parameter</span></span> | <span data-ttu-id="886f2-124">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-124">Type</span></span> | <span data-ttu-id="886f2-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-125">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="886f2-126">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="886f2-126">subscribers</span></span> | <span data-ttu-id="886f2-127">String []</span><span class="sxs-lookup"><span data-stu-id="886f2-127">String[]</span></span> | <span data-ttu-id="886f2-128">Jede Zeichenfolge steht für eine Mobiltelefonnummer mit Landesvorwahl (zB.</span><span class="sxs-lookup"><span data-stu-id="886f2-128">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="886f2-129">+ 911111111111)</span><span class="sxs-lookup"><span data-stu-id="886f2-129">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="886f2-130">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="886f2-130">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="886f2-131">Antworttext</span><span class="sxs-lookup"><span data-stu-id="886f2-131">Response body</span></span>
| <span data-ttu-id="886f2-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-132">Parameter</span></span> | <span data-ttu-id="886f2-133">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-133">Type</span></span> | <span data-ttu-id="886f2-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-134">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="886f2-135">result</span><span class="sxs-lookup"><span data-stu-id="886f2-135">result</span></span> | <span data-ttu-id="886f2-136">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="886f2-136">JSON object</span></span> | <span data-ttu-id="886f2-137">Jeder Schlüssel dieses JSON-Objekts stellt die Mobiltelefonnummer dar, und value stellt das JSON-Objekt dar, das Erfolg oder Fehler mit Reason enthält.</span><span class="sxs-lookup"><span data-stu-id="886f2-137">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="886f2-138">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="886f2-138">Sample JSON Response</span></span>

```javascript
{
    "result": {
        "+911111111111": {
            "isAdded": true
        },
        "+911111111112": {
            "isAdded": true
        }
    }
}
```

## <a name="get-subscribers"></a><span data-ttu-id="886f2-139">/Subscribers abrufen</span><span class="sxs-lookup"><span data-stu-id="886f2-139">GET /subscribers</span></span>

    <span data-ttu-id="886f2-140">POST {Endpunkt-URL}/v1/groups/{groupId}/subscribers</span><span class="sxs-lookup"><span data-stu-id="886f2-140">POST {endpoint-url}/v1/groups/{groupId}/subscribers</span></span>

### <a name="request-parameters"></a><span data-ttu-id="886f2-141">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="886f2-141">Request Parameters</span></span>
|  | <span data-ttu-id="886f2-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-142">Parameter</span></span> | <span data-ttu-id="886f2-143">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-143">Type</span></span> | <span data-ttu-id="886f2-144">Optional?</span><span class="sxs-lookup"><span data-stu-id="886f2-144">Optional?</span></span> | <span data-ttu-id="886f2-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-145">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="886f2-146">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-146">URL Path Parameter</span></span> | <span data-ttu-id="886f2-147">groupId</span><span class="sxs-lookup"><span data-stu-id="886f2-147">groupId</span></span> | <span data-ttu-id="886f2-148">String</span><span class="sxs-lookup"><span data-stu-id="886f2-148">String</span></span> | <span data-ttu-id="886f2-149">Nein</span><span class="sxs-lookup"><span data-stu-id="886f2-149">No</span></span> | <span data-ttu-id="886f2-150">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="886f2-150">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="886f2-151">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="886f2-151">HTTP Header</span></span> | <span data-ttu-id="886f2-152">accessToken</span><span class="sxs-lookup"><span data-stu-id="886f2-152">accessToken</span></span> | <span data-ttu-id="886f2-153">String</span><span class="sxs-lookup"><span data-stu-id="886f2-153">String</span></span> | <span data-ttu-id="886f2-154">Nein</span><span class="sxs-lookup"><span data-stu-id="886f2-154">No</span></span> | <span data-ttu-id="886f2-155">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="886f2-155">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="886f2-156">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="886f2-156">Request body</span></span>

| <span data-ttu-id="886f2-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-157">Parameter</span></span> | <span data-ttu-id="886f2-158">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-158">Type</span></span> | <span data-ttu-id="886f2-159">Optional?</span><span class="sxs-lookup"><span data-stu-id="886f2-159">Optional?</span></span> | <span data-ttu-id="886f2-160">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-160">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="886f2-161">Cursor</span><span class="sxs-lookup"><span data-stu-id="886f2-161">cursor</span></span> | <span data-ttu-id="886f2-162">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="886f2-162">String</span></span> | <span data-ttu-id="886f2-163">Ja</span><span class="sxs-lookup"><span data-stu-id="886f2-163">Yes</span></span> | <span data-ttu-id="886f2-164">Anfang des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="886f2-164">Start of resultset.</span></span> <span data-ttu-id="886f2-165">Zur Paginierung.</span><span class="sxs-lookup"><span data-stu-id="886f2-165">For pagination.</span></span> <span data-ttu-id="886f2-166">Zurückgegeben im Antworttext</span><span class="sxs-lookup"><span data-stu-id="886f2-166">Returned in Response Body</span></span> |
| <span data-ttu-id="886f2-167">count</span><span class="sxs-lookup"><span data-stu-id="886f2-167">count</span></span> | <span data-ttu-id="886f2-168">int</span><span class="sxs-lookup"><span data-stu-id="886f2-168">int</span></span> | <span data-ttu-id="886f2-169">Ja</span><span class="sxs-lookup"><span data-stu-id="886f2-169">Yes</span></span> | <span data-ttu-id="886f2-170">Standard: 50.</span><span class="sxs-lookup"><span data-stu-id="886f2-170">Default: 50.</span></span> <span data-ttu-id="886f2-171">Max: 50.</span><span class="sxs-lookup"><span data-stu-id="886f2-171">Max: 50.</span></span> <span data-ttu-id="886f2-172">Anzahl der Abonnenten, die in einem Resultset zurückgegeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="886f2-172">Number of subscribers to be returned in a resultset</span></span>|

### <a name="response-body"></a><span data-ttu-id="886f2-173">Antworttext</span><span class="sxs-lookup"><span data-stu-id="886f2-173">Response body</span></span>

| <span data-ttu-id="886f2-174">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-174">Parameter</span></span> | <span data-ttu-id="886f2-175">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-175">Type</span></span> | <span data-ttu-id="886f2-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-176">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="886f2-177">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="886f2-177">subscribers</span></span> | <span data-ttu-id="886f2-178">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="886f2-178">JSON Array</span></span> | <span data-ttu-id="886f2-179">Array von JSON-Objekten, die jeweils einen Teilnehmer der Gruppe darstellen</span><span class="sxs-lookup"><span data-stu-id="886f2-179">Array of JSON objects each representing a subscriber of the group</span></span> |
| <span data-ttu-id="886f2-180">Cursor</span><span class="sxs-lookup"><span data-stu-id="886f2-180">cursor</span></span> | <span data-ttu-id="886f2-181">String</span><span class="sxs-lookup"><span data-stu-id="886f2-181">String</span></span> | <span data-ttu-id="886f2-182">Anfang des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="886f2-182">Start of resultset.</span></span> <span data-ttu-id="886f2-183">Zur Paginierung.</span><span class="sxs-lookup"><span data-stu-id="886f2-183">For pagination.</span></span> <span data-ttu-id="886f2-184">Wird im Anforderungstext zum Abrufen des nächsten Resultsets verwendet.</span><span class="sxs-lookup"><span data-stu-id="886f2-184">To be used in Request body for fetching next result set.</span></span> <span data-ttu-id="886f2-185">Wird nur dann als Antwort angezeigt, wenn ein gültiger nächster Resultset vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="886f2-185">Present in response only if there is a valid next result set.</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="886f2-186">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="886f2-186">Sample JSON Response</span></span>

```javascript
{
    "subscribers": [
        {
            "id": "e2238eb5-2f45-4783-8f4b-571549db86c0",
            "mobileNumber": "+91109999999",
            "name": "",
            "profilePic": "",
            "isProvisioned": false
        }
    ]
}
```

## <a name="remove-subscribers"></a><span data-ttu-id="886f2-187">/Subscribers entfernen</span><span class="sxs-lookup"><span data-stu-id="886f2-187">REMOVE /subscribers</span></span>

    <span data-ttu-id="886f2-188">PUT {Endpoint-URL}/v1/groups/{groupId}/subscribers/remove</span><span class="sxs-lookup"><span data-stu-id="886f2-188">PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove</span></span>

### <a name="request-parameters"></a><span data-ttu-id="886f2-189">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="886f2-189">Request Parameters</span></span>
|  | <span data-ttu-id="886f2-190">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-190">Parameter</span></span> | <span data-ttu-id="886f2-191">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-191">Type</span></span> | <span data-ttu-id="886f2-192">Optional?</span><span class="sxs-lookup"><span data-stu-id="886f2-192">Optional?</span></span> | <span data-ttu-id="886f2-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-193">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="886f2-194">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-194">URL Path Parameter</span></span> | <span data-ttu-id="886f2-195">groupId</span><span class="sxs-lookup"><span data-stu-id="886f2-195">groupId</span></span> | <span data-ttu-id="886f2-196">String</span><span class="sxs-lookup"><span data-stu-id="886f2-196">String</span></span> | <span data-ttu-id="886f2-197">Nein</span><span class="sxs-lookup"><span data-stu-id="886f2-197">No</span></span> | <span data-ttu-id="886f2-198">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="886f2-198">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="886f2-199">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="886f2-199">HTTP Header</span></span> | <span data-ttu-id="886f2-200">accessToken</span><span class="sxs-lookup"><span data-stu-id="886f2-200">accessToken</span></span> | <span data-ttu-id="886f2-201">String</span><span class="sxs-lookup"><span data-stu-id="886f2-201">String</span></span> | <span data-ttu-id="886f2-202">Nein</span><span class="sxs-lookup"><span data-stu-id="886f2-202">No</span></span> | <span data-ttu-id="886f2-203">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="886f2-203">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="886f2-204">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="886f2-204">Request body</span></span>
| <span data-ttu-id="886f2-205">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-205">Parameter</span></span> | <span data-ttu-id="886f2-206">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-206">Type</span></span> | <span data-ttu-id="886f2-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-207">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="886f2-208">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="886f2-208">subscribers</span></span> | <span data-ttu-id="886f2-209">String []</span><span class="sxs-lookup"><span data-stu-id="886f2-209">String[]</span></span> | <span data-ttu-id="886f2-210">Jede Zeichenfolge steht für eine Mobiltelefonnummer mit Landesvorwahl (zB.</span><span class="sxs-lookup"><span data-stu-id="886f2-210">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="886f2-211">+ 911111111111)</span><span class="sxs-lookup"><span data-stu-id="886f2-211">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="886f2-212">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="886f2-212">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="886f2-213">Antworttext</span><span class="sxs-lookup"><span data-stu-id="886f2-213">Response body</span></span>
| <span data-ttu-id="886f2-214">Parameter</span><span class="sxs-lookup"><span data-stu-id="886f2-214">Parameter</span></span> | <span data-ttu-id="886f2-215">Typ</span><span class="sxs-lookup"><span data-stu-id="886f2-215">Type</span></span> | <span data-ttu-id="886f2-216">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="886f2-216">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="886f2-217">result</span><span class="sxs-lookup"><span data-stu-id="886f2-217">result</span></span> | <span data-ttu-id="886f2-218">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="886f2-218">JSON object</span></span> | <span data-ttu-id="886f2-219">Jeder Schlüssel dieses JSON-Objekts stellt die Mobiltelefonnummer dar, und value stellt das JSON-Objekt dar, das Erfolg oder Fehler mit Reason enthält.</span><span class="sxs-lookup"><span data-stu-id="886f2-219">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="886f2-220">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="886f2-220">Sample JSON Response</span></span>

```javascript
{
    "result": {
        "+911111111111": {
            "isRemoved": true
        },
        "+911111111112": {
            "isRemoved": true
        }
    }
}
```

