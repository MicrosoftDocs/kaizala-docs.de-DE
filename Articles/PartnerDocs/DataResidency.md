# <a name="data-residency-and-go-local-support-in-microsoft-kaizala"></a><span data-ttu-id="d1405-101">Daten Wohnsitz und lokale Unterstützung in Microsoft Kaizala</span><span class="sxs-lookup"><span data-stu-id="d1405-101">Data residency and go-local support in Microsoft Kaizala</span></span>

<span data-ttu-id="d1405-102">Ab April 2019 wird Microsoft Kaizala den regionalen Daten-Residency-Support über die Rechenzentren in Europa (EU), Asien-Pazifik (APAC), USA (USA) und Indien (IN) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d1405-102">Beginning April 2019, Microsoft Kaizala will provide regional data residency support through the datacenters in Europe (EU), Asia Pacific (APAC), United States (US), and India (IN).</span></span> <span data-ttu-id="d1405-103">Dies hat zur Folge, dass Kaizala-Kundendaten im Zusammenhang mit [Organisations Chats und Gruppen](https://support.office.com/article/organization-chats-and-groups-in-kaizala-c8a7855c-d232-4914-811c-f6708734dcc3) wie Nachrichten, Anlagen und Kaizala-Aktionen haben, die im Rechenzentrum ihrer Abrechnungs Region gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d1405-103">This means Kaizala customers will have data related to [organization chats and groups](https://support.office.com/article/organization-chats-and-groups-in-kaizala-c8a7855c-d232-4914-811c-f6708734dcc3) such as messages, attachments, and Kaizala actions stored in the datacenter of their billing region.</span></span>

<span data-ttu-id="d1405-104">Zusätzlich zur Unterstützung der Ziele von Data Residency innerhalb der Region können Kaizala-Dienst Datencenter auch Failover-und Notfallwiederherstellung über die Rechenzentren erleichtern.</span><span class="sxs-lookup"><span data-stu-id="d1405-104">In addition to supporting the goals of within-region data residency, Kaizala service datacenters will also facilitate failover and disaster recovery through the datacenters.</span></span>

## <a name="global-datacenter-footprint-with-data-residency-support"></a><span data-ttu-id="d1405-105">Globaler Datencenter-Footprint mit Data Residency-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d1405-105">Global datacenter footprint with data residency support</span></span>

<span data-ttu-id="d1405-106">Derzeit verfügt Kaizala über acht Rechenzentren (Primary und Backup) in drei Regionen und einem Land:</span><span class="sxs-lookup"><span data-stu-id="d1405-106">Currently, Kaizala has eight datacenters (primary and backup) in three regions and one country:</span></span>

- <span data-ttu-id="d1405-107">APAC (bedient Asien-Pazifik außer Indien)-Rechenzentren in Singapur und Hongkong</span><span class="sxs-lookup"><span data-stu-id="d1405-107">APAC (Serves Asia Pacific except India) - Datacenters in Singapore and Hong Kong</span></span>
- <span data-ttu-id="d1405-108">EMEA (EU, MEA)-Rechenzentren in Dublin und Amsterdam</span><span class="sxs-lookup"><span data-stu-id="d1405-108">EMEA (EU, MEA) - Datacenters in Dublin and Amsterdam</span></span>
- <span data-ttu-id="d1405-109">AMER (Nord-und Südamerika)-Rechenzentren in Texas und Illinois</span><span class="sxs-lookup"><span data-stu-id="d1405-109">AMER (North and South Americas) - Datacenters in Texas and Illinois</span></span>
- <span data-ttu-id="d1405-110">Indien (go-local)-Rechenzentren in Chennai und Pune</span><span class="sxs-lookup"><span data-stu-id="d1405-110">India (Go-Local) - Datacenters in Chennai and Pune</span></span>

<span data-ttu-id="d1405-111">Neben der Bereitstellung von COMPUTE und Storage bietet Kaizala auch Unterstützung für Daten Residency, robustes Failover und Notfallwiederherstellung für Unternehmenskunden.</span><span class="sxs-lookup"><span data-stu-id="d1405-111">In addition to providing compute and storage, Kaizala also provides data residency support, robust failover, and disaster recovery support to enterprise customers.</span></span> <span data-ttu-id="d1405-112">Außerdem können diese Skalierungseinheiten sowohl für Unternehmens-als auch für allgemeine Kunden eine verbesserte Konnektivität und Messagingleistung sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="d1405-112">Also, these scale units help ensure improved connectivity and messaging performance to both enterprise and general customers.</span></span> 

![Grafik mit Daten Wohnsitz und lokalen Geo-Begrenzungen in Kaizala](Images/data-residency-geo-boundaries.png)

## <a name="how-is-data-stored-in-kaizala"></a><span data-ttu-id="d1405-114">Wie werden Daten in Kaizala gespeichert?</span><span class="sxs-lookup"><span data-stu-id="d1405-114">How is data stored in Kaizala</span></span>

<span data-ttu-id="d1405-115">Kaizala speichert Daten basierend auf den Datentypen der Nachrichten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="d1405-115">Kaizala stores data differently based on data types of the messages.</span></span>

- <span data-ttu-id="d1405-116">**Chats, likes und comments** -alle Nachrichten, Vorlieben und Kommentardaten, die zu Organisationsgruppen-oder org 1:1-Chats gehören, werden in einem sicheren Office 365-und Azure powered Chat-Dienst gespeichert, der auf der Grundlage ihres Abrechnungs Landes Regional begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="d1405-116">**Chats, likes, and comments** - All messages, likes, and comment data belonging to organization group or org 1:1 chats are stored in a secure Office 365 and Azure powered chat service that is regionally bounded for tenants, based on their billing country.</span></span>
- <span data-ttu-id="d1405-117">**Attachments** – alle Anlagen befinden sich zusammen mit Chatnachrichten in derselben Daten Grenze.</span><span class="sxs-lookup"><span data-stu-id="d1405-117">**Attachments** - All attachments are co-located along with chat messages in the same data boundary.</span></span>
- <span data-ttu-id="d1405-118">**Kaizala Action Cards** -alle Kaizala-Aktionskarten Daten, die Metadaten, Aktionspaket und Antwort Berichtsdaten enthalten, sind mit Chatdienst in derselben Daten Grenze zusammengefunden.</span><span class="sxs-lookup"><span data-stu-id="d1405-118">**Kaizala Action cards** - All Kaizala Action card data, which includes metadata, action package, and response report data, are co-located with chat service in the same data boundary.</span></span>
- <span data-ttu-id="d1405-119">**Calling** -Transient, Kaizala-Anrufdaten werden nicht in Rechenzentren gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1405-119">**Calling** - Being transient, Kaizala calling data is not stored in datacenters.</span></span> <span data-ttu-id="d1405-120">Anrufprotokolle folgen jedoch denselben Daten Wohnsitz wie Chats.</span><span class="sxs-lookup"><span data-stu-id="d1405-120">However, call logs follow the same data residency as chats.</span></span>

### <a name="example"></a><span data-ttu-id="d1405-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d1405-121">Example</span></span>

<span data-ttu-id="d1405-122">Contoso hat sein Office 365-Abrechnungs Land in der EU.</span><span class="sxs-lookup"><span data-stu-id="d1405-122">Contoso has its Office 365 billing country in EU.</span></span> <span data-ttu-id="d1405-123">Contoso hat sich auf Kaizala im April 2019 angemeldet, und alle Kern Daten, einschließlich Chats, Anlagen und Aktionskarten, werden in Ruhe ausschließlich in EU-Einheiten (Dublin und Amsterdam) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1405-123">Contoso has signed up on Kaizala in April 2019 and all of its core data including chats, attachments and action cards will be stored at rest exclusively in EU scale units (Dublin and Amsterdam).</span></span>

## <a name="what-is-in-store-in-future"></a><span data-ttu-id="d1405-124">Was ist in der Zukunft?</span><span class="sxs-lookup"><span data-stu-id="d1405-124">What is in store in future</span></span>

- <span data-ttu-id="d1405-125">Onboarding auf der Seite für die **Datenspeicherort** -für Unternehmen ist der Datenspeicherort für unterschiedliche Arbeitsauslastungen von Office 365 unter dem Office 365-Administratorportal unter Home\Organizational-Profil sichtbar.</span><span class="sxs-lookup"><span data-stu-id="d1405-125">**Onboarding on to data location page** - For enterprises, the data location for different workloads of Office 365 is visible under Office 365 admin portal under Home\Organizational Profile.</span></span> <span data-ttu-id="d1405-126">Die Möglichkeit zur Onboarding-Kaizala auf der Seite Datenspeicherort im Administratorportal wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1405-126">The ability to onboard Kaizala to the data location page on admin portal is forthcoming.</span></span> <span data-ttu-id="d1405-127">In diesem Abschnitt finden Sie Updates.</span><span class="sxs-lookup"><span data-stu-id="d1405-127">Watch this section for updates.</span></span>
- <span data-ttu-id="d1405-128">**Neue Rechenzentren** – das Kaizala-Team beruht ständig auf der Erweiterung der Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="d1405-128">**New datacenters** - The Kaizala team is continuously looking at expansion based on providing the best user experience to users.</span></span> <span data-ttu-id="d1405-129">Wenn Sie einen geschäftlichen Fall haben, veröffentlichen Sie Ihre Fragen in unserer [TechNet-Community](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala).</span><span class="sxs-lookup"><span data-stu-id="d1405-129">If you have a business case, then post your questions in our [Technet community](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala).</span></span>

## <a name="faqs"></a><span data-ttu-id="d1405-130">FAQs</span><span class="sxs-lookup"><span data-stu-id="d1405-130">FAQs</span></span>

### <a name="what-does-it-mean-for-existing-enterprise-customers"></a><span data-ttu-id="d1405-131">Was bedeutet dies für bestehende Unternehmenskunden?</span><span class="sxs-lookup"><span data-stu-id="d1405-131">What does it mean for existing enterprise customers?</span></span>

<span data-ttu-id="d1405-132">Bestehende Kunden in Indien haben bereits Ihren Daten Wohnsitz in Indien.</span><span class="sxs-lookup"><span data-stu-id="d1405-132">Existing customers in India already have their data residency within India.</span></span> <span data-ttu-id="d1405-133">Daten für alle nicht von Indien bestehenden Mandanten bleiben jedoch weiterhin am Gruppen Standort (basierend auf dem Landescode des Erstellers).</span><span class="sxs-lookup"><span data-stu-id="d1405-133">Data for all non-India existing tenants however will continue to stay in the group location (based on creator’s country code).</span></span> <span data-ttu-id="d1405-134">Nach dem 2019. April beginnen jedoch alle neueren Organisationsgruppen und Nachrichten vorhandener Organisationsgruppen oder Chats nach Daten Wohnsitz basierend auf der Abrechnungs Region des Mandanten.</span><span class="sxs-lookup"><span data-stu-id="d1405-134">However after April 2019, all the newer organization groups and messages of existing organization groups or chats will start following data residency based on the tenant’s billing region.</span></span>

### <a name="what-does-it-mean-for-new-enterprise-customers"></a><span data-ttu-id="d1405-135">Was bedeutet dies für neue Enterprise-Kunden?</span><span class="sxs-lookup"><span data-stu-id="d1405-135">What does it mean for new enterprise customers?</span></span>

<span data-ttu-id="d1405-136">Der Daten Wohnsitz wird automatisch für alle Kunden angewendet, die sich nach April 2019 auf Kaizala registrieren.</span><span class="sxs-lookup"><span data-stu-id="d1405-136">Data residency will be automatically applicable for all the customers who sign up on Kaizala after April 2019.</span></span> <span data-ttu-id="d1405-137">Darüber hinaus sollte auf den neuesten Android-oder iOS-App-Versionen der Daten Wohnsitz auf Aktionskarten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1405-137">Additionally, data residency on action cards should be applicable on the latest Android or iOS app versions.</span></span>
 
### <a name="i-do-have-more-questions-who-do-i-reach-out-to"></a><span data-ttu-id="d1405-138">Ich habe noch weitere Fragen.</span><span class="sxs-lookup"><span data-stu-id="d1405-138">I do have more questions.</span></span> <span data-ttu-id="d1405-139">An wen kann ich mich wenden?</span><span class="sxs-lookup"><span data-stu-id="d1405-139">Who do I reach out to?</span></span>

<span data-ttu-id="d1405-140">Wenn Sie weitere Fragen haben, wenden Sie sich an Ihr Account-Team oder unsere [TechNet-Community](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala).</span><span class="sxs-lookup"><span data-stu-id="d1405-140">In case of more questions, contact your account team or our [Technet community](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala).</span></span> <span data-ttu-id="d1405-141">Darüber hinaus können Sie in [Kaizalafeedback@microsoft.com](mailto:kaizalafeedback@microsoft.com)schreiben.</span><span class="sxs-lookup"><span data-stu-id="d1405-141">Additionally, you can write to [Kaizalafeedback@microsoft.com](mailto:kaizalafeedback@microsoft.com).</span></span>







