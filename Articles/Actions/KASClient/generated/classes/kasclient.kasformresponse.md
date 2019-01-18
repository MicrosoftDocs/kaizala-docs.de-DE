---
ms.openlocfilehash: 84e9530593e8850a0cf354ae2e07c77e0b68db75
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728059"
---
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
* [<ui>sendTime</ui>](kasclient.kasformresponse.md#sendtime)
* [serverToLocalAssetUrlMap](kasclient.kasformresponse.md#servertolocalasseturlmap)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasformresponse.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="groupid"></a>

###  <a name="groupid"></a>groupId

**● GroupId**: *`string`* = ""

Gruppen-id

___

<a id="groupname"></a>

###  <a name="groupname"></a>groupName

**● GroupName**: *`string`* = ""

Gruppenname

___

<a id="id"></a>

###  <a name="id"></a>id

**●-Id**: *`string`* = ""

Eine eindeutige Antwort-Id, die im Fall eines WAN-aktualisieren eine vorhandene Antwort erforderlich

___

<a id="questiontoanswermap"></a>

###  <a name="questiontoanswermap"></a>questionToAnswerMap

**● QuestionToAnswerMap**:*`object`*

Eine Zuordnung der Frage Id Dictionary<QuestionId beantworten: number, Antwort: String>
#### <a name="type-declaration"></a>Typdeklaration

___

<a id="responderid"></a>

###  <a name="responderid"></a>responderId

**● ResponderId**: *`string`* = ""

Responder-id

___

<a id="respondername"></a>

###  <a name="respondername"></a>responderName

**● ResponderName**: *`string`* = ""

Responder name

___

<a id="sendstatus"></a>

###  <a name="sendstatus"></a>sendStatus

**● SendStatus**: *[KASFormMessageSendStatus](../enums/kasclient.kasformmessagesendstatus.md)* = KASFormMessageSendStatus.Unknown

Status der Antwort-Nachricht senden

___

<a id="sendtime"></a>

###  <a name="sendtime"></a>sendTime

**● SendTime**: *`number`* = 0

Antwortzeit senden

___

<a id="servertolocalasseturlmap"></a>

###  <a name="servertolocalasseturlmap"></a>serverToLocalAssetUrlMap

**● ServerToLocalAssetUrlMap**:*`object`*

Eine Zuordnung für ServerUrl gegen localURL im aller Anlagen Bild für eine Antwort Dictionary<ServerUrl: string, localURL im: String>
#### <a name="type-declaration"></a>Typdeklaration

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASFormResponse](kasclient.kasformresponse.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASFormResponse](kasclient.kasformresponse.md)

___

