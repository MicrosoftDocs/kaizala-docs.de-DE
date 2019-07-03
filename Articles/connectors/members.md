---
title: /members
description: Referenzartikel zur API für Abfragegruppen Mitgliederdaten
topic: Reference
author: nitinjms
ms.openlocfilehash: d4f71858cfd58a4d6dd33f3d3d14b5ac855a757a
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535774"
---
# <a name="members"></a><span data-ttu-id="7a215-103">/members</span><span class="sxs-lookup"><span data-stu-id="7a215-103">/members</span></span>
<span data-ttu-id="7a215-104">API-Endpunkt zum Hinzufügen oder Löschen von Mitgliedern aus unterhaltungsgruppen in Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7a215-104">API end-point to add or delete members from conversation groups inside Kaizala.</span></span>

## <a name="get-members"></a><span data-ttu-id="7a215-105">/Members abrufen</span><span class="sxs-lookup"><span data-stu-id="7a215-105">GET /members</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="7a215-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="7a215-106">Request Parameters</span></span>

|  | <span data-ttu-id="7a215-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-107">Parameter</span></span> | <span data-ttu-id="7a215-108">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-108">Type</span></span> | <span data-ttu-id="7a215-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="7a215-109">Optional?</span></span> | <span data-ttu-id="7a215-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7a215-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-111">URL Path Parameter</span></span> | <span data-ttu-id="7a215-112">groupId</span><span class="sxs-lookup"><span data-stu-id="7a215-112">groupId</span></span> | <span data-ttu-id="7a215-113">String</span><span class="sxs-lookup"><span data-stu-id="7a215-113">String</span></span> | <span data-ttu-id="7a215-114">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-114">No</span></span> | <span data-ttu-id="7a215-115">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a215-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7a215-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7a215-116">HTTP Header</span></span> | <span data-ttu-id="7a215-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="7a215-117">accessToken</span></span> | <span data-ttu-id="7a215-118">String</span><span class="sxs-lookup"><span data-stu-id="7a215-118">String</span></span> | <span data-ttu-id="7a215-119">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-119">No</span></span> | <span data-ttu-id="7a215-120">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="7a215-120">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="7a215-121">Antworttext</span><span class="sxs-lookup"><span data-stu-id="7a215-121">Response body</span></span>

| <span data-ttu-id="7a215-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-122">Parameter</span></span> | <span data-ttu-id="7a215-123">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-123">Type</span></span> | <span data-ttu-id="7a215-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7a215-125">Elemente</span><span class="sxs-lookup"><span data-stu-id="7a215-125">members</span></span> | <span data-ttu-id="7a215-126">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="7a215-126">JSON Array</span></span> | <span data-ttu-id="7a215-127">Array von JSON-Objekten, die jeweils ein Mitglied der Gruppe darstellen</span><span class="sxs-lookup"><span data-stu-id="7a215-127">Array of JSON objects each representing a member of the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7a215-128">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="7a215-128">Sample JSON Response</span></span>

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

## <a name="put-members"></a><span data-ttu-id="7a215-129">Put/Members</span><span class="sxs-lookup"><span data-stu-id="7a215-129">PUT /members</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="7a215-130">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="7a215-130">Request Parameters</span></span>

|  | <span data-ttu-id="7a215-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-131">Parameter</span></span> | <span data-ttu-id="7a215-132">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-132">Type</span></span> | <span data-ttu-id="7a215-133">Optional?</span><span class="sxs-lookup"><span data-stu-id="7a215-133">Optional?</span></span> | <span data-ttu-id="7a215-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7a215-135">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-135">URL Path Parameter</span></span> | <span data-ttu-id="7a215-136">groupId</span><span class="sxs-lookup"><span data-stu-id="7a215-136">groupId</span></span> | <span data-ttu-id="7a215-137">String</span><span class="sxs-lookup"><span data-stu-id="7a215-137">String</span></span> | <span data-ttu-id="7a215-138">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-138">No</span></span> | <span data-ttu-id="7a215-139">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a215-139">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7a215-140">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7a215-140">HTTP Header</span></span> | <span data-ttu-id="7a215-141">accessToken</span><span class="sxs-lookup"><span data-stu-id="7a215-141">accessToken</span></span> | <span data-ttu-id="7a215-142">String</span><span class="sxs-lookup"><span data-stu-id="7a215-142">String</span></span> | <span data-ttu-id="7a215-143">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-143">No</span></span> | <span data-ttu-id="7a215-144">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="7a215-144">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="7a215-145">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7a215-145">HTTP Header</span></span> | <span data-ttu-id="7a215-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7a215-146">Content-Type</span></span> | <span data-ttu-id="7a215-147">String</span><span class="sxs-lookup"><span data-stu-id="7a215-147">String</span></span> | <span data-ttu-id="7a215-148">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-148">No</span></span> | <span data-ttu-id="7a215-149">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="7a215-149">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="7a215-150">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="7a215-150">Request body</span></span>

| <span data-ttu-id="7a215-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-151">Parameter</span></span> | <span data-ttu-id="7a215-152">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-152">Type</span></span> | <span data-ttu-id="7a215-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7a215-154">Elemente</span><span class="sxs-lookup"><span data-stu-id="7a215-154">members</span></span> | <span data-ttu-id="7a215-155">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="7a215-155">String Array</span></span> | <span data-ttu-id="7a215-156">Array mit gut formatierten Telefonnummern neuer Mitglieder, die hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="7a215-156">Array of well-formatted phone numbers of new members to be added</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="7a215-157">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="7a215-157">Sample JSON Request</span></span>

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a><span data-ttu-id="7a215-158">Antworttext</span><span class="sxs-lookup"><span data-stu-id="7a215-158">Response body</span></span>

| <span data-ttu-id="7a215-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-159">Parameter</span></span> | <span data-ttu-id="7a215-160">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-160">Type</span></span> | <span data-ttu-id="7a215-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-161">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7a215-162">result</span><span class="sxs-lookup"><span data-stu-id="7a215-162">result</span></span> | <span data-ttu-id="7a215-163">Boolesch</span><span class="sxs-lookup"><span data-stu-id="7a215-163">Boolean</span></span> | <span data-ttu-id="7a215-164">True, wenn alle Telefonnummern erfolgreich der Gruppe hinzugefügt wurden</span><span class="sxs-lookup"><span data-stu-id="7a215-164">True when all phone numbers have successfully been added to the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7a215-165">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="7a215-165">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a><span data-ttu-id="7a215-166">/Members löschen</span><span class="sxs-lookup"><span data-stu-id="7a215-166">DELETE /members</span></span>

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a><span data-ttu-id="7a215-167">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="7a215-167">Request Parameters</span></span>

|  | <span data-ttu-id="7a215-168">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-168">Parameter</span></span> | <span data-ttu-id="7a215-169">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-169">Type</span></span> | <span data-ttu-id="7a215-170">Optional?</span><span class="sxs-lookup"><span data-stu-id="7a215-170">Optional?</span></span> | <span data-ttu-id="7a215-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-171">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7a215-172">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-172">URL Path Parameter</span></span> | <span data-ttu-id="7a215-173">groupId</span><span class="sxs-lookup"><span data-stu-id="7a215-173">groupId</span></span> | <span data-ttu-id="7a215-174">String</span><span class="sxs-lookup"><span data-stu-id="7a215-174">String</span></span> | <span data-ttu-id="7a215-175">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-175">No</span></span> | <span data-ttu-id="7a215-176">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a215-176">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7a215-177">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-177">URL Path Parameter</span></span> | <span data-ttu-id="7a215-178">memberId</span><span class="sxs-lookup"><span data-stu-id="7a215-178">memberId</span></span> | <span data-ttu-id="7a215-179">String</span><span class="sxs-lookup"><span data-stu-id="7a215-179">String</span></span> | <span data-ttu-id="7a215-180">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-180">No</span></span> | <span data-ttu-id="7a215-181">GUID, die die Mitglieds-ID des bestimmten Members darstellt</span><span class="sxs-lookup"><span data-stu-id="7a215-181">GUID representing the memberId of the specific member</span></span> |
| <span data-ttu-id="7a215-182">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7a215-182">HTTP Header</span></span> | <span data-ttu-id="7a215-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="7a215-183">accessToken</span></span> | <span data-ttu-id="7a215-184">String</span><span class="sxs-lookup"><span data-stu-id="7a215-184">String</span></span> | <span data-ttu-id="7a215-185">Nein</span><span class="sxs-lookup"><span data-stu-id="7a215-185">No</span></span> | <span data-ttu-id="7a215-186">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="7a215-186">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="7a215-187">Antworttext</span><span class="sxs-lookup"><span data-stu-id="7a215-187">Response body</span></span>

| <span data-ttu-id="7a215-188">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a215-188">Parameter</span></span> | <span data-ttu-id="7a215-189">Typ</span><span class="sxs-lookup"><span data-stu-id="7a215-189">Type</span></span> | <span data-ttu-id="7a215-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a215-190">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7a215-191">result</span><span class="sxs-lookup"><span data-stu-id="7a215-191">result</span></span> | <span data-ttu-id="7a215-192">Boolesch</span><span class="sxs-lookup"><span data-stu-id="7a215-192">Boolean</span></span> | <span data-ttu-id="7a215-193">True, wenn das angegebene Element erfolgreich aus der Gruppe entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="7a215-193">True when the specified member has successfully been removed from the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7a215-194">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="7a215-194">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```
