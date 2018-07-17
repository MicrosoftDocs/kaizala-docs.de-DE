---
title: /Media
description: Referenzartikel für API zum Senden von Anlagen von Medien zu Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 3cf1e6b235d6bf324011f0b054408eb418eb0871
ms.sourcegitcommit: 523ff9067dc81712d7da2b103a3a1a0f0236b8e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2018
ms.locfileid: "20399377"
---
# <a name="media"></a><span data-ttu-id="533dc-103">/Media</span><span class="sxs-lookup"><span data-stu-id="533dc-103">/media</span></span>
<span data-ttu-id="533dc-104">API-Endpunkt zu Unterhaltungsgruppen innerhalb Kaizala Media Dateianhänge.</span><span class="sxs-lookup"><span data-stu-id="533dc-104">API end-point to send media attachments to conversation groups inside Kaizala.</span></span>

<span data-ttu-id="533dc-105">Dateiformate werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="533dc-105">Supported file formats are:</span></span>

| <span data-ttu-id="533dc-106">Medientyp</span><span class="sxs-lookup"><span data-stu-id="533dc-106">Media Type</span></span> | <span data-ttu-id="533dc-107">ActionType</span><span class="sxs-lookup"><span data-stu-id="533dc-107">ActionType</span></span> | <span data-ttu-id="533dc-108">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="533dc-108">Extension</span></span> |
|---|---|---|
| <span data-ttu-id="533dc-109">Bilder</span><span class="sxs-lookup"><span data-stu-id="533dc-109">Images</span></span> | <span data-ttu-id="533dc-110">Image</span><span class="sxs-lookup"><span data-stu-id="533dc-110">Image</span></span> | <span data-ttu-id="533dc-111">JPG, JPEG, PNG</span><span class="sxs-lookup"><span data-stu-id="533dc-111">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="533dc-112">Album</span><span class="sxs-lookup"><span data-stu-id="533dc-112">Album</span></span> | <span data-ttu-id="533dc-113">Album</span><span class="sxs-lookup"><span data-stu-id="533dc-113">Album</span></span> | <span data-ttu-id="533dc-114">JPG, JPEG, PNG</span><span class="sxs-lookup"><span data-stu-id="533dc-114">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="533dc-115">Audiodateien</span><span class="sxs-lookup"><span data-stu-id="533dc-115">Audio Files</span></span> | <span data-ttu-id="533dc-116">Audio</span><span class="sxs-lookup"><span data-stu-id="533dc-116">Audio</span></span> |<span data-ttu-id="533dc-117">MP3, WAV</span><span class="sxs-lookup"><span data-stu-id="533dc-117">.mp3, .wav</span></span> |
| <span data-ttu-id="533dc-118">Dokumente</span><span class="sxs-lookup"><span data-stu-id="533dc-118">Documents</span></span> | <span data-ttu-id="533dc-119">Document</span><span class="sxs-lookup"><span data-stu-id="533dc-119">Document</span></span> | <span data-ttu-id="533dc-120">doc-, DOCX-, xls, XLSX, PPT-, PPTX-Format, PDF</span><span class="sxs-lookup"><span data-stu-id="533dc-120">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span></span> |
| <span data-ttu-id="533dc-121">Videos</span><span class="sxs-lookup"><span data-stu-id="533dc-121">Videos</span></span> | <span data-ttu-id="533dc-122">Video</span><span class="sxs-lookup"><span data-stu-id="533dc-122">Video</span></span> | <span data-ttu-id="533dc-123">MP4, .3gpp</span><span class="sxs-lookup"><span data-stu-id="533dc-123">.mp4, .3gpp</span></span> |

<span data-ttu-id="533dc-124">Dateianhängen Medien zu Kaizala erfolgt in zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="533dc-124">Posting media attachments to Kaizala is a two step process.</span></span> <span data-ttu-id="533dc-125">Zunächst müssen Sie die Mediendatei in einem Repository mit den Endpunkt /media hochladen und verwenden Sie die Ressource URL höher als Aktion innerhalb der Kaizala für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="533dc-125">First, you will need to upload the media file to a repository using the /media endpoint and then use the resource URL later to post as an Action inside Kaizala.</span></span>

<span data-ttu-id="533dc-126">Entsprechende Inhalte-Type(mime type) muss in der Kopfzeile der Mediendatei festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="533dc-126">Corresponding content-type(mime type) needs to be set in content header of the media file.</span></span> <span data-ttu-id="533dc-127">Ohne diese api wird nicht unterstützte Media(415) Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="533dc-127">Without this api will throw unsupported Media(415) error.</span></span> 

## <a name="post-media"></a><span data-ttu-id="533dc-128">POST-/media</span><span class="sxs-lookup"><span data-stu-id="533dc-128">POST /media</span></span>

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a><span data-ttu-id="533dc-129">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="533dc-129">Request Parameters</span></span>

|  | <span data-ttu-id="533dc-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-130">Parameter</span></span> | <span data-ttu-id="533dc-131">Typ</span><span class="sxs-lookup"><span data-stu-id="533dc-131">Type</span></span> | <span data-ttu-id="533dc-132">Optional?</span><span class="sxs-lookup"><span data-stu-id="533dc-132">Optional?</span></span> | <span data-ttu-id="533dc-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533dc-133">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="533dc-134">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="533dc-134">HTTP Header</span></span> | <span data-ttu-id="533dc-135">accessToken</span><span class="sxs-lookup"><span data-stu-id="533dc-135">accessToken</span></span> | <span data-ttu-id="533dc-136">String</span><span class="sxs-lookup"><span data-stu-id="533dc-136">String</span></span> | <span data-ttu-id="533dc-137">Nein</span><span class="sxs-lookup"><span data-stu-id="533dc-137">No</span></span> | <span data-ttu-id="533dc-138">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="533dc-138">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="533dc-139">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="533dc-139">HTTP Header</span></span> | <span data-ttu-id="533dc-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="533dc-140">Content-Type</span></span> | <span data-ttu-id="533dc-141">String</span><span class="sxs-lookup"><span data-stu-id="533dc-141">String</span></span> | <span data-ttu-id="533dc-142">Nein</span><span class="sxs-lookup"><span data-stu-id="533dc-142">No</span></span> | <span data-ttu-id="533dc-143">Um anzugeben, dass eine Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="533dc-143">To indicate that a file is being uploaded.</span></span> <span data-ttu-id="533dc-144">Wert: Multipart/Formulardaten</span><span class="sxs-lookup"><span data-stu-id="533dc-144">value: multipart/form-data</span></span> |

### <a name="request-body"></a><span data-ttu-id="533dc-145">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="533dc-145">Request body</span></span>

| <span data-ttu-id="533dc-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-146">Parameter</span></span> | <span data-ttu-id="533dc-147">Typ</span><span class="sxs-lookup"><span data-stu-id="533dc-147">Type</span></span> | <span data-ttu-id="533dc-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533dc-148">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="533dc-149">POST-Text</span><span class="sxs-lookup"><span data-stu-id="533dc-149">POST Body</span></span> | <span data-ttu-id="533dc-150">files</span><span class="sxs-lookup"><span data-stu-id="533dc-150">files</span></span> | <span data-ttu-id="533dc-151">Media-Datei in einem Format Multipart/Formulardaten hochgeladen werden</span><span class="sxs-lookup"><span data-stu-id="533dc-151">Media file to be uploaded in a multipart/form-data format</span></span> |

### <a name="response-body"></a><span data-ttu-id="533dc-152">Antworttext</span><span class="sxs-lookup"><span data-stu-id="533dc-152">Response body</span></span>

| <span data-ttu-id="533dc-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-153">Parameter</span></span> | <span data-ttu-id="533dc-154">Typ</span><span class="sxs-lookup"><span data-stu-id="533dc-154">Type</span></span> | <span data-ttu-id="533dc-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533dc-155">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="533dc-156">mediaResource</span><span class="sxs-lookup"><span data-stu-id="533dc-156">mediaResource</span></span> | <span data-ttu-id="533dc-157">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="533dc-157">String</span></span> | <span data-ttu-id="533dc-158">Codierte Media-Daten in den nachfolgenden Send-Aktion Anrufe verwendet werden</span><span class="sxs-lookup"><span data-stu-id="533dc-158">Encoded media data to be used in subsequent send action calls</span></span> |

## <a name="post-groupsgroupidactions"></a><span data-ttu-id="533dc-159">POST-/groups/ {GroupId} / Aktionen</span><span class="sxs-lookup"><span data-stu-id="533dc-159">POST /groups/{groupId}/actions</span></span>

<span data-ttu-id="533dc-160">Nachdem Sie die Mediendatei hochgeladen haben, können Sie eine Mediendatei in einer Gruppe veröffentlichen, mithilfe von unten API</span><span class="sxs-lookup"><span data-stu-id="533dc-160">Once you have uploaded the media file, you can post a media file to a group by using below API</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a><span data-ttu-id="533dc-161">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="533dc-161">Request Parameters</span></span>

|  | <span data-ttu-id="533dc-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-162">Parameter</span></span> | <span data-ttu-id="533dc-163">Typ</span><span class="sxs-lookup"><span data-stu-id="533dc-163">Type</span></span> | <span data-ttu-id="533dc-164">Optional?</span><span class="sxs-lookup"><span data-stu-id="533dc-164">Optional?</span></span> | <span data-ttu-id="533dc-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533dc-165">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="533dc-166">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-166">URL Path Parameter</span></span> | <span data-ttu-id="533dc-167">groupId</span><span class="sxs-lookup"><span data-stu-id="533dc-167">groupId</span></span> | <span data-ttu-id="533dc-168">String</span><span class="sxs-lookup"><span data-stu-id="533dc-168">String</span></span> | <span data-ttu-id="533dc-169">Nein</span><span class="sxs-lookup"><span data-stu-id="533dc-169">No</span></span> | <span data-ttu-id="533dc-170">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="533dc-170">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="533dc-171">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="533dc-171">HTTP Header</span></span> | <span data-ttu-id="533dc-172">accessToken</span><span class="sxs-lookup"><span data-stu-id="533dc-172">accessToken</span></span> | <span data-ttu-id="533dc-173">String</span><span class="sxs-lookup"><span data-stu-id="533dc-173">String</span></span> | <span data-ttu-id="533dc-174">Nein</span><span class="sxs-lookup"><span data-stu-id="533dc-174">No</span></span> | <span data-ttu-id="533dc-175">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="533dc-175">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="533dc-176">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="533dc-176">HTTP Header</span></span> | <span data-ttu-id="533dc-177">Content-Type</span><span class="sxs-lookup"><span data-stu-id="533dc-177">Content-Type</span></span> | <span data-ttu-id="533dc-178">String</span><span class="sxs-lookup"><span data-stu-id="533dc-178">String</span></span> | <span data-ttu-id="533dc-179">Nein</span><span class="sxs-lookup"><span data-stu-id="533dc-179">No</span></span> | <span data-ttu-id="533dc-180">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="533dc-180">value: application/json</span></span> |

### <a name="request-body"></a><span data-ttu-id="533dc-181">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="533dc-181">Request body</span></span>

| <span data-ttu-id="533dc-182">Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-182">Parameter</span></span> | <span data-ttu-id="533dc-183">Typ</span><span class="sxs-lookup"><span data-stu-id="533dc-183">Type</span></span> | <span data-ttu-id="533dc-184">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533dc-184">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="533dc-185">actionType</span><span class="sxs-lookup"><span data-stu-id="533dc-185">actionType</span></span> | <span data-ttu-id="533dc-186">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="533dc-186">String</span></span> | <span data-ttu-id="533dc-187">ID der Kaizala Aktion senden.</span><span class="sxs-lookup"><span data-stu-id="533dc-187">Id of the Kaizala Action to send.</span></span> <span data-ttu-id="533dc-188">Finden Sie in der Tabelle oben unterstützten Dateiformaten und ihren jeweiligen ActionType.</span><span class="sxs-lookup"><span data-stu-id="533dc-188">Please refer to the table above for supported file formats and their respective ActionType.</span></span> |
| <span data-ttu-id="533dc-189">actionBody</span><span class="sxs-lookup"><span data-stu-id="533dc-189">actionBody</span></span> | <span data-ttu-id="533dc-190">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="533dc-190">JSON Object</span></span> | <span data-ttu-id="533dc-191">Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="533dc-191">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="533dc-192">Für jede der unterstützten MediaType nachstehend definierten Parameter.</span><span class="sxs-lookup"><span data-stu-id="533dc-192">Parameters defined below for each of the supported MediaType.</span></span> |

#### <a name="actionbody-for-media-files"></a><span data-ttu-id="533dc-193">ActionBody für Media-Dateien</span><span class="sxs-lookup"><span data-stu-id="533dc-193">actionBody for media files</span></span>

| <span data-ttu-id="533dc-194">Parameter</span><span class="sxs-lookup"><span data-stu-id="533dc-194">Parameter</span></span> | <span data-ttu-id="533dc-195">Typ</span><span class="sxs-lookup"><span data-stu-id="533dc-195">Type</span></span> | <span data-ttu-id="533dc-196">Optional?</span><span class="sxs-lookup"><span data-stu-id="533dc-196">Optional?</span></span> | <span data-ttu-id="533dc-197">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533dc-197">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="533dc-198">mediaResource</span><span class="sxs-lookup"><span data-stu-id="533dc-198">mediaResource</span></span> | <span data-ttu-id="533dc-199">String</span><span class="sxs-lookup"><span data-stu-id="533dc-199">String</span></span> | <span data-ttu-id="533dc-200">Nein</span><span class="sxs-lookup"><span data-stu-id="533dc-200">No</span></span> | <span data-ttu-id="533dc-201">MediaResource Zeichenfolge aus einem vorherigen Aufruf von /media, in dem Sie müssen die Anlage hochladen</span><span class="sxs-lookup"><span data-stu-id="533dc-201">MediaResource string from a previous call to /media where you need to upload the attachment</span></span> |
| <span data-ttu-id="533dc-202">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="533dc-202">caption</span></span> | <span data-ttu-id="533dc-203">String</span><span class="sxs-lookup"><span data-stu-id="533dc-203">String</span></span> | <span data-ttu-id="533dc-204">Ja</span><span class="sxs-lookup"><span data-stu-id="533dc-204">Yes</span></span> | <span data-ttu-id="533dc-205">Text Zeichenfolge, die die Mediendatei als Teil der Nachricht dargestellt mit</span><span class="sxs-lookup"><span data-stu-id="533dc-205">Text String that is shown alongwith the media file as a part of the message</span></span> |


#### <a name="sample-json-request-for-a-media-action"></a><span data-ttu-id="533dc-206">Beispiel für eine Anforderung für eine Aktion Media JSON</span><span class="sxs-lookup"><span data-stu-id="533dc-206">Sample JSON Request for a Media Action</span></span>

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

#### <a name="sample-json-response"></a><span data-ttu-id="533dc-207">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="533dc-207">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


