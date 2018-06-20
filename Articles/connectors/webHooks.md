---
title: /webhooks
description: Referenzartikel für API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: 8b78449ba41042de262bed7e3317771ef33c8031
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905388"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="10550-103">APIs für das registrieren & Webhooks verwalten</span><span class="sxs-lookup"><span data-stu-id="10550-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="10550-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="10550-104">/webhook</span></span>
<span data-ttu-id="10550-105">Zum Verwalten von Abonnements auf Ereignisse innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="10550-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="10550-106">WebHooks besteht aus einem kompakten HTTP-Muster ein einfachen Publisher-Abonnent-Modells für Verdrahtung zusammen Web-APIs und SaaS Services bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="10550-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="10550-107">Wenn ein Ereignis in Kaizala passiert, wird eine Benachrichtigung in Form von HTTP POST-Anforderung an die registrierten Abonnenten gesendet.</span><span class="sxs-lookup"><span data-stu-id="10550-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="10550-108">Die POST-Anforderung enthält Informationen über das Ereignis für den Empfänger an, entsprechend agieren kann.</span><span class="sxs-lookup"><span data-stu-id="10550-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="10550-109">WebHooks verwenden, können Sie verschiedene Abonnieren von Ereignissen, die innerhalb einer Unterhaltung Gruppe in Kaizala Kontext auftreten.</span><span class="sxs-lookup"><span data-stu-id="10550-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="10550-110">/Webhook buchen</span><span class="sxs-lookup"><span data-stu-id="10550-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="10550-111">Um sicherzustellen, dass Ihr Dienstendpunkt Webhook authentisch und betriebsbereit ist wird wir Ihr Callback-URL überprüfen, bevor Abonnement erstellen.</span><span class="sxs-lookup"><span data-stu-id="10550-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="10550-112">Zur Überprüfung werden wir Sie ein Token Validation senden, die Sie uns wieder innerhalb von 5 Sekunden senden müssen.</span><span class="sxs-lookup"><span data-stu-id="10550-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="10550-113">Erfahren Sie mehr</span><span class="sxs-lookup"><span data-stu-id="10550-113">Read More</span></span>](WebHookValidaton.md)

##### <a name="request-parameters"></a><span data-ttu-id="10550-114">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="10550-114">Request Parameters</span></span>

|  | <span data-ttu-id="10550-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-115">Parameter</span></span> | <span data-ttu-id="10550-116">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-116">Type</span></span> | <span data-ttu-id="10550-117">Optional?</span><span class="sxs-lookup"><span data-stu-id="10550-117">Optional?</span></span> | <span data-ttu-id="10550-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="10550-119">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="10550-119">HTTP Header</span></span> | <span data-ttu-id="10550-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="10550-120">accessToken</span></span> | <span data-ttu-id="10550-121">String</span><span class="sxs-lookup"><span data-stu-id="10550-121">String</span></span> | <span data-ttu-id="10550-122">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-122">No</span></span> | <span data-ttu-id="10550-123">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="10550-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="10550-124">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="10550-124">HTTP Header</span></span> | <span data-ttu-id="10550-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="10550-125">Content-Type</span></span> | <span data-ttu-id="10550-126">String</span><span class="sxs-lookup"><span data-stu-id="10550-126">String</span></span> | <span data-ttu-id="10550-127">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-127">No</span></span> | <span data-ttu-id="10550-128">"Application/Json"</span><span class="sxs-lookup"><span data-stu-id="10550-128">"application/json"</span></span> |

##### <a name="request-body"></a><span data-ttu-id="10550-129">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="10550-129">Request body</span></span>

|  <span data-ttu-id="10550-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-130">Parameter</span></span> | <span data-ttu-id="10550-131">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-131">Type</span></span> | <span data-ttu-id="10550-132">Optional?</span><span class="sxs-lookup"><span data-stu-id="10550-132">Optional?</span></span> | <span data-ttu-id="10550-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="10550-134">objectId</span><span class="sxs-lookup"><span data-stu-id="10550-134">objectId</span></span> | <span data-ttu-id="10550-135">String</span><span class="sxs-lookup"><span data-stu-id="10550-135">String</span></span> | <span data-ttu-id="10550-136">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-136">No</span></span> | <span data-ttu-id="10550-137">Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id</span><span class="sxs-lookup"><span data-stu-id="10550-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="10550-138">objectType</span><span class="sxs-lookup"><span data-stu-id="10550-138">objectType</span></span> | <span data-ttu-id="10550-139">String</span><span class="sxs-lookup"><span data-stu-id="10550-139">String</span></span> | <span data-ttu-id="10550-140">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-140">No</span></span> | <span data-ttu-id="10550-141">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="10550-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="10550-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="10550-142">eventTypes</span></span> | <span data-ttu-id="10550-143">Array</span><span class="sxs-lookup"><span data-stu-id="10550-143">Array</span></span> | <span data-ttu-id="10550-144">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-144">No</span></span> | <span data-ttu-id="10550-145">Array von verschiedenen Arten von Ereignissen, denen Sie die Webhook zu abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="10550-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="10550-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="10550-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="10550-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="10550-147">callBackUrl</span></span> | <span data-ttu-id="10550-148">String</span><span class="sxs-lookup"><span data-stu-id="10550-148">String</span></span> | <span data-ttu-id="10550-149">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-149">No</span></span> | <span data-ttu-id="10550-150">HTTPS-URL, an die die abonnierten Ereignisse, gemeldet werden müssen</span><span class="sxs-lookup"><span data-stu-id="10550-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="10550-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="10550-151">callBackToken</span></span> | <span data-ttu-id="10550-152">String</span><span class="sxs-lookup"><span data-stu-id="10550-152">String</span></span> | <span data-ttu-id="10550-153">Ja</span><span class="sxs-lookup"><span data-stu-id="10550-153">Yes</span></span> | <span data-ttu-id="10550-154">Ein optionaler Parameter können Sie festlegen, die im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="10550-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="10550-155">callBackContext</span><span class="sxs-lookup"><span data-stu-id="10550-155">callBackContext</span></span> | <span data-ttu-id="10550-156">String</span><span class="sxs-lookup"><span data-stu-id="10550-156">String</span></span> | <span data-ttu-id="10550-157">Ja</span><span class="sxs-lookup"><span data-stu-id="10550-157">Yes</span></span> | <span data-ttu-id="10550-158">Ein optionaler Parameter können Sie festlegen, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="10550-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="10550-159">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="10550-159">validity</span></span> | <span data-ttu-id="10550-160">String</span><span class="sxs-lookup"><span data-stu-id="10550-160">String</span></span> | <span data-ttu-id="10550-161">Ja</span><span class="sxs-lookup"><span data-stu-id="10550-161">Yes</span></span> | <span data-ttu-id="10550-162">Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="10550-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="10550-163">Der Standardwert lautet 2 Jahre</span><span class="sxs-lookup"><span data-stu-id="10550-163">Default is 2 years</span></span> |


##### <a name="response-body"></a><span data-ttu-id="10550-164">Antworttext</span><span class="sxs-lookup"><span data-stu-id="10550-164">Response body</span></span>
| <span data-ttu-id="10550-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-165">Parameter</span></span> | <span data-ttu-id="10550-166">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-166">Type</span></span> | <span data-ttu-id="10550-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="10550-168">webhookId</span><span class="sxs-lookup"><span data-stu-id="10550-168">webhookId</span></span> | <span data-ttu-id="10550-169">String</span><span class="sxs-lookup"><span data-stu-id="10550-169">String</span></span> | <span data-ttu-id="10550-170">Bezeichner für die WebHook erstellt</span><span class="sxs-lookup"><span data-stu-id="10550-170">Identifier representing the webHook created</span></span> |

##### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="10550-171">Anforderungstextkörper - alle Ereignisse auf Gruppenebene abonnieren</span><span class="sxs-lookup"><span data-stu-id="10550-171">Request Body - Subscribe to all events at group level</span></span>

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


<span data-ttu-id="10550-172">Finden Sie Webhook Antwortschema für registrierte Ereignisse in Kaizala [**hier**](EventSchema.md).</span><span class="sxs-lookup"><span data-stu-id="10550-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

### <a name="get-webhook"></a><span data-ttu-id="10550-173">Abrufen von /webhook</span><span class="sxs-lookup"><span data-stu-id="10550-173">Get /webhook</span></span>

    GET {endpoint-url}/v1/webhook

##### <a name="request-parameters"></a><span data-ttu-id="10550-174">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="10550-174">Request Parameters</span></span>


|  | <span data-ttu-id="10550-175">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-175">Parameter</span></span> | <span data-ttu-id="10550-176">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-176">Type</span></span> | <span data-ttu-id="10550-177">Optional?</span><span class="sxs-lookup"><span data-stu-id="10550-177">Optional?</span></span> | <span data-ttu-id="10550-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-178">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="10550-179">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="10550-179">HTTP Header</span></span> | <span data-ttu-id="10550-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="10550-180">accessToken</span></span> | <span data-ttu-id="10550-181">String</span><span class="sxs-lookup"><span data-stu-id="10550-181">String</span></span> | <span data-ttu-id="10550-182">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-182">No</span></span> | <span data-ttu-id="10550-183">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="10550-183">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="10550-184">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="10550-184">Query parameter</span></span> | <span data-ttu-id="10550-185">objectId</span><span class="sxs-lookup"><span data-stu-id="10550-185">objectId</span></span> | <span data-ttu-id="10550-186">String</span><span class="sxs-lookup"><span data-stu-id="10550-186">String</span></span> | <span data-ttu-id="10550-187">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-187">No</span></span> | <span data-ttu-id="10550-188">Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id</span><span class="sxs-lookup"><span data-stu-id="10550-188">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="10550-189">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="10550-189">Query parameter</span></span> | <span data-ttu-id="10550-190">objectType</span><span class="sxs-lookup"><span data-stu-id="10550-190">objectType</span></span> | <span data-ttu-id="10550-191">String</span><span class="sxs-lookup"><span data-stu-id="10550-191">String</span></span> | <span data-ttu-id="10550-192">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-192">No</span></span> | <span data-ttu-id="10550-193">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="10550-193">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

##### <a name="response-body"></a><span data-ttu-id="10550-194">Antworttext</span><span class="sxs-lookup"><span data-stu-id="10550-194">Response body</span></span>

| <span data-ttu-id="10550-195">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-195">Parameter</span></span> | <span data-ttu-id="10550-196">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-196">Type</span></span> | <span data-ttu-id="10550-197">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-197">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="10550-198">webhooks</span><span class="sxs-lookup"><span data-stu-id="10550-198">webhooks</span></span> | <span data-ttu-id="10550-199">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="10550-199">JSON Object Array</span></span> | <span data-ttu-id="10550-200">Array von Webhooks auf ObjectId abonniert</span><span class="sxs-lookup"><span data-stu-id="10550-200">Array of webhooks subscribed on the objectId</span></span> |

######  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="10550-201">JSON-Struktur für jede einzelne Webhook in das Array Webhooks []:</span><span class="sxs-lookup"><span data-stu-id="10550-201">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="10550-202">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-202">Parameter</span></span> | <span data-ttu-id="10550-203">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-203">Type</span></span> | <span data-ttu-id="10550-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-204">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="10550-205">id</span><span class="sxs-lookup"><span data-stu-id="10550-205">id</span></span> | <span data-ttu-id="10550-206">String</span><span class="sxs-lookup"><span data-stu-id="10550-206">String</span></span> | <span data-ttu-id="10550-207">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="10550-207">Webhook Identifier</span></span> |
| <span data-ttu-id="10550-208">objectId</span><span class="sxs-lookup"><span data-stu-id="10550-208">objectId</span></span> | <span data-ttu-id="10550-209">String</span><span class="sxs-lookup"><span data-stu-id="10550-209">String</span></span> | <span data-ttu-id="10550-210">Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="10550-210">Object Identifier</span></span> |
| <span data-ttu-id="10550-211">objectType</span><span class="sxs-lookup"><span data-stu-id="10550-211">objectType</span></span> | <span data-ttu-id="10550-212">String</span><span class="sxs-lookup"><span data-stu-id="10550-212">String</span></span> | <span data-ttu-id="10550-213">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="10550-213">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="10550-214">events</span><span class="sxs-lookup"><span data-stu-id="10550-214">events</span></span> | <span data-ttu-id="10550-215">String]</span><span class="sxs-lookup"><span data-stu-id="10550-215">String[]</span></span> | <span data-ttu-id="10550-216">Ereignisliste mit jedem Wert als eines der "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ankündigung", "MemberAdded", "MemberRemoved", "GroupAdded" " GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="10550-216">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="10550-217">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="10550-217">callBackUrl</span></span> | <span data-ttu-id="10550-218">String</span><span class="sxs-lookup"><span data-stu-id="10550-218">String</span></span> | <span data-ttu-id="10550-219">Callback-URL an die die abonnierten Ereignisse, gemeldet werden müssen</span><span class="sxs-lookup"><span data-stu-id="10550-219">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="10550-220">callBackToken</span><span class="sxs-lookup"><span data-stu-id="10550-220">callBackToken</span></span> | <span data-ttu-id="10550-221">String</span><span class="sxs-lookup"><span data-stu-id="10550-221">String</span></span> | <span data-ttu-id="10550-222">Parameter der im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="10550-222">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="10550-223">callBackContext</span><span class="sxs-lookup"><span data-stu-id="10550-223">callBackContext</span></span> | <span data-ttu-id="10550-224">String</span><span class="sxs-lookup"><span data-stu-id="10550-224">String</span></span> | <span data-ttu-id="10550-225">Parameter, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet</span><span class="sxs-lookup"><span data-stu-id="10550-225">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="10550-226">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="10550-226">validity</span></span> | <span data-ttu-id="10550-227">String</span><span class="sxs-lookup"><span data-stu-id="10550-227">String</span></span> | <span data-ttu-id="10550-228">Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="10550-228">Validity for the WebHook to be active in EPOCH format.</span></span> |

###### <a name="sample-json-response"></a><span data-ttu-id="10550-229">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="10550-229">Sample JSON Response</span></span>

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
        }
    ]
}
```

### <a name="delete-webhook"></a><span data-ttu-id="10550-230">/Webhook löschen</span><span class="sxs-lookup"><span data-stu-id="10550-230">Delete /webhook</span></span>

    DELETE {endpoint-url}/v1/webhook

##### <a name="request-parameters"></a><span data-ttu-id="10550-231">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="10550-231">Request Parameters</span></span>
|  | <span data-ttu-id="10550-232">Parameter</span><span class="sxs-lookup"><span data-stu-id="10550-232">Parameter</span></span> | <span data-ttu-id="10550-233">Typ</span><span class="sxs-lookup"><span data-stu-id="10550-233">Type</span></span> | <span data-ttu-id="10550-234">Optional?</span><span class="sxs-lookup"><span data-stu-id="10550-234">Optional?</span></span> | <span data-ttu-id="10550-235">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10550-235">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="10550-236">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="10550-236">HTTP Header</span></span> | <span data-ttu-id="10550-237">accessToken</span><span class="sxs-lookup"><span data-stu-id="10550-237">accessToken</span></span> | <span data-ttu-id="10550-238">String</span><span class="sxs-lookup"><span data-stu-id="10550-238">String</span></span> | <span data-ttu-id="10550-239">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-239">No</span></span> | <span data-ttu-id="10550-240">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="10550-240">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="10550-241">Pfadparameter</span><span class="sxs-lookup"><span data-stu-id="10550-241">Path parameter</span></span> | <span data-ttu-id="10550-242">webhookId</span><span class="sxs-lookup"><span data-stu-id="10550-242">webhookId</span></span> | <span data-ttu-id="10550-243">String</span><span class="sxs-lookup"><span data-stu-id="10550-243">String</span></span> | <span data-ttu-id="10550-244">Nein</span><span class="sxs-lookup"><span data-stu-id="10550-244">No</span></span> | <span data-ttu-id="10550-245">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="10550-245">Webhook Identifier</span></span> |
