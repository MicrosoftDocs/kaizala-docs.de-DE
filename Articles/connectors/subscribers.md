---
title: /Subscribers
description: Verweisen auf Artikel, um die API zum Abrufen von Abonnenten Daten für öffentliche Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: b026c8c38ce3cea600219a3e5713726013e62367
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905335"
---
# <a name="apis-to-query-subscribers-data-in-a-public-group"></a><span data-ttu-id="9e35e-103">APIs für das Abfragen von Daten in einer öffentlichen Gruppe-Abonnenten</span><span class="sxs-lookup"><span data-stu-id="9e35e-103">APIs to query subscribers data in a public group</span></span>
## <a name="subscribers"></a><span data-ttu-id="9e35e-104">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="9e35e-104">/subscribers</span></span>

<span data-ttu-id="9e35e-105">API-Endpunkt hinzufügen, Abrufen oder Abonnenten von verwalteten öffentliche Gruppe löschen.</span><span class="sxs-lookup"><span data-stu-id="9e35e-105">API end-point to add, get or delete subscribers from Managed Public group.</span></span>

### <a name="add-subscribers"></a><span data-ttu-id="9e35e-106">/Subscribers hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9e35e-106">ADD /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add

##### <a name="request-parameters"></a><span data-ttu-id="9e35e-107">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-107">Request Parameters</span></span>
|  | <span data-ttu-id="9e35e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-108">Parameter</span></span> | <span data-ttu-id="9e35e-109">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-109">Type</span></span> | <span data-ttu-id="9e35e-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="9e35e-110">Optional?</span></span> | <span data-ttu-id="9e35e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9e35e-112">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-112">URL Path Parameter</span></span> | <span data-ttu-id="9e35e-113">groupId</span><span class="sxs-lookup"><span data-stu-id="9e35e-113">groupId</span></span> | <span data-ttu-id="9e35e-114">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-114">String</span></span> | <span data-ttu-id="9e35e-115">Nein</span><span class="sxs-lookup"><span data-stu-id="9e35e-115">No</span></span> | <span data-ttu-id="9e35e-116">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e35e-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="9e35e-117">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9e35e-117">HTTP Header</span></span> | <span data-ttu-id="9e35e-118">accessToken</span><span class="sxs-lookup"><span data-stu-id="9e35e-118">accessToken</span></span> | <span data-ttu-id="9e35e-119">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-119">String</span></span> | <span data-ttu-id="9e35e-120">Nein</span><span class="sxs-lookup"><span data-stu-id="9e35e-120">No</span></span> | <span data-ttu-id="9e35e-121">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="9e35e-121">Access Token received from the auth end-point</span></span> |

##### <a name="request-body"></a><span data-ttu-id="9e35e-122">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="9e35e-122">Request body</span></span>
| <span data-ttu-id="9e35e-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-123">Parameter</span></span> | <span data-ttu-id="9e35e-124">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-124">Type</span></span> | <span data-ttu-id="9e35e-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-125">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9e35e-126">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="9e35e-126">subscribers</span></span> | <span data-ttu-id="9e35e-127">String]</span><span class="sxs-lookup"><span data-stu-id="9e35e-127">String[]</span></span> | <span data-ttu-id="9e35e-128">Jede Zeichenfolge stellt Mobiltelefonnummer mit Ländercode (z. B..</span><span class="sxs-lookup"><span data-stu-id="9e35e-128">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="9e35e-129">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="9e35e-129">+911111111111)</span></span> |

###### <a name="sample-json-request"></a><span data-ttu-id="9e35e-130">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e35e-130">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

##### <a name="response-body"></a><span data-ttu-id="9e35e-131">Antworttext</span><span class="sxs-lookup"><span data-stu-id="9e35e-131">Response body</span></span>
| <span data-ttu-id="9e35e-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-132">Parameter</span></span> | <span data-ttu-id="9e35e-133">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-133">Type</span></span> | <span data-ttu-id="9e35e-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-134">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9e35e-135">result</span><span class="sxs-lookup"><span data-stu-id="9e35e-135">result</span></span> | <span data-ttu-id="9e35e-136">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e35e-136">JSON object</span></span> | <span data-ttu-id="9e35e-137">Jeder Schlüssel in Json-Objekt repräsentiert die Mobiltelefonnummer und Wert darstellt, enthält Erfolg oder Fehler mit Grund Json-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e35e-137">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="9e35e-138">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="9e35e-138">Sample JSON Response</span></span>

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

### <a name="get-subscribers"></a><span data-ttu-id="9e35e-139">Abrufen von /subscribers</span><span class="sxs-lookup"><span data-stu-id="9e35e-139">GET /subscribers</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subscribers

##### <a name="request-parameters"></a><span data-ttu-id="9e35e-140">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-140">Request Parameters</span></span>
|  | <span data-ttu-id="9e35e-141">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-141">Parameter</span></span> | <span data-ttu-id="9e35e-142">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-142">Type</span></span> | <span data-ttu-id="9e35e-143">Optional?</span><span class="sxs-lookup"><span data-stu-id="9e35e-143">Optional?</span></span> | <span data-ttu-id="9e35e-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-144">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9e35e-145">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-145">URL Path Parameter</span></span> | <span data-ttu-id="9e35e-146">groupId</span><span class="sxs-lookup"><span data-stu-id="9e35e-146">groupId</span></span> | <span data-ttu-id="9e35e-147">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-147">String</span></span> | <span data-ttu-id="9e35e-148">Nein</span><span class="sxs-lookup"><span data-stu-id="9e35e-148">No</span></span> | <span data-ttu-id="9e35e-149">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e35e-149">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="9e35e-150">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9e35e-150">HTTP Header</span></span> | <span data-ttu-id="9e35e-151">accessToken</span><span class="sxs-lookup"><span data-stu-id="9e35e-151">accessToken</span></span> | <span data-ttu-id="9e35e-152">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-152">String</span></span> | <span data-ttu-id="9e35e-153">Nein</span><span class="sxs-lookup"><span data-stu-id="9e35e-153">No</span></span> | <span data-ttu-id="9e35e-154">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="9e35e-154">Access Token received from the auth end-point</span></span> |

##### <a name="request-body"></a><span data-ttu-id="9e35e-155">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="9e35e-155">Request body</span></span>

| <span data-ttu-id="9e35e-156">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-156">Parameter</span></span> | <span data-ttu-id="9e35e-157">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-157">Type</span></span> | <span data-ttu-id="9e35e-158">Optional?</span><span class="sxs-lookup"><span data-stu-id="9e35e-158">Optional?</span></span> | <span data-ttu-id="9e35e-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-159">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="9e35e-160">Cursor</span><span class="sxs-lookup"><span data-stu-id="9e35e-160">cursor</span></span> | <span data-ttu-id="9e35e-161">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-161">String</span></span> | <span data-ttu-id="9e35e-162">Ja</span><span class="sxs-lookup"><span data-stu-id="9e35e-162">Yes</span></span> | <span data-ttu-id="9e35e-163">Anfang des Resultset.</span><span class="sxs-lookup"><span data-stu-id="9e35e-163">Start of resultset.</span></span> <span data-ttu-id="9e35e-164">Für die Paginierung.</span><span class="sxs-lookup"><span data-stu-id="9e35e-164">For pagination.</span></span> <span data-ttu-id="9e35e-165">In Antworttext zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="9e35e-165">Returned in Response Body</span></span> |
| <span data-ttu-id="9e35e-166">count</span><span class="sxs-lookup"><span data-stu-id="9e35e-166">count</span></span> | <span data-ttu-id="9e35e-167">int</span><span class="sxs-lookup"><span data-stu-id="9e35e-167">int</span></span> | <span data-ttu-id="9e35e-168">Ja</span><span class="sxs-lookup"><span data-stu-id="9e35e-168">Yes</span></span> | <span data-ttu-id="9e35e-169">Standard: 50.</span><span class="sxs-lookup"><span data-stu-id="9e35e-169">Default: 50.</span></span> <span data-ttu-id="9e35e-170">Max: 50.</span><span class="sxs-lookup"><span data-stu-id="9e35e-170">Max: 50.</span></span> <span data-ttu-id="9e35e-171">Anzahl von Abonnenten in einem Resultset zurückgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="9e35e-171">Number of subscribers to be returned in a resultset</span></span>|

##### <a name="response-body"></a><span data-ttu-id="9e35e-172">Antworttext</span><span class="sxs-lookup"><span data-stu-id="9e35e-172">Response body</span></span>

| <span data-ttu-id="9e35e-173">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-173">Parameter</span></span> | <span data-ttu-id="9e35e-174">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-174">Type</span></span> | <span data-ttu-id="9e35e-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-175">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9e35e-176">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="9e35e-176">subscribers</span></span> | <span data-ttu-id="9e35e-177">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="9e35e-177">JSON Array</span></span> | <span data-ttu-id="9e35e-178">Array von JSON-Objekten jeder Teilnehmer an der Gruppe darstellt</span><span class="sxs-lookup"><span data-stu-id="9e35e-178">Array of JSON objects each representing a subscriber of the group</span></span> |
| <span data-ttu-id="9e35e-179">Cursor</span><span class="sxs-lookup"><span data-stu-id="9e35e-179">cursor</span></span> | <span data-ttu-id="9e35e-180">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-180">String</span></span> | <span data-ttu-id="9e35e-181">Anfang des Resultset.</span><span class="sxs-lookup"><span data-stu-id="9e35e-181">Start of resultset.</span></span> <span data-ttu-id="9e35e-182">Für die Paginierung.</span><span class="sxs-lookup"><span data-stu-id="9e35e-182">For pagination.</span></span> <span data-ttu-id="9e35e-183">Legen Sie für die nächste Ergebnis im Textkörper der Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e35e-183">To be used in Request body for fetching next result set.</span></span> <span data-ttu-id="9e35e-184">Teilnehmende Antwort nur dann, wenn eine gültige nächste Resultset.</span><span class="sxs-lookup"><span data-stu-id="9e35e-184">Present in response only if there is a valid next result set.</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="9e35e-185">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="9e35e-185">Sample JSON Response</span></span>

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

### <a name="remove-subscribers"></a><span data-ttu-id="9e35e-186">/Subscribers entfernen</span><span class="sxs-lookup"><span data-stu-id="9e35e-186">REMOVE /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove

##### <a name="request-parameters"></a><span data-ttu-id="9e35e-187">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-187">Request Parameters</span></span>
|  | <span data-ttu-id="9e35e-188">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-188">Parameter</span></span> | <span data-ttu-id="9e35e-189">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-189">Type</span></span> | <span data-ttu-id="9e35e-190">Optional?</span><span class="sxs-lookup"><span data-stu-id="9e35e-190">Optional?</span></span> | <span data-ttu-id="9e35e-191">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-191">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9e35e-192">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-192">URL Path Parameter</span></span> | <span data-ttu-id="9e35e-193">groupId</span><span class="sxs-lookup"><span data-stu-id="9e35e-193">groupId</span></span> | <span data-ttu-id="9e35e-194">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-194">String</span></span> | <span data-ttu-id="9e35e-195">Nein</span><span class="sxs-lookup"><span data-stu-id="9e35e-195">No</span></span> | <span data-ttu-id="9e35e-196">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e35e-196">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="9e35e-197">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9e35e-197">HTTP Header</span></span> | <span data-ttu-id="9e35e-198">accessToken</span><span class="sxs-lookup"><span data-stu-id="9e35e-198">accessToken</span></span> | <span data-ttu-id="9e35e-199">String</span><span class="sxs-lookup"><span data-stu-id="9e35e-199">String</span></span> | <span data-ttu-id="9e35e-200">Nein</span><span class="sxs-lookup"><span data-stu-id="9e35e-200">No</span></span> | <span data-ttu-id="9e35e-201">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="9e35e-201">Access Token received from the auth end-point</span></span> |

##### <a name="request-body"></a><span data-ttu-id="9e35e-202">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="9e35e-202">Request body</span></span>
| <span data-ttu-id="9e35e-203">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-203">Parameter</span></span> | <span data-ttu-id="9e35e-204">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-204">Type</span></span> | <span data-ttu-id="9e35e-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-205">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9e35e-206">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="9e35e-206">subscribers</span></span> | <span data-ttu-id="9e35e-207">String]</span><span class="sxs-lookup"><span data-stu-id="9e35e-207">String[]</span></span> | <span data-ttu-id="9e35e-208">Jede Zeichenfolge stellt Mobiltelefonnummer mit Ländercode (z. B..</span><span class="sxs-lookup"><span data-stu-id="9e35e-208">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="9e35e-209">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="9e35e-209">+911111111111)</span></span> |

###### <a name="sample-json-request"></a><span data-ttu-id="9e35e-210">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e35e-210">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

##### <a name="response-body"></a><span data-ttu-id="9e35e-211">Antworttext</span><span class="sxs-lookup"><span data-stu-id="9e35e-211">Response body</span></span>
| <span data-ttu-id="9e35e-212">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e35e-212">Parameter</span></span> | <span data-ttu-id="9e35e-213">Typ</span><span class="sxs-lookup"><span data-stu-id="9e35e-213">Type</span></span> | <span data-ttu-id="9e35e-214">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e35e-214">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9e35e-215">result</span><span class="sxs-lookup"><span data-stu-id="9e35e-215">result</span></span> | <span data-ttu-id="9e35e-216">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e35e-216">JSON object</span></span> | <span data-ttu-id="9e35e-217">Jeder Schlüssel in Json-Objekt repräsentiert die Mobiltelefonnummer und Wert darstellt, enthält Erfolg oder Fehler mit Grund Json-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e35e-217">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="9e35e-218">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="9e35e-218">Sample JSON Response</span></span>

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

