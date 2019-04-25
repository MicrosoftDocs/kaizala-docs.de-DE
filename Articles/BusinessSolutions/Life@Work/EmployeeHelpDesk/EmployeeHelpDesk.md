# <a name="employee-help-desk"></a><span data-ttu-id="7414c-101">Mitarbeiter-Helpdesk</span><span class="sxs-lookup"><span data-stu-id="7414c-101">Employee Help Desk</span></span>

 <span data-ttu-id="7414c-102">In einer Organisation prüft das Helpdesk-Team die von Mitarbeitern ausgelösten Abfragen, weist es einem Field Agent zu und aktualisiert den Auflösungsstatus auf den Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="7414c-102">In an Organization, helpdesk team looks into the queries raised by employees, assigns it to a field agent and updates back the resolution status to the employee.</span></span> <span data-ttu-id="7414c-103">Alle Abfragen werden als Tickets für eine einfache Verfolgung und Lösung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="7414c-103">All the queries are logged in as tickets for easy tracking and resolution.</span></span> <span data-ttu-id="7414c-104">Ein Ticket System ermöglicht es Helpdesk-Agenten, Feedback systematisch zu erfassen, zu kategorisieren, zu lösen und zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="7414c-104">A ticketing system enables helpdesk agents to systematically capture, categorize, resolve and collect feedback.</span></span> <span data-ttu-id="7414c-105">Dadurch kann eine Organisation in der Abfrage Auflösung effektiv sein und hat einen Multiplikatoreffekt für die Mitarbeiter Zufriedenheitsbewertung.</span><span class="sxs-lookup"><span data-stu-id="7414c-105">This enables an organization to be effective in query resolution and has a multiplier effect on employee satisfaction scores.</span></span>

<span data-ttu-id="7414c-106">Diese Lösung verwendet Kaizala als Front-End, SharePoint als Backend und Flow als Mittel zur Interaktion mit Kaizala und SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7414c-106">This solution uses Kaizala as the front-end, SharePoint as the backend and Flow as a means to interact with Kaizala and SharePoint.</span></span> <span data-ttu-id="7414c-107">Ein Benutzer erstellt das Ticket durch Senden eines Formulars in Kaizala, die mit dieser Karte übermittelten Ticket Details werden erfasst und mithilfe von Flow in SharePoint gespeichert. bei Übermittlung erhält der Benutzer eine aktualisierte Karte, entweder wenn-</span><span class="sxs-lookup"><span data-stu-id="7414c-107">A user creates the ticket by submitting a form in Kaizala, ticket details submitted using this card is captured and stored in the SharePoint using Flow.On submission, User gets an updated card,either when-</span></span>

   1. <span data-ttu-id="7414c-108">Der Helpdesk-Agent aktualisiert den Status des Tickets in SharePoint (neu, zugewiesen oder aufgelöst) oder</span><span class="sxs-lookup"><span data-stu-id="7414c-108">Help desk agent updates the status of the ticket in SharePoint (New, Assigned or Resolved) or</span></span>

   2. <span data-ttu-id="7414c-109">Helpdesk-Agents fügt Kommentare zu dem Ticket in SharePoint oder</span><span class="sxs-lookup"><span data-stu-id="7414c-109">Help desk agents adds comments on the ticket in SharePoint or</span></span>

   3. <span data-ttu-id="7414c-110">Sowohl der Helpdesk-Agent aktualisiert den Status als auch Kommentare in SharePoint</span><span class="sxs-lookup"><span data-stu-id="7414c-110">Both, help desk agent updates status and adds comments in SharePoint</span></span>

<span data-ttu-id="7414c-111">Wenn der Benutzer mit der vorgeschlagenen Lösung zufrieden ist, hat der Benutzer die Möglichkeit, das Ticket zu beenden und Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="7414c-111">If the user is satisfied with the proposed resolution, user has the ability to close the ticket and submit feedback.</span></span> <span data-ttu-id="7414c-112">Wenn der Benutzer mit der Lösung nicht zufrieden ist, kann der Benutzer das Ticket erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="7414c-112">If the user is not satisfied with the resolution, user can re-open the ticket.</span></span> <span data-ttu-id="7414c-113">Benutzer Feedback – Bewertung und Kommentare, Status erneut geöffnet oder geschlossen wird in SharePoint wieder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7414c-113">User Feedback - Rating and comments, status- Reopened or closed is updated back in SharePoint.</span></span>

> <span data-ttu-id="7414c-114">Hinweis: diese Karte funktioniert nur in Hub-und Spoke-Gruppen</span><span class="sxs-lookup"><span data-stu-id="7414c-114">Note: This card works only in Hub and spoke groups</span></span>

  <span data-ttu-id="7414c-115">Benutzeransicht der Ticketerstellung und-Übermittlung:</span><span class="sxs-lookup"><span data-stu-id="7414c-115">User view of ticket creation and submission:</span></span>

  <img src="EmployeeHelpdesk-Images/1.jpg" width="350">

   <span data-ttu-id="7414c-116">Anzeigen der Aktualisierung des Status auf "zugewiesen" in SharePoint und der entsprechenden Karte, die an den Benutzer gesendet wird</span><span class="sxs-lookup"><span data-stu-id="7414c-116">View on updating the status to "Assigned" in sharepoint and the corresponding card that is sent to user</span></span>

   <img src="EmployeeHelpdesk-Images/2.jpg" width="600">

   <span data-ttu-id="7414c-117">Ansicht des Status, der auf "aufgelöst" in SharePoint aktualisiert wird, und die entsprechende Karte, die an den Benutzer gesendet wird</span><span class="sxs-lookup"><span data-stu-id="7414c-117">View of status being updated to "Resolved" in sharepoint and the corresponding card that is sent to user</span></span>
   
   <img src="EmployeeHelpdesk-Images/3.jpg" width="600">

   <span data-ttu-id="7414c-118">Benutzer Feedback Ansicht</span><span class="sxs-lookup"><span data-stu-id="7414c-118">User Feedback view</span></span>

   <img src="EmployeeHelpdesk-Images/4.jpg" width="350">


## <a name="implementation-steps"></a><span data-ttu-id="7414c-119">ImplementierungsSchritte:</span><span class="sxs-lookup"><span data-stu-id="7414c-119">Implementation Steps:</span></span>
<span data-ttu-id="7414c-120">Dies ist im Wesentlichen in drei Schritte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="7414c-120">This is broadly divided into 3 steps:</span></span>

1. <span data-ttu-id="7414c-121">Aktionspakete hochladen, mit denen ein Benutzer (*2 Aktionspakete*) aktivieren kann</span><span class="sxs-lookup"><span data-stu-id="7414c-121">Upload action packages that enable a user to (*2 Action Packages*)</span></span>

   1. <span data-ttu-id="7414c-122">Erstellen und übermitteln eines Tickets für das Helpdesk (*CreateTicket-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="7414c-122">Create and submit a ticket to help desk (*CreateTicket-ActionPackage.Zip*)</span></span>

   2. <span data-ttu-id="7414c-123">Receive Status Updates & comments from Help Desk (*StatusUpdateFromHelpdesk-ActionPackage. zip*)</span><span class="sxs-lookup"><span data-stu-id="7414c-123">Receive status updates & comments from help desk (*StatusUpdateFromHelpdesk-ActionPackage.Zip*)</span></span>

2. <span data-ttu-id="7414c-124">Einrichten einer SharePoint-Liste, mit der Helpdesk-Agents</span><span class="sxs-lookup"><span data-stu-id="7414c-124">Set up a SharePoint list that enables helpdesk agents to</span></span>

    1. <span data-ttu-id="7414c-125">Speichern der Ticket Details</span><span class="sxs-lookup"><span data-stu-id="7414c-125">Store the ticket details</span></span>

    2. <span data-ttu-id="7414c-126">Zuweisen, kommentieren und Ändern des Ticket Status</span><span class="sxs-lookup"><span data-stu-id="7414c-126">Assign, comment and change the ticket status</span></span>

3. <span data-ttu-id="7414c-127">Konfigurieren von Microsoft Flow für die Interaktion mit SharePoint und Kaizala (*3 Flows*)</span><span class="sxs-lookup"><span data-stu-id="7414c-127">Configure Microsoft Flow to interact with SharePoint and Kaizala (*3 Flows*)</span></span>

    1. <span data-ttu-id="7414c-128">So erfassen Sie Ticket Details von der Karte und speichern Sie in SharePoint (*TicketCreationFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="7414c-128">To collect ticket details from the card and store it in SharePoint(*TicketCreationFlow.Zip*)</span></span>
    
    2. <span data-ttu-id="7414c-129">So senden Sie dem Benutzer eine aktualisierte Karte, wenn der Helpdesk-Agent den Status, Kommentare oder beides in SharePoint aktualisiert (*TicketStatusUpdatesFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="7414c-129">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint(*TicketStatusUpdatesFlow.Zip*)</span></span>

    3. <span data-ttu-id="7414c-130">So aktualisieren Sie die SharePoint-Liste, wenn der Benutzer das Schließen, erneutes Öffnen oder Hinzufügen von Feedback Kommentaren von der Karte auswählt (*TicketReopenFlow. zip*)</span><span class="sxs-lookup"><span data-stu-id="7414c-130">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card(*TicketReopenFlow.Zip*)</span></span>

### <a name="upload-action-packages"></a><span data-ttu-id="7414c-131">Aktionspakete hochladen</span><span class="sxs-lookup"><span data-stu-id="7414c-131">Upload Action Packages</span></span>
1. <span data-ttu-id="7414c-132">Laden Sie die Datei ["EmployeeHelpDesk-SolutionPackage. zip"](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/EmployeeHelpdesk-SolutionPackage.zip) (*Diese enthält 2 Aktionspakete und 3 Flows*).</span><span class="sxs-lookup"><span data-stu-id="7414c-132">Download the ["EmployeeHelpDesk-SolutionPackage.zip"](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/EmployeeHelpdesk-SolutionPackage.zip) (*This contains 2 Action Packages and 3 Flows*)</span></span>

2. <span data-ttu-id="7414c-133">Laden Sie die neueste Version von Kaizala ["ActionSDK. zip"](https://manage.kaiza.la/MiniApps/DownloadSDK) (*Diese enthält KASClient. js*)</span><span class="sxs-lookup"><span data-stu-id="7414c-133">Download the latest version of Kaizala ["ActionSDK.Zip"](https://manage.kaiza.la/MiniApps/DownloadSDK) (*This contains KASClient.js*)</span></span>

3. <span data-ttu-id="7414c-134">Einrichten des "CreateTicket-ActionPackage. zip"</span><span class="sxs-lookup"><span data-stu-id="7414c-134">Set up the "CreateTicket-ActionPackage.Zip"</span></span>

   1. <span data-ttu-id="7414c-135">Unzip "CreateTicket-ActionPackage. zip" in einen Ordner</span><span class="sxs-lookup"><span data-stu-id="7414c-135">Unzip "CreateTicket-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="7414c-136">Ändern der Aktion "ID" und "Anbietername" in Package. JSON</span><span class="sxs-lookup"><span data-stu-id="7414c-136">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="7414c-137">Hinzufügen von KASClient. js zu diesem Ordner</span><span class="sxs-lookup"><span data-stu-id="7414c-137">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="7414c-138">ZIP alle Inhalte in diesem Ordner (*dieser Ordner ist Ihr geändertes Aktionspaket, das in das Kaizala-Verwaltungs Portal importiert werden sollte*)</span><span class="sxs-lookup"><span data-stu-id="7414c-138">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="7414c-139">[Importieren](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) des bearbeiteten Aktionspakets in das [Kaizala-Verwaltungs Portal](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="7414c-139">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="7414c-140">[Veröffentlichen](https://docs.microsoft.com/en-us/kaizala/actions/publish) Sie die Aktion, und fügen Sie die Aktion zu einer Gruppe hinzu, der Sie die Karte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7414c-140">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="7414c-141">Wählen Sie Benutzerrollen als Administrator und Mitglied aus.</span><span class="sxs-lookup"><span data-stu-id="7414c-141">Select user roles as admin and member</span></span>

4. <span data-ttu-id="7414c-142">Einrichten von "StatusUpdateFromHelpDesk-ActionPackage. zip"</span><span class="sxs-lookup"><span data-stu-id="7414c-142">Set up "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

   1.  <span data-ttu-id="7414c-143">Unzip "StatusUpdateFromHelpDesk-ActionPackage. zip" in einen Ordner</span><span class="sxs-lookup"><span data-stu-id="7414c-143">Unzip "StatusUpdateFromHelpDesk-ActionPackage.Zip" to a folder</span></span>

   2. <span data-ttu-id="7414c-144">Ändern der Aktion "ID" und "Anbietername" in Package. JSON</span><span class="sxs-lookup"><span data-stu-id="7414c-144">Change the action "id" and "provider name" in package.json</span></span>

   3. <span data-ttu-id="7414c-145">Hinzufügen von KASClient. js zu diesem Ordner</span><span class="sxs-lookup"><span data-stu-id="7414c-145">Add KASClient.js to this folder</span></span> 

   4. <span data-ttu-id="7414c-146">ZIP alle Inhalte in diesem Ordner (*dieser Ordner ist Ihr geändertes Aktionspaket, das in das Kaizala-Verwaltungs Portal importiert werden sollte*)</span><span class="sxs-lookup"><span data-stu-id="7414c-146">Zip all the contents in this folder (*This folder is your modified action package which should be imported to Kaizala Management Portal*)</span></span>

   5. <span data-ttu-id="7414c-147">[Importieren](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) des bearbeiteten Aktionspakets in das [Kaizala-Verwaltungs Portal](https://manage.kaiza.la/)</span><span class="sxs-lookup"><span data-stu-id="7414c-147">[Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to [Kaizala Management Portal](https://manage.kaiza.la/)</span></span>

   6. <span data-ttu-id="7414c-148">[Veröffentlichen](https://docs.microsoft.com/en-us/kaizala/actions/publish) Sie die Aktion, und fügen Sie die Aktion zu einer Gruppe hinzu, der Sie die Karte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7414c-148">[Publish](https://docs.microsoft.com/en-us/kaizala/actions/publish) the action and add the action to a group where you want to add the card</span></span>

   7. <span data-ttu-id="7414c-149">Benutzerrolle als Administrator auswählen</span><span class="sxs-lookup"><span data-stu-id="7414c-149">Select user role as admin</span></span>

       > <span data-ttu-id="7414c-150">Hinweis: "CreateTicket-ActionPackage. zip" ist die Karte, die zum Auslösen eines Tickets verwendet wird und dem Administrator und den Abonnenten zur Verfügung gestellt werden soll. " StatusUpdateFromHelpDesk-ActionPackage. zip "zeigt Helpdesk-Kommentare und Status Updates an.</span><span class="sxs-lookup"><span data-stu-id="7414c-150">Note: "CreateTicket-ActionPackage.Zip" is the card that is used to raise a ticket and should be made available to admin and Subscribers."StatusUpdateFromHelpDesk-ActionPackage.Zip" show helpdesk comments and status updates.</span></span> <span data-ttu-id="7414c-151">Abonnenten müssen diese Karte nicht in der Aktions Palette sehen, daher wird Sie nur dem Administrator angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7414c-151">Subscribers do not have to see this card in action palette, hence this is only made visible to admin.</span></span>

### <a name="set-up-a-sharepoint-list"></a><span data-ttu-id="7414c-152">Einrichten einer SharePoint-Liste</span><span class="sxs-lookup"><span data-stu-id="7414c-152">Set up a SharePoint List</span></span>

1. <span data-ttu-id="7414c-153">[Erstellen](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) einer neuen Liste in SharePoint</span><span class="sxs-lookup"><span data-stu-id="7414c-153">[Create](https://support.office.com/en-us/article/create-a-list-in-sharepoint-0d397414-d95f-41eb-addd-5e6eff41b083) a new list in SharePoint</span></span>

2. <span data-ttu-id="7414c-154">[Hinzufügen](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) von Spalten und [Bearbeiten](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*wie unten in der gleichen Reihenfolge und im Format*) Spalteneinstellungen für diese Liste</span><span class="sxs-lookup"><span data-stu-id="7414c-154">[Add](https://support.office.com/en-us/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) columns and [Edit](https://support.office.com/en-us/article/Edit-list-settings-in-SharePoint-Online-4d35793b-246e-42a3-990c-563a83795b7f) (*as below in the same order and format*) column settings for this list</span></span>


    <span data-ttu-id="7414c-155">Spalten Empfohlene Einstellungen--------|---Department | Einzelne Textzeile | Einzelne Textzeile Kategorie | Einzelne Textzeile Beschreibung | Mehrere Textzeilen Fotos | Mehrere Textzeilen Creatorname | Einzelne Textzeile CreatorContact | Einzelne Textzeile ReportedAt | Einzelne Textzeile ZugewiesenAn | Einzelne Textzeile AssignedBy | Einzelne Zeile des Text Status | Auswahl mit Optionen als neu, zugewiesen, aufgelöst, geschlossen und erneut geöffnet (*diese Ticket Phasen sind obligatorisch*) HelpdeskComments | Mehrere Textzeilen UserFeedback | Mehrere Textzeilen ReasonsToReopen | Mehrere Textzeilen CreatorKaizalaName | Einzelne Textzeile CreatorKaizalaContact | Einzelne Textzeile User Rating | Einzelne Textzeile</span><span class="sxs-lookup"><span data-stu-id="7414c-155">Column  Recommended settings  -------- |---   Department|Single line of text   Location|Single line of text   Category|Single line of text   Description |Multiple lines of text   Photos|Multiple lines of text   CreatorName|Single line of text   CreatorContact|Single line of text   ReportedAt|Single line of text   AssignedTo|Single line of text   AssignedBy|Single line of text   Status|Choice with options as New, Assigned, Resolved, Closed and Reopened (*These ticket stages are mandatory*)   HelpdeskComments|Multiple lines of text   UserFeedback|Multiple lines of text   ReasonsToReopen|Multiple lines of text   CreatorKaizalaName|Single line of text   CreatorKaizalaContact|Single line of text   UserRating|Single line of text</span></span>
 

4. <span data-ttu-id="7414c-156">[Bearbeiten Sie die Listenansicht](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) , um die ID an erster Stelle zu positionieren. Dies ist die eindeutige Ticket-ID, die auf der Karte angezeigt wird, nachdem das Ticket zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7414c-156">[Edit list view](https://support.office.com/en-gb/article/edit-a-list-view-in-sharepoint-online-15916903-e79a-423f-b4e2-02d37e1ff372) to position ID in first place.This is the unique ticket ID that will be displayed in the card, once the ticket is assigned.</span></span>

     ><span data-ttu-id="7414c-157">Hinweis: Excel-Vorlage für Spaltenkopfzeilen [herunterladen](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx)</span><span class="sxs-lookup"><span data-stu-id="7414c-157">Note: [Download](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/Life%40Work/EmployeeHelpDesk/HelpdeskTemplate.xlsx) excel template for column headers</span></span>

### <a name="import-and-set-up-flows"></a><span data-ttu-id="7414c-158">Importieren und Einrichten von Flows</span><span class="sxs-lookup"><span data-stu-id="7414c-158">Import and Set up Flows</span></span>

<span data-ttu-id="7414c-159">Diese Lösung hat drei Flüsse,</span><span class="sxs-lookup"><span data-stu-id="7414c-159">This solution has 3 Flows,</span></span>

1. <span data-ttu-id="7414c-160">So erfassen Sie Ticket Details von der Karte und speichern Sie in SharePoint</span><span class="sxs-lookup"><span data-stu-id="7414c-160">To collect ticket details from the card and store it in SharePoint</span></span>

    1. <span data-ttu-id="7414c-161">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "TicketCreationFlow. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="7414c-161">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketCreationFlow.Zip" to your Microsoft Flow account</span></span>

          > <span data-ttu-id="7414c-162">Hinweis – Wenn Sie noch nie SharePoint-oder Kaizala-Verbindungen verwendet haben, fügen Sie zunächst [Verbindungen hinzu](https://docs.microsoft.com/en-us/flow/add-manage-connections) .</span><span class="sxs-lookup"><span data-stu-id="7414c-162">Note- If you have never used Sharepoint or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)</span></span>    

    2. <span data-ttu-id="7414c-163">Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*)</span><span class="sxs-lookup"><span data-stu-id="7414c-163">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="7414c-164">Im ersten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-164">In the First block</span></span> 

               1. <span data-ttu-id="7414c-165">Geben Sie die Gruppen-ID ein, oder wählen Sie den Gruppennamen aus, dem Sie die Karte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7414c-165">Enter the Group ID or Select the Group name where you want to add the card</span></span>

               2. <span data-ttu-id="7414c-166">Klicken Sie auf Aktionspaket Feld, um die Aktions-ID einzugeben, die Sie für "CreateTicket-ActionPackage. zip" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7414c-166">Click on Action Package field to enter action id that you have given for "CreateTicket-ActionPackage.zip"</span></span>

               3. <span data-ttu-id="7414c-167">Aktion "alle" zuordnen</span><span class="sxs-lookup"><span data-stu-id="7414c-167">Map action to "All"</span></span>

                  <img src="EmployeeHelpdesk-Images/5.JPG" width="600">

          2. <span data-ttu-id="7414c-168">Im letzten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-168">In the Last block</span></span>

               1. <span data-ttu-id="7414c-169">Eingeben der SharePoint-Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="7414c-169">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="7414c-170">Listen Name eingeben</span><span class="sxs-lookup"><span data-stu-id="7414c-170">Enter List Name</span></span>
                  
                  <img src="EmployeeHelpdesk-Images/6.JPG" width="600">

                   > <span data-ttu-id="7414c-171">Hinweis: alle Spalten in der SharePoint-Liste werden beim Eingeben des &-Listen namens der SharePoint-Website in Flow angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7414c-171">Note: All the columns in the SharePoint list will be displayed in Flow on entering Sharepoint Site address & List Name.</span></span> <span data-ttu-id="7414c-172">Überprüfen Sie die Zuordnung von SharePoint-Listenfeldern in Flow.</span><span class="sxs-lookup"><span data-stu-id="7414c-172">Verify the mapping of SharePoint list fields in Flow.</span></span> 

          3.  <span data-ttu-id="7414c-173">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="7414c-173">Save the Flow</span></span>
           

2. <span data-ttu-id="7414c-174">So senden Sie dem Benutzer eine aktualisierte Karte, wenn der Helpdesk-Agent den Status, Kommentare oder beides in SharePoint aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7414c-174">To send the user an updated card when help desk agent updates the status, comments or both in the SharePoint</span></span>

    1. <span data-ttu-id="7414c-175">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "TicketStatusUpdatesFlow. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="7414c-175">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketStatusUpdatesFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="7414c-176">Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*)</span><span class="sxs-lookup"><span data-stu-id="7414c-176">Edit details in Imported Flow (*See steps below*)</span></span> 

          1. <span data-ttu-id="7414c-177">Im ersten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-177">In the first block</span></span>

               1.  <span data-ttu-id="7414c-178">Eingeben der SharePoint-Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="7414c-178">Enter the SharePoint Site address</span></span>

               2. <span data-ttu-id="7414c-179">Listen Name eingeben</span><span class="sxs-lookup"><span data-stu-id="7414c-179">Enter List Name</span></span>

                  <img src="EmployeeHelpdesk-Images/6.5.jpg" width="600">

          2. <span data-ttu-id="7414c-180">Im letzten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-180">In the last block</span></span>

               1. <span data-ttu-id="7414c-181">Geben Sie die Gruppen-ID ein, oder wählen Sie Gruppenname aus, an die Sie die Statusaktualisierungen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="7414c-181">Enter the group ID or select group name to where you want to send the status updates</span></span>

               2. <span data-ttu-id="7414c-182">Klicken Sie auf Aktion, um "Aktionspaket" auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7414c-182">Click on Action to select "Action Package"</span></span> 

               3. <span data-ttu-id="7414c-183">Klicken Sie auf Aktionspaket, um die Aktions-ID einzugeben, die Sie für "StatusUpdateFromHelpDesk-ActionPackage. zip" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7414c-183">Click on Action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

               4. <span data-ttu-id="7414c-184">Körper "ActionBody" zuordnen</span><span class="sxs-lookup"><span data-stu-id="7414c-184">Map body to "ActionBody"</span></span>

                  <img src="EmployeeHelpdesk-Images/7.JPG" width="600">

        3.  <span data-ttu-id="7414c-185">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="7414c-185">Save the Flow</span></span>
    
3. <span data-ttu-id="7414c-186">So aktualisieren Sie die SharePoint-Liste, wenn der Benutzer das Schließen, erneutes Öffnen oder Hinzufügen von Feedback Kommentaren von der Karte auswählt</span><span class="sxs-lookup"><span data-stu-id="7414c-186">To update the SharePoint list when the user chooses to close, reopen or adds feedback comments from the card</span></span>
 
    1. <span data-ttu-id="7414c-187">[Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "TicketReopenFlow. zip" in Ihr Microsoft Flow-Konto</span><span class="sxs-lookup"><span data-stu-id="7414c-187">[Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "TicketReopenFlow.Zip" to your Microsoft Flow account</span></span>

    2. <span data-ttu-id="7414c-188">Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*)</span><span class="sxs-lookup"><span data-stu-id="7414c-188">Edit details in Imported Flow (*See steps below*)</span></span> 

        1. <span data-ttu-id="7414c-189">Im ersten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-189">In the First block</span></span> 

             1. <span data-ttu-id="7414c-190">Wählen Sie Gruppenname aus, oder geben Sie die Gruppen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="7414c-190">Select group name or enter the group ID</span></span>

             2. <span data-ttu-id="7414c-191">Klicken Sie auf Aktionspaket, um die Aktions-ID einzugeben, die Sie für "StatusUpdateFromHelpDesk-ActionPackage. zip" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7414c-191">Click on action package to enter action id that you have given for "StatusUpdateFromHelpDesk-ActionPackage.Zip"</span></span>

             3. <span data-ttu-id="7414c-192">Aktion "alle" zuordnen</span><span class="sxs-lookup"><span data-stu-id="7414c-192">Map action to "All"</span></span>

                <img src="EmployeeHelpdesk-Images/8.JPG" width="600">

        2. <span data-ttu-id="7414c-193">Im zweiten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-193">In the second block</span></span>

             1. <span data-ttu-id="7414c-194">Geben Sie die Websiteadresse ein.</span><span class="sxs-lookup"><span data-stu-id="7414c-194">Enter the site address</span></span>

             2. <span data-ttu-id="7414c-195">Geben Sie den Listennamen ein.</span><span class="sxs-lookup"><span data-stu-id="7414c-195">Enter the list name</span></span> 

                <img src="EmployeeHelpdesk-Images/9.JPG" width="600">

        3. <span data-ttu-id="7414c-196">Im letzten Block</span><span class="sxs-lookup"><span data-stu-id="7414c-196">In the Last block</span></span>

             1. <span data-ttu-id="7414c-197">Geben Sie die Websiteadresse ein.</span><span class="sxs-lookup"><span data-stu-id="7414c-197">Enter the site address</span></span>

             2. <span data-ttu-id="7414c-198">Geben Sie den Listennamen ein.</span><span class="sxs-lookup"><span data-stu-id="7414c-198">Enter the list name</span></span>

                <img src="EmployeeHelpdesk-Images/10.JPG" width="600">

        4.  <span data-ttu-id="7414c-199">Speichern des Flusses</span><span class="sxs-lookup"><span data-stu-id="7414c-199">Save the Flow</span></span>
