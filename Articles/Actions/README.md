---
ms.openlocfilehash: bcc9a8ad0b6aba1f52204730326cdc8e72b586e4
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727723"
---
# <a name="kaizala-actions"></a><span data-ttu-id="2c56b-101">Kaizala Aktionen</span><span class="sxs-lookup"><span data-stu-id="2c56b-101">Kaizala Actions</span></span>

## <a name="overview"></a><span data-ttu-id="2c56b-102">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2c56b-102">Overview</span></span>
<span data-ttu-id="2c56b-103">Kaizala Aktionen sind grundlegende 'Arbeitseinheiten', mit denen Benutzer in einem Unterhaltungskontext innerhalb Kaizala Arbeit vermitteln.</span><span class="sxs-lookup"><span data-stu-id="2c56b-103">Kaizala Actions are basic 'units of work' that help users get work done within a conversation context inside Kaizala.</span></span> <span data-ttu-id="2c56b-104">Einige dieser Aktionen wie Auftrag, Umfrage, Umfrage usw. sind gelieferten Out-of-the-Box und verfügen über dieselbe Funktionalität bereichsbezogenen.</span><span class="sxs-lookup"><span data-stu-id="2c56b-104">Some of these Actions like Job, Survey, Poll, etc. are shipped out-of-the-box and provide scoped functionality.</span></span> <span data-ttu-id="2c56b-105">Diese Aktionen innerhalb der app Kaizala ermittelt werden können und in einem Unterhaltungskontext aus der Palette Aktion aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="2c56b-105">These Actions can be discovered within the Kaizala app and can be invoked in a conversation context from the Action Palette.</span></span> 

<span data-ttu-id="2c56b-106">[Kaizala-Verwaltungsportal](https://manage.kaiza.la) ist das Gateway für die Entwicklung, testen, Genehmigung oder beim Veröffentlichen der neuen Kaizala Aktionen.</span><span class="sxs-lookup"><span data-stu-id="2c56b-106">[Kaizala Management Portal](https://manage.kaiza.la) is the gateway for all development, testing, approval or publishing of new Kaizala Actions.</span></span>

<span data-ttu-id="2c56b-107">Die Möglichkeit, aufzurufen, oder erstellen Sie eine neue Instanz einer Aktion kann derzeit nur eine bestimmte Gruppe Mitglieder zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2c56b-107">The ability to invoke or create a new instance of an Action can currently be scoped to members of a specific group only.</span></span> <span data-ttu-id="2c56b-108">Unterstützung für die Veröffentlichung in Mitglied aller Gruppen, die mit einer Organisation über die Kaizala-Verwaltungsportal zugeordnet wird in Kürze bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2c56b-108">Support for publishing to members of all groups mapped to an organization through the Kaizala Management Portal is coming soon.</span></span>

<span data-ttu-id="2c56b-109">Alle Aktionen, die in einer Gruppe von Benutzern veröffentlicht werden können von ihnen auf allen Unterhaltungen aufgerufen werden, den, denen Sie gehören.</span><span class="sxs-lookup"><span data-stu-id="2c56b-109">All Actions that are published to a set of users can be invoked by them on any conversations they are part of.</span></span> <span data-ttu-id="2c56b-110">Dazu gehören die 1:1-Unterhaltungen, private Gruppen oder Gruppen, die zu einer Organisation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2c56b-110">These include their 1:1 conversations, private groups or groups mapped to an organization.</span></span>

<span data-ttu-id="2c56b-111">Aktuell enthält eine Kaizala-Aktion vier verschiedene Ansichten, die definiert werden können:</span><span class="sxs-lookup"><span data-stu-id="2c56b-111">A Kaizala Action currently contains four different views that can be defined:</span></span>

* <span data-ttu-id="2c56b-112">Eine Ansicht erstellen, wenn eine Aktion aus der Palette aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2c56b-112">A creation view when an Action is invoked from the palette</span></span>
* <span data-ttu-id="2c56b-113">Eine Kartenansicht, die auf die Zeichenbereich Chat, wenn eine Instanz der Aktion angezeigt wird, wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="2c56b-113">A card view that appears on the chat canvas when an instance of the Action is sent</span></span>
* <span data-ttu-id="2c56b-114">Eine Ansicht Responder für Benutzer an die Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="2c56b-114">A responder view for users to respond to the Kaizala Action</span></span>
* <span data-ttu-id="2c56b-115">Eine Zusammenfassung zusammengefasster zum Anzeigen Antworten</span><span class="sxs-lookup"><span data-stu-id="2c56b-115">A summary view to view aggregated responses</span></span>

<span data-ttu-id="2c56b-116">Neue Kaizala Aktionen, die Kaizalas Personen Netzwerk nutzen können erstellt und Mobilfunktionen überzeugende Erstellen guter auf folgende Weise:</span><span class="sxs-lookup"><span data-stu-id="2c56b-116">You can create new Kaizala Actions that leverage Kaizala’s people network and mobile capabilities to create compelling experiences in the following ways:</span></span>

* <span data-ttu-id="2c56b-117">**Design eine neue Kaizala-Aktion durch den Kaizala-Verwaltungsportal** – Sie können eine benutzerdefinierte Aktion Kaizala über die Aktion Designer-Schnittstelle auf Grundlage der vorhandenen Vorlagen Aktion entwerfen.</span><span class="sxs-lookup"><span data-stu-id="2c56b-117">**Design a new Kaizala Action through the Kaizala Management Portal** - You can design a custom Kaizala Action through the Action Designer interface by building on the existing Action templates.</span></span>
* <span data-ttu-id="2c56b-118">**Entwickeln Sie ein neues Paket Kaizala Aktion** - komplexe neue Kaizala Aktionen, die benutzerdefinierte Funktionen von webtechnologien wie HTML-, CSS- und JavaScript bereitstellen können erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c56b-118">**Develop a new Kaizala Action package** - You can create complex new Kaizala Actions that provide custom functionality using web technologies like HTML, CSS and JavaScript.</span></span> <span data-ttu-id="2c56b-119">Führen Sie die unten aufgeführten Links, über die verschiedenen Phasen der Entwicklung einer Aktion Kaizala zu informieren.</span><span class="sxs-lookup"><span data-stu-id="2c56b-119">Follow the links below to learn about various stages of developement of a Kaizala Action.</span></span>
    *   [<span data-ttu-id="2c56b-120">Anatomie einer Aktion Kaizala-Paket</span><span class="sxs-lookup"><span data-stu-id="2c56b-120">Anatomy of a Kaizala Action package</span></span>](anatomy.md)
    *   [<span data-ttu-id="2c56b-121">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="2c56b-121">Get Started</span></span>](get_started.md)
    *   [<span data-ttu-id="2c56b-122">Entwickeln</span><span class="sxs-lookup"><span data-stu-id="2c56b-122">Develop</span></span>](develop.md)
    *   [<span data-ttu-id="2c56b-123">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="2c56b-123">Test and Debug</span></span>](test.md)
    *   [<span data-ttu-id="2c56b-124">Publish</span><span class="sxs-lookup"><span data-stu-id="2c56b-124">Publish</span></span>](publish.md)

<span data-ttu-id="2c56b-125">Alle Kaizala Aktionen müssen [Validierungsrichtlinien](validation.md) qualifiziert Kaizala Clients veröffentlicht werden soll, zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="2c56b-125">All Kaizala Actions need to confirm to the [validation policies](validation.md) to be eligible to be published to Kaizala clients.</span></span>

## <a name="build-your-first-kaizala-action"></a><span data-ttu-id="2c56b-126">Erstellen Sie Ihre erste Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="2c56b-126">Build your first Kaizala Action</span></span>

<span data-ttu-id="2c56b-127">Sie können die erste Kaizala Aktion erstellen, indem Sie unsere einfache [Lernprogramm](tutorial.md) ausprobieren</span><span class="sxs-lookup"><span data-stu-id="2c56b-127">You can try out building your first Kaizala Action by following our simple [tutorial](tutorial.md)</span></span>

## <a name="download-sample-action-packages"></a><span data-ttu-id="2c56b-128">Beispiel-Aktion Pakete herunterladen</span><span class="sxs-lookup"><span data-stu-id="2c56b-128">Download Sample Action Packages</span></span>

*  [<span data-ttu-id="2c56b-129">Beispiel-Aktion in der Anforderung / Antwort-format</span><span class="sxs-lookup"><span data-stu-id="2c56b-129">Sample Action in Request-Response format</span></span>](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/Sample%20Request-Response%20Action.zip)
*  [<span data-ttu-id="2c56b-130">Beispiel-Aktion in nur Antwortformat</span><span class="sxs-lookup"><span data-stu-id="2c56b-130">Sample Action in Response only format</span></span>](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/Sample%20Response%20Action.zip)
