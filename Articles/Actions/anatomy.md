# <a name="anatomy-of-a-kaizala-action-package"></a><span data-ttu-id="547cc-101">Anatomie eines Kaizala-Aktionspakets</span><span class="sxs-lookup"><span data-stu-id="547cc-101">Anatomy of a Kaizala Action package</span></span>

<span data-ttu-id="547cc-102">Ein Kaizala-Aktionspaket ist eine reguläre ZIP-Datei, die nicht kennwortgeschützt ist und eine maximale Größe von 1MB hat.</span><span class="sxs-lookup"><span data-stu-id="547cc-102">A Kaizala Action package is a regular ZIP file which is not password protected and has a maximum size of 1MB.</span></span> <span data-ttu-id="547cc-103">Die Ressourcen im Paket befinden sich im Stamm der ZIP-Datei und nicht in einer Verzeichnisstruktur.</span><span class="sxs-lookup"><span data-stu-id="547cc-103">The resources in the package are at the root of the zip file and not in any directory structure.</span></span> <span data-ttu-id="547cc-104">Die Ressourcen können auch nicht auf externe Ressourcen verweisen, die nicht im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="547cc-104">The resources also cannot reference any external resources other than those present in the package.</span></span>

<span data-ttu-id="547cc-105">Die grundlegenden Komponenten eines Kaizala-Aktionspakets sind</span><span class="sxs-lookup"><span data-stu-id="547cc-105">The basic components of a Kaizala Action package are</span></span> 
*   <span data-ttu-id="547cc-106">Eine Manifestdatei im JSON-Format</span><span class="sxs-lookup"><span data-stu-id="547cc-106">A manifest file in JSON format</span></span>
*   <span data-ttu-id="547cc-107">Ein App-Modell für Ihre Kaizala-Aktion im JSON-Format</span><span class="sxs-lookup"><span data-stu-id="547cc-107">An app model for your Kaizala Action in JSON format</span></span>
*   <span data-ttu-id="547cc-108">Webressourcen, die ihre Kaizala-Aktion darstellen-HTML-, JS-, CSS-und Bilddateien</span><span class="sxs-lookup"><span data-stu-id="547cc-108">Web resources that constitute your Kaizala Action - HTML, JS, CSS and image files</span></span>

## <a name="package-manifest"></a><span data-ttu-id="547cc-109">Paket Manifest</span><span class="sxs-lookup"><span data-stu-id="547cc-109">Package Manifest</span></span>

<span data-ttu-id="547cc-110">Das Manifest gibt die Einstellungen der Kaizala-Aktion an, wie beispielsweise die folgenden:</span><span class="sxs-lookup"><span data-stu-id="547cc-110">The manifest specifies settings of the Kaizala Action, such as the following:</span></span>
*   <span data-ttu-id="547cc-111">Der Anzeigename, die Beschreibung, die ID, die Version und das Aktionssymbol der Aktion.</span><span class="sxs-lookup"><span data-stu-id="547cc-111">The Action's display name, description, ID, version, and Action icon.</span></span>
*   <span data-ttu-id="547cc-112">Verschiedene Ansichten, die ihre Aktion definieren und ihre jeweiligen Aufruf gibt zurück-Punkte zuordnen</span><span class="sxs-lookup"><span data-stu-id="547cc-112">Various views that define your Action and mapping them to their respective invokation points</span></span>
    * <span data-ttu-id="547cc-113">Eine Erstellungsansicht, wenn eine Aktion aus der Palette aufgerufen wird</span><span class="sxs-lookup"><span data-stu-id="547cc-113">A creation view when an Action is invoked from the palette</span></span>
    * <span data-ttu-id="547cc-114">Eine Kartenansicht, die im Chatbereich angezeigt wird, wenn eine Instanz der Aktion gesendet wird</span><span class="sxs-lookup"><span data-stu-id="547cc-114">A card view that appears on the chat canvas when an instance of the Action is sent</span></span>
    * <span data-ttu-id="547cc-115">Eine responderansicht für Benutzer zur Reaktion auf die Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="547cc-115">A responder view for users to respond to the Kaizala Action</span></span>
    * <span data-ttu-id="547cc-116">Eine Zusammenfassungsansicht zum Anzeigen von aggregierten Antworten</span><span class="sxs-lookup"><span data-stu-id="547cc-116">A summary view to view aggregated responses</span></span>
*   <span data-ttu-id="547cc-117">Bezeichnungen, die in den systemeigenen Ansichten verwendet werden, die Ihre benutzerdefinierten Ansichten Kapseln</span><span class="sxs-lookup"><span data-stu-id="547cc-117">Labels to be used across the native views that encapsulate your custom views</span></span>

<span data-ttu-id="547cc-118">Weitere Informationen finden Sie unter [Paket Manifest-Schema im JSON-Format](package_manifest_schema.md).</span><span class="sxs-lookup"><span data-stu-id="547cc-118">For more information, see [Package Manifest Schema in JSON format](package_manifest_schema.md).</span></span>

## <a name="app-model"></a><span data-ttu-id="547cc-119">App-Modell</span><span class="sxs-lookup"><span data-stu-id="547cc-119">App Model</span></span>

<span data-ttu-id="547cc-120">Das App-Modell gibt die Funktionen der Kaizala-Aktion an, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="547cc-120">The App Model specifies the capabilities of the Kaizala Action including:</span></span>
*   <span data-ttu-id="547cc-121">Das Datenmodell für das Form-Objekt, das verwendet werden soll, um die Kaizala-Aggregations Dienste zu nutzen</span><span class="sxs-lookup"><span data-stu-id="547cc-121">The data model for the Form object to be used to leverage the Kaizala Aggregation Services</span></span>
*   <span data-ttu-id="547cc-122">Eigenschaften für das Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="547cc-122">Properties for the form object</span></span>
*   <span data-ttu-id="547cc-123">Dem Form-Objekt zugeordnete Einstellungen</span><span class="sxs-lookup"><span data-stu-id="547cc-123">Settings associated with the Form object</span></span>

<span data-ttu-id="547cc-124">Weitere Informationen finden Sie unter [App-Modell Schema im JSON-Format](appModel_schema.md).</span><span class="sxs-lookup"><span data-stu-id="547cc-124">For more information, see [App Model Schema in JSON format](appModel_schema.md).</span></span>

## <a name="web-resources"></a><span data-ttu-id="547cc-125">WebRessourcen</span><span class="sxs-lookup"><span data-stu-id="547cc-125">Web Resources</span></span>

<span data-ttu-id="547cc-126">Wie oben erwähnt, muss das Kaizala-Paket alle Ressourcen enthalten, auf die innerhalb des Pakets verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="547cc-126">As mentioned above, the Kaizala package must include all the resources being referenced inside the package.</span></span> <span data-ttu-id="547cc-127">Dies umfasst alle HTML-, JavaScript-, CSS-und Bildressourcen.</span><span class="sxs-lookup"><span data-stu-id="547cc-127">This includes all the HTML, JavaScript, CSS and image resources.</span></span>

<span data-ttu-id="547cc-128">Die einfachste Kaizala-Aktion besteht aus drei HTML-Seiten, die angezeigt werden, wenn</span><span class="sxs-lookup"><span data-stu-id="547cc-128">The most basic Kaizala Action consists of three HTML pages that are displayed when</span></span>
*   <span data-ttu-id="547cc-129">Die Kaizal-Aktion wird aus der Aktions Palette in der Client-App-Erstellungsansicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="547cc-129">The Kaizal Action is invoked from the Action Palette in the client app - Creation view</span></span>
*   <span data-ttu-id="547cc-130">Ein Benutzer versucht, auf eine auf der Chat-Canvas in der Client-App-Antwort Ansicht veröffentlichte Aktionskarten Instanz zu Antworten</span><span class="sxs-lookup"><span data-stu-id="547cc-130">A user tries to respond to a Action card instance posted on the Chat Canvas in the client app - Response view</span></span>
*   <span data-ttu-id="547cc-131">Ein Benutzer versucht, die Zusammenfassung aller Antworten anzuzeigen, die für eine bestimmte Aktion veröffentlicht wurden Instanz-Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="547cc-131">A user tries to view the summary of all responses posted for a specific Action instace - Summary view</span></span>

<span data-ttu-id="547cc-132">Um mit der Kaizala-Client-App zu interagieren, können Sie die von uns bereitgestellten [JavaScript-API von KASClient. js](KASClient/README.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="547cc-132">To interact with the Kaizala client app, you can use the [KASClient.js JavaScript API](KASClient/README.md) that we provide.</span></span>


