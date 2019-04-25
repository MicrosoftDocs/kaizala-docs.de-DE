#   <a name="app-apis"></a>App-APIs:

| **API** | Beschreibung | Anforderungs Parameter | Antwort Ausgabe |
| :---: | :---: | :---: | :--- |
| **getUsersDetailsAsync** | Ruft Benutzer Details (Name, PIC, Telefonnummer usw.) gegen ihre IDs ab. | userIds-Array von Benutzer-IDs | *JSON der Benutzerinformationen* |
| **showContactPickerAsync** | Zeigt eine systemeigene Kontaktauswahl an und gibt ein Array mit allen Details der ausgewählten Benutzer zurück. | <ul><li>*Titel der Kontaktauswahl*</li><li>*selectedMutableUser* -Array ausgewählter userids</li><li>*selectedImmutableUser* -Array fester ausgewählter Benutzer-IDs</li><li>*isSingleSelection* -Einzelauswahl in der Kontaktauswahl</li></ul> | Array aller Details der ausgewählten Benutzer (*Array von JSON*) |
| **showImagePickerAsync** | Zeigt eine systemeigene Bildauswahl an und gibt den ausgewählten Bild Pfad zurück. | | *Ausgewählte Bildposition* |
| **showAttachmentPickerAsync** | Zeigt eine Anlagenauswahl in der systemeigenen Ebene an. | <ul><li>*supportedTypes* -Array unterstützter Anlagentypen für die Auswahl</li><li>zusätzliche Requisiten zum Konfigurieren der Auswahl</li></ul> | |
| **downloadAttachmentAsync** | Herunterladen der angegebenen Anlage | <ul><li>*Anlage mit einem gültigen Serverpfad zum herunterladen*</li><li>Rückruf beim Herunterladen des Downloads</li></ul> | |
| **cancelAttachmentDownloadAsync** | Abbrechen eines in der Warteschlange befindlichen Downloadvorgangs für eine Anlage | attachment | |
| **showPlacePickerAsync** | Zeigt eine systemeigene Ortsauswahl an und gibt die ausgewählte Stelle zurück (lt, LG, n) | Ausgewählter Speicherort | Breite/Länge |
| **showLocationOnMap** | Öffnet Native Maps mit vorgegebenem Speicherort | [KASLocation](KASLocation.md) -Typ | |
| **showDurationPickerAsync** | Zeigt eine systemeigene Dauer Auswahl mit Tag/Stunde/Minute an. | Standarddauer für die Auswahl | |
| **isTalkBackEnabledAsync** | Ruft ab, ob die Kommandofunktion aktiviert ist oder nicht | | Boolean |
| **generateUUIDAsync** | Ruft die neue UUID ab. | | Neu generierte UUID |
| **getCurrentDeviceLocationAsync** | Ruft den aktuellen Geräte Speicherort ab. | | |
| **getAppLocaleAsync** | Ruft die aktuelle App-Gebietsschema Sprache ab, in der die APP gerendert wird, nützlich für die Lokalisierung von Aktions Zeichenfolgen. | | Locale |
| **getConversationParticipantsCountAsync** | Ruft alle Teilnehmer-IDs der aktuellen Unterhaltung ab. | | Anzahl der Teilnehmer |
| **getConversationNameAsync** | Ruft den aktuellen Unterhaltungs Namen ab. | | Name der Unterhaltung |
| **dismissCurrentScreen** | Schließen des aktuellen Bildschirms (Erstellung, Antwort oder Zusammenfassung) | | |
| **showProgressBar** | Zeigt eine systemeigene vollständige Sreen-Statusanzeige mit dem angegebenen Text an. | Anzuzeigender Text | |
| **hideProgressBar** | Blendet die aktuelle Statusanzeige aus, falls vorhanden. | | |
| **getCurrentUserIdAsync** | Ruft die aktuelle Benutzer-ID ab, die die Aktion geöffnet hat. | | Benutzer-ID |
| **showImageImmersiveView** | Zeigt das Bild in der immersiven Ansicht | Array der Bild-URL | |
| **openAttachmentImmersiveView** | Anlage in immersiver Ansicht öffnen | Attachment-Objekt | |
| **hasStorageAccessForAttachmentType** | überprüft, ob die APP Lese-/Schreibzugriff auf den Speicher hat | Anlagentyp | |
| **generateBase64ThumbnailAsync** | Erstellt eine Base64-Miniaturansicht für ein Bild | localPath für die imageAttachment, deren Miniaturansicht generiert werden muss | |
| **getFontSizeMultiplierAsync** | Ruft den Schriftgrad Multiplikator für große Text-Current nur für iOS erforderlich ist. | | |
| **getLocalizedStringsAsync** | Ruft das Wörterbuch der lokalisierten Zeichenfolgen basierend auf dem aktuellen App-Gebietsschema ab. | Zeichenfolgen müssen innerhalb des Pakets mit Namen wie: strings_en. JSON, strings_hi. JSON, etc. bereitgestellt werden.    | Zeichenfolgen JSON |
| **logToReport** | Protokolliert einen Fehler für "Bericht senden". | Anlagentyp | |
| **isCurrentUserO365SubscribedAsync** | Überprüft, ob der aktuelle Benutzer ein O365-Abonnent ist | | Boolean |
| **registerHardwareBackPressCallback** | Registriert einen Rückruf, der auf Hardware-Schaltflächen drücken (für Android) ausgeführt werden soll | | |
| **initLocalizationStringsAsync** | Initialisiert die Zuordnung der Lokalisierungs Zeichenfolgen | Wörterbuch-die Zeichenfolgen Karte | Success (Boolean) gibt den Erfolg/Misserfolg der Initialisierung an |
| **getString** |   Gibt eine Zeichenfolge aus der lokalisierten Zeichenfolgen Datei zurück. |stringId ||


##  <a name="get-user-info"></a>Benutzerinformationen abrufen

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

##  <a name="show-contact-picker"></a>Kontaktauswahl anzeigen

```typescript
/**
  * Shows a native contact picker, and returns an array of all the selected users' details
  * @param {Callback} callback with below parameters:
  * * * * @param {KASUser[]} selectedUsers (array of user details) can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showContactPickerAsync(callback: function(users: KASUser[], error: string))
```

##  <a name="show-image-picker"></a>Bildauswahl anzeigen

```typescript
/**
  * Shows a native image picker, and returns the selected image path
  * @param {Callback} callback with below parameters:
  * * * * @param {string} selectedImagePath can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showImagePickerAsync(callback: function(selectedImagePath: string, error: string))
```

##  <a name="get-current-device-location"></a>Abrufen des aktuellen Gerätespeicher Orts

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a>Platzieren der Auswahl

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a>Standort auf Karten anzeigen

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a>Fehlermeldung anzeigen (Warnung oder Toast)

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a>Aktuelle Sprache abrufen, die von der APP verwendet wird

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a>Abrufen des Namens der aktuellen Unterhaltung

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a>Ausblenden des Bildschirms der aktuell geöffneten Aktion

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a>Systemeigene Statusanzeige anzeigen

```typescript
/**
  * Shows a native full sreen progress bar with the given text
  * @param {string} text
  */
  function showProgressBar(text: string)
```

##  <a name="hide-native-progress-bar"></a>Systemeigene Statusanzeige ausblenden

```typescript
/**
  * Hides the current progress bar, if any
  */
  function hideProgressBar()
```

##  <a name="get-current-user-id"></a>Aktuelle Benutzer-ID abrufen

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a>Register für Hardware-zurück-Tastendruck (Android)

```typescript
/**
  * Registers a callback to be executed on hardware back button press (for Android)
  * @param {Callback} callback to be executed
  */
  function registerHardwareBackPressCallback(callback: function())
```

##  <a name="localization-for-action"></a>Lokalisierung für Aktion

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

##  <a name="printf-for-action"></a>printf () für Aktion

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
