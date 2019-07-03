<span data-ttu-id="d90d8-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="d90d8-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span></span>

# <a name="class-kasformprocessedsummary"></a><span data-ttu-id="d90d8-102">Klasse: KASFormProcessedSummary</span><span class="sxs-lookup"><span data-stu-id="d90d8-102">Class: KASFormProcessedSummary</span></span>

## <a name="hierarchy"></a><span data-ttu-id="d90d8-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="d90d8-103">Hierarchy</span></span>

<span data-ttu-id="d90d8-104">**KASFormProcessedSummary**</span><span class="sxs-lookup"><span data-stu-id="d90d8-104">**KASFormProcessedSummary**</span></span>

## <a name="index"></a><span data-ttu-id="d90d8-105">Index </span><span class="sxs-lookup"><span data-stu-id="d90d8-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="d90d8-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d90d8-106">Properties</span></span>

* [<span data-ttu-id="d90d8-107">JSON</span><span class="sxs-lookup"><span data-stu-id="d90d8-107">json</span></span>](kasclient.kasformprocessedsummary.md#json)
* [<span data-ttu-id="d90d8-108">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="d90d8-108">nonRespondersInConversation</span></span>](kasclient.kasformprocessedsummary.md#nonrespondersinconversation)
* [<span data-ttu-id="d90d8-109">Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="d90d8-109">results</span></span>](kasclient.kasformprocessedsummary.md#results)
* [<span data-ttu-id="d90d8-110">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="d90d8-110">targetResponderCount</span></span>](kasclient.kasformprocessedsummary.md#targetrespondercount)
* [<span data-ttu-id="d90d8-111">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="d90d8-111">totalResponseCount</span></span>](kasclient.kasformprocessedsummary.md#totalresponsecount)
### <a name="methods"></a><span data-ttu-id="d90d8-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d90d8-112">Methods</span></span>

* [<span data-ttu-id="d90d8-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="d90d8-113">fromJSON</span></span>](kasclient.kasformprocessedsummary.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="d90d8-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d90d8-114">Properties</span></span>

<a id="json"></a>

###  <a name="json"></a><span data-ttu-id="d90d8-115">json</span><span class="sxs-lookup"><span data-stu-id="d90d8-115">json</span></span>

<span data-ttu-id="d90d8-116">**● JSON**:*`JSON`*</span><span class="sxs-lookup"><span data-stu-id="d90d8-116">**● json**: *`JSON`*</span></span>

___
<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a><span data-ttu-id="d90d8-117">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="d90d8-117">nonRespondersInConversation</span></span>

<span data-ttu-id="d90d8-118">**● nonRespondersInConversation**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="d90d8-118">**● nonRespondersInConversation**: *`string`[]* =  []</span></span>

<span data-ttu-id="d90d8-119">Wie viele in der Unterhaltung nicht antworteten</span><span class="sxs-lookup"><span data-stu-id="d90d8-119">How many in the conversation did not respond</span></span>

___
<a id="results"></a>

###  <a name="results"></a><span data-ttu-id="d90d8-120">results</span><span class="sxs-lookup"><span data-stu-id="d90d8-120">results</span></span>

<span data-ttu-id="d90d8-121">**● Ergebnisse**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="d90d8-121">**● results**: *`object`*</span></span>

<span data-ttu-id="d90d8-122">Aggregiertes Ergebnis für das Wörterbuch<fragwürdigen Aggregations Fragen: Number, result: KASQuestionResult></span><span class="sxs-lookup"><span data-stu-id="d90d8-122">Aggregated result for aggregative questions Dictionary<QuestionId: number, Result: KASQuestionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="d90d8-123">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="d90d8-123">Type declaration</span></span>

___
<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a><span data-ttu-id="d90d8-124">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="d90d8-124">targetResponderCount</span></span>

<span data-ttu-id="d90d8-125">**● targetResponderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="d90d8-125">**● targetResponderCount**: *`number`* = 0</span></span>

<span data-ttu-id="d90d8-126">Wie viele in der Unterhaltung zugewiesen wurden, um auf dieses Formular zu Antworten</span><span class="sxs-lookup"><span data-stu-id="d90d8-126">How many in the conversation were assigned to respond to this form</span></span>

___
<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a><span data-ttu-id="d90d8-127">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="d90d8-127">totalResponseCount</span></span>

<span data-ttu-id="d90d8-128">**● totalResponseCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="d90d8-128">**● totalResponseCount**: *`number`* = 0</span></span>

<span data-ttu-id="d90d8-129">Wie viele Antworten insgesamt für das Formular empfangen wurden, wobei mehrere Antworten von einer Person berücksichtigt wurden</span><span class="sxs-lookup"><span data-stu-id="d90d8-129">How many total responses were received for the form, considering multiple responses from one person</span></span>

___

## <a name="methods"></a><span data-ttu-id="d90d8-130">Methoden</span><span class="sxs-lookup"><span data-stu-id="d90d8-130">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="d90d8-131">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="d90d8-131">`<Static>` fromJSON</span></span>

<span data-ttu-id="d90d8-132">▸- **fromJSON**(Objekt *`JSON`*:): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="d90d8-132">▸ **fromJSON**(object: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

<span data-ttu-id="d90d8-133">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="d90d8-133">**Parameters:**</span></span>

| <span data-ttu-id="d90d8-134">Name</span><span class="sxs-lookup"><span data-stu-id="d90d8-134">Name</span></span> | <span data-ttu-id="d90d8-135">Typ</span><span class="sxs-lookup"><span data-stu-id="d90d8-135">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="d90d8-136">Objekt</span><span class="sxs-lookup"><span data-stu-id="d90d8-136">object</span></span> | `JSON` |

<span data-ttu-id="d90d8-137">**Gibt Folgendes zurück:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="d90d8-137">**Returns:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

___

