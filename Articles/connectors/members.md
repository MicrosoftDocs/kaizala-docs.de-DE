---
title: /Members
description: Referenzartikel für API zum Abfragen von Gruppenmitglieder Daten
topic: Reference
author: nitinjms
ms.openlocfilehash: a2bbbc19e74140737e768b55f296f2463004d2fa
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190792"
---
# <a name="members"></a><span data-ttu-id="8b349-103">/Members</span><span class="sxs-lookup"><span data-stu-id="8b349-103">/members</span></span>
<span data-ttu-id="8b349-104">API-Endpunkt zum Hinzufügen oder Löschen von Mitgliedern aus Konversationsgruppen innerhalb von Kaizala.</span><span class="sxs-lookup"><span data-stu-id="8b349-104">API end-point to add or delete members from conversation groups inside Kaizala.</span></span>

## <a name="get-members"></a><span data-ttu-id="8b349-105">/Members abrufen</span><span class="sxs-lookup"><span data-stu-id="8b349-105">GET /members</span></span>

    GET {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="8b349-106">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="8b349-106">Request Parameters</span></span>

|  | <span data-ttu-id="8b349-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-107">Parameter</span></span> | <span data-ttu-id="8b349-108">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-108">Type</span></span> | <span data-ttu-id="8b349-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="8b349-109">Optional?</span></span> | <span data-ttu-id="8b349-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="8b349-111">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-111">URL Path Parameter</span></span> | <span data-ttu-id="8b349-112">groupId</span><span class="sxs-lookup"><span data-stu-id="8b349-112">groupId</span></span> | <span data-ttu-id="8b349-113">String</span><span class="sxs-lookup"><span data-stu-id="8b349-113">String</span></span> | <span data-ttu-id="8b349-114">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-114">No</span></span> | <span data-ttu-id="8b349-115">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="8b349-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="8b349-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="8b349-116">HTTP Header</span></span> | <span data-ttu-id="8b349-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="8b349-117">accessToken</span></span> | <span data-ttu-id="8b349-118">String</span><span class="sxs-lookup"><span data-stu-id="8b349-118">String</span></span> | <span data-ttu-id="8b349-119">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-119">No</span></span> | <span data-ttu-id="8b349-120">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="8b349-120">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="8b349-121">Antworttext</span><span class="sxs-lookup"><span data-stu-id="8b349-121">Response body</span></span>

| <span data-ttu-id="8b349-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-122">Parameter</span></span> | <span data-ttu-id="8b349-123">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-123">Type</span></span> | <span data-ttu-id="8b349-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-124">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8b349-125">members</span><span class="sxs-lookup"><span data-stu-id="8b349-125">members</span></span> | <span data-ttu-id="8b349-126">JSON-Array</span><span class="sxs-lookup"><span data-stu-id="8b349-126">JSON Array</span></span> | <span data-ttu-id="8b349-127">Array von JSON-Objekten, die jeweils ein Mitglied der Gruppe darstellen</span><span class="sxs-lookup"><span data-stu-id="8b349-127">Array of JSON objects each representing a member of the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="8b349-128">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="8b349-128">Sample JSON Response</span></span>

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

## <a name="put-members"></a><span data-ttu-id="8b349-129">PUT/Members</span><span class="sxs-lookup"><span data-stu-id="8b349-129">PUT /members</span></span>

    PUT {endpoint-url}/v1/groups/{groupId}/members

### <a name="request-parameters"></a><span data-ttu-id="8b349-130">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="8b349-130">Request Parameters</span></span>

|  | <span data-ttu-id="8b349-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-131">Parameter</span></span> | <span data-ttu-id="8b349-132">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-132">Type</span></span> | <span data-ttu-id="8b349-133">Optional?</span><span class="sxs-lookup"><span data-stu-id="8b349-133">Optional?</span></span> | <span data-ttu-id="8b349-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="8b349-135">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-135">URL Path Parameter</span></span> | <span data-ttu-id="8b349-136">groupId</span><span class="sxs-lookup"><span data-stu-id="8b349-136">groupId</span></span> | <span data-ttu-id="8b349-137">String</span><span class="sxs-lookup"><span data-stu-id="8b349-137">String</span></span> | <span data-ttu-id="8b349-138">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-138">No</span></span> | <span data-ttu-id="8b349-139">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="8b349-139">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="8b349-140">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="8b349-140">HTTP Header</span></span> | <span data-ttu-id="8b349-141">accessToken</span><span class="sxs-lookup"><span data-stu-id="8b349-141">accessToken</span></span> | <span data-ttu-id="8b349-142">String</span><span class="sxs-lookup"><span data-stu-id="8b349-142">String</span></span> | <span data-ttu-id="8b349-143">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-143">No</span></span> | <span data-ttu-id="8b349-144">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="8b349-144">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="8b349-145">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="8b349-145">HTTP Header</span></span> | <span data-ttu-id="8b349-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8b349-146">Content-Type</span></span> | <span data-ttu-id="8b349-147">String</span><span class="sxs-lookup"><span data-stu-id="8b349-147">String</span></span> | <span data-ttu-id="8b349-148">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-148">No</span></span> | <span data-ttu-id="8b349-149">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="8b349-149">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="8b349-150">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="8b349-150">Request body</span></span>

| <span data-ttu-id="8b349-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-151">Parameter</span></span> | <span data-ttu-id="8b349-152">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-152">Type</span></span> | <span data-ttu-id="8b349-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8b349-154">members</span><span class="sxs-lookup"><span data-stu-id="8b349-154">members</span></span> | <span data-ttu-id="8b349-155">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="8b349-155">String Array</span></span> | <span data-ttu-id="8b349-156">Array von formatierten Telefonnummern neuer Mitglieder, die hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="8b349-156">Array of well-formatted phone numbers of new members to be added</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="8b349-157">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="8b349-157">Sample JSON Request</span></span>

```javascript
{
  "members": [
      "+91000000000",
      "+91900000000"
  ]
}
```

### <a name="response-body"></a><span data-ttu-id="8b349-158">Antworttext</span><span class="sxs-lookup"><span data-stu-id="8b349-158">Response body</span></span>

| <span data-ttu-id="8b349-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-159">Parameter</span></span> | <span data-ttu-id="8b349-160">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-160">Type</span></span> | <span data-ttu-id="8b349-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-161">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8b349-162">result</span><span class="sxs-lookup"><span data-stu-id="8b349-162">result</span></span> | <span data-ttu-id="8b349-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="8b349-163">Boolean</span></span> | <span data-ttu-id="8b349-164">True, wenn alle Telefonnummern erfolgreich der Gruppe hinzugefügt wurden</span><span class="sxs-lookup"><span data-stu-id="8b349-164">True when all phone numbers have succesfully been added to the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="8b349-165">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="8b349-165">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```

## <a name="delete-members"></a><span data-ttu-id="8b349-166">/Members löschen</span><span class="sxs-lookup"><span data-stu-id="8b349-166">DELETE /members</span></span>

    DELETE {endpoint-url}/v1/groups/{groupId}/members/{memberId}

### <a name="request-parameters"></a><span data-ttu-id="8b349-167">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="8b349-167">Request Parameters</span></span>

|  | <span data-ttu-id="8b349-168">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-168">Parameter</span></span> | <span data-ttu-id="8b349-169">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-169">Type</span></span> | <span data-ttu-id="8b349-170">Optional?</span><span class="sxs-lookup"><span data-stu-id="8b349-170">Optional?</span></span> | <span data-ttu-id="8b349-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-171">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="8b349-172">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-172">URL Path Parameter</span></span> | <span data-ttu-id="8b349-173">groupId</span><span class="sxs-lookup"><span data-stu-id="8b349-173">groupId</span></span> | <span data-ttu-id="8b349-174">String</span><span class="sxs-lookup"><span data-stu-id="8b349-174">String</span></span> | <span data-ttu-id="8b349-175">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-175">No</span></span> | <span data-ttu-id="8b349-176">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="8b349-176">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="8b349-177">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-177">URL Path Parameter</span></span> | <span data-ttu-id="8b349-178">memberId</span><span class="sxs-lookup"><span data-stu-id="8b349-178">memberId</span></span> | <span data-ttu-id="8b349-179">String</span><span class="sxs-lookup"><span data-stu-id="8b349-179">String</span></span> | <span data-ttu-id="8b349-180">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-180">No</span></span> | <span data-ttu-id="8b349-181">GUID, die die Member-ID des bestimmten Members darstellt</span><span class="sxs-lookup"><span data-stu-id="8b349-181">GUID representing the memberId of the specific member</span></span> |
| <span data-ttu-id="8b349-182">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="8b349-182">HTTP Header</span></span> | <span data-ttu-id="8b349-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="8b349-183">accessToken</span></span> | <span data-ttu-id="8b349-184">String</span><span class="sxs-lookup"><span data-stu-id="8b349-184">String</span></span> | <span data-ttu-id="8b349-185">Nein</span><span class="sxs-lookup"><span data-stu-id="8b349-185">No</span></span> | <span data-ttu-id="8b349-186">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="8b349-186">Access Token received from the auth end-point</span></span> |

### <a name="response-body"></a><span data-ttu-id="8b349-187">Antworttext</span><span class="sxs-lookup"><span data-stu-id="8b349-187">Response body</span></span>

| <span data-ttu-id="8b349-188">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b349-188">Parameter</span></span> | <span data-ttu-id="8b349-189">Typ</span><span class="sxs-lookup"><span data-stu-id="8b349-189">Type</span></span> | <span data-ttu-id="8b349-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b349-190">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8b349-191">result</span><span class="sxs-lookup"><span data-stu-id="8b349-191">result</span></span> | <span data-ttu-id="8b349-192">Boolean</span><span class="sxs-lookup"><span data-stu-id="8b349-192">Boolean</span></span> | <span data-ttu-id="8b349-193">True, wenn das angegebene Element erfolgreich aus der Gruppe entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="8b349-193">True when the specified member has succesfully been removed from the group</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="8b349-194">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="8b349-194">Sample JSON Response</span></span>

```javascript
{
    "result": "true"
}
```
