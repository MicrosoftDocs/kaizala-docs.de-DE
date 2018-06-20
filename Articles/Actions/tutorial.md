# <a name="practice-tutorial-creating-a-new-kaizala-action"></a><span data-ttu-id="41177-101">Praxis-Lernprogramm: Erstellen einer neuen Kaizala-Aktion</span><span class="sxs-lookup"><span data-stu-id="41177-101">Practice Tutorial: Creating a new Kaizala Action</span></span> 

## <a name="overview"></a><span data-ttu-id="41177-102">Übersicht</span><span class="sxs-lookup"><span data-stu-id="41177-102">Overview</span></span> 
<span data-ttu-id="41177-103">In diesem Lernprogramm erstellen wir eine benutzerdefinierte Kaizala-Aktion mit dem extensible Aktion Framework der Kaizala-Plattform.</span><span class="sxs-lookup"><span data-stu-id="41177-103">In this tutorial, we will create a custom Kaizala Action utilizing the extensible Action framework provided by the Kaizala platform.</span></span>

<span data-ttu-id="41177-104">Es wird eine Aktion "Bitten Sie Feedback" erstellt, die zulässig, Kaizala Benutzer des Clientcomputers fordern Feedback von anderen Benutzern im Hinblick auf Stern Bewertungen von 1 bis 5 auf Fragen – Kommentare, die sie bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="41177-104">We will create an “Ask Feedback” Action which will allow Kaizala users to ask for feedback from other users in terms of 1-to-5 star ratings on questions asked – along with any comments they would like to provide.</span></span>  

<span data-ttu-id="41177-105">Sie können Beispiel Kaizala Aktion Pakete [hier](https://manage.kaiza.la/MiniApps/DownloadSDK)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="41177-105">You can download sample Kaizala Action packages from [here](https://manage.kaiza.la/MiniApps/DownloadSDK).</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="41177-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="41177-106">Pre-requisites</span></span> 
* <span data-ttu-id="41177-107">Einem Smartphone (Android/iOS) mit Kaizala app installiert</span><span class="sxs-lookup"><span data-stu-id="41177-107">A smartphone (Android/iOS) with Kaizala app installed</span></span> 
* <span data-ttu-id="41177-108">Ein Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="41177-108">An Office365 Account</span></span> 
* <span data-ttu-id="41177-109">Zugriff auf eine HTML/JS-Editor (Studio Code/Etc Editor/visuelle.)</span><span class="sxs-lookup"><span data-stu-id="41177-109">Access to an HTML/JS editor (notepad/Visual Studio Code/etc.)</span></span> 

## <a name="steps-to-create-a-sample-action"></a><span data-ttu-id="41177-110">Schritte zum Erstellen einer Stichprobe Aktion</span><span class="sxs-lookup"><span data-stu-id="41177-110">Steps to create a sample Action</span></span>

*   <span data-ttu-id="41177-111">**Schritt 1:** Erstellen Sie ein neues Verzeichnis für Ihr Paket Aktion</span><span class="sxs-lookup"><span data-stu-id="41177-111">**Step 1:** Create a new directory for your Action package</span></span>  
    * <span data-ttu-id="41177-112">Erstellen Sie ein neues Verzeichnis auf Ihrem Desktop, und nennen Sie sie "SampleAction"</span><span class="sxs-lookup"><span data-stu-id="41177-112">Create a new directory on your desktop & name it “SampleAction”</span></span> 
    * <span data-ttu-id="41177-113">Speichern Sie alle nachfolgenden Dateien in diesem Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="41177-113">Place all the subsequent files in this directory</span></span>

*   <span data-ttu-id="41177-114">**Schritt 2:** Ein Datenmodell für die Aktion definieren</span><span class="sxs-lookup"><span data-stu-id="41177-114">**Step 2:** Define a data model for your Action</span></span> 
    * <span data-ttu-id="41177-115">Erstens müssen definieren das Datenmodell der verwendet wird, in unserer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="41177-115">First, we need to define the data model which will be used in our custom Action</span></span> 
    * <span data-ttu-id="41177-116">Die Kaizala Aktionen sind derzeit Datenmodelle Formular basiert.</span><span class="sxs-lookup"><span data-stu-id="41177-116">The Kaizala Actions are currently form based data models.</span></span> <span data-ttu-id="41177-117">Wir müssen also zuerst die wir in unseren Formular einschließen müssen Fragen definieren.</span><span class="sxs-lookup"><span data-stu-id="41177-117">So, we will first need to define the ‘questions’ we need to include in our form.</span></span> 
    * <span data-ttu-id="41177-118">Da hierbei handelt es sich um eine Aktion "Bitten Sie Feedback" – Es werden zwei Datenelemente verwenden möchten</span><span class="sxs-lookup"><span data-stu-id="41177-118">Since this is a “Ask Feedback” action – we will plan to use two pieces of data</span></span> 
        * <span data-ttu-id="41177-119">Numerische Bewertung (Wert 1 bis 5)</span><span class="sxs-lookup"><span data-stu-id="41177-119">Numeric rating (value 1 to 5)</span></span> 
        * <span data-ttu-id="41177-120">Kommentar/Verbatim Feedback, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="41177-120">Comment/Verbatim feedback if any</span></span>  

    *   <span data-ttu-id="41177-121">Kaizala Forms-Infrastruktur unter Fragetypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="41177-121">Kaizala Forms infrastructure supports below question types:</span></span>

        | <span data-ttu-id="41177-122">Art der Frage</span><span class="sxs-lookup"><span data-stu-id="41177-122">Question Type</span></span> | <span data-ttu-id="41177-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41177-123">Description</span></span> |
        | :---: | :---: | 
        | <span data-ttu-id="41177-124">SingleSelect</span><span class="sxs-lookup"><span data-stu-id="41177-124">SingleSelect</span></span> | <span data-ttu-id="41177-125">Einzelwertoption Frage mit Optionen</span><span class="sxs-lookup"><span data-stu-id="41177-125">Single choice question with options</span></span> |
        | <span data-ttu-id="41177-126">MultiSelect</span><span class="sxs-lookup"><span data-stu-id="41177-126">MultiSelect</span></span> | <span data-ttu-id="41177-127">Mehrere Choice-Frage mit Optionen</span><span class="sxs-lookup"><span data-stu-id="41177-127">Multiple choice question with options</span></span> | 
        | <span data-ttu-id="41177-128">Text</span><span class="sxs-lookup"><span data-stu-id="41177-128">Text</span></span> | <span data-ttu-id="41177-129">Frage und Antwort wird eine nur-text</span><span class="sxs-lookup"><span data-stu-id="41177-129">Question with a plain text answer</span></span> |
        | <span data-ttu-id="41177-130">Numerisch</span><span class="sxs-lookup"><span data-stu-id="41177-130">Numeric</span></span> | <span data-ttu-id="41177-131">Mit einem numerischen Antwort Frage</span><span class="sxs-lookup"><span data-stu-id="41177-131">Question with a numeric answer</span></span> | 
        | <span data-ttu-id="41177-132">Speicherort</span><span class="sxs-lookup"><span data-stu-id="41177-132">Location</span></span> | <span data-ttu-id="41177-133">Frage mit einer Antwort Speicherort</span><span class="sxs-lookup"><span data-stu-id="41177-133">Question with a location answer</span></span> | 
        | <span data-ttu-id="41177-134">DateTime</span><span class="sxs-lookup"><span data-stu-id="41177-134">DateTime</span></span> | <span data-ttu-id="41177-135">Frage mit DateTime-Antwort</span><span class="sxs-lookup"><span data-stu-id="41177-135">Question with DateTime answer</span></span> | 
        | <span data-ttu-id="41177-136">Image</span><span class="sxs-lookup"><span data-stu-id="41177-136">Image</span></span> | <span data-ttu-id="41177-137">Frage mit einem Bild als Antwort</span><span class="sxs-lookup"><span data-stu-id="41177-137">Question with a picture as an answer</span></span> | 
    

    * <span data-ttu-id="41177-138">Für unsere zwei Fragen verwenden Fragetyp 'Numeric' und 'Text' wir zur Bewertung von Anzahl & Kommentare</span><span class="sxs-lookup"><span data-stu-id="41177-138">For our two questions we will use Question Type of 'Numeric' & 'Text' for Rating number & comments respectively</span></span> 
        * <span data-ttu-id="41177-139">Erstellen Sie eine neue Datei mit dem Namen "appModel.json", und legen Sie den folgenden Inhalt in der Datei.</span><span class="sxs-lookup"><span data-stu-id="41177-139">Create a new file called “appModel.json” and place the following content in the file.</span></span> <span data-ttu-id="41177-140">Die Datei enthält die beiden Fragen in der Reihenfolge aufgeführt</span><span class="sxs-lookup"><span data-stu-id="41177-140">The file contains the two questions listed in order</span></span> 
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
        * <span data-ttu-id="41177-141">Hinweis: Über Code enthält außerdem zusätzlichen Metadaten wir kennen zu einem späteren Zeitpunkt (außerhalb des Gültigkeitsbereichs für diese Sitzung)</span><span class="sxs-lookup"><span data-stu-id="41177-141">Note: Above code also contains additional metadata we will learn about later (out of scope for this session)</span></span> 
        * <span data-ttu-id="41177-142">Speichern Sie die Datei</span><span class="sxs-lookup"><span data-stu-id="41177-142">Save the file</span></span>
        
*   <span data-ttu-id="41177-143">**Schritt 3:** Definieren einer Ansicht für das Erstellen der Anforderung für feedback</span><span class="sxs-lookup"><span data-stu-id="41177-143">**Step 3:** Define a view for creating the request for feedback</span></span>  
    *   <span data-ttu-id="41177-144">Es wird jetzt eine neue HTML-Datei erstellt, die zum Erstellen neuer Instanzen von unseren Kaizala-Aktion verwendet wird</span><span class="sxs-lookup"><span data-stu-id="41177-144">We will now create a new HTML file which will be used to create new instances of  our Kaizala Action</span></span> 
    *   <span data-ttu-id="41177-145">Dies ist die Ansicht, die aufgerufen wird, wenn das Symbol aus der Palette getippt wird.</span><span class="sxs-lookup"><span data-stu-id="41177-145">This is the view that is invoked when the icon is tapped from the palette.</span></span> <span data-ttu-id="41177-146">In dieser Ansicht möchten wir sie bitten, was sie Feedback wünschen.</span><span class="sxs-lookup"><span data-stu-id="41177-146">In this view, we would like to ask them what they would like feedback on.</span></span> 
    * <span data-ttu-id="41177-147">Erstellen Sie eine neue Datei namens "CreationView.html" und Ort der unter HTML in der Datei</span><span class="sxs-lookup"><span data-stu-id="41177-147">Create a new file called “CreationView.html” and place the below HTML in the file</span></span> 
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
    *   <span data-ttu-id="41177-148">Speichern Sie die Datei</span><span class="sxs-lookup"><span data-stu-id="41177-148">Save the file</span></span> 
*   <span data-ttu-id="41177-149">**Schritt 4:** Enthalten Sie die Kaizala Forms JS-SDK</span><span class="sxs-lookup"><span data-stu-id="41177-149">**Step 4:** Include the Kaizala Forms JS SDK</span></span> 
    * <span data-ttu-id="41177-150">Um Entwicklern die Nutzung der Forms-Infrastruktur zu erleichtern, bietet Kaizala eine JavaScript-Wrapper-Bibliothek, die Sie in Ihre benutzerdefinierten Aktionen hinzufügen können</span><span class="sxs-lookup"><span data-stu-id="41177-150">To make it easy for developers to leverage the Forms Infrastructure, Kaizala provides a JavaScript wrapper library that you can include in your custom Actions</span></span> 
    * <span data-ttu-id="41177-151">Laden Sie die folgende Datei & platzieren Sie diese im gleichen Verzeichnis befindet wie die datamodel.json und CreationView.html</span><span class="sxs-lookup"><span data-stu-id="41177-151">Download the file below & place it in the same directory as your datamodel.json and CreationView.html</span></span> 
      *   <span data-ttu-id="41177-152">[Kaizala Forms JS-SDK ](https://manage.kaiza.la/MiniApps/downloadSDK).</span><span class="sxs-lookup"><span data-stu-id="41177-152">[Kaizala Forms JS SDK ](https://manage.kaiza.la/MiniApps/downloadSDK).</span></span> [<span data-ttu-id="41177-153">Erfahren Sie mehr</span><span class="sxs-lookup"><span data-stu-id="41177-153">Read more</span></span>](KASClient/README.md)
 
 
 
 
*   <span data-ttu-id="41177-154">**Schritt 5:** Verwenden Sie das Kaizala Forms JS-SDK Formular senden</span><span class="sxs-lookup"><span data-stu-id="41177-154">**Step 5:** Use the Kaizala Forms JS SDK to submit form</span></span>   
    * <span data-ttu-id="41177-155">Hinzufügen den folgende Codeausschnitt in das <head> Bestandteil Ihrer "CreationView.html" verweisen auf die Kaizala Forms JS-SDK</span><span class="sxs-lookup"><span data-stu-id="41177-155">Add the following code snippet in the <head> element of your “CreationView.html” to refer to the Kaizala Forms JS SDK</span></span> 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * <span data-ttu-id="41177-156">Nun, wenn der Benutzer auf Absenden klickt, müssen wir stellen Sie sicher, dass er eine Frage, um Feedback auf – Fragen und erstellen Sie die Formularinstanz eingegeben hat</span><span class="sxs-lookup"><span data-stu-id="41177-156">Now, when the user clicks submit, we need to verify that he has entered a question to ask feedback on – and create the Form Instance</span></span>  
    * <span data-ttu-id="41177-157">Wir müssen auch das Formular beim Laden der Seite zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="41177-157">We also need to instantiate the form on page load.</span></span> <span data-ttu-id="41177-158">Fügen Sie den folgenden JavaScript-Codeausschnitt an Ihre "CreationView.html" innerhalb der <head> Element</span><span class="sxs-lookup"><span data-stu-id="41177-158">Add the following JavaScript snippet to your “CreationView.html” inside the <head> element</span></span> 
        `````
            <script type="text/javascript"> 
                var _form; // type: KASForm
         
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

    *   <span data-ttu-id="41177-159">Speichern Sie die Datei</span><span class="sxs-lookup"><span data-stu-id="41177-159">Save the file</span></span>

*   <span data-ttu-id="41177-160">**Schritt 6:** Erstellen Sie das Manifest der Aktion-Paket</span><span class="sxs-lookup"><span data-stu-id="41177-160">**Step 6:** Create the Action package manifest</span></span>   
    *   <span data-ttu-id="41177-161">Nun, da wir haben einen Semblance was wir erreichen möchten und erfolgreich erstellt eine Ansicht – es wird jetzt Erstellen der Paketmanifestdatei, bezieht sich auf diese Dateien.</span><span class="sxs-lookup"><span data-stu-id="41177-161">Now that we have a semblance of what we want to achieve and successfully created a view – we will now create the package manifest file that refers to these files.</span></span> 
    * <span data-ttu-id="41177-162">Paket-Manifestdatei enthält wichtige Informationen für die Plattform Kaizala dafür zu erkennen und die benutzerdefinierte Kaizala-Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="41177-162">Package manifest file provides essential information for the Kaizala platform for it to recognize and run your custom Kaizala action.</span></span> 
    * <span data-ttu-id="41177-163">Erstellen Sie ein Paketmanifest und geben Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="41177-163">We will create a package manifest and specify the following things:</span></span> 
        * <span data-ttu-id="41177-164">Anzeigename für die Aktion Kaizala</span><span class="sxs-lookup"><span data-stu-id="41177-164">Display name for your Kaizala Action</span></span> 
        * <span data-ttu-id="41177-165">Benutzerdefinierte Id für die Aktion</span><span class="sxs-lookup"><span data-stu-id="41177-165">Custom Id for the Action</span></span> 
        * <span data-ttu-id="41177-166">Zuordnen der Erstellung Ansicht zu unserer CreationView.html-Seite</span><span class="sxs-lookup"><span data-stu-id="41177-166">Mapping of the creation view to our CreationView.html page</span></span> 

    * <span data-ttu-id="41177-167">Vor dem Ausführen der benötigen wir ein Symbol für das Paket Aktion.</span><span class="sxs-lookup"><span data-stu-id="41177-167">Before that we will need an icon for the Action package.</span></span> <span data-ttu-id="41177-168">Laden Sie die [Symboldatei](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & icon.png im selben Ordner wie die anderen Dateien speichern.</span><span class="sxs-lookup"><span data-stu-id="41177-168">Download the [icon file](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & save it as icon.png in the same folder as the other files.</span></span>

    * <span data-ttu-id="41177-169">Erstellen Sie eine neue Datei mit dem Namen "package.json", und fügen Sie Sie der Datei folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="41177-169">Create a new file called “package.json” and add following snippet to the file.</span></span> <span data-ttu-id="41177-170">Stellen Sie sicher, dass Sie die Id, um Ihre Aktion eindeutige/unterschiedlichen Stellen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="41177-170">Ensure that you edit the id to make your Action unique/distinct</span></span> 
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
    * <span data-ttu-id="41177-171">Sie können die Karte, die angezeigt wird auf Kaizala Chat Zeichenbereich konfigurieren, durch die Zeichenfolgen im Paketmanifest angeben.</span><span class="sxs-lookup"><span data-stu-id="41177-171">You can configure the card that appears on Kaizala chat canvas by specifying the strings in the package manifest.</span></span>  
    * <span data-ttu-id="41177-172">Ändern Sie das Objekt "Ansichten" in Ihrem Paketmanifest entsprechend der unter Snippet:</span><span class="sxs-lookup"><span data-stu-id="41177-172">Modify the “Views” object in you package manifest to match the below snippet:</span></span>
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
    * <span data-ttu-id="41177-173">Speichern Sie die Datei</span><span class="sxs-lookup"><span data-stu-id="41177-173">Save the file</span></span>

*   <span data-ttu-id="41177-174">**Schritt 7:** Erstellen Sie die Antwort-Ansicht</span><span class="sxs-lookup"><span data-stu-id="41177-174">**Step 7:** Create the response view</span></span>   
    * <span data-ttu-id="41177-175">Jetzt erstellen die Ansicht wir, die Kaizala Benutzer zu einer Instanz von unseren Aktion reagiert</span><span class="sxs-lookup"><span data-stu-id="41177-175">Now we will create the view that appears to Kaizala users responding to an instance of our action</span></span> 
    * <span data-ttu-id="41177-176">Erstellen einen neuen Datei Anruf ResponseView.html, und fügen Sie die unten Ausschnitt in der Datei</span><span class="sxs-lookup"><span data-stu-id="41177-176">Create a new file call ResponseView.html and insert the below snippet in the file</span></span> 
    * <span data-ttu-id="41177-177">Wir die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="41177-177">We will do the following</span></span> 
        * <span data-ttu-id="41177-178">Radio Schaltfläche Auswahl für die Bewertung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="41177-178">Add radio button selection for the rating</span></span> 
        * <span data-ttu-id="41177-179">Vorbereiten einer Form Response-Objekt und den Code zum Senden des Formulars</span><span class="sxs-lookup"><span data-stu-id="41177-179">Prepare a form response object and code to submit the form</span></span> 
        ````` 
            <html> 
             
            <head> 
                <title></title> 
                <script type="text/javascript" src="KASClient.js"></script> 
                <script> 
                    var _form; // type: KASForm
                    var _myFormResponses; // type: KASFormResponse[]
             
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
                    var _users; // type: Dictionary<UserId: KASUser>
             
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
                           _users = users;  // Document title would be the form title 
                           
                           document.getElementById("title").innerHTML = _form.title; 
                           
                           // Get all responses of the user, and find the average
                           var totalRating = 0;                        
                           var responseCount = 0;          
                           for (var userId in _users) {
                              var userResponses = _formSummary.getResponsesForUserId(userId); // type: Dictionary<QuestionId, string[]>
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
           "views": { 
                    "CreationView": { 
                        "labelHeader": "Feedback requested", 
                        "sourceLocation": "CreationView.html"            
                    }, 
                    "ChatCanvasCardView": {
                        "labelResponded": "You have provided feedback.", 
                        "labelRespondToForm": "PROVIDE FEEDBACK", 
                        "isResponseEditable": true 
                    }, 
                    "ResponseView": { 
                        "labelHeader": "Provide feedback",
                        "sourceLocation": "ResponseView.html" 
                    }, 
                    "ResponseResultsView": { 
                        "labelPageHeader": "Feedback summary"
                        "sourceLocation": "SummaryView.html" 
                    } 
           }       
         `````
 
 
*   **Step 9:** Create the Kaizala Action package 
    * Zip all the files into a single zip file 
    * Make sure that the zip does not include another directory inside it – but the files are present at the root directory of the zip

*   **Step 10:** Log in to the Kaizala Management Portal  
    * Open a browser window and navigate to https://manage.kaiza.la/ 
    * On the top left corner, click on “Sign In” 
    * Enter your Office365 credentials to log in to the portal. If requested, grant permissions to the management portal to access your profile information (needed only for the first time) 
    * Tap on “Add Phone number” on the top right hand corner & verify your phone number 

*   **Step 11:** Upload the action package  
    * Navigate to “Actions” using the left Navbar 
    * From the drop-down on the right – choose “Import Action” and click Start 
    * Click on upload – and select the zip file you created 
    * Click on import
    * Once the package is successfully imported, confirm by browsing to Actions again.You should see your Action listed under “created by this Id”
    * You can test this Action by following steps [here](test.md)

*   **Step 12:** Create a new Kaizala Group  
    * On Kaizala Management portal, navigate to “Groups” using the left navbar 
    * Tap on “Create Group” 
    * Name the group “Kaizala Actions Testing” 
    * Verify that the group appears on your Kaizala app

*   **Step 13:** Publish the Action to the Group  
    * Navigate to “Groups” using the left Navbar 
    * Tap on the group name you created in Step 13 
    * Tap on the “Actions” tab 
    * Select the Action you created in Step 12 & click “Add Action”. You should now see your custom Kaizala Action appearing on the Discover tab

*   **Step 14:** Use custom Kaizala Action  
    * Add the custom Action to your palette and use it in your group. 

 
 
 
 
 
