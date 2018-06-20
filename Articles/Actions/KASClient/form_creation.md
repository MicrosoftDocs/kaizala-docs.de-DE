#   <a name="form-creation-flow-apis"></a>Bilden Sie Erstellung Fluss APIs:

| **API** | Beschreibung | Anforderungsparameter | Antwort-Ausgabe |
| :---: | :---: | :---: | :--- |
| **initFormAsync** | Initialisiert und gibt ein leeres Formular-Objekt auf der Standard-Datei in das Paket vorhanden basieren |  | Form-Objekt |
| **submitFormRequest** | Sendet das neu erstellte Formular als Anforderung. Dies führt zu eine neuen Unterhaltung Karte | <ul><li>Formular</li><li>Boolean – sollten vergrößert werden soll oder nicht</li></ul>| |
| **submitFormRequestWithoutDismiss** | Sendet das neu erstellte Formular als Anforderung. Dies führt zu eine neuen Unterhaltung Karte |<ul><li>Formular</li><li>Boolean – sollten vergrößert werden soll oder nicht</li></ul>| |
| **updateForm** | Verwendet für die Änderung in Formularfeldern wie Titel, Beschreibung und Einstellungen | <ul><li>Felder, die aktualisiert werden müssen</li><li>Boolean – sollten vergrößert werden soll oder nicht</li></ul> | |

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

##  <a name="submit-the-newly-created-form"></a>Das neu erstellte Formular übermitteln

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


##  <a name="update-form"></a>Formular für das Aktualisieren

```typescript

  /**
  * use for making changes in form fields like title, description and settings.
  */
  function updateForm(fields: string, shouldInflate: boolean,callback: (success: boolean) => void)
  ```

