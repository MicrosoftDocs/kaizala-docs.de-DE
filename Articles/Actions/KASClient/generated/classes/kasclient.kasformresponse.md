[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)

# <a name="class-kasformresponse"></a>Klasse: KASFormResponse

## <a name="hierarchy"></a>Hierarchie

**KASFormResponse**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [groupId](kasclient.kasformresponse.md#groupid)
* [GroupName](kasclient.kasformresponse.md#groupname)
* [id](kasclient.kasformresponse.md#id)
* [questionToAnswerMap](kasclient.kasformresponse.md#questiontoanswermap)
* [responderId](kasclient.kasformresponse.md#responderid)
* [responderName](kasclient.kasformresponse.md#respondername)
* [sendStatus](kasclient.kasformresponse.md#sendstatus)
* [Sendezeit](kasclient.kasformresponse.md#sendtime)
* [serverToLocalAssetUrlMap](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="groupid"></a>

###  <a name="groupid"></a>groupId

**● Gruppen**-Nr *`string`* : = ""

Gruppen-ID

___
<a id="groupname"></a>

###  <a name="groupname"></a>GroupName

**● GroupName**: *`string`* = ""

Group Name

___
<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

Eine eindeutige Antwort-ID, die für den Fall einer Aktualisierung einer vorhandenen Antwort erforderlich ist

___
<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a>questionToAnswerMap

**● questionToAnswerMap**:*`object`*

Eine Zuordnung der Frage-ID zum beantworten des Wörterbuchs<fragwürdig: Number, Answer: String>
#### <a name="type-declaration"></a>Typdeklaration

___
<a id="responderid"></a>

###  <a name="responderid"></a>responderId

**● responderId**: *`string`* = ""

Responder-ID

___
<a id="respondername"></a>

###  <a name="respondername"></a>responderName

**● responderName**: *`string`* = ""

Name des Responders

___
<a id="sendstatus"></a>

###  <a name="sendstatus"></a>sendStatus

**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus. Unknown

Status der Antwortnachricht senden

___
<a id="sendtime"></a>

###  <a name="sendtime"></a>Sendezeit

**● Sendezeit**: *`number`* = 0

Antwort Sende Zeit

___
<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a>serverToLocalAssetUrlMap

**● serverToLocalAssetUrlMap**:*`object`*

Eine Zuordnung für serverUrl gegen localUrl aller Bildanlagen zu einem Antwort Wörterbuch<serverUrl: String, localUrl: String>
#### <a name="type-declaration"></a>Typdeklaration

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASFormResponse](kasclient.kasformresponse.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASFormResponse](kasclient.kasformresponse.md)

___

