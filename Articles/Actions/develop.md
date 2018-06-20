# <a name="developing-a-new-kaizala-action"></a><span data-ttu-id="cb01d-101">Entwickeln eine neue Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="cb01d-101">Developing a new Kaizala Action</span></span>

<span data-ttu-id="cb01d-102">Ein Paket Kaizala-Aktion ist eine Zip-Datei, die alle benötigte Manifest und Resource-Dateien im Stammverzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="cb01d-102">A Kaizala Action package is a zip file which contains all the requried manifest and resource files at the root.</span></span>

<span data-ttu-id="cb01d-103">Erstellen Sie zunächst einen neuen Ordner auf Ihrem PC zu vereinfachen Ihre Arbeit Dorectory.</span><span class="sxs-lookup"><span data-stu-id="cb01d-103">To begin with, create a new folder on your PC to make it your working dorectory.</span></span>

<span data-ttu-id="cb01d-104">Sie benötigen einen Code-Editor zum Arbeiten mit verschiedenen Arten von Webressourcen & Manifestdateien.</span><span class="sxs-lookup"><span data-stu-id="cb01d-104">You will need a code editor to work with different kinds of web resources & manifest files.</span></span>

>   <span data-ttu-id="cb01d-105">Es wird empfohlen, den Visual Studio-Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="cb01d-105">We recommend the Visual Studio Code editor.</span></span> <span data-ttu-id="cb01d-106">Sie können es [hier](https://code.visualstudio.com/) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-106">You can download it from [here](https://code.visualstudio.com/)</span></span>

## <a name="defining-the-app-model"></a><span data-ttu-id="cb01d-107">Definieren das App-Modell</span><span class="sxs-lookup"><span data-stu-id="cb01d-107">Defining the App Model</span></span>

<span data-ttu-id="cb01d-108">Die Kaizala Aktionen unterstützt derzeit Formular basiert von Datenmodellen, die zum Erstellen, erfassen und das Aggregieren von Daten mithilfe der Kaizala Aggregation Dienste verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cb01d-108">The Kaizala Actions currently support form based data models that can be used for creating, collecting and aggregating data using the Kaizala Aggregation Services.</span></span>

<span data-ttu-id="cb01d-109">Daher müssen Sie zunächst die müssen Sie ein Form-Objekt erstellen, um Fragen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="cb01d-109">So, you will first need to define the ‘questions’ you need to include to create a form object.</span></span>

<span data-ttu-id="cb01d-110">Verweisen Sie auf die [app Modellschema JSON](appModel_schema.md) , um Ihre Aktion app-Modell erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-110">Refer to the [app Model JSON Schema](appModel_schema.md) to create your Action's app model.</span></span>

## <a name="define-the-creation-view"></a><span data-ttu-id="cb01d-111">Definieren der Ansicht erstellen</span><span class="sxs-lookup"><span data-stu-id="cb01d-111">Define the Creation View</span></span>

<span data-ttu-id="cb01d-112">Wenn eine neue Instanz der Kaizala Aktion aus der app-Aktion Palette aufgerufen wird, die HTML-Ressource gekennzeichnet, wie die CreationView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="cb01d-112">When a new instance of the Kaizala Action is invoked from the app's Action Palette, the HTML resource marked as the CreationView is rendered.</span></span> <span data-ttu-id="cb01d-113">Das Ziel dieser Ansicht erstellen ist, erstellen Sie eine neue Instanz des Form-Objekts wie in der app-Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="cb01d-113">The objective of this creation view is to create a new instance of the Form object as defined in the app model.</span></span> 

<span data-ttu-id="cb01d-114">Zur Interaktion mit der Kaizala Aggregation-Dienste und erstellen neue Formularinstanz, können Sie auf die APIs im [KASClient JS SDK](KASClient/README.md)verweisen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-114">To interact with the Kaizala Aggregation Services and creating the new form instance, you can refer to the APIs in the [KASClient JS SDK](KASClient/README.md).</span></span> <span data-ttu-id="cb01d-115">Sie müssen die [KASClient JS-Datei](https://manage.kaiza.la/MiniApps/DownloadSDK) herunterladen und es in Ihr Paket aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-115">You will need to download the [KASClient JS File](https://manage.kaiza.la/MiniApps/DownloadSDK) and include it in your package.</span></span>

<span data-ttu-id="cb01d-116">Erstellen Sie eine neue HTML-Datei, die in dieser Ansicht Erstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb01d-116">Create a new HTML file that represents this creation view.</span></span> <span data-ttu-id="cb01d-117">In der entsprechenden Javascript-Datei Aufrufen des KASClient JS-SDK, und erstellen Sie ein Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cb01d-117">In the corresponding javascript file, invoke the KASClient JS SDK and create a form object.</span></span>

## <a name="create-the-package-manifest-file"></a><span data-ttu-id="cb01d-118">Erstellen Sie die Paket-Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="cb01d-118">Create the Package Manifest file</span></span>

<span data-ttu-id="cb01d-119">Nun, Sie haben eine Semblance der verfügbare zu erreichen und eine Ansicht – erfolgreich erstellt haben können Sie mit dem Erstellen Ihrer Paket-Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="cb01d-119">Now that you have a semblance of what you want to achieve and have successfully created a view – you can start creating your package manifest file.</span></span>

<span data-ttu-id="cb01d-120">Die Manifestdatei Kaizala Paket enthält wichtige Informationen für die Plattform Kaizala dafür zu erkennen und die benutzerdefinierte Kaizala-Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-120">The Kaizala Package manifest file provides essential information for the Kaizala platform for it to recognize and run your custom Kaizala action.</span></span>

<span data-ttu-id="cb01d-121">Verweisen Sie auf das [Paket JSON-Manifestschemas](package_manifest_schema.md) Manifest für Ihre Aktion-Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-121">Refer to the [package manifest JSON Schema](package_manifest_schema.md) to create your Action's package manifest.</span></span>

<span data-ttu-id="cb01d-122">Zu diesem Zeitpunkt sollten Sie auch eine Symboldatei für die benutzerdefinierte Aktion im Paket einschließen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-122">At this point, you should also include an icon file for your custom Action in the package.</span></span>

<span data-ttu-id="cb01d-123">Verweisen auf Ihre Erstellung Ansicht HTML-Datei in der Paketmanifest-, und ordnen sie die entsprechenden Parameter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cb01d-123">Refer to your creation view HTML file in the package manifest and map it to the relevant paramter object.</span></span>

## <a name="configure-the-card-that-appears-on-the-conversation-canvas"></a><span data-ttu-id="cb01d-124">Konfigurieren Sie die Karte, die angezeigt wird, klicken Sie auf die Unterhaltung Zeichenbereich</span><span class="sxs-lookup"><span data-stu-id="cb01d-124">Configure the card that appears on the conversation canvas</span></span>

<span data-ttu-id="cb01d-125">Wenn eine neue Instanz einer Aktion Kaizala erstellt und in einer Unterhaltung gebucht, wird eine Aktion Karte auf den Zeichenbereich für andere Benutzer in der Unterhaltung anzeigen und senden ihre Antworten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb01d-125">When a new instance of a Kaizala Action is created and posted in a conversation, an Action Card is displayed on the canvas for other users in the conversation to view and submit their responses.</span></span>

<span data-ttu-id="cb01d-126">Um die Kartenansicht Chat anpassen, finden Sie unter [Anpassen von ChatCardView](ChatCanvasCardView.md)</span><span class="sxs-lookup"><span data-stu-id="cb01d-126">In order to customize the Chat Card View, please refer to [Customizing ChatCardView](ChatCanvasCardView.md)</span></span> 
## <a name="define-the-response--summary-views"></a><span data-ttu-id="cb01d-127">Definieren der Antwort & Übersichten</span><span class="sxs-lookup"><span data-stu-id="cb01d-127">Define the Response & Summary Views</span></span>

<span data-ttu-id="cb01d-128">Wenn Benutzer versuchen, Details anzeigen und reagieren auf eine Instanz der Kaizala-Aktion in einer Unterhaltung gebucht, können sie zwei Arten von Ansichten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-128">When users try to view details and respond to an instance of the Kaizala Action posted in a conversation, they can see two types of views.</span></span>
*   <span data-ttu-id="cb01d-129">Antwort Ansicht beim Tippen Sie auf die primäre Taste Call-to-Action und eine Antwort bereitstellen möchten</span><span class="sxs-lookup"><span data-stu-id="cb01d-129">Response view when they tap on the primary call-to-action button and want to post a reponse</span></span>
*   <span data-ttu-id="cb01d-130">Ansicht "Zusammenfassung" beim Tippen Sie auf der Karte Kopfzeile und die Aggregierte Ansicht der alle gebucht Reesponses anzeigen möchten</span><span class="sxs-lookup"><span data-stu-id="cb01d-130">Summary view when they tap on the card header and would like to view the aggregated view of all the reesponses posted</span></span>

<span data-ttu-id="cb01d-131">Erstellen Sie eine oder mehrere HTML-Dateien nach Bedarf, definieren Sie die Aktion, und ordnen sie Sie in der Manifestdatei Paket die Grundlage-Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb01d-131">Create one or more HTML files as required for you to define your Action and map them to the relevent parameters in the package manifest file.</span></span>

<span data-ttu-id="cb01d-132">Zur Interaktion mit der Kaizala Aggregation Dienste und die Kaizala Native Client zum Abrufen von Informationen, senden eine Antwort oder aggregierte Antworten erhalten möchten, können Sie auf die APIs im [JS-SDK KASClient](KASClient/README.md)verweisen.</span><span class="sxs-lookup"><span data-stu-id="cb01d-132">To interact with the Kaizala Aggregation Services and the Kaizala Native client to retrieve information, submit a response or get aggregated responses, you can refer to the APIs in the [KASClient JS SDK](KASClient/README.md).</span></span>


## <a name="create-the-zip-file"></a><span data-ttu-id="cb01d-133">Erstellen Sie die ZIP-Datei</span><span class="sxs-lookup"><span data-stu-id="cb01d-133">Create the ZIP file</span></span>

<span data-ttu-id="cb01d-134">Wählen Sie alle Dateien im Arbeitsverzeichnis, und erstellen Sie eine neue Zip-Datei für Ihr Paket.</span><span class="sxs-lookup"><span data-stu-id="cb01d-134">Select all the files in your working directory and create a new zip file for your package.</span></span> <span data-ttu-id="cb01d-135">Stellen Sie sicher, dass alle Dateien im Stammverzeichnis des Pakets vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cb01d-135">Ensure that all files are present in the root directory of the package.</span></span>

*   <span data-ttu-id="cb01d-136">Weiter: [Veröffentlichen](publish.md)</span><span class="sxs-lookup"><span data-stu-id="cb01d-136">Next: [Publish](publish.md)</span></span>
