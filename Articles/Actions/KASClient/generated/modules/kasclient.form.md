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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASForm}-Formular kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="submitformrequestv2"></a>

###  <a name="submitformrequestv2"></a>submitFormRequestV2

▸ **submitFormRequestV2**(Form: *[KASForm](../classes/kasclient.kasform.md)*, shouldDismiss?: *`boolean`*, shouldSendToSubscribers?: *`boolean`*):`void`

Übermittelt das neu erstellte Formular als Anforderung. Dies führt zu einer neuen Unterhaltungs Karte

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| Formular | [KASForm](../classes/kasclient.kasform.md) | - |  \- |
| `Default value`shouldDismiss | `boolean` | false |  true, wenn das Formular bei der Übermittlung zurückgewiesen werden muss; false andernfalls |
| `Default value`shouldSendToSubscribers | `boolean` | true |

**Gibt Folgendes zurück:**`void`

___

<a id="submitformrequestwithoutdismiss"></a>

###  <a name="submitformrequestwithoutdismiss"></a>submitFormRequestWithoutDismiss

▸ **submitFormRequestWithoutDismiss**(Form: *[KASForm](../classes/kasclient.kasform.md)*, shouldInflate: *`boolean`*):`void`

Übermittelt das neu erstellte Formular als Anforderung. Dies führt zu einer neuen Unterhaltungs Karte

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

Verwenden Sie, um Änderungen an Formularfeldern wie Titel, Beschreibung und Einstellungen vorzunehmen.

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
| callback | `function` |  unter params:<br><br>\*@param {Boolean} Success true, wenn Update erfolgreich war; false andernfalls |

**Gibt Folgendes zurück:**`void`

___

## <a name="response"></a>Antwort

<a id="canrespondtoformasync"></a>

###  <a name="canrespondtoformasync"></a>canRespondToFormAsync

▸ **canRespondToFormAsync**(Callback: *`function`*):`void`

Ruft ab, ob der aktuelle Benutzer auf das Formularantworten kann.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} canRespond true, wenn der aktuelle Benutzer Antworten darf |

**Gibt Folgendes zurück:**`void`

___

<a id="getformasync"></a>

###  <a name="getformasync"></a>getFormAsync

▸ **getFormAsync**(Callback: *`function`*):`void`

Ruft das Formularobjekt ab, das der Unterhaltungs Karte zugeordnet ist.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASForm}-Formular kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getformstatusasync"></a>

###  <a name="getformstatusasync"></a>getFormStatusAsync

▸ **getFormStatusAsync**(Callback: *`function`*):`void`

Ruft den Status des Formulars ab, das der Unterhaltungs Karte zugeordnet ist.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} IsActive true, wenn das Formular noch nicht abgelaufen ist<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getmyformresponsesasync"></a>

###  <a name="getmyformresponsesasync"></a>getMyFormResponsesAsync

▸ **getMyFormResponsesAsync**(Callback: *`function`*, onlyCurrentResponse?: *`boolean`*):`void`

Ruft alle Antworten des aktuellen Benutzers anhand des Formulars ab.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| callback | `function` | - |  mit folgenden Parametern:<br><br>\*@param {KASFormResponse\[\]}-antworten können im fehlerfall null sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |
| `Default value`onlyCurrentResponse | `boolean` | true |  Gilt für Antwort Aktionen, bei denen diese Methode nur die aktuelle Antwort im Kontext zurückgibt, legen Sie dieses Flag auf false fest, um stattdessen alle Antworten abzurufen. Der Standardwert ist true. |

**Gibt Folgendes zurück:**`void`

___

<a id="sumbitformresponse"></a>

###  <a name="sumbitformresponse"></a>sumbitFormResponse

▸ **sumbitFormResponse**(questionToAnswerMap: *`JSON`*, Response-Nr *`string`*.:, IsEdit: *`boolean`*, *`boolean`* showInChatCanvas:, IsAnonymous: *`boolean`*):`void`

Übermittelt eine neue Antwort auf das Formular, das der Unterhaltungs Karte zugeordnet ist. Dadurch wird der aktuelle Bildschirm ausgeblendet.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var questionToAnswerMap = JSON.parse("{}");
questionToAnswerMap[0] = answer;
KASClient.Form.sumbitFormResponse(questionToAnswerMap,
   null,
   false,
   false,
   false);
```

#### <a name="note"></a>Hinweis

```
questionToAnswerMap is a map which has key as question Id and value as the response to the question
Say question is of type "text" which means it takes text as response. You should define it like
var question = new KASClient.KASQuestion();
question.id = 1;
question.type = KASClient.KASQuestionType.Text;
question.title = "Enter your name";
This KASQuestion is to be added to form.questions[] array.
Now questionToAnswerMap for this should look like this {1: "<answer>"}
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  Frage-ID zur Antwort Zuordnung |
| Antwort-Nr. | `string` |  ausgefüllt werden, wenn die aktuelle Antwort eine Bearbeitung/Aktualisierung einer vorherigen ist |
| isEdit | `boolean` |  Gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung zu einem vorherigen handelt. |
| showInChatCanvas | `boolean` |  Gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht. |
| isAnonymous | `boolean` |  Gibt an, ob die Antwort als anonym registriert werden soll oder nicht. |

**Gibt Folgendes zurück:**`void`

___

<a id="sumbitformresponsewithoutdismiss"></a>

###  <a name="sumbitformresponsewithoutdismiss"></a>sumbitFormResponseWithoutDismiss

▸ **sumbitFormResponseWithoutDismiss**(questionToAnswerMap: *`JSON`*, Response-Nr *`string`*.:, IsEdit: *`boolean`*, *`boolean`* showInChatCanvas:, IsAnonymous: *`boolean`*):`void`

Übermittelt eine neue Antwort auf das Formular, das der Unterhaltungs Karte zugeordnet ist.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var questionToAnswerMap = JSON.parse("{}");
questionToAnswerMap[0] = answer;
KASClient.Form.sumbitFormResponseWithoutDismiss(questionToAnswerMap,
   null,
   false,
   false,
   false);
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| questionToAnswerMap | `JSON` |  Frage-ID zur Antwort Zuordnung |
| Antwort-Nr. | `string` |  ausgefüllt werden, wenn die aktuelle Antwort eine Bearbeitung/Aktualisierung einer vorherigen ist |
| isEdit | `boolean` |  Gibt an, ob es sich bei der aktuellen Antwort um eine Bearbeitung/Aktualisierung zu einem vorherigen handelt. |
| showInChatCanvas | `boolean` |  Gibt an, ob für diese Antwort eine separate Chat Karte erstellt werden muss oder nicht. |
| isAnonymous | `boolean` |  Gibt an, ob die Antwort als anonym registriert werden soll oder nicht. |

**Gibt Folgendes zurück:**`void`

___

## <a name="summary"></a>Zusammenfassung

<a id="formsummarycallback"></a>

###  <a name="formsummarycallback"></a>FormSummaryCallback

**Ƭ FormSummaryCallback**:*`function`*

#### <a name="type-declaration"></a>Typdeklaration
▸ (flatSummary: *[KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)*, ProcessedSummary: *[KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)*, Error: *`string`*):`void`

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

Schließt das der Karte zugeordnete Formular, es werden jedoch keine weiteren Antworten zugelassen.

**Gibt Folgendes zurück:**`void`

___

<a id="copyformandforward"></a>

###  <a name="copyformandforward"></a>copyFormAndForward

▸ **copyFormAndForward**():`void`

Startet die Unterhaltungs Auswahl, um eine Kopie des vorhandenen Formulars als neue Unterhaltungs Karte weiterzuleiten.

**Gibt Folgendes zurück:**`void`

___

<a id="getactioninstancelocaldatacacheasync"></a>

###  <a name="getactioninstancelocaldatacacheasync"></a>getActionInstanceLocalDataCacheAsync

▸ **getActionInstanceLocalDataCacheAsync**(Callback: *`function`*):`void`

Ruft die ActionInstance-Eigenschaften aus dem lokalen Datencache ab, sofern vorhanden, dass diese Eigenschaften auf der Ebene der Aktionsinstanz gespeichert werden. Daher werden die für die jeweilige Aktionsinstanz gespeicherten lokalen Daten von dieser API zurückgegeben.
#### <a name="note"></a>Hinweis

Diese API funktioniert bei historischen Nachrichten nicht erwartungsgemäß.

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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASActionProperties} Aktioneigenschaften-ActionInstance/-Formulareigenschaften<br><br>\*@param {String}-Fehler-JSON-Zeichenfolge für das KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___

<a id="getactionpackagelocaldatacacheasync"></a>

###  <a name="getactionpackagelocaldatacacheasync"></a>getActionPackageLocalDataCacheAsync

▸ **getActionPackageLocalDataCacheAsync**(Callback: *`function`*):`void`

Ruft die Aktionspaket Eigenschaften aus dem lokalen Datencache ab, sofern vorhanden, dass diese Eigenschaften auf der Ebene des Aktionspakets gespeichert werden. Daher erhalten alle Aktionsinstanzen, die aus diesem Aktionspaket erstellt wurden, dieselben Daten.
#### <a name="note"></a>Hinweis

Diese API funktioniert bei historischen Nachrichten nicht erwartungsgemäß.

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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASActionPackageProperties} actionPackageProperties-Aktionspaket Eigenschaften<br><br>\*@param {String}-Fehler-JSON-Zeichenfolge für das KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___

<a id="getformreactionasync"></a>

###  <a name="getformreactionasync"></a>getFormReactionAsync

▸ **getFormReactionAsync**(Callback: *`function`*):`void`

Ruft die konsolidierte Reaktion (likes und comments) der Unterhaltungs Karte ab, die dem Formular zugeordnet ist.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASFormReaction}-Reaktion kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getformsummaryasync"></a>

###  <a name="getformsummaryasync"></a>getFormSummaryAsync

▸ **getFormSummaryAsync**(MostUpdatedCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*, notifyCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*):`void`

Ruft flache Antworten aller Benutzer ab und verarbeitet eine Zusammenfassung aller Antworten, die dem Formular zugeordnet sind. Sie erfordert zwei Rückrufe:
#### <a name="note"></a>Hinweis

Dies ist nützlich, wenn das Netzwerk flockig/getrennt ist, sodass die Zusammenfassung sofort mit den aktuellen Daten angezeigt werden kann, die wir haben, aber mit der Option, Sie später beim Eintreffen der neuesten Daten vom Server zu aktualisieren. Keines der Rückrufe ist obligatorisch, wenn 1 also NULL ist, kann diese Methode verwendet werden, um eine Zusammenfassung immer vom Server abzurufen, und wenn 2nd NULL ist, kann dies verwendet werden, um eine Zusammenfassung aus der lokalen Datenbank abzurufen.

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
| mostUpdatedCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  , um sofort die aktuellste Zusammenfassung aus der lokalen Datenbank abzurufen. Sie hat folgende Parameter:<br><br>\*@param {KASFormFlatSummary} flatSummary kann im Fehlerfall NULL sein<br><br>\*@param {KASFormProcessedSummary} processedSummary kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |
| notifyCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  um mit der neuesten Zusammenfassung benachrichtigt zu werden, die vom Server abgerufen wurde. Sie hat folgende Parameter:<br><br>\*@param {KASFormFlatSummary} flatSummary kann im Fehlerfall NULL sein<br><br>\*@param {KASFormProcessedSummary} processedSummary kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getformurlasync"></a>

###  <a name="getformurlasync"></a>getFormURLAsync

▸ **getFormURLAsync**(Callback: *`function`*):`void`

Ruft die Datei-URL vom Server ab, die flache Antworten enthält, die dem Formular zugeordnet sind.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {String}-URL kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASFormUserCapabilities}-Berechtigungen<br><br>\*@param {string} Error Error String im Fehlerfall; andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="issubscribed"></a>

###  <a name="issubscribed"></a>isSubscribed

▸ **** IsSubscribed (Callback: *`function`*):`void`

Ruft ab, ob der aktuelle Benutzer Abonnent ist oder nicht

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} isSubscribed true, wenn der aktuelle Benutzer Abonnent |

**Gibt Folgendes zurück:**`void`

___

<a id="likeform"></a>

###  <a name="likeform"></a>likeForm

▸ **likeForm**():`void`

Anforderungen zum Hinzufügen einer like-Anzahl zu einem Formular kann die Anzahl verringert werden, wenn der aktuelle Benutzer das Formular bereits gemocht hat.

**Gibt Folgendes zurück:**`void`

___

<a id="sendreminderstorespond"></a>

###  <a name="sendreminderstorespond"></a>sendRemindersToRespond

▸ **sendRemindersToRespond**():`void`

Sendet eine Erinnerung (eine neue Unterhaltungs Karte) an die vorhandene Karte

**Gibt Folgendes zurück:**`void`

___

<a id="shareformurl"></a>

###  <a name="shareformurl"></a>shareFormURL

▸ **shareFormURL**(URL: *`string`*):`void`

Freigeben der vom Server abgerufenen Ergebnis-URL-startet systemeigener Freigabe Bildschirm für die Formular-URL

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| url | `string` |  freigegeben werden |

**Gibt Folgendes zurück:**`void`

___

<a id="showallreactions"></a>

###  <a name="showallreactions"></a>showAllReactions

▸ **showAllReactions**(showComments?: *`boolean`*):`void`

Zeigt den gesamten Reaktions Bildschirm (likes und comments) für das Formular an.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`showComments | `boolean` | true |  true, wenn Kommentare auch angezeigt werden müssen; false andernfalls |

**Gibt Folgendes zurück:**`void`

___

<a id="updateactioninstancelocaldatacacheasync"></a>

###  <a name="updateactioninstancelocaldatacacheasync"></a>updateActionInstanceLocalDataCacheAsync

▸ **updateActionInstanceLocalDataCacheAsync**(Aktioneigenschaften: *[KASActionProperties](../classes/kasclient.kasactionproperties.md)*, Callback: *`function`*):`void`

Aktualisiert/speichert die angegebenen ActionInstance-Eigenschaften im lokalen Datencache diese Eigenschaften werden auf der Ebene der Aktionsinstanz gespeichert. Jede Aktionsinstanz kann also einige lokale Daten im Cache speichern und nur von dieser bestimmten Instanz aus zugänglich sein.

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

Diese API funktioniert bei historischen Nachrichten nicht erwartungsgemäß.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Aktioneigenschaften | [KASActionProperties](../classes/kasclient.kasactionproperties.md) |  ActionInstance/Formulareigenschaften, die aktualisiert/gespeichert werden sollen |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} Success gibt an, ob das Update erfolgreich ist oder nicht<br><br>\*@param {String}-Fehler-JSON-Zeichenfolge für das KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___

<a id="updateactionpackagelocaldatacacheasync"></a>

###  <a name="updateactionpackagelocaldatacacheasync"></a>updateActionPackageLocalDataCacheAsync

▸ **updateActionPackageLocalDataCacheAsync**(ActionPackageProperties: *[KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md)*, Callback: *`function`*):`void`

Aktualisiert/speichert die angegebenen Eigenschaften des Aktionspakets im lokalen Datencache diese Eigenschaften werden auf der Ebene des Aktionspakets gespeichert. Daher werden die Daten für alle Aktionsinstanzen freigegeben, die aus diesem Aktionspaket erstellt wurden.

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

Diese API funktioniert bei historischen Nachrichten nicht erwartungsgemäß.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionPackageProperties | [KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md) |  Aktionspaket Eigenschaften, die aktualisiert/gespeichert werden sollen |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} Success gibt an, ob das Update erfolgreich ist oder nicht<br><br>\*@param {String}-Fehler-JSON-Zeichenfolge für das KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___

<a id="updateformpropertiesasync"></a>

###  <a name="updateformpropertiesasync"></a>updateFormPropertiesAsync

▸ **updateFormPropertiesAsync**(propertyUpdates: * [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md)[]*, notifyUsers: * `string`[]*, notificationMessage: *`string`*, Callback: *`function`*):`void`

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

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| propertyUpdates | [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md) [] |  ein Array aller Update-Informationen, die benötigt werden, um durchgeführt werden, Update-Infos können erstellt werden, mit KASFormPropertyUpdateFactory |
| notifyUsers | `string`[] |  Senden von Push-Benachrichtigungen an diese Benutzer-IDs zu diesem Update |
| notificationMessage | `string` |  Push-Benachrichtigung |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} Success gibt an, ob das Update erfolgreich ist oder nicht |

**Gibt Folgendes zurück:**`void`

___

