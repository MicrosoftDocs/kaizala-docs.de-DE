---
title: /webhooks
description: Referenzartikel zur API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: a2cdb74284f6980644366cf3b61740ea46389512
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190732"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="9695e-103">APIs zum Registrieren von & Manage webhooks</span><span class="sxs-lookup"><span data-stu-id="9695e-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="9695e-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="9695e-104">/webhook</span></span>
<span data-ttu-id="9695e-105">API-Endpunkt zum Verwalten von Abonnements für Ereignisse in Kaizala.</span><span class="sxs-lookup"><span data-stu-id="9695e-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="9695e-106">WebHooks ist ein leichtes HTTP-Muster, das ein einfaches Publisher/Subscriber-Modell für die Verbindung von Web-APIs und SaaS-Diensten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9695e-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="9695e-107">Wenn in Kaizala ein Ereignis auftritt, wird eine Benachrichtigung in Form einer HTTP-POST-Anforderung an registrierte Abonnenten gesendet.</span><span class="sxs-lookup"><span data-stu-id="9695e-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="9695e-108">Die POST-Anforderung enthält Informationen über das Ereignis, mit denen der Empfänger entsprechend handeln kann.</span><span class="sxs-lookup"><span data-stu-id="9695e-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="9695e-109">Mit webHooks können Sie verschiedene Ereignisse abonnieren, die innerhalb eines unterhaltungsgruppen Kontexts in Kaizala auftreten.</span><span class="sxs-lookup"><span data-stu-id="9695e-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="9695e-110">POST/webhook</span><span class="sxs-lookup"><span data-stu-id="9695e-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="9695e-111">Um sicherzustellen, dass Ihr webhook-Dienstendpunkt authentisch ist und funktioniert, überprüfen wir Ihre Rückruf-URL, bevor Sie ein Abonnement erstellen.</span><span class="sxs-lookup"><span data-stu-id="9695e-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="9695e-112">Zur Überprüfung senden wir Ihnen ein Validierungs Token zu, das Sie innerhalb von 5 Sekunden zurücksenden müssen.</span><span class="sxs-lookup"><span data-stu-id="9695e-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="9695e-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9695e-113">Read More</span></span>](WebHookValidaton.md)

#### <a name="request-parameters"></a><span data-ttu-id="9695e-114">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="9695e-114">Request Parameters</span></span>

|  | <span data-ttu-id="9695e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-115">Parameter</span></span> | <span data-ttu-id="9695e-116">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-116">Type</span></span> | <span data-ttu-id="9695e-117">Optional?</span><span class="sxs-lookup"><span data-stu-id="9695e-117">Optional?</span></span> | <span data-ttu-id="9695e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9695e-119">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9695e-119">HTTP Header</span></span> | <span data-ttu-id="9695e-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="9695e-120">accessToken</span></span> | <span data-ttu-id="9695e-121">String</span><span class="sxs-lookup"><span data-stu-id="9695e-121">String</span></span> | <span data-ttu-id="9695e-122">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-122">No</span></span> | <span data-ttu-id="9695e-123">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="9695e-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="9695e-124">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9695e-124">HTTP Header</span></span> | <span data-ttu-id="9695e-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9695e-125">Content-Type</span></span> | <span data-ttu-id="9695e-126">String</span><span class="sxs-lookup"><span data-stu-id="9695e-126">String</span></span> | <span data-ttu-id="9695e-127">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-127">No</span></span> | <span data-ttu-id="9695e-128">"application/json"</span><span class="sxs-lookup"><span data-stu-id="9695e-128">"application/json"</span></span> |

#### <a name="request-body"></a><span data-ttu-id="9695e-129">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="9695e-129">Request body</span></span>

|  <span data-ttu-id="9695e-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-130">Parameter</span></span> | <span data-ttu-id="9695e-131">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-131">Type</span></span> | <span data-ttu-id="9695e-132">Optional?</span><span class="sxs-lookup"><span data-stu-id="9695e-132">Optional?</span></span> | <span data-ttu-id="9695e-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="9695e-134">objectId</span><span class="sxs-lookup"><span data-stu-id="9695e-134">objectId</span></span> | <span data-ttu-id="9695e-135">String</span><span class="sxs-lookup"><span data-stu-id="9695e-135">String</span></span> | <span data-ttu-id="9695e-136">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-136">No</span></span> | <span data-ttu-id="9695e-137">Bezeichner, der das Objekt darstellt, in dem der Kontext der webhooks erstellt werden muss. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier</span><span class="sxs-lookup"><span data-stu-id="9695e-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="9695e-138">objectType</span><span class="sxs-lookup"><span data-stu-id="9695e-138">objectType</span></span> | <span data-ttu-id="9695e-139">String</span><span class="sxs-lookup"><span data-stu-id="9695e-139">String</span></span> | <span data-ttu-id="9695e-140">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-140">No</span></span> | <span data-ttu-id="9695e-141">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="9695e-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="9695e-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="9695e-142">eventTypes</span></span> | <span data-ttu-id="9695e-143">Array</span><span class="sxs-lookup"><span data-stu-id="9695e-143">Array</span></span> | <span data-ttu-id="9695e-144">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-144">No</span></span> | <span data-ttu-id="9695e-145">Array unterschiedlicher Ereignistypen, für die Sie den webhook abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="9695e-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="9695e-146">Unterstützte Ereignisse sind folgende: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ansage", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="9695e-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="9695e-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="9695e-147">callBackUrl</span></span> | <span data-ttu-id="9695e-148">String</span><span class="sxs-lookup"><span data-stu-id="9695e-148">String</span></span> | <span data-ttu-id="9695e-149">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-149">No</span></span> | <span data-ttu-id="9695e-150">HTTPS-URL, an die die abonnierten Ereignisse benachrichtigt werden müssen</span><span class="sxs-lookup"><span data-stu-id="9695e-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="9695e-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="9695e-151">callBackToken</span></span> | <span data-ttu-id="9695e-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-152">String</span></span> | <span data-ttu-id="9695e-153">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-153">Yes</span></span> | <span data-ttu-id="9695e-154">Optionaler Parameter, den Sie festlegen können, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf des webHooks gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="9695e-155">callBackcontext</span><span class="sxs-lookup"><span data-stu-id="9695e-155">callBackContext</span></span> | <span data-ttu-id="9695e-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-156">String</span></span> | <span data-ttu-id="9695e-157">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-157">Yes</span></span> | <span data-ttu-id="9695e-158">Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als ' context ' gesendet wird, bei jedem Rückruf, der vom webHook ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="9695e-159">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="9695e-159">validity</span></span> | <span data-ttu-id="9695e-160">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-160">String</span></span> | <span data-ttu-id="9695e-161">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-161">Yes</span></span> | <span data-ttu-id="9695e-162">Gültigkeit für die webHook-Aktivität im EPOCH-Format.</span><span class="sxs-lookup"><span data-stu-id="9695e-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="9695e-163">Standardwert ist 2 Jahre</span><span class="sxs-lookup"><span data-stu-id="9695e-163">Default is 2 years</span></span> |


#### <a name="response-body"></a><span data-ttu-id="9695e-164">Antworttext</span><span class="sxs-lookup"><span data-stu-id="9695e-164">Response body</span></span>
| <span data-ttu-id="9695e-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-165">Parameter</span></span> | <span data-ttu-id="9695e-166">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-166">Type</span></span> | <span data-ttu-id="9695e-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9695e-168">webhook-Nr.</span><span class="sxs-lookup"><span data-stu-id="9695e-168">webhookId</span></span> | <span data-ttu-id="9695e-169">String</span><span class="sxs-lookup"><span data-stu-id="9695e-169">String</span></span> | <span data-ttu-id="9695e-170">Bezeichner, der den erstellten webHook darstellt</span><span class="sxs-lookup"><span data-stu-id="9695e-170">Identifier representing the webHook created</span></span> |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="9695e-171">AnforderungsText – abonnieren aller Ereignisse auf Gruppenebene</span><span class="sxs-lookup"><span data-stu-id="9695e-171">Request Body - Subscribe to all events at group level</span></span>

```javascript
{  
   "objectId":"74943849802190eaea3810",
   "objectType":"Group",
   "eventTypes":[
      "ActionCreated",
      "ActionResponse",
      "SurveyCreated",
      "JobCreated",
      "SurveyResponse",
      "JobResponse",
      "TextMessageCreated",
      "AttachmentCreated",
      "Announcement",
      "MemberAdded",
      "MemberRemoved",
      "GroupAdded",
      "GroupRemoved"
   ],
   "callBackUrl":"https://requestb.in/123",
   "callBackToken":"tokenToBeVerifiedByCallback",
   "callBackContext":"Any data which is required to be returned in callback"
}

```


<span data-ttu-id="9695e-172">Das webhook-Antwortschema für registrierte Ereignisse in Kaizala finden Sie [**hier**](EventSchema.md).</span><span class="sxs-lookup"><span data-stu-id="9695e-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

> <span data-ttu-id="9695e-173">**Hinweis:** Kaizala garantiert, dass die webhook-Antwort mindestens einmal bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-173">**Note:** Kaizala guarantees at-least once delivery of webhook response.</span></span> <span data-ttu-id="9695e-174">In bestimmten Fällen kann es vorkommen, dass Kaizala doppelte webhook-Antwort für dasselbe Ereignis sendet.</span><span class="sxs-lookup"><span data-stu-id="9695e-174">It may happen, in certain cases, that Kaizala may send duplicate webhook response for the same event.</span></span>

### <a name="get-webhook"></a><span data-ttu-id="9695e-175">/Webhook abrufen</span><span class="sxs-lookup"><span data-stu-id="9695e-175">Get /webhook</span></span>

    <span data-ttu-id="9695e-176">GET {Endpoint-URL}/v1/webhook</span><span class="sxs-lookup"><span data-stu-id="9695e-176">GET {endpoint-url}/v1/webhook</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="9695e-177">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="9695e-177">Request Parameters</span></span>


|  | <span data-ttu-id="9695e-178">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-178">Parameter</span></span> | <span data-ttu-id="9695e-179">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-179">Type</span></span> | <span data-ttu-id="9695e-180">Optional?</span><span class="sxs-lookup"><span data-stu-id="9695e-180">Optional?</span></span> | <span data-ttu-id="9695e-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-181">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9695e-182">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9695e-182">HTTP Header</span></span> | <span data-ttu-id="9695e-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="9695e-183">accessToken</span></span> | <span data-ttu-id="9695e-184">String</span><span class="sxs-lookup"><span data-stu-id="9695e-184">String</span></span> | <span data-ttu-id="9695e-185">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-185">No</span></span> | <span data-ttu-id="9695e-186">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="9695e-186">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="9695e-187">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="9695e-187">Query parameter</span></span> | <span data-ttu-id="9695e-188">objectId</span><span class="sxs-lookup"><span data-stu-id="9695e-188">objectId</span></span> | <span data-ttu-id="9695e-189">String</span><span class="sxs-lookup"><span data-stu-id="9695e-189">String</span></span> | <span data-ttu-id="9695e-190">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-190">No</span></span> | <span data-ttu-id="9695e-191">Bezeichner, der das Objekt darstellt, in dem der Kontext der webhooks erstellt werden muss. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier</span><span class="sxs-lookup"><span data-stu-id="9695e-191">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="9695e-192">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="9695e-192">Query parameter</span></span> | <span data-ttu-id="9695e-193">objectType</span><span class="sxs-lookup"><span data-stu-id="9695e-193">objectType</span></span> | <span data-ttu-id="9695e-194">String</span><span class="sxs-lookup"><span data-stu-id="9695e-194">String</span></span> | <span data-ttu-id="9695e-195">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-195">No</span></span> | <span data-ttu-id="9695e-196">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="9695e-196">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

#### <a name="response-body"></a><span data-ttu-id="9695e-197">Antworttext</span><span class="sxs-lookup"><span data-stu-id="9695e-197">Response body</span></span>

| <span data-ttu-id="9695e-198">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-198">Parameter</span></span> | <span data-ttu-id="9695e-199">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-199">Type</span></span> | <span data-ttu-id="9695e-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9695e-201">webhooks</span><span class="sxs-lookup"><span data-stu-id="9695e-201">webhooks</span></span> | <span data-ttu-id="9695e-202">JSON-Objekt Array</span><span class="sxs-lookup"><span data-stu-id="9695e-202">JSON Object Array</span></span> | <span data-ttu-id="9695e-203">Array von webhooks, die für die objectId abonniert wurden</span><span class="sxs-lookup"><span data-stu-id="9695e-203">Array of webhooks subscribed on the objectId</span></span> |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="9695e-204">JSON-Struktur für jeden einzelnen webhook im Array webhooks []:</span><span class="sxs-lookup"><span data-stu-id="9695e-204">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="9695e-205">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-205">Parameter</span></span> | <span data-ttu-id="9695e-206">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-206">Type</span></span> | <span data-ttu-id="9695e-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-207">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="9695e-208">id</span><span class="sxs-lookup"><span data-stu-id="9695e-208">id</span></span> | <span data-ttu-id="9695e-209">String</span><span class="sxs-lookup"><span data-stu-id="9695e-209">String</span></span> | <span data-ttu-id="9695e-210">Webhook-ID</span><span class="sxs-lookup"><span data-stu-id="9695e-210">Webhook Identifier</span></span> |
| <span data-ttu-id="9695e-211">objectId</span><span class="sxs-lookup"><span data-stu-id="9695e-211">objectId</span></span> | <span data-ttu-id="9695e-212">String</span><span class="sxs-lookup"><span data-stu-id="9695e-212">String</span></span> | <span data-ttu-id="9695e-213">Objektbezeichner</span><span class="sxs-lookup"><span data-stu-id="9695e-213">Object Identifier</span></span> |
| <span data-ttu-id="9695e-214">objectType</span><span class="sxs-lookup"><span data-stu-id="9695e-214">objectType</span></span> | <span data-ttu-id="9695e-215">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-215">String</span></span> | <span data-ttu-id="9695e-216">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="9695e-216">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="9695e-217">events</span><span class="sxs-lookup"><span data-stu-id="9695e-217">events</span></span> | <span data-ttu-id="9695e-218">String []</span><span class="sxs-lookup"><span data-stu-id="9695e-218">String[]</span></span> | <span data-ttu-id="9695e-219">Ereignisliste mit jedem Wert von "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ansage", "MemberAdded", "MemberRemoved", "GroupAdded"; " GroupRemoved "</span><span class="sxs-lookup"><span data-stu-id="9695e-219">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="9695e-220">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="9695e-220">callBackUrl</span></span> | <span data-ttu-id="9695e-221">String</span><span class="sxs-lookup"><span data-stu-id="9695e-221">String</span></span> | <span data-ttu-id="9695e-222">Rückruf-URL, an die die abonnierten Ereignisse benachrichtigt werden müssen</span><span class="sxs-lookup"><span data-stu-id="9695e-222">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="9695e-223">callBackToken</span><span class="sxs-lookup"><span data-stu-id="9695e-223">callBackToken</span></span> | <span data-ttu-id="9695e-224">String</span><span class="sxs-lookup"><span data-stu-id="9695e-224">String</span></span> | <span data-ttu-id="9695e-225">Parameter, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf des webHooks gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-225">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="9695e-226">callBackcontext</span><span class="sxs-lookup"><span data-stu-id="9695e-226">callBackContext</span></span> | <span data-ttu-id="9695e-227">String</span><span class="sxs-lookup"><span data-stu-id="9695e-227">String</span></span> | <span data-ttu-id="9695e-228">Parameter, der in der JSON-Nutzlast als "Context" gesendet wird und jeder Rückruf durch den webHook erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9695e-228">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="9695e-229">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="9695e-229">validity</span></span> | <span data-ttu-id="9695e-230">String</span><span class="sxs-lookup"><span data-stu-id="9695e-230">String</span></span> | <span data-ttu-id="9695e-231">Gültigkeit für die webHook-Aktivität im EPOCH-Format.</span><span class="sxs-lookup"><span data-stu-id="9695e-231">Validity for the WebHook to be active in EPOCH format.</span></span> |
| <span data-ttu-id="9695e-232">Active</span><span class="sxs-lookup"><span data-stu-id="9695e-232">active</span></span> | <span data-ttu-id="9695e-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="9695e-233">Boolean</span></span> | <span data-ttu-id="9695e-234">True, wenn der Status von webhook aktiv ist</span><span class="sxs-lookup"><span data-stu-id="9695e-234">True, if the state of webhook is active</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="9695e-235">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="9695e-235">Sample JSON Response</span></span>

```javascript
{
    "webhooks": [
        {
            "id": "dac6fccf-f2e9-4abc-94d7-793037e99da7",
            "objectId": "b21405d1-4b10-4c46-bfa9-8338592f3782",
            "objectType": "Group",
            "events": [
                "ActionCreated",
                "ActionResponse",
                "SurveyCreated",
                "JobCreated",
                "SurveyResponse",
                "JobResponse",
                "TextMessageCreated",
                "AttachmentCreated",
                "Announcement",
                "MemberAdded",
                "MemberRemoved",
                "GroupAdded",
                "GroupRemoved"
            ],
            "filters": [],
            "callbackUrl": "https://requestb.in/12786un1",
            "callbackToken": "tokenToBeVerifiedByCallback",
            "ts": 1505491564677,
            "validity": 1568605416677
            "active": true
        }
    ]
}
```

### <a name="delete-webhook"></a><span data-ttu-id="9695e-236">/Webhook löschen</span><span class="sxs-lookup"><span data-stu-id="9695e-236">Delete /webhook</span></span>

    <span data-ttu-id="9695e-237">DELETE {Endpoint-URL}/v1/webhook</span><span class="sxs-lookup"><span data-stu-id="9695e-237">DELETE {endpoint-url}/v1/webhook</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="9695e-238">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="9695e-238">Request Parameters</span></span>
|  | <span data-ttu-id="9695e-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-239">Parameter</span></span> | <span data-ttu-id="9695e-240">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-240">Type</span></span> | <span data-ttu-id="9695e-241">Optional?</span><span class="sxs-lookup"><span data-stu-id="9695e-241">Optional?</span></span> | <span data-ttu-id="9695e-242">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-242">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9695e-243">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9695e-243">HTTP Header</span></span> | <span data-ttu-id="9695e-244">accessToken</span><span class="sxs-lookup"><span data-stu-id="9695e-244">accessToken</span></span> | <span data-ttu-id="9695e-245">String</span><span class="sxs-lookup"><span data-stu-id="9695e-245">String</span></span> | <span data-ttu-id="9695e-246">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-246">No</span></span> | <span data-ttu-id="9695e-247">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="9695e-247">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="9695e-248">Path-Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-248">Path parameter</span></span> | <span data-ttu-id="9695e-249">webhook-Nr.</span><span class="sxs-lookup"><span data-stu-id="9695e-249">webhookId</span></span> | <span data-ttu-id="9695e-250">String</span><span class="sxs-lookup"><span data-stu-id="9695e-250">String</span></span> | <span data-ttu-id="9695e-251">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-251">No</span></span> | <span data-ttu-id="9695e-252">Webhook-ID</span><span class="sxs-lookup"><span data-stu-id="9695e-252">Webhook Identifier</span></span> |

### <a name="put-webhook"></a><span data-ttu-id="9695e-253">PUT/webhook</span><span class="sxs-lookup"><span data-stu-id="9695e-253">PUT /webhook</span></span>

    PUT {endpoint-url}/v1/webhook/{webhookId}

<span data-ttu-id="9695e-254">Jeder Parameter für den webhook kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9695e-254">Any parameter for the webhook can be updated.</span></span> <span data-ttu-id="9695e-255">Der AnforderungsText kann je nach Bedarf 1 oder mehr Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="9695e-255">Request Body may contain 1 or more parameters, as needed.</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="9695e-256">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="9695e-256">Request Parameters</span></span>

|  | <span data-ttu-id="9695e-257">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-257">Parameter</span></span> | <span data-ttu-id="9695e-258">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-258">Type</span></span> | <span data-ttu-id="9695e-259">Optional?</span><span class="sxs-lookup"><span data-stu-id="9695e-259">Optional?</span></span> | <span data-ttu-id="9695e-260">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-260">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="9695e-261">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="9695e-261">HTTP Header</span></span> | <span data-ttu-id="9695e-262">accessToken</span><span class="sxs-lookup"><span data-stu-id="9695e-262">accessToken</span></span> | <span data-ttu-id="9695e-263">String</span><span class="sxs-lookup"><span data-stu-id="9695e-263">String</span></span> | <span data-ttu-id="9695e-264">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-264">No</span></span> | <span data-ttu-id="9695e-265">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="9695e-265">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="9695e-266">Path-Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-266">Path parameter</span></span> | <span data-ttu-id="9695e-267">webhook-Nr.</span><span class="sxs-lookup"><span data-stu-id="9695e-267">webhookId</span></span> | <span data-ttu-id="9695e-268">String</span><span class="sxs-lookup"><span data-stu-id="9695e-268">String</span></span> | <span data-ttu-id="9695e-269">Nein</span><span class="sxs-lookup"><span data-stu-id="9695e-269">No</span></span> | <span data-ttu-id="9695e-270">Webhook-ID</span><span class="sxs-lookup"><span data-stu-id="9695e-270">Webhook Identifier</span></span> |

#### <a name="request-body"></a><span data-ttu-id="9695e-271">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="9695e-271">Request body</span></span>

|  <span data-ttu-id="9695e-272">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695e-272">Parameter</span></span> | <span data-ttu-id="9695e-273">Typ</span><span class="sxs-lookup"><span data-stu-id="9695e-273">Type</span></span> | <span data-ttu-id="9695e-274">Optional?</span><span class="sxs-lookup"><span data-stu-id="9695e-274">Optional?</span></span> | <span data-ttu-id="9695e-275">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9695e-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="9695e-276">objectId</span><span class="sxs-lookup"><span data-stu-id="9695e-276">objectId</span></span> | <span data-ttu-id="9695e-277">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-277">String</span></span> | <span data-ttu-id="9695e-278">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-278">Yes</span></span> | <span data-ttu-id="9695e-279">Bezeichner, der das Objekt darstellt, in dem der Kontext der webhooks erstellt werden muss. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier</span><span class="sxs-lookup"><span data-stu-id="9695e-279">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="9695e-280">objectType</span><span class="sxs-lookup"><span data-stu-id="9695e-280">objectType</span></span> | <span data-ttu-id="9695e-281">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-281">String</span></span> | <span data-ttu-id="9695e-282">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-282">Yes</span></span> | <span data-ttu-id="9695e-283">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="9695e-283">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="9695e-284">eventTypes</span><span class="sxs-lookup"><span data-stu-id="9695e-284">eventTypes</span></span> | <span data-ttu-id="9695e-285">Array</span><span class="sxs-lookup"><span data-stu-id="9695e-285">Array</span></span> | <span data-ttu-id="9695e-286">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-286">Yes</span></span> | <span data-ttu-id="9695e-287">Array unterschiedlicher Ereignistypen, für die Sie den webhook abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="9695e-287">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="9695e-288">Unterstützte Ereignisse sind folgende: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ansage", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="9695e-288">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="9695e-289">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="9695e-289">callBackUrl</span></span> | <span data-ttu-id="9695e-290">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-290">String</span></span> | <span data-ttu-id="9695e-291">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-291">Yes</span></span> | <span data-ttu-id="9695e-292">HTTPS-URL, an die die abonnierten Ereignisse benachrichtigt werden müssen</span><span class="sxs-lookup"><span data-stu-id="9695e-292">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="9695e-293">callBackToken</span><span class="sxs-lookup"><span data-stu-id="9695e-293">callBackToken</span></span> | <span data-ttu-id="9695e-294">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-294">String</span></span> | <span data-ttu-id="9695e-295">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-295">Yes</span></span> | <span data-ttu-id="9695e-296">Optionaler Parameter, den Sie festlegen können, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf des webHooks gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-296">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="9695e-297">callBackcontext</span><span class="sxs-lookup"><span data-stu-id="9695e-297">callBackContext</span></span> | <span data-ttu-id="9695e-298">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9695e-298">String</span></span> | <span data-ttu-id="9695e-299">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-299">Yes</span></span> | <span data-ttu-id="9695e-300">Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als ' context ' gesendet wird, bei jedem Rückruf, der vom webHook ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-300">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="9695e-301">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="9695e-301">validity</span></span> | <span data-ttu-id="9695e-302">String</span><span class="sxs-lookup"><span data-stu-id="9695e-302">String</span></span> | <span data-ttu-id="9695e-303">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-303">Yes</span></span> | <span data-ttu-id="9695e-304">Gültigkeit für die webHook-Aktivität im EPOCH-Format.</span><span class="sxs-lookup"><span data-stu-id="9695e-304">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="9695e-305">Standardwert ist 2 Jahre</span><span class="sxs-lookup"><span data-stu-id="9695e-305">Default is 2 years</span></span> |
| <span data-ttu-id="9695e-306">Aktiv</span><span class="sxs-lookup"><span data-stu-id="9695e-306">Active</span></span> | <span data-ttu-id="9695e-307">Boolean</span><span class="sxs-lookup"><span data-stu-id="9695e-307">Boolean</span></span> | <span data-ttu-id="9695e-308">Ja</span><span class="sxs-lookup"><span data-stu-id="9695e-308">Yes</span></span> | <span data-ttu-id="9695e-309">Ändern Sie den Zustand der webhook in aktiv, wenn der Wert true ist</span><span class="sxs-lookup"><span data-stu-id="9695e-309">Change the state of webhook to Active, if the value is true</span></span> |


#### <a name="sample-request-body"></a><span data-ttu-id="9695e-310">Beispiel für AnforderungsText</span><span class="sxs-lookup"><span data-stu-id="9695e-310">Sample Request Body</span></span>

````javascript
    { 
       "objectId":"74943849802190eaea3810",
       "objectType":"Group",
       "eventTypes":[
          "ActionCreated",
          "ActionResponse",
          "SurveyCreated",
          "JobCreated",
          "SurveyResponse",
          "JobResponse",
          "TextMessageCreated",
          "AttachmentCreated",
          "Announcement",
          "MemberAdded",
          "MemberRemoved",
          "GroupAdded",
          "GroupRemoved"
       ],
       "callBackUrl":"https://requestb.in/123",
       "callBackToken":"tokenToBeVerifiedByCallback",
      "Active": "true" 
    } 

````

## <a name="auto-disable-of-webhooks"></a><span data-ttu-id="9695e-311">Automatische deAktivierung von webhooks</span><span class="sxs-lookup"><span data-stu-id="9695e-311">Auto-Disable of Webhooks</span></span>

<span data-ttu-id="9695e-312">Zur Verbesserung der Zuverlässigkeit unserer webhooks haben wir vor kurzem die Wiederholungs-und deAktivierungs Logik hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9695e-312">To improve the Reliability of our Webhooks, we recently have added the Retry and Disabling Logic.</span></span> <span data-ttu-id="9695e-313">Die mit einem webhook registrierte Callback-URL/-Endpunkt, wenn Sie nicht erreichbar ist oder nicht mit einem anderen Statuscode als 2xx (> = 3xx) antwortet, dann versucht unser Dienst, es sechs Mal exponentiell innerhalb einer Spanne von 2 Tagen zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="9695e-313">The Callback Url/Endpoint registered with a webhook, if not reachable or does not respond with a status code other than 2xx (>=3xx), then our Service will try to reach/retry it for 6 times in an exponential way within a span of 2 Days.</span></span> 

<span data-ttu-id="9695e-314">Wenn es noch 2 Tage fehlschlägt, wird der entsprechende webhook deaktiviert, und der Besitzer muss es mit der Put-/webhook-API aktualisieren, bevor es wieder beginnt zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9695e-314">If it is still failing for 2 days, then the corresponding Webhook will be disabled, and the owner needs to update it with the Put /webhook API before it starts working again.</span></span> <span data-ttu-id="9695e-315">Beispielsweise</span><span class="sxs-lookup"><span data-stu-id="9695e-315">For e.g.</span></span>

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a><span data-ttu-id="9695e-316">AnforderungsText:</span><span class="sxs-lookup"><span data-stu-id="9695e-316">Request Body:</span></span>
````javascript
{ 
  "Active": "true" 
} 
````
