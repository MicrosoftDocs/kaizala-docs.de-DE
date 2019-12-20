---
title: /messages
description: Referenzartikel zur API zum Abfragen von Nachrichten, die von Ina Group gesendet werden
topic: Reference
author: nitinjms
ms.openlocfilehash: 64d694e067336a7da0c08ea116498086ee5650ce
ms.sourcegitcommit: 9e57984827280ed977019d33dd78b1ce5e3097fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2019
ms.locfileid: "40809431"
---
# <a name="messages"></a><span data-ttu-id="60cc4-103">/messages</span><span class="sxs-lookup"><span data-stu-id="60cc4-103">/messages</span></span>

<span data-ttu-id="60cc4-104">API-Endpunkt zum Senden von Nachrichten an unterhaltungsgruppen in Kaizala.</span><span class="sxs-lookup"><span data-stu-id="60cc4-104">API end-point to send messages to conversation groups inside Kaizala.</span></span>

## <a name="post-messages"></a><span data-ttu-id="60cc4-105">Post/Messages</span><span class="sxs-lookup"><span data-stu-id="60cc4-105">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a><span data-ttu-id="60cc4-106">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="60cc4-106">Request Parameters</span></span>

|  | <span data-ttu-id="60cc4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="60cc4-107">Parameter</span></span> | <span data-ttu-id="60cc4-108">Typ</span><span class="sxs-lookup"><span data-stu-id="60cc4-108">Type</span></span> | <span data-ttu-id="60cc4-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="60cc4-109">Optional?</span></span> | <span data-ttu-id="60cc4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60cc4-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="60cc4-111">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="60cc4-111">URL Path Parameter</span></span> | <span data-ttu-id="60cc4-112">groupId</span><span class="sxs-lookup"><span data-stu-id="60cc4-112">groupId</span></span> | <span data-ttu-id="60cc4-113">String</span><span class="sxs-lookup"><span data-stu-id="60cc4-113">String</span></span> | <span data-ttu-id="60cc4-114">Nein</span><span class="sxs-lookup"><span data-stu-id="60cc4-114">No</span></span> | <span data-ttu-id="60cc4-115">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="60cc4-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="60cc4-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="60cc4-116">HTTP Header</span></span> | <span data-ttu-id="60cc4-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="60cc4-117">accessToken</span></span> | <span data-ttu-id="60cc4-118">String</span><span class="sxs-lookup"><span data-stu-id="60cc4-118">String</span></span> | <span data-ttu-id="60cc4-119">Nein</span><span class="sxs-lookup"><span data-stu-id="60cc4-119">No</span></span> | <span data-ttu-id="60cc4-120">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="60cc4-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="60cc4-121">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="60cc4-121">HTTP Header</span></span> | <span data-ttu-id="60cc4-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="60cc4-122">Content-Type</span></span> | <span data-ttu-id="60cc4-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60cc4-123">String</span></span> | <span data-ttu-id="60cc4-124">Nein</span><span class="sxs-lookup"><span data-stu-id="60cc4-124">No</span></span> | <span data-ttu-id="60cc4-125">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="60cc4-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="60cc4-126">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="60cc4-126">Request body</span></span>

| <span data-ttu-id="60cc4-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="60cc4-127">Parameter</span></span> | <span data-ttu-id="60cc4-128">Typ</span><span class="sxs-lookup"><span data-stu-id="60cc4-128">Type</span></span> | <span data-ttu-id="60cc4-129">Optional?</span><span class="sxs-lookup"><span data-stu-id="60cc4-129">Optional?</span></span> | <span data-ttu-id="60cc4-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60cc4-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="60cc4-131">message</span><span class="sxs-lookup"><span data-stu-id="60cc4-131">message</span></span> | <span data-ttu-id="60cc4-132">String</span><span class="sxs-lookup"><span data-stu-id="60cc4-132">String</span></span> | <span data-ttu-id="60cc4-133">Nein</span><span class="sxs-lookup"><span data-stu-id="60cc4-133">No</span></span> | <span data-ttu-id="60cc4-134">Zu sendende Text Nachricht (maximale Grenze von 4000 Zeichen)</span><span class="sxs-lookup"><span data-stu-id="60cc4-134">Text message to be sent (Max limit of 4000 Characters)</span></span> |
| <span data-ttu-id="60cc4-135">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="60cc4-135">sendToAllSubscribers</span></span> | <span data-ttu-id="60cc4-136">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="60cc4-136">Bool</span></span> | <span data-ttu-id="60cc4-137">Ja</span><span class="sxs-lookup"><span data-stu-id="60cc4-137">Yes</span></span> | <span data-ttu-id="60cc4-138">Default: false.</span><span class="sxs-lookup"><span data-stu-id="60cc4-138">Default: false.</span></span> <span data-ttu-id="60cc4-139">Gilt nur für den Fall, dass die Gruppen-Nr zu einer öffentlichen Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="60cc4-139">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="60cc4-140">True, wenn die Textnachricht an alle Abonnenten gesendet werden soll, für die der Benutzer des Tokens Administrator der öffentlichen Gruppe sein muss.</span><span class="sxs-lookup"><span data-stu-id="60cc4-140">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="60cc4-141">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="60cc4-141">subscribers</span></span> | <span data-ttu-id="60cc4-142">String []</span><span class="sxs-lookup"><span data-stu-id="60cc4-142">String[]</span></span> | <span data-ttu-id="60cc4-143">Ja</span><span class="sxs-lookup"><span data-stu-id="60cc4-143">Yes</span></span> | <span data-ttu-id="60cc4-144">Jedes Element entspricht einer Mobiltelefonnummer (mit Landesvorwahl).</span><span class="sxs-lookup"><span data-stu-id="60cc4-144">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="60cc4-145">EG.</span><span class="sxs-lookup"><span data-stu-id="60cc4-145">Eg.</span></span> <span data-ttu-id="60cc4-146">+ 911999999999).</span><span class="sxs-lookup"><span data-stu-id="60cc4-146">+911999999999).</span></span> <span data-ttu-id="60cc4-147">Die Text Nachricht wird nur an die ausgewählten Abonnenten gesendet.</span><span class="sxs-lookup"><span data-stu-id="60cc4-147">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="60cc4-148">Für die selektive Kommunikation mit Teilnehmern im Kontext einer öffentlichen Gruppe verwendet werden</span><span class="sxs-lookup"><span data-stu-id="60cc4-148">To be used for selective communication to subscribers in context of a Public Group</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="60cc4-149">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="60cc4-149">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a><span data-ttu-id="60cc4-150">Antworttext</span><span class="sxs-lookup"><span data-stu-id="60cc4-150">Response body</span></span>

| <span data-ttu-id="60cc4-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="60cc4-151">Parameter</span></span> | <span data-ttu-id="60cc4-152">Typ</span><span class="sxs-lookup"><span data-stu-id="60cc4-152">Type</span></span> | <span data-ttu-id="60cc4-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60cc4-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="60cc4-154">referenceId</span><span class="sxs-lookup"><span data-stu-id="60cc4-154">referenceId</span></span> | <span data-ttu-id="60cc4-155">String</span><span class="sxs-lookup"><span data-stu-id="60cc4-155">String</span></span> | <span data-ttu-id="60cc4-156">GUID, die den erfolgreichen Abschluss der Anforderung darstellt</span><span class="sxs-lookup"><span data-stu-id="60cc4-156">GUID representing the successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="60cc4-157">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="60cc4-157">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
