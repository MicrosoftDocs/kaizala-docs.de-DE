---
title: /subGroups
description: Referenzartikel für Abfragen Untergruppe von Daten-API
topic: Reference
author: nitinjms
ms.openlocfilehash: 1f6d013b4d6657eaaaadb9fe3244c2d9383e56f6
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905328"
---
# <a name="apis-to-query-subgroups-within-a-group"></a><span data-ttu-id="d9457-103">APIs für die Abfrage Untergruppen innerhalb einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="d9457-103">APIs to query subgroups within a group</span></span>
## <a name="subgroups"></a><span data-ttu-id="d9457-104">/subGroups</span><span class="sxs-lookup"><span data-stu-id="d9457-104">/subGroups</span></span>
<span data-ttu-id="d9457-105">API-Endpunkt zur Interaktion mit der Unterhaltung Unterseite innerhalb Kaizala gruppiert.</span><span class="sxs-lookup"><span data-stu-id="d9457-105">API end-point to interact with the conversation sub-groups inside Kaizala.</span></span>

### <a name="get-subgroups"></a><span data-ttu-id="d9457-106">Abrufen von /subGroups</span><span class="sxs-lookup"><span data-stu-id="d9457-106">GET /subGroups</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a><span data-ttu-id="d9457-107">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="d9457-107">Request Parameters</span></span>

|  | <span data-ttu-id="d9457-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-108">Parameter</span></span> | <span data-ttu-id="d9457-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d9457-109">Type</span></span> | <span data-ttu-id="d9457-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="d9457-110">Optional?</span></span> | <span data-ttu-id="d9457-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9457-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="d9457-112">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="d9457-112">HTTP Header</span></span> | <span data-ttu-id="d9457-113">accessToken</span><span class="sxs-lookup"><span data-stu-id="d9457-113">accessToken</span></span> | <span data-ttu-id="d9457-114">String</span><span class="sxs-lookup"><span data-stu-id="d9457-114">String</span></span> | <span data-ttu-id="d9457-115">Nein</span><span class="sxs-lookup"><span data-stu-id="d9457-115">No</span></span> | <span data-ttu-id="d9457-116">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="d9457-116">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="d9457-117">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-117">URL Path Parameter</span></span> | <span data-ttu-id="d9457-118">groupId</span><span class="sxs-lookup"><span data-stu-id="d9457-118">groupId</span></span> | <span data-ttu-id="d9457-119">String</span><span class="sxs-lookup"><span data-stu-id="d9457-119">String</span></span> | <span data-ttu-id="d9457-120">Nein</span><span class="sxs-lookup"><span data-stu-id="d9457-120">No</span></span> | <span data-ttu-id="d9457-121">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9457-121">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="d9457-122">URL-Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="d9457-122">URL Query Parameter</span></span> | <span data-ttu-id="d9457-123">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="d9457-123">fetchAllGroups</span></span> | <span data-ttu-id="d9457-124">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9457-124">Boolean</span></span> | <span data-ttu-id="d9457-125">Ja</span><span class="sxs-lookup"><span data-stu-id="d9457-125">Yes</span></span> | <span data-ttu-id="d9457-126">Parameter, um anzugeben, wenn alle Untergruppen in der Hierarchie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9457-126">Parameter to specify if you would like to fetch all the subGroups across the hierarchy</span></span> |

##### <a name="response-body"></a><span data-ttu-id="d9457-127">Antworttext</span><span class="sxs-lookup"><span data-stu-id="d9457-127">Response body</span></span>

| <span data-ttu-id="d9457-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-128">Parameter</span></span> | <span data-ttu-id="d9457-129">Typ</span><span class="sxs-lookup"><span data-stu-id="d9457-129">Type</span></span> | <span data-ttu-id="d9457-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9457-130">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d9457-131">Gruppen</span><span class="sxs-lookup"><span data-stu-id="d9457-131">groups</span></span> | <span data-ttu-id="d9457-132">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="d9457-132">JSON Object Array</span></span> | <span data-ttu-id="d9457-133">Array von Gruppen mit der Liste der Untergruppen, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="d9457-133">Array of groups with the list of subGroups if any</span></span> |

######  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="d9457-134">JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:</span><span class="sxs-lookup"><span data-stu-id="d9457-134">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="d9457-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-135">Parameter</span></span> | <span data-ttu-id="d9457-136">Typ</span><span class="sxs-lookup"><span data-stu-id="d9457-136">Type</span></span> | <span data-ttu-id="d9457-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9457-137">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d9457-138">groupId</span><span class="sxs-lookup"><span data-stu-id="d9457-138">groupId</span></span> | <span data-ttu-id="d9457-139">String</span><span class="sxs-lookup"><span data-stu-id="d9457-139">String</span></span> | <span data-ttu-id="d9457-140">GUID der Gruppe zugeordnete</span><span class="sxs-lookup"><span data-stu-id="d9457-140">GUID associated with the group</span></span> |
| <span data-ttu-id="d9457-141">groupName</span><span class="sxs-lookup"><span data-stu-id="d9457-141">groupName</span></span> | <span data-ttu-id="d9457-142">String</span><span class="sxs-lookup"><span data-stu-id="d9457-142">String</span></span> | <span data-ttu-id="d9457-143">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="d9457-143">Name of the group</span></span> |
| <span data-ttu-id="d9457-144">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="d9457-144">groupImageURL</span></span> | <span data-ttu-id="d9457-145">String</span><span class="sxs-lookup"><span data-stu-id="d9457-145">String</span></span> | <span data-ttu-id="d9457-146">Zeichenfolge, die die URL des Bilds Profil Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="d9457-146">String specifying the URL of the group profile picture</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="d9457-147">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="d9457-147">Sample JSON Response</span></span>

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

### <a name="post-subgroups"></a><span data-ttu-id="d9457-148">POST-/subGroups</span><span class="sxs-lookup"><span data-stu-id="d9457-148">POST /subGroups</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

##### <a name="request-parameters"></a><span data-ttu-id="d9457-149">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="d9457-149">Request Parameters</span></span>

|  | <span data-ttu-id="d9457-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-150">Parameter</span></span> | <span data-ttu-id="d9457-151">Typ</span><span class="sxs-lookup"><span data-stu-id="d9457-151">Type</span></span> | <span data-ttu-id="d9457-152">Optional?</span><span class="sxs-lookup"><span data-stu-id="d9457-152">Optional?</span></span> | <span data-ttu-id="d9457-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9457-153">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="d9457-154">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="d9457-154">HTTP Header</span></span> | <span data-ttu-id="d9457-155">accessToken</span><span class="sxs-lookup"><span data-stu-id="d9457-155">accessToken</span></span> | <span data-ttu-id="d9457-156">String</span><span class="sxs-lookup"><span data-stu-id="d9457-156">String</span></span> | <span data-ttu-id="d9457-157">Nein</span><span class="sxs-lookup"><span data-stu-id="d9457-157">No</span></span> | <span data-ttu-id="d9457-158">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="d9457-158">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="d9457-159">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-159">URL Path Parameter</span></span> | <span data-ttu-id="d9457-160">groupId</span><span class="sxs-lookup"><span data-stu-id="d9457-160">groupId</span></span> | <span data-ttu-id="d9457-161">String</span><span class="sxs-lookup"><span data-stu-id="d9457-161">String</span></span> | <span data-ttu-id="d9457-162">Nein</span><span class="sxs-lookup"><span data-stu-id="d9457-162">No</span></span> | <span data-ttu-id="d9457-163">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9457-163">GUID representing the groupId of the specific group resource</span></span> |

##### <a name="request-body"></a><span data-ttu-id="d9457-164">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="d9457-164">Request body</span></span>

|  | <span data-ttu-id="d9457-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-165">Parameter</span></span> | <span data-ttu-id="d9457-166">Typ</span><span class="sxs-lookup"><span data-stu-id="d9457-166">Type</span></span> | <span data-ttu-id="d9457-167">Optional?</span><span class="sxs-lookup"><span data-stu-id="d9457-167">Optional?</span></span> | <span data-ttu-id="d9457-168">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9457-168">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="d9457-169">groupName</span><span class="sxs-lookup"><span data-stu-id="d9457-169">groupName</span></span> | <span data-ttu-id="d9457-170">String</span><span class="sxs-lookup"><span data-stu-id="d9457-170">String</span></span> | <span data-ttu-id="d9457-171">Nein</span><span class="sxs-lookup"><span data-stu-id="d9457-171">No</span></span> | <span data-ttu-id="d9457-172">Der Name der Gruppe "Sub"</span><span class="sxs-lookup"><span data-stu-id="d9457-172">Name of the sub group</span></span> |
| <span data-ttu-id="d9457-173">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="d9457-173">groupImageURL</span></span> | <span data-ttu-id="d9457-174">String</span><span class="sxs-lookup"><span data-stu-id="d9457-174">String</span></span> | <span data-ttu-id="d9457-175">Ja</span><span class="sxs-lookup"><span data-stu-id="d9457-175">Yes</span></span> | <span data-ttu-id="d9457-176">Media-URL des Bilds Gruppe; Bild muss durch den Pfad /media hochgeladen werden</span><span class="sxs-lookup"><span data-stu-id="d9457-176">Media URL of the group image; Image needs to be uploaded through the /media path</span></span> |
| <span data-ttu-id="d9457-177">Elemente</span><span class="sxs-lookup"><span data-stu-id="d9457-177">members</span></span> | <span data-ttu-id="d9457-178">Array</span><span class="sxs-lookup"><span data-stu-id="d9457-178">Array</span></span> | <span data-ttu-id="d9457-179">Ja</span><span class="sxs-lookup"><span data-stu-id="d9457-179">Yes</span></span> | <span data-ttu-id="d9457-180">Zeichenfolgenarray gut formatierte Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="d9457-180">String array of well-formatted phone numbers</span></span> |
| <span data-ttu-id="d9457-181">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="d9457-181">welcomeMessage</span></span> | <span data-ttu-id="d9457-182">Array</span><span class="sxs-lookup"><span data-stu-id="d9457-182">Array</span></span> | <span data-ttu-id="d9457-183">Nein</span><span class="sxs-lookup"><span data-stu-id="d9457-183">No</span></span> | <span data-ttu-id="d9457-184">Zeichenfolgenarray gut formatierte Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="d9457-184">String array of well-formatted phone numbers</span></span>  |
| <span data-ttu-id="d9457-185">addUserToGroup</span><span class="sxs-lookup"><span data-stu-id="d9457-185">addUserToGroup</span></span> | <span data-ttu-id="d9457-186">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9457-186">Boolean</span></span> | <span data-ttu-id="d9457-187">Ja</span><span class="sxs-lookup"><span data-stu-id="d9457-187">Yes</span></span> | <span data-ttu-id="d9457-188">Auf False festgelegt, wenn der Benutzer standardmäßig nicht der Gruppe hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="d9457-188">Set to False if the calling user should not be added to the group by default</span></span>  |


###### <a name="sample-json-request"></a><span data-ttu-id="d9457-189">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9457-189">Sample JSON Request</span></span>

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

##### <a name="response-body"></a><span data-ttu-id="d9457-190">Antworttext</span><span class="sxs-lookup"><span data-stu-id="d9457-190">Response body</span></span>

| <span data-ttu-id="d9457-191">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9457-191">Parameter</span></span> | <span data-ttu-id="d9457-192">Typ</span><span class="sxs-lookup"><span data-stu-id="d9457-192">Type</span></span> | <span data-ttu-id="d9457-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9457-193">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="d9457-194">groupId</span><span class="sxs-lookup"><span data-stu-id="d9457-194">groupId</span></span> | <span data-ttu-id="d9457-195">String</span><span class="sxs-lookup"><span data-stu-id="d9457-195">String</span></span> | <span data-ttu-id="d9457-196">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="d9457-196">Group Identifier</span></span> |
| <span data-ttu-id="d9457-197">groupName</span><span class="sxs-lookup"><span data-stu-id="d9457-197">groupName</span></span> | <span data-ttu-id="d9457-198">String</span><span class="sxs-lookup"><span data-stu-id="d9457-198">String</span></span> | <span data-ttu-id="d9457-199">Name der Gruppe erstellt</span><span class="sxs-lookup"><span data-stu-id="d9457-199">Name of the group created</span></span> |


###### <a name="sample-json-response"></a><span data-ttu-id="d9457-200">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="d9457-200">Sample JSON Response</span></span>

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
