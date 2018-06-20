---
title: /Media
description: Referenzartikel für API zum Senden von Anlagen von Medien zu Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 0b74ce931344407b6e2962f447a0b2c8e721275e
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905348"
---
# <a name="apis-to-query-media-resources"></a><span data-ttu-id="58357-103">APIs für die Abfrage Media-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="58357-103">APIs to query media resources</span></span>
## <a name="media"></a><span data-ttu-id="58357-104">/Media</span><span class="sxs-lookup"><span data-stu-id="58357-104">/media</span></span>
<span data-ttu-id="58357-105">API-Endpunkt zu Unterhaltungsgruppen innerhalb Kaizala Media Dateianhänge.</span><span class="sxs-lookup"><span data-stu-id="58357-105">API end-point to send media attachments to conversation groups inside Kaizala.</span></span>

<span data-ttu-id="58357-106">Dateiformate werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="58357-106">Supported file formats are:</span></span>

| <span data-ttu-id="58357-107">Medientyp</span><span class="sxs-lookup"><span data-stu-id="58357-107">Media Type</span></span> | <span data-ttu-id="58357-108">ActionType</span><span class="sxs-lookup"><span data-stu-id="58357-108">ActionType</span></span> | <span data-ttu-id="58357-109">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="58357-109">Extension</span></span> |
|---|---|---|
| <span data-ttu-id="58357-110">Bilder</span><span class="sxs-lookup"><span data-stu-id="58357-110">Images</span></span> | <span data-ttu-id="58357-111">Image</span><span class="sxs-lookup"><span data-stu-id="58357-111">Image</span></span> | <span data-ttu-id="58357-112">JPG, JPEG, PNG</span><span class="sxs-lookup"><span data-stu-id="58357-112">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="58357-113">Album</span><span class="sxs-lookup"><span data-stu-id="58357-113">Album</span></span> | <span data-ttu-id="58357-114">Album</span><span class="sxs-lookup"><span data-stu-id="58357-114">Album</span></span> | <span data-ttu-id="58357-115">JPG, JPEG, PNG</span><span class="sxs-lookup"><span data-stu-id="58357-115">.jpg, .jpeg, .png</span></span> |
| <span data-ttu-id="58357-116">Audiodateien</span><span class="sxs-lookup"><span data-stu-id="58357-116">Audio Files</span></span> | <span data-ttu-id="58357-117">Audio</span><span class="sxs-lookup"><span data-stu-id="58357-117">Audio</span></span> |<span data-ttu-id="58357-118">MP3, WAV</span><span class="sxs-lookup"><span data-stu-id="58357-118">.mp3, .wav</span></span> |
| <span data-ttu-id="58357-119">Dokumente</span><span class="sxs-lookup"><span data-stu-id="58357-119">Documents</span></span> | <span data-ttu-id="58357-120">Document</span><span class="sxs-lookup"><span data-stu-id="58357-120">Document</span></span> | <span data-ttu-id="58357-121">doc-, DOCX-, xls, XLSX, PPT-, PPTX-Format, PDF</span><span class="sxs-lookup"><span data-stu-id="58357-121">.doc, .docx, .xls, .xlsx, .ppt, .pptx, .pdf</span></span> |
| <span data-ttu-id="58357-122">Videos</span><span class="sxs-lookup"><span data-stu-id="58357-122">Videos</span></span> | <span data-ttu-id="58357-123">Video</span><span class="sxs-lookup"><span data-stu-id="58357-123">Video</span></span> | <span data-ttu-id="58357-124">MP4, .3gpp</span><span class="sxs-lookup"><span data-stu-id="58357-124">.mp4, .3gpp</span></span> |

<span data-ttu-id="58357-125">Dateianhängen Medien zu Kaizala erfolgt in zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="58357-125">Posting media attachments to Kaizala is a two step process.</span></span> <span data-ttu-id="58357-126">Zunächst müssen Sie die Mediendatei in einem Repository mit den Endpunkt /media hochladen und verwenden Sie die Ressource URL höher als Aktion innerhalb der Kaizala für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="58357-126">First, you will need to upload the media file to a repository using the /media endpoint and then use the resource URL later to post as an Action inside Kaizala.</span></span>

<span data-ttu-id="58357-127">Entsprechende Inhalte-Type(mime type) muss in der Kopfzeile der Mediendatei festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58357-127">Corresponding content-type(mime type) needs to be set in content header of the media file.</span></span> <span data-ttu-id="58357-128">Ohne diese api wird nicht unterstützte Media(415) Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="58357-128">Without this api will throw unsupported Media(415) error.</span></span> 

### <a name="post-media"></a><span data-ttu-id="58357-129">POST-/media</span><span class="sxs-lookup"><span data-stu-id="58357-129">POST /media</span></span>

    POST {endpoint-url}/v1/media

##### <a name="request-parameters"></a><span data-ttu-id="58357-130">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="58357-130">Request Parameters</span></span>

|  | <span data-ttu-id="58357-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-131">Parameter</span></span> | <span data-ttu-id="58357-132">Typ</span><span class="sxs-lookup"><span data-stu-id="58357-132">Type</span></span> | <span data-ttu-id="58357-133">Optional?</span><span class="sxs-lookup"><span data-stu-id="58357-133">Optional?</span></span> | <span data-ttu-id="58357-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58357-134">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="58357-135">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="58357-135">HTTP Header</span></span> | <span data-ttu-id="58357-136">accessToken</span><span class="sxs-lookup"><span data-stu-id="58357-136">accessToken</span></span> | <span data-ttu-id="58357-137">String</span><span class="sxs-lookup"><span data-stu-id="58357-137">String</span></span> | <span data-ttu-id="58357-138">Nein</span><span class="sxs-lookup"><span data-stu-id="58357-138">No</span></span> | <span data-ttu-id="58357-139">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="58357-139">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="58357-140">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="58357-140">HTTP Header</span></span> | <span data-ttu-id="58357-141">Content-Type</span><span class="sxs-lookup"><span data-stu-id="58357-141">Content-Type</span></span> | <span data-ttu-id="58357-142">String</span><span class="sxs-lookup"><span data-stu-id="58357-142">String</span></span> | <span data-ttu-id="58357-143">Nein</span><span class="sxs-lookup"><span data-stu-id="58357-143">No</span></span> | <span data-ttu-id="58357-144">Um anzugeben, dass eine Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="58357-144">To indicate that a file is being uploaded.</span></span> <span data-ttu-id="58357-145">Wert: Multipart/Formulardaten</span><span class="sxs-lookup"><span data-stu-id="58357-145">value: multipart/form-data</span></span> |

##### <a name="request-body"></a><span data-ttu-id="58357-146">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="58357-146">Request body</span></span>

| <span data-ttu-id="58357-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-147">Parameter</span></span> | <span data-ttu-id="58357-148">Typ</span><span class="sxs-lookup"><span data-stu-id="58357-148">Type</span></span> | <span data-ttu-id="58357-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58357-149">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="58357-150">POST-Text</span><span class="sxs-lookup"><span data-stu-id="58357-150">POST Body</span></span> | <span data-ttu-id="58357-151">files</span><span class="sxs-lookup"><span data-stu-id="58357-151">files</span></span> | <span data-ttu-id="58357-152">Media-Datei in einem Format Multipart/Formulardaten hochgeladen werden</span><span class="sxs-lookup"><span data-stu-id="58357-152">Media file to be uploaded in a multipart/form-data format</span></span> |

##### <a name="response-body"></a><span data-ttu-id="58357-153">Antworttext</span><span class="sxs-lookup"><span data-stu-id="58357-153">Response body</span></span>

| <span data-ttu-id="58357-154">Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-154">Parameter</span></span> | <span data-ttu-id="58357-155">Typ</span><span class="sxs-lookup"><span data-stu-id="58357-155">Type</span></span> | <span data-ttu-id="58357-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58357-156">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="58357-157">mediaResource</span><span class="sxs-lookup"><span data-stu-id="58357-157">mediaResource</span></span> | <span data-ttu-id="58357-158">String</span><span class="sxs-lookup"><span data-stu-id="58357-158">String</span></span> | <span data-ttu-id="58357-159">Codierte Media-Daten in den nachfolgenden Send-Aktion Anrufe verwendet werden</span><span class="sxs-lookup"><span data-stu-id="58357-159">Encoded media data to be used in subsequent send action calls</span></span> |

### <a name="post-groupsgroupidactions"></a><span data-ttu-id="58357-160">POST-/groups/ {GroupId} / Aktionen</span><span class="sxs-lookup"><span data-stu-id="58357-160">POST /groups/{groupId}/actions</span></span>

<span data-ttu-id="58357-161">Nachdem Sie die Mediendatei hochgeladen haben, können Sie eine Mediendatei in einer Gruppe veröffentlichen, mithilfe von unten API</span><span class="sxs-lookup"><span data-stu-id="58357-161">Once you have uploaded the media file, you can post a media file to a group by using below API</span></span>

    POST {endpoint-url}/v1/groups/{groupId}/actions

##### <a name="request-parameters"></a><span data-ttu-id="58357-162">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="58357-162">Request Parameters</span></span>

|  | <span data-ttu-id="58357-163">Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-163">Parameter</span></span> | <span data-ttu-id="58357-164">Typ</span><span class="sxs-lookup"><span data-stu-id="58357-164">Type</span></span> | <span data-ttu-id="58357-165">Optional?</span><span class="sxs-lookup"><span data-stu-id="58357-165">Optional?</span></span> | <span data-ttu-id="58357-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58357-166">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="58357-167">URL-Pfad-Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-167">URL Path Parameter</span></span> | <span data-ttu-id="58357-168">groupId</span><span class="sxs-lookup"><span data-stu-id="58357-168">groupId</span></span> | <span data-ttu-id="58357-169">String</span><span class="sxs-lookup"><span data-stu-id="58357-169">String</span></span> | <span data-ttu-id="58357-170">Nein</span><span class="sxs-lookup"><span data-stu-id="58357-170">No</span></span> | <span data-ttu-id="58357-171">GUID, die die GroupId der Ressource bestimmte Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="58357-171">GUID representing the groupId of the specific group resource</span></span> |
| <span data-ttu-id="58357-172">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="58357-172">HTTP Header</span></span> | <span data-ttu-id="58357-173">accessToken</span><span class="sxs-lookup"><span data-stu-id="58357-173">accessToken</span></span> | <span data-ttu-id="58357-174">String</span><span class="sxs-lookup"><span data-stu-id="58357-174">String</span></span> | <span data-ttu-id="58357-175">Nein</span><span class="sxs-lookup"><span data-stu-id="58357-175">No</span></span> | <span data-ttu-id="58357-176">Access Token vom Auth Endpunkt</span><span class="sxs-lookup"><span data-stu-id="58357-176">Access Token received from the auth end-point</span></span> |
| <span data-ttu-id="58357-177">HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="58357-177">HTTP Header</span></span> | <span data-ttu-id="58357-178">Content-Type</span><span class="sxs-lookup"><span data-stu-id="58357-178">Content-Type</span></span> | <span data-ttu-id="58357-179">String</span><span class="sxs-lookup"><span data-stu-id="58357-179">String</span></span> | <span data-ttu-id="58357-180">Nein</span><span class="sxs-lookup"><span data-stu-id="58357-180">No</span></span> | <span data-ttu-id="58357-181">Wert: Application/Json</span><span class="sxs-lookup"><span data-stu-id="58357-181">value: application/json</span></span> |

##### <a name="request-body"></a><span data-ttu-id="58357-182">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="58357-182">Request body</span></span>

| <span data-ttu-id="58357-183">Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-183">Parameter</span></span> | <span data-ttu-id="58357-184">Typ</span><span class="sxs-lookup"><span data-stu-id="58357-184">Type</span></span> | <span data-ttu-id="58357-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58357-185">Description</span></span> |
| :---: | :---: | :--- |
| <span data-ttu-id="58357-186">actionType</span><span class="sxs-lookup"><span data-stu-id="58357-186">actionType</span></span> | <span data-ttu-id="58357-187">String</span><span class="sxs-lookup"><span data-stu-id="58357-187">String</span></span> | <span data-ttu-id="58357-188">ID der Kaizala Aktion senden.</span><span class="sxs-lookup"><span data-stu-id="58357-188">Id of the Kaizala Action to send.</span></span> <span data-ttu-id="58357-189">Finden Sie in der Tabelle oben unterstützten Dateiformaten und ihren jeweiligen ActionType.</span><span class="sxs-lookup"><span data-stu-id="58357-189">Please refer to the table above for supported file formats and their respective ActionType.</span></span> |
| <span data-ttu-id="58357-190">actionBody</span><span class="sxs-lookup"><span data-stu-id="58357-190">actionBody</span></span> | <span data-ttu-id="58357-191">JSON-Objekt</span><span class="sxs-lookup"><span data-stu-id="58357-191">JSON Object</span></span> | <span data-ttu-id="58357-192">Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="58357-192">Object representing data needed for the respective Action.</span></span> <span data-ttu-id="58357-193">Für jede der unterstützten MediaType nachstehend definierten Parameter.</span><span class="sxs-lookup"><span data-stu-id="58357-193">Parameters defined below for each of the supported MediaType.</span></span> |

###### <a name="actionbody-for-media-files"></a><span data-ttu-id="58357-194">ActionBody für Media-Dateien</span><span class="sxs-lookup"><span data-stu-id="58357-194">actionBody for media files</span></span>

| <span data-ttu-id="58357-195">Parameter</span><span class="sxs-lookup"><span data-stu-id="58357-195">Parameter</span></span> | <span data-ttu-id="58357-196">Typ</span><span class="sxs-lookup"><span data-stu-id="58357-196">Type</span></span> | <span data-ttu-id="58357-197">Optional?</span><span class="sxs-lookup"><span data-stu-id="58357-197">Optional?</span></span> | <span data-ttu-id="58357-198">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58357-198">Description</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="58357-199">mediaResource</span><span class="sxs-lookup"><span data-stu-id="58357-199">mediaResource</span></span> | <span data-ttu-id="58357-200">String</span><span class="sxs-lookup"><span data-stu-id="58357-200">String</span></span> | <span data-ttu-id="58357-201">Nein</span><span class="sxs-lookup"><span data-stu-id="58357-201">No</span></span> | <span data-ttu-id="58357-202">MediaResource Zeichenfolge aus einem vorherigen Aufruf von /media, in dem Sie müssen die Anlage hochladen</span><span class="sxs-lookup"><span data-stu-id="58357-202">MediaResource string from a previous call to /media where you need to upload the attachment</span></span> |
| <span data-ttu-id="58357-203">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="58357-203">caption</span></span> | <span data-ttu-id="58357-204">String</span><span class="sxs-lookup"><span data-stu-id="58357-204">String</span></span> | <span data-ttu-id="58357-205">Ja</span><span class="sxs-lookup"><span data-stu-id="58357-205">Yes</span></span> | <span data-ttu-id="58357-206">Text Zeichenfolge, die die Mediendatei als Teil der Nachricht dargestellt mit</span><span class="sxs-lookup"><span data-stu-id="58357-206">Text String that is shown alongwith the media file as a part of the message</span></span> |


###### <a name="sample-json-request-for-a-media-action"></a><span data-ttu-id="58357-207">Beispiel für eine Anforderung für eine Aktion Media JSON</span><span class="sxs-lookup"><span data-stu-id="58357-207">Sample JSON Request for a Media Action</span></span>

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

###### <a name="sample-json-response"></a><span data-ttu-id="58357-208">Beispiel von JSON-Antwort</span><span class="sxs-lookup"><span data-stu-id="58357-208">Sample JSON Response</span></span>

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


