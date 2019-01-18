---
ms.openlocfilehash: 84e9530593e8850a0cf354ae2e07c77e0b68db75
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728059"
---
<span data-ttu-id="8e423-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="8e423-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)</span></span>

# <a name="class-kasformresponse"></a><span data-ttu-id="8e423-102">Klasse: KASFormResponse</span><span class="sxs-lookup"><span data-stu-id="8e423-102">Class: KASFormResponse</span></span>

## <a name="hierarchy"></a><span data-ttu-id="8e423-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="8e423-103">Hierarchy</span></span>

<span data-ttu-id="8e423-104">**KASFormResponse**</span><span class="sxs-lookup"><span data-stu-id="8e423-104">**KASFormResponse**</span></span>

## <a name="index"></a><span data-ttu-id="8e423-105">Index </span><span class="sxs-lookup"><span data-stu-id="8e423-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="8e423-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e423-106">Properties</span></span>

* [<span data-ttu-id="8e423-107">groupId</span><span class="sxs-lookup"><span data-stu-id="8e423-107">groupId</span></span>](kasclient.kasformresponse.md#groupid)
* [<span data-ttu-id="8e423-108">groupName</span><span class="sxs-lookup"><span data-stu-id="8e423-108">groupName</span></span>](kasclient.kasformresponse.md#groupname)
* [<span data-ttu-id="8e423-109">id</span><span class="sxs-lookup"><span data-stu-id="8e423-109">id</span></span>](kasclient.kasformresponse.md#id)
* [<span data-ttu-id="8e423-110">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="8e423-110">questionToAnswerMap</span></span>](kasclient.kasformresponse.md#questiontoanswermap)
* [<span data-ttu-id="8e423-111">responderId</span><span class="sxs-lookup"><span data-stu-id="8e423-111">responderId</span></span>](kasclient.kasformresponse.md#responderid)
* [<span data-ttu-id="8e423-112">responderName</span><span class="sxs-lookup"><span data-stu-id="8e423-112">responderName</span></span>](kasclient.kasformresponse.md#respondername)
* [<span data-ttu-id="8e423-113">sendStatus</span><span class="sxs-lookup"><span data-stu-id="8e423-113">sendStatus</span></span>](kasclient.kasformresponse.md#sendstatus)
* [<span data-ttu-id="8e423-114"><ui>sendTime</ui></span><span class="sxs-lookup"><span data-stu-id="8e423-114">sendTime</span></span>](kasclient.kasformresponse.md#sendtime)
* [<span data-ttu-id="8e423-115">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="8e423-115">serverToLocalAssetUrlMap</span></span>](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a><span data-ttu-id="8e423-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="8e423-116">Methods</span></span>

* [<span data-ttu-id="8e423-117">fromJSON</span><span class="sxs-lookup"><span data-stu-id="8e423-117">fromJSON</span></span>](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="8e423-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e423-118">Properties</span></span>

<a id="groupid"></a>

###  <a name="groupid"></a><span data-ttu-id="8e423-119">groupId</span><span class="sxs-lookup"><span data-stu-id="8e423-119">groupId</span></span>

<span data-ttu-id="8e423-120">**● GroupId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8e423-120">**● groupId**: *`string`* = ""</span></span>

<span data-ttu-id="8e423-121">Gruppen-id</span><span class="sxs-lookup"><span data-stu-id="8e423-121">Group id</span></span>

___

<a id="groupname"></a>

###  <a name="groupname"></a><span data-ttu-id="8e423-122">groupName</span><span class="sxs-lookup"><span data-stu-id="8e423-122">groupName</span></span>

<span data-ttu-id="8e423-123">**● GroupName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8e423-123">**● groupName**: *`string`* = ""</span></span>

<span data-ttu-id="8e423-124">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="8e423-124">Group Name</span></span>

___

<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="8e423-125">id</span><span class="sxs-lookup"><span data-stu-id="8e423-125">id</span></span>

<span data-ttu-id="8e423-126">**●-Id**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8e423-126">**● id**: *`string`* = ""</span></span>

<span data-ttu-id="8e423-127">Eine eindeutige Antwort-Id, die im Fall eines WAN-aktualisieren eine vorhandene Antwort erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e423-127">A unique response id, required in case of updating an existing response</span></span>

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a><span data-ttu-id="8e423-128">questionToAnswerMap</span><span class="sxs-lookup"><span data-stu-id="8e423-128">questionToAnswerMap</span></span>

<span data-ttu-id="8e423-129">**● QuestionToAnswerMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="8e423-129">**● questionToAnswerMap**: *`object`*</span></span>

<span data-ttu-id="8e423-130">Eine Zuordnung der Frage Id Dictionary<QuestionId beantworten: number, Antwort: String></span><span class="sxs-lookup"><span data-stu-id="8e423-130">A map of question id to answer Dictionary<QuestionId: number, Answer: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="8e423-131">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="8e423-131">Type declaration</span></span>

___

<a id="responderid"></a>

###  <a name="responderid"></a><span data-ttu-id="8e423-132">responderId</span><span class="sxs-lookup"><span data-stu-id="8e423-132">responderId</span></span>

<span data-ttu-id="8e423-133">**● ResponderId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8e423-133">**● responderId**: *`string`* = ""</span></span>

<span data-ttu-id="8e423-134">Responder-id</span><span class="sxs-lookup"><span data-stu-id="8e423-134">Responder id</span></span>

___

<a id="respondername"></a>

###  <a name="respondername"></a><span data-ttu-id="8e423-135">responderName</span><span class="sxs-lookup"><span data-stu-id="8e423-135">responderName</span></span>

<span data-ttu-id="8e423-136">**● ResponderName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="8e423-136">**● responderName**: *`string`* = ""</span></span>

<span data-ttu-id="8e423-137">Responder name</span><span class="sxs-lookup"><span data-stu-id="8e423-137">Responder name</span></span>

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a><span data-ttu-id="8e423-138">sendStatus</span><span class="sxs-lookup"><span data-stu-id="8e423-138">sendStatus</span></span>

<span data-ttu-id="8e423-139">**● SendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus.Unknown</span><span class="sxs-lookup"><span data-stu-id="8e423-139">**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* =  KASFormMessageSendStatus.Unknown</span></span>

<span data-ttu-id="8e423-140">Status der Antwort-Nachricht senden</span><span class="sxs-lookup"><span data-stu-id="8e423-140">Response message send status</span></span>

___

<a id="sendtime"></a>

###  <a name="sendtime"></a><span data-ttu-id="8e423-141">sendTime</span><span class="sxs-lookup"><span data-stu-id="8e423-141">sendTime</span></span>

<span data-ttu-id="8e423-142">**● SendTime**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="8e423-142">**● sendTime**: *`number`* = 0</span></span>

<span data-ttu-id="8e423-143">Antwortzeit senden</span><span class="sxs-lookup"><span data-stu-id="8e423-143">Response send time</span></span>

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a><span data-ttu-id="8e423-144">serverToLocalAssetUrlMap</span><span class="sxs-lookup"><span data-stu-id="8e423-144">serverToLocalAssetUrlMap</span></span>

<span data-ttu-id="8e423-145">**● ServerToLocalAssetUrlMap**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="8e423-145">**● serverToLocalAssetUrlMap**: *`object`*</span></span>

<span data-ttu-id="8e423-146">Eine Zuordnung für ServerUrl gegen localURL im aller Anlagen Bild für eine Antwort Dictionary<ServerUrl: string, localURL im: String></span><span class="sxs-lookup"><span data-stu-id="8e423-146">A map for serverUrl against localUrl of all the image attachments to a response Dictionary<ServerUrl: string, LocalUrl: string></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="8e423-147">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="8e423-147">Type declaration</span></span>

___

## <a name="methods"></a><span data-ttu-id="8e423-148">Methoden</span><span class="sxs-lookup"><span data-stu-id="8e423-148">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="8e423-149">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="8e423-149">`<Static>` fromJSON</span></span>

<span data-ttu-id="8e423-150">▸ **FromJSON**(Objekt: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="8e423-150">▸ **fromJSON**(object: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)</span></span>

<span data-ttu-id="8e423-151">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="8e423-151">**Parameters:**</span></span>

| <span data-ttu-id="8e423-152">Name</span><span class="sxs-lookup"><span data-stu-id="8e423-152">Name</span></span> | <span data-ttu-id="8e423-153">Typ</span><span class="sxs-lookup"><span data-stu-id="8e423-153">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="8e423-154">object</span><span class="sxs-lookup"><span data-stu-id="8e423-154">object</span></span> | `any` |

<span data-ttu-id="8e423-155">**Gibt:** [KASFormResponse](kasclient.kasformresponse.md)</span><span class="sxs-lookup"><span data-stu-id="8e423-155">**Returns:** [KASFormResponse](kasclient.kasformresponse.md)</span></span>

___

