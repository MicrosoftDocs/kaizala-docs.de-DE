---
title: /Messages
description: Referenzartikel für API auf Abfragenachrichten gesendet, einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 58839035fca768f92eda40974029208eb31dda7f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/31/2018
ms.locfileid: "27465701"
---
# <a name="messages"></a><span data-ttu-id="7f596-103">/Messages</span><span class="sxs-lookup"><span data-stu-id="7f596-103">/messages</span></span>

<span data-ttu-id="7f596-104">Zum Senden von Nachrichten an Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7f596-104">API end-point to send messages to conversation groups inside Kaizala.</span></span>

## <a name="post-messages"></a><span data-ttu-id="7f596-105">POST-/messages</span><span class="sxs-lookup"><span data-stu-id="7f596-105">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a><span data-ttu-id="7f596-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="7f596-106">Request Parameters</span></span>

|  | <span data-ttu-id="7f596-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f596-107">Parameter</span></span> | <span data-ttu-id="7f596-108">Typ</span><span class="sxs-lookup"><span data-stu-id="7f596-108">Type</span></span> | <span data-ttu-id="7f596-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="7f596-109">Optional?</span></span> | <span data-ttu-id="7f596-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f596-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7f596-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="7f596-111">URL Path Parameter</span></span> | <span data-ttu-id="7f596-112">groupId</span><span class="sxs-lookup"><span data-stu-id="7f596-112">groupId</span></span> | <span data-ttu-id="7f596-113">String</span><span class="sxs-lookup"><span data-stu-id="7f596-113">String</span></span> | <span data-ttu-id="7f596-114">Nein</span><span class="sxs-lookup"><span data-stu-id="7f596-114">No</span></span> | <span data-ttu-id="7f596-115">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f596-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7f596-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7f596-116">HTTP Header</span></span> | <span data-ttu-id="7f596-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="7f596-117">accessToken</span></span> | <span data-ttu-id="7f596-118">String</span><span class="sxs-lookup"><span data-stu-id="7f596-118">String</span></span> | <span data-ttu-id="7f596-119">Nein</span><span class="sxs-lookup"><span data-stu-id="7f596-119">No</span></span> | <span data-ttu-id="7f596-120">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7f596-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="7f596-121">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7f596-121">HTTP Header</span></span> | <span data-ttu-id="7f596-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7f596-122">Content-Type</span></span> | <span data-ttu-id="7f596-123">String</span><span class="sxs-lookup"><span data-stu-id="7f596-123">String</span></span> | <span data-ttu-id="7f596-124">Nein</span><span class="sxs-lookup"><span data-stu-id="7f596-124">No</span></span> | <span data-ttu-id="7f596-125">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="7f596-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="7f596-126">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="7f596-126">Request body</span></span>

| <span data-ttu-id="7f596-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f596-127">Parameter</span></span> | <span data-ttu-id="7f596-128">Typ</span><span class="sxs-lookup"><span data-stu-id="7f596-128">Type</span></span> | <span data-ttu-id="7f596-129">Optional?</span><span class="sxs-lookup"><span data-stu-id="7f596-129">Optional?</span></span> | <span data-ttu-id="7f596-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f596-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="7f596-131">message</span><span class="sxs-lookup"><span data-stu-id="7f596-131">message</span></span> | <span data-ttu-id="7f596-132">String</span><span class="sxs-lookup"><span data-stu-id="7f596-132">String</span></span> | <span data-ttu-id="7f596-133">Nein</span><span class="sxs-lookup"><span data-stu-id="7f596-133">No</span></span> | <span data-ttu-id="7f596-134">Textnachricht (Max 1.000 Zeichen begrenzt) gesendet werden</span><span class="sxs-lookup"><span data-stu-id="7f596-134">Text message to be sent (Max limit of 1000 Characters)</span></span> |
| <span data-ttu-id="7f596-135">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="7f596-135">sendToAllSubscribers</span></span> | <span data-ttu-id="7f596-136">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="7f596-136">Bool</span></span> | <span data-ttu-id="7f596-137">Ja</span><span class="sxs-lookup"><span data-stu-id="7f596-137">Yes</span></span> | <span data-ttu-id="7f596-138">Standard: False.</span><span class="sxs-lookup"><span data-stu-id="7f596-138">Default: false.</span></span> <span data-ttu-id="7f596-139">Gültige nur im Fall der GroupId öffentliche Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="7f596-139">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="7f596-140">True, um die Text-Nachricht an alle Abonnenten senden bewirkt, dass die das Token Benutzer Admin der Gruppe der öffentlich sein</span><span class="sxs-lookup"><span data-stu-id="7f596-140">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="7f596-141">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="7f596-141">subscribers</span></span> | <span data-ttu-id="7f596-142">String]</span><span class="sxs-lookup"><span data-stu-id="7f596-142">String[]</span></span> | <span data-ttu-id="7f596-143">Ja</span><span class="sxs-lookup"><span data-stu-id="7f596-143">Yes</span></span> | <span data-ttu-id="7f596-144">Jedes Element entspricht einer Mobiltelefonnummer (mit Ländercode.</span><span class="sxs-lookup"><span data-stu-id="7f596-144">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="7f596-145">EG.</span><span class="sxs-lookup"><span data-stu-id="7f596-145">Eg.</span></span> <span data-ttu-id="7f596-146">+911999999999).</span><span class="sxs-lookup"><span data-stu-id="7f596-146">+911999999999).</span></span> <span data-ttu-id="7f596-147">Textnachricht wird nur für die ausgewählten Abonnenten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f596-147">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="7f596-148">Für selektive Kommunikation für Abonnenten im Kontext eines öffentliche Gruppe verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="7f596-148">To be used for selective communication to subscribers in context of a Public Group</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="7f596-149">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f596-149">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a><span data-ttu-id="7f596-150">Antworttext</span><span class="sxs-lookup"><span data-stu-id="7f596-150">Response body</span></span>

| <span data-ttu-id="7f596-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f596-151">Parameter</span></span> | <span data-ttu-id="7f596-152">Typ</span><span class="sxs-lookup"><span data-stu-id="7f596-152">Type</span></span> | <span data-ttu-id="7f596-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f596-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7f596-154">referenceId</span><span class="sxs-lookup"><span data-stu-id="7f596-154">referenceId</span></span> | <span data-ttu-id="7f596-155">String</span><span class="sxs-lookup"><span data-stu-id="7f596-155">String</span></span> | <span data-ttu-id="7f596-156">GUID, die den erfolgreichen Abschluss der Anforderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f596-156">GUID representing the successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="7f596-157">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="7f596-157">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
