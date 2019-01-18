---
ms.openlocfilehash: bb410570ca61dd12bc05c9b5b2d9f0b154b2e7da
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728051"
---
<span data-ttu-id="c4876-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASParticipantData](../classes/kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="c4876-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASParticipantData](../classes/kasclient.kasparticipantdata.md)</span></span>

# <a name="class-kasparticipantdata"></a><span data-ttu-id="c4876-102">Klasse: KASParticipantData</span><span class="sxs-lookup"><span data-stu-id="c4876-102">Class: KASParticipantData</span></span>

<span data-ttu-id="c4876-103">Definiert die Eigenschaften eines Teilnehmers Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="c4876-103">Defines properties of a conversation participant</span></span>
## <a name="hierarchy"></a><span data-ttu-id="c4876-104">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="c4876-104">Hierarchy</span></span>

<span data-ttu-id="c4876-105">**KASParticipantData**</span><span class="sxs-lookup"><span data-stu-id="c4876-105">**KASParticipantData**</span></span>

## <a name="index"></a><span data-ttu-id="c4876-106">Index </span><span class="sxs-lookup"><span data-stu-id="c4876-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="c4876-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4876-107">Properties</span></span>

* [<span data-ttu-id="c4876-108">participantId</span><span class="sxs-lookup"><span data-stu-id="c4876-108">participantId</span></span>](kasclient.kasparticipantdata.md#participantid)
* [<span data-ttu-id="c4876-109">participantRole</span><span class="sxs-lookup"><span data-stu-id="c4876-109">participantRole</span></span>](kasclient.kasparticipantdata.md#participantrole)
* [<span data-ttu-id="c4876-110">participantType</span><span class="sxs-lookup"><span data-stu-id="c4876-110">participantType</span></span>](kasclient.kasparticipantdata.md#participanttype)
### <a name="methods"></a><span data-ttu-id="c4876-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4876-111">Methods</span></span>

* [<span data-ttu-id="c4876-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="c4876-112">fromJSON</span></span>](kasclient.kasparticipantdata.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="c4876-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4876-113">Properties</span></span>

<a id="participantid"></a>

###  <a name="participantid"></a><span data-ttu-id="c4876-114">participantId</span><span class="sxs-lookup"><span data-stu-id="c4876-114">participantId</span></span>

<span data-ttu-id="c4876-115">**● ParticipantId**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="c4876-115">**● participantId**: *`string`* = ""</span></span>

___

<a id="participantrole"></a>

###  <a name="participantrole"></a><span data-ttu-id="c4876-116">participantRole</span><span class="sxs-lookup"><span data-stu-id="c4876-116">participantRole</span></span>

<span data-ttu-id="c4876-117">**● ParticipantRole**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole.NONE</span><span class="sxs-lookup"><span data-stu-id="c4876-117">**● participantRole**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* =  KASParticipantRole.NONE</span></span>

___

<a id="participanttype"></a>

###  <a name="participanttype"></a><span data-ttu-id="c4876-118">participantType</span><span class="sxs-lookup"><span data-stu-id="c4876-118">participantType</span></span>

<span data-ttu-id="c4876-119">**● ParticipantType**: *[KASParticipantType](../enums/kasclient.kasparticipanttype.md)* = KASParticipantType.NONE</span><span class="sxs-lookup"><span data-stu-id="c4876-119">**● participantType**: *[KASParticipantType](../enums/kasclient.kasparticipanttype.md)* =  KASParticipantType.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="c4876-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4876-120">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="c4876-121">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="c4876-121">`<Static>` fromJSON</span></span>

<span data-ttu-id="c4876-122">▸ **FromJSON**(Objekt: *`any`*): [KASParticipantData](kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="c4876-122">▸ **fromJSON**(object: *`any`*): [KASParticipantData](kasclient.kasparticipantdata.md)</span></span>

<span data-ttu-id="c4876-123">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="c4876-123">**Parameters:**</span></span>

| <span data-ttu-id="c4876-124">Name</span><span class="sxs-lookup"><span data-stu-id="c4876-124">Name</span></span> | <span data-ttu-id="c4876-125">Typ</span><span class="sxs-lookup"><span data-stu-id="c4876-125">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="c4876-126">object</span><span class="sxs-lookup"><span data-stu-id="c4876-126">object</span></span> | `any` |

<span data-ttu-id="c4876-127">**Gibt:** [KASParticipantData](kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="c4876-127">**Returns:** [KASParticipantData](kasclient.kasparticipantdata.md)</span></span>

___

