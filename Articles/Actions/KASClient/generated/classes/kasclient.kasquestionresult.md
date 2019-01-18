---
ms.openlocfilehash: 1e51f3aa34eb9a0a229cae1d4fd25be002447a1e
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728090"
---
<span data-ttu-id="decbb-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="decbb-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span></span>

# <a name="class-kasquestionresult"></a><span data-ttu-id="decbb-102">Klasse: KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="decbb-102">Class: KASQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="decbb-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="decbb-103">Hierarchy</span></span>

<span data-ttu-id="decbb-104">**KASQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="decbb-104">**KASQuestionResult**</span></span>

<span data-ttu-id="decbb-105">↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="decbb-105">↳  [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span></span>

<span data-ttu-id="decbb-106">↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="decbb-106">↳  [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

<span data-ttu-id="decbb-107">↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="decbb-107">↳  [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

## <a name="index"></a><span data-ttu-id="decbb-108">Index </span><span class="sxs-lookup"><span data-stu-id="decbb-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="decbb-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="decbb-109">Properties</span></span>

* [<span data-ttu-id="decbb-110">questionId</span><span class="sxs-lookup"><span data-stu-id="decbb-110">questionId</span></span>](kasclient.kasquestionresult.md#questionid)
* [<span data-ttu-id="decbb-111">questionTitle</span><span class="sxs-lookup"><span data-stu-id="decbb-111">questionTitle</span></span>](kasclient.kasquestionresult.md#questiontitle)
* [<span data-ttu-id="decbb-112">questionType</span><span class="sxs-lookup"><span data-stu-id="decbb-112">questionType</span></span>](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="decbb-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="decbb-113">Methods</span></span>

* [<span data-ttu-id="decbb-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="decbb-114">fromJSON</span></span>](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="decbb-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="decbb-115">Properties</span></span>

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="decbb-116">questionId</span><span class="sxs-lookup"><span data-stu-id="decbb-116">questionId</span></span>

<span data-ttu-id="decbb-117">**● QuestionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="decbb-117">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="decbb-118">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="decbb-118">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="decbb-119">questionTitle</span><span class="sxs-lookup"><span data-stu-id="decbb-119">questionTitle</span></span>

<span data-ttu-id="decbb-120">**● QuestionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="decbb-120">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="decbb-121">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="decbb-121">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="decbb-122">questionType</span><span class="sxs-lookup"><span data-stu-id="decbb-122">questionType</span></span>

<span data-ttu-id="decbb-123">**● QuestionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="decbb-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="decbb-124">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="decbb-124">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="decbb-125">Methoden</span><span class="sxs-lookup"><span data-stu-id="decbb-125">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="decbb-126">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="decbb-126">`<Static>` fromJSON</span></span>

<span data-ttu-id="decbb-127">▸ **FromJSON**(Objekt: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="decbb-127">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="decbb-128">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="decbb-128">**Parameters:**</span></span>

| <span data-ttu-id="decbb-129">Name</span><span class="sxs-lookup"><span data-stu-id="decbb-129">Name</span></span> | <span data-ttu-id="decbb-130">Typ</span><span class="sxs-lookup"><span data-stu-id="decbb-130">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="decbb-131">object</span><span class="sxs-lookup"><span data-stu-id="decbb-131">object</span></span> | `any` |

<span data-ttu-id="decbb-132">**Gibt:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="decbb-132">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

