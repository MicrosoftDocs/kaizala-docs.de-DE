[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)

# <a name="class-kasquestion"></a>Klasse: KASQuestion

## <a name="hierarchy"></a>Hierarchie

**KASQuestion**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [Attachments-List](kasclient.kasquestion.md#attachmentslist)
* [config](kasclient.kasquestion.md#config)
* [Display Type](kasclient.kasquestion.md#displaytype)
* [id](kasclient.kasquestion.md#id)
* [isEditable](kasclient.kasquestion.md#iseditable)
* [isExcludedFromReporting](kasclient.kasquestion.md#isexcludedfromreporting)
* [isunsichtbar](kasclient.kasquestion.md#isinvisible)
* [isResponseOptional](kasclient.kasquestion.md#isresponseoptional)
* [options](kasclient.kasquestion.md#options)
* [questionMetadata](kasclient.kasquestion.md#questionmetadata)
* [title](kasclient.kasquestion.md#title)
* [type](kasclient.kasquestion.md#type)
* [valif](kasclient.kasquestion.md#valif)
* [visif](kasclient.kasquestion.md#visif)
### <a name="methods"></a>Methoden

* [getAPICompatibleQuestionType](kasclient.kasquestion.md#getapicompatiblequestiontype)
* [toAPICompatibleJSON](kasclient.kasquestion.md#toapicompatiblejson)
* [toClientJSON](kasclient.kasquestion.md#toclientjson)
* [toJSON](kasclient.kasquestion.md#tojson)
* [validateResponse](kasclient.kasquestion.md#validateresponse)
* [fromJSON](kasclient.kasquestion.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentslist"></a>

###  <a name="attachmentslist"></a>Attachments-List

**●**Attachments: * [KASAttachment](kasclient.kasattachment.md)[]* = []

Attchments eines Frage-Arrays von KASAttachment

___
<a id="config"></a>

###  <a name="config"></a>config

**● config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* = NULL

Konfiguration/Verhalten einer Frage

___
<a id="displaytype"></a>

###  <a name="displaytype"></a>Display Type

**● Display**Type: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* = KASQuestionDisplayType. None

Anzeigetyp der Fragen Optionen

___
<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`number`* = 0

Index der Frage, beginnt mit 0

___
<a id="iseditable"></a>

###  <a name="iseditable"></a>isEditable

**●**IsEditable: *`boolean`* = true

Gibt an, ob die Frage vom Responder bearbeitet werden kann, der Standardwert ist true.

___
<a id="isexcludedfromreporting"></a>

###  <a name="isexcludedfromreporting"></a>isExcludedFromReporting

**● isExcludedFromReporting**: *`boolean`* = false

Gibt an, ob die Frage von allen Arten von Berichten übersprungen wird.

___
<a id="isinvisible"></a>

###  <a name="isinvisible"></a>isunsichtbar

**● isunsichtbar**: *`boolean`* = false

Gibt an, ob die Frage für den Responder unsichtbar sein soll, der Standardwert ist false.

___
<a id="isresponseoptional"></a>

###  <a name="isresponseoptional"></a>isResponseOptional

**● isResponseOptional**: *`boolean`* = false

Gibt an, ob eine Antwort auf diese Frage erforderlich ist.

___
<a id="options"></a>

###  <a name="options"></a>options

**● Optionen**: * [KASQuestionOption](kasclient.kasquestionoption.md)[]* = []

Liste der Optionen für die Frage

___
<a id="questionmetadata"></a>

###  <a name="questionmetadata"></a>questionMetadata

**● questionMetadata**:*`string`*

___
<a id="title"></a>

###  <a name="title"></a>title

**● Title**: *`string`* = ""

Titel der Frage

___
<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None

Typ der Frage

___
<a id="valif"></a>

###  <a name="valif"></a>valif

**● valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* = NULL

Validierungsregeln für eine Frage-JSON von Regel (n), Fehlerzeichenfolge und Hilfezeichenfolge

___
<a id="visif"></a>

###  <a name="visif"></a>visif

**● visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* = NULL

Sichtbarkeitsregeln einer Frage-Regel Zeichenfolge

___

## <a name="methods"></a>Methoden

<a id="getapicompatiblequestiontype"></a>

###  <a name="getapicompatiblequestiontype"></a>getAPICompatibleQuestionType

▸ **getAPICompatibleQuestionType**(Typ: *`string`*):`string`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| type | `string` |

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
<a id="validateresponse"></a>

###  <a name="validateresponse"></a>validateResponse

▸ **validateResponse**(Antwort: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Antwort | `string` |

**Gibt Folgendes zurück:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASQuestion](kasclient.kasquestion.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASQuestion](kasclient.kasquestion.md)

___

