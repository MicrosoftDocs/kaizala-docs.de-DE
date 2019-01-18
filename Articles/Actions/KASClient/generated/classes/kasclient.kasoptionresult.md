---
ms.openlocfilehash: c52e672a7e3356171388692054fcd1dc3cee5365
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728058"
---
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

**● OptionId**: *`number`* = 0

Index der option

___

<a id="optiontitle"></a>

###  <a name="optiontitle"></a>optionTitle

**● OptionTitle**: *`string`* = ""

Titel der option

___

<a id="respondertoresponsecount"></a>

###  <a name="respondertoresponsecount"></a>responderToResponseCount

**● ResponderToResponseCount**:*`object`*

Eine Übersicht über die Benutzer-Ids für ihre Antwort Count Dictionary<UserId: string, ResponseCount: Number>
#### <a name="type-declaration"></a>Typdeklaration

___

<a id="totalresponsescount"></a>

###  <a name="totalresponsescount"></a>totalResponsesCount

**● TotalResponsesCount**: *`number`* = 0

Wie viele diese Option ausgewählt haben

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASOptionResult](kasclient.kasoptionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASOptionResult](kasclient.kasoptionresult.md)

___

