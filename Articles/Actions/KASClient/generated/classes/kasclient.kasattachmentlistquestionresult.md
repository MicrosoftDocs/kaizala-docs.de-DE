---
ms.openlocfilehash: 84017de85cac36d49be86fe3a7a2aca9bb9b4d34
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728068"
---
<span data-ttu-id="8c7e9-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c7e9-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)</span></span>

# <a name="class-kasattachmentlistquestionresult"></a><span data-ttu-id="8c7e9-102">Klasse: KASAttachmentListQuestionResult</span><span class="sxs-lookup"><span data-stu-id="8c7e9-102">Class: KASAttachmentListQuestionResult</span></span>

<span data-ttu-id="8c7e9-103">Dieses Modell enthält Daten für jede Antwort auf eine Frage Listentyp Anlage.</span><span class="sxs-lookup"><span data-stu-id="8c7e9-103">This model contains data for every response to an Attachment List Type question.</span></span>
## <a name="hierarchy"></a><span data-ttu-id="8c7e9-104">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="8c7e9-104">Hierarchy</span></span>

 [<span data-ttu-id="8c7e9-105">KASQuestionResult</span><span class="sxs-lookup"><span data-stu-id="8c7e9-105">KASQuestionResult</span></span>](kasclient.kasquestionresult.md)

<span data-ttu-id="8c7e9-106">**↳ KASAttachmentListQuestionResult**</span><span class="sxs-lookup"><span data-stu-id="8c7e9-106">**↳ KASAttachmentListQuestionResult**</span></span>

## <a name="index"></a><span data-ttu-id="8c7e9-107">Index </span><span class="sxs-lookup"><span data-stu-id="8c7e9-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="8c7e9-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c7e9-108">Properties</span></span>

* [<span data-ttu-id="8c7e9-109">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="8c7e9-109">attachmentListType</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [<span data-ttu-id="8c7e9-110">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="8c7e9-110">attachmentsResponseJSONStrings</span></span>](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [<span data-ttu-id="8c7e9-111">questionId</span><span class="sxs-lookup"><span data-stu-id="8c7e9-111">questionId</span></span>](kasclient.kasattachmentlistquestionresult.md#questionid)
* [<span data-ttu-id="8c7e9-112">questionTitle</span><span class="sxs-lookup"><span data-stu-id="8c7e9-112">questionTitle</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [<span data-ttu-id="8c7e9-113">questionType</span><span class="sxs-lookup"><span data-stu-id="8c7e9-113">questionType</span></span>](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [<span data-ttu-id="8c7e9-114">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="8c7e9-114">timeStamps</span></span>](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [<span data-ttu-id="8c7e9-115">userInfo</span><span class="sxs-lookup"><span data-stu-id="8c7e9-115">userInfo</span></span>](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a><span data-ttu-id="8c7e9-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="8c7e9-116">Methods</span></span>

* [<span data-ttu-id="8c7e9-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="8c7e9-117">fromJSON</span></span>](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="8c7e9-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c7e9-118">Properties</span></span>

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a><span data-ttu-id="8c7e9-119">attachmentListType</span><span class="sxs-lookup"><span data-stu-id="8c7e9-119">attachmentListType</span></span>

<span data-ttu-id="8c7e9-120">**● AttachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType.GENERIC</span><span class="sxs-lookup"><span data-stu-id="8c7e9-120">**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* =  AttachmentListResponseType.GENERIC</span></span>

<span data-ttu-id="8c7e9-121">AttachmentListType: enthält den Typ der Anlage Liste Antwort</span><span class="sxs-lookup"><span data-stu-id="8c7e9-121">attachmentListType: contains the type of the attachment list response</span></span>

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a><span data-ttu-id="8c7e9-122">attachmentsResponseJSONStrings</span><span class="sxs-lookup"><span data-stu-id="8c7e9-122">attachmentsResponseJSONStrings</span></span>

<span data-ttu-id="8c7e9-123">**● AttachmentsResponseJSONStrings**: \* `string`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="8c7e9-123">**● attachmentsResponseJSONStrings**: *`string`[]* =  []</span></span>

<span data-ttu-id="8c7e9-124">AttachmentsResponseJSONStrings: enthält die Liste der Anlagen, die jeder Antwort als eine JSON-Zeichenfolge, die direkt in der QuestionIdToAnswerMap verfügbar ist, entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c7e9-124">attachmentsResponseJSONStrings: contains the list of attachments corresponding to every response as a JSON string which is directly available in the questionIdToAnswerMap.</span></span>

___

<a id="questionid"></a>

###  <a name="questionid"></a><span data-ttu-id="8c7e9-125">questionId</span><span class="sxs-lookup"><span data-stu-id="8c7e9-125">questionId</span></span>

<span data-ttu-id="8c7e9-126">**● QuestionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="8c7e9-126">**● questionId**: *`number`* = 0</span></span>

<span data-ttu-id="8c7e9-127">Index der Frage</span><span class="sxs-lookup"><span data-stu-id="8c7e9-127">Index of the question</span></span>

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a><span data-ttu-id="8c7e9-128">questionTitle</span><span class="sxs-lookup"><span data-stu-id="8c7e9-128">questionTitle</span></span>

<span data-ttu-id="8c7e9-129">**● QuestionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8c7e9-129">**● questionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="8c7e9-130">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="8c7e9-130">Title of the question</span></span>

___

<a id="questiontype"></a>

###  <a name="questiontype"></a><span data-ttu-id="8c7e9-131">questionType</span><span class="sxs-lookup"><span data-stu-id="8c7e9-131">questionType</span></span>

<span data-ttu-id="8c7e9-132">**● QuestionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="8c7e9-132">**● questionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="8c7e9-133">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="8c7e9-133">Type of the question</span></span>

___

<a id="timestamps"></a>

###  <a name="timestamps"></a><span data-ttu-id="8c7e9-134">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="8c7e9-134">timeStamps</span></span>

<span data-ttu-id="8c7e9-135">**● Zeitstempel**: \* `string`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="8c7e9-135">**● timeStamps**: *`string`[]* =  []</span></span>

<span data-ttu-id="8c7e9-136">Zeitstempel: der Zeitstempel der Antwort für jede Antwort enthält.</span><span class="sxs-lookup"><span data-stu-id="8c7e9-136">timeStamps: contains the response timestamps for every response.</span></span>

___

<a id="userinfo"></a>

###  <a name="userinfo"></a><span data-ttu-id="8c7e9-137">userInfo</span><span class="sxs-lookup"><span data-stu-id="8c7e9-137">userInfo</span></span>

<span data-ttu-id="8c7e9-138">**● UserInfo**: \* [KASUser](kasclient.kasuser.md)[]\* =]</span><span class="sxs-lookup"><span data-stu-id="8c7e9-138">**● userInfo**: *[KASUser](kasclient.kasuser.md)[]* =  []</span></span>

<span data-ttu-id="8c7e9-139">UserInfo: enthält die Instanzen von KASUser mit Details für die Teilnehmer für die bestimmten Antwort, damit das Bild Name und Profil des Befragten angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="8c7e9-139">userInfo: contains instances of KASUser with details for the respondent for the particular response so that we can show the name and profile picture of the respondent.</span></span>

___

## <a name="methods"></a><span data-ttu-id="8c7e9-140">Methoden</span><span class="sxs-lookup"><span data-stu-id="8c7e9-140">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="8c7e9-141">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="8c7e9-141">`<Static>` fromJSON</span></span>

<span data-ttu-id="8c7e9-142">▸ **FromJSON**(Objekt: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c7e9-142">▸ **fromJSON**(object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

<span data-ttu-id="8c7e9-143">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="8c7e9-143">**Parameters:**</span></span>

| <span data-ttu-id="8c7e9-144">Name</span><span class="sxs-lookup"><span data-stu-id="8c7e9-144">Name</span></span> | <span data-ttu-id="8c7e9-145">Typ</span><span class="sxs-lookup"><span data-stu-id="8c7e9-145">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="8c7e9-146">object</span><span class="sxs-lookup"><span data-stu-id="8c7e9-146">object</span></span> | `any` |

<span data-ttu-id="8c7e9-147">**Gibt:** [KASQuestionResult](kasclient.kasquestionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c7e9-147">**Returns:** [KASQuestionResult](kasclient.kasquestionresult.md)</span></span>

___

