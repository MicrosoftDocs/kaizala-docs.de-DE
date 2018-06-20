#   <a name="form-creation-flow-apis"></a><span data-ttu-id="848d6-101">Bilden Sie Erstellung Fluss APIs:</span><span class="sxs-lookup"><span data-stu-id="848d6-101">Form creation flow APIs:</span></span>

| <span data-ttu-id="848d6-102">**API**</span><span class="sxs-lookup"><span data-stu-id="848d6-102">**API**</span></span> | <span data-ttu-id="848d6-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="848d6-103">Description</span></span> | <span data-ttu-id="848d6-104">Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="848d6-104">Request Parameter</span></span> | <span data-ttu-id="848d6-105">Antwort-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="848d6-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="848d6-106">**initFormAsync**</span><span class="sxs-lookup"><span data-stu-id="848d6-106">**initFormAsync**</span></span> | <span data-ttu-id="848d6-107">Initialisiert und gibt ein leeres Formular-Objekt auf der Standard-Datei in das Paket vorhanden basieren</span><span class="sxs-lookup"><span data-stu-id="848d6-107">Initializes and returns an empty form object based on the default form file present in the package</span></span> |  | <span data-ttu-id="848d6-108">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="848d6-108">Form Object</span></span> |
| <span data-ttu-id="848d6-109">**submitFormRequest**</span><span class="sxs-lookup"><span data-stu-id="848d6-109">**submitFormRequest**</span></span> | <span data-ttu-id="848d6-110">Sendet das neu erstellte Formular als Anforderung.</span><span class="sxs-lookup"><span data-stu-id="848d6-110">Submits the newly created form as a request.</span></span> <span data-ttu-id="848d6-111">Dies führt zu eine neuen Unterhaltung Karte</span><span class="sxs-lookup"><span data-stu-id="848d6-111">This results a new conversation card</span></span> | <ul><li><span data-ttu-id="848d6-112">Formular</span><span class="sxs-lookup"><span data-stu-id="848d6-112">Form</span></span></li><li><span data-ttu-id="848d6-113">Boolean – sollten vergrößert werden soll oder nicht</span><span class="sxs-lookup"><span data-stu-id="848d6-113">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="848d6-114">**submitFormRequestWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="848d6-114">**submitFormRequestWithoutDismiss**</span></span> | <span data-ttu-id="848d6-115">Sendet das neu erstellte Formular als Anforderung.</span><span class="sxs-lookup"><span data-stu-id="848d6-115">Submits the newly created form as a request.</span></span> <span data-ttu-id="848d6-116">Dies führt zu eine neuen Unterhaltung Karte</span><span class="sxs-lookup"><span data-stu-id="848d6-116">This results a new conversation card</span></span> |<ul><li><span data-ttu-id="848d6-117">Formular</span><span class="sxs-lookup"><span data-stu-id="848d6-117">Form</span></span></li><li><span data-ttu-id="848d6-118">Boolean – sollten vergrößert werden soll oder nicht</span><span class="sxs-lookup"><span data-stu-id="848d6-118">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="848d6-119">**updateForm**</span><span class="sxs-lookup"><span data-stu-id="848d6-119">**updateForm**</span></span> | <span data-ttu-id="848d6-120">Verwendet für die Änderung in Formularfeldern wie Titel, Beschreibung und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="848d6-120">Used for making changes in form fields like title, description and settings</span></span> | <ul><li><span data-ttu-id="848d6-121">Felder, die aktualisiert werden müssen</span><span class="sxs-lookup"><span data-stu-id="848d6-121">Fields that require updation</span></span></li><li><span data-ttu-id="848d6-122">Boolean – sollten vergrößert werden soll oder nicht</span><span class="sxs-lookup"><span data-stu-id="848d6-122">Boolean – should inflate/not</span></span></li></ul> | |

##  <a name="initialize-a-form"></a><span data-ttu-id="848d6-123">Initialisieren eines Formulars</span><span class="sxs-lookup"><span data-stu-id="848d6-123">Initialize a Form</span></span>

```typescript
/**
  * Initializes and returns an empty form object based on the default form file present in the package
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function initFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="submit-the-newly-created-form"></a><span data-ttu-id="848d6-124">Das neu erstellte Formular übermitteln</span><span class="sxs-lookup"><span data-stu-id="848d6-124">Submit the newly created Form</span></span>

```typescript
/**
  * Submits the newly created form as a request. This results a new conversation card
  * @param {KASForm} form
  */
  function submitFormRequest(form: KASForm)
  ```

```typescript
  /**
  * Submits the newly created form as a request. This results a new conversation card
  * @param {KASForm} form
  */
  function submitFormRequestWithoutDismiss(form: KASForm, shouldInflate: boolean)
  ```


##  <a name="update-form"></a><span data-ttu-id="848d6-125">Formular für das Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="848d6-125">Update Form</span></span>

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

