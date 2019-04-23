# <a name="auto-post-twitter-updates-to-kaizala"></a><span data-ttu-id="d25b8-101">Automatisches Veröffentlichen von Twitter-Updates für Kaizala</span><span class="sxs-lookup"><span data-stu-id="d25b8-101">Auto-Post Twitter updates to Kaizala</span></span>

<span data-ttu-id="d25b8-102">Posting to Twitter Employee Pages ist Teil des täglichen Geschäfts, aber es ist schwierig, dieselben Informationen mehrmals veröffentlichen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d25b8-102">Posting to Twitter employee pages is part of daily business, but having to post the same information multiple times is quite difficult.</span></span> <span data-ttu-id="d25b8-103">Wenn Sie Mitarbeiter dazu ermuntern, Social Media-Updates zu teilen, können Sie die folgenden Funktionen drastisch erweitern.</span><span class="sxs-lookup"><span data-stu-id="d25b8-103">Encouraging employees to share social media updates, when done properly can dramatically expand company's following.</span></span> 

<span data-ttu-id="d25b8-104">Diese Beispiellösung spart Ihnen Zeit, indem Sie tweets von Ihrem offiziellen Twitter-Konto zu Kaizala-Gruppen automatisch veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d25b8-104">This sample solution saves your time by auto-posting Tweets from your official Twitter account to Kaizala groups.</span></span> <span data-ttu-id="d25b8-105">Eine Ansage Karte wird an die Gruppe gesendet, wenn ein oder alle der folgenden Auslöser auftreten.</span><span class="sxs-lookup"><span data-stu-id="d25b8-105">An announcement card is sent to the group when one or all the below triggers occur</span></span>

1. <span data-ttu-id="d25b8-106">Ein neuer Tweet wird in einem bestimmten Twitter-handle veröffentlicht, z. b. "@InsideFabrikam"</span><span class="sxs-lookup"><span data-stu-id="d25b8-106">A new tweet is posted on a specific Twitter handle E.g.,"@InsideFabrikam"</span></span>

2. <span data-ttu-id="d25b8-107">Ein Beitrag wird in diesem Twitter-handle erneut tweeted</span><span class="sxs-lookup"><span data-stu-id="d25b8-107">A post is re-tweeted in that Twitter handle</span></span> 
    
3. <span data-ttu-id="d25b8-108">Ein Beitrag hat einen bestimmten hashtag, z. b. "#EmployeeEngagement"</span><span class="sxs-lookup"><span data-stu-id="d25b8-108">A post has a specific hashtag E.g.,"#EmployeeEngagement"</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/6.png" alt="Tweet" width="400" />

<span data-ttu-id="d25b8-109">Diese Karte hat drei Felder: Kartentitel, Anlagen (Bilder, Videos oder GIF) und Body (Beschreibung).</span><span class="sxs-lookup"><span data-stu-id="d25b8-109">This card has three fields- card title, attachments(images, videos or GIF) and body (description).</span></span> <span data-ttu-id="d25b8-110">Der Ankündigungstext hat die Twitter-URL und beim Tippen auf diese URL werden Benutzer auf die Statusseite auf Twitter umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d25b8-110">The announcement body has the Twitter URL and on tapping this URL, users would be directed to status page on Twitter.</span></span>

> <span data-ttu-id="d25b8-111">Hinweis: bei Video-oder GIF-Bildern wird die Miniaturansicht in der Chat Kartenansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d25b8-111">Note: In case of Video or GIF, thumbnail is shown in chat card view</span></span>

<span data-ttu-id="d25b8-112">Chat Kartenansicht:</span><span class="sxs-lookup"><span data-stu-id="d25b8-112">Chat card View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

<span data-ttu-id="d25b8-113">Immersive Ansicht:</span><span class="sxs-lookup"><span data-stu-id="d25b8-113">Immersive View:</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/2.png" alt="Immersive view Logo" width="190" />

<span data-ttu-id="d25b8-114">In diesem Szenario wird Flow verwendet, um die Karte an eine ausgewählte Gruppe in Kaizala zu senden.</span><span class="sxs-lookup"><span data-stu-id="d25b8-114">In this scenario, Flow is used to send the card to a selected group in Kaizala.</span></span>

<img src="AutoPostTwitterUpdatesToKaizalaImages/3.png" alt="Flow+Twitter>Kaizala" width="500" />

## <a name="implementation-steps"></a><span data-ttu-id="d25b8-115">Implementierungsschritte:</span><span class="sxs-lookup"><span data-stu-id="d25b8-115">Implementation steps:</span></span>

1. <span data-ttu-id="d25b8-116">Laden Sie die [AutoPostTwitterUpdatesToKaizala-SolutionPackage. zip](https://aka.ms/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*Dieses enthält Flow-Paket*)</span><span class="sxs-lookup"><span data-stu-id="d25b8-116">Download the [AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip](https://aka.ms/AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip) (*This contains Flow Package*)</span></span>

2. <span data-ttu-id="d25b8-117">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "AutoPostTwitterUpdatesToKaizala-SolutionPackage. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="d25b8-117">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "AutoPostTwitterUpdatesToKaizala-SolutionPackage.zip" to your Microsoft Flow account</span></span>

     > <span data-ttu-id="d25b8-118">Hinweis: Wenn Sie nie Twitter-oder Kaizala-Verbindungen verwendet haben, fügen Sie zunächst [Verbindungen hinzu](https://docs.microsoft.com/en-us/flow/add-manage-connections) .</span><span class="sxs-lookup"><span data-stu-id="d25b8-118">Note- If you have never used Twitter or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>

3. <span data-ttu-id="d25b8-119">Bearbeiten des Flusses (nach*folgend*)</span><span class="sxs-lookup"><span data-stu-id="d25b8-119">Edit the Flow (*as Below*)</span></span>

    1.  <span data-ttu-id="d25b8-120">Im ersten Block des Flusses</span><span class="sxs-lookup"><span data-stu-id="d25b8-120">In the first block of the Flow</span></span>
    
        <span data-ttu-id="d25b8-121">Geben Sie den Twitter-Handle ein, oder geben Sie den hashtag ein.</span><span class="sxs-lookup"><span data-stu-id="d25b8-121">Enter the Twitter handle or enter the hashtag, or both</span></span>
        
        <img src="AutoPostTwitterUpdatesToKaizalaImages/4.PNG" alt="Firstblock>Kaizala" width="400" />
    
    2.  <span data-ttu-id="d25b8-122">Im letzten Block des Flusses</span><span class="sxs-lookup"><span data-stu-id="d25b8-122">In the last block of the Flow</span></span>
      
        1. <span data-ttu-id="d25b8-123">Wählen Sie den Gruppennamen aus.</span><span class="sxs-lookup"><span data-stu-id="d25b8-123">Select the group name</span></span> 
    
        2. <span data-ttu-id="d25b8-124">Geben Sie den Titel ein.</span><span class="sxs-lookup"><span data-stu-id="d25b8-124">Enter the title.</span></span> <span data-ttu-id="d25b8-125">Der Titel ist für Benutzer in der Chat Kartenansicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="d25b8-125">The title will be visible to users in chat card view.</span></span> <span data-ttu-id="d25b8-126">Beispielsweise "InsideFabrikam"</span><span class="sxs-lookup"><span data-stu-id="d25b8-126">E.g., "InsideFabrikam"</span></span>
     
        <img src="AutoPostTwitterUpdatesToKaizalaImages/5.PNG" alt="Flow+Twitter>Kaizala" width="400" />
     
4. <span data-ttu-id="d25b8-127">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="d25b8-127">Save the flow</span></span>

<span data-ttu-id="d25b8-128">Die Ansage wird an die ausgewählte Kaizala-Gruppe gesendet, und jeder Zeitablauf wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d25b8-128">Announcement will be sent to the selected Kaizala group, each time Flow is triggered.</span></span>

> <span data-ttu-id="d25b8-129">Hinweis: bei Tweets mit Umfragen/Standort wird nur die Umfrage-Frage/der Tweet-Text in der Karte angezeigt, nicht die Abstimmungsoptionen oder der Tweet-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d25b8-129">Note:In case of tweets with polls/location only the poll question/tweet text will show up in the card, not the poll options or the tweet location</span></span>

> <span data-ttu-id="d25b8-130">Hinweis: erkundigen Sie sich bei Ihrem IT-Administrator im Falle einer [DLP-Richtlinie](https://docs.microsoft.com/en-us/flow/prevent-data-loss) , die von Ihrer Organisation für Twitter festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d25b8-130">Note: Please check with your IT admin in case of any [DLP policy](https://docs.microsoft.com/en-us/flow/prevent-data-loss) set by your organization for Twitter</span></span>
