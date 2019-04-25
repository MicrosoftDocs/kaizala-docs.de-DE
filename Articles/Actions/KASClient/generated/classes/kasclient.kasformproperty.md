<span data-ttu-id="24736-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProperty](../classes/kasclient.kasformproperty.md)</span><span class="sxs-lookup"><span data-stu-id="24736-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProperty](../classes/kasclient.kasformproperty.md)</span></span>

# <a name="class-kasformproperty"></a><span data-ttu-id="24736-102">Klasse: KASFormProperty</span><span class="sxs-lookup"><span data-stu-id="24736-102">Class: KASFormProperty</span></span>

## <a name="hierarchy"></a><span data-ttu-id="24736-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="24736-103">Hierarchy</span></span>

<span data-ttu-id="24736-104">**KASFormProperty**</span><span class="sxs-lookup"><span data-stu-id="24736-104">**KASFormProperty**</span></span>

## <a name="index"></a><span data-ttu-id="24736-105">Index </span><span class="sxs-lookup"><span data-stu-id="24736-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="24736-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24736-106">Properties</span></span>

* [<span data-ttu-id="24736-107">name</span><span class="sxs-lookup"><span data-stu-id="24736-107">name</span></span>](kasclient.kasformproperty.md#name)
* [<span data-ttu-id="24736-108">type</span><span class="sxs-lookup"><span data-stu-id="24736-108">type</span></span>](kasclient.kasformproperty.md#type)
* [<span data-ttu-id="24736-109">value</span><span class="sxs-lookup"><span data-stu-id="24736-109">value</span></span>](kasclient.kasformproperty.md#value)
### <a name="methods"></a><span data-ttu-id="24736-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="24736-110">Methods</span></span>

* [<span data-ttu-id="24736-111">getAPICompatiblePropertyType</span><span class="sxs-lookup"><span data-stu-id="24736-111">getAPICompatiblePropertyType</span></span>](kasclient.kasformproperty.md#getapicompatiblepropertytype)
* [<span data-ttu-id="24736-112">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="24736-112">toAPICompatibleJSON</span></span>](kasclient.kasformproperty.md#toapicompatiblejson)
* [<span data-ttu-id="24736-113">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="24736-113">toClientJSON</span></span>](kasclient.kasformproperty.md#toclientjson)
* [<span data-ttu-id="24736-114">toJSON</span><span class="sxs-lookup"><span data-stu-id="24736-114">toJSON</span></span>](kasclient.kasformproperty.md#tojson)
* [<span data-ttu-id="24736-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="24736-115">fromJSON</span></span>](kasclient.kasformproperty.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="24736-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24736-116">Properties</span></span>

<a id="name"></a>

###  <a name="name"></a><span data-ttu-id="24736-117">name</span><span class="sxs-lookup"><span data-stu-id="24736-117">name</span></span>

<span data-ttu-id="24736-118">**● Name**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="24736-118">**● name**: *`string`* = ""</span></span>

<span data-ttu-id="24736-119">Name der Metadaten</span><span class="sxs-lookup"><span data-stu-id="24736-119">Name of the metadata</span></span>

___

<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="24736-120">Typ</span><span class="sxs-lookup"><span data-stu-id="24736-120">type</span></span>

<span data-ttu-id="24736-121">**● Typ**: *[KASFormPropertyType](../enums/kasclient.kasformpropertytype.md)* = KASFormPropertyType. Text</span><span class="sxs-lookup"><span data-stu-id="24736-121">**● type**: *[KASFormPropertyType](../enums/kasclient.kasformpropertytype.md)* =  KASFormPropertyType.Text</span></span>

<span data-ttu-id="24736-122">Typ der Metadaten</span><span class="sxs-lookup"><span data-stu-id="24736-122">Type of the metadata</span></span>

___

<a id="value"></a>

###  <a name="value"></a><span data-ttu-id="24736-123">Wert</span><span class="sxs-lookup"><span data-stu-id="24736-123">value</span></span>

<span data-ttu-id="24736-124">**● Wert**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="24736-124">**● value**: *`string`* = ""</span></span>

<span data-ttu-id="24736-125">Wert der Metadaten</span><span class="sxs-lookup"><span data-stu-id="24736-125">Value of the metadata</span></span>

___

## <a name="methods"></a><span data-ttu-id="24736-126">Methoden</span><span class="sxs-lookup"><span data-stu-id="24736-126">Methods</span></span>

<a id="getapicompatiblepropertytype"></a>

###  <a name="getapicompatiblepropertytype"></a><span data-ttu-id="24736-127">getAPICompatiblePropertyType</span><span class="sxs-lookup"><span data-stu-id="24736-127">getAPICompatiblePropertyType</span></span>

<span data-ttu-id="24736-128">▸ **getAPICompatiblePropertyType**(Typ: *`string`*):`string`</span><span class="sxs-lookup"><span data-stu-id="24736-128">▸ **getAPICompatiblePropertyType**(type: *`string`*): `string`</span></span>

<span data-ttu-id="24736-129">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="24736-129">**Parameters:**</span></span>

| <span data-ttu-id="24736-130">Name</span><span class="sxs-lookup"><span data-stu-id="24736-130">Name</span></span> | <span data-ttu-id="24736-131">Typ</span><span class="sxs-lookup"><span data-stu-id="24736-131">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="24736-132">Typ</span><span class="sxs-lookup"><span data-stu-id="24736-132">type</span></span> | `string` |

<span data-ttu-id="24736-133">**Gibt Folgendes zurück:**`string`</span><span class="sxs-lookup"><span data-stu-id="24736-133">**Returns:** `string`</span></span>

___

<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a><span data-ttu-id="24736-134">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="24736-134">toAPICompatibleJSON</span></span>

<span data-ttu-id="24736-135">▸ **toAPICompatibleJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="24736-135">▸ **toAPICompatibleJSON**(): `JSON`</span></span>

<span data-ttu-id="24736-136">**Gibt Folgendes zurück:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="24736-136">**Returns:** `JSON`</span></span>

___

<a id="toclientjson"></a>

###  <a name="toclientjson"></a><span data-ttu-id="24736-137">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="24736-137">toClientJSON</span></span>

<span data-ttu-id="24736-138">▸ **toClientJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="24736-138">▸ **toClientJSON**(): `JSON`</span></span>

<span data-ttu-id="24736-139">**Gibt Folgendes zurück:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="24736-139">**Returns:** `JSON`</span></span>

___

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="24736-140">toJSON</span><span class="sxs-lookup"><span data-stu-id="24736-140">toJSON</span></span>

<span data-ttu-id="24736-141">▸ **tojson**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="24736-141">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="24736-142">**Gibt Folgendes zurück:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="24736-142">**Returns:** `JSON`</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="24736-143">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="24736-143">`<Static>` fromJSON</span></span>

<span data-ttu-id="24736-144">▸ **fromJSON**(Object: *`JSON`*): [KASFormProperty](kasclient.kasformproperty.md)</span><span class="sxs-lookup"><span data-stu-id="24736-144">▸ **fromJSON**(object: *`JSON`*): [KASFormProperty](kasclient.kasformproperty.md)</span></span>

<span data-ttu-id="24736-145">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="24736-145">**Parameters:**</span></span>

| <span data-ttu-id="24736-146">Name</span><span class="sxs-lookup"><span data-stu-id="24736-146">Name</span></span> | <span data-ttu-id="24736-147">Typ</span><span class="sxs-lookup"><span data-stu-id="24736-147">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="24736-148">Objekt</span><span class="sxs-lookup"><span data-stu-id="24736-148">object</span></span> | `JSON` |

<span data-ttu-id="24736-149">**Gibt Folgendes zurück:** [KASFormProperty](kasclient.kasformproperty.md)</span><span class="sxs-lookup"><span data-stu-id="24736-149">**Returns:** [KASFormProperty](kasclient.kasformproperty.md)</span></span>

___

