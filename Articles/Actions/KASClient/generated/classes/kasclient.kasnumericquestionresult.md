[](../README.md) > [KASClient](../modules/kasclient.md) > [KASNumericQuestionResult](../classes/kasclient.kasnumericquestionresult.md)

# <a name="class-kasnumericquestionresult"></a>Klasse: KASNumericQuestionResult

## <a name="hierarchy"></a>Hierarchie

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASNumericQuestionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [durchschnittliche](kasclient.kasnumericquestionresult.md#average)
* [Frag-Nr.](kasclient.kasnumericquestionresult.md#questionid)
* [questionTitle](kasclient.kasnumericquestionresult.md#questiontitle)
* [questiontype](kasclient.kasnumericquestionresult.md#questiontype)
* [Summe](kasclient.kasnumericquestionresult.md#sum)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasnumericquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="average"></a>

###  <a name="average"></a>durchschnittliche

**● Durchschnitt**: *`number`* = 0

___

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

<a id="sum"></a>

###  <a name="sum"></a>Summe

**● Sum**: *`number`* = 0

Für numerische Fragen ist das aggregierte Ergebnis Sum und der Mittelwert aller Antworten

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`any`*): [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASNumericQuestionResult](kasclient.kasnumericquestionresult.md)

___

