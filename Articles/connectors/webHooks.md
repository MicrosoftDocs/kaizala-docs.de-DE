---
title: /webhooks
description: Referenzartikel für API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: 00cbca686e8948d61425f067356e8c7eadb1892c
ms.sourcegitcommit: 27dd3ded71b4a77258961a2fc93c1ec0d02f2980
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25450928"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="5c00f-103">APIs für das registrieren & Webhooks verwalten</span><span class="sxs-lookup"><span data-stu-id="5c00f-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="5c00f-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="5c00f-104">/webhook</span></span>
<span data-ttu-id="5c00f-105">Zum Verwalten von Abonnements auf Ereignisse innerhalb Kaizala API-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5c00f-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="5c00f-106">WebHooks besteht aus einem kompakten HTTP-Muster ein einfachen Publisher-Abonnent-Modells für Verdrahtung zusammen Web-APIs und SaaS Services bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5c00f-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="5c00f-107">Wenn ein Ereignis in Kaizala passiert, wird eine Benachrichtigung in Form von HTTP POST-Anforderung an die registrierten Abonnenten gesendet.</span><span class="sxs-lookup"><span data-stu-id="5c00f-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="5c00f-108">Die POST-Anforderung enthält Informationen über das Ereignis für den Empfänger an, entsprechend agieren kann.</span><span class="sxs-lookup"><span data-stu-id="5c00f-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="5c00f-109">WebHooks verwenden, können Sie verschiedene Abonnieren von Ereignissen, die innerhalb einer Unterhaltung Gruppe in Kaizala Kontext auftreten.</span><span class="sxs-lookup"><span data-stu-id="5c00f-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="5c00f-110">/Webhook buchen</span><span class="sxs-lookup"><span data-stu-id="5c00f-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="5c00f-111">Um sicherzustellen, dass Ihr Dienstendpunkt Webhook authentisch und betriebsbereit ist wird wir Ihr Callback-URL überprüfen, bevor Abonnement erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c00f-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="5c00f-112">Zur Überprüfung werden wir Sie ein Token Validation senden, die Sie uns wieder innerhalb von 5 Sekunden senden müssen.</span><span class="sxs-lookup"><span data-stu-id="5c00f-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="5c00f-113">Erfahren Sie mehr</span><span class="sxs-lookup"><span data-stu-id="5c00f-113">Read More</span></span>](WebHookValidaton.md)

#### <a name="request-parameters"></a><span data-ttu-id="5c00f-114">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-114">Request Parameters</span></span>

|  | <span data-ttu-id="5c00f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-115">Parameter</span></span> | <span data-ttu-id="5c00f-116">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-116">Type</span></span> | <span data-ttu-id="5c00f-117">Optional?</span><span class="sxs-lookup"><span data-stu-id="5c00f-117">Optional?</span></span> | <span data-ttu-id="5c00f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c00f-119">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="5c00f-119">HTTP Header</span></span> | <span data-ttu-id="5c00f-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-120">accessToken</span></span> | <span data-ttu-id="5c00f-121">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-121">String</span></span> | <span data-ttu-id="5c00f-122">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-122">No</span></span> | <span data-ttu-id="5c00f-123">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5c00f-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="5c00f-124">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="5c00f-124">HTTP Header</span></span> | <span data-ttu-id="5c00f-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5c00f-125">Content-Type</span></span> | <span data-ttu-id="5c00f-126">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-126">String</span></span> | <span data-ttu-id="5c00f-127">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-127">No</span></span> | <span data-ttu-id="5c00f-128">"Application/Json"</span><span class="sxs-lookup"><span data-stu-id="5c00f-128">"application/json"</span></span> |

#### <a name="request-body"></a><span data-ttu-id="5c00f-129">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="5c00f-129">Request body</span></span>

|  <span data-ttu-id="5c00f-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-130">Parameter</span></span> | <span data-ttu-id="5c00f-131">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-131">Type</span></span> | <span data-ttu-id="5c00f-132">Optional?</span><span class="sxs-lookup"><span data-stu-id="5c00f-132">Optional?</span></span> | <span data-ttu-id="5c00f-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c00f-134">objectId</span><span class="sxs-lookup"><span data-stu-id="5c00f-134">objectId</span></span> | <span data-ttu-id="5c00f-135">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-135">String</span></span> | <span data-ttu-id="5c00f-136">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-136">No</span></span> | <span data-ttu-id="5c00f-137">Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id</span><span class="sxs-lookup"><span data-stu-id="5c00f-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="5c00f-138">objectType</span><span class="sxs-lookup"><span data-stu-id="5c00f-138">objectType</span></span> | <span data-ttu-id="5c00f-139">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-139">String</span></span> | <span data-ttu-id="5c00f-140">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-140">No</span></span> | <span data-ttu-id="5c00f-141">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="5c00f-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="5c00f-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="5c00f-142">eventTypes</span></span> | <span data-ttu-id="5c00f-143">Array</span><span class="sxs-lookup"><span data-stu-id="5c00f-143">Array</span></span> | <span data-ttu-id="5c00f-144">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-144">No</span></span> | <span data-ttu-id="5c00f-145">Array von verschiedenen Arten von Ereignissen, denen Sie die Webhook zu abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="5c00f-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="5c00f-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="5c00f-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="5c00f-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="5c00f-147">callBackUrl</span></span> | <span data-ttu-id="5c00f-148">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-148">String</span></span> | <span data-ttu-id="5c00f-149">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-149">No</span></span> | <span data-ttu-id="5c00f-150">HTTPS-URL, an die die abonnierten Ereignisse, gemeldet werden müssen</span><span class="sxs-lookup"><span data-stu-id="5c00f-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="5c00f-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-151">callBackToken</span></span> | <span data-ttu-id="5c00f-152">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-152">String</span></span> | <span data-ttu-id="5c00f-153">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-153">Yes</span></span> | <span data-ttu-id="5c00f-154">Ein optionaler Parameter können Sie festlegen, die im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="5c00f-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="5c00f-155">callBackContext</span><span class="sxs-lookup"><span data-stu-id="5c00f-155">callBackContext</span></span> | <span data-ttu-id="5c00f-156">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-156">String</span></span> | <span data-ttu-id="5c00f-157">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-157">Yes</span></span> | <span data-ttu-id="5c00f-158">Ein optionaler Parameter können Sie festlegen, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="5c00f-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="5c00f-159">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="5c00f-159">validity</span></span> | <span data-ttu-id="5c00f-160">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-160">String</span></span> | <span data-ttu-id="5c00f-161">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-161">Yes</span></span> | <span data-ttu-id="5c00f-162">Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="5c00f-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="5c00f-163">Der Standardwert lautet 2 Jahre</span><span class="sxs-lookup"><span data-stu-id="5c00f-163">Default is 2 years</span></span> |


#### <a name="response-body"></a><span data-ttu-id="5c00f-164">Antworttext</span><span class="sxs-lookup"><span data-stu-id="5c00f-164">Response body</span></span>
| <span data-ttu-id="5c00f-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-165">Parameter</span></span> | <span data-ttu-id="5c00f-166">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-166">Type</span></span> | <span data-ttu-id="5c00f-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="5c00f-168">webhookId</span><span class="sxs-lookup"><span data-stu-id="5c00f-168">webhookId</span></span> | <span data-ttu-id="5c00f-169">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-169">String</span></span> | <span data-ttu-id="5c00f-170">Bezeichner für die WebHook erstellt</span><span class="sxs-lookup"><span data-stu-id="5c00f-170">Identifier representing the webHook created</span></span> |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="5c00f-171">Anforderungstextkörper - alle Ereignisse auf Gruppenebene abonnieren</span><span class="sxs-lookup"><span data-stu-id="5c00f-171">Request Body - Subscribe to all events at group level</span></span>

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


<span data-ttu-id="5c00f-172">Finden Sie Webhook Antwortschema für registrierte Ereignisse in Kaizala [**hier**](EventSchema.md).</span><span class="sxs-lookup"><span data-stu-id="5c00f-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

### <a name="get-webhook"></a><span data-ttu-id="5c00f-173">Abrufen von /webhook</span><span class="sxs-lookup"><span data-stu-id="5c00f-173">Get /webhook</span></span>

    GET {endpoint-url}/v1/webhook

#### <a name="request-parameters"></a><span data-ttu-id="5c00f-174">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-174">Request Parameters</span></span>


|  | <span data-ttu-id="5c00f-175">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-175">Parameter</span></span> | <span data-ttu-id="5c00f-176">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-176">Type</span></span> | <span data-ttu-id="5c00f-177">Optional?</span><span class="sxs-lookup"><span data-stu-id="5c00f-177">Optional?</span></span> | <span data-ttu-id="5c00f-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-178">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c00f-179">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="5c00f-179">HTTP Header</span></span> | <span data-ttu-id="5c00f-180">accessToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-180">accessToken</span></span> | <span data-ttu-id="5c00f-181">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-181">String</span></span> | <span data-ttu-id="5c00f-182">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-182">No</span></span> | <span data-ttu-id="5c00f-183">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5c00f-183">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="5c00f-184">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-184">Query parameter</span></span> | <span data-ttu-id="5c00f-185">objectId</span><span class="sxs-lookup"><span data-stu-id="5c00f-185">objectId</span></span> | <span data-ttu-id="5c00f-186">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-186">String</span></span> | <span data-ttu-id="5c00f-187">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-187">No</span></span> | <span data-ttu-id="5c00f-188">Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id</span><span class="sxs-lookup"><span data-stu-id="5c00f-188">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="5c00f-189">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-189">Query parameter</span></span> | <span data-ttu-id="5c00f-190">objectType</span><span class="sxs-lookup"><span data-stu-id="5c00f-190">objectType</span></span> | <span data-ttu-id="5c00f-191">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-191">String</span></span> | <span data-ttu-id="5c00f-192">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-192">No</span></span> | <span data-ttu-id="5c00f-193">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="5c00f-193">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

#### <a name="response-body"></a><span data-ttu-id="5c00f-194">Antworttext</span><span class="sxs-lookup"><span data-stu-id="5c00f-194">Response body</span></span>

| <span data-ttu-id="5c00f-195">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-195">Parameter</span></span> | <span data-ttu-id="5c00f-196">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-196">Type</span></span> | <span data-ttu-id="5c00f-197">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-197">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="5c00f-198">webhooks</span><span class="sxs-lookup"><span data-stu-id="5c00f-198">webhooks</span></span> | <span data-ttu-id="5c00f-199">JSON-Objekt-Array</span><span class="sxs-lookup"><span data-stu-id="5c00f-199">JSON Object Array</span></span> | <span data-ttu-id="5c00f-200">Array von Webhooks auf ObjectId abonniert</span><span class="sxs-lookup"><span data-stu-id="5c00f-200">Array of webhooks subscribed on the objectId</span></span> |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="5c00f-201">JSON-Struktur für jede einzelne Webhook in das Array Webhooks []:</span><span class="sxs-lookup"><span data-stu-id="5c00f-201">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="5c00f-202">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-202">Parameter</span></span> | <span data-ttu-id="5c00f-203">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-203">Type</span></span> | <span data-ttu-id="5c00f-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-204">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="5c00f-205">id</span><span class="sxs-lookup"><span data-stu-id="5c00f-205">id</span></span> | <span data-ttu-id="5c00f-206">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-206">String</span></span> | <span data-ttu-id="5c00f-207">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5c00f-207">Webhook Identifier</span></span> |
| <span data-ttu-id="5c00f-208">objectId</span><span class="sxs-lookup"><span data-stu-id="5c00f-208">objectId</span></span> | <span data-ttu-id="5c00f-209">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-209">String</span></span> | <span data-ttu-id="5c00f-210">Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="5c00f-210">Object Identifier</span></span> |
| <span data-ttu-id="5c00f-211">objectType</span><span class="sxs-lookup"><span data-stu-id="5c00f-211">objectType</span></span> | <span data-ttu-id="5c00f-212">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-212">String</span></span> | <span data-ttu-id="5c00f-213">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="5c00f-213">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="5c00f-214">events</span><span class="sxs-lookup"><span data-stu-id="5c00f-214">events</span></span> | <span data-ttu-id="5c00f-215">String]</span><span class="sxs-lookup"><span data-stu-id="5c00f-215">String[]</span></span> | <span data-ttu-id="5c00f-216">Ereignisliste mit jedem Wert als eines der "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Ankündigung", "MemberAdded", "MemberRemoved", "GroupAdded" " GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="5c00f-216">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="5c00f-217">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="5c00f-217">callBackUrl</span></span> | <span data-ttu-id="5c00f-218">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-218">String</span></span> | <span data-ttu-id="5c00f-219">Callback-URL an die die abonnierten Ereignisse, gemeldet werden müssen</span><span class="sxs-lookup"><span data-stu-id="5c00f-219">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="5c00f-220">callBackToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-220">callBackToken</span></span> | <span data-ttu-id="5c00f-221">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-221">String</span></span> | <span data-ttu-id="5c00f-222">Parameter der im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="5c00f-222">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="5c00f-223">callBackContext</span><span class="sxs-lookup"><span data-stu-id="5c00f-223">callBackContext</span></span> | <span data-ttu-id="5c00f-224">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-224">String</span></span> | <span data-ttu-id="5c00f-225">Parameter, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet</span><span class="sxs-lookup"><span data-stu-id="5c00f-225">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="5c00f-226">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="5c00f-226">validity</span></span> | <span data-ttu-id="5c00f-227">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c00f-227">String</span></span> | <span data-ttu-id="5c00f-228">Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="5c00f-228">Validity for the WebHook to be active in EPOCH format.</span></span> |
| <span data-ttu-id="5c00f-229">aktive</span><span class="sxs-lookup"><span data-stu-id="5c00f-229">active</span></span> | <span data-ttu-id="5c00f-230">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c00f-230">Boolean</span></span> | <span data-ttu-id="5c00f-231">True, wenn der Status der Webhook aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5c00f-231">True, if the state of webhook is active</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="5c00f-232">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="5c00f-232">Sample JSON Response</span></span>

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

### <a name="delete-webhook"></a><span data-ttu-id="5c00f-233">/Webhook löschen</span><span class="sxs-lookup"><span data-stu-id="5c00f-233">Delete /webhook</span></span>

    DELETE {endpoint-url}/v1/webhook

#### <a name="request-parameters"></a><span data-ttu-id="5c00f-234">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-234">Request Parameters</span></span>
|  | <span data-ttu-id="5c00f-235">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-235">Parameter</span></span> | <span data-ttu-id="5c00f-236">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-236">Type</span></span> | <span data-ttu-id="5c00f-237">Optional?</span><span class="sxs-lookup"><span data-stu-id="5c00f-237">Optional?</span></span> | <span data-ttu-id="5c00f-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-238">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c00f-239">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="5c00f-239">HTTP Header</span></span> | <span data-ttu-id="5c00f-240">accessToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-240">accessToken</span></span> | <span data-ttu-id="5c00f-241">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-241">String</span></span> | <span data-ttu-id="5c00f-242">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-242">No</span></span> | <span data-ttu-id="5c00f-243">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5c00f-243">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="5c00f-244">Pfadparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-244">Path parameter</span></span> | <span data-ttu-id="5c00f-245">webhookId</span><span class="sxs-lookup"><span data-stu-id="5c00f-245">webhookId</span></span> | <span data-ttu-id="5c00f-246">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-246">String</span></span> | <span data-ttu-id="5c00f-247">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-247">No</span></span> | <span data-ttu-id="5c00f-248">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5c00f-248">Webhook Identifier</span></span> |

### <a name="put-webhook"></a><span data-ttu-id="5c00f-249">PLATZIEREN Sie /webhook</span><span class="sxs-lookup"><span data-stu-id="5c00f-249">PUT /webhook</span></span>

    PUT {endpoint-url}/v1/webhook/{webhookId}

<span data-ttu-id="5c00f-250">Parameter für die Webhook kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5c00f-250">Any parameter for the webhook can be updated.</span></span> <span data-ttu-id="5c00f-251">Anforderungstext kann 1 oder mehrere Parameter enthalten, je nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="5c00f-251">Request Body may contain 1 or more parameters, as needed.</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="5c00f-252">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-252">Request Parameters</span></span>

|  | <span data-ttu-id="5c00f-253">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-253">Parameter</span></span> | <span data-ttu-id="5c00f-254">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-254">Type</span></span> | <span data-ttu-id="5c00f-255">Optional?</span><span class="sxs-lookup"><span data-stu-id="5c00f-255">Optional?</span></span> | <span data-ttu-id="5c00f-256">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-256">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c00f-257">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="5c00f-257">HTTP Header</span></span> | <span data-ttu-id="5c00f-258">accessToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-258">accessToken</span></span> | <span data-ttu-id="5c00f-259">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-259">String</span></span> | <span data-ttu-id="5c00f-260">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-260">No</span></span> | <span data-ttu-id="5c00f-261">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5c00f-261">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="5c00f-262">Pfadparameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-262">Path parameter</span></span> | <span data-ttu-id="5c00f-263">webhookId</span><span class="sxs-lookup"><span data-stu-id="5c00f-263">webhookId</span></span> | <span data-ttu-id="5c00f-264">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-264">String</span></span> | <span data-ttu-id="5c00f-265">Nein</span><span class="sxs-lookup"><span data-stu-id="5c00f-265">No</span></span> | <span data-ttu-id="5c00f-266">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5c00f-266">Webhook Identifier</span></span> |

#### <a name="request-body"></a><span data-ttu-id="5c00f-267">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="5c00f-267">Request body</span></span>

|  <span data-ttu-id="5c00f-268">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c00f-268">Parameter</span></span> | <span data-ttu-id="5c00f-269">Typ</span><span class="sxs-lookup"><span data-stu-id="5c00f-269">Type</span></span> | <span data-ttu-id="5c00f-270">Optional?</span><span class="sxs-lookup"><span data-stu-id="5c00f-270">Optional?</span></span> | <span data-ttu-id="5c00f-271">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c00f-271">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c00f-272">objectId</span><span class="sxs-lookup"><span data-stu-id="5c00f-272">objectId</span></span> | <span data-ttu-id="5c00f-273">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-273">String</span></span> | <span data-ttu-id="5c00f-274">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-274">Yes</span></span> | <span data-ttu-id="5c00f-275">Bezeichner, die für das Objekt, in welchen, das Kontext die Webhooks erstellt werden müssen. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id</span><span class="sxs-lookup"><span data-stu-id="5c00f-275">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="5c00f-276">objectType</span><span class="sxs-lookup"><span data-stu-id="5c00f-276">objectType</span></span> | <span data-ttu-id="5c00f-277">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-277">String</span></span> | <span data-ttu-id="5c00f-278">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-278">Yes</span></span> | <span data-ttu-id="5c00f-279">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="5c00f-279">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="5c00f-280">eventTypes</span><span class="sxs-lookup"><span data-stu-id="5c00f-280">eventTypes</span></span> | <span data-ttu-id="5c00f-281">Array</span><span class="sxs-lookup"><span data-stu-id="5c00f-281">Array</span></span> | <span data-ttu-id="5c00f-282">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-282">Yes</span></span> | <span data-ttu-id="5c00f-283">Array von verschiedenen Arten von Ereignissen, denen Sie die Webhook zu abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="5c00f-283">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="5c00f-284">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="5c00f-284">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="5c00f-285">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="5c00f-285">callBackUrl</span></span> | <span data-ttu-id="5c00f-286">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-286">String</span></span> | <span data-ttu-id="5c00f-287">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-287">Yes</span></span> | <span data-ttu-id="5c00f-288">HTTPS-URL, an die die abonnierten Ereignisse, gemeldet werden müssen</span><span class="sxs-lookup"><span data-stu-id="5c00f-288">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="5c00f-289">callBackToken</span><span class="sxs-lookup"><span data-stu-id="5c00f-289">callBackToken</span></span> | <span data-ttu-id="5c00f-290">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-290">String</span></span> | <span data-ttu-id="5c00f-291">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-291">Yes</span></span> | <span data-ttu-id="5c00f-292">Ein optionaler Parameter können Sie festlegen, die im HTTP-Header 'Kz-rückruftoken' mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="5c00f-292">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="5c00f-293">callBackContext</span><span class="sxs-lookup"><span data-stu-id="5c00f-293">callBackContext</span></span> | <span data-ttu-id="5c00f-294">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-294">String</span></span> | <span data-ttu-id="5c00f-295">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-295">Yes</span></span> | <span data-ttu-id="5c00f-296">Ein optionaler Parameter können Sie festlegen, die in der Nutzlast JSON als "Kontext" mit jedem Rückruf, die durch die WebHook gesendet wird</span><span class="sxs-lookup"><span data-stu-id="5c00f-296">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="5c00f-297">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="5c00f-297">validity</span></span> | <span data-ttu-id="5c00f-298">String</span><span class="sxs-lookup"><span data-stu-id="5c00f-298">String</span></span> | <span data-ttu-id="5c00f-299">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-299">Yes</span></span> | <span data-ttu-id="5c00f-300">Gültigkeitsdauer für die WebHook im Format EPOCHE aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="5c00f-300">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="5c00f-301">Der Standardwert lautet 2 Jahre</span><span class="sxs-lookup"><span data-stu-id="5c00f-301">Default is 2 years</span></span> |
| <span data-ttu-id="5c00f-302">Aktiv</span><span class="sxs-lookup"><span data-stu-id="5c00f-302">Active</span></span> | <span data-ttu-id="5c00f-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c00f-303">Boolean</span></span> | <span data-ttu-id="5c00f-304">Ja</span><span class="sxs-lookup"><span data-stu-id="5c00f-304">Yes</span></span> | <span data-ttu-id="5c00f-305">Ändern Sie den Status der Webhook aktiv, wenn der Wert true ist</span><span class="sxs-lookup"><span data-stu-id="5c00f-305">Change the state of webhook to Active, if the value is true</span></span> |


#### <a name="sample-request-body"></a><span data-ttu-id="5c00f-306">Beispiel-Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="5c00f-306">Sample Request Body</span></span>

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

## <a name="auto-disable-of-webhooks"></a><span data-ttu-id="5c00f-307">Auto-Deaktivieren des Webhooks</span><span class="sxs-lookup"><span data-stu-id="5c00f-307">Auto-Disable of Webhooks</span></span>

<span data-ttu-id="5c00f-308">Um die Zuverlässigkeit der unsere Webhooks zu verbessern, haben wir kürzlich die "Wiederholen" und deaktivieren Logik hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5c00f-308">To improve the Reliability of our Webhooks, we recently have added the Retry and Disabling Logic.</span></span> <span data-ttu-id="5c00f-309">Url der Callback-/ Endpunkt mit einer Webhook registriert, wenn nicht erreichbar oder reagiert nicht mit dem Statuscode als 2xx (> = 3xx), und klicken Sie dann unseren Dienst versucht, Reichweite/es für 6 Zeiten auf exponentielle Weise innerhalb eines Textabschnitts 2 Tage wiederholen.</span><span class="sxs-lookup"><span data-stu-id="5c00f-309">The Callback Url/Endpoint registered with a webhook, if not reachable or does not respond with a status code other than 2xx (>=3xx), then our Service will try to reach/retry it for 6 times in an exponential way within a span of 2 Days.</span></span> 

<span data-ttu-id="5c00f-310">Wenn sie weiterhin für 2 Tage fehlschlägt, wird der entsprechende Webhook deaktiviert, und der Besitzer muss mit der Put-/webhook API aktualisieren, bevor er beginnt erneut arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c00f-310">If it is still failing for 2 days, then the corresponding Webhook will be disabled, and the owner needs to update it with the Put /webhook API before it starts working again.</span></span> <span data-ttu-id="5c00f-311">Für diese Vorgaben unter</span><span class="sxs-lookup"><span data-stu-id="5c00f-311">For e.g.</span></span>

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a><span data-ttu-id="5c00f-312">Anforderungstext:</span><span class="sxs-lookup"><span data-stu-id="5c00f-312">Request Body:</span></span>
````javascript
{ 
  "Active": "true" 
} 
````
