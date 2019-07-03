<span data-ttu-id="a330f-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a330f-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span></span>

# <a name="class-kasattachmentlistquestionresult"></a><span data-ttu-id="a330f-102">Klasse: KASAttachmentListQuestionResult</span><span class="sxs-lookup"><span data-stu-id="a330f-102">Class: KASAttachmentListQuestionResult</span></span>

<span data-ttu-id="a330f-103">Dieses Modell enthält Daten für jede Antwort auf eine Art von Anlagen Listentyp Frage.</span><span class="sxs-lookup"><span data-stu-id="a330f-103">This model contains data for every response to an Attachment List Type question.</span></span>
## <a name="hierarchy"></a><span data-ttu-id="a330f-104">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="a330f-104">Hierarchy</span></span>

 [<span data-ttu-id="a330f-105">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="a330f-105">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="a330f-106">**↳ KASAttachmentListQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="a330f-106">**↳ KASAttachmentListQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="a330f-107">Index </span><span class="sxs-lookup"><span data-stu-id="a330f-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="a330f-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a330f-108">Properties</span></span>

* [<span data-ttu-id="a330f-109">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="a330f-109">attachmentListType</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [<span data-ttu-id="a330f-110">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="a330f-110">attachmentsResponseJSONStrings</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [<span data-ttu-id="a330f-111">Fragen-Nr</span><span class="sxs-lookup"><span data-stu-id="a330f-111">questionId</span></span>](kasclient.kasattachmentlistquestionresult.md#questionid)
* [<span data-ttu-id="a330f-112">questionTitle</span><span class="sxs-lookup"><span data-stu-id="a330f-112">questionTitle</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [<span data-ttu-id="a330f-113">questiontype</span><span class="sxs-lookup"><span data-stu-id="a330f-113">questionType</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [<span data-ttu-id="a330f-114">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="a330f-114">timeStamps</span></span>](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [<span data-ttu-id="a330f-115">userInfo</span><span class="sxs-lookup"><span data-stu-id="a330f-115">userInfo</span></span>](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a><span data-ttu-id="a330f-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="a330f-116">Methods</span></span>

* [<span data-ttu-id="a330f-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="a330f-117">fromJSON</span></span>](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="a330f-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a330f-118">Properties</span></span>

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a><span data-ttu-id="a330f-119">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="a330f-119">attachmentListType</span></span>

<span data-ttu-id="a330f-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType. Generic</span><span class="sxs-lookup"><span data-stu-id="a330f-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* =  AttachmentListResponseType.GENERIC</span></span>

<span data-ttu-id="a330f-121">attachmentListType: enthält den Typ der Anlage Listen Antwort</span><span class="sxs-lookup"><span data-stu-id="a330f-121">attachmentListType: contains the type of the attachment list response</span></span>

___
<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a><span data-ttu-id="a330f-122">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="a330f-122">attachmentsResponseJSONStrings</span></span>

<span data-ttu-id="a330f-123">**● attachmentsResponseJSONStrings**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="a330f-123">**● attachmentsResponseJSONStrings**: *`string`[]* =  []</span></span>

<span data-ttu-id="a330f-124">attachmentsResponseJSONStrings: enthält die Liste der Anlagen, die jeder Antwort als JSON-Zeichenfolge entsprechen, die direkt im questionIdToAnswerMap verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a330f-124">attachmentsResponseJSONStrings: contains the list of attachments corresponding to every response as a JSON string which is directly available in the questionIdToAnswerMap.</span></span>

___
<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="a330f-125">Fragen-Nr</span><span class="sxs-lookup"><span data-stu-id="a330f-125">questionId</span></span>

<span data-ttu-id="a330f-126">**● Frag**-Nr *`number`* : = 0</span><span class="sxs-lookup"><span data-stu-id="a330f-126">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="a330f-127">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="a330f-127">Index of the question</span></span>

___
<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="a330f-128">questionTitle</span><span class="sxs-lookup"><span data-stu-id="a330f-128">questionTitle</span></span>

<span data-ttu-id="a330f-129">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="a330f-129">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="a330f-130">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="a330f-130">Title of the question</span></span>

___
<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="a330f-131">questiontype</span><span class="sxs-lookup"><span data-stu-id="a330f-131">questionType</span></span>

<span data-ttu-id="a330f-132">**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="a330f-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="a330f-133">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="a330f-133">Type of the question</span></span>

___
<a id="timestamps"></a>

###  <a name="timestamps"></a><span data-ttu-id="a330f-134">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="a330f-134">timeStamps</span></span>

<span data-ttu-id="a330f-135">**● Zeitstempel**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="a330f-135">**● timeStamps**: *`string`[]* =  []</span></span>

<span data-ttu-id="a330f-136">Timestamps: enthält die Antwortzeit Stempel für jede Antwort.</span><span class="sxs-lookup"><span data-stu-id="a330f-136">timeStamps: contains the response timestamps for every response.</span></span>

___
<a id="userinfo"></a>

###  <a name="userinfo"></a><span data-ttu-id="a330f-137">userInfo</span><span class="sxs-lookup"><span data-stu-id="a330f-137">userInfo</span></span>

<span data-ttu-id="a330f-138">**●**InfoInfo: \* [KASUser](kasclient.kasuser.md)[]\* = []</span><span class="sxs-lookup"><span data-stu-id="a330f-138">**● userInfo**: *[KASUser](kasclient.kasuser.md)[]* =  []</span></span>

<span data-ttu-id="a330f-139">Benutzername: enthält Instanzen von KASUser mit Details für den Teilnehmer für die jeweilige Antwort, sodass wir den Namen und das Profilbild des Befragten anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="a330f-139">userInfo: contains instances of KASUser with details for the respondent for the particular response so that we can show the name and profile picture of the respondent.</span></span>

___

## <a name="methods"></a><span data-ttu-id="a330f-140">Methoden</span><span class="sxs-lookup"><span data-stu-id="a330f-140">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="a330f-141">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="a330f-141">`<Static>` fromJSON</span></span>

<span data-ttu-id="a330f-142">▸- **fromJSON**(Objekt *`any`*:): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a330f-142">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="a330f-143">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="a330f-143">**Parameters:**</span></span>

| <span data-ttu-id="a330f-144">Name</span><span class="sxs-lookup"><span data-stu-id="a330f-144">Name</span></span> | <span data-ttu-id="a330f-145">Typ</span><span class="sxs-lookup"><span data-stu-id="a330f-145">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="a330f-146">Objekt</span><span class="sxs-lookup"><span data-stu-id="a330f-146">object</span></span> | `any` |

<span data-ttu-id="a330f-147">**Gibt Folgendes zurück:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a330f-147">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

