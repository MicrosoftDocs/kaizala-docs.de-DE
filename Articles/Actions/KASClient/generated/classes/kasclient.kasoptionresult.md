[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionResult](../classes/kasclient.kasoptionresult.md)

# <a name="class-kasoptionresult"></a>Klasse: KASOptionResult

## <a name="hierarchy"></a>Hierarchie

**KASOptionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [optionId](kasclient.kasoptionresult.md#optionid)
* [optionTitle](kasclient.kasoptionresult.md#optiontitle)
* [responderToResponseCount](kasclient.kasoptionresult.md#respondertoresponsecount)
* [totalResponsesCount](kasclient.kasoptionresult.md#totalresponsescount)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasoptionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="optionid"></a>

###  <a name="optionid"></a>optionId

**● options**-Nr *`number`* : = 0

Index der Option

___
<a id="optiontitle"></a>

###  <a name="optiontitle"></a>optionTitle

**● optionTitle**: *`string`* = ""

Titel der Option

___
<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a>responderToResponseCount

**● responderToResponseCount**:*`object`*

Eine Zuordnung von Benutzer-IDs für Ihr Antwort zählungs Wörterbuch<UserID: String, ResponseCount: Number>
#### <a name="type-declaration"></a>Typdeklaration

___
<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a>totalResponsesCount

**● totalResponsesCount**: *`number`* = 0

Wie viele haben diese Option gewählt?

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASOptionResult](kasclient.kasoptionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASOptionResult](kasclient.kasoptionresult.md)

___

