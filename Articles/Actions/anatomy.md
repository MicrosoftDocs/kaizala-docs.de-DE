# <a name="anatomy-of-a-kaizala-action-package"></a><span data-ttu-id="1ca19-101">Anatomie einer Aktion Kaizala-Paket</span><span class="sxs-lookup"><span data-stu-id="1ca19-101">Anatomy of a Kaizala Action package</span></span>

<span data-ttu-id="1ca19-102">Ein Paket Kaizala-Aktion ist eine regulären Zipdatei, die nicht mit Kennwortschutz versehen ist und weist eine maximale Größe von 1MB.</span><span class="sxs-lookup"><span data-stu-id="1ca19-102">A Kaizala Action package is a regular ZIP file which is not password protected and has a maximum size of 1MB.</span></span> <span data-ttu-id="1ca19-103">Die Ressourcen im Paket werden im Stammverzeichnis der Zip-Datei und nicht in eine beliebige Verzeichnisstruktur.</span><span class="sxs-lookup"><span data-stu-id="1ca19-103">The resources in the package are at the root of the zip file and not in any directory structure.</span></span> <span data-ttu-id="1ca19-104">Die Ressourcen können nicht auch alle externen Ressourcen anwesenden im Paket verweisen.</span><span class="sxs-lookup"><span data-stu-id="1ca19-104">The resources also cannot reference any external resources other than those present in the package.</span></span>

<span data-ttu-id="1ca19-105">Sind die grundlegenden Komponenten eines Pakets Kaizala Aktion</span><span class="sxs-lookup"><span data-stu-id="1ca19-105">The basic components of a Kaizala Action package are</span></span> 
*   <span data-ttu-id="1ca19-106">Eine Manifestdatei im JSON-format</span><span class="sxs-lookup"><span data-stu-id="1ca19-106">A manifest file in JSON format</span></span>
*   <span data-ttu-id="1ca19-107">Eine app-Modell für die Aktion Kaizala im JSON-format</span><span class="sxs-lookup"><span data-stu-id="1ca19-107">An app model for your Kaizala Action in JSON format</span></span>
*   <span data-ttu-id="1ca19-108">Webressourcen, die Ihre Aktion Kaizala - HTML, JS, CSS bilden und Bilddateien</span><span class="sxs-lookup"><span data-stu-id="1ca19-108">Web resources that constitute your Kaizala Action - HTML, JS, CSS and image files</span></span>

## <a name="package-manifest"></a><span data-ttu-id="1ca19-109">Paketmanifest</span><span class="sxs-lookup"><span data-stu-id="1ca19-109">Package Manifest</span></span>

<span data-ttu-id="1ca19-110">Mit dem Manifest werden Einstellungen der Aktion Kaizala wie die folgenden:</span><span class="sxs-lookup"><span data-stu-id="1ca19-110">The manifest specifies settings of the Kaizala Action, such as the following:</span></span>
*   <span data-ttu-id="1ca19-111">Der Aktion angezeigter Name, Beschreibung, ID, Version und Aktionssymbol.</span><span class="sxs-lookup"><span data-stu-id="1ca19-111">The Action's display name, description, ID, version, and Action icon.</span></span>
*   <span data-ttu-id="1ca19-112">Verschiedene Ansichten, die die Aktion und ihre jeweiligen Invokation Punkt zuordnen definieren</span><span class="sxs-lookup"><span data-stu-id="1ca19-112">Various views that define your Action and mapping them to their respective invokation points</span></span>
    * <span data-ttu-id="1ca19-113">Eine Ansicht erstellen, wenn eine Aktion aus der Palette aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1ca19-113">A creation view when an Action is invoked from the palette</span></span>
    * <span data-ttu-id="1ca19-114">Eine Kartenansicht, die auf die Zeichenbereich Chat, wenn eine Instanz der Aktion angezeigt wird, wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="1ca19-114">A card view that appears on the chat canvas when an instance of the Action is sent</span></span>
    * <span data-ttu-id="1ca19-115">Eine Ansicht Responder für Benutzer an die Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="1ca19-115">A responder view for users to respond to the Kaizala Action</span></span>
    * <span data-ttu-id="1ca19-116">Eine Zusammenfassung zusammengefasster zum Anzeigen Antworten</span><span class="sxs-lookup"><span data-stu-id="1ca19-116">A summary view to view aggregated responses</span></span>
*   <span data-ttu-id="1ca19-117">Über die systemeigenen Ansichten verwendet werden, die Ihre benutzerdefinierten Ansichten kapseln Etiketten</span><span class="sxs-lookup"><span data-stu-id="1ca19-117">Labels to be used across the native views that encapsulate your custom views</span></span>

<span data-ttu-id="1ca19-118">Weitere Informationen finden Sie unter [Package-Manifestschema im JSON-Format](package_manifest_schema.md).</span><span class="sxs-lookup"><span data-stu-id="1ca19-118">For more information, see [Package Manifest Schema in JSON format](package_manifest_schema.md).</span></span>

## <a name="app-model"></a><span data-ttu-id="1ca19-119">App-Modell</span><span class="sxs-lookup"><span data-stu-id="1ca19-119">App Model</span></span>

<span data-ttu-id="1ca19-120">Das App-Modell gibt an, das die Funktionen des die Kaizala Aktion, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="1ca19-120">The App Model specifies the capabilities of the Kaizala Action including:</span></span>
*   <span data-ttu-id="1ca19-121">Das Datenmodell für das Form-Objekt verwendet werden, um die Kaizala Aggregation Dienste nutzen</span><span class="sxs-lookup"><span data-stu-id="1ca19-121">The data model for the Form object to be used to leverage the Kaizala Aggregation Services</span></span>
*   <span data-ttu-id="1ca19-122">Eigenschaften für das Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ca19-122">Properties for the form object</span></span>
*   <span data-ttu-id="1ca19-123">Einstellungen für das Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ca19-123">Settings associated with the Form object</span></span>

<span data-ttu-id="1ca19-124">Weitere Informationen finden Sie unter [App Modellschema im JSON-Format](appModel_schema.md).</span><span class="sxs-lookup"><span data-stu-id="1ca19-124">For more information, see [App Model Schema in JSON format](appModel_schema.md).</span></span>

## <a name="web-resources"></a><span data-ttu-id="1ca19-125">Webressourcen</span><span class="sxs-lookup"><span data-stu-id="1ca19-125">Web Resources</span></span>

<span data-ttu-id="1ca19-126">Wie bereits erwähnt, muss das Paket Kaizala alle Ressourcen im Paket referenzierten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ca19-126">As mentioned above, the Kaizala package must include all the resources being referenced inside the package.</span></span> <span data-ttu-id="1ca19-127">Dazu gehören alle HTML, JavaScript, CSS- und Bild-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1ca19-127">This includes all the HTML, JavaScript, CSS and image resources.</span></span>

<span data-ttu-id="1ca19-128">Grundlegende Kaizala Aktion besteht aus drei HTML-Seiten, die angezeigt wird, wenn</span><span class="sxs-lookup"><span data-stu-id="1ca19-128">The most basic Kaizala Action consists of three HTML pages that are displayed when</span></span>
*   <span data-ttu-id="1ca19-129">Die Kaizal-Aktion wird aus der Palette-Aktion in der Client-app - Erstellung Ansicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ca19-129">The Kaizal Action is invoked from the Action Palette in the client app - Creation view</span></span>
*   <span data-ttu-id="1ca19-130">Ein Benutzer versucht, eine Aktion Karte-Instanz auf die Chat Zeichenbereich in der Client-app - Antwort Ansicht gebucht beantworten</span><span class="sxs-lookup"><span data-stu-id="1ca19-130">A user tries to respond to a Action card instance posted on the Chat Canvas in the client app - Response view</span></span>
*   <span data-ttu-id="1ca19-131">Ein Benutzer versucht, die Zusammenfassung aller Antworten für eine bestimmte Aktion Instanz - Zusammenfassungsansicht veröffentlicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="1ca19-131">A user tries to view the summary of all responses posted for a specific Action instace - Summary view</span></span>

<span data-ttu-id="1ca19-132">Zur Interaktion mit der Kaizala-Client-app können Sie die [KASClient.js JavaScript-API](KASClient/README.md) verwenden, die wir bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1ca19-132">To interact with the Kaizala client app, you can use the [KASClient.js JavaScript API](KASClient/README.md) that we provide.</span></span>


