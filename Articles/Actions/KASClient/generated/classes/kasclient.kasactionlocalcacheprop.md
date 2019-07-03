<span data-ttu-id="50610-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)</span><span class="sxs-lookup"><span data-stu-id="50610-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)</span></span>

# <a name="class-kasactionlocalcacheprop"></a><span data-ttu-id="50610-102">Klasse: KASActionLocalCacheProp</span><span class="sxs-lookup"><span data-stu-id="50610-102">Class: KASActionLocalCacheProp</span></span>

## <a name="hierarchy"></a><span data-ttu-id="50610-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="50610-103">Hierarchy</span></span>

<span data-ttu-id="50610-104">**KASActionLocalCacheProp**</span><span class="sxs-lookup"><span data-stu-id="50610-104">**KASActionLocalCacheProp**</span></span>

## <a name="index"></a><span data-ttu-id="50610-105">Index </span><span class="sxs-lookup"><span data-stu-id="50610-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="50610-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50610-106">Properties</span></span>

* [<span data-ttu-id="50610-107">cacheScope</span><span class="sxs-lookup"><span data-stu-id="50610-107">cacheScope</span></span>](kasclient.kasactionlocalcacheprop.md#cachescope)
* [<span data-ttu-id="50610-108">cacheVisibility</span><span class="sxs-lookup"><span data-stu-id="50610-108">cacheVisibility</span></span>](kasclient.kasactionlocalcacheprop.md#cachevisibility)
* [<span data-ttu-id="50610-109">key</span><span class="sxs-lookup"><span data-stu-id="50610-109">key</span></span>](kasclient.kasactionlocalcacheprop.md#key)
* [<span data-ttu-id="50610-110">value</span><span class="sxs-lookup"><span data-stu-id="50610-110">value</span></span>](kasclient.kasactionlocalcacheprop.md#value)
### <a name="methods"></a><span data-ttu-id="50610-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="50610-111">Methods</span></span>

* [<span data-ttu-id="50610-112">toJSON</span><span class="sxs-lookup"><span data-stu-id="50610-112">toJSON</span></span>](kasclient.kasactionlocalcacheprop.md#tojson)
* [<span data-ttu-id="50610-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="50610-113">fromJSON</span></span>](kasclient.kasactionlocalcacheprop.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="50610-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50610-114">Properties</span></span>

<a id="cachescope"></a>

###  <a name="cachescope"></a><span data-ttu-id="50610-115">cacheScope</span><span class="sxs-lookup"><span data-stu-id="50610-115">cacheScope</span></span>

<span data-ttu-id="50610-116">**● cacheScope**: *[cacheScope](../enums/kasclient.cachescope.md)* = cacheScope. Global</span><span class="sxs-lookup"><span data-stu-id="50610-116">**● cacheScope**: *[CacheScope](../enums/kasclient.cachescope.md)* =  CacheScope.Global</span></span>

<span data-ttu-id="50610-117">cacheScope gibt an, dass die Daten auf globaler oder converastion Ebene gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="50610-117">cacheScope indicates the data will store at global or converastion level.</span></span>

___
<a id="cachevisibility"></a>

###  <a name="cachevisibility"></a><span data-ttu-id="50610-118">cacheVisibility</span><span class="sxs-lookup"><span data-stu-id="50610-118">cacheVisibility</span></span>

<span data-ttu-id="50610-119">**● cacheVisibility**: *[cacheVisibility](../enums/kasclient.cachevisibility.md)* = cacheVisibility. app</span><span class="sxs-lookup"><span data-stu-id="50610-119">**● cacheVisibility**: *[CacheVisibility](../enums/kasclient.cachevisibility.md)* =  CacheVisibility.App</span></span>

<span data-ttu-id="50610-120">cacheVisibility gibt an, dass die Daten für andere apps sichtbar sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="50610-120">cacheVisibility indicates that the data visible to other app or not.</span></span>

___
<a id="key"></a>

###  <a name="key"></a><span data-ttu-id="50610-121">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="50610-121">key</span></span>

<span data-ttu-id="50610-122">**● Taste**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="50610-122">**● key**: *`string`* = ""</span></span>

<span data-ttu-id="50610-123">Schlüssel des im Cache gespeicherten Werts</span><span class="sxs-lookup"><span data-stu-id="50610-123">key of the value stored in cache</span></span>

___
<a id="value"></a>

###  <a name="value"></a><span data-ttu-id="50610-124">Wert</span><span class="sxs-lookup"><span data-stu-id="50610-124">value</span></span>

<span data-ttu-id="50610-125">**● Wert**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="50610-125">**● value**: *`string`* = ""</span></span>

___

## <a name="methods"></a><span data-ttu-id="50610-126">Methoden</span><span class="sxs-lookup"><span data-stu-id="50610-126">Methods</span></span>

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="50610-127">toJSON</span><span class="sxs-lookup"><span data-stu-id="50610-127">toJSON</span></span>

<span data-ttu-id="50610-128">▸ **tojson**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="50610-128">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="50610-129">**Gibt Folgendes zurück:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="50610-129">**Returns:** `JSON`</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="50610-130">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="50610-130">`<Static>` fromJSON</span></span>

<span data-ttu-id="50610-131">▸- **fromJSON**(Objekt *`JSON`*:): [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)</span><span class="sxs-lookup"><span data-stu-id="50610-131">▸ **fromJSON**(object: *`JSON`*): [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)</span></span>

<span data-ttu-id="50610-132">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="50610-132">**Parameters:**</span></span>

| <span data-ttu-id="50610-133">Name</span><span class="sxs-lookup"><span data-stu-id="50610-133">Name</span></span> | <span data-ttu-id="50610-134">Typ</span><span class="sxs-lookup"><span data-stu-id="50610-134">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="50610-135">Objekt</span><span class="sxs-lookup"><span data-stu-id="50610-135">object</span></span> | `JSON` |

<span data-ttu-id="50610-136">**Gibt Folgendes zurück:** [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)</span><span class="sxs-lookup"><span data-stu-id="50610-136">**Returns:** [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)</span></span>

___

