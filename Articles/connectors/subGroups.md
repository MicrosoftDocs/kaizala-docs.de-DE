---
title: /subGroups
description: Referenzartikel für Abfragen Untergruppe von Daten-API
topic: Reference
author: nitinjms
ms.openlocfilehash: 195088d1eb665498407224b89c63521c24a5c63a
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399367"
---
# <a name="subgroups"></a><span data-ttu-id="11c9a-103">/subGroups</span><span class="sxs-lookup"><span data-stu-id="11c9a-103">/subGroups</span></span>
<span data-ttu-id="11c9a-104">API-Endpunkt zur Interaktion mit der Unterhaltung Unterseite innerhalb Kaizala gruppiert.</span><span class="sxs-lookup"><span data-stu-id="11c9a-104">API end-point to interact with the conversation sub-groups inside Kaizala.</span></span>

## <a name="get-subgroups"></a><span data-ttu-id="11c9a-105">Abrufen von /subGroups</span><span class="sxs-lookup"><span data-stu-id="11c9a-105">GET /subGroups</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="11c9a-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-106">Request Parameters</span></span>

|  | <span data-ttu-id="11c9a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-107">Parameter</span></span> | <span data-ttu-id="11c9a-108">Typ</span><span class="sxs-lookup"><span data-stu-id="11c9a-108">Type</span></span> | <span data-ttu-id="11c9a-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="11c9a-109">Optional?</span></span> | <span data-ttu-id="11c9a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11c9a-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="11c9a-111">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="11c9a-111">HTTP Header</span></span> | <span data-ttu-id="11c9a-112">accessToken</span><span class="sxs-lookup"><span data-stu-id="11c9a-112">accessToken</span></span> | <span data-ttu-id="11c9a-113">String</span><span class="sxs-lookup"><span data-stu-id="11c9a-113">String</span></span> | <span data-ttu-id="11c9a-114">Nein</span><span class="sxs-lookup"><span data-stu-id="11c9a-114">No</span></span> | <span data-ttu-id="11c9a-115">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="11c9a-115">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="11c9a-116">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-116">URL Path Parameter</span></span> | <span data-ttu-id="11c9a-117">groupId</span><span class="sxs-lookup"><span data-stu-id="11c9a-117">groupId</span></span> | <span data-ttu-id="11c9a-118">String</span><span class="sxs-lookup"><span data-stu-id="11c9a-118">String</span></span> | <span data-ttu-id="11c9a-119">Nein</span><span class="sxs-lookup"><span data-stu-id="11c9a-119">No</span></span> | <span data-ttu-id="11c9a-120">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="11c9a-120">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="11c9a-121">URL-Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-121">URL Query Parameter</span></span> | <span data-ttu-id="11c9a-122">fetchAllGroups</span><span class="sxs-lookup"><span data-stu-id="11c9a-122">fetchAllGroups</span></span> | <span data-ttu-id="11c9a-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="11c9a-123">Boolean</span></span> | <span data-ttu-id="11c9a-124">Ja</span><span class="sxs-lookup"><span data-stu-id="11c9a-124">Yes</span></span> | <span data-ttu-id="11c9a-125">Parameter, um anzugeben, wenn alle Untergruppen in der Hierarchie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="11c9a-125">Parameter to specify if you would like to fetch all the subGroups across the hierarchy</span></span> |

### <a name="response-body"></a><span data-ttu-id="11c9a-126">Antworttext</span><span class="sxs-lookup"><span data-stu-id="11c9a-126">Response body</span></span>

| <span data-ttu-id="11c9a-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-127">Parameter</span></span> | <span data-ttu-id="11c9a-128">Typ</span><span class="sxs-lookup"><span data-stu-id="11c9a-128">Type</span></span> | <span data-ttu-id="11c9a-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11c9a-129">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="11c9a-130">Gruppen</span><span class="sxs-lookup"><span data-stu-id="11c9a-130">groups</span></span> | <span data-ttu-id="11c9a-131">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="11c9a-131">JSON Object Array</span></span> | <span data-ttu-id="11c9a-132">Array von Gruppen mit der Liste der Untergruppen, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="11c9a-132">Array of groups with the list of subGroups if any</span></span> |

####  <a name="json-structure-for-each-individual-group-in-the-array-groups"></a><span data-ttu-id="11c9a-133">JSON-Struktur für jede einzelne Gruppe im Array gruppiert []:</span><span class="sxs-lookup"><span data-stu-id="11c9a-133">JSON structure for each individual group in the array groups[]:</span></span>

| <span data-ttu-id="11c9a-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-134">Parameter</span></span> | <span data-ttu-id="11c9a-135">Typ</span><span class="sxs-lookup"><span data-stu-id="11c9a-135">Type</span></span> | <span data-ttu-id="11c9a-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11c9a-136">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="11c9a-137">groupId</span><span class="sxs-lookup"><span data-stu-id="11c9a-137">groupId</span></span> | <span data-ttu-id="11c9a-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11c9a-138">String</span></span> | <span data-ttu-id="11c9a-139">GUID der Gruppe zugeordnete</span><span class="sxs-lookup"><span data-stu-id="11c9a-139">GUID associated with the group</span></span> |
| <span data-ttu-id="11c9a-140">groupName</span><span class="sxs-lookup"><span data-stu-id="11c9a-140">groupName</span></span> | <span data-ttu-id="11c9a-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11c9a-141">String</span></span> | <span data-ttu-id="11c9a-142">Der Name der Gruppe</span><span class="sxs-lookup"><span data-stu-id="11c9a-142">Name of the group</span></span> |
| <span data-ttu-id="11c9a-143">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="11c9a-143">groupImageURL</span></span> | <span data-ttu-id="11c9a-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11c9a-144">String</span></span> | <span data-ttu-id="11c9a-145">Zeichenfolge, die die URL des Bilds Profil Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="11c9a-145">String specifying the URL of the group profile picture</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="11c9a-146">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="11c9a-146">Sample JSON Response</span></span>

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

## <a name="post-subgroups"></a><span data-ttu-id="11c9a-147">POST-/subGroups</span><span class="sxs-lookup"><span data-stu-id="11c9a-147">POST /subGroups</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/subGroups

### <a name="request-parameters"></a><span data-ttu-id="11c9a-148">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-148">Request Parameters</span></span>

|  | <span data-ttu-id="11c9a-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-149">Parameter</span></span> | <span data-ttu-id="11c9a-150">Typ</span><span class="sxs-lookup"><span data-stu-id="11c9a-150">Type</span></span> | <span data-ttu-id="11c9a-151">Optional?</span><span class="sxs-lookup"><span data-stu-id="11c9a-151">Optional?</span></span> | <span data-ttu-id="11c9a-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11c9a-152">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="11c9a-153">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="11c9a-153">HTTP Header</span></span> | <span data-ttu-id="11c9a-154">accessToken</span><span class="sxs-lookup"><span data-stu-id="11c9a-154">accessToken</span></span> | <span data-ttu-id="11c9a-155">String</span><span class="sxs-lookup"><span data-stu-id="11c9a-155">String</span></span> | <span data-ttu-id="11c9a-156">Nein</span><span class="sxs-lookup"><span data-stu-id="11c9a-156">No</span></span> | <span data-ttu-id="11c9a-157">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="11c9a-157">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="11c9a-158">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-158">URL Path Parameter</span></span> | <span data-ttu-id="11c9a-159">groupId</span><span class="sxs-lookup"><span data-stu-id="11c9a-159">groupId</span></span> | <span data-ttu-id="11c9a-160">String</span><span class="sxs-lookup"><span data-stu-id="11c9a-160">String</span></span> | <span data-ttu-id="11c9a-161">Nein</span><span class="sxs-lookup"><span data-stu-id="11c9a-161">No</span></span> | <span data-ttu-id="11c9a-162">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="11c9a-162">GUID representing the groupId of the specific group resource</span></span> |

### <a name="request-body"></a><span data-ttu-id="11c9a-163">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="11c9a-163">Request body</span></span>

|  | <span data-ttu-id="11c9a-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-164">Parameter</span></span> | <span data-ttu-id="11c9a-165">Typ</span><span class="sxs-lookup"><span data-stu-id="11c9a-165">Type</span></span> | <span data-ttu-id="11c9a-166">Optional?</span><span class="sxs-lookup"><span data-stu-id="11c9a-166">Optional?</span></span> | <span data-ttu-id="11c9a-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11c9a-167">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="11c9a-168">groupName</span><span class="sxs-lookup"><span data-stu-id="11c9a-168">groupName</span></span> | <span data-ttu-id="11c9a-169">String</span><span class="sxs-lookup"><span data-stu-id="11c9a-169">String</span></span> | <span data-ttu-id="11c9a-170">Nein</span><span class="sxs-lookup"><span data-stu-id="11c9a-170">No</span></span> | <span data-ttu-id="11c9a-171">Der Name der Gruppe "Sub"</span><span class="sxs-lookup"><span data-stu-id="11c9a-171">Name of the sub group</span></span> |
| <span data-ttu-id="11c9a-172">groupImageURL</span><span class="sxs-lookup"><span data-stu-id="11c9a-172">groupImageURL</span></span> | <span data-ttu-id="11c9a-173">String</span><span class="sxs-lookup"><span data-stu-id="11c9a-173">String</span></span> | <span data-ttu-id="11c9a-174">Ja</span><span class="sxs-lookup"><span data-stu-id="11c9a-174">Yes</span></span> | <span data-ttu-id="11c9a-175">Media-URL des Bilds Gruppe; Bild muss durch den Pfad /media hochgeladen werden</span><span class="sxs-lookup"><span data-stu-id="11c9a-175">Media URL of the group image; Image needs to be uploaded through the /media path</span></span> |
| <span data-ttu-id="11c9a-176">Elemente</span><span class="sxs-lookup"><span data-stu-id="11c9a-176">members</span></span> | <span data-ttu-id="11c9a-177">Array</span><span class="sxs-lookup"><span data-stu-id="11c9a-177">Array</span></span> | <span data-ttu-id="11c9a-178">Ja</span><span class="sxs-lookup"><span data-stu-id="11c9a-178">Yes</span></span> | <span data-ttu-id="11c9a-179">Zeichenfolgenarray gut formatierte Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="11c9a-179">String array of well-formatted phone numbers</span></span> |
| <span data-ttu-id="11c9a-180">welcomeMessage</span><span class="sxs-lookup"><span data-stu-id="11c9a-180">welcomeMessage</span></span> | <span data-ttu-id="11c9a-181">Array</span><span class="sxs-lookup"><span data-stu-id="11c9a-181">Array</span></span> | <span data-ttu-id="11c9a-182">Nein</span><span class="sxs-lookup"><span data-stu-id="11c9a-182">No</span></span> | <span data-ttu-id="11c9a-183">Zeichenfolgenarray gut formatierte Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="11c9a-183">String array of well-formatted phone numbers</span></span>  |
| <span data-ttu-id="11c9a-184">addUserToGroup</span><span class="sxs-lookup"><span data-stu-id="11c9a-184">addUserToGroup</span></span> | <span data-ttu-id="11c9a-185">Boolean</span><span class="sxs-lookup"><span data-stu-id="11c9a-185">Boolean</span></span> | <span data-ttu-id="11c9a-186">Ja</span><span class="sxs-lookup"><span data-stu-id="11c9a-186">Yes</span></span> | <span data-ttu-id="11c9a-187">Auf False festgelegt, wenn der Benutzer standardmäßig nicht der Gruppe hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="11c9a-187">Set to False if the calling user should not be added to the group by default</span></span>  |


#### <a name="sample-json-request"></a><span data-ttu-id="11c9a-188">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="11c9a-188">Sample JSON Request</span></span>

```javascript
{
  "groupName": "Test Group",
  "groupImageUrl": "",
  "members": [ "+919652000000", "+919910000005"],
  "welcomeMessage": "Hello",
  "addUserToGroup": false
}
```

### <a name="response-body"></a><span data-ttu-id="11c9a-189">Antworttext</span><span class="sxs-lookup"><span data-stu-id="11c9a-189">Response body</span></span>

| <span data-ttu-id="11c9a-190">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c9a-190">Parameter</span></span> | <span data-ttu-id="11c9a-191">Typ</span><span class="sxs-lookup"><span data-stu-id="11c9a-191">Type</span></span> | <span data-ttu-id="11c9a-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11c9a-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="11c9a-193">groupId</span><span class="sxs-lookup"><span data-stu-id="11c9a-193">groupId</span></span> | <span data-ttu-id="11c9a-194">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11c9a-194">String</span></span> | <span data-ttu-id="11c9a-195">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="11c9a-195">Group Identifier</span></span> |
| <span data-ttu-id="11c9a-196">groupName</span><span class="sxs-lookup"><span data-stu-id="11c9a-196">groupName</span></span> | <span data-ttu-id="11c9a-197">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11c9a-197">String</span></span> | <span data-ttu-id="11c9a-198">Name der Gruppe erstellt</span><span class="sxs-lookup"><span data-stu-id="11c9a-198">Name of the group created</span></span> |


#### <a name="sample-json-response"></a><span data-ttu-id="11c9a-199">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="11c9a-199">Sample JSON Response</span></span>

```javascript
{
    "groupId": "853654b2-5874-462d-b709-0c4e43a7083f",
    "groupName": "Test Group"
}
```
