# <a name="create-an-action-using-component-card-controls"></a><span data-ttu-id="8ccc0-101">Erstellen einer Aktion mithilfe von Komponenten Karten-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8ccc0-101">Create an Action using Component Card Controls</span></span> 

## <a name="overview"></a><span data-ttu-id="8ccc0-102">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8ccc0-102">Overview</span></span>
<span data-ttu-id="8ccc0-103">In diesem Artikel werden die verschiedenen Steuerelemente für Komponenten Karten behandelt, die in einer Aktion mithilfe des Component Card Frameworks verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-103">In this article, we will cover the various component cards controls which can be used in an action using component card framework.</span></span>

<span data-ttu-id="8ccc0-104">Im folgenden werden die unterstützten Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8ccc0-104">The following are the controls supported</span></span>
* <span data-ttu-id="8ccc0-105">Textfeld/numerischer Textrahmen</span><span class="sxs-lookup"><span data-stu-id="8ccc0-105">Text Box / Numeric Text Box</span></span>
* <span data-ttu-id="8ccc0-106">Standort</span><span class="sxs-lookup"><span data-stu-id="8ccc0-106">Location</span></span>
* <span data-ttu-id="8ccc0-107">Anlagefeld</span><span class="sxs-lookup"><span data-stu-id="8ccc0-107">Attachment Box</span></span>
* <span data-ttu-id="8ccc0-108">Einzelnes Select-Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="8ccc0-108">Single Select Check-Box</span></span>
* <span data-ttu-id="8ccc0-109">Slider mit Textfeld</span><span class="sxs-lookup"><span data-stu-id="8ccc0-109">Slider with Text Box</span></span>
* <span data-ttu-id="8ccc0-110">Datumssteuerelement</span><span class="sxs-lookup"><span data-stu-id="8ccc0-110">Date Control</span></span>
* <span data-ttu-id="8ccc0-111">Zeitsteuerelement</span><span class="sxs-lookup"><span data-stu-id="8ccc0-111">Time Control</span></span>
* <span data-ttu-id="8ccc0-112">Text Bereich</span><span class="sxs-lookup"><span data-stu-id="8ccc0-112">Text Area</span></span>
* <span data-ttu-id="8ccc0-113">Dropdown</span><span class="sxs-lookup"><span data-stu-id="8ccc0-113">Dropdown</span></span>


<span data-ttu-id="8ccc0-114">Wir werden die Dateiänderungen auflisten, die erforderlich sind, um das Steuerelement auf einer benutzerdefinierten Karte zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-114">We will list down the file changes needed to enable the control in a custom card.</span></span> <span data-ttu-id="8ccc0-115">Sie müssen die folgenden Details in den entsprechenden Dateien wie unten angegeben hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-115">You will need to add the following details in the corresponding files as given below.</span></span>

## <a name="creation-view"></a><span data-ttu-id="8ccc0-116">Erstellungsansicht</span><span class="sxs-lookup"><span data-stu-id="8ccc0-116">Creation view</span></span>
<span data-ttu-id="8ccc0-117">Im folgenden finden Sie den Codeausschnitt, der innerhalb einer Seite (zB:  \<div id='page_1'\> ... \</div\> ) in "CreationView.html" angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-117">The following contains the code snippet that should go inside a page (eg: \<div id='page_1'\>...\</div\>) in "CreationView.html".</span></span>

* <span data-ttu-id="8ccc0-118">Textfeld **/numerisches Textfeld:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-118">**Text Box / Numeric Text Box:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span> <span data-ttu-id="8ccc0-119">Für das numerische Textfeld bleibt der Codeausschnitt unverändert.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-119">For the numeric text box, the code snippet remains the same.</span></span> <span data-ttu-id="8ccc0-120">Nur Änderung erforderlich ist, dass der Eingabetyp "Number" anstelle von "Text" sein sollte.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-120">Only change required is that the input type should be "number" instead of "text".</span></span>

  `````
    <div class='section-div'>
    <div id='LABEL1' class='field-label'>
    </div>
    <input id='INPUT1' type='text' contenteditable='true' class='textbox-1'>
    </div>
  `````

* <span data-ttu-id="8ccc0-121">**Speicherort:** Dieses Steuerelement verfügt über eine Bezeichnungs-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-121">**Location:** This control has a LABEL ID (to prompt the user as to what data the control is for).</span></span>

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
  
* <span data-ttu-id="8ccc0-122">**Anlagefeld:** Dieses Steuerelement verfügt über eine Bezeichnungs-ID (zum auffordern des Benutzers hinsichtlich der Daten, für die das Steuerelement verwendet wird) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-122">**Attachment Box:** This control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>
    
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
 
* <span data-ttu-id="8ccc0-123">**Einzelnes Select-Kontrollkästchen:** Dieses Steuerelement verfügt über eine Bezeichnungs-ID (zum auffordern des Benutzers hinsichtlich der Daten, für die das Steuerelement verwendet wird) und eine CheckBox-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-123">**Single select Check-Box:** This control has a LABEL ID (to prompt the user as to what data the control is for) and a CHECKBOX ID (to point to the value that needs to be inserted).</span></span> <span data-ttu-id="8ccc0-124">Die ID sollte CheckBox vorangestellt sein (zB: "CheckBox1").</span><span class="sxs-lookup"><span data-stu-id="8ccc0-124">The ID should be prefixed with CHECKBOX (eg: CHECKBOX1).</span></span> <span data-ttu-id="8ccc0-125">Die IDs der einzelnen Optionen sollten dem übergeordneten Kontrollkästchen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-125">The IDs of the individual options should be mapped to the parent checkbox.</span></span> <span data-ttu-id="8ccc0-126">Dieses Steuerelement kann auch nicht als standardmäßig vorgenommen werden, die erste Option wird ausgewählt, wenn das Formular gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-126">Also, this control cannot be made optional as by default, the first option will be selected when the form is rendered.</span></span>

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
  
* <span data-ttu-id="8ccc0-127">**Slider mit TextBox:** Dieses Steuerelement verfügt über eine Label-ID (um den Benutzer zu Fragen, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (zur direkten Eingabe eines numerischen Werts).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-127">**Slider with TextBox:** This control has a LABEL ID (to prompt the user as to what data the control is for) and a INPUT ID (to enter a numerical value directly).</span></span> <span data-ttu-id="8ccc0-128">Die Option kann nicht als standardmäßig vorgenommen werden, da der Schieberegler immer mit einem Standardwert initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-128">It cannot be made optional as by default as the slider will always be initialized with a default value.</span></span>

  `````
    <div class='section-div slider-with-textbox'>
    <div id='LABEL6' class='field-label'>
    </div>
    <input id='INPUT6' type='range' class='slider-bar'>
    <input class='slider-textbox' type='number'>
    </input>
    </div>
  `````

* <span data-ttu-id="8ccc0-129">**Datumssteuerelement:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-129">**Date Control:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>
    
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


* <span data-ttu-id="8ccc0-130">**Zeitsteuerung:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-130">**Time Control:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>
    
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
    
* <span data-ttu-id="8ccc0-131">**Text Bereich:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-131">**Text Area:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span>

  `````
    <div class='section-div'>
    <div id='LABEL9' class='field-label'>
    </div>
    <textarea id='INPUT9' contenteditable='true' class='text-area'>
    </textarea>
    </div>
  `````
 
* <span data-ttu-id="8ccc0-132">**Dropdown:** Jedes Steuerelement verfügt über eine Label-ID (zum auffordern des Benutzers, welche Daten das Steuerelement verwendet) und eine Eingabe-ID (um auf den Wert zu deuten, der eingefügt werden muss).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-132">**Dropdown:** Each control has a LABEL ID (to prompt the user as to what data the control is for) and an INPUT ID (to point to the value that needs to be inserted).</span></span> <span data-ttu-id="8ccc0-133">Dieses Steuerelement kann nicht optional vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-133">This control cannot be made optional.</span></span>

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

## <a name="summary-view"></a><span data-ttu-id="8ccc0-134">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="8ccc0-134">Summary View</span></span>
<span data-ttu-id="8ccc0-135">Dies ist der Codeausschnitt, der in Container in "SummaryView.html" eingehen sollte.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-135">This is the code snippet that should go inside container in "SummaryView.html".</span></span> <span data-ttu-id="8ccc0-136">Das Suffix der Antwort in der ID ist die Frage Nummer in AppModel, der die Frage zugeordnet wurde (beginnend mit 1).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-136">The suffix of ANSWER in the id is the question number in AppModel to which the question has been mapped (starting from 1).</span></span> <span data-ttu-id="8ccc0-137">Unten sehen Sie ein Beispiel für ein beliebiges Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-137">Below is a an example for any control.</span></span> <span data-ttu-id="8ccc0-138">Die Anzahl der Antworten im AppModel sollte der Anzahl der Abschnitte in der SummaryView.html entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-138">The number of answers in the AppModel should be equal to the number of sections in the "SummaryView.html".</span></span>

  `````
      <div class='section-div-summary'>
      <div id='ANSWER_1' class='field-label-summary'>
      </div>
      <label class='answer-label'>
      </label>
      </div>
  ````` 
    
## <a name="appmodel-file"></a><span data-ttu-id="8ccc0-139">AppModel-Datei</span><span class="sxs-lookup"><span data-stu-id="8ccc0-139">AppModel File</span></span>
<span data-ttu-id="8ccc0-140">Dies ist der Codeausschnitt, der in "AppModel.jsONCONFIG" eingefügt werden soll, in dem das Datenmodell definiert ist: der Titel entspricht dem, was die Zusammenfassungsansicht entsprechend den tatsächlichen vom Benutzer eingegebenen Daten anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-140">This is the code snippet that should go inside "AppModel.jsonConfig" where the data model is defined - the title will correspond to the what the Summary View will display corresponding to the actual data entered by the user.</span></span>
<span data-ttu-id="8ccc0-141">Unten sehen Sie ein Beispiel für das TextBox-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-141">Below is a an example for TextBox control.</span></span> <span data-ttu-id="8ccc0-142">Ein ähnliches Format muss auch für andere Steuerelemente befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-142">A similar format needs to be followed for other controls as well.</span></span> <span data-ttu-id="8ccc0-143">Beachten Sie, dass für Attachment der Typ "attachmentlist" und für Location der Typ "Location" sein sollte.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-143">Please note that for Attachment the type should be "AttachmentList" and for Location the type should be "Location".</span></span>
  ````` 
      {
      "title": "Name",
      "type": "Text"
      }
  `````

## <a name="configuration-file"></a><span data-ttu-id="8ccc0-144">Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="8ccc0-144">Configuration File</span></span>
    
<span data-ttu-id="8ccc0-145">Dies ist der Codeausschnitt, der in die Datei "Config.js" gehen sollte.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-145">This is the code snippet that should go inside "Config.js" file.</span></span> <span data-ttu-id="8ccc0-146">In SUBMIT_IDS müssen Sie die Eingabe-ID des Steuerelements in derselben Reihenfolge ablegen, in der die Fragen im AppModel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-146">In SUBMIT_IDS you need to put the INPUT ID of the control in the same sequence as the questions are present in the AppModel.</span></span> <span data-ttu-id="8ccc0-147">Falls Sie es optional machen möchten, fügen Sie es bitte im OPTIONAL_IDS Wörterbuch mit entsprechender Seitenzahl hinzu-Falls nichts in einer Seite optional ist, weisen Sie der entsprechenden Seite ein leeres Array zu (siehe Beispiel für page_2).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-147">In case you want to make it optional, please add it in the OPTIONAL_IDS dictionary with corresponding page number - in case nothing in a page is optional, assign an empty array to the corresponding page (as seen in the example for page_2).</span></span> <span data-ttu-id="8ccc0-148">Optionale Frage Bezeichnungen werden automatisch mit der Zeichenfolge "(optional)" angefügt, wenn das Formular gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-148">Optional question labels will automatically be appended with the string '(optional)' when the form is rendered.</span></span> <span data-ttu-id="8ccc0-149">Unten sehen Sie ein Beispiel für das TextBox-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-149">Below is a an example for TextBox control.</span></span> <span data-ttu-id="8ccc0-150">Für alle Steuerelemente wird ein ähnliches Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-150">All controls will have a similar format.</span></span> <span data-ttu-id="8ccc0-151">Beachten Sie, dass für Bilder und Speicherort kein Eintrag in SUBMIT_IDS erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-151">Please note that for Images and Location, we don't need an entry in SUBMIT_IDS.</span></span>

  `````
    var SUBMIT_IDS = ['INPUT1'];
    var OPTIONAL_IDS = {
    "page_1": ["INPUT1"],
    "page_2": []
    };// in case you have a page 2 where all questions are mandatory
  `````

## <a name="localized-strings-file---strings_enjson"></a><span data-ttu-id="8ccc0-152">Lokalisierte Zeichenfolgen Datei – strings_en.jsauf</span><span class="sxs-lookup"><span data-stu-id="8ccc0-152">Localized Strings File - strings_en.json</span></span>
<span data-ttu-id="8ccc0-153">Dies ist der Codeausschnitt, der in die Zeichenfolgen Datei, in der die Zeichenfolgendefiniert sind, gehen sollte.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-153">This is the code snippet that should go inside the strings file where the strings are defined.</span></span> <span data-ttu-id="8ccc0-154">Für ein TextBox-Steuerelemente mit der ID As INPUT1 ist eine Bezeichnung zugeordnet, die den Benutzer dazu auffordert, die Frage zu beantworten. Anschließend gibt es einen optionalen Platzhalter, der als Ghost-Text im TextBox-Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-154">For a textbox with ID as INPUT1 there is a label associated which prompts the user as to what the question is; then there is an optional placeholder which appears as a ghost-text inside the textbox.</span></span> <span data-ttu-id="8ccc0-155">Dies ist ein Beispiel für das TextBox-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-155">This is an example of Textbox control.</span></span> <span data-ttu-id="8ccc0-156">Für alle Steuerelemente wird ein ähnliches Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-156">All controls will have similar format.</span></span>

  `````
    "LABEL1": "Please enter your name",
    "INPUT1_placeholder": "Tap to enter name"
  `````

