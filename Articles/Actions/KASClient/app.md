#   <a name="app-apis"></a>App-APIs:

| **API** | Beschreibung | Anforderungsparameter | Antwort-Ausgabe |
| :---: | :---: | :---: | :--- |
| **getUsersDetailsAsync** | Ruft den Benutzer Details (Name, Pic, Telefonnummer usw.) vor deren ids | Benutzer-IDs Array von Benutzer-ids | *JSON von Benutzerinformationen* |
| **showContactPickerAsync** | Zeigt eine systemeigene kontaktauswahlfunktion und gibt ein Array von Details für alle ausgewählten Benutzer | <ul><li>*Titel des Kontakts Personenauswahl*</li><li>*SelectedMutableUser* - Array mit den ausgewählten Benutzer-IDs</li><li>*SelectedImmutableUser* - Array mit fester ausgewählten Benutzer-IDs</li><li>*IsSingleSelection* - Einfachauswahl in Kontakt Personenauswahl</li></ul> | Array von alle ausgewählten Benutzer Details (*Array von JSON*) |
| **showImagePickerAsync** | Zeigt eine systemeigene Bildauswahl und gibt den Pfad des ausgewählten Bildes | | *Ausgewähltes Bildspeicherort* |
| **showAttachmentPickerAsync** | Zeigt eine Anlage Personenauswahl in der systemeigenen Ebene | <ul><li>*SupportedTypes* - Array von Anlagen in unterstützten Typen der Auswahl</li><li>zusätzliche Eigenschaften zum Konfigurieren der Personenauswahl</li></ul> | |
| **downloadAttachmentAsync** | Laden Sie das angegebene Attachment-Objekt | <ul><li>*Anlage mit einem gültigen Serverpfad zum Herunterladen*</li><li>Rückruf Download nach Abschluss</li></ul> | |
| **cancelAttachmentDownloadAsync** | Abbrechen eines Downloadvorgangs in der Warteschlange für eine Anlage | Anlage | |
| **showPlacePickerAsync** | Zeigt eine systemeigene Place Personenauswahl und gibt die ausgewählte Stelle (Lt, Lg, n) | Ausgewählten Speicherort | Breitengrad/Längengrad |
| **showLocationOnMap** | Öffnet systemeigene Karten mit angegebenen Speicherort | [KASLocation](KASLocation.md) -Typ | |
| **showDurationPickerAsync** | Zeigt eine systemeigene Dauer Personenauswahl mit Tag, Stunde, minute | Standardmäßig über die Dauer, für die Personenauswahl angezeigt werden soll | |
| **isTalkBackEnabledAsync** | Ruft ab, ob Talkback oder nicht aktiviert ist | | Boolean |
| **generateUUIDAsync** | Ruft die neue UUID | | Neu generierte uuid |
| **getCurrentDeviceLocationAsync** | Ruft den aktuellen Speicherort des Geräts | | |
| **getAppLocaleAsync** | Ruft das aktuelle Gebietsschema der app-Sprache, in der die app gerendert wird, hilfreich für die Lokalisierung von Zeichenfolgen der Aktivität, | | Locale |
| **getConversationParticipantsCountAsync** | Ruft alle Teilnehmer-Ids der aktuellen Unterhaltung | | Anzahl der Teilnehmer |
| **getConversationNameAsync** | Ruft den Namen des aktuellen Unterhaltung | | Name der Unterhaltung |
| **dismissCurrentScreen** | Schließen Sie den aktuellen Bildschirm (Erstellung,-Antwort oder Zusammenfassung) | | |
| **showProgressBar** | Zeigt eine systemeigene vollständige Sreen Statusanzeige mit dem angegebenen text | Anzuzeigender Text | |
| **hideProgressBar** | Die aktuellen Statusanzeige ausgeblendet, sofern vorhanden | | |
| **getCurrentUserIdAsync** | Ruft die aktuellen Benutzer-Id, die die Aktion geöffnet. | | User ID |
| **showImageImmersiveView** | Bild in fesselnden Ansicht zeigt | Array von Bildern-url | |
| **openAttachmentImmersiveView** | Anlage in fesselnden Ansicht öffnen | Attachment-Objekt | |
| **hasStorageAccessForAttachmentType** | überprüft, ob die app Lese-Schreib-Zugriff auf den Speicher besitzt. | Anlagetyp | |
| **generateBase64ThumbnailAsync** | Generiert Base64-Miniaturansicht für ein Bild | LocalPath für die ImageAttachment, deren Miniaturansicht generiert werden muss | |
| **getFontSizeMultiplierAsync** | Dient zum Abrufen des Schriftart Größe Multiplikator für große Text – aktuelle nur von iOS erforderlich | | |
| **getLocalizedStringsAsync** | Ruft die lokalisierten Zeichenfolgen Wörterbuch basierend auf aktuellen Gebietsschema der app ab | Zeichenfolgen müssen in das Paket mit dem Namen wie angegeben werden: strings_en.json, strings_hi.json usw..    | Zeichenfolgen JSON |
| **logToReport** | Meldet einen Fehler für "Senden Bericht" | Anlagetyp | |
| **isCurrentUserO365SubscribedAsync** | Überprüft, ob der aktuelle Benutzer ein O365-Abonnenten | | Boolean |
| **registerHardwareBackPressCallback** | Registriert einen Rückruf in Hardware drücken Sie die zurück-Schaltfläche (für Android) ausgeführt werden | | |
| **initLocalizationStringsAsync** | Initialisiert Map der Lokalisierung Zeichenfolgen | Dictionary - Zuordnung der Zeichenfolgen | Success(Boolean) steht für den Erfolg/Fehlschlag der Initialisierung |
| **getString** |   Gibt eine Zeichenfolge zurück, aus der lokalisierten Zeichenfolgen-Datei |stringId ||


##  <a name="get-user-info"></a>Benutzerinformationen

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

##  <a name="show-contact-picker"></a>Anzeigen der kontaktauswahlfunktion

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

##  <a name="get-current-device-location"></a>Pfad für aktuellen abrufen

```typescript
/**
  * Gets the current device location
  * @param {Callback} callback with below parameters:
  * * * * @param {string} location can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentDeviceLocationAsync(callback: function(location: string, error: string))
```

##  <a name="place-picker"></a>Ort Personenauswahl

```typescript
/**
  * Shows a native place picker, and returns the selected place (lt, lg, n)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASLocation} selectedLocation can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function showPlacePickerAsync(callback: (selectedLocation: KASLocation, error: string))
```

##  <a name="show-location-on-maps"></a>Speicherort auf Karten anzeigen

```typescript
/**
  * Opens up native maps with a marker at selected location(KASLocation type)
  * @param {KASLocation} selectedLocation
  */
  function showLocationOnMap(selectedLocation: KASLocation)
```

##  <a name="show-error-message-alert-or-toast"></a>Anzeigen der Fehlermeldung (Warnung oder Toast)

```typescript
/**
  * Shows a native alert (for iOS) or a toast (for Android) with the message
  * @param {string} message
  */
  function showNativeErrorMessage(message: string)
```

##  <a name="get-current-language-used-by-the-app"></a>Abrufen der aktuellen Sprache wird von der app

```typescript
/**
  * Gets the current app locale, the language in which the app is rendered, useful for localizing MiniApp's strings
  * @param {Callback} callback with below parameters:
  * * * * @param {string} locale can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getAppLocaleAsync(callback: function(locale: string, error: string))
```

##  <a name="get-the-name-of-the-current-conversation"></a>Ruft den Namen der aktuellen Unterhaltung

```typescript
/**
  * Gets the current conversation name
  * @param {Callback} callback with below parameters:
  * * * * @param {string} name can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getConversationNameAsync(callback: function(name: string, error: string))
```

##  <a name="dismiss-the-currently-opened-actions-screen"></a>Schließen Sie die aktuell geöffneten Aktion Bildschirm

```typescript
/**
  * Dismiss the current screen (Creation, Response, or Summary)
  */
  function dismissCurrentScreen()
```

##  <a name="show-native-progress-bar"></a>Systemeigene Statusanzeige einblenden

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

##  <a name="get-current-user-id"></a>Abrufen der aktuellen Benutzer-id

```typescript
/**
  * Gets the current user id who has opened the MiniApp
  * @param {Callback} callback with below parameters:
  * * * * @param {string} userId can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getCurrentUserIdAsync(callback: function(userId: string, error: string))
```

##  <a name="register-for-hardware-back-button-press-android"></a>Registrieren Sie sich für die Hardware zurück-Schaltfläche drücken (Android)

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

##  <a name="printf-for-action"></a>printf() für Aktion

```typescript
/**
  * Returns a string.
  * @param {string} string denotes the formatted string. Specifier should be mentioned like {0},{1},{2}.....
  * @param {string[]} args array of arguments.
  */
  function printf(main: string, ...args: any[]): string
```
