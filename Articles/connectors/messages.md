---
title: /Messages
description: Referenzartikel zur API zum Abfragen von Nachrichten, die an Ina Group gesendet wurden
topic: Reference
author: nitinjms
ms.openlocfilehash: 8efad3236e852276e11c3052f98ac6f1d5541b0a
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190712"
---
# <a name="messages"></a><span data-ttu-id="182cf-103">/Messages</span><span class="sxs-lookup"><span data-stu-id="182cf-103">/messages</span></span>

<span data-ttu-id="182cf-104">API-Endpunkt zum Senden von Nachrichten an unterhaltungsgruppen innerhalb von Kaizala.</span><span class="sxs-lookup"><span data-stu-id="182cf-104">API end-point to send messages to conversation groups inside Kaizala.</span></span>

## <a name="post-messages"></a><span data-ttu-id="182cf-105">POST/Messages</span><span class="sxs-lookup"><span data-stu-id="182cf-105">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

### <a name="request-parameters"></a><span data-ttu-id="182cf-106">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="182cf-106">Request Parameters</span></span>

|  | <span data-ttu-id="182cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="182cf-107">Parameter</span></span> | <span data-ttu-id="182cf-108">Typ</span><span class="sxs-lookup"><span data-stu-id="182cf-108">Type</span></span> | <span data-ttu-id="182cf-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="182cf-109">Optional?</span></span> | <span data-ttu-id="182cf-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="182cf-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="182cf-111">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="182cf-111">URL Path Parameter</span></span> | <span data-ttu-id="182cf-112">groupId</span><span class="sxs-lookup"><span data-stu-id="182cf-112">groupId</span></span> | <span data-ttu-id="182cf-113">String</span><span class="sxs-lookup"><span data-stu-id="182cf-113">String</span></span> | <span data-ttu-id="182cf-114">Nein</span><span class="sxs-lookup"><span data-stu-id="182cf-114">No</span></span> | <span data-ttu-id="182cf-115">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="182cf-115">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="182cf-116">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="182cf-116">HTTP Header</span></span> | <span data-ttu-id="182cf-117">accessToken</span><span class="sxs-lookup"><span data-stu-id="182cf-117">accessToken</span></span> | <span data-ttu-id="182cf-118">String</span><span class="sxs-lookup"><span data-stu-id="182cf-118">String</span></span> | <span data-ttu-id="182cf-119">Nein</span><span class="sxs-lookup"><span data-stu-id="182cf-119">No</span></span> | <span data-ttu-id="182cf-120">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="182cf-120">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="182cf-121">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="182cf-121">HTTP Header</span></span> | <span data-ttu-id="182cf-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="182cf-122">Content-Type</span></span> | <span data-ttu-id="182cf-123">String</span><span class="sxs-lookup"><span data-stu-id="182cf-123">String</span></span> | <span data-ttu-id="182cf-124">Nein</span><span class="sxs-lookup"><span data-stu-id="182cf-124">No</span></span> | <span data-ttu-id="182cf-125">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="182cf-125">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="182cf-126">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="182cf-126">Request body</span></span>

| <span data-ttu-id="182cf-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="182cf-127">Parameter</span></span> | <span data-ttu-id="182cf-128">Typ</span><span class="sxs-lookup"><span data-stu-id="182cf-128">Type</span></span> | <span data-ttu-id="182cf-129">Optional?</span><span class="sxs-lookup"><span data-stu-id="182cf-129">Optional?</span></span> | <span data-ttu-id="182cf-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="182cf-130">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="182cf-131">message</span><span class="sxs-lookup"><span data-stu-id="182cf-131">message</span></span> | <span data-ttu-id="182cf-132">String</span><span class="sxs-lookup"><span data-stu-id="182cf-132">String</span></span> | <span data-ttu-id="182cf-133">Nein</span><span class="sxs-lookup"><span data-stu-id="182cf-133">No</span></span> | <span data-ttu-id="182cf-134">Zu sendende Text Nachricht (maximale Grenze von 1000 Zeichen)</span><span class="sxs-lookup"><span data-stu-id="182cf-134">Text message to be sent (Max limit of 1000 Characters)</span></span> |
| <span data-ttu-id="182cf-135">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="182cf-135">sendToAllSubscribers</span></span> | <span data-ttu-id="182cf-136">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="182cf-136">Bool</span></span> | <span data-ttu-id="182cf-137">Ja</span><span class="sxs-lookup"><span data-stu-id="182cf-137">Yes</span></span> | <span data-ttu-id="182cf-138">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="182cf-138">Default: false.</span></span> <span data-ttu-id="182cf-139">Gilt nur für den Fall, dass die Gruppen-zu einer öffentlichen Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="182cf-139">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="182cf-140">True, um die Textnachricht an alle Abonnenten zu senden, für die der Benutzer des Tokens als Administrator der öffentlichen Gruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="182cf-140">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="182cf-141">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="182cf-141">subscribers</span></span> | <span data-ttu-id="182cf-142">String []</span><span class="sxs-lookup"><span data-stu-id="182cf-142">String[]</span></span> | <span data-ttu-id="182cf-143">Ja</span><span class="sxs-lookup"><span data-stu-id="182cf-143">Yes</span></span> | <span data-ttu-id="182cf-144">Jedes Element entspricht einer Mobiltelefonnummer (mit Landesvorwahl.</span><span class="sxs-lookup"><span data-stu-id="182cf-144">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="182cf-145">EG.</span><span class="sxs-lookup"><span data-stu-id="182cf-145">Eg.</span></span> <span data-ttu-id="182cf-146">+ 911999999999).</span><span class="sxs-lookup"><span data-stu-id="182cf-146">+911999999999).</span></span> <span data-ttu-id="182cf-147">Text Nachricht wird nur an die ausgewählten Abonnenten gesendet.</span><span class="sxs-lookup"><span data-stu-id="182cf-147">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="182cf-148">Zur selektiven Kommunikation mit Abonnenten im Kontext einer öffentlichen Gruppe</span><span class="sxs-lookup"><span data-stu-id="182cf-148">To be used for selective communication to subscribers in context of a Public Group</span></span> |

#### <a name="sample-json-request"></a><span data-ttu-id="182cf-149">JSON-Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="182cf-149">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

### <a name="response-body"></a><span data-ttu-id="182cf-150">Antworttext</span><span class="sxs-lookup"><span data-stu-id="182cf-150">Response body</span></span>

| <span data-ttu-id="182cf-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="182cf-151">Parameter</span></span> | <span data-ttu-id="182cf-152">Typ</span><span class="sxs-lookup"><span data-stu-id="182cf-152">Type</span></span> | <span data-ttu-id="182cf-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="182cf-153">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="182cf-154">referenceId</span><span class="sxs-lookup"><span data-stu-id="182cf-154">referenceId</span></span> | <span data-ttu-id="182cf-155">String</span><span class="sxs-lookup"><span data-stu-id="182cf-155">String</span></span> | <span data-ttu-id="182cf-156">GUID, die den erfolgreichen Abschluss der Anforderung darstellt</span><span class="sxs-lookup"><span data-stu-id="182cf-156">GUID representing the successful completion of the request</span></span> |

#### <a name="sample-json-response"></a><span data-ttu-id="182cf-157">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="182cf-157">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
