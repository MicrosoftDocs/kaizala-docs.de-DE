#   <a name="form-response-flow-apis"></a>Bilden Sie Antwort Fluss APIs:

| **API** | Beschreibung | Anforderungsparameter | Antwort-Ausgabe |
| :---: | :---: | :---: | :--- |
| **canRespondToFormAsync** | Ruft ab, ob der aktuelle Benutzer beantwortet werden können |  | True, wenn der aktuelle Benutzer berechtigt ist, reagieren CanRespond (boolesch)- |
| **getFormAsync** | | | Form-Objekt |
| **getFormStatusAsync** | Ruft den Status des Formulars der Unterhaltung Karte zugeordnete ab | | True, wenn das Formular noch nicht abgelaufen ist IsActive (boolesch)- |
| **getMyFormResponsesAsync** | Dient zum Abrufen aller Antworten des aktuellen Benutzers für das Formular | | Array von Antwortobjekte |
| **sumbitFormResponse** | Sendet eine neue Antwort für das Formular der Unterhaltung Karte zugeordnete – schließt den aktuellen Bildschirm |  <ul><li>QuestionToAnswerMap (JSON) - Frage Id Zuordnung zu beantworten.</li><li>responseId(string) gefüllt werden soll, wenn die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</li><li>IsEdit (boolesch) gibt an, ob die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</li><li>showInChatCanvas(Boolean) gibt an, ob eine separate Chat Karte für diese Antwort oder nicht erstellt werden soll</li><li>isAnonymous(boolean) gibt an, ob die Antwort als anonym erfasst werden sollen</li></ul> | |
| **sumbitFormResponseWithoutDismiss** | Sendet eine neue Antwort für das Formular für die Unterhaltung Karte ohne Schließen des aktuellen Bildschirms zugeordneten |  <ul><li>QuestionToAnswerMap (JSON) - Frage Id Zuordnung zu beantworten.</li><li>responseId(string) gefüllt werden soll, wenn die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</li><li>IsEdit (boolesch) gibt an, ob die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist</li><li>showInChatCanvas(Boolean) gibt an, ob eine separate Chat Karte für diese Antwort oder nicht erstellt werden soll</li><li>isAnonymous(boolean) gibt an, ob die Antwort als anonym erfasst werden sollen</li></ul> | |


##  <a name="get-the-associated-form"></a>Abrufen des zugeordneten Formulars

```typescript
/**
  * Gets the form object associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {KASForm} form can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormAsync(callback: function(form: KASForm, error: string))
```

##  <a name="check-if-the-associated-form-is-expired-or-not"></a>Überprüfen Sie, ob das Formular zugeordnete oder nicht abgelaufen ist

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a>Abrufen Sie aller Antworten des aktuellen Benutzers

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a>Senden Sie eine neue Antwort für das zugeordnete Formular

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
