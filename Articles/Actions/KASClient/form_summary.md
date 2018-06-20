#   <a name="form-summary-flow-apis"></a><span data-ttu-id="5c237-101">Bilden Sie Zusammenfassung Fluss APIs:</span><span class="sxs-lookup"><span data-stu-id="5c237-101">Form summary flow APIs:</span></span>

| <span data-ttu-id="5c237-102">**API**</span><span class="sxs-lookup"><span data-stu-id="5c237-102">**API**</span></span> | <span data-ttu-id="5c237-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c237-103">Description</span></span> | <span data-ttu-id="5c237-104">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="5c237-104">Request Parameter</span></span> | <span data-ttu-id="5c237-105">Antwort-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5c237-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="5c237-106">**shouldSeeFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-106">**shouldSeeFormSummaryAsync**</span></span> | <span data-ttu-id="5c237-107">Ruft ab, ob das Formular Zusammenfassung für den aktuellen Benutzer sichtbar ist</span><span class="sxs-lookup"><span data-stu-id="5c237-107">Gets whether the form summary is visible to the current user</span></span> |  | <span data-ttu-id="5c237-108">*ShouldSeeSummary ((boolesch))* - True, wenn der aktuelle Benutzer berechtigt ist, finden in Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5c237-108">*shouldSeeSummary (boolean)* - true if current user is allowed to see summary</span></span> |
| <span data-ttu-id="5c237-109">**getFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-109">**getFormSummaryAsync**</span></span> | <span data-ttu-id="5c237-110">Ruft alle Benutzer und verarbeiteten Zusammenfassung von alle Antworten, die dem Formular zugeordneten Antworten</span><span class="sxs-lookup"><span data-stu-id="5c237-110">Gets responses by all the users, and processed summary from all the responses associated with the form</span></span> | <span data-ttu-id="5c237-111">Flaches Formular Zusammenfassung Rückruf umfasst und verarbeitet Formular Zusammenfassung Rückruf</span><span class="sxs-lookup"><span data-stu-id="5c237-111">Involves flat form summary callback and processed form summary callback</span></span> | <span data-ttu-id="5c237-112">Zusammenfassung-Objekte</span><span class="sxs-lookup"><span data-stu-id="5c237-112">Summary objects</span></span> |
| <span data-ttu-id="5c237-113">**getFlatFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-113">**getFlatFormSummaryAsync**</span></span> | <span data-ttu-id="5c237-114">Ruft die flache Antworten von allen Benutzern, die dem Formular (es wird empfohlen, getFormSummary() anstelle von dies verwenden) zugeordneten</span><span class="sxs-lookup"><span data-stu-id="5c237-114">Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)</span></span> | | <span data-ttu-id="5c237-115">*FlatSummary* – Zusammenfassung-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c237-115">*flatSummary* – summary object</span></span> |
| <span data-ttu-id="5c237-116">**getProcessedFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-116">**getProcessedFormSummaryAsync**</span></span> | <span data-ttu-id="5c237-117">Ruft verarbeitet Übersicht über alle dem Formular (es wird empfohlen, getFormSummary() anstelle von dies verwenden) zugeordneten Antworten</span><span class="sxs-lookup"><span data-stu-id="5c237-117">Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)</span></span> | | <span data-ttu-id="5c237-118">*ProcessedSummary* – Zusammenfassung-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c237-118">*processedSummary* – summary object</span></span> |
| <span data-ttu-id="5c237-119">**getAggregatedFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-119">**getAggregatedFormSummaryAsync**</span></span> | <span data-ttu-id="5c237-120">Ruft zusammenfassende aus allen Antworten, die dem Formular zugeordneten zusammengefasster</span><span class="sxs-lookup"><span data-stu-id="5c237-120">Gets aggregated summary from all the responses associated with the form</span></span> | | <span data-ttu-id="5c237-121">*AggregatedSummary* – Zusammenfassung-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c237-121">*aggregatedSummary* – summary object</span></span> |
| <span data-ttu-id="5c237-122">**getFormURLAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-122">**getFormURLAsync**</span></span> | <span data-ttu-id="5c237-123">Ruft die Url der Datei vom Server, die mit dem Formular zugeordnete flache Antworten enthält</span><span class="sxs-lookup"><span data-stu-id="5c237-123">Gets the file url from server containing flat responses associated with the form</span></span> | | <span data-ttu-id="5c237-124">Url</span><span class="sxs-lookup"><span data-stu-id="5c237-124">Url</span></span> |
| <span data-ttu-id="5c237-125">**shareFormURL**</span><span class="sxs-lookup"><span data-stu-id="5c237-125">**shareFormURL**</span></span> | <span data-ttu-id="5c237-126">Startet systemeigene Bildschirmfreigabe für die Formular-url</span><span class="sxs-lookup"><span data-stu-id="5c237-126">Launches native share screen for the form url</span></span> | <span data-ttu-id="5c237-127">URL, die gemeinsam genutzt werden</span><span class="sxs-lookup"><span data-stu-id="5c237-127">Url to be shared</span></span> | |
| <span data-ttu-id="5c237-128">**getFormReactionAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-128">**getFormReactionAsync**</span></span> | <span data-ttu-id="5c237-129">Dient zum Abrufen der konsolidierten Reaktion der dem Formular zugeordneten Unterhaltung Karte ("gefällt mir" und Kommentare)</span><span class="sxs-lookup"><span data-stu-id="5c237-129">Gets the consolidated reaction (likes and comments) of the conversation card associated with the form</span></span> | | <span data-ttu-id="5c237-130">Reaktion-Objekt</span><span class="sxs-lookup"><span data-stu-id="5c237-130">Reaction object</span></span> |
| <span data-ttu-id="5c237-131">**showAllReactions**</span><span class="sxs-lookup"><span data-stu-id="5c237-131">**showAllReactions**</span></span> | <span data-ttu-id="5c237-132">Zeigt alle den Reaktion Bildschirm ("gefällt mir" und Kommentare) für das Formular</span><span class="sxs-lookup"><span data-stu-id="5c237-132">Shows all the reaction screen (likes and comments) against the form</span></span> | | |
| <span data-ttu-id="5c237-133">**likeForm**</span><span class="sxs-lookup"><span data-stu-id="5c237-133">**likeForm**</span></span> | <span data-ttu-id="5c237-134">Anfragen eines Formulars, die Anzahl der like Anzahl hinzuzufügende können sinken, wenn der aktuelle Benutzer das Formular bereits gefallen hat</span><span class="sxs-lookup"><span data-stu-id="5c237-134">Requests to add a like count to a form, the count may decrease if the current user has already liked the form</span></span> | | |
| <span data-ttu-id="5c237-135">**addCommentOnForm**</span><span class="sxs-lookup"><span data-stu-id="5c237-135">**addCommentOnForm**</span></span> | <span data-ttu-id="5c237-136">Anforderungen an einen Kommentar zu einem Formular hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5c237-136">Requests to add a comment to a form</span></span> | | |
| <span data-ttu-id="5c237-137">**respondToForm**</span><span class="sxs-lookup"><span data-stu-id="5c237-137">**respondToForm**</span></span> | <span data-ttu-id="5c237-138">Anforderungen an eine Antwort zu einem Formular hinzufügen, indem Sie Antwort Bildschirm starten</span><span class="sxs-lookup"><span data-stu-id="5c237-138">Requests to add a response to a form, by launching response screen</span></span> | | |
| <span data-ttu-id="5c237-139">**sendRemindersToRespond**</span><span class="sxs-lookup"><span data-stu-id="5c237-139">**sendRemindersToRespond**</span></span> | <span data-ttu-id="5c237-140">Sendet eine Erinnerung (eine neue Unterhaltung Karte) gegen die vorhandene Karte</span><span class="sxs-lookup"><span data-stu-id="5c237-140">Sends a reminder (a new conversation card) against the existing card</span></span> | | |
| <span data-ttu-id="5c237-141">**copyFormAndForward**</span><span class="sxs-lookup"><span data-stu-id="5c237-141">**copyFormAndForward**</span></span> | <span data-ttu-id="5c237-142">Startet die Unterhaltung Auswahl um eine Kopie des Formulars als eine neue Unterhaltung Karte weiterzuleiten</span><span class="sxs-lookup"><span data-stu-id="5c237-142">Launches the conversation picker to forward a copy of the existing form as a new conversation card</span></span> | | |
| <span data-ttu-id="5c237-143">**updateFormPropertiesAsync**</span><span class="sxs-lookup"><span data-stu-id="5c237-143">**updateFormPropertiesAsync**</span></span> | <span data-ttu-id="5c237-144">Buchen Sie eine Anforderung zum Aktualisieren der dem Formular zugeordneten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c237-144">Post a request to update the properties associated with the form</span></span> |  <ul><li><span data-ttu-id="5c237-145">*PropertyUpdates* – ein Array mit allen Update Ereignisinfos hinzu, die erforderlich sind, ausgeführt werden – *Array von KASFormPropertyUpdateInfo*</span><span class="sxs-lookup"><span data-stu-id="5c237-145">*propertyUpdates* - an array of all update infos that are needed to be performed – *array of KASFormPropertyUpdateInfo*</span></span></li><li><span data-ttu-id="5c237-146">*NotifyUsers* - Pushbenachrichtigungen senden an diese Benutzer-Ids zu diesem Update – *Array von Zeichenfolgen*</span><span class="sxs-lookup"><span data-stu-id="5c237-146">*notifyUsers* - send push notifications to these user ids regarding this update – *array of strings*</span></span></li><li><span data-ttu-id="5c237-147">*NotificationMessage* - Push Notification wird die *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="5c237-147">*notificationMessage* - push notification message *string*</span></span></li></ul> | <span data-ttu-id="5c237-148">*Success(Boolean)* - gibt den Erfolg/Fehler des Updates</span><span class="sxs-lookup"><span data-stu-id="5c237-148">*Success(Boolean)* - denotes the success/failure of the update</span></span>|

##   <a name="get-the-summary-associated-with-the-form"></a><span data-ttu-id="5c237-149">Hier finden Sie die dem Formular zugeordnete Übersicht</span><span class="sxs-lookup"><span data-stu-id="5c237-149">Get the summary associated with the Form</span></span>

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

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a><span data-ttu-id="5c237-150">Hier finden Sie dem Formular zugeordnete flache-Übersicht (alle Antworten)</span><span class="sxs-lookup"><span data-stu-id="5c237-150">Get the flat summary (all responses) associated with the Form</span></span>

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a><span data-ttu-id="5c237-151">Hier finden Sie dem Formular zugeordnete verarbeitete-Übersicht (aggregierten Antworten)</span><span class="sxs-lookup"><span data-stu-id="5c237-151">Get the processed summary (aggregated responses) associated with the Form</span></span>

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a><span data-ttu-id="5c237-152">(Vom Server) abgerufen Sie, und erhalten Sie die Ergebnis-Url (alle Antworten), die dem Formular zugeordneten</span><span class="sxs-lookup"><span data-stu-id="5c237-152">Fetch (from server) and get the result url (all responses) associated with the Form</span></span>

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a><span data-ttu-id="5c237-153">Freigeben Sie das Ergebnis, das vom Server Url abgerufen</span><span class="sxs-lookup"><span data-stu-id="5c237-153">Share the result url fetched from server</span></span>

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a><span data-ttu-id="5c237-154">Abrufen Sie alle dem Formular zugeordneten Reaktionen</span><span class="sxs-lookup"><span data-stu-id="5c237-154">Get all the reactions associated with the Form</span></span>

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a><span data-ttu-id="5c237-155">Zeigen Sie alle dem Formular zugeordneten Reaktionen an</span><span class="sxs-lookup"><span data-stu-id="5c237-155">Show all the reactions associated with the Form</span></span>

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a><span data-ttu-id="5c237-156">Platzieren auf dem Formular ein ähnliches (die Karte zugeordneten Unterhaltung aktivieren)</span><span class="sxs-lookup"><span data-stu-id="5c237-156">Put a like on the Form (in turn the associated conversation card)</span></span>

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a><span data-ttu-id="5c237-157">Antwort-Ansicht für das Formular anzeigen</span><span class="sxs-lookup"><span data-stu-id="5c237-157">Show response view for the Form</span></span>

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a><span data-ttu-id="5c237-158">Erinnern Sie andere Personen zu reagieren</span><span class="sxs-lookup"><span data-stu-id="5c237-158">Remind other people to respond</span></span>

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a><span data-ttu-id="5c237-159">Weiterleiten Sie ein neues Formular, das von der zugehörigen dupliziert</span><span class="sxs-lookup"><span data-stu-id="5c237-159">Forward a new Form duplicated from the associated one</span></span>

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a><span data-ttu-id="5c237-160">Schließen Sie das Formular (in Turn Antworten darauf)</span><span class="sxs-lookup"><span data-stu-id="5c237-160">Close the Form (in turn responses to it)</span></span>

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
