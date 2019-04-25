#   <a name="form-response-flow-apis"></a><span data-ttu-id="b43e1-101">Formular Antwort Fluss-APIs:</span><span class="sxs-lookup"><span data-stu-id="b43e1-101">Form response flow APIs:</span></span>

| <span data-ttu-id="b43e1-102">**API**</span><span class="sxs-lookup"><span data-stu-id="b43e1-102">**API**</span></span> | <span data-ttu-id="b43e1-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43e1-103">Description</span></span> | <span data-ttu-id="b43e1-104">Anforderungs Parameter</span><span class="sxs-lookup"><span data-stu-id="b43e1-104">Request Parameter</span></span> | <span data-ttu-id="b43e1-105">Antwort Ausgabe</span><span class="sxs-lookup"><span data-stu-id="b43e1-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="b43e1-106">**canRespondToFormAsync**</span><span class="sxs-lookup"><span data-stu-id="b43e1-106">**canRespondToFormAsync**</span></span> | <span data-ttu-id="b43e1-107">Ruft ab, ob der aktuelle Benutzer auf das Formularantworten kann.</span><span class="sxs-lookup"><span data-stu-id="b43e1-107">Gets whether the current user can respond to the form</span></span> |  | <span data-ttu-id="b43e1-108">canRespond (Boolean)-true, wenn der aktuelle Benutzer antwortet</span><span class="sxs-lookup"><span data-stu-id="b43e1-108">canRespond (Boolean) - true if current user is allowed to respond</span></span> |
| <span data-ttu-id="b43e1-109">**getFormAsync**</span><span class="sxs-lookup"><span data-stu-id="b43e1-109">**getFormAsync**</span></span> | | | <span data-ttu-id="b43e1-110">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="b43e1-110">Form object</span></span> |
| <span data-ttu-id="b43e1-111">**getFormStatusAsync**</span><span class="sxs-lookup"><span data-stu-id="b43e1-111">**getFormStatusAsync**</span></span> | <span data-ttu-id="b43e1-112">Ruft den Status des Formulars ab, das der Unterhaltungs Karte zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b43e1-112">Gets the status of the form associated with the conversation card</span></span> | | <span data-ttu-id="b43e1-113">IsActive (Boolean)-true, wenn das Formular noch nicht abgelaufen ist</span><span class="sxs-lookup"><span data-stu-id="b43e1-113">isActive (Boolean) - true if the form is not yet expired</span></span> |
| <span data-ttu-id="b43e1-114">**getMyFormResponsesAsync**</span><span class="sxs-lookup"><span data-stu-id="b43e1-114">**getMyFormResponsesAsync**</span></span> | <span data-ttu-id="b43e1-115">Ruft alle Antworten des aktuellen Benutzers anhand des Formulars ab.</span><span class="sxs-lookup"><span data-stu-id="b43e1-115">Gets all the responses of the current user against the form</span></span> | | <span data-ttu-id="b43e1-116">Array von Response-Objekten</span><span class="sxs-lookup"><span data-stu-id="b43e1-116">Array of response objects</span></span> |
| <span data-ttu-id="b43e1-117">**sumbitFormResponse**</span><span class="sxs-lookup"><span data-stu-id="b43e1-117">**sumbitFormResponse**</span></span> | <span data-ttu-id="b43e1-118">Übermittelt eine neue Antwort auf das Formular, das der Unterhaltungs Karte zugeordnet ist – weist den aktuellen Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="b43e1-118">Submits a new response against the form associated with the conversation card – dismisses the current screen</span></span> |  <ul><li><span data-ttu-id="b43e1-119">questionToAnswerMap (JSON) – Frage-ID für die Antwort Zuordnung</span><span class="sxs-lookup"><span data-stu-id="b43e1-119">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="b43e1-120">Antwort-Nr. (Zeichenfolge), die ausgefüllt werden soll, wenn die aktuelle Antwort eine Bearbeitung/Aktualisierung auf eine frühere ist.</span><span class="sxs-lookup"><span data-stu-id="b43e1-120">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="b43e1-121">isEdit (Boolean) gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt.</span><span class="sxs-lookup"><span data-stu-id="b43e1-121">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="b43e1-122">showInChatCanvas (Boolean) gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b43e1-122">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="b43e1-123">isAnonymous (Boolean) gibt an, ob die Antwort als anonym oder nicht registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b43e1-123">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |
| <span data-ttu-id="b43e1-124">**sumbitFormResponseWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="b43e1-124">**sumbitFormResponseWithoutDismiss**</span></span> | <span data-ttu-id="b43e1-125">Übermittelt eine neue Antwort für das Formular, das der Unterhaltungs Karte zugeordnet ist, ohne den aktuellen Bildschirm zu verWerfen.</span><span class="sxs-lookup"><span data-stu-id="b43e1-125">Submits a new response against the form associated with the conversation card without dismissing the current screen</span></span> |  <ul><li><span data-ttu-id="b43e1-126">questionToAnswerMap (JSON) – Frage-ID für die Antwort Zuordnung</span><span class="sxs-lookup"><span data-stu-id="b43e1-126">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="b43e1-127">Antwort-Nr. (Zeichenfolge), die ausgefüllt werden soll, wenn die aktuelle Antwort eine Bearbeitung/Aktualisierung auf eine frühere ist.</span><span class="sxs-lookup"><span data-stu-id="b43e1-127">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="b43e1-128">isEdit (Boolean) gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt.</span><span class="sxs-lookup"><span data-stu-id="b43e1-128">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="b43e1-129">showInChatCanvas (Boolean) gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b43e1-129">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="b43e1-130">isAnonymous (Boolean) gibt an, ob die Antwort als anonym oder nicht registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b43e1-130">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |


##  <a name="get-the-associated-form"></a><span data-ttu-id="b43e1-131">Abrufen des zugeordneten Formulars</span><span class="sxs-lookup"><span data-stu-id="b43e1-131">Get the associated Form</span></span>

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a><span data-ttu-id="b43e1-132">Überprüfen, ob das zugehörige Formular abgelaufen ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="b43e1-132">Check if the associated form is expired or not</span></span>

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a><span data-ttu-id="b43e1-133">Abrufen aller Antworten des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="b43e1-133">Get all the responses of the current user</span></span>

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a><span data-ttu-id="b43e1-134">Senden einer neuen Antwort für das zugeordnete Formular</span><span class="sxs-lookup"><span data-stu-id="b43e1-134">Submit a new response for the associated Form</span></span>

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
