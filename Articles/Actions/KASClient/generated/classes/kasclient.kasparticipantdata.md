<span data-ttu-id="3e160-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASParticipantData](../classes/kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="3e160-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASParticipantData](../classes/kasclient.kasparticipantdata.md)</span></span>

# <a name="class-kasparticipantdata"></a><span data-ttu-id="3e160-102">Klasse: KASParticipantData</span><span class="sxs-lookup"><span data-stu-id="3e160-102">Class: KASParticipantData</span></span>

<span data-ttu-id="3e160-103">Definiert die Eigenschaften eines Unterhaltungs Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="3e160-103">Defines properties of a conversation participant</span></span>
## <a name="hierarchy"></a><span data-ttu-id="3e160-104">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="3e160-104">Hierarchy</span></span>

<span data-ttu-id="3e160-105">**KASParticipantData**</span><span class="sxs-lookup"><span data-stu-id="3e160-105">**KASParticipantData**</span></span>

## <a name="index"></a><span data-ttu-id="3e160-106">Index </span><span class="sxs-lookup"><span data-stu-id="3e160-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="3e160-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e160-107">Properties</span></span>

* [<span data-ttu-id="3e160-108">Teilnehmer-Nr.</span><span class="sxs-lookup"><span data-stu-id="3e160-108">participantId</span></span>](kasclient.kasparticipantdata.md#participantid)
* [<span data-ttu-id="3e160-109">participantRole</span><span class="sxs-lookup"><span data-stu-id="3e160-109">participantRole</span></span>](kasclient.kasparticipantdata.md#participantrole)
* [<span data-ttu-id="3e160-110">Teilnehmertyp</span><span class="sxs-lookup"><span data-stu-id="3e160-110">participantType</span></span>](kasclient.kasparticipantdata.md#participanttype)
### <a name="methods"></a><span data-ttu-id="3e160-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="3e160-111">Methods</span></span>

* [<span data-ttu-id="3e160-112">fromJSON</span><span class="sxs-lookup"><span data-stu-id="3e160-112">fromJSON</span></span>](kasclient.kasparticipantdata.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="3e160-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e160-113">Properties</span></span>

<a id="participantid"></a>

###  <a name="participantid"></a><span data-ttu-id="3e160-114">Teilnehmer-Nr.</span><span class="sxs-lookup"><span data-stu-id="3e160-114">participantId</span></span>

<span data-ttu-id="3e160-115">**● Teilnehmer**-Nr *`string`* .: = ""</span><span class="sxs-lookup"><span data-stu-id="3e160-115">**● participantId**: *`string`* = ""</span></span>

___

<a id="participantrole"></a>

###  <a name="participantrole"></a><span data-ttu-id="3e160-116">participantRole</span><span class="sxs-lookup"><span data-stu-id="3e160-116">participantRole</span></span>

<span data-ttu-id="3e160-117">**● participantRole**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole. None</span><span class="sxs-lookup"><span data-stu-id="3e160-117">**● participantRole**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* =  KASParticipantRole.NONE</span></span>

___

<a id="participanttype"></a>

###  <a name="participanttype"></a><span data-ttu-id="3e160-118">Teilnehmertyp</span><span class="sxs-lookup"><span data-stu-id="3e160-118">participantType</span></span>

<span data-ttu-id="3e160-119">**● Teilnehmertyp**: *[KASParticipantType](../enums/kasclient.kasparticipanttype.md)* = KASParticipantType. None</span><span class="sxs-lookup"><span data-stu-id="3e160-119">**● participantType**: *[KASParticipantType](../enums/kasclient.kasparticipanttype.md)* =  KASParticipantType.NONE</span></span>

___

## <a name="methods"></a><span data-ttu-id="3e160-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="3e160-120">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="3e160-121">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="3e160-121">`<Static>` fromJSON</span></span>

<span data-ttu-id="3e160-122">▸ **fromJSON**(Object: *`any`*): [KASParticipantData](kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="3e160-122">▸ **fromJSON**(object: *`any`*): [KASParticipantData](kasclient.kasparticipantdata.md)</span></span>

<span data-ttu-id="3e160-123">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="3e160-123">**Parameters:**</span></span>

| <span data-ttu-id="3e160-124">Name</span><span class="sxs-lookup"><span data-stu-id="3e160-124">Name</span></span> | <span data-ttu-id="3e160-125">Typ</span><span class="sxs-lookup"><span data-stu-id="3e160-125">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="3e160-126">Objekt</span><span class="sxs-lookup"><span data-stu-id="3e160-126">object</span></span> | `any` |

<span data-ttu-id="3e160-127">**Gibt Folgendes zurück:** [KASParticipantData](kasclient.kasparticipantdata.md)</span><span class="sxs-lookup"><span data-stu-id="3e160-127">**Returns:** [KASParticipantData](kasclient.kasparticipantdata.md)</span></span>

___

