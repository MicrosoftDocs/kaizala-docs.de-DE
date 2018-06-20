---
title: /Actions
description: Referenzartikel für API zum Senden/Action-Instanzen abrufen
topic: Reference
author: nitinjms
ms.openlocfilehash: 6f58e45b9eb5d4a4987c3aeb36ff8fe1862fe7bc
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905326"
---
# <a name="api-to-sendretrieve-action-instances"></a><span data-ttu-id="73f57-103">API zum Senden/Action-Instanzen abrufen</span><span class="sxs-lookup"><span data-stu-id="73f57-103">API to send/retrieve Action instances</span></span>
## <a name="actions"></a><span data-ttu-id="73f57-104">/Actions</span><span class="sxs-lookup"><span data-stu-id="73f57-104">/actions</span></span>
<span data-ttu-id="73f57-105">API-Endpunkt zu senden oder Instanzen von Kaizala Aktionen zu/aus der Unterhaltungsgruppen innerhalb Kaizala abgerufen.</span><span class="sxs-lookup"><span data-stu-id="73f57-105">API end-point to send/retrieve instances of Kaizala Actions to/from conversation groups inside Kaizala.</span></span> <span data-ttu-id="73f57-106">Aktuellen Bereich besteht darin, folgende Aktivitätstypen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="73f57-106">Current scope is to support following action types:</span></span>

| <span data-ttu-id="73f57-107">Aktion</span><span class="sxs-lookup"><span data-stu-id="73f57-107">Action</span></span> | <span data-ttu-id="73f57-108">ERSTE unterstützt</span><span class="sxs-lookup"><span data-stu-id="73f57-108">GET Supported</span></span> | <span data-ttu-id="73f57-109">POST unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73f57-109">POST Supported</span></span> | <span data-ttu-id="73f57-110">Id</span><span class="sxs-lookup"><span data-stu-id="73f57-110">Id</span></span> |
| :---: | :---: | :---: | :---: |
| <span data-ttu-id="73f57-111">Bild Anlage</span><span class="sxs-lookup"><span data-stu-id="73f57-111">Picture Attachment</span></span> | <span data-ttu-id="73f57-112">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-112">Yes</span></span> | <span data-ttu-id="73f57-113">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-113">Yes</span></span> | <span data-ttu-id="73f57-114">Abbildung</span><span class="sxs-lookup"><span data-stu-id="73f57-114">image</span></span> |
| <span data-ttu-id="73f57-115">Audio-Anlage</span><span class="sxs-lookup"><span data-stu-id="73f57-115">Audio Attachment</span></span> | <span data-ttu-id="73f57-116">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-116">No</span></span> | <span data-ttu-id="73f57-117">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-117">Yes</span></span> | <span data-ttu-id="73f57-118">audio</span><span class="sxs-lookup"><span data-stu-id="73f57-118">audio</span></span> |
| <span data-ttu-id="73f57-119">Dokument-Anlage</span><span class="sxs-lookup"><span data-stu-id="73f57-119">Document Attachment</span></span> | <span data-ttu-id="73f57-120">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-120">No</span></span> | <span data-ttu-id="73f57-121">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-121">Yes</span></span> | <span data-ttu-id="73f57-122">document</span><span class="sxs-lookup"><span data-stu-id="73f57-122">document</span></span> |
| <span data-ttu-id="73f57-123">Kontakt in der Anlage</span><span class="sxs-lookup"><span data-stu-id="73f57-123">Contact Attachment</span></span> | <span data-ttu-id="73f57-124">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-124">No</span></span> | <span data-ttu-id="73f57-125">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-125">No</span></span> | <span data-ttu-id="73f57-126">N/V</span><span class="sxs-lookup"><span data-stu-id="73f57-126">n/a</span></span> |
| <span data-ttu-id="73f57-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="73f57-127">Job</span></span> | <span data-ttu-id="73f57-128">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-128">Yes</span></span> | <span data-ttu-id="73f57-129">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-129">Yes</span></span> | <span data-ttu-id="73f57-130">Auftrag</span><span class="sxs-lookup"><span data-stu-id="73f57-130">job</span></span> |
| <span data-ttu-id="73f57-131">Umfrage</span><span class="sxs-lookup"><span data-stu-id="73f57-131">Survey</span></span> | <span data-ttu-id="73f57-132">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-132">Yes</span></span> | <span data-ttu-id="73f57-133">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-133">Yes</span></span> | <span data-ttu-id="73f57-134">Umfrage</span><span class="sxs-lookup"><span data-stu-id="73f57-134">survey</span></span> |
| <span data-ttu-id="73f57-135">Foto mit Speicherort</span><span class="sxs-lookup"><span data-stu-id="73f57-135">Photo with Location</span></span> | <span data-ttu-id="73f57-136">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-136">Yes</span></span> | <span data-ttu-id="73f57-137">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-137">No</span></span> | <span data-ttu-id="73f57-138">photoWithLocation</span><span class="sxs-lookup"><span data-stu-id="73f57-138">photoWithLocation</span></span> |
| <span data-ttu-id="73f57-139">Treffen wir uns</span><span class="sxs-lookup"><span data-stu-id="73f57-139">Let's Meet</span></span> | <span data-ttu-id="73f57-140">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-140">Yes</span></span> | <span data-ttu-id="73f57-141">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-141">Yes</span></span> | <span data-ttu-id="73f57-142">letsmeet</span><span class="sxs-lookup"><span data-stu-id="73f57-142">letsmeet</span></span> |
| <span data-ttu-id="73f57-143">Schnelle Umfrage</span><span class="sxs-lookup"><span data-stu-id="73f57-143">Quick Poll</span></span> | <span data-ttu-id="73f57-144">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-144">Yes</span></span> | <span data-ttu-id="73f57-145">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-145">Yes</span></span> | <span data-ttu-id="73f57-146">Umfrage</span><span class="sxs-lookup"><span data-stu-id="73f57-146">poll</span></span> |
| <span data-ttu-id="73f57-147">Speicherort freigeben</span><span class="sxs-lookup"><span data-stu-id="73f57-147">Share Location</span></span> | <span data-ttu-id="73f57-148">Ja</span><span class="sxs-lookup"><span data-stu-id="73f57-148">Yes</span></span> | <span data-ttu-id="73f57-149">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-149">No</span></span> | <span data-ttu-id="73f57-150">shareLocation</span><span class="sxs-lookup"><span data-stu-id="73f57-150">shareLocation</span></span> |
| <span data-ttu-id="73f57-151">Speicherort der Anforderung</span><span class="sxs-lookup"><span data-stu-id="73f57-151">Request Location</span></span> | <span data-ttu-id="73f57-152">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-152">No</span></span> | <span data-ttu-id="73f57-153">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-153">No</span></span> | <span data-ttu-id="73f57-154">N/V</span><span class="sxs-lookup"><span data-stu-id="73f57-154">n/a</span></span> |
| <span data-ttu-id="73f57-155">Live-Speicherort</span><span class="sxs-lookup"><span data-stu-id="73f57-155">Live Location</span></span> | <span data-ttu-id="73f57-156">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-156">No</span></span> | <span data-ttu-id="73f57-157">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-157">No</span></span> | <span data-ttu-id="73f57-158">N/V</span><span class="sxs-lookup"><span data-stu-id="73f57-158">n/a</span></span> |
| <span data-ttu-id="73f57-159">Announcement</span><span class="sxs-lookup"><span data-stu-id="73f57-159">Announcement</span></span> | <span data-ttu-id="73f57-160">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-160">No</span></span> | <span data-ttu-id="73f57-161">Nein</span><span class="sxs-lookup"><span data-stu-id="73f57-161">No</span></span> | <span data-ttu-id="73f57-162">N/V</span><span class="sxs-lookup"><span data-stu-id="73f57-162">n/a</span></span> |


*   <span data-ttu-id="73f57-163">API zum Abrufen von [Aktionen](actions_get.md) und [Aktionsdetails](actionDetails.md)</span><span class="sxs-lookup"><span data-stu-id="73f57-163">API to retreive [Actions](actions_get.md) and [Action details](actionDetails.md)</span></span>
*   [<span data-ttu-id="73f57-164">API neue Instanzen des Objekts Aktionen für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="73f57-164">API to post new instances of Actions</span></span>](actions_post.md)
*   [<span data-ttu-id="73f57-165">API neue Aktion Antworten/bearbeiten vorhandene Aktion Antworten für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="73f57-165">API to post new action responses/edit existing action responses</span></span>](action_responses.md)