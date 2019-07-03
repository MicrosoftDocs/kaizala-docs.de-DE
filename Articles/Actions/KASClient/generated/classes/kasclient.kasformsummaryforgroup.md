<span data-ttu-id="a7cd7-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a7cd7-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span></span>

# <a name="class-kasformsummaryforgroup"></a><span data-ttu-id="a7cd7-102">Klasse: KASFormSummaryForGroup</span><span class="sxs-lookup"><span data-stu-id="a7cd7-102">Class: KASFormSummaryForGroup</span></span>

## <a name="hierarchy"></a><span data-ttu-id="a7cd7-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="a7cd7-103">Hierarchy</span></span>

<span data-ttu-id="a7cd7-104">**KASFormSummaryForGroup**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-104">**KASFormSummaryForGroup**</span></span>

## <a name="index"></a><span data-ttu-id="a7cd7-105">Index </span><span class="sxs-lookup"><span data-stu-id="a7cd7-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="a7cd7-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7cd7-106">Properties</span></span>

* [<span data-ttu-id="a7cd7-107">Cursor</span><span class="sxs-lookup"><span data-stu-id="a7cd7-107">cursor</span></span>](kasclient.kasformsummaryforgroup.md#cursor)
* [<span data-ttu-id="a7cd7-108">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="a7cd7-108">directMemberResponses</span></span>](kasclient.kasformsummaryforgroup.md#directmemberresponses)
* [<span data-ttu-id="a7cd7-109">responderCount</span><span class="sxs-lookup"><span data-stu-id="a7cd7-109">responderCount</span></span>](kasclient.kasformsummaryforgroup.md#respondercount)
* [<span data-ttu-id="a7cd7-110">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="a7cd7-110">subgroupSummary</span></span>](kasclient.kasformsummaryforgroup.md#subgroupsummary)
* [<span data-ttu-id="a7cd7-111">targetCount</span><span class="sxs-lookup"><span data-stu-id="a7cd7-111">targetCount</span></span>](kasclient.kasformsummaryforgroup.md#targetcount)
### <a name="methods"></a><span data-ttu-id="a7cd7-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a7cd7-112">Methods</span></span>

* [<span data-ttu-id="a7cd7-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="a7cd7-113">fromJSON</span></span>](kasclient.kasformsummaryforgroup.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="a7cd7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7cd7-114">Properties</span></span>

<a id="cursor"></a>

###  <a name="cursor"></a><span data-ttu-id="a7cd7-115">Cursor</span><span class="sxs-lookup"><span data-stu-id="a7cd7-115">cursor</span></span>

<span data-ttu-id="a7cd7-116">**● Cursor**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="a7cd7-116">**● cursor**: *`string`* = ""</span></span>

___
<a id="directmemberresponses"></a>

###  <a name="directmemberresponses"></a><span data-ttu-id="a7cd7-117">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="a7cd7-117">directMemberResponses</span></span>

<span data-ttu-id="a7cd7-118">**● directMemberResponses**: \* `KASActionInstanceResponse`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="a7cd7-118">**● directMemberResponses**: *`KASActionInstanceResponse`[]* =  []</span></span>

<span data-ttu-id="a7cd7-119">Zusammenfassung der Beispiele für die Gruppe {"c": "125955414", "RDC": 3, " \[ RS": {"ID": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "Rid": "0a228aee-c5c0-4dc5-bca0-42a634474e2b @ 1", "RS": {"0": "Jbbl", "1": "1540980866017", "2": "{" lt ": 0," LG ": 0," ACC " : 0, "n": "", "Ty": 0} "}}, {" ID ":" 41e589cf-ad48-46b9-9290-786bf64cd599 "," n ":" SRK "," Rid ":" 13dfa760-DF77-4c88-a9f6-f34a76136439 @ 1 "," RS ": {" 0 ":" Gnuk "," 1 ":" 1540981299094 "," 2 ":" {"lt": 0, "LG": 0, "ACC": "", "Ty": 0} "}} \]," SGS ": {" 0c6207fc-39ce-4b74-b420-db2d52f2cd08 @ 1 ": {" n ": NULL," RDC ": 1," TC ": 6}}," TC ": 6}</span><span class="sxs-lookup"><span data-stu-id="a7cd7-119">Sample summary for group { "c": "125955414", "rdc": 3, "rs": \[ { "id": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "rid": "0a228aee-c5c0-4dc5-bca0-42a634474e2b@1", "rs": { "0": "Jbbl", "1": "1540980866017", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } }, { "id": "41e589cf-ad48-46b9-9290-786bf64cd599", "n": "SRK", "rid": "13dfa760-df77-4c88-a9f6-f34a76136439@1", "rs": { "0": "Gnuk", "1": "1540981299094", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } } \], "sgs": { "0c6207fc-39ce-4b74-b420-db2d52f2cd08@1": { "n": null, "rdc": 1, "tc": 6 } }, "tc": 6 }</span></span>

___
<a id="respondercount"></a>

###  <a name="respondercount"></a><span data-ttu-id="a7cd7-120">responderCount</span><span class="sxs-lookup"><span data-stu-id="a7cd7-120">responderCount</span></span>

<span data-ttu-id="a7cd7-121">**● responderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="a7cd7-121">**● responderCount**: *`number`* = 0</span></span>

___
<a id="subgroupsummary"></a>

###  <a name="subgroupsummary"></a><span data-ttu-id="a7cd7-122">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="a7cd7-122">subgroupSummary</span></span>

<span data-ttu-id="a7cd7-123">**● subgroupSummary**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="a7cd7-123">**● subgroupSummary**: *`object`*</span></span>

#### <a name="type-declaration"></a><span data-ttu-id="a7cd7-124">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="a7cd7-124">Type declaration</span></span>

___
<a id="targetcount"></a>

###  <a name="targetcount"></a><span data-ttu-id="a7cd7-125">targetCount</span><span class="sxs-lookup"><span data-stu-id="a7cd7-125">targetCount</span></span>

<span data-ttu-id="a7cd7-126">**● targetCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="a7cd7-126">**● targetCount**: *`number`* = 0</span></span>

___

## <a name="methods"></a><span data-ttu-id="a7cd7-127">Methoden</span><span class="sxs-lookup"><span data-stu-id="a7cd7-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="a7cd7-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="a7cd7-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="a7cd7-129">▸- **fromJSON**(Objekt *`any`*:): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a7cd7-129">▸ **fromJSON**(object: *`any`*): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

<span data-ttu-id="a7cd7-130">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-130">**Parameters:**</span></span>

| <span data-ttu-id="a7cd7-131">Name</span><span class="sxs-lookup"><span data-stu-id="a7cd7-131">Name</span></span> | <span data-ttu-id="a7cd7-132">Typ</span><span class="sxs-lookup"><span data-stu-id="a7cd7-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="a7cd7-133">Objekt</span><span class="sxs-lookup"><span data-stu-id="a7cd7-133">object</span></span> | `any` |

<span data-ttu-id="a7cd7-134">**Gibt Folgendes zurück:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a7cd7-134">**Returns:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

___

