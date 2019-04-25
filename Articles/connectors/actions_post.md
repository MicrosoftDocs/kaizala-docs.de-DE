---
title: /Actions_post
description: Referenzartikel zur API zum Nachschlagen von Aktionen in einer Kaizala-Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 5ca7c92f76a0e0e18025dda2526b53515a003e90
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190742"
---
# <a name="post-a-action-in-a-group"></a><span data-ttu-id="f4723-103">Veröffentlichen einer Aktion in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="f4723-103">Post a Action in a group</span></span>
## <a name="post-actions"></a><span data-ttu-id="f4723-104">POST/Actions</span><span class="sxs-lookup"><span data-stu-id="f4723-104">POST /actions</span></span>

    POST {endpoint-url}/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="f4723-105">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="f4723-105">Request Parameters</span></span>

|  | <span data-ttu-id="f4723-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-106">Parameter</span></span> | <span data-ttu-id="f4723-107">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-107">Type</span></span> | <span data-ttu-id="f4723-108">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-108">Optional?</span></span> | <span data-ttu-id="f4723-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-109">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-110">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-110">URL Path Parameter</span></span> | <span data-ttu-id="f4723-111">groupId</span><span class="sxs-lookup"><span data-stu-id="f4723-111">groupId</span></span> | <span data-ttu-id="f4723-112">String</span><span class="sxs-lookup"><span data-stu-id="f4723-112">String</span></span> | <span data-ttu-id="f4723-113">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-113">No</span></span> | <span data-ttu-id="f4723-114">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="f4723-114">Group Identifier</span></span> |
| <span data-ttu-id="f4723-115">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="f4723-115">HTTP Header</span></span> | <span data-ttu-id="f4723-116">accessToken</span><span class="sxs-lookup"><span data-stu-id="f4723-116">accessToken</span></span> | <span data-ttu-id="f4723-117">String</span><span class="sxs-lookup"><span data-stu-id="f4723-117">String</span></span> | <span data-ttu-id="f4723-118">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-118">No</span></span> | <span data-ttu-id="f4723-119">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="f4723-119">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="f4723-120">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="f4723-120">HTTP Header</span></span> | <span data-ttu-id="f4723-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f4723-121">Content-Type</span></span> | <span data-ttu-id="f4723-122">String</span><span class="sxs-lookup"><span data-stu-id="f4723-122">String</span></span> | <span data-ttu-id="f4723-123">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-123">No</span></span> | <span data-ttu-id="f4723-124">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="f4723-124">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="f4723-125">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="f4723-125">Request body</span></span>

| <span data-ttu-id="f4723-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-126">Parameter</span></span> | <span data-ttu-id="f4723-127">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-127">Type</span></span> | <span data-ttu-id="f4723-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-128">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f4723-129">id</span><span class="sxs-lookup"><span data-stu-id="f4723-129">id</span></span> | <span data-ttu-id="f4723-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f4723-130">String</span></span> | <span data-ttu-id="f4723-131">ID des Kaizala-Aktionspakets.</span><span class="sxs-lookup"><span data-stu-id="f4723-131">Id of the Kaizala Action package.</span></span> <span data-ttu-id="f4723-132">Entweder von ActionType oder ID sollte angegeben werden</span><span class="sxs-lookup"><span data-stu-id="f4723-132">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="f4723-133">actionType</span><span class="sxs-lookup"><span data-stu-id="f4723-133">actionType</span></span> | <span data-ttu-id="f4723-134">String</span><span class="sxs-lookup"><span data-stu-id="f4723-134">String</span></span> | <span data-ttu-id="f4723-135">Enum "Survey"/"Job".</span><span class="sxs-lookup"><span data-stu-id="f4723-135">Enum "Survey"/"Job".</span></span> <span data-ttu-id="f4723-136">Entweder von ActionType oder ID sollte angegeben werden</span><span class="sxs-lookup"><span data-stu-id="f4723-136">Either of actionType or Id should be specified</span></span> |
| <span data-ttu-id="f4723-137">actionBody</span><span class="sxs-lookup"><span data-stu-id="f4723-137">actionBody</span></span> | <span data-ttu-id="f4723-138">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="f4723-138">JSON Object</span></span> | <span data-ttu-id="f4723-139">Objekt, das die für die jeweilige Aktion erforderlichen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4723-139">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="f4723-140">Die unten definierten Parameter für jede der unterstützten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f4723-140">Parameters defined below for each of the supported Actions.</span></span> |


#### <a name="actionbody-for-an-announcement-action"></a><span data-ttu-id="f4723-141">actionBody für eine Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="f4723-141">actionBody for an Announcement Action</span></span>

| <span data-ttu-id="f4723-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-142">Parameter</span></span> | <span data-ttu-id="f4723-143">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-143">Type</span></span> | <span data-ttu-id="f4723-144">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-144">Optional?</span></span> | <span data-ttu-id="f4723-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-145">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-146">title</span><span class="sxs-lookup"><span data-stu-id="f4723-146">title</span></span> | <span data-ttu-id="f4723-147">String</span><span class="sxs-lookup"><span data-stu-id="f4723-147">String</span></span> | <span data-ttu-id="f4723-148">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-148">No</span></span> | <span data-ttu-id="f4723-149">Titel der Ansage</span><span class="sxs-lookup"><span data-stu-id="f4723-149">Title of the Announcement</span></span> |
| <span data-ttu-id="f4723-150">MediaResources</span><span class="sxs-lookup"><span data-stu-id="f4723-150">MediaResources</span></span> | <span data-ttu-id="f4723-151">String []</span><span class="sxs-lookup"><span data-stu-id="f4723-151">String[]</span></span> | <span data-ttu-id="f4723-152">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-152">Yes</span></span> | <span data-ttu-id="f4723-153">Array von Medienressourcen</span><span class="sxs-lookup"><span data-stu-id="f4723-153">Array of media resources</span></span> |
| <span data-ttu-id="f4723-154">Nachricht</span><span class="sxs-lookup"><span data-stu-id="f4723-154">Message</span></span> | <span data-ttu-id="f4723-155">String</span><span class="sxs-lookup"><span data-stu-id="f4723-155">String</span></span> | <span data-ttu-id="f4723-156">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-156">No</span></span> | <span data-ttu-id="f4723-157">Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="f4723-157">Message Body</span></span> |

#### <a name="sample-json-request-for-an-announcement-action"></a><span data-ttu-id="f4723-158">JSON-Beispielanforderung für eine Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="f4723-158">Sample JSON Request for an Announcement Action</span></span>

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

#### <a name="actionbody-for-a-job-action"></a><span data-ttu-id="f4723-159">actionBody für eine Auftragsaktion</span><span class="sxs-lookup"><span data-stu-id="f4723-159">actionBody for a Job Action</span></span>

| <span data-ttu-id="f4723-160">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-160">Parameter</span></span> | <span data-ttu-id="f4723-161">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-161">Type</span></span> | <span data-ttu-id="f4723-162">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-162">Optional?</span></span> | <span data-ttu-id="f4723-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-163">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-164">title</span><span class="sxs-lookup"><span data-stu-id="f4723-164">title</span></span> | <span data-ttu-id="f4723-165">String</span><span class="sxs-lookup"><span data-stu-id="f4723-165">String</span></span> | <span data-ttu-id="f4723-166">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-166">No</span></span> | <span data-ttu-id="f4723-167">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="f4723-167">Title of the Job</span></span> |
| <span data-ttu-id="f4723-168">assignedTo</span><span class="sxs-lookup"><span data-stu-id="f4723-168">assignedTo</span></span> | <span data-ttu-id="f4723-169">String []</span><span class="sxs-lookup"><span data-stu-id="f4723-169">String[]</span></span> | <span data-ttu-id="f4723-170">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-170">No</span></span> | <span data-ttu-id="f4723-171">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="f4723-171">Title of the Job</span></span> |
| <span data-ttu-id="f4723-172">dueDate</span><span class="sxs-lookup"><span data-stu-id="f4723-172">dueDate</span></span> | <span data-ttu-id="f4723-173">long</span><span class="sxs-lookup"><span data-stu-id="f4723-173">long</span></span> | <span data-ttu-id="f4723-174">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-174">Yes</span></span> | <span data-ttu-id="f4723-175">Standard: 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="f4723-175">Default: 24hrs.</span></span> <span data-ttu-id="f4723-176">Anzahl der Stunden, die vor der Ausführung des Auftrags ausgeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="f4723-176">Number of hours before which job should be completed</span></span> |

##### <a name="sample-json-request-for-a-job-action"></a><span data-ttu-id="f4723-177">JSON-Beispielanforderung für eine Auftragsaktion</span><span class="sxs-lookup"><span data-stu-id="f4723-177">Sample JSON Request for a Job Action</span></span>

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

#### <a name="actionbody-for-a-poll-action"></a><span data-ttu-id="f4723-178">actionBody für eine Abfrage Aktion</span><span class="sxs-lookup"><span data-stu-id="f4723-178">actionBody for a Poll Action</span></span>

| <span data-ttu-id="f4723-179">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-179">Parameter</span></span> | <span data-ttu-id="f4723-180">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-180">Type</span></span> | <span data-ttu-id="f4723-181">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-181">Optional?</span></span> | <span data-ttu-id="f4723-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-182">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-183">Frage</span><span class="sxs-lookup"><span data-stu-id="f4723-183">question</span></span> | <span data-ttu-id="f4723-184">String</span><span class="sxs-lookup"><span data-stu-id="f4723-184">String</span></span> | <span data-ttu-id="f4723-185">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-185">No</span></span> | <span data-ttu-id="f4723-186">Umfrage Frage</span><span class="sxs-lookup"><span data-stu-id="f4723-186">Poll Question</span></span> |
| <span data-ttu-id="f4723-187">Auswahlmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="f4723-187">Choices</span></span> | <span data-ttu-id="f4723-188">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="f4723-188">Json Array</span></span> | <span data-ttu-id="f4723-189">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-189">No</span></span> | <span data-ttu-id="f4723-190">Auswahlmöglichkeiten für die Umfrage.</span><span class="sxs-lookup"><span data-stu-id="f4723-190">Choices available for the poll.</span></span> <span data-ttu-id="f4723-191">Jede Auswahl hat die folgende Komponente:</span><span class="sxs-lookup"><span data-stu-id="f4723-191">Each Choice have below component:</span></span> <ol><li><span data-ttu-id="f4723-192">Title (obligatorische & im Zeichenfolgenformat)</span><span class="sxs-lookup"><span data-stu-id="f4723-192">title (Mandatory & in String format)</span></span> </li><li><span data-ttu-id="f4723-193">Bild (optional)</span><span class="sxs-lookup"><span data-stu-id="f4723-193">image (optional)</span></span></li></ol> |
| <span data-ttu-id="f4723-194">expiryInHours</span><span class="sxs-lookup"><span data-stu-id="f4723-194">expiryInHours</span></span> | <span data-ttu-id="f4723-195">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="f4723-195">Integer</span></span> | <span data-ttu-id="f4723-196">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-196">Yes</span></span> | <span data-ttu-id="f4723-197">Standard: 720.</span><span class="sxs-lookup"><span data-stu-id="f4723-197">Default:720.</span></span> <span data-ttu-id="f4723-198">Anzahl der Stunden, in denen eine Reformprogramms große-Umfrage abläuft</span><span class="sxs-lookup"><span data-stu-id="f4723-198">Number of hours in which a gven poll would expire</span></span> |

##### <a name="sample-json-request-for-a-poll-action"></a><span data-ttu-id="f4723-199">JSON-Beispielanforderung für eine Abfrage Aktion</span><span class="sxs-lookup"><span data-stu-id="f4723-199">Sample JSON Request for a Poll Action</span></span>

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
#### <a name="actionbody-for-a-lets-meet-action"></a><span data-ttu-id="f4723-200">actionBody für eine Let es Meet-Aktion</span><span class="sxs-lookup"><span data-stu-id="f4723-200">actionBody for a Let's Meet Action</span></span>

| <span data-ttu-id="f4723-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-201">Parameter</span></span> | <span data-ttu-id="f4723-202">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-202">Type</span></span> | <span data-ttu-id="f4723-203">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-203">Optional?</span></span> | <span data-ttu-id="f4723-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-204">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-205">title</span><span class="sxs-lookup"><span data-stu-id="f4723-205">title</span></span> | <span data-ttu-id="f4723-206">String</span><span class="sxs-lookup"><span data-stu-id="f4723-206">String</span></span> | <span data-ttu-id="f4723-207">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-207">No</span></span> | <span data-ttu-id="f4723-208">Titel der Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="f4723-208">Title of the Meeting Request</span></span>  |
| <span data-ttu-id="f4723-209">Startzeit</span><span class="sxs-lookup"><span data-stu-id="f4723-209">startingTime</span></span> | <span data-ttu-id="f4723-210">DateTime</span><span class="sxs-lookup"><span data-stu-id="f4723-210">DateTime</span></span> | <span data-ttu-id="f4723-211">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-211">No</span></span> | <span data-ttu-id="f4723-212">Startzeit für die Besprechung</span><span class="sxs-lookup"><span data-stu-id="f4723-212">Starting time for the meeting</span></span> |
| <span data-ttu-id="f4723-213">DurationInMins</span><span class="sxs-lookup"><span data-stu-id="f4723-213">DurationInMins</span></span> | <span data-ttu-id="f4723-214">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="f4723-214">Integer</span></span> | <span data-ttu-id="f4723-215">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-215">No</span></span> | <span data-ttu-id="f4723-216">Standard: 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="f4723-216">Default: 30 mins.</span></span> <span data-ttu-id="f4723-217">Die Anzahl der Minuten, für die eine Besprechung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4723-217">Number of minutes for which a meeting would be conducted</span></span> |
| <span data-ttu-id="f4723-218">Compliance</span><span class="sxs-lookup"><span data-stu-id="f4723-218">place</span></span> | <span data-ttu-id="f4723-219">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="f4723-219">JSON object</span></span> | <span data-ttu-id="f4723-220">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-220">Yes</span></span> | <span data-ttu-id="f4723-221">Besprechungs Speicherort.</span><span class="sxs-lookup"><span data-stu-id="f4723-221">Meeting Location.</span></span> <span data-ttu-id="f4723-222">Enthält 3 Komponenten: Breite, Länge, Name</span><span class="sxs-lookup"><span data-stu-id="f4723-222">Contains 3 components: latitude, longitude, name</span></span>  |
| <span data-ttu-id="f4723-223">Agendas</span><span class="sxs-lookup"><span data-stu-id="f4723-223">agenda</span></span> | <span data-ttu-id="f4723-224">String</span><span class="sxs-lookup"><span data-stu-id="f4723-224">String</span></span> | <span data-ttu-id="f4723-225">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-225">Yes</span></span> | <span data-ttu-id="f4723-226">Agenda für die Besprechung/Beschreibung der Besprechung</span><span class="sxs-lookup"><span data-stu-id="f4723-226">Agenda for the Meeting / Description for the meeting</span></span> |
| <span data-ttu-id="f4723-227">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="f4723-227">isSenderOnly</span></span> | <span data-ttu-id="f4723-228">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="f4723-228">Bool</span></span> | <span data-ttu-id="f4723-229">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-229">Yes</span></span> | <span data-ttu-id="f4723-230">Nur für Absender, um die Zusammenfassung der Let es Meet anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4723-230">For allowing only sender to view Let's Meet summary.</span></span> <span data-ttu-id="f4723-231">Standard: false</span><span class="sxs-lookup"><span data-stu-id="f4723-231">Default: false</span></span> |

##### <a name="sample-json-request-for-a-lets-meet-action"></a><span data-ttu-id="f4723-232">JSON-Beispielanforderung für eine Let es Meet-Aktion</span><span class="sxs-lookup"><span data-stu-id="f4723-232">Sample JSON Request for a Let's Meet Action</span></span>

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a><span data-ttu-id="f4723-233">actionBody für eine Umfrageaktion oder eine Aktionspaket Instanz (ID):</span><span class="sxs-lookup"><span data-stu-id="f4723-233">actionBody for a Survey Action Or Action package instance(id) :</span></span>

| <span data-ttu-id="f4723-234">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-234">Parameter</span></span> | <span data-ttu-id="f4723-235">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-235">Type</span></span> | <span data-ttu-id="f4723-236">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-236">Optional?</span></span> | <span data-ttu-id="f4723-237">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-237">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-238">title</span><span class="sxs-lookup"><span data-stu-id="f4723-238">title</span></span> | <span data-ttu-id="f4723-239">String</span><span class="sxs-lookup"><span data-stu-id="f4723-239">String</span></span> | <span data-ttu-id="f4723-240">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-240">No</span></span> | <span data-ttu-id="f4723-241">Titel des Auftrags</span><span class="sxs-lookup"><span data-stu-id="f4723-241">Title of the Job</span></span> |
| <span data-ttu-id="f4723-242">dueDate</span><span class="sxs-lookup"><span data-stu-id="f4723-242">dueDate</span></span> | <span data-ttu-id="f4723-243">long</span><span class="sxs-lookup"><span data-stu-id="f4723-243">long</span></span> | <span data-ttu-id="f4723-244">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-244">Yes</span></span> | <span data-ttu-id="f4723-245">Standard: 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="f4723-245">Default: 24hrs.</span></span> <span data-ttu-id="f4723-246">Anzahl der Stunden, die vor der Ausführung des Auftrags ausgeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="f4723-246">Number of hours before which job should be completed</span></span> |
| <span data-ttu-id="f4723-247">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="f4723-247">isAnonymous</span></span> | <span data-ttu-id="f4723-248">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="f4723-248">Bool</span></span> | <span data-ttu-id="f4723-249">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-249">Yes</span></span> | <span data-ttu-id="f4723-250">Für die Gewährung anonymer Umfrage Antworten.</span><span class="sxs-lookup"><span data-stu-id="f4723-250">For allowing anonymous survey responses.</span></span> <span data-ttu-id="f4723-251">Standard: false</span><span class="sxs-lookup"><span data-stu-id="f4723-251">Default: false</span></span> |
| <span data-ttu-id="f4723-252">isSenderOnly</span><span class="sxs-lookup"><span data-stu-id="f4723-252">isSenderOnly</span></span> | <span data-ttu-id="f4723-253">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="f4723-253">Bool</span></span> | <span data-ttu-id="f4723-254">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-254">Yes</span></span> | <span data-ttu-id="f4723-255">Nur für Absender, um die Umfragezusammenfassung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4723-255">For allowing only sender to view survey summary.</span></span> <span data-ttu-id="f4723-256">Standard: false</span><span class="sxs-lookup"><span data-stu-id="f4723-256">Default: false</span></span> |
| <span data-ttu-id="f4723-257">acceptMultipleResponses</span><span class="sxs-lookup"><span data-stu-id="f4723-257">acceptMultipleResponses</span></span> | <span data-ttu-id="f4723-258">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="f4723-258">Bool</span></span> | <span data-ttu-id="f4723-259">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-259">Yes</span></span> | <span data-ttu-id="f4723-260">Für das Zulassen von mehreren Antworten vom gleichen Responder.</span><span class="sxs-lookup"><span data-stu-id="f4723-260">For allowing multiple responses from same responder.</span></span> <span data-ttu-id="f4723-261">Standard: false</span><span class="sxs-lookup"><span data-stu-id="f4723-261">Default: false</span></span> |
| <span data-ttu-id="f4723-262">Fragen</span><span class="sxs-lookup"><span data-stu-id="f4723-262">questions</span></span> | <span data-ttu-id="f4723-263">object[]</span><span class="sxs-lookup"><span data-stu-id="f4723-263">object[]</span></span> | <span data-ttu-id="f4723-264">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-264">No</span></span> | <span data-ttu-id="f4723-265">Jedes Element von Object [] wird im folgenden als Question-Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f4723-265">Each element of object[] is described below as Question object</span></span> |
| <span data-ttu-id="f4723-266">properties</span><span class="sxs-lookup"><span data-stu-id="f4723-266">properties</span></span> | <span data-ttu-id="f4723-267">object[]</span><span class="sxs-lookup"><span data-stu-id="f4723-267">object[]</span></span> | <span data-ttu-id="f4723-268">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-268">No</span></span> | <span data-ttu-id="f4723-269">Jedes Element von Object [] wird im folgenden als Property-Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f4723-269">Each element of object[] is described below as Property Object.</span></span> <span data-ttu-id="f4723-270">Nur gültig zum Erstellen einer Aktionspaket Instanz</span><span class="sxs-lookup"><span data-stu-id="f4723-270">Only valid for creating Action Package Instance</span></span> |

##### <a name="structure-for-question-object"></a><span data-ttu-id="f4723-271">Struktur für Question-Objekt</span><span class="sxs-lookup"><span data-stu-id="f4723-271">Structure for Question object</span></span>

| <span data-ttu-id="f4723-272">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-272">Parameter</span></span> | <span data-ttu-id="f4723-273">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-273">Type</span></span> | <span data-ttu-id="f4723-274">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-274">Optional?</span></span> | <span data-ttu-id="f4723-275">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-276">title</span><span class="sxs-lookup"><span data-stu-id="f4723-276">title</span></span> | <span data-ttu-id="f4723-277">String</span><span class="sxs-lookup"><span data-stu-id="f4723-277">String</span></span> | <span data-ttu-id="f4723-278">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-278">No</span></span> | <span data-ttu-id="f4723-279">Der Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="f4723-279">Title of the question</span></span> |
| <span data-ttu-id="f4723-280">type</span><span class="sxs-lookup"><span data-stu-id="f4723-280">type</span></span> | <span data-ttu-id="f4723-281">String</span><span class="sxs-lookup"><span data-stu-id="f4723-281">String</span></span> | <span data-ttu-id="f4723-282">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-282">No</span></span> | <span data-ttu-id="f4723-283">Typ der Frage.</span><span class="sxs-lookup"><span data-stu-id="f4723-283">Type of the question.</span></span> <span data-ttu-id="f4723-284">Enumeration: SingleOption/multiOption/Text/Image/numeric/Date/Location/Attachmentlist</span><span class="sxs-lookup"><span data-stu-id="f4723-284">Enum: SingleOption/MultiOption/Text/Image/Numeric/Date/Location/AttachmentList</span></span> |
| <span data-ttu-id="f4723-285">isUnsichtbar</span><span class="sxs-lookup"><span data-stu-id="f4723-285">isInvisible</span></span> | <span data-ttu-id="f4723-286">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="f4723-286">Bool</span></span> | <span data-ttu-id="f4723-287">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-287">Yes</span></span> | <span data-ttu-id="f4723-288">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="f4723-288">Default: false.</span></span> <span data-ttu-id="f4723-289">So steuern Sie die Sichtbarkeit der Frage</span><span class="sxs-lookup"><span data-stu-id="f4723-289">To control the visibility of the question</span></span> |
| <span data-ttu-id="f4723-290">options</span><span class="sxs-lookup"><span data-stu-id="f4723-290">options</span></span> | <span data-ttu-id="f4723-291">object[]</span><span class="sxs-lookup"><span data-stu-id="f4723-291">object[]</span></span> | <span data-ttu-id="f4723-292">Ja</span><span class="sxs-lookup"><span data-stu-id="f4723-292">Yes</span></span> | <span data-ttu-id="f4723-293">Obligatorisch für SingleOption-und multiOption-Fragentyp.</span><span class="sxs-lookup"><span data-stu-id="f4723-293">Mandatory for SingleOption and MultiOption question type.</span></span> <span data-ttu-id="f4723-294">jedes Element von Object [] wird im folgenden als Option-Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f4723-294">each element of object[] is described below as Option object</span></span> |

###### <a name="structure-for-option-object"></a><span data-ttu-id="f4723-295">Struktur für Option-Objekt</span><span class="sxs-lookup"><span data-stu-id="f4723-295">Structure for Option object</span></span>

| <span data-ttu-id="f4723-296">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-296">Parameter</span></span> | <span data-ttu-id="f4723-297">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-297">Type</span></span> | <span data-ttu-id="f4723-298">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-298">Optional?</span></span> | <span data-ttu-id="f4723-299">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-299">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-300">title</span><span class="sxs-lookup"><span data-stu-id="f4723-300">title</span></span> | <span data-ttu-id="f4723-301">String</span><span class="sxs-lookup"><span data-stu-id="f4723-301">String</span></span> | <span data-ttu-id="f4723-302">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-302">No</span></span> | <span data-ttu-id="f4723-303">Titel der Option</span><span class="sxs-lookup"><span data-stu-id="f4723-303">Title of the Option</span></span> |

###### <a name="structure-for-property-object"></a><span data-ttu-id="f4723-304">Struktur für Property-Objekt</span><span class="sxs-lookup"><span data-stu-id="f4723-304">Structure for Property object</span></span>

| <span data-ttu-id="f4723-305">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-305">Parameter</span></span> | <span data-ttu-id="f4723-306">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-306">Type</span></span> | <span data-ttu-id="f4723-307">Optional?</span><span class="sxs-lookup"><span data-stu-id="f4723-307">Optional?</span></span> | <span data-ttu-id="f4723-308">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-308">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f4723-309">name</span><span class="sxs-lookup"><span data-stu-id="f4723-309">name</span></span> | <span data-ttu-id="f4723-310">String</span><span class="sxs-lookup"><span data-stu-id="f4723-310">String</span></span> | <span data-ttu-id="f4723-311">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-311">No</span></span> | <span data-ttu-id="f4723-312">Name der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4723-312">Name of the property</span></span> |
| <span data-ttu-id="f4723-313">type</span><span class="sxs-lookup"><span data-stu-id="f4723-313">type</span></span> | <span data-ttu-id="f4723-314">String</span><span class="sxs-lookup"><span data-stu-id="f4723-314">String</span></span> | <span data-ttu-id="f4723-315">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-315">No</span></span> | <span data-ttu-id="f4723-316">Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f4723-316">Type of the property.</span></span> <span data-ttu-id="f4723-317">Enum: Text, numeric, Location, DateTime, Stringlist, Attachment, Stringset, Attachmentlist</span><span class="sxs-lookup"><span data-stu-id="f4723-317">Enum: Text, Numeric, Location, DateTime, StringList, Attachment, StringSet, AttachmentList</span></span> |
| <span data-ttu-id="f4723-318">value</span><span class="sxs-lookup"><span data-stu-id="f4723-318">value</span></span> | <span data-ttu-id="f4723-319">String</span><span class="sxs-lookup"><span data-stu-id="f4723-319">String</span></span> | <span data-ttu-id="f4723-320">Nein</span><span class="sxs-lookup"><span data-stu-id="f4723-320">No</span></span> | <span data-ttu-id="f4723-321">Wert der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4723-321">Value of the property</span></span> |

##### <a name="sample-json-request-for-a-survey-action"></a><span data-ttu-id="f4723-322">JSON-Beispielanforderung für eine Umfrageaktion</span><span class="sxs-lookup"><span data-stu-id="f4723-322">Sample JSON Request for a Survey Action</span></span>

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

##### <a name="response-body"></a><span data-ttu-id="f4723-323">Antworttext</span><span class="sxs-lookup"><span data-stu-id="f4723-323">Response body</span></span>

| <span data-ttu-id="f4723-324">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4723-324">Parameter</span></span> | <span data-ttu-id="f4723-325">Typ</span><span class="sxs-lookup"><span data-stu-id="f4723-325">Type</span></span> | <span data-ttu-id="f4723-326">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4723-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f4723-327">referenceId</span><span class="sxs-lookup"><span data-stu-id="f4723-327">referenceId</span></span> | <span data-ttu-id="f4723-328">String</span><span class="sxs-lookup"><span data-stu-id="f4723-328">String</span></span> | <span data-ttu-id="f4723-329">Anforderungs-ID</span><span class="sxs-lookup"><span data-stu-id="f4723-329">Request identifier</span></span> |
| <span data-ttu-id="f4723-330">actionId</span><span class="sxs-lookup"><span data-stu-id="f4723-330">actionId</span></span> | <span data-ttu-id="f4723-331">String</span><span class="sxs-lookup"><span data-stu-id="f4723-331">String</span></span> | <span data-ttu-id="f4723-332">Aktionsbezeichner</span><span class="sxs-lookup"><span data-stu-id="f4723-332">Action identifier</span></span> |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
