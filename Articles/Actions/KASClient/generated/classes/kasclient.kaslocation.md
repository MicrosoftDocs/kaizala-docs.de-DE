<span data-ttu-id="19833-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASLocation](../classes/kasclient.kaslocation.md)</span><span class="sxs-lookup"><span data-stu-id="19833-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASLocation](../classes/kasclient.kaslocation.md)</span></span>

# <a name="class-kaslocation"></a><span data-ttu-id="19833-102">Klasse: KASLocation</span><span class="sxs-lookup"><span data-stu-id="19833-102">Class: KASLocation</span></span>

## <a name="hierarchy"></a><span data-ttu-id="19833-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="19833-103">Hierarchy</span></span>

<span data-ttu-id="19833-104">**KASLocation**</span><span class="sxs-lookup"><span data-stu-id="19833-104">**KASLocation**</span></span>

## <a name="index"></a><span data-ttu-id="19833-105">Index </span><span class="sxs-lookup"><span data-stu-id="19833-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="19833-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19833-106">Properties</span></span>

* [<span data-ttu-id="19833-107">latitude</span><span class="sxs-lookup"><span data-stu-id="19833-107">latitude</span></span>](kasclient.kaslocation.md#latitude)
* [<span data-ttu-id="19833-108">longitude</span><span class="sxs-lookup"><span data-stu-id="19833-108">longitude</span></span>](kasclient.kaslocation.md#longitude)
* [<span data-ttu-id="19833-109">placeAddress</span><span class="sxs-lookup"><span data-stu-id="19833-109">placeAddress</span></span>](kasclient.kaslocation.md#placeaddress)
* [<span data-ttu-id="19833-110">Ortsname</span><span class="sxs-lookup"><span data-stu-id="19833-110">placeName</span></span>](kasclient.kaslocation.md#placename)
### <a name="methods"></a><span data-ttu-id="19833-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="19833-111">Methods</span></span>

* [<span data-ttu-id="19833-112">IsEmpty</span><span class="sxs-lookup"><span data-stu-id="19833-112">isEmpty</span></span>](kasclient.kaslocation.md#isempty)
* [<span data-ttu-id="19833-113">IsEqual</span><span class="sxs-lookup"><span data-stu-id="19833-113">isEqual</span></span>](kasclient.kaslocation.md#isequal)
* [<span data-ttu-id="19833-114">toJSON</span><span class="sxs-lookup"><span data-stu-id="19833-114">toJSON</span></span>](kasclient.kaslocation.md#tojson)
* [<span data-ttu-id="19833-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="19833-115">fromJSON</span></span>](kasclient.kaslocation.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="19833-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19833-116">Properties</span></span>

<a id="latitude"></a>

###  <a name="latitude"></a><span data-ttu-id="19833-117">latitude</span><span class="sxs-lookup"><span data-stu-id="19833-117">latitude</span></span>

<span data-ttu-id="19833-118">**● Latitude**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="19833-118">**● latitude**: *`number`* = 0</span></span>

<span data-ttu-id="19833-119">Breite des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="19833-119">Latitude of the location</span></span>

___
<a id="longitude"></a>

###  <a name="longitude"></a><span data-ttu-id="19833-120">longitude</span><span class="sxs-lookup"><span data-stu-id="19833-120">longitude</span></span>

<span data-ttu-id="19833-121">**● Längengrad**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="19833-121">**● longitude**: *`number`* = 0</span></span>

<span data-ttu-id="19833-122">Längengrad des Standorts</span><span class="sxs-lookup"><span data-stu-id="19833-122">Longitude of the location</span></span>

___
<a id="placeaddress"></a>

###  <a name="placeaddress"></a><span data-ttu-id="19833-123">placeAddress</span><span class="sxs-lookup"><span data-stu-id="19833-123">placeAddress</span></span>

<span data-ttu-id="19833-124">**● placeAddress**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="19833-124">**● placeAddress**: *`string`* = ""</span></span>

<span data-ttu-id="19833-125">Adresse des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="19833-125">Address of the location</span></span>

___
<a id="placename"></a>

###  <a name="placename"></a><span data-ttu-id="19833-126">Ortsname</span><span class="sxs-lookup"><span data-stu-id="19833-126">placeName</span></span>

<span data-ttu-id="19833-127">**● Ortsname**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="19833-127">**● placeName**: *`string`* = ""</span></span>

<span data-ttu-id="19833-128">Name des Speicherorts</span><span class="sxs-lookup"><span data-stu-id="19833-128">Name of the location</span></span>

___

## <a name="methods"></a><span data-ttu-id="19833-129">Methoden</span><span class="sxs-lookup"><span data-stu-id="19833-129">Methods</span></span>

<a id="isempty"></a>

###  <a name="isempty"></a><span data-ttu-id="19833-130">IsEmpty</span><span class="sxs-lookup"><span data-stu-id="19833-130">isEmpty</span></span>

<span data-ttu-id="19833-131">▸ **IsEmpty**():`boolean`</span><span class="sxs-lookup"><span data-stu-id="19833-131">▸ **isEmpty**(): `boolean`</span></span>

<span data-ttu-id="19833-132">**Gibt Folgendes zurück:**`boolean`</span><span class="sxs-lookup"><span data-stu-id="19833-132">**Returns:** `boolean`</span></span>

___
<a id="isequal"></a>

###  <a name="isequal"></a><span data-ttu-id="19833-133">IsEqual</span><span class="sxs-lookup"><span data-stu-id="19833-133">isEqual</span></span>

<span data-ttu-id="19833-134">▸ **IsEqual**(Location: *[KASLocation](kasclient.kaslocation.md)*):`boolean`</span><span class="sxs-lookup"><span data-stu-id="19833-134">▸ **isEqual**(location: *[KASLocation](kasclient.kaslocation.md)*): `boolean`</span></span>

<span data-ttu-id="19833-135">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="19833-135">**Parameters:**</span></span>

| <span data-ttu-id="19833-136">Name</span><span class="sxs-lookup"><span data-stu-id="19833-136">Name</span></span> | <span data-ttu-id="19833-137">Typ</span><span class="sxs-lookup"><span data-stu-id="19833-137">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="19833-138">location</span><span class="sxs-lookup"><span data-stu-id="19833-138">location</span></span> | [<span data-ttu-id="19833-139">KASLocation</span><span class="sxs-lookup"><span data-stu-id="19833-139">KASLocation</span></span>](kasclient.kaslocation.md) |

<span data-ttu-id="19833-140">**Gibt Folgendes zurück:**`boolean`</span><span class="sxs-lookup"><span data-stu-id="19833-140">**Returns:** `boolean`</span></span>

___
<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="19833-141">toJSON</span><span class="sxs-lookup"><span data-stu-id="19833-141">toJSON</span></span>

<span data-ttu-id="19833-142">▸ **tojson**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="19833-142">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="19833-143">**Gibt Folgendes zurück:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="19833-143">**Returns:** `JSON`</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="19833-144">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="19833-144">`<Static>` fromJSON</span></span>

<span data-ttu-id="19833-145">▸- **fromJSON**(Objekt *`JSON`*:): [KASLocation](kasclient.kaslocation.md)</span><span class="sxs-lookup"><span data-stu-id="19833-145">▸ **fromJSON**(object: *`JSON`*): [KASLocation](kasclient.kaslocation.md)</span></span>

<span data-ttu-id="19833-146">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="19833-146">**Parameters:**</span></span>

| <span data-ttu-id="19833-147">Name</span><span class="sxs-lookup"><span data-stu-id="19833-147">Name</span></span> | <span data-ttu-id="19833-148">Typ</span><span class="sxs-lookup"><span data-stu-id="19833-148">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="19833-149">Objekt</span><span class="sxs-lookup"><span data-stu-id="19833-149">object</span></span> | `JSON` |

<span data-ttu-id="19833-150">**Gibt Folgendes zurück:** [KASLocation](kasclient.kaslocation.md)</span><span class="sxs-lookup"><span data-stu-id="19833-150">**Returns:** [KASLocation](kasclient.kaslocation.md)</span></span>

___

