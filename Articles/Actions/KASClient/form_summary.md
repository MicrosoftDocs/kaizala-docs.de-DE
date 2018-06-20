#   <a name="form-summary-flow-apis"></a>Bilden Sie Zusammenfassung Fluss APIs:

| **API** | Beschreibung | Anforderungsparameter | Antwort-Ausgabe |
| :---: | :---: | :---: | :--- |
| **shouldSeeFormSummaryAsync** | Ruft ab, ob das Formular Zusammenfassung für den aktuellen Benutzer sichtbar ist |  | *ShouldSeeSummary ((boolesch))* - True, wenn der aktuelle Benutzer berechtigt ist, finden in Zusammenfassung |
| **getFormSummaryAsync** | Ruft alle Benutzer und verarbeiteten Zusammenfassung von alle Antworten, die dem Formular zugeordneten Antworten | Flaches Formular Zusammenfassung Rückruf umfasst und verarbeitet Formular Zusammenfassung Rückruf | Zusammenfassung-Objekte |
| **getFlatFormSummaryAsync** | Ruft die flache Antworten von allen Benutzern, die dem Formular (es wird empfohlen, getFormSummary() anstelle von dies verwenden) zugeordneten | | *FlatSummary* – Zusammenfassung-Objekt |
| **getProcessedFormSummaryAsync** | Ruft verarbeitet Übersicht über alle dem Formular (es wird empfohlen, getFormSummary() anstelle von dies verwenden) zugeordneten Antworten | | *ProcessedSummary* – Zusammenfassung-Objekt |
| **getAggregatedFormSummaryAsync** | Ruft zusammenfassende aus allen Antworten, die dem Formular zugeordneten zusammengefasster | | *AggregatedSummary* – Zusammenfassung-Objekt |
| **getFormURLAsync** | Ruft die Url der Datei vom Server, die mit dem Formular zugeordnete flache Antworten enthält | | Url |
| **shareFormURL** | Startet systemeigene Bildschirmfreigabe für die Formular-url | URL, die gemeinsam genutzt werden | |
| **getFormReactionAsync** | Dient zum Abrufen der konsolidierten Reaktion der dem Formular zugeordneten Unterhaltung Karte ("gefällt mir" und Kommentare) | | Reaktion-Objekt |
| **showAllReactions** | Zeigt alle den Reaktion Bildschirm ("gefällt mir" und Kommentare) für das Formular | | |
| **likeForm** | Anfragen eines Formulars, die Anzahl der like Anzahl hinzuzufügende können sinken, wenn der aktuelle Benutzer das Formular bereits gefallen hat | | |
| **addCommentOnForm** | Anforderungen an einen Kommentar zu einem Formular hinzufügen | | |
| **respondToForm** | Anforderungen an eine Antwort zu einem Formular hinzufügen, indem Sie Antwort Bildschirm starten | | |
| **sendRemindersToRespond** | Sendet eine Erinnerung (eine neue Unterhaltung Karte) gegen die vorhandene Karte | | |
| **copyFormAndForward** | Startet die Unterhaltung Auswahl um eine Kopie des Formulars als eine neue Unterhaltung Karte weiterzuleiten | | |
| **updateFormPropertiesAsync** | Buchen Sie eine Anforderung zum Aktualisieren der dem Formular zugeordneten Eigenschaften |  <ul><li>*PropertyUpdates* – ein Array mit allen Update Ereignisinfos hinzu, die erforderlich sind, ausgeführt werden – *Array von KASFormPropertyUpdateInfo*</li><li>*NotifyUsers* - Pushbenachrichtigungen senden an diese Benutzer-Ids zu diesem Update – *Array von Zeichenfolgen*</li><li>*NotificationMessage* - Push Notification wird die *Zeichenfolge*</li></ul> | *Success(Boolean)* - gibt den Erfolg/Fehler des Updates|

##   <a name="get-the-summary-associated-with-the-form"></a>Hier finden Sie die dem Formular zugeordnete Übersicht

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

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a>Hier finden Sie dem Formular zugeordnete flache-Übersicht (alle Antworten)

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a>Hier finden Sie dem Formular zugeordnete verarbeitete-Übersicht (aggregierten Antworten)

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a>(Vom Server) abgerufen Sie, und erhalten Sie die Ergebnis-Url (alle Antworten), die dem Formular zugeordneten

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a>Freigeben Sie das Ergebnis, das vom Server Url abgerufen

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a>Abrufen Sie alle dem Formular zugeordneten Reaktionen

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a>Zeigen Sie alle dem Formular zugeordneten Reaktionen an

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a>Platzieren auf dem Formular ein ähnliches (die Karte zugeordneten Unterhaltung aktivieren)

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a>Antwort-Ansicht für das Formular anzeigen

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a>Erinnern Sie andere Personen zu reagieren

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a>Weiterleiten Sie ein neues Formular, das von der zugehörigen dupliziert

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a>Schließen Sie das Formular (in Turn Antworten darauf)

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
