# <a name="generate-tenant-level-user-token"></a><span data-ttu-id="c55de-101">Generieren eines Benutzertokens auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="c55de-101">Generate tenant-level user token</span></span>

<span data-ttu-id="c55de-102">Ein Benutzer Aktualisierungstoken auf Mandantenebene kann verwendet werden, um Zugriff auf alle Gruppen des Benutzers zu gewähren, in denen der Benutzer ein Administrator ist. Für einen Mandanten Benutzer gewährt dieses Token Zugriff auf alle Gruppen für eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="c55de-102">Tenant-level user refresh token can be used to grant access to all the user's groups where user is an admin. For a Tenant user, this token grants access to all the groups for an organization.</span></span>

## <a name="steps-to-generate-tenant-level-user-token"></a><span data-ttu-id="c55de-103">Schritte zum Generieren des Benutzertokens auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="c55de-103">Steps to generate Tenant-level user token</span></span>
*   <span data-ttu-id="c55de-104">**Schritt 1: Registrieren eines Connectors für Entwickler**</span><span class="sxs-lookup"><span data-stu-id="c55de-104">**Step 1: Developer registers a Connector**</span></span>

    *   <span data-ttu-id="c55de-105">Entwickler navigiert zu Kaizala Management Portal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="c55de-105">Developer navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="c55de-106">Anmelden mit einem vorhandenen Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="c55de-106">Log in using an existing Office365 account</span></span>
    *   <span data-ttu-id="c55de-107">Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.</span><span class="sxs-lookup"><span data-stu-id="c55de-107">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="c55de-108">Telefonnummer eingeben</span><span class="sxs-lookup"><span data-stu-id="c55de-108">Enter Phone number</span></span>
        *   <span data-ttu-id="c55de-109">Tippen Sie auf "PIN generieren".</span><span class="sxs-lookup"><span data-stu-id="c55de-109">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="c55de-110">ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="c55de-110">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="c55de-111">Tippen Sie im linken Menü auf "Connectors".</span><span class="sxs-lookup"><span data-stu-id="c55de-111">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="c55de-112">Tippen Sie auf "Connector hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c55de-112">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="c55de-113">Registrieren eines Connectors für das Drittanbietersystem, das die API verwendet</span><span class="sxs-lookup"><span data-stu-id="c55de-113">Register a connector for the 3rd party system that will use the API</span></span>
        *   <span data-ttu-id="c55de-114">Geben Sie den Namen des Connectors und weitere Details ein.</span><span class="sxs-lookup"><span data-stu-id="c55de-114">Enter the name of the Connector and other details.</span></span> <span data-ttu-id="c55de-115">Tippen Sie auf weiter</span><span class="sxs-lookup"><span data-stu-id="c55de-115">Tap on Continue</span></span>
        *   <span data-ttu-id="c55de-116">Wählen Sie Berechtigungen aus, die für den Connector vorgesehen sind, um Zugriff auf</span><span class="sxs-lookup"><span data-stu-id="c55de-116">Select permissions that is intended for the Connector to have access to</span></span>
        *   <span data-ttu-id="c55de-117">Tippen Sie auf Verbinder erstellen.</span><span class="sxs-lookup"><span data-stu-id="c55de-117">Tap on Create Connector</span></span>
    *   <span data-ttu-id="c55de-118">Beachten Sie die ID & Secret, die generiert und im Portal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c55de-118">Note the ID & Secret that get generated and displayed on the portal</span></span>

*   <span data-ttu-id="c55de-119">**Schritt 2: Mandanten Benutzer "erteilt" den Connector-Zugriff auf alle Gruppen, für die er Administrator ist**</span><span class="sxs-lookup"><span data-stu-id="c55de-119">**Step 2: Tenant User “grants” the Connector access to all groups that he is admin to**</span></span>

    *   <span data-ttu-id="c55de-120">Benutzer navigiert zu Kaizala Management Portal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="c55de-120">User navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="c55de-121">Anmelden mit einem vorhandenen Office365-Konto (SKU-festgelegt)</span><span class="sxs-lookup"><span data-stu-id="c55de-121">Log in using an existing Office365 (SKU TBD) account</span></span>
    *   <span data-ttu-id="c55de-122">Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.</span><span class="sxs-lookup"><span data-stu-id="c55de-122">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="c55de-123">Telefonnummer eingeben</span><span class="sxs-lookup"><span data-stu-id="c55de-123">Enter Phone number</span></span>
        *   <span data-ttu-id="c55de-124">Tippen Sie auf "PIN generieren".</span><span class="sxs-lookup"><span data-stu-id="c55de-124">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="c55de-125">ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="c55de-125">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="c55de-126">Tippen Sie im linken Menü auf "Connectors".</span><span class="sxs-lookup"><span data-stu-id="c55de-126">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="c55de-127">Tippen Sie auf den Namen des Connectors, auf den der Connector zugreifen muss.</span><span class="sxs-lookup"><span data-stu-id="c55de-127">Tap on the connector name which needs to be accessed by the Connector</span></span>
    *   <span data-ttu-id="c55de-128">Tippen Sie auf "Benutzertoken generieren".</span><span class="sxs-lookup"><span data-stu-id="c55de-128">Tap on “Generate user token”</span></span>
    *   <span data-ttu-id="c55de-129">Hinweis das Aktualisierungs Token, das generiert und im Portal angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="c55de-129">Note the Refresh Token that gets generated and displayed on the portal</span></span>

*   <span data-ttu-id="c55de-130">**Schritt 3: Benutzer Freigabe des Aktualisierungs Tokens mit dem App-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="c55de-130">**Step 3: User shares the Refresh Token with the App Developer**</span></span>

    *   <span data-ttu-id="c55de-131">Der Administrator muss das in Schritt 2 erhaltene Aktualisierungstoken manuell mit dem App-Entwickler freigeben.</span><span class="sxs-lookup"><span data-stu-id="c55de-131">Admin needs to manually share the refresh token received in Step 2 with the app developer</span></span>

*   <span data-ttu-id="c55de-132">**Schritt 4: App-Entwickler Ruft die Kaizala-Plattform-Rest-API zum Generieren von Zugriffs Token**</span><span class="sxs-lookup"><span data-stu-id="c55de-132">**Step 4: App Developer calls the Kaizala Platform Rest API to generate Access Token**</span></span>

    *   <span data-ttu-id="c55de-133">Entwickler können nun das Aktualisierungstoken verwenden.</span><span class="sxs-lookup"><span data-stu-id="c55de-133">Developer can now use the Refresh token.</span></span> <span data-ttu-id="c55de-134">eine Connector-ID und ein Connector Secret, um die REST-API aufzurufen, um Zugriffs Token zu generieren (Weitere Informationen finden Sie weiter unten)</span><span class="sxs-lookup"><span data-stu-id="c55de-134">a Connector ID and Connector Secret to call the REST API inorder to generate Access Token (more info below)</span></span>

