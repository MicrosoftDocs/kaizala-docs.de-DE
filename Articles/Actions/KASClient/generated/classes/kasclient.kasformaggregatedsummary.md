[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormAggregatedSummary](../classes/kasclient.kasformaggregatedsummary.md)

# <a name="class-kasformaggregatedsummary"></a>Klasse: KASFormAggregatedSummary

## <a name="hierarchy"></a>Hierarchie

**KASFormAggregatedSummary**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [formId](kasclient.kasformaggregatedsummary.md#formid)
* [formStatus](kasclient.kasformaggregatedsummary.md#formstatus)
* [JSON](kasclient.kasformaggregatedsummary.md#json)
* [result](kasclient.kasformaggregatedsummary.md#result)
* [targetResponderCount](kasclient.kasformaggregatedsummary.md#targetrespondercount)
* [totalDeliveryCount](kasclient.kasformaggregatedsummary.md#totaldeliverycount)
* [totalParticipantsCount](kasclient.kasformaggregatedsummary.md#totalparticipantscount)
* [totalResponseCount](kasclient.kasformaggregatedsummary.md#totalresponsecount)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasformaggregatedsummary.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="formid"></a>

###  <a name="formid"></a>formId

**● Formular**-Nr *`string`* : = ""

___
<a id="formstatus"></a>

###  <a name="formstatus"></a>formStatus

**● formStatus**: *[formStatus](../enums/kasclient.formstatus.md)* = formStatus. Active

___
<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___
<a id="result"></a>

###  <a name="result"></a>result

**● Ergebnis**: * `any`[]* = []

___
<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● targetResponderCount**: *`number`* = 0

___
<a id="totaldeliverycount"></a>

###  <a name="totaldeliverycount"></a>totalDeliveryCount

**● totalDeliveryCount**: *`number`* =-1

___
<a id="totalparticipantscount"></a>

###  <a name="totalparticipantscount"></a>totalParticipantsCount

**● totalParticipantsCount**: *`number`* = 0

___
<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● totalResponseCount**: *`number`* = 0

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`JSON`*, questions: * [KASQuestion](kasclient.kasquestion.md)[]*): [KASFormAggregatedSummary](kasclient.kasformaggregatedsummary.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |
| Fragen | [KASQuestion](kasclient.kasquestion.md) [] |

**Gibt Folgendes zurück:** [KASFormAggregatedSummary](kasclient.kasformaggregatedsummary.md)

___

