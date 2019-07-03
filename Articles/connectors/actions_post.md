---
title: /Actions_post
description: Referenzartikel zur API zur Post-Aktion in einer Kaizala-Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 8a5e6e3c4d2f294e7c507e661ec8e5df7c717ec6
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535776"
---
# <a name="post-a-action-in-a-group"></a><span data-ttu-id="8d877-103">Posten einer Aktion in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="8d877-103">Post a Action in a group</span></span>
## <a name="post-actions"></a><span data-ttu-id="8d877-104">Post/Actions</span><span class="sxs-lookup"><span data-stu-id="8d877-104">POST /actions</span></span>

    POST {endpoint-url}/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="8d877-105">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="8d877-105">Request Parameters</span></span>

|  | <span data-ttu-id="8d877-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-106">Parameter</span></span> | <span data-ttu-id="8d877-107">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-107">Type</span></span> | <span data-ttu-id="8d877-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-108">Optional?</span></span> | <span data-ttu-id="8d877-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-110">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-110">URL Path Parameter</span></span> | <span data-ttu-id="8d877-111">groupId</span><span class="sxs-lookup"><span data-stu-id="8d877-111">groupId</span></span> | <span data-ttu-id="8d877-112">String</span><span class="sxs-lookup"><span data-stu-id="8d877-112">String</span></span> | <span data-ttu-id="8d877-113">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-113">No</span></span> | <span data-ttu-id="8d877-114">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="8d877-114">Group Identifier</span></span> |
| <span data-ttu-id="8d877-115">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="8d877-115">HTTP Header</span></span> | <span data-ttu-id="8d877-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="8d877-116">accessToken</span></span> | <span data-ttu-id="8d877-117">String</span><span class="sxs-lookup"><span data-stu-id="8d877-117">String</span></span> | <span data-ttu-id="8d877-118">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-118">No</span></span> | <span data-ttu-id="8d877-119">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="8d877-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="8d877-120">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="8d877-120">HTTP Header</span></span> | <span data-ttu-id="8d877-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8d877-121">Content-Type</span></span> | <span data-ttu-id="8d877-122">String</span><span class="sxs-lookup"><span data-stu-id="8d877-122">String</span></span> | <span data-ttu-id="8d877-123">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-123">No</span></span> | <span data-ttu-id="8d877-124">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="8d877-124">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="8d877-125">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="8d877-125">Request body</span></span>

| <span data-ttu-id="8d877-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-126">Parameter</span></span> | <span data-ttu-id="8d877-127">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-127">Type</span></span> | <span data-ttu-id="8d877-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-128">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8d877-129">id</span><span class="sxs-lookup"><span data-stu-id="8d877-129">id</span></span> | <span data-ttu-id="8d877-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d877-130">String</span></span> | <span data-ttu-id="8d877-131">ID des Kaizala-Aktionspakets.</span><span class="sxs-lookup"><span data-stu-id="8d877-131">Id of the Kaizala Action package.</span></span> <span data-ttu-id="8d877-132">Entweder von Action Type oder ID sollte angegeben werden</span><span class="sxs-lookup"><span data-stu-id="8d877-132">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="8d877-133">actionType</span><span class="sxs-lookup"><span data-stu-id="8d877-133">actionType</span></span> | <span data-ttu-id="8d877-134">String</span><span class="sxs-lookup"><span data-stu-id="8d877-134">String</span></span> | <span data-ttu-id="8d877-135">Enum "Survey"/"Job".</span><span class="sxs-lookup"><span data-stu-id="8d877-135">Enum "Survey"/"Job".</span></span> <span data-ttu-id="8d877-136">Entweder von Action Type oder ID sollte angegeben werden</span><span class="sxs-lookup"><span data-stu-id="8d877-136">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="8d877-137">actionBody</span><span class="sxs-lookup"><span data-stu-id="8d877-137">actionBody</span></span> | <span data-ttu-id="8d877-138">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d877-138">JSON Object</span></span> | <span data-ttu-id="8d877-139">Objekt, das für die jeweilige Aktion erforderliche Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d877-139">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="8d877-140">Für jede der unterstützten Aktionen definierte Parameter.</span><span class="sxs-lookup"><span data-stu-id="8d877-140">Parameters defined below for each of the supported Actions.</span></span> |


#### <a name="actionbody-for-an-announcement-action"></a><span data-ttu-id="8d877-141">actionBody für eine Ankündigungs Aktion</span><span class="sxs-lookup"><span data-stu-id="8d877-141">actionBody for an Announcement Action</span></span>

| <span data-ttu-id="8d877-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-142">Parameter</span></span> | <span data-ttu-id="8d877-143">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-143">Type</span></span> | <span data-ttu-id="8d877-144">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-144">Optional?</span></span> | <span data-ttu-id="8d877-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-145">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-146">title</span><span class="sxs-lookup"><span data-stu-id="8d877-146">title</span></span> | <span data-ttu-id="8d877-147">String</span><span class="sxs-lookup"><span data-stu-id="8d877-147">String</span></span> | <span data-ttu-id="8d877-148">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-148">No</span></span> | <span data-ttu-id="8d877-149">Titel der Ansage</span><span class="sxs-lookup"><span data-stu-id="8d877-149">Title of the Announcement</span></span> |
| <span data-ttu-id="8d877-150">MediaResources</span><span class="sxs-lookup"><span data-stu-id="8d877-150">MediaResources</span></span> | <span data-ttu-id="8d877-151">String []</span><span class="sxs-lookup"><span data-stu-id="8d877-151">String[]</span></span> | <span data-ttu-id="8d877-152">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-152">Yes</span></span> | <span data-ttu-id="8d877-153">Array von Medienressourcen</span><span class="sxs-lookup"><span data-stu-id="8d877-153">Array of media resources</span></span> |
| <span data-ttu-id="8d877-154">Nachricht</span><span class="sxs-lookup"><span data-stu-id="8d877-154">Message</span></span> | <span data-ttu-id="8d877-155">String</span><span class="sxs-lookup"><span data-stu-id="8d877-155">String</span></span> | <span data-ttu-id="8d877-156">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-156">No</span></span> | <span data-ttu-id="8d877-157">Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="8d877-157">Message Body</span></span> |

#### <a name="sample-json-request-for-an-announcement-action"></a><span data-ttu-id="8d877-158">JSON-Beispielanforderung für eine Ankündigungs Aktion</span><span class="sxs-lookup"><span data-stu-id="8d877-158">Sample JSON Request for an Announcement Action</span></span>

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

#### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="8d877-159">actionBody für eine Auftragsaktion</span><span class="sxs-lookup"><span data-stu-id="8d877-159">actionBody for a Job Action</span></span>

| <span data-ttu-id="8d877-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-160">Parameter</span></span> | <span data-ttu-id="8d877-161">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-161">Type</span></span> | <span data-ttu-id="8d877-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-162">Optional?</span></span> | <span data-ttu-id="8d877-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-164">title</span><span class="sxs-lookup"><span data-stu-id="8d877-164">title</span></span> | <span data-ttu-id="8d877-165">String</span><span class="sxs-lookup"><span data-stu-id="8d877-165">String</span></span> | <span data-ttu-id="8d877-166">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-166">No</span></span> | <span data-ttu-id="8d877-167">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="8d877-167">Title of the Job</span></span> |
| <span data-ttu-id="8d877-168">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8d877-168">assignedTo</span></span> | <span data-ttu-id="8d877-169">String []</span><span class="sxs-lookup"><span data-stu-id="8d877-169">String[]</span></span> | <span data-ttu-id="8d877-170">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-170">No</span></span> | <span data-ttu-id="8d877-171">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="8d877-171">Title of the Job</span></span> |
| <span data-ttu-id="8d877-172">DueDate</span><span class="sxs-lookup"><span data-stu-id="8d877-172">dueDate</span></span> | <span data-ttu-id="8d877-173">long</span><span class="sxs-lookup"><span data-stu-id="8d877-173">long</span></span> | <span data-ttu-id="8d877-174">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-174">Yes</span></span> | <span data-ttu-id="8d877-175">Standard: 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="8d877-175">Default: 24hrs.</span></span> <span data-ttu-id="8d877-176">Anzahl der Stunden vor dem Abschluss des Auftrags</span><span class="sxs-lookup"><span data-stu-id="8d877-176">Number of hours before which job should be completed</span></span> |

##### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="8d877-177">JSON-Beispielanforderung für eine Auftragsaktion</span><span class="sxs-lookup"><span data-stu-id="8d877-177">Sample JSON Request for a Job Action</span></span>

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

#### <a name="actionbody-for-a-poll-action"></a><span data-ttu-id="8d877-178">actionBody für eine Abfrage Aktion</span><span class="sxs-lookup"><span data-stu-id="8d877-178">actionBody for a Poll Action</span></span>

| <span data-ttu-id="8d877-179">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-179">Parameter</span></span> | <span data-ttu-id="8d877-180">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-180">Type</span></span> | <span data-ttu-id="8d877-181">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-181">Optional?</span></span> | <span data-ttu-id="8d877-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-182">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-183">Frage</span><span class="sxs-lookup"><span data-stu-id="8d877-183">question</span></span> | <span data-ttu-id="8d877-184">String</span><span class="sxs-lookup"><span data-stu-id="8d877-184">String</span></span> | <span data-ttu-id="8d877-185">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-185">No</span></span> | <span data-ttu-id="8d877-186">Umfrage Frage</span><span class="sxs-lookup"><span data-stu-id="8d877-186">Poll Question</span></span> |
| <span data-ttu-id="8d877-187">Auswahlmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="8d877-187">Choices</span></span> | <span data-ttu-id="8d877-188">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="8d877-188">Json Array</span></span> | <span data-ttu-id="8d877-189">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-189">No</span></span> | <span data-ttu-id="8d877-190">Verfügbare Auswahlmöglichkeiten für die Umfrage.</span><span class="sxs-lookup"><span data-stu-id="8d877-190">Choices available for the poll.</span></span> <span data-ttu-id="8d877-191">Jede Auswahl ist Unterkomponente:</span><span class="sxs-lookup"><span data-stu-id="8d877-191">Each Choice have below component:</span></span> <ol><li><span data-ttu-id="8d877-192">Title (obligatorisch #a0 im Zeichenfolgenformat)</span><span class="sxs-lookup"><span data-stu-id="8d877-192">title (Mandatory & in String format)</span></span> </li><li><span data-ttu-id="8d877-193">Image (optional)</span><span class="sxs-lookup"><span data-stu-id="8d877-193">image (optional)</span></span></li></ol> |
| <span data-ttu-id="8d877-194">expiryInHours</span><span class="sxs-lookup"><span data-stu-id="8d877-194">expiryInHours</span></span> | <span data-ttu-id="8d877-195">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="8d877-195">Integer</span></span> | <span data-ttu-id="8d877-196">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-196">Yes</span></span> | <span data-ttu-id="8d877-197">Standard: 720.</span><span class="sxs-lookup"><span data-stu-id="8d877-197">Default:720.</span></span> <span data-ttu-id="8d877-198">Anzahl der Stunden, in denen eine bestimmte Umfrage ablaufen würde</span><span class="sxs-lookup"><span data-stu-id="8d877-198">Number of hours in which a given poll would expire</span></span> |

##### <a name="sample-json-request-for-a-poll-action"></a><span data-ttu-id="8d877-199">JSON-Beispielanforderung für eine Abfrage Aktion</span><span class="sxs-lookup"><span data-stu-id="8d877-199">Sample JSON Request for a Poll Action</span></span>

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
#### <a name="actionbody-for-a-lets-meet-action"></a><span data-ttu-id="8d877-200">actionBody für eine Let es Meet-Aktion</span><span class="sxs-lookup"><span data-stu-id="8d877-200">actionBody for a Let's Meet Action</span></span>

| <span data-ttu-id="8d877-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-201">Parameter</span></span> | <span data-ttu-id="8d877-202">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-202">Type</span></span> | <span data-ttu-id="8d877-203">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-203">Optional?</span></span> | <span data-ttu-id="8d877-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-204">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-205">title</span><span class="sxs-lookup"><span data-stu-id="8d877-205">title</span></span> | <span data-ttu-id="8d877-206">String</span><span class="sxs-lookup"><span data-stu-id="8d877-206">String</span></span> | <span data-ttu-id="8d877-207">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-207">No</span></span> | <span data-ttu-id="8d877-208">Titel der Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="8d877-208">Title of the Meeting Request</span></span>  |
| <span data-ttu-id="8d877-209">Startzeit</span><span class="sxs-lookup"><span data-stu-id="8d877-209">startingTime</span></span> | <span data-ttu-id="8d877-210">DateTime</span><span class="sxs-lookup"><span data-stu-id="8d877-210">DateTime</span></span> | <span data-ttu-id="8d877-211">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-211">No</span></span> | <span data-ttu-id="8d877-212">Startzeit für die Besprechung</span><span class="sxs-lookup"><span data-stu-id="8d877-212">Starting time for the meeting</span></span> |
| <span data-ttu-id="8d877-213">DurationInMins</span><span class="sxs-lookup"><span data-stu-id="8d877-213">DurationInMins</span></span> | <span data-ttu-id="8d877-214">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="8d877-214">Integer</span></span> | <span data-ttu-id="8d877-215">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-215">No</span></span> | <span data-ttu-id="8d877-216">Standard: 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8d877-216">Default: 30 mins.</span></span> <span data-ttu-id="8d877-217">Anzahl der Minuten, für die eine Besprechung durchgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="8d877-217">Number of minutes for which a meeting would be conducted</span></span> |
| <span data-ttu-id="8d877-218">Ort</span><span class="sxs-lookup"><span data-stu-id="8d877-218">place</span></span> | <span data-ttu-id="8d877-219">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d877-219">JSON object</span></span> | <span data-ttu-id="8d877-220">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-220">Yes</span></span> | <span data-ttu-id="8d877-221">Besprechungs Standort.</span><span class="sxs-lookup"><span data-stu-id="8d877-221">Meeting Location.</span></span> <span data-ttu-id="8d877-222">Enthält 3 Komponenten: Latitude, Längengrad, Name</span><span class="sxs-lookup"><span data-stu-id="8d877-222">Contains 3 components: latitude, longitude, name</span></span>  |
| <span data-ttu-id="8d877-223">Agendas</span><span class="sxs-lookup"><span data-stu-id="8d877-223">agenda</span></span> | <span data-ttu-id="8d877-224">String</span><span class="sxs-lookup"><span data-stu-id="8d877-224">String</span></span> | <span data-ttu-id="8d877-225">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-225">Yes</span></span> | <span data-ttu-id="8d877-226">Agenda für die Besprechung/Beschreibung für die Besprechung</span><span class="sxs-lookup"><span data-stu-id="8d877-226">Agenda for the Meeting / Description for the meeting</span></span> |
| <span data-ttu-id="8d877-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="8d877-227">isSenderOnly</span></span> | <span data-ttu-id="8d877-228">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="8d877-228">Bool</span></span> | <span data-ttu-id="8d877-229">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-229">Yes</span></span> | <span data-ttu-id="8d877-230">Damit nur Absender die Zusammenfassung von Let es Meet anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="8d877-230">For allowing only sender to view Let's Meet summary.</span></span> <span data-ttu-id="8d877-231">Standard: false</span><span class="sxs-lookup"><span data-stu-id="8d877-231">Default: false</span></span> |

##### <a name="sample-json-request-for-a-lets-meet-action"></a><span data-ttu-id="8d877-232">JSON-Beispielanforderung für eine Let es Meet-Aktion</span><span class="sxs-lookup"><span data-stu-id="8d877-232">Sample JSON Request for a Let's Meet Action</span></span>

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="8d877-233">actionBody für eine Umfrageaktion oder eine Aktionspaket Instanz (ID):</span><span class="sxs-lookup"><span data-stu-id="8d877-233">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="8d877-234">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-234">Parameter</span></span> | <span data-ttu-id="8d877-235">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-235">Type</span></span> | <span data-ttu-id="8d877-236">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-236">Optional?</span></span> | <span data-ttu-id="8d877-237">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-237">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-238">title</span><span class="sxs-lookup"><span data-stu-id="8d877-238">title</span></span> | <span data-ttu-id="8d877-239">String</span><span class="sxs-lookup"><span data-stu-id="8d877-239">String</span></span> | <span data-ttu-id="8d877-240">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-240">No</span></span> | <span data-ttu-id="8d877-241">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="8d877-241">Title of the Job</span></span> |
| <span data-ttu-id="8d877-242">DueDate</span><span class="sxs-lookup"><span data-stu-id="8d877-242">dueDate</span></span> | <span data-ttu-id="8d877-243">long</span><span class="sxs-lookup"><span data-stu-id="8d877-243">long</span></span> | <span data-ttu-id="8d877-244">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-244">Yes</span></span> | <span data-ttu-id="8d877-245">Standard: 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="8d877-245">Default: 24hrs.</span></span> <span data-ttu-id="8d877-246">Anzahl der Stunden vor dem Abschluss des Auftrags</span><span class="sxs-lookup"><span data-stu-id="8d877-246">Number of hours before which job should be completed</span></span> |
| <span data-ttu-id="8d877-247">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="8d877-247">isAnonymous</span></span> | <span data-ttu-id="8d877-248">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="8d877-248">Bool</span></span> | <span data-ttu-id="8d877-249">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-249">Yes</span></span> | <span data-ttu-id="8d877-250">Für das zulassen anonymer Umfrage Antworten.</span><span class="sxs-lookup"><span data-stu-id="8d877-250">For allowing anonymous survey responses.</span></span> <span data-ttu-id="8d877-251">Standard: false</span><span class="sxs-lookup"><span data-stu-id="8d877-251">Default: false</span></span> |
| <span data-ttu-id="8d877-252">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="8d877-252">isSenderOnly</span></span> | <span data-ttu-id="8d877-253">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="8d877-253">Bool</span></span> | <span data-ttu-id="8d877-254">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-254">Yes</span></span> | <span data-ttu-id="8d877-255">Für die Möglichkeit, dass nur Absender die Umfragezusammenfassung anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="8d877-255">For allowing only sender to view survey summary.</span></span> <span data-ttu-id="8d877-256">Standard: false</span><span class="sxs-lookup"><span data-stu-id="8d877-256">Default: false</span></span> |
| <span data-ttu-id="8d877-257">acceptMultipleResponses</span><span class="sxs-lookup"><span data-stu-id="8d877-257">acceptMultipleResponses</span></span> | <span data-ttu-id="8d877-258">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="8d877-258">Bool</span></span> | <span data-ttu-id="8d877-259">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-259">Yes</span></span> | <span data-ttu-id="8d877-260">Für das Zulassen mehrerer Antworten von demselben Responder.</span><span class="sxs-lookup"><span data-stu-id="8d877-260">For allowing multiple responses from same responder.</span></span> <span data-ttu-id="8d877-261">Standard: false</span><span class="sxs-lookup"><span data-stu-id="8d877-261">Default: false</span></span> |
| <span data-ttu-id="8d877-262">Fragen</span><span class="sxs-lookup"><span data-stu-id="8d877-262">questions</span></span> | <span data-ttu-id="8d877-263">object[]</span><span class="sxs-lookup"><span data-stu-id="8d877-263">object[]</span></span> | <span data-ttu-id="8d877-264">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-264">No</span></span> | <span data-ttu-id="8d877-265">Jedes Element von Object [] wird im folgenden als Question-Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d877-265">Each element of object[] is described below as Question object</span></span> |
| <span data-ttu-id="8d877-266">properties</span><span class="sxs-lookup"><span data-stu-id="8d877-266">properties</span></span> | <span data-ttu-id="8d877-267">object[]</span><span class="sxs-lookup"><span data-stu-id="8d877-267">object[]</span></span> | <span data-ttu-id="8d877-268">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-268">No</span></span> | <span data-ttu-id="8d877-269">Jedes Element von Object [] wird im folgenden als Property-Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d877-269">Each element of object[] is described below as Property Object.</span></span> <span data-ttu-id="8d877-270">Nur gültig zum Erstellen einer Aktionspaket Instanz</span><span class="sxs-lookup"><span data-stu-id="8d877-270">Only valid for creating Action Package Instance</span></span> |

##### <a name="structure-for-question-object"></a><span data-ttu-id="8d877-271">Struktur für Question-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d877-271">Structure for Question object</span></span>

| <span data-ttu-id="8d877-272">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-272">Parameter</span></span> | <span data-ttu-id="8d877-273">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-273">Type</span></span> | <span data-ttu-id="8d877-274">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-274">Optional?</span></span> | <span data-ttu-id="8d877-275">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-276">title</span><span class="sxs-lookup"><span data-stu-id="8d877-276">title</span></span> | <span data-ttu-id="8d877-277">String</span><span class="sxs-lookup"><span data-stu-id="8d877-277">String</span></span> | <span data-ttu-id="8d877-278">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-278">No</span></span> | <span data-ttu-id="8d877-279">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="8d877-279">Title of the question</span></span> |
| <span data-ttu-id="8d877-280">type</span><span class="sxs-lookup"><span data-stu-id="8d877-280">type</span></span> | <span data-ttu-id="8d877-281">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d877-281">String</span></span> | <span data-ttu-id="8d877-282">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-282">No</span></span> | <span data-ttu-id="8d877-283">Der Typ der Frage.</span><span class="sxs-lookup"><span data-stu-id="8d877-283">Type of the question.</span></span> <span data-ttu-id="8d877-284">Enumeration: SingleOption/multioption/Text/Image/numerisch/Datum/Ort/Anlage Liste</span><span class="sxs-lookup"><span data-stu-id="8d877-284">Enum: SingleOption/MultiOption/Text/Image/Numeric/Date/Location/AttachmentList</span></span> |
| <span data-ttu-id="8d877-285">isunsichtbar</span><span class="sxs-lookup"><span data-stu-id="8d877-285">isInvisible</span></span> | <span data-ttu-id="8d877-286">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="8d877-286">Bool</span></span> | <span data-ttu-id="8d877-287">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-287">Yes</span></span> | <span data-ttu-id="8d877-288">Default: false.</span><span class="sxs-lookup"><span data-stu-id="8d877-288">Default: false.</span></span> <span data-ttu-id="8d877-289">So steuern Sie die Sichtbarkeit der Frage</span><span class="sxs-lookup"><span data-stu-id="8d877-289">To control the visibility of the question</span></span> |
| <span data-ttu-id="8d877-290">options</span><span class="sxs-lookup"><span data-stu-id="8d877-290">options</span></span> | <span data-ttu-id="8d877-291">object[]</span><span class="sxs-lookup"><span data-stu-id="8d877-291">object[]</span></span> | <span data-ttu-id="8d877-292">Ja</span><span class="sxs-lookup"><span data-stu-id="8d877-292">Yes</span></span> | <span data-ttu-id="8d877-293">Obligatorisch für SingleOption und multioption-Fragentyp.</span><span class="sxs-lookup"><span data-stu-id="8d877-293">Mandatory for SingleOption and MultiOption question type.</span></span> <span data-ttu-id="8d877-294">jedes Element von Object [] wird im folgenden als Optionsobjekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d877-294">each element of object[] is described below as Option object</span></span> |

###### <a name="structure-for-option-object"></a><span data-ttu-id="8d877-295">Struktur für Optionsobjekt</span><span class="sxs-lookup"><span data-stu-id="8d877-295">Structure for Option object</span></span>

| <span data-ttu-id="8d877-296">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-296">Parameter</span></span> | <span data-ttu-id="8d877-297">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-297">Type</span></span> | <span data-ttu-id="8d877-298">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-298">Optional?</span></span> | <span data-ttu-id="8d877-299">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-299">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-300">title</span><span class="sxs-lookup"><span data-stu-id="8d877-300">title</span></span> | <span data-ttu-id="8d877-301">String</span><span class="sxs-lookup"><span data-stu-id="8d877-301">String</span></span> | <span data-ttu-id="8d877-302">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-302">No</span></span> | <span data-ttu-id="8d877-303">Titel der Option</span><span class="sxs-lookup"><span data-stu-id="8d877-303">Title of the Option</span></span> |

###### <a name="structure-for-property-object"></a><span data-ttu-id="8d877-304">Struktur für Property-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d877-304">Structure for Property object</span></span>

| <span data-ttu-id="8d877-305">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-305">Parameter</span></span> | <span data-ttu-id="8d877-306">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-306">Type</span></span> | <span data-ttu-id="8d877-307">Optional?</span><span class="sxs-lookup"><span data-stu-id="8d877-307">Optional?</span></span> | <span data-ttu-id="8d877-308">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-308">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="8d877-309">name</span><span class="sxs-lookup"><span data-stu-id="8d877-309">name</span></span> | <span data-ttu-id="8d877-310">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d877-310">String</span></span> | <span data-ttu-id="8d877-311">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-311">No</span></span> | <span data-ttu-id="8d877-312">Name der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d877-312">Name of the property</span></span> |
| <span data-ttu-id="8d877-313">type</span><span class="sxs-lookup"><span data-stu-id="8d877-313">type</span></span> | <span data-ttu-id="8d877-314">String</span><span class="sxs-lookup"><span data-stu-id="8d877-314">String</span></span> | <span data-ttu-id="8d877-315">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-315">No</span></span> | <span data-ttu-id="8d877-316">Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8d877-316">Type of the property.</span></span> <span data-ttu-id="8d877-317">Enum: Text, numeric, Location, DateTime, stringlist, Attachment, stringset, attachmentlist</span><span class="sxs-lookup"><span data-stu-id="8d877-317">Enum: Text, Numeric, Location, DateTime, StringList, Attachment, StringSet, AttachmentList</span></span> |
| <span data-ttu-id="8d877-318">value</span><span class="sxs-lookup"><span data-stu-id="8d877-318">value</span></span> | <span data-ttu-id="8d877-319">String</span><span class="sxs-lookup"><span data-stu-id="8d877-319">String</span></span> | <span data-ttu-id="8d877-320">Nein</span><span class="sxs-lookup"><span data-stu-id="8d877-320">No</span></span> | <span data-ttu-id="8d877-321">Wert der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d877-321">Value of the property</span></span> |

##### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="8d877-322">JSON-Beispielanforderung für eine Umfrageaktion</span><span class="sxs-lookup"><span data-stu-id="8d877-322">Sample JSON Request for a Survey Action</span></span>

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

##### <a name="response-body"></a><span data-ttu-id="8d877-323">Antworttext</span><span class="sxs-lookup"><span data-stu-id="8d877-323">Response body</span></span>

| <span data-ttu-id="8d877-324">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d877-324">Parameter</span></span> | <span data-ttu-id="8d877-325">Typ</span><span class="sxs-lookup"><span data-stu-id="8d877-325">Type</span></span> | <span data-ttu-id="8d877-326">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d877-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8d877-327">referenceId</span><span class="sxs-lookup"><span data-stu-id="8d877-327">referenceId</span></span> | <span data-ttu-id="8d877-328">String</span><span class="sxs-lookup"><span data-stu-id="8d877-328">String</span></span> | <span data-ttu-id="8d877-329">Anforderungs-ID</span><span class="sxs-lookup"><span data-stu-id="8d877-329">Request identifier</span></span> |
| <span data-ttu-id="8d877-330">actionId</span><span class="sxs-lookup"><span data-stu-id="8d877-330">actionId</span></span> | <span data-ttu-id="8d877-331">String</span><span class="sxs-lookup"><span data-stu-id="8d877-331">String</span></span> | <span data-ttu-id="8d877-332">Aktions-ID</span><span class="sxs-lookup"><span data-stu-id="8d877-332">Action identifier</span></span> |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
