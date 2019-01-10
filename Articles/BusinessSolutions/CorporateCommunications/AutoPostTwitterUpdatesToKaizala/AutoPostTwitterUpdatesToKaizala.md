# <a name="auto-post-twitter-updates-to-kaizala"></a><span data-ttu-id="8d818-101">Updates zu Kaizala Auto-Post Twitter (engl.)</span><span class="sxs-lookup"><span data-stu-id="8d818-101">Auto-Post Twitter updates to Kaizala</span></span>

<span data-ttu-id="8d818-102">Buchen, um Mitarbeiter Seiten Twitter ist Teil der Geschäftsalltag, jedoch müssen die gleiche Informationen mehrmals buchen ist ziemlich komplex.</span><span class="sxs-lookup"><span data-stu-id="8d818-102">Posting to Twitter employee pages is part of daily business, but having to post the same information multiple times is quite difficult.</span></span> <span data-ttu-id="8d818-103">Förderung der Mitarbeiter soziale Medien-Updates gemeinsam nutzen, wenn keine weiteren ordnungsgemäß kann erheblich des Unternehmens Folgendes erweitern.</span><span class="sxs-lookup"><span data-stu-id="8d818-103">Encouraging employees to share social media updates, when done properly can dramatically expand company's following.</span></span> 

<span data-ttu-id="8d818-104">In diesem beispiellösung speichert Ihrer Termine durch die automatische-Veröffentlichung der Statusupdates von Ihrem Konto offizielle Twitter auf Kaizala Gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d818-104">This sample solution saves your time by auto-posting the status updates from your official twitter account to Kaizala groups.</span></span> <span data-ttu-id="8d818-105">Eine Ankündigung Karte werden gesendet, um die Gruppe aus, wenn eine oder alle der unten Trigger auftreten</span><span class="sxs-lookup"><span data-stu-id="8d818-105">An announcement card is sent to the group when one or all the below triggers occur</span></span>

1. <span data-ttu-id="8d818-106">Ein neuer Tweet wird auf einen bestimmten Twitter Ziehpunkt E.g.,"@InsideFabrikam gebucht"</span><span class="sxs-lookup"><span data-stu-id="8d818-106">A new tweet is posted on a specific twitter handle E.g.,"@InsideFabrikam"</span></span>

2. <span data-ttu-id="8d818-107">Ein Beitrag ist neu in diesem Twitter Handle tweeted</span><span class="sxs-lookup"><span data-stu-id="8d818-107">A post is re-tweeted in that twitter handle</span></span> 
    
3. <span data-ttu-id="8d818-108">Ein Beitrag ist eine bestimmte Hashtag E.g.,"#EmployeeEngagement"</span><span class="sxs-lookup"><span data-stu-id="8d818-108">A post has a specific hashtag E.g.,"#EmployeeEngagement"</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/6.png" alt="Tweet" width="400" />

<span data-ttu-id="8d818-109">Diese Karte verfügt über drei Felder-Karte Titel Anlagen (Bilder, Videos und GIF) und den Text (Beschreibung).</span><span class="sxs-lookup"><span data-stu-id="8d818-109">This card has three fields- card title, attachments(images, videos or GIF) and body (description).</span></span> <span data-ttu-id="8d818-110">Die Ankündigung Nachrichtentext enthält die Twitter-URL und auf diese URL tippen, würde an Statusseite auf Twitter Benutzer weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8d818-110">The announcement body has the twitter URL and on tapping this URL, users would be directed to status page on twitter.</span></span>

> <span data-ttu-id="8d818-111">Hinweis: Im Fall eines WAN-Video oder GIF, wird in der Miniaturansicht in Kartenansicht Chat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d818-111">Note: In case of Video or GIF, thumbnail is shown in chat card view</span></span>

<span data-ttu-id="8d818-112">Chat-Karte anzeigen:</span><span class="sxs-lookup"><span data-stu-id="8d818-112">Chat card View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

<span data-ttu-id="8d818-113">Fesselnden anzeigen:</span><span class="sxs-lookup"><span data-stu-id="8d818-113">Immersive View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/2.png" alt="Immersive view Logo" width="190" />

<span data-ttu-id="8d818-114">In diesem Szenario wird Ablauf die Karte auf eine ausgewählte Gruppe in Kaizala senden.</span><span class="sxs-lookup"><span data-stu-id="8d818-114">In this scenario, Flow is used to send the card to a selected group in Kaizala.</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/3.png" alt="Flow+Twitter>Kaizala" width="500" />

## <a name="implementation-steps"></a><span data-ttu-id="8d818-115">Implementierungsschritte:</span><span class="sxs-lookup"><span data-stu-id="8d818-115">Implementation steps:</span></span>

1. <span data-ttu-id="8d818-116">Laden Sie die [AutoPostTwitterUpdatesToKaizala SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/AutoPostTwitterUpdatesToKaizala/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*Dies enthält Flow-Paket*)</span><span class="sxs-lookup"><span data-stu-id="8d818-116">Download the [AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/AutoPostTwitterUpdatesToKaizala/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*This contains Flow Package*)</span></span>

2. <span data-ttu-id="8d818-117">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) "AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip" Flow Microsoft-Konto</span><span class="sxs-lookup"><span data-stu-id="8d818-117">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip" to your Microsoft Flow account</span></span>

     > <span data-ttu-id="8d818-118">Hinweis-Wenn Sie noch nie verwendet haben, Twitter oder Kaizala Verbindungen, die erste [Verbindungen hinzuzufügen](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span><span class="sxs-lookup"><span data-stu-id="8d818-118">Note- If you have never used Twitter or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>

3. <span data-ttu-id="8d818-119">Bearbeiten Sie den Ablauf (*wie unten*)</span><span class="sxs-lookup"><span data-stu-id="8d818-119">Edit the Flow (*as Below*)</span></span>

    1.  <span data-ttu-id="8d818-120">In der erste Block des Datenflusses</span><span class="sxs-lookup"><span data-stu-id="8d818-120">In the first block of the Flow</span></span>
    
        <span data-ttu-id="8d818-121">Geben Sie das Handle Twitter, oder geben Sie die Hashtag oder beides</span><span class="sxs-lookup"><span data-stu-id="8d818-121">Enter the twitter handle or enter the hashtag, or both</span></span>
        
        <img src="AutoPostTwitterUpdatesToKaizalaImages/4.PNG" alt="Firstblock>Kaizala" width="400" />
    
    2.  <span data-ttu-id="8d818-122">In den letzten Block mit den Ablauf</span><span class="sxs-lookup"><span data-stu-id="8d818-122">In the last block of the Flow</span></span>
      
        1. <span data-ttu-id="8d818-123">Wählen Sie den Namen der Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="8d818-123">Select the group name</span></span> 
    
        2. <span data-ttu-id="8d818-124">Geben Sie den Titel.</span><span class="sxs-lookup"><span data-stu-id="8d818-124">Enter the title.</span></span> <span data-ttu-id="8d818-125">Der Titel wird für Benutzer in Chat Kartenansicht sichtbar sein.</span><span class="sxs-lookup"><span data-stu-id="8d818-125">The title will be visible to users in chat card view.</span></span> <span data-ttu-id="8d818-126">Z. B. "InsideFabrikam"</span><span class="sxs-lookup"><span data-stu-id="8d818-126">E.g., "InsideFabrikam"</span></span>
     
        <img src="AutoPostTwitterUpdatesToKaizalaImages/5.PNG" alt="Flow+Twitter>Kaizala" width="400" />
     
4. <span data-ttu-id="8d818-127">Speichern Sie den Ablauf</span><span class="sxs-lookup"><span data-stu-id="8d818-127">Save the flow</span></span>

<span data-ttu-id="8d818-128">Ankündigung wird an der ausgewählten Gruppe Kaizala jedes Mal gesendet, den Fluss ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8d818-128">Announcement will be sent to the selected Kaizala group, each time Flow is triggered.</span></span>

> <span data-ttu-id="8d818-129">Hinweis: im Fall eines WAN-Tweets durch Umfragen/Speicherort nur der Umfrage Frage/Tweet Text wird angezeigt, in die Karte, nicht die Umfrage Optionen oder den Speicherort Tweet</span><span class="sxs-lookup"><span data-stu-id="8d818-129">Note:In case of tweets with polls/location only the poll question/tweet text will show up in the card, not the poll options or the tweet location</span></span>

> <span data-ttu-id="8d818-130">Hinweis: Überprüfen Sie mit Ihren IT-Administrator bei einer [DLP-Richtlinie](https://docs.microsoft.com/en-us/flow/prevent-data-loss) in Ihrer Organisation für Twitter festgelegt</span><span class="sxs-lookup"><span data-stu-id="8d818-130">Note: Please check with your IT admin in case of any [DLP policy](https://docs.microsoft.com/en-us/flow/prevent-data-loss) set by your organization for Twitter</span></span>
