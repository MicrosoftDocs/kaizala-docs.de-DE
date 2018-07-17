---
title: /Responses
description: Referenzartikel für API zum Abrufen von Daten für Kaizala Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: 7eee4d159fa932bec1e949ea6fd2b558d2154e7b
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399371"
---
# <a name="post-response-to-an-action"></a><span data-ttu-id="23dfb-103">POST-Antwort auf eine Aktivität</span><span class="sxs-lookup"><span data-stu-id="23dfb-103">Post response to an Action</span></span>
## <a name="post-responses"></a><span data-ttu-id="23dfb-104">POST-/responses</span><span class="sxs-lookup"><span data-stu-id="23dfb-104">POST /responses</span></span>

    POST {endpoint-url}/groups/{groupId}/actions/{actionId}/responses

### <a name="request-parameters"></a><span data-ttu-id="23dfb-105">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-105">Request Parameters</span></span>

|  | <span data-ttu-id="23dfb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-106">Parameter</span></span> | <span data-ttu-id="23dfb-107">Typ</span><span class="sxs-lookup"><span data-stu-id="23dfb-107">Type</span></span> | <span data-ttu-id="23dfb-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="23dfb-108">Optional?</span></span> | <span data-ttu-id="23dfb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23dfb-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="23dfb-110">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-110">URL Path Parameter</span></span> | <span data-ttu-id="23dfb-111">groupId</span><span class="sxs-lookup"><span data-stu-id="23dfb-111">groupId</span></span> | <span data-ttu-id="23dfb-112">String</span><span class="sxs-lookup"><span data-stu-id="23dfb-112">String</span></span> | <span data-ttu-id="23dfb-113">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-113">No</span></span> | <span data-ttu-id="23dfb-114">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="23dfb-114">Group Identifier</span></span> |
| <span data-ttu-id="23dfb-115">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-115">URL Path Parameter</span></span> | <span data-ttu-id="23dfb-116">actionId</span><span class="sxs-lookup"><span data-stu-id="23dfb-116">actionId</span></span> | <span data-ttu-id="23dfb-117">String</span><span class="sxs-lookup"><span data-stu-id="23dfb-117">String</span></span> | <span data-ttu-id="23dfb-118">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-118">No</span></span> | <span data-ttu-id="23dfb-119">Aktionsbezeichner</span><span class="sxs-lookup"><span data-stu-id="23dfb-119">Action Identifier</span></span> |
| <span data-ttu-id="23dfb-120">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="23dfb-120">HTTP Header</span></span> | <span data-ttu-id="23dfb-121">accessToken</span><span class="sxs-lookup"><span data-stu-id="23dfb-121">accessToken</span></span> | <span data-ttu-id="23dfb-122">String</span><span class="sxs-lookup"><span data-stu-id="23dfb-122">String</span></span> | <span data-ttu-id="23dfb-123">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-123">No</span></span> | <span data-ttu-id="23dfb-124">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="23dfb-124">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="23dfb-125">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="23dfb-125">HTTP Header</span></span> | <span data-ttu-id="23dfb-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="23dfb-126">Content-Type</span></span> | <span data-ttu-id="23dfb-127">String</span><span class="sxs-lookup"><span data-stu-id="23dfb-127">String</span></span> | <span data-ttu-id="23dfb-128">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-128">No</span></span> | <span data-ttu-id="23dfb-129">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="23dfb-129">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="23dfb-130">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="23dfb-130">Request body</span></span>

| <span data-ttu-id="23dfb-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-131">Parameter</span></span> | <span data-ttu-id="23dfb-132">Typ</span><span class="sxs-lookup"><span data-stu-id="23dfb-132">Type</span></span> | <span data-ttu-id="23dfb-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23dfb-133">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="23dfb-134">id</span><span class="sxs-lookup"><span data-stu-id="23dfb-134">id</span></span> | <span data-ttu-id="23dfb-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="23dfb-135">String</span></span> | <span data-ttu-id="23dfb-136">ID des Pakets Kaizala Aktion.</span><span class="sxs-lookup"><span data-stu-id="23dfb-136">Id of the Kaizala Action package.</span></span> <span data-ttu-id="23dfb-137">Entweder ActionType oder Id muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="23dfb-137">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="23dfb-138">actionType</span><span class="sxs-lookup"><span data-stu-id="23dfb-138">actionType</span></span> | <span data-ttu-id="23dfb-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="23dfb-139">String</span></span> | <span data-ttu-id="23dfb-140">Enumeration "Umfrage" / "Job".</span><span class="sxs-lookup"><span data-stu-id="23dfb-140">Enum "Survey"/"Job".</span></span> <span data-ttu-id="23dfb-141">Entweder ActionType oder Id muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="23dfb-141">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="23dfb-142">responseId</span><span class="sxs-lookup"><span data-stu-id="23dfb-142">responseId</span></span> | <span data-ttu-id="23dfb-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="23dfb-143">String</span></span> | <span data-ttu-id="23dfb-144">Zum Aktualisieren der vorhandenen Antwort</span><span class="sxs-lookup"><span data-stu-id="23dfb-144">For updating existing response</span></span> |
| <span data-ttu-id="23dfb-145">actionBody</span><span class="sxs-lookup"><span data-stu-id="23dfb-145">actionBody</span></span> | <span data-ttu-id="23dfb-146">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="23dfb-146">JSON Object</span></span> | <span data-ttu-id="23dfb-147">Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="23dfb-147">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="23dfb-148">Parameter für die einzelnen unterstützten Aktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="23dfb-148">Parameters defined below for each of the supported Actions.</span></span> |

#### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="23dfb-149">ActionBody für eine Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="23dfb-149">actionBody for a Job Action</span></span>

| <span data-ttu-id="23dfb-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-150">Parameter</span></span> | <span data-ttu-id="23dfb-151">Typ</span><span class="sxs-lookup"><span data-stu-id="23dfb-151">Type</span></span> | <span data-ttu-id="23dfb-152">Optional?</span><span class="sxs-lookup"><span data-stu-id="23dfb-152">Optional?</span></span> | <span data-ttu-id="23dfb-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23dfb-153">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="23dfb-154">isCompleted</span><span class="sxs-lookup"><span data-stu-id="23dfb-154">isCompleted</span></span> | <span data-ttu-id="23dfb-155">Bool</span><span class="sxs-lookup"><span data-stu-id="23dfb-155">Bool</span></span> | <span data-ttu-id="23dfb-156">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-156">No</span></span> | <span data-ttu-id="23dfb-157">Markieren Sie den Auftrag als erledigt</span><span class="sxs-lookup"><span data-stu-id="23dfb-157">Mark the job as completed</span></span> |


##### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="23dfb-158">Beispiel für eine Anforderung für eine Aktion Auftrag JSON</span><span class="sxs-lookup"><span data-stu-id="23dfb-158">Sample JSON Request for a Job Action</span></span>

```javascript
{
    actionType:"Job",
    actionBody: {
        isCompleted : true
    }
}
```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="23dfb-159">ActionBody für eine Umfrage oder-Aktion Paket instance(id):</span><span class="sxs-lookup"><span data-stu-id="23dfb-159">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="23dfb-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-160">Parameter</span></span> | <span data-ttu-id="23dfb-161">Typ</span><span class="sxs-lookup"><span data-stu-id="23dfb-161">Type</span></span> | <span data-ttu-id="23dfb-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="23dfb-162">Optional?</span></span> | <span data-ttu-id="23dfb-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23dfb-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="23dfb-164">responseName</span><span class="sxs-lookup"><span data-stu-id="23dfb-164">responseName</span></span> | <span data-ttu-id="23dfb-165">String</span><span class="sxs-lookup"><span data-stu-id="23dfb-165">String</span></span> | <span data-ttu-id="23dfb-166">Ja</span><span class="sxs-lookup"><span data-stu-id="23dfb-166">Yes</span></span> | <span data-ttu-id="23dfb-167">Zur eindeutigen Identifizierung einer Antwort</span><span class="sxs-lookup"><span data-stu-id="23dfb-167">For uniquely identifying a response</span></span> |
| <span data-ttu-id="23dfb-168">responseLocation</span><span class="sxs-lookup"><span data-stu-id="23dfb-168">responseLocation</span></span> | <span data-ttu-id="23dfb-169">Objekt "Location"</span><span class="sxs-lookup"><span data-stu-id="23dfb-169">Location object</span></span> | <span data-ttu-id="23dfb-170">Ja</span><span class="sxs-lookup"><span data-stu-id="23dfb-170">Yes</span></span> | <span data-ttu-id="23dfb-171">Für die Antwort des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="23dfb-171">For identifying response's location</span></span> |
| <span data-ttu-id="23dfb-172">Antworten</span><span class="sxs-lookup"><span data-stu-id="23dfb-172">answers</span></span> | <span data-ttu-id="23dfb-173">object[]</span><span class="sxs-lookup"><span data-stu-id="23dfb-173">object[]</span></span> | <span data-ttu-id="23dfb-174">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-174">No</span></span> | <span data-ttu-id="23dfb-175">Antwort von jede Frage (basierend auf Index).</span><span class="sxs-lookup"><span data-stu-id="23dfb-175">Answer of each question(based on index).</span></span> <span data-ttu-id="23dfb-176">Objekt wird vom Typ String für Fragetyp sein: SingleOption/Text/Image-Objekt wird vom Typ String [] für Fragetyp sein: MultiOption/AttachmentList,-Objekt wird vom Typ double für Fragetyp sein: numerische/Datum</span><span class="sxs-lookup"><span data-stu-id="23dfb-176">object will be of type string for question type: SingleOption/Text/Image, object will be of type string[] for question type: MultiOption/AttachmentList, object will be of type double for question type: Numeric/Date</span></span> |

##### <a name="structure-for-location-object"></a><span data-ttu-id="23dfb-177">Struktur für Location-Objekt</span><span class="sxs-lookup"><span data-stu-id="23dfb-177">Structure for Location object</span></span>

| <span data-ttu-id="23dfb-178">Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-178">Parameter</span></span> | <span data-ttu-id="23dfb-179">Typ</span><span class="sxs-lookup"><span data-stu-id="23dfb-179">Type</span></span> | <span data-ttu-id="23dfb-180">Optional?</span><span class="sxs-lookup"><span data-stu-id="23dfb-180">Optional?</span></span> | <span data-ttu-id="23dfb-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23dfb-181">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="23dfb-182">latitude</span><span class="sxs-lookup"><span data-stu-id="23dfb-182">latitude</span></span> | <span data-ttu-id="23dfb-183">Double</span><span class="sxs-lookup"><span data-stu-id="23dfb-183">Double</span></span> | <span data-ttu-id="23dfb-184">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-184">No</span></span> | <span data-ttu-id="23dfb-185">Breite des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="23dfb-185">Latitude of the location</span></span> |
| <span data-ttu-id="23dfb-186">longitude</span><span class="sxs-lookup"><span data-stu-id="23dfb-186">longitude</span></span> | <span data-ttu-id="23dfb-187">Double</span><span class="sxs-lookup"><span data-stu-id="23dfb-187">Double</span></span> | <span data-ttu-id="23dfb-188">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-188">No</span></span> | <span data-ttu-id="23dfb-189">Länge des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="23dfb-189">Longitude of the location</span></span> |
| <span data-ttu-id="23dfb-190">name</span><span class="sxs-lookup"><span data-stu-id="23dfb-190">name</span></span> | <span data-ttu-id="23dfb-191">String</span><span class="sxs-lookup"><span data-stu-id="23dfb-191">String</span></span> | <span data-ttu-id="23dfb-192">Nein</span><span class="sxs-lookup"><span data-stu-id="23dfb-192">No</span></span> | <span data-ttu-id="23dfb-193">Name des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="23dfb-193">Name of the location</span></span> |

##### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="23dfb-194">Beispiel für eine Anforderung für eine Aktion Umfrage JSON</span><span class="sxs-lookup"><span data-stu-id="23dfb-194">Sample JSON Request for a Survey Action</span></span>

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
<span data-ttu-id="23dfb-195">Sie müssen Bild hochladen (v1-Media api) und dann als Antwort auf Bild Typ Frage MediaResource der Antwort verwenden.</span><span class="sxs-lookup"><span data-stu-id="23dfb-195">You need to upload image (v1/media api) and then use mediaResource of the response as answer to Image type question.</span></span>

#### <a name="response-body"></a><span data-ttu-id="23dfb-196">Antworttext</span><span class="sxs-lookup"><span data-stu-id="23dfb-196">Response body</span></span>

| <span data-ttu-id="23dfb-197">Parameter</span><span class="sxs-lookup"><span data-stu-id="23dfb-197">Parameter</span></span> | <span data-ttu-id="23dfb-198">Typ</span><span class="sxs-lookup"><span data-stu-id="23dfb-198">Type</span></span> | <span data-ttu-id="23dfb-199">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23dfb-199">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="23dfb-200">responseId</span><span class="sxs-lookup"><span data-stu-id="23dfb-200">responseId</span></span> | <span data-ttu-id="23dfb-201">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="23dfb-201">String</span></span> | <span data-ttu-id="23dfb-202">Antwort-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="23dfb-202">Response Identifier.</span></span> <span data-ttu-id="23dfb-203">Sie dienen zum Aktualisieren der Antwort</span><span class="sxs-lookup"><span data-stu-id="23dfb-203">Can you be used for updating response</span></span> |

```javascript
{
    "responseId": "bbcf469e-4027-40b7-a80b-a961a48619e7"
}
```
