---
ms.openlocfilehash: e2ff630472614067d27e76e75b42a4845fd08534
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728046"
---
<span data-ttu-id="78739-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="78739-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormSummaryForGroup](../classes/kasclient.kasformsummaryforgroup.md)</span></span>

# <a name="class-kasformsummaryforgroup"></a><span data-ttu-id="78739-102">Klasse: KASFormSummaryForGroup</span><span class="sxs-lookup"><span data-stu-id="78739-102">Class: KASFormSummaryForGroup</span></span>

## <a name="hierarchy"></a><span data-ttu-id="78739-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="78739-103">Hierarchy</span></span>

<span data-ttu-id="78739-104">**KASFormSummaryForGroup**</span><span class="sxs-lookup"><span data-stu-id="78739-104">**KASFormSummaryForGroup**</span></span>

## <a name="index"></a><span data-ttu-id="78739-105">Index </span><span class="sxs-lookup"><span data-stu-id="78739-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="78739-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78739-106">Properties</span></span>

* [<span data-ttu-id="78739-107">Cursor</span><span class="sxs-lookup"><span data-stu-id="78739-107">cursor</span></span>](kasclient.kasformsummaryforgroup.md#cursor)
* [<span data-ttu-id="78739-108">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="78739-108">directMemberResponses</span></span>](kasclient.kasformsummaryforgroup.md#directmemberresponses)
* [<span data-ttu-id="78739-109">responderCount</span><span class="sxs-lookup"><span data-stu-id="78739-109">responderCount</span></span>](kasclient.kasformsummaryforgroup.md#respondercount)
* [<span data-ttu-id="78739-110">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="78739-110">subgroupSummary</span></span>](kasclient.kasformsummaryforgroup.md#subgroupsummary)
* [<span data-ttu-id="78739-111">targetCount</span><span class="sxs-lookup"><span data-stu-id="78739-111">targetCount</span></span>](kasclient.kasformsummaryforgroup.md#targetcount)
### <a name="methods"></a><span data-ttu-id="78739-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="78739-112">Methods</span></span>

* [<span data-ttu-id="78739-113">fromJSON</span><span class="sxs-lookup"><span data-stu-id="78739-113">fromJSON</span></span>](kasclient.kasformsummaryforgroup.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="78739-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78739-114">Properties</span></span>

<a id="cursor"></a>

###  <a name="cursor"></a><span data-ttu-id="78739-115">Cursor</span><span class="sxs-lookup"><span data-stu-id="78739-115">cursor</span></span>

<span data-ttu-id="78739-116">**● Cursor**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="78739-116">**● cursor**: *`string`* = ""</span></span>

___

<a id="directmemberresponses"></a>

###  <a name="directmemberresponses"></a><span data-ttu-id="78739-117">directMemberResponses</span><span class="sxs-lookup"><span data-stu-id="78739-117">directMemberResponses</span></span>

<span data-ttu-id="78739-118">**● DirectMemberResponses**: \* `KASActionInstanceResponse`[]\* =]</span><span class="sxs-lookup"><span data-stu-id="78739-118">**● directMemberResponses**: *`KASActionInstanceResponse`[]* =  []</span></span>

<span data-ttu-id="78739-119">Beispiel für Gruppe zusammenfassenden {"c": "125955414", "Rdc": 3, "Rs": \[ {"Id": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "entfernen": "0a228aee-c5c0-4dc5-bca0-42a634474e2b@1", "Rs": {"0": "Jbbl", "1": "1540980866017", "2": "{"Lt":"Lg"0:0,"Acc" : 0, "n": "","Ty": 0} "}}, {"Id":"41e589cf-ad48-46b9-9290-786bf64cd599","n":"SRK","entfernen":"13dfa760-df77-4c88-a9f6-f34a76136439@1","Rs": {"0":"Gnuk","1":"1540981299094","2":" {"Lt": "Lg" 0:0, "Acc": 0, "n": "","Ty": 0} "}} \],"Sgs": {" 0c6207fc-39ce-4b74-b420-db2d52f2cd08@1 ": {"n":"Rdc"null: 1,"Tc": 6}},"Tc": 6}</span><span class="sxs-lookup"><span data-stu-id="78739-119">Sample summary for group { "c": "125955414", "rdc": 3, "rs": \[ { "id": "5a1d8f15-79b8-4cd5-a497-a5caff979b74", "n": "ABC", "rid": "0a228aee-c5c0-4dc5-bca0-42a634474e2b@1", "rs": { "0": "Jbbl", "1": "1540980866017", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } }, { "id": "41e589cf-ad48-46b9-9290-786bf64cd599", "n": "SRK", "rid": "13dfa760-df77-4c88-a9f6-f34a76136439@1", "rs": { "0": "Gnuk", "1": "1540981299094", "2": "{"lt":0,"lg":0,"acc":0,"n":"","ty":0}" } } \], "sgs": { "0c6207fc-39ce-4b74-b420-db2d52f2cd08@1": { "n": null, "rdc": 1, "tc": 6 } }, "tc": 6 }</span></span>

___

<a id="respondercount"></a>

###  <a name="respondercount"></a><span data-ttu-id="78739-120">responderCount</span><span class="sxs-lookup"><span data-stu-id="78739-120">responderCount</span></span>

<span data-ttu-id="78739-121">**● ResponderCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="78739-121">**● responderCount**: *`number`* = 0</span></span>

___

<a id="subgroupsummary"></a>

###  <a name="subgroupsummary"></a><span data-ttu-id="78739-122">subgroupSummary</span><span class="sxs-lookup"><span data-stu-id="78739-122">subgroupSummary</span></span>

<span data-ttu-id="78739-123">**● SubgroupSummary**:*`object`*</span><span class="sxs-lookup"><span data-stu-id="78739-123">**● subgroupSummary**: *`object`*</span></span>

#### <a name="type-declaration"></a><span data-ttu-id="78739-124">Typdeklaration</span><span class="sxs-lookup"><span data-stu-id="78739-124">Type declaration</span></span>

___

<a id="targetcount"></a>

###  <a name="targetcount"></a><span data-ttu-id="78739-125">targetCount</span><span class="sxs-lookup"><span data-stu-id="78739-125">targetCount</span></span>

<span data-ttu-id="78739-126">**● TargetCount**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="78739-126">**● targetCount**: *`number`* = 0</span></span>

___

## <a name="methods"></a><span data-ttu-id="78739-127">Methoden</span><span class="sxs-lookup"><span data-stu-id="78739-127">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="78739-128">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="78739-128">`<Static>` fromJSON</span></span>

<span data-ttu-id="78739-129">▸ **FromJSON**(Objekt: *`any`*): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="78739-129">▸ **fromJSON**(object: *`any`*): [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

<span data-ttu-id="78739-130">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="78739-130">**Parameters:**</span></span>

| <span data-ttu-id="78739-131">Name</span><span class="sxs-lookup"><span data-stu-id="78739-131">Name</span></span> | <span data-ttu-id="78739-132">Typ</span><span class="sxs-lookup"><span data-stu-id="78739-132">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="78739-133">object</span><span class="sxs-lookup"><span data-stu-id="78739-133">object</span></span> | `any` |

<span data-ttu-id="78739-134">**Gibt:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span><span class="sxs-lookup"><span data-stu-id="78739-134">**Returns:** [KASFormSummaryForGroup](kasclient.kasformsummaryforgroup.md)</span></span>

___

