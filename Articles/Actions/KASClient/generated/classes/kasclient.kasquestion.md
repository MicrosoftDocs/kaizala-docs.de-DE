---
ms.openlocfilehash: cd7a7880b45a68ea4ac977487756c754a2291dd4
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728074"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)

# <a name="class-kasquestion"></a>Klasse: KASQuestion

## <a name="hierarchy"></a>Hierarchie

**KASQuestion**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [config](kasclient.kasquestion.md#config)
* [displayType](kasclient.kasquestion.md#displaytype)
* [id](kasclient.kasquestion.md#id)
* [isEditable](kasclient.kasquestion.md#iseditable)
* [isExcludedFromReporting](kasclient.kasquestion.md#isexcludedfromreporting)
* [isInvisible](kasclient.kasquestion.md#isinvisible)
* [isResponseOptional](kasclient.kasquestion.md#isresponseoptional)
* [options](kasclient.kasquestion.md#options)
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

<a id="config"></a>

###  <a name="config"></a>config

**● Config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* = Null

Konfiguration/Verhalten einer Frage

___

<a id="displaytype"></a>

###  <a name="displaytype"></a>displayType

**● DisplayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* = KASQuestionDisplayType.None

Typ der Optionen für die Frage anzeigen

___

<a id="id"></a>

###  <a name="id"></a>id

**●-Id**: *`number`* = 0

Index der Frage, beginnt mit 0

___

<a id="iseditable"></a>

###  <a name="iseditable"></a>isEditable

**● IsEditable**: *`boolean`* = True

Kennzeichnet der Standardwert ist true, wenn die Frage vom Responder bearbeitet werden kann,

___

<a id="isexcludedfromreporting"></a>

###  <a name="isexcludedfromreporting"></a>isExcludedFromReporting

**● IsExcludedFromReporting**: *`boolean`* = False

Gibt an, ob die Frage aus allen möglichen reporting übersprungen werden

___

<a id="isinvisible"></a>

###  <a name="isinvisible"></a>isInvisible

**● IsInvisible**: *`boolean`* = False

Gibt an, wenn die Frage für den-Responder nicht sichtbar sein soll, standardmäßig false ist

___

<a id="isresponseoptional"></a>

###  <a name="isresponseoptional"></a>isResponseOptional

**● IsResponseOptional**: *`boolean`* = False

Gibt an, ob es obligatorisch ist, diese Frage zu beantworten

___

<a id="options"></a>

###  <a name="options"></a>options

**● Optionen**: * [KASQuestionOption](kasclient.kasquestionoption.md)[]* =]

Liste der Optionen für die Frage

___

<a id="title"></a>

###  <a name="title"></a>title

**● Titel**: *`string`* = ""

Titel der Frage

___

<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None

Typ der Frage

___

<a id="valif"></a>

###  <a name="valif"></a>valif

**● Valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* = Null

Eine Frage - JSON von Regeln, Fehlerzeichenfolge und Hilfezeichenfolge Validierungsregeln

___

<a id="visif"></a>

###  <a name="visif"></a>visif

**● Visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* = Null

Regeln für die Sichtbarkeit der eine Frage - Regelzeichenfolge

___

## <a name="methods"></a>Methoden

<a id="getapicompatiblequestiontype"></a>

###  <a name="getapicompatiblequestiontype"></a>getAPICompatibleQuestionType

▸ **GetAPICompatibleQuestionType**(Typ: *`string`*):`string`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Typ | `string` |

**Gibt:**`string`

___

<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a>toAPICompatibleJSON

▸ **ToAPICompatibleJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="toclientjson"></a>

###  <a name="toclientjson"></a>toClientJSON

▸ **ToClientJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="validateresponse"></a>

###  <a name="validateresponse"></a>validateResponse

▸ **ValidateResponse**(Antwort: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Antwort | `string` |

**Gibt:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASQuestion](kasclient.kasquestion.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASQuestion](kasclient.kasquestion.md)

___

