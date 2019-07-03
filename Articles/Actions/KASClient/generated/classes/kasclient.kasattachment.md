<span data-ttu-id="ee02e-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="ee02e-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)</span></span>

# <a name="class-kasattachment"></a><span data-ttu-id="ee02e-102">Klasse: KASAttachment</span><span class="sxs-lookup"><span data-stu-id="ee02e-102">Class: KASAttachment</span></span>

## <a name="hierarchy"></a><span data-ttu-id="ee02e-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="ee02e-103">Hierarchy</span></span>

<span data-ttu-id="ee02e-104">**KASAttachment**</span><span class="sxs-lookup"><span data-stu-id="ee02e-104">**KASAttachment**</span></span>

<span data-ttu-id="ee02e-105">↳ [KASAudioAttachment](kasclient.kasaudioattachment.md)</span><span class="sxs-lookup"><span data-stu-id="ee02e-105">↳  [KASAudioAttachment](kasclient.kasaudioattachment.md)</span></span>

<span data-ttu-id="ee02e-106">↳ [KASImageAttachment](kasclient.kasimageattachment.md)</span><span class="sxs-lookup"><span data-stu-id="ee02e-106">↳  [KASImageAttachment](kasclient.kasimageattachment.md)</span></span>

<span data-ttu-id="ee02e-107">↳ [KASVideoAttachment](kasclient.kasvideoattachment.md)</span><span class="sxs-lookup"><span data-stu-id="ee02e-107">↳  [KASVideoAttachment](kasclient.kasvideoattachment.md)</span></span>

## <a name="index"></a><span data-ttu-id="ee02e-108">Index </span><span class="sxs-lookup"><span data-stu-id="ee02e-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="ee02e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee02e-109">Properties</span></span>

* [<span data-ttu-id="ee02e-110">attachmentId</span><span class="sxs-lookup"><span data-stu-id="ee02e-110">attachmentId</span></span>](kasclient.kasattachment.md#attachmentid)
* [<span data-ttu-id="ee02e-111">fileName</span><span class="sxs-lookup"><span data-stu-id="ee02e-111">fileName</span></span>](kasclient.kasattachment.md#filename)
* [<span data-ttu-id="ee02e-112">hasSetThumbnail</span><span class="sxs-lookup"><span data-stu-id="ee02e-112">hasSetThumbnail</span></span>](kasclient.kasattachment.md#hassetthumbnail)
* [<span data-ttu-id="ee02e-113">LocalPath</span><span class="sxs-lookup"><span data-stu-id="ee02e-113">localPath</span></span>](kasclient.kasattachment.md#localpath)
* [<span data-ttu-id="ee02e-114">requireHighResThumbnail</span><span class="sxs-lookup"><span data-stu-id="ee02e-114">requireHighResThumbnail</span></span>](kasclient.kasattachment.md#requirehighresthumbnail)
* [<span data-ttu-id="ee02e-115">Direktive ServerPath existiert</span><span class="sxs-lookup"><span data-stu-id="ee02e-115">serverPath</span></span>](kasclient.kasattachment.md#serverpath)
* [<span data-ttu-id="ee02e-116">size</span><span class="sxs-lookup"><span data-stu-id="ee02e-116">size</span></span>](kasclient.kasattachment.md#size)
* [<span data-ttu-id="ee02e-117">thumbnail</span><span class="sxs-lookup"><span data-stu-id="ee02e-117">thumbnail</span></span>](kasclient.kasattachment.md#thumbnail)
* [<span data-ttu-id="ee02e-118">type</span><span class="sxs-lookup"><span data-stu-id="ee02e-118">type</span></span>](kasclient.kasattachment.md#type)
### <a name="methods"></a><span data-ttu-id="ee02e-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee02e-119">Methods</span></span>

* [<span data-ttu-id="ee02e-120">toJSON</span><span class="sxs-lookup"><span data-stu-id="ee02e-120">toJSON</span></span>](kasclient.kasattachment.md#tojson)
* [<span data-ttu-id="ee02e-121">fromJSON</span><span class="sxs-lookup"><span data-stu-id="ee02e-121">fromJSON</span></span>](kasclient.kasattachment.md#fromjson)
* [<span data-ttu-id="ee02e-122">hasLocalPath</span><span class="sxs-lookup"><span data-stu-id="ee02e-122">hasLocalPath</span></span>](kasclient.kasattachment.md#haslocalpath)
* [<span data-ttu-id="ee02e-123">hasServerPath</span><span class="sxs-lookup"><span data-stu-id="ee02e-123">hasServerPath</span></span>](kasclient.kasattachment.md#hasserverpath)
* [<span data-ttu-id="ee02e-124">populateModelFromJSON</span><span class="sxs-lookup"><span data-stu-id="ee02e-124">populateModelFromJSON</span></span>](kasclient.kasattachment.md#populatemodelfromjson)

---

## <a name="properties"></a><span data-ttu-id="ee02e-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee02e-125">Properties</span></span>

<a id="attachmentid"></a>

###  <a name="attachmentid"></a><span data-ttu-id="ee02e-126">attachmentId</span><span class="sxs-lookup"><span data-stu-id="ee02e-126">attachmentId</span></span>

<span data-ttu-id="ee02e-127">**● Attachment**-Nr *`string`* : = ""</span><span class="sxs-lookup"><span data-stu-id="ee02e-127">**● attachmentId**: *`string`* = ""</span></span>

___
<a id="filename"></a>

###  <a name="filename"></a><span data-ttu-id="ee02e-128">fileName</span><span class="sxs-lookup"><span data-stu-id="ee02e-128">fileName</span></span>

<span data-ttu-id="ee02e-129">**● filename**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="ee02e-129">**● fileName**: *`string`* = ""</span></span>

___
<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a><span data-ttu-id="ee02e-130">hasSetThumbnail</span><span class="sxs-lookup"><span data-stu-id="ee02e-130">hasSetThumbnail</span></span>

<span data-ttu-id="ee02e-131">**● hasSetThumbnail**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="ee02e-131">**● hasSetThumbnail**: *`boolean`* = false</span></span>

___
<a id="localpath"></a>

###  <a name="localpath"></a><span data-ttu-id="ee02e-132">LocalPath</span><span class="sxs-lookup"><span data-stu-id="ee02e-132">localPath</span></span>

<span data-ttu-id="ee02e-133">**● LocalPath**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="ee02e-133">**● localPath**: *`string`* = ""</span></span>

___
<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a><span data-ttu-id="ee02e-134">requireHighResThumbnail</span><span class="sxs-lookup"><span data-stu-id="ee02e-134">requireHighResThumbnail</span></span>

<span data-ttu-id="ee02e-135">**● requireHighResThumbnail**: *`boolean`* = false</span><span class="sxs-lookup"><span data-stu-id="ee02e-135">**● requireHighResThumbnail**: *`boolean`* = false</span></span>

___
<a id="serverpath"></a>

###  <a name="serverpath"></a><span data-ttu-id="ee02e-136">Direktive ServerPath existiert</span><span class="sxs-lookup"><span data-stu-id="ee02e-136">serverPath</span></span>

<span data-ttu-id="ee02e-137">**● Direktive ServerPath existiert**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="ee02e-137">**● serverPath**: *`string`* = ""</span></span>

___
<a id="size"></a>

###  <a name="size"></a><span data-ttu-id="ee02e-138">size</span><span class="sxs-lookup"><span data-stu-id="ee02e-138">size</span></span>

<span data-ttu-id="ee02e-139">**● Größe**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="ee02e-139">**● size**: *`number`* = 0</span></span>

___
<a id="thumbnail"></a>

###  <a name="thumbnail"></a><span data-ttu-id="ee02e-140">Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="ee02e-140">thumbnail</span></span>

<span data-ttu-id="ee02e-141">**● Thumbnail**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="ee02e-141">**● thumbnail**: *`string`* = ""</span></span>

___
<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="ee02e-142">type</span><span class="sxs-lookup"><span data-stu-id="ee02e-142">type</span></span>

<span data-ttu-id="ee02e-143">**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType. Image</span><span class="sxs-lookup"><span data-stu-id="ee02e-143">**● type**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* =  KASAttachmentType.Image</span></span>

___

## <a name="methods"></a><span data-ttu-id="ee02e-144">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee02e-144">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="ee02e-145">toJSON</span><span class="sxs-lookup"><span data-stu-id="ee02e-145">toJSON</span></span>

<span data-ttu-id="ee02e-146">▸ **tojson**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="ee02e-146">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="ee02e-147">Die folgenden Zeichenfolgenschlüssel ("Ty", "AFN", "ASB" usw.) Muss mit der Darstellung des Attachment-Objektmodells in IOS-und Android-Code synchronisiert sein.</span><span class="sxs-lookup"><span data-stu-id="ee02e-147">The following string keys("ty", "afn", "asb", etc.) MUST be in sync with the Attachment object model representation in iOS and Android code.</span></span> <span data-ttu-id="ee02e-148">Dies ist für die ordnungsgemäße Serialisierung und Deserialisierung über die Kas-Brücke unerlässlich.</span><span class="sxs-lookup"><span data-stu-id="ee02e-148">This is vital for proper serialization and deserialization over the KAS bridge.</span></span>

<span data-ttu-id="ee02e-149">**Gibt Folgendes zurück:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="ee02e-149">**Returns:** `JSON`</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="ee02e-150">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="ee02e-150">`<Static>` fromJSON</span></span>

<span data-ttu-id="ee02e-151">▸- **fromJSON**(Objekt *`any`*:): [KASAttachment](kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="ee02e-151">▸ **fromJSON**(object: *`any`*): [KASAttachment](kasclient.kasattachment.md)</span></span>

<span data-ttu-id="ee02e-152">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="ee02e-152">**Parameters:**</span></span>

| <span data-ttu-id="ee02e-153">Name</span><span class="sxs-lookup"><span data-stu-id="ee02e-153">Name</span></span> | <span data-ttu-id="ee02e-154">Typ</span><span class="sxs-lookup"><span data-stu-id="ee02e-154">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="ee02e-155">Objekt</span><span class="sxs-lookup"><span data-stu-id="ee02e-155">object</span></span> | `any` |

<span data-ttu-id="ee02e-156">**Gibt Folgendes zurück:** [KASAttachment](kasclient.kasattachment.md)</span><span class="sxs-lookup"><span data-stu-id="ee02e-156">**Returns:** [KASAttachment](kasclient.kasattachment.md)</span></span>

___
<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a><span data-ttu-id="ee02e-157">`<Static>`hasLocalPath</span><span class="sxs-lookup"><span data-stu-id="ee02e-157">`<Static>` hasLocalPath</span></span>

<span data-ttu-id="ee02e-158">▸ **hasLocalPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`</span><span class="sxs-lookup"><span data-stu-id="ee02e-158">▸ **hasLocalPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*): `boolean`</span></span>

<span data-ttu-id="ee02e-159">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="ee02e-159">**Parameters:**</span></span>

| <span data-ttu-id="ee02e-160">Name</span><span class="sxs-lookup"><span data-stu-id="ee02e-160">Name</span></span> | <span data-ttu-id="ee02e-161">Typ</span><span class="sxs-lookup"><span data-stu-id="ee02e-161">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="ee02e-162">obj</span><span class="sxs-lookup"><span data-stu-id="ee02e-162">obj</span></span> | [<span data-ttu-id="ee02e-163">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="ee02e-163">KASAttachment</span></span>](kasclient.kasattachment.md) |

<span data-ttu-id="ee02e-164">**Gibt Folgendes zurück:**`boolean`</span><span class="sxs-lookup"><span data-stu-id="ee02e-164">**Returns:** `boolean`</span></span>

___
<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a><span data-ttu-id="ee02e-165">`<Static>`hasServerPath</span><span class="sxs-lookup"><span data-stu-id="ee02e-165">`<Static>` hasServerPath</span></span>

<span data-ttu-id="ee02e-166">▸ **hasServerPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`</span><span class="sxs-lookup"><span data-stu-id="ee02e-166">▸ **hasServerPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*): `boolean`</span></span>

<span data-ttu-id="ee02e-167">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="ee02e-167">**Parameters:**</span></span>

| <span data-ttu-id="ee02e-168">Name</span><span class="sxs-lookup"><span data-stu-id="ee02e-168">Name</span></span> | <span data-ttu-id="ee02e-169">Typ</span><span class="sxs-lookup"><span data-stu-id="ee02e-169">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="ee02e-170">obj</span><span class="sxs-lookup"><span data-stu-id="ee02e-170">obj</span></span> | [<span data-ttu-id="ee02e-171">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="ee02e-171">KASAttachment</span></span>](kasclient.kasattachment.md) |

<span data-ttu-id="ee02e-172">**Gibt Folgendes zurück:**`boolean`</span><span class="sxs-lookup"><span data-stu-id="ee02e-172">**Returns:** `boolean`</span></span>

___
<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a><span data-ttu-id="ee02e-173">`<Static>`populateModelFromJSON</span><span class="sxs-lookup"><span data-stu-id="ee02e-173">`<Static>` populateModelFromJSON</span></span>

<span data-ttu-id="ee02e-174">▸ **populateModelFromJSON**(Attachment: *[KASAttachment](kasclient.kasattachment.md)*, Object: *`JSON`*):`void`</span><span class="sxs-lookup"><span data-stu-id="ee02e-174">▸ **populateModelFromJSON**(attachment: *[KASAttachment](kasclient.kasattachment.md)*, object: *`JSON`*): `void`</span></span>

<span data-ttu-id="ee02e-175">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="ee02e-175">**Parameters:**</span></span>

| <span data-ttu-id="ee02e-176">Name</span><span class="sxs-lookup"><span data-stu-id="ee02e-176">Name</span></span> | <span data-ttu-id="ee02e-177">Typ</span><span class="sxs-lookup"><span data-stu-id="ee02e-177">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="ee02e-178">attachment</span><span class="sxs-lookup"><span data-stu-id="ee02e-178">attachment</span></span> | [<span data-ttu-id="ee02e-179">KASAttachment</span><span class="sxs-lookup"><span data-stu-id="ee02e-179">KASAttachment</span></span>](kasclient.kasattachment.md) |
| <span data-ttu-id="ee02e-180">Objekt</span><span class="sxs-lookup"><span data-stu-id="ee02e-180">object</span></span> | `JSON` |

<span data-ttu-id="ee02e-181">**Gibt Folgendes zurück:**`void`</span><span class="sxs-lookup"><span data-stu-id="ee02e-181">**Returns:** `void`</span></span>

___

