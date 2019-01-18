---
ms.openlocfilehash: 35a77307e603499ebf73881ff861b61cb7d41e76
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728097"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormFlatSummary](../classes/kasclient.kasformflatsummary.md)

# <a name="class-kasformflatsummary"></a>Klasse: KASFormFlatSummary

## <a name="hierarchy"></a>Hierarchie

**KASFormFlatSummary**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [conversationId](kasclient.kasformflatsummary.md#conversationid)
* [formId](kasclient.kasformflatsummary.md#formid)
* [JSON](kasclient.kasformflatsummary.md#json)
### <a name="methods"></a>Methoden

* [getAllResponses](kasclient.kasformflatsummary.md#getallresponses)
* [getQuestionResponsesForUserId](kasclient.kasformflatsummary.md#getquestionresponsesforuserid)
* [getRespondedUserIds](kasclient.kasformflatsummary.md#getrespondeduserids)
* [getResponsesForUserId](kasclient.kasformflatsummary.md#getresponsesforuserid)
* [getTotalResponseCount](kasclient.kasformflatsummary.md#gettotalresponsecount)
* [fromJSON](kasclient.kasformflatsummary.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="conversationid"></a>

###  <a name="conversationid"></a>conversationId

**● ConversationId**: *`string`* = ""

Die Id des zugeordneten Unterhaltung sollte nicht geändert werden

___

<a id="formid"></a>

###  <a name="formid"></a>formId

**● FormId**: *`string`* = ""

Die Id des dem Formular zugeordneten sollte nicht geändert werden

___

<a id="json"></a>

###  <a name="json"></a>json

**● Json**:*`JSON`*

___

## <a name="methods"></a>Methoden

<a id="getallresponses"></a>

###  <a name="getallresponses"></a>getAllResponses

▸ **GetAllResponses**():`__type`

Dient zum Abrufen aller Antworten aller Benutzer

**Gibt:**`__type`

___

<a id="getquestionresponsesforuserid"></a>

###  <a name="getquestionresponsesforuserid"></a>getQuestionResponsesForUserId

▸ **GetQuestionResponsesForUserId**(Benutzer-ID: *`string`*, QuestionId: *`number`*): `string`]

Dient zum Abrufen aller Antworten eines Benutzers für eine bestimmte Frage

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  Die eindeutige Id des Benutzers |
| questionId | `number` |  die Id der Frage |

**Gibt:** `string`Liste aller Antworten für die Frage vom Benutzer angegebener]

___

<a id="getrespondeduserids"></a>

###  <a name="getrespondeduserids"></a>getRespondedUserIds

▸ **GetRespondedUserIds**(): `string`]

Ruft die Benutzer-Ids, die auf dem Formular reagiert

**Gibt:** `string`[] Liste mit allen geantwortet haben Benutzer-Ids

___

<a id="getresponsesforuserid"></a>

###  <a name="getresponsesforuserid"></a>getResponsesForUserId

▸ **GetResponsesForUserId**(Benutzer-ID: *`string`*):`__type`

Dient zum Abrufen aller Antworten eines Benutzers zu einem Formular

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  Die eindeutige Id des Benutzers |

**Gibt:** `__type` Frage-Id an, die Liste der Antworten

___

<a id="gettotalresponsecount"></a>

###  <a name="gettotalresponsecount"></a>getTotalResponseCount

▸ **GetTotalResponseCount**():`number`

Ruft alle Antworten von allen Benutzern Anzahl

**Gibt:** `number` Anzahl aller Antworten

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*, IsResponseAppended: *`boolean`*): [KASFormFlatSummary](kasclient.kasformflatsummary.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |
| isResponseAppended | `boolean` |

**Gibt:** [KASFormFlatSummary](kasclient.kasformflatsummary.md)

___

