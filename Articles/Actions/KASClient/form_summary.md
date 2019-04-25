#   <a name="form-summary-flow-apis"></a><span data-ttu-id="f6061-101">Fluss-APIs für formularzusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="f6061-101">Form summary flow APIs:</span></span>

| <span data-ttu-id="f6061-102">**API**</span><span class="sxs-lookup"><span data-stu-id="f6061-102">**API**</span></span> | <span data-ttu-id="f6061-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6061-103">Description</span></span> | <span data-ttu-id="f6061-104">Anforderungs Parameter</span><span class="sxs-lookup"><span data-stu-id="f6061-104">Request Parameter</span></span> | <span data-ttu-id="f6061-105">Antwort Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f6061-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="f6061-106">**shouldSeeFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-106">**shouldSeeFormSummaryAsync**</span></span> | <span data-ttu-id="f6061-107">Ruft ab, ob die formularzusammenfassung für den aktuellen Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="f6061-107">Gets whether the form summary is visible to the current user</span></span> |  | <span data-ttu-id="f6061-108">*shouldSeeSummary (Boolean)* -true, wenn der aktuelle Benutzer eine Zusammenfassung anzeigen darf</span><span class="sxs-lookup"><span data-stu-id="f6061-108">*shouldSeeSummary (boolean)* - true if current user is allowed to see summary</span></span> |
| <span data-ttu-id="f6061-109">**getFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-109">**getFormSummaryAsync**</span></span> | <span data-ttu-id="f6061-110">Ruft Antworten aller Benutzer ab und verarbeitet eine Zusammenfassung aller Antworten, die dem Formular zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f6061-110">Gets responses by all the users, and processed summary from all the responses associated with the form</span></span> | <span data-ttu-id="f6061-111">Beinhaltet einen zusammenfassenden Rückruf und einen zusammenfassenden Rückruf</span><span class="sxs-lookup"><span data-stu-id="f6061-111">Involves flat form summary callback and processed form summary callback</span></span> | <span data-ttu-id="f6061-112">Sammelobjekte</span><span class="sxs-lookup"><span data-stu-id="f6061-112">Summary objects</span></span> |
| <span data-ttu-id="f6061-113">**getFlatFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-113">**getFlatFormSummaryAsync**</span></span> | <span data-ttu-id="f6061-114">Ruft flache Antworten aller Benutzer ab, die dem Formular zugeordnet sind (es wird empfohlen, getFormSummary () anstelle davon zu verwenden).</span><span class="sxs-lookup"><span data-stu-id="f6061-114">Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)</span></span> | | <span data-ttu-id="f6061-115">*flatSummary* – Summary-Objekt</span><span class="sxs-lookup"><span data-stu-id="f6061-115">*flatSummary* – summary object</span></span> |
| <span data-ttu-id="f6061-116">**getProcessedFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-116">**getProcessedFormSummaryAsync**</span></span> | <span data-ttu-id="f6061-117">Ruft die verarbeitete Zusammenfassung aller Antworten ab, die dem Formular zugeordnet sind (es wird empfohlen, getFormSummary () anstelle davon zu verwenden).</span><span class="sxs-lookup"><span data-stu-id="f6061-117">Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)</span></span> | | <span data-ttu-id="f6061-118">*processedSummary* – Summary-Objekt</span><span class="sxs-lookup"><span data-stu-id="f6061-118">*processedSummary* – summary object</span></span> |
| <span data-ttu-id="f6061-119">**getAggregatedFormSummaryAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-119">**getAggregatedFormSummaryAsync**</span></span> | <span data-ttu-id="f6061-120">Ruft aggregierte Zusammenfassung aller Antworten ab, die dem Formular zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f6061-120">Gets aggregated summary from all the responses associated with the form</span></span> | | <span data-ttu-id="f6061-121">*aggregatedSummary* – Summary-Objekt</span><span class="sxs-lookup"><span data-stu-id="f6061-121">*aggregatedSummary* – summary object</span></span> |
| <span data-ttu-id="f6061-122">**getFormURLAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-122">**getFormURLAsync**</span></span> | <span data-ttu-id="f6061-123">Ruft die Datei-URL vom Server ab, die flache Antworten enthält, die dem Formular zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f6061-123">Gets the file url from server containing flat responses associated with the form</span></span> | | <span data-ttu-id="f6061-124">Url</span><span class="sxs-lookup"><span data-stu-id="f6061-124">Url</span></span> |
| <span data-ttu-id="f6061-125">**shareFormURL**</span><span class="sxs-lookup"><span data-stu-id="f6061-125">**shareFormURL**</span></span> | <span data-ttu-id="f6061-126">Startet systemeigene Freigabe Bildschirm für die Formular-URL</span><span class="sxs-lookup"><span data-stu-id="f6061-126">Launches native share screen for the form url</span></span> | <span data-ttu-id="f6061-127">Gemeinsame URL</span><span class="sxs-lookup"><span data-stu-id="f6061-127">Url to be shared</span></span> | |
| <span data-ttu-id="f6061-128">**getFormReactionAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-128">**getFormReactionAsync**</span></span> | <span data-ttu-id="f6061-129">Ruft die konsolidierte Reaktion (likes und comments) der Unterhaltungs Karte ab, die dem Formular zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f6061-129">Gets the consolidated reaction (likes and comments) of the conversation card associated with the form</span></span> | | <span data-ttu-id="f6061-130">Reaktions Objekt</span><span class="sxs-lookup"><span data-stu-id="f6061-130">Reaction object</span></span> |
| <span data-ttu-id="f6061-131">**showAllReactions**</span><span class="sxs-lookup"><span data-stu-id="f6061-131">**showAllReactions**</span></span> | <span data-ttu-id="f6061-132">Zeigt den gesamten Reaktions Bildschirm (likes und comments) für das Formular an.</span><span class="sxs-lookup"><span data-stu-id="f6061-132">Shows all the reaction screen (likes and comments) against the form</span></span> | | |
| <span data-ttu-id="f6061-133">**likeForm**</span><span class="sxs-lookup"><span data-stu-id="f6061-133">**likeForm**</span></span> | <span data-ttu-id="f6061-134">Anforderungen zum Hinzufügen einer like-Anzahl zu einem Formular kann die Anzahl verringert werden, wenn der aktuelle Benutzer das Formular bereits gemocht hat.</span><span class="sxs-lookup"><span data-stu-id="f6061-134">Requests to add a like count to a form, the count may decrease if the current user has already liked the form</span></span> | | |
| <span data-ttu-id="f6061-135">**addCommentOnForm**</span><span class="sxs-lookup"><span data-stu-id="f6061-135">**addCommentOnForm**</span></span> | <span data-ttu-id="f6061-136">Anforderungen zum Hinzufügen eines Kommentars zu einem Formular</span><span class="sxs-lookup"><span data-stu-id="f6061-136">Requests to add a comment to a form</span></span> | | |
| <span data-ttu-id="f6061-137">**respondToForm**</span><span class="sxs-lookup"><span data-stu-id="f6061-137">**respondToForm**</span></span> | <span data-ttu-id="f6061-138">Anforderungen zum Hinzufügen einer Antwort zu einem Formular durch Starten des Antwort Bildschirms</span><span class="sxs-lookup"><span data-stu-id="f6061-138">Requests to add a response to a form, by launching response screen</span></span> | | |
| <span data-ttu-id="f6061-139">**sendRemindersToRespond**</span><span class="sxs-lookup"><span data-stu-id="f6061-139">**sendRemindersToRespond**</span></span> | <span data-ttu-id="f6061-140">Sendet eine Erinnerung (eine neue Unterhaltungs Karte) an die vorhandene Karte</span><span class="sxs-lookup"><span data-stu-id="f6061-140">Sends a reminder (a new conversation card) against the existing card</span></span> | | |
| <span data-ttu-id="f6061-141">**copyFormAndForward**</span><span class="sxs-lookup"><span data-stu-id="f6061-141">**copyFormAndForward**</span></span> | <span data-ttu-id="f6061-142">Startet die Unterhaltungs Auswahl, um eine Kopie des vorhandenen Formulars als neue Unterhaltungs Karte weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f6061-142">Launches the conversation picker to forward a copy of the existing form as a new conversation card</span></span> | | |
| <span data-ttu-id="f6061-143">**updateFormPropertiesAsync**</span><span class="sxs-lookup"><span data-stu-id="f6061-143">**updateFormPropertiesAsync**</span></span> | <span data-ttu-id="f6061-144">Bereitstelleneiner Anforderung zum Aktualisieren der dem Formular zugeordneten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6061-144">Post a request to update the properties associated with the form</span></span> |  <ul><li><span data-ttu-id="f6061-145">*propertyUpdates* – ein Array aller Aktualisierungsinformationen, die durchgeführt werden müssen – *Array von KASFormPropertyUpdateInfo*</span><span class="sxs-lookup"><span data-stu-id="f6061-145">*propertyUpdates* - an array of all update infos that are needed to be performed – *array of KASFormPropertyUpdateInfo*</span></span></li><li><span data-ttu-id="f6061-146">*notifyUsers* -Senden von Push-Benachrichtigungen an diese Benutzer-IDs zu diesem Update – *Array von Zeichenfolgen*</span><span class="sxs-lookup"><span data-stu-id="f6061-146">*notifyUsers* - send push notifications to these user ids regarding this update – *array of strings*</span></span></li><li><span data-ttu-id="f6061-147">*notificationMessage* -Push-Benachrichtigungs *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f6061-147">*notificationMessage* - push notification message *string*</span></span></li></ul> | <span data-ttu-id="f6061-148">*Success (Boolean)* – der Erfolg/Fehler des Updates</span><span class="sxs-lookup"><span data-stu-id="f6061-148">*Success(Boolean)* - denotes the success/failure of the update</span></span>|

##   <a name="get-the-summary-associated-with-the-form"></a><span data-ttu-id="f6061-149">Abrufen der dem Formular zugeordneten Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f6061-149">Get the summary associated with the Form</span></span>

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

##   <a name="get-the-flat-summary-all-responses-associated-with-the-form"></a><span data-ttu-id="f6061-150">Abrufen der flachen Zusammenfassung (alle Antworten), die dem Formular zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="f6061-150">Get the flat summary (all responses) associated with the Form</span></span>

```typescript
/**
  * Gets flat responses by all the users associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormFlatSummary} flatSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFlatFormSummaryAsync(callback: function(flatSummary: KASFormFlatSummary, error: string))
```

##   <a name="get-the-processed-summary-aggregated-responses-associated-with-the-form"></a><span data-ttu-id="f6061-151">Abrufen der verarbeiteten Zusammenfassung (aggregierte Antworten), die dem Formular zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="f6061-151">Get the processed summary (aggregated responses) associated with the Form</span></span>

```typescript
/**
  * Gets processed summary from all the responses associated with the form (It is advised to use getFormSummary() instead of this)
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormProcessedSummary} processedSummary can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getProcessedFormSummaryAsync(callback: function(processedSummary: KASFormProcessedSummary, error: string))
```

##   <a name="fetch-from-server-and-get-the-result-url-all-responses-associated-with-the-form"></a><span data-ttu-id="f6061-152">FETCH (vom Server) und Abrufen der Ergebnis-URL (alle Antworten), die dem Formular zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="f6061-152">Fetch (from server) and get the result url (all responses) associated with the Form</span></span>

```typescript
/**
  * Gets the file url from server containing flat responses associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {string} url can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormURLAsync(callback: function(url: string, error: string))
```

##   <a name="share-the-result-url-fetched-from-server"></a><span data-ttu-id="f6061-153">Freigeben der vom Server abgerufenen Ergebnis-URL</span><span class="sxs-lookup"><span data-stu-id="f6061-153">Share the result url fetched from server</span></span>

```typescript
/**
  * Launches native share screen for the form url
  * @param {string} url to be shared
  */
  function shareFormURL(url: string)
```

##   <a name="get-all-the-reactions-associated-with-the-form"></a><span data-ttu-id="f6061-154">Alle dem Formular zugeordneten Reaktionen abrufen</span><span class="sxs-lookup"><span data-stu-id="f6061-154">Get all the reactions associated with the Form</span></span>

```typescript
/**
  * Gets the consolidated reaction (likes and comments) of the conversation card associated with the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormReaction} reaction can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormReactionAsync(callback: function(reaction: KASFormReaction, error: string))
```

##   <a name="show-all-the-reactions-associated-with-the-form"></a><span data-ttu-id="f6061-155">Alle dem Formular zugeordneten Reaktionen anzeigen</span><span class="sxs-lookup"><span data-stu-id="f6061-155">Show all the reactions associated with the Form</span></span>

```typescript
/**
  * Shows all the reaction screen (likes and comments) against the form
  */
  function showAllReactions()
```

##   <a name="put-a-like-on-the-form-in-turn-the-associated-conversation-card"></a><span data-ttu-id="f6061-156">Setzen Sie ein like auf dem Formular (im Gegenzug die zugehörige Unterhaltungs Karte)</span><span class="sxs-lookup"><span data-stu-id="f6061-156">Put a like on the Form (in turn the associated conversation card)</span></span>

```typescript
/**
  * Requests to add a like count to a form, the count may decrease if the current user has already liked the form
  */
  function likeForm()
```

##   <a name="show-response-view-for-the-form"></a><span data-ttu-id="f6061-157">Anzeigen der Antwort Ansicht für das Formular</span><span class="sxs-lookup"><span data-stu-id="f6061-157">Show response view for the Form</span></span>

```typescript
/**
  * Requests to add a response to a form, by launching response screen
  */
  function respondToForm()
```

##   <a name="remind-other-people-to-respond"></a><span data-ttu-id="f6061-158">Andere Personen daran erinnern, zu Antworten</span><span class="sxs-lookup"><span data-stu-id="f6061-158">Remind other people to respond</span></span>

```typescript
/**
  * Sends a reminder (a new conversation card) against the existing card
  */
  function sendRemindersToRespond()
```

##   <a name="forward-a-new-form-duplicated-from-the-associated-one"></a><span data-ttu-id="f6061-159">Weiterleiten eines neuen Formulars, das aus dem verknüpften Formular dupliziert wurde</span><span class="sxs-lookup"><span data-stu-id="f6061-159">Forward a new Form duplicated from the associated one</span></span>

```typescript
/**
  * Launches the conversation picker to forward a copy of the existing form as a new conversation card
  */
  function copyFormAndForward() 
```

##   <a name="close-the-form-in-turn-responses-to-it"></a><span data-ttu-id="f6061-160">Das Formular geschlossen (im Gegenzug Antworten)</span><span class="sxs-lookup"><span data-stu-id="f6061-160">Close the Form (in turn responses to it)</span></span>

```typescript
/**
  * Closes the form associated with the card, no responses will be allowed further
  */
  function closeForm()
```
