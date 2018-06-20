# <a name="practice-tutorial-creating-a-new-kaizala-action"></a>Praxis-Lernprogramm: Erstellen einer neuen Kaizala-Aktion 

## <a name="overview"></a>Übersicht 
In diesem Lernprogramm erstellen wir eine benutzerdefinierte Kaizala-Aktion mit dem extensible Aktion Framework der Kaizala-Plattform.

Es wird eine Aktion "Bitten Sie Feedback" erstellt, die zulässig, Kaizala Benutzer des Clientcomputers fordern Feedback von anderen Benutzern im Hinblick auf Stern Bewertungen von 1 bis 5 auf Fragen – Kommentare, die sie bereitstellen möchten.  

Sie können Beispiel Kaizala Aktion Pakete [hier](https://manage.kaiza.la/MiniApps/DownloadSDK)heruntergeladen werden.

## <a name="pre-requisites"></a>Voraussetzungen 
* Einem Smartphone (Android/iOS) mit Kaizala app installiert 
* Ein Office365-Konto 
* Zugriff auf eine HTML/JS-Editor (Studio Code/Etc Editor/visuelle.) 

## <a name="steps-to-create-a-sample-action"></a>Schritte zum Erstellen einer Stichprobe Aktion

*   **Schritt 1:** Erstellen Sie ein neues Verzeichnis für Ihr Paket Aktion  
    * Erstellen Sie ein neues Verzeichnis auf Ihrem Desktop, und nennen Sie sie "SampleAction" 
    * Speichern Sie alle nachfolgenden Dateien in diesem Verzeichnis

*   **Schritt 2:** Ein Datenmodell für die Aktion definieren 
    * Erstens müssen definieren das Datenmodell der verwendet wird, in unserer benutzerdefinierten Aktion 
    * Die Kaizala Aktionen sind derzeit Datenmodelle Formular basiert. Wir müssen also zuerst die wir in unseren Formular einschließen müssen Fragen definieren. 
    * Da hierbei handelt es sich um eine Aktion "Bitten Sie Feedback" – Es werden zwei Datenelemente verwenden möchten 
        * Numerische Bewertung (Wert 1 bis 5) 
        * Kommentar/Verbatim Feedback, falls vorhanden  

    *   Kaizala Forms-Infrastruktur unter Fragetypen werden unterstützt:

        | Art der Frage | Beschreibung |
        | :---: | :---: | 
        | SingleSelect | Einzelwertoption Frage mit Optionen |
        | MultiSelect | Mehrere Choice-Frage mit Optionen | 
        | Text | Frage und Antwort wird eine nur-text |
        | Numerisch | Mit einem numerischen Antwort Frage | 
        | Speicherort | Frage mit einer Antwort Speicherort | 
        | DateTime | Frage mit DateTime-Antwort | 
        | Image | Frage mit einem Bild als Antwort | 
    

    * Für unsere zwei Fragen verwenden Fragetyp 'Numeric' und 'Text' wir zur Bewertung von Anzahl & Kommentare 
        * Erstellen Sie eine neue Datei mit dem Namen "appModel.json", und legen Sie den folgenden Inhalt in der Datei. Die Datei enthält die beiden Fragen in der Reihenfolge aufgeführt 
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
        * Hinweis: Über Code enthält außerdem zusätzlichen Metadaten wir kennen zu einem späteren Zeitpunkt (außerhalb des Gültigkeitsbereichs für diese Sitzung) 
        * Speichern Sie die Datei
        
*   **Schritt 3:** Definieren einer Ansicht für das Erstellen der Anforderung für feedback  
    *   Es wird jetzt eine neue HTML-Datei erstellt, die zum Erstellen neuer Instanzen von unseren Kaizala-Aktion verwendet wird 
    *   Dies ist die Ansicht, die aufgerufen wird, wenn das Symbol aus der Palette getippt wird. In dieser Ansicht möchten wir sie bitten, was sie Feedback wünschen. 
    * Erstellen Sie eine neue Datei namens "CreationView.html" und Ort der unter HTML in der Datei 
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
    *   Speichern Sie die Datei 
*   **Schritt 4:** Enthalten Sie die Kaizala Forms JS-SDK 
    * Um Entwicklern die Nutzung der Forms-Infrastruktur zu erleichtern, bietet Kaizala eine JavaScript-Wrapper-Bibliothek, die Sie in Ihre benutzerdefinierten Aktionen hinzufügen können 
    * Laden Sie die folgende Datei & platzieren Sie diese im gleichen Verzeichnis befindet wie die datamodel.json und CreationView.html 
      *   [Kaizala Forms JS-SDK ](https://manage.kaiza.la/MiniApps/downloadSDK). [Erfahren Sie mehr](KASClient/README.md)
 
 
 
 
*   **Schritt 5:** Verwenden Sie das Kaizala Forms JS-SDK Formular senden   
    * Hinzufügen den folgende Codeausschnitt in das <head> Bestandteil Ihrer "CreationView.html" verweisen auf die Kaizala Forms JS-SDK 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * Nun, wenn der Benutzer auf Absenden klickt, müssen wir stellen Sie sicher, dass er eine Frage, um Feedback auf – Fragen und erstellen Sie die Formularinstanz eingegeben hat  
    * Wir müssen auch das Formular beim Laden der Seite zu instanziieren. Fügen Sie den folgenden JavaScript-Codeausschnitt an Ihre "CreationView.html" innerhalb der <head> Element 
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

    *   Speichern Sie die Datei

*   **Schritt 6:** Erstellen Sie das Manifest der Aktion-Paket   
    *   Nun, da wir haben einen Semblance was wir erreichen möchten und erfolgreich erstellt eine Ansicht – es wird jetzt Erstellen der Paketmanifestdatei, bezieht sich auf diese Dateien. 
    * Paket-Manifestdatei enthält wichtige Informationen für die Plattform Kaizala dafür zu erkennen und die benutzerdefinierte Kaizala-Aktion ausführen. 
    * Erstellen Sie ein Paketmanifest und geben Sie Folgendes: 
        * Anzeigename für die Aktion Kaizala 
        * Benutzerdefinierte Id für die Aktion 
        * Zuordnen der Erstellung Ansicht zu unserer CreationView.html-Seite 

    * Vor dem Ausführen der benötigen wir ein Symbol für das Paket Aktion. Laden Sie die [Symboldatei](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & icon.png im selben Ordner wie die anderen Dateien speichern.

    * Erstellen Sie eine neue Datei mit dem Namen "package.json", und fügen Sie Sie der Datei folgenden Codeausschnitt. Stellen Sie sicher, dass Sie die Id, um Ihre Aktion eindeutige/unterschiedlichen Stellen bearbeiten 
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
    * Sie können die Karte, die angezeigt wird auf Kaizala Chat Zeichenbereich konfigurieren, durch die Zeichenfolgen im Paketmanifest angeben.  
    * Ändern Sie das Objekt "Ansichten" in Ihrem Paketmanifest entsprechend der unter Snippet:
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
    * Speichern Sie die Datei

*   **Schritt 7:** Erstellen Sie die Antwort-Ansicht   
    * Jetzt erstellen die Ansicht wir, die Kaizala Benutzer zu einer Instanz von unseren Aktion reagiert 
    * Erstellen einen neuen Datei Anruf ResponseView.html, und fügen Sie die unten Ausschnitt in der Datei 
    * Wir die folgenden Schritte aus. 
        * Radio Schaltfläche Auswahl für die Bewertung hinzufügen 
        * Vorbereiten einer Form Response-Objekt und den Code zum Senden des Formulars 
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

 
 
 
 
 
