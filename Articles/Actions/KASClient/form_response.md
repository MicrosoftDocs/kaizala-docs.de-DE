#   <a name="form-response-flow-apis"></a><span data-ttu-id="17eff-101">Bilden Sie Antwort Fluss APIs:</span><span class="sxs-lookup"><span data-stu-id="17eff-101">Form response flow APIs:</span></span>

| <span data-ttu-id="17eff-102">**API**</span><span class="sxs-lookup"><span data-stu-id="17eff-102">**API**</span></span> | <span data-ttu-id="17eff-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17eff-103">Description</span></span> | <span data-ttu-id="17eff-104">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="17eff-104">Request Parameter</span></span> | <span data-ttu-id="17eff-105">Antwort-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="17eff-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="17eff-106">**canRespondToFormAsync**</span><span class="sxs-lookup"><span data-stu-id="17eff-106">**canRespondToFormAsync**</span></span> | <span data-ttu-id="17eff-107">Ruft ab, ob der aktuelle Benutzer beantwortet werden können</span><span class="sxs-lookup"><span data-stu-id="17eff-107">Gets whether the current user can respond to the form</span></span> |  | <span data-ttu-id="17eff-108">True, wenn der aktuelle Benutzer berechtigt ist, reagieren CanRespond (boolesch)-</span><span class="sxs-lookup"><span data-stu-id="17eff-108">canRespond (Boolean) - true if current user is allowed to respond</span></span> |
| <span data-ttu-id="17eff-109">**getFormAsync**</span><span class="sxs-lookup"><span data-stu-id="17eff-109">**getFormAsync**</span></span> | | | <span data-ttu-id="17eff-110">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="17eff-110">Form object</span></span> |
| <span data-ttu-id="17eff-111">**getFormStatusAsync**</span><span class="sxs-lookup"><span data-stu-id="17eff-111">**getFormStatusAsync**</span></span> | <span data-ttu-id="17eff-112">Ruft den Status des Formulars der Unterhaltung Karte zugeordnete ab</span><span class="sxs-lookup"><span data-stu-id="17eff-112">Gets the status of the form associated with the conversation card</span></span> | | <span data-ttu-id="17eff-113">True, wenn das Formular noch nicht abgelaufen ist IsActive (boolesch)-</span><span class="sxs-lookup"><span data-stu-id="17eff-113">isActive (Boolean) - true if the form is not yet expired</span></span> |
| <span data-ttu-id="17eff-114">**getMyFormResponsesAsync**</span><span class="sxs-lookup"><span data-stu-id="17eff-114">**getMyFormResponsesAsync**</span></span> | <span data-ttu-id="17eff-115">Dient zum Abrufen aller Antworten des aktuellen Benutzers für das Formular</span><span class="sxs-lookup"><span data-stu-id="17eff-115">Gets all the responses of the current user against the form</span></span> | | <span data-ttu-id="17eff-116">Array von Antwortobjekte</span><span class="sxs-lookup"><span data-stu-id="17eff-116">Array of response objects</span></span> |
| <span data-ttu-id="17eff-117">**sumbitFormResponse**</span><span class="sxs-lookup"><span data-stu-id="17eff-117">**sumbitFormResponse**</span></span> | <span data-ttu-id="17eff-118">Sendet eine neue Antwort für das Formular der Unterhaltung Karte zugeordnete – schließt den aktuellen Bildschirm</span><span class="sxs-lookup"><span data-stu-id="17eff-118">Submits a new response against the form associated with the conversation card – dismisses the current screen</span></span> |  <ul><li><span data-ttu-id="17eff-119">QuestionToAnswerMap (JSON) - Frage Id Zuordnung zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="17eff-119">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="17eff-120">responseId(string) gefüllt werden soll, wenn die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</span><span class="sxs-lookup"><span data-stu-id="17eff-120">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="17eff-121">IsEdit (boolesch) gibt an, ob die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</span><span class="sxs-lookup"><span data-stu-id="17eff-121">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="17eff-122">showInChatCanvas(Boolean) gibt an, ob eine separate Chat Karte für diese Antwort oder nicht erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="17eff-122">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="17eff-123">isAnonymous(boolean) gibt an, ob die Antwort als anonym erfasst werden sollen</span><span class="sxs-lookup"><span data-stu-id="17eff-123">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |
| <span data-ttu-id="17eff-124">**sumbitFormResponseWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="17eff-124">**sumbitFormResponseWithoutDismiss**</span></span> | <span data-ttu-id="17eff-125">Sendet eine neue Antwort für das Formular für die Unterhaltung Karte ohne Schließen des aktuellen Bildschirms zugeordneten</span><span class="sxs-lookup"><span data-stu-id="17eff-125">Submits a new response against the form associated with the conversation card without dismissing the current screen</span></span> |  <ul><li><span data-ttu-id="17eff-126">QuestionToAnswerMap (JSON) - Frage Id Zuordnung zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="17eff-126">questionToAnswerMap (JSON ) - question id to answer mapping</span></span></li><li><span data-ttu-id="17eff-127">responseId(string) gefüllt werden soll, wenn die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</span><span class="sxs-lookup"><span data-stu-id="17eff-127">responseId(string) to be filled if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="17eff-128">IsEdit (boolesch) gibt an, ob die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</span><span class="sxs-lookup"><span data-stu-id="17eff-128">isEdit (boolean) denotes if the current response is an edit/update to a previous one</span></span></li><li><span data-ttu-id="17eff-129">showInChatCanvas(Boolean) gibt an, ob eine separate Chat Karte für diese Antwort oder nicht erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="17eff-129">showInChatCanvas(Boolean) denotes if a separate chat card needs to be created for this response or not</span></span></li><li><span data-ttu-id="17eff-130">isAnonymous(boolean) gibt an, ob die Antwort als anonym erfasst werden sollen</span><span class="sxs-lookup"><span data-stu-id="17eff-130">isAnonymous(boolean) denotes if the response should be registered as anonymous or not</span></span></li></ul> | |


##  <a name="get-the-associated-form"></a><span data-ttu-id="17eff-131">Abrufen des zugeordneten Formulars</span><span class="sxs-lookup"><span data-stu-id="17eff-131">Get the associated Form</span></span>

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a><span data-ttu-id="17eff-132">Überprüfen Sie, ob das Formular zugeordnete oder nicht abgelaufen ist</span><span class="sxs-lookup"><span data-stu-id="17eff-132">Check if the associated form is expired or not</span></span>

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a><span data-ttu-id="17eff-133">Abrufen Sie aller Antworten des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="17eff-133">Get all the responses of the current user</span></span>

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a><span data-ttu-id="17eff-134">Senden Sie eine neue Antwort für das zugeordnete Formular</span><span class="sxs-lookup"><span data-stu-id="17eff-134">Submit a new response for the associated Form</span></span>

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
