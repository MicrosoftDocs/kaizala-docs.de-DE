<span data-ttu-id="a6270-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a6270-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)</span></span>

# <a name="class-kasquestionresult"></a><span data-ttu-id="a6270-102">Klasse: KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="a6270-102">Class: KASQuestionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="a6270-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="a6270-103">Hierarchy</span></span>

<span data-ttu-id="a6270-104">**KASQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="a6270-104">**KASQuestionResult**</span></span>

<span data-ttu-id="a6270-105">↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a6270-105">↳  [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)</span></span>

<span data-ttu-id="a6270-106">↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a6270-106">↳  [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)</span></span>

<span data-ttu-id="a6270-107">↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a6270-107">↳  [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)</span></span>

## <a name="index"></a><span data-ttu-id="a6270-108">Index </span><span class="sxs-lookup"><span data-stu-id="a6270-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="a6270-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6270-109">Properties</span></span>

* [<span data-ttu-id="a6270-110">Fragen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6270-110">questionId</span></span>](kasclient.kasquestionresult.md#questionid)
* [<span data-ttu-id="a6270-111">questionTitle</span><span class="sxs-lookup"><span data-stu-id="a6270-111">questionTitle</span></span>](kasclient.kasquestionresult.md#questiontitle)
* [<span data-ttu-id="a6270-112">questiontype</span><span class="sxs-lookup"><span data-stu-id="a6270-112">questionType</span></span>](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a><span data-ttu-id="a6270-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="a6270-113">Methods</span></span>

* [<span data-ttu-id="a6270-114">fromJSON</span><span class="sxs-lookup"><span data-stu-id="a6270-114">fromJSON</span></span>](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="a6270-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6270-115">Properties</span></span>

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="a6270-116">Fragen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6270-116">questionId</span></span>

<span data-ttu-id="a6270-117">**● Frag**-Nr *`number`* : = 0</span><span class="sxs-lookup"><span data-stu-id="a6270-117">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="a6270-118">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="a6270-118">Index of the question</span></span>

___
<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="a6270-119">questionTitle</span><span class="sxs-lookup"><span data-stu-id="a6270-119">questionTitle</span></span>

<span data-ttu-id="a6270-120">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="a6270-120">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="a6270-121">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="a6270-121">Title of the question</span></span>

___
<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="a6270-122">questiontype</span><span class="sxs-lookup"><span data-stu-id="a6270-122">questionType</span></span>

<span data-ttu-id="a6270-123">**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="a6270-123">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="a6270-124">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="a6270-124">Type of the question</span></span>

___

## <a name="methods"></a><span data-ttu-id="a6270-125">Methoden</span><span class="sxs-lookup"><span data-stu-id="a6270-125">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="a6270-126">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="a6270-126">`<Static>` fromJSON</span></span>

<span data-ttu-id="a6270-127">▸- **fromJSON**(Objekt *`any`*:): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a6270-127">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="a6270-128">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="a6270-128">**Parameters:**</span></span>

| <span data-ttu-id="a6270-129">Name</span><span class="sxs-lookup"><span data-stu-id="a6270-129">Name</span></span> | <span data-ttu-id="a6270-130">Typ</span><span class="sxs-lookup"><span data-stu-id="a6270-130">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="a6270-131">Objekt</span><span class="sxs-lookup"><span data-stu-id="a6270-131">object</span></span> | `any` |

<span data-ttu-id="a6270-132">**Gibt Folgendes zurück:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a6270-132">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

