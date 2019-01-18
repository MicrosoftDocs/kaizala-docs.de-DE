---
ms.openlocfilehash: 84017de85cac36d49be86fe3a7a2aca9bb9b4d34
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728068"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)

# <a name="class-kasattachmentlistquestionresult"></a>Klasse: KASAttachmentListQuestionResult

Dieses Modell enthält Daten für jede Antwort auf eine Frage Listentyp Anlage.
## <a name="hierarchy"></a>Hierarchie

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASAttachmentListQuestionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentListType](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [attachmentsResponseJSONStrings](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [questionId](kasclient.kasattachmentlistquestionresult.md#questionid)
* [questionTitle](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [questionType](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [Zeitstempel](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [userInfo](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a>attachmentListType

**● AttachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType.GENERIC

AttachmentListType: enthält den Typ der Anlage Liste Antwort

___

<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a>attachmentsResponseJSONStrings

**● AttachmentsResponseJSONStrings**: * `string`[]* =]

AttachmentsResponseJSONStrings: enthält die Liste der Anlagen, die jeder Antwort als eine JSON-Zeichenfolge, die direkt in der QuestionIdToAnswerMap verfügbar ist, entspricht.

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

<a id="timestamps"></a>

###  <a name="timestamps"></a>Zeitstempel

**● Zeitstempel**: * `string`[]* =]

Zeitstempel: der Zeitstempel der Antwort für jede Antwort enthält.

___

<a id="userinfo"></a>

###  <a name="userinfo"></a>userInfo

**● UserInfo**: * [KASUser](kasclient.kasuser.md)[]* =]

UserInfo: enthält die Instanzen von KASUser mit Details für die Teilnehmer für die bestimmten Antwort, damit das Bild Name und Profil des Befragten angezeigt werden können.

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

