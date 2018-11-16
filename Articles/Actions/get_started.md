# <a name="get-started-with-custom-kaizala-actions"></a><span data-ttu-id="e30d2-101">Erste Schritte mit benutzerdefinierten Kaizala Aktionen</span><span class="sxs-lookup"><span data-stu-id="e30d2-101">Get Started with custom Kaizala Actions</span></span>

## <a name="kaizala-action-development-lifecycle"></a><span data-ttu-id="e30d2-102">Kaizala Aktion Entwicklungslebenszyklus</span><span class="sxs-lookup"><span data-stu-id="e30d2-102">Kaizala Action Development Lifecycle</span></span>

<span data-ttu-id="e30d2-103">Der normalen Entwicklungszyklus einer Aktion Kaizala umfasst die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e30d2-103">The typical development lifecycle of a Kaizala Action includes the following steps:</span></span>

  <span data-ttu-id="e30d2-104">**Schritt 1: entscheiden Sie sich für den Zweck der Aktion Kaizala**</span><span class="sxs-lookup"><span data-stu-id="e30d2-104">**Step 1 - Decide on the purpose of the Kaizala Action**</span></span>
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
<span data-ttu-id="e30d2-105">Überlegen Sie sich, was die wichtigsten Features und Szenarios sind, und konstruieren Sie Ihr Design um diese herum.</span><span class="sxs-lookup"><span data-stu-id="e30d2-105">Decide the most important features and scenarios and focus your design around them.</span></span>

   <span data-ttu-id="e30d2-106">**Schritt 2: Identifizieren Sie das Datenmodell für die Aktion Kaizala**</span><span class="sxs-lookup"><span data-stu-id="e30d2-106">**Step 2 - Identify the data model for the Kaizala Action**</span></span>

<span data-ttu-id="e30d2-107">Alle Kaizala Aktionen sind derzeit Formular basiert – d. h. ist das Datenmodell das Aggregieren Informationen anfordert, erfassen und eine Reihe von Frage und Antworttypen, die von der Plattform Kaizala Aggregation Services (KAS) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e30d2-107">All Kaizala Actions are currently Form based - i.e. the data model for requesting, collecting and aggregating information is a set of question and answer types that are supported by the Kaizala Aggregation Services (KAS) platform.</span></span> <span data-ttu-id="e30d2-108">Stellen Sie sich wie die Daten für die Aktion erforderlich Levergage können der Formular-Infrastruktur effektiv funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e30d2-108">Think of how the data required for your action can levergage the form infrastructure to work effectively.</span></span>

   <span data-ttu-id="e30d2-109">**Schritt 3: Entwerfen und implementieren die Benutzer wünschen und die Benutzeroberfläche für das Add-in.**</span><span class="sxs-lookup"><span data-stu-id="e30d2-109">**Step 3 - Design and implement the user experience and user interface for the add-in.**</span></span>

<span data-ttu-id="e30d2-110">Entwerfen Sie ein schnelles und flüssiges Zusammenspiel Benutzererlebnis, der konsistente, leicht zu, mit häufig vorkommenden Szenarien erlernen, die nur einige Schritte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e30d2-110">Design a fast and fluid user experience that is consistent, easy to learn, with primary scenarios that require only a few steps to complete.</span></span> <span data-ttu-id="e30d2-111">Denken Sie daran, dass eine Aktion Kaizala also auf externen Quellen - verweisen kann nicht praktikabel im Hinblick auf was Sie innerhalb der Aktion implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e30d2-111">Remember that a Kaizala Action cannot refer to external sources - so be practical in terms of what you would like to implement within your Action.</span></span>

<span data-ttu-id="e30d2-112">Sie können aus einer Vielzahl von Webentwicklungstools auswählen und HTML und JavaScript verwenden, um die Benutzeroberfläche zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="e30d2-112">You can choose from a variety of web development tools and use HTML and JavaScript to implement the user interface.</span></span>

<span data-ttu-id="e30d2-113">KAS Client JS-SDK können Sie mit der Kaizala Aggregation Dienste und die systemeigene Kaizala Client interagieren.</span><span class="sxs-lookup"><span data-stu-id="e30d2-113">You can use the KAS Client JS SDK to interact with the Kaizala Aggregation Services and the native Kaizala Client.</span></span> 

   <span data-ttu-id="e30d2-114">**Schritt 4 – erstellen eine Manifestdatei für die Aktion auf die Paket-Manifestschema basierte**</span><span class="sxs-lookup"><span data-stu-id="e30d2-114">**Step 4 -Create a manifest file for the Action based on the Package Manifest Schema**</span></span>

<span data-ttu-id="e30d2-115">Erstellen einer Manifestdatei im JSON-Schreibweise zu identifizieren, die Aktion und die zugehörigen Komponenten, und geben Sie die Namen der Dateien anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e30d2-115">Create a manifest file in JSON notation to identify the Action and its components and specify the names of the view files.</span></span>

<span data-ttu-id="e30d2-116">**Schritt 5 – eine ZIP-Datei des Pakets erstellen und auf das Portal hochladen**</span><span class="sxs-lookup"><span data-stu-id="e30d2-116">**Step 5 - Create a ZIP file of the package and upload it on the portal**</span></span>

<span data-ttu-id="e30d2-117">Erstellen Sie eine ZIP-Datei des Pakets mit aller die Ressourcen im Stammverzeichnis des Pakets.</span><span class="sxs-lookup"><span data-stu-id="e30d2-117">Create a ZIP file of the package with all of it's resources at the root of the package.</span></span>

<span data-ttu-id="e30d2-118">Laden Sie das Paket auf dem Kaizala-Verwaltungsportal.</span><span class="sxs-lookup"><span data-stu-id="e30d2-118">Upload the package on the Kaizala Management Portal.</span></span> <span data-ttu-id="e30d2-119">Nach dem Hochladen ist Aktion im Zustand Entwurf</span><span class="sxs-lookup"><span data-stu-id="e30d2-119">After upload, Action is in Draft state</span></span>

<span data-ttu-id="e30d2-120">**Schritt 6: Phase die Aktion Entwurf**</span><span class="sxs-lookup"><span data-stu-id="e30d2-120">**Step 6 - Stage the Draft Action**</span></span>

<span data-ttu-id="e30d2-121">Tippen Sie auf der Detailseite der Aktion Version sich im Entwurf Zustand befindet, auf die Schaltfläche "Stufe".</span><span class="sxs-lookup"><span data-stu-id="e30d2-121">On the detail page of the Action version which is in draft state, Tap on 'Stage' button.</span></span> <span data-ttu-id="e30d2-122">Nachdem eine Aktion bereitgestellt wird, können testen und Debuggen die Aktion</span><span class="sxs-lookup"><span data-stu-id="e30d2-122">Once an Action is staged, you can test & debug the Action</span></span> 

 <span data-ttu-id="e30d2-123">**Schritt 7: Aktivieren der mehrstufigen Aktion**</span><span class="sxs-lookup"><span data-stu-id="e30d2-123">**Step 7 - Activate the Staged Action**</span></span>

<span data-ttu-id="e30d2-124">Sobald eine Aktivität befindet sich in mehrstufigen Zustand und erfolgreich getestet wurde, können Sie die Aktion in Ihrer Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e30d2-124">Once an Action is in staged state, and has been tested successfully, you can activate the Action in your organization.</span></span> <span data-ttu-id="e30d2-125">Aktion verschiebt in aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="e30d2-125">Action moves to Active state.</span></span> <span data-ttu-id="e30d2-126">Andere Mitglieder in Ihrer Organisation können diese Aktion auch ihren jeweiligen Gruppen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e30d2-126">Other members in your organization can also add this Action to their respective groups.</span></span>

  <span data-ttu-id="e30d2-127">**Schritt 8: Fügen Sie den jeweiligen Gruppen**</span><span class="sxs-lookup"><span data-stu-id="e30d2-127">**Step 8 - Add the Action to respective groups**</span></span>

<span data-ttu-id="e30d2-128">Sobald Aktion aktiv ist, können Sie die Aktion zu Gruppen zugeordnet Ihrer Organisation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e30d2-128">Once Action is in Active state, you can deploy the Action to groups associated with your organization.</span></span> 

