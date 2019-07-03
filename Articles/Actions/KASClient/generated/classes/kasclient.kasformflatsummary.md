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

**● Conversation**-Nr *`string`* : = ""

Die ID der zugeordneten Unterhaltung sollte nicht geändert werden

___
<a id="formid"></a>

###  <a name="formid"></a>formId

**● Formular**-Nr *`string`* : = ""

Die ID des zugeordneten Formulars sollte nicht geändert werden.

___
<a id="json"></a>

###  <a name="json"></a>json

**● JSON**:*`JSON`*

___

## <a name="methods"></a>Methoden

<a id="getallresponses"></a>

###  <a name="getallresponses"></a>getAllResponses

▸ **getAllResponses**():`__type`

Ruft alle Antworten aller Benutzer ab.

**Gibt Folgendes zurück:**`__type`

___
<a id="getquestionresponsesforuserid"></a>

###  <a name="getquestionresponsesforuserid"></a>getQuestionResponsesForUserId

▸ **getQuestionResponsesForUserId**(UserID: *`string`*, question ID: *`number`*): `string`[]

Ruft alle Antworten eines Benutzers gegen eine bestimmte Frage ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  die eindeutige ID des Benutzers |
| Fragen-Nr | `number` |  die ID der Frage |

**Gibt Folgendes zurück:** `string`[] Liste aller Antworten, die der Benutzer für diese Frage angegeben hat.

___
<a id="getrespondeduserids"></a>

###  <a name="getrespondeduserids"></a>getRespondedUserIds

▸ **getRespondedUserIds**(): `string`[]

Ruft alle Benutzer-IDs ab, die auf das Formular geantwortet haben.

**Gibt Folgendes zurück:** `string`[] Liste aller geantworteten Benutzer-IDs

___
<a id="getresponsesforuserid"></a>

###  <a name="getresponsesforuserid"></a>getResponsesForUserId

▸ **getResponsesForUserId**(UserID: *`string`*):`__type`

Ruft alle Antworten eines Benutzers in ein Formular ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  die eindeutige ID des Benutzers |

**Gibt Folgendes zurück:** `__type` Frage-ID zur Liste der Antworten

___
<a id="gettotalresponsecount"></a>

###  <a name="gettotalresponsecount"></a>getTotalResponseCount

▸ **getTotalResponseCount**():`number`

Ruft die Anzahl aller Antworten aller Benutzer ab.

**Gibt Folgendes zurück:** `number` Anzahl aller Antworten

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`any`*, isResponseAppended: *`boolean`*): [KASFormFlatSummary](kasclient.kasformflatsummary.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |
| isResponseAppended | `boolean` |

**Gibt Folgendes zurück:** [KASFormFlatSummary](kasclient.kasformflatsummary.md)

___

