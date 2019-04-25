---
title: /Media
description: Referenzartikel zur API zum Senden von Medien Anlagen an Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 3cf1e6b235d6bf324011f0b054408eb418eb0871
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190694"
---
# <a name="media"></a><span data-ttu-id="7acaf-103">/Media</span><span class="sxs-lookup"><span data-stu-id="7acaf-103">/media</span></span>
<span data-ttu-id="7acaf-104">API-Endpunkt zum Senden von Medien Anlagen an unterhaltungsgruppen innerhalb von Kaizala.</span><span class="sxs-lookup"><span data-stu-id="7acaf-104">API end-point to send media attachments to conversation groups inside Kaizala.</span></span>

<span data-ttu-id="7acaf-105">Unterstützte Dateiformate sind:</span><span class="sxs-lookup"><span data-stu-id="7acaf-105">Supported file formats are:</span></span>

| <span data-ttu-id="7acaf-106">Medientyp</span><span class="sxs-lookup"><span data-stu-id="7acaf-106">Media Type</span></span> | <span data-ttu-id="7acaf-107">ActionType</span><span class="sxs-lookup"><span data-stu-id="7acaf-107">ActionType</span></span> | <span data-ttu-id="7acaf-108">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7acaf-108">Extension</span></span> |
|---|---|---|
| <span data-ttu-id="7acaf-109">Bilder</span><span class="sxs-lookup"><span data-stu-id="7acaf-109">Images</span></span> | <span data-ttu-id="7acaf-110">Image</span><span class="sxs-lookup"><span data-stu-id="7acaf-110">Image</span></span> | <span data-ttu-id="7acaf-111">. jpg,. JPEG,. png</span><span class="sxs-lookup"><span data-stu-id="7acaf-111">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="7acaf-112">Album</span><span class="sxs-lookup"><span data-stu-id="7acaf-112">Album</span></span> | <span data-ttu-id="7acaf-113">Album</span><span class="sxs-lookup"><span data-stu-id="7acaf-113">Album</span></span> | <span data-ttu-id="7acaf-114">. jpg,. JPEG,. png</span><span class="sxs-lookup"><span data-stu-id="7acaf-114">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="7acaf-115">AudioDateien</span><span class="sxs-lookup"><span data-stu-id="7acaf-115">Audio Files</span></span> | <span data-ttu-id="7acaf-116">Audio</span><span class="sxs-lookup"><span data-stu-id="7acaf-116">Audio</span></span> |<span data-ttu-id="7acaf-117">. MP3,. wav</span><span class="sxs-lookup"><span data-stu-id="7acaf-117">.mp3, .wav</span></span> |
| <span data-ttu-id="7acaf-118">Dokumente</span><span class="sxs-lookup"><span data-stu-id="7acaf-118">Documents</span></span> | <span data-ttu-id="7acaf-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="7acaf-119">Document</span></span> | <span data-ttu-id="7acaf-120">. doc,. docx,. xls,. xlsx,. ppt,. pptx,. PDF</span><span class="sxs-lookup"><span data-stu-id="7acaf-120">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span></span> |
| <span data-ttu-id="7acaf-121">Videos</span><span class="sxs-lookup"><span data-stu-id="7acaf-121">Videos</span></span> | <span data-ttu-id="7acaf-122">Video</span><span class="sxs-lookup"><span data-stu-id="7acaf-122">Video</span></span> | <span data-ttu-id="7acaf-123">. MP4,. 3GPP</span><span class="sxs-lookup"><span data-stu-id="7acaf-123">.mp4, .3gpp</span></span> |

<span data-ttu-id="7acaf-124">Das Veröffentlichen von Medien Anlagen an Kaizala erfolgt in zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="7acaf-124">Posting media attachments to Kaizala is a two step process.</span></span> <span data-ttu-id="7acaf-125">Zunächst müssen Sie die Mediendatei mithilfe des/Media-Endpunkts in ein Repository hochladen und dann später die Ressourcen-URL als Aktion innerhalb von Kaizala bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7acaf-125">First, you will need to upload the media file to a repository using the /media endpoint and then use the resource URL later to post as an Action inside Kaizala.</span></span>

<span data-ttu-id="7acaf-126">Der entsprechende Inhaltstyp (MIME-Typ) muss in der Inhalts Kopfzeile der Mediendatei festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7acaf-126">Corresponding content-type(mime type) needs to be set in content header of the media file.</span></span> <span data-ttu-id="7acaf-127">Ohne diese API werden nicht unterstützte Medien (415) Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7acaf-127">Without this api will throw unsupported Media(415) error.</span></span> 

## <a name="post-media"></a><span data-ttu-id="7acaf-128">POST/Media</span><span class="sxs-lookup"><span data-stu-id="7acaf-128">POST /media</span></span>

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a><span data-ttu-id="7acaf-129">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-129">Request Parameters</span></span>

|  | <span data-ttu-id="7acaf-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-130">Parameter</span></span> | <span data-ttu-id="7acaf-131">Typ</span><span class="sxs-lookup"><span data-stu-id="7acaf-131">Type</span></span> | <span data-ttu-id="7acaf-132">Optional?</span><span class="sxs-lookup"><span data-stu-id="7acaf-132">Optional?</span></span> | <span data-ttu-id="7acaf-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7acaf-133">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7acaf-134">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7acaf-134">HTTP Header</span></span> | <span data-ttu-id="7acaf-135">accessToken</span><span class="sxs-lookup"><span data-stu-id="7acaf-135">accessToken</span></span> | <span data-ttu-id="7acaf-136">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-136">String</span></span> | <span data-ttu-id="7acaf-137">Nein</span><span class="sxs-lookup"><span data-stu-id="7acaf-137">No</span></span> | <span data-ttu-id="7acaf-138">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="7acaf-138">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="7acaf-139">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7acaf-139">HTTP Header</span></span> | <span data-ttu-id="7acaf-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7acaf-140">Content-Type</span></span> | <span data-ttu-id="7acaf-141">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-141">String</span></span> | <span data-ttu-id="7acaf-142">Nein</span><span class="sxs-lookup"><span data-stu-id="7acaf-142">No</span></span> | <span data-ttu-id="7acaf-143">, Um anzugeben, dass eine Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="7acaf-143">To indicate that a file is being uploaded.</span></span> <span data-ttu-id="7acaf-144">Wert: Multipart/Form-Data</span><span class="sxs-lookup"><span data-stu-id="7acaf-144">value: multipart/form-data</span></span> |

### <a name="request-body"></a><span data-ttu-id="7acaf-145">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="7acaf-145">Request body</span></span>

| <span data-ttu-id="7acaf-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-146">Parameter</span></span> | <span data-ttu-id="7acaf-147">Typ</span><span class="sxs-lookup"><span data-stu-id="7acaf-147">Type</span></span> | <span data-ttu-id="7acaf-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7acaf-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7acaf-149">POST-Textkörper</span><span class="sxs-lookup"><span data-stu-id="7acaf-149">POST Body</span></span> | <span data-ttu-id="7acaf-150">files</span><span class="sxs-lookup"><span data-stu-id="7acaf-150">files</span></span> | <span data-ttu-id="7acaf-151">Mediendatei, die in einem mehrteiligen/Formular-Datenformat hochgeladen werden soll</span><span class="sxs-lookup"><span data-stu-id="7acaf-151">Media file to be uploaded in a multipart/form-data format</span></span> |

### <a name="response-body"></a><span data-ttu-id="7acaf-152">Antworttext</span><span class="sxs-lookup"><span data-stu-id="7acaf-152">Response body</span></span>

| <span data-ttu-id="7acaf-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-153">Parameter</span></span> | <span data-ttu-id="7acaf-154">Typ</span><span class="sxs-lookup"><span data-stu-id="7acaf-154">Type</span></span> | <span data-ttu-id="7acaf-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7acaf-155">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7acaf-156">mediaResource</span><span class="sxs-lookup"><span data-stu-id="7acaf-156">mediaResource</span></span> | <span data-ttu-id="7acaf-157">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-157">String</span></span> | <span data-ttu-id="7acaf-158">Codierte Mediendaten, die bei nachfolgenden Sende Aktionsaufrufen verwendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="7acaf-158">Encoded media data to be used in subsequent send action calls</span></span> |

## <a name="post-groupsgroupidactions"></a><span data-ttu-id="7acaf-159">POST/groups/{groupId}/actions</span><span class="sxs-lookup"><span data-stu-id="7acaf-159">POST /groups/{groupId}/actions</span></span>

<span data-ttu-id="7acaf-160">Nachdem Sie die Mediendatei hochgeladen haben, können Sie mithilfe der folgenden API eine Mediendatei in einer Gruppe veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="7acaf-160">Once you have uploaded the media file, you can post a media file to a group by using below API</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="7acaf-161">AnforderungsParameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-161">Request Parameters</span></span>

|  | <span data-ttu-id="7acaf-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-162">Parameter</span></span> | <span data-ttu-id="7acaf-163">Typ</span><span class="sxs-lookup"><span data-stu-id="7acaf-163">Type</span></span> | <span data-ttu-id="7acaf-164">Optional?</span><span class="sxs-lookup"><span data-stu-id="7acaf-164">Optional?</span></span> | <span data-ttu-id="7acaf-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7acaf-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="7acaf-166">URL-Pfad Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-166">URL Path Parameter</span></span> | <span data-ttu-id="7acaf-167">groupId</span><span class="sxs-lookup"><span data-stu-id="7acaf-167">groupId</span></span> | <span data-ttu-id="7acaf-168">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-168">String</span></span> | <span data-ttu-id="7acaf-169">Nein</span><span class="sxs-lookup"><span data-stu-id="7acaf-169">No</span></span> | <span data-ttu-id="7acaf-170">GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt</span><span class="sxs-lookup"><span data-stu-id="7acaf-170">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="7acaf-171">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7acaf-171">HTTP Header</span></span> | <span data-ttu-id="7acaf-172">accessToken</span><span class="sxs-lookup"><span data-stu-id="7acaf-172">accessToken</span></span> | <span data-ttu-id="7acaf-173">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-173">String</span></span> | <span data-ttu-id="7acaf-174">Nein</span><span class="sxs-lookup"><span data-stu-id="7acaf-174">No</span></span> | <span data-ttu-id="7acaf-175">Vom Endpunkt auth empfangenes Zugriffs Token</span><span class="sxs-lookup"><span data-stu-id="7acaf-175">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="7acaf-176">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="7acaf-176">HTTP Header</span></span> | <span data-ttu-id="7acaf-177">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7acaf-177">Content-Type</span></span> | <span data-ttu-id="7acaf-178">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-178">String</span></span> | <span data-ttu-id="7acaf-179">Nein</span><span class="sxs-lookup"><span data-stu-id="7acaf-179">No</span></span> | <span data-ttu-id="7acaf-180">Wert: Application/JSON</span><span class="sxs-lookup"><span data-stu-id="7acaf-180">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="7acaf-181">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="7acaf-181">Request body</span></span>

| <span data-ttu-id="7acaf-182">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-182">Parameter</span></span> | <span data-ttu-id="7acaf-183">Typ</span><span class="sxs-lookup"><span data-stu-id="7acaf-183">Type</span></span> | <span data-ttu-id="7acaf-184">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7acaf-184">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="7acaf-185">actionType</span><span class="sxs-lookup"><span data-stu-id="7acaf-185">actionType</span></span> | <span data-ttu-id="7acaf-186">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-186">String</span></span> | <span data-ttu-id="7acaf-187">ID der zu sendenden Kaizala-Aktion.</span><span class="sxs-lookup"><span data-stu-id="7acaf-187">Id of the Kaizala Action to send.</span></span> <span data-ttu-id="7acaf-188">Unterstützte Dateiformate und deren jeweiliger Action Type finden Sie in der obigen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7acaf-188">Please refer to the table above for supported file formats and their respective ActionType.</span></span> |
| <span data-ttu-id="7acaf-189">actionBody</span><span class="sxs-lookup"><span data-stu-id="7acaf-189">actionBody</span></span> | <span data-ttu-id="7acaf-190">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="7acaf-190">JSON Object</span></span> | <span data-ttu-id="7acaf-191">Objekt, das die für die jeweilige Aktion erforderlichen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="7acaf-191">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="7acaf-192">Die unten definierten Parameter für jeden der unterstützten MediaType.</span><span class="sxs-lookup"><span data-stu-id="7acaf-192">Parameters defined below for each of the supported MediaType.</span></span> |

#### <a name="actionbody-for-media-files"></a><span data-ttu-id="7acaf-193">actionBody für Mediendateien</span><span class="sxs-lookup"><span data-stu-id="7acaf-193">actionBody for media files</span></span>

| <span data-ttu-id="7acaf-194">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acaf-194">Parameter</span></span> | <span data-ttu-id="7acaf-195">Typ</span><span class="sxs-lookup"><span data-stu-id="7acaf-195">Type</span></span> | <span data-ttu-id="7acaf-196">Optional?</span><span class="sxs-lookup"><span data-stu-id="7acaf-196">Optional?</span></span> | <span data-ttu-id="7acaf-197">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7acaf-197">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="7acaf-198">mediaResource</span><span class="sxs-lookup"><span data-stu-id="7acaf-198">mediaResource</span></span> | <span data-ttu-id="7acaf-199">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-199">String</span></span> | <span data-ttu-id="7acaf-200">Nein</span><span class="sxs-lookup"><span data-stu-id="7acaf-200">No</span></span> | <span data-ttu-id="7acaf-201">MediaResource-Zeichenfolge aus einem vorherigen Aufruf an/Media, in dem Sie die Anlage hochladen müssen</span><span class="sxs-lookup"><span data-stu-id="7acaf-201">MediaResource string from a previous call to /media where you need to upload the attachment</span></span> |
| <span data-ttu-id="7acaf-202">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="7acaf-202">caption</span></span> | <span data-ttu-id="7acaf-203">String</span><span class="sxs-lookup"><span data-stu-id="7acaf-203">String</span></span> | <span data-ttu-id="7acaf-204">Ja</span><span class="sxs-lookup"><span data-stu-id="7acaf-204">Yes</span></span> | <span data-ttu-id="7acaf-205">Text Zeichenfolge, die alongwith der Mediendatei als Teil der Nachricht angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="7acaf-205">Text String that is shown alongwith the media file as a part of the message</span></span> |


#### <a name="sample-json-request-for-a-media-action"></a><span data-ttu-id="7acaf-206">JSON-Beispielanforderung für eine Medienaktion</span><span class="sxs-lookup"><span data-stu-id="7acaf-206">Sample JSON Request for a Media Action</span></span>

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

#### <a name="sample-json-response"></a><span data-ttu-id="7acaf-207">JSON-Beispielantwort</span><span class="sxs-lookup"><span data-stu-id="7acaf-207">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


