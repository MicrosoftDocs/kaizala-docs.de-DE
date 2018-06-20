---
title: /Responses
description: Referenzartikel für API zum Abrufen von Daten für Kaizala Aktionen
topic: Reference
author: nitinjms
ms.openlocfilehash: f22c65a754c3b86cf59991c33a43d0ef83a5472c
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905324"
---
# <a name="post-response-to-an-action"></a><span data-ttu-id="e1851-103">POST-Antwort auf eine Aktivität</span><span class="sxs-lookup"><span data-stu-id="e1851-103">Post response to an Action</span></span>
### <a name="post-responses"></a><span data-ttu-id="e1851-104">POST-/responses</span><span class="sxs-lookup"><span data-stu-id="e1851-104">POST /responses</span></span>

    POST {endpoint-url}/groups/{groupId}/actions/{actionId}/responses

##### <a name="request-parameters"></a><span data-ttu-id="e1851-105">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="e1851-105">Request Parameters</span></span>

|  | <span data-ttu-id="e1851-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-106">Parameter</span></span> | <span data-ttu-id="e1851-107">Typ</span><span class="sxs-lookup"><span data-stu-id="e1851-107">Type</span></span> | <span data-ttu-id="e1851-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="e1851-108">Optional?</span></span> | <span data-ttu-id="e1851-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1851-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="e1851-110">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-110">URL Path Parameter</span></span> | <span data-ttu-id="e1851-111">groupId</span><span class="sxs-lookup"><span data-stu-id="e1851-111">groupId</span></span> | <span data-ttu-id="e1851-112">String</span><span class="sxs-lookup"><span data-stu-id="e1851-112">String</span></span> | <span data-ttu-id="e1851-113">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-113">No</span></span> | <span data-ttu-id="e1851-114">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="e1851-114">Group Identifier</span></span> |
| <span data-ttu-id="e1851-115">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-115">URL Path Parameter</span></span> | <span data-ttu-id="e1851-116">actionId</span><span class="sxs-lookup"><span data-stu-id="e1851-116">actionId</span></span> | <span data-ttu-id="e1851-117">String</span><span class="sxs-lookup"><span data-stu-id="e1851-117">String</span></span> | <span data-ttu-id="e1851-118">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-118">No</span></span> | <span data-ttu-id="e1851-119">Aktionsbezeichner</span><span class="sxs-lookup"><span data-stu-id="e1851-119">Action Identifier</span></span> |
| <span data-ttu-id="e1851-120">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="e1851-120">HTTP Header</span></span> | <span data-ttu-id="e1851-121">accessToken</span><span class="sxs-lookup"><span data-stu-id="e1851-121">accessToken</span></span> | <span data-ttu-id="e1851-122">String</span><span class="sxs-lookup"><span data-stu-id="e1851-122">String</span></span> | <span data-ttu-id="e1851-123">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-123">No</span></span> | <span data-ttu-id="e1851-124">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e1851-124">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="e1851-125">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="e1851-125">HTTP Header</span></span> | <span data-ttu-id="e1851-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e1851-126">Content-Type</span></span> | <span data-ttu-id="e1851-127">String</span><span class="sxs-lookup"><span data-stu-id="e1851-127">String</span></span> | <span data-ttu-id="e1851-128">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-128">No</span></span> | <span data-ttu-id="e1851-129">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="e1851-129">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="e1851-130">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="e1851-130">Request body</span></span>

| <span data-ttu-id="e1851-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-131">Parameter</span></span> | <span data-ttu-id="e1851-132">Typ</span><span class="sxs-lookup"><span data-stu-id="e1851-132">Type</span></span> | <span data-ttu-id="e1851-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1851-133">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="e1851-134">id</span><span class="sxs-lookup"><span data-stu-id="e1851-134">id</span></span> | <span data-ttu-id="e1851-135">String</span><span class="sxs-lookup"><span data-stu-id="e1851-135">String</span></span> | <span data-ttu-id="e1851-136">ID des Pakets Kaizala Aktion.</span><span class="sxs-lookup"><span data-stu-id="e1851-136">Id of the Kaizala Action package.</span></span> <span data-ttu-id="e1851-137">Entweder ActionType oder Id muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="e1851-137">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="e1851-138">actionType</span><span class="sxs-lookup"><span data-stu-id="e1851-138">actionType</span></span> | <span data-ttu-id="e1851-139">String</span><span class="sxs-lookup"><span data-stu-id="e1851-139">String</span></span> | <span data-ttu-id="e1851-140">Enumeration "Umfrage" / "Job".</span><span class="sxs-lookup"><span data-stu-id="e1851-140">Enum "Survey"/"Job".</span></span> <span data-ttu-id="e1851-141">Entweder ActionType oder Id muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="e1851-141">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="e1851-142">responseId</span><span class="sxs-lookup"><span data-stu-id="e1851-142">responseId</span></span> | <span data-ttu-id="e1851-143">String</span><span class="sxs-lookup"><span data-stu-id="e1851-143">String</span></span> | <span data-ttu-id="e1851-144">Zum Aktualisieren der vorhandenen Antwort</span><span class="sxs-lookup"><span data-stu-id="e1851-144">For updating existing response</span></span> |
| <span data-ttu-id="e1851-145">actionBody</span><span class="sxs-lookup"><span data-stu-id="e1851-145">actionBody</span></span> | <span data-ttu-id="e1851-146">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="e1851-146">JSON Object</span></span> | <span data-ttu-id="e1851-147">Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1851-147">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="e1851-148">Parameter für die einzelnen unterstützten Aktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e1851-148">Parameters defined below for each of the supported Actions.</span></span> |

###### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="e1851-149">ActionBody für eine Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="e1851-149">actionBody for a Job Action</span></span>

| <span data-ttu-id="e1851-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-150">Parameter</span></span> | <span data-ttu-id="e1851-151">Typ</span><span class="sxs-lookup"><span data-stu-id="e1851-151">Type</span></span> | <span data-ttu-id="e1851-152">Optional?</span><span class="sxs-lookup"><span data-stu-id="e1851-152">Optional?</span></span> | <span data-ttu-id="e1851-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1851-153">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="e1851-154">isCompleted</span><span class="sxs-lookup"><span data-stu-id="e1851-154">isCompleted</span></span> | <span data-ttu-id="e1851-155">Bool</span><span class="sxs-lookup"><span data-stu-id="e1851-155">Bool</span></span> | <span data-ttu-id="e1851-156">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-156">No</span></span> | <span data-ttu-id="e1851-157">Markieren Sie den Auftrag als erledigt</span><span class="sxs-lookup"><span data-stu-id="e1851-157">Mark the job as completed</span></span> |


###### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="e1851-158">Beispiel für eine Anforderung für eine Aktion Auftrag JSON</span><span class="sxs-lookup"><span data-stu-id="e1851-158">Sample JSON Request for a Job Action</span></span>

```javascript
{
    actionType:"Job",
    actionBody: {
        isCompleted : true
    }
}
```

###### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="e1851-159">ActionBody für eine Umfrage oder-Aktion Paket instance(id):</span><span class="sxs-lookup"><span data-stu-id="e1851-159">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="e1851-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-160">Parameter</span></span> | <span data-ttu-id="e1851-161">Typ</span><span class="sxs-lookup"><span data-stu-id="e1851-161">Type</span></span> | <span data-ttu-id="e1851-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="e1851-162">Optional?</span></span> | <span data-ttu-id="e1851-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1851-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="e1851-164">responseName</span><span class="sxs-lookup"><span data-stu-id="e1851-164">responseName</span></span> | <span data-ttu-id="e1851-165">String</span><span class="sxs-lookup"><span data-stu-id="e1851-165">String</span></span> | <span data-ttu-id="e1851-166">Ja</span><span class="sxs-lookup"><span data-stu-id="e1851-166">Yes</span></span> | <span data-ttu-id="e1851-167">Zur eindeutigen Identifizierung einer Antwort</span><span class="sxs-lookup"><span data-stu-id="e1851-167">For uniquely identifying a response</span></span> |
| <span data-ttu-id="e1851-168">responseLocation</span><span class="sxs-lookup"><span data-stu-id="e1851-168">responseLocation</span></span> | <span data-ttu-id="e1851-169">Objekt "Location"</span><span class="sxs-lookup"><span data-stu-id="e1851-169">Location object</span></span> | <span data-ttu-id="e1851-170">Ja</span><span class="sxs-lookup"><span data-stu-id="e1851-170">Yes</span></span> | <span data-ttu-id="e1851-171">Für die Antwort des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="e1851-171">For identifying response's location</span></span> |
| <span data-ttu-id="e1851-172">Antworten</span><span class="sxs-lookup"><span data-stu-id="e1851-172">answers</span></span> | <span data-ttu-id="e1851-173">object[]</span><span class="sxs-lookup"><span data-stu-id="e1851-173">object[]</span></span> | <span data-ttu-id="e1851-174">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-174">No</span></span> | <span data-ttu-id="e1851-175">Antwort von jede Frage (basierend auf Index).</span><span class="sxs-lookup"><span data-stu-id="e1851-175">Answer of each question(based on index).</span></span> <span data-ttu-id="e1851-176">Objekt wird vom Typ String für Fragetyp sein: SingleOption/Text/Image-Objekt wird vom Typ String [] für Fragetyp sein: MultiOption/AttachmentList,-Objekt wird vom Typ double für Fragetyp sein: numerische/Datum</span><span class="sxs-lookup"><span data-stu-id="e1851-176">object will be of type string for question type: SingleOption/Text/Image, object will be of type string[] for question type: MultiOption/AttachmentList, object will be of type double for question type: Numeric/Date</span></span> |

###### <a name="structure-for-location-object"></a><span data-ttu-id="e1851-177">Struktur für Location-Objekt</span><span class="sxs-lookup"><span data-stu-id="e1851-177">Structure for Location object</span></span>

| <span data-ttu-id="e1851-178">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-178">Parameter</span></span> | <span data-ttu-id="e1851-179">Typ</span><span class="sxs-lookup"><span data-stu-id="e1851-179">Type</span></span> | <span data-ttu-id="e1851-180">Optional?</span><span class="sxs-lookup"><span data-stu-id="e1851-180">Optional?</span></span> | <span data-ttu-id="e1851-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1851-181">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="e1851-182">latitude</span><span class="sxs-lookup"><span data-stu-id="e1851-182">latitude</span></span> | <span data-ttu-id="e1851-183">Double</span><span class="sxs-lookup"><span data-stu-id="e1851-183">Double</span></span> | <span data-ttu-id="e1851-184">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-184">No</span></span> | <span data-ttu-id="e1851-185">Breite des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="e1851-185">Latitude of the location</span></span> |
| <span data-ttu-id="e1851-186">longitude</span><span class="sxs-lookup"><span data-stu-id="e1851-186">longitude</span></span> | <span data-ttu-id="e1851-187">Double</span><span class="sxs-lookup"><span data-stu-id="e1851-187">Double</span></span> | <span data-ttu-id="e1851-188">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-188">No</span></span> | <span data-ttu-id="e1851-189">Länge des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="e1851-189">Longitude of the location</span></span> |
| <span data-ttu-id="e1851-190">name</span><span class="sxs-lookup"><span data-stu-id="e1851-190">name</span></span> | <span data-ttu-id="e1851-191">String</span><span class="sxs-lookup"><span data-stu-id="e1851-191">String</span></span> | <span data-ttu-id="e1851-192">Nein</span><span class="sxs-lookup"><span data-stu-id="e1851-192">No</span></span> | <span data-ttu-id="e1851-193">Name des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="e1851-193">Name of the location</span></span> |

###### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="e1851-194">Beispiel für eine Anforderung für eine Aktion Umfrage JSON</span><span class="sxs-lookup"><span data-stu-id="e1851-194">Sample JSON Request for a Survey Action</span></span>

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
<span data-ttu-id="e1851-195">Sie müssen Bild hochladen (v1-Media api) und dann als Antwort auf Bild Typ Frage MediaResource der Antwort verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1851-195">You need to upload image (v1/media api) and then use mediaResource of the response as answer to Image type question.</span></span>

###### <a name="response-body"></a><span data-ttu-id="e1851-196">Antworttext</span><span class="sxs-lookup"><span data-stu-id="e1851-196">Response body</span></span>

| <span data-ttu-id="e1851-197">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1851-197">Parameter</span></span> | <span data-ttu-id="e1851-198">Typ</span><span class="sxs-lookup"><span data-stu-id="e1851-198">Type</span></span> | <span data-ttu-id="e1851-199">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1851-199">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="e1851-200">responseId</span><span class="sxs-lookup"><span data-stu-id="e1851-200">responseId</span></span> | <span data-ttu-id="e1851-201">String</span><span class="sxs-lookup"><span data-stu-id="e1851-201">String</span></span> | <span data-ttu-id="e1851-202">Antwort-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e1851-202">Response Identifier.</span></span> <span data-ttu-id="e1851-203">Sie dienen zum Aktualisieren der Antwort</span><span class="sxs-lookup"><span data-stu-id="e1851-203">Can you be used for updating response</span></span> |

```javascript
{
    "responseId": "bbcf469e-4027-40b7-a80b-a961a48619e7"
}
```
