---
title: /subGroups
description: Referenzartikel zur API zum Abfragen von Untergruppen Daten
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190688"
---
# <a name="subgroups"></a><span data-ttu-id="eb263-103">/subGroups</span><span class="sxs-lookup"><span data-stu-id="eb263-103">/subGroups</span></span>
<span data-ttu-id="eb263-104">API-Endpunkt für die Interaktion mit den Unterhaltungs-Untergruppen innerhalb von Kaizala.</span><span class="sxs-lookup"><span data-stu-id="eb263-104">API end-point to interact with the conversation sub-groups inside Kaizala.</span></span>

## <a name="get-subgroups"></a><span data-ttu-id="eb263-105">/SubGroups abrufen</span><span class="sxs-lookup"><span data-stu-id="eb263-105">GET /subGroups</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="eb263-106">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="eb263-106">Request Parameters</span></span>

|  | <span data-ttu-id="eb263-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-107">Parameter</span></span> | <span data-ttu-id="eb263-108">Typ</span><span class="sxs-lookup"><span data-stu-id="eb263-108">Type</span></span> | <span data-ttu-id="eb263-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="eb263-109">Optional?</span></span> | <span data-ttu-id="eb263-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb263-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="eb263-111">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="eb263-111">HTTP Header</span></span> | <span data-ttu-id="eb263-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="eb263-112">accessToken</span></span> | <span data-ttu-id="eb263-113">String</span><span class="sxs-lookup"><span data-stu-id="eb263-113">String</span></span> | <span data-ttu-id="eb263-114">Nein</span><span class="sxs-lookup"><span data-stu-id="eb263-114">No</span></span> | <span data-ttu-id="eb263-115">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="eb263-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="eb263-116">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-116">URL Path Parameter</span></span> | <span data-ttu-id="eb263-117">groupId</span><span class="sxs-lookup"><span data-stu-id="eb263-117">groupId</span></span> | <span data-ttu-id="eb263-118">String</span><span class="sxs-lookup"><span data-stu-id="eb263-118">String</span></span> | <span data-ttu-id="eb263-119">Nein</span><span class="sxs-lookup"><span data-stu-id="eb263-119">No</span></span> | <span data-ttu-id="eb263-120">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="eb263-120">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="eb263-121">URL-Abfrage Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-121">URL Query Parameter</span></span> | <span data-ttu-id="eb263-122">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="eb263-122">fetchAllGroups</span></span> | <span data-ttu-id="eb263-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="eb263-123">Boolean</span></span> | <span data-ttu-id="eb263-124">Ja</span><span class="sxs-lookup"><span data-stu-id="eb263-124">Yes</span></span> | <span data-ttu-id="eb263-125">Parameter, mit dem angegeben wird, ob alle Untergruppen in der Hierarchie abgerufen werden sollen</span><span class="sxs-lookup"><span data-stu-id="eb263-125">Parameter to specify if you would like to fetch all the subGroups across the hierarchy</span></span> |

### <a name="response-body"></a><span data-ttu-id="eb263-126">Antworttext</span><span class="sxs-lookup"><span data-stu-id="eb263-126">Response body</span></span>

| <span data-ttu-id="eb263-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-127">Parameter</span></span> | <span data-ttu-id="eb263-128">Typ</span><span class="sxs-lookup"><span data-stu-id="eb263-128">Type</span></span> | <span data-ttu-id="eb263-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb263-129">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="eb263-130">groups</span><span class="sxs-lookup"><span data-stu-id="eb263-130">groups</span></span> | <span data-ttu-id="eb263-131">JSON-Objekt Array</span><span class="sxs-lookup"><span data-stu-id="eb263-131">JSON Object Array</span></span> | <span data-ttu-id="eb263-132">Array von Gruppen mit der Liste der Untergruppen, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="eb263-132">Array of groups with the list of subGroups if any</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="eb263-133">JSON-Struktur für jede einzelne Gruppe in den Array Gruppen []:</span><span class="sxs-lookup"><span data-stu-id="eb263-133">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="eb263-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-134">Parameter</span></span> | <span data-ttu-id="eb263-135">Typ</span><span class="sxs-lookup"><span data-stu-id="eb263-135">Type</span></span> | <span data-ttu-id="eb263-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb263-136">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="eb263-137">groupId</span><span class="sxs-lookup"><span data-stu-id="eb263-137">groupId</span></span> | <span data-ttu-id="eb263-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb263-138">String</span></span> | <span data-ttu-id="eb263-139">Der Gruppe zugeordnete GUID</span><span class="sxs-lookup"><span data-stu-id="eb263-139">GUID associated with the group</span></span> |
| <span data-ttu-id="eb263-140">groupName</span><span class="sxs-lookup"><span data-stu-id="eb263-140">groupName</span></span> | <span data-ttu-id="eb263-141">String</span><span class="sxs-lookup"><span data-stu-id="eb263-141">String</span></span> | <span data-ttu-id="eb263-142">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="eb263-142">Name of the group</span></span> |
| <span data-ttu-id="eb263-143">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="eb263-143">groupImageURL</span></span> | <span data-ttu-id="eb263-144">String</span><span class="sxs-lookup"><span data-stu-id="eb263-144">String</span></span> | <span data-ttu-id="eb263-145">Zeichenfolge, die die URL des Gruppenprofil Bilds angibt</span><span class="sxs-lookup"><span data-stu-id="eb263-145">String specifying the URL of the group profile picture</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="eb263-146">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="eb263-146">Sample JSON Response</span></span>

```javascript
{
  "groups": [
    {
      "groupName": "Sample group name",
      "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
      "groupImageUrl": "{sample group image URL here}",
      "subGroups": [
          {
            "groupName": "Sample sub group name",
            "groupId": "853654b2-guid-462d-b709-0c4e43a7083f",
            "groupImageUrl": "{sample sub group image URL here}",
          }
      ]
    }
  ]
}
```

## <a name="post-subgroups"></a><span data-ttu-id="eb263-147">POST/subGroups</span><span class="sxs-lookup"><span data-stu-id="eb263-147">POST /subGroups</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="eb263-148">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="eb263-148">Request Parameters</span></span>

|  | <span data-ttu-id="eb263-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-149">Parameter</span></span> | <span data-ttu-id="eb263-150">Typ</span><span class="sxs-lookup"><span data-stu-id="eb263-150">Type</span></span> | <span data-ttu-id="eb263-151">Optional?</span><span class="sxs-lookup"><span data-stu-id="eb263-151">Optional?</span></span> | <span data-ttu-id="eb263-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb263-152">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="eb263-153">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="eb263-153">HTTP Header</span></span> | <span data-ttu-id="eb263-154">accessToken</span><span class="sxs-lookup"><span data-stu-id="eb263-154">accessToken</span></span> | <span data-ttu-id="eb263-155">String</span><span class="sxs-lookup"><span data-stu-id="eb263-155">String</span></span> | <span data-ttu-id="eb263-156">Nein</span><span class="sxs-lookup"><span data-stu-id="eb263-156">No</span></span> | <span data-ttu-id="eb263-157">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="eb263-157">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="eb263-158">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-158">URL Path Parameter</span></span> | <span data-ttu-id="eb263-159">groupId</span><span class="sxs-lookup"><span data-stu-id="eb263-159">groupId</span></span> | <span data-ttu-id="eb263-160">String</span><span class="sxs-lookup"><span data-stu-id="eb263-160">String</span></span> | <span data-ttu-id="eb263-161">Nein</span><span class="sxs-lookup"><span data-stu-id="eb263-161">No</span></span> | <span data-ttu-id="eb263-162">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="eb263-162">GUID representing the groupId of the specific group resource</span></span> |

### <a name="request-body"></a><span data-ttu-id="eb263-163">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="eb263-163">Request body</span></span>

|  | <span data-ttu-id="eb263-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-164">Parameter</span></span> | <span data-ttu-id="eb263-165">Typ</span><span class="sxs-lookup"><span data-stu-id="eb263-165">Type</span></span> | <span data-ttu-id="eb263-166">Optional?</span><span class="sxs-lookup"><span data-stu-id="eb263-166">Optional?</span></span> | <span data-ttu-id="eb263-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb263-167">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="eb263-168">groupName</span><span class="sxs-lookup"><span data-stu-id="eb263-168">groupName</span></span> | <span data-ttu-id="eb263-169">String</span><span class="sxs-lookup"><span data-stu-id="eb263-169">String</span></span> | <span data-ttu-id="eb263-170">Nein</span><span class="sxs-lookup"><span data-stu-id="eb263-170">No</span></span> | <span data-ttu-id="eb263-171">Name der Untergruppe</span><span class="sxs-lookup"><span data-stu-id="eb263-171">Name of the sub group</span></span> |
| <span data-ttu-id="eb263-172">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="eb263-172">groupImageURL</span></span> | <span data-ttu-id="eb263-173">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb263-173">String</span></span> | <span data-ttu-id="eb263-174">Ja</span><span class="sxs-lookup"><span data-stu-id="eb263-174">Yes</span></span> | <span data-ttu-id="eb263-175">Medien-URL des Gruppen Bilds; Das Bild muss über den/Media-Pfad hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="eb263-175">Media URL of the group image; Image needs to be uploaded through the /media path</span></span> |
| <span data-ttu-id="eb263-176">members</span><span class="sxs-lookup"><span data-stu-id="eb263-176">members</span></span> | <span data-ttu-id="eb263-177">Array</span><span class="sxs-lookup"><span data-stu-id="eb263-177">Array</span></span> | <span data-ttu-id="eb263-178">Ja</span><span class="sxs-lookup"><span data-stu-id="eb263-178">Yes</span></span> | <span data-ttu-id="eb263-179">Zeichenfolgenarray von formatierten Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="eb263-179">String array of well-formatted phone numbers</span></span> |
| <span data-ttu-id="eb263-180">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="eb263-180">welcomeMessage</span></span> | <span data-ttu-id="eb263-181">Array</span><span class="sxs-lookup"><span data-stu-id="eb263-181">Array</span></span> | <span data-ttu-id="eb263-182">Nein</span><span class="sxs-lookup"><span data-stu-id="eb263-182">No</span></span> | <span data-ttu-id="eb263-183">Zeichenfolgenarray von formatierten Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="eb263-183">String array of well-formatted phone numbers</span></span>  |
| <span data-ttu-id="eb263-184">addUserToGroup</span><span class="sxs-lookup"><span data-stu-id="eb263-184">addUserToGroup</span></span> | <span data-ttu-id="eb263-185">Boolean</span><span class="sxs-lookup"><span data-stu-id="eb263-185">Boolean</span></span> | <span data-ttu-id="eb263-186">Ja</span><span class="sxs-lookup"><span data-stu-id="eb263-186">Yes</span></span> | <span data-ttu-id="eb263-187">Wird auf false festgelegt, wenn der aufrufende Benutzer standardmäßig nicht der Gruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb263-187">Set to False if the calling user should not be added to the group by default</span></span>  |


#### <a name="sample-json-request"></a><span data-ttu-id="eb263-188">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="eb263-188">Sample JSON Request</span></span>

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

### <a name="response-body"></a><span data-ttu-id="eb263-189">Antworttext</span><span class="sxs-lookup"><span data-stu-id="eb263-189">Response body</span></span>

| <span data-ttu-id="eb263-190">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb263-190">Parameter</span></span> | <span data-ttu-id="eb263-191">Typ</span><span class="sxs-lookup"><span data-stu-id="eb263-191">Type</span></span> | <span data-ttu-id="eb263-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb263-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="eb263-193">groupId</span><span class="sxs-lookup"><span data-stu-id="eb263-193">groupId</span></span> | <span data-ttu-id="eb263-194">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb263-194">String</span></span> | <span data-ttu-id="eb263-195">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="eb263-195">Group Identifier</span></span> |
| <span data-ttu-id="eb263-196">groupName</span><span class="sxs-lookup"><span data-stu-id="eb263-196">groupName</span></span> | <span data-ttu-id="eb263-197">String</span><span class="sxs-lookup"><span data-stu-id="eb263-197">String</span></span> | <span data-ttu-id="eb263-198">Name der erstellten Gruppe</span><span class="sxs-lookup"><span data-stu-id="eb263-198">Name of the group created</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="eb263-199">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="eb263-199">Sample JSON Response</span></span>

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
