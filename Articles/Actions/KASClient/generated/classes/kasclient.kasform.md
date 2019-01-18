---
ms.openlocfilehash: a2550fdcf4a5d37ac751dd188ae3cf1338962e57
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728115"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASForm](../classes/kasclient.kasform.md)

# <a name="class-kasform"></a>Klasse: KASForm

## <a name="hierarchy"></a>Hierarchie

**KASForm**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [allowSendReminder](kasclient.kasform.md#allowsendreminder)
* [conversationId](kasclient.kasform.md#conversationid)
* [creatorId](kasclient.kasform.md#creatorid)
* [Kennwortablauf](kasclient.kasform.md#expiry)
* [id](kasclient.kasform.md#id)
* [isAnonymous](kasclient.kasform.md#isanonymous)
* [isGroupLevelAggregationRequired](kasclient.kasform.md#isgrouplevelaggregationrequired)
* [isLocationRequested](kasclient.kasform.md#islocationrequested)
* [isResponseAppended](kasclient.kasform.md#isresponseappended)
* [JSON](kasclient.kasform.md#json)
* [packageId](kasclient.kasform.md#packageid)
* [properties](kasclient.kasform.md#properties)
* [Fragen](kasclient.kasform.md#questions)
* [Definition](kasclient.kasform.md#reporttype)
* [title](kasclient.kasform.md#title)
* [type](kasclient.kasform.md#type)
* [version](kasclient.kasform.md#version)
* [visibility](kasclient.kasform.md#visibility)
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

**● AllowSendReminder**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility.Sender

Wer kann Erinnerung erhalten, Standardwert Absender

___

<a id="conversationid"></a>

###  <a name="conversationid"></a>conversationId

**● ConversationId**: *`string`* = ""

Zugehörige Konversations-Id, sollte nicht geändert werden

___

<a id="creatorid"></a>

###  <a name="creatorid"></a>creatorId

**● CreatorId**: *`string`* = ""

Benutzer-Id, die das Formular erstellt hat, sollte nicht geändert werden

___

<a id="expiry"></a>

###  <a name="expiry"></a>Kennwortablauf

**● Ablauf**: *`number`* = 0

Ablaufzeit des Formulars

___

<a id="id"></a>

###  <a name="id"></a>id

**●-Id**: *`string`* = ""

Id bilden, sollte nicht geändert werden

___

<a id="isanonymous"></a>

###  <a name="isanonymous"></a>isAnonymous

**● IsAnonymous**: *`boolean`* = False

Wenn das Formular anonyme ist, ist die Standardeinstellung "false"

___

<a id="isgrouplevelaggregationrequired"></a>

###  <a name="isgrouplevelaggregationrequired"></a>isGroupLevelAggregationRequired

**● IsGroupLevelAggregationRequired**: *`boolean`* = False

Gibt an, ob die Server Untergruppe Level Aggregation auf Ergebnisse für diese Aktionsinstanz geschehen soll

___

<a id="islocationrequested"></a>

###  <a name="islocationrequested"></a>isLocationRequested

**● IsLocationRequested**: *`boolean`* = False

Gibt die Teilnehmer Speicherort mit der Antwort oder nicht angeschlossen ist, standardmäßig false ist

___

<a id="isresponseappended"></a>

###  <a name="isresponseappended"></a>isResponseAppended

**● IsResponseAppended**: *`boolean`* = False

Gibt an, wenn mehrere Antworten von einem Benutzer oder nicht zugelassen sind, standardmäßig false ist

___

<a id="json"></a>

###  <a name="json"></a>json

**● Json**:*`JSON`*

___

<a id="packageid"></a>

###  <a name="packageid"></a>packageId

**● PackageId**: *`string`* = ""

Konfigurationspaket-Id von der MiniApp, sollte nicht geändert werden

___

<a id="properties"></a>

###  <a name="properties"></a>properties

**● Eigenschaften**: * [KASFormProperty](kasclient.kasformproperty.md)[]* =]

Eine Liste der dem Formular zugeordneten Metadaten

___

<a id="questions"></a>

###  <a name="questions"></a>Fragen

**● Fragen**: * [KASQuestion](kasclient.kasquestion.md)[]* =]

Alle dem Formular zugeordneten Fragen

___

<a id="reporttype"></a>

###  <a name="reporttype"></a>Definition

**● Definition**: *`number`* = 0

Berichtstyp Umfrage, Standard ist 0, für den Auftrag wird 1

___

<a id="title"></a>

###  <a name="title"></a>title

**● Titel**: *`string`* = ""

Formulartitel

___

<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *`number`* = 20

Typ des Formulars Standardeinstellung ist 20, sollte nicht geändert werden

___

<a id="version"></a>

###  <a name="version"></a>Version

**● Version**: *`number`* = 2

Version des Formulars, der Standardwert ist 2, sollte nicht geändert werden

___

<a id="visibility"></a>

###  <a name="visibility"></a>visibility

**● Sichtbarkeit**: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)* = KASFormResultVisibility.All

Wem die Zusammenfassung des Formulars angezeigt werden, ist mit Standardwert alle

___

## <a name="methods"></a>Methoden

<a id="getapicompatiblevisibilitytype"></a>

###  <a name="getapicompatiblevisibilitytype"></a>getAPICompatibleVisibilityType

▸ **GetAPICompatibleVisibilityType**(VisibilityType: *[KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md)*):`string`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| visibilityType | [KASFormResultVisibility](../enums/kasclient.kasformresultvisibility.md) |

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

<a id="addresponsenotificationforaddrow"></a>

### <a name="static-addresponsenotificationforaddrow"></a>`<Static>`addResponseNotificationForAddRow

▸ **AddResponseNotificationForAddRow**(Formular: *[KASForm](kasclient.kasform.md)*, NotificationSpec: *[KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Formular | [KASForm](kasclient.kasform.md) |
| notificationSpec | [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md) |

**Gibt:**`void`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`JSON`*): [KASForm](kasclient.kasform.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `JSON` |

**Gibt:** [KASForm](kasclient.kasform.md)

___

