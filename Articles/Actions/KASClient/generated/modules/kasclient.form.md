---
ms.openlocfilehash: 5e5778d41163788bd93609d0f41019e68b8d6f22
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728150"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [Formular](../modules/kasclient.form.md)

# <a name="module-form"></a>Modul: Formular

## <a name="index"></a>Index 

### <a name="creation"></a>Erstellen

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

## <a name="creation"></a>Erstellen

<a id="initformasync"></a>

###  <a name="initformasync"></a>initFormAsync

▸ **InitFormAsync**(Rückruf: *`function`*):`void`

Initialisiert und gibt ein leeres Formular-Objekt auf der Standard-Datei in das Paket vorhanden basieren

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASForm} @param Formular kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="submitformrequestv2"></a>

###  <a name="submitformrequestv2"></a>submitFormRequestV2

▸ **submitFormRequestV2**(Formular: *[KASForm](../classes/kasclient.kasform.md)*, ShouldDismiss?: *`boolean`*, ShouldSendToSubscribers?: *`boolean`*):`void`

Sendet das neu erstellte Formular als Anforderung. Dies führt zu eine neuen Unterhaltung Karte

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| Formular | [KASForm](../classes/kasclient.kasform.md) | - |  \- |
| `Default value`shouldDismiss | `boolean` | false |  True, wenn das Formular muss beim Absenden geschlossen werden; False, andernfalls |
| `Default value`shouldSendToSubscribers | `boolean` | true |

**Gibt:**`void`

___

<a id="submitformrequestwithoutdismiss"></a>

###  <a name="submitformrequestwithoutdismiss"></a>submitFormRequestWithoutDismiss

▸ **SubmitFormRequestWithoutDismiss**(Formular: *[KASForm](../classes/kasclient.kasform.md)*, ShouldInflate: *`boolean`*):`void`

Sendet das neu erstellte Formular als Anforderung. Dies führt zu eine neuen Unterhaltung Karte

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Formular | [KASForm](../classes/kasclient.kasform.md) |  \- |
| shouldInflate | `boolean` |  Boolean – sollten vergrößert werden soll oder nicht |

**Gibt:**`void`

___

<a id="updateform"></a>

###  <a name="updateform"></a>updateForm

▸ **UpdateForm**(Felder: *`string`*, ShouldInflate: *`boolean`*, Rückruf: *`function`*):`void`

Verwenden Sie für die Änderung in Formularfeldern wie Titel, Beschreibung und Einstellungen.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| fields | `string` |  JSON-Zeichenfolge der Felder, die aktualisiert werden müssen |
| shouldInflate | `boolean` |  Boolean – sollten vergrößert werden soll oder nicht |
| callback | `function` |  mit unten Params:<br><br>\*{Boolean} @param Erfolg true zurück, wenn Aktualisierung erfolgreich abgeschlossen wurde; False, andernfalls |

**Gibt:**`void`

___

## <a name="response"></a>Antwort

<a id="canrespondtoformasync"></a>

###  <a name="canrespondtoformasync"></a>canRespondToFormAsync

▸ **CanRespondToFormAsync**(Rückruf: *`function`*):`void`

Ruft ab, ob der aktuelle Benutzer beantwortet werden können

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param CanRespond True, wenn der aktuelle Benutzer reagieren |

**Gibt:**`void`

___

<a id="getformasync"></a>

###  <a name="getformasync"></a>getFormAsync

▸ **GetFormAsync**(Rückruf: *`function`*):`void`

Dient zum Abrufen der Unterhaltung Karte zugeordneten Form-Objekts

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASForm} @param Formular kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getformstatusasync"></a>

###  <a name="getformstatusasync"></a>getFormStatusAsync

▸ **GetFormStatusAsync**(Rückruf: *`function`*):`void`

Ruft den Status des Formulars der Unterhaltung Karte zugeordnete ab

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param IsActive true zurück, wenn das Formular noch nicht abgelaufen ist<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getmyformresponsesasync"></a>

###  <a name="getmyformresponsesasync"></a>getMyFormResponsesAsync

▸ **GetMyFormResponsesAsync**(Rückruf: *`function`*, OnlyCurrentResponse?: *`boolean`*):`void`

Dient zum Abrufen aller Antworten des aktuellen Benutzers für das Formular

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| callback | `function` | - |  mit folgenden Parameter:<br><br>\*@param {KASFormResponse\[\]} Antworten können bei einem Fehler null sein<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |
| `Default value`onlyCurrentResponse | `boolean` | true |  Anwendbar für Antwortaktionen, in dem diese Methode nur die aktuelle Antwort im Kontext, gibt, legen Sie dieses Flag auf "false", um alle Antworten stattdessen abzurufen. Der Standardwert ist true |

**Gibt:**`void`

___

<a id="sumbitformresponse"></a>

###  <a name="sumbitformresponse"></a>sumbitFormResponse

▸ **SumbitFormResponse**(QuestionToAnswerMap: *`JSON`*, ResponseId: *`string`*, IsEdit: *`boolean`*, ShowInChatCanvas: *`boolean`*, IsAnonymous: *`boolean`*):`void`

Sendet eine neue Antwort für das Formular, das die Unterhaltung Karte zugeordnet wird dies zu den aktuellen Bildschirm schließen

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| questionToAnswerMap | `JSON` |  Frage Id Zuordnung zu beantworten. |
| responseId | `string` |  Wenn die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist gefüllt werden soll |
| isEdit | `boolean` |  Gibt an, ob die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist |
| showInChatCanvas | `boolean` |  Gibt an, ob eine separate Chat Karte für diese Antwort oder nicht erstellt werden soll |
| isAnonymous | `boolean` |  Gibt an, ob die Antwort als anonym erfasst werden sollen |

**Gibt:**`void`

___

<a id="sumbitformresponsewithoutdismiss"></a>

###  <a name="sumbitformresponsewithoutdismiss"></a>sumbitFormResponseWithoutDismiss

▸ **SumbitFormResponseWithoutDismiss**(QuestionToAnswerMap: *`JSON`*, ResponseId: *`string`*, IsEdit: *`boolean`*, ShowInChatCanvas: *`boolean`*, IsAnonymous: *`boolean`*):`void`

Sendet eine neue Antwort für das Formular, das die Unterhaltung Karte zugeordnet wird nicht dadurch den aktuellen Bildschirm schließen

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| questionToAnswerMap | `JSON` |  Frage Id Zuordnung zu beantworten. |
| responseId | `string` |  Wenn die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist gefüllt werden soll |
| isEdit | `boolean` |  Gibt an, ob die aktuelle Antwort ein bearbeiten/Update mit einer früheren ist |
| showInChatCanvas | `boolean` |  Gibt an, ob eine separate Chat Karte für diese Antwort oder nicht erstellt werden soll |
| isAnonymous | `boolean` |  Gibt an, ob die Antwort als anonym erfasst werden sollen |

**Gibt:**`void`

___

## <a name="summary"></a>Zusammenfassung

<a id="formsummarycallback"></a>

###  <a name="formsummarycallback"></a>FormSummaryCallback

**Ƭ FormSummaryCallback**:*`function`*

#### <a name="type-declaration"></a>Typdeklaration
▸ (FlatSummary: *[KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)*, ProcessedSummary: *[KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)*, Fehler: *`string`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| flatSummary | [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md) |
| processedSummary | [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md) |
| error | `string` |

**Gibt:**`void`

___

<a id="addcommentonform"></a>

###  <a name="addcommentonform"></a>addCommentOnForm

▸ **AddCommentOnForm**(Kommentar: *`string`*):`void`

Anforderungen an einen Kommentar zu einem Formular hinzufügen

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Kommentar | `string` |

**Gibt:**`void`

___

<a id="closeform"></a>

###  <a name="closeform"></a>closeForm

▸ **CloseForm**():`void`

Schließt das Formular der Karte zugeordnete keine Antworten Weitere zulässig

**Gibt:**`void`

___

<a id="copyformandforward"></a>

###  <a name="copyformandforward"></a>copyFormAndForward

▸ **CopyFormAndForward**():`void`

Startet die Unterhaltung Auswahl um eine Kopie des Formulars als eine neue Unterhaltung Karte weiterzuleiten

**Gibt:**`void`

___

<a id="getactioninstancelocaldatacacheasync"></a>

###  <a name="getactioninstancelocaldatacacheasync"></a>getActionInstanceLocalDataCacheAsync

▸ **GetActionInstanceLocalDataCacheAsync**(Rückruf: *`function`*):`void`

Level-Instanz abgerufen, die ActionInstance Eigenschaften aus dem lokalen Datencache, sofern diese Eigenschaften vorhanden, eine Aktion gespeichert werden. Damit die lokalen Daten gespeichert, die für die jeweilige Aktion, die Instanz von dieser API zurückgegeben werden.
#### <a name="note"></a>Hinweis

Diese API funktioniert nicht wie erwartet im Fall eines WAN-älterer Nachrichten.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASActionProperties} @param ActionProperties ActionInstance/Formulareigenschaften<br><br>\*{Zeichenfolge} @param Json Fehlerzeichenfolge für das KASError-Objekt, das mit Fehlercode und/oder Beschreibung. |

**Gibt:**`void`

___

<a id="getactionpackagelocaldatacacheasync"></a>

###  <a name="getactionpackagelocaldatacacheasync"></a>getActionPackageLocalDataCacheAsync

▸ **GetActionPackageLocalDataCacheAsync**(Rückruf: *`function`*):`void`

Ruft die Aktion Paketeigenschaften aus dem lokalen Datencache, sofern diese Eigenschaften vorhanden sind auf der Ebene der Aktion Paket gespeichert werden. Damit alle Action-Instanzen aus diesem Paket Aktion erstellt erhält die gleichen Daten.
#### <a name="note"></a>Hinweis

Diese API funktioniert nicht wie erwartet im Fall eines WAN-älterer Nachrichten.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASActionPackageProperties} @param ActionPackageProperties Aktion-Paket-Eigenschaften<br><br>\*{Zeichenfolge} @param Json Fehlerzeichenfolge für das KASError-Objekt, das mit Fehlercode und/oder Beschreibung. |

**Gibt:**`void`

___

<a id="getformreactionasync"></a>

###  <a name="getformreactionasync"></a>getFormReactionAsync

▸ **GetFormReactionAsync**(Rückruf: *`function`*):`void`

Dient zum Abrufen der konsolidierten Reaktion der dem Formular zugeordneten Unterhaltung Karte ("gefällt mir" und Kommentare)

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASFormReaction} @param Reaktion kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getformsummaryasync"></a>

###  <a name="getformsummaryasync"></a>getFormSummaryAsync

▸ **GetFormSummaryAsync**(MostUpdatedCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*, NotifyCallback: *[FormSummaryCallback](kasclient.form.md#formsummarycallback)*):`void`

Ruft in flache Antworten von allen Benutzern und Übersicht über alle dem Formular zugeordneten Antworten verarbeitet. Es erfordert zwei Rückrufe:
#### <a name="note"></a>Hinweis

Dies ist nützlich, wenn das Netzwerk arbeitende/getrennt ist, damit diese Zusammenfassung sofort angezeigt werden kann, mit der präsentieren von Daten, die wir, wobei jedoch eine Option, um sie später Ankunft von neuesten Daten vom Server aktualisieren! Keiner der Rückrufe ist obligatorisch, wenn 1. ist NULL, diese Methode kann immer abzurufenden Zusammenfassung vom Server verwendet werden und wenn 2. ist NULL, dies kann immer abzurufenden Zusammenfassung aus lokalen Datenbank verwendet werden!

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| mostUpdatedCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  um die aktuellste Zusammenfassung aus lokalen Datenbank sofort zu erhalten. Es besteht aus folgenden Parameter:<br><br>\*{KASFormFlatSummary} @param FlatSummary kann bei einem Fehler null sein.<br><br>\*{KASFormProcessedSummary} @param ProcessedSummary kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |
| notifyCallback | [FormSummaryCallback](kasclient.form.md#formsummarycallback) |  um benachrichtigt zu werden, mit der neuesten Zusammenfassung vom Server abgerufen. Es besteht aus folgenden Parameter:<br><br>\*{KASFormFlatSummary} @param FlatSummary kann bei einem Fehler null sein.<br><br>\*{KASFormProcessedSummary} @param ProcessedSummary kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getformurlasync"></a>

###  <a name="getformurlasync"></a>getFormURLAsync

▸ **GetFormURLAsync**(Rückruf: *`function`*):`void`

Ruft die Url der Datei vom Server, die mit dem Formular zugeordnete flache Antworten enthält

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*@param {Zeichenfolge} Url kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getformusercapabilitiesasync"></a>

###  <a name="getformusercapabilitiesasync"></a>getFormUserCapabilitiesAsync

▸ **GetFormUserCapabilitiesAsync**(Rückruf: *`function`*):`void`

Ruft bilden Berechtigungen

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASFormUserCapabilities} @param Berechtigungen<br><br>\*{Zeichenfolge} @param Fehler Fehlerzeichenfolge bei einem Fehler; andernfalls NULL |

**Gibt:**`void`

___

<a id="issubscribed"></a>

###  <a name="issubscribed"></a>isSubscribed

▸ **IsSubscribed**(Rückruf: *`function`*):`void`

Ruft ab, ob der aktuelle Benutzer Abonnenten oder nicht ist

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param IsSubscribed True, wenn der aktuelle Benutzer Abonnenten |

**Gibt:**`void`

___

<a id="likeform"></a>

###  <a name="likeform"></a>likeForm

▸ **LikeForm**():`void`

Anfragen eines Formulars, die Anzahl der like Anzahl hinzuzufügende können sinken, wenn der aktuelle Benutzer das Formular bereits gefallen hat

**Gibt:**`void`

___

<a id="sendreminderstorespond"></a>

###  <a name="sendreminderstorespond"></a>sendRemindersToRespond

▸ **SendRemindersToRespond**():`void`

Sendet eine Erinnerung (eine neue Unterhaltung Karte) gegen die vorhandene Karte

**Gibt:**`void`

___

<a id="shareformurl"></a>

###  <a name="shareformurl"></a>shareFormURL

▸ **ShareFormURL**(Url: *`string`*):`void`

Die Ergebnis-Url vom Server - abgerufene freigeben startet systemeigene Bildschirmfreigabe für die Formular-Url

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| url | `string` |  gemeinsam genutzt werden |

**Gibt:**`void`

___

<a id="showallreactions"></a>

###  <a name="showallreactions"></a>showAllReactions

▸ **ShowAllReactions**(ShowComments?: *`boolean`*):`void`

Zeigt alle den Reaktion Bildschirm ("gefällt mir" und Kommentare) für das Formular

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`showComments | `boolean` | true |  True, wenn Kommentare müssen auch angezeigt werden soll; False, andernfalls |

**Gibt:**`void`

___

<a id="updateactioninstancelocaldatacacheasync"></a>

###  <a name="updateactioninstancelocaldatacacheasync"></a>updateActionInstanceLocalDataCacheAsync

▸ **UpdateActionInstanceLocalDataCacheAsync**(ActionProperties: *[KASActionProperties](../classes/kasclient.kasactionproperties.md)*, Rückruf: *`function`*):`void`

Updates/speichert den angegebenen ActionInstance-Eigenschaften auf den lokalen Datencache, die, den diese Eigenschaften auf eine Aktion Instanzebene gespeichert sind. Jede Aktionsinstanz kann also einige lokalen Daten im Cache speichern und es werden nur in der betreffenden Instanz zugreifen können

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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

Diese API funktioniert nicht wie erwartet im Fall eines WAN-älterer Nachrichten.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionProperties | [KASActionProperties](../classes/kasclient.kasactionproperties.md) |  ActionInstance/Formulareigenschaften aktualisiert/gespeichert werden |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param Success gibt an, ob die Aktualisierung erfolgreich ist.<br><br>\*{Zeichenfolge} @param Json Fehlerzeichenfolge für das KASError-Objekt, das mit Fehlercode und/oder Beschreibung. |

**Gibt:**`void`

___

<a id="updateactionpackagelocaldatacacheasync"></a>

###  <a name="updateactionpackagelocaldatacacheasync"></a>updateActionPackageLocalDataCacheAsync

▸ **UpdateActionPackageLocalDataCacheAsync**(ActionPackageProperties: *[KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md)*, Rückruf: *`function`*):`void`

Updates/speichert den angegebenen Eigenschaften der Aktion Paket an den lokalen Datencache, wenn, den diese Eigenschaften auf der Ebene der Aktion Paket gespeichert werden. So werden die Daten von allen Aktionsinstanzen aus diesem Paket Aktion erstellt freigegeben.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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

Diese API funktioniert nicht wie erwartet im Fall eines WAN-älterer Nachrichten.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionPackageProperties | [KASActionPackageProperties](../classes/kasclient.kasactionpackageproperties.md) |  Eigenschaften der Aktion Paket aktualisiert/gespeichert werden |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param Success gibt an, ob die Aktualisierung erfolgreich ist.<br><br>\*{Zeichenfolge} @param Json Fehlerzeichenfolge für das KASError-Objekt, das mit Fehlercode und/oder Beschreibung. |

**Gibt:**`void`

___

<a id="updateformpropertiesasync"></a>

###  <a name="updateformpropertiesasync"></a>updateFormPropertiesAsync

▸ **UpdateFormPropertiesAsync**(PropertyUpdates: * [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md)[]*, NotifyUsers: * `string`[]*, NotificationMessage: *`string`*, Rückruf: *`function`*):`void`

Buchen Sie eine Anforderung zum Aktualisieren der dem Formular zugeordneten Eigenschaften

#### <a name="sample-usage"></a>Beispiel für die Verwendung

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
| propertyUpdates | [KASFormPropertyUpdateInfo](../classes/kasclient.kasformpropertyupdateinfo.md) [] |  ein Array von allen Update Ereignisinfos hinzu, die erforderlich sind, ausgeführt werden, können Update Ereignisinfos hinzu mit erstellt werden KASFormPropertyUpdateFactory |
| notifyUsers | `string`[] |  Senden von Pushbenachrichtigungen an diese Benutzer-Ids zu diesem update |
| notificationMessage | `string` |  Push-Benachrichtigung |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param Success gibt an, ob die Aktualisierung erfolgreich ist. |

**Gibt:**`void`

___

