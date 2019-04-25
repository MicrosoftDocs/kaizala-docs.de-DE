# <a name="employee-help-desk"></a><span data-ttu-id="6eab2-101">Mitarbeiter-Helpdesk</span><span class="sxs-lookup"><span data-stu-id="6eab2-101">Employee Help Desk</span></span>

 <span data-ttu-id="6eab2-102">In einer Organisation prüft das Helpdesk-Team die von Mitarbeitern ausgelösten Abfragen, weist es einem Field Agent zu und aktualisiert den Auflösungsstatus auf den Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="6eab2-102">In an Organization, helpdesk team looks into the queries raised by employees, assigns it to a field agent and updates back the resolution status to the employee.</span></span> <span data-ttu-id="6eab2-103">Alle Abfragen werden als Tickets für eine einfache Verfolgung und Lösung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="6eab2-103">All the queries are logged in as tickets for easy tracking and resolution.</span></span> <span data-ttu-id="6eab2-104">Ein Ticket System ermöglicht es Helpdesk-Agenten, Feedback systematisch zu erfassen, zu kategorisieren, zu lösen und zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="6eab2-104">A ticketing system enables helpdesk agents to systematically capture, categorize, resolve and collect feedback.</span></span> <span data-ttu-id="6eab2-105">Dadurch kann eine Organisation in der Abfrage Auflösung effektiv sein und hat einen Multiplikatoreffekt für die Mitarbeiter Zufriedenheitsbewertung.</span><span class="sxs-lookup"><span data-stu-id="6eab2-105">This enables an organization to be effective in query resolution and has a multiplier effect on employee satisfaction scores.</span></span>

<span data-ttu-id="6eab2-106">Diese Lösung verwendet Kaizala als Front-End, SharePoint als Backend und Flow als Mittel zur Interaktion mit Kaizala und SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6eab2-106">This solution uses Kaizala as the front-end, SharePoint as the backend and Flow as a means to interact with Kaizala and SharePoint.</span></span> <span data-ttu-id="6eab2-107">Ein Benutzer erstellt das Ticket durch Senden eines Formulars in Kaizala, die mit dieser Karte übermittelten Ticket Details werden erfasst und mithilfe von Flow in SharePoint gespeichert. bei Übermittlung erhält der Benutzer eine aktualisierte Karte, entweder wenn-</span><span class="sxs-lookup"><span data-stu-id="6eab2-107">A user creates the ticket by submitting a form in Kaizala, ticket details submitted using this card is captured and stored in the SharePoint using Flow.On submission, User gets an updated card,either when-</span></span>

   1. <span data-ttu-id="6eab2-108">Der Helpdesk-Agent aktualisiert den Status des Tickets in SharePoint (neu, zugewiesen oder aufgelöst) oder</span><span class="sxs-lookup"><span data-stu-id="6eab2-108">Help desk agent updates the status of the ticket in SharePoint (New, Assigned or Resolved) or</span></span>

   2. <span data-ttu-id="6eab2-109">Helpdesk-Agents fügt Kommentare zu dem Ticket in SharePoint oder</span><span class="sxs-lookup"><span data-stu-id="6eab2-109">Help desk agents adds comments on the ticket in SharePoint or</span></span>

   3. <span data-ttu-id="6eab2-110">Sowohl der Helpdesk-Agent aktualisiert den Status als auch Kommentare in SharePoint</span><span class="sxs-lookup"><span data-stu-id="6eab2-110">Both, help desk agent updates status and adds comments in SharePoint</span></span>

<span data-ttu-id="6eab2-111">Wenn der Benutzer mit der vorgeschlagenen Lösung zufrieden ist, hat der Benutzer die Möglichkeit, das Ticket zu beenden und Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="6eab2-111">If the user is satisfied with the proposed resolution, user has the ability to close the ticket and submit feedback.</span></span> <span data-ttu-id="6eab2-112">Wenn der Benutzer mit der Lösung nicht zufrieden ist, kann der Benutzer das Ticket erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="6eab2-112">If the user is not satisfied with the resolution, user can re-open the ticket.</span></span> <span data-ttu-id="6eab2-113">Benutzer Feedback – Bewertung und Kommentare, Status erneut geöffnet oder geschlossen wird in SharePoint wieder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6eab2-113">User Feedback - Rating and comments, status- Reopened or closed is updated back in SharePoint.</span></span>

> <span data-ttu-id="6eab2-114">Hinweis: diese Karte funktioniert nur in Hub-und Spoke-Gruppen</span><span class="sxs-lookup"><span data-stu-id="6eab2-114">Note: This card works only in Hub and spoke groups</span></span>

  <span data-ttu-id="6eab2-115">Benutzeransicht der Ticketerstellung und-Übermittlung:</span><span class="sxs-lookup"><span data-stu-id="6eab2-115">User view of ticket creation and submission:</span></span>

  <img src="EmployeeHelpdesk-Images/1.jpg" width="350">

   <span data-ttu-id="6eab2-116">Ansicht des Status, der auf "zugewiesen" in SharePoint aktualisiert wird, und die entsprechende Karte, die an den Benutzer gesendet wird</span><span class="sxs-lookup"><span data-stu-id="6eab2-116">View of status being updated to "Assigned" in sharepoint and the corresponding card that is sent to user</span></span>

   <img src="EmployeeHelpdesk-Images/2.jpg" width="600">

   <span data-ttu-id="6eab2-117">Ansicht des Status, der auf "aufgelöst" in SharePoint aktualisiert wird, und die entsprechende Karte, die an den Benutzer gesendet wird</span><span class="sxs-lookup"><span data-stu-id="6eab2-117">View of status being updated to "Resolved" in sharepoint and the corresponding card that is sent to user</span></span>
   
   <img src="EmployeeHelpdesk-Images/3.jpg" width="600">

   <span data-ttu-id="6eab2-118">Benutzer Feedback Ansicht</span><span class="sxs-lookup"><span data-stu-id="6eab2-118">User Feedback view</span></span>

   <img src="EmployeeHelpdesk-Images/4.jpg" width="350">


## <a name="implementation-steps"></a><span data-ttu-id="6eab2-119">ImplementierungsSchritte:</span><span class="sxs-lookup"><span data-stu-id="6eab2-119">Implementation Steps:</span></span>
<span data-ttu-id="6eab2-120">Dies ist im Wesentlichen in drei Schritte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="6eab2-120">This is broadly divided into 3 steps:</span></span>

1. <span data-ttu-id="6eab2-121">Aktionspakete hochladen, mit denen ein Benutzer (*2 Aktionspakete*) aktivieren kann</span><span class="sxs-lookup"><span data-stu-id="6eab2-121">Upload action packages that enable a user to (*2 Action Packages*)</span></span>

   1. <span data-ttu-id="6eab2-122">Erstellen und übermitteln eines Tickets für das Helpdesk (*CreateTicket-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-122">Create and submit a ticket to help desk (*CreateTicket-ActionPackage.Zip*)</span></span>

   2. <span data-ttu-id="6eab2-123">Receive Status Updates & comments from Help Desk (*StatusUpdateFromHelpdesk-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-123">Receive status updates & comments from help desk (*StatusUpdateFromHelpdesk-ActionPackage.Zip*)</span></span>

2. <span data-ttu-id="6eab2-124">Einrichten einer SharePoint-Liste, mit der Helpdesk-Agents</span><span class="sxs-lookup"><span data-stu-id="6eab2-124">Set up a SharePoint list that enables helpdesk agents to</span></span>

    1. <span data-ttu-id="6eab2-125">Speichern der Ticket Details</span><span class="sxs-lookup"><span data-stu-id="6eab2-125">Store the ticket details</span></span>

    2. <span data-ttu-id="6eab2-126">Zuweisen, kommentieren und Ändern des Ticket Status</span><span class="sxs-lookup"><span data-stu-id="6eab2-126">Assign, comment and change the ticket status</span></span>

3. <span data-ttu-id="6eab2-127">Konfigurieren von Microsoft Flow für die Interaktion mit SharePoint und Kaizala (*3 Flows*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-127">Configure Microsoft Flow to interact with SharePoint and Kaizala (*3 Flows*)</span></span>

    1. <span data-ttu-id="6eab2-128">So erfassen Sie Ticket Details von der Karte und speichern Sie in SharePoint (*TicketCreationFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-128">To collect ticket details from the card and store it in SharePoint(*TicketCreationFlow.Zip*)</span></span>
    
    2. <span data-ttu-id="6eab2-129">So senden Sie dem Benutzer eine aktualisierte Karte, wenn der Helpdesk-Agent den Status, Kommentare oder beides in SharePoint aktualisiert (*TicketStatusUpdatesFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-129">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint(*TicketStatusUpdatesFlow.Zip*)</span></span>

    3. <span data-ttu-id="6eab2-130">So aktualisieren Sie die SharePoint-Liste, wenn der Benutzer das Schließen, erneutes Öffnen oder Hinzufügen von Feedback Kommentaren von der Karte auswählt (*TicketReopenFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-130">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card(*TicketReopenFlow.Zip*)</span></span>

### <a name="upload-action-packages"></a><span data-ttu-id="6eab2-131">Aktionspakete hochladen</span><span class="sxs-lookup"><span data-stu-id="6eab2-131">Upload Action Packages</span></span>
1. <span data-ttu-id="6eab2-132">Laden Sie die Datei ["EmployeeHelpDesk-SolutionPackage. zip"](https://aka.ms/EmployeeHelpdesk-SolutionPackage.zip)(*Diese enthält 2 Aktionspakete und 3 Flows*).</span><span class="sxs-lookup"><span data-stu-id="6eab2-132">Download the ["EmployeeHelpDesk-SolutionPackage.zip"](https://aka.ms/EmployeeHelpdesk-SolutionPackage.zip)(*This contains 2 Action Packages and 3 Flows*)</span></span>

2. <span data-ttu-id="6eab2-133">Laden Sie die neueste Version von Kaizala ["ActionSDK. zip"](https://manage.kaiza.la/MiniApps/DownloadSDK) (*Diese enthält KASClient. js*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-133">Download the latest version of Kaizala ["ActionSDK.Zip"](https://manage.kaiza.la/MiniApps/DownloadSDK) (*This contains KASClient.js*)</span></span>

3. <span data-ttu-id="6eab2-134">Einrichten des "CreateTicket-ActionPackage. zip"</span><span class="sxs-lookup"><span data-stu-id="6eab2-134">Set up the "CreateTicket-ActionPackage.Zip"</span></span>

   1. <span data-ttu-id="6eab2-135">Unzip "CreateTicket-ActionPackage. zip" in einen Ordner</span><span class="sxs-lookup"><span data-stu-id="6eab2-135">Unzip "CreateTicket-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="6eab2-136">Ändern der Aktion "ID" und "Anbietername" in Package. JSON</span><span class="sxs-lookup"><span data-stu-id="6eab2-136">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="6eab2-137">Hinzufügen von KASClient. js zu diesem Ordner</span><span class="sxs-lookup"><span data-stu-id="6eab2-137">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="6eab2-138">ZIP alle Inhalte in diesem Ordner (*dieser Ordner ist Ihr geändertes Aktionspaket, das in das Kaizala-Verwaltungs Portal importiert werden sollte*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-138">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="6eab2-139">[Importieren](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) des bearbeiteten Aktionspakets in das [Kaizala-Verwaltungs Portal](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="6eab2-139">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="6eab2-140">[Veröffentlichen](https://docs.microsoft.com/en-us/kaizala/actions/publish) Sie die Aktion, und fügen Sie die Aktion zu einer Gruppe hinzu, der Sie die Karte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6eab2-140">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="6eab2-141">Wählen Sie Benutzerrollen als Administrator und Mitglied aus.</span><span class="sxs-lookup"><span data-stu-id="6eab2-141">Select user roles as admin and member</span></span>

4. <span data-ttu-id="6eab2-142">Einrichten von "StatusUpdateFromHelpDesk-ActionPackage. zip"</span><span class="sxs-lookup"><span data-stu-id="6eab2-142">Set up "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

   1.  <span data-ttu-id="6eab2-143">Unzip "StatusUpdateFromHelpDesk-ActionPackage. zip" in einen Ordner</span><span class="sxs-lookup"><span data-stu-id="6eab2-143">Unzip "StatusUpdateFromHelpDesk-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="6eab2-144">Ändern der Aktion "ID" und "Anbietername" in Package. JSON</span><span class="sxs-lookup"><span data-stu-id="6eab2-144">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="6eab2-145">Hinzufügen von KASClient. js zu diesem Ordner</span><span class="sxs-lookup"><span data-stu-id="6eab2-145">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="6eab2-146">ZIP alle Inhalte in diesem Ordner (*dieser Ordner ist Ihr geändertes Aktionspaket, das in das Kaizala-Verwaltungs Portal importiert werden sollte*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-146">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="6eab2-147">[Importieren](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) des bearbeiteten Aktionspakets in das [Kaizala-Verwaltungs Portal](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="6eab2-147">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="6eab2-148">[Veröffentlichen](https://docs.microsoft.com/en-us/kaizala/actions/publish) Sie die Aktion, und fügen Sie die Aktion zu einer Gruppe hinzu, der Sie die Karte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6eab2-148">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="6eab2-149">Benutzerrolle als Administrator auswählen</span><span class="sxs-lookup"><span data-stu-id="6eab2-149">Select user role as admin</span></span>

       > <span data-ttu-id="6eab2-150">Hinweis: "CreateTicket-ActionPackage. zip" ist die Karte, die zum Auslösen eines Tickets verwendet wird und dem Administrator und den Abonnenten zur Verfügung gestellt werden soll. " StatusUpdateFromHelpDesk-ActionPackage. zip "zeigt Helpdesk-Kommentare und Status Updates an.</span><span class="sxs-lookup"><span data-stu-id="6eab2-150">Note: "CreateTicket-ActionPackage.Zip" is the card that is used to raise a ticket and should be made available to admin and Subscribers."StatusUpdateFromHelpDesk-ActionPackage.Zip" show helpdesk comments and status updates.</span></span> <span data-ttu-id="6eab2-151">Abonnenten müssen diese Karte nicht in der Aktions Palette sehen, daher wird Sie nur dem Administrator angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6eab2-151">Subscribers do not have to see this card in action palette, hence this is only made visible to admin.</span></span>

### <a name="set-up-a-sharepoint-list"></a><span data-ttu-id="6eab2-152">Einrichten einer SharePoint-Liste</span><span class="sxs-lookup"><span data-stu-id="6eab2-152">Set up a SharePoint List</span></span>

1. <span data-ttu-id="6eab2-153">[Erstellen](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) einer neuen Liste in SharePoint</span><span class="sxs-lookup"><span data-stu-id="6eab2-153">[Create](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) a new list in SharePoint</span></span>

2. <span data-ttu-id="6eab2-154">[Hinzufügen](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) von Spalten und [Bearbeiten](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*wie unten in der gleichen Reihenfolge und im Format*) Spalteneinstellungen für diese Liste</span><span class="sxs-lookup"><span data-stu-id="6eab2-154">[Add](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) columns and [Edit](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*as below in the same order and format*) column settings for this list</span></span>


    |<span data-ttu-id="6eab2-155">Spalte</span><span class="sxs-lookup"><span data-stu-id="6eab2-155">Column</span></span>|<span data-ttu-id="6eab2-156">Empfohlene Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6eab2-156">Recommended settings</span></span>|
    |-------- |---|
    |<span data-ttu-id="6eab2-157">Abteilung</span><span class="sxs-lookup"><span data-stu-id="6eab2-157">Department</span></span>|<span data-ttu-id="6eab2-158">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-158">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-159">Ort</span><span class="sxs-lookup"><span data-stu-id="6eab2-159">Location</span></span>|<span data-ttu-id="6eab2-160">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-160">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-161">Kategorie</span><span class="sxs-lookup"><span data-stu-id="6eab2-161">Category</span></span>|<span data-ttu-id="6eab2-162">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-162">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6eab2-163">Description</span></span> |<span data-ttu-id="6eab2-164">Mehrere Textzeilen</span><span class="sxs-lookup"><span data-stu-id="6eab2-164">Multiple lines of text</span></span>|
    |<span data-ttu-id="6eab2-165">Fotos</span><span class="sxs-lookup"><span data-stu-id="6eab2-165">Photos</span></span>|<span data-ttu-id="6eab2-166">Mehrere Textzeilen</span><span class="sxs-lookup"><span data-stu-id="6eab2-166">Multiple lines of text</span></span>|
    |<span data-ttu-id="6eab2-167">Creatorname</span><span class="sxs-lookup"><span data-stu-id="6eab2-167">CreatorName</span></span>|<span data-ttu-id="6eab2-168">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-168">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-169">CreatorContact</span><span class="sxs-lookup"><span data-stu-id="6eab2-169">CreatorContact</span></span>|<span data-ttu-id="6eab2-170">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-170">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-171">ReportedAt</span><span class="sxs-lookup"><span data-stu-id="6eab2-171">ReportedAt</span></span>|<span data-ttu-id="6eab2-172">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-172">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-173">AssignedTo</span><span class="sxs-lookup"><span data-stu-id="6eab2-173">AssignedTo</span></span>|<span data-ttu-id="6eab2-174">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-174">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-175">AssignedBy</span><span class="sxs-lookup"><span data-stu-id="6eab2-175">AssignedBy</span></span>|<span data-ttu-id="6eab2-176">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-176">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-177">Status</span><span class="sxs-lookup"><span data-stu-id="6eab2-177">Status</span></span>|<span data-ttu-id="6eab2-178">Auswahl mit Optionen als neu, zugewiesen, aufgelöst, geschlossen und erneut geöffnet (*diese Ticket Phasen sind obligatorisch*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-178">Choice with options as New, Assigned, Resolved, Closed and Reopened (*These ticket stages are mandatory*)</span></span>|
    |<span data-ttu-id="6eab2-179">HelpdeskComments</span><span class="sxs-lookup"><span data-stu-id="6eab2-179">HelpdeskComments</span></span>|<span data-ttu-id="6eab2-180">Mehrere Textzeilen</span><span class="sxs-lookup"><span data-stu-id="6eab2-180">Multiple lines of text</span></span>|
    |<span data-ttu-id="6eab2-181">UserFeedback</span><span class="sxs-lookup"><span data-stu-id="6eab2-181">UserFeedback</span></span>|<span data-ttu-id="6eab2-182">Mehrere Textzeilen</span><span class="sxs-lookup"><span data-stu-id="6eab2-182">Multiple lines of text</span></span>|
    |<span data-ttu-id="6eab2-183">ReasonsToReopen</span><span class="sxs-lookup"><span data-stu-id="6eab2-183">ReasonsToReopen</span></span>|<span data-ttu-id="6eab2-184">Mehrere Textzeilen</span><span class="sxs-lookup"><span data-stu-id="6eab2-184">Multiple lines of text</span></span>|
    |<span data-ttu-id="6eab2-185">CreatorKaizalaName</span><span class="sxs-lookup"><span data-stu-id="6eab2-185">CreatorKaizalaName</span></span>|<span data-ttu-id="6eab2-186">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-186">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-187">CreatorKaizalaContact</span><span class="sxs-lookup"><span data-stu-id="6eab2-187">CreatorKaizalaContact</span></span>|<span data-ttu-id="6eab2-188">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-188">Single line of text</span></span>|
    |<span data-ttu-id="6eab2-189">User Rating</span><span class="sxs-lookup"><span data-stu-id="6eab2-189">UserRating</span></span>|<span data-ttu-id="6eab2-190">Eine Textzeile</span><span class="sxs-lookup"><span data-stu-id="6eab2-190">Single line of text</span></span>|
 

4. <span data-ttu-id="6eab2-191">[Bearbeiten Sie die Listenansicht](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) , um die ID an erster Stelle zu positionieren. Dies ist die eindeutige Ticket-ID, die auf der Karte angezeigt wird, nachdem das Ticket zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="6eab2-191">[Edit list view](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) to position ID in first place.This is the unique ticket ID that will be displayed in the card, once the ticket is assigned.</span></span>

     ><span data-ttu-id="6eab2-192">Hinweis: Excel-Vorlage für Spaltenkopfzeilen [herunterladen](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx)</span><span class="sxs-lookup"><span data-stu-id="6eab2-192">Note: [Download](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx) excel template for column headers</span></span>

### <a name="import-and-set-up-flows"></a><span data-ttu-id="6eab2-193">Importieren und Einrichten von Flows</span><span class="sxs-lookup"><span data-stu-id="6eab2-193">Import and Set up Flows</span></span>

<span data-ttu-id="6eab2-194">Diese Lösung hat drei Flüsse,</span><span class="sxs-lookup"><span data-stu-id="6eab2-194">This solution has 3 Flows,</span></span>

1. <span data-ttu-id="6eab2-195">So erfassen Sie Ticket Details von der Karte und speichern Sie in SharePoint</span><span class="sxs-lookup"><span data-stu-id="6eab2-195">To collect ticket details from the card and store it in SharePoint</span></span>

    1. <span data-ttu-id="6eab2-196">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "TicketCreationFlow. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="6eab2-196">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketCreationFlow.Zip" to your Microsoft Flow account</span></span>

          > <span data-ttu-id="6eab2-197">Hinweis – Wenn Sie noch nie SharePoint-oder Kaizala-Verbindungen verwendet haben, fügen Sie zunächst [Verbindungen hinzu](https://docs.microsoft.com/en-us/flow/add-manage-connections) .</span><span class="sxs-lookup"><span data-stu-id="6eab2-197">Note- If you have never used Sharepoint or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>    

    2. <span data-ttu-id="6eab2-198">Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-198">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="6eab2-199">Im ersten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-199">In the First block</span></span> 

               1. <span data-ttu-id="6eab2-200">Geben Sie die Gruppen-ID ein, oder wählen Sie den Gruppennamen aus, dem Sie die Karte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6eab2-200">Enter the Group ID or Select the Group name where you want to add the card</span></span>

               2. <span data-ttu-id="6eab2-201">Klicken Sie auf Aktionspaket Feld, um die Aktions-ID einzugeben, die Sie für "CreateTicket-ActionPackage. zip" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="6eab2-201">Click on Action Package field to enter action id that you have given for "CreateTicket-ActionPackage.zip"</span></span>

               3. <span data-ttu-id="6eab2-202">Aktion "alle" zuordnen</span><span class="sxs-lookup"><span data-stu-id="6eab2-202">Map action to "All"</span></span>

                  <img src="EmployeeHelpdesk-Images/5.JPG" width="600">

          2. <span data-ttu-id="6eab2-203">Im letzten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-203">In the Last block</span></span>

               1. <span data-ttu-id="6eab2-204">Eingeben der SharePoint-Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="6eab2-204">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="6eab2-205">Listen Name eingeben</span><span class="sxs-lookup"><span data-stu-id="6eab2-205">Enter List Name</span></span>
                  
                  <img src="EmployeeHelpdesk-Images/6.JPG" width="600">

                   > <span data-ttu-id="6eab2-206">Hinweis: alle Spalten in der SharePoint-Liste werden beim Eingeben des &-Listen namens der SharePoint-Website in Flow angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6eab2-206">Note: All the columns in the SharePoint list will be displayed in Flow on entering Sharepoint Site address & List Name.</span></span> <span data-ttu-id="6eab2-207">Überprüfen Sie die Zuordnung von SharePoint-Listenfeldern in Flow.</span><span class="sxs-lookup"><span data-stu-id="6eab2-207">Verify the mapping of SharePoint list fields in Flow.</span></span> 

          3.  <span data-ttu-id="6eab2-208">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="6eab2-208">Save the Flow</span></span>
           

2. <span data-ttu-id="6eab2-209">So senden Sie dem Benutzer eine aktualisierte Karte, wenn der Helpdesk-Agent den Status, Kommentare oder beides in SharePoint aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6eab2-209">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint</span></span>

    1. <span data-ttu-id="6eab2-210">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "TicketStatusUpdatesFlow. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="6eab2-210">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketStatusUpdatesFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="6eab2-211">Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-211">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="6eab2-212">Im ersten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-212">In the first block</span></span>

               1.  <span data-ttu-id="6eab2-213">Eingeben der SharePoint-Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="6eab2-213">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="6eab2-214">Listen Name eingeben</span><span class="sxs-lookup"><span data-stu-id="6eab2-214">Enter List Name</span></span>

                  <img src="EmployeeHelpdesk-Images/6.5.jpg" width="600">

          2. <span data-ttu-id="6eab2-215">Im letzten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-215">In the last block</span></span>

               1. <span data-ttu-id="6eab2-216">Geben Sie die Gruppen-ID ein, oder wählen Sie Gruppenname aus, an die Sie die Statusaktualisierungen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="6eab2-216">Enter the group ID or select group name to where you want to send the status updates</span></span>

               2. <span data-ttu-id="6eab2-217">Klicken Sie auf Aktion, um "Aktionspaket" auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6eab2-217">Click on Action to select "Action Package"</span></span> 

               3. <span data-ttu-id="6eab2-218">Klicken Sie auf Aktionspaket, um die Aktions-ID einzugeben, die Sie für "StatusUpdateFromHelpDesk-ActionPackage. zip" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="6eab2-218">Click on Action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

               4. <span data-ttu-id="6eab2-219">Körper "ActionBody" zuordnen</span><span class="sxs-lookup"><span data-stu-id="6eab2-219">Map body to "ActionBody"</span></span>

                  <img src="EmployeeHelpdesk-Images/7.JPG" width="600">

        3.  <span data-ttu-id="6eab2-220">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="6eab2-220">Save the Flow</span></span>
    
3. <span data-ttu-id="6eab2-221">So aktualisieren Sie die SharePoint-Liste, wenn der Benutzer das Schließen, erneutes Öffnen oder Hinzufügen von Feedback Kommentaren von der Karte auswählt</span><span class="sxs-lookup"><span data-stu-id="6eab2-221">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card</span></span>
 
    1. <span data-ttu-id="6eab2-222">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "TicketReopenFlow. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="6eab2-222">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketReopenFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="6eab2-223">Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*)</span><span class="sxs-lookup"><span data-stu-id="6eab2-223">Edit details in Imported Flow (*See steps below*)</span></span> 

        1. <span data-ttu-id="6eab2-224">Im ersten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-224">In the First block</span></span> 

             1. <span data-ttu-id="6eab2-225">Wählen Sie Gruppenname aus, oder geben Sie die Gruppen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="6eab2-225">Select group name or enter the group ID</span></span>

             2. <span data-ttu-id="6eab2-226">Klicken Sie auf Aktionspaket, um die Aktions-ID einzugeben, die Sie für "StatusUpdateFromHelpDesk-ActionPackage. zip" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="6eab2-226">Click on action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

             3. <span data-ttu-id="6eab2-227">Aktion "alle" zuordnen</span><span class="sxs-lookup"><span data-stu-id="6eab2-227">Map action to "All"</span></span>

                <img src="EmployeeHelpdesk-Images/8.JPG" width="600">

        2. <span data-ttu-id="6eab2-228">Im zweiten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-228">In the second block</span></span>

             1. <span data-ttu-id="6eab2-229">Geben Sie die Websiteadresse ein.</span><span class="sxs-lookup"><span data-stu-id="6eab2-229">Enter the site address</span></span>

             2. <span data-ttu-id="6eab2-230">Geben Sie den Listennamen ein.</span><span class="sxs-lookup"><span data-stu-id="6eab2-230">Enter the list name</span></span> 

                <img src="EmployeeHelpdesk-Images/9.JPG" width="600">

        3. <span data-ttu-id="6eab2-231">Im letzten Block</span><span class="sxs-lookup"><span data-stu-id="6eab2-231">In the Last block</span></span>

             1. <span data-ttu-id="6eab2-232">Geben Sie die Websiteadresse ein.</span><span class="sxs-lookup"><span data-stu-id="6eab2-232">Enter the site address</span></span>

             2. <span data-ttu-id="6eab2-233">Geben Sie den Listennamen ein.</span><span class="sxs-lookup"><span data-stu-id="6eab2-233">Enter the list name</span></span>

                <img src="EmployeeHelpdesk-Images/10.JPG" width="600">

        4.  <span data-ttu-id="6eab2-234">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="6eab2-234">Save the Flow</span></span>
