# <a name="get-started-with-custom-kaizala-actions"></a><span data-ttu-id="43638-101">Erste Schritte mit benutzerdefinierten Kaizala-Aktionen</span><span class="sxs-lookup"><span data-stu-id="43638-101">Get Started with custom Kaizala Actions</span></span>

## <a name="kaizala-action-development-lifecycle"></a><span data-ttu-id="43638-102">Kaizala-Aktions Entwicklungslebenszyklus</span><span class="sxs-lookup"><span data-stu-id="43638-102">Kaizala Action Development Lifecycle</span></span>

<span data-ttu-id="43638-103">Der typische Entwicklungslebenszyklus einer Kaizala-Aktion umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="43638-103">The typical development lifecycle of a Kaizala Action includes the following steps:</span></span>

  <span data-ttu-id="43638-104">**Schritt 1: Bestimmen des Zwecks der Kaizala-Aktion**</span><span class="sxs-lookup"><span data-stu-id="43638-104">**Step 1 - Decide on the purpose of the Kaizala Action**</span></span>
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
<span data-ttu-id="43638-105">Überlegen Sie sich, was die wichtigsten Features und Szenarios sind, und konstruieren Sie Ihr Design um diese herum.</span><span class="sxs-lookup"><span data-stu-id="43638-105">Decide the most important features and scenarios and focus your design around them.</span></span>

   <span data-ttu-id="43638-106">**Schritt 2: Identifizieren des Datenmodells für die Kaizala-Aktion**</span><span class="sxs-lookup"><span data-stu-id="43638-106">**Step 2 - Identify the data model for the Kaizala Action**</span></span>

<span data-ttu-id="43638-107">Alle Kaizala-Aktionen sind derzeit Formular basiert, d.h. das Datenmodell zum anfordern, sammeln und Aggregieren von Informationen ist eine Reihe von Frage-und Antworttypen, die von der Kaizala-Aggregations Dienste-Plattform (KAS) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="43638-107">All Kaizala Actions are currently Form based - i.e. the data model for requesting, collecting and aggregating information is a set of question and answer types that are supported by the Kaizala Aggregation Services (KAS) platform.</span></span> <span data-ttu-id="43638-108">Stellen Sie sich vor, wie die für Ihre Aktion erforderlichen Daten levergage können, damit die formularinfrastruktur effektiv funktioniert.</span><span class="sxs-lookup"><span data-stu-id="43638-108">Think of how the data required for your action can levergage the form infrastructure to work effectively.</span></span>

   <span data-ttu-id="43638-109">**Schritt 3: Entwerfen und Implementieren der Benutzerumgebung und der Benutzeroberfläche für das Add-in.**</span><span class="sxs-lookup"><span data-stu-id="43638-109">**Step 3 - Design and implement the user experience and user interface for the add-in.**</span></span>

<span data-ttu-id="43638-110">Entwerfen Sie eine schnelle und flüssige Benutzererfahrung, die konsistent und leicht zu erlernen ist, und für deren primäre Szenarien nur wenige Schritte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="43638-110">Design a fast and fluid user experience that is consistent, easy to learn, with primary scenarios that require only a few steps to complete.</span></span> <span data-ttu-id="43638-111">Denken Sie daran, dass eine Kaizala-Aktion nicht auf externe Quellen verweisen kann – also im Hinblick darauf, was Sie in ihrer Aktion implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="43638-111">Remember that a Kaizala Action cannot refer to external sources - so be practical in terms of what you would like to implement within your Action.</span></span>

<span data-ttu-id="43638-112">Sie können aus einer Vielzahl von Webentwicklungstools auswählen und HTML und JavaScript verwenden, um die Benutzeroberfläche zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="43638-112">You can choose from a variety of web development tools and use HTML and JavaScript to implement the user interface.</span></span>

<span data-ttu-id="43638-113">Sie können das KAS-Client-JS-SDK verwenden, um mit den Kaizala-Aggregations Diensten und dem systemeigenen Kaizala-Client zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="43638-113">You can use the KAS Client JS SDK to interact with the Kaizala Aggregation Services and the native Kaizala Client.</span></span> 

   <span data-ttu-id="43638-114">**Schritt 4: Erstellen einer Manifestdatei für die Aktion basierend auf dem Paketmanifest-Schema**</span><span class="sxs-lookup"><span data-stu-id="43638-114">**Step 4 -Create a manifest file for the Action based on the Package Manifest Schema**</span></span>

<span data-ttu-id="43638-115">Erstellen Sie eine Manifestdatei in JSON-Notation, um die Aktion und ihre Komponenten zu identifizieren und die Namen der Ansichtsdateien anzugeben.</span><span class="sxs-lookup"><span data-stu-id="43638-115">Create a manifest file in JSON notation to identify the Action and its components and specify the names of the view files.</span></span>

<span data-ttu-id="43638-116">**Schritt 5: Erstellen einer ZIP-Datei des Pakets und hochladen im Portal**</span><span class="sxs-lookup"><span data-stu-id="43638-116">**Step 5 - Create a ZIP file of the package and upload it on the portal**</span></span>

<span data-ttu-id="43638-117">Erstellen Sie eine ZIP-Datei des Pakets mit allen Ressourcen im Stammverzeichnis des Pakets.</span><span class="sxs-lookup"><span data-stu-id="43638-117">Create a ZIP file of the package with all of it's resources at the root of the package.</span></span>

<span data-ttu-id="43638-118">Laden Sie das Paket im Kaizala-Verwaltungs Portal hoch.</span><span class="sxs-lookup"><span data-stu-id="43638-118">Upload the package on the Kaizala Management Portal.</span></span> <span data-ttu-id="43638-119">Nach dem Hochladen befindet sich die Aktion im Entwurfsstatus.</span><span class="sxs-lookup"><span data-stu-id="43638-119">After upload, Action is in Draft state</span></span>

<span data-ttu-id="43638-120">**Schritt 6-Phase der Entwurfs Aktion**</span><span class="sxs-lookup"><span data-stu-id="43638-120">**Step 6 - Stage the Draft Action**</span></span>

<span data-ttu-id="43638-121">Tippen Sie auf der Detailseite der Aktions Version, die sich im Entwurfszustand befindet, auf die Schaltfläche "Stufe".</span><span class="sxs-lookup"><span data-stu-id="43638-121">On the detail page of the Action version which is in draft state, Tap on 'Stage' button.</span></span> <span data-ttu-id="43638-122">Nachdem eine Aktion ausgeführt wurde, können Sie & testen, um die Aktion zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="43638-122">Once an Action is staged, you can test & debug the Action</span></span> 

 <span data-ttu-id="43638-123">**Schritt 7 – Aktivieren der stufenweisen Aktion**</span><span class="sxs-lookup"><span data-stu-id="43638-123">**Step 7 - Activate the Staged Action**</span></span>

<span data-ttu-id="43638-124">Sobald sich eine Aktion im Status "Staging" befindet und erfolgreich getestet wurde, können Sie die Aktion in Ihrer Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="43638-124">Once an Action is in staged state, and has been tested successfully, you can activate the Action in your organization.</span></span> <span data-ttu-id="43638-125">Aktion wechselt in den aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="43638-125">Action moves to Active state.</span></span> <span data-ttu-id="43638-126">Andere Mitglieder in Ihrer Organisation können diese Aktion auch zu ihren jeweiligen Gruppen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="43638-126">Other members in your organization can also add this Action to their respective groups.</span></span>

  <span data-ttu-id="43638-127">**Schritt 8: Hinzufügen der Aktion zu den entsprechenden Gruppen**</span><span class="sxs-lookup"><span data-stu-id="43638-127">**Step 8 - Add the Action to respective groups**</span></span>

<span data-ttu-id="43638-128">Sobald sich die Aktion im aktiven Zustand befindet, können Sie die Aktion für Gruppen bereitstellen, die Ihrer Organisation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="43638-128">Once Action is in Active state, you can deploy the Action to groups associated with your organization.</span></span> 

