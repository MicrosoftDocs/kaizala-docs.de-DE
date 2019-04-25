[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponse](../classes/kasclient.kasformresponse.md)

# <a name="class-kasformresponse"></a>Klasse: KASFormResponse

## <a name="hierarchy"></a>Hierarchie

**KASFormResponse**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [groupId](kasclient.kasformresponse.md#groupid)
* [groupName](kasclient.kasformresponse.md#groupname)
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

**● Groupi**: *`string`* = ""

Gruppen-ID

___

<a id="groupname"></a>

###  <a name="groupname"></a>groupName

**● GroupName**: *`string`* = ""

Group Name

___

<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

Eine eindeutige Antwort-ID, die bei der Aktualisierung einer vorhandenen Antwort erforderlich ist

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a>questionToAnswerMap

**● questionToAnswerMap**:*`object`*

Eine Karte der Frage-ID zur Antwort Dictionary<QuestionId: Number, Answer: string>
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

Respondername

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a>sendStatus

**● sendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus. Unknown

Sendestatus der Antwortnachricht

___

<a id="sendtime"></a>

###  <a name="sendtime"></a>Sendezeit

**● Sendezeit**: *`number`* = 0

Uhrzeit der Antwort Übermittlung

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a>serverToLocalAssetUrlMap

**● serverToLocalAssetUrlMap**:*`object`*

Eine Zuordnung für serverUrl für localUrl aller Bildanlagen an eine Antwort Dictionary<ServerUrl: String, LocalUrl: string>
#### <a name="type-declaration"></a>Typdeklaration

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASFormResponse](kasclient.kasformresponse.md)

___

