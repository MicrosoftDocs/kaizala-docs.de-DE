#   <a name="app-apis"></a><span data-ttu-id="66c7c-101">App-APIs:</span><span class="sxs-lookup"><span data-stu-id="66c7c-101">App APIs:</span></span>

| <span data-ttu-id="66c7c-102">**API**</span><span class="sxs-lookup"><span data-stu-id="66c7c-102">**API**</span></span> | <span data-ttu-id="66c7c-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66c7c-103">Description</span></span> | <span data-ttu-id="66c7c-104">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="66c7c-104">Request Parameter</span></span> | <span data-ttu-id="66c7c-105">Antwort-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="66c7c-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="66c7c-106">**getUsersDetailsAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-106">**getUsersDetailsAsync**</span></span> | <span data-ttu-id="66c7c-107">Ruft den Benutzer Details (Name, Pic, Telefonnummer usw.) vor deren ids</span><span class="sxs-lookup"><span data-stu-id="66c7c-107">Gets users' details (name, pic, phone number, etc.) against their ids</span></span> | <span data-ttu-id="66c7c-108">Benutzer-IDs Array von Benutzer-ids</span><span class="sxs-lookup"><span data-stu-id="66c7c-108">userIds array of user ids</span></span> | <span data-ttu-id="66c7c-109">*JSON von Benutzerinformationen*</span><span class="sxs-lookup"><span data-stu-id="66c7c-109">*JSON of user info*</span></span> |
| <span data-ttu-id="66c7c-110">**showContactPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-110">**showContactPickerAsync**</span></span> | <span data-ttu-id="66c7c-111">Zeigt eine systemeigene kontaktauswahlfunktion und gibt ein Array von Details für alle ausgewählten Benutzer</span><span class="sxs-lookup"><span data-stu-id="66c7c-111">Shows a native contact picker, and returns an array of all the selected users' detail</span></span> | <ul><li><span data-ttu-id="66c7c-112">*Titel des Kontakts Personenauswahl*</span><span class="sxs-lookup"><span data-stu-id="66c7c-112">*title of Contact Picker*</span></span></li><li><span data-ttu-id="66c7c-113">*SelectedMutableUser* - Array mit den ausgewählten Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="66c7c-113">*selectedMutableUser* - array of selected userIds</span></span></li><li><span data-ttu-id="66c7c-114">*SelectedImmutableUser* - Array mit fester ausgewählten Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="66c7c-114">*selectedImmutableUser* - array of fixed selected userIds</span></span></li><li><span data-ttu-id="66c7c-115">*IsSingleSelection* - Einfachauswahl in Kontakt Personenauswahl</span><span class="sxs-lookup"><span data-stu-id="66c7c-115">*isSingleSelection* - single selection in Contact Picker</span></span></li></ul> | <span data-ttu-id="66c7c-116">Array von alle ausgewählten Benutzer Details (*Array von JSON*)</span><span class="sxs-lookup"><span data-stu-id="66c7c-116">Array of all the selected users' details (*Array of JSON*)</span></span> |
| <span data-ttu-id="66c7c-117">**showImagePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-117">**showImagePickerAsync**</span></span> | <span data-ttu-id="66c7c-118">Zeigt eine systemeigene Bildauswahl und gibt den Pfad des ausgewählten Bildes</span><span class="sxs-lookup"><span data-stu-id="66c7c-118">Shows a native image picker, and returns the selected image path</span></span> | | <span data-ttu-id="66c7c-119">*Ausgewähltes Bildspeicherort*</span><span class="sxs-lookup"><span data-stu-id="66c7c-119">*Selected image location*</span></span> |
| <span data-ttu-id="66c7c-120">**showAttachmentPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-120">**showAttachmentPickerAsync**</span></span> | <span data-ttu-id="66c7c-121">Zeigt eine Anlage Personenauswahl in der systemeigenen Ebene</span><span class="sxs-lookup"><span data-stu-id="66c7c-121">Displays an attachment picker in the native layer</span></span> | <ul><li><span data-ttu-id="66c7c-122">*SupportedTypes* - Array von Anlagen in unterstützten Typen der Auswahl</span><span class="sxs-lookup"><span data-stu-id="66c7c-122">*supportedTypes* - array of supported attachment types for the picker</span></span></li><li><span data-ttu-id="66c7c-123">zusätzliche Eigenschaften zum Konfigurieren der Personenauswahl</span><span class="sxs-lookup"><span data-stu-id="66c7c-123">additional props to configure the picker</span></span></li></ul> | |
| <span data-ttu-id="66c7c-124">**downloadAttachmentAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-124">**downloadAttachmentAsync**</span></span> | <span data-ttu-id="66c7c-125">Laden Sie das angegebene Attachment-Objekt</span><span class="sxs-lookup"><span data-stu-id="66c7c-125">Download the attachment specified</span></span> | <ul><li><span data-ttu-id="66c7c-126">*Anlage mit einem gültigen Serverpfad zum Herunterladen*</span><span class="sxs-lookup"><span data-stu-id="66c7c-126">*attachment with a valid server path to download*</span></span></li><li><span data-ttu-id="66c7c-127">Rückruf Download nach Abschluss</span><span class="sxs-lookup"><span data-stu-id="66c7c-127">callback on download completion</span></span></li></ul> | |
| <span data-ttu-id="66c7c-128">**cancelAttachmentDownloadAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-128">**cancelAttachmentDownloadAsync**</span></span> | <span data-ttu-id="66c7c-129">Abbrechen eines Downloadvorgangs in der Warteschlange für eine Anlage</span><span class="sxs-lookup"><span data-stu-id="66c7c-129">Cancel a download operation queued for an attachment</span></span> | <span data-ttu-id="66c7c-130">Anlage</span><span class="sxs-lookup"><span data-stu-id="66c7c-130">attachment</span></span> | |
| <span data-ttu-id="66c7c-131">**showPlacePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-131">**showPlacePickerAsync**</span></span> | <span data-ttu-id="66c7c-132">Zeigt eine systemeigene Place Personenauswahl und gibt die ausgewählte Stelle (Lt, Lg, n)</span><span class="sxs-lookup"><span data-stu-id="66c7c-132">Shows a native place picker, and returns the selected place (lt, lg, n)</span></span> | <span data-ttu-id="66c7c-133">Ausgewählten Speicherort</span><span class="sxs-lookup"><span data-stu-id="66c7c-133">Selected location</span></span> | <span data-ttu-id="66c7c-134">Breitengrad/Längengrad</span><span class="sxs-lookup"><span data-stu-id="66c7c-134">Latitude/longitude</span></span> |
| <span data-ttu-id="66c7c-135">**showLocationOnMap**</span><span class="sxs-lookup"><span data-stu-id="66c7c-135">**showLocationOnMap**</span></span> | <span data-ttu-id="66c7c-136">Öffnet systemeigene Karten mit angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="66c7c-136">Opens up native maps with given location</span></span> | <span data-ttu-id="66c7c-137">[KASLocation](KASLocation.md) -Typ</span><span class="sxs-lookup"><span data-stu-id="66c7c-137">[KASLocation](KASLocation.md) type</span></span> | |
| <span data-ttu-id="66c7c-138">**showDurationPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-138">**showDurationPickerAsync**</span></span> | <span data-ttu-id="66c7c-139">Zeigt eine systemeigene Dauer Personenauswahl mit Tag, Stunde, minute</span><span class="sxs-lookup"><span data-stu-id="66c7c-139">Shows a native duration picker with day/hour/minute</span></span> | <span data-ttu-id="66c7c-140">Standardmäßig über die Dauer, für die Personenauswahl angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="66c7c-140">Default duration to be shown on picker</span></span> | |
| <span data-ttu-id="66c7c-141">**isTalkBackEnabledAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-141">**isTalkBackEnabledAsync**</span></span> | <span data-ttu-id="66c7c-142">Ruft ab, ob Talkback oder nicht aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="66c7c-142">Gets whether talkback is enabled or not</span></span> | | <span data-ttu-id="66c7c-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="66c7c-143">Boolean</span></span> |
| <span data-ttu-id="66c7c-144">**generateUUIDAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-144">**generateUUIDAsync**</span></span> | <span data-ttu-id="66c7c-145">Ruft die neue UUID</span><span class="sxs-lookup"><span data-stu-id="66c7c-145">Gets the new UUID</span></span> | | <span data-ttu-id="66c7c-146">Neu generierte uuid</span><span class="sxs-lookup"><span data-stu-id="66c7c-146">Newly generated uuid</span></span> |
| <span data-ttu-id="66c7c-147">**getCurrentDeviceLocationAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-147">**getCurrentDeviceLocationAsync**</span></span> | <span data-ttu-id="66c7c-148">Ruft den aktuellen Speicherort des Geräts</span><span class="sxs-lookup"><span data-stu-id="66c7c-148">Gets the current device location</span></span> | | |
| <span data-ttu-id="66c7c-149">**getAppLocaleAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-149">**getAppLocaleAsync**</span></span> | <span data-ttu-id="66c7c-150">Ruft das aktuelle Gebietsschema der app-Sprache, in der die app gerendert wird, hilfreich für die Lokalisierung von Zeichenfolgen der Aktivität,</span><span class="sxs-lookup"><span data-stu-id="66c7c-150">Gets the current app locale -language in which the app is rendered, useful for localizing Action's strings</span></span> | | <span data-ttu-id="66c7c-151">Locale</span><span class="sxs-lookup"><span data-stu-id="66c7c-151">Locale</span></span> |
| <span data-ttu-id="66c7c-152">**getConversationParticipantsCountAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-152">**getConversationParticipantsCountAsync**</span></span> | <span data-ttu-id="66c7c-153">Ruft alle Teilnehmer-Ids der aktuellen Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="66c7c-153">Gets all the participant-ids of the current conversation</span></span> | | <span data-ttu-id="66c7c-154">Anzahl der Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="66c7c-154">Count of participants</span></span> |
| <span data-ttu-id="66c7c-155">**getConversationNameAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-155">**getConversationNameAsync**</span></span> | <span data-ttu-id="66c7c-156">Ruft den Namen des aktuellen Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="66c7c-156">Gets the current conversation name</span></span> | | <span data-ttu-id="66c7c-157">Name der Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="66c7c-157">Name of the conversation</span></span> |
| <span data-ttu-id="66c7c-158">**dismissCurrentScreen**</span><span class="sxs-lookup"><span data-stu-id="66c7c-158">**dismissCurrentScreen**</span></span> | <span data-ttu-id="66c7c-159">Schließen Sie den aktuellen Bildschirm (Erstellung,-Antwort oder Zusammenfassung)</span><span class="sxs-lookup"><span data-stu-id="66c7c-159">Dismiss the current screen (Creation, Response, or Summary)</span></span> | | |
| <span data-ttu-id="66c7c-160">**showProgressBar**</span><span class="sxs-lookup"><span data-stu-id="66c7c-160">**showProgressBar**</span></span> | <span data-ttu-id="66c7c-161">Zeigt eine systemeigene vollständige Sreen Statusanzeige mit dem angegebenen text</span><span class="sxs-lookup"><span data-stu-id="66c7c-161">Shows a native full sreen progress bar with the given text</span></span> | <span data-ttu-id="66c7c-162">Anzuzeigender Text</span><span class="sxs-lookup"><span data-stu-id="66c7c-162">Text to display</span></span> | |
| <span data-ttu-id="66c7c-163">**hideProgressBar**</span><span class="sxs-lookup"><span data-stu-id="66c7c-163">**hideProgressBar**</span></span> | <span data-ttu-id="66c7c-164">Die aktuellen Statusanzeige ausgeblendet, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="66c7c-164">Hides the current progress bar, if any</span></span> | | |
| <span data-ttu-id="66c7c-165">**getCurrentUserIdAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-165">**getCurrentUserIdAsync**</span></span> | <span data-ttu-id="66c7c-166">Ruft die aktuellen Benutzer-Id, die die Aktion geöffnet.</span><span class="sxs-lookup"><span data-stu-id="66c7c-166">Gets the current user id who has opened the Action</span></span> | | <span data-ttu-id="66c7c-167">User ID</span><span class="sxs-lookup"><span data-stu-id="66c7c-167">User ID</span></span> |
| <span data-ttu-id="66c7c-168">**showImageImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="66c7c-168">**showImageImmersiveView**</span></span> | <span data-ttu-id="66c7c-169">Bild in fesselnden Ansicht zeigt</span><span class="sxs-lookup"><span data-stu-id="66c7c-169">Shows Image in Immersive view</span></span> | <span data-ttu-id="66c7c-170">Array von Bildern-url</span><span class="sxs-lookup"><span data-stu-id="66c7c-170">Array of images url</span></span> | |
| <span data-ttu-id="66c7c-171">**openAttachmentImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="66c7c-171">**openAttachmentImmersiveView**</span></span> | <span data-ttu-id="66c7c-172">Anlage in fesselnden Ansicht öffnen</span><span class="sxs-lookup"><span data-stu-id="66c7c-172">Open attachment in Immersive view</span></span> | <span data-ttu-id="66c7c-173">Attachment-Objekt</span><span class="sxs-lookup"><span data-stu-id="66c7c-173">Attachment object</span></span> | |
| <span data-ttu-id="66c7c-174">**hasStorageAccessForAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="66c7c-174">**hasStorageAccessForAttachmentType**</span></span> | <span data-ttu-id="66c7c-175">überprüft, ob die app Lese-Schreib-Zugriff auf den Speicher besitzt.</span><span class="sxs-lookup"><span data-stu-id="66c7c-175">checks whether app has read/write access to the storage</span></span> | <span data-ttu-id="66c7c-176">Anlagetyp</span><span class="sxs-lookup"><span data-stu-id="66c7c-176">Attachment type</span></span> | |
| <span data-ttu-id="66c7c-177">**generateBase64ThumbnailAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-177">**generateBase64ThumbnailAsync**</span></span> | <span data-ttu-id="66c7c-178">Generiert Base64-Miniaturansicht für ein Bild</span><span class="sxs-lookup"><span data-stu-id="66c7c-178">Generates Base64 thumbnail for an image</span></span> | <span data-ttu-id="66c7c-179">LocalPath für die ImageAttachment, deren Miniaturansicht generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="66c7c-179">localPath for the imageAttachment whose thumbnail needs to be generated</span></span> | |
| <span data-ttu-id="66c7c-180">**getFontSizeMultiplierAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-180">**getFontSizeMultiplierAsync**</span></span> | <span data-ttu-id="66c7c-181">Dient zum Abrufen des Schriftart Größe Multiplikator für große Text – aktuelle nur von iOS erforderlich</span><span class="sxs-lookup"><span data-stu-id="66c7c-181">Gets the font size multiplier for large text -   Current only required by iOS</span></span> | | |
| <span data-ttu-id="66c7c-182">**getLocalizedStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-182">**getLocalizedStringsAsync**</span></span> | <span data-ttu-id="66c7c-183">Ruft die lokalisierten Zeichenfolgen Wörterbuch basierend auf aktuellen Gebietsschema der app ab</span><span class="sxs-lookup"><span data-stu-id="66c7c-183">Gets the localized strings' dictionary based on current app locale</span></span> | <span data-ttu-id="66c7c-184">Zeichenfolgen müssen in das Paket mit dem Namen wie angegeben werden: strings_en.json, strings_hi.json usw..</span><span class="sxs-lookup"><span data-stu-id="66c7c-184">Strings must be provided inside the package with names like: strings_en.json, strings_hi.json, etc.</span></span>    | <span data-ttu-id="66c7c-185">Zeichenfolgen JSON</span><span class="sxs-lookup"><span data-stu-id="66c7c-185">Strings JSON</span></span> |
| <span data-ttu-id="66c7c-186">**logToReport**</span><span class="sxs-lookup"><span data-stu-id="66c7c-186">**logToReport**</span></span> | <span data-ttu-id="66c7c-187">Meldet einen Fehler für "Senden Bericht"</span><span class="sxs-lookup"><span data-stu-id="66c7c-187">Logs an error for "Send report"</span></span> | <span data-ttu-id="66c7c-188">Anlagetyp</span><span class="sxs-lookup"><span data-stu-id="66c7c-188">Attachment type</span></span> | |
| <span data-ttu-id="66c7c-189">**isCurrentUserO365SubscribedAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-189">**isCurrentUserO365SubscribedAsync**</span></span> | <span data-ttu-id="66c7c-190">Überprüft, ob der aktuelle Benutzer ein O365-Abonnenten</span><span class="sxs-lookup"><span data-stu-id="66c7c-190">Checks if the current user an O365 subscriber</span></span> | | <span data-ttu-id="66c7c-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="66c7c-191">Boolean</span></span> |
| <span data-ttu-id="66c7c-192">**registerHardwareBackPressCallback**</span><span class="sxs-lookup"><span data-stu-id="66c7c-192">**registerHardwareBackPressCallback**</span></span> | <span data-ttu-id="66c7c-193">Registriert einen Rückruf in Hardware drücken Sie die zurück-Schaltfläche (für Android) ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="66c7c-193">Registers a callback to be executed on hardware back button press (for Android)</span></span> | | |
| <span data-ttu-id="66c7c-194">**initLocalizationStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="66c7c-194">**initLocalizationStringsAsync**</span></span> | <span data-ttu-id="66c7c-195">Initialisiert Map der Lokalisierung Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="66c7c-195">Initializes the localization strings' map</span></span> | <span data-ttu-id="66c7c-196">Dictionary - Zuordnung der Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="66c7c-196">Dictionary  - the strings' map</span></span> | <span data-ttu-id="66c7c-197">Success(Boolean) steht für den Erfolg/Fehlschlag der Initialisierung</span><span class="sxs-lookup"><span data-stu-id="66c7c-197">Success(Boolean) denotes the success/failure of the initialization</span></span> |
| <span data-ttu-id="66c7c-198">**getString**</span><span class="sxs-lookup"><span data-stu-id="66c7c-198">**getString**</span></span> |   <span data-ttu-id="66c7c-199">Gibt eine Zeichenfolge zurück, aus der lokalisierten Zeichenfolgen-Datei</span><span class="sxs-lookup"><span data-stu-id="66c7c-199">Returns a string from the localized strings' file</span></span> |<span data-ttu-id="66c7c-200">stringId</span><span class="sxs-lookup"><span data-stu-id="66c7c-200">stringId</span></span> ||


##  <a name="get-user-info"></a><span data-ttu-id="66c7c-201">Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="66c7c-201">Get user info</span></span>

```typescript
/**
  * Gets users' details (name, pic, phone number, etc.) against their ids
  * @param {string[]} userIds array of user ids
  * @param {Callback} callback with below parameters:
  * * * * @param {Dictionary<UserId: string, UserInfo: KASUser>} userIdToInfoMap (users' details against their ids) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getUsersDetailsAsync(userIds: string[], callback: function(userIdToInfoMap: {}, error: string))
```

##  <a name="show-contact-picker"></a><span data-ttu-id="66c7c-202">Anzeigen der kontaktauswahlfunktion</span><span class="sxs-lookup"><span data-stu-id="66c7c-202">Show contact picker</span></span>

```typescript
/**
  * Shows a native contact picker, and returns an array of all the selected users' details
  * @param {Callback} callback with below parameters:
  * * * * @param {KASUser[]} selectedUsers (array of user details) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showContactPickerAsync(callback: function(users: KASUser[], error: string))
```

##  <a name="show-image-picker"></a><span data-ttu-id="66c7c-203">Bildauswahl anzeigen</span><span class="sxs-lookup"><span data-stu-id="66c7c-203">Show image picker</span></span>

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a><span data-ttu-id="66c7c-204">Pfad für aktuellen abrufen</span><span class="sxs-lookup"><span data-stu-id="66c7c-204">Get current device location</span></span>

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a><span data-ttu-id="66c7c-205">Ort Personenauswahl</span><span class="sxs-lookup"><span data-stu-id="66c7c-205">Place picker</span></span>

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a><span data-ttu-id="66c7c-206">Speicherort auf Karten anzeigen</span><span class="sxs-lookup"><span data-stu-id="66c7c-206">Show location on maps</span></span>

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a><span data-ttu-id="66c7c-207">Anzeigen der Fehlermeldung (Warnung oder Toast)</span><span class="sxs-lookup"><span data-stu-id="66c7c-207">Show error message (alert or toast)</span></span>

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a><span data-ttu-id="66c7c-208">Abrufen der aktuellen Sprache wird von der app</span><span class="sxs-lookup"><span data-stu-id="66c7c-208">Get current language used by the app</span></span>

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a><span data-ttu-id="66c7c-209">Ruft den Namen der aktuellen Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="66c7c-209">Get the name of the current conversation</span></span>

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a><span data-ttu-id="66c7c-210">Schließen Sie die aktuell geöffneten Aktion Bildschirm</span><span class="sxs-lookup"><span data-stu-id="66c7c-210">Dismiss the currently opened Action's screen</span></span>

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a><span data-ttu-id="66c7c-211">Systemeigene Statusanzeige einblenden</span><span class="sxs-lookup"><span data-stu-id="66c7c-211">Show native progress bar</span></span>

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a><span data-ttu-id="66c7c-212">Systemeigene Statusanzeige ausblenden</span><span class="sxs-lookup"><span data-stu-id="66c7c-212">Hide native progress bar</span></span>

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a><span data-ttu-id="66c7c-213">Abrufen der aktuellen Benutzer-id</span><span class="sxs-lookup"><span data-stu-id="66c7c-213">Get current user id</span></span>

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a><span data-ttu-id="66c7c-214">Registrieren Sie sich für die Hardware zurück-Schaltfläche drücken (Android)</span><span class="sxs-lookup"><span data-stu-id="66c7c-214">Register for hardware back button press (Android)</span></span>

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a><span data-ttu-id="66c7c-215">Lokalisierung für Aktion</span><span class="sxs-lookup"><span data-stu-id="66c7c-215">Localization for Action</span></span>

```typescript
/**
  * Gets the localized strings' dictionary based on current app locale.
  * Strings must be provided inside the package with names like: strings_en.json, strings_hi.json, etc.
  * @param {Callback} callback with below parameters:
  * * * * @param {JSON} strings can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getLocalizedStringsAsync(callback: (strings: JSON, error: string))
```

##  <a name="printf-for-action"></a><span data-ttu-id="66c7c-216">printf() für Aktion</span><span class="sxs-lookup"><span data-stu-id="66c7c-216">printf() for Action</span></span>

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
