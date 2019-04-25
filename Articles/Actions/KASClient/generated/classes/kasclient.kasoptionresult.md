<span data-ttu-id="9ab3a-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9ab3a-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span></span>

# <a name="class-kasoptionresult"></a><span data-ttu-id="9ab3a-102">Klasse: KASOptionResult</span><span class="sxs-lookup"><span data-stu-id="9ab3a-102">Class: KASOptionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="9ab3a-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="9ab3a-103">Hierarchy</span></span>

<span data-ttu-id="9ab3a-104">**KASOptionResult**</span><span class="sxs-lookup"><span data-stu-id="9ab3a-104">**KASOptionResult**</span></span>

## <a name="index"></a><span data-ttu-id="9ab3a-105">Index </span><span class="sxs-lookup"><span data-stu-id="9ab3a-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="9ab3a-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ab3a-106">Properties</span></span>

* [<span data-ttu-id="9ab3a-107">optionId</span><span class="sxs-lookup"><span data-stu-id="9ab3a-107">optionId</span></span>](kasclient.kasoptionresult.md#optionid)
* [<span data-ttu-id="9ab3a-108">optionTitle</span><span class="sxs-lookup"><span data-stu-id="9ab3a-108">optionTitle</span></span>](kasclient.kasoptionresult.md#optiontitle)
* [<span data-ttu-id="9ab3a-109">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="9ab3a-109">responderToResponseCount</span></span>](kasclient.kasoptionresult.md#respondertoresponsecount)
* [<span data-ttu-id="9ab3a-110">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="9ab3a-110">totalResponsesCount</span></span>](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a><span data-ttu-id="9ab3a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9ab3a-111">Methods</span></span>

* [<span data-ttu-id="9ab3a-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="9ab3a-112">fromJSON</span></span>](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="9ab3a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ab3a-113">Properties</span></span>

<a id="optionid"></a>

###  <a name="optionid"></a><span data-ttu-id="9ab3a-114">optionId</span><span class="sxs-lookup"><span data-stu-id="9ab3a-114">optionId</span></span>

<span data-ttu-id="9ab3a-115">**● options**-Nr *`number`* .: = 0</span><span class="sxs-lookup"><span data-stu-id="9ab3a-115">**● optionId**: *`number`* = 0</span></span>

<span data-ttu-id="9ab3a-116">Index der Option</span><span class="sxs-lookup"><span data-stu-id="9ab3a-116">Index of the option</span></span>

___

<a id="optiontitle"></a>

###  <a name="optiontitle"></a><span data-ttu-id="9ab3a-117">optionTitle</span><span class="sxs-lookup"><span data-stu-id="9ab3a-117">optionTitle</span></span>

<span data-ttu-id="9ab3a-118">**● optionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="9ab3a-118">**● optionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="9ab3a-119">Titel der Option</span><span class="sxs-lookup"><span data-stu-id="9ab3a-119">Title of the option</span></span>

___

<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a><span data-ttu-id="9ab3a-120">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="9ab3a-120">responderToResponseCount</span></span>

<span data-ttu-id="9ab3a-121">**● responderToResponseCount**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="9ab3a-121">**● responderToResponseCount**: *`object`*</span></span>

<span data-ttu-id="9ab3a-122">Eine Zuordnung von Benutzer-IDs mit ihrer Antwort Anzahl Dictionary<UserId: String, ResponseCount: number></span><span class="sxs-lookup"><span data-stu-id="9ab3a-122">A map of user ids against their response count Dictionary<UserId: string, ResponseCount: number></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="9ab3a-123">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="9ab3a-123">Type declaration</span></span>

___

<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a><span data-ttu-id="9ab3a-124">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="9ab3a-124">totalResponsesCount</span></span>

<span data-ttu-id="9ab3a-125">**● totalResponsesCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="9ab3a-125">**● totalResponsesCount**: *`number`* = 0</span></span>

<span data-ttu-id="9ab3a-126">Wie viele haben diese Option gewählt?</span><span class="sxs-lookup"><span data-stu-id="9ab3a-126">How many have chosen this option</span></span>

___

## <a name="methods"></a><span data-ttu-id="9ab3a-127">Methoden</span><span class="sxs-lookup"><span data-stu-id="9ab3a-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="9ab3a-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="9ab3a-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="9ab3a-129">▸ **fromJSON**(Object: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9ab3a-129">▸ **fromJSON**(object: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

<span data-ttu-id="9ab3a-130">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="9ab3a-130">**Parameters:**</span></span>

| <span data-ttu-id="9ab3a-131">Name</span><span class="sxs-lookup"><span data-stu-id="9ab3a-131">Name</span></span> | <span data-ttu-id="9ab3a-132">Typ</span><span class="sxs-lookup"><span data-stu-id="9ab3a-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="9ab3a-133">Objekt</span><span class="sxs-lookup"><span data-stu-id="9ab3a-133">object</span></span> | `any` |

<span data-ttu-id="9ab3a-134">**Gibt Folgendes zurück:** [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9ab3a-134">**Returns:** [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

___

