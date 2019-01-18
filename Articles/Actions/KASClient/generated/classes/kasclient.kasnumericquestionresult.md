---
ms.openlocfilehash: 9384cc245b6c5c3d8889e6c9025eae7f31802469
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728093"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASNumericQuestionResult](../classes/kasclient.kasnumericquestionresult.md)

# <a name="class-kasnumericquestionresult"></a>Klasse: KASNumericQuestionResult

## <a name="hierarchy"></a>Hierarchie

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASNumericQuestionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [Durchschnitt](kasclient.kasnumericquestionresult.md#average)
* [questionId](kasclient.kasnumericquestionresult.md#questionid)
* [questionTitle](kasclient.kasnumericquestionresult.md#questiontitle)
* [questionType](kasclient.kasnumericquestionresult.md#questiontype)
* [Summe](kasclient.kasnumericquestionresult.md#sum)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasnumericquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="average"></a>

###  <a name="average"></a>average

**● Durchschnitt**: *`number`* = 0

___

<a id="questionid"></a>

###  <a name="questionid"></a>questionId

**● QuestionId**: *`number`* = 0

Index der Frage

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● QuestionTitle**: *`string`* = ""

Titel der Frage

___

<a id="questiontype"></a>

###  <a name="questiontype"></a>questionType

**● QuestionType**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None

Typ der Frage

___

<a id="sum"></a>

###  <a name="sum"></a>sum

**● Summe**: *`number`* = 0

Für numerische Fragen werden das Ergebnis aggregierte Summe und Durchschnitt aller Antworten

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

___

