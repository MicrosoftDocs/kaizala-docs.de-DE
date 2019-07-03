---
title: /webhooks
description: Referenzartikel zur API zum Verwalten von Kaizala-Abonnements
topic: Reference
author: nitinjms
ms.openlocfilehash: e5064e88bbc492a21883ad813792a1d69f54769c
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535772"
---
# <a name="apis-to-register--manage-webhooks"></a><span data-ttu-id="0ed1d-103">APIs zum Registrieren #a0 Verwalten von webhooks</span><span class="sxs-lookup"><span data-stu-id="0ed1d-103">APIs to register & manage webhooks</span></span>
## <a name="webhook"></a><span data-ttu-id="0ed1d-104">/webhook</span><span class="sxs-lookup"><span data-stu-id="0ed1d-104">/webhook</span></span>
<span data-ttu-id="0ed1d-105">API-Endpunkt zum Verwalten von Abonnements für Ereignisse in Kaizala.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-105">API end-point to manage subscriptions to events inside Kaizala.</span></span>

<span data-ttu-id="0ed1d-106">Webhooks ist ein leichtes http-Muster, das ein einfaches Publisher/Subscriber-Modell für die Verkabelung von webapis und Saas-Diensten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-106">WebHooks is a lightweight HTTP pattern providing a simple publisher/subscriber model for wiring together Web APIs and SaaS services.</span></span> <span data-ttu-id="0ed1d-107">Wenn ein Ereignis in Kaizala erfolgt, wird eine Benachrichtigung in Form einer HTTP POST-Anforderung an registrierte Abonnenten gesendet.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-107">When an event happens in Kaizala, a notification is sent in the form of an HTTP POST request to registered subscribers.</span></span> <span data-ttu-id="0ed1d-108">Die Post-Anforderung enthält Informationen über das Ereignis, das es dem Empfänger ermöglicht, entsprechend zu handeln.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-108">The POST request contains information about the event which makes it possible for the receiver to act accordingly.</span></span>


<span data-ttu-id="0ed1d-109">Mithilfe von webhooks können Sie verschiedene Ereignisse abonnieren, die innerhalb eines unterhaltungsgruppen Kontexts in Kaizala auftreten.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-109">Using WebHooks, you can subscribe to various events that occur within a conversation group context in Kaizala.</span></span>

### <a name="post-webhook"></a><span data-ttu-id="0ed1d-110">Post/webhook</span><span class="sxs-lookup"><span data-stu-id="0ed1d-110">POST /webhook</span></span>

    POST {endpoint-url}/v1/webhook

<span data-ttu-id="0ed1d-111">Um sicherzustellen, dass Ihr webhook-Dienstendpunkt authentisch ist und funktioniert, überprüfen wir Ihre Rückruf-URL vor dem Erstellen des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-111">To ensure your webhook service endpoint is authentic and working we will verify your callback URL before creating subscription.</span></span> <span data-ttu-id="0ed1d-112">Zur Überprüfung senden wir Ihnen ein Validierungs Token, das Sie benötigen, um uns innerhalb von 5 Sekunden zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-112">For verification we will send you a validation token which you need to send us back within 5 seconds.</span></span> [<span data-ttu-id="0ed1d-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ed1d-113">Read More</span></span>](WebHookValidation.md)

#### <a name="request-parameters"></a><span data-ttu-id="0ed1d-114">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-114">Request Parameters</span></span>

|  | <span data-ttu-id="0ed1d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-115">Parameter</span></span> | <span data-ttu-id="0ed1d-116">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-116">Type</span></span> | <span data-ttu-id="0ed1d-117">Optional?</span><span class="sxs-lookup"><span data-stu-id="0ed1d-117">Optional?</span></span> | <span data-ttu-id="0ed1d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-118">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-119">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="0ed1d-119">HTTP Header</span></span> | <span data-ttu-id="0ed1d-120">accessToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-120">accessToken</span></span> | <span data-ttu-id="0ed1d-121">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-121">String</span></span> | <span data-ttu-id="0ed1d-122">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-122">No</span></span> | <span data-ttu-id="0ed1d-123">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="0ed1d-123">Access Token received from the auth end-point</span></span> || <span data-ttu-id="0ed1d-124">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="0ed1d-124">HTTP Header</span></span> | <span data-ttu-id="0ed1d-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0ed1d-125">Content-Type</span></span> | <span data-ttu-id="0ed1d-126">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-126">String</span></span> | <span data-ttu-id="0ed1d-127">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-127">No</span></span> | <span data-ttu-id="0ed1d-128">"application/json"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-128">"application/json"</span></span> |

#### <a name="request-body"></a><span data-ttu-id="0ed1d-129">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-129">Request body</span></span>

|  <span data-ttu-id="0ed1d-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-130">Parameter</span></span> | <span data-ttu-id="0ed1d-131">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-131">Type</span></span> | <span data-ttu-id="0ed1d-132">Optional?</span><span class="sxs-lookup"><span data-stu-id="0ed1d-132">Optional?</span></span> | <span data-ttu-id="0ed1d-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-133">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-134">objectId</span><span class="sxs-lookup"><span data-stu-id="0ed1d-134">objectId</span></span> | <span data-ttu-id="0ed1d-135">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-135">String</span></span> | <span data-ttu-id="0ed1d-136">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-136">No</span></span> | <span data-ttu-id="0ed1d-137">Bezeichner, der das Objekt darstellt, in welchem Kontext die webhooks erstellt werden müssen. Für ObjectType = Group, den Bezeichner der Gruppe, für ObjectType = Action, seine Aktions-ID, für ObjectType = ActionPackage, dessen Aktionspaket-ID</span><span class="sxs-lookup"><span data-stu-id="0ed1d-137">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="0ed1d-138">objectType</span><span class="sxs-lookup"><span data-stu-id="0ed1d-138">objectType</span></span> | <span data-ttu-id="0ed1d-139">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-139">String</span></span> | <span data-ttu-id="0ed1d-140">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-140">No</span></span> | <span data-ttu-id="0ed1d-141">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-141">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="0ed1d-142">eventTypes</span><span class="sxs-lookup"><span data-stu-id="0ed1d-142">eventTypes</span></span> | <span data-ttu-id="0ed1d-143">Array</span><span class="sxs-lookup"><span data-stu-id="0ed1d-143">Array</span></span> | <span data-ttu-id="0ed1d-144">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-144">No</span></span> | <span data-ttu-id="0ed1d-145">Array verschiedener Ereignistypen, für die Sie den webhook abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-145">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="0ed1d-146">Unterstützte Ereignisse sind: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Announcement", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-146">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="0ed1d-147">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="0ed1d-147">callBackUrl</span></span> | <span data-ttu-id="0ed1d-148">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-148">String</span></span> | <span data-ttu-id="0ed1d-149">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-149">No</span></span> | <span data-ttu-id="0ed1d-150">HTTPS-URL, zu der die abonnierten Ereignisse benachrichtigt werden müssen</span><span class="sxs-lookup"><span data-stu-id="0ed1d-150">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="0ed1d-151">callBackToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-151">callBackToken</span></span> | <span data-ttu-id="0ed1d-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-152">String</span></span> | <span data-ttu-id="0ed1d-153">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-153">Yes</span></span> | <span data-ttu-id="0ed1d-154">Optionaler Parameter, den Sie festlegen können, welcher im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0ed1d-154">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="0ed1d-155">callbackcontext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-155">callBackContext</span></span> | <span data-ttu-id="0ed1d-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-156">String</span></span> | <span data-ttu-id="0ed1d-157">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-157">Yes</span></span> | <span data-ttu-id="0ed1d-158">Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als "Context" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0ed1d-158">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="0ed1d-159">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="0ed1d-159">validity</span></span> | <span data-ttu-id="0ed1d-160">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-160">String</span></span> | <span data-ttu-id="0ed1d-161">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-161">Yes</span></span> | <span data-ttu-id="0ed1d-162">Gültigkeit, damit der webhook im Epoch-Format aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-162">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="0ed1d-163">Der Standardwert ist 2 Jahre.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-163">Default is 2 years</span></span> |


#### <a name="response-body"></a><span data-ttu-id="0ed1d-164">Antworttext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-164">Response body</span></span>
| <span data-ttu-id="0ed1d-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-165">Parameter</span></span> | <span data-ttu-id="0ed1d-166">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-166">Type</span></span> | <span data-ttu-id="0ed1d-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-167">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-168">webhook-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-168">webhookId</span></span> | <span data-ttu-id="0ed1d-169">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-169">String</span></span> | <span data-ttu-id="0ed1d-170">Bezeichner, der den erstellten webhook darstellt</span><span class="sxs-lookup"><span data-stu-id="0ed1d-170">Identifier representing the webHook created</span></span> |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a><span data-ttu-id="0ed1d-171">Anforderungstext – abonnieren aller Ereignisse auf Gruppenebene</span><span class="sxs-lookup"><span data-stu-id="0ed1d-171">Request Body - Subscribe to all events at group level</span></span>

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


<span data-ttu-id="0ed1d-172">Sie können das webhook-Antwortschema für registrierte Ereignisse in Kaizala [**hier**](EventSchema.md)finden.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-172">You can find webhook response schema for registered events in Kaizala [**here**](EventSchema.md).</span></span>

> <span data-ttu-id="0ed1d-173">**Hinweis:** Kaizala garantiert mindestens einmal die Zustellung der webhook-Antwort.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-173">**Note:** Kaizala guarantees at-least once delivery of webhook response.</span></span> <span data-ttu-id="0ed1d-174">In bestimmten Fällen kann es vorkommen, dass Kaizala doppelte webhook-Antwort für dasselbe Ereignis senden kann.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-174">It may happen, in certain cases, that Kaizala may send duplicate webhook response for the same event.</span></span>

### <a name="get-webhook"></a><span data-ttu-id="0ed1d-175">/Webhook abrufen</span><span class="sxs-lookup"><span data-stu-id="0ed1d-175">Get /webhook</span></span>

    <span data-ttu-id="0ed1d-176">Get {Endpunkt-URL}/v1/webhook</span><span class="sxs-lookup"><span data-stu-id="0ed1d-176">GET {endpoint-url}/v1/webhook</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="0ed1d-177">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-177">Request Parameters</span></span>


|  | <span data-ttu-id="0ed1d-178">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-178">Parameter</span></span> | <span data-ttu-id="0ed1d-179">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-179">Type</span></span> | <span data-ttu-id="0ed1d-180">Optional?</span><span class="sxs-lookup"><span data-stu-id="0ed1d-180">Optional?</span></span> | <span data-ttu-id="0ed1d-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-181">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-182">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="0ed1d-182">HTTP Header</span></span> | <span data-ttu-id="0ed1d-183">accessToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-183">accessToken</span></span> | <span data-ttu-id="0ed1d-184">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-184">String</span></span> | <span data-ttu-id="0ed1d-185">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-185">No</span></span> | <span data-ttu-id="0ed1d-186">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="0ed1d-186">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="0ed1d-187">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-187">Query parameter</span></span> | <span data-ttu-id="0ed1d-188">objectId</span><span class="sxs-lookup"><span data-stu-id="0ed1d-188">objectId</span></span> | <span data-ttu-id="0ed1d-189">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-189">String</span></span> | <span data-ttu-id="0ed1d-190">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-190">No</span></span> | <span data-ttu-id="0ed1d-191">Bezeichner, der das Objekt darstellt, in welchem Kontext die webhooks erstellt werden müssen. Für ObjectType = Group, den Bezeichner der Gruppe, für ObjectType = Action, seine Aktions-ID, für ObjectType = ActionPackage, dessen Aktionspaket-ID</span><span class="sxs-lookup"><span data-stu-id="0ed1d-191">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="0ed1d-192">Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-192">Query parameter</span></span> | <span data-ttu-id="0ed1d-193">objectType</span><span class="sxs-lookup"><span data-stu-id="0ed1d-193">objectType</span></span> | <span data-ttu-id="0ed1d-194">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-194">String</span></span> | <span data-ttu-id="0ed1d-195">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-195">No</span></span> | <span data-ttu-id="0ed1d-196">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-196">Enum: "Group"/"Action"/"ActionPackage"</span></span> |

#### <a name="response-body"></a><span data-ttu-id="0ed1d-197">Antworttext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-197">Response body</span></span>

| <span data-ttu-id="0ed1d-198">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-198">Parameter</span></span> | <span data-ttu-id="0ed1d-199">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-199">Type</span></span> | <span data-ttu-id="0ed1d-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-200">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-201">webhooks</span><span class="sxs-lookup"><span data-stu-id="0ed1d-201">webhooks</span></span> | <span data-ttu-id="0ed1d-202">JSON-Objekt Array</span><span class="sxs-lookup"><span data-stu-id="0ed1d-202">JSON Object Array</span></span> | <span data-ttu-id="0ed1d-203">Array von webhooks, die für die ObjectID abonniert sind</span><span class="sxs-lookup"><span data-stu-id="0ed1d-203">Array of webhooks subscribed on the objectId</span></span> |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a><span data-ttu-id="0ed1d-204">JSON-Struktur für jeden einzelnen webhook im Array webhooks []:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-204">JSON structure for each individual webhook in the array webhooks[]:</span></span>

| <span data-ttu-id="0ed1d-205">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-205">Parameter</span></span> | <span data-ttu-id="0ed1d-206">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-206">Type</span></span> | <span data-ttu-id="0ed1d-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-207">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-208">id</span><span class="sxs-lookup"><span data-stu-id="0ed1d-208">id</span></span> | <span data-ttu-id="0ed1d-209">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-209">String</span></span> | <span data-ttu-id="0ed1d-210">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0ed1d-210">Webhook Identifier</span></span> |
| <span data-ttu-id="0ed1d-211">objectId</span><span class="sxs-lookup"><span data-stu-id="0ed1d-211">objectId</span></span> | <span data-ttu-id="0ed1d-212">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-212">String</span></span> | <span data-ttu-id="0ed1d-213">Objektbezeichner</span><span class="sxs-lookup"><span data-stu-id="0ed1d-213">Object Identifier</span></span> |
| <span data-ttu-id="0ed1d-214">objectType</span><span class="sxs-lookup"><span data-stu-id="0ed1d-214">objectType</span></span> | <span data-ttu-id="0ed1d-215">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-215">String</span></span> | <span data-ttu-id="0ed1d-216">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-216">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="0ed1d-217">events</span><span class="sxs-lookup"><span data-stu-id="0ed1d-217">events</span></span> | <span data-ttu-id="0ed1d-218">String []</span><span class="sxs-lookup"><span data-stu-id="0ed1d-218">String[]</span></span> | <span data-ttu-id="0ed1d-219">Ereignisliste mit jedem Wert als eine von "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Announcement", "MemberAdded", "MemberRemoved", "GroupAdded", " GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-219">Event list with each value as one of "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="0ed1d-220">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="0ed1d-220">callBackUrl</span></span> | <span data-ttu-id="0ed1d-221">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-221">String</span></span> | <span data-ttu-id="0ed1d-222">Rückruf-URL, zu der die abonnierten Ereignisse benachrichtigt werden müssen</span><span class="sxs-lookup"><span data-stu-id="0ed1d-222">Callback URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="0ed1d-223">callBackToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-223">callBackToken</span></span> | <span data-ttu-id="0ed1d-224">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-224">String</span></span> | <span data-ttu-id="0ed1d-225">Parameter, der im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0ed1d-225">Parameter which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="0ed1d-226">callbackcontext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-226">callBackContext</span></span> | <span data-ttu-id="0ed1d-227">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-227">String</span></span> | <span data-ttu-id="0ed1d-228">In der JSON-Nutzlast als "Context" gesendeter Parameter mit jedem Rückruf, der vom webhook vorgenommen wird</span><span class="sxs-lookup"><span data-stu-id="0ed1d-228">Parameter sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="0ed1d-229">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="0ed1d-229">validity</span></span> | <span data-ttu-id="0ed1d-230">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-230">String</span></span> | <span data-ttu-id="0ed1d-231">Gültigkeit, damit der webhook im Epoch-Format aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-231">Validity for the WebHook to be active in EPOCH format.</span></span> |
| <span data-ttu-id="0ed1d-232">Active</span><span class="sxs-lookup"><span data-stu-id="0ed1d-232">active</span></span> | <span data-ttu-id="0ed1d-233">Boolesch</span><span class="sxs-lookup"><span data-stu-id="0ed1d-233">Boolean</span></span> | <span data-ttu-id="0ed1d-234">True, wenn der Status von webhook aktiv ist</span><span class="sxs-lookup"><span data-stu-id="0ed1d-234">True, if the state of webhook is active</span></span> |

##### <a name="sample-json-response"></a><span data-ttu-id="0ed1d-235">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="0ed1d-235">Sample JSON Response</span></span>

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

### <a name="delete-webhook"></a><span data-ttu-id="0ed1d-236">/Webhook löschen</span><span class="sxs-lookup"><span data-stu-id="0ed1d-236">Delete /webhook</span></span>

    <span data-ttu-id="0ed1d-237">DELETE {Endpunkt-URL}/v1/webhook</span><span class="sxs-lookup"><span data-stu-id="0ed1d-237">DELETE {endpoint-url}/v1/webhook</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="0ed1d-238">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-238">Request Parameters</span></span>
|  | <span data-ttu-id="0ed1d-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-239">Parameter</span></span> | <span data-ttu-id="0ed1d-240">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-240">Type</span></span> | <span data-ttu-id="0ed1d-241">Optional?</span><span class="sxs-lookup"><span data-stu-id="0ed1d-241">Optional?</span></span> | <span data-ttu-id="0ed1d-242">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-242">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-243">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="0ed1d-243">HTTP Header</span></span> | <span data-ttu-id="0ed1d-244">accessToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-244">accessToken</span></span> | <span data-ttu-id="0ed1d-245">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-245">String</span></span> | <span data-ttu-id="0ed1d-246">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-246">No</span></span> | <span data-ttu-id="0ed1d-247">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="0ed1d-247">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="0ed1d-248">Path-Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-248">Path parameter</span></span> | <span data-ttu-id="0ed1d-249">webhook-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-249">webhookId</span></span> | <span data-ttu-id="0ed1d-250">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-250">String</span></span> | <span data-ttu-id="0ed1d-251">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-251">No</span></span> | <span data-ttu-id="0ed1d-252">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0ed1d-252">Webhook Identifier</span></span> |

### <a name="put-webhook"></a><span data-ttu-id="0ed1d-253">Put/webhook</span><span class="sxs-lookup"><span data-stu-id="0ed1d-253">PUT /webhook</span></span>

    PUT {endpoint-url}/v1/webhook/{webhookId}

<span data-ttu-id="0ed1d-254">Jeder Parameter für den webhook kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-254">Any parameter for the webhook can be updated.</span></span> <span data-ttu-id="0ed1d-255">Der Anforderungstext kann bei Bedarf 1 oder mehr Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-255">Request Body may contain 1 or more parameters, as needed.</span></span>

#### <a name="request-parameters"></a><span data-ttu-id="0ed1d-256">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-256">Request Parameters</span></span>

|  | <span data-ttu-id="0ed1d-257">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-257">Parameter</span></span> | <span data-ttu-id="0ed1d-258">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-258">Type</span></span> | <span data-ttu-id="0ed1d-259">Optional?</span><span class="sxs-lookup"><span data-stu-id="0ed1d-259">Optional?</span></span> | <span data-ttu-id="0ed1d-260">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-260">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-261">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="0ed1d-261">HTTP Header</span></span> | <span data-ttu-id="0ed1d-262">accessToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-262">accessToken</span></span> | <span data-ttu-id="0ed1d-263">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-263">String</span></span> | <span data-ttu-id="0ed1d-264">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-264">No</span></span> | <span data-ttu-id="0ed1d-265">Vom auth-Endpunkt empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="0ed1d-265">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="0ed1d-266">Path-Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-266">Path parameter</span></span> | <span data-ttu-id="0ed1d-267">webhook-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-267">webhookId</span></span> | <span data-ttu-id="0ed1d-268">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-268">String</span></span> | <span data-ttu-id="0ed1d-269">Nein</span><span class="sxs-lookup"><span data-stu-id="0ed1d-269">No</span></span> | <span data-ttu-id="0ed1d-270">Webhook-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0ed1d-270">Webhook Identifier</span></span> |

#### <a name="request-body"></a><span data-ttu-id="0ed1d-271">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-271">Request body</span></span>

|  <span data-ttu-id="0ed1d-272">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed1d-272">Parameter</span></span> | <span data-ttu-id="0ed1d-273">Typ</span><span class="sxs-lookup"><span data-stu-id="0ed1d-273">Type</span></span> | <span data-ttu-id="0ed1d-274">Optional?</span><span class="sxs-lookup"><span data-stu-id="0ed1d-274">Optional?</span></span> | <span data-ttu-id="0ed1d-275">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed1d-275">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="0ed1d-276">objectId</span><span class="sxs-lookup"><span data-stu-id="0ed1d-276">objectId</span></span> | <span data-ttu-id="0ed1d-277">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-277">String</span></span> | <span data-ttu-id="0ed1d-278">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-278">Yes</span></span> | <span data-ttu-id="0ed1d-279">Bezeichner, der das Objekt darstellt, in welchem Kontext die webhooks erstellt werden müssen. Für ObjectType = Group, den Bezeichner der Gruppe, für ObjectType = Action, seine Aktions-ID, für ObjectType = ActionPackage, dessen Aktionspaket-ID</span><span class="sxs-lookup"><span data-stu-id="0ed1d-279">Identifier representing the object in which context the webhooks need to be created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="0ed1d-280">objectType</span><span class="sxs-lookup"><span data-stu-id="0ed1d-280">objectType</span></span> | <span data-ttu-id="0ed1d-281">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-281">String</span></span> | <span data-ttu-id="0ed1d-282">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-282">Yes</span></span> | <span data-ttu-id="0ed1d-283">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-283">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="0ed1d-284">eventTypes</span><span class="sxs-lookup"><span data-stu-id="0ed1d-284">eventTypes</span></span> | <span data-ttu-id="0ed1d-285">Array</span><span class="sxs-lookup"><span data-stu-id="0ed1d-285">Array</span></span> | <span data-ttu-id="0ed1d-286">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-286">Yes</span></span> | <span data-ttu-id="0ed1d-287">Array verschiedener Ereignistypen, für die Sie den webhook abonnieren müssen.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-287">Array of different types of events you need to subscribe the webhook to.</span></span> <span data-ttu-id="0ed1d-288">Unterstützte Ereignisse sind: "ActionCreated", "ActionResponse", "SurveyCreated", "JobCreated", "SurveyResponse", "JobResponse", "TextMessageCreated", "AttachmentCreated", "Announcement", "MemberAdded", "MemberRemoved", "GroupAdded", "GroupRemoved"</span><span class="sxs-lookup"><span data-stu-id="0ed1d-288">Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved"</span></span> |
| <span data-ttu-id="0ed1d-289">callBackUrl</span><span class="sxs-lookup"><span data-stu-id="0ed1d-289">callBackUrl</span></span> | <span data-ttu-id="0ed1d-290">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-290">String</span></span> | <span data-ttu-id="0ed1d-291">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-291">Yes</span></span> | <span data-ttu-id="0ed1d-292">HTTPS-URL, zu der die abonnierten Ereignisse benachrichtigt werden müssen</span><span class="sxs-lookup"><span data-stu-id="0ed1d-292">HTTPS URL to which the subscribed events need to be notified to</span></span> |
| <span data-ttu-id="0ed1d-293">callBackToken</span><span class="sxs-lookup"><span data-stu-id="0ed1d-293">callBackToken</span></span> | <span data-ttu-id="0ed1d-294">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-294">String</span></span> | <span data-ttu-id="0ed1d-295">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-295">Yes</span></span> | <span data-ttu-id="0ed1d-296">Optionaler Parameter, den Sie festlegen können, welcher im HTTP-Header "KZ-Callback-Token" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0ed1d-296">Optional parameter you can set which will be sent in the HTTP header 'kz-callback-token' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="0ed1d-297">callbackcontext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-297">callBackContext</span></span> | <span data-ttu-id="0ed1d-298">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ed1d-298">String</span></span> | <span data-ttu-id="0ed1d-299">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-299">Yes</span></span> | <span data-ttu-id="0ed1d-300">Optionaler Parameter, den Sie festlegen können, der in der JSON-Nutzlast als "Context" mit jedem Rückruf gesendet wird, der vom webhook erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0ed1d-300">Optional parameter you can set which will be sent in the JSON payload as 'context' with every callBack made by the WebHook</span></span> |
| <span data-ttu-id="0ed1d-301">Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="0ed1d-301">validity</span></span> | <span data-ttu-id="0ed1d-302">String</span><span class="sxs-lookup"><span data-stu-id="0ed1d-302">String</span></span> | <span data-ttu-id="0ed1d-303">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-303">Yes</span></span> | <span data-ttu-id="0ed1d-304">Gültigkeit, damit der webhook im Epoch-Format aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-304">Validity for the WebHook to be active in EPOCH format.</span></span> <span data-ttu-id="0ed1d-305">Der Standardwert ist 2 Jahre.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-305">Default is 2 years</span></span> |
| <span data-ttu-id="0ed1d-306">Aktiv</span><span class="sxs-lookup"><span data-stu-id="0ed1d-306">Active</span></span> | <span data-ttu-id="0ed1d-307">Boolesch</span><span class="sxs-lookup"><span data-stu-id="0ed1d-307">Boolean</span></span> | <span data-ttu-id="0ed1d-308">Ja</span><span class="sxs-lookup"><span data-stu-id="0ed1d-308">Yes</span></span> | <span data-ttu-id="0ed1d-309">Ändern des Status von webhook in "aktiv", wenn der Wert "true" lautet</span><span class="sxs-lookup"><span data-stu-id="0ed1d-309">Change the state of webhook to Active, if the value is true</span></span> |


#### <a name="sample-request-body"></a><span data-ttu-id="0ed1d-310">Beispiel Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="0ed1d-310">Sample Request Body</span></span>

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

## <a name="auto-disable-of-webhooks"></a><span data-ttu-id="0ed1d-311">Automatisches Deaktivieren von webhooks</span><span class="sxs-lookup"><span data-stu-id="0ed1d-311">Auto-Disable of Webhooks</span></span>

<span data-ttu-id="0ed1d-312">Um die Zuverlässigkeit unserer webhooks zu verbessern, haben wir vor kurzem die Logik wiederholen und deaktivieren hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-312">To improve the Reliability of our Webhooks, we recently have added the Retry and Disabling Logic.</span></span> <span data-ttu-id="0ed1d-313">Die mit einem webhook registrierte Rückruf-URL/der Endpunkt, wenn Sie nicht erreichbar ist oder nicht mit einem anderen Statuscode als 2xx (>= 3xx) antwortet, versucht unser Dienst, ihn 6 Mal exponentiell innerhalb einer Spanne von 2 Tagen zu erreichen/wiederholen.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-313">The Callback Url/Endpoint registered with a webhook, if not reachable or does not respond with a status code other than 2xx (>=3xx), then our Service will try to reach/retry it for 6 times in an exponential way within a span of 2 Days.</span></span> 

<span data-ttu-id="0ed1d-314">Wenn es immer noch 2 Tage lang nicht funktioniert, wird der entsprechende webhook deaktiviert, und der Besitzer muss ihn mit der Put/webhook-API aktualisieren, bevor er wieder mit der Arbeit beginnt.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-314">If it is still failing for 2 days, then the corresponding Webhook will be disabled, and the owner needs to update it with the Put /webhook API before it starts working again.</span></span> <span data-ttu-id="0ed1d-315">Für z.b.</span><span class="sxs-lookup"><span data-stu-id="0ed1d-315">For e.g.</span></span>

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a><span data-ttu-id="0ed1d-316">Anforderungstext:</span><span class="sxs-lookup"><span data-stu-id="0ed1d-316">Request Body:</span></span>
````javascript
{ 
  "Active": "true" 
} 
````
