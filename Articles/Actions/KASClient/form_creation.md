#   <a name="form-creation-flow-apis"></a>Formular Erstellungs Fluss-APIs:

| **API** | Beschreibung | Anforderungs Parameter | Antwort Ausgabe |
| :---: | :---: | :---: | :--- |
| **initFormAsync** | Initialisiert und gibt ein leeres Form-Objekt basierend auf der im Paket vorhandenen Standardformular Datei zurück. |  | Form-Objekt |
| **submitFormRequest** | Übermittelt das neu erstellte Formular als Anforderung. Dies führt zu einer neuen Unterhaltungs Karte | <ul><li>Formular</li><li>Boolean – sollte aufblasen/nicht</li></ul>| |
| **submitFormRequestWithoutDismiss** | Übermittelt das neu erstellte Formular als Anforderung. Dies führt zu einer neuen Unterhaltungs Karte |<ul><li>Formular</li><li>Boolean – sollte aufblasen/nicht</li></ul>| |
| **updateForm** | Wird zum vornehmen von Änderungen an Formularfeldern wie Titel, Beschreibung und Einstellungen verwendet. | <ul><li>Felder, die updation erfordern</li><li>Boolean – sollte aufblasen/nicht</li></ul> | |

##  <a name="initialize-a-form"></a>Initialisieren eines Formulars

```typescript
/**
  * Initializes and returns an empty form object based on the default form file present in the package
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function initFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="submit-the-newly-created-form"></a>ÜberMitteln des neu erstellten Formulars

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


##  <a name="update-form"></a>Formular aktualisieren

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

