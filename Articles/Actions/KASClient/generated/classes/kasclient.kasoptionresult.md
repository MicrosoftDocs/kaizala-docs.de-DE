---
ms.openlocfilehash: c52e672a7e3356171388692054fcd1dc3cee5365
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728058"
---
<span data-ttu-id="846aa-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="846aa-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)</span></span>

# <a name="class-kasoptionresult"></a><span data-ttu-id="846aa-102">Klasse: KASOptionResult</span><span class="sxs-lookup"><span data-stu-id="846aa-102">Class: KASOptionResult</span></span>

## <a name="hierarchy"></a><span data-ttu-id="846aa-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="846aa-103">Hierarchy</span></span>

<span data-ttu-id="846aa-104">**KASOptionResult**</span><span class="sxs-lookup"><span data-stu-id="846aa-104">**KASOptionResult**</span></span>

## <a name="index"></a><span data-ttu-id="846aa-105">Index </span><span class="sxs-lookup"><span data-stu-id="846aa-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="846aa-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="846aa-106">Properties</span></span>

* [<span data-ttu-id="846aa-107">optionId</span><span class="sxs-lookup"><span data-stu-id="846aa-107">optionId</span></span>](kasclient.kasoptionresult.md#optionid)
* [<span data-ttu-id="846aa-108">optionTitle</span><span class="sxs-lookup"><span data-stu-id="846aa-108">optionTitle</span></span>](kasclient.kasoptionresult.md#optiontitle)
* [<span data-ttu-id="846aa-109">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="846aa-109">responderToResponseCount</span></span>](kasclient.kasoptionresult.md#respondertoresponsecount)
* [<span data-ttu-id="846aa-110">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="846aa-110">totalResponsesCount</span></span>](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a><span data-ttu-id="846aa-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="846aa-111">Methods</span></span>

* [<span data-ttu-id="846aa-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="846aa-112">fromJSON</span></span>](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="846aa-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="846aa-113">Properties</span></span>

<a id="optionid"></a>

###  <a name="optionid"></a><span data-ttu-id="846aa-114">optionId</span><span class="sxs-lookup"><span data-stu-id="846aa-114">optionId</span></span>

<span data-ttu-id="846aa-115">**● OptionId**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="846aa-115">**● optionId**: *`number`* = 0</span></span>

<span data-ttu-id="846aa-116">Index der option</span><span class="sxs-lookup"><span data-stu-id="846aa-116">Index of the option</span></span>

___

<a id="optiontitle"></a>

###  <a name="optiontitle"></a><span data-ttu-id="846aa-117">optionTitle</span><span class="sxs-lookup"><span data-stu-id="846aa-117">optionTitle</span></span>

<span data-ttu-id="846aa-118">**● OptionTitle**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="846aa-118">**● optionTitle**: *`string`* = ""</span></span>

<span data-ttu-id="846aa-119">Titel der option</span><span class="sxs-lookup"><span data-stu-id="846aa-119">Title of the option</span></span>

___

<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a><span data-ttu-id="846aa-120">responderToResponseCount</span><span class="sxs-lookup"><span data-stu-id="846aa-120">responderToResponseCount</span></span>

<span data-ttu-id="846aa-121">**● ResponderToResponseCount**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="846aa-121">**● responderToResponseCount**: *`object`*</span></span>

<span data-ttu-id="846aa-122">Eine Übersicht über die Benutzer-Ids für ihre Antwort Count Dictionary<UserId: string, ResponseCount: Number></span><span class="sxs-lookup"><span data-stu-id="846aa-122">A map of user ids against their response count Dictionary<UserId: string, ResponseCount: number></span></span>
#### <a name="type-declaration"></a><span data-ttu-id="846aa-123">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="846aa-123">Type declaration</span></span>

___

<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a><span data-ttu-id="846aa-124">totalResponsesCount</span><span class="sxs-lookup"><span data-stu-id="846aa-124">totalResponsesCount</span></span>

<span data-ttu-id="846aa-125">**● TotalResponsesCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="846aa-125">**● totalResponsesCount**: *`number`* = 0</span></span>

<span data-ttu-id="846aa-126">Wie viele diese Option ausgewählt haben</span><span class="sxs-lookup"><span data-stu-id="846aa-126">How many have chosen this option</span></span>

___

## <a name="methods"></a><span data-ttu-id="846aa-127">Methoden</span><span class="sxs-lookup"><span data-stu-id="846aa-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="846aa-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="846aa-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="846aa-129">▸ **FromJSON**(Objekt: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="846aa-129">▸ **fromJSON**(object: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

<span data-ttu-id="846aa-130">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="846aa-130">**Parameters:**</span></span>

| <span data-ttu-id="846aa-131">Name</span><span class="sxs-lookup"><span data-stu-id="846aa-131">Name</span></span> | <span data-ttu-id="846aa-132">Typ</span><span class="sxs-lookup"><span data-stu-id="846aa-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="846aa-133">object</span><span class="sxs-lookup"><span data-stu-id="846aa-133">object</span></span> | `any` |

<span data-ttu-id="846aa-134">**Gibt:** [KASOptionResult](kasclient.kasoptionresult.md)</span><span class="sxs-lookup"><span data-stu-id="846aa-134">**Returns:** [KASOptionResult](kasclient.kasoptionresult.md)</span></span>

___

