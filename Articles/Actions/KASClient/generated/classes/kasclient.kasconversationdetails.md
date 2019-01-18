---
ms.openlocfilehash: 2462effb40cd9759a8822cc8dcc09834fcef727b
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728102"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASConversationDetails](../classes/kasclient.kasconversationdetails.md)

# <a name="class-kasconversationdetails"></a>Klasse: KASConversationDetails

Details der Host und Quelle Unterhaltung definiert
## <a name="hierarchy"></a>Hierarchie

**KASConversationDetails**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [currentUserId](kasclient.kasconversationdetails.md#currentuserid)
* [currentUserRoleInHostConversation](kasclient.kasconversationdetails.md#currentuserroleinhostconversation)
* [hostConversationId](kasclient.kasconversationdetails.md#hostconversationid)
* [hostConversationParticipantsMap](kasclient.kasconversationdetails.md#hostconversationparticipantsmap)
* [hostConversationTitle](kasclient.kasconversationdetails.md#hostconversationtitle)
* [hostConversationType](kasclient.kasconversationdetails.md#hostconversationtype)
* [sourceConversationId](kasclient.kasconversationdetails.md#sourceconversationid)
* [sourceConversationTitle](kasclient.kasconversationdetails.md#sourceconversationtitle)
* [sourceConversationType](kasclient.kasconversationdetails.md#sourceconversationtype)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasconversationdetails.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="currentuserid"></a>

###  <a name="currentuserid"></a>currentUserId

**● CurrentUserId**: *`string`* = ""

___

<a id="currentuserroleinhostconversation"></a>

###  <a name="currentuserroleinhostconversation"></a>currentUserRoleInHostConversation

**● CurrentUserRoleInHostConversation**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole.NONE

___

<a id="hostconversationid"></a>

###  <a name="hostconversationid"></a>hostConversationId

**● HostConversationId**: *`string`* = ""

___

<a id="hostconversationparticipantsmap"></a>

###  <a name="hostconversationparticipantsmap"></a>hostConversationParticipantsMap

**● HostConversationParticipantsMap**:*`object`*

#### <a name="type-declaration"></a>Typdeklaration

___

<a id="hostconversationtitle"></a>

###  <a name="hostconversationtitle"></a>hostConversationTitle

**● HostConversationTitle**: *`string`* = ""

___

<a id="hostconversationtype"></a>

###  <a name="hostconversationtype"></a>hostConversationType

**● HostConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType.NONE

___

<a id="sourceconversationid"></a>

###  <a name="sourceconversationid"></a>sourceConversationId

**● SourceConversationId**: *`string`* = ""

___

<a id="sourceconversationtitle"></a>

###  <a name="sourceconversationtitle"></a>sourceConversationTitle

**● SourceConversationTitle**: *`string`* = ""

___

<a id="sourceconversationtype"></a>

###  <a name="sourceconversationtype"></a>sourceConversationType

**● SourceConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType.NONE

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASConversationDetails](kasclient.kasconversationdetails.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASConversationDetails](kasclient.kasconversationdetails.md)

___

