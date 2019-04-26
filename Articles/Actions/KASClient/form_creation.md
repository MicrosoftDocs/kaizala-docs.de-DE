#   <a name="form-creation-flow-apis"></a><span data-ttu-id="245e0-101">Formular Erstellungs Fluss-APIs:</span><span class="sxs-lookup"><span data-stu-id="245e0-101">Form creation flow APIs:</span></span>

| <span data-ttu-id="245e0-102">**API**</span><span class="sxs-lookup"><span data-stu-id="245e0-102">**API**</span></span> | <span data-ttu-id="245e0-103">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="245e0-103">Description</span></span> | <span data-ttu-id="245e0-104">Anforderungs Parameter</span><span class="sxs-lookup"><span data-stu-id="245e0-104">Request Parameter</span></span> | <span data-ttu-id="245e0-105">Antwort Ausgabe</span><span class="sxs-lookup"><span data-stu-id="245e0-105">Response Output</span></span> |
| :---: | :---: | :---: | :--- |
| <span data-ttu-id="245e0-106">**initFormAsync**</span><span class="sxs-lookup"><span data-stu-id="245e0-106">**initFormAsync**</span></span> | <span data-ttu-id="245e0-107">Initialisiert und gibt ein leeres Form-Objekt basierend auf der im Paket vorhandenen Standardformular Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="245e0-107">Initializes and returns an empty form object based on the default form file present in the package</span></span> |  | <span data-ttu-id="245e0-108">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="245e0-108">Form Object</span></span> |
| <span data-ttu-id="245e0-109">**submitFormRequest**</span><span class="sxs-lookup"><span data-stu-id="245e0-109">**submitFormRequest**</span></span> | <span data-ttu-id="245e0-110">Übermittelt das neu erstellte Formular als Anforderung.</span><span class="sxs-lookup"><span data-stu-id="245e0-110">Submits the newly created form as a request.</span></span> <span data-ttu-id="245e0-111">Dies führt zu einer neuen Unterhaltungs Karte</span><span class="sxs-lookup"><span data-stu-id="245e0-111">This results a new conversation card</span></span> | <ul><li><span data-ttu-id="245e0-112">Formular</span><span class="sxs-lookup"><span data-stu-id="245e0-112">Form</span></span></li><li><span data-ttu-id="245e0-113">Boolean – sollte aufblasen/nicht</span><span class="sxs-lookup"><span data-stu-id="245e0-113">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="245e0-114">**submitFormRequestWithoutDismiss**</span><span class="sxs-lookup"><span data-stu-id="245e0-114">**submitFormRequestWithoutDismiss**</span></span> | <span data-ttu-id="245e0-115">Übermittelt das neu erstellte Formular als Anforderung.</span><span class="sxs-lookup"><span data-stu-id="245e0-115">Submits the newly created form as a request.</span></span> <span data-ttu-id="245e0-116">Dies führt zu einer neuen Unterhaltungs Karte</span><span class="sxs-lookup"><span data-stu-id="245e0-116">This results a new conversation card</span></span> |<ul><li><span data-ttu-id="245e0-117">Formular</span><span class="sxs-lookup"><span data-stu-id="245e0-117">Form</span></span></li><li><span data-ttu-id="245e0-118">Boolean – sollte aufblasen/nicht</span><span class="sxs-lookup"><span data-stu-id="245e0-118">Boolean – should inflate/not</span></span></li></ul>| |
| <span data-ttu-id="245e0-119">**updateForm**</span><span class="sxs-lookup"><span data-stu-id="245e0-119">**updateForm**</span></span> | <span data-ttu-id="245e0-120">Wird zum vornehmen von Änderungen an Formularfeldern wie Titel, Beschreibung und Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="245e0-120">Used for making changes in form fields like title, description and settings</span></span> | <ul><li><span data-ttu-id="245e0-121">Felder, die updation erfordern</span><span class="sxs-lookup"><span data-stu-id="245e0-121">Fields that require updation</span></span></li><li><span data-ttu-id="245e0-122">Boolean – sollte aufblasen/nicht</span><span class="sxs-lookup"><span data-stu-id="245e0-122">Boolean – should inflate/not</span></span></li></ul> | |

##  <a name="initialize-a-form"></a><span data-ttu-id="245e0-123">Initialisieren eines Formulars</span><span class="sxs-lookup"><span data-stu-id="245e0-123">Initialize a Form</span></span>

```typescript
/**
  * Initializes and returns an empty form object based on the default form file present in the package
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function initFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="submit-the-newly-created-form"></a><span data-ttu-id="245e0-124">ÜberMitteln des neu erstellten Formulars</span><span class="sxs-lookup"><span data-stu-id="245e0-124">Submit the newly created Form</span></span>

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


##  <a name="update-form"></a><span data-ttu-id="245e0-125">Formular aktualisieren</span><span class="sxs-lookup"><span data-stu-id="245e0-125">Update Form</span></span>

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

