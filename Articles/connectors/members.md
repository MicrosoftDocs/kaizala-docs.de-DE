---
title: /Members
description: Referenzartikel für Abfragen Gruppe Mitglieder von Daten-API
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905351"
---
# <a name="members"></a><span data-ttu-id="48c1e-103">/Members</span><span class="sxs-lookup"><span data-stu-id="48c1e-103">/members</span></span>
<span data-ttu-id="48c1e-104">Hinzufügen oder Löschen von Mitgliedern aus Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="48c1e-104">API end-point to add or delete members from conversation groups inside Kaizala.</span></span>

## <a name="get-members"></a><span data-ttu-id="48c1e-105">Abrufen von /members</span><span class="sxs-lookup"><span data-stu-id="48c1e-105">GET /members</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="48c1e-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-106">Request Parameters</span></span>

|  | <span data-ttu-id="48c1e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-107">Parameter</span></span> | <span data-ttu-id="48c1e-108">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-108">Type</span></span> | <span data-ttu-id="48c1e-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="48c1e-109">Optional?</span></span> | <span data-ttu-id="48c1e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="48c1e-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-111">URL Path Parameter</span></span> | <span data-ttu-id="48c1e-112">groupId</span><span class="sxs-lookup"><span data-stu-id="48c1e-112">groupId</span></span> | <span data-ttu-id="48c1e-113">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-113">String</span></span> | <span data-ttu-id="48c1e-114">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-114">No</span></span> | <span data-ttu-id="48c1e-115">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="48c1e-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="48c1e-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="48c1e-116">HTTP Header</span></span> | <span data-ttu-id="48c1e-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="48c1e-117">accessToken</span></span> | <span data-ttu-id="48c1e-118">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-118">String</span></span> | <span data-ttu-id="48c1e-119">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-119">No</span></span> | <span data-ttu-id="48c1e-120">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="48c1e-120">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="48c1e-121">Antworttext</span><span class="sxs-lookup"><span data-stu-id="48c1e-121">Response body</span></span>

| <span data-ttu-id="48c1e-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-122">Parameter</span></span> | <span data-ttu-id="48c1e-123">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-123">Type</span></span> | <span data-ttu-id="48c1e-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48c1e-125">Elemente</span><span class="sxs-lookup"><span data-stu-id="48c1e-125">members</span></span> | <span data-ttu-id="48c1e-126">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="48c1e-126">JSON Array</span></span> | <span data-ttu-id="48c1e-127">Array von JSON-Objekten jedes, ein Mitglied der Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="48c1e-127">Array of JSON objects each representing a member of the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="48c1e-128">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="48c1e-128">Sample JSON Response</span></span>

```javascript
{
  "members": [
    {
      "id": "4deffa08-guid-4b87-8c2f-d944565f5f31",
      "role": "Admin",
      "mobileNumber": "+919652000000",
      "isProvisioned": true
    },
    {
      "id": "2e20e9ac-guid-47bd-abac-1f5236004684",
      "role": "Member",
      "mobileNumber": "+919652000001",
      "isProvisioned": false
    }
  ]
}
```

## <a name="put-members"></a><span data-ttu-id="48c1e-129">PLATZIEREN Sie /members</span><span class="sxs-lookup"><span data-stu-id="48c1e-129">PUT /members</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="48c1e-130">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-130">Request Parameters</span></span>

|  | <span data-ttu-id="48c1e-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-131">Parameter</span></span> | <span data-ttu-id="48c1e-132">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-132">Type</span></span> | <span data-ttu-id="48c1e-133">Optional?</span><span class="sxs-lookup"><span data-stu-id="48c1e-133">Optional?</span></span> | <span data-ttu-id="48c1e-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="48c1e-135">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-135">URL Path Parameter</span></span> | <span data-ttu-id="48c1e-136">groupId</span><span class="sxs-lookup"><span data-stu-id="48c1e-136">groupId</span></span> | <span data-ttu-id="48c1e-137">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-137">String</span></span> | <span data-ttu-id="48c1e-138">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-138">No</span></span> | <span data-ttu-id="48c1e-139">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="48c1e-139">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="48c1e-140">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="48c1e-140">HTTP Header</span></span> | <span data-ttu-id="48c1e-141">accessToken</span><span class="sxs-lookup"><span data-stu-id="48c1e-141">accessToken</span></span> | <span data-ttu-id="48c1e-142">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-142">String</span></span> | <span data-ttu-id="48c1e-143">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-143">No</span></span> | <span data-ttu-id="48c1e-144">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="48c1e-144">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="48c1e-145">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="48c1e-145">HTTP Header</span></span> | <span data-ttu-id="48c1e-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="48c1e-146">Content-Type</span></span> | <span data-ttu-id="48c1e-147">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-147">String</span></span> | <span data-ttu-id="48c1e-148">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-148">No</span></span> | <span data-ttu-id="48c1e-149">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="48c1e-149">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="48c1e-150">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="48c1e-150">Request body</span></span>

| <span data-ttu-id="48c1e-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-151">Parameter</span></span> | <span data-ttu-id="48c1e-152">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-152">Type</span></span> | <span data-ttu-id="48c1e-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48c1e-154">Elemente</span><span class="sxs-lookup"><span data-stu-id="48c1e-154">members</span></span> | <span data-ttu-id="48c1e-155">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="48c1e-155">String Array</span></span> | <span data-ttu-id="48c1e-156">Array von gut formatierte Telefonnummern der neuen Elemente hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="48c1e-156">Array of well-formatted phone numbers of new members to be added</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="48c1e-157">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="48c1e-157">Sample JSON Request</span></span>

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a><span data-ttu-id="48c1e-158">Antworttext</span><span class="sxs-lookup"><span data-stu-id="48c1e-158">Response body</span></span>

| <span data-ttu-id="48c1e-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-159">Parameter</span></span> | <span data-ttu-id="48c1e-160">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-160">Type</span></span> | <span data-ttu-id="48c1e-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-161">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48c1e-162">result</span><span class="sxs-lookup"><span data-stu-id="48c1e-162">result</span></span> | <span data-ttu-id="48c1e-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="48c1e-163">Boolean</span></span> | <span data-ttu-id="48c1e-164">True, wenn alle Rufnummer erfolgreich an die Gruppe hinzugefügt wurden</span><span class="sxs-lookup"><span data-stu-id="48c1e-164">True when all phone numbers have succesfully been added to the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="48c1e-165">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="48c1e-165">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a><span data-ttu-id="48c1e-166">/Members löschen</span><span class="sxs-lookup"><span data-stu-id="48c1e-166">DELETE /members</span></span>

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a><span data-ttu-id="48c1e-167">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-167">Request Parameters</span></span>

|  | <span data-ttu-id="48c1e-168">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-168">Parameter</span></span> | <span data-ttu-id="48c1e-169">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-169">Type</span></span> | <span data-ttu-id="48c1e-170">Optional?</span><span class="sxs-lookup"><span data-stu-id="48c1e-170">Optional?</span></span> | <span data-ttu-id="48c1e-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-171">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="48c1e-172">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-172">URL Path Parameter</span></span> | <span data-ttu-id="48c1e-173">groupId</span><span class="sxs-lookup"><span data-stu-id="48c1e-173">groupId</span></span> | <span data-ttu-id="48c1e-174">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-174">String</span></span> | <span data-ttu-id="48c1e-175">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-175">No</span></span> | <span data-ttu-id="48c1e-176">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="48c1e-176">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="48c1e-177">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-177">URL Path Parameter</span></span> | <span data-ttu-id="48c1e-178">memberId</span><span class="sxs-lookup"><span data-stu-id="48c1e-178">memberId</span></span> | <span data-ttu-id="48c1e-179">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-179">String</span></span> | <span data-ttu-id="48c1e-180">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-180">No</span></span> | <span data-ttu-id="48c1e-181">GUID, die die MemberId des bestimmten Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="48c1e-181">GUID representing the memberId of the specific member</span></span> |
| <span data-ttu-id="48c1e-182">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="48c1e-182">HTTP Header</span></span> | <span data-ttu-id="48c1e-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="48c1e-183">accessToken</span></span> | <span data-ttu-id="48c1e-184">String</span><span class="sxs-lookup"><span data-stu-id="48c1e-184">String</span></span> | <span data-ttu-id="48c1e-185">Nein</span><span class="sxs-lookup"><span data-stu-id="48c1e-185">No</span></span> | <span data-ttu-id="48c1e-186">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="48c1e-186">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="48c1e-187">Antworttext</span><span class="sxs-lookup"><span data-stu-id="48c1e-187">Response body</span></span>

| <span data-ttu-id="48c1e-188">Parameter</span><span class="sxs-lookup"><span data-stu-id="48c1e-188">Parameter</span></span> | <span data-ttu-id="48c1e-189">Typ</span><span class="sxs-lookup"><span data-stu-id="48c1e-189">Type</span></span> | <span data-ttu-id="48c1e-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48c1e-190">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="48c1e-191">result</span><span class="sxs-lookup"><span data-stu-id="48c1e-191">result</span></span> | <span data-ttu-id="48c1e-192">Boolean</span><span class="sxs-lookup"><span data-stu-id="48c1e-192">Boolean</span></span> | <span data-ttu-id="48c1e-193">True, wenn das angegebene Element wurde erfolgreich aus der Gruppe entfernt</span><span class="sxs-lookup"><span data-stu-id="48c1e-193">True when the specified member has succesfully been removed from the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="48c1e-194">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="48c1e-194">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```
