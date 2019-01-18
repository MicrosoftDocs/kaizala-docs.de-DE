---
ms.openlocfilehash: 01bf00e0a8aeca6f09a8243b297470606736d7ab
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728114"
---
<span data-ttu-id="95a39-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormPropertyUpdateFactory](../classes/kasclient.kasformpropertyupdatefactory.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormPropertyUpdateFactory](../classes/kasclient.kasformpropertyupdatefactory.md)</span></span>

# <a name="class-kasformpropertyupdatefactory"></a><span data-ttu-id="95a39-102">Klasse: KASFormPropertyUpdateFactory</span><span class="sxs-lookup"><span data-stu-id="95a39-102">Class: KASFormPropertyUpdateFactory</span></span>

## <a name="hierarchy"></a><span data-ttu-id="95a39-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="95a39-103">Hierarchy</span></span>

<span data-ttu-id="95a39-104">**KASFormPropertyUpdateFactory**</span><span class="sxs-lookup"><span data-stu-id="95a39-104">**KASFormPropertyUpdateFactory**</span></span>

## <a name="index"></a><span data-ttu-id="95a39-105">Index </span><span class="sxs-lookup"><span data-stu-id="95a39-105">Index</span></span>

### <a name="methods"></a><span data-ttu-id="95a39-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="95a39-106">Methods</span></span>

* [<span data-ttu-id="95a39-107">addEntriesInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="95a39-107">addEntriesInPropertyValue</span></span>](kasclient.kasformpropertyupdatefactory.md#addentriesinpropertyvalue)
* [<span data-ttu-id="95a39-108">addProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-108">addProperty</span></span>](kasclient.kasformpropertyupdatefactory.md#addproperty)
* [<span data-ttu-id="95a39-109">deleteEntriesFromPropertyValue</span><span class="sxs-lookup"><span data-stu-id="95a39-109">deleteEntriesFromPropertyValue</span></span>](kasclient.kasformpropertyupdatefactory.md#deleteentriesfrompropertyvalue)
* [<span data-ttu-id="95a39-110">deleteProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-110">deleteProperty</span></span>](kasclient.kasformpropertyupdatefactory.md#deleteproperty)
* [<span data-ttu-id="95a39-111">replaceEntryInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="95a39-111">replaceEntryInPropertyValue</span></span>](kasclient.kasformpropertyupdatefactory.md#replaceentryinpropertyvalue)
* [<span data-ttu-id="95a39-112">updateValueInProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-112">updateValueInProperty</span></span>](kasclient.kasformpropertyupdatefactory.md#updatevalueinproperty)

---

## <a name="methods"></a><span data-ttu-id="95a39-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="95a39-113">Methods</span></span>

<a id="addentriesinpropertyvalue"></a>

### <a name="static-addentriesinpropertyvalue"></a><span data-ttu-id="95a39-114">`<Static>`addEntriesInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="95a39-114">`<Static>` addEntriesInPropertyValue</span></span>

<span data-ttu-id="95a39-115">▸ **AddEntriesInPropertyValue**(Einträge: \* `string`[]\*, Eigenschaft: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-115">▸ **addEntriesInPropertyValue**(entries: *`string`[]*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="95a39-116">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="95a39-116">**Parameters:**</span></span>

| <span data-ttu-id="95a39-117">Name</span><span class="sxs-lookup"><span data-stu-id="95a39-117">Name</span></span> | <span data-ttu-id="95a39-118">Typ</span><span class="sxs-lookup"><span data-stu-id="95a39-118">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="95a39-119">Einträge</span><span class="sxs-lookup"><span data-stu-id="95a39-119">entries</span></span> | <span data-ttu-id="95a39-120">`string`[]</span><span class="sxs-lookup"><span data-stu-id="95a39-120"></span></span> |
| <span data-ttu-id="95a39-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95a39-121">property</span></span> | [<span data-ttu-id="95a39-122">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-122">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="95a39-123">**Gibt:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-123">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="addproperty"></a>

### <a name="static-addproperty"></a><span data-ttu-id="95a39-124">`<Static>`addProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-124">`<Static>` addProperty</span></span>

<span data-ttu-id="95a39-125">▸ **AddProperty**(Eigenschaft: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-125">▸ **addProperty**(property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="95a39-126">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="95a39-126">**Parameters:**</span></span>

| <span data-ttu-id="95a39-127">Name</span><span class="sxs-lookup"><span data-stu-id="95a39-127">Name</span></span> | <span data-ttu-id="95a39-128">Typ</span><span class="sxs-lookup"><span data-stu-id="95a39-128">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="95a39-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95a39-129">property</span></span> | [<span data-ttu-id="95a39-130">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-130">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="95a39-131">**Gibt:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-131">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="deleteentriesfrompropertyvalue"></a>

### <a name="static-deleteentriesfrompropertyvalue"></a><span data-ttu-id="95a39-132">`<Static>`deleteEntriesFromPropertyValue</span><span class="sxs-lookup"><span data-stu-id="95a39-132">`<Static>` deleteEntriesFromPropertyValue</span></span>

<span data-ttu-id="95a39-133">▸ **DeleteEntriesFromPropertyValue**(Einträge: \* `string`[]\*, Eigenschaft: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-133">▸ **deleteEntriesFromPropertyValue**(entries: *`string`[]*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="95a39-134">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="95a39-134">**Parameters:**</span></span>

| <span data-ttu-id="95a39-135">Name</span><span class="sxs-lookup"><span data-stu-id="95a39-135">Name</span></span> | <span data-ttu-id="95a39-136">Typ</span><span class="sxs-lookup"><span data-stu-id="95a39-136">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="95a39-137">Einträge</span><span class="sxs-lookup"><span data-stu-id="95a39-137">entries</span></span> | <span data-ttu-id="95a39-138">`string`[]</span><span class="sxs-lookup"><span data-stu-id="95a39-138"></span></span> |
| <span data-ttu-id="95a39-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95a39-139">property</span></span> | [<span data-ttu-id="95a39-140">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-140">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="95a39-141">**Gibt:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-141">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="deleteproperty"></a>

### <a name="static-deleteproperty"></a><span data-ttu-id="95a39-142">`<Static>`deleteProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-142">`<Static>` deleteProperty</span></span>

<span data-ttu-id="95a39-143">▸ **DeleteProperty**(Eigenschaft: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-143">▸ **deleteProperty**(property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="95a39-144">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="95a39-144">**Parameters:**</span></span>

| <span data-ttu-id="95a39-145">Name</span><span class="sxs-lookup"><span data-stu-id="95a39-145">Name</span></span> | <span data-ttu-id="95a39-146">Typ</span><span class="sxs-lookup"><span data-stu-id="95a39-146">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="95a39-147">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95a39-147">property</span></span> | [<span data-ttu-id="95a39-148">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-148">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="95a39-149">**Gibt:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-149">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="replaceentryinpropertyvalue"></a>

### <a name="static-replaceentryinpropertyvalue"></a><span data-ttu-id="95a39-150">`<Static>`replaceEntryInPropertyValue</span><span class="sxs-lookup"><span data-stu-id="95a39-150">`<Static>` replaceEntryInPropertyValue</span></span>

<span data-ttu-id="95a39-151">▸ **ReplaceEntryInPropertyValue**(OldEntry: *`string`*, NewEntry: *`string`*, Eigenschaft: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-151">▸ **replaceEntryInPropertyValue**(oldEntry: *`string`*, newEntry: *`string`*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="95a39-152">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="95a39-152">**Parameters:**</span></span>

| <span data-ttu-id="95a39-153">Name</span><span class="sxs-lookup"><span data-stu-id="95a39-153">Name</span></span> | <span data-ttu-id="95a39-154">Typ</span><span class="sxs-lookup"><span data-stu-id="95a39-154">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="95a39-155">oldEntry</span><span class="sxs-lookup"><span data-stu-id="95a39-155">oldEntry</span></span> | `string` |
| <span data-ttu-id="95a39-156">newEntry</span><span class="sxs-lookup"><span data-stu-id="95a39-156">newEntry</span></span> | `string` |
| <span data-ttu-id="95a39-157">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95a39-157">property</span></span> | [<span data-ttu-id="95a39-158">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-158">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="95a39-159">**Gibt:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-159">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

<a id="updatevalueinproperty"></a>

### <a name="static-updatevalueinproperty"></a><span data-ttu-id="95a39-160">`<Static>`updateValueInProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-160">`<Static>` updateValueInProperty</span></span>

<span data-ttu-id="95a39-161">▸ **UpdateValueInProperty**(NewValue: *`string`*, Eigenschaft: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-161">▸ **updateValueInProperty**(newValue: *`string`*, property: *[KASFormProperty](kasclient.kasformproperty.md)*): [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

<span data-ttu-id="95a39-162">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="95a39-162">**Parameters:**</span></span>

| <span data-ttu-id="95a39-163">Name</span><span class="sxs-lookup"><span data-stu-id="95a39-163">Name</span></span> | <span data-ttu-id="95a39-164">Typ</span><span class="sxs-lookup"><span data-stu-id="95a39-164">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="95a39-165">newValue</span><span class="sxs-lookup"><span data-stu-id="95a39-165">newValue</span></span> | `string` |
| <span data-ttu-id="95a39-166">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95a39-166">property</span></span> | [<span data-ttu-id="95a39-167">KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="95a39-167">KASFormProperty</span></span>](kasclient.kasformproperty.md) |

<span data-ttu-id="95a39-168">**Gibt:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span><span class="sxs-lookup"><span data-stu-id="95a39-168">**Returns:** [KASFormPropertyUpdateInfo](kasclient.kasformpropertyupdateinfo.md)</span></span>

___

