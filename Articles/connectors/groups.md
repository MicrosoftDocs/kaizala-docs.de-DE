---
title: /Groups
description: Referenzartikel für API zum Abfragen von Gruppendaten
topic: Reference
author: nitinjms
ms.openlocfilehash: 6a0b56d36aef458b5a3d302235499f445ed134e6
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190716"
---
# <a name="groups"></a><span data-ttu-id="f7b8b-103">/Groups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-103">/groups</span></span>
<span data-ttu-id="f7b8b-104">API-Endpunkt für die Interaktion mit den unterhaltungsgruppen in Kaizala.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-104">API end-point to interact with the conversation groups inside Kaizala.</span></span>

## <a name="post-groups"></a><span data-ttu-id="f7b8b-105">POST/Groups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-105">POST /groups</span></span>

    Post {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="f7b8b-106">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-106">Request Parameters</span></span>

|  | <span data-ttu-id="f7b8b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-107">Parameter</span></span> | <span data-ttu-id="f7b8b-108">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-108">Type</span></span> | <span data-ttu-id="f7b8b-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="f7b8b-109">Optional?</span></span> | <span data-ttu-id="f7b8b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-111">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="f7b8b-111">HTTP Header</span></span> | <span data-ttu-id="f7b8b-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="f7b8b-112">accessToken</span></span> | <span data-ttu-id="f7b8b-113">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-113">String</span></span> | <span data-ttu-id="f7b8b-114">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-114">No</span></span> | <span data-ttu-id="f7b8b-115">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="f7b8b-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="f7b8b-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="f7b8b-116">HTTP Header</span></span> | <span data-ttu-id="f7b8b-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f7b8b-117">Content-Type</span></span> | <span data-ttu-id="f7b8b-118">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-118">String</span></span> | <span data-ttu-id="f7b8b-119">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-119">No</span></span> | <span data-ttu-id="f7b8b-120">"application/json"</span><span class="sxs-lookup"><span data-stu-id="f7b8b-120">"application/json"</span></span> |

### <a name="request-body"></a><span data-ttu-id="f7b8b-121">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="f7b8b-121">Request body</span></span>

| <span data-ttu-id="f7b8b-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-122">Parameter</span></span> | <span data-ttu-id="f7b8b-123">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-123">Type</span></span> | <span data-ttu-id="f7b8b-124">Optional?</span><span class="sxs-lookup"><span data-stu-id="f7b8b-124">Optional?</span></span> | <span data-ttu-id="f7b8b-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-125">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="f7b8b-126">name</span><span class="sxs-lookup"><span data-stu-id="f7b8b-126">name</span></span> | <span data-ttu-id="f7b8b-127">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-127">String</span></span> | <span data-ttu-id="f7b8b-128">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-128">No</span></span> | <span data-ttu-id="f7b8b-129">Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-129">Group name</span></span> |
| <span data-ttu-id="f7b8b-130">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="f7b8b-130">welcomeMessage</span></span> | <span data-ttu-id="f7b8b-131">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-131">String</span></span> | <span data-ttu-id="f7b8b-132">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-132">No</span></span> | <span data-ttu-id="f7b8b-133">Willkommensnachricht, die dem neuen Gruppenmitglied angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="f7b8b-133">Welcome message which will be displayed to new group member</span></span> |
| <span data-ttu-id="f7b8b-134">members</span><span class="sxs-lookup"><span data-stu-id="f7b8b-134">members</span></span> | <span data-ttu-id="f7b8b-135">String []</span><span class="sxs-lookup"><span data-stu-id="f7b8b-135">String[]</span></span> | <span data-ttu-id="f7b8b-136">Ja</span><span class="sxs-lookup"><span data-stu-id="f7b8b-136">Yes</span></span> | <span data-ttu-id="f7b8b-137">Mobiltelefonnummer (mit Landesvorwahl) der hinzuzufügenden Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-137">Mobile number(with country code) of members to be added.</span></span> <span data-ttu-id="f7b8b-138">Standard: der Benutzer des Zugriffstokens wird als Administrator der Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-138">Default: Access token's user will be added as admin of the group</span></span> |
| <span data-ttu-id="f7b8b-139">groupType</span><span class="sxs-lookup"><span data-stu-id="f7b8b-139">groupType</span></span> | <span data-ttu-id="f7b8b-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7b8b-140">String</span></span> | <span data-ttu-id="f7b8b-141">Ja</span><span class="sxs-lookup"><span data-stu-id="f7b8b-141">Yes</span></span> | <span data-ttu-id="f7b8b-142">Enum: Group/Connectgroup.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-142">Enum: Group/ConnectGroup.</span></span> <span data-ttu-id="f7b8b-143">Connectgroup erstellt eine verwaltete öffentliche Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-143">ConnectGroup will create Managed Public group.</span></span> <span data-ttu-id="f7b8b-144">Standard: Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-144">Default: Group</span></span> |

#### <a name="sample-json-request-for-create-group"></a><span data-ttu-id="f7b8b-145">JSON-Beispielanforderung für Create Group</span><span class="sxs-lookup"><span data-stu-id="f7b8b-145">Sample JSON Request for Create Group</span></span>

```javascript
{
    name:"Kaizala Test group",
    welcomeMessage:"Welcome to group created programmatically",
    members:["+911099999999"],
    groupType: "Group"
}
```

### <a name="response-body"></a><span data-ttu-id="f7b8b-146">Antworttext</span><span class="sxs-lookup"><span data-stu-id="f7b8b-146">Response body</span></span>

| <span data-ttu-id="f7b8b-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-147">Parameter</span></span> | <span data-ttu-id="f7b8b-148">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-148">Type</span></span> | <span data-ttu-id="f7b8b-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-149">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-150">groupName</span><span class="sxs-lookup"><span data-stu-id="f7b8b-150">groupName</span></span> | <span data-ttu-id="f7b8b-151">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-151">String</span></span> | <span data-ttu-id="f7b8b-152">Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-152">Group name</span></span> |
| <span data-ttu-id="f7b8b-153">groupId</span><span class="sxs-lookup"><span data-stu-id="f7b8b-153">groupId</span></span> | <span data-ttu-id="f7b8b-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7b8b-154">String</span></span> | <span data-ttu-id="f7b8b-155">Gruppenbezeichner, der bei nachfolgenden API-Aufrufen verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="f7b8b-155">Group Identifier which can be used in subsequent api calls</span></span> |
| <span data-ttu-id="f7b8b-156">membersAdded</span><span class="sxs-lookup"><span data-stu-id="f7b8b-156">membersAdded</span></span> | <span data-ttu-id="f7b8b-157">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-157">bool</span></span> | <span data-ttu-id="f7b8b-158">True, wenn alle Elemente erfolgreich hinzugefügt werden</span><span class="sxs-lookup"><span data-stu-id="f7b8b-158">True if all members are successfully added</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="f7b8b-159">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="f7b8b-159">Sample JSON Response</span></span>

```javascript
{
   "groupName": "Kaizala Test group",
   "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
   "membersAdded": true
}
```


## <a name="get-groups"></a><span data-ttu-id="f7b8b-160">/Groups abrufen</span><span class="sxs-lookup"><span data-stu-id="f7b8b-160">GET /groups</span></span>

    GET {endpoint-url}/v1/groups

### <a name="request-parameters"></a><span data-ttu-id="f7b8b-161">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-161">Request Parameters</span></span>

|  | <span data-ttu-id="f7b8b-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-162">Parameter</span></span> | <span data-ttu-id="f7b8b-163">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-163">Type</span></span> | <span data-ttu-id="f7b8b-164">Optional?</span><span class="sxs-lookup"><span data-stu-id="f7b8b-164">Optional?</span></span> | <span data-ttu-id="f7b8b-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-166">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="f7b8b-166">HTTP Header</span></span> | <span data-ttu-id="f7b8b-167">accessToken</span><span class="sxs-lookup"><span data-stu-id="f7b8b-167">accessToken</span></span> | <span data-ttu-id="f7b8b-168">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-168">String</span></span> | <span data-ttu-id="f7b8b-169">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-169">No</span></span> | <span data-ttu-id="f7b8b-170">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="f7b8b-170">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="f7b8b-171">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-171">Query parameter</span></span> | <span data-ttu-id="f7b8b-172">showDetail</span><span class="sxs-lookup"><span data-stu-id="f7b8b-172">showDetail</span></span> | <span data-ttu-id="f7b8b-173">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-173">bool</span></span> | <span data-ttu-id="f7b8b-174">Ja</span><span class="sxs-lookup"><span data-stu-id="f7b8b-174">Yes</span></span> | <span data-ttu-id="f7b8b-175">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-175">Default: false.</span></span> <span data-ttu-id="f7b8b-176">True, um alle Gruppendetails zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="f7b8b-176">True to return all group details</span></span> |
| <span data-ttu-id="f7b8b-177">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-177">Query parameter</span></span> | <span data-ttu-id="f7b8b-178">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-178">fetchAllGroups</span></span> | <span data-ttu-id="f7b8b-179">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-179">bool</span></span> | <span data-ttu-id="f7b8b-180">Ja</span><span class="sxs-lookup"><span data-stu-id="f7b8b-180">Yes</span></span> | <span data-ttu-id="f7b8b-181">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-181">Default: false.</span></span> <span data-ttu-id="f7b8b-182">True, um alle über-und Untergruppen zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="f7b8b-182">True to return all parent and sub groups</span></span> |

### <a name="response-body"></a><span data-ttu-id="f7b8b-183">Antworttext</span><span class="sxs-lookup"><span data-stu-id="f7b8b-183">Response body</span></span>

| <span data-ttu-id="f7b8b-184">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-184">Parameter</span></span> | <span data-ttu-id="f7b8b-185">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-185">Type</span></span> | <span data-ttu-id="f7b8b-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-186">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-187">groups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-187">groups</span></span> | <span data-ttu-id="f7b8b-188">JSON-Objekt Array</span><span class="sxs-lookup"><span data-stu-id="f7b8b-188">JSON Object Array</span></span> | <span data-ttu-id="f7b8b-189">Array von Gruppen, auf die der Benutzer mit der Access Token zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="f7b8b-189">Array of groups that the user has access to with the accessToken</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="f7b8b-190">JSON-Struktur für jede einzelne Gruppe in den Array Gruppen []:</span><span class="sxs-lookup"><span data-stu-id="f7b8b-190">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="f7b8b-191">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-191">Parameter</span></span> | <span data-ttu-id="f7b8b-192">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-192">Type</span></span> | <span data-ttu-id="f7b8b-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-193">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-194">groupId</span><span class="sxs-lookup"><span data-stu-id="f7b8b-194">groupId</span></span> | <span data-ttu-id="f7b8b-195">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7b8b-195">String</span></span> | <span data-ttu-id="f7b8b-196">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="f7b8b-196">Group Identifier</span></span> |
| <span data-ttu-id="f7b8b-197">groupName</span><span class="sxs-lookup"><span data-stu-id="f7b8b-197">groupName</span></span> | <span data-ttu-id="f7b8b-198">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-198">String</span></span> | <span data-ttu-id="f7b8b-199">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-199">Name of the group</span></span> |
| <span data-ttu-id="f7b8b-200">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="f7b8b-200">groupImageURL</span></span> | <span data-ttu-id="f7b8b-201">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-201">String</span></span> | <span data-ttu-id="f7b8b-202">Zeichenfolge, die die URL des Gruppenprofil Bilds angibt</span><span class="sxs-lookup"><span data-stu-id="f7b8b-202">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="f7b8b-203">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-203">hasSubGroups</span></span> | <span data-ttu-id="f7b8b-204">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-204">bool</span></span> | <span data-ttu-id="f7b8b-205">True, wenn die Gruppe Untergruppen hat</span><span class="sxs-lookup"><span data-stu-id="f7b8b-205">True if the group has subgroups</span></span> |
| <span data-ttu-id="f7b8b-206">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-206">hasParentGroups</span></span> | <span data-ttu-id="f7b8b-207">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-207">bool</span></span> | <span data-ttu-id="f7b8b-208">True, wenn die Gruppe übergeordnete Gruppen hat</span><span class="sxs-lookup"><span data-stu-id="f7b8b-208">True if the group has parent groups</span></span> |
| <span data-ttu-id="f7b8b-209">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="f7b8b-209">isMappedToTenant</span></span> | <span data-ttu-id="f7b8b-210">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-210">bool</span></span> | <span data-ttu-id="f7b8b-211">True, wenn die Gruppe Organisationsgruppe ist</span><span class="sxs-lookup"><span data-stu-id="f7b8b-211">True if the group is Organisation group</span></span> |
| <span data-ttu-id="f7b8b-212">groupType</span><span class="sxs-lookup"><span data-stu-id="f7b8b-212">groupType</span></span> | <span data-ttu-id="f7b8b-213">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-213">String</span></span> | <span data-ttu-id="f7b8b-214">Group/Connectgroup.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-214">Group/ConnectGroup.</span></span> <span data-ttu-id="f7b8b-215">Connectgroup wenn die Gruppe in verwalteter öffentlicher Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-215">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="f7b8b-216">userCount</span><span class="sxs-lookup"><span data-stu-id="f7b8b-216">userCount</span></span> | <span data-ttu-id="f7b8b-217">Numeric</span><span class="sxs-lookup"><span data-stu-id="f7b8b-217">Numeric</span></span> | <span data-ttu-id="f7b8b-218">Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie</span><span class="sxs-lookup"><span data-stu-id="f7b8b-218">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="f7b8b-219">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="f7b8b-219">currentLevelUserCount</span></span> | <span data-ttu-id="f7b8b-220">Numeric</span><span class="sxs-lookup"><span data-stu-id="f7b8b-220">Numeric</span></span> | <span data-ttu-id="f7b8b-221">Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="f7b8b-221">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="f7b8b-222">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="f7b8b-222">Sample JSON Response</span></span>

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

## <a name="get-groupsgroupid"></a><span data-ttu-id="f7b8b-223">/Groups/{groupId} abrufen</span><span class="sxs-lookup"><span data-stu-id="f7b8b-223">GET /groups/{groupId}</span></span>

<span data-ttu-id="f7b8b-224">Sie können Details zu einem bestimmten Resource-Element (eine Gruppe hier) abrufen, indem Sie den Bezeichner als URL-Pfadparameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-224">You can get details about a specific resource member (a group here) by specifying the identifier as a URL path parameter</span></span>

    GET {endpoint-url}/groups/{groupId}

### <a name="request-parameters"></a><span data-ttu-id="f7b8b-225">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-225">Request Parameters</span></span>

|  | <span data-ttu-id="f7b8b-226">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-226">Parameter</span></span> | <span data-ttu-id="f7b8b-227">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-227">Type</span></span> | <span data-ttu-id="f7b8b-228">Optional?</span><span class="sxs-lookup"><span data-stu-id="f7b8b-228">Optional?</span></span> | <span data-ttu-id="f7b8b-229">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-229">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-230">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-230">URL Path Parameter</span></span> | <span data-ttu-id="f7b8b-231">groupId</span><span class="sxs-lookup"><span data-stu-id="f7b8b-231">groupId</span></span> | <span data-ttu-id="f7b8b-232">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-232">String</span></span> | <span data-ttu-id="f7b8b-233">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-233">No</span></span> | <span data-ttu-id="f7b8b-234">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="f7b8b-234">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="f7b8b-235">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="f7b8b-235">HTTP Header</span></span> | <span data-ttu-id="f7b8b-236">accessToken</span><span class="sxs-lookup"><span data-stu-id="f7b8b-236">accessToken</span></span> | <span data-ttu-id="f7b8b-237">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-237">String</span></span> | <span data-ttu-id="f7b8b-238">Nein</span><span class="sxs-lookup"><span data-stu-id="f7b8b-238">No</span></span> | <span data-ttu-id="f7b8b-239">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="f7b8b-239">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="f7b8b-240">Antworttext</span><span class="sxs-lookup"><span data-stu-id="f7b8b-240">Response body</span></span>

| <span data-ttu-id="f7b8b-241">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-241">Parameter</span></span> | <span data-ttu-id="f7b8b-242">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-242">Type</span></span> | <span data-ttu-id="f7b8b-243">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-243">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-244">groups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-244">groups</span></span> | <span data-ttu-id="f7b8b-245">JSON-Objekt Array</span><span class="sxs-lookup"><span data-stu-id="f7b8b-245">JSON Object Array</span></span> | <span data-ttu-id="f7b8b-246">Array von Gruppen, auf die der Benutzer mit der Access Token zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="f7b8b-246">Array of groups that the user has access to with the accessToken</span></span> |

<span data-ttu-id="f7b8b-247">JSON-Struktur für jede einzelne Gruppe in den Array Gruppen []:</span><span class="sxs-lookup"><span data-stu-id="f7b8b-247">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="f7b8b-248">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b8b-248">Parameter</span></span> | <span data-ttu-id="f7b8b-249">Typ</span><span class="sxs-lookup"><span data-stu-id="f7b8b-249">Type</span></span> | <span data-ttu-id="f7b8b-250">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7b8b-250">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="f7b8b-251">groupId</span><span class="sxs-lookup"><span data-stu-id="f7b8b-251">groupId</span></span> | <span data-ttu-id="f7b8b-252">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7b8b-252">String</span></span> | <span data-ttu-id="f7b8b-253">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="f7b8b-253">Group Identifier</span></span> |
| <span data-ttu-id="f7b8b-254">groupName</span><span class="sxs-lookup"><span data-stu-id="f7b8b-254">groupName</span></span> | <span data-ttu-id="f7b8b-255">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-255">String</span></span> | <span data-ttu-id="f7b8b-256">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-256">Name of the group</span></span> |
| <span data-ttu-id="f7b8b-257">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="f7b8b-257">groupImageURL</span></span> | <span data-ttu-id="f7b8b-258">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-258">String</span></span> | <span data-ttu-id="f7b8b-259">Zeichenfolge, die die URL des Gruppenprofil Bilds angibt</span><span class="sxs-lookup"><span data-stu-id="f7b8b-259">String specifying the URL of the group profile picture</span></span> |
| <span data-ttu-id="f7b8b-260">hasSubGroups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-260">hasSubGroups</span></span> | <span data-ttu-id="f7b8b-261">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-261">bool</span></span> | <span data-ttu-id="f7b8b-262">True, wenn die Gruppe Untergruppen hat</span><span class="sxs-lookup"><span data-stu-id="f7b8b-262">True if the group has subgroups</span></span> |
| <span data-ttu-id="f7b8b-263">hasParentGroups</span><span class="sxs-lookup"><span data-stu-id="f7b8b-263">hasParentGroups</span></span> | <span data-ttu-id="f7b8b-264">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-264">bool</span></span> | <span data-ttu-id="f7b8b-265">True, wenn die Gruppe übergeordnete Gruppen hat</span><span class="sxs-lookup"><span data-stu-id="f7b8b-265">True if the group has parent groups</span></span> |
| <span data-ttu-id="f7b8b-266">isMappedToTenant</span><span class="sxs-lookup"><span data-stu-id="f7b8b-266">isMappedToTenant</span></span> | <span data-ttu-id="f7b8b-267">bool</span><span class="sxs-lookup"><span data-stu-id="f7b8b-267">bool</span></span> | <span data-ttu-id="f7b8b-268">True, wenn die Gruppe Organisationsgruppe ist</span><span class="sxs-lookup"><span data-stu-id="f7b8b-268">True if the group is Organisation group</span></span> |
| <span data-ttu-id="f7b8b-269">groupType</span><span class="sxs-lookup"><span data-stu-id="f7b8b-269">groupType</span></span> | <span data-ttu-id="f7b8b-270">String</span><span class="sxs-lookup"><span data-stu-id="f7b8b-270">String</span></span> | <span data-ttu-id="f7b8b-271">Group/Connectgroup.</span><span class="sxs-lookup"><span data-stu-id="f7b8b-271">Group/ConnectGroup.</span></span> <span data-ttu-id="f7b8b-272">Connectgroup wenn die Gruppe in verwalteter öffentlicher Gruppe</span><span class="sxs-lookup"><span data-stu-id="f7b8b-272">ConnectGroup if the group in Managed Public group</span></span> |
| <span data-ttu-id="f7b8b-273">userCount</span><span class="sxs-lookup"><span data-stu-id="f7b8b-273">userCount</span></span> | <span data-ttu-id="f7b8b-274">Numeric</span><span class="sxs-lookup"><span data-stu-id="f7b8b-274">Numeric</span></span> | <span data-ttu-id="f7b8b-275">Gesamtzahl der Benutzer unter dieser Gruppe in der Hierarchie</span><span class="sxs-lookup"><span data-stu-id="f7b8b-275">Total number of users under this group across the hierarchy</span></span> |
| <span data-ttu-id="f7b8b-276">currentLevelUserCount</span><span class="sxs-lookup"><span data-stu-id="f7b8b-276">currentLevelUserCount</span></span> | <span data-ttu-id="f7b8b-277">Numeric</span><span class="sxs-lookup"><span data-stu-id="f7b8b-277">Numeric</span></span> | <span data-ttu-id="f7b8b-278">Gesamtzahl der einzelnen Mitglieder der Gruppe auf der aktuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="f7b8b-278">Total number of individual members of the group at the current level</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="f7b8b-279">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="f7b8b-279">Sample JSON Response</span></span>

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

