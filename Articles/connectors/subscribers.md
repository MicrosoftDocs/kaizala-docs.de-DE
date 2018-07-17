---
title: /Subscribers
description: Verweisen auf Artikel, um die API zum Abrufen von Abonnenten Daten für öffentliche Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6f9055ce909ecc24bac77c3770477f405c8d27
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399365"
---
# <a name="subscribers"></a><span data-ttu-id="541a6-103">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="541a6-103">/subscribers</span></span>

<span data-ttu-id="541a6-104">API-Endpunkt hinzufügen, Abrufen oder Abonnenten von verwalteten öffentliche Gruppe löschen.</span><span class="sxs-lookup"><span data-stu-id="541a6-104">API end-point to add, get or delete subscribers from Managed Public group.</span></span>

## <a name="add-subscribers"></a><span data-ttu-id="541a6-105">/Subscribers hinzufügen</span><span class="sxs-lookup"><span data-stu-id="541a6-105">ADD /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/add

### <a name="request-parameters"></a><span data-ttu-id="541a6-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="541a6-106">Request Parameters</span></span>
|  | <span data-ttu-id="541a6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-107">Parameter</span></span> | <span data-ttu-id="541a6-108">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-108">Type</span></span> | <span data-ttu-id="541a6-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="541a6-109">Optional?</span></span> | <span data-ttu-id="541a6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="541a6-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-111">URL Path Parameter</span></span> | <span data-ttu-id="541a6-112">groupId</span><span class="sxs-lookup"><span data-stu-id="541a6-112">groupId</span></span> | <span data-ttu-id="541a6-113">String</span><span class="sxs-lookup"><span data-stu-id="541a6-113">String</span></span> | <span data-ttu-id="541a6-114">Nein</span><span class="sxs-lookup"><span data-stu-id="541a6-114">No</span></span> | <span data-ttu-id="541a6-115">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="541a6-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="541a6-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="541a6-116">HTTP Header</span></span> | <span data-ttu-id="541a6-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="541a6-117">accessToken</span></span> | <span data-ttu-id="541a6-118">String</span><span class="sxs-lookup"><span data-stu-id="541a6-118">String</span></span> | <span data-ttu-id="541a6-119">Nein</span><span class="sxs-lookup"><span data-stu-id="541a6-119">No</span></span> | <span data-ttu-id="541a6-120">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="541a6-120">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="541a6-121">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="541a6-121">Request body</span></span>
| <span data-ttu-id="541a6-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-122">Parameter</span></span> | <span data-ttu-id="541a6-123">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-123">Type</span></span> | <span data-ttu-id="541a6-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="541a6-125">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="541a6-125">subscribers</span></span> | <span data-ttu-id="541a6-126">String]</span><span class="sxs-lookup"><span data-stu-id="541a6-126">String[]</span></span> | <span data-ttu-id="541a6-127">Jede Zeichenfolge stellt Mobiltelefonnummer mit Ländercode (z. B..</span><span class="sxs-lookup"><span data-stu-id="541a6-127">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="541a6-128">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="541a6-128">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="541a6-129">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="541a6-129">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="541a6-130">Antworttext</span><span class="sxs-lookup"><span data-stu-id="541a6-130">Response body</span></span>
| <span data-ttu-id="541a6-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-131">Parameter</span></span> | <span data-ttu-id="541a6-132">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-132">Type</span></span> | <span data-ttu-id="541a6-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-133">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="541a6-134">result</span><span class="sxs-lookup"><span data-stu-id="541a6-134">result</span></span> | <span data-ttu-id="541a6-135">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="541a6-135">JSON object</span></span> | <span data-ttu-id="541a6-136">Jeder Schlüssel in Json-Objekt repräsentiert die Mobiltelefonnummer und Wert darstellt, enthält Erfolg oder Fehler mit Grund Json-Objekt</span><span class="sxs-lookup"><span data-stu-id="541a6-136">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="541a6-137">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="541a6-137">Sample JSON Response</span></span>

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

## <a name="get-subscribers"></a><span data-ttu-id="541a6-138">Abrufen von /subscribers</span><span class="sxs-lookup"><span data-stu-id="541a6-138">GET /subscribers</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subscribers

### <a name="request-parameters"></a><span data-ttu-id="541a6-139">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="541a6-139">Request Parameters</span></span>
|  | <span data-ttu-id="541a6-140">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-140">Parameter</span></span> | <span data-ttu-id="541a6-141">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-141">Type</span></span> | <span data-ttu-id="541a6-142">Optional?</span><span class="sxs-lookup"><span data-stu-id="541a6-142">Optional?</span></span> | <span data-ttu-id="541a6-143">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-143">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="541a6-144">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-144">URL Path Parameter</span></span> | <span data-ttu-id="541a6-145">groupId</span><span class="sxs-lookup"><span data-stu-id="541a6-145">groupId</span></span> | <span data-ttu-id="541a6-146">String</span><span class="sxs-lookup"><span data-stu-id="541a6-146">String</span></span> | <span data-ttu-id="541a6-147">Nein</span><span class="sxs-lookup"><span data-stu-id="541a6-147">No</span></span> | <span data-ttu-id="541a6-148">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="541a6-148">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="541a6-149">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="541a6-149">HTTP Header</span></span> | <span data-ttu-id="541a6-150">accessToken</span><span class="sxs-lookup"><span data-stu-id="541a6-150">accessToken</span></span> | <span data-ttu-id="541a6-151">String</span><span class="sxs-lookup"><span data-stu-id="541a6-151">String</span></span> | <span data-ttu-id="541a6-152">Nein</span><span class="sxs-lookup"><span data-stu-id="541a6-152">No</span></span> | <span data-ttu-id="541a6-153">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="541a6-153">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="541a6-154">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="541a6-154">Request body</span></span>

| <span data-ttu-id="541a6-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-155">Parameter</span></span> | <span data-ttu-id="541a6-156">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-156">Type</span></span> | <span data-ttu-id="541a6-157">Optional?</span><span class="sxs-lookup"><span data-stu-id="541a6-157">Optional?</span></span> | <span data-ttu-id="541a6-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-158">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="541a6-159">Cursor</span><span class="sxs-lookup"><span data-stu-id="541a6-159">cursor</span></span> | <span data-ttu-id="541a6-160">String</span><span class="sxs-lookup"><span data-stu-id="541a6-160">String</span></span> | <span data-ttu-id="541a6-161">Ja</span><span class="sxs-lookup"><span data-stu-id="541a6-161">Yes</span></span> | <span data-ttu-id="541a6-162">Anfang des Resultset.</span><span class="sxs-lookup"><span data-stu-id="541a6-162">Start of resultset.</span></span> <span data-ttu-id="541a6-163">Für die Paginierung.</span><span class="sxs-lookup"><span data-stu-id="541a6-163">For pagination.</span></span> <span data-ttu-id="541a6-164">In Antworttext zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="541a6-164">Returned in Response Body</span></span> |
| <span data-ttu-id="541a6-165">count</span><span class="sxs-lookup"><span data-stu-id="541a6-165">count</span></span> | <span data-ttu-id="541a6-166">int</span><span class="sxs-lookup"><span data-stu-id="541a6-166">int</span></span> | <span data-ttu-id="541a6-167">Ja</span><span class="sxs-lookup"><span data-stu-id="541a6-167">Yes</span></span> | <span data-ttu-id="541a6-168">Standard: 50.</span><span class="sxs-lookup"><span data-stu-id="541a6-168">Default: 50.</span></span> <span data-ttu-id="541a6-169">Max: 50.</span><span class="sxs-lookup"><span data-stu-id="541a6-169">Max: 50.</span></span> <span data-ttu-id="541a6-170">Anzahl von Abonnenten in einem Resultset zurückgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="541a6-170">Number of subscribers to be returned in a resultset</span></span>|

### <a name="response-body"></a><span data-ttu-id="541a6-171">Antworttext</span><span class="sxs-lookup"><span data-stu-id="541a6-171">Response body</span></span>

| <span data-ttu-id="541a6-172">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-172">Parameter</span></span> | <span data-ttu-id="541a6-173">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-173">Type</span></span> | <span data-ttu-id="541a6-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-174">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="541a6-175">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="541a6-175">subscribers</span></span> | <span data-ttu-id="541a6-176">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="541a6-176">JSON Array</span></span> | <span data-ttu-id="541a6-177">Array von JSON-Objekten jeder Teilnehmer an der Gruppe darstellt</span><span class="sxs-lookup"><span data-stu-id="541a6-177">Array of JSON objects each representing a subscriber of the group</span></span> |
| <span data-ttu-id="541a6-178">Cursor</span><span class="sxs-lookup"><span data-stu-id="541a6-178">cursor</span></span> | <span data-ttu-id="541a6-179">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="541a6-179">String</span></span> | <span data-ttu-id="541a6-180">Anfang des Resultset.</span><span class="sxs-lookup"><span data-stu-id="541a6-180">Start of resultset.</span></span> <span data-ttu-id="541a6-181">Für die Paginierung.</span><span class="sxs-lookup"><span data-stu-id="541a6-181">For pagination.</span></span> <span data-ttu-id="541a6-182">Legen Sie für die nächste Ergebnis im Textkörper der Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="541a6-182">To be used in Request body for fetching next result set.</span></span> <span data-ttu-id="541a6-183">Teilnehmende Antwort nur dann, wenn eine gültige nächste Resultset.</span><span class="sxs-lookup"><span data-stu-id="541a6-183">Present in response only if there is a valid next result set.</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="541a6-184">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="541a6-184">Sample JSON Response</span></span>

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

## <a name="remove-subscribers"></a><span data-ttu-id="541a6-185">/Subscribers entfernen</span><span class="sxs-lookup"><span data-stu-id="541a6-185">REMOVE /subscribers</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/subscribers/remove

### <a name="request-parameters"></a><span data-ttu-id="541a6-186">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="541a6-186">Request Parameters</span></span>
|  | <span data-ttu-id="541a6-187">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-187">Parameter</span></span> | <span data-ttu-id="541a6-188">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-188">Type</span></span> | <span data-ttu-id="541a6-189">Optional?</span><span class="sxs-lookup"><span data-stu-id="541a6-189">Optional?</span></span> | <span data-ttu-id="541a6-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-190">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="541a6-191">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-191">URL Path Parameter</span></span> | <span data-ttu-id="541a6-192">groupId</span><span class="sxs-lookup"><span data-stu-id="541a6-192">groupId</span></span> | <span data-ttu-id="541a6-193">String</span><span class="sxs-lookup"><span data-stu-id="541a6-193">String</span></span> | <span data-ttu-id="541a6-194">Nein</span><span class="sxs-lookup"><span data-stu-id="541a6-194">No</span></span> | <span data-ttu-id="541a6-195">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="541a6-195">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="541a6-196">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="541a6-196">HTTP Header</span></span> | <span data-ttu-id="541a6-197">accessToken</span><span class="sxs-lookup"><span data-stu-id="541a6-197">accessToken</span></span> | <span data-ttu-id="541a6-198">String</span><span class="sxs-lookup"><span data-stu-id="541a6-198">String</span></span> | <span data-ttu-id="541a6-199">Nein</span><span class="sxs-lookup"><span data-stu-id="541a6-199">No</span></span> | <span data-ttu-id="541a6-200">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="541a6-200">Access Token received from the auth end-point</span></span> |

### <a name="request-body"></a><span data-ttu-id="541a6-201">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="541a6-201">Request body</span></span>
| <span data-ttu-id="541a6-202">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-202">Parameter</span></span> | <span data-ttu-id="541a6-203">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-203">Type</span></span> | <span data-ttu-id="541a6-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-204">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="541a6-205">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="541a6-205">subscribers</span></span> | <span data-ttu-id="541a6-206">String]</span><span class="sxs-lookup"><span data-stu-id="541a6-206">String[]</span></span> | <span data-ttu-id="541a6-207">Jede Zeichenfolge stellt Mobiltelefonnummer mit Ländercode (z. B..</span><span class="sxs-lookup"><span data-stu-id="541a6-207">Each string represents mobile number with country code(Eg.</span></span> <span data-ttu-id="541a6-208">+911111111111)</span><span class="sxs-lookup"><span data-stu-id="541a6-208">+911111111111)</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="541a6-209">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="541a6-209">Sample JSON Request</span></span>
```javascript
{
    subscribers : ["+911111111111", "+911111111112"]
}
```

### <a name="response-body"></a><span data-ttu-id="541a6-210">Antworttext</span><span class="sxs-lookup"><span data-stu-id="541a6-210">Response body</span></span>
| <span data-ttu-id="541a6-211">Parameter</span><span class="sxs-lookup"><span data-stu-id="541a6-211">Parameter</span></span> | <span data-ttu-id="541a6-212">Typ</span><span class="sxs-lookup"><span data-stu-id="541a6-212">Type</span></span> | <span data-ttu-id="541a6-213">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="541a6-213">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="541a6-214">result</span><span class="sxs-lookup"><span data-stu-id="541a6-214">result</span></span> | <span data-ttu-id="541a6-215">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="541a6-215">JSON object</span></span> | <span data-ttu-id="541a6-216">Jeder Schlüssel in Json-Objekt repräsentiert die Mobiltelefonnummer und Wert darstellt, enthält Erfolg oder Fehler mit Grund Json-Objekt</span><span class="sxs-lookup"><span data-stu-id="541a6-216">each key of this Json Object represents the mobile number and value represents the Json object containing success or failure with reason</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="541a6-217">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="541a6-217">Sample JSON Response</span></span>

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

