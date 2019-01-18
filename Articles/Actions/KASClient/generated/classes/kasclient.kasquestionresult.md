---
ms.openlocfilehash: 1e51f3aa34eb9a0a229cae1d4fd25be002447a1e
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728090"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)

# <a name="class-kasquestionresult"></a>Klasse: KASQuestionResult

## <a name="hierarchy"></a>Hierarchie

**KASQuestionResult**

↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)

↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [questionId](kasclient.kasquestionresult.md#questionid)
* [questionTitle](kasclient.kasquestionresult.md#questiontitle)
* [questionType](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

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

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASQuestionResult](kasclient.kasquestionresult.md)

___

