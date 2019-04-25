<span data-ttu-id="977c4-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="977c4-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span></span>

# <a name="class-kasattachmentlistquestionresult"></a><span data-ttu-id="977c4-102">Klasse: KASAttachmentListQuestionResult</span><span class="sxs-lookup"><span data-stu-id="977c4-102">Class: KASAttachmentListQuestionResult</span></span>

<span data-ttu-id="977c4-103">Dieses Modell enthält Daten für jede Antwort auf eine Frage zum Anlagen Listentyp.</span><span class="sxs-lookup"><span data-stu-id="977c4-103">This model contains data for every response to an Attachment List Type question.</span></span>
## <a name="hierarchy"></a><span data-ttu-id="977c4-104">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="977c4-104">Hierarchy</span></span>

 [<span data-ttu-id="977c4-105">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="977c4-105">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="977c4-106">**↳ KASAttachmentListQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="977c4-106">**↳ KASAttachmentListQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="977c4-107">Index </span><span class="sxs-lookup"><span data-stu-id="977c4-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="977c4-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="977c4-108">Properties</span></span>

* [<span data-ttu-id="977c4-109">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="977c4-109">attachmentListType</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [<span data-ttu-id="977c4-110">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="977c4-110">attachmentsResponseJSONStrings</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [<span data-ttu-id="977c4-111">Frag-Nr.</span><span class="sxs-lookup"><span data-stu-id="977c4-111">questionId</span></span>](kasclient.kasattachmentlistquestionresult.md#questionid)
* [<span data-ttu-id="977c4-112">questionTitle</span><span class="sxs-lookup"><span data-stu-id="977c4-112">questionTitle</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [<span data-ttu-id="977c4-113">questiontype</span><span class="sxs-lookup"><span data-stu-id="977c4-113">questionType</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [<span data-ttu-id="977c4-114">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="977c4-114">timeStamps</span></span>](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [<span data-ttu-id="977c4-115">userInfo</span><span class="sxs-lookup"><span data-stu-id="977c4-115">userInfo</span></span>](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a><span data-ttu-id="977c4-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="977c4-116">Methods</span></span>

* [<span data-ttu-id="977c4-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="977c4-117">fromJSON</span></span>](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="977c4-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="977c4-118">Properties</span></span>

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a><span data-ttu-id="977c4-119">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="977c4-119">attachmentListType</span></span>

<span data-ttu-id="977c4-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType. Generic</span><span class="sxs-lookup"><span data-stu-id="977c4-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* =  AttachmentListResponseType.GENERIC</span></span>

<span data-ttu-id="977c4-121">attachmentListType: enthält den Typ der Antwort der Anlagenliste.</span><span class="sxs-lookup"><span data-stu-id="977c4-121">attachmentListType: contains the type of the attachment list response</span></span>

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a><span data-ttu-id="977c4-122">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="977c4-122">attachmentsResponseJSONStrings</span></span>

<span data-ttu-id="977c4-123">**● attachmentsResponseJSONStrings**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="977c4-123">**● attachmentsResponseJSONStrings**: *`string`[]* =  []</span></span>

<span data-ttu-id="977c4-124">attachmentsResponseJSONStrings: enthält die Liste der Anlagen, die jeder Antwort als JSON-Zeichenfolge entspricht, die in der questionIdToAnswerMap direkt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="977c4-124">attachmentsResponseJSONStrings: contains the list of attachments corresponding to every response as a JSON string which is directly available in the questionIdToAnswerMap.</span></span>

___

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="977c4-125">Frag-Nr.</span><span class="sxs-lookup"><span data-stu-id="977c4-125">questionId</span></span>

<span data-ttu-id="977c4-126">**● Frage**-Nr *`number`* .: = 0</span><span class="sxs-lookup"><span data-stu-id="977c4-126">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="977c4-127">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="977c4-127">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="977c4-128">questionTitle</span><span class="sxs-lookup"><span data-stu-id="977c4-128">questionTitle</span></span>

<span data-ttu-id="977c4-129">**● questionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="977c4-129">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="977c4-130">Der Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="977c4-130">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="977c4-131">questiontype</span><span class="sxs-lookup"><span data-stu-id="977c4-131">questionType</span></span>

<span data-ttu-id="977c4-132">**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None</span><span class="sxs-lookup"><span data-stu-id="977c4-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="977c4-133">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="977c4-133">Type of the question</span></span>

___

<a id="timestamps"></a>

###  <a name="timestamps"></a><span data-ttu-id="977c4-134">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="977c4-134">timeStamps</span></span>

<span data-ttu-id="977c4-135">**● Zeitstempel**: \* `string`[]\* = []</span><span class="sxs-lookup"><span data-stu-id="977c4-135">**● timeStamps**: *`string`[]* =  []</span></span>

<span data-ttu-id="977c4-136">Timestamps: enthält die Antwortzeit Stempel für jede Antwort.</span><span class="sxs-lookup"><span data-stu-id="977c4-136">timeStamps: contains the response timestamps for every response.</span></span>

___

<a id="userinfo"></a>

###  <a name="userinfo"></a><span data-ttu-id="977c4-137">userInfo</span><span class="sxs-lookup"><span data-stu-id="977c4-137">userInfo</span></span>

<span data-ttu-id="977c4-138">**●**info info: \* [KASUser](kasclient.kasuser.md)[]\* = []</span><span class="sxs-lookup"><span data-stu-id="977c4-138">**● userInfo**: *[KASUser](kasclient.kasuser.md)[]* =  []</span></span>

<span data-ttu-id="977c4-139">Benutzerinfo: enthält Instanzen von KASUser mit Details für den Beklagten für die jeweilige Antwort, sodass der Name und das Profilbild des Befragten angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="977c4-139">userInfo: contains instances of KASUser with details for the respondent for the particular response so that we can show the name and profile picture of the respondent.</span></span>

___

## <a name="methods"></a><span data-ttu-id="977c4-140">Methoden</span><span class="sxs-lookup"><span data-stu-id="977c4-140">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="977c4-141">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="977c4-141">`<Static>` fromJSON</span></span>

<span data-ttu-id="977c4-142">▸ **fromJSON**(Object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="977c4-142">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="977c4-143">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="977c4-143">**Parameters:**</span></span>

| <span data-ttu-id="977c4-144">Name</span><span class="sxs-lookup"><span data-stu-id="977c4-144">Name</span></span> | <span data-ttu-id="977c4-145">Typ</span><span class="sxs-lookup"><span data-stu-id="977c4-145">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="977c4-146">Objekt</span><span class="sxs-lookup"><span data-stu-id="977c4-146">object</span></span> | `any` |

<span data-ttu-id="977c4-147">**Gibt Folgendes zurück:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="977c4-147">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

