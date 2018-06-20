# <a name="generate-tenant-level-user-token"></a><span data-ttu-id="6936e-101">Benutzertoken auf Mandantenebene generieren</span><span class="sxs-lookup"><span data-stu-id="6936e-101">Generate tenant-level user token</span></span>

<span data-ttu-id="6936e-102">Aktualisierungstoken auf Mandantenebene Benutzer kann verwendet werden, gewähren Zugriff zu Gruppen des Benutzers, in dem Benutzer Administrator ist Für einen Benutzer Mandanten gewährt dieses Token Zugriff auf alle Gruppen für eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="6936e-102">Tenant-level user refresh token can be used to grant access to all the user's groups where user is an admin. For a Tenant user, this token grants access to all the groups for an organization.</span></span>

## <a name="steps-to-generate-tenant-level-user-token"></a><span data-ttu-id="6936e-103">Schritte zum Generieren von Benutzertoken auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="6936e-103">Steps to generate Tenant-level user token</span></span>
*   <span data-ttu-id="6936e-104">**Schritt 1: Entwickler registriert einen Connector**</span><span class="sxs-lookup"><span data-stu-id="6936e-104">**Step 1: Developer registers a Connector**</span></span>

    *   <span data-ttu-id="6936e-105">Entwickler navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="6936e-105">Developer navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="6936e-106">Melden Sie sich mit einem vorhandenen Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="6936e-106">Log in using an existing Office365 account</span></span>
    *   <span data-ttu-id="6936e-107">Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal</span><span class="sxs-lookup"><span data-stu-id="6936e-107">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="6936e-108">Geben Sie Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="6936e-108">Enter Phone number</span></span>
        *   <span data-ttu-id="6936e-109">Tippen Sie auf "PIN generieren"</span><span class="sxs-lookup"><span data-stu-id="6936e-109">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="6936e-110">Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen</span><span class="sxs-lookup"><span data-stu-id="6936e-110">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="6936e-111">Tippen Sie auf "Connectors" im linken Menü</span><span class="sxs-lookup"><span data-stu-id="6936e-111">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="6936e-112">Tippen Sie auf "Connector hinzufügen"</span><span class="sxs-lookup"><span data-stu-id="6936e-112">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="6936e-113">Registrieren Sie einen Connector für das 3. Partei-System, das die API verwenden</span><span class="sxs-lookup"><span data-stu-id="6936e-113">Register a connector for the 3rd party system that will use the API</span></span>
        *   <span data-ttu-id="6936e-114">Geben Sie den Namen des Connectors und andere Details.</span><span class="sxs-lookup"><span data-stu-id="6936e-114">Enter the name of the Connector and other details.</span></span> <span data-ttu-id="6936e-115">Tippen Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="6936e-115">Tap on Continue</span></span>
        *   <span data-ttu-id="6936e-116">Wählen Sie Berechtigungen, mit denen bestimmt ist für den Zugriff auf den Connector</span><span class="sxs-lookup"><span data-stu-id="6936e-116">Select permissions that is intended for the Connector to have access to</span></span>
        *   <span data-ttu-id="6936e-117">Tippen Sie auf Connector erstellen</span><span class="sxs-lookup"><span data-stu-id="6936e-117">Tap on Create Connector</span></span>
    *   <span data-ttu-id="6936e-118">Beachten Sie die ID & geheimen Schlüssel, die generiert abrufen und auf dem Portal angezeigt</span><span class="sxs-lookup"><span data-stu-id="6936e-118">Note the ID & Secret that get generated and displayed on the portal</span></span>

*   <span data-ttu-id="6936e-119">**Schritt 2: Benutzer Mandanten "gewährt" den Connector Zugriff auf alle Gruppen, denen er Administrator ist**</span><span class="sxs-lookup"><span data-stu-id="6936e-119">**Step 2: Tenant User “grants” the Connector access to all groups that he is admin to**</span></span>

    *   <span data-ttu-id="6936e-120">Benutzer navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="6936e-120">User navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="6936e-121">Melden Sie sich mit einer vorhandenen Office365 Konto (SKU TBD)</span><span class="sxs-lookup"><span data-stu-id="6936e-121">Log in using an existing Office365 (SKU TBD) account</span></span>
    *   <span data-ttu-id="6936e-122">Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal</span><span class="sxs-lookup"><span data-stu-id="6936e-122">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="6936e-123">Geben Sie Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="6936e-123">Enter Phone number</span></span>
        *   <span data-ttu-id="6936e-124">Tippen Sie auf "PIN generieren"</span><span class="sxs-lookup"><span data-stu-id="6936e-124">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="6936e-125">Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen</span><span class="sxs-lookup"><span data-stu-id="6936e-125">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="6936e-126">Tippen Sie auf "Connectors" im linken Menü</span><span class="sxs-lookup"><span data-stu-id="6936e-126">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="6936e-127">Tippen Sie auf den Namen des Connectors ein, die vom Connector zugegriffen werden muss</span><span class="sxs-lookup"><span data-stu-id="6936e-127">Tap on the connector name which needs to be accessed by the Connector</span></span>
    *   <span data-ttu-id="6936e-128">Tippen Sie auf "Benutzertoken generieren"</span><span class="sxs-lookup"><span data-stu-id="6936e-128">Tap on “Generate user token”</span></span>
    *   <span data-ttu-id="6936e-129">Beachten Sie die Refresh Token, die generiert dient zum Abrufen und auf dem Portal angezeigt</span><span class="sxs-lookup"><span data-stu-id="6936e-129">Note the Refresh Token that gets generated and displayed on the portal</span></span>

*   <span data-ttu-id="6936e-130">**Schritt 3: Benutzer teilt Token aktualisieren, mit der App-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="6936e-130">**Step 3: User shares the Refresh Token with the App Developer**</span></span>

    *   <span data-ttu-id="6936e-131">Admin muss manuell freigeben der Aktualisierungstoken erhalten in Schritt2 mit dem app-Entwickler</span><span class="sxs-lookup"><span data-stu-id="6936e-131">Admin needs to manually share the refresh token received in Step 2 with the app developer</span></span>

*   <span data-ttu-id="6936e-132">**Schritt 4: App-Entwickler ruft der Kaizala Plattform Rest-API zum Generieren von Access-Token**</span><span class="sxs-lookup"><span data-stu-id="6936e-132">**Step 4: App Developer calls the Kaizala Platform Rest API to generate Access Token**</span></span>

    *   <span data-ttu-id="6936e-133">Entwickler kann nun die Aktualisierungstoken verwenden.</span><span class="sxs-lookup"><span data-stu-id="6936e-133">Developer can now use the Refresh token.</span></span> <span data-ttu-id="6936e-134">eine Connector-ID und geheimen Schlüssel Connector aufrufen, die REST-API Bankkontodaten zum Generieren von Access Token (Weitere Informationen weiter unten)</span><span class="sxs-lookup"><span data-stu-id="6936e-134">a Connector ID and Connector Secret to call the REST API inorder to generate Access Token (more info below)</span></span>

