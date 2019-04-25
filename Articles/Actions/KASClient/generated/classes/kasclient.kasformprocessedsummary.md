<span data-ttu-id="32386-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="32386-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)</span></span>

# <a name="class-kasformprocessedsummary"></a><span data-ttu-id="32386-102">Klasse: KASFormProcessedSummary</span><span class="sxs-lookup"><span data-stu-id="32386-102">Class: KASFormProcessedSummary</span></span>

## <a name="hierarchy"></a><span data-ttu-id="32386-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="32386-103">Hierarchy</span></span>

<span data-ttu-id="32386-104">**KASFormProcessedSummary**</span><span class="sxs-lookup"><span data-stu-id="32386-104">**KASFormProcessedSummary**</span></span>

## <a name="index"></a><span data-ttu-id="32386-105">Index </span><span class="sxs-lookup"><span data-stu-id="32386-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="32386-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32386-106">Properties</span></span>

* [<span data-ttu-id="32386-107">JSON</span><span class="sxs-lookup"><span data-stu-id="32386-107">json</span></span>](kasclient.kasformprocessedsummary.md#json)
* [<span data-ttu-id="32386-108">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="32386-108">nonRespondersInConversation</span></span>](kasclient.kasformprocessedsummary.md#nonrespondersinconversation)
* [<span data-ttu-id="32386-109">Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="32386-109">results</span></span>](kasclient.kasformprocessedsummary.md#results)
* [<span data-ttu-id="32386-110">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="32386-110">targetResponderCount</span></span>](kasclient.kasformprocessedsummary.md#targetrespondercount)
* [<span data-ttu-id="32386-111">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="32386-111">totalResponseCount</span></span>](kasclient.kasformprocessedsummary.md#totalresponsecount)
### <a name="methods"></a><span data-ttu-id="32386-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="32386-112">Methods</span></span>

* [<span data-ttu-id="32386-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="32386-113">fromJSON</span></span>](kasclient.kasformprocessedsummary.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="32386-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32386-114">Properties</span></span>

<a id="json"></a>

###  <a name="json"></a><span data-ttu-id="32386-115">json</span><span class="sxs-lookup"><span data-stu-id="32386-115">json</span></span>

<span data-ttu-id="32386-116">**● JSON**:*`JSON`*</span><span class="sxs-lookup"><span data-stu-id="32386-116">**● json**: *`JSON`*</span></span>

___

<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a><span data-ttu-id="32386-117">nonRespondersInConversation</span><span class="sxs-lookup"><span data-stu-id="32386-117">nonRespondersInConversation</span></span>

<span data-ttu-id="32386-118">**● nonRespondersInConversation**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="32386-118">**● nonRespondersInConversation**: *`string`[]* =  []</span></span>

<span data-ttu-id="32386-119">Wie viele in der Unterhaltung nicht reagierten</span><span class="sxs-lookup"><span data-stu-id="32386-119">How many in the conversation did not respond</span></span>

___

<a id="results"></a>

###  <a name="results"></a><span data-ttu-id="32386-120">results</span><span class="sxs-lookup"><span data-stu-id="32386-120">results</span></span>

<span data-ttu-id="32386-121">**● Ergebnisse**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="32386-121">**● results**: *`object`*</span></span>

<span data-ttu-id="32386-122">Aggregiertes Ergebnis für aggregierte Fragen Dictionary<QuestionId: Number, result: KASQuestionResult></span><span class="sxs-lookup"><span data-stu-id="32386-122">Aggregated result for aggregative questions Dictionary<QuestionId: number, Result: KASQuestionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="32386-123">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="32386-123">Type declaration</span></span>

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a><span data-ttu-id="32386-124">targetResponderCount</span><span class="sxs-lookup"><span data-stu-id="32386-124">targetResponderCount</span></span>

<span data-ttu-id="32386-125">**● targetResponderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="32386-125">**● targetResponderCount**: *`number`* = 0</span></span>

<span data-ttu-id="32386-126">Wie viele in der Unterhaltung zugewiesen wurden, um auf dieses Formular zu reagieren</span><span class="sxs-lookup"><span data-stu-id="32386-126">How many in the conversation were assigned to respond to this form</span></span>

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a><span data-ttu-id="32386-127">totalResponseCount</span><span class="sxs-lookup"><span data-stu-id="32386-127">totalResponseCount</span></span>

<span data-ttu-id="32386-128">**● totalResponseCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="32386-128">**● totalResponseCount**: *`number`* = 0</span></span>

<span data-ttu-id="32386-129">Wie viele Gesamt Antworten wurden für das Formular empfangen, wenn mehrere Antworten von einer Person berücksichtigt werden</span><span class="sxs-lookup"><span data-stu-id="32386-129">How many total responses were received for the form, considering multiple responses from one person</span></span>

___

## <a name="methods"></a><span data-ttu-id="32386-130">Methoden</span><span class="sxs-lookup"><span data-stu-id="32386-130">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="32386-131">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="32386-131">`<Static>` fromJSON</span></span>

<span data-ttu-id="32386-132">▸ **fromJSON**(Object: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="32386-132">▸ **fromJSON**(object: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

<span data-ttu-id="32386-133">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="32386-133">**Parameters:**</span></span>

| <span data-ttu-id="32386-134">Name</span><span class="sxs-lookup"><span data-stu-id="32386-134">Name</span></span> | <span data-ttu-id="32386-135">Typ</span><span class="sxs-lookup"><span data-stu-id="32386-135">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="32386-136">Objekt</span><span class="sxs-lookup"><span data-stu-id="32386-136">object</span></span> | `JSON` |

<span data-ttu-id="32386-137">**Gibt Folgendes zurück:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span><span class="sxs-lookup"><span data-stu-id="32386-137">**Returns:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)</span></span>

___

