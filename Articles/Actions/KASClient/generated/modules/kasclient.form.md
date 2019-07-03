[](../README.md) > [KASClient](../modules/kasclient.md) > -[Formular](../modules/kasclient.form.md)

# <a name="module-form"></a>Modul: Form

## <a name="index"></a>Index 

### <a name="creation"></a>Erstellung

* [initFormAsync](kasclient.form.md#initformasync)
* [submitFormRequestV2](kasclient.form.md#submitformrequestv2)
* [submitFormRequestWithoutDismiss](kasclient.form.md#submitformrequestwithoutdismiss)
* [updateForm](kasclient.form.md#updateform)
### <a name="response"></a>Antwort

* [canRespondToFormAsync](kasclient.form.md#canrespondtoformasync)
* [getFormAsync](kasclient.form.md#getformasync)
* [getFormStatusAsync](kasclient.form.md#getformstatusasync)
* [getMyFormResponsesAsync](kasclient.form.md#getmyformresponsesasync)
* [sumbitFormResponse](kasclient.form.md#sumbitformresponse)
* [sumbitFormResponseWithoutDismiss](kasclient.form.md#sumbitformresponsewithoutdismiss)
### <a name="summary"></a>Zusammenfassung

* [FormSummaryCallback](kasclient.form.md#formsummarycallback)
* [addCommentOnForm](kasclient.form.md#addcommentonform)
* [closeForm](kasclient.form.md#closeform)
* [copyFormAndForward](kasclient.form.md#copyformandforward)
* [executeActionFetchQueryAsync](kasclient.form.md#executeactionfetchqueryasync)
* [fetchFormAsync](kasclient.form.md#fetchformasync)
* [fetchFormInfosAsync](kasclient.form.md#fetchforminfosasync)
* [getActionInstanceLocalDataCacheAsync](kasclient.form.md#getactioninstancelocaldatacacheasync)
* [getActionPackageLocalDataCacheAsync](kasclient.form.md#getactionpackagelocaldatacacheasync)
* [getFormReactionAsync](kasclient.form.md#getformreactionasync)
* [getFormSummaryAsync](kasclient.form.md#getformsummaryasync)
* [getFormURLAsync](kasclient.form.md#getformurlasync)
* [getFormUserCapabilitiesAsync](kasclient.form.md#getformusercapabilitiesasync)
* [isSubscribed](kasclient.form.md#issubscribed)
* [likeForm](kasclient.form.md#likeform)
* [sendRemindersToRespond](kasclient.form.md#sendreminderstorespond)
* [shareFormURL](kasclient.form.md#shareformurl)
* [showAllReactions](kasclient.form.md#showallreactions)
* [updateActionInstanceLocalDataCacheAsync](kasclient.form.md#updateactioninstancelocaldatacacheasync)
* [updateActionPackageLocalDataCacheAsync](kasclient.form.md#updateactionpackagelocaldatacacheasync)
* [updateFormPropertiesAsync](kasclient.form.md#updateformpropertiesasync)

---

## <a name="creation"></a>Erstellung

<a id="initformasync"></a>

###  <a name="initformasync"></a>initFormAsync

▸ **initFormAsync**(Callback: *`function`*):`void`

Initialisiert und gibt ein leeres Form-Objekt basierend auf der im Paket vorhandenen Standardformular Datei zurück.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.Form.initFormAsync(function (form, error) {
     if (error != null) {
         // use form
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASForm}-Formular kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="submitformrequestv2"></a>

###  <a name="submitformrequestv2"></a>submitFormRequestV2

▸ **submitFormRequestV2**(Formular: *[KASForm](../classes/kasclient.kasform.md)*, shouldDismiss?: *`boolean`*, shouldSendToSubscribers?: *`boolean`*):`void`

Sendet das neu erstellte Formular als Anforderung. Dadurch wird eine neue Unterhaltungs Karte angezeigt.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| Formular | [KASForm](../classes/kasclient.kasform.md) | - |  \- |
| `Default value`shouldDismiss | `boolean` | false |  true, wenn das Formular bei der Übermittlung entlassen werden muss, andernfalls false. false andernfalls |
| `Default value`shouldSendToSubscribers | `boolean` | true |  gilt in öffentlichen Gruppen als auf false festgelegt, wenn die Anforderung nicht für Abonnenten vorgesehen ist. |

**Gibt Folgendes zurück:**`void`

___
<a id="submitformrequestwithoutdismiss"></a>

###  <a name="submitformrequestwithoutdismiss"></a>submitFormRequestWithoutDismiss

▸ **submitFormRequestWithoutDismiss**(Formular: *[KASForm](../classes/kasclient.kasform.md)*, shouldInflate: *`boolean`*):`void`

Sendet das neu erstellte Formular als Anforderung. Dadurch wird eine neue Unterhaltungs Karte angezeigt.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Formular | [KASForm](../classes/kasclient.kasform.md) |  \- |
| shouldInflate | `boolean` |  Boolean – sollte aufblasen/nicht |

**Gibt Folgendes zurück:**`void`

___
<a id="updateform"></a>

###  <a name="updateform"></a>updateForm

▸ **updateForm**(Fields *`string`*:, shouldInflate *`boolean`*:, Callback *`function`*:):`void`

Verwenden Sie für das vornehmen von Änderungen in Formularfeldern wie Titel, Beschreibung und Einstellungen.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
  var fieldsToUpdate = {"title" : "<updated title", "exp" : "<expiry time>",
           "vis" : "<result visibility - set as sender/all/admin>", "Description": "<Updated survey desc>"};
  KASClient.Form.updateForm(JSON.stringify(fieldsToUpdate), false, function(success) {
       if(success) {
         //do something
       }
   });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| fields | `string` |  JSON-Zeichenfolge von Feldern, die updation erfordern |
| shouldInflate | `boolean` |  Boolean – sollte aufblasen/nicht |
| callback | `function` |  mit unter Parameter:<br><br>\*@param {Boolean} Success true, wenn Update erfolgreich war; andernfalls false. false andernfalls |

**Gibt Folgendes zurück:**`void`

___

## <a name="response"></a>Antwort

<a id="canrespondtoformasync"></a>

###  <a name="canrespondtoformasync"></a>canRespondToFormAsync

▸ **canRespondToFormAsync**(Callback: *`function`*):`void`

Ruft ab, ob der aktuelle Benutzer auf das Formular reagieren kann.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} canRespond true, wenn der aktuelle Benutzer Antworten darf |

**Gibt Folgendes zurück:**`void`

___
<a id="getformasync"></a>

###  <a name="getformasync"></a>getFormAsync

▸ **getFormAsync**(Callback: *`function`*):`void`

Ruft das der Unterhaltungs Karte zugeordnete Form-Objekt ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASForm}-Formular kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getformstatusasync"></a>

###  <a name="getformstatusasync"></a>getFormStatusAsync

▸ **getFormStatusAsync**(Callback: *`function`*):`void`

Ruft den Status des Formulars ab, das der Unterhaltungs Karte zugeordnet ist.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} IsActive true, wenn das Formular noch nicht abgelaufen ist<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getmyformresponsesasync"></a>

###  <a name="getmyformresponsesasync"></a>getMyFormResponsesAsync

▸ **getMyFormResponsesAsync**(Callback: *`function`*, onlyCurrentResponse?: *`boolean`*):`void`

Ruft alle Antworten des aktuellen Benutzers anhand des Formulars ab.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| callback | `function` | - |  mit den folgenden Parametern:<br><br>\*@param {KASFormResponse\[\]} Antworten können im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |
| `Default value`onlyCurrentResponse | `boolean` | true |  Gilt für Antwort Aktionen, bei denen diese Methode nur die aktuelle Antwort im Kontext zurückgibt, legen Sie dieses Flag auf false fest, um stattdessen alle Antworten abzurufen. Der Standardwert ist true. |

**Gibt Folgendes zurück:**`void`

___
<a id="sumbitformresponse"></a>

###  <a name="sumbitformresponse"></a>sumbitFormResponse

▸ **sumbitFormResponse**(questionToAnswerMap: *`JSON`*, Antwort-Nr *`string`*:, IsEdit *`boolean`*:, showInChatCanvas *`boolean`*:, IsAnonymous *`boolean`*:):`void`

Sendet eine neue Antwort an das mit der Unterhaltungs Karte verknüpfte Formular. Dadurch wird der aktuelle Bildschirm verworfen.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var questionToAnswerMap = { "0": "answer" };
KASClient.Form.sumbitFormResponse(questionToAnswerMap, null, false, false, false);
```

#### <a name="note"></a>Hinweis

```
questionToAnswerMap is a map which has key as question Id and value as the response to the question
Say question of id 1 is of type "Text" which means it takes string as response. You should define it like {1: "<answer>"}
```

Der Antwort Wert für _[KASQuestionType](../enums/kasclient.kasquestiontype.md)_ sollte wie folgt lauten:
*   **Einzelne Auswahl** : Options-ID (Zeichenfolge). beispielsweise "1"
*   **MultiSelect** : Stringified-Array mit Options-IDs. beispielsweise JSON. stringify (\[1, 3\])
*   **Text** : String. beispielsweise "Dummy"
*   **Numerisch** : Number. beispielsweise 543
*   **Speicherort** : Stringified _[KASLocation](../classes/kasclient.kaslocation.md)_ -Objekt. beispielsweise JSON. stringify (Location. tojson ()) oder JSON. stringify ({"LG": 70,4, "lt": 18,6, "n": "Address"})
*   **DateTime** : Epoch Timestamp in millieseconds. beispielsweise 1550651524074
*   **Image** : Image Path. beispielsweise "file://imagePath.png"
*   **Attachmentlist** : Stringified Array of _[KASAttachment](../classes/kasclient.kasattachment.md)_ Objects. z.b. JSON. stringify (Attachments), Attachments is Array of KASAttachment
*   **Faxnummer** : Stringified _[KASPhoneNumber](../classes/kasclient.kasphonenumber.md)_ -Objekt. z.b. Son. stringify (Telefonnummer. tojson ()) oder JSON. stringify ({"CC": "+ 91", "PN": "98XXXXXXX6"})
*   **DateOnly** : Datumszeichenfolge (yyyy-mm-dd). beispielsweise "2019-04-17"

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  Frage-ID zur Antwort Zuordnung |
| Antwort-Nr | `string` |  auszufüllen, wenn es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt |
| isEdit | `boolean` |  Gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt. |
| showInChatCanvas | `boolean` |  Gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht. |
| isAnonymous | `boolean` |  kennzeichnet, ob die Antwort als anonym oder nicht registriert werden soll. |

**Gibt Folgendes zurück:**`void`

___
<a id="sumbitformresponsewithoutdismiss"></a>

###  <a name="sumbitformresponsewithoutdismiss"></a>sumbitFormResponseWithoutDismiss

▸ **sumbitFormResponseWithoutDismiss**(questionToAnswerMap: *`JSON`*, Antwort-Nr *`string`*:, IsEdit *`boolean`*:, showInChatCanvas *`boolean`*:, IsAnonymous *`boolean`*:):`void`

Sendet eine neue Antwort auf das Formular, das der Unterhaltungs Karte zugeordnet ist. Dadurch wird der aktuelle Bildschirm nicht verworfen.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var questionToAnswerMap = { "0": "answer" };
KASClient.Form.sumbitFormResponseWithoutDismiss(questionToAnswerMap, null, false, false, false);
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  Frage-ID für die Antwort Zuordnung (Weitere Informationen finden Sie unter _[sumbitFormResponse](kasclient.form.md#sumbitformresponse)_ ) |
| Antwort-Nr | `string` |  auszufüllen, wenn es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt |
| isEdit | `boolean` |  Gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung auf eine frühere handelt. |
| showInChatCanvas | `boolean` |  Gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht. |
| isAnonymous | `boolean` |  kennzeichnet, ob die Antwort als anonym oder nicht registriert werden soll. |

**Gibt Folgendes zurück:**`void`

___

## <a name="summary"></a>Zusammenfassung

<a id="formsummarycallback"></a>

###  <a name="formsummarycallback"></a>FormSummaryCallback

**Ƭ-FormSummaryCallback**:*`function`*

#### <a name="type-declaration"></a>Typdeklaration
▸ (flatSummary: *[KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)*, processedSummary: *[KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)*, Error: *`string`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| flatSummary | [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md) |
| processedSummary | [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md) |
| error | `string` |

**Gibt Folgendes zurück:**`void`

___
<a id="addcommentonform"></a>

###  <a name="addcommentonform"></a>addCommentOnForm

▸ **addCommentOnForm**(comment: *`string`*):`void`

Anforderungen zum Hinzufügen eines Kommentars zu einem Formular

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Kommentar | `string` |

**Gibt Folgendes zurück:**`void`

___
<a id="closeform"></a>

###  <a name="closeform"></a>closeForm

▸ **closeForm**():`void`

Schließt das der Karte zugeordnete Formular, es werden keine weiteren Antworten zugelassen.

**Gibt Folgendes zurück:**`void`

___
<a id="copyformandforward"></a>

###  <a name="copyformandforward"></a>copyFormAndForward

▸ **copyFormAndForward**():`void`

Startet die Unterhaltungs Auswahl, um eine Kopie des vorhandenen Formulars als neue Unterhaltungs Karte weiterzuleiten.

**Gibt Folgendes zurück:**`void`

___
<a id="executeactionfetchqueryasync"></a>

###  <a name="executeactionfetchqueryasync"></a>executeActionFetchQueryAsync

▸ **executeActionFetchQueryAsync**(Formular-Nr *`string`*:, fetchJsonQueryId *`string`*:, fetchJsonQueryParams *`JSON`*:, Callback *`function`*:):`void`

Ruft Aktionsinstanzen (oder Formular) Zeilen/Antworten mit FetchJson-Abfrage (SQL im JSON-Format) ab. Mit dieser API können Sie Rich-Abfragen für alle Zeilen ausführen und detaillierte oder Zusammenfassungen als Ergebnis erhalten. Diese Abfragen müssen in der appModel der Aktion erwähnt werden, damit Aktions Entwicklerberechtigungen für die Abfrageebene haben. Eine solche Abfrage kann nur mit der Abfrage-ID und ggf. den erforderlichen Platzhalterwerten ausgeführt werden.
#### <a name="note"></a>Hinweis

1.  Aktionsinstanz-Spalte/Frage-IDs werden als Attribut-IDs der FetchJson-Abfrage verwendet.
2.  Die Ausgabe wird eine Liste mit Zeilen sein, wobei jede Zeile Spalten-ID-Wert-Paare enthält.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
// AppModel questions: ResponderName (0) | City (1) | FavoriteMovie (2)
// Query (q123): SELECT question0 WHERE question1="@param1" AND question2="@param2"
// To fetch responders from "Mumbai" whose favorite movie is "Harry Potter"
var params = { "@param1": "Mumbai", "@param2": "Harry Potter"};
KASClient.Form.executeActionFetchQueryAsync("XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", "q123", params, function (result, error) {
   if (!error) {
       for (var i = 0; i < result.rows.length; i++) {
           var row = result.rows[i];
           console.log("Responder name: " + row["0"]);
       }
   }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| formId | `string` |  Aktionsinstanz-ID (oder Formular), deren Zeilen abgerufen werden müssen |
| fetchJsonQueryId | `string` |  FetchJson-Abfrage-ID (im Aktionspaket erwähnt) |
| fetchJsonQueryParams | `JSON` |  Zuordnung von Abfrageparameter Platzhaltern zu Werten |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {JSON} fetchJsonResult – das FetchJson-Abfrageergebnis<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="fetchformasync"></a>

###  <a name="fetchformasync"></a>fetchFormAsync

▸- **fetchFormAsync**(Formular- *`string`* Nr:, *`function`* Rückruf:):`void`

Ruft eine Aktionsinstanz (oder ein Formular) für die angegebene ID ab. Zunächst wird versucht, die Instanz lokal abzurufen, dann wird Sie vom Server als Fallback abgerufen.
#### <a name="note"></a>Hinweis

Eine Aktion kann Instanzen von sich selbst oder eine andere Aktion abrufen, die zu ihrer eigenen appGroup gehört.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| formId | `string` |  ID der Instanz, die abgerufen werden soll |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASForm} Form-Action-Instanz (oder Formular)<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="fetchforminfosasync"></a>

###  <a name="fetchforminfosasync"></a>fetchFormInfosAsync

▸ **fetchFormInfosAsync**(Request: *[KASFormInfoRequest](../classes/kasclient.kasforminforequest.md)*, Callback: *`function`*):`void`

Ruft die Aktionsinstanz (oder das Formular) Informationen eines Aktionspakets ab. Dies ist nützlich im Datenzugriff durch einen anderen Vorgang, bei dem eine Aktion die Zeilen/Antworten einer Instanz einer anderen Aktion abrufen kann – diese API dient zum Abrufen der zum Abrufen von Zeilen erforderlichen Instanz-ID.
#### <a name="note"></a>Hinweis

Eine Aktion kann Instanzen von sich selbst oder eine andere Aktion abrufen, die zu ihrer eigenen appGroup gehört.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var request = new KASClient.KASFormInfoRequest();
request.packageId = "some-package-id";
request.scopeId = "XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"; // Group id

KASClient.Form.fetchFormInfosAsync(request, function (response, error) {
   if (!error) {
       for (var i = 0; i < response.formInfos.length; i++) {
           var formInfo = response.formInfos[i]; // KASFormInfo
           console.log("Instance id: " + formInfo.id);
           console.log("Instance title: " + formInfo.title);
       }
   }
})
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Anfrage | [KASFormInfoRequest](../classes/kasclient.kasforminforequest.md) |  Anforderung mit API-Parametern |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASFormInfoResponse} Antwort-Antwort mit Aktionsinstanz (oder Formular) Infos<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="getactioninstancelocaldatacacheasync"></a>

###  <a name="getactioninstancelocaldatacacheasync"></a>getActionInstanceLocalDataCacheAsync

▸ **getActionInstanceLocalDataCacheAsync**(Callback: *`function`*):`void`

Ruft die ActionInstance-Eigenschaften aus dem lokalen Datencache ab, falls vorhanden. diese Eigenschaften werden auf der Ebene der Aktionsinstanz gespeichert. Daher werden die für die jeweilige Aktionsinstanz gespeicherten lokalen Daten von dieser API zurückgegeben.
#### <a name="note"></a>Hinweis

Diese API funktioniert nicht wie erwartet bei Verlaufsmeldungen.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.Form.getActionInstanceLocalDataCacheAsync(function (actionPackageProperties, error) {
     if (error == null && actionPackageProperties != null && actionPackageProperties.properties) {
          if (actionPackageProperties.properties.hasOwnProperty("prop1") {
             console.log(actionPackageProperties.properties["prop1"]);
          }
     }
 });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASActionProperties} aktioneigenschaften ActionInstance/Form-Eigenschaften<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="getactionpackagelocaldatacacheasync"></a>

###  <a name="getactionpackagelocaldatacacheasync"></a>getActionPackageLocalDataCacheAsync

▸ **getActionPackageLocalDataCacheAsync**(Callback: *`function`*):`void`

Ruft die Aktionspaket Eigenschaften aus dem lokalen Datencache ab, falls vorhanden. diese Eigenschaften werden auf der Ebene des Aktionspakets gespeichert. Daher erhalten alle Aktionsinstanzen, die aus diesem Aktionspaket erstellt werden, dieselben Daten.
#### <a name="note"></a>Hinweis

Diese API funktioniert nicht wie erwartet bei Verlaufsmeldungen.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.Form.getActionPackageLocalDataCacheAsync(function (actionPackageProperties, error) {
     if (error == null && actionPackageProperties != null && actionPackageProperties.properties) {
          if (actionPackageProperties.properties.hasOwnProperty("prop1") {
             console.log(actionPackageProperties.properties["prop1"]);
          }
     }
 });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASActionPackageProperties} actionPackageProperties-Aktionspaket Eigenschaften<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="getformreactionasync"></a>

###  <a name="getformreactionasync"></a>getFormReactionAsync

▸ **getFormReactionAsync**(Callback: *`function`*):`void`

Ruft die konsolidierte Reaktion (likes and comments) der Unterhaltungs Karte ab, die dem Formular zugeordnet ist.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASFormReaction} Reaktion kann im Fehlerfall NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getformsummaryasync"></a>

###  <a name="getformsummaryasync"></a>getFormSummaryAsync

▸ **getFormSummaryAsync**(mostUpdatedCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*, notifyCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*):`void`

Ruft flache Antworten aller Benutzer und verarbeitete Zusammenfassung aus allen dem Formular zugeordneten Antworten ab. Es werden zwei Rückrufe benötigt:
#### <a name="note"></a>Hinweis

Dies ist nützlich, wenn das Netzwerk schuppig/getrennt ist, sodass die Zusammenfassung sofort mit den vorhandenen Daten angezeigt werden kann, die wir haben, aber mit einer Option, Sie später bei der Ankunft der neuesten Daten vom Server zu aktualisieren! Keine der Rückrufe sind obligatorisch, wenn also 1st gleich NULL ist, kann diese Methode verwendet werden, um die Zusammenfassung immer vom Server abzurufen, und wenn 2nd gleich NULL ist, kann dies verwendet werden, um die Zusammenfassung immer aus der lokalen Datenbank abzurufen!

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.Form.getFormSummaryAsync(
   // Data fetched from database
   function (flatSummary, processedSummary, error) {
      if (error != null) {
      }
   },
   // Data fetched from server
   function (flatSummary, processedSummary, error) {
      if (error != null) {
      }
   })
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| mostUpdatedCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  , um sofort die aktuellste Zusammenfassung aus der lokalen Datenbank abzurufen. Es hat folgende Parameter:<br><br>\*@param {KASFormFlatSummary} flatSummary kann im Falle eines Fehlers NULL sein<br><br>\*@param {KASFormProcessedSummary} processedSummary kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |
| notifyCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  So erhalten Sie eine Benachrichtigung mit der neuesten Zusammenfassung, die vom Server abgerufen wurde. Es hat folgende Parameter:<br><br>\*@param {KASFormFlatSummary} flatSummary kann im Falle eines Fehlers NULL sein<br><br>\*@param {KASFormProcessedSummary} processedSummary kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getformurlasync"></a>

###  <a name="getformurlasync"></a>getFormURLAsync

▸ **getFormURLAsync**(Callback: *`function`*):`void`

Ruft die Datei-URL vom Server ab, der dem Formular zugeordnete flache Antworten enthält.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {String} URL kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getformusercapabilitiesasync"></a>

###  <a name="getformusercapabilitiesasync"></a>getFormUserCapabilitiesAsync

▸ **getFormUserCapabilitiesAsync**(Callback: *`function`*):`void`

Ruft Formular Berechtigungen ab.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.Form.getFormUserCapabilitiesAsync(function (permissions, error) {
    if(!error) {
        canRespond = permissions.canRespond;
        canSendReminder = permissions.canSendReminder;
        shouldSeeSummary = permissions.shouldSeeSummary;
    }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASFormUserCapabilities}-Berechtigungen<br><br>\*@param {string} Error Error String im Fall eines Fehlers; andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="issubscribed"></a>

###  <a name="issubscribed"></a>isSubscribed

▸ **** IsSubscribed (Rückruf: *`function`*):`void`

Ruft ab, ob der aktuelle Benutzer Abonnent ist oder nicht.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} IsSubscribed true, wenn der Abonnent des aktuellen Benutzers |

**Gibt Folgendes zurück:**`void`

___
<a id="likeform"></a>

###  <a name="likeform"></a>likeForm

▸ **likeForm**():`void`

Anforderungen zum Hinzufügen einer like-Anzahl zu einem Formular kann die Anzahl verringern, wenn der aktuelle Benutzer das Formular bereits gewünscht hat

**Gibt Folgendes zurück:**`void`

___
<a id="sendreminderstorespond"></a>

###  <a name="sendreminderstorespond"></a>sendRemindersToRespond

▸ **sendRemindersToRespond**():`void`

Sendet eine Erinnerung (eine neue Gesprächs Karte) für die vorhandene Karte.

**Gibt Folgendes zurück:**`void`

___
<a id="shareformurl"></a>

###  <a name="shareformurl"></a>shareFormURL

▸ **shareFormURL**(URL: *`string`*):`void`

Freigabe der vom Server abgerufenen Ergebnis-URL – Start des systemeigenen Freigabe Bildschirms für die Formular-URL

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| url | `string` |  gemeinsam genutzt werden |

**Gibt Folgendes zurück:**`void`

___
<a id="showallreactions"></a>

###  <a name="showallreactions"></a>showAllReactions

▸ **showAllReactions**(showComments?: *`boolean`*):`void`

Zeigt alle Reaktions Schirme (likes und Kommentare) für das Formular an.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`showComments | `boolean` | true |  true, wenn Kommentare auch angezeigt werden müssen; andernfalls false. false andernfalls |

**Gibt Folgendes zurück:**`void`

___
<a id="updateactioninstancelocaldatacacheasync"></a>

###  <a name="updateactioninstancelocaldatacacheasync"></a>updateActionInstanceLocalDataCacheAsync

▸ **updateActionInstanceLocalDataCacheAsync**(aktioneigenschaften: *[KASActionProperties](../classes/kasclient.kasactionproperties.md)*, Callback: *`function`*):`void`

Aktualisiert/speichert die angegebenen ActionInstance-Eigenschaften im lokalen Datencache. diese Eigenschaften werden auf der Ebene der Aktionsinstanz gespeichert. Jede Aktionsinstanz kann also einige lokale Daten im Cache speichern, und auf diese wird nur von dieser bestimmten Instanz zugegriffen.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var actionPackageProperties = KASClient.KASActionPackageProperties.fromJSON(JSON.parse("{}"));
actionPackageProperties.properties = JSON.parse("{}");
actionPackageProperties.properties[prop1] = value1;
KASClient.Form.updateActionInstanceLocalDataCacheAsync(actionPackageProperties, function(success, error) {
     if(!error) {
     }
});
```
#### <a name="note"></a>Hinweis

Diese API funktioniert nicht wie erwartet bei Verlaufsmeldungen.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| aktioneigenschaften | [KASActionProperties](../classes/kasclient.kasactionproperties.md) |  ActionInstance/Formulareigenschaften werden aktualisiert/gespeichert |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} Success gibt an, ob das Update erfolgreich ist oder nicht<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="updateactionpackagelocaldatacacheasync"></a>

###  <a name="updateactionpackagelocaldatacacheasync"></a>updateActionPackageLocalDataCacheAsync

▸ **updateActionPackageLocalDataCacheAsync**(actionPackageProperties: *[KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md)*, Callback: *`function`*):`void`

Aktualisiert/speichert die Eigenschaften des angegebenen Aktionspakets im lokalen Datencache. diese Eigenschaften werden auf der Ebene des Aktionspakets gespeichert. Die Daten werden also für alle Aktionsinstanzen freigegeben, die aus diesem Aktionspaket erstellt wurden.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var actionPackageProperties = KASClient.KASActionPackageProperties.fromJSON(JSON.parse("{}"));
actionPackageProperties.properties = JSON.parse("{}");
actionPackageProperties.properties[prop1] = value1;
KASClient.Form.updateActionPackageLocalDataCacheAsync(actionPackageProperties, function(success, error) {
     if(!error) {
     }
});
```
#### <a name="note"></a>Hinweis

Diese API funktioniert nicht wie erwartet bei Verlaufsmeldungen.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionPackageProperties | [KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md) |  Eigenschaften des Aktionspakets, die aktualisiert/gespeichert werden sollen |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} Success gibt an, ob das Update erfolgreich ist oder nicht<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="updateformpropertiesasync"></a>

###  <a name="updateformpropertiesasync"></a>updateFormPropertiesAsync

▸ **updateFormPropertiesAsync**(propertyUpdates: * [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md)[]*, notifyUsers: * `string`[]*, notificationMessage: *`string`*, Callback: *`function`*, shouldSendToSubscribers?: *`boolean`*):`void`

Bereitstelleneiner Anforderung zum Aktualisieren der dem Formular zugeordneten Eigenschaften

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var updateProperties = [];
var currentFormProperty = new KASClient.KASFormProperty(); // type: KASFormProperty
currentFormProperty.name = "<name>";
currentFormProperty.value = "<value>";
var property1ToAdd = KASClient.KASFormPropertyUpdateFactory.addProperty(currentFormProperty); //use updateValueInProperty in case of existing form property
updateProperties.push(property1ToAdd);
var notifyUsersList = [];
// notifyUsersList.push(<"uid1">);
// notifyUsersList.push("<uid2>");
KASClient.Form.updateFormPropertiesAsync(updateProperties, notifyUsersList, notificationMessage, function (success) {
  if (success) {
  }
});
```

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| propertyUpdates | [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md) [] | - |  ein Array mit allen Aktualisierungs Infos, die ausgeführt werden müssen, Update Infos können mit KASFormPropertyUpdateFactory erstellt werden. |
| notifyUsers | `string`[] | - |  Senden von Push-Benachrichtigungen an diese Benutzer-IDs zu diesem Update |
| notificationMessage | `string` | - |  Push-Benachrichtigungsnachricht |
| callback | `function` | - |  mit den folgenden Parametern:<br><br>\*@param {Boolean} Success gibt an, ob das Update erfolgreich ist oder nicht |
| `Default value`shouldSendToSubscribers | `boolean` | false |  Optionales Feld (Standardwert ist false) nur in öffentlichen Gruppen anwendbar. Wenn dieser Wert auf true festgelegt ist, werden die Eigenschaftenaktualisierungen auch Abonnenten in einer öffentlichen Gruppe erreichen. |

**Gibt Folgendes zurück:**`void`

___

