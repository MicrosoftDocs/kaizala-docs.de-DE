# <a name="display-sharepoint-announcements-in-kaizala-groups"></a><span data-ttu-id="e27ac-101">Anzeigen von SharePoint-Ankündigungen in Kaizala Gruppen</span><span class="sxs-lookup"><span data-stu-id="e27ac-101">Display SharePoint Announcements in Kaizala groups</span></span> 
<span data-ttu-id="e27ac-102">Organisationen verwenden SharePoint Ankündigung app Neuigkeiten, Status und andere kurze Informationen zu Mitarbeitern gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="e27ac-102">Organizations use SharePoint Announcement app to share news, status and other short bits of information to employees .</span></span> <span data-ttu-id="e27ac-103">Ankündigung der SharePoint-app, die mit einer Liste stammen, ist eine spezielle Art von Liste, die Sie einer Ankündigungen erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="e27ac-103">Sharepoint Announcement app, that comes with a list, is a special type of list that lets you create an announcements.</span></span>

<span data-ttu-id="e27ac-104">In diesem Beispiel verwenden, können Organisationen SharePoint Ankündigungen für die erste Zeile und mobile Mitarbeiter auf Kaizala freigeben.</span><span class="sxs-lookup"><span data-stu-id="e27ac-104">Using this sample, organizations can share SharePoint announcements with the first line and mobile workers on Kaizala.</span></span> <span data-ttu-id="e27ac-105">Diese Karte hat 3 Felder in Chat Karte-Anlagen anzeigen (In diesem Beispiel Fotostory mit Bildern), Titel und die Ankündigung Body (Beschreibung).</span><span class="sxs-lookup"><span data-stu-id="e27ac-105">This card has 3 fields in chat card view- Attachments( In this example, Photo story of images), Title and Announcement body (description).</span></span> <span data-ttu-id="e27ac-106">Dies wird als eine Karte Out-of-Box-Ankündigung an eine Gruppe Kaizala gesendet.</span><span class="sxs-lookup"><span data-stu-id="e27ac-106">This is sent to a Kaizala group as an out-of-box announcement card.</span></span>

<span data-ttu-id="e27ac-107">Die Kartenansicht Chat ist als unten</span><span class="sxs-lookup"><span data-stu-id="e27ac-107">The chat card view is as below</span></span>

<img src="SharepointAnnouncementImages/1.png" alt="Chat card view Logo" width="340" />

<span data-ttu-id="e27ac-108">Klicken Sie auf die Karte tippen fesselnden Ansicht ist, als unter</span><span class="sxs-lookup"><span data-stu-id="e27ac-108">On tapping the card, immersive view is as below</span></span>

<img src="SharepointAnnouncementImages/2.png" alt="immersive view Logo" width="180" />

<span data-ttu-id="e27ac-109">In diesem Szenario kann sich grob in 2 Schritte unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="e27ac-109">This scenario can be broadly divided into 2 steps:</span></span>
1. <span data-ttu-id="e27ac-110">Erstellen Sie eine Ankündigungsliste mit Spalten - Titel, Anlagen und Ankündigung body(description)</span><span class="sxs-lookup"><span data-stu-id="e27ac-110">Create an announcement list with columns- Title, attachments and announcement body(description)</span></span> 

    > <span data-ttu-id="e27ac-111">Hinweis: Rich-Text wird von Out-of-Box-Ankündigung Karte nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e27ac-111">Note: Rich text is not supported by out-of-box announcement card.</span></span> <span data-ttu-id="e27ac-112">Schalten Sie rich-Text für Sharepoint-Spalte, die Ankündigung body(description) beim Erstellen der Spalte hat.</span><span class="sxs-lookup"><span data-stu-id="e27ac-112">Switch off rich text for sharepoint column that has Announcement body(description) while creating that column.</span></span>

    <img src="SharepointAnnouncementImages/3.5.png" width="200" />

2. <span data-ttu-id="e27ac-113">Konfigurieren Sie Fluss so, dass, wenn ein neues Element erstellt oder vorhandenes Element wird in der Ankündigungsliste geändert, eine Karte Out-of-Box-Ankündigung an eine Gruppe Kaizala gesendet wird</span><span class="sxs-lookup"><span data-stu-id="e27ac-113">Configure Flow such that, when a new item is created or existing item is modified in announcement list, an out-of-box announcement card is sent to a Kaizala group</span></span>

    <img src="SharepointAnnouncementImages/3.png" alt="Sharepoint&Flow Logo" width="400" />

## <a name="implementation-steps"></a><span data-ttu-id="e27ac-114">Implementierungsschritte</span><span class="sxs-lookup"><span data-stu-id="e27ac-114">Implementation steps</span></span>


1. <span data-ttu-id="e27ac-115">[Ankündigung hinzufügen app](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) für SharePoint-Website (*wie unten*)</span><span class="sxs-lookup"><span data-stu-id="e27ac-115">[Add Announcement app](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) to SharePoint site(*as below*)</span></span>
     1. <span data-ttu-id="e27ac-116">Klicken Sie auf das einstellungssymbol</span><span class="sxs-lookup"><span data-stu-id="e27ac-116">Click on the settings icon</span></span>
     2.  <span data-ttu-id="e27ac-117">Klicken Sie auf App hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e27ac-117">Click on Add an App</span></span> 
     3.  <span data-ttu-id="e27ac-118">Wählen Sie aus der Liste der verfügbaren Apps Ankündigung-App</span><span class="sxs-lookup"><span data-stu-id="e27ac-118">Select Announcement App from the list of available Apps</span></span>
2. <span data-ttu-id="e27ac-119">Verwenden Sie das [hervorgehobene Content-Webpart](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*bei Bedarf für Visualisierung*)</span><span class="sxs-lookup"><span data-stu-id="e27ac-119">Use the [highlighted content web part](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*if necessary , for visualization*)</span></span>
3. <span data-ttu-id="e27ac-120">Laden Sie die [SharepointAnnouncementOnKaizala SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*Dies ist ein Flow-Paket*)</span><span class="sxs-lookup"><span data-stu-id="e27ac-120">Download the [SharepointAnnouncementOnKaizala-SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*This is a Flow package*)</span></span>
4. <span data-ttu-id="e27ac-121">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip Flow Microsoft-Konto</span><span class="sxs-lookup"><span data-stu-id="e27ac-121">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip to your Microsoft Flow account</span></span>
    > <span data-ttu-id="e27ac-122">Hinweis: Wenn Sie noch nie, Sharepoint oder Kaizala Verbindung mit der ersten [Hinzufügen von Verbindungen verwendet haben](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="e27ac-122">Note: If you have never used Sharepoint or Kaizala connection, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>
5. <span data-ttu-id="e27ac-123">Bearbeiten Sie den Ablauf (*wie unten*)</span><span class="sxs-lookup"><span data-stu-id="e27ac-123">Edit the Flow (*as below*)</span></span>
    1. <span data-ttu-id="e27ac-124">In der erste Block des Datenflusses</span><span class="sxs-lookup"><span data-stu-id="e27ac-124">In the first block of the Flow</span></span>
    
         1. <span data-ttu-id="e27ac-125">Geben Sie die Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="e27ac-125">Enter the site address</span></span>
         2. <span data-ttu-id="e27ac-126">Geben Sie den Namen der Liste (*Schritte zur Liste Name ist wie im folgenden*)</span><span class="sxs-lookup"><span data-stu-id="e27ac-126">Enter the List name (*steps to get List name is as below*)</span></span>
            - <span data-ttu-id="e27ac-127">Klicken Sie auf der Registerkarte der Website Inhalt auf der linken Ecke des Bildschirms</span><span class="sxs-lookup"><span data-stu-id="e27ac-127">Click on site contents tab on the left hand corner of the screen</span></span>
            - <span data-ttu-id="e27ac-128">Wählen Sie die Ankündigung aus, aus der Sie Ansagen an Kaizala senden möchten</span><span class="sxs-lookup"><span data-stu-id="e27ac-128">Select the announcement list from which you want to send announcements to Kaizala</span></span>
            - <span data-ttu-id="e27ac-129">Klicken Sie auf das einstellungssymbol für in der oberen rechten Ecke des Bildschirms</span><span class="sxs-lookup"><span data-stu-id="e27ac-129">Click on settings icon at the top right corner of the screen</span></span>
            - <span data-ttu-id="e27ac-130">Wechseln Sie zu Einstellungen für die Liste</span><span class="sxs-lookup"><span data-stu-id="e27ac-130">Go to List settings</span></span>
            - <span data-ttu-id="e27ac-131">Kopieren Sie die URL der Liste im Browser.</span><span class="sxs-lookup"><span data-stu-id="e27ac-131">Copy the URL of the list from the browser.</span></span>
            - <span data-ttu-id="e27ac-132">Die URL decodieren (Sie können die URL decodieren [hier](https://www.url-encode-decode.com/) )</span><span class="sxs-lookup"><span data-stu-id="e27ac-132">Decode the URL (you can decode the URL [here](https://www.url-encode-decode.com/) )</span></span>
        <img src="SharepointAnnouncementImages/4.PNG" alt="" width="500" />
      
    2. <span data-ttu-id="e27ac-133">In der zweite Block des Datenflusses</span><span class="sxs-lookup"><span data-stu-id="e27ac-133">In the second block of the Flow</span></span>
   
        <span data-ttu-id="e27ac-134">Ordnen Sie "Wert" Feld mit der Spaltentitel der Ankündigungsliste, die Ankündigung body(description) von dynamischen Inhalten hat.</span><span class="sxs-lookup"><span data-stu-id="e27ac-134">Map "value" field with column title of announcement list, that has announcement body(description) from Dynamic content.</span></span> <span data-ttu-id="e27ac-135">In den unten Beispiel ist der Spaltentitel "Ankündigung Body" </span><span class="sxs-lookup"><span data-stu-id="e27ac-135">In the below example, the column title is "Announcement Body"  </span></span><img src="SharepointAnnouncementImages/5.png" alt="" width="600" />
       
    3. <span data-ttu-id="e27ac-136">In den letzten Block mit den Ablauf</span><span class="sxs-lookup"><span data-stu-id="e27ac-136">In the last block of the Flow</span></span>
    
       <span data-ttu-id="e27ac-137">Wählen Sie den Namen der Gruppe aus der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="e27ac-137">Select the group name from dropdown.</span></span> <span data-ttu-id="e27ac-138">In diesem Beispiel ist "Everyone@Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="e27ac-138">In this Example it is "Everyone@Fabrikam"</span></span>
       <img src="SharepointAnnouncementImages/6.png" alt="" width="450" />
6. <span data-ttu-id="e27ac-139">Speichern Sie den Ablauf</span><span class="sxs-lookup"><span data-stu-id="e27ac-139">Save the flow</span></span>

<span data-ttu-id="e27ac-140">Ankündigung an gesendet der ausgewählten Gruppe Kaizala jedes Mal Flow ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e27ac-140">Announcement will be sent to the selected Kaizala group, each time flow is triggered.</span></span>

> <span data-ttu-id="e27ac-141">Hinweis: Textdatei wird als Anlage nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e27ac-141">Note: Text file is not supported as attachment</span></span>
