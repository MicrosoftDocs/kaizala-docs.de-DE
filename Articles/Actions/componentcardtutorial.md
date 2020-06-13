# <a name="create-an-action-using-component-card-controls"></a>Erstellen einer Aktion mithilfe von Komponenten Karten-Steuerelementen 

## <a name="overview"></a>Übersicht
In diesem Artikel werden die verschiedenen Steuerelemente für Komponenten Karten behandelt, die in einer Aktion mithilfe des Component Card Frameworks verwendet werden können.

Im folgenden werden die unterstützten Steuerelemente
* Textfeld/numerischer Textrahmen
* Standort
* Anlagefeld
* Einzelnes Select-Kontrollkästchen
* Slider mit Textfeld
* Datumssteuerelement
* Zeitsteuerelement
* Text Bereich
* Dropdown


Wir werden die Dateiänderungen auflisten, die erforderlich sind, um das Steuerelement auf einer benutzerdefinierten Karte zu aktivieren. Sie müssen die folgenden Details in den entsprechenden Dateien wie unten angegeben hinzufügen.

## <a name="creation-view"></a>Erstellungsansicht
Im folgenden finden Sie den Codeausschnitt, der innerhalb einer Seite (zB:  \<div id='page_1'\> ... \</div\> ) in "CreationView.html" angezeigt werden soll.

* Textfeld **/numerisches Textfeld:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss). Für das numerische Textfeld bleibt der Codeausschnitt unverändert. Nur Änderung erforderlich ist, dass der Eingabetyp "Number" anstelle von "Text" sein sollte.

  `````
    <div class='section-div'>
    <div id='LABEL1' class='field-label'>
    </div>
    <input id='INPUT1' type='text' contenteditable='true' class='textbox-1'>
    </div>
  `````

* **Speicherort:** Dieses Steuerelement verfügt über eine Bezeichnungs-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet).

  `````
    <div class='section-div'>
    <div id='LABEL21' class='field-label'>
    </div>
    <img class='location-image' id='location'>
    <div style='padding: 8px 15pt 15pt; display: inline-flex;'>
    <div class='location-div1'>
    <label class='location-address' id='location_text'>
    </label>
    </div>
    <div class='location-div2'>
    <label id='refresh-location-text' onclick='refreshLocation();' class='refresh-location-text'>
    </label>
    </div>
    </div>
    </div>
  `````
  
* **Anlagefeld:** Dieses Steuerelement verfügt über eine Bezeichnungs-ID (zum auffordern des Benutzers hinsichtlich der Daten, für die das Steuerelement verwendet wird) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).
    
  ````` 
      <div class='section-div'>
      <div id='LABEL4' class='field-label'>
      </div>
      <div id='INPUT4' class='scroll-div' title='Attachments'>
      <div class='horizontal-div'>
      <div class='attachment-div'>
      <img class='section-img' onclick='addAttachment()'>
      </div>
      </div>
      </div>
      </div>
  `````
 
* **Einzelnes Select-Kontrollkästchen:** Dieses Steuerelement verfügt über eine Bezeichnungs-ID (zum auffordern des Benutzers hinsichtlich der Daten, für die das Steuerelement verwendet wird) und eine CheckBox-ID (um auf den Wert zu deuten, der eingefügt werden muss). Die ID sollte CheckBox vorangestellt sein (zB: "CheckBox1"). Die IDs der einzelnen Optionen sollten dem übergeordneten Kontrollkästchen zugeordnet werden. Dieses Steuerelement kann auch nicht als standardmäßig vorgenommen werden, die erste Option wird ausgewählt, wenn das Formular gerendert wird.

  `````
      <div class='section-div'>
      <div id='LABEL5' class='field-label'>
      </div>
      <div class='option-div' id='CHECKBOX1'>
      <div class='single-select-rounded'>
      <label id='CHECKBOX1_1' class='selected-label'>
      </label>
      </div>
      <div class='single-select-rounded'>
      <label id='CHECKBOX1_2' class='unselected-label'>
      </label>
      </div>
      <div class='single-select-rounded'>
      <label id='CHECKBOX1_3' class='unselected-label'>
      </label>
      </div>
      </div>
      </div>
  `````
  
* **Slider mit TextBox:** Dieses Steuerelement verfügt über eine Label-ID (um den Benutzer zu Fragen, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (zur direkten Eingabe eines numerischen Werts). Die Option kann nicht als standardmäßig vorgenommen werden, da der Schieberegler immer mit einem Standardwert initialisiert wird.

  `````
    <div class='section-div slider-with-textbox'>
    <div id='LABEL6' class='field-label'>
    </div>
    <input id='INPUT6' type='range' class='slider-bar'>
    <input class='slider-textbox' type='number'>
    </input>
    </div>
  `````

* **Datumssteuerelement:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).
    
    `````
        <div class='section-div'>
        <div id='LABEL7' class='field-label'>
        </div>
        <div id='INPUT7' onClick='event_click(this)' class='textbox-1 image_right_date' value=''>
        </div>
        <div style='width: 0px; height: 0px; overflow: hidden;'>
        <input type='date' onChange='change_date_format(this)' class='textbox-1'>
        </div>
        </div>
  `````


* **Zeitsteuerung:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).
    
  `````
      <div class='section-div'>
      <div id='LABEL8' class='field-label'>
      </div>
      <div id='INPUT8' onClick='event_click(this)' class='textbox-1 image_right_time' value=''>
      </div>
      <div style='width: 0px; height: 0px; overflow: hidden;'>
      <input type='time' onChange='change_time_format(this)' class='textbox-1'>
      </div>
      </div>
  `````
    
* **Text Bereich:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).

  `````
    <div class='section-div'>
    <div id='LABEL9' class='field-label'>
    </div>
    <textarea id='INPUT9' contenteditable='true' class='text-area'>
    </textarea>
    </div>
  `````
 
* **Dropdown:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss). Dieses Steuerelement kann nicht optional vorgenommen werden.

  `````
      <div class='section-div'>
      <div id='LABEL10' class='field-label'>
      </div>
      <table id='INPUT10' class='feedbackSlderTable' title='TapBasedSlider'>
      </table>
      <div class='progressbar-outer-div'>
      <div class='progressbar-inner-div'>
      </div>
      </div>
      </div>
  `````

## <a name="summary-view"></a>Zusammenfassungsansicht
Dies ist der Codeausschnitt, der in Container in "SummaryView.html" eingehen sollte. Das Suffix der Antwort in der ID ist die Frage Nummer in AppModel, der die Frage zugeordnet wurde (beginnend mit 1). Unten sehen Sie ein Beispiel für ein beliebiges Steuerelement. Die Anzahl der Antworten im AppModel sollte der Anzahl der Abschnitte in der SummaryView.html entsprechen.

  `````
      <div class='section-div-summary'>
      <div id='ANSWER_1' class='field-label-summary'>
      </div>
      <label class='answer-label'>
      </label>
      </div>
  ````` 
    
## <a name="appmodel-file"></a>AppModel-Datei
Dies ist der Codeausschnitt, der in "AppModel.jsONCONFIG" eingefügt werden soll, in dem das Datenmodell definiert ist: der Titel entspricht dem, was die Zusammenfassungsansicht entsprechend den tatsächlichen vom Benutzer eingegebenen Daten anzeigt.
Unten sehen Sie ein Beispiel für das TextBox-Steuerelement. Ein ähnliches Format muss auch für andere Steuerelemente befolgt werden. Beachten Sie, dass für Attachment der Typ "attachmentlist" und für Location der Typ "Location" sein sollte.
  ````` 
      {
      "title": "Name",
      "type": "Text"
      }
  `````

## <a name="configuration-file"></a>Konfigurationsdatei
    
Dies ist der Codeausschnitt, der in die Datei "Config.js" gehen sollte. In SUBMIT_IDS müssen Sie die Eingabe-ID des Steuerelements in derselben Reihenfolge ablegen, in der die Fragen im AppModel vorhanden sind. Falls Sie es optional machen möchten, fügen Sie es bitte im OPTIONAL_IDS Wörterbuch mit entsprechender Seitenzahl hinzu-Falls nichts in einer Seite optional ist, weisen Sie der entsprechenden Seite ein leeres Array zu (siehe Beispiel für page_2). Optionale Frage Bezeichnungen werden automatisch mit der Zeichenfolge "(optional)" angefügt, wenn das Formular gerendert wird. Unten sehen Sie ein Beispiel für das TextBox-Steuerelement. Für alle Steuerelemente wird ein ähnliches Format verwendet. Beachten Sie, dass für Bilder und Speicherort kein Eintrag in SUBMIT_IDS erforderlich ist.

  `````
    var SUBMIT_IDS = ['INPUT1'];
    var OPTIONAL_IDS = {
    "page_1": ["INPUT1"],
    "page_2": []
    };// in case you have a page 2 where all questions are mandatory
  `````

## <a name="localized-strings-file---strings_enjson"></a>Lokalisierte Zeichenfolgen Datei – strings_en.jsauf
Dies ist der Codeausschnitt, der in die Zeichenfolgen Datei, in der die Zeichenfolgendefiniert sind, gehen sollte. Für ein TextBox-Steuerelemente mit der ID As INPUT1 ist eine Bezeichnung zugeordnet, die den Benutzer dazu auffordert, die Frage zu beantworten. Anschließend gibt es einen optionalen Platzhalter, der als Ghost-Text im TextBox-Element angezeigt wird. Dies ist ein Beispiel für das TextBox-Steuerelement. Für alle Steuerelemente wird ein ähnliches Format verwendet.

  `````
    "LABEL1": "Please enter your name",
    "INPUT1_placeholder": "Tap to enter name"
  `````

