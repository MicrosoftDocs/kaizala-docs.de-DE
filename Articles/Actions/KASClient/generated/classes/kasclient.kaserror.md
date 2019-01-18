---
ms.openlocfilehash: fb1ab90d11725ffb657738e090e9e83baee6b886
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728086"
---
<span data-ttu-id="74ad9-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="74ad9-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)</span></span>

# <a name="class-kaserror"></a><span data-ttu-id="74ad9-102">Klasse: KASError</span><span class="sxs-lookup"><span data-stu-id="74ad9-102">Class: KASError</span></span>

## <a name="hierarchy"></a><span data-ttu-id="74ad9-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="74ad9-103">Hierarchy</span></span>

<span data-ttu-id="74ad9-104">**KASError**</span><span class="sxs-lookup"><span data-stu-id="74ad9-104">**KASError**</span></span>

## <a name="index"></a><span data-ttu-id="74ad9-105">Index </span><span class="sxs-lookup"><span data-stu-id="74ad9-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="74ad9-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74ad9-106">Properties</span></span>

* [<span data-ttu-id="74ad9-107">description</span><span class="sxs-lookup"><span data-stu-id="74ad9-107">description</span></span>](kasclient.kaserror.md#description)
* [<span data-ttu-id="74ad9-108">errorCode</span><span class="sxs-lookup"><span data-stu-id="74ad9-108">errorCode</span></span>](kasclient.kaserror.md#errorcode)
### <a name="methods"></a><span data-ttu-id="74ad9-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="74ad9-109">Methods</span></span>

* [<span data-ttu-id="74ad9-110">fromString</span><span class="sxs-lookup"><span data-stu-id="74ad9-110">fromString</span></span>](kasclient.kaserror.md#fromstring)

---

## <a name="properties"></a><span data-ttu-id="74ad9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74ad9-111">Properties</span></span>

<a id="description"></a>

###  <a name="description"></a><span data-ttu-id="74ad9-112">description</span><span class="sxs-lookup"><span data-stu-id="74ad9-112">description</span></span>

<span data-ttu-id="74ad9-113">**● Beschreibung**: *`String`* = ""</span><span class="sxs-lookup"><span data-stu-id="74ad9-113">**● description**: *`String`* = ""</span></span>

___

<a id="errorcode"></a>

###  <a name="errorcode"></a><span data-ttu-id="74ad9-114">errorCode</span><span class="sxs-lookup"><span data-stu-id="74ad9-114">errorCode</span></span>

<span data-ttu-id="74ad9-115">**● ErrorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* = KASErrorCode.NONE</span><span class="sxs-lookup"><span data-stu-id="74ad9-115">**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* =  KASErrorCode.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="74ad9-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="74ad9-116">Methods</span></span>

<a id="fromstring"></a>

### <a name="static-fromstring"></a><span data-ttu-id="74ad9-117">`<Static>`fromString</span><span class="sxs-lookup"><span data-stu-id="74ad9-117">`<Static>` fromString</span></span>

<span data-ttu-id="74ad9-118">▸ **FromString**(StringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="74ad9-118">▸ **fromString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)</span></span>

<span data-ttu-id="74ad9-119">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="74ad9-119">**Parameters:**</span></span>

| <span data-ttu-id="74ad9-120">Name</span><span class="sxs-lookup"><span data-stu-id="74ad9-120">Name</span></span> | <span data-ttu-id="74ad9-121">Typ</span><span class="sxs-lookup"><span data-stu-id="74ad9-121">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="74ad9-122">stringifyError</span><span class="sxs-lookup"><span data-stu-id="74ad9-122">stringifyError</span></span> | `string` |

<span data-ttu-id="74ad9-123">**Gibt:** [KASError](kasclient.kaserror.md)</span><span class="sxs-lookup"><span data-stu-id="74ad9-123">**Returns:** [KASError](kasclient.kaserror.md)</span></span>

___

