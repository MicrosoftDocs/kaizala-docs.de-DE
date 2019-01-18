---
ms.openlocfilehash: 3b1a2cbce6762e7efcb4371db75d71596d651887
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728056"
---
<span data-ttu-id="2a093-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormReaction](../classes/kasclient.kasformreaction.md)</span><span class="sxs-lookup"><span data-stu-id="2a093-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormReaction](../classes/kasclient.kasformreaction.md)</span></span>

# <a name="class-kasformreaction"></a><span data-ttu-id="2a093-102">Klasse: KASFormReaction</span><span class="sxs-lookup"><span data-stu-id="2a093-102">Class: KASFormReaction</span></span>

## <a name="hierarchy"></a><span data-ttu-id="2a093-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="2a093-103">Hierarchy</span></span>

<span data-ttu-id="2a093-104">**KASFormReaction**</span><span class="sxs-lookup"><span data-stu-id="2a093-104">**KASFormReaction**</span></span>

## <a name="index"></a><span data-ttu-id="2a093-105">Index </span><span class="sxs-lookup"><span data-stu-id="2a093-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="2a093-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a093-106">Properties</span></span>

* [<span data-ttu-id="2a093-107">commentsCount</span><span class="sxs-lookup"><span data-stu-id="2a093-107">commentsCount</span></span>](kasclient.kasformreaction.md#commentscount)
* [<span data-ttu-id="2a093-108">didIComment</span><span class="sxs-lookup"><span data-stu-id="2a093-108">didIComment</span></span>](kasclient.kasformreaction.md#didicomment)
* [<span data-ttu-id="2a093-109">didILike</span><span class="sxs-lookup"><span data-stu-id="2a093-109">didILike</span></span>](kasclient.kasformreaction.md#didilike)
* [<span data-ttu-id="2a093-110">hideComments</span><span class="sxs-lookup"><span data-stu-id="2a093-110">hideComments</span></span>](kasclient.kasformreaction.md#hidecomments)
* [<span data-ttu-id="2a093-111">hideLikes</span><span class="sxs-lookup"><span data-stu-id="2a093-111">hideLikes</span></span>](kasclient.kasformreaction.md#hidelikes)
* [<span data-ttu-id="2a093-112">hideLikesDetails</span><span class="sxs-lookup"><span data-stu-id="2a093-112">hideLikesDetails</span></span>](kasclient.kasformreaction.md#hidelikesdetails)
* [<span data-ttu-id="2a093-113">likesCount</span><span class="sxs-lookup"><span data-stu-id="2a093-113">likesCount</span></span>](kasclient.kasformreaction.md#likescount)
### <a name="methods"></a><span data-ttu-id="2a093-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="2a093-114">Methods</span></span>

* [<span data-ttu-id="2a093-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="2a093-115">fromJSON</span></span>](kasclient.kasformreaction.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="2a093-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a093-116">Properties</span></span>

<a id="commentscount"></a>

###  <a name="commentscount"></a><span data-ttu-id="2a093-117">commentsCount</span><span class="sxs-lookup"><span data-stu-id="2a093-117">commentsCount</span></span>

<span data-ttu-id="2a093-118">**● CommentsCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="2a093-118">**● commentsCount**: *`number`* = 0</span></span>

<span data-ttu-id="2a093-119">Anzahl von Kommentaren für das Formular empfangen</span><span class="sxs-lookup"><span data-stu-id="2a093-119">Number of comments received for the form</span></span>

___

<a id="didicomment"></a>

###  <a name="didicomment"></a><span data-ttu-id="2a093-120">didIComment</span><span class="sxs-lookup"><span data-stu-id="2a093-120">didIComment</span></span>

<span data-ttu-id="2a093-121">**● DidIComment**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="2a093-121">**● didIComment**: *`boolean`* = false</span></span>

<span data-ttu-id="2a093-122">Gibt an, ob der aktuelle Benutzer bereits gefallen hat</span><span class="sxs-lookup"><span data-stu-id="2a093-122">Denotes whether the current user has already liked or not</span></span>

___

<a id="didilike"></a>

###  <a name="didilike"></a><span data-ttu-id="2a093-123">didILike</span><span class="sxs-lookup"><span data-stu-id="2a093-123">didILike</span></span>

<span data-ttu-id="2a093-124">**● DidILike**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="2a093-124">**● didILike**: *`boolean`* = false</span></span>

<span data-ttu-id="2a093-125">Gibt an, ob der aktuelle Benutzer bereits gefallen hat</span><span class="sxs-lookup"><span data-stu-id="2a093-125">Denotes whether the current user has already liked or not</span></span>

___

<a id="hidecomments"></a>

###  <a name="hidecomments"></a><span data-ttu-id="2a093-126">hideComments</span><span class="sxs-lookup"><span data-stu-id="2a093-126">hideComments</span></span>

<span data-ttu-id="2a093-127">**● HideComments**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="2a093-127">**● hideComments**: *`boolean`* = false</span></span>

<span data-ttu-id="2a093-128">Gibt an, ob Kommentare oder nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a093-128">Denotes whether to show comments or not</span></span>

___

<a id="hidelikes"></a>

###  <a name="hidelikes"></a><span data-ttu-id="2a093-129">hideLikes</span><span class="sxs-lookup"><span data-stu-id="2a093-129">hideLikes</span></span>

<span data-ttu-id="2a093-130">**● HideLikes**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="2a093-130">**● hideLikes**: *`boolean`* = false</span></span>

<span data-ttu-id="2a093-131">Gibt an, ob angezeigt oder nicht "gefällt mir"</span><span class="sxs-lookup"><span data-stu-id="2a093-131">Denotes whether to show likes or not</span></span>

___

<a id="hidelikesdetails"></a>

###  <a name="hidelikesdetails"></a><span data-ttu-id="2a093-132">hideLikesDetails</span><span class="sxs-lookup"><span data-stu-id="2a093-132">hideLikesDetails</span></span>

<span data-ttu-id="2a093-133">**● HideLikesDetails**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="2a093-133">**● hideLikesDetails**: *`boolean`* = false</span></span>

<span data-ttu-id="2a093-134">Gibt an, ob die anzuzeigenden Imeersive Ansicht oder nicht "gefällt mir"</span><span class="sxs-lookup"><span data-stu-id="2a093-134">Denotes whether to show likes imeersive view or not</span></span>

___

<a id="likescount"></a>

###  <a name="likescount"></a><span data-ttu-id="2a093-135">likesCount</span><span class="sxs-lookup"><span data-stu-id="2a093-135">likesCount</span></span>

<span data-ttu-id="2a093-136">**● LikesCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="2a093-136">**● likesCount**: *`number`* = 0</span></span>

<span data-ttu-id="2a093-137">Anzahl der "gefällt mir" für das Formular empfangen</span><span class="sxs-lookup"><span data-stu-id="2a093-137">Number of likes received for the form</span></span>

___

## <a name="methods"></a><span data-ttu-id="2a093-138">Methoden</span><span class="sxs-lookup"><span data-stu-id="2a093-138">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="2a093-139">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="2a093-139">`<Static>` fromJSON</span></span>

<span data-ttu-id="2a093-140">▸ **FromJSON**(Objekt: *`JSON`*): [KASFormReaction](kasclient.kasformreaction.md)</span><span class="sxs-lookup"><span data-stu-id="2a093-140">▸ **fromJSON**(object: *`JSON`*): [KASFormReaction](kasclient.kasformreaction.md)</span></span>

<span data-ttu-id="2a093-141">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="2a093-141">**Parameters:**</span></span>

| <span data-ttu-id="2a093-142">Name</span><span class="sxs-lookup"><span data-stu-id="2a093-142">Name</span></span> | <span data-ttu-id="2a093-143">Typ</span><span class="sxs-lookup"><span data-stu-id="2a093-143">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="2a093-144">object</span><span class="sxs-lookup"><span data-stu-id="2a093-144">object</span></span> | `JSON` |

<span data-ttu-id="2a093-145">**Gibt:** [KASFormReaction](kasclient.kasformreaction.md)</span><span class="sxs-lookup"><span data-stu-id="2a093-145">**Returns:** [KASFormReaction](kasclient.kasformreaction.md)</span></span>

___

