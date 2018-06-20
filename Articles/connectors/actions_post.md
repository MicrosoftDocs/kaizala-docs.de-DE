---
title: / Actions_post
description: Referenzartikel für API-Aktion auf einer Gruppe Kaizala bereitstellen
topic: Reference
author: nitinjms
ms.openlocfilehash: 015a60bbef7be7108cc0edc10e81cc1f8b5636e2
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905329"
---
# <a name="post-a-action-in-a-group"></a><span data-ttu-id="42d81-103">Eine Aktion nach der in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="42d81-103">Post a Action in a group</span></span>
### <a name="post-actions"></a><span data-ttu-id="42d81-104">POST-/actions</span><span class="sxs-lookup"><span data-stu-id="42d81-104">POST /actions</span></span>

    POST {endpoint-url}/groups/{groupId}/actions

##### <a name="request-parameters"></a><span data-ttu-id="42d81-105">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="42d81-105">Request Parameters</span></span>

|  | <span data-ttu-id="42d81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-106">Parameter</span></span> | <span data-ttu-id="42d81-107">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-107">Type</span></span> | <span data-ttu-id="42d81-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-108">Optional?</span></span> | <span data-ttu-id="42d81-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-110">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-110">URL Path Parameter</span></span> | <span data-ttu-id="42d81-111">groupId</span><span class="sxs-lookup"><span data-stu-id="42d81-111">groupId</span></span> | <span data-ttu-id="42d81-112">String</span><span class="sxs-lookup"><span data-stu-id="42d81-112">String</span></span> | <span data-ttu-id="42d81-113">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-113">No</span></span> | <span data-ttu-id="42d81-114">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="42d81-114">Group Identifier</span></span> |
| <span data-ttu-id="42d81-115">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="42d81-115">HTTP Header</span></span> | <span data-ttu-id="42d81-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="42d81-116">accessToken</span></span> | <span data-ttu-id="42d81-117">String</span><span class="sxs-lookup"><span data-stu-id="42d81-117">String</span></span> | <span data-ttu-id="42d81-118">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-118">No</span></span> | <span data-ttu-id="42d81-119">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="42d81-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="42d81-120">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="42d81-120">HTTP Header</span></span> | <span data-ttu-id="42d81-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="42d81-121">Content-Type</span></span> | <span data-ttu-id="42d81-122">String</span><span class="sxs-lookup"><span data-stu-id="42d81-122">String</span></span> | <span data-ttu-id="42d81-123">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-123">No</span></span> | <span data-ttu-id="42d81-124">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="42d81-124">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="42d81-125">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="42d81-125">Request body</span></span>

| <span data-ttu-id="42d81-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-126">Parameter</span></span> | <span data-ttu-id="42d81-127">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-127">Type</span></span> | <span data-ttu-id="42d81-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-128">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="42d81-129">id</span><span class="sxs-lookup"><span data-stu-id="42d81-129">id</span></span> | <span data-ttu-id="42d81-130">String</span><span class="sxs-lookup"><span data-stu-id="42d81-130">String</span></span> | <span data-ttu-id="42d81-131">ID des Pakets Kaizala Aktion.</span><span class="sxs-lookup"><span data-stu-id="42d81-131">Id of the Kaizala Action package.</span></span> <span data-ttu-id="42d81-132">Entweder ActionType oder Id muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="42d81-132">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="42d81-133">actionType</span><span class="sxs-lookup"><span data-stu-id="42d81-133">actionType</span></span> | <span data-ttu-id="42d81-134">String</span><span class="sxs-lookup"><span data-stu-id="42d81-134">String</span></span> | <span data-ttu-id="42d81-135">Enumeration "Umfrage" / "Job".</span><span class="sxs-lookup"><span data-stu-id="42d81-135">Enum "Survey"/"Job".</span></span> <span data-ttu-id="42d81-136">Entweder ActionType oder Id muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="42d81-136">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="42d81-137">actionBody</span><span class="sxs-lookup"><span data-stu-id="42d81-137">actionBody</span></span> | <span data-ttu-id="42d81-138">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="42d81-138">JSON Object</span></span> | <span data-ttu-id="42d81-139">Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="42d81-139">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="42d81-140">Parameter für die einzelnen unterstützten Aktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="42d81-140">Parameters defined below for each of the supported Actions.</span></span> |


###### <a name="actionbody-for-an-announcement-action"></a><span data-ttu-id="42d81-141">ActionBody für eine Ankündigung-Aktion</span><span class="sxs-lookup"><span data-stu-id="42d81-141">actionBody for an Announcement Action</span></span>

| <span data-ttu-id="42d81-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-142">Parameter</span></span> | <span data-ttu-id="42d81-143">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-143">Type</span></span> | <span data-ttu-id="42d81-144">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-144">Optional?</span></span> | <span data-ttu-id="42d81-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-145">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-146">title</span><span class="sxs-lookup"><span data-stu-id="42d81-146">title</span></span> | <span data-ttu-id="42d81-147">String</span><span class="sxs-lookup"><span data-stu-id="42d81-147">String</span></span> | <span data-ttu-id="42d81-148">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-148">No</span></span> | <span data-ttu-id="42d81-149">Titel der Ankündigung</span><span class="sxs-lookup"><span data-stu-id="42d81-149">Title of the Announcement</span></span> |
| <span data-ttu-id="42d81-150">MediaResources</span><span class="sxs-lookup"><span data-stu-id="42d81-150">MediaResources</span></span> | <span data-ttu-id="42d81-151">String]</span><span class="sxs-lookup"><span data-stu-id="42d81-151">String[]</span></span> | <span data-ttu-id="42d81-152">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-152">Yes</span></span> | <span data-ttu-id="42d81-153">Array von Medienressourcen</span><span class="sxs-lookup"><span data-stu-id="42d81-153">Array of media resources</span></span> |
| <span data-ttu-id="42d81-154">Nachricht</span><span class="sxs-lookup"><span data-stu-id="42d81-154">Message</span></span> | <span data-ttu-id="42d81-155">String</span><span class="sxs-lookup"><span data-stu-id="42d81-155">String</span></span> | <span data-ttu-id="42d81-156">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-156">No</span></span> | <span data-ttu-id="42d81-157">Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="42d81-157">Message Body</span></span> |

###### <a name="sample-json-request-for-an-announcement-action"></a><span data-ttu-id="42d81-158">Beispiel für eine Anforderung für eine Aktion Ankündigung JSON</span><span class="sxs-lookup"><span data-stu-id="42d81-158">Sample JSON Request for an Announcement Action</span></span>

```javascript
{
  "actionType" : "Announcement",
  "actionBody" : 
  {
    "Message":"Announcement from API Message text",
    "Title" : "Title text", 
    "MediaResources" : 
    [
      "eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNV","eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VE"
    ]
  }
}

```

###### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="42d81-159">ActionBody für eine Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="42d81-159">actionBody for a Job Action</span></span>

| <span data-ttu-id="42d81-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-160">Parameter</span></span> | <span data-ttu-id="42d81-161">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-161">Type</span></span> | <span data-ttu-id="42d81-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-162">Optional?</span></span> | <span data-ttu-id="42d81-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-164">title</span><span class="sxs-lookup"><span data-stu-id="42d81-164">title</span></span> | <span data-ttu-id="42d81-165">String</span><span class="sxs-lookup"><span data-stu-id="42d81-165">String</span></span> | <span data-ttu-id="42d81-166">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-166">No</span></span> | <span data-ttu-id="42d81-167">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="42d81-167">Title of the Job</span></span> |
| <span data-ttu-id="42d81-168">assignedTo</span><span class="sxs-lookup"><span data-stu-id="42d81-168">assignedTo</span></span> | <span data-ttu-id="42d81-169">String]</span><span class="sxs-lookup"><span data-stu-id="42d81-169">String[]</span></span> | <span data-ttu-id="42d81-170">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-170">No</span></span> | <span data-ttu-id="42d81-171">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="42d81-171">Title of the Job</span></span> |
| <span data-ttu-id="42d81-172">dueDate</span><span class="sxs-lookup"><span data-stu-id="42d81-172">dueDate</span></span> | <span data-ttu-id="42d81-173">long</span><span class="sxs-lookup"><span data-stu-id="42d81-173">long</span></span> | <span data-ttu-id="42d81-174">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-174">Yes</span></span> | <span data-ttu-id="42d81-175">Standard: 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="42d81-175">Default: 24hrs.</span></span> <span data-ttu-id="42d81-176">Anzahl der Stunden, die vor denen Auftrag ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="42d81-176">Number of hours before which job should be completed</span></span> |

###### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="42d81-177">Beispiel für eine Anforderung für eine Aktion Auftrag JSON</span><span class="sxs-lookup"><span data-stu-id="42d81-177">Sample JSON Request for a Job Action</span></span>

```javascript
{
    actionType:"Job",
    actionBody: {
        title : "test job",
        assignedTo : ["+911111111111", "+911111111112"],
        dueDate : 10
    }
}

```

###### <a name="actionbody-for-a-poll-action"></a><span data-ttu-id="42d81-178">ActionBody für eine Aktion eines Abrufs</span><span class="sxs-lookup"><span data-stu-id="42d81-178">actionBody for a Poll Action</span></span>

| <span data-ttu-id="42d81-179">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-179">Parameter</span></span> | <span data-ttu-id="42d81-180">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-180">Type</span></span> | <span data-ttu-id="42d81-181">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-181">Optional?</span></span> | <span data-ttu-id="42d81-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-182">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-183">question</span><span class="sxs-lookup"><span data-stu-id="42d81-183">question</span></span> | <span data-ttu-id="42d81-184">String</span><span class="sxs-lookup"><span data-stu-id="42d81-184">String</span></span> | <span data-ttu-id="42d81-185">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-185">No</span></span> | <span data-ttu-id="42d81-186">Abstimmungsfrage</span><span class="sxs-lookup"><span data-stu-id="42d81-186">Poll Question</span></span> |
| <span data-ttu-id="42d81-187">Choices</span><span class="sxs-lookup"><span data-stu-id="42d81-187">Choices</span></span> | <span data-ttu-id="42d81-188">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="42d81-188">Json Array</span></span> | <span data-ttu-id="42d81-189">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-189">No</span></span> | <span data-ttu-id="42d81-190">Optionen für die Umfrage zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="42d81-190">Choices available for the poll.</span></span> <span data-ttu-id="42d81-191">Jede Auswahl werden unter Komponente:</span><span class="sxs-lookup"><span data-stu-id="42d81-191">Each Choice have below component:</span></span> <ol><li><span data-ttu-id="42d81-192">Titel (obligatorisch & im Zeichenformat)</span><span class="sxs-lookup"><span data-stu-id="42d81-192">title (Mandatory & in String format)</span></span> </li><li><span data-ttu-id="42d81-193">Bild (optional)</span><span class="sxs-lookup"><span data-stu-id="42d81-193">image (optional)</span></span></li></ol> |
| <span data-ttu-id="42d81-194">expiryInHours</span><span class="sxs-lookup"><span data-stu-id="42d81-194">expiryInHours</span></span> | <span data-ttu-id="42d81-195">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="42d81-195">Integer</span></span> | <span data-ttu-id="42d81-196">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-196">Yes</span></span> | <span data-ttu-id="42d81-197">Standard: 720.</span><span class="sxs-lookup"><span data-stu-id="42d81-197">Default:720.</span></span> <span data-ttu-id="42d81-198">Anzahl der Stunden, in denen eine Umfrage Gven abläuft</span><span class="sxs-lookup"><span data-stu-id="42d81-198">Number of hours in which a gven poll would expire</span></span> |

###### <a name="sample-json-request-for-a-poll-action"></a><span data-ttu-id="42d81-199">Beispiel für eine Anforderung für eine Aktion Umfrage JSON</span><span class="sxs-lookup"><span data-stu-id="42d81-199">Sample JSON Request for a Poll Action</span></span>

```javascript
{actionType:"Poll", actionBody:{question:"Do you find Kaizala extensibility easy to use?", 
    choices:
        [
        {title:"Yes",image:"eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNVcFRWRlZXVjFoWldtTmtaV1puYUdscWMzUjFkbmQ0ZVhxRGhJV0doNGlKaXBLVGxKV1dsNWlabXFLanBLV21wNmlwcXJLenRMVzJ0N2k1dXNMRHhNWEd4OGpKeXRMVDFOWFcxOWpaMnVIaTQrVGw1dWZvNmVyeDh2UDA5ZmIzK1BuNi84UUFId0VBQXdFQkFRRUJBUUVCQVFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSRUFBZ0VDQkFRREJBY0ZCQVFBQVFKM0FBRUNBeEVFQlNFeEJoSkJVUWRoY1JNaU1vRUlGRUtSb2JIQkNTTXpVdkFWWW5MUkNoWWtOT0VsOFJjWUdSb21KeWdwS2pVMk56ZzVPa05FUlVaSFNFbEtVMVJWVmxkWVdWcGpaR1ZtWjJocGFuTjBkWFozZUhsNmdvT0VoWWFIaUltS2twT1VsWmFYbUptYW9xT2twYWFucUttcXNyTzB0YmEzdUxtNndzUEV4Y2JIeU1uSzB0UFUxZGJYMk5uYTR1UGs1ZWJuNk9ucTh2UDA5ZmIzK1BuNi85b0FEQU1CQUFJUkF4RUFQd0N4UlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVsQUMwVW1hTTByZ0xSU1pvelJjQmFLVE5HYUxnTFJTWm96UmNCYUtUTkdhTGdMUlNab3pSY0JhS1ROR2FMb0JhS0tLWUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSWVsTFNIcFNld0MwVVVVd0NpaWs3MEFMUlNZb3hTMUFXaWt4UmlqVUJhS1RGR0tOUUZvcE1VWW8xQVdrUFNqRkJIRkR2WUJhS1RGR0tOUUZvcE1VWW8xQVdpa3hSaWpVQmFLVEZHS05RRm9wQlMwd0NpaWlnQW9vb29BS0tLS0FDaWlpZ0FwRDBwYVE5S1QyQVdpaWltQVVuZWxwTzlJQmFLS0tZQlJSUlFBVVVVVUFGRkZGQUJTSHBTMGg2VW5zQXRGRkZNQW9vb29BS0tLS0FDaWlpZ0JPOUxTZDZXa2dDaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFKaWpGTFJTc2dFeFJpbHBPOUZrQVlveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQlJSUlRBS0tLS0FDaWlpZ0Fvb29vQVR2UzBuZWxwSUFvb29wZ0ZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVuZWxwTzlMc0F0RkZGTUFvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FFNzB0SjNwYVNBS0tLS1lCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSjNwYVR2U0FXaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFDZDZXazcwdEpBRkZGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDa3BhS0FFeFJpbG9wV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDVXRGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdELzlrPSIsIkFjdGlvblR5cGUiOjMsIkZpbGVzIjpbeyJJZCI6ImU1Y2YyMWJmLWQ3OGItNGY4Yi1iYjY3LTM2NTJlNDk1ZDEyZSIsIk5hbWUiOiJ0ZXN0LnBuZyIsIlNpemUiOjQsIlVybCI6Imh0dHBzOi8vY2RuLmthc2NvcmUub3NpLm9mZmljZS5uZXQvNzVlOGU3YjYzZDJhNGMxMGNkYzMwMjA4YWEyN2YxYzI5ODdkODY4YTBlNzY0ZmM3NDJhOTRmNjU0OWQ4YmRiMi5wbmc/c3Y9MjAxNS0xMi0xMSZzcj1iJnNpZz00aXFzd2pGVll5cUdxeUtnNmNkTWRVUW1pQWV6OHNWOTUxVVNjVW1MekxrJTNEJnN0PTIwMTctMDUtMTdUMDclM0EwNCUzQTQxWiZzZT0yMjkxLTAzLTAyVDA4JTNBMDQlM0E0MVomc3A9ciJ9XX0="},
        {title:"No"},
        {title:"Not at all"}
        ],
    expiryInHours:10}}
```
###### <a name="actionbody-for-a-lets-meet-action"></a><span data-ttu-id="42d81-200">ActionBody für eine wir erfüllen Aktion</span><span class="sxs-lookup"><span data-stu-id="42d81-200">actionBody for a Let's Meet Action</span></span>

| <span data-ttu-id="42d81-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-201">Parameter</span></span> | <span data-ttu-id="42d81-202">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-202">Type</span></span> | <span data-ttu-id="42d81-203">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-203">Optional?</span></span> | <span data-ttu-id="42d81-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-204">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-205">title</span><span class="sxs-lookup"><span data-stu-id="42d81-205">title</span></span> | <span data-ttu-id="42d81-206">String</span><span class="sxs-lookup"><span data-stu-id="42d81-206">String</span></span> | <span data-ttu-id="42d81-207">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-207">No</span></span> | <span data-ttu-id="42d81-208">Titel der Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="42d81-208">Title of the Meeting Request</span></span>  |
| <span data-ttu-id="42d81-209">startingTime</span><span class="sxs-lookup"><span data-stu-id="42d81-209">startingTime</span></span> | <span data-ttu-id="42d81-210">DateTime</span><span class="sxs-lookup"><span data-stu-id="42d81-210">DateTime</span></span> | <span data-ttu-id="42d81-211">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-211">No</span></span> | <span data-ttu-id="42d81-212">Die Startzeit für die Besprechung</span><span class="sxs-lookup"><span data-stu-id="42d81-212">Starting time for the meeting</span></span> |
| <span data-ttu-id="42d81-213">DurationInMins</span><span class="sxs-lookup"><span data-stu-id="42d81-213">DurationInMins</span></span> | <span data-ttu-id="42d81-214">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="42d81-214">Integer</span></span> | <span data-ttu-id="42d81-215">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-215">No</span></span> | <span data-ttu-id="42d81-216">Standard: 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="42d81-216">Default: 30 mins.</span></span> <span data-ttu-id="42d81-217">Anzahl der Minuten für die eine Besprechung durchgeführt werden würde</span><span class="sxs-lookup"><span data-stu-id="42d81-217">Number of minutes for which a meeting would be conducted</span></span> |
| <span data-ttu-id="42d81-218">Platzieren</span><span class="sxs-lookup"><span data-stu-id="42d81-218">place</span></span> | <span data-ttu-id="42d81-219">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="42d81-219">JSON object</span></span> | <span data-ttu-id="42d81-220">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-220">Yes</span></span> | <span data-ttu-id="42d81-221">Speicherort der Besprechung.</span><span class="sxs-lookup"><span data-stu-id="42d81-221">Meeting Location.</span></span> <span data-ttu-id="42d81-222">3-Komponenten enthält: Breitengrad, Längengrad, Name</span><span class="sxs-lookup"><span data-stu-id="42d81-222">Contains 3 components: latitude, longitude, name</span></span>  |
| <span data-ttu-id="42d81-223">Tagesordnung</span><span class="sxs-lookup"><span data-stu-id="42d81-223">agenda</span></span> | <span data-ttu-id="42d81-224">String</span><span class="sxs-lookup"><span data-stu-id="42d81-224">String</span></span> | <span data-ttu-id="42d81-225">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-225">Yes</span></span> | <span data-ttu-id="42d81-226">Tagesordnung für die Besprechung / Beschreibung für die Besprechung</span><span class="sxs-lookup"><span data-stu-id="42d81-226">Agenda for the Meeting / Description for the meeting</span></span> |
| <span data-ttu-id="42d81-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="42d81-227">isSenderOnly</span></span> | <span data-ttu-id="42d81-228">Bool</span><span class="sxs-lookup"><span data-stu-id="42d81-228">Bool</span></span> | <span data-ttu-id="42d81-229">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-229">Yes</span></span> | <span data-ttu-id="42d81-230">Für das Zulassen nur Absender treffen wir uns Zusammenfassung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="42d81-230">For allowing only sender to view Let's Meet summary.</span></span> <span data-ttu-id="42d81-231">Standard: false</span><span class="sxs-lookup"><span data-stu-id="42d81-231">Default: false</span></span> |

###### <a name="sample-json-request-for-a-lets-meet-action"></a><span data-ttu-id="42d81-232">Beispiel von JSON-Anforderung für eine treffen wir uns Aktion</span><span class="sxs-lookup"><span data-stu-id="42d81-232">Sample JSON Request for a Let's Meet Action</span></span>

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

###### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="42d81-233">ActionBody für eine Umfrage oder-Aktion Paket instance(id):</span><span class="sxs-lookup"><span data-stu-id="42d81-233">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="42d81-234">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-234">Parameter</span></span> | <span data-ttu-id="42d81-235">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-235">Type</span></span> | <span data-ttu-id="42d81-236">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-236">Optional?</span></span> | <span data-ttu-id="42d81-237">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-237">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-238">title</span><span class="sxs-lookup"><span data-stu-id="42d81-238">title</span></span> | <span data-ttu-id="42d81-239">String</span><span class="sxs-lookup"><span data-stu-id="42d81-239">String</span></span> | <span data-ttu-id="42d81-240">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-240">No</span></span> | <span data-ttu-id="42d81-241">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="42d81-241">Title of the Job</span></span> |
| <span data-ttu-id="42d81-242">dueDate</span><span class="sxs-lookup"><span data-stu-id="42d81-242">dueDate</span></span> | <span data-ttu-id="42d81-243">long</span><span class="sxs-lookup"><span data-stu-id="42d81-243">long</span></span> | <span data-ttu-id="42d81-244">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-244">Yes</span></span> | <span data-ttu-id="42d81-245">Standard: 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="42d81-245">Default: 24hrs.</span></span> <span data-ttu-id="42d81-246">Anzahl der Stunden, die vor denen Auftrag ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="42d81-246">Number of hours before which job should be completed</span></span> |
| <span data-ttu-id="42d81-247">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="42d81-247">isAnonymous</span></span> | <span data-ttu-id="42d81-248">Bool</span><span class="sxs-lookup"><span data-stu-id="42d81-248">Bool</span></span> | <span data-ttu-id="42d81-249">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-249">Yes</span></span> | <span data-ttu-id="42d81-250">Für anonyme Umfrageantworten zulassen.</span><span class="sxs-lookup"><span data-stu-id="42d81-250">For allowing anonymous survey responses.</span></span> <span data-ttu-id="42d81-251">Standard: false</span><span class="sxs-lookup"><span data-stu-id="42d81-251">Default: false</span></span> |
| <span data-ttu-id="42d81-252">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="42d81-252">isSenderOnly</span></span> | <span data-ttu-id="42d81-253">Bool</span><span class="sxs-lookup"><span data-stu-id="42d81-253">Bool</span></span> | <span data-ttu-id="42d81-254">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-254">Yes</span></span> | <span data-ttu-id="42d81-255">Für das Zulassen nur Absender Umfrage Zusammenfassung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="42d81-255">For allowing only sender to view survey summary.</span></span> <span data-ttu-id="42d81-256">Standard: false</span><span class="sxs-lookup"><span data-stu-id="42d81-256">Default: false</span></span> |
| <span data-ttu-id="42d81-257">acceptMultipleResponses</span><span class="sxs-lookup"><span data-stu-id="42d81-257">acceptMultipleResponses</span></span> | <span data-ttu-id="42d81-258">Bool</span><span class="sxs-lookup"><span data-stu-id="42d81-258">Bool</span></span> | <span data-ttu-id="42d81-259">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-259">Yes</span></span> | <span data-ttu-id="42d81-260">Mehrere Antworten von den gleichen Responder zulässt.</span><span class="sxs-lookup"><span data-stu-id="42d81-260">For allowing multiple responses from same responder.</span></span> <span data-ttu-id="42d81-261">Standard: false</span><span class="sxs-lookup"><span data-stu-id="42d81-261">Default: false</span></span> |
| <span data-ttu-id="42d81-262">Fragen</span><span class="sxs-lookup"><span data-stu-id="42d81-262">questions</span></span> | <span data-ttu-id="42d81-263">object[]</span><span class="sxs-lookup"><span data-stu-id="42d81-263">object[]</span></span> | <span data-ttu-id="42d81-264">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-264">No</span></span> | <span data-ttu-id="42d81-265">Jedes Element des Object [] wird als Objekt "Question" unten erläutert.</span><span class="sxs-lookup"><span data-stu-id="42d81-265">Each element of object[] is described below as Question object</span></span> |
| <span data-ttu-id="42d81-266">properties</span><span class="sxs-lookup"><span data-stu-id="42d81-266">properties</span></span> | <span data-ttu-id="42d81-267">object[]</span><span class="sxs-lookup"><span data-stu-id="42d81-267">object[]</span></span> | <span data-ttu-id="42d81-268">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-268">No</span></span> | <span data-ttu-id="42d81-269">Jedes Element des Object [] wird als Property-Objekt unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="42d81-269">Each element of object[] is described below as Property Object.</span></span> <span data-ttu-id="42d81-270">Nur gültig für das Paket Aktionsinstanz erstellen</span><span class="sxs-lookup"><span data-stu-id="42d81-270">Only valid for creating Action Package Instance</span></span> |

###### <a name="structure-for-question-object"></a><span data-ttu-id="42d81-271">Struktur für Objekt "Question"</span><span class="sxs-lookup"><span data-stu-id="42d81-271">Structure for Question object</span></span>

| <span data-ttu-id="42d81-272">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-272">Parameter</span></span> | <span data-ttu-id="42d81-273">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-273">Type</span></span> | <span data-ttu-id="42d81-274">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-274">Optional?</span></span> | <span data-ttu-id="42d81-275">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-276">title</span><span class="sxs-lookup"><span data-stu-id="42d81-276">title</span></span> | <span data-ttu-id="42d81-277">String</span><span class="sxs-lookup"><span data-stu-id="42d81-277">String</span></span> | <span data-ttu-id="42d81-278">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-278">No</span></span> | <span data-ttu-id="42d81-279">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="42d81-279">Title of the question</span></span> |
| <span data-ttu-id="42d81-280">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-280">type</span></span> | <span data-ttu-id="42d81-281">String</span><span class="sxs-lookup"><span data-stu-id="42d81-281">String</span></span> | <span data-ttu-id="42d81-282">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-282">No</span></span> | <span data-ttu-id="42d81-283">Typ der Frage.</span><span class="sxs-lookup"><span data-stu-id="42d81-283">Type of the question.</span></span> <span data-ttu-id="42d81-284">Enum: SingleOption/MultiOption/Text/Image/numerischen/Datum/Speicherort/AttachmentList</span><span class="sxs-lookup"><span data-stu-id="42d81-284">Enum: SingleOption/MultiOption/Text/Image/Numeric/Date/Location/AttachmentList</span></span> |
| <span data-ttu-id="42d81-285">isInvisible</span><span class="sxs-lookup"><span data-stu-id="42d81-285">isInvisible</span></span> | <span data-ttu-id="42d81-286">Bool</span><span class="sxs-lookup"><span data-stu-id="42d81-286">Bool</span></span> | <span data-ttu-id="42d81-287">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-287">Yes</span></span> | <span data-ttu-id="42d81-288">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="42d81-288">Default: false.</span></span> <span data-ttu-id="42d81-289">Um die Sichtbarkeit der Frage steuern</span><span class="sxs-lookup"><span data-stu-id="42d81-289">To control the visibility of the question</span></span> |
| <span data-ttu-id="42d81-290">options</span><span class="sxs-lookup"><span data-stu-id="42d81-290">options</span></span> | <span data-ttu-id="42d81-291">object[]</span><span class="sxs-lookup"><span data-stu-id="42d81-291">object[]</span></span> | <span data-ttu-id="42d81-292">Ja</span><span class="sxs-lookup"><span data-stu-id="42d81-292">Yes</span></span> | <span data-ttu-id="42d81-293">Obligatorisch für SingleOption und MultiOption Frage.</span><span class="sxs-lookup"><span data-stu-id="42d81-293">Mandatory for SingleOption and MultiOption question type.</span></span> <span data-ttu-id="42d81-294">jedes Element des Object [] wird als Optionsobjekt unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="42d81-294">each element of object[] is described below as Option object</span></span> |

###### <a name="structure-for-option-object"></a><span data-ttu-id="42d81-295">Struktur für Option-Objekt</span><span class="sxs-lookup"><span data-stu-id="42d81-295">Structure for Option object</span></span>

| <span data-ttu-id="42d81-296">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-296">Parameter</span></span> | <span data-ttu-id="42d81-297">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-297">Type</span></span> | <span data-ttu-id="42d81-298">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-298">Optional?</span></span> | <span data-ttu-id="42d81-299">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-299">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-300">title</span><span class="sxs-lookup"><span data-stu-id="42d81-300">title</span></span> | <span data-ttu-id="42d81-301">String</span><span class="sxs-lookup"><span data-stu-id="42d81-301">String</span></span> | <span data-ttu-id="42d81-302">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-302">No</span></span> | <span data-ttu-id="42d81-303">Titel der Option</span><span class="sxs-lookup"><span data-stu-id="42d81-303">Title of the Option</span></span> |

###### <a name="structure-for-property-object"></a><span data-ttu-id="42d81-304">Struktur für Property-Objekt</span><span class="sxs-lookup"><span data-stu-id="42d81-304">Structure for Property object</span></span>

| <span data-ttu-id="42d81-305">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-305">Parameter</span></span> | <span data-ttu-id="42d81-306">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-306">Type</span></span> | <span data-ttu-id="42d81-307">Optional?</span><span class="sxs-lookup"><span data-stu-id="42d81-307">Optional?</span></span> | <span data-ttu-id="42d81-308">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-308">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="42d81-309">name</span><span class="sxs-lookup"><span data-stu-id="42d81-309">name</span></span> | <span data-ttu-id="42d81-310">String</span><span class="sxs-lookup"><span data-stu-id="42d81-310">String</span></span> | <span data-ttu-id="42d81-311">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-311">No</span></span> | <span data-ttu-id="42d81-312">Name der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="42d81-312">Name of the property</span></span> |
| <span data-ttu-id="42d81-313">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-313">type</span></span> | <span data-ttu-id="42d81-314">String</span><span class="sxs-lookup"><span data-stu-id="42d81-314">String</span></span> | <span data-ttu-id="42d81-315">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-315">No</span></span> | <span data-ttu-id="42d81-316">Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="42d81-316">Type of the property.</span></span> <span data-ttu-id="42d81-317">Enum: Text, Numeric, Position, DateTime, StringList, Attachment, StringSet, AttachmentList</span><span class="sxs-lookup"><span data-stu-id="42d81-317">Enum: Text, Numeric, Location, DateTime, StringList, Attachment, StringSet, AttachmentList</span></span> |
| <span data-ttu-id="42d81-318">Wert</span><span class="sxs-lookup"><span data-stu-id="42d81-318">value</span></span> | <span data-ttu-id="42d81-319">String</span><span class="sxs-lookup"><span data-stu-id="42d81-319">String</span></span> | <span data-ttu-id="42d81-320">Nein</span><span class="sxs-lookup"><span data-stu-id="42d81-320">No</span></span> | <span data-ttu-id="42d81-321">Wert der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="42d81-321">Value of the property</span></span> |

###### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="42d81-322">Beispiel für eine Anforderung für eine Aktion Umfrage JSON</span><span class="sxs-lookup"><span data-stu-id="42d81-322">Sample JSON Request for a Survey Action</span></span>

```javascript
{
  actionType: "Survey",
  actionBody: {
    isAnonymous:false,
    isSenderOnly:false,
    acceptMultipleResponses:true,
    dueDate:10,
    title: "A test survey!!",
    questions: [
        {
            title: "a test question written here",
            type: "Text"
        },
        {
            title: "Single select question",
            type: "SingleOption",
            options: [{title:"Opt1"},{title:"Opt2"}]
        },
        {
            title: "Multi select question",
            type: "MultiOption",
            options: [{title:"MOpt1"},{title:"MOpt2"},{title:"MOpt3"}]
        },
        {
            title: "Numeric question",
            type: "Numeric"
        },
        {
            title: "Location question",
            type: "Location"
        },
        {
            title: "DateTime question",
            type: "DateTime"
        },
        {
            title: "Image question",
            type: "Image"
        }
        ]
  }
}
```

###### <a name="response-body"></a><span data-ttu-id="42d81-323">Antworttext</span><span class="sxs-lookup"><span data-stu-id="42d81-323">Response body</span></span>

| <span data-ttu-id="42d81-324">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d81-324">Parameter</span></span> | <span data-ttu-id="42d81-325">Typ</span><span class="sxs-lookup"><span data-stu-id="42d81-325">Type</span></span> | <span data-ttu-id="42d81-326">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d81-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="42d81-327">referenceId</span><span class="sxs-lookup"><span data-stu-id="42d81-327">referenceId</span></span> | <span data-ttu-id="42d81-328">String</span><span class="sxs-lookup"><span data-stu-id="42d81-328">String</span></span> | <span data-ttu-id="42d81-329">Anforderungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="42d81-329">Request identifier</span></span> |
| <span data-ttu-id="42d81-330">actionId</span><span class="sxs-lookup"><span data-stu-id="42d81-330">actionId</span></span> | <span data-ttu-id="42d81-331">String</span><span class="sxs-lookup"><span data-stu-id="42d81-331">String</span></span> | <span data-ttu-id="42d81-332">Aktionsbezeichner</span><span class="sxs-lookup"><span data-stu-id="42d81-332">Action identifier</span></span> |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
