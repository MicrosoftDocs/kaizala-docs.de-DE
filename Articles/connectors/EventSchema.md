# <a name="webhook-response-schema-for-registered-events"></a><span data-ttu-id="8db2b-101">Webhook Antwortschema für registrierte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8db2b-101">Webhook response schema for registered events</span></span>

<span data-ttu-id="8db2b-102">Wenn eine Webhook registriert ist, wird eine Antwort WebHook für jedes Ereignis Kaizala auf die registrierten ObjectId für registrierte Ereignisse gefiltert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8db2b-102">If a webhook is registered, Kaizala returns a webHook response for each event on the registered objectId, filtered for registered events.</span></span> <span data-ttu-id="8db2b-103">Hier finden Sie Informationen über Schemas für verschiedene Webhook Antwort für verschiedene Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8db2b-103">Below is schema details for different webhook response for different events.</span></span>

## <a name="response-body"></a><span data-ttu-id="8db2b-104">Antworttext</span><span class="sxs-lookup"><span data-stu-id="8db2b-104">Response Body</span></span>
| <span data-ttu-id="8db2b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-105">Parameter</span></span> | <span data-ttu-id="8db2b-106">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-106">Type</span></span> | <span data-ttu-id="8db2b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-107">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-108">objectId</span><span class="sxs-lookup"><span data-stu-id="8db2b-108">objectId</span></span> | <span data-ttu-id="8db2b-109">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-109">String</span></span> | <span data-ttu-id="8db2b-110">Bezeichner, die für das Objekt, in welchen, das Kontext der Webhook erstellt wurde. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id</span><span class="sxs-lookup"><span data-stu-id="8db2b-110">Identifier representing the object in which context the webhook has been created.For ObjectType=Group, its group's Identifier, For ObjectType=Action, its actionId, For ObjectType=ActionPackage, its action-package-id</span></span> |
| <span data-ttu-id="8db2b-111">objectType</span><span class="sxs-lookup"><span data-stu-id="8db2b-111">objectType</span></span> | <span data-ttu-id="8db2b-112">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-112">String</span></span> | <span data-ttu-id="8db2b-113">Enum: "Group" / "Aktion" / "ActionPackage"</span><span class="sxs-lookup"><span data-stu-id="8db2b-113">Enum: "Group"/"Action"/"ActionPackage"</span></span> |
| <span data-ttu-id="8db2b-114">eventType</span><span class="sxs-lookup"><span data-stu-id="8db2b-114">eventType</span></span> | <span data-ttu-id="8db2b-115">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-115">String</span></span> | <span data-ttu-id="8db2b-116">Registrierte Ereignis, das aufgerufen wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-116">Registered event that has been invoked</span></span> |
| <span data-ttu-id="8db2b-117">eventId</span><span class="sxs-lookup"><span data-stu-id="8db2b-117">eventId</span></span> | <span data-ttu-id="8db2b-118">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-118">String</span></span> | <span data-ttu-id="8db2b-119">Bezeichner für das Ereignis</span><span class="sxs-lookup"><span data-stu-id="8db2b-119">Identifier representing the event</span></span> |
| <span data-ttu-id="8db2b-120">data</span><span class="sxs-lookup"><span data-stu-id="8db2b-120">data</span></span> | <span data-ttu-id="8db2b-121">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="8db2b-121">JSON Object</span></span> | <span data-ttu-id="8db2b-122">Ein Objekt, Daten, die spezifisch für dieses Ereignis darstellt.</span><span class="sxs-lookup"><span data-stu-id="8db2b-122">Object representing data specific to that event.</span></span> <span data-ttu-id="8db2b-123">Parameter für jeden unterstützten Ereignisempfänger beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8db2b-123">Parameters defined below for each of the supported event.</span></span> |
| <span data-ttu-id="8db2b-124">context</span><span class="sxs-lookup"><span data-stu-id="8db2b-124">context</span></span> | <span data-ttu-id="8db2b-125">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-125">String</span></span> | <span data-ttu-id="8db2b-126">Gibt-Wert, der bei der Registrierung einer Webhook unter Parameter 'CallbackContext' festgelegt wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-126">Returns value that has been set while registering a webhook under parameter 'callbackContext'</span></span>|
| <span data-ttu-id="8db2b-127">fromUser</span><span class="sxs-lookup"><span data-stu-id="8db2b-127">fromUser</span></span> | <span data-ttu-id="8db2b-128">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-128">String</span></span> | <span data-ttu-id="8db2b-129">Telefonnummer des Absenders</span><span class="sxs-lookup"><span data-stu-id="8db2b-129">Sender's phone number</span></span> |
| <span data-ttu-id="8db2b-130">fromUserId</span><span class="sxs-lookup"><span data-stu-id="8db2b-130">fromUserId</span></span> | <span data-ttu-id="8db2b-131">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-131">String</span></span> | <span data-ttu-id="8db2b-132">Benutzer-ID des Absenders</span><span class="sxs-lookup"><span data-stu-id="8db2b-132">Sender's userId</span></span> |
| <span data-ttu-id="8db2b-133">fromUserName</span><span class="sxs-lookup"><span data-stu-id="8db2b-133">fromUserName</span></span> | <span data-ttu-id="8db2b-134">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-134">String</span></span> | <span data-ttu-id="8db2b-135">Registrierte Namen mit Kaizala des Absenders</span><span class="sxs-lookup"><span data-stu-id="8db2b-135">Sender's registered name with Kaizala</span></span> |
| <span data-ttu-id="8db2b-136">fromUserProfilePic</span><span class="sxs-lookup"><span data-stu-id="8db2b-136">fromUserProfilePic</span></span> | <span data-ttu-id="8db2b-137">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-137">url</span></span> | <span data-ttu-id="8db2b-138">Des Absenders Profil Pic</span><span class="sxs-lookup"><span data-stu-id="8db2b-138">Sender's Profile Pic</span></span> |

<span data-ttu-id="8db2b-139">Der Parameter 'Daten' würde je nach Ereignis WebHook variieren.</span><span class="sxs-lookup"><span data-stu-id="8db2b-139">The parameter 'data' would vary depending on the webHook event.</span></span> <span data-ttu-id="8db2b-140">Schema finden Sie für jedes Ereignis unten.</span><span class="sxs-lookup"><span data-stu-id="8db2b-140">You can find schema for each event below.</span></span>

### <a name="data-for-event-textmessagecreated"></a><span data-ttu-id="8db2b-141">Daten für 'TextMessageCreated'-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8db2b-141">data for event 'TextMessageCreated'</span></span>
| <span data-ttu-id="8db2b-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-142">Parameter</span></span> | <span data-ttu-id="8db2b-143">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-143">Type</span></span> | <span data-ttu-id="8db2b-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-144">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-145">text</span><span class="sxs-lookup"><span data-stu-id="8db2b-145">text</span></span> | <span data-ttu-id="8db2b-146">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-146">String</span></span> | <span data-ttu-id="8db2b-147">Textnachricht, die gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-147">Text Message that has been sent</span></span> |

#### <a name="sample-webhook-response-for-textmessagecreated"></a><span data-ttu-id="8db2b-148">Beispiel WebHook Antwort für 'TextMessageCreated'</span><span class="sxs-lookup"><span data-stu-id="8db2b-148">Sample webHook response for 'TextMessageCreated'</span></span>
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

### <a name="data-for-event-attachmentcreated"></a><span data-ttu-id="8db2b-149">Daten für 'AttachmentCreated'-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8db2b-149">data for event 'AttachmentCreated'</span></span>
| <span data-ttu-id="8db2b-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-150">Parameter</span></span> | <span data-ttu-id="8db2b-151">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-151">Type</span></span> | <span data-ttu-id="8db2b-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-152">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-153">Medien</span><span class="sxs-lookup"><span data-stu-id="8db2b-153">media</span></span> | <span data-ttu-id="8db2b-154">Array</span><span class="sxs-lookup"><span data-stu-id="8db2b-154">Array</span></span> | <span data-ttu-id="8db2b-155">Jedes Element enthält, MediaUrl und mediaFileName</span><span class="sxs-lookup"><span data-stu-id="8db2b-155">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="8db2b-156">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="8db2b-156">mediaUrl</span></span> | <span data-ttu-id="8db2b-157">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-157">url</span></span> | <span data-ttu-id="8db2b-158">URL des Bilds</span><span class="sxs-lookup"><span data-stu-id="8db2b-158">url of the image</span></span> |
| <span data-ttu-id="8db2b-159">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="8db2b-159">mediaFileName</span></span> | <span data-ttu-id="8db2b-160">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-160">String</span></span> | <span data-ttu-id="8db2b-161">Dateiname</span><span class="sxs-lookup"><span data-stu-id="8db2b-161">Filename</span></span> |
| <span data-ttu-id="8db2b-162">actionType</span><span class="sxs-lookup"><span data-stu-id="8db2b-162">actionType</span></span> | <span data-ttu-id="8db2b-163">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-163">String</span></span> | <span data-ttu-id="8db2b-164">Enum-Wert: 'Image'</span><span class="sxs-lookup"><span data-stu-id="8db2b-164">Enum value : 'Image'</span></span> |
| <span data-ttu-id="8db2b-165">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="8db2b-165">caption</span></span> | <span data-ttu-id="8db2b-166">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-166">String</span></span> | <span data-ttu-id="8db2b-167">Beschriftung mit dem Bild zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="8db2b-167">caption attached with the image</span></span> |

#### <a name="sample-webhook-response-for-attachmentcreated"></a><span data-ttu-id="8db2b-168">Beispiel WebHook Antwort für 'AttachmentCreated'</span><span class="sxs-lookup"><span data-stu-id="8db2b-168">Sample webHook response for 'AttachmentCreated'</span></span>
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
### <a name="data-for-event-announcement"></a><span data-ttu-id="8db2b-169">Daten für das Ereignis 'Ankündigung'</span><span class="sxs-lookup"><span data-stu-id="8db2b-169">data for event 'Announcement'</span></span>
| <span data-ttu-id="8db2b-170">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-170">Parameter</span></span> | <span data-ttu-id="8db2b-171">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-171">Type</span></span> | <span data-ttu-id="8db2b-172">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-172">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-173">title</span><span class="sxs-lookup"><span data-stu-id="8db2b-173">title</span></span> | <span data-ttu-id="8db2b-174">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-174">String</span></span> | <span data-ttu-id="8db2b-175">Titel der Ankündigung Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-175">Title of Announcement Action</span></span> |
| <span data-ttu-id="8db2b-176">text</span><span class="sxs-lookup"><span data-stu-id="8db2b-176">text</span></span> | <span data-ttu-id="8db2b-177">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-177">String</span></span> | <span data-ttu-id="8db2b-178">Nachrichtentext der Ankündigung Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-178">Message body of Announcement Action</span></span> |
| <span data-ttu-id="8db2b-179">Medien</span><span class="sxs-lookup"><span data-stu-id="8db2b-179">media</span></span> | <span data-ttu-id="8db2b-180">Array</span><span class="sxs-lookup"><span data-stu-id="8db2b-180">Array</span></span> | <span data-ttu-id="8db2b-181">Jedes Element enthält, MediaUrl und mediaFileName</span><span class="sxs-lookup"><span data-stu-id="8db2b-181">Each item contains mediaUrl and mediaFileName</span></span>|
| <span data-ttu-id="8db2b-182">mediaUrl</span><span class="sxs-lookup"><span data-stu-id="8db2b-182">mediaUrl</span></span> | <span data-ttu-id="8db2b-183">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-183">url</span></span> | <span data-ttu-id="8db2b-184">URL des Bilds</span><span class="sxs-lookup"><span data-stu-id="8db2b-184">url of the image</span></span> |
| <span data-ttu-id="8db2b-185">mediaFileName</span><span class="sxs-lookup"><span data-stu-id="8db2b-185">mediaFileName</span></span> | <span data-ttu-id="8db2b-186">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-186">String</span></span> | <span data-ttu-id="8db2b-187">Dateiname</span><span class="sxs-lookup"><span data-stu-id="8db2b-187">Filename</span></span> |


#### <a name="sample-webhook-response-for-announcement"></a><span data-ttu-id="8db2b-188">Beispiel WebHook Antwort für 'Ankündigung'</span><span class="sxs-lookup"><span data-stu-id="8db2b-188">Sample webHook response for 'Announcement'</span></span>
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

### <a name="data-for-event-jobcreated"></a><span data-ttu-id="8db2b-189">Daten für 'JobCreated'-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8db2b-189">data for event 'JobCreated'</span></span>
| <span data-ttu-id="8db2b-190">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-190">Parameter</span></span> | <span data-ttu-id="8db2b-191">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-191">Type</span></span> | <span data-ttu-id="8db2b-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-192">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-193">title</span><span class="sxs-lookup"><span data-stu-id="8db2b-193">title</span></span> | <span data-ttu-id="8db2b-194">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-194">String</span></span> | <span data-ttu-id="8db2b-195">Titel der Ankündigung Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-195">Title of Announcement Action</span></span> |
| <span data-ttu-id="8db2b-196">text</span><span class="sxs-lookup"><span data-stu-id="8db2b-196">text</span></span> | <span data-ttu-id="8db2b-197">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-197">String</span></span> | <span data-ttu-id="8db2b-198">Nachrichtentext der Ankündigung Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-198">Message body of Announcement Action</span></span> |
| <span data-ttu-id="8db2b-199">actionId</span><span class="sxs-lookup"><span data-stu-id="8db2b-199">actionId</span></span> | <span data-ttu-id="8db2b-200">Id</span><span class="sxs-lookup"><span data-stu-id="8db2b-200">Id</span></span> | <span data-ttu-id="8db2b-201">Bezeichner für die betreffende Instanz des Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-201">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="8db2b-202">dueDate</span><span class="sxs-lookup"><span data-stu-id="8db2b-202">dueDate</span></span> | <span data-ttu-id="8db2b-203">Date</span><span class="sxs-lookup"><span data-stu-id="8db2b-203">Date</span></span> | <span data-ttu-id="8db2b-204">Datum nach dem Auftrag abläuft</span><span class="sxs-lookup"><span data-stu-id="8db2b-204">Date by which job would expire</span></span> |
| <span data-ttu-id="8db2b-205">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8db2b-205">assignedTo</span></span> | <span data-ttu-id="8db2b-206">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="8db2b-206">String Array</span></span> | <span data-ttu-id="8db2b-207">Array von Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="8db2b-207">Array of phone numbers</span></span> |


#### <a name="sample-webhook-response-for-jobcreated"></a><span data-ttu-id="8db2b-208">Beispiel WebHook Antwort für 'JobCreated'</span><span class="sxs-lookup"><span data-stu-id="8db2b-208">Sample webHook response for 'JobCreated'</span></span>
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

### <a name="data-for-event-jobresponse"></a><span data-ttu-id="8db2b-209">Daten für 'JobResponse'-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8db2b-209">data for event 'JobResponse'</span></span>
| <span data-ttu-id="8db2b-210">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-210">Parameter</span></span> | <span data-ttu-id="8db2b-211">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-211">Type</span></span> | <span data-ttu-id="8db2b-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-212">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-213">title</span><span class="sxs-lookup"><span data-stu-id="8db2b-213">title</span></span> | <span data-ttu-id="8db2b-214">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-214">String</span></span> | <span data-ttu-id="8db2b-215">Titel der Ankündigung Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-215">Title of Announcement Action</span></span> |
| <span data-ttu-id="8db2b-216">text</span><span class="sxs-lookup"><span data-stu-id="8db2b-216">text</span></span> | <span data-ttu-id="8db2b-217">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-217">String</span></span> | <span data-ttu-id="8db2b-218">Nachrichtentext der Ankündigung Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-218">Message body of Announcement Action</span></span> |
| <span data-ttu-id="8db2b-219">actionId</span><span class="sxs-lookup"><span data-stu-id="8db2b-219">actionId</span></span> | <span data-ttu-id="8db2b-220">Id</span><span class="sxs-lookup"><span data-stu-id="8db2b-220">Id</span></span> | <span data-ttu-id="8db2b-221">Bezeichner für die betreffende Instanz des Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-221">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="8db2b-222">groupId</span><span class="sxs-lookup"><span data-stu-id="8db2b-222">groupId</span></span> | <span data-ttu-id="8db2b-223">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-223">String</span></span> | <span data-ttu-id="8db2b-224">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="8db2b-224">Group Identifier</span></span> |
| <span data-ttu-id="8db2b-225">responseId</span><span class="sxs-lookup"><span data-stu-id="8db2b-225">responseId</span></span> | <span data-ttu-id="8db2b-226">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-226">String</span></span> | <span data-ttu-id="8db2b-227">GUID zum Identifizieren dieser Antwort</span><span class="sxs-lookup"><span data-stu-id="8db2b-227">GUID for identifying that Response</span></span> |
| <span data-ttu-id="8db2b-228">responseDetails</span><span class="sxs-lookup"><span data-stu-id="8db2b-228">responseDetails</span></span> | <span data-ttu-id="8db2b-229">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="8db2b-229">String Array</span></span> | <span data-ttu-id="8db2b-230">Array von Antwortobjekte</span><span class="sxs-lookup"><span data-stu-id="8db2b-230">Array of Response Objects</span></span> |
| <span data-ttu-id="8db2b-231">Benutzer, dem</span><span class="sxs-lookup"><span data-stu-id="8db2b-231">assignee</span></span> | <span data-ttu-id="8db2b-232">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-232">String</span></span> | <span data-ttu-id="8db2b-233">Telefonnummer der zugewiesenen Person</span><span class="sxs-lookup"><span data-stu-id="8db2b-233">Assignee's Phone Number</span></span> |
| <span data-ttu-id="8db2b-234">assigneeName</span><span class="sxs-lookup"><span data-stu-id="8db2b-234">assigneeName</span></span> | <span data-ttu-id="8db2b-235">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-235">String</span></span> | <span data-ttu-id="8db2b-236">Benutzer, die dem Namen</span><span class="sxs-lookup"><span data-stu-id="8db2b-236">Assignee's Name</span></span> |
| <span data-ttu-id="8db2b-237">assigneeProfilePic</span><span class="sxs-lookup"><span data-stu-id="8db2b-237">assigneeProfilePic</span></span> | <span data-ttu-id="8db2b-238">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-238">url</span></span> | <span data-ttu-id="8db2b-239">URL von der zugewiesenen Profil pic</span><span class="sxs-lookup"><span data-stu-id="8db2b-239">url of the assignee's profile pic</span></span> |
| <span data-ttu-id="8db2b-240">isCompleted</span><span class="sxs-lookup"><span data-stu-id="8db2b-240">isCompleted</span></span> | <span data-ttu-id="8db2b-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-241">Boolean</span></span> | <span data-ttu-id="8db2b-242">Ist der Auftrag werden abgeschlossen?</span><span class="sxs-lookup"><span data-stu-id="8db2b-242">Is the Job completed?</span></span> |




#### <a name="sample-webhook-response-for-jobresponse"></a><span data-ttu-id="8db2b-243">Beispiel WebHook Antwort für 'JobResponse'</span><span class="sxs-lookup"><span data-stu-id="8db2b-243">Sample webHook response for 'JobResponse'</span></span>
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

### <a name="data-for-event-actioncreated--surveycreated"></a><span data-ttu-id="8db2b-244">Daten für das Ereignis 'ActionCreated' / 'SurveyCreated'</span><span class="sxs-lookup"><span data-stu-id="8db2b-244">data for event 'ActionCreated' / 'SurveyCreated'</span></span>
| <span data-ttu-id="8db2b-245">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-245">Parameter</span></span> | <span data-ttu-id="8db2b-246">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-246">Type</span></span> | <span data-ttu-id="8db2b-247">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-247">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-248">actionId</span><span class="sxs-lookup"><span data-stu-id="8db2b-248">actionId</span></span> | <span data-ttu-id="8db2b-249">Id</span><span class="sxs-lookup"><span data-stu-id="8db2b-249">Id</span></span> | <span data-ttu-id="8db2b-250">Bezeichner für die betreffende Instanz des Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-250">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="8db2b-251">groupId</span><span class="sxs-lookup"><span data-stu-id="8db2b-251">groupId</span></span> | <span data-ttu-id="8db2b-252">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-252">String</span></span> | <span data-ttu-id="8db2b-253">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="8db2b-253">Group Identifier</span></span> |
| <span data-ttu-id="8db2b-254">responseId</span><span class="sxs-lookup"><span data-stu-id="8db2b-254">responseId</span></span> | <span data-ttu-id="8db2b-255">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-255">String</span></span> | <span data-ttu-id="8db2b-256">GUID zum Identifizieren dieser Antwort</span><span class="sxs-lookup"><span data-stu-id="8db2b-256">GUID for identifying that Response</span></span> |
| <span data-ttu-id="8db2b-257">Fragen</span><span class="sxs-lookup"><span data-stu-id="8db2b-257">questions</span></span> | <span data-ttu-id="8db2b-258">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="8db2b-258">String Array</span></span> | <span data-ttu-id="8db2b-259">Array von Objekten</span><span class="sxs-lookup"><span data-stu-id="8db2b-259">Array of Objects</span></span> |
| <span data-ttu-id="8db2b-260">Responder</span><span class="sxs-lookup"><span data-stu-id="8db2b-260">responder</span></span> | <span data-ttu-id="8db2b-261">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-261">String</span></span> | <span data-ttu-id="8db2b-262">Telefonnummer des Responders</span><span class="sxs-lookup"><span data-stu-id="8db2b-262">responder's Phone Number</span></span> |
| <span data-ttu-id="8db2b-263">responderName</span><span class="sxs-lookup"><span data-stu-id="8db2b-263">responderName</span></span> | <span data-ttu-id="8db2b-264">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-264">String</span></span> | <span data-ttu-id="8db2b-265">Name des Responders</span><span class="sxs-lookup"><span data-stu-id="8db2b-265">responder's Name</span></span> |
| <span data-ttu-id="8db2b-266">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="8db2b-266">responderProfilePic</span></span> | <span data-ttu-id="8db2b-267">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-267">url</span></span> | <span data-ttu-id="8db2b-268">URL der Responder Profil pic</span><span class="sxs-lookup"><span data-stu-id="8db2b-268">url of the responder's profile pic</span></span> |
| <span data-ttu-id="8db2b-269">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="8db2b-269">isAnonymous</span></span> | <span data-ttu-id="8db2b-270">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-270">Boolean</span></span> | <span data-ttu-id="8db2b-271">Die Antwort Umfrage ist anonym gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-271">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="8db2b-272">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="8db2b-272">isUpdateResponse</span></span> | <span data-ttu-id="8db2b-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-273">Boolean</span></span> | <span data-ttu-id="8db2b-274">Die Antwort aktualisiert wurde, vom Responder, nachdem die Antwort zuvor übermittelt wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-274">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="8db2b-275">Schemadetails für 'ResponseWithQuestions'-Objekt</span><span class="sxs-lookup"><span data-stu-id="8db2b-275">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="8db2b-276">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-276">Parameter</span></span> | <span data-ttu-id="8db2b-277">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-277">Type</span></span> | <span data-ttu-id="8db2b-278">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-278">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-279">title</span><span class="sxs-lookup"><span data-stu-id="8db2b-279">title</span></span> | <span data-ttu-id="8db2b-280">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-280">String</span></span> | <span data-ttu-id="8db2b-281">Frage Titel</span><span class="sxs-lookup"><span data-stu-id="8db2b-281">Question Title</span></span> |
| <span data-ttu-id="8db2b-282">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-282">type</span></span> | <span data-ttu-id="8db2b-283">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-283">String</span></span> | <span data-ttu-id="8db2b-284">QuestionType</span><span class="sxs-lookup"><span data-stu-id="8db2b-284">QuestionType</span></span> |
| <span data-ttu-id="8db2b-285">options</span><span class="sxs-lookup"><span data-stu-id="8db2b-285">options</span></span> | <span data-ttu-id="8db2b-286">Array</span><span class="sxs-lookup"><span data-stu-id="8db2b-286">Array</span></span> | <span data-ttu-id="8db2b-287">Liste der Optionen (Schlüssel / Wert-Paar) für mit mehreren choice Fragen</span><span class="sxs-lookup"><span data-stu-id="8db2b-287">List of options (key-value pair) applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="8db2b-288">isInvisible</span><span class="sxs-lookup"><span data-stu-id="8db2b-288">isInvisible</span></span> | <span data-ttu-id="8db2b-289">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-289">Boolean</span></span> | <span data-ttu-id="8db2b-290">Die Frage wird von der Benutzeroberfläche ausgeblendet werden</span><span class="sxs-lookup"><span data-stu-id="8db2b-290">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a><span data-ttu-id="8db2b-291">Beispiel-WebHook Antwort für 'ActionCreated' / 'SurveyCreated'</span><span class="sxs-lookup"><span data-stu-id="8db2b-291">Sample webHook response for 'ActionCreated' / 'SurveyCreated'</span></span>
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



### <a name="data-for-event-surveyresponse-actionresponse"></a><span data-ttu-id="8db2b-292">Daten für das Ereignis 'SurveyResponse' / 'ActionResponse'</span><span class="sxs-lookup"><span data-stu-id="8db2b-292">data for event 'SurveyResponse'/ 'ActionResponse'</span></span>
| <span data-ttu-id="8db2b-293">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-293">Parameter</span></span> | <span data-ttu-id="8db2b-294">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-294">Type</span></span> | <span data-ttu-id="8db2b-295">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-295">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-296">actionId</span><span class="sxs-lookup"><span data-stu-id="8db2b-296">actionId</span></span> | <span data-ttu-id="8db2b-297">Id</span><span class="sxs-lookup"><span data-stu-id="8db2b-297">Id</span></span> | <span data-ttu-id="8db2b-298">Bezeichner für die betreffende Instanz des Auftrags-Aktion</span><span class="sxs-lookup"><span data-stu-id="8db2b-298">Identifier for that particular instance of Job Action</span></span> |
| <span data-ttu-id="8db2b-299">groupId</span><span class="sxs-lookup"><span data-stu-id="8db2b-299">groupId</span></span> | <span data-ttu-id="8db2b-300">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-300">String</span></span> | <span data-ttu-id="8db2b-301">Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="8db2b-301">Group Identifier</span></span> |
| <span data-ttu-id="8db2b-302">responseId</span><span class="sxs-lookup"><span data-stu-id="8db2b-302">responseId</span></span> | <span data-ttu-id="8db2b-303">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-303">String</span></span> | <span data-ttu-id="8db2b-304">GUID zum Identifizieren dieser Antwort</span><span class="sxs-lookup"><span data-stu-id="8db2b-304">GUID for identifying that Response</span></span> |
| <span data-ttu-id="8db2b-305">responseDetails</span><span class="sxs-lookup"><span data-stu-id="8db2b-305">responseDetails</span></span> | <span data-ttu-id="8db2b-306">Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="8db2b-306">String Array</span></span> | <span data-ttu-id="8db2b-307">Array von 'ResponseWithQuestions'-Objekten</span><span class="sxs-lookup"><span data-stu-id="8db2b-307">Array of 'responseWithQuestions' Objects</span></span> |
| <span data-ttu-id="8db2b-308">Responder</span><span class="sxs-lookup"><span data-stu-id="8db2b-308">responder</span></span> | <span data-ttu-id="8db2b-309">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-309">String</span></span> | <span data-ttu-id="8db2b-310">Telefonnummer des Responders</span><span class="sxs-lookup"><span data-stu-id="8db2b-310">responder's Phone Number</span></span> |
| <span data-ttu-id="8db2b-311">responderName</span><span class="sxs-lookup"><span data-stu-id="8db2b-311">responderName</span></span> | <span data-ttu-id="8db2b-312">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-312">String</span></span> | <span data-ttu-id="8db2b-313">Name des Responders</span><span class="sxs-lookup"><span data-stu-id="8db2b-313">responder's Name</span></span> |
| <span data-ttu-id="8db2b-314">responderProfilePic</span><span class="sxs-lookup"><span data-stu-id="8db2b-314">responderProfilePic</span></span> | <span data-ttu-id="8db2b-315">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-315">url</span></span> | <span data-ttu-id="8db2b-316">URL der Responder Profil pic</span><span class="sxs-lookup"><span data-stu-id="8db2b-316">url of the responder's profile pic</span></span> |
| <span data-ttu-id="8db2b-317">isAnonymous</span><span class="sxs-lookup"><span data-stu-id="8db2b-317">isAnonymous</span></span> | <span data-ttu-id="8db2b-318">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-318">Boolean</span></span> | <span data-ttu-id="8db2b-319">Die Antwort Umfrage ist anonym gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-319">Is the Survey response been submitted anonymously</span></span> |
| <span data-ttu-id="8db2b-320">isUpdateResponse</span><span class="sxs-lookup"><span data-stu-id="8db2b-320">isUpdateResponse</span></span> | <span data-ttu-id="8db2b-321">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-321">Boolean</span></span> | <span data-ttu-id="8db2b-322">Die Antwort aktualisiert wurde, vom Responder, nachdem die Antwort zuvor übermittelt wurde</span><span class="sxs-lookup"><span data-stu-id="8db2b-322">Has the response been updated by responder, since the response was submitted earlier</span></span> |


#### <a name="schema-details-for-responsewithquestions-object"></a><span data-ttu-id="8db2b-323">Schemadetails für 'ResponseWithQuestions'-Objekt</span><span class="sxs-lookup"><span data-stu-id="8db2b-323">Schema details for 'responseWithQuestions' object</span></span>
| <span data-ttu-id="8db2b-324">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-324">Parameter</span></span> | <span data-ttu-id="8db2b-325">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-325">Type</span></span> | <span data-ttu-id="8db2b-326">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-326">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-327">title</span><span class="sxs-lookup"><span data-stu-id="8db2b-327">title</span></span> | <span data-ttu-id="8db2b-328">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-328">String</span></span> | <span data-ttu-id="8db2b-329">Frage Titel</span><span class="sxs-lookup"><span data-stu-id="8db2b-329">Question Title</span></span> |
| <span data-ttu-id="8db2b-330">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-330">type</span></span> | <span data-ttu-id="8db2b-331">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-331">String</span></span> | <span data-ttu-id="8db2b-332">QuestionType</span><span class="sxs-lookup"><span data-stu-id="8db2b-332">QuestionType</span></span> |
| <span data-ttu-id="8db2b-333">options</span><span class="sxs-lookup"><span data-stu-id="8db2b-333">options</span></span> | <span data-ttu-id="8db2b-334">Array</span><span class="sxs-lookup"><span data-stu-id="8db2b-334">Array</span></span> | <span data-ttu-id="8db2b-335">Liste der Optionen für mit mehreren choice Fragen</span><span class="sxs-lookup"><span data-stu-id="8db2b-335">List of options applicable for Multi-choice questions</span></span> |
| <span data-ttu-id="8db2b-336">answer</span><span class="sxs-lookup"><span data-stu-id="8db2b-336">answer</span></span> | <span data-ttu-id="8db2b-337">Array von Json-Objekt</span><span class="sxs-lookup"><span data-stu-id="8db2b-337">Array of Json Object</span></span> | <span data-ttu-id="8db2b-338">Antworten</span><span class="sxs-lookup"><span data-stu-id="8db2b-338">Answers</span></span> |
| <span data-ttu-id="8db2b-339">isInvisible</span><span class="sxs-lookup"><span data-stu-id="8db2b-339">isInvisible</span></span> | <span data-ttu-id="8db2b-340">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db2b-340">Boolean</span></span> | <span data-ttu-id="8db2b-341">Die Frage wird von der Benutzeroberfläche ausgeblendet werden</span><span class="sxs-lookup"><span data-stu-id="8db2b-341">Is the question hidden from UI</span></span> |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a><span data-ttu-id="8db2b-342">Beispiel WebHook Antwort für 'SurveyResponse' 'ActionResponse'</span><span class="sxs-lookup"><span data-stu-id="8db2b-342">Sample webHook response for 'SurveyResponse' 'ActionResponse'</span></span>
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


### <a name="data-for-event-memberadded--memberremoved"></a><span data-ttu-id="8db2b-343">Daten für das Ereignis 'MemberAdded' / 'MemberRemoved'</span><span class="sxs-lookup"><span data-stu-id="8db2b-343">data for event 'MemberAdded' / 'MemberRemoved'</span></span>
| <span data-ttu-id="8db2b-344">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db2b-344">Parameter</span></span> | <span data-ttu-id="8db2b-345">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-345">Type</span></span> | <span data-ttu-id="8db2b-346">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db2b-346">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="8db2b-347">Mitglied</span><span class="sxs-lookup"><span data-stu-id="8db2b-347">member</span></span> | <span data-ttu-id="8db2b-348">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-348">String</span></span> | <span data-ttu-id="8db2b-349">Telefonnummer des Elements hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8db2b-349">Phone Number of the added Member</span></span> |
| <span data-ttu-id="8db2b-350">memberName</span><span class="sxs-lookup"><span data-stu-id="8db2b-350">memberName</span></span> | <span data-ttu-id="8db2b-351">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-351">String</span></span> | <span data-ttu-id="8db2b-352">Name des Elements hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8db2b-352">Name of the added Member</span></span> |
| <span data-ttu-id="8db2b-353">Typ</span><span class="sxs-lookup"><span data-stu-id="8db2b-353">type</span></span> | <span data-ttu-id="8db2b-354">String</span><span class="sxs-lookup"><span data-stu-id="8db2b-354">String</span></span> | <span data-ttu-id="8db2b-355">Rolle des Elements hinzugefügt Membership</span><span class="sxs-lookup"><span data-stu-id="8db2b-355">Membership role of the added member</span></span> |
| <span data-ttu-id="8db2b-356">memberProfilePic</span><span class="sxs-lookup"><span data-stu-id="8db2b-356">memberProfilePic</span></span> | <span data-ttu-id="8db2b-357">url</span><span class="sxs-lookup"><span data-stu-id="8db2b-357">url</span></span> | <span data-ttu-id="8db2b-358">URL von der zugewiesenen Profil pic</span><span class="sxs-lookup"><span data-stu-id="8db2b-358">url of the assignee's profile pic</span></span> |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a><span data-ttu-id="8db2b-359">Beispiel-WebHook Antwort für 'MemberAdded' / 'MemberRemoved'</span><span class="sxs-lookup"><span data-stu-id="8db2b-359">Sample webHook response for 'MemberAdded' /'MemberRemoved'</span></span>
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

