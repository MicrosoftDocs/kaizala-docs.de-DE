<span data-ttu-id="804f4-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="804f4-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span></span>

# <a name="class-kaserror"></a><span data-ttu-id="804f4-102">Klasse: KASError</span><span class="sxs-lookup"><span data-stu-id="804f4-102">Class: KASError</span></span>

## <a name="hierarchy"></a><span data-ttu-id="804f4-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="804f4-103">Hierarchy</span></span>

<span data-ttu-id="804f4-104">**KASError**</span><span class="sxs-lookup"><span data-stu-id="804f4-104">**KASError**</span></span>

## <a name="index"></a><span data-ttu-id="804f4-105">Index </span><span class="sxs-lookup"><span data-stu-id="804f4-105">Index</span></span>

### <a name="constructors"></a><span data-ttu-id="804f4-106">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="804f4-106">Constructors</span></span>

* [<span data-ttu-id="804f4-107">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="804f4-107">constructor</span></span>](kasclient.kaserror.md#constructor)
### <a name="properties"></a><span data-ttu-id="804f4-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="804f4-108">Properties</span></span>

* [<span data-ttu-id="804f4-109">description</span><span class="sxs-lookup"><span data-stu-id="804f4-109">description</span></span>](kasclient.kaserror.md#description)
* [<span data-ttu-id="804f4-110">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="804f4-110">errorCode</span></span>](kasclient.kaserror.md#errorcode)
### <a name="methods"></a><span data-ttu-id="804f4-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="804f4-111">Methods</span></span>

* [<span data-ttu-id="804f4-112">ToString</span><span class="sxs-lookup"><span data-stu-id="804f4-112">toString</span></span>](kasclient.kaserror.md#tostring)
* [<span data-ttu-id="804f4-113">fromErrorString</span><span class="sxs-lookup"><span data-stu-id="804f4-113">fromErrorString</span></span>](kasclient.kaserror.md#fromerrorstring)
* [<span data-ttu-id="804f4-114">fromString</span><span class="sxs-lookup"><span data-stu-id="804f4-114">fromString</span></span>](kasclient.kaserror.md#fromstring)

---

## <a name="constructors"></a><span data-ttu-id="804f4-115">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="804f4-115">Constructors</span></span>

<a id="constructor"></a>

###  <a name="constructor"></a><span data-ttu-id="804f4-116">constructor</span><span class="sxs-lookup"><span data-stu-id="804f4-116">constructor</span></span>

<span data-ttu-id="804f4-117">⊕ **New KASError**(ErrorCode: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)*, Description: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="804f4-117">⊕ **new KASError**(errorCode: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)*, description: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="804f4-118">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="804f4-118">**Parameters:**</span></span>

| <span data-ttu-id="804f4-119">Name</span><span class="sxs-lookup"><span data-stu-id="804f4-119">Name</span></span> | <span data-ttu-id="804f4-120">Typ</span><span class="sxs-lookup"><span data-stu-id="804f4-120">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="804f4-121">errorCode</span><span class="sxs-lookup"><span data-stu-id="804f4-121">errorCode</span></span> | [<span data-ttu-id="804f4-122">KASErrorCode</span><span class="sxs-lookup"><span data-stu-id="804f4-122">KASErrorCode</span></span>](../enums/kasclient.kaserrorcode.md) |
| <span data-ttu-id="804f4-123">description</span><span class="sxs-lookup"><span data-stu-id="804f4-123">description</span></span> | `string` |

<span data-ttu-id="804f4-124">**Gibt Folgendes zurück:** [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="804f4-124">**Returns:** [KASError](kasclient.kaserror.md)</span></span>

___

## <a name="properties"></a><span data-ttu-id="804f4-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="804f4-125">Properties</span></span>

<a id="description"></a>

###  <a name="description"></a><span data-ttu-id="804f4-126">description</span><span class="sxs-lookup"><span data-stu-id="804f4-126">description</span></span>

<span data-ttu-id="804f4-127">**● Description**: *`String`* = ""</span><span class="sxs-lookup"><span data-stu-id="804f4-127">**● description**: *`String`* = ""</span></span>

___
<a id="errorcode"></a>

###  <a name="errorcode"></a><span data-ttu-id="804f4-128">errorCode</span><span class="sxs-lookup"><span data-stu-id="804f4-128">errorCode</span></span>

<span data-ttu-id="804f4-129">**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* = KASErrorCode. None</span><span class="sxs-lookup"><span data-stu-id="804f4-129">**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* =  KASErrorCode.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="804f4-130">Methoden</span><span class="sxs-lookup"><span data-stu-id="804f4-130">Methods</span></span>

<a id="tostring"></a>

###  <a name="tostring"></a><span data-ttu-id="804f4-131">ToString</span><span class="sxs-lookup"><span data-stu-id="804f4-131">toString</span></span>

<span data-ttu-id="804f4-132">▸ **ToString**():`string`</span><span class="sxs-lookup"><span data-stu-id="804f4-132">▸ **toString**(): `string`</span></span>

<span data-ttu-id="804f4-133">**Gibt Folgendes zurück:**`string`</span><span class="sxs-lookup"><span data-stu-id="804f4-133">**Returns:** `string`</span></span>

___
<a id="fromerrorstring"></a>

### <a name="static-fromerrorstring"></a><span data-ttu-id="804f4-134">`<Static>`fromErrorString</span><span class="sxs-lookup"><span data-stu-id="804f4-134">`<Static>` fromErrorString</span></span>

<span data-ttu-id="804f4-135">▸ **fromErrorString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="804f4-135">▸ **fromErrorString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="804f4-136">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="804f4-136">**Parameters:**</span></span>

| <span data-ttu-id="804f4-137">Name</span><span class="sxs-lookup"><span data-stu-id="804f4-137">Name</span></span> | <span data-ttu-id="804f4-138">Typ</span><span class="sxs-lookup"><span data-stu-id="804f4-138">Type</span></span> | <span data-ttu-id="804f4-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="804f4-139">Description</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="804f4-140">stringifyError</span><span class="sxs-lookup"><span data-stu-id="804f4-140">stringifyError</span></span> | `string` |  <span data-ttu-id="804f4-141">stringified-Wörterbuch des Fehlers mit Code und Beschreibung</span><span class="sxs-lookup"><span data-stu-id="804f4-141">stringified dictionary of error with code and description</span></span> |

<span data-ttu-id="804f4-142">**Gibt Folgendes zurück:** [KASError](kasclient.kaserror.md) gibt KASError-Objekt zurück, das aus stringified-Fehler gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="804f4-142">**Returns:** [KASError](kasclient.kaserror.md) returns KASError object made from stringified error.</span></span> <span data-ttu-id="804f4-143">Für NULL-Zeichenfolge wird NULL-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="804f4-143">For null string, null object is returned.</span></span>

___
<a id="fromstring"></a>

### <a name="static-fromstring"></a><span data-ttu-id="804f4-144">`<Static>`fromString</span><span class="sxs-lookup"><span data-stu-id="804f4-144">`<Static>` fromString</span></span>

<span data-ttu-id="804f4-145">▸ **fromtype**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="804f4-145">▸ **fromString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="804f4-146">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="804f4-146">**Parameters:**</span></span>

| <span data-ttu-id="804f4-147">Name</span><span class="sxs-lookup"><span data-stu-id="804f4-147">Name</span></span> | <span data-ttu-id="804f4-148">Typ</span><span class="sxs-lookup"><span data-stu-id="804f4-148">Type</span></span> | <span data-ttu-id="804f4-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="804f4-149">Description</span></span> |
| ------ | ------ | ------ |
| <span data-ttu-id="804f4-150">stringifyError</span><span class="sxs-lookup"><span data-stu-id="804f4-150">stringifyError</span></span> | `string` |  <span data-ttu-id="804f4-151">stringified-Wörterbuch des Fehlers mit Code und Beschreibung</span><span class="sxs-lookup"><span data-stu-id="804f4-151">stringified dictionary of error with code and description</span></span> |

<span data-ttu-id="804f4-152">**Gibt Folgendes zurück:** [KASError](kasclient.kaserror.md) gibt KASError-Objekt zurück, das aus stringified-Fehler gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="804f4-152">**Returns:** [KASError](kasclient.kaserror.md) returns KASError object made from stringified error.</span></span> <span data-ttu-id="804f4-153">Bei NULL-Zeichenfolge wird auch ungleich NULL-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="804f4-153">For null string also, non-null error code is returned</span></span>

___

