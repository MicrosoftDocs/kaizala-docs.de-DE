# <a name="webhook-response-schema-for-registered-events"></a><span data-ttu-id="fbb44-101">Webhook-Antwortschema für registrierte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="fbb44-101">Webhook response schema for registered events</span></span>

<span data-ttu-id="fbb44-102">Wenn ein webhook registriert ist, gibt Kaizala für jedes Ereignis in der registrierten objectId, gefiltert nach registrierten Ereignissen, eine webHook-Antwort zurück.</span><span class="sxs-lookup"><span data-stu-id="fbb44-102">If a webhook is registered, Kaizala returns a webHook response for each event on the registered objectId, filtered for registered events.</span></span> <span data-ttu-id="fbb44-103">NachFolgend finden Sie Schema Details für verschiedene webhook-Antworten für verschiedene Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="fbb44-103">Below is schema details for different webhook response for different events.</span></span>

## <a name="response-body"></a><span data-ttu-id="fbb44-104">Antworttext</span><span class="sxs-lookup"><span data-stu-id="fbb44-104">Response Body</span></span>
| <span data-ttu-id="fbb44-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-105">Parameter</span></span> | <span data-ttu-id="fbb44-106">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-106">Type</span></span> | <span data-ttu-id="fbb44-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-107">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-108">objectId</span><span class="sxs-lookup"><span data-stu-id="fbb44-108">objectId</span></span> | <span data-ttu-id="fbb44-109">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-109">String</span></span> | <span data-ttu-id="fbb44-110">Bezeichner, der das Objekt darstellt, in dem der webhook erstellt wurde. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier</span><span class="sxs-lookup"><span data-stu-id="fbb44-110">Identifier representing the object in which context the webhook has been created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="fbb44-111">objectType</span><span class="sxs-lookup"><span data-stu-id="fbb44-111">objectType</span></span> | <span data-ttu-id="fbb44-112">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-112">String</span></span> | <span data-ttu-id="fbb44-113">Enum: "Group"/"action"/"ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="fbb44-113">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="fbb44-114">eventType</span><span class="sxs-lookup"><span data-stu-id="fbb44-114">eventType</span></span> | <span data-ttu-id="fbb44-115">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-115">String</span></span> | <span data-ttu-id="fbb44-116">Registriertes Ereignis, das aufgerufen wurde</span><span class="sxs-lookup"><span data-stu-id="fbb44-116">Registered event that has been invoked</span></span> |
| <span data-ttu-id="fbb44-117">eventId</span><span class="sxs-lookup"><span data-stu-id="fbb44-117">eventId</span></span> | <span data-ttu-id="fbb44-118">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-118">String</span></span> | <span data-ttu-id="fbb44-119">Bezeichner, der das Ereignis darstellt</span><span class="sxs-lookup"><span data-stu-id="fbb44-119">Identifier representing the event</span></span> |
| <span data-ttu-id="fbb44-120">data</span><span class="sxs-lookup"><span data-stu-id="fbb44-120">data</span></span> | <span data-ttu-id="fbb44-121">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="fbb44-121">JSON Object</span></span> | <span data-ttu-id="fbb44-122">Objekt, das die für dieses ereignisspezifischen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="fbb44-122">Object representing data specific to that event.</span></span> <span data-ttu-id="fbb44-123">Für jedes unterstützte Ereignis definierte Parameter.</span><span class="sxs-lookup"><span data-stu-id="fbb44-123">Parameters defined below for each of the supported event.</span></span> |
| <span data-ttu-id="fbb44-124">context</span><span class="sxs-lookup"><span data-stu-id="fbb44-124">context</span></span> | <span data-ttu-id="fbb44-125">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-125">String</span></span> | <span data-ttu-id="fbb44-126">Gibt den Wert zurück, der bei der Registrierung eines webhooks unter dem Parameter "callbackcontext" festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fbb44-126">Returns value that has been set while registering a webhook under parameter 'callbackContext'</span></span>|
| <span data-ttu-id="fbb44-127">fromUser</span><span class="sxs-lookup"><span data-stu-id="fbb44-127">fromUser</span></span> | <span data-ttu-id="fbb44-128">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-128">String</span></span> | <span data-ttu-id="fbb44-129">Telefonnummer des abSenders</span><span class="sxs-lookup"><span data-stu-id="fbb44-129">Sender's phone number</span></span> |
| <span data-ttu-id="fbb44-130">fromUserId</span><span class="sxs-lookup"><span data-stu-id="fbb44-130">fromUserId</span></span> | <span data-ttu-id="fbb44-131">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-131">String</span></span> | <span data-ttu-id="fbb44-132">Absender-ID</span><span class="sxs-lookup"><span data-stu-id="fbb44-132">Sender's userId</span></span> |
| <span data-ttu-id="fbb44-133">fromUserName</span><span class="sxs-lookup"><span data-stu-id="fbb44-133">fromUserName</span></span> | <span data-ttu-id="fbb44-134">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-134">String</span></span> | <span data-ttu-id="fbb44-135">Registrierter Name des abSenders mit Kaizala</span><span class="sxs-lookup"><span data-stu-id="fbb44-135">Sender's registered name with Kaizala</span></span> |
| <span data-ttu-id="fbb44-136">fromUserProfilePic</span><span class="sxs-lookup"><span data-stu-id="fbb44-136">fromUserProfilePic</span></span> | <span data-ttu-id="fbb44-137">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-137">url</span></span> | <span data-ttu-id="fbb44-138">Profilbild des abSenders</span><span class="sxs-lookup"><span data-stu-id="fbb44-138">Sender's Profile Pic</span></span> |

<span data-ttu-id="fbb44-139">Der Parameter "Data" würde je nach webHook-Ereignis variieren.</span><span class="sxs-lookup"><span data-stu-id="fbb44-139">The parameter 'data' would vary depending on the webHook event.</span></span> <span data-ttu-id="fbb44-140">Nachfolgend finden Sie ein Schema für jedes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fbb44-140">You can find schema for each event below.</span></span>

### <a name="data-for-event-textmessagecreated"></a><span data-ttu-id="fbb44-141">Daten für das Ereignis ' TextMessageCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-141">data for event 'TextMessageCreated'</span></span>
| <span data-ttu-id="fbb44-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-142">Parameter</span></span> | <span data-ttu-id="fbb44-143">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-143">Type</span></span> | <span data-ttu-id="fbb44-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-144">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-145">text</span><span class="sxs-lookup"><span data-stu-id="fbb44-145">text</span></span> | <span data-ttu-id="fbb44-146">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-146">String</span></span> | <span data-ttu-id="fbb44-147">Text Nachricht, die gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="fbb44-147">Text Message that has been sent</span></span> |

#### <a name="sample-webhook-response-for-textmessagecreated"></a><span data-ttu-id="fbb44-148">Beispiel-webHook-Antwort für ' TextMessageCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-148">Sample webHook response for 'TextMessageCreated'</span></span>
```javascript
{
  "objectId": "8c2050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "TextMessageCreated",
  "eventId": "55ed01-02b5-491e-8e7e-484726da976b",
  "data": {
    "text": "Test Message"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-attachmentcreated"></a><span data-ttu-id="fbb44-149">Daten für das Ereignis ' AttachmentCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-149">data for event 'AttachmentCreated'</span></span>
| <span data-ttu-id="fbb44-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-150">Parameter</span></span> | <span data-ttu-id="fbb44-151">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-151">Type</span></span> | <span data-ttu-id="fbb44-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-152">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-153">Medien</span><span class="sxs-lookup"><span data-stu-id="fbb44-153">media</span></span> | <span data-ttu-id="fbb44-154">Array</span><span class="sxs-lookup"><span data-stu-id="fbb44-154">Array</span></span> | <span data-ttu-id="fbb44-155">Jedes Element enthält mediaUrl und mediaFileName</span><span class="sxs-lookup"><span data-stu-id="fbb44-155">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="fbb44-156">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="fbb44-156">mediaUrl</span></span> | <span data-ttu-id="fbb44-157">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-157">url</span></span> | <span data-ttu-id="fbb44-158">URL des Bilds</span><span class="sxs-lookup"><span data-stu-id="fbb44-158">url of the image</span></span> |
| <span data-ttu-id="fbb44-159">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="fbb44-159">mediaFileName</span></span> | <span data-ttu-id="fbb44-160">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-160">String</span></span> | <span data-ttu-id="fbb44-161">Filename</span><span class="sxs-lookup"><span data-stu-id="fbb44-161">Filename</span></span> |
| <span data-ttu-id="fbb44-162">actionType</span><span class="sxs-lookup"><span data-stu-id="fbb44-162">actionType</span></span> | <span data-ttu-id="fbb44-163">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-163">String</span></span> | <span data-ttu-id="fbb44-164">Enumerationswert: ' Image '</span><span class="sxs-lookup"><span data-stu-id="fbb44-164">Enum value : 'Image'</span></span> |
| <span data-ttu-id="fbb44-165">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="fbb44-165">caption</span></span> | <span data-ttu-id="fbb44-166">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-166">String</span></span> | <span data-ttu-id="fbb44-167">mit dem Bild verknüpfte Beschriftung</span><span class="sxs-lookup"><span data-stu-id="fbb44-167">caption attached with the image</span></span> |

#### <a name="sample-webhook-response-for-attachmentcreated"></a><span data-ttu-id="fbb44-168">Beispiel-webHook-Antwort für ' AttachmentCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-168">Sample webHook response for 'AttachmentCreated'</span></span>
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "AttachmentCreated",
  "eventId": "59e2e9f9-9b10-4b67-8bc5-3f85a04f2d91",
  "data": {
    "media": [
      {
        "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/0ad142c52b30d797addebadb620c19bf6f018299ed4acdce5760e45e2e4bc4ae.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Thbp46wdgoqbDaAF06v2Y2ijzny0jx2fBDo1EZab%2BNY%3D&amp;st=2018-03-22T10:22:21Z&amp;se=2292-01-05T11:22:21Z&amp;sp=r",
        "mediaFileName": "IMG_18-03-22_165220084_1.jpg"
      }
    ],
    "actionType": "Image",
    "caption": "Testing."
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```
### <a name="data-for-event-announcement"></a><span data-ttu-id="fbb44-169">Daten für Ereignis Ansage</span><span class="sxs-lookup"><span data-stu-id="fbb44-169">data for event 'Announcement'</span></span>
| <span data-ttu-id="fbb44-170">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-170">Parameter</span></span> | <span data-ttu-id="fbb44-171">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-171">Type</span></span> | <span data-ttu-id="fbb44-172">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-172">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-173">title</span><span class="sxs-lookup"><span data-stu-id="fbb44-173">title</span></span> | <span data-ttu-id="fbb44-174">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-174">String</span></span> | <span data-ttu-id="fbb44-175">Titel der Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-175">Title of Announcement Action</span></span> |
| <span data-ttu-id="fbb44-176">text</span><span class="sxs-lookup"><span data-stu-id="fbb44-176">text</span></span> | <span data-ttu-id="fbb44-177">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-177">String</span></span> | <span data-ttu-id="fbb44-178">Nachrichtentext der Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-178">Message body of Announcement Action</span></span> |
| <span data-ttu-id="fbb44-179">Medien</span><span class="sxs-lookup"><span data-stu-id="fbb44-179">media</span></span> | <span data-ttu-id="fbb44-180">Array</span><span class="sxs-lookup"><span data-stu-id="fbb44-180">Array</span></span> | <span data-ttu-id="fbb44-181">Jedes Element enthält mediaUrl und mediaFileName</span><span class="sxs-lookup"><span data-stu-id="fbb44-181">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="fbb44-182">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="fbb44-182">mediaUrl</span></span> | <span data-ttu-id="fbb44-183">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-183">url</span></span> | <span data-ttu-id="fbb44-184">URL des Bilds</span><span class="sxs-lookup"><span data-stu-id="fbb44-184">url of the image</span></span> |
| <span data-ttu-id="fbb44-185">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="fbb44-185">mediaFileName</span></span> | <span data-ttu-id="fbb44-186">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-186">String</span></span> | <span data-ttu-id="fbb44-187">Filename</span><span class="sxs-lookup"><span data-stu-id="fbb44-187">Filename</span></span> |


#### <a name="sample-webhook-response-for-announcement"></a><span data-ttu-id="fbb44-188">Beispiel-webHook-Antwort für "Ansage"</span><span class="sxs-lookup"><span data-stu-id="fbb44-188">Sample webHook response for 'Announcement'</span></span>
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "Announcement",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "text": "Caption :Testing.",
    "title": "Sent by Robin Richard",
    "media": [
      {
        "url": "https://cdn.inc-000.kms.osi.office.net/contenthost/beb2cfef8732c6cc3b54652c1f6f99d64f529fd9be3d409e2966552639fb791f.jpeg",
        "fileName": "e3c145f1-5e6f-4ee9-bd83-49ec3a1c2550.jpeg"
      }
    ]
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobcreated"></a><span data-ttu-id="fbb44-189">Daten für das Ereignis ' JobCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-189">data for event 'JobCreated'</span></span>
| <span data-ttu-id="fbb44-190">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-190">Parameter</span></span> | <span data-ttu-id="fbb44-191">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-191">Type</span></span> | <span data-ttu-id="fbb44-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-193">title</span><span class="sxs-lookup"><span data-stu-id="fbb44-193">title</span></span> | <span data-ttu-id="fbb44-194">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-194">String</span></span> | <span data-ttu-id="fbb44-195">Titel der Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-195">Title of Announcement Action</span></span> |
| <span data-ttu-id="fbb44-196">text</span><span class="sxs-lookup"><span data-stu-id="fbb44-196">text</span></span> | <span data-ttu-id="fbb44-197">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-197">String</span></span> | <span data-ttu-id="fbb44-198">Nachrichtentext der Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-198">Message body of Announcement Action</span></span> |
| <span data-ttu-id="fbb44-199">actionId</span><span class="sxs-lookup"><span data-stu-id="fbb44-199">actionId</span></span> | <span data-ttu-id="fbb44-200">Id</span><span class="sxs-lookup"><span data-stu-id="fbb44-200">Id</span></span> | <span data-ttu-id="fbb44-201">Bezeichner für diese bestimmte Instanz von Job-Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-201">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="fbb44-202">dueDate</span><span class="sxs-lookup"><span data-stu-id="fbb44-202">dueDate</span></span> | <span data-ttu-id="fbb44-203">Date</span><span class="sxs-lookup"><span data-stu-id="fbb44-203">Date</span></span> | <span data-ttu-id="fbb44-204">Datum, an dem der Auftrag ablaufen würde</span><span class="sxs-lookup"><span data-stu-id="fbb44-204">Date by which job would expire</span></span> |
| <span data-ttu-id="fbb44-205">assignedTo</span><span class="sxs-lookup"><span data-stu-id="fbb44-205">assignedTo</span></span> | <span data-ttu-id="fbb44-206">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="fbb44-206">String Array</span></span> | <span data-ttu-id="fbb44-207">Array von Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="fbb44-207">Array of phone numbers</span></span> |


#### <a name="sample-webhook-response-for-jobcreated"></a><span data-ttu-id="fbb44-208">Beispiel-webHook-Antwort für ' JobCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-208">Sample webHook response for 'JobCreated'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "assignedTo": [
      "+919740797266"
    ],
    "title": "Test Job",
    "dueDate": "2018-03-22T18:29:59Z",
    "actionId": "aeb012-31a0-477a-a131-8a1e2791b36e",
    "groupId": "8c291050-9be8-6-97f5-bb7013930027"
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobresponse"></a><span data-ttu-id="fbb44-209">Daten für das Ereignis ' JobResponse '</span><span class="sxs-lookup"><span data-stu-id="fbb44-209">data for event 'JobResponse'</span></span>
| <span data-ttu-id="fbb44-210">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-210">Parameter</span></span> | <span data-ttu-id="fbb44-211">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-211">Type</span></span> | <span data-ttu-id="fbb44-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-212">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-213">title</span><span class="sxs-lookup"><span data-stu-id="fbb44-213">title</span></span> | <span data-ttu-id="fbb44-214">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-214">String</span></span> | <span data-ttu-id="fbb44-215">Titel der Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-215">Title of Announcement Action</span></span> |
| <span data-ttu-id="fbb44-216">text</span><span class="sxs-lookup"><span data-stu-id="fbb44-216">text</span></span> | <span data-ttu-id="fbb44-217">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-217">String</span></span> | <span data-ttu-id="fbb44-218">Nachrichtentext der Ansage Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-218">Message body of Announcement Action</span></span> |
| <span data-ttu-id="fbb44-219">actionId</span><span class="sxs-lookup"><span data-stu-id="fbb44-219">actionId</span></span> | <span data-ttu-id="fbb44-220">Id</span><span class="sxs-lookup"><span data-stu-id="fbb44-220">Id</span></span> | <span data-ttu-id="fbb44-221">Bezeichner für diese bestimmte Instanz von Job-Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-221">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="fbb44-222">groupId</span><span class="sxs-lookup"><span data-stu-id="fbb44-222">groupId</span></span> | <span data-ttu-id="fbb44-223">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-223">String</span></span> | <span data-ttu-id="fbb44-224">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="fbb44-224">Group Identifier</span></span> |
| <span data-ttu-id="fbb44-225">Antwort-Nr.</span><span class="sxs-lookup"><span data-stu-id="fbb44-225">responseId</span></span> | <span data-ttu-id="fbb44-226">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-226">String</span></span> | <span data-ttu-id="fbb44-227">GUID zum Identifizieren dieser Antwort</span><span class="sxs-lookup"><span data-stu-id="fbb44-227">GUID for identifying that Response</span></span> |
| <span data-ttu-id="fbb44-228">responseDetails</span><span class="sxs-lookup"><span data-stu-id="fbb44-228">responseDetails</span></span> | <span data-ttu-id="fbb44-229">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="fbb44-229">String Array</span></span> | <span data-ttu-id="fbb44-230">Array von Response-Objekten</span><span class="sxs-lookup"><span data-stu-id="fbb44-230">Array of Response Objects</span></span> |
| <span data-ttu-id="fbb44-231">Empfänger</span><span class="sxs-lookup"><span data-stu-id="fbb44-231">assignee</span></span> | <span data-ttu-id="fbb44-232">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-232">String</span></span> | <span data-ttu-id="fbb44-233">Telefonnummer des Empfängers</span><span class="sxs-lookup"><span data-stu-id="fbb44-233">Assignee's Phone Number</span></span> |
| <span data-ttu-id="fbb44-234">assigneeName</span><span class="sxs-lookup"><span data-stu-id="fbb44-234">assigneeName</span></span> | <span data-ttu-id="fbb44-235">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-235">String</span></span> | <span data-ttu-id="fbb44-236">Name des Empfängers</span><span class="sxs-lookup"><span data-stu-id="fbb44-236">Assignee's Name</span></span> |
| <span data-ttu-id="fbb44-237">assigneeProfilePic</span><span class="sxs-lookup"><span data-stu-id="fbb44-237">assigneeProfilePic</span></span> | <span data-ttu-id="fbb44-238">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-238">url</span></span> | <span data-ttu-id="fbb44-239">URL des Profils des Empfängers PIC</span><span class="sxs-lookup"><span data-stu-id="fbb44-239">url of the assignee's profile pic</span></span> |
| <span data-ttu-id="fbb44-240">isCompleted</span><span class="sxs-lookup"><span data-stu-id="fbb44-240">isCompleted</span></span> | <span data-ttu-id="fbb44-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-241">Boolean</span></span> | <span data-ttu-id="fbb44-242">Ist der Auftrag abgeschlossen?</span><span class="sxs-lookup"><span data-stu-id="fbb44-242">Is the Job completed?</span></span> |




#### <a name="sample-webhook-response-for-jobresponse"></a><span data-ttu-id="fbb44-243">Beispiel-webHook-Antwort für ' JobResponse '</span><span class="sxs-lookup"><span data-stu-id="fbb44-243">Sample webHook response for 'JobResponse'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "actionId": "2ce34820-3d67-4807-9a1d-7cf099c2e7ae",
    "groupId": "8c291050-9be8-45d6-97f5-bb7013930027",
    "responseId": "80a883ec-e6c7-4dc8-979d-d268bbeeee8b",
    "responseDetails": {
      "response": {
        "assignee": "++91xxxxxxxx",
        "assigneeName": "Robin Richard",
        "assigneeProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d536285d08e6409e416.jpg",
        "isCompleted": true
      }
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-actioncreated--surveycreated"></a><span data-ttu-id="fbb44-244">Daten für das Ereignis ' ActionCreated '/' SurveyCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-244">data for event 'ActionCreated' / 'SurveyCreated'</span></span>
| <span data-ttu-id="fbb44-245">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-245">Parameter</span></span> | <span data-ttu-id="fbb44-246">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-246">Type</span></span> | <span data-ttu-id="fbb44-247">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-247">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-248">actionId</span><span class="sxs-lookup"><span data-stu-id="fbb44-248">actionId</span></span> | <span data-ttu-id="fbb44-249">Id</span><span class="sxs-lookup"><span data-stu-id="fbb44-249">Id</span></span> | <span data-ttu-id="fbb44-250">Bezeichner für diese bestimmte Instanz von Job-Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-250">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="fbb44-251">groupId</span><span class="sxs-lookup"><span data-stu-id="fbb44-251">groupId</span></span> | <span data-ttu-id="fbb44-252">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fbb44-252">String</span></span> | <span data-ttu-id="fbb44-253">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="fbb44-253">Group Identifier</span></span> |
| <span data-ttu-id="fbb44-254">Antwort-Nr.</span><span class="sxs-lookup"><span data-stu-id="fbb44-254">responseId</span></span> | <span data-ttu-id="fbb44-255">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-255">String</span></span> | <span data-ttu-id="fbb44-256">GUID zum Identifizieren dieser Antwort</span><span class="sxs-lookup"><span data-stu-id="fbb44-256">GUID for identifying that Response</span></span> |
| <span data-ttu-id="fbb44-257">Fragen</span><span class="sxs-lookup"><span data-stu-id="fbb44-257">questions</span></span> | <span data-ttu-id="fbb44-258">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="fbb44-258">String Array</span></span> | <span data-ttu-id="fbb44-259">Array von Objekten</span><span class="sxs-lookup"><span data-stu-id="fbb44-259">Array of Objects</span></span> |
| <span data-ttu-id="fbb44-260">Responder</span><span class="sxs-lookup"><span data-stu-id="fbb44-260">responder</span></span> | <span data-ttu-id="fbb44-261">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-261">String</span></span> | <span data-ttu-id="fbb44-262">Telefonnummer des Responders</span><span class="sxs-lookup"><span data-stu-id="fbb44-262">responder's Phone Number</span></span> |
| <span data-ttu-id="fbb44-263">responderName</span><span class="sxs-lookup"><span data-stu-id="fbb44-263">responderName</span></span> | <span data-ttu-id="fbb44-264">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-264">String</span></span> | <span data-ttu-id="fbb44-265">Name des Responders</span><span class="sxs-lookup"><span data-stu-id="fbb44-265">responder's Name</span></span> |
| <span data-ttu-id="fbb44-266">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="fbb44-266">responderProfilePic</span></span> | <span data-ttu-id="fbb44-267">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-267">url</span></span> | <span data-ttu-id="fbb44-268">URL des Profils des Responders PIC</span><span class="sxs-lookup"><span data-stu-id="fbb44-268">url of the responder's profile pic</span></span> |
| <span data-ttu-id="fbb44-269">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="fbb44-269">isAnonymous</span></span> | <span data-ttu-id="fbb44-270">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-270">Boolean</span></span> | <span data-ttu-id="fbb44-271">Wurde die Umfrageantwort anonym übermittelt</span><span class="sxs-lookup"><span data-stu-id="fbb44-271">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="fbb44-272">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="fbb44-272">isUpdateResponse</span></span> | <span data-ttu-id="fbb44-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-273">Boolean</span></span> | <span data-ttu-id="fbb44-274">Wurde die Antwort von Responder aktualisiert, da die Antwort zuvor übermittelt wurde</span><span class="sxs-lookup"><span data-stu-id="fbb44-274">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="fbb44-275">Schema Details für ' responseWithQuestions '-Objekt</span><span class="sxs-lookup"><span data-stu-id="fbb44-275">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="fbb44-276">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-276">Parameter</span></span> | <span data-ttu-id="fbb44-277">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-277">Type</span></span> | <span data-ttu-id="fbb44-278">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-278">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-279">title</span><span class="sxs-lookup"><span data-stu-id="fbb44-279">title</span></span> | <span data-ttu-id="fbb44-280">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-280">String</span></span> | <span data-ttu-id="fbb44-281">Frage Titel</span><span class="sxs-lookup"><span data-stu-id="fbb44-281">Question Title</span></span> |
| <span data-ttu-id="fbb44-282">type</span><span class="sxs-lookup"><span data-stu-id="fbb44-282">type</span></span> | <span data-ttu-id="fbb44-283">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fbb44-283">String</span></span> | <span data-ttu-id="fbb44-284">Questiontype</span><span class="sxs-lookup"><span data-stu-id="fbb44-284">QuestionType</span></span> |
| <span data-ttu-id="fbb44-285">options</span><span class="sxs-lookup"><span data-stu-id="fbb44-285">options</span></span> | <span data-ttu-id="fbb44-286">Array</span><span class="sxs-lookup"><span data-stu-id="fbb44-286">Array</span></span> | <span data-ttu-id="fbb44-287">Liste der Optionen (Schlüssel-Wert-Paar), die für Fragen mit mehreren Auswahlen gelten</span><span class="sxs-lookup"><span data-stu-id="fbb44-287">List of options (key-value pair) applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="fbb44-288">isUnsichtbar</span><span class="sxs-lookup"><span data-stu-id="fbb44-288">isInvisible</span></span> | <span data-ttu-id="fbb44-289">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-289">Boolean</span></span> | <span data-ttu-id="fbb44-290">Ist die Frage von der Benutzeroberfläche ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="fbb44-290">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a><span data-ttu-id="fbb44-291">Beispiel-webHook-Antwort für ' ActionCreated '/' SurveyCreated '</span><span class="sxs-lookup"><span data-stu-id="fbb44-291">Sample webHook response for 'ActionCreated' / 'SurveyCreated'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "ActionCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```



### <a name="data-for-event-surveyresponse-actionresponse"></a><span data-ttu-id="fbb44-292">Daten für das Ereignis ' SurveyResponse '/' ActionResponse '</span><span class="sxs-lookup"><span data-stu-id="fbb44-292">data for event 'SurveyResponse'/ 'ActionResponse'</span></span>
| <span data-ttu-id="fbb44-293">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-293">Parameter</span></span> | <span data-ttu-id="fbb44-294">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-294">Type</span></span> | <span data-ttu-id="fbb44-295">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-295">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-296">actionId</span><span class="sxs-lookup"><span data-stu-id="fbb44-296">actionId</span></span> | <span data-ttu-id="fbb44-297">Id</span><span class="sxs-lookup"><span data-stu-id="fbb44-297">Id</span></span> | <span data-ttu-id="fbb44-298">Bezeichner für diese bestimmte Instanz von Job-Aktion</span><span class="sxs-lookup"><span data-stu-id="fbb44-298">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="fbb44-299">groupId</span><span class="sxs-lookup"><span data-stu-id="fbb44-299">groupId</span></span> | <span data-ttu-id="fbb44-300">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fbb44-300">String</span></span> | <span data-ttu-id="fbb44-301">Gruppenbezeichner</span><span class="sxs-lookup"><span data-stu-id="fbb44-301">Group Identifier</span></span> |
| <span data-ttu-id="fbb44-302">Antwort-Nr.</span><span class="sxs-lookup"><span data-stu-id="fbb44-302">responseId</span></span> | <span data-ttu-id="fbb44-303">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-303">String</span></span> | <span data-ttu-id="fbb44-304">GUID zum Identifizieren dieser Antwort</span><span class="sxs-lookup"><span data-stu-id="fbb44-304">GUID for identifying that Response</span></span> |
| <span data-ttu-id="fbb44-305">responseDetails</span><span class="sxs-lookup"><span data-stu-id="fbb44-305">responseDetails</span></span> | <span data-ttu-id="fbb44-306">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="fbb44-306">String Array</span></span> | <span data-ttu-id="fbb44-307">Array von ' responseWithQuestions '-Objekten</span><span class="sxs-lookup"><span data-stu-id="fbb44-307">Array of 'responseWithQuestions' Objects</span></span> |
| <span data-ttu-id="fbb44-308">Responder</span><span class="sxs-lookup"><span data-stu-id="fbb44-308">responder</span></span> | <span data-ttu-id="fbb44-309">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-309">String</span></span> | <span data-ttu-id="fbb44-310">Telefonnummer des Responders</span><span class="sxs-lookup"><span data-stu-id="fbb44-310">responder's Phone Number</span></span> |
| <span data-ttu-id="fbb44-311">responderName</span><span class="sxs-lookup"><span data-stu-id="fbb44-311">responderName</span></span> | <span data-ttu-id="fbb44-312">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-312">String</span></span> | <span data-ttu-id="fbb44-313">Name des Responders</span><span class="sxs-lookup"><span data-stu-id="fbb44-313">responder's Name</span></span> |
| <span data-ttu-id="fbb44-314">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="fbb44-314">responderProfilePic</span></span> | <span data-ttu-id="fbb44-315">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-315">url</span></span> | <span data-ttu-id="fbb44-316">URL des Profils des Responders PIC</span><span class="sxs-lookup"><span data-stu-id="fbb44-316">url of the responder's profile pic</span></span> |
| <span data-ttu-id="fbb44-317">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="fbb44-317">isAnonymous</span></span> | <span data-ttu-id="fbb44-318">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-318">Boolean</span></span> | <span data-ttu-id="fbb44-319">Wurde die Umfrageantwort anonym übermittelt</span><span class="sxs-lookup"><span data-stu-id="fbb44-319">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="fbb44-320">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="fbb44-320">isUpdateResponse</span></span> | <span data-ttu-id="fbb44-321">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-321">Boolean</span></span> | <span data-ttu-id="fbb44-322">Wurde die Antwort von Responder aktualisiert, da die Antwort zuvor übermittelt wurde</span><span class="sxs-lookup"><span data-stu-id="fbb44-322">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="fbb44-323">Schema Details für ' responseWithQuestions '-Objekt</span><span class="sxs-lookup"><span data-stu-id="fbb44-323">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="fbb44-324">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-324">Parameter</span></span> | <span data-ttu-id="fbb44-325">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-325">Type</span></span> | <span data-ttu-id="fbb44-326">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-327">title</span><span class="sxs-lookup"><span data-stu-id="fbb44-327">title</span></span> | <span data-ttu-id="fbb44-328">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-328">String</span></span> | <span data-ttu-id="fbb44-329">Frage Titel</span><span class="sxs-lookup"><span data-stu-id="fbb44-329">Question Title</span></span> |
| <span data-ttu-id="fbb44-330">type</span><span class="sxs-lookup"><span data-stu-id="fbb44-330">type</span></span> | <span data-ttu-id="fbb44-331">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fbb44-331">String</span></span> | <span data-ttu-id="fbb44-332">Questiontype</span><span class="sxs-lookup"><span data-stu-id="fbb44-332">QuestionType</span></span> |
| <span data-ttu-id="fbb44-333">options</span><span class="sxs-lookup"><span data-stu-id="fbb44-333">options</span></span> | <span data-ttu-id="fbb44-334">Array</span><span class="sxs-lookup"><span data-stu-id="fbb44-334">Array</span></span> | <span data-ttu-id="fbb44-335">Liste der Optionen, die für Fragen mit mehreren Auswahlen gelten</span><span class="sxs-lookup"><span data-stu-id="fbb44-335">List of options applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="fbb44-336">Antwort</span><span class="sxs-lookup"><span data-stu-id="fbb44-336">answer</span></span> | <span data-ttu-id="fbb44-337">Array des JSON-Objekts</span><span class="sxs-lookup"><span data-stu-id="fbb44-337">Array of Json Object</span></span> | <span data-ttu-id="fbb44-338">Antworten</span><span class="sxs-lookup"><span data-stu-id="fbb44-338">Answers</span></span> |
| <span data-ttu-id="fbb44-339">isUnsichtbar</span><span class="sxs-lookup"><span data-stu-id="fbb44-339">isInvisible</span></span> | <span data-ttu-id="fbb44-340">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb44-340">Boolean</span></span> | <span data-ttu-id="fbb44-341">Ist die Frage von der Benutzeroberfläche ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="fbb44-341">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a><span data-ttu-id="fbb44-342">Beispiel-webHook-Antwort für ' SurveyResponse ' ' ActionResponse '</span><span class="sxs-lookup"><span data-stu-id="fbb44-342">Sample webHook response for 'SurveyResponse' 'ActionResponse'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "SurveyResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```


### <a name="data-for-event-memberadded--memberremoved"></a><span data-ttu-id="fbb44-343">Daten für das Ereignis ' MemberAdded '/' MemberRemoved '</span><span class="sxs-lookup"><span data-stu-id="fbb44-343">data for event 'MemberAdded' / 'MemberRemoved'</span></span>
| <span data-ttu-id="fbb44-344">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-344">Parameter</span></span> | <span data-ttu-id="fbb44-345">Typ</span><span class="sxs-lookup"><span data-stu-id="fbb44-345">Type</span></span> | <span data-ttu-id="fbb44-346">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-346">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="fbb44-347">Element</span><span class="sxs-lookup"><span data-stu-id="fbb44-347">member</span></span> | <span data-ttu-id="fbb44-348">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-348">String</span></span> | <span data-ttu-id="fbb44-349">Telefonnummer des hinzugefügten Members</span><span class="sxs-lookup"><span data-stu-id="fbb44-349">Phone Number of the added Member</span></span> |
| <span data-ttu-id="fbb44-350">memberName</span><span class="sxs-lookup"><span data-stu-id="fbb44-350">memberName</span></span> | <span data-ttu-id="fbb44-351">String</span><span class="sxs-lookup"><span data-stu-id="fbb44-351">String</span></span> | <span data-ttu-id="fbb44-352">Name des hinzugefügten Members</span><span class="sxs-lookup"><span data-stu-id="fbb44-352">Name of the added Member</span></span> |
| <span data-ttu-id="fbb44-353">type</span><span class="sxs-lookup"><span data-stu-id="fbb44-353">type</span></span> | <span data-ttu-id="fbb44-354">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fbb44-354">String</span></span> | <span data-ttu-id="fbb44-355">Mitgliedschafts Rolle des hinzugefügten Members</span><span class="sxs-lookup"><span data-stu-id="fbb44-355">Membership role of the added member</span></span> |
| <span data-ttu-id="fbb44-356">memberProfilePic</span><span class="sxs-lookup"><span data-stu-id="fbb44-356">memberProfilePic</span></span> | <span data-ttu-id="fbb44-357">url</span><span class="sxs-lookup"><span data-stu-id="fbb44-357">url</span></span> | <span data-ttu-id="fbb44-358">URL des Profils des Empfängers PIC</span><span class="sxs-lookup"><span data-stu-id="fbb44-358">url of the assignee's profile pic</span></span> |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a><span data-ttu-id="fbb44-359">Beispiel-webHook-Antwort für ' MemberAdded '/' MemberRemoved '</span><span class="sxs-lookup"><span data-stu-id="fbb44-359">Sample webHook response for 'MemberAdded' /'MemberRemoved'</span></span>
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "member": "+91xxxxxxxx",
    "memberName": "Jan Decker",
    "memberProfilePic": "https://mobileonlyapps.blob.core.windows.net/polymer-7ebb8d90e1324b5cbd61d1e10a30ada7/bbac582a4364860679d40fda7c6b.jpg",
    "type": "Member"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

