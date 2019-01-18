---
ms.openlocfilehash: 1b4a3a6805310a9a0eb7c63701c367d96aa5fe61
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728077"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormAggregatedSummary](../classes/kasclient.kasformaggregatedsummary.md)

# <a name="class-kasformaggregatedsummary"></a>Klasse: KASFormAggregatedSummary

## <a name="hierarchy"></a>Hierarchie

**KASFormAggregatedSummary**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [formId](kasclient.kasformaggregatedsummary.md#formid)
* [formStatus](kasclient.kasformaggregatedsummary.md#formstatus)
* [JSON](kasclient.kasformaggregatedsummary.md#json)
* [Ergebnis](kasclient.kasformaggregatedsummary.md#result)
* [targetResponderCount](kasclient.kasformaggregatedsummary.md#targetrespondercount)
* [totalParticipantsCount](kasclient.kasformaggregatedsummary.md#totalparticipantscount)
* [totalResponseCount](kasclient.kasformaggregatedsummary.md#totalresponsecount)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasformaggregatedsummary.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="formid"></a>

###  <a name="formid"></a>formId

**● FormId**: *`string`* = ""

___

<a id="formstatus"></a>

###  <a name="formstatus"></a>formStatus

**● FormStatus**: *[FormStatus](../enums/kasclient.formstatus.md)* = FormStatus.Active

___

<a id="json"></a>

###  <a name="json"></a>json

**● Json**:*`JSON`*

___

<a id="result"></a>

###  <a name="result"></a>result

**● Ergebnis**: * `any`[]* =]

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● TargetResponderCount**: *`number`* = 0

___

<a id="totalparticipantscount"></a>

###  <a name="totalparticipantscount"></a>totalParticipantsCount

**● TotalParticipantsCount**: *`number`* = 0

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● TotalResponseCount**: *`number`* = 0

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`JSON`*, Fragen: * [KASQuestion](kasclient.kasquestion.md)[]*): [KASFormAggregatedSummary](kasclient.kasformaggregatedsummary.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `JSON` |
| Fragen | [KASQuestion](kasclient.kasquestion.md) [] |

**Gibt:** [KASFormAggregatedSummary](kasclient.kasformaggregatedsummary.md)

___

