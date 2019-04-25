#   <a name="form-response-flow-apis"></a>Formular Antwort Fluss-APIs:

| **API** | Beschreibung | Anforderungs Parameter | Antwort Ausgabe |
| :---: | :---: | :---: | :--- |
| **canRespondToFormAsync** | Ruft ab, ob der aktuelle Benutzer auf das Formularantworten kann. |  | canRespond (Boolean)-true, wenn der aktuelle Benutzer antwortet |
| **getFormAsync** | | | Form-Objekt |
| **getFormStatusAsync** | Ruft den Status des Formulars ab, das der Unterhaltungs Karte zugeordnet ist. | | IsActive (Boolean)-true, wenn das Formular noch nicht abgelaufen ist |
| **getMyFormResponsesAsync** | Ruft alle Antworten des aktuellen Benutzers anhand des Formulars ab. | | Array von Response-Objekten |
| **sumbitFormResponse** | Übermittelt eine neue Antwort auf das Formular, das der Unterhaltungs Karte zugeordnet ist – weist den aktuellen Bildschirm ab. |  <ul><li>questionToAnswerMap (JSON) – Frage-ID für die Antwort Zuordnung</li><li>Antwort-Nr. (Zeichenfolge), die ausgefüllt werden soll, wenn die aktuelle Antwort eine Bearbeitung/Aktualisierung auf eine frühere ist.</li><li>isEdit (Boolean) gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt.</li><li>showInChatCanvas (Boolean) gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht.</li><li>isAnonymous (Boolean) gibt an, ob die Antwort als anonym oder nicht registriert werden soll.</li></ul> | |
| **sumbitFormResponseWithoutDismiss** | Übermittelt eine neue Antwort für das Formular, das der Unterhaltungs Karte zugeordnet ist, ohne den aktuellen Bildschirm zu verWerfen. |  <ul><li>questionToAnswerMap (JSON) – Frage-ID für die Antwort Zuordnung</li><li>Antwort-Nr. (Zeichenfolge), die ausgefüllt werden soll, wenn die aktuelle Antwort eine Bearbeitung/Aktualisierung auf eine frühere ist.</li><li>isEdit (Boolean) gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt.</li><li>showInChatCanvas (Boolean) gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht.</li><li>isAnonymous (Boolean) gibt an, ob die Antwort als anonym oder nicht registriert werden soll.</li></ul> | |


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

##  <a name="check-if-the-associated-form-is-expired-or-not"></a>Überprüfen, ob das zugehörige Formular abgelaufen ist oder nicht

```typescript
/**
  * Gets the status of the form associated with the conversation card
  * @param {Callback} callback with below parameters:
  * * * * @param {boolean} isActive true if the form is not yet expired
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getFormStatusAsync(callback: function(isActive: boolean, error: string))
```

##  <a name="get-all-the-responses-of-the-current-user"></a>Abrufen aller Antworten des aktuellen Benutzers

```typescript
/**
  * Gets all the responses of the current user against the form
  * @param {Callback} callback with below parameters:
  * * * * @param {KASFormResponse[]} responses can be null in case of error
  * * * * @param {string} error message in case of error, null otherwise
  */
  function getMyFormResponsesAsync(callback: function(responses: KASFormResponse[], error: string))
```

##  <a name="submit-a-new-response-for-the-associated-form"></a>Senden einer neuen Antwort für das zugeordnete Formular

```typescript
/**
  * Submits a new response against the form associated with the conversation card
  * @param {JSON} questionToAnswerMap question id to answer mapping
  * @param {string} responseId to be filled if the current response is an edit/update to a previous one
  * @param {boolean} isEdit denotes if the current response is an edit/update to a previous one
  */
  function sumbitFormResponse(questionToAnswerMap: JSON, responseId: string, isEdit: boolean)
  ```
