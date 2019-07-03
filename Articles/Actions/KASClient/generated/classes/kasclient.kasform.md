[](../README.md) > [KASClient](../modules/kasclient.md) > [KASForm](../classes/kasclient.kasform.md)

# <a name="class-kasform"></a>Klasse: KASForm

## <a name="hierarchy"></a>Hierarchie

**KASForm**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [allowSendReminder](kasclient.kasform.md#allowsendreminder)
* [canFetchAnonymousShareLink](kasclient.kasform.md#canfetchanonymoussharelink)
* [conversationId](kasclient.kasform.md#conversationid)
* [creatorId](kasclient.kasform.md#creatorid)
* [Ablauf](kasclient.kasform.md#expiry)
* [id](kasclient.kasform.md#id)
* [isAnonymous](kasclient.kasform.md#isanonymous)
* [isGroupLevelAggregationRequired](kasclient.kasform.md#isgrouplevelaggregationrequired)
* [isLocationRequested](kasclient.kasform.md#islocationrequested)
* [isResponseAppended](kasclient.kasform.md#isresponseappended)
* [JSON](kasclient.kasform.md#json)
* [packageId](kasclient.kasform.md#packageid)
* [packageMinorVersion](kasclient.kasform.md#packageminorversion)
* [properties](kasclient.kasform.md#properties)
* [Fragen](kasclient.kasform.md#questions)
* [reportType](kasclient.kasform.md#reporttype)
* [title](kasclient.kasform.md#title)
* [type](kasclient.kasform.md#type)
* [version](kasclient.kasform.md#version)
* [Sicht](kasclient.kasform.md#visibility)
### <a name="methods"></a>Methoden

* [getAPICompatibleVisibilityType](kasclient.kasform.md#getapicompatiblevisibilitytype)
* [toAPICompatibleJSON](kasclient.kasform.md#toapicompatiblejson)
* [toClientJSON](kasclient.kasform.md#toclientjson)
* [toJSON](kasclient.kasform.md#tojson)
* [addResponseNotificationForAddRow](kasclient.kasform.md#addresponsenotificationforaddrow)
* [fromJSON](kasclient.kasform.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="allowsendreminder"></a>

###  <a name="allowsendreminder"></a>allowSendReminder

**● allowSendReminder**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility. Sender

Wer Erinnerung senden kann, der Standardwert lautet Absender.

___
<a id="canfetchanonymoussharelink"></a>

###  <a name="canfetchanonymoussharelink"></a>canFetchAnonymousShareLink

**● canFetchAnonymousShareLink**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility. MembersAndSubscribers

Wer anonyme Antwort Freigabe-Link abrufen kann, der Standardwert ist jeder

___
<a id="conversationid"></a>

###  <a name="conversationid"></a>conversationId

**● Conversation**-Nr *`string`* : = ""

Zugeordnete Unterhaltungs-ID sollte nicht geändert werden

___
<a id="creatorid"></a>

###  <a name="creatorid"></a>creatorId

**● creatorname**: *`string`* = ""

Benutzer-ID, die das Formular erstellt hat, sollte nicht geändert werden

___
<a id="expiry"></a>

###  <a name="expiry"></a>Ablauf

**● Ablaufdatum**: *`number`* = 0

Ablaufdatum des Formulars

___
<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

Formular-ID, sollte nicht geändert werden

___
<a id="isanonymous"></a>

###  <a name="isanonymous"></a>isAnonymous

**● IsAnonymous**: *`boolean`* = false

Wenn das Formular anonym ist, lautet der Standardwert false.

___
<a id="isgrouplevelaggregationrequired"></a>

###  <a name="isgrouplevelaggregationrequired"></a>isGroupLevelAggregationRequired

**● isGroupLevelAggregationRequired**: *`boolean`* = false

Gibt an, ob der Server eine Aggregation auf Untergruppenebene für Ergebnisse dieser Aktionsinstanz ausführen soll.

___
<a id="islocationrequested"></a>

###  <a name="islocationrequested"></a>isLocationRequested

**● isLocationRequested**: *`boolean`* = false

Gibt an, ob die Position der Teilnehmer mit der Antwort verbunden ist oder nicht, Standardwert ist false.

___
<a id="isresponseappended"></a>

###  <a name="isresponseappended"></a>isResponseAppended

**● isResponseAppended**: *`boolean`* = false

Gibt an, ob mehrere Antworten von einem Benutzer zulässig sind oder nicht, der Standardwert ist false.

___
<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___
<a id="packageid"></a>

###  <a name="packageid"></a>packageId

**● Packaged**: *`string`* = ""

Paket-ID des MiniApp, sollte nicht geändert werden

___
<a id="packageminorversion"></a>

###  <a name="packageminorversion"></a>packageMinorVersion

**● packageMinorVersion**: *`number`* =-1

Paket-neben Version

___
<a id="properties"></a>

###  <a name="properties"></a>properties

**● Eigenschaften**: * [KASFormProperty](kasclient.kasformproperty.md)[]* = []

Eine Liste der dem Formular zugeordneten Metadaten

___
<a id="questions"></a>

###  <a name="questions"></a>Fragen

**● Questions**: * [KASQuestion](kasclient.kasquestion.md)[]* = []

Alle Fragen im Zusammenhang mit dem Formular

___
<a id="reporttype"></a>

###  <a name="reporttype"></a>reportType

**● reportType**: *`number`* = 0

Berichtstyp der Umfrage, Standardwert ist 0, für Auftrag sollte es 1 sein.

___
<a id="title"></a>

###  <a name="title"></a>title

**● Title**: *`string`* = ""

Formulartitel

___
<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *`number`* = 20

Der Typ des Formulars, Standardwert ist 20, sollte nicht geändert werden

___
<a id="version"></a>

###  <a name="version"></a>Version

**● Version**: *`number`* = 2

Version des Formulars, Standardwert 2, sollte nicht geändert werden

___
<a id="visibility"></a>

###  <a name="visibility"></a>visibility

**● Sichtbarkeit**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility. all

Wer die Zusammenfassung des Formulars sehen kann, der Standardwert ist "All".

___

## <a name="methods"></a>Methoden

<a id="getapicompatiblevisibilitytype"></a>

###  <a name="getapicompatiblevisibilitytype"></a>getAPICompatibleVisibilityType

▸ **getAPICompatibleVisibilityType**(visibilitytype: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)*):`string`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| visibilitytype | [KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md) |

**Gibt Folgendes zurück:**`string`

___
<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a>toAPICompatibleJSON

▸ **toAPICompatibleJSON**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="toclientjson"></a>

###  <a name="toclientjson"></a>toClientJSON

▸ **toClientJSON**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="addresponsenotificationforaddrow"></a>

### <a name="static-addresponsenotificationforaddrow"></a>`<Static>`addResponseNotificationForAddRow

▸ **addResponseNotificationForAddRow**(Formular: *[KASForm](kasclient.kasform.md)*, notificationSpec: *[KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Formular | [KASForm](kasclient.kasform.md) |
| notificationSpec | [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md) |

**Gibt Folgendes zurück:**`void`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`JSON`*:): [KASForm](kasclient.kasform.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |

**Gibt Folgendes zurück:** [KASForm](kasclient.kasform.md)

___

