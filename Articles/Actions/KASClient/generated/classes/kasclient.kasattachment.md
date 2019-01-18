---
ms.openlocfilehash: 5ea10ec4a326c6ae1ceaae4db8a2994d25e17fce
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728078"
---
<span data-ttu-id="25be0-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="25be0-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)</span></span>

# <a name="class-kasattachment"></a><span data-ttu-id="25be0-102">Klasse: KASAttachment</span><span class="sxs-lookup"><span data-stu-id="25be0-102">Class: KASAttachment</span></span>

## <a name="hierarchy"></a><span data-ttu-id="25be0-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="25be0-103">Hierarchy</span></span>

<span data-ttu-id="25be0-104">**KASAttachment**</span><span class="sxs-lookup"><span data-stu-id="25be0-104">**KASAttachment**</span></span>

<span data-ttu-id="25be0-105">↳ [KASAudioAttachment](kasclient.kasaudioattachment.md)</span><span class="sxs-lookup"><span data-stu-id="25be0-105">↳  [KASAudioAttachment](kasclient.kasaudioattachment.md)</span></span>

<span data-ttu-id="25be0-106">↳ [KASImageAttachment](kasclient.kasimageattachment.md)</span><span class="sxs-lookup"><span data-stu-id="25be0-106">↳  [KASImageAttachment](kasclient.kasimageattachment.md)</span></span>

<span data-ttu-id="25be0-107">↳ [KASVideoAttachment](kasclient.kasvideoattachment.md)</span><span class="sxs-lookup"><span data-stu-id="25be0-107">↳  [KASVideoAttachment](kasclient.kasvideoattachment.md)</span></span>

## <a name="index"></a><span data-ttu-id="25be0-108">Index </span><span class="sxs-lookup"><span data-stu-id="25be0-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="25be0-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25be0-109">Properties</span></span>

* [<span data-ttu-id="25be0-110">attachmentId</span><span class="sxs-lookup"><span data-stu-id="25be0-110">attachmentId</span></span>](kasclient.kasattachment.md#attachmentid)
* [<span data-ttu-id="25be0-111">fileName</span><span class="sxs-lookup"><span data-stu-id="25be0-111">fileName</span></span>](kasclient.kasattachment.md#filename)
* [<span data-ttu-id="25be0-112">hasSetThumbnail</span><span class="sxs-lookup"><span data-stu-id="25be0-112">hasSetThumbnail</span></span>](kasclient.kasattachment.md#hassetthumbnail)
* [<span data-ttu-id="25be0-113">localPath</span><span class="sxs-lookup"><span data-stu-id="25be0-113">localPath</span></span>](kasclient.kasattachment.md#localpath)
* [<span data-ttu-id="25be0-114">requireHighResThumbnail</span><span class="sxs-lookup"><span data-stu-id="25be0-114">requireHighResThumbnail</span></span>](kasclient.kasattachment.md#requirehighresthumbnail)
* [<span data-ttu-id="25be0-115">serverPath</span><span class="sxs-lookup"><span data-stu-id="25be0-115">serverPath</span></span>](kasclient.kasattachment.md#serverpath)
* [<span data-ttu-id="25be0-116">size</span><span class="sxs-lookup"><span data-stu-id="25be0-116">size</span></span>](kasclient.kasattachment.md#size)
* [<span data-ttu-id="25be0-117">thumbnail</span><span class="sxs-lookup"><span data-stu-id="25be0-117">thumbnail</span></span>](kasclient.kasattachment.md#thumbnail)
* [<span data-ttu-id="25be0-118">type</span><span class="sxs-lookup"><span data-stu-id="25be0-118">type</span></span>](kasclient.kasattachment.md#type)
### <a name="methods"></a><span data-ttu-id="25be0-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="25be0-119">Methods</span></span>

* [<span data-ttu-id="25be0-120">toJSON</span><span class="sxs-lookup"><span data-stu-id="25be0-120">toJSON</span></span>](kasclient.kasattachment.md#tojson)
* [<span data-ttu-id="25be0-121">fromJSON</span><span class="sxs-lookup"><span data-stu-id="25be0-121">fromJSON</span></span>](kasclient.kasattachment.md#fromjson)
* [<span data-ttu-id="25be0-122">hasLocalPath</span><span class="sxs-lookup"><span data-stu-id="25be0-122">hasLocalPath</span></span>](kasclient.kasattachment.md#haslocalpath)
* [<span data-ttu-id="25be0-123">hasServerPath</span><span class="sxs-lookup"><span data-stu-id="25be0-123">hasServerPath</span></span>](kasclient.kasattachment.md#hasserverpath)
* [<span data-ttu-id="25be0-124">populateModelFromJSON</span><span class="sxs-lookup"><span data-stu-id="25be0-124">populateModelFromJSON</span></span>](kasclient.kasattachment.md#populatemodelfromjson)

---

## <a name="properties"></a><span data-ttu-id="25be0-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25be0-125">Properties</span></span>

<a id="attachmentid"></a>

###  <a name="attachmentid"></a><span data-ttu-id="25be0-126">attachmentId</span><span class="sxs-lookup"><span data-stu-id="25be0-126">attachmentId</span></span>

<span data-ttu-id="25be0-127">**● AttachmentId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="25be0-127">**● attachmentId**: *`string`* = ""</span></span>

___

<a id="filename"></a>

###  <a name="filename"></a><span data-ttu-id="25be0-128">fileName</span><span class="sxs-lookup"><span data-stu-id="25be0-128">fileName</span></span>

<span data-ttu-id="25be0-129">**● FileName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="25be0-129">**● fileName**: *`string`* = ""</span></span>

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a><span data-ttu-id="25be0-130">hasSetThumbnail</span><span class="sxs-lookup"><span data-stu-id="25be0-130">hasSetThumbnail</span></span>

<span data-ttu-id="25be0-131">**● HasSetThumbnail**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="25be0-131">**● hasSetThumbnail**: *`boolean`* = false</span></span>

___

<a id="localpath"></a>

###  <a name="localpath"></a><span data-ttu-id="25be0-132">localPath</span><span class="sxs-lookup"><span data-stu-id="25be0-132">localPath</span></span>

<span data-ttu-id="25be0-133">**● LocalPath**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="25be0-133">**● localPath**: *`string`* = ""</span></span>

___

<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a><span data-ttu-id="25be0-134">requireHighResThumbnail</span><span class="sxs-lookup"><span data-stu-id="25be0-134">requireHighResThumbnail</span></span>

<span data-ttu-id="25be0-135">**● RequireHighResThumbnail**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="25be0-135">**● requireHighResThumbnail**: *`boolean`* = false</span></span>

___

<a id="serverpath"></a>

###  <a name="serverpath"></a><span data-ttu-id="25be0-136">serverPath</span><span class="sxs-lookup"><span data-stu-id="25be0-136">serverPath</span></span>

<span data-ttu-id="25be0-137">**● ServerPath**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="25be0-137">**● serverPath**: *`string`* = ""</span></span>

___

<a id="size"></a>

###  <a name="size"></a><span data-ttu-id="25be0-138">size</span><span class="sxs-lookup"><span data-stu-id="25be0-138">size</span></span>

<span data-ttu-id="25be0-139">**● Größe**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="25be0-139">**● size**: *`number`* = 0</span></span>

___

<a id="thumbnail"></a>

###  <a name="thumbnail"></a><span data-ttu-id="25be0-140">Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="25be0-140">thumbnail</span></span>

<span data-ttu-id="25be0-141">**● Miniaturansicht**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="25be0-141">**● thumbnail**: *`string`* = ""</span></span>

___

<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="25be0-142">type</span><span class="sxs-lookup"><span data-stu-id="25be0-142">type</span></span>

<span data-ttu-id="25be0-143">**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType.Image</span><span class="sxs-lookup"><span data-stu-id="25be0-143">**● type**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* =  KASAttachmentType.Image</span></span>

___

## <a name="methods"></a><span data-ttu-id="25be0-144">Methoden</span><span class="sxs-lookup"><span data-stu-id="25be0-144">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="25be0-145">toJSON</span><span class="sxs-lookup"><span data-stu-id="25be0-145">toJSON</span></span>

<span data-ttu-id="25be0-146">▸ **ToJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="25be0-146">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="25be0-147">Die folgenden Zeichenfolgenschlüssel ("Ty", "Afn", "Asb" usw.) MUSS mit der Attachment-Objektmodell Darstellung in iOS und Android Code synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="25be0-147">The following string keys("ty", "afn", "asb", etc.) MUST be in sync with the Attachment object model representation in iOS and Android code.</span></span> <span data-ttu-id="25be0-148">Dies ist für die ordnungsgemäße Serialisierung und Deserialisierung wichtiger über die KAS-Brücke.</span><span class="sxs-lookup"><span data-stu-id="25be0-148">This is vital for proper serialization and deserialization over the KAS bridge.</span></span>

<span data-ttu-id="25be0-149">**Gibt:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="25be0-149">**Returns:** `JSON`</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="25be0-150">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="25be0-150">`<Static>` fromJSON</span></span>

<span data-ttu-id="25be0-151">▸ **FromJSON**(Objekt: *`any`*): [KASAttachment](kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="25be0-151">▸ **fromJSON**(object: *`any`*): [KASAttachment](kasclient.kasattachment.md)</span></span>

<span data-ttu-id="25be0-152">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="25be0-152">**Parameters:**</span></span>

| <span data-ttu-id="25be0-153">Name</span><span class="sxs-lookup"><span data-stu-id="25be0-153">Name</span></span> | <span data-ttu-id="25be0-154">Typ</span><span class="sxs-lookup"><span data-stu-id="25be0-154">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="25be0-155">object</span><span class="sxs-lookup"><span data-stu-id="25be0-155">object</span></span> | `any` |

<span data-ttu-id="25be0-156">**Gibt:** [KASAttachment](kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="25be0-156">**Returns:** [KASAttachment](kasclient.kasattachment.md)</span></span>

___

<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a><span data-ttu-id="25be0-157">`<Static>`hasLocalPath</span><span class="sxs-lookup"><span data-stu-id="25be0-157">`<Static>` hasLocalPath</span></span>

<span data-ttu-id="25be0-158">▸ **HasLocalPath**(Obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`</span><span class="sxs-lookup"><span data-stu-id="25be0-158">▸ **hasLocalPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*): `boolean`</span></span>

<span data-ttu-id="25be0-159">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="25be0-159">**Parameters:**</span></span>

| <span data-ttu-id="25be0-160">Name</span><span class="sxs-lookup"><span data-stu-id="25be0-160">Name</span></span> | <span data-ttu-id="25be0-161">Typ</span><span class="sxs-lookup"><span data-stu-id="25be0-161">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="25be0-162">obj</span><span class="sxs-lookup"><span data-stu-id="25be0-162">obj</span></span> | [<span data-ttu-id="25be0-163">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="25be0-163">KASAttachment</span></span>](kasclient.kasattachment.md) |

<span data-ttu-id="25be0-164">**Gibt:**`boolean`</span><span class="sxs-lookup"><span data-stu-id="25be0-164">**Returns:** `boolean`</span></span>

___

<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a><span data-ttu-id="25be0-165">`<Static>`hasServerPath</span><span class="sxs-lookup"><span data-stu-id="25be0-165">`<Static>` hasServerPath</span></span>

<span data-ttu-id="25be0-166">▸ **HasServerPath**(Obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`</span><span class="sxs-lookup"><span data-stu-id="25be0-166">▸ **hasServerPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*): `boolean`</span></span>

<span data-ttu-id="25be0-167">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="25be0-167">**Parameters:**</span></span>

| <span data-ttu-id="25be0-168">Name</span><span class="sxs-lookup"><span data-stu-id="25be0-168">Name</span></span> | <span data-ttu-id="25be0-169">Typ</span><span class="sxs-lookup"><span data-stu-id="25be0-169">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="25be0-170">obj</span><span class="sxs-lookup"><span data-stu-id="25be0-170">obj</span></span> | [<span data-ttu-id="25be0-171">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="25be0-171">KASAttachment</span></span>](kasclient.kasattachment.md) |

<span data-ttu-id="25be0-172">**Gibt:**`boolean`</span><span class="sxs-lookup"><span data-stu-id="25be0-172">**Returns:** `boolean`</span></span>

___

<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a><span data-ttu-id="25be0-173">`<Static>`populateModelFromJSON</span><span class="sxs-lookup"><span data-stu-id="25be0-173">`<Static>` populateModelFromJSON</span></span>

<span data-ttu-id="25be0-174">▸ **PopulateModelFromJSON**(Anlage: *[KASAttachment](kasclient.kasattachment.md)*, Object: *`JSON`*):`void`</span><span class="sxs-lookup"><span data-stu-id="25be0-174">▸ **populateModelFromJSON**(attachment: *[KASAttachment](kasclient.kasattachment.md)*, object: *`JSON`*): `void`</span></span>

<span data-ttu-id="25be0-175">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="25be0-175">**Parameters:**</span></span>

| <span data-ttu-id="25be0-176">Name</span><span class="sxs-lookup"><span data-stu-id="25be0-176">Name</span></span> | <span data-ttu-id="25be0-177">Typ</span><span class="sxs-lookup"><span data-stu-id="25be0-177">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="25be0-178">Anlage</span><span class="sxs-lookup"><span data-stu-id="25be0-178">attachment</span></span> | [<span data-ttu-id="25be0-179">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="25be0-179">KASAttachment</span></span>](kasclient.kasattachment.md) |
| <span data-ttu-id="25be0-180">object</span><span class="sxs-lookup"><span data-stu-id="25be0-180">object</span></span> | `JSON` |

<span data-ttu-id="25be0-181">**Gibt:**`void`</span><span class="sxs-lookup"><span data-stu-id="25be0-181">**Returns:** `void`</span></span>

___

