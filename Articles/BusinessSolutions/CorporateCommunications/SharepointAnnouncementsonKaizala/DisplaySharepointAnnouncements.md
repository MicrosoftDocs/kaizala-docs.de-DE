# <a name="display-sharepoint-announcements-in-kaizala-groups"></a><span data-ttu-id="8d55f-101">Anzeigen von SharePoint-anSagen in Kaizala-Gruppen</span><span class="sxs-lookup"><span data-stu-id="8d55f-101">Display SharePoint Announcements in Kaizala groups</span></span> 
<span data-ttu-id="8d55f-102">Organisationen verwenden SharePoint-Ansage-App zum Freigeben von Nachrichten, Status und anderen kurzen Informationen zu Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="8d55f-102">Organizations use SharePoint Announcement app to share news, status and other short bits of information to employees .</span></span> <span data-ttu-id="8d55f-103">SharePoint-Ansage-APP, die mit einer Liste geliefert wird, ist ein spezieller Listentyp, mit dem Sie Ankündigungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="8d55f-103">Sharepoint Announcement app, that comes with a list, is a special type of list that lets you create announcements.</span></span>

<span data-ttu-id="8d55f-104">Mithilfe dieses Beispiels können Organisationen SharePoint-Ankündigungen mit der ersten und mobilen Arbeitskräften in Kaizala freigeben.</span><span class="sxs-lookup"><span data-stu-id="8d55f-104">Using this sample, organizations can share SharePoint announcements with the first line and mobile workers on Kaizala.</span></span> <span data-ttu-id="8d55f-105">Diese Karte hat 3 Felder in der Chat Kartenansicht-Anlagen (in diesem Beispiel Fotostory von Bildern), Titel und Ansagetext (Beschreibung).</span><span class="sxs-lookup"><span data-stu-id="8d55f-105">This card has 3 fields in chat card view- Attachments( In this example, Photo story of images), Title and Announcement body (description).</span></span> <span data-ttu-id="8d55f-106">Diese wird an eine Kaizala-Gruppe als out-of-Box-Ansage Karte gesendet.</span><span class="sxs-lookup"><span data-stu-id="8d55f-106">This is sent to a Kaizala group as an out-of-box announcement card.</span></span>

<span data-ttu-id="8d55f-107">Die Chat Kartenansicht ist wie folgt.</span><span class="sxs-lookup"><span data-stu-id="8d55f-107">The chat card view is as below</span></span>

<img src="SharepointAnnouncementImages/1.png" alt="Chat card view Logo" width="340" />

<span data-ttu-id="8d55f-108">Beim Tippen auf die Karte ist die immersive Ansicht wie folgt.</span><span class="sxs-lookup"><span data-stu-id="8d55f-108">On tapping the card, immersive view is as below</span></span>

<img src="SharepointAnnouncementImages/2.png" alt="immersive view Logo" width="180" />

<span data-ttu-id="8d55f-109">Dieses Szenario kann grob in zwei Schritte unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="8d55f-109">This scenario can be broadly divided into 2 steps:</span></span>
1. <span data-ttu-id="8d55f-110">Erstellen einer Ankündigungsliste mit Spalten-Titel, Anlagen und Ansagetext (Beschreibung)</span><span class="sxs-lookup"><span data-stu-id="8d55f-110">Create an announcement list with columns- Title, attachments and announcement body(description)</span></span> 

    > <span data-ttu-id="8d55f-111">Hinweis: Rich-Text wird nicht von einer Vorankündigungs Karte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d55f-111">Note: Rich text is not supported by out-of-box announcement card.</span></span> <span data-ttu-id="8d55f-112">Deaktivieren Sie Rich-Text für SharePoint-Kolumnen mit dem Ankündigungstext (Beschreibung) beim Erstellen dieser Spalte.</span><span class="sxs-lookup"><span data-stu-id="8d55f-112">Switch off rich text for sharepoint column that has Announcement body(description) while creating that column.</span></span>

    <img src="SharepointAnnouncementImages/3.5.png" width="200" />

2. <span data-ttu-id="8d55f-113">Konfigurieren Sie Flow so, dass bei der Erstellung eines neuen Elements oder eines vorhandenen Elements in der Ankündigungsliste eine Out-of-Box-Ansage Karte an eine Kaizala-Gruppe gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d55f-113">Configure Flow such that, when a new item is created or existing item is modified in announcement list, an out-of-box announcement card is sent to a Kaizala group</span></span>

    <img src="SharepointAnnouncementImages/3.png" alt="Sharepoint&Flow Logo" width="400" />

## <a name="implementation-steps"></a><span data-ttu-id="8d55f-114">Implementierungsschritte</span><span class="sxs-lookup"><span data-stu-id="8d55f-114">Implementation steps</span></span>


1. <span data-ttu-id="8d55f-115">[Hinzufügen](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) einer Ankündigungs-App zur SharePoint-Website (siehe*unten*)</span><span class="sxs-lookup"><span data-stu-id="8d55f-115">[Add Announcement app](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) to SharePoint site(*as below*)</span></span>
     1. <span data-ttu-id="8d55f-116">Klicken Sie auf das Symbol "Einstellungen"</span><span class="sxs-lookup"><span data-stu-id="8d55f-116">Click on the settings icon</span></span>
     2.  <span data-ttu-id="8d55f-117">Klicken Sie auf app hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d55f-117">Click on Add an App</span></span> 
     3.  <span data-ttu-id="8d55f-118">Wählen Sie Ansage-App aus der Liste der verfügbaren Apps aus.</span><span class="sxs-lookup"><span data-stu-id="8d55f-118">Select Announcement App from the list of available Apps</span></span>
2. <span data-ttu-id="8d55f-119">Verwenden des [hervorgehobenen Inhalts](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) Webparts (*Falls erforderlich, zur Visualisierung*)</span><span class="sxs-lookup"><span data-stu-id="8d55f-119">Use the [highlighted content web part](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*if necessary , for visualization*)</span></span>
3. <span data-ttu-id="8d55f-120">Laden Sie die [SharepointAnnouncementOnKaizala-SolutionPackage. zip](https://aka.ms/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*Dies ist ein Flow-Paket*)</span><span class="sxs-lookup"><span data-stu-id="8d55f-120">Download the [SharepointAnnouncementOnKaizala-SolutionPackage.zip](https://aka.ms/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*This is a Flow package*)</span></span>
4. <span data-ttu-id="8d55f-121">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage. zip zu Ihrem Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="8d55f-121">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip to your Microsoft Flow account</span></span>
   
   > <span data-ttu-id="8d55f-122">Hinweis: Wenn Sie die SharePoint-oder Kaizala-Verbindung noch nie verwendet haben, fügen Sie zunächst [Verbindungen hinzu](https://docs.microsoft.com/en-us/flow/add-manage-connections) .</span><span class="sxs-lookup"><span data-stu-id="8d55f-122">Note: If you have never used Sharepoint or Kaizala connection, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>
   
5. <span data-ttu-id="8d55f-123">Bearbeiten des Flusses (nach*folgend*)</span><span class="sxs-lookup"><span data-stu-id="8d55f-123">Edit the Flow (*as below*)</span></span>
    1. <span data-ttu-id="8d55f-124">Im ersten Block des Flusses</span><span class="sxs-lookup"><span data-stu-id="8d55f-124">In the first block of the Flow</span></span>
    
         1. <span data-ttu-id="8d55f-125">Geben Sie die Websiteadresse ein.</span><span class="sxs-lookup"><span data-stu-id="8d55f-125">Enter the site address</span></span>
         2. <span data-ttu-id="8d55f-126">Geben Sie den Namen der Liste ein (*Schritte zum Abrufen des Listen namens ist wie folgt*)</span><span class="sxs-lookup"><span data-stu-id="8d55f-126">Enter the List name (*steps to get List name is as below*)</span></span>
            - <span data-ttu-id="8d55f-127">Klicken Sie in der linken Ecke des Bildschirms auf die Registerkarte Websiteinhalte.</span><span class="sxs-lookup"><span data-stu-id="8d55f-127">Click on site contents tab on the left hand corner of the screen</span></span>
            - <span data-ttu-id="8d55f-128">Wählen Sie die Ankündigungsliste aus, an die Sie Ankündigungen an Kaizala senden möchten.</span><span class="sxs-lookup"><span data-stu-id="8d55f-128">Select the announcement list from which you want to send announcements to Kaizala</span></span>
            - <span data-ttu-id="8d55f-129">Klicken Sie auf das Symbol "Einstellungen" in der oberen rechten Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="8d55f-129">Click on settings icon at the top right corner of the screen</span></span>
            - <span data-ttu-id="8d55f-130">Wechseln zu Listeneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8d55f-130">Go to List settings</span></span>
            - <span data-ttu-id="8d55f-131">Kopieren Sie die URL der Liste aus dem Browser.</span><span class="sxs-lookup"><span data-stu-id="8d55f-131">Copy the URL of the list from the browser.</span></span>
            - <span data-ttu-id="8d55f-132">DeCodieren Sie die URL (Sie können die URL [hier](https://www.url-encode-decode.com/) decodieren)</span><span class="sxs-lookup"><span data-stu-id="8d55f-132">Decode the URL (you can decode the URL [here](https://www.url-encode-decode.com/) )</span></span>
        <img src="SharepointAnnouncementImages/4.PNG" alt="" width="500" />
      
    2. <span data-ttu-id="8d55f-133">Im zweiten Block des Flusses</span><span class="sxs-lookup"><span data-stu-id="8d55f-133">In the second block of the Flow</span></span>
   
        <span data-ttu-id="8d55f-134">Ordnen Sie das Feld Wert mit dem Spaltentitel der Ankündigungsliste zu, der den Text der Ansage (Beschreibung) aus dem dynamischen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="8d55f-134">Map "value" field with column title of announcement list, that has announcement body(description) from Dynamic content.</span></span> <span data-ttu-id="8d55f-135">Im folgenden Beispiel lautet der Spaltentitel "Ansagetext". </span><span class="sxs-lookup"><span data-stu-id="8d55f-135">In the below example, the column title is "Announcement Body"  </span></span><img src="SharepointAnnouncementImages/5.png" alt="" width="600" />
       
    3. <span data-ttu-id="8d55f-136">Im letzten Block des Flusses</span><span class="sxs-lookup"><span data-stu-id="8d55f-136">In the last block of the Flow</span></span>
    
       <span data-ttu-id="8d55f-137">Wählen Sie den Gruppennamen aus Dropdown aus.</span><span class="sxs-lookup"><span data-stu-id="8d55f-137">Select the group name from dropdown.</span></span> <span data-ttu-id="8d55f-138">In diesem Beispiel lautet "jeder @ Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="8d55f-138">In this Example it is "Everyone@Fabrikam"</span></span>
       <img src="SharepointAnnouncementImages/6.png" alt="" width="450" />
6. <span data-ttu-id="8d55f-139">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="8d55f-139">Save the flow</span></span>

<span data-ttu-id="8d55f-140">Die Ansage wird an die ausgewählte Kaizala-Gruppe gesendet, und jeder Zeitablauf wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8d55f-140">Announcement will be sent to the selected Kaizala group, each time flow is triggered.</span></span>

> <span data-ttu-id="8d55f-141">Hinweis: Textdatei wird als Anlage nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8d55f-141">Note: Text file is not supported as attachment</span></span>
