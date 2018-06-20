---
title: Locations
description: Referenzartikel für API zum Abfrage Gruppieren von Daten
topic: Reference
author: nitinjms
ms.openlocfilehash: 010d6d30c72355e2575cda2f8104316a5a770ac4
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905341"
---
# <a name="apis-to-query-kaizala-groups"></a><span data-ttu-id="c6462-103">APIs für die Abfrage Kaizala Gruppen</span><span class="sxs-lookup"><span data-stu-id="c6462-103">APIs to query Kaizala groups</span></span>
## <a name="groups"></a><span data-ttu-id="c6462-104">Locations</span><span class="sxs-lookup"><span data-stu-id="c6462-104">/groups</span></span>
<span data-ttu-id="c6462-105">Interaktion mit der Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c6462-105">API end-point to interact with the conversation groups inside Kaizala.</span></span>

### <a name="post-groups"></a><span data-ttu-id="c6462-106">POST-Locations</span><span class="sxs-lookup"><span data-stu-id="c6462-106">POST /groups</span></span>

    Post {endpoint-url}/v1/groups

##### <a name="request-parameters"></a><span data-ttu-id="c6462-107">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="c6462-107">Request Parameters</span></span>

|  | <span data-ttu-id="c6462-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-108">Parameter</span></span> | <span data-ttu-id="c6462-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-109">Type</span></span> | <span data-ttu-id="c6462-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="c6462-110">Optional?</span></span> | <span data-ttu-id="c6462-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c6462-112">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c6462-112">HTTP Header</span></span> | <span data-ttu-id="c6462-113">accessToken</span><span class="sxs-lookup"><span data-stu-id="c6462-113">accessToken</span></span> | <span data-ttu-id="c6462-114">String</span><span class="sxs-lookup"><span data-stu-id="c6462-114">String</span></span> | <span data-ttu-id="c6462-115">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-115">No</span></span> | <span data-ttu-id="c6462-116">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c6462-116">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="c6462-117">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c6462-117">HTTP Header</span></span> | <span data-ttu-id="c6462-118">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c6462-118">Content-Type</span></span> | <span data-ttu-id="c6462-119">String</span><span class="sxs-lookup"><span data-stu-id="c6462-119">String</span></span> | <span data-ttu-id="c6462-120">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-120">No</span></span> | <span data-ttu-id="c6462-121">"Application/Json"</span><span class="sxs-lookup"><span data-stu-id="c6462-121">"application/json"</span></span> |

##### <a name="request-body"></a><span data-ttu-id="c6462-122">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="c6462-122">Request body</span></span>

| <span data-ttu-id="c6462-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-123">Parameter</span></span> | <span data-ttu-id="c6462-124">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-124">Type</span></span> | <span data-ttu-id="c6462-125">Optional?</span><span class="sxs-lookup"><span data-stu-id="c6462-125">Optional?</span></span> | <span data-ttu-id="c6462-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-126">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="c6462-127">name</span><span class="sxs-lookup"><span data-stu-id="c6462-127">name</span></span> | <span data-ttu-id="c6462-128">String</span><span class="sxs-lookup"><span data-stu-id="c6462-128">String</span></span> | <span data-ttu-id="c6462-129">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-129">No</span></span> | <span data-ttu-id="c6462-130">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="c6462-130">Group name</span></span> |
| <span data-ttu-id="c6462-131">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="c6462-131">welcomeMessage</span></span> | <span data-ttu-id="c6462-132">String</span><span class="sxs-lookup"><span data-stu-id="c6462-132">String</span></span> | <span data-ttu-id="c6462-133">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-133">No</span></span> | <span data-ttu-id="c6462-134">Willkommensnachricht das neue Mitglied der Gruppe angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="c6462-134">Welcome message which will be displayed to new group member</span></span> |
| <span data-ttu-id="c6462-135">Elemente</span><span class="sxs-lookup"><span data-stu-id="c6462-135">members</span></span> | <span data-ttu-id="c6462-136">String]</span><span class="sxs-lookup"><span data-stu-id="c6462-136">String[]</span></span> | <span data-ttu-id="c6462-137">Ja</span><span class="sxs-lookup"><span data-stu-id="c6462-137">Yes</span></span> | <span data-ttu-id="c6462-138">Die Mobiltelefonnummer (mit Ländercode) Mitglieder hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6462-138">Mobile number(with country code) of members to be added.</span></span> <span data-ttu-id="c6462-139">Standard: Zugangs-Token Benutzer wird als Administrator der Gruppe hinzugefügt werden</span><span class="sxs-lookup"><span data-stu-id="c6462-139">Default: Access token's user will be added as admin of the group</span></span> |
| <span data-ttu-id="c6462-140">groupType</span><span class="sxs-lookup"><span data-stu-id="c6462-140">groupType</span></span> | <span data-ttu-id="c6462-141">String</span><span class="sxs-lookup"><span data-stu-id="c6462-141">String</span></span> | <span data-ttu-id="c6462-142">Ja</span><span class="sxs-lookup"><span data-stu-id="c6462-142">Yes</span></span> | <span data-ttu-id="c6462-143">Enum: Gruppe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="c6462-143">Enum: Group/ConnectGroup.</span></span> <span data-ttu-id="c6462-144">ConnectGroup werden verwaltete öffentliche Gruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6462-144">ConnectGroup will create Managed Public group.</span></span> <span data-ttu-id="c6462-145">Standard: Gruppe</span><span class="sxs-lookup"><span data-stu-id="c6462-145">Default: Group</span></span> |

###### <a name="sample-json-request-for-create-group"></a><span data-ttu-id="c6462-146">Beispiel für eine Anforderung für JSON Gruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="c6462-146">Sample JSON Request for Create Group</span></span>

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

##### <a name="response-body"></a><span data-ttu-id="c6462-147">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c6462-147">Response body</span></span>

| <span data-ttu-id="c6462-148">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-148">Parameter</span></span> | <span data-ttu-id="c6462-149">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-149">Type</span></span> | <span data-ttu-id="c6462-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-150">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c6462-151">groupName</span><span class="sxs-lookup"><span data-stu-id="c6462-151">groupName</span></span> | <span data-ttu-id="c6462-152">String</span><span class="sxs-lookup"><span data-stu-id="c6462-152">String</span></span> | <span data-ttu-id="c6462-153">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="c6462-153">Group name</span></span> |
| <span data-ttu-id="c6462-154">groupId</span><span class="sxs-lookup"><span data-stu-id="c6462-154">groupId</span></span> | <span data-ttu-id="c6462-155">String</span><span class="sxs-lookup"><span data-stu-id="c6462-155">String</span></span> | <span data-ttu-id="c6462-156">Gruppen-ID, die im weiteren API-Aufrufe verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="c6462-156">Group Identifier which can be used in subsequent api calls</span></span> |
| <span data-ttu-id="c6462-157">membersAdded</span><span class="sxs-lookup"><span data-stu-id="c6462-157">membersAdded</span></span> | <span data-ttu-id="c6462-158">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-158">bool</span></span> | <span data-ttu-id="c6462-159">True, wenn alle Mitglieder sind erfolgreich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6462-159">True if all members are successfully added</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="c6462-160">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="c6462-160">Sample JSON Response</span></span>

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


### <a name="get-groups"></a><span data-ttu-id="c6462-161">Abrufen von Locations</span><span class="sxs-lookup"><span data-stu-id="c6462-161">GET /groups</span></span>

    GET {endpoint-url}/v1/groups

##### <a name="request-parameters"></a><span data-ttu-id="c6462-162">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="c6462-162">Request Parameters</span></span>

|  | <span data-ttu-id="c6462-163">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-163">Parameter</span></span> | <span data-ttu-id="c6462-164">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-164">Type</span></span> | <span data-ttu-id="c6462-165">Optional?</span><span class="sxs-lookup"><span data-stu-id="c6462-165">Optional?</span></span> | <span data-ttu-id="c6462-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-166">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c6462-167">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c6462-167">HTTP Header</span></span> | <span data-ttu-id="c6462-168">accessToken</span><span class="sxs-lookup"><span data-stu-id="c6462-168">accessToken</span></span> | <span data-ttu-id="c6462-169">String</span><span class="sxs-lookup"><span data-stu-id="c6462-169">String</span></span> | <span data-ttu-id="c6462-170">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-170">No</span></span> | <span data-ttu-id="c6462-171">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c6462-171">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="c6462-172">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="c6462-172">Query parameter</span></span> | <span data-ttu-id="c6462-173">showDetail</span><span class="sxs-lookup"><span data-stu-id="c6462-173">showDetail</span></span> | <span data-ttu-id="c6462-174">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-174">bool</span></span> | <span data-ttu-id="c6462-175">Ja</span><span class="sxs-lookup"><span data-stu-id="c6462-175">Yes</span></span> | <span data-ttu-id="c6462-176">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="c6462-176">Default: false.</span></span> <span data-ttu-id="c6462-177">True, wenn Return Gruppe alle details</span><span class="sxs-lookup"><span data-stu-id="c6462-177">True to return all group details</span></span> |
| <span data-ttu-id="c6462-178">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="c6462-178">Query parameter</span></span> | <span data-ttu-id="c6462-179">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="c6462-179">fetchAllGroups</span></span> | <span data-ttu-id="c6462-180">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-180">bool</span></span> | <span data-ttu-id="c6462-181">Ja</span><span class="sxs-lookup"><span data-stu-id="c6462-181">Yes</span></span> | <span data-ttu-id="c6462-182">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="c6462-182">Default: false.</span></span> <span data-ttu-id="c6462-183">True zurück, um alle übergeordneten und sub-Gruppen</span><span class="sxs-lookup"><span data-stu-id="c6462-183">True to return all parent and sub groups</span></span> |

##### <a name="response-body"></a><span data-ttu-id="c6462-184">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c6462-184">Response body</span></span>

| <span data-ttu-id="c6462-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-185">Parameter</span></span> | <span data-ttu-id="c6462-186">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-186">Type</span></span> | <span data-ttu-id="c6462-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-187">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c6462-188">Gruppen</span><span class="sxs-lookup"><span data-stu-id="c6462-188">groups</span></span> | <span data-ttu-id="c6462-189">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="c6462-189">JSON Object Array</span></span> | <span data-ttu-id="c6462-190">Array von Gruppen, dass der Benutzer Zugriff auf mit der AccessToken hat.</span><span class="sxs-lookup"><span data-stu-id="c6462-190">Array of groups that the user has access to with the accessToken</span></span> |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="c6462-191">JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:</span><span class="sxs-lookup"><span data-stu-id="c6462-191">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="c6462-192">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-192">Parameter</span></span> | <span data-ttu-id="c6462-193">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-193">Type</span></span> | <span data-ttu-id="c6462-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-194">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c6462-195">groupId</span><span class="sxs-lookup"><span data-stu-id="c6462-195">groupId</span></span> | <span data-ttu-id="c6462-196">String</span><span class="sxs-lookup"><span data-stu-id="c6462-196">String</span></span> | <span data-ttu-id="c6462-197">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="c6462-197">Group Identifier</span></span> |
| <span data-ttu-id="c6462-198">groupName</span><span class="sxs-lookup"><span data-stu-id="c6462-198">groupName</span></span> | <span data-ttu-id="c6462-199">String</span><span class="sxs-lookup"><span data-stu-id="c6462-199">String</span></span> | <span data-ttu-id="c6462-200">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="c6462-200">Name of the group</span></span> |
| <span data-ttu-id="c6462-201">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="c6462-201">groupImageURL</span></span> | <span data-ttu-id="c6462-202">String</span><span class="sxs-lookup"><span data-stu-id="c6462-202">String</span></span> | <span data-ttu-id="c6462-203">Zeichenfolge, die die URL des Bilds Profil Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="c6462-203">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="c6462-204">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="c6462-204">hasSubGroups</span></span> | <span data-ttu-id="c6462-205">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-205">bool</span></span> | <span data-ttu-id="c6462-206">True, wenn die Gruppe Untergruppen besitzt.</span><span class="sxs-lookup"><span data-stu-id="c6462-206">True if the group has subgroups</span></span> |
| <span data-ttu-id="c6462-207">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="c6462-207">hasParentGroups</span></span> | <span data-ttu-id="c6462-208">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-208">bool</span></span> | <span data-ttu-id="c6462-209">True, wenn die Gruppe verfügt über die übergeordneten Gruppen</span><span class="sxs-lookup"><span data-stu-id="c6462-209">True if the group has parent groups</span></span> |
| <span data-ttu-id="c6462-210">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="c6462-210">isMappedToTenant</span></span> | <span data-ttu-id="c6462-211">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-211">bool</span></span> | <span data-ttu-id="c6462-212">True, wenn die Gruppe Organisation Gruppe ist</span><span class="sxs-lookup"><span data-stu-id="c6462-212">True if the group is Organisation group</span></span> |
| <span data-ttu-id="c6462-213">groupType</span><span class="sxs-lookup"><span data-stu-id="c6462-213">groupType</span></span> | <span data-ttu-id="c6462-214">String</span><span class="sxs-lookup"><span data-stu-id="c6462-214">String</span></span> | <span data-ttu-id="c6462-215">Gruppe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="c6462-215">Group/ConnectGroup.</span></span> <span data-ttu-id="c6462-216">ConnectGroup Wenn die Gruppe in der Gruppe Public verwaltet</span><span class="sxs-lookup"><span data-stu-id="c6462-216">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="c6462-217">userCount</span><span class="sxs-lookup"><span data-stu-id="c6462-217">userCount</span></span> | <span data-ttu-id="c6462-218">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c6462-218">Numeric</span></span> | <span data-ttu-id="c6462-219">Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie</span><span class="sxs-lookup"><span data-stu-id="c6462-219">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="c6462-220">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="c6462-220">currentLevelUserCount</span></span> | <span data-ttu-id="c6462-221">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c6462-221">Numeric</span></span> | <span data-ttu-id="c6462-222">Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="c6462-222">Total number of individual members of the group at the current level</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="c6462-223">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="c6462-223">Sample JSON Response</span></span>

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": false,
      "hasParentGroups": false,
      "callerRole": "Admin",
      "currentLevelSubGroupCount": 0,
      "currentLevelParentGroupCount": 0,
      "userCount": 2,
      "uniqueUserCount": 0,
      "currentLevelUserCount": 2,
      "currentLevelUnProvisionedUserCount": 0,
      "unProvisionedUserCount": 0,
      "isMappedToTenant": false,
      "groupType": "Group",
      "isDuplicate": false,
      "isEditable": true,
      "isDetailsReadable": true
    }
  ]
}
```

### <a name="get-groupsgroupid"></a><span data-ttu-id="c6462-224">Abrufen von /groups/ {GroupId}</span><span class="sxs-lookup"><span data-stu-id="c6462-224">GET /groups/{groupId}</span></span>

<span data-ttu-id="c6462-225">Sie können die Details zu einer bestimmten Ressource Member (hier eine Gruppe) abrufen, indem der Bezeichner als URL Path-Parameter angeben</span><span class="sxs-lookup"><span data-stu-id="c6462-225">You can get details about a specific resource member (a group here) by specifying the identifier as a URL path parameter</span></span>

    GET {endpoint-url}/groups/{groupId}

##### <a name="request-parameters"></a><span data-ttu-id="c6462-226">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="c6462-226">Request Parameters</span></span>

|  | <span data-ttu-id="c6462-227">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-227">Parameter</span></span> | <span data-ttu-id="c6462-228">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-228">Type</span></span> | <span data-ttu-id="c6462-229">Optional?</span><span class="sxs-lookup"><span data-stu-id="c6462-229">Optional?</span></span> | <span data-ttu-id="c6462-230">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-230">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c6462-231">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-231">URL Path Parameter</span></span> | <span data-ttu-id="c6462-232">groupId</span><span class="sxs-lookup"><span data-stu-id="c6462-232">groupId</span></span> | <span data-ttu-id="c6462-233">String</span><span class="sxs-lookup"><span data-stu-id="c6462-233">String</span></span> | <span data-ttu-id="c6462-234">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-234">No</span></span> | <span data-ttu-id="c6462-235">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6462-235">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="c6462-236">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c6462-236">HTTP Header</span></span> | <span data-ttu-id="c6462-237">accessToken</span><span class="sxs-lookup"><span data-stu-id="c6462-237">accessToken</span></span> | <span data-ttu-id="c6462-238">String</span><span class="sxs-lookup"><span data-stu-id="c6462-238">String</span></span> | <span data-ttu-id="c6462-239">Nein</span><span class="sxs-lookup"><span data-stu-id="c6462-239">No</span></span> | <span data-ttu-id="c6462-240">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c6462-240">Access Token received from the auth end-point</span></span> |

##### <a name="response-body"></a><span data-ttu-id="c6462-241">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c6462-241">Response body</span></span>

| <span data-ttu-id="c6462-242">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-242">Parameter</span></span> | <span data-ttu-id="c6462-243">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-243">Type</span></span> | <span data-ttu-id="c6462-244">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-244">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c6462-245">Gruppen</span><span class="sxs-lookup"><span data-stu-id="c6462-245">groups</span></span> | <span data-ttu-id="c6462-246">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="c6462-246">JSON Object Array</span></span> | <span data-ttu-id="c6462-247">Array von Gruppen, dass der Benutzer Zugriff auf mit der AccessToken hat.</span><span class="sxs-lookup"><span data-stu-id="c6462-247">Array of groups that the user has access to with the accessToken</span></span> |

<span data-ttu-id="c6462-248">JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:</span><span class="sxs-lookup"><span data-stu-id="c6462-248">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="c6462-249">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6462-249">Parameter</span></span> | <span data-ttu-id="c6462-250">Typ</span><span class="sxs-lookup"><span data-stu-id="c6462-250">Type</span></span> | <span data-ttu-id="c6462-251">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6462-251">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c6462-252">groupId</span><span class="sxs-lookup"><span data-stu-id="c6462-252">groupId</span></span> | <span data-ttu-id="c6462-253">String</span><span class="sxs-lookup"><span data-stu-id="c6462-253">String</span></span> | <span data-ttu-id="c6462-254">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="c6462-254">Group Identifier</span></span> |
| <span data-ttu-id="c6462-255">groupName</span><span class="sxs-lookup"><span data-stu-id="c6462-255">groupName</span></span> | <span data-ttu-id="c6462-256">String</span><span class="sxs-lookup"><span data-stu-id="c6462-256">String</span></span> | <span data-ttu-id="c6462-257">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="c6462-257">Name of the group</span></span> |
| <span data-ttu-id="c6462-258">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="c6462-258">groupImageURL</span></span> | <span data-ttu-id="c6462-259">String</span><span class="sxs-lookup"><span data-stu-id="c6462-259">String</span></span> | <span data-ttu-id="c6462-260">Zeichenfolge, die die URL des Bilds Profil Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="c6462-260">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="c6462-261">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="c6462-261">hasSubGroups</span></span> | <span data-ttu-id="c6462-262">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-262">bool</span></span> | <span data-ttu-id="c6462-263">True, wenn die Gruppe Untergruppen besitzt.</span><span class="sxs-lookup"><span data-stu-id="c6462-263">True if the group has subgroups</span></span> |
| <span data-ttu-id="c6462-264">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="c6462-264">hasParentGroups</span></span> | <span data-ttu-id="c6462-265">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-265">bool</span></span> | <span data-ttu-id="c6462-266">True, wenn die Gruppe verfügt über die übergeordneten Gruppen</span><span class="sxs-lookup"><span data-stu-id="c6462-266">True if the group has parent groups</span></span> |
| <span data-ttu-id="c6462-267">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="c6462-267">isMappedToTenant</span></span> | <span data-ttu-id="c6462-268">bool</span><span class="sxs-lookup"><span data-stu-id="c6462-268">bool</span></span> | <span data-ttu-id="c6462-269">True, wenn die Gruppe Organisation Gruppe ist</span><span class="sxs-lookup"><span data-stu-id="c6462-269">True if the group is Organisation group</span></span> |
| <span data-ttu-id="c6462-270">groupType</span><span class="sxs-lookup"><span data-stu-id="c6462-270">groupType</span></span> | <span data-ttu-id="c6462-271">String</span><span class="sxs-lookup"><span data-stu-id="c6462-271">String</span></span> | <span data-ttu-id="c6462-272">Gruppe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="c6462-272">Group/ConnectGroup.</span></span> <span data-ttu-id="c6462-273">ConnectGroup Wenn die Gruppe in der Gruppe Public verwaltet</span><span class="sxs-lookup"><span data-stu-id="c6462-273">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="c6462-274">userCount</span><span class="sxs-lookup"><span data-stu-id="c6462-274">userCount</span></span> | <span data-ttu-id="c6462-275">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c6462-275">Numeric</span></span> | <span data-ttu-id="c6462-276">Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie</span><span class="sxs-lookup"><span data-stu-id="c6462-276">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="c6462-277">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="c6462-277">currentLevelUserCount</span></span> | <span data-ttu-id="c6462-278">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c6462-278">Numeric</span></span> | <span data-ttu-id="c6462-279">Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="c6462-279">Total number of individual members of the group at the current level</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="c6462-280">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="c6462-280">Sample JSON Response</span></span>

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "hasSubGroups": true,
      "userCount": 200,
      "currentLevelUserCount": 10
    }
  ]
}
```

