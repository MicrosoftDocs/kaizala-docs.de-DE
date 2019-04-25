---
title: /Responses
description: Referenzartikel zur API zum Abrufen von Antwortdaten für Kaizala-Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: 7eee4d159fa932bec1e949ea6fd2b558d2154e7b
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190726"
---
# <a name="post-response-to-an-action"></a><span data-ttu-id="12da4-103">Post-Antwort auf eine Aktion</span><span class="sxs-lookup"><span data-stu-id="12da4-103">Post response to an Action</span></span>
## <a name="post-responses"></a><span data-ttu-id="12da4-104">POST/Responses</span><span class="sxs-lookup"><span data-stu-id="12da4-104">POST /responses</span></span>

    POST {endpoint-url}/groups/{groupId}/actions/{actionId}/responses

### <a name="request-parameters"></a><span data-ttu-id="12da4-105">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="12da4-105">Request Parameters</span></span>

|  | <span data-ttu-id="12da4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-106">Parameter</span></span> | <span data-ttu-id="12da4-107">Typ</span><span class="sxs-lookup"><span data-stu-id="12da4-107">Type</span></span> | <span data-ttu-id="12da4-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="12da4-108">Optional?</span></span> | <span data-ttu-id="12da4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12da4-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="12da4-110">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-110">URL Path Parameter</span></span> | <span data-ttu-id="12da4-111">groupId</span><span class="sxs-lookup"><span data-stu-id="12da4-111">groupId</span></span> | <span data-ttu-id="12da4-112">String</span><span class="sxs-lookup"><span data-stu-id="12da4-112">String</span></span> | <span data-ttu-id="12da4-113">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-113">No</span></span> | <span data-ttu-id="12da4-114">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12da4-114">Group Identifier</span></span> |
| <span data-ttu-id="12da4-115">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-115">URL Path Parameter</span></span> | <span data-ttu-id="12da4-116">actionId</span><span class="sxs-lookup"><span data-stu-id="12da4-116">actionId</span></span> | <span data-ttu-id="12da4-117">String</span><span class="sxs-lookup"><span data-stu-id="12da4-117">String</span></span> | <span data-ttu-id="12da4-118">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-118">No</span></span> | <span data-ttu-id="12da4-119">Aktionsbezeichner</span><span class="sxs-lookup"><span data-stu-id="12da4-119">Action Identifier</span></span> |
| <span data-ttu-id="12da4-120">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="12da4-120">HTTP Header</span></span> | <span data-ttu-id="12da4-121">accessToken</span><span class="sxs-lookup"><span data-stu-id="12da4-121">accessToken</span></span> | <span data-ttu-id="12da4-122">String</span><span class="sxs-lookup"><span data-stu-id="12da4-122">String</span></span> | <span data-ttu-id="12da4-123">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-123">No</span></span> | <span data-ttu-id="12da4-124">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="12da4-124">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="12da4-125">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="12da4-125">HTTP Header</span></span> | <span data-ttu-id="12da4-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="12da4-126">Content-Type</span></span> | <span data-ttu-id="12da4-127">String</span><span class="sxs-lookup"><span data-stu-id="12da4-127">String</span></span> | <span data-ttu-id="12da4-128">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-128">No</span></span> | <span data-ttu-id="12da4-129">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="12da4-129">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="12da4-130">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="12da4-130">Request body</span></span>

| <span data-ttu-id="12da4-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-131">Parameter</span></span> | <span data-ttu-id="12da4-132">Typ</span><span class="sxs-lookup"><span data-stu-id="12da4-132">Type</span></span> | <span data-ttu-id="12da4-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12da4-133">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="12da4-134">id</span><span class="sxs-lookup"><span data-stu-id="12da4-134">id</span></span> | <span data-ttu-id="12da4-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="12da4-135">String</span></span> | <span data-ttu-id="12da4-136">ID des Kaizala-Aktionspakets.</span><span class="sxs-lookup"><span data-stu-id="12da4-136">Id of the Kaizala Action package.</span></span> <span data-ttu-id="12da4-137">Entweder von ActionType oder ID sollte angegeben werden</span><span class="sxs-lookup"><span data-stu-id="12da4-137">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="12da4-138">actionType</span><span class="sxs-lookup"><span data-stu-id="12da4-138">actionType</span></span> | <span data-ttu-id="12da4-139">String</span><span class="sxs-lookup"><span data-stu-id="12da4-139">String</span></span> | <span data-ttu-id="12da4-140">Enum "Survey"/"Job".</span><span class="sxs-lookup"><span data-stu-id="12da4-140">Enum "Survey"/"Job".</span></span> <span data-ttu-id="12da4-141">Entweder von ActionType oder ID sollte angegeben werden</span><span class="sxs-lookup"><span data-stu-id="12da4-141">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="12da4-142">Antwort-Nr.</span><span class="sxs-lookup"><span data-stu-id="12da4-142">responseId</span></span> | <span data-ttu-id="12da4-143">String</span><span class="sxs-lookup"><span data-stu-id="12da4-143">String</span></span> | <span data-ttu-id="12da4-144">Zum Aktualisieren vorhandener Antwort</span><span class="sxs-lookup"><span data-stu-id="12da4-144">For updating existing response</span></span> |
| <span data-ttu-id="12da4-145">actionBody</span><span class="sxs-lookup"><span data-stu-id="12da4-145">actionBody</span></span> | <span data-ttu-id="12da4-146">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="12da4-146">JSON Object</span></span> | <span data-ttu-id="12da4-147">Objekt, das die für die jeweilige Aktion erforderlichen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="12da4-147">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="12da4-148">Die unten definierten Parameter für jede der unterstützten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="12da4-148">Parameters defined below for each of the supported Actions.</span></span> |

#### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="12da4-149">actionBody für eine Auftragsaktion</span><span class="sxs-lookup"><span data-stu-id="12da4-149">actionBody for a Job Action</span></span>

| <span data-ttu-id="12da4-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-150">Parameter</span></span> | <span data-ttu-id="12da4-151">Typ</span><span class="sxs-lookup"><span data-stu-id="12da4-151">Type</span></span> | <span data-ttu-id="12da4-152">Optional?</span><span class="sxs-lookup"><span data-stu-id="12da4-152">Optional?</span></span> | <span data-ttu-id="12da4-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12da4-153">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="12da4-154">isCompleted</span><span class="sxs-lookup"><span data-stu-id="12da4-154">isCompleted</span></span> | <span data-ttu-id="12da4-155">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="12da4-155">Bool</span></span> | <span data-ttu-id="12da4-156">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-156">No</span></span> | <span data-ttu-id="12da4-157">Markieren des Auftrags als abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="12da4-157">Mark the job as completed</span></span> |


##### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="12da4-158">JSON-Beispielanforderung für eine Auftragsaktion</span><span class="sxs-lookup"><span data-stu-id="12da4-158">Sample JSON Request for a Job Action</span></span>

```javascript
{
    actionType:"Job",
    actionBody: {
        isCompleted : true
    }
}
```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="12da4-159">actionBody für eine Umfrageaktion oder eine Aktionspaket Instanz (ID):</span><span class="sxs-lookup"><span data-stu-id="12da4-159">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="12da4-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-160">Parameter</span></span> | <span data-ttu-id="12da4-161">Typ</span><span class="sxs-lookup"><span data-stu-id="12da4-161">Type</span></span> | <span data-ttu-id="12da4-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="12da4-162">Optional?</span></span> | <span data-ttu-id="12da4-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12da4-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="12da4-164">Antwortname</span><span class="sxs-lookup"><span data-stu-id="12da4-164">responseName</span></span> | <span data-ttu-id="12da4-165">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="12da4-165">String</span></span> | <span data-ttu-id="12da4-166">Ja</span><span class="sxs-lookup"><span data-stu-id="12da4-166">Yes</span></span> | <span data-ttu-id="12da4-167">Zur eindeutigen Identifizierung einer Antwort</span><span class="sxs-lookup"><span data-stu-id="12da4-167">For uniquely identifying a response</span></span> |
| <span data-ttu-id="12da4-168">responseLocation</span><span class="sxs-lookup"><span data-stu-id="12da4-168">responseLocation</span></span> | <span data-ttu-id="12da4-169">Objekt "Location"</span><span class="sxs-lookup"><span data-stu-id="12da4-169">Location object</span></span> | <span data-ttu-id="12da4-170">Ja</span><span class="sxs-lookup"><span data-stu-id="12da4-170">Yes</span></span> | <span data-ttu-id="12da4-171">Zur Identifizierung des Standorts der Antwort</span><span class="sxs-lookup"><span data-stu-id="12da4-171">For identifying response's location</span></span> |
| <span data-ttu-id="12da4-172">Antworten</span><span class="sxs-lookup"><span data-stu-id="12da4-172">answers</span></span> | <span data-ttu-id="12da4-173">object[]</span><span class="sxs-lookup"><span data-stu-id="12da4-173">object[]</span></span> | <span data-ttu-id="12da4-174">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-174">No</span></span> | <span data-ttu-id="12da4-175">Antwort der einzelnen Fragen (basierend auf Index).</span><span class="sxs-lookup"><span data-stu-id="12da4-175">Answer of each question(based on index).</span></span> <span data-ttu-id="12da4-176">Objekt wird vom Typ String für Fragentyp: SingleOption/Text/Image, Object vom Typ String [] für Fragentyp: multiOption/Attachmentlist, Objekt vom Typ Double für Fragentyp: numerisch/Datum</span><span class="sxs-lookup"><span data-stu-id="12da4-176">object will be of type string for question type: SingleOption/Text/Image, object will be of type string[] for question type: MultiOption/AttachmentList, object will be of type double for question type: Numeric/Date</span></span> |

##### <a name="structure-for-location-object"></a><span data-ttu-id="12da4-177">Struktur für Location-Objekt</span><span class="sxs-lookup"><span data-stu-id="12da4-177">Structure for Location object</span></span>

| <span data-ttu-id="12da4-178">Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-178">Parameter</span></span> | <span data-ttu-id="12da4-179">Typ</span><span class="sxs-lookup"><span data-stu-id="12da4-179">Type</span></span> | <span data-ttu-id="12da4-180">Optional?</span><span class="sxs-lookup"><span data-stu-id="12da4-180">Optional?</span></span> | <span data-ttu-id="12da4-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12da4-181">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="12da4-182">latitude</span><span class="sxs-lookup"><span data-stu-id="12da4-182">latitude</span></span> | <span data-ttu-id="12da4-183">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="12da4-183">Double</span></span> | <span data-ttu-id="12da4-184">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-184">No</span></span> | <span data-ttu-id="12da4-185">Breitengrad des Standorts</span><span class="sxs-lookup"><span data-stu-id="12da4-185">Latitude of the location</span></span> |
| <span data-ttu-id="12da4-186">longitude</span><span class="sxs-lookup"><span data-stu-id="12da4-186">longitude</span></span> | <span data-ttu-id="12da4-187">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="12da4-187">Double</span></span> | <span data-ttu-id="12da4-188">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-188">No</span></span> | <span data-ttu-id="12da4-189">Länge des Standorts</span><span class="sxs-lookup"><span data-stu-id="12da4-189">Longitude of the location</span></span> |
| <span data-ttu-id="12da4-190">name</span><span class="sxs-lookup"><span data-stu-id="12da4-190">name</span></span> | <span data-ttu-id="12da4-191">String</span><span class="sxs-lookup"><span data-stu-id="12da4-191">String</span></span> | <span data-ttu-id="12da4-192">Nein</span><span class="sxs-lookup"><span data-stu-id="12da4-192">No</span></span> | <span data-ttu-id="12da4-193">Name des Standorts</span><span class="sxs-lookup"><span data-stu-id="12da4-193">Name of the location</span></span> |

##### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="12da4-194">JSON-Beispielanforderung für eine Umfrageaktion</span><span class="sxs-lookup"><span data-stu-id="12da4-194">Sample JSON Request for a Survey Action</span></span>

```javascript
{
  "actionType" : "Survey",
  "actionBody" : 
  {
    "responseName" : "API response",
    "responseLocation" : 
    {
      "latitude" : 1, 
      "longitude" : 1, 
      "name" : "locationName234"
    },
    "Answers" : ["Response from API", "Opt1", ["MOpt1","MOpt2"],123,{"lt" : 1, "lg" : 1, "n":"cool"}, 1500377471, "eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNVcFRWRlZXVjFoWldtTmtaV1puYUdscWMzUjFkbmQ0ZVhxRGhJV0doNGlKaXBLVGxKV1dsNWlabXFLanBLV21wNmlwcXJLenRMVzJ0N2k1dXNMRHhNWEd4OGpKeXRMVDFOWFcxOWpaMnVIaTQrVGw1dWZvNmVyeDh2UDA5ZmIzK1BuNi84UUFId0VBQXdFQkFRRUJBUUVCQVFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSRUFBZ0VDQkFRREJBY0ZCQVFBQVFKM0FBRUNBeEVFQlNFeEJoSkJVUWRoY1JNaU1vRUlGRUtSb2JIQkNTTXpVdkFWWW5MUkNoWWtOT0VsOFJjWUdSb21KeWdwS2pVMk56ZzVPa05FUlVaSFNFbEtVMVJWVmxkWVdWcGpaR1ZtWjJocGFuTjBkWFozZUhsNmdvT0VoWWFIaUltS2twT1VsWmFYbUptYW9xT2twYWFucUttcXNyTzB0YmEzdUxtNndzUEV4Y2JIeU1uSzB0UFUxZGJYMk5uYTR1UGs1ZWJuNk9ucTh2UDA5ZmIzK1BuNi85b0FEQU1CQUFJUkF4RUFQd0N4UlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVsQUMwVW1hTTByZ0xSU1pvelJjQmFLVE5HYUxnTFJTWm96UmNCYUtUTkdhTGdMUlNab3pSY0JhS1ROR2FMb0JhS0tLWUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSWVsTFNIcFNld0MwVVVVd0NpaWs3MEFMUlNZb3hTMUFXaWt4UmlqVUJhS1RGR0tOUUZvcE1VWW8xQVdrUFNqRkJIRkR2WUJhS1RGR0tOUUZvcE1VWW8xQVdpa3hSaWpVQmFLVEZHS05RRm9wQlMwd0NpaWlnQW9vb29BS0tLS0FDaWlpZ0FwRDBwYVE5S1QyQVdpaWltQVVuZWxwTzlJQmFLS0tZQlJSUlFBVVVVVUFGRkZGQUJTSHBTMGg2VW5zQXRGRkZNQW9vb29BS0tLS0FDaWlpZ0JPOUxTZDZXa2dDaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFKaWpGTFJTc2dFeFJpbHBPOUZrQVlveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQlJSUlRBS0tLS0FDaWlpZ0Fvb29vQVR2UzBuZWxwSUFvb29wZ0ZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVuZWxwTzlMc0F0RkZGTUFvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FFNzB0SjNwYVNBS0tLS1lCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSjNwYVR2U0FXaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFDZDZXazcwdEpBRkZGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDa3BhS0FFeFJpbG9wV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDVXRGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdELzlrPSIsIkFjdGlvblR5cGUiOjMsIkZpbGVzIjpbeyJJZCI6ImU1Y2YyMWJmLWQ3OGItNGY4Yi1iYjY3LTM2NTJlNDk1ZDEyZSIsIk5hbWUiOiJ0ZXN0LnBuZyIsIlNpemUiOjQsIlVybCI6Imh0dHBzOi8vY2RuLmthc2NvcmUub3NpLm9mZmljZS5uZXQvNzVlOGU3YjYzZDJhNGMxMGNkYzMwMjA4YWEyN2YxYzI5ODdkODY4YTBlNzY0ZmM3NDJhOTRmNjU0OWQ4YmRiMi5wbmc/c3Y9MjAxNS0xMi0xMSZzcj1iJnNpZz00aXFzd2pGVll5cUdxeUtnNmNkTWRVUW1pQWV6OHNWOTUxVVNjVW1MekxrJTNEJnN0PTIwMTctMDUtMTdUMDclM0EwNCUzQTQxWiZzZT0yMjkxLTAzLTAyVDA4JTNBMDQlM0E0MVomc3A9ciJ9XX0="]
  }
}
```
<span data-ttu-id="12da4-195">Sie müssen Image (v1/Media-API) hochladen und dann mediaResource der Antwort als Antwort auf Bildtyp Frage verwenden.</span><span class="sxs-lookup"><span data-stu-id="12da4-195">You need to upload image (v1/media api) and then use mediaResource of the response as answer to Image type question.</span></span>

#### <a name="response-body"></a><span data-ttu-id="12da4-196">Antworttext</span><span class="sxs-lookup"><span data-stu-id="12da4-196">Response body</span></span>

| <span data-ttu-id="12da4-197">Parameter</span><span class="sxs-lookup"><span data-stu-id="12da4-197">Parameter</span></span> | <span data-ttu-id="12da4-198">Typ</span><span class="sxs-lookup"><span data-stu-id="12da4-198">Type</span></span> | <span data-ttu-id="12da4-199">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12da4-199">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="12da4-200">Antwort-Nr.</span><span class="sxs-lookup"><span data-stu-id="12da4-200">responseId</span></span> | <span data-ttu-id="12da4-201">String</span><span class="sxs-lookup"><span data-stu-id="12da4-201">String</span></span> | <span data-ttu-id="12da4-202">Antwort-ID.</span><span class="sxs-lookup"><span data-stu-id="12da4-202">Response Identifier.</span></span> <span data-ttu-id="12da4-203">Können Sie für die Aktualisierung der Antwort verwendet werden</span><span class="sxs-lookup"><span data-stu-id="12da4-203">Can you be used for updating response</span></span> |

```javascript
{
    "responseId": "bbcf469e-4027-40b7-a80b-a961a48619e7"
}
```
