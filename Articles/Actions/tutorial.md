# <a name="practice-tutorial-creating-a-new-kaizala-action"></a>Übungs Lernprogramm: Erstellen einer neuen Kaizala-Aktion 

## <a name="overview"></a>Übersicht 
In diesem Lernprogramm erstellen wir eine benutzerdefinierte Kaizala-Aktion unter Verwendung des erweiterbaren Aktions Frameworks, das von der Kaizala-Plattform bereitgestellt wird.

Wir erstellen eine "Ask Feedback"-Aktion, die es Kaizala-Benutzern ermöglicht, Feedback von anderen Benutzern im Hinblick auf die 1-zu-5-Sterne-Bewertungen zu Fragen zu stellen – zusammen mit allen Kommentaren, die Sie bereitstellen möchten.  

Sie können Beispiel-Kaizala-Aktionspakete von [hier](https://manage.kaiza.la/MiniApps/DownloadSDK)herunterladen.

## <a name="pre-requisites"></a>Voraussetzungen 
* Ein Smartphone (Android/iOS) mit installierter Kaizala-App 
* Ein Office365-Konto 
* Zugriff auf einen HTML/JS-Editor (Notepad/Visual Studio Code/etc.) 

## <a name="steps-to-create-a-sample-action"></a>Schritte zum Erstellen einer Beispielaktion

*   **Schritt 1:** Erstellen eines neuen Verzeichnisses für Ihr Aktionspaket  
    * Erstellen eines neuen Verzeichnisses auf dem Desktop & Name "Sample-Funktion" 
    * Platzieren Sie alle nachfolgenden Dateien in diesem Verzeichnis.

*   **Schritt 2:** Definieren eines Datenmodells für Ihre Aktion 
    * Zunächst müssen wir das Datenmodell definieren, das in der benutzerdefinierten Aktion verwendet wird. 
    * Die Kaizala-Aktionen sind derzeit formularbasierte Datenmodelle. Daher müssen wir zunächst die "Fragen" definieren, die in unserem Formular eingeschlossen werden müssen. 
    * Da es sich um eine "Ask Feedback"-Aktion handelt, planen wir die Verwendung von zwei Daten teilen. 
        * Numerische Bewertung (Wert 1 bis 5) 
        * Kommentar/Verbatim-Feedback, falls vorhanden  

    *   Die Kaizala-formularinfrastruktur unterstützt folgende Fragetypen:

        | Fragetyp | Beschreibung |
        | :---: | :---: | 
        | SingleSelect | Einzelne Auswahlfrage mit Optionen |
        | MultiSelect | Multiple Choice-Frage mit Optionen | 
        | Text | Frage mit nur-Text-Antwort |
        | Numeric | Frage mit einer numerischen Antwort | 
        | Ort | Frage mit Standort Antwort | 
        | DateTime | Frage mit DateTime-Antwort | 
        | Image | Frage mit einem Bild als Antwort | 
    

    * Für unsere beiden Fragen verwenden wir den Fragetyp "numerischer" & ' Text ' für die Bewertung der &-Kommentare. 
        * Erstellen Sie eine neue Datei mit dem Namen "appModel. JSON", und platzieren Sie den folgenden Inhalt in der Datei. Die Datei enthält die beiden in der Reihenfolge aufgeführten Fragen. 
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
        * Hinweis: der obige Code enthält auch zusätzliche Metadaten, die wir später erfahren werden (außerhalb des Bereichs für diese Sitzung). 
        * Speichern der Datei
        
*   **Schritt 3:** Definieren einer Ansicht zum Erstellen der Anforderung für Feedback  
    *   Jetzt erstellen wir eine neue HTML-Datei, die zum Erstellen neuer Instanzen der Kaizala-Aktion verwendet wird. 
    *   Dies ist die Ansicht, die aufgerufen wird, wenn das Symbol von der Palette aus getappt wird. In dieser Ansicht möchten wir Sie Fragen, was Sie Feedback zu wünschen. 
    * Erstellen Sie eine neue Datei mit dem Namen "CreationView. html", und platzieren Sie den folgenden HTML-Code in der Datei. 
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
    *   Speichern der Datei 
*   **Schritt 4:** Schließen Sie das Kaizala Forms JS SDK ein. 
    * Um Entwicklern die Nutzung der Formularinfrastruktur zu erleichtern, stellt Kaizala eine JavaScript-Wrapperbibliothek bereit, die Sie in Ihre benutzerdefinierten Aktionen aufnehmen können. 
    * Laden Sie die Datei unten & in demselben Verzeichnis wie Ihre Datenmodell. JSON und CreationView. html 
      *   [Kaizala Forms js SDK ](https://manage.kaiza.la/MiniApps/downloadSDK). [Weitere Informationen](KASClient/README.md)
 
 
 
 
*   **Schritt 5:** Verwenden des Kaizala Forms JS-SDK zum Senden eines Formulars   
    * Fügen Sie den folgenden Codeausschnitt im <head> Element des "CreationView. html" hinzu, um auf das KAIZALA Forms js SDK zu verweisen. 
        `````
        <head> 
            <script type="text/javascript" src="KASClient.js"></script> 
        </head> 
        `````
    * Wenn der Benutzer jetzt auf Senden klickt, müssen wir überprüfen, ob er eine Frage eingegeben hat, um Feedback zu stellen – und die Formularinstanz erstellen.  
    * Außerdem müssen wir das Formular beim Laden der Seite instanziieren. Fügen Sie den folgenden JavaScript-Codeausschnitt zu Ihrem "CreationView. HTML <head> " innerhalb des-Elements hinzu. 
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

    *   Speichern der Datei

*   **Schritt 6:** Erstellen des Aktionspaket Manifests   
    *   Nun, da wir einen Anschein dessen haben, was wir erreichen und erfolgreich eine Ansicht erstellen möchten, wird nun die Paket Manifestdatei erstellt, die auf diese Dateien verweist. 
    * Die Paket Manifestdatei enthält wichtige Informationen für die Kaizala-Plattform, damit Sie Ihre benutzerdefinierte Kaizala-Aktion erkennen und ausführen kann. 
    * Wir erstellen ein Paketmanifest und geben Folgendes an: 
        * Anzeigename für Ihre Kaizala-Aktion 
        * Benutzerdefinierte ID für die Aktion 
        * Zuordnung der Erstellungsansicht zu unserer CreationView. HTML-Seite 

    * Zuvor benötigen wir ein Symbol für das Aktionspaket. Laden Sie die [Symboldatei](https://github.com/Microsoft/kaizala-docs-preview/blob/master/kaizala/platform/v1/docs/actions/icon.png) & speichern Sie Sie als Icon. png im gleichen Ordner wie die anderen Dateien.

    * Erstellen Sie eine neue Datei mit dem Namen "Package. JSON", und fügen Sie der Datei den folgenden Codeausschnitt hinzu. Stellen Sie sicher, dass Sie die ID bearbeiten, damit Ihre Aktion eindeutig ist. 
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
    * Sie können die Karte konfigurieren, die auf Kaizala Chat Canvas angezeigt wird, indem Sie die Zeichenfolgen im Paketmanifest angeben.  
    * Ändern Sie das Objekt "Views" in Ihrem Paketmanifest so, dass es mit dem folgenden Codeausschnitt übereinstimmt:
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
    * Speichern der Datei

*   **Schritt 7:** Erstellen der Antwort Ansicht   
    * Jetzt erstellen wir die Ansicht, die angezeigt wird, wenn Benutzer auf eine Instanz unserer Aktion reagieren Kaizala 
    * Erstellen Sie einen neuen Datei Aufruf ResponseView. html, und fügen Sie den folgenden Codeausschnitt in die Datei ein. 
    * Wir gehen wie folgt vor: 
        * Hinzufügen einer Optionsfeldauswahl für die Bewertung 
        * Vorbereiten eines Formular Antwortobjekts und des Codes zum Senden des Formulars 
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
           "Views": {              "CreationView": {                  "labelHeader": "Feedback angefordert",                  "SourceLocation": "CreationView. html"                        },              "ChatCanvasCardView": {                 " labelResponded ":" Sie haben Feedback zur Verfügung gestellt                  . "," labelRespondToForm ":" Feedback                  senden "," isResponseEditable              ":              true}," ResponseView  ": {" labelHeader ":" Feedback senden ",                 " SourceLocation ":" ResponseView. html "              },              " ResponseResultsView ": {  " labelPageHeader ":" Feedback Zusammenfassung ",                 " SourceLocation ":" SummaryView. html "              }     }        `````
 
 
*   **Schritt 9:** Erstellen des Kaizala-Aktionspakets 
    * ZIP alle Dateien in einer einzigen ZIP-Datei 
    * Stellen Sie sicher, dass der ZIP kein anderes Verzeichnis enthält, aber die Dateien befinden sich im Stammverzeichnis des ZIP-Verzeichnisses.

*   **Schritt 10:** Melden Sie sich beim Kaizala-Verwaltungs Portal an.  
    * Öffnen Sie ein Browserfenster, und navigieren Sie zuhttps://manage.kaiza.la/ 
    * Klicken Sie in der oberen linken Ecke auf "Anmelden". 
    * Geben Sie Ihre Office365-Anmeldeinformationen ein, um sich beim Portal anzumelden. Erteilen Sie auf Anforderung Berechtigungen für das Verwaltungsportal, um auf Ihre Profilinformationen zuzugreifen (nur zum ersten Mal erforderlich). 
    * Tippen Sie auf "Telefonnummer hinzufügen" in der oberen rechten Ecke & überprüfen Sie Ihre Telefonnummer 

*   **Schritt 11:** Hochladen des Aktionspakets  
    * Navigieren Sie zu "Aktionen" mit dem linken navbar 
    * Klicken Sie in der Dropdownliste auf der rechten Seite auf "Aktion importieren" und dann auf Start. 
    * Klicken Sie auf Hochladen und wählen Sie die ZIP-Datei aus, die Sie erstellt haben. 
    * Klicken Sie auf Importieren
    * Nachdem das Paket erfolgreich importiert wurde, bestätigen Sie, dass Sie erneut nach Aktionen navigieren. Die Aktion sollte unter "mit dieser ID erstellt" aufgeführt sein.
    * Sie können diese Aktion testen, indem Sie [](test.md) die folgenden Schritte ausführen.

*   **Schritt 12:** Erstellen einer neuen Kaizala-Gruppe  
    * Navigieren Sie im Kaizala-Verwaltungsportal zu "Gruppen", indem Sie den linken navbar 
    * Tippen Sie auf "Gruppe erstellen". 
    * Name der Gruppe "Kaizala Actions testing" 
    * Sicherstellen, dass die Gruppe in der Kaizala-App angezeigt wird

*   **Schritt 13:** Veröffentlichen der Aktion in der Gruppe  
    * Navigieren Sie zu "Gruppen" mithilfe der linken navbar 
    * Tippen Sie auf den Gruppennamen, den Sie in Schritt 13 erstellt haben. 
    * Tippen Sie auf die Registerkarte "Aktionen" 
    * Wählen Sie die in Schritt 12 erstellte Aktion & klicken Sie auf Aktion hinzufügen. Die benutzerdefinierte Kaizala-Aktion sollte jetzt auf der Registerkarte Discover angezeigt werden.

*   **Schritt 14:** Benutzerdefinierte Kaizala-Aktion verwenden  
    * Fügen Sie die benutzerdefinierte Aktion zu Ihrer Palette hinzu, und verwenden Sie Sie in Ihrer Gruppe. 

 
 
 
 
 
