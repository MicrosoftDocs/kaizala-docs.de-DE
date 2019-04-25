#   <a name="form-summary-flow-apis"></a>Fluss-APIs für formularzusammenfassung:

| **API** | Beschreibung | Anforderungs Parameter | Antwort Ausgabe |
| :---: | :---: | :---: | :--- |
| **shouldSeeFormSummaryAsync** | Ruft ab, ob die formularzusammenfassung für den aktuellen Benutzer sichtbar ist. |  | *shouldSeeSummary (Boolean)* -true, wenn der aktuelle Benutzer eine Zusammenfassung anzeigen darf |
| **getFormSummaryAsync** | Ruft Antworten aller Benutzer ab und verarbeitet eine Zusammenfassung aller Antworten, die dem Formular zugeordnet sind. | Beinhaltet einen zusammenfassenden Rückruf und einen zusammenfassenden Rückruf | Sammelobjekte |
| **getFlatFormSummaryAsync** | Ruft flache Antworten aller Benutzer ab, die dem Formular zugeordnet sind (es wird empfohlen, getFormSummary () anstelle davon zu verwenden). | | *flatSummary* – Summary-Objekt |
| **getProcessedFormSummaryAsync** | Ruft die verarbeitete Zusammenfassung aller Antworten ab, die dem Formular zugeordnet sind (es wird empfohlen, getFormSummary () anstelle davon zu verwenden). | | *processedSummary* – Summary-Objekt |
| **getAggregatedFormSummaryAsync** | Ruft aggregierte Zusammenfassung aller Antworten ab, die dem Formular zugeordnet sind. | | *aggregatedSummary* – Summary-Objekt |
| **getFormURLAsync** | Ruft die Datei-URL vom Server ab, die flache Antworten enthält, die dem Formular zugeordnet sind. | | Url |
| **shareFormURL** | Startet systemeigene Freigabe Bildschirm für die Formular-URL | Gemeinsame URL | |
| **getFormReactionAsync** | Ruft die konsolidierte Reaktion (likes und comments) der Unterhaltungs Karte ab, die dem Formular zugeordnet ist. | | Reaktions Objekt |
| **showAllReactions** | Zeigt den gesamten Reaktions Bildschirm (likes und comments) für das Formular an. | | |
| **likeForm** | Anforderungen zum Hinzufügen einer like-Anzahl zu einem Formular kann die Anzahl verringert werden, wenn der aktuelle Benutzer das Formular bereits gemocht hat. | | |
| **addCommentOnForm** | Anforderungen zum Hinzufügen eines Kommentars zu einem Formular | | |
| **respondToForm** | Anforderungen zum Hinzufügen einer Antwort zu einem Formular durch Starten des Antwort Bildschirms | | |
| **sendRemindersToRespond** | Sendet eine Erinnerung (eine neue Unterhaltungs Karte) an die vorhandene Karte | | |
| **copyFormAndForward** | Startet die Unterhaltungs Auswahl, um eine Kopie des vorhandenen Formulars als neue Unterhaltungs Karte weiterzuleiten. | | |
| **updateFormPropertiesAsync** | Bereitstelleneiner Anforderung zum Aktualisieren der dem Formular zugeordneten Eigenschaften |  <ul><li>*propertyUpdates* – ein Array aller Aktualisierungsinformationen, die durchgeführt werden müssen – *Array von KASFormPropertyUpdateInfo*</li><li>*notifyUsers* -Senden von Push-Benachrichtigungen an diese Benutzer-IDs zu diesem Update – *Array von Zeichenfolgen*</li><li>*notificationMessage* -Push-Benachrichtigungs *Zeichenfolge*</li></ul> | *Success (Boolean)* – der Erfolg/Fehler des Updates|

##   <a name="get-the-summary-associated-with-the-form"></a>Abrufen der dem Formular zugeordneten Zusammenfassung

```typescript 
/**
  * Gets flat responses by all the users, and processed summary from all the responses associated
  * with the form. It requires two callbacks:
  * @param {Callback} mostUpdatedCallback to immediately get the most updated summary from local database. It has below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  * @param {Callback} notifyCallback to get notified with the latest summary fetched from server. It has below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  *
  * This is useful when the network is flaky/disconnected, so that summary can
  * immediately be shown with the present data we have, but with an option to refresh
  * it later on arrival of latest data from server! None of the callbacks are mandatory,
  * so if 1st is nil, this method can be used to always fetch summary from server, and
  * if 2nd is nil, this can be used to always fetch summary from local database!
  */
  function getFormSummaryAsync(mostUpdatedCallback: function(flatSummary: KASFormFlatSummary, processedSummary: KASFormProcessedSummary, error: string),
                   notifyCallback: function(flatSummary: KASFormFlatSummary, processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a>Abrufen der flachen Zusammenfassung (alle Antworten), die dem Formular zugeordnet sind

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a>Abrufen der verarbeiteten Zusammenfassung (aggregierte Antworten), die dem Formular zugeordnet sind

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a>FETCH (vom Server) und Abrufen der Ergebnis-URL (alle Antworten), die dem Formular zugeordnet sind

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a>Freigeben der vom Server abgerufenen Ergebnis-URL

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a>Alle dem Formular zugeordneten Reaktionen abrufen

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a>Alle dem Formular zugeordneten Reaktionen anzeigen

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a>Setzen Sie ein like auf dem Formular (im Gegenzug die zugehörige Unterhaltungs Karte)

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a>Anzeigen der Antwort Ansicht für das Formular

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a>Andere Personen daran erinnern, zu Antworten

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a>Weiterleiten eines neuen Formulars, das aus dem verknüpften Formular dupliziert wurde

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a>Das Formular geschlossen (im Gegenzug Antworten)

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
