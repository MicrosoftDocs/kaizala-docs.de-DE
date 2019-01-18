---
ms.openlocfilehash: 7d76c2a5eae67bd6c1063b2595561e299f9f9160
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728052"
---
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

**● Json**:*`JSON`*

___

<a id="nonrespondersinconversation"></a>

###  <a name="nonrespondersinconversation"></a>nonRespondersInConversation

**● NonRespondersInConversation**: * `string`[]* =]

Wie viele in der Unterhaltung hat nicht geantwortet

___

<a id="results"></a>

###  <a name="results"></a>Ergebnisse

**● Ergebnisse**:*`object`*

Ergebnis für aggregative Fragen Dictionary<QuestionId aggregiert: number, Ergebnis: KASQuestionResult>
#### <a name="type-declaration"></a>Typdeklaration

___

<a id="targetrespondercount"></a>

###  <a name="targetrespondercount"></a>targetResponderCount

**● TargetResponderCount**: *`number`* = 0

Wie viele in der Unterhaltung zugewiesen wurden, um auf dieses Formular zu reagieren

___

<a id="totalresponsecount"></a>

###  <a name="totalresponsecount"></a>totalResponseCount

**● TotalResponseCount**: *`number`* = 0

Wie viele gesamtantworten für das Formular, erwägen mehrere Antworten von einer Person empfangen wurden

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`JSON`*): [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `JSON` |

**Gibt:** [KASFormProcessedSummary](kasclient.kasformprocessedsummary.md)

___

