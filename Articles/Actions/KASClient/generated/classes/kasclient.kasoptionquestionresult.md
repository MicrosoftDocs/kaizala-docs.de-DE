---
ms.openlocfilehash: 73491a2b9d73d311550fe14f32a34d5670e3f892
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728044"
---
<span data-ttu-id="08385-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="08385-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)</span></span>

# <a name="class-kasoptionquestionresult"></a><span data-ttu-id="08385-102">Klasse: KASOptionQuestionResult</span><span class="sxs-lookup"><span data-stu-id="08385-102">Class: KASOptionQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="08385-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="08385-103">Hierarchy</span></span>

 [<span data-ttu-id="08385-104">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="08385-104">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="08385-105">**↳ KASOptionQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="08385-105">**↳ KASOptionQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="08385-106">Index </span><span class="sxs-lookup"><span data-stu-id="08385-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="08385-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08385-107">Properties</span></span>

* [<span data-ttu-id="08385-108">optionResults</span><span class="sxs-lookup"><span data-stu-id="08385-108">optionResults</span></span>](kasclient.kasoptionquestionresult.md#optionresults)
* [<span data-ttu-id="08385-109">questionId</span><span class="sxs-lookup"><span data-stu-id="08385-109">questionId</span></span>](kasclient.kasoptionquestionresult.md#questionid)
* [<span data-ttu-id="08385-110">questionTitle</span><span class="sxs-lookup"><span data-stu-id="08385-110">questionTitle</span></span>](kasclient.kasoptionquestionresult.md#questiontitle)
* [<span data-ttu-id="08385-111">questionType</span><span class="sxs-lookup"><span data-stu-id="08385-111">questionType</span></span>](kasclient.kasoptionquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="08385-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="08385-112">Methods</span></span>

* [<span data-ttu-id="08385-113">getResultsOrder</span><span class="sxs-lookup"><span data-stu-id="08385-113">getResultsOrder</span></span>](kasclient.kasoptionquestionresult.md#getresultsorder)
* [<span data-ttu-id="08385-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="08385-114">fromJSON</span></span>](kasclient.kasoptionquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="08385-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08385-115">Properties</span></span>

<a id="optionresults"></a>

###  <a name="optionresults"></a><span data-ttu-id="08385-116">optionResults</span><span class="sxs-lookup"><span data-stu-id="08385-116">optionResults</span></span>

<span data-ttu-id="08385-117">**● OptionResults**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="08385-117">**● optionResults**: *`object`*</span></span>

<span data-ttu-id="08385-118">Für SingleSelect/MultiSelect Frage, wird das Ergebnis Option Id im Vergleich zu ihren zählt Dictionary<OptionId sein: number, OptionResult: KASOptionResult></span><span class="sxs-lookup"><span data-stu-id="08385-118">For SingleSelect/MultiSelect question, the result will be option id versus their counts Dictionary<OptionId: number, OptionResult: KASOptionResult></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="08385-119">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="08385-119">Type declaration</span></span>

___

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="08385-120">questionId</span><span class="sxs-lookup"><span data-stu-id="08385-120">questionId</span></span>

<span data-ttu-id="08385-121">**● QuestionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="08385-121">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="08385-122">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="08385-122">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="08385-123">questionTitle</span><span class="sxs-lookup"><span data-stu-id="08385-123">questionTitle</span></span>

<span data-ttu-id="08385-124">**● QuestionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="08385-124">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="08385-125">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="08385-125">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="08385-126">questionType</span><span class="sxs-lookup"><span data-stu-id="08385-126">questionType</span></span>

<span data-ttu-id="08385-127">**● QuestionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="08385-127">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="08385-128">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="08385-128">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="08385-129">Methoden</span><span class="sxs-lookup"><span data-stu-id="08385-129">Methods</span></span>

<a id="getresultsorder"></a>

###  <a name="getresultsorder"></a><span data-ttu-id="08385-130">getResultsOrder</span><span class="sxs-lookup"><span data-stu-id="08385-130">getResultsOrder</span></span>

<span data-ttu-id="08385-131">▸ **GetResultsOrder**(): `number`]</span><span class="sxs-lookup"><span data-stu-id="08385-131">▸ **getResultsOrder**(): `number`[]</span></span>

<span data-ttu-id="08385-132">Ruft alle in ihrer gesamtantworten Anzahl (absteigend) sortiert Option-ids</span><span class="sxs-lookup"><span data-stu-id="08385-132">Gets all the option ids sorted in their total responses count (descending)</span></span>

<span data-ttu-id="08385-133">**Gibt:** `number`Liste mit der Option-Ids]</span><span class="sxs-lookup"><span data-stu-id="08385-133">**Returns:** `number`[] list of all the option ids</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="08385-134">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="08385-134">`<Static>` fromJSON</span></span>

<span data-ttu-id="08385-135">▸ **FromJSON**(Objekt: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="08385-135">▸ **fromJSON**(object: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

<span data-ttu-id="08385-136">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="08385-136">**Parameters:**</span></span>

| <span data-ttu-id="08385-137">Name</span><span class="sxs-lookup"><span data-stu-id="08385-137">Name</span></span> | <span data-ttu-id="08385-138">Typ</span><span class="sxs-lookup"><span data-stu-id="08385-138">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="08385-139">object</span><span class="sxs-lookup"><span data-stu-id="08385-139">object</span></span> | `any` |

<span data-ttu-id="08385-140">**Gibt:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="08385-140">**Returns:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

___

