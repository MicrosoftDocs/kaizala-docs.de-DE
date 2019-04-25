<span data-ttu-id="23cbb-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="23cbb-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span></span>

# <a name="class-kasquestionresult"></a><span data-ttu-id="23cbb-102">Klasse: KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="23cbb-102">Class: KASQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="23cbb-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="23cbb-103">Hierarchy</span></span>

<span data-ttu-id="23cbb-104">**KASQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="23cbb-104">**KASQuestionResult**</span></span>

<span data-ttu-id="23cbb-105">↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="23cbb-105">↳  [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span></span>

<span data-ttu-id="23cbb-106">↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="23cbb-106">↳  [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

<span data-ttu-id="23cbb-107">↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="23cbb-107">↳  [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

## <a name="index"></a><span data-ttu-id="23cbb-108">Index </span><span class="sxs-lookup"><span data-stu-id="23cbb-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="23cbb-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23cbb-109">Properties</span></span>

* [<span data-ttu-id="23cbb-110">Frag-Nr.</span><span class="sxs-lookup"><span data-stu-id="23cbb-110">questionId</span></span>](kasclient.kasquestionresult.md#questionid)
* [<span data-ttu-id="23cbb-111">questionTitle</span><span class="sxs-lookup"><span data-stu-id="23cbb-111">questionTitle</span></span>](kasclient.kasquestionresult.md#questiontitle)
* [<span data-ttu-id="23cbb-112">questiontype</span><span class="sxs-lookup"><span data-stu-id="23cbb-112">questionType</span></span>](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="23cbb-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="23cbb-113">Methods</span></span>

* [<span data-ttu-id="23cbb-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="23cbb-114">fromJSON</span></span>](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="23cbb-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23cbb-115">Properties</span></span>

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="23cbb-116">Frag-Nr.</span><span class="sxs-lookup"><span data-stu-id="23cbb-116">questionId</span></span>

<span data-ttu-id="23cbb-117">**● Frage**-Nr *`number`* .: = 0</span><span class="sxs-lookup"><span data-stu-id="23cbb-117">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="23cbb-118">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="23cbb-118">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="23cbb-119">questionTitle</span><span class="sxs-lookup"><span data-stu-id="23cbb-119">questionTitle</span></span>

<span data-ttu-id="23cbb-120">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="23cbb-120">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="23cbb-121">Der Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="23cbb-121">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="23cbb-122">questiontype</span><span class="sxs-lookup"><span data-stu-id="23cbb-122">questionType</span></span>

<span data-ttu-id="23cbb-123">**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="23cbb-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="23cbb-124">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="23cbb-124">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="23cbb-125">Methoden</span><span class="sxs-lookup"><span data-stu-id="23cbb-125">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="23cbb-126">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="23cbb-126">`<Static>` fromJSON</span></span>

<span data-ttu-id="23cbb-127">▸ **fromJSON**(Object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="23cbb-127">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="23cbb-128">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="23cbb-128">**Parameters:**</span></span>

| <span data-ttu-id="23cbb-129">Name</span><span class="sxs-lookup"><span data-stu-id="23cbb-129">Name</span></span> | <span data-ttu-id="23cbb-130">Typ</span><span class="sxs-lookup"><span data-stu-id="23cbb-130">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="23cbb-131">Objekt</span><span class="sxs-lookup"><span data-stu-id="23cbb-131">object</span></span> | `any` |

<span data-ttu-id="23cbb-132">**Gibt Folgendes zurück:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="23cbb-132">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

