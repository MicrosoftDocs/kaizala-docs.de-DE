[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionResult](../classes/kasclient.kasattachmentlistquestionresult.md)

# <a name="class-kasattachmentlistquestionresult"></a>Klasse: KASAttachmentListQuestionResult

Dieses Modell enthält Daten für jede Antwort auf eine Art von Anlagen Listentyp Frage.
## <a name="hierarchy"></a>Hierarchie

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASAttachmentListQuestionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentListType](kasclient.kasattachmentlistquestionresult.md#attachmentlisttype)
* [attachmentsResponseJSONStrings](kasclient.kasattachmentlistquestionresult.md#attachmentsresponsejsonstrings)
* [Fragen-Nr](kasclient.kasattachmentlistquestionresult.md#questionid)
* [questionTitle](kasclient.kasattachmentlistquestionresult.md#questiontitle)
* [questiontype](kasclient.kasattachmentlistquestionresult.md#questiontype)
* [Zeitstempel](kasclient.kasattachmentlistquestionresult.md#timestamps)
* [userInfo](kasclient.kasattachmentlistquestionresult.md#userinfo)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasattachmentlistquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a>attachmentListType

**● attachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType. Generic

attachmentListType: enthält den Typ der Anlage Listen Antwort

___
<a id="attachmentsresponsejsonstrings"></a>

###  <a name="attachmentsresponsejsonstrings"></a>attachmentsResponseJSONStrings

**● attachmentsResponseJSONStrings**: * `string`[]* = []

attachmentsResponseJSONStrings: enthält die Liste der Anlagen, die jeder Antwort als JSON-Zeichenfolge entsprechen, die direkt im questionIdToAnswerMap verfügbar ist.

___
<a id="questionid"></a>

###  <a name="questionid"></a>Fragen-Nr

**● Frag**-Nr *`number`* : = 0

Index der Frage

___
<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● questionTitle**: *`string`* = ""

Titel der Frage

___
<a id="questiontype"></a>

###  <a name="questiontype"></a>questiontype

**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None

Typ der Frage

___
<a id="timestamps"></a>

###  <a name="timestamps"></a>Zeitstempel

**● Zeitstempel**: * `string`[]* = []

Timestamps: enthält die Antwortzeit Stempel für jede Antwort.

___
<a id="userinfo"></a>

###  <a name="userinfo"></a>userInfo

**●**InfoInfo: * [KASUser](kasclient.kasuser.md)[]* = []

Benutzername: enthält Instanzen von KASUser mit Details für den Teilnehmer für die jeweilige Antwort, sodass wir den Namen und das Profilbild des Befragten anzeigen können.

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASQuestionResult](kasclient.kasquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASQuestionResult](kasclient.kasquestionresult.md)

___

