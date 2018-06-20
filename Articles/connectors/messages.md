---
title: /Messages
description: Referenzartikel für API auf Abfragenachrichten gesendet, einer Gruppe
topic: Reference
author: nitinjms
ms.openlocfilehash: 25e3a918c95bd045a374de0420eda6324d46046a
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905368"
---
# <a name="apis-to-query-messages-sent-in-a-group"></a><span data-ttu-id="e2e22-103">APIs für die von Abfragenachrichten in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="e2e22-103">APIs to query messages sent in a group</span></span>
## <a name="messages"></a><span data-ttu-id="e2e22-104">/Messages</span><span class="sxs-lookup"><span data-stu-id="e2e22-104">/messages</span></span>
<span data-ttu-id="e2e22-105">Zum Senden von Nachrichten an Unterhaltungsgruppen innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e2e22-105">API end-point to send messages to conversation groups inside Kaizala.</span></span>

### <a name="post-messages"></a><span data-ttu-id="e2e22-106">POST-/messages</span><span class="sxs-lookup"><span data-stu-id="e2e22-106">POST /messages</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/messages

##### <a name="request-parameters"></a><span data-ttu-id="e2e22-107">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="e2e22-107">Request Parameters</span></span>

|  | <span data-ttu-id="e2e22-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e22-108">Parameter</span></span> | <span data-ttu-id="e2e22-109">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e22-109">Type</span></span> | <span data-ttu-id="e2e22-110">Optional?</span><span class="sxs-lookup"><span data-stu-id="e2e22-110">Optional?</span></span> | <span data-ttu-id="e2e22-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e22-111">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="e2e22-112">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e22-112">URL Path Parameter</span></span> | <span data-ttu-id="e2e22-113">groupId</span><span class="sxs-lookup"><span data-stu-id="e2e22-113">groupId</span></span> | <span data-ttu-id="e2e22-114">String</span><span class="sxs-lookup"><span data-stu-id="e2e22-114">String</span></span> | <span data-ttu-id="e2e22-115">Nein</span><span class="sxs-lookup"><span data-stu-id="e2e22-115">No</span></span> | <span data-ttu-id="e2e22-116">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2e22-116">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="e2e22-117">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="e2e22-117">HTTP Header</span></span> | <span data-ttu-id="e2e22-118">accessToken</span><span class="sxs-lookup"><span data-stu-id="e2e22-118">accessToken</span></span> | <span data-ttu-id="e2e22-119">String</span><span class="sxs-lookup"><span data-stu-id="e2e22-119">String</span></span> | <span data-ttu-id="e2e22-120">Nein</span><span class="sxs-lookup"><span data-stu-id="e2e22-120">No</span></span> | <span data-ttu-id="e2e22-121">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e2e22-121">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="e2e22-122">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="e2e22-122">HTTP Header</span></span> | <span data-ttu-id="e2e22-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e2e22-123">Content-Type</span></span> | <span data-ttu-id="e2e22-124">String</span><span class="sxs-lookup"><span data-stu-id="e2e22-124">String</span></span> | <span data-ttu-id="e2e22-125">Nein</span><span class="sxs-lookup"><span data-stu-id="e2e22-125">No</span></span> | <span data-ttu-id="e2e22-126">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="e2e22-126">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="e2e22-127">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="e2e22-127">Request body</span></span>

| <span data-ttu-id="e2e22-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e22-128">Parameter</span></span> | <span data-ttu-id="e2e22-129">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e22-129">Type</span></span> | <span data-ttu-id="e2e22-130">Optional?</span><span class="sxs-lookup"><span data-stu-id="e2e22-130">Optional?</span></span> | <span data-ttu-id="e2e22-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e22-131">Description</span></span> |
| :---: | :---: | :--- | :--- |
| <span data-ttu-id="e2e22-132">message</span><span class="sxs-lookup"><span data-stu-id="e2e22-132">message</span></span> | <span data-ttu-id="e2e22-133">String</span><span class="sxs-lookup"><span data-stu-id="e2e22-133">String</span></span> | <span data-ttu-id="e2e22-134">Nein</span><span class="sxs-lookup"><span data-stu-id="e2e22-134">No</span></span> | <span data-ttu-id="e2e22-135">Textnachricht (Max 1.000 Zeichen begrenzt) gesendet werden</span><span class="sxs-lookup"><span data-stu-id="e2e22-135">Text message to be sent (Max limit of 1000 Characters)</span></span> |
| <span data-ttu-id="e2e22-136">sendToAllSubscribers</span><span class="sxs-lookup"><span data-stu-id="e2e22-136">sendToAllSubscribers</span></span> | <span data-ttu-id="e2e22-137">Bool</span><span class="sxs-lookup"><span data-stu-id="e2e22-137">Bool</span></span> | <span data-ttu-id="e2e22-138">Ja</span><span class="sxs-lookup"><span data-stu-id="e2e22-138">Yes</span></span> | <span data-ttu-id="e2e22-139">Standard: false.</span><span class="sxs-lookup"><span data-stu-id="e2e22-139">Default: false.</span></span> <span data-ttu-id="e2e22-140">Gültige nur im Fall der GroupId öffentliche Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="e2e22-140">Valid only in case the groupId belongs to a Public Group.</span></span> <span data-ttu-id="e2e22-141">True, um die Text-Nachricht an alle Abonnenten senden bewirkt, dass die das Token Benutzer Admin der Gruppe der öffentlich sein</span><span class="sxs-lookup"><span data-stu-id="e2e22-141">True to send the text message to all subscribers which requires the token's user to be admin of the Public Group</span></span> |
| <span data-ttu-id="e2e22-142">Abonnenten</span><span class="sxs-lookup"><span data-stu-id="e2e22-142">subscribers</span></span> | <span data-ttu-id="e2e22-143">String]</span><span class="sxs-lookup"><span data-stu-id="e2e22-143">String[]</span></span> | <span data-ttu-id="e2e22-144">Ja</span><span class="sxs-lookup"><span data-stu-id="e2e22-144">Yes</span></span> | <span data-ttu-id="e2e22-145">Jedes Element entspricht einer Mobiltelefonnummer (mit Ländercode.</span><span class="sxs-lookup"><span data-stu-id="e2e22-145">Each element corresponds to a mobile number(with country code.</span></span> <span data-ttu-id="e2e22-146">EG.</span><span class="sxs-lookup"><span data-stu-id="e2e22-146">Eg.</span></span> <span data-ttu-id="e2e22-147">+911999999999).</span><span class="sxs-lookup"><span data-stu-id="e2e22-147">+911999999999).</span></span> <span data-ttu-id="e2e22-148">Textnachricht wird nur für die ausgewählten Abonnenten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2e22-148">Text message will be sent only to the selected subscribers.</span></span> <span data-ttu-id="e2e22-149">Für selektive Kommunikation für Abonnenten im Kontext eines öffentliche Gruppe verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="e2e22-149">To be used for selective communication to subscribers in context of a Public Group</span></span> |

###### <a name="sample-json-request"></a><span data-ttu-id="e2e22-150">Beispiel für JSON-Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2e22-150">Sample JSON Request</span></span>

```javascript
{
  "message": "Hello All! Welcome to Kaizala.",
  "subscribers": ["+911999999999","+911999999998"]
}
```

##### <a name="response-body"></a><span data-ttu-id="e2e22-151">Antworttext</span><span class="sxs-lookup"><span data-stu-id="e2e22-151">Response body</span></span>

| <span data-ttu-id="e2e22-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e22-152">Parameter</span></span> | <span data-ttu-id="e2e22-153">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e22-153">Type</span></span> | <span data-ttu-id="e2e22-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e22-154">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="e2e22-155">referenceId</span><span class="sxs-lookup"><span data-stu-id="e2e22-155">referenceId</span></span> | <span data-ttu-id="e2e22-156">String</span><span class="sxs-lookup"><span data-stu-id="e2e22-156">String</span></span> | <span data-ttu-id="e2e22-157">GUID, die nach erfolgreicher Abschluss der Anforderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2e22-157">GUID representing the succesful completion of the request</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="e2e22-158">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="e2e22-158">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```
