# <a name="practice-tutorial-creating-a-new-kaizala-action"></a><span data-ttu-id="78c4d-101">Übungs Lernprogramm: Erstellen einer neuen Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="78c4d-101">Practice Tutorial: Creating a new Kaizala Action</span></span> 

## <a name="overview"></a><span data-ttu-id="78c4d-102">Übersicht</span><span class="sxs-lookup"><span data-stu-id="78c4d-102">Overview</span></span> 
<span data-ttu-id="78c4d-103">In diesem Lernprogramm erstellen wir eine benutzerdefinierte Kaizala-Aktion unter Verwendung des erweiterbaren Aktions Frameworks, das von der Kaizala-Plattform bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="78c4d-103">In this tutorial, we will create a custom Kaizala Action utilizing the extensible Action framework provided by the Kaizala platform.</span></span>

<span data-ttu-id="78c4d-104">Wir erstellen eine "Ask Feedback"-Aktion, die es Kaizala-Benutzern ermöglicht, Feedback von anderen Benutzern im Hinblick auf die 1-zu-5-Sterne-Bewertungen zu Fragen zu stellen – zusammen mit allen Kommentaren, die Sie bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="78c4d-104">We will create an “Ask Feedback” Action which will allow Kaizala users to ask for feedback from other users in terms of 1-to-5 star ratings on questions asked – along with any comments they would like to provide.</span></span>  

<span data-ttu-id="78c4d-105">Sie können Beispiel-Kaizala-Aktionspakete von [hier](https://manage.kaiza.la/MiniApps/DownloadSDK)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-105">You can download sample Kaizala Action packages from [here](https://manage.kaiza.la/MiniApps/DownloadSDK).</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="78c4d-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="78c4d-106">Pre-requisites</span></span> 
* <span data-ttu-id="78c4d-107">Ein Smartphone (Android/iOS) mit installierter Kaizala-App</span><span class="sxs-lookup"><span data-stu-id="78c4d-107">A smartphone (Android/iOS) with Kaizala app installed</span></span> 
* <span data-ttu-id="78c4d-108">Ein Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="78c4d-108">An Office365 Account</span></span> 
* <span data-ttu-id="78c4d-109">Zugriff auf einen HTML/JS-Editor (Notepad/Visual Studio Code/etc.)</span><span class="sxs-lookup"><span data-stu-id="78c4d-109">Access to an HTML/JS editor (notepad/Visual Studio Code/etc.)</span></span> 

## <a name="steps-to-create-a-sample-action"></a><span data-ttu-id="78c4d-110">Schritte zum Erstellen einer Beispielaktion</span><span class="sxs-lookup"><span data-stu-id="78c4d-110">Steps to create a sample Action</span></span>

*   <span data-ttu-id="78c4d-111">**Schritt 1:** Erstellen eines neuen Verzeichnisses für Ihr Aktionspaket</span><span class="sxs-lookup"><span data-stu-id="78c4d-111">**Step 1:** Create a new directory for your Action package</span></span>  
    * <span data-ttu-id="78c4d-112">Erstellen eines neuen Verzeichnisses auf dem Desktop & Name "Sample-Funktion"</span><span class="sxs-lookup"><span data-stu-id="78c4d-112">Create a new directory on your desktop & name it “SampleAction”</span></span> 
    * <span data-ttu-id="78c4d-113">Platzieren Sie alle nachfolgenden Dateien in diesem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="78c4d-113">Place all the subsequent files in this directory</span></span>

*   <span data-ttu-id="78c4d-114">**Schritt 2:** Definieren eines Datenmodells für Ihre Aktion</span><span class="sxs-lookup"><span data-stu-id="78c4d-114">**Step 2:** Define a data model for your Action</span></span> 
    * <span data-ttu-id="78c4d-115">Zunächst müssen wir das Datenmodell definieren, das in der benutzerdefinierten Aktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78c4d-115">First, we need to define the data model which will be used in our custom Action</span></span> 
    * <span data-ttu-id="78c4d-116">Die Kaizala-Aktionen sind derzeit formularbasierte Datenmodelle.</span><span class="sxs-lookup"><span data-stu-id="78c4d-116">The Kaizala Actions are currently form based data models.</span></span> <span data-ttu-id="78c4d-117">Daher müssen wir zunächst die "Fragen" definieren, die in unserem Formular eingeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-117">So, we will first need to define the ‘questions’ we need to include in our form.</span></span> 
    * <span data-ttu-id="78c4d-118">Da es sich um eine "Ask Feedback"-Aktion handelt, planen wir die Verwendung von zwei Daten teilen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-118">Since this is a “Ask Feedback” action – we will plan to use two pieces of data</span></span> 
        * <span data-ttu-id="78c4d-119">Numerische Bewertung (Wert 1 bis 5)</span><span class="sxs-lookup"><span data-stu-id="78c4d-119">Numeric rating (value 1 to 5)</span></span> 
        * <span data-ttu-id="78c4d-120">Kommentar/Verbatim-Feedback, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="78c4d-120">Comment/Verbatim feedback if any</span></span>  

    *   <span data-ttu-id="78c4d-121">Die Kaizala-formularinfrastruktur unterstützt folgende Fragetypen:</span><span class="sxs-lookup"><span data-stu-id="78c4d-121">Kaizala Forms infrastructure supports below question types:</span></span>

        | <span data-ttu-id="78c4d-122">Fragetyp</span><span class="sxs-lookup"><span data-stu-id="78c4d-122">Question Type</span></span> | <span data-ttu-id="78c4d-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78c4d-123">Description</span></span> |
        | :---: | :---: | 
        | <span data-ttu-id="78c4d-124">SingleSelect</span><span class="sxs-lookup"><span data-stu-id="78c4d-124">SingleSelect</span></span> | <span data-ttu-id="78c4d-125">Einzelne Auswahlfrage mit Optionen</span><span class="sxs-lookup"><span data-stu-id="78c4d-125">Single choice question with options</span></span> |
        | <span data-ttu-id="78c4d-126">MultiSelect</span><span class="sxs-lookup"><span data-stu-id="78c4d-126">MultiSelect</span></span> | <span data-ttu-id="78c4d-127">Multiple Choice-Frage mit Optionen</span><span class="sxs-lookup"><span data-stu-id="78c4d-127">Multiple choice question with options</span></span> | 
        | <span data-ttu-id="78c4d-128">Text</span><span class="sxs-lookup"><span data-stu-id="78c4d-128">Text</span></span> | <span data-ttu-id="78c4d-129">Frage mit nur-Text-Antwort</span><span class="sxs-lookup"><span data-stu-id="78c4d-129">Question with a plain text answer</span></span> |
        | <span data-ttu-id="78c4d-130">Numeric</span><span class="sxs-lookup"><span data-stu-id="78c4d-130">Numeric</span></span> | <span data-ttu-id="78c4d-131">Frage mit einer numerischen Antwort</span><span class="sxs-lookup"><span data-stu-id="78c4d-131">Question with a numeric answer</span></span> | 
        | <span data-ttu-id="78c4d-132">Ort</span><span class="sxs-lookup"><span data-stu-id="78c4d-132">Location</span></span> | <span data-ttu-id="78c4d-133">Frage mit Standort Antwort</span><span class="sxs-lookup"><span data-stu-id="78c4d-133">Question with a location answer</span></span> | 
        | <span data-ttu-id="78c4d-134">DateTime</span><span class="sxs-lookup"><span data-stu-id="78c4d-134">DateTime</span></span> | <span data-ttu-id="78c4d-135">Frage mit DateTime-Antwort</span><span class="sxs-lookup"><span data-stu-id="78c4d-135">Question with DateTime answer</span></span> | 
        | <span data-ttu-id="78c4d-136">Image</span><span class="sxs-lookup"><span data-stu-id="78c4d-136">Image</span></span> | <span data-ttu-id="78c4d-137">Frage mit einem Bild als Antwort</span><span class="sxs-lookup"><span data-stu-id="78c4d-137">Question with a picture as an answer</span></span> | 
    

    * <span data-ttu-id="78c4d-138">Für unsere beiden Fragen verwenden wir den Fragetyp "numerischer" & ' Text ' für die Bewertung der &-Kommentare.</span><span class="sxs-lookup"><span data-stu-id="78c4d-138">For our two questions we will use Question Type of 'Numeric' & 'Text' for Rating number & comments respectively</span></span> 
        * <span data-ttu-id="78c4d-139">Erstellen Sie eine neue Datei mit dem Namen "appModel. JSON", und platzieren Sie den folgenden Inhalt in der Datei.</span><span class="sxs-lookup"><span data-stu-id="78c4d-139">Create a new file called “appModel.json” and place the following content in the file.</span></span> <span data-ttu-id="78c4d-140">Die Datei enthält die beiden in der Reihenfolge aufgeführten Fragen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-140">The file contains the two questions listed in order</span></span> 
        `````
        { 
            "questions": [{ 
                    "title": "Rating", 
                    "type": "Numeric" 
                }, 
                { 
                    "title": "Comments", 
                    "type": "Text" 
                } 
            ], 
            "title": "Ask Feedback", 
            "visibility": "All", 
            "isAnonymous": false, 
            "isResponseAppended": false 
        } 
        `````
        * <span data-ttu-id="78c4d-141">Hinweis: der obige Code enthält auch zusätzliche Metadaten, die wir später erfahren werden (außerhalb des Bereichs für diese Sitzung).</span><span class="sxs-lookup"><span data-stu-id="78c4d-141">Note: Above code also contains additional metadata we will learn about later (out of scope for this session)</span></span> 
        * <span data-ttu-id="78c4d-142">Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="78c4d-142">Save the file</span></span>
        
*   <span data-ttu-id="78c4d-143">**Schritt 3:** Definieren einer Ansicht zum Erstellen der Anforderung für Feedback</span><span class="sxs-lookup"><span data-stu-id="78c4d-143">**Step 3:** Define a view for creating the request for feedback</span></span>  
    *   <span data-ttu-id="78c4d-144">Jetzt erstellen wir eine neue HTML-Datei, die zum Erstellen neuer Instanzen der Kaizala-Aktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78c4d-144">We will now create a new HTML file which will be used to create new instances of  our Kaizala Action</span></span> 
    *   <span data-ttu-id="78c4d-145">Dies ist die Ansicht, die aufgerufen wird, wenn das Symbol von der Palette aus getappt wird.</span><span class="sxs-lookup"><span data-stu-id="78c4d-145">This is the view that is invoked when the icon is tapped from the palette.</span></span> <span data-ttu-id="78c4d-146">In dieser Ansicht möchten wir Sie Fragen, was Sie Feedback zu wünschen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-146">In this view, we would like to ask them what they would like feedback on.</span></span> 
    * <span data-ttu-id="78c4d-147">Erstellen Sie eine neue Datei mit dem Namen "CreationView. html", und platzieren Sie den folgenden HTML-Code in der Datei.</span><span class="sxs-lookup"><span data-stu-id="78c4d-147">Create a new file called “CreationView.html” and place the below HTML in the file</span></span> 
        `````
        <html> 
         
        <head> 
        </head> 
         
        <body onload="onCreatePageLoad()"> 
            <br/> <br/> 
            <div> 
                <p>What would you like feedback on?</p> 
                <br/> <br/> 
                <input type="text" name="description" id="description" placeholder="Enter question text here" value=""> 
            </div> 
            <br/> <br/> 
            <div> 
                <input type="submit" name="submit" value="Submit" onclick="submitData()"> 
            </div> 
        </body> 
         
        </html> 
        `````
    *   <span data-ttu-id="78c4d-148">Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="78c4d-148">Save the file</span></span> 
*   <span data-ttu-id="78c4d-149">**Schritt 4:** Schließen Sie das Kaizala Forms JS SDK ein.</span><span class="sxs-lookup"><span data-stu-id="78c4d-149">**Step 4:** Include the Kaizala Forms JS SDK</span></span> 
    * <span data-ttu-id="78c4d-150">Um Entwicklern die Nutzung der Formularinfrastruktur zu erleichtern, stellt Kaizala eine JavaScript-Wrapperbibliothek bereit, die Sie in Ihre benutzerdefinierten Aktionen aufnehmen können.</span><span class="sxs-lookup"><span data-stu-id="78c4d-150">To make it easy for developers to leverage the Forms Infrastructure, Kaizala provides a JavaScript wrapper library that you can include in your custom Actions</span></span> 
    * <span data-ttu-id="78c4d-151">Laden Sie die Datei unten & in demselben Verzeichnis wie Ihre Datenmodell. JSON und CreationView. html</span><span class="sxs-lookup"><span data-stu-id="78c4d-151">Download the file below & place it in the same directory as your datamodel.json and CreationView.html</span></span> 
      *   <span data-ttu-id="78c4d-152">[Kaizala Forms js SDK ](https://manage.kaiza.la/MiniApps/downloadSDK).</span><span class="sxs-lookup"><span data-stu-id="78c4d-152">[Kaizala Forms JS SDK ](https://manage.kaiza.la/MiniApps/downloadSDK).</span></span> [<span data-ttu-id="78c4d-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="78c4d-153">Read more</span></span>](KASClient/README.md)
 
 
 
 
*   <span data-ttu-id="78c4d-154">**Schritt 5:** Verwenden des Kaizala Forms JS-SDK zum Senden eines Formulars</span><span class="sxs-lookup"><span data-stu-id="78c4d-154">**Step 5:** Use the Kaizala Forms JS SDK to submit form</span></span>   
    * <span data-ttu-id="78c4d-155">Fügen Sie den folgenden Codeausschnitt im <head> Element des "CreationView. html" hinzu, um auf das KAIZALA Forms js SDK zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-155">Add the following code snippet in the <head> element of your “CreationView.html” to refer to the Kaizala Forms JS SDK</span></span> 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * <span data-ttu-id="78c4d-156">Wenn der Benutzer jetzt auf Senden klickt, müssen wir überprüfen, ob er eine Frage eingegeben hat, um Feedback zu stellen – und die Formularinstanz erstellen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-156">Now, when the user clicks submit, we need to verify that he has entered a question to ask feedback on – and create the Form Instance</span></span>  
    * <span data-ttu-id="78c4d-157">Außerdem müssen wir das Formular beim Laden der Seite instanziieren.</span><span class="sxs-lookup"><span data-stu-id="78c4d-157">We also need to instantiate the form on page load.</span></span> <span data-ttu-id="78c4d-158">Fügen Sie den folgenden JavaScript-Codeausschnitt zu Ihrem "CreationView. HTML <head> " innerhalb des-Elements hinzu.</span><span class="sxs-lookup"><span data-stu-id="78c4d-158">Add the following JavaScript snippet to your “CreationView.html” inside the <head> element</span></span> 
        `````
            <script type="text/javascript"> 
                var _form; // type: KASForm
         
                // Below will be called on onload of CreationView.html 
                function onCreatePageLoad() { 
                    KASClient.Form.initFormAsync (function (form, error) { 
                        if (error != null) { 
                            showAlert("Error:initFormAsync:" + error); 
                            return; 
                        } 
                        _form = form; 
                    }); 
                } 
         
                function submitData() {
                    var description = document.getElementById("description").value; 
                    if (description == null || description == "") { 
                        KASClient.App.showNativeErrorMessage("Please enter the details for what you would like feedback on."); 
                    } else { 
                        // Set the description to form title 
                        _form.title = description; 
         
                        // Finally send the request 
                        KASClient.Form.submitFormRequest(_form); 
                    } 
                } 
            </script>
        `````

    *   <span data-ttu-id="78c4d-159">Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="78c4d-159">Save the file</span></span>

*   <span data-ttu-id="78c4d-160">**Schritt 6:** Erstellen des Aktionspaket Manifests</span><span class="sxs-lookup"><span data-stu-id="78c4d-160">**Step 6:** Create the Action package manifest</span></span>   
    *   <span data-ttu-id="78c4d-161">Nun, da wir einen Anschein dessen haben, was wir erreichen und erfolgreich eine Ansicht erstellen möchten, wird nun die Paket Manifestdatei erstellt, die auf diese Dateien verweist.</span><span class="sxs-lookup"><span data-stu-id="78c4d-161">Now that we have a semblance of what we want to achieve and successfully created a view – we will now create the package manifest file that refers to these files.</span></span> 
    * <span data-ttu-id="78c4d-162">Die Paket Manifestdatei enthält wichtige Informationen für die Kaizala-Plattform, damit Sie Ihre benutzerdefinierte Kaizala-Aktion erkennen und ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="78c4d-162">Package manifest file provides essential information for the Kaizala platform for it to recognize and run your custom Kaizala action.</span></span> 
    * <span data-ttu-id="78c4d-163">Wir erstellen ein Paketmanifest und geben Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="78c4d-163">We will create a package manifest and specify the following things:</span></span> 
        * <span data-ttu-id="78c4d-164">Anzeigename für Ihre Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="78c4d-164">Display name for your Kaizala Action</span></span> 
        * <span data-ttu-id="78c4d-165">Benutzerdefinierte ID für die Aktion</span><span class="sxs-lookup"><span data-stu-id="78c4d-165">Custom Id for the Action</span></span> 
        * <span data-ttu-id="78c4d-166">Zuordnung der Erstellungsansicht zu unserer CreationView. HTML-Seite</span><span class="sxs-lookup"><span data-stu-id="78c4d-166">Mapping of the creation view to our CreationView.html page</span></span> 

    * <span data-ttu-id="78c4d-167">Zuvor benötigen wir ein Symbol für das Aktionspaket.</span><span class="sxs-lookup"><span data-stu-id="78c4d-167">Before that we will need an icon for the Action package.</span></span> <span data-ttu-id="78c4d-168">Laden Sie die [Symboldatei](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & speichern Sie Sie als Icon. png im gleichen Ordner wie die anderen Dateien.</span><span class="sxs-lookup"><span data-stu-id="78c4d-168">Download the [icon file](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & save it as icon.png in the same folder as the other files.</span></span>

    * <span data-ttu-id="78c4d-169">Erstellen Sie eine neue Datei mit dem Namen "Package. JSON", und fügen Sie der Datei den folgenden Codeausschnitt hinzu.</span><span class="sxs-lookup"><span data-stu-id="78c4d-169">Create a new file called “package.json” and add following snippet to the file.</span></span> <span data-ttu-id="78c4d-170">Stellen Sie sicher, dass Sie die ID bearbeiten, damit Ihre Aktion eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="78c4d-170">Ensure that you edit the id to make your Action unique/distinct</span></span> 
        `````
        { 
            "id": "com.microsoft.mobile.kaizala.swads.FeedbackSample", 
            "schemaVersion": 1, 
            "version": 1,
            "minorVersion": 1,
            "providerName": "Microsoft Inc.", 
            "displayName": "Ask Feedback", 
            "description": "Custom action to collect feedback.", 
            "icon": "icon.png", 
            "appModel": "appModel.json", 
            "views": { 
                "CreationView": { 
                    "labelHeader": "Feedback requested", 
                    "sourceLocation": "CreationView.html" 
                } 
            } 
        }
        `````
    * <span data-ttu-id="78c4d-171">Sie können die Karte konfigurieren, die auf Kaizala Chat Canvas angezeigt wird, indem Sie die Zeichenfolgen im Paketmanifest angeben.</span><span class="sxs-lookup"><span data-stu-id="78c4d-171">You can configure the card that appears on Kaizala chat canvas by specifying the strings in the package manifest.</span></span>  
    * <span data-ttu-id="78c4d-172">Ändern Sie das Objekt "Views" in Ihrem Paketmanifest so, dass es mit dem folgenden Codeausschnitt übereinstimmt:</span><span class="sxs-lookup"><span data-stu-id="78c4d-172">Modify the “Views” object in you package manifest to match the below snippet:</span></span>
        `````
        "views": { 
                    "CreationView": { 
                        "labelHeader": "Feedback requested", 
                        "sourceLocation": "CreationView.html"            
                    }, 
                    "ChatCanvasCardView": { 
                        "labelResponded": "You have provided feedback.", 
                        "labelRespondToForm": "PROVIDE FEEDBACK", 
                        "isResponseEditable": true 
                    } 
        }   
        `````
    * <span data-ttu-id="78c4d-173">Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="78c4d-173">Save the file</span></span>

*   <span data-ttu-id="78c4d-174">**Schritt 7:** Erstellen der Antwort Ansicht</span><span class="sxs-lookup"><span data-stu-id="78c4d-174">**Step 7:** Create the response view</span></span>   
    * <span data-ttu-id="78c4d-175">Jetzt erstellen wir die Ansicht, die angezeigt wird, wenn Benutzer auf eine Instanz unserer Aktion reagieren Kaizala</span><span class="sxs-lookup"><span data-stu-id="78c4d-175">Now we will create the view that appears to Kaizala users responding to an instance of our action</span></span> 
    * <span data-ttu-id="78c4d-176">Erstellen Sie einen neuen Datei Aufruf ResponseView. html, und fügen Sie den folgenden Codeausschnitt in die Datei ein.</span><span class="sxs-lookup"><span data-stu-id="78c4d-176">Create a new file call ResponseView.html and insert the below snippet in the file</span></span> 
    * <span data-ttu-id="78c4d-177">Wir gehen wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="78c4d-177">We will do the following</span></span> 
        * <span data-ttu-id="78c4d-178">Hinzufügen einer Optionsfeldauswahl für die Bewertung</span><span class="sxs-lookup"><span data-stu-id="78c4d-178">Add radio button selection for the rating</span></span> 
        * <span data-ttu-id="78c4d-179">Vorbereiten eines Formular Antwortobjekts und des Codes zum Senden des Formulars</span><span class="sxs-lookup"><span data-stu-id="78c4d-179">Prepare a form response object and code to submit the form</span></span> 
        ````` 
            <html> 
             
            <head> 
                <title></title> 
                <script type="text/javascript" src="KASClient.js"></script> 
                <script> 
                    var _form; // type: KASForm
                    var _myFormResponses; // type: KASFormResponse[]
             
                    // Below will be called on onload of ResponseView.html 
                    function onResponsePageLoad() { 
                        KASClient.Form.getFormAsync(function (form, error) { 
                            if (error != null) { 
                                KASClient.App.showNativeErrorMessage("Error:getFormAsync:" + error); 
                                return; 
                            } 
                            _form = form; 
                            
                            // Document title would be the form title
                            document.getElementById("title").innerHTML = _form.title;
                            
                            KASClient.Form.getMyFormResponsesAsync(function (responses, error) { 
                                if (error != null) { 
                                    KASClient.App.showNativeErrorMessage("Error:getMyFormResponsesAsync:" + error); 
                                    return; 
                                } 
                                _myFormResponses = responses;
                                
                                // Render previous response, if any
                                if (isCurrentUserResponded()) {
                                    var rating = _myFormResponses[0].questionToAnswerMap["0"];
                                    var remark = _myFormResponses[0].questionToAnswerMap["1"];

                                    var options = document.getElementsByName('option');
                                    options[rating - 1].checked = true;

                                    document.getElementById("description").value = remark;
                                    document.getElementById("description").placeholder = "";
                                }
                            }); 
                        }); 
                    } 
             
                    function submitData() { 
                        var selectedOption = getSelectedOption(); 
                        var remark = document.getElementById("description").value; 
                        submitFormResponse(selectedOption, remark); 
                    } 
             
                    function getSelectedOption() { 
                        // Check which radio button is checked 
                        var options = document.getElementsByName('option'); 
                        for (var i = 0; i < options.length; i++) { 
                            if (options[i].checked) { 
                                return parseInt(options[i].value); 
                            } 
                        } 
                    } 
             
                    // Below will be called when responder submits a new response 
                    function submitFormResponse(selectedOption, remark) { 
                        if (remark == null || remark == "") { 
                            KASClient.App.showNativeErrorMessage("Please fill remark"); 
                        } else if (selectedOption == "") { 
                            KASClient.App.showNativeErrorMessage("Please select one option"); 
                        } else { 
                            // For submitting response a question-answer 
                            // map is required, lets create that! 
                            var questionToAnswerMap = JSON.parse("{}"); 
                            questionToAnswerMap[0] = selectedOption; 
                            questionToAnswerMap[1] = remark; 
             
                            var responseId = null; 
                            var isEditingPreviousResponse = false;
                            
                            // If there is a previous response, update it
                            if (isCurrentUserResponded()) {
                                responseId = _myFormResponses[0].id;
                                isEditingPreviousResponse = true;
                            }
             
                            // Finally submit the response 
                            KASClient.Form.sumbitFormResponse(questionToAnswerMap, responseId, isEditingPreviousResponse); 
                        } 
                    }
                    
                    function isCurrentUserResponded() {
                        return _myFormResponses && _myFormResponses.length > 0;
                    }
                </script> 
            </head> 
             
            <body onload="onResponsePageLoad()"> 
                <br/> <br/> 
                <div> 
                    <p id="title"></p> 
                </div> 
                <div> 
                    <br/> <br/> 
                    <div> 
                        <p>Select your rating:</p> 
                        <br/> <br/> 
                        <div> 
                            <label>1</label> 
                            <input type="radio" name="option" id="option0" value="1" checked> 
                        </div> 
                        <div> 
                            <label>2</label> 
                            <input type="radio" name="option" id="option1" value="2"> 
                        </div> 
                        <div> 
                            <label>3</label> 
                            <input type="radio" name="option" id="option2" value="3"> 
                        </div> 
                        <div> 
                            <label>4</label> 
                            <input type="radio" name="option" id="option3" value="4"> 
                        </div> 
                        <div> 
                            <label>5</label> 
                            <input type="radio" name="option" id="option4" value="5"> 
                        </div> 
                    </div> 
                    <br/> <br/> 
                    <div> 
                        <p>Comments</p> 
                        <input type="text" name="description" id="description" placeholder="Please enter your comments here."> 
                    </div> 
                    <br/> <br/> 
                </div> 
                <div class="footer"> 
                    <input type="submit" name="submit" value="Submit" onclick="submitData()"> 
                </div> 
            </body> 
             
            </html> 
            `````
*   **Step 8:** Create the summary view   
    * Now we will create the view that appears to Kaizala users viewing the summary of the action 
    * Create a new file call SummaryView.html and insert the below snippet in the file. This will create a summary view of the total ratings and comments

            <html> 
             
            <head> 
                <title></title> 
                <script type="text/javascript" src="KASClient.js"></script> 
                <script type="text/javascript"> 
                    // Globals 
                    var _form; // type: KASForm 
                    var _myFormResponses; // type: KASFormResponse[]
                    var _formSummary; // type: KASFormFlatSummary 
                    var _users; // type: Dictionary<UserId: KASUser>
             
                    // Below will be called on onload of SummaryView.html 
                    function onSummaryPageLoad() {            
                        KASClient.Form.getFormAsync(function (form, error) {                
                           if (error != null) {                    
                              KASClient.App.showNativeErrorMessage("Error:getFormAsync:" + error);                    
                              return;                
                           }                
                           _form = form;
                           KASClient.App.showProgressBar("Fetching summary");
                           KASClient.Form.getFormSummaryAsync(
                              function (flatSummary, processedSummary, error) { // In this callback data is fetched from local database
                                 if (error != null) {                    
                                    KASClient.App.showNativeErrorMessage("Error:getFormSummaryAsync:callback1:" + error);                    
                                    return;                
                                 } 
                                 onGetSummary(flatSummary);
                              },
                              function (flatSummary, processedSummary, error) { // In this callback data is fetched from server
                                 KASClient.App.hideProgressBar();
                                 if (error != null) {                    
                                    KASClient.App.showNativeErrorMessage("Error:getFormSummaryAsync:callback2:" + error);                    
                                    return;                
                                 }
                                 onGetSummary(flatSummary);
                              }
                           );           
                        });        
                     }

                     function onGetSummary(summary) {
                        _formSummary = summary;                    
                        KASClient.App.getUsersDetailsAsync(_formSummary.getRespondedUserIds(), function (users,
                           error) {                        
                           if (error != null) {                            
                              KASClient.App.showNativeErrorMessage("Error:getUsersDetailsAsync:" + error);                            
                              return;                        
                           }                        
                           _users = users;  // Document title would be the form title 
                           
                           document.getElementById("title").innerHTML = _form.title; 
                           
                           // Get all responses of the user, and find the average
                           var totalRating = 0;                        
                           var responseCount = 0;          
                           for (var userId in _users) {
                              var userResponses = _formSummary.getResponsesForUserId(userId); // type: Dictionary<QuestionId, string[]>
                              totalRating += parseInt(userResponses["0"][0]);                            
                              responseCount += 1;                       
                           } 
                           
                           document.getElementById("avg").innerHTML = totalRating / responseCount;                    
                        });
                     }
                </script> 
            </head> 
             
            <body onload="onSummaryPageLoad()"> 
                <div class="header"> 
                    <p id="title">Title</p> 
                    <br/> <br/> 
                    <p id="rating">Average Rating: </p> 
                    <p id="avg">avg</p> 
                </div> 
            </body> 
             
            </html>

    

    * Edit the Views object in your package manifest to the following: 
        `````
           <span data-ttu-id="78c4d-180">"Views": {              "CreationView": {                  "labelHeader": "Feedback angefordert",                  "SourceLocation": "CreationView. html"                        },              "ChatCanvasCardView": {                 " labelResponded ":" Sie haben Feedback zur Verfügung gestellt                  . "," labelRespondToForm ":" Feedback                  senden "," isResponseEditable              ":              true}," ResponseView  ": {" labelHeader ":" Feedback senden ",                 " SourceLocation ":" ResponseView. html "              },              " ResponseResultsView ": {  " labelPageHeader ":" Feedback Zusammenfassung ",                 " SourceLocation ":" SummaryView. html "              }     }        \`\`\`\`\`</span><span class="sxs-lookup"><span data-stu-id="78c4d-180">"views": {              "CreationView": {                  "labelHeader": "Feedback requested",                  "sourceLocation": "CreationView.html"                         },              "ChatCanvasCardView": {                   "labelResponded": "You have provided feedback.",                  "labelRespondToForm": "PROVIDE FEEDBACK",                  "isResponseEditable": true              },              "ResponseView": {  "labelHeader": "Provide feedback",                   "sourceLocation": "ResponseView.html"              },              "ResponseResultsView": {  "labelPageHeader": "Feedback summary",                   "sourceLocation": "SummaryView.html"              }     }         \`\`\`\`\`</span></span>
 
 
*   <span data-ttu-id="78c4d-181">**Schritt 9:** Erstellen des Kaizala-Aktionspakets</span><span class="sxs-lookup"><span data-stu-id="78c4d-181">**Step 9:** Create the Kaizala Action package</span></span> 
    * <span data-ttu-id="78c4d-182">ZIP alle Dateien in einer einzigen ZIP-Datei</span><span class="sxs-lookup"><span data-stu-id="78c4d-182">Zip all the files into a single zip file</span></span> 
    * <span data-ttu-id="78c4d-183">Stellen Sie sicher, dass der ZIP kein anderes Verzeichnis enthält, aber die Dateien befinden sich im Stammverzeichnis des ZIP-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="78c4d-183">Make sure that the zip does not include another directory inside it – but the files are present at the root directory of the zip</span></span>

*   <span data-ttu-id="78c4d-184">**Schritt 10:** Melden Sie sich beim Kaizala-Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="78c4d-184">**Step 10:** Log in to the Kaizala Management Portal</span></span>  
    * <span data-ttu-id="78c4d-185">Öffnen Sie ein Browserfenster, und navigieren Sie zuhttps://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="78c4d-185">Open a browser window and navigate to https://manage.kaiza.la/</span></span> 
    * <span data-ttu-id="78c4d-186">Klicken Sie in der oberen linken Ecke auf "Anmelden".</span><span class="sxs-lookup"><span data-stu-id="78c4d-186">On the top left corner, click on “Sign In”</span></span> 
    * <span data-ttu-id="78c4d-187">Geben Sie Ihre Office365-Anmeldeinformationen ein, um sich beim Portal anzumelden.</span><span class="sxs-lookup"><span data-stu-id="78c4d-187">Enter your Office365 credentials to log in to the portal.</span></span> <span data-ttu-id="78c4d-188">Erteilen Sie auf Anforderung Berechtigungen für das Verwaltungsportal, um auf Ihre Profilinformationen zuzugreifen (nur zum ersten Mal erforderlich).</span><span class="sxs-lookup"><span data-stu-id="78c4d-188">If requested, grant permissions to the management portal to access your profile information (needed only for the first time)</span></span> 
    * <span data-ttu-id="78c4d-189">Tippen Sie auf "Telefonnummer hinzufügen" in der oberen rechten Ecke & überprüfen Sie Ihre Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="78c4d-189">Tap on “Add Phone number” on the top right hand corner & verify your phone number</span></span> 

*   <span data-ttu-id="78c4d-190">**Schritt 11:** Hochladen des Aktionspakets</span><span class="sxs-lookup"><span data-stu-id="78c4d-190">**Step 11:** Upload the action package</span></span>  
    * <span data-ttu-id="78c4d-191">Navigieren Sie zu "Aktionen" mit dem linken navbar</span><span class="sxs-lookup"><span data-stu-id="78c4d-191">Navigate to “Actions” using the left Navbar</span></span> 
    * <span data-ttu-id="78c4d-192">Klicken Sie in der Dropdownliste auf der rechten Seite auf "Aktion importieren" und dann auf Start.</span><span class="sxs-lookup"><span data-stu-id="78c4d-192">From the drop-down on the right – choose “Import Action” and click Start</span></span> 
    * <span data-ttu-id="78c4d-193">Klicken Sie auf Hochladen und wählen Sie die ZIP-Datei aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="78c4d-193">Click on upload – and select the zip file you created</span></span> 
    * <span data-ttu-id="78c4d-194">Klicken Sie auf Importieren</span><span class="sxs-lookup"><span data-stu-id="78c4d-194">Click on import</span></span>
    * <span data-ttu-id="78c4d-195">Nachdem das Paket erfolgreich importiert wurde, bestätigen Sie, dass Sie erneut nach Aktionen navigieren. Die Aktion sollte unter "mit dieser ID erstellt" aufgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="78c4d-195">Once the package is successfully imported, confirm by browsing to Actions again.You should see your Action listed under “created by this Id”</span></span>
    * <span data-ttu-id="78c4d-196">Sie können diese Aktion testen, indem Sie [](test.md) die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-196">You can test this Action by following steps [here](test.md)</span></span>

*   <span data-ttu-id="78c4d-197">**Schritt 12:** Erstellen einer neuen Kaizala-Gruppe</span><span class="sxs-lookup"><span data-stu-id="78c4d-197">**Step 12:** Create a new Kaizala Group</span></span>  
    * <span data-ttu-id="78c4d-198">Navigieren Sie im Kaizala-Verwaltungsportal zu "Gruppen", indem Sie den linken navbar</span><span class="sxs-lookup"><span data-stu-id="78c4d-198">On Kaizala Management portal, navigate to “Groups” using the left navbar</span></span> 
    * <span data-ttu-id="78c4d-199">Tippen Sie auf "Gruppe erstellen".</span><span class="sxs-lookup"><span data-stu-id="78c4d-199">Tap on “Create Group”</span></span> 
    * <span data-ttu-id="78c4d-200">Name der Gruppe "Kaizala Actions testing"</span><span class="sxs-lookup"><span data-stu-id="78c4d-200">Name the group “Kaizala Actions Testing”</span></span> 
    * <span data-ttu-id="78c4d-201">Sicherstellen, dass die Gruppe in der Kaizala-App angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="78c4d-201">Verify that the group appears on your Kaizala app</span></span>

*   <span data-ttu-id="78c4d-202">**Schritt 13:** Veröffentlichen der Aktion in der Gruppe</span><span class="sxs-lookup"><span data-stu-id="78c4d-202">**Step 13:** Publish the Action to the Group</span></span>  
    * <span data-ttu-id="78c4d-203">Navigieren Sie zu "Gruppen" mithilfe der linken navbar</span><span class="sxs-lookup"><span data-stu-id="78c4d-203">Navigate to “Groups” using the left Navbar</span></span> 
    * <span data-ttu-id="78c4d-204">Tippen Sie auf den Gruppennamen, den Sie in Schritt 13 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="78c4d-204">Tap on the group name you created in Step 13</span></span> 
    * <span data-ttu-id="78c4d-205">Tippen Sie auf die Registerkarte "Aktionen"</span><span class="sxs-lookup"><span data-stu-id="78c4d-205">Tap on the “Actions” tab</span></span> 
    * <span data-ttu-id="78c4d-206">Wählen Sie die in Schritt 12 erstellte Aktion & klicken Sie auf Aktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="78c4d-206">Select the Action you created in Step 12 & click “Add Action”.</span></span> <span data-ttu-id="78c4d-207">Die benutzerdefinierte Kaizala-Aktion sollte jetzt auf der Registerkarte Discover angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="78c4d-207">You should now see your custom Kaizala Action appearing on the Discover tab</span></span>

*   <span data-ttu-id="78c4d-208">**Schritt 14:** Benutzerdefinierte Kaizala-Aktion verwenden</span><span class="sxs-lookup"><span data-stu-id="78c4d-208">**Step 14:** Use custom Kaizala Action</span></span>  
    * <span data-ttu-id="78c4d-209">Fügen Sie die benutzerdefinierte Aktion zu Ihrer Palette hinzu, und verwenden Sie Sie in Ihrer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="78c4d-209">Add the custom Action to your palette and use it in your group.</span></span> 

 
 
 
 
 
