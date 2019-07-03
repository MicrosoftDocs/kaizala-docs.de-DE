[](../README.md) > [KASClient](../modules/kasclient.md) > [KASOptionQuestionResult](../classes/kasclient.kasoptionquestionresult.md)

# <a name="class-kasoptionquestionresult"></a>Klasse: KASOptionQuestionResult

## <a name="hierarchy"></a>Hierarchie

 [KASQuestionResult](kasclient.kasquestionresult.md)

**↳ KASOptionQuestionResult**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [optionResults](kasclient.kasoptionquestionresult.md#optionresults)
* [Fragen-Nr](kasclient.kasoptionquestionresult.md#questionid)
* [questionTitle](kasclient.kasoptionquestionresult.md#questiontitle)
* [questiontype](kasclient.kasoptionquestionresult.md#questiontype)
### <a name="methods"></a>Methoden

* [getResultsOrder](kasclient.kasoptionquestionresult.md#getresultsorder)
* [fromJSON](kasclient.kasoptionquestionresult.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="optionresults"></a>

###  <a name="optionresults"></a>optionResults

**● optionResults**:*`object`*

Für SingleSelect/MultiSelect-Frage ist das Ergebnis die Options-ID im Vergleich zu Ihrem Counts-Wörterbuch<Optionskennung: Number, OptionResult: KASOptionResult>
#### <a name="type-declaration"></a>Typdeklaration

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

## <a name="methods"></a>Methoden

<a id="getresultsorder"></a>

###  <a name="getresultsorder"></a>getResultsOrder

▸ **getResultsOrder**(): `number`[]

Ruft alle Options-IDs ab, die in der Gesamtanzahl der Antworten sortiert sind (absteigend).

**Gibt Folgendes zurück:** `number`[] Liste aller Options-IDs

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASOptionQuestionResult](kasclient.kasoptionquestionresult.md)

___

