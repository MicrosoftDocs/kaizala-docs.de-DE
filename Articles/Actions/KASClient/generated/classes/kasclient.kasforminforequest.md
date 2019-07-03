<span data-ttu-id="b61f5-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormInfoRequest](../classes/kasclient.kasforminforequest.md)</span><span class="sxs-lookup"><span data-stu-id="b61f5-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormInfoRequest](../classes/kasclient.kasforminforequest.md)</span></span>

# <a name="class-kasforminforequest"></a><span data-ttu-id="b61f5-102">Klasse: KASFormInfoRequest</span><span class="sxs-lookup"><span data-stu-id="b61f5-102">Class: KASFormInfoRequest</span></span>

<span data-ttu-id="b61f5-103">Dadurch wird die Anforderung für die KASClient. Form. fetchFormInfosAsync-API gekapselt.</span><span class="sxs-lookup"><span data-stu-id="b61f5-103">This encapsulates the request for KASClient.Form.fetchFormInfosAsync api.</span></span> <span data-ttu-id="b61f5-104">Diese API wird zum Abrufen von Aktionsinstanz-(oder Formular-) Infos für eine Action-Styl verwendet.</span><span class="sxs-lookup"><span data-stu-id="b61f5-104">This api is used to fetch Action instance (or form) infos for an Action pacakge</span></span>
## <a name="hierarchy"></a><span data-ttu-id="b61f5-105">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="b61f5-105">Hierarchy</span></span>

<span data-ttu-id="b61f5-106">**KASFormInfoRequest**</span><span class="sxs-lookup"><span data-stu-id="b61f5-106">**KASFormInfoRequest**</span></span>

## <a name="index"></a><span data-ttu-id="b61f5-107">Index </span><span class="sxs-lookup"><span data-stu-id="b61f5-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="b61f5-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b61f5-108">Properties</span></span>

* [<span data-ttu-id="b61f5-109">creatorId</span><span class="sxs-lookup"><span data-stu-id="b61f5-109">creatorId</span></span>](kasclient.kasforminforequest.md#creatorid)
* [<span data-ttu-id="b61f5-110">Cursor</span><span class="sxs-lookup"><span data-stu-id="b61f5-110">cursor</span></span>](kasclient.kasforminforequest.md#cursor)
* [<span data-ttu-id="b61f5-111">packageId</span><span class="sxs-lookup"><span data-stu-id="b61f5-111">packageId</span></span>](kasclient.kasforminforequest.md#packageid)
* [<span data-ttu-id="b61f5-112">scopeId</span><span class="sxs-lookup"><span data-stu-id="b61f5-112">scopeId</span></span>](kasclient.kasforminforequest.md#scopeid)

---

## <a name="properties"></a><span data-ttu-id="b61f5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b61f5-113">Properties</span></span>

<a id="creatorid"></a>

###  <a name="creatorid"></a><span data-ttu-id="b61f5-114">creatorId</span><span class="sxs-lookup"><span data-stu-id="b61f5-114">creatorId</span></span>

<span data-ttu-id="b61f5-115">**● creatorname**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b61f5-115">**● creatorId**: *`string`* = ""</span></span>

<span data-ttu-id="b61f5-116">Aktionsinstanz (oder Formular) Creator ID – optionales Feld</span><span class="sxs-lookup"><span data-stu-id="b61f5-116">Action instance (or form) creator id - optional field</span></span>

___
<a id="cursor"></a>

###  <a name="cursor"></a><span data-ttu-id="b61f5-117">Cursor</span><span class="sxs-lookup"><span data-stu-id="b61f5-117">cursor</span></span>

<span data-ttu-id="b61f5-118">**● Cursor**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b61f5-118">**● cursor**: *`string`* = ""</span></span>

<span data-ttu-id="b61f5-119">Cursor zum Abrufen von Antworten im Batchmodus</span><span class="sxs-lookup"><span data-stu-id="b61f5-119">Cursor to fetch responses in batch</span></span>

___
<a id="packageid"></a>

###  <a name="packageid"></a><span data-ttu-id="b61f5-120">packageId</span><span class="sxs-lookup"><span data-stu-id="b61f5-120">packageId</span></span>

<span data-ttu-id="b61f5-121">**● Packaged**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="b61f5-121">**● packageId**: *`string`* = ""</span></span>

<span data-ttu-id="b61f5-122">Aktionspaket-ID, deren Instanzen abgerufen werden müssen</span><span class="sxs-lookup"><span data-stu-id="b61f5-122">Action package id whose instances need to be fetched</span></span>

___
<a id="scopeid"></a>

###  <a name="scopeid"></a><span data-ttu-id="b61f5-123">scopeId</span><span class="sxs-lookup"><span data-stu-id="b61f5-123">scopeId</span></span>

<span data-ttu-id="b61f5-124">**● Bereichs**-Nr *`string`* : = ""</span><span class="sxs-lookup"><span data-stu-id="b61f5-124">**● scopeId**: *`string`* = ""</span></span>

<span data-ttu-id="b61f5-125">Bereichs-ID – Gruppen-ID für einzelnen/Gruppenbereich, Mandanten-ID für MANDANTENBEREICH, Benutzer-ID für Benutzerbereich</span><span class="sxs-lookup"><span data-stu-id="b61f5-125">Scope id - group id for Single/Group scope, tenant id for Tenant scope, user id for User scope</span></span>

___

