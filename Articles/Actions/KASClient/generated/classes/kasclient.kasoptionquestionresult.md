<span data-ttu-id="4739a-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4739a-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)</span></span>

# <a name="class-kasoptionquestionresult"></a><span data-ttu-id="4739a-102">Klasse: KASOptionQuestionResult</span><span class="sxs-lookup"><span data-stu-id="4739a-102">Class: KASOptionQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="4739a-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="4739a-103">Hierarchy</span></span>

 [<span data-ttu-id="4739a-104">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="4739a-104">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="4739a-105">**↳ KASOptionQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="4739a-105">**↳ KASOptionQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="4739a-106">Index </span><span class="sxs-lookup"><span data-stu-id="4739a-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="4739a-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4739a-107">Properties</span></span>

* [<span data-ttu-id="4739a-108">optionResults</span><span class="sxs-lookup"><span data-stu-id="4739a-108">optionResults</span></span>](kasclient.kasoptionquestionresult.md#optionresults)
* [<span data-ttu-id="4739a-109">Fragen-Nr</span><span class="sxs-lookup"><span data-stu-id="4739a-109">questionId</span></span>](kasclient.kasoptionquestionresult.md#questionid)
* [<span data-ttu-id="4739a-110">questionTitle</span><span class="sxs-lookup"><span data-stu-id="4739a-110">questionTitle</span></span>](kasclient.kasoptionquestionresult.md#questiontitle)
* [<span data-ttu-id="4739a-111">questiontype</span><span class="sxs-lookup"><span data-stu-id="4739a-111">questionType</span></span>](kasclient.kasoptionquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="4739a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4739a-112">Methods</span></span>

* [<span data-ttu-id="4739a-113">getResultsOrder</span><span class="sxs-lookup"><span data-stu-id="4739a-113">getResultsOrder</span></span>](kasclient.kasoptionquestionresult.md#getresultsorder)
* [<span data-ttu-id="4739a-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="4739a-114">fromJSON</span></span>](kasclient.kasoptionquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="4739a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4739a-115">Properties</span></span>

<a id="optionresults"></a>

###  <a name="optionresults"></a><span data-ttu-id="4739a-116">optionResults</span><span class="sxs-lookup"><span data-stu-id="4739a-116">optionResults</span></span>

<span data-ttu-id="4739a-117">**● optionResults**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="4739a-117">**● optionResults**: *`object`*</span></span>

<span data-ttu-id="4739a-118">Für SingleSelect/MultiSelect-Frage ist das Ergebnis die Options-ID im Vergleich zu Ihrem Counts-Wörterbuch<Optionskennung: Number, OptionResult: KASOptionResult></span><span class="sxs-lookup"><span data-stu-id="4739a-118">For SingleSelect/MultiSelect question, the result will be option id versus their counts Dictionary<OptionId: number, OptionResult: KASOptionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="4739a-119">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="4739a-119">Type declaration</span></span>

___
<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="4739a-120">Fragen-Nr</span><span class="sxs-lookup"><span data-stu-id="4739a-120">questionId</span></span>

<span data-ttu-id="4739a-121">**● Frag**-Nr *`number`* : = 0</span><span class="sxs-lookup"><span data-stu-id="4739a-121">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="4739a-122">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="4739a-122">Index of the question</span></span>

___
<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="4739a-123">questionTitle</span><span class="sxs-lookup"><span data-stu-id="4739a-123">questionTitle</span></span>

<span data-ttu-id="4739a-124">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="4739a-124">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="4739a-125">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="4739a-125">Title of the question</span></span>

___
<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="4739a-126">questiontype</span><span class="sxs-lookup"><span data-stu-id="4739a-126">questionType</span></span>

<span data-ttu-id="4739a-127">**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="4739a-127">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="4739a-128">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="4739a-128">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="4739a-129">Methoden</span><span class="sxs-lookup"><span data-stu-id="4739a-129">Methods</span></span>

<a id="getresultsorder"></a>

###  <a name="getresultsorder"></a><span data-ttu-id="4739a-130">getResultsOrder</span><span class="sxs-lookup"><span data-stu-id="4739a-130">getResultsOrder</span></span>

<span data-ttu-id="4739a-131">▸ **getResultsOrder**(): `number`[]</span><span class="sxs-lookup"><span data-stu-id="4739a-131">▸ **getResultsOrder**(): `number`[]</span></span>

<span data-ttu-id="4739a-132">Ruft alle Options-IDs ab, die in der Gesamtanzahl der Antworten sortiert sind (absteigend).</span><span class="sxs-lookup"><span data-stu-id="4739a-132">Gets all the option ids sorted in their total responses count (descending)</span></span>

<span data-ttu-id="4739a-133">**Gibt Folgendes zurück:** `number`[] Liste aller Options-IDs</span><span class="sxs-lookup"><span data-stu-id="4739a-133">**Returns:** `number`[] list of all the option ids</span></span>

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="4739a-134">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="4739a-134">`<Static>` fromJSON</span></span>

<span data-ttu-id="4739a-135">▸- **fromJSON**(Objekt *`any`*:): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4739a-135">▸ **fromJSON**(object: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

<span data-ttu-id="4739a-136">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="4739a-136">**Parameters:**</span></span>

| <span data-ttu-id="4739a-137">Name</span><span class="sxs-lookup"><span data-stu-id="4739a-137">Name</span></span> | <span data-ttu-id="4739a-138">Typ</span><span class="sxs-lookup"><span data-stu-id="4739a-138">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="4739a-139">Objekt</span><span class="sxs-lookup"><span data-stu-id="4739a-139">object</span></span> | `any` |

<span data-ttu-id="4739a-140">**Gibt Folgendes zurück:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="4739a-140">**Returns:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

___

