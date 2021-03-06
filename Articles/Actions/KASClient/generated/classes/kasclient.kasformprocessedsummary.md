[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProcessedSummary](../classes/kasclient.kasformprocessedsummary.md)

# <a name="class-kasformprocessedsummary"></a>Klasse: KASFormProcessedSummary

## <a name="hierarchy"></a>Hierarchie

**KASFormProcessedSummary**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [JSON](kasclient.kasformprocessedsummary.md#json)
* [nonRespondersInConversation](kasclient.kasformprocessedsummary.md#nonrespondersinconversation)
* [Ergebnisse](kasclient.kasformprocessedsummary.md#results)
* [targetResponderCount](kasclient.kasformprocessedsummary.md#targetrespondercount)
* [totalResponseCount](kasclient.kasformprocessedsummary.md#totalresponsecount)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasformprocessedsummary.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___
<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a>nonRespondersInConversation

**● nonRespondersInConversation**: * `string`[]* = []

Wie viele in der Unterhaltung nicht antworteten

___
<a id="results"></a>

###  <a name="results"></a>results

**● Ergebnisse**:*`object`*

Aggregiertes Ergebnis für das Wörterbuch<fragwürdigen Aggregations Fragen: Number, result: KASQuestionResult>
#### <a name="type-declaration"></a>Typdeklaration

___
<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● targetResponderCount**: *`number`* = 0

Wie viele in der Unterhaltung zugewiesen wurden, um auf dieses Formular zu Antworten

___
<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● totalResponseCount**: *`number`* = 0

Wie viele Antworten insgesamt für das Formular empfangen wurden, wobei mehrere Antworten von einer Person berücksichtigt wurden

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`JSON`*:): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |

**Gibt Folgendes zurück:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

___

