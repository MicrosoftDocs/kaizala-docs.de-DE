---
ms.openlocfilehash: 73491a2b9d73d311550fe14f32a34d5670e3f892
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728044"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)

# <a name="class-kasoptionquestionresult"></a>Klasse: KASOptionQuestionResult

## <a name="hierarchy"></a>Hierarchie

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASOptionQuestionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [optionResults](kasclient.kasoptionquestionresult.md#optionresults)
* [questionId](kasclient.kasoptionquestionresult.md#questionid)
* [questionTitle](kasclient.kasoptionquestionresult.md#questiontitle)
* [questionType](kasclient.kasoptionquestionresult.md#questiontype)
### <a name="methods"></a>Methoden

* [getResultsOrder](kasclient.kasoptionquestionresult.md#getresultsorder)
* [fromJSON](kasclient.kasoptionquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="optionresults"></a>

###  <a name="optionresults"></a>optionResults

**● OptionResults**:*`object`*

Für SingleSelect/MultiSelect Frage, wird das Ergebnis Option Id im Vergleich zu ihren zählt Dictionary<OptionId sein: number, OptionResult: KASOptionResult>
#### <a name="type-declaration"></a>Typdeklaration

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

## <a name="methods"></a>Methoden

<a id="getresultsorder"></a>

###  <a name="getresultsorder"></a>getResultsOrder

▸ **GetResultsOrder**(): `number`]

Ruft alle in ihrer gesamtantworten Anzahl (absteigend) sortiert Option-ids

**Gibt:** `number`Liste mit der Option-Ids]

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

___

