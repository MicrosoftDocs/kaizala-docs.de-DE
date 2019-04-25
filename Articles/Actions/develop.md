# <a name="developing-a-new-kaizala-action"></a><span data-ttu-id="13f24-101">Entwickeln einer neuen Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="13f24-101">Developing a new Kaizala Action</span></span>

<span data-ttu-id="13f24-102">Ein Kaizala-Aktionspaket ist eine ZIP-Datei, die alle requried-Manifest-und-Ressourcendateien im Stammverzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="13f24-102">A Kaizala Action package is a zip file which contains all the requried manifest and resource files at the root.</span></span>

<span data-ttu-id="13f24-103">Erstellen Sie zunächst einen neuen Ordner auf Ihrem PC, um ihn zu Ihrem Arbeitsverzeichnis zu machen.</span><span class="sxs-lookup"><span data-stu-id="13f24-103">To begin with, create a new folder on your PC to make it your working directory.</span></span>

<span data-ttu-id="13f24-104">Sie benötigen einen Code-Editor, um mit verschiedenen Arten von Webressourcen & Manifestdateien arbeiten.</span><span class="sxs-lookup"><span data-stu-id="13f24-104">You will need a code editor to work with different kinds of web resources & manifest files.</span></span>

>   <span data-ttu-id="13f24-105">Wir empfehlen den Code-Editor von Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="13f24-105">We recommend the Visual Studio Code editor.</span></span> <span data-ttu-id="13f24-106">Sie können es von [hier](https://code.visualstudio.com/) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="13f24-106">You can download it from [here](https://code.visualstudio.com/)</span></span>

## <a name="defining-the-app-model"></a><span data-ttu-id="13f24-107">Definieren des App-Modells</span><span class="sxs-lookup"><span data-stu-id="13f24-107">Defining the App Model</span></span>

<span data-ttu-id="13f24-108">Die Kaizala-Aktionen unterstützen derzeit formularbasierte Datenmodelle, die zum Erstellen, sammeln und Aggregieren von Daten mithilfe der Kaizala-Aggregations Dienste verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="13f24-108">The Kaizala Actions currently support form based data models that can be used for creating, collecting and aggregating data using the Kaizala Aggregation Services.</span></span>

<span data-ttu-id="13f24-109">Daher müssen Sie zunächst die "Fragen" definieren, die Sie zum Erstellen eines Form-Objekts hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="13f24-109">So, you will first need to define the ‘questions’ you need to include to create a form object.</span></span>

<span data-ttu-id="13f24-110">Verwenden Sie das [JSON-Schema des App-Modells](appModel_schema.md) , um das App-Modell Ihrer Aktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13f24-110">Refer to the [app Model JSON Schema](appModel_schema.md) to create your Action's app model.</span></span>

## <a name="define-the-creation-view"></a><span data-ttu-id="13f24-111">Definieren der ErstellungsAnsicht</span><span class="sxs-lookup"><span data-stu-id="13f24-111">Define the Creation View</span></span>

<span data-ttu-id="13f24-112">Wenn eine neue Instanz der Kaizala-Aktion aus der Aktions Palette der app aufgerufen wird, wird die als CreationView gekennzeichnete HTML-Ressource gerendert.</span><span class="sxs-lookup"><span data-stu-id="13f24-112">When a new instance of the Kaizala Action is invoked from the app's Action Palette, the HTML resource marked as the CreationView is rendered.</span></span> <span data-ttu-id="13f24-113">Das Ziel dieser Erstellungsansicht besteht darin, eine neue Instanz des Form-Objekts zu erstellen, wie im App-Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="13f24-113">The objective of this creation view is to create a new instance of the Form object as defined in the app model.</span></span> 

<span data-ttu-id="13f24-114">Um mit den Kaizala-Aggregations Diensten zu interagieren und die neue Formularinstanz zu erstellen, können Sie auf die APIs im [KASCLIENT js SDK](KASClient/README.md)verweisen.</span><span class="sxs-lookup"><span data-stu-id="13f24-114">To interact with the Kaizala Aggregation Services and creating the new form instance, you can refer to the APIs in the [KASClient JS SDK](KASClient/README.md).</span></span> <span data-ttu-id="13f24-115">Sie müssen die [KASCLIENT JS-Datei](https://manage.kaiza.la/MiniApps/DownloadSDK) herunterladen und in Ihr Paket aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="13f24-115">You will need to download the [KASClient JS File](https://manage.kaiza.la/MiniApps/DownloadSDK) and include it in your package.</span></span>

<span data-ttu-id="13f24-116">Erstellen Sie eine neue HTML-Datei, die diese Erstellungsansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="13f24-116">Create a new HTML file that represents this creation view.</span></span> <span data-ttu-id="13f24-117">Rufen Sie in der entsprechenden JavaScript-Datei das KASClient JS-SDK auf, und erstellen Sie ein Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="13f24-117">In the corresponding javascript file, invoke the KASClient JS SDK and create a form object.</span></span>

## <a name="create-the-package-manifest-file"></a><span data-ttu-id="13f24-118">Erstellen der Paket Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="13f24-118">Create the Package Manifest file</span></span>

<span data-ttu-id="13f24-119">Nachdem Sie nun einen Anschein haben, was Sie erreichen möchten und eine Ansicht erfolgreich erstellt haben, können Sie mit dem Erstellen Ihrer Paket Manifestdatei beginnen.</span><span class="sxs-lookup"><span data-stu-id="13f24-119">Now that you have a semblance of what you want to achieve and have successfully created a view – you can start creating your package manifest file.</span></span>

<span data-ttu-id="13f24-120">Die Kaizala-Paket Manifestdatei enthält wichtige Informationen für die Kaizala-Plattform, damit Sie Ihre benutzerdefinierte Kaizala-Aktion erkennen und ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="13f24-120">The Kaizala Package manifest file provides essential information for the Kaizala platform for it to recognize and run your custom Kaizala action.</span></span>

<span data-ttu-id="13f24-121">Weitere Informationen finden Sie unter [JSON-Schema des paketmanifests](package_manifest_schema.md) , um das Paketmanifest ihrer Aktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13f24-121">Refer to the [package manifest JSON Schema](package_manifest_schema.md) to create your Action's package manifest.</span></span>

<span data-ttu-id="13f24-122">An diesem Punkt sollten Sie auch eine Symboldatei für die benutzerdefinierte Aktion in das Paket einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="13f24-122">At this point, you should also include an icon file for your custom Action in the package.</span></span>

<span data-ttu-id="13f24-123">Verweisen Sie im Paketmanifest auf die HTML-Datei für die Erstellungsansicht, und ordnen Sie Sie dem entsprechenden Parameter-Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="13f24-123">Refer to your creation view HTML file in the package manifest and map it to the relevant parameter object.</span></span>

## <a name="configure-the-card-that-appears-on-the-conversation-canvas"></a><span data-ttu-id="13f24-124">Konfigurieren der Karte, die auf der Unterhaltungs Leinwand angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="13f24-124">Configure the card that appears on the conversation canvas</span></span>

<span data-ttu-id="13f24-125">Wenn eine neue Instanz einer Kaizala-Aktion erstellt und in einer Unterhaltung bereitgestellt wird, wird eine Aktionskarte auf dem Arbeitsbereich angezeigt, damit andere Benutzer in der Unterhaltung ihre Antworten anzeigen und senden können.</span><span class="sxs-lookup"><span data-stu-id="13f24-125">When a new instance of a Kaizala Action is created and posted in a conversation, an Action Card is displayed on the canvas for other users in the conversation to view and submit their responses.</span></span>

<span data-ttu-id="13f24-126">Informationen zum Anpassen der Chat Kartenansicht finden Sie unter [Customizing ChatCardView](ChatCanvasCardView.md)</span><span class="sxs-lookup"><span data-stu-id="13f24-126">In order to customize the Chat Card View, please refer to [Customizing ChatCardView](ChatCanvasCardView.md)</span></span> 
## <a name="define-the-response--summary-views"></a><span data-ttu-id="13f24-127">Definieren der Reaktions-&-ZusammenfassungsAnsichten</span><span class="sxs-lookup"><span data-stu-id="13f24-127">Define the Response & Summary Views</span></span>

<span data-ttu-id="13f24-128">Wenn Benutzer versuchen, Details anzuzeigen und auf eine Instanz der Kaizala-Aktion zu antworten, die in einer Unterhaltung veröffentlicht wurde, können zwei Arten von Ansichten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="13f24-128">When users try to view details and respond to an instance of the Kaizala Action posted in a conversation, they can see two types of views.</span></span>
*   <span data-ttu-id="13f24-129">Antwort Ansicht, wenn Sie auf die primäre Schaltfläche "Call-to-Action" tippen und eine reponsse veröffentlichen möchten</span><span class="sxs-lookup"><span data-stu-id="13f24-129">Response view when they tap on the primary call-to-action button and want to post a reponse</span></span>
*   <span data-ttu-id="13f24-130">Zusammenfassungsansicht, wenn Sie auf den Karten Kopf tippen und die aggregierte Ansicht aller gebuchten reesponses anzeigen möchten</span><span class="sxs-lookup"><span data-stu-id="13f24-130">Summary view when they tap on the card header and would like to view the aggregated view of all the reesponses posted</span></span>

<span data-ttu-id="13f24-131">Erstellen Sie mindestens eine HTML-Datei, die Sie zum Definieren der Aktion benötigen, und ordnen Sie Sie den relevante-Parametern in der Paket Manifestdatei zu.</span><span class="sxs-lookup"><span data-stu-id="13f24-131">Create one or more HTML files as required for you to define your Action and map them to the relevent parameters in the package manifest file.</span></span>

<span data-ttu-id="13f24-132">Wenn Sie mit den Kaizala-Aggregations Diensten und dem nativen Client von Kaizala interagieren möchten, um Informationen abzurufen, eine Antwort zu senden oder aggregierte Antworten abzurufen, können Sie sich auf die APIs im [KASCLIENT js SDK](KASClient/README.md)beziehen.</span><span class="sxs-lookup"><span data-stu-id="13f24-132">To interact with the Kaizala Aggregation Services and the Kaizala Native client to retrieve information, submit a response or get aggregated responses, you can refer to the APIs in the [KASClient JS SDK](KASClient/README.md).</span></span>


## <a name="create-the-zip-file"></a><span data-ttu-id="13f24-133">Erstellen der ZIP-Datei</span><span class="sxs-lookup"><span data-stu-id="13f24-133">Create the ZIP file</span></span>

<span data-ttu-id="13f24-134">Wählen Sie alle Dateien in Ihrem Arbeitsverzeichnis aus, und erstellen Sie eine neue ZIP-Datei für Ihr Paket.</span><span class="sxs-lookup"><span data-stu-id="13f24-134">Select all the files in your working directory and create a new zip file for your package.</span></span> <span data-ttu-id="13f24-135">Stellen Sie sicher, dass alle Dateien im Stammverzeichnis des Pakets vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="13f24-135">Ensure that all files are present in the root directory of the package.</span></span>

*   <span data-ttu-id="13f24-136">Weiter: [Publish](publish.md)</span><span class="sxs-lookup"><span data-stu-id="13f24-136">Next: [Publish](publish.md)</span></span>
