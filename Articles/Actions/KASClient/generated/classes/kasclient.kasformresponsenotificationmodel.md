---
ms.openlocfilehash: 94efbe6f80d643bdc930e2c23de6197d8b20d7ad
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728072"
---
<span data-ttu-id="6ec1c-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponseNotificationModel](../classes/kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="6ec1c-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponseNotificationModel](../classes/kasclient.kasformresponsenotificationmodel.md)</span></span>

# <a name="class-kasformresponsenotificationmodel"></a><span data-ttu-id="6ec1c-102">Klasse: KASFormResponseNotificationModel</span><span class="sxs-lookup"><span data-stu-id="6ec1c-102">Class: KASFormResponseNotificationModel</span></span>

## <a name="hierarchy"></a><span data-ttu-id="6ec1c-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="6ec1c-103">Hierarchy</span></span>

<span data-ttu-id="6ec1c-104">**KASFormResponseNotificationModel**</span><span class="sxs-lookup"><span data-stu-id="6ec1c-104">**KASFormResponseNotificationModel**</span></span>

## <a name="index"></a><span data-ttu-id="6ec1c-105">Index </span><span class="sxs-lookup"><span data-stu-id="6ec1c-105">Index</span></span>

### <a name="constructors"></a><span data-ttu-id="6ec1c-106">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="6ec1c-106">Constructors</span></span>

* [<span data-ttu-id="6ec1c-107">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="6ec1c-107">constructor</span></span>](kasclient.kasformresponsenotificationmodel.md#constructor)
### <a name="properties"></a><span data-ttu-id="6ec1c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ec1c-108">Properties</span></span>

* [<span data-ttu-id="6ec1c-109">messagePreview</span><span class="sxs-lookup"><span data-stu-id="6ec1c-109">messagePreview</span></span>](kasclient.kasformresponsenotificationmodel.md#messagepreview)
* [<span data-ttu-id="6ec1c-110">messageTarget</span><span class="sxs-lookup"><span data-stu-id="6ec1c-110">messageTarget</span></span>](kasclient.kasformresponsenotificationmodel.md#messagetarget)
* [<span data-ttu-id="6ec1c-111">pushTarget</span><span class="sxs-lookup"><span data-stu-id="6ec1c-111">pushTarget</span></span>](kasclient.kasformresponsenotificationmodel.md#pushtarget)
### <a name="methods"></a><span data-ttu-id="6ec1c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ec1c-112">Methods</span></span>

* [<span data-ttu-id="6ec1c-113">toJSON</span><span class="sxs-lookup"><span data-stu-id="6ec1c-113">toJSON</span></span>](kasclient.kasformresponsenotificationmodel.md#tojson)
* [<span data-ttu-id="6ec1c-114">fromJson</span><span class="sxs-lookup"><span data-stu-id="6ec1c-114">fromJson</span></span>](kasclient.kasformresponsenotificationmodel.md#fromjson)

---

## <a name="constructors"></a><span data-ttu-id="6ec1c-115">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="6ec1c-115">Constructors</span></span>

<a id="constructor"></a>

###  <a name="constructor"></a><span data-ttu-id="6ec1c-116">constructor</span><span class="sxs-lookup"><span data-stu-id="6ec1c-116">constructor</span></span>

<span data-ttu-id="6ec1c-117">⊕ **neue KASFormResponseNotificationModel**(MessageTarget?: \* [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, PushTarget?: \* [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, MessagePreview?: *`String`*): [ KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="6ec1c-117">⊕ **new KASFormResponseNotificationModel**(messageTarget?: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, pushTarget?: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, messagePreview?: *`String`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

<span data-ttu-id="6ec1c-118">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="6ec1c-118">**Parameters:**</span></span>

| <span data-ttu-id="6ec1c-119">Name</span><span class="sxs-lookup"><span data-stu-id="6ec1c-119">Name</span></span> | <span data-ttu-id="6ec1c-120">Typ</span><span class="sxs-lookup"><span data-stu-id="6ec1c-120">Type</span></span> | <span data-ttu-id="6ec1c-121">Standardwert</span><span class="sxs-lookup"><span data-stu-id="6ec1c-121">Default value</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="6ec1c-122">`Default value`messageTarget</span><span class="sxs-lookup"><span data-stu-id="6ec1c-122">`Default value` messageTarget</span></span> | <span data-ttu-id="6ec1c-123">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) []</span><span class="sxs-lookup"><span data-stu-id="6ec1c-123">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]</span></span> |  <span data-ttu-id="6ec1c-124">null</span><span class="sxs-lookup"><span data-stu-id="6ec1c-124">null</span></span> |
| <span data-ttu-id="6ec1c-125">`Default value`pushTarget</span><span class="sxs-lookup"><span data-stu-id="6ec1c-125">`Default value` pushTarget</span></span> | <span data-ttu-id="6ec1c-126">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) []</span><span class="sxs-lookup"><span data-stu-id="6ec1c-126">[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]</span></span> |  <span data-ttu-id="6ec1c-127">null</span><span class="sxs-lookup"><span data-stu-id="6ec1c-127">null</span></span> |
| <span data-ttu-id="6ec1c-128">`Default value`messagePreview</span><span class="sxs-lookup"><span data-stu-id="6ec1c-128">`Default value` messagePreview</span></span> | `String` |  <span data-ttu-id="6ec1c-129">null</span><span class="sxs-lookup"><span data-stu-id="6ec1c-129">null</span></span> |

<span data-ttu-id="6ec1c-130">**Gibt:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="6ec1c-130">**Returns:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

___

## <a name="properties"></a><span data-ttu-id="6ec1c-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ec1c-131">Properties</span></span>

<a id="messagepreview"></a>

###  <a name="messagepreview"></a><span data-ttu-id="6ec1c-132">messagePreview</span><span class="sxs-lookup"><span data-stu-id="6ec1c-132">messagePreview</span></span>

<span data-ttu-id="6ec1c-133">**● MessagePreview**: *`String`* = ""</span><span class="sxs-lookup"><span data-stu-id="6ec1c-133">**● messagePreview**: *`String`* = ""</span></span>

___

<a id="messagetarget"></a>

###  <a name="messagetarget"></a><span data-ttu-id="6ec1c-134">messageTarget</span><span class="sxs-lookup"><span data-stu-id="6ec1c-134">messageTarget</span></span>

<span data-ttu-id="6ec1c-135">**● MessageTarget**: \* [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)]\*</span><span class="sxs-lookup"><span data-stu-id="6ec1c-135">**● messageTarget**: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*</span></span>

___

<a id="pushtarget"></a>

###  <a name="pushtarget"></a><span data-ttu-id="6ec1c-136">pushTarget</span><span class="sxs-lookup"><span data-stu-id="6ec1c-136">pushTarget</span></span>

<span data-ttu-id="6ec1c-137">**● PushTarget**: \* [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)]\*</span><span class="sxs-lookup"><span data-stu-id="6ec1c-137">**● pushTarget**: *[KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*</span></span>

___

## <a name="methods"></a><span data-ttu-id="6ec1c-138">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ec1c-138">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="6ec1c-139">toJSON</span><span class="sxs-lookup"><span data-stu-id="6ec1c-139">toJSON</span></span>

<span data-ttu-id="6ec1c-140">▸ **ToJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="6ec1c-140">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="6ec1c-141">**Gibt:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="6ec1c-141">**Returns:** `JSON`</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="6ec1c-142">`<Static>`fromJson</span><span class="sxs-lookup"><span data-stu-id="6ec1c-142">`<Static>` fromJson</span></span>

<span data-ttu-id="6ec1c-143">▸ **FromJson**(Objekt: *`JSON`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="6ec1c-143">▸ **fromJson**(object: *`JSON`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

<span data-ttu-id="6ec1c-144">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="6ec1c-144">**Parameters:**</span></span>

| <span data-ttu-id="6ec1c-145">Name</span><span class="sxs-lookup"><span data-stu-id="6ec1c-145">Name</span></span> | <span data-ttu-id="6ec1c-146">Typ</span><span class="sxs-lookup"><span data-stu-id="6ec1c-146">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="6ec1c-147">object</span><span class="sxs-lookup"><span data-stu-id="6ec1c-147">object</span></span> | `JSON` |

<span data-ttu-id="6ec1c-148">**Gibt:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span><span class="sxs-lookup"><span data-stu-id="6ec1c-148">**Returns:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)</span></span>

___

