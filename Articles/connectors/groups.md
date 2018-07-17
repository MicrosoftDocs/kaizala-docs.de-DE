---
title: Locations
description: Referenzartikel für API zum Abfrage Gruppieren von Daten
topic: Reference
author: nitinjms
ms.openlocfilehash: 6a0b56d36aef458b5a3d302235499f445ed134e6
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399373"
---
# <a name="groups"></a><span data-ttu-id="c683e-103">Locations</span><span class="sxs-lookup"><span data-stu-id="c683e-103">/groups</span></span>
<span data-ttu-id="c683e-104">Interaktion mit der Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c683e-104">API end-point to interact with the conversation groups inside Kaizala.</span></span>

## <a name="post-groups"></a><span data-ttu-id="c683e-105">POST-Locations</span><span class="sxs-lookup"><span data-stu-id="c683e-105">POST /groups</span></span>

    Post {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="c683e-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="c683e-106">Request Parameters</span></span>

|  | <span data-ttu-id="c683e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-107">Parameter</span></span> | <span data-ttu-id="c683e-108">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-108">Type</span></span> | <span data-ttu-id="c683e-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="c683e-109">Optional?</span></span> | <span data-ttu-id="c683e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c683e-111">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c683e-111">HTTP Header</span></span> | <span data-ttu-id="c683e-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="c683e-112">accessToken</span></span> | <span data-ttu-id="c683e-113">String</span><span class="sxs-lookup"><span data-stu-id="c683e-113">String</span></span> | <span data-ttu-id="c683e-114">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-114">No</span></span> | <span data-ttu-id="c683e-115">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c683e-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="c683e-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c683e-116">HTTP Header</span></span> | <span data-ttu-id="c683e-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c683e-117">Content-Type</span></span> | <span data-ttu-id="c683e-118">String</span><span class="sxs-lookup"><span data-stu-id="c683e-118">String</span></span> | <span data-ttu-id="c683e-119">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-119">No</span></span> | <span data-ttu-id="c683e-120">"Application/Json"</span><span class="sxs-lookup"><span data-stu-id="c683e-120">"application/json"</span></span> |

### <a name="request-body"></a><span data-ttu-id="c683e-121">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="c683e-121">Request body</span></span>

| <span data-ttu-id="c683e-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-122">Parameter</span></span> | <span data-ttu-id="c683e-123">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-123">Type</span></span> | <span data-ttu-id="c683e-124">Optional?</span><span class="sxs-lookup"><span data-stu-id="c683e-124">Optional?</span></span> | <span data-ttu-id="c683e-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-125">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="c683e-126">name</span><span class="sxs-lookup"><span data-stu-id="c683e-126">name</span></span> | <span data-ttu-id="c683e-127">String</span><span class="sxs-lookup"><span data-stu-id="c683e-127">String</span></span> | <span data-ttu-id="c683e-128">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-128">No</span></span> | <span data-ttu-id="c683e-129">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="c683e-129">Group name</span></span> |
| <span data-ttu-id="c683e-130">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="c683e-130">welcomeMessage</span></span> | <span data-ttu-id="c683e-131">String</span><span class="sxs-lookup"><span data-stu-id="c683e-131">String</span></span> | <span data-ttu-id="c683e-132">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-132">No</span></span> | <span data-ttu-id="c683e-133">Willkommensnachricht das neue Mitglied der Gruppe angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="c683e-133">Welcome message which will be displayed to new group member</span></span> |
| <span data-ttu-id="c683e-134">Elemente</span><span class="sxs-lookup"><span data-stu-id="c683e-134">members</span></span> | <span data-ttu-id="c683e-135">String]</span><span class="sxs-lookup"><span data-stu-id="c683e-135">String[]</span></span> | <span data-ttu-id="c683e-136">Ja</span><span class="sxs-lookup"><span data-stu-id="c683e-136">Yes</span></span> | <span data-ttu-id="c683e-137">Die Mobiltelefonnummer (mit Ländercode) Mitglieder hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c683e-137">Mobile number(with country code) of members to be added.</span></span> <span data-ttu-id="c683e-138">Standard: Zugangs-Token Benutzer wird als Administrator der Gruppe hinzugefügt werden</span><span class="sxs-lookup"><span data-stu-id="c683e-138">Default: Access token's user will be added as admin of the group</span></span> |
| <span data-ttu-id="c683e-139">groupType</span><span class="sxs-lookup"><span data-stu-id="c683e-139">groupType</span></span> | <span data-ttu-id="c683e-140">String</span><span class="sxs-lookup"><span data-stu-id="c683e-140">String</span></span> | <span data-ttu-id="c683e-141">Ja</span><span class="sxs-lookup"><span data-stu-id="c683e-141">Yes</span></span> | <span data-ttu-id="c683e-142">Enum: Gruppe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="c683e-142">Enum: Group/ConnectGroup.</span></span> <span data-ttu-id="c683e-143">ConnectGroup werden verwaltete öffentliche Gruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="c683e-143">ConnectGroup will create Managed Public group.</span></span> <span data-ttu-id="c683e-144">Standard: Gruppe</span><span class="sxs-lookup"><span data-stu-id="c683e-144">Default: Group</span></span> |

#### <a name="sample-json-request-for-create-group"></a><span data-ttu-id="c683e-145">Beispiel für eine Anforderung für JSON Gruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="c683e-145">Sample JSON Request for Create Group</span></span>

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

### <a name="response-body"></a><span data-ttu-id="c683e-146">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c683e-146">Response body</span></span>

| <span data-ttu-id="c683e-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-147">Parameter</span></span> | <span data-ttu-id="c683e-148">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-148">Type</span></span> | <span data-ttu-id="c683e-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-149">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c683e-150">groupName</span><span class="sxs-lookup"><span data-stu-id="c683e-150">groupName</span></span> | <span data-ttu-id="c683e-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-151">String</span></span> | <span data-ttu-id="c683e-152">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="c683e-152">Group name</span></span> |
| <span data-ttu-id="c683e-153">groupId</span><span class="sxs-lookup"><span data-stu-id="c683e-153">groupId</span></span> | <span data-ttu-id="c683e-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-154">String</span></span> | <span data-ttu-id="c683e-155">Gruppen-ID, die im weiteren API-Aufrufe verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="c683e-155">Group Identifier which can be used in subsequent api calls</span></span> |
| <span data-ttu-id="c683e-156">membersAdded</span><span class="sxs-lookup"><span data-stu-id="c683e-156">membersAdded</span></span> | <span data-ttu-id="c683e-157">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-157">bool</span></span> | <span data-ttu-id="c683e-158">True, wenn alle Mitglieder sind erfolgreich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c683e-158">True if all members are successfully added</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="c683e-159">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="c683e-159">Sample JSON Response</span></span>

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


## <a name="get-groups"></a><span data-ttu-id="c683e-160">Abrufen von Locations</span><span class="sxs-lookup"><span data-stu-id="c683e-160">GET /groups</span></span>

    GET {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="c683e-161">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="c683e-161">Request Parameters</span></span>

|  | <span data-ttu-id="c683e-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-162">Parameter</span></span> | <span data-ttu-id="c683e-163">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-163">Type</span></span> | <span data-ttu-id="c683e-164">Optional?</span><span class="sxs-lookup"><span data-stu-id="c683e-164">Optional?</span></span> | <span data-ttu-id="c683e-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c683e-166">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c683e-166">HTTP Header</span></span> | <span data-ttu-id="c683e-167">accessToken</span><span class="sxs-lookup"><span data-stu-id="c683e-167">accessToken</span></span> | <span data-ttu-id="c683e-168">String</span><span class="sxs-lookup"><span data-stu-id="c683e-168">String</span></span> | <span data-ttu-id="c683e-169">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-169">No</span></span> | <span data-ttu-id="c683e-170">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c683e-170">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="c683e-171">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="c683e-171">Query parameter</span></span> | <span data-ttu-id="c683e-172">showDetail</span><span class="sxs-lookup"><span data-stu-id="c683e-172">showDetail</span></span> | <span data-ttu-id="c683e-173">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-173">bool</span></span> | <span data-ttu-id="c683e-174">Ja</span><span class="sxs-lookup"><span data-stu-id="c683e-174">Yes</span></span> | <span data-ttu-id="c683e-175">Standard: False.</span><span class="sxs-lookup"><span data-stu-id="c683e-175">Default: false.</span></span> <span data-ttu-id="c683e-176">True, wenn Return Gruppe alle details</span><span class="sxs-lookup"><span data-stu-id="c683e-176">True to return all group details</span></span> |
| <span data-ttu-id="c683e-177">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="c683e-177">Query parameter</span></span> | <span data-ttu-id="c683e-178">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="c683e-178">fetchAllGroups</span></span> | <span data-ttu-id="c683e-179">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-179">bool</span></span> | <span data-ttu-id="c683e-180">Ja</span><span class="sxs-lookup"><span data-stu-id="c683e-180">Yes</span></span> | <span data-ttu-id="c683e-181">Standard: False.</span><span class="sxs-lookup"><span data-stu-id="c683e-181">Default: false.</span></span> <span data-ttu-id="c683e-182">True zurück, um alle übergeordneten und sub-Gruppen</span><span class="sxs-lookup"><span data-stu-id="c683e-182">True to return all parent and sub groups</span></span> |

### <a name="response-body"></a><span data-ttu-id="c683e-183">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c683e-183">Response body</span></span>

| <span data-ttu-id="c683e-184">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-184">Parameter</span></span> | <span data-ttu-id="c683e-185">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-185">Type</span></span> | <span data-ttu-id="c683e-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c683e-187">Gruppen</span><span class="sxs-lookup"><span data-stu-id="c683e-187">groups</span></span> | <span data-ttu-id="c683e-188">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="c683e-188">JSON Object Array</span></span> | <span data-ttu-id="c683e-189">Array von Gruppen, dass der Benutzer Zugriff auf mit der AccessToken hat.</span><span class="sxs-lookup"><span data-stu-id="c683e-189">Array of groups that the user has access to with the accessToken</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="c683e-190">JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:</span><span class="sxs-lookup"><span data-stu-id="c683e-190">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="c683e-191">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-191">Parameter</span></span> | <span data-ttu-id="c683e-192">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-192">Type</span></span> | <span data-ttu-id="c683e-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-193">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c683e-194">groupId</span><span class="sxs-lookup"><span data-stu-id="c683e-194">groupId</span></span> | <span data-ttu-id="c683e-195">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-195">String</span></span> | <span data-ttu-id="c683e-196">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="c683e-196">Group Identifier</span></span> |
| <span data-ttu-id="c683e-197">groupName</span><span class="sxs-lookup"><span data-stu-id="c683e-197">groupName</span></span> | <span data-ttu-id="c683e-198">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-198">String</span></span> | <span data-ttu-id="c683e-199">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="c683e-199">Name of the group</span></span> |
| <span data-ttu-id="c683e-200">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="c683e-200">groupImageURL</span></span> | <span data-ttu-id="c683e-201">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-201">String</span></span> | <span data-ttu-id="c683e-202">Zeichenfolge, die die URL des Bilds Profil Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="c683e-202">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="c683e-203">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="c683e-203">hasSubGroups</span></span> | <span data-ttu-id="c683e-204">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-204">bool</span></span> | <span data-ttu-id="c683e-205">True, wenn die Gruppe Untergruppen besitzt.</span><span class="sxs-lookup"><span data-stu-id="c683e-205">True if the group has subgroups</span></span> |
| <span data-ttu-id="c683e-206">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="c683e-206">hasParentGroups</span></span> | <span data-ttu-id="c683e-207">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-207">bool</span></span> | <span data-ttu-id="c683e-208">True, wenn die Gruppe verfügt über die übergeordneten Gruppen</span><span class="sxs-lookup"><span data-stu-id="c683e-208">True if the group has parent groups</span></span> |
| <span data-ttu-id="c683e-209">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="c683e-209">isMappedToTenant</span></span> | <span data-ttu-id="c683e-210">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-210">bool</span></span> | <span data-ttu-id="c683e-211">True, wenn die Gruppe Organisation Gruppe ist</span><span class="sxs-lookup"><span data-stu-id="c683e-211">True if the group is Organisation group</span></span> |
| <span data-ttu-id="c683e-212">groupType</span><span class="sxs-lookup"><span data-stu-id="c683e-212">groupType</span></span> | <span data-ttu-id="c683e-213">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-213">String</span></span> | <span data-ttu-id="c683e-214">Gruppe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="c683e-214">Group/ConnectGroup.</span></span> <span data-ttu-id="c683e-215">ConnectGroup Wenn die Gruppe in der Gruppe Public verwaltet</span><span class="sxs-lookup"><span data-stu-id="c683e-215">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="c683e-216">userCount</span><span class="sxs-lookup"><span data-stu-id="c683e-216">userCount</span></span> | <span data-ttu-id="c683e-217">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c683e-217">Numeric</span></span> | <span data-ttu-id="c683e-218">Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie</span><span class="sxs-lookup"><span data-stu-id="c683e-218">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="c683e-219">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="c683e-219">currentLevelUserCount</span></span> | <span data-ttu-id="c683e-220">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c683e-220">Numeric</span></span> | <span data-ttu-id="c683e-221">Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="c683e-221">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="c683e-222">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="c683e-222">Sample JSON Response</span></span>

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

## <a name="get-groupsgroupid"></a><span data-ttu-id="c683e-223">Abrufen von /groups/ {GroupId}</span><span class="sxs-lookup"><span data-stu-id="c683e-223">GET /groups/{groupId}</span></span>

<span data-ttu-id="c683e-224">Sie können die Details zu einer bestimmten Ressource Member (hier eine Gruppe) abrufen, indem der Bezeichner als URL Path-Parameter angeben</span><span class="sxs-lookup"><span data-stu-id="c683e-224">You can get details about a specific resource member (a group here) by specifying the identifier as a URL path parameter</span></span>

    GET {endpoint-url}/groups/{groupId}

### <a name="request-parameters"></a><span data-ttu-id="c683e-225">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="c683e-225">Request Parameters</span></span>

|  | <span data-ttu-id="c683e-226">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-226">Parameter</span></span> | <span data-ttu-id="c683e-227">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-227">Type</span></span> | <span data-ttu-id="c683e-228">Optional?</span><span class="sxs-lookup"><span data-stu-id="c683e-228">Optional?</span></span> | <span data-ttu-id="c683e-229">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-229">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c683e-230">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-230">URL Path Parameter</span></span> | <span data-ttu-id="c683e-231">groupId</span><span class="sxs-lookup"><span data-stu-id="c683e-231">groupId</span></span> | <span data-ttu-id="c683e-232">String</span><span class="sxs-lookup"><span data-stu-id="c683e-232">String</span></span> | <span data-ttu-id="c683e-233">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-233">No</span></span> | <span data-ttu-id="c683e-234">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="c683e-234">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="c683e-235">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="c683e-235">HTTP Header</span></span> | <span data-ttu-id="c683e-236">accessToken</span><span class="sxs-lookup"><span data-stu-id="c683e-236">accessToken</span></span> | <span data-ttu-id="c683e-237">String</span><span class="sxs-lookup"><span data-stu-id="c683e-237">String</span></span> | <span data-ttu-id="c683e-238">Nein</span><span class="sxs-lookup"><span data-stu-id="c683e-238">No</span></span> | <span data-ttu-id="c683e-239">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c683e-239">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="c683e-240">Antworttext</span><span class="sxs-lookup"><span data-stu-id="c683e-240">Response body</span></span>

| <span data-ttu-id="c683e-241">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-241">Parameter</span></span> | <span data-ttu-id="c683e-242">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-242">Type</span></span> | <span data-ttu-id="c683e-243">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c683e-244">Gruppen</span><span class="sxs-lookup"><span data-stu-id="c683e-244">groups</span></span> | <span data-ttu-id="c683e-245">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="c683e-245">JSON Object Array</span></span> | <span data-ttu-id="c683e-246">Array von Gruppen, dass der Benutzer Zugriff auf mit der AccessToken hat.</span><span class="sxs-lookup"><span data-stu-id="c683e-246">Array of groups that the user has access to with the accessToken</span></span> |

<span data-ttu-id="c683e-247">JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:</span><span class="sxs-lookup"><span data-stu-id="c683e-247">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="c683e-248">Parameter</span><span class="sxs-lookup"><span data-stu-id="c683e-248">Parameter</span></span> | <span data-ttu-id="c683e-249">Typ</span><span class="sxs-lookup"><span data-stu-id="c683e-249">Type</span></span> | <span data-ttu-id="c683e-250">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c683e-250">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="c683e-251">groupId</span><span class="sxs-lookup"><span data-stu-id="c683e-251">groupId</span></span> | <span data-ttu-id="c683e-252">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-252">String</span></span> | <span data-ttu-id="c683e-253">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="c683e-253">Group Identifier</span></span> |
| <span data-ttu-id="c683e-254">groupName</span><span class="sxs-lookup"><span data-stu-id="c683e-254">groupName</span></span> | <span data-ttu-id="c683e-255">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-255">String</span></span> | <span data-ttu-id="c683e-256">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="c683e-256">Name of the group</span></span> |
| <span data-ttu-id="c683e-257">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="c683e-257">groupImageURL</span></span> | <span data-ttu-id="c683e-258">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-258">String</span></span> | <span data-ttu-id="c683e-259">Zeichenfolge, die die URL des Bilds Profil Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="c683e-259">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="c683e-260">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="c683e-260">hasSubGroups</span></span> | <span data-ttu-id="c683e-261">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-261">bool</span></span> | <span data-ttu-id="c683e-262">True, wenn die Gruppe Untergruppen besitzt.</span><span class="sxs-lookup"><span data-stu-id="c683e-262">True if the group has subgroups</span></span> |
| <span data-ttu-id="c683e-263">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="c683e-263">hasParentGroups</span></span> | <span data-ttu-id="c683e-264">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-264">bool</span></span> | <span data-ttu-id="c683e-265">True, wenn die Gruppe verfügt über die übergeordneten Gruppen</span><span class="sxs-lookup"><span data-stu-id="c683e-265">True if the group has parent groups</span></span> |
| <span data-ttu-id="c683e-266">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="c683e-266">isMappedToTenant</span></span> | <span data-ttu-id="c683e-267">bool</span><span class="sxs-lookup"><span data-stu-id="c683e-267">bool</span></span> | <span data-ttu-id="c683e-268">True, wenn die Gruppe Organisation Gruppe ist</span><span class="sxs-lookup"><span data-stu-id="c683e-268">True if the group is Organisation group</span></span> |
| <span data-ttu-id="c683e-269">groupType</span><span class="sxs-lookup"><span data-stu-id="c683e-269">groupType</span></span> | <span data-ttu-id="c683e-270">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c683e-270">String</span></span> | <span data-ttu-id="c683e-271">Gruppe/ConnectGroup.</span><span class="sxs-lookup"><span data-stu-id="c683e-271">Group/ConnectGroup.</span></span> <span data-ttu-id="c683e-272">ConnectGroup Wenn die Gruppe in der Gruppe Public verwaltet</span><span class="sxs-lookup"><span data-stu-id="c683e-272">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="c683e-273">userCount</span><span class="sxs-lookup"><span data-stu-id="c683e-273">userCount</span></span> | <span data-ttu-id="c683e-274">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c683e-274">Numeric</span></span> | <span data-ttu-id="c683e-275">Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie</span><span class="sxs-lookup"><span data-stu-id="c683e-275">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="c683e-276">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="c683e-276">currentLevelUserCount</span></span> | <span data-ttu-id="c683e-277">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c683e-277">Numeric</span></span> | <span data-ttu-id="c683e-278">Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="c683e-278">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="c683e-279">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="c683e-279">Sample JSON Response</span></span>

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

