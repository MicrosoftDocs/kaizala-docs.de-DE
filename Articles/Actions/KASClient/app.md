#   <a name="app-apis"></a><span data-ttu-id="382f8-101">App-APIs:</span><span class="sxs-lookup"><span data-stu-id="382f8-101">App APIs:</span></span>

| <span data-ttu-id="382f8-102">**API**</span><span class="sxs-lookup"><span data-stu-id="382f8-102">**API**</span></span> | <span data-ttu-id="382f8-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="382f8-103">Description</span></span> | <span data-ttu-id="382f8-104">Anforderungs Parameter</span><span class="sxs-lookup"><span data-stu-id="382f8-104">Request Parameter</span></span> | <span data-ttu-id="382f8-105">Antwort Ausgabe</span><span class="sxs-lookup"><span data-stu-id="382f8-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="382f8-106">**getUsersDetailsAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-106">**getUsersDetailsAsync**</span></span> | <span data-ttu-id="382f8-107">Ruft Benutzer Details (Name, PIC, Telefonnummer usw.) gegen ihre IDs ab.</span><span class="sxs-lookup"><span data-stu-id="382f8-107">Gets users' details (name, pic, phone number, etc.) against their ids</span></span> | <span data-ttu-id="382f8-108">userIds-Array von Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="382f8-108">userIds array of user ids</span></span> | <span data-ttu-id="382f8-109">*JSON der Benutzerinformationen*</span><span class="sxs-lookup"><span data-stu-id="382f8-109">*JSON of user info*</span></span> |
| <span data-ttu-id="382f8-110">**showContactPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-110">**showContactPickerAsync**</span></span> | <span data-ttu-id="382f8-111">Zeigt eine systemeigene Kontaktauswahl an und gibt ein Array mit allen Details der ausgewählten Benutzer zurück.</span><span class="sxs-lookup"><span data-stu-id="382f8-111">Shows a native contact picker, and returns an array of all the selected users' detail</span></span> | <ul><li><span data-ttu-id="382f8-112">*Titel der Kontaktauswahl*</span><span class="sxs-lookup"><span data-stu-id="382f8-112">*title of Contact Picker*</span></span></li><li><span data-ttu-id="382f8-113">*selectedMutableUser* -Array ausgewählter userids</span><span class="sxs-lookup"><span data-stu-id="382f8-113">*selectedMutableUser* - array of selected userIds</span></span></li><li><span data-ttu-id="382f8-114">*selectedImmutableUser* -Array fester ausgewählter Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="382f8-114">*selectedImmutableUser* - array of fixed selected userIds</span></span></li><li><span data-ttu-id="382f8-115">*isSingleSelection* -Einzelauswahl in der Kontaktauswahl</span><span class="sxs-lookup"><span data-stu-id="382f8-115">*isSingleSelection* - single selection in Contact Picker</span></span></li></ul> | <span data-ttu-id="382f8-116">Array aller Details der ausgewählten Benutzer (*Array von JSON*)</span><span class="sxs-lookup"><span data-stu-id="382f8-116">Array of all the selected users' details (*Array of JSON*)</span></span> |
| <span data-ttu-id="382f8-117">**showImagePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-117">**showImagePickerAsync**</span></span> | <span data-ttu-id="382f8-118">Zeigt eine systemeigene Bildauswahl an und gibt den ausgewählten Bild Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="382f8-118">Shows a native image picker, and returns the selected image path</span></span> | | <span data-ttu-id="382f8-119">*Ausgewählte Bildposition*</span><span class="sxs-lookup"><span data-stu-id="382f8-119">*Selected image location*</span></span> |
| <span data-ttu-id="382f8-120">**showAttachmentPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-120">**showAttachmentPickerAsync**</span></span> | <span data-ttu-id="382f8-121">Zeigt eine Anlagenauswahl in der systemeigenen Ebene an.</span><span class="sxs-lookup"><span data-stu-id="382f8-121">Displays an attachment picker in the native layer</span></span> | <ul><li><span data-ttu-id="382f8-122">*supportedTypes* -Array unterstützter Anlagentypen für die Auswahl</span><span class="sxs-lookup"><span data-stu-id="382f8-122">*supportedTypes* - array of supported attachment types for the picker</span></span></li><li><span data-ttu-id="382f8-123">zusätzliche Requisiten zum Konfigurieren der Auswahl</span><span class="sxs-lookup"><span data-stu-id="382f8-123">additional props to configure the picker</span></span></li></ul> | |
| <span data-ttu-id="382f8-124">**downloadAttachmentAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-124">**downloadAttachmentAsync**</span></span> | <span data-ttu-id="382f8-125">Herunterladen der angegebenen Anlage</span><span class="sxs-lookup"><span data-stu-id="382f8-125">Download the attachment specified</span></span> | <ul><li><span data-ttu-id="382f8-126">*Anlage mit einem gültigen Serverpfad zum herunterladen*</span><span class="sxs-lookup"><span data-stu-id="382f8-126">*attachment with a valid server path to download*</span></span></li><li><span data-ttu-id="382f8-127">Rückruf beim Herunterladen des Downloads</span><span class="sxs-lookup"><span data-stu-id="382f8-127">callback on download completion</span></span></li></ul> | |
| <span data-ttu-id="382f8-128">**cancelAttachmentDownloadAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-128">**cancelAttachmentDownloadAsync**</span></span> | <span data-ttu-id="382f8-129">Abbrechen eines in der Warteschlange befindlichen Downloadvorgangs für eine Anlage</span><span class="sxs-lookup"><span data-stu-id="382f8-129">Cancel a download operation queued for an attachment</span></span> | <span data-ttu-id="382f8-130">attachment</span><span class="sxs-lookup"><span data-stu-id="382f8-130">attachment</span></span> | |
| <span data-ttu-id="382f8-131">**showPlacePickerAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-131">**showPlacePickerAsync**</span></span> | <span data-ttu-id="382f8-132">Zeigt eine systemeigene Ortsauswahl an und gibt die ausgewählte Stelle zurück (lt, LG, n)</span><span class="sxs-lookup"><span data-stu-id="382f8-132">Shows a native place picker, and returns the selected place (lt, lg, n)</span></span> | <span data-ttu-id="382f8-133">Ausgewählter Speicherort</span><span class="sxs-lookup"><span data-stu-id="382f8-133">Selected location</span></span> | <span data-ttu-id="382f8-134">Breite/Länge</span><span class="sxs-lookup"><span data-stu-id="382f8-134">Latitude/longitude</span></span> |
| <span data-ttu-id="382f8-135">**showLocationOnMap**</span><span class="sxs-lookup"><span data-stu-id="382f8-135">**showLocationOnMap**</span></span> | <span data-ttu-id="382f8-136">Öffnet Native Maps mit vorgegebenem Speicherort</span><span class="sxs-lookup"><span data-stu-id="382f8-136">Opens up native maps with given location</span></span> | <span data-ttu-id="382f8-137">[KASLocation](KASLocation.md) -Typ</span><span class="sxs-lookup"><span data-stu-id="382f8-137">[KASLocation](KASLocation.md) type</span></span> | |
| <span data-ttu-id="382f8-138">**showDurationPickerAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-138">**showDurationPickerAsync**</span></span> | <span data-ttu-id="382f8-139">Zeigt eine systemeigene Dauer Auswahl mit Tag/Stunde/Minute an.</span><span class="sxs-lookup"><span data-stu-id="382f8-139">Shows a native duration picker with day/hour/minute</span></span> | <span data-ttu-id="382f8-140">Standarddauer für die Auswahl</span><span class="sxs-lookup"><span data-stu-id="382f8-140">Default duration to be shown on picker</span></span> | |
| <span data-ttu-id="382f8-141">**isTalkBackEnabledAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-141">**isTalkBackEnabledAsync**</span></span> | <span data-ttu-id="382f8-142">Ruft ab, ob die Kommandofunktion aktiviert ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="382f8-142">Gets whether talkback is enabled or not</span></span> | | <span data-ttu-id="382f8-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="382f8-143">Boolean</span></span> |
| <span data-ttu-id="382f8-144">**generateUUIDAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-144">**generateUUIDAsync**</span></span> | <span data-ttu-id="382f8-145">Ruft die neue UUID ab.</span><span class="sxs-lookup"><span data-stu-id="382f8-145">Gets the new UUID</span></span> | | <span data-ttu-id="382f8-146">Neu generierte UUID</span><span class="sxs-lookup"><span data-stu-id="382f8-146">Newly generated uuid</span></span> |
| <span data-ttu-id="382f8-147">**getCurrentDeviceLocationAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-147">**getCurrentDeviceLocationAsync**</span></span> | <span data-ttu-id="382f8-148">Ruft den aktuellen Geräte Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="382f8-148">Gets the current device location</span></span> | | |
| <span data-ttu-id="382f8-149">**getAppLocaleAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-149">**getAppLocaleAsync**</span></span> | <span data-ttu-id="382f8-150">Ruft die aktuelle App-Gebietsschema Sprache ab, in der die APP gerendert wird, nützlich für die Lokalisierung von Aktions Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="382f8-150">Gets the current app locale -language in which the app is rendered, useful for localizing Action's strings</span></span> | | <span data-ttu-id="382f8-151">Locale</span><span class="sxs-lookup"><span data-stu-id="382f8-151">Locale</span></span> |
| <span data-ttu-id="382f8-152">**getConversationParticipantsCountAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-152">**getConversationParticipantsCountAsync**</span></span> | <span data-ttu-id="382f8-153">Ruft alle Teilnehmer-IDs der aktuellen Unterhaltung ab.</span><span class="sxs-lookup"><span data-stu-id="382f8-153">Gets all the participant-ids of the current conversation</span></span> | | <span data-ttu-id="382f8-154">Anzahl der Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="382f8-154">Count of participants</span></span> |
| <span data-ttu-id="382f8-155">**getConversationNameAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-155">**getConversationNameAsync**</span></span> | <span data-ttu-id="382f8-156">Ruft den aktuellen Unterhaltungs Namen ab.</span><span class="sxs-lookup"><span data-stu-id="382f8-156">Gets the current conversation name</span></span> | | <span data-ttu-id="382f8-157">Name der Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="382f8-157">Name of the conversation</span></span> |
| <span data-ttu-id="382f8-158">**dismissCurrentScreen**</span><span class="sxs-lookup"><span data-stu-id="382f8-158">**dismissCurrentScreen**</span></span> | <span data-ttu-id="382f8-159">Schließen des aktuellen Bildschirms (Erstellung, Antwort oder Zusammenfassung)</span><span class="sxs-lookup"><span data-stu-id="382f8-159">Dismiss the current screen (Creation, Response, or Summary)</span></span> | | |
| <span data-ttu-id="382f8-160">**showProgressBar**</span><span class="sxs-lookup"><span data-stu-id="382f8-160">**showProgressBar**</span></span> | <span data-ttu-id="382f8-161">Zeigt eine systemeigene vollständige Sreen-Statusanzeige mit dem angegebenen Text an.</span><span class="sxs-lookup"><span data-stu-id="382f8-161">Shows a native full sreen progress bar with the given text</span></span> | <span data-ttu-id="382f8-162">Anzuzeigender Text</span><span class="sxs-lookup"><span data-stu-id="382f8-162">Text to display</span></span> | |
| <span data-ttu-id="382f8-163">**hideProgressBar**</span><span class="sxs-lookup"><span data-stu-id="382f8-163">**hideProgressBar**</span></span> | <span data-ttu-id="382f8-164">Blendet die aktuelle Statusanzeige aus, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="382f8-164">Hides the current progress bar, if any</span></span> | | |
| <span data-ttu-id="382f8-165">**getCurrentUserIdAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-165">**getCurrentUserIdAsync**</span></span> | <span data-ttu-id="382f8-166">Ruft die aktuelle Benutzer-ID ab, die die Aktion geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="382f8-166">Gets the current user id who has opened the Action</span></span> | | <span data-ttu-id="382f8-167">Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="382f8-167">User ID</span></span> |
| <span data-ttu-id="382f8-168">**showImageImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="382f8-168">**showImageImmersiveView**</span></span> | <span data-ttu-id="382f8-169">Zeigt das Bild in der immersiven Ansicht</span><span class="sxs-lookup"><span data-stu-id="382f8-169">Shows Image in Immersive view</span></span> | <span data-ttu-id="382f8-170">Array der Bild-URL</span><span class="sxs-lookup"><span data-stu-id="382f8-170">Array of images url</span></span> | |
| <span data-ttu-id="382f8-171">**openAttachmentImmersiveView**</span><span class="sxs-lookup"><span data-stu-id="382f8-171">**openAttachmentImmersiveView**</span></span> | <span data-ttu-id="382f8-172">Anlage in immersiver Ansicht öffnen</span><span class="sxs-lookup"><span data-stu-id="382f8-172">Open attachment in Immersive view</span></span> | <span data-ttu-id="382f8-173">Attachment-Objekt</span><span class="sxs-lookup"><span data-stu-id="382f8-173">Attachment object</span></span> | |
| <span data-ttu-id="382f8-174">**hasStorageAccessForAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="382f8-174">**hasStorageAccessForAttachmentType**</span></span> | <span data-ttu-id="382f8-175">überprüft, ob die APP Lese-/Schreibzugriff auf den Speicher hat</span><span class="sxs-lookup"><span data-stu-id="382f8-175">checks whether app has read/write access to the storage</span></span> | <span data-ttu-id="382f8-176">Anlagentyp</span><span class="sxs-lookup"><span data-stu-id="382f8-176">Attachment type</span></span> | |
| <span data-ttu-id="382f8-177">**generateBase64ThumbnailAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-177">**generateBase64ThumbnailAsync**</span></span> | <span data-ttu-id="382f8-178">Erstellt eine Base64-Miniaturansicht für ein Bild</span><span class="sxs-lookup"><span data-stu-id="382f8-178">Generates Base64 thumbnail for an image</span></span> | <span data-ttu-id="382f8-179">localPath für die imageAttachment, deren Miniaturansicht generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="382f8-179">localPath for the imageAttachment whose thumbnail needs to be generated</span></span> | |
| <span data-ttu-id="382f8-180">**getFontSizeMultiplierAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-180">**getFontSizeMultiplierAsync**</span></span> | <span data-ttu-id="382f8-181">Ruft den Schriftgrad Multiplikator für große Text-Current nur für iOS erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="382f8-181">Gets the font size multiplier for large text -   Current only required by iOS</span></span> | | |
| <span data-ttu-id="382f8-182">**getLocalizedStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-182">**getLocalizedStringsAsync**</span></span> | <span data-ttu-id="382f8-183">Ruft das Wörterbuch der lokalisierten Zeichenfolgen basierend auf dem aktuellen App-Gebietsschema ab.</span><span class="sxs-lookup"><span data-stu-id="382f8-183">Gets the localized strings' dictionary based on current app locale</span></span> | <span data-ttu-id="382f8-184">Zeichenfolgen müssen innerhalb des Pakets mit Namen wie: strings_en. JSON, strings_hi. JSON, etc. bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="382f8-184">Strings must be provided inside the package with names like: strings_en.json, strings_hi.json, etc.</span></span>    | <span data-ttu-id="382f8-185">Zeichenfolgen JSON</span><span class="sxs-lookup"><span data-stu-id="382f8-185">Strings JSON</span></span> |
| <span data-ttu-id="382f8-186">**logToReport**</span><span class="sxs-lookup"><span data-stu-id="382f8-186">**logToReport**</span></span> | <span data-ttu-id="382f8-187">Protokolliert einen Fehler für "Bericht senden".</span><span class="sxs-lookup"><span data-stu-id="382f8-187">Logs an error for "Send report"</span></span> | <span data-ttu-id="382f8-188">Anlagentyp</span><span class="sxs-lookup"><span data-stu-id="382f8-188">Attachment type</span></span> | |
| <span data-ttu-id="382f8-189">**isCurrentUserO365SubscribedAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-189">**isCurrentUserO365SubscribedAsync**</span></span> | <span data-ttu-id="382f8-190">Überprüft, ob der aktuelle Benutzer ein O365-Abonnent ist</span><span class="sxs-lookup"><span data-stu-id="382f8-190">Checks if the current user an O365 subscriber</span></span> | | <span data-ttu-id="382f8-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="382f8-191">Boolean</span></span> |
| <span data-ttu-id="382f8-192">**registerHardwareBackPressCallback**</span><span class="sxs-lookup"><span data-stu-id="382f8-192">**registerHardwareBackPressCallback**</span></span> | <span data-ttu-id="382f8-193">Registriert einen Rückruf, der auf Hardware-Schaltflächen drücken (für Android) ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="382f8-193">Registers a callback to be executed on hardware back button press (for Android)</span></span> | | |
| <span data-ttu-id="382f8-194">**initLocalizationStringsAsync**</span><span class="sxs-lookup"><span data-stu-id="382f8-194">**initLocalizationStringsAsync**</span></span> | <span data-ttu-id="382f8-195">Initialisiert die Zuordnung der Lokalisierungs Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="382f8-195">Initializes the localization strings' map</span></span> | <span data-ttu-id="382f8-196">Wörterbuch-die Zeichenfolgen Karte</span><span class="sxs-lookup"><span data-stu-id="382f8-196">Dictionary  - the strings' map</span></span> | <span data-ttu-id="382f8-197">Success (Boolean) gibt den Erfolg/Misserfolg der Initialisierung an</span><span class="sxs-lookup"><span data-stu-id="382f8-197">Success(Boolean) denotes the success/failure of the initialization</span></span> |
| <span data-ttu-id="382f8-198">**getString**</span><span class="sxs-lookup"><span data-stu-id="382f8-198">**getString**</span></span> |   <span data-ttu-id="382f8-199">Gibt eine Zeichenfolge aus der lokalisierten Zeichenfolgen Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="382f8-199">Returns a string from the localized strings' file</span></span> |<span data-ttu-id="382f8-200">stringId</span><span class="sxs-lookup"><span data-stu-id="382f8-200">stringId</span></span> ||


##  <a name="get-user-info"></a><span data-ttu-id="382f8-201">Benutzerinformationen abrufen</span><span class="sxs-lookup"><span data-stu-id="382f8-201">Get user info</span></span>

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

##  <a name="show-contact-picker"></a><span data-ttu-id="382f8-202">Kontaktauswahl anzeigen</span><span class="sxs-lookup"><span data-stu-id="382f8-202">Show contact picker</span></span>

```typescript
/**
  * Shows a native contact picker, and returns an array of all the selected users' details
  * @param {Callback} callback with below parameters:
  * * * * @param {KASUser[]} selectedUsers (array of user details) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showContactPickerAsync(callback: function(users: KASUser[], error: string))
```

##  <a name="show-image-picker"></a><span data-ttu-id="382f8-203">Bildauswahl anzeigen</span><span class="sxs-lookup"><span data-stu-id="382f8-203">Show image picker</span></span>

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a><span data-ttu-id="382f8-204">Abrufen des aktuellen Gerätespeicher Orts</span><span class="sxs-lookup"><span data-stu-id="382f8-204">Get current device location</span></span>

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a><span data-ttu-id="382f8-205">Platzieren der Auswahl</span><span class="sxs-lookup"><span data-stu-id="382f8-205">Place picker</span></span>

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a><span data-ttu-id="382f8-206">Standort auf Karten anzeigen</span><span class="sxs-lookup"><span data-stu-id="382f8-206">Show location on maps</span></span>

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a><span data-ttu-id="382f8-207">Fehlermeldung anzeigen (Warnung oder Toast)</span><span class="sxs-lookup"><span data-stu-id="382f8-207">Show error message (alert or toast)</span></span>

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a><span data-ttu-id="382f8-208">Aktuelle Sprache abrufen, die von der APP verwendet wird</span><span class="sxs-lookup"><span data-stu-id="382f8-208">Get current language used by the app</span></span>

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a><span data-ttu-id="382f8-209">Abrufen des Namens der aktuellen Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="382f8-209">Get the name of the current conversation</span></span>

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a><span data-ttu-id="382f8-210">Ausblenden des Bildschirms der aktuell geöffneten Aktion</span><span class="sxs-lookup"><span data-stu-id="382f8-210">Dismiss the currently opened Action's screen</span></span>

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a><span data-ttu-id="382f8-211">Systemeigene Statusanzeige anzeigen</span><span class="sxs-lookup"><span data-stu-id="382f8-211">Show native progress bar</span></span>

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a><span data-ttu-id="382f8-212">Systemeigene Statusanzeige ausblenden</span><span class="sxs-lookup"><span data-stu-id="382f8-212">Hide native progress bar</span></span>

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a><span data-ttu-id="382f8-213">Aktuelle Benutzer-ID abrufen</span><span class="sxs-lookup"><span data-stu-id="382f8-213">Get current user id</span></span>

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a><span data-ttu-id="382f8-214">Register für Hardware-zurück-Tastendruck (Android)</span><span class="sxs-lookup"><span data-stu-id="382f8-214">Register for hardware back button press (Android)</span></span>

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a><span data-ttu-id="382f8-215">Lokalisierung für Aktion</span><span class="sxs-lookup"><span data-stu-id="382f8-215">Localization for Action</span></span>

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

##  <a name="printf-for-action"></a><span data-ttu-id="382f8-216">printf () für Aktion</span><span class="sxs-lookup"><span data-stu-id="382f8-216">printf() for Action</span></span>

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
