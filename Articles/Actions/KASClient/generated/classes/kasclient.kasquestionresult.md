[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestionResult](../classes/kasclient.kasquestionresult.md)

# <a name="class-kasquestionresult"></a>Klasse: KASQuestionResult

## <a name="hierarchy"></a>Hierarchie

**KASQuestionResult**

↳ [KASAttachmentListQuestionResult](kasclient.kasattachmentlistquestionresult.md)

↳ [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

↳ [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [Frag-Nr.](kasclient.kasquestionresult.md#questionid)
* [questionTitle](kasclient.kasquestionresult.md#questiontitle)
* [questiontype](kasclient.kasquestionresult.md#questiontype)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="questionid"></a>

###  <a name="questionid"></a>Frag-Nr.

**● Frage**-Nr *`number`* .: = 0

Index der Frage

___

<a id="questiontitle"></a>

###  <a name="questiontitle"></a>questionTitle

**● questionTitle**: *`string`* = ""

Der Titel der Frage

___

<a id="questiontype"></a>

###  <a name="questiontype"></a>questiontype

**● questiontype**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType. None

Typ der Frage

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`any`*): [KASQuestionResult](kasclient.kasquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASQuestionResult](kasclient.kasquestionresult.md)

___

