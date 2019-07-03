[](../README.md) > [KASClient](../modules/kasclient.md) > [KASConversationDetails](../classes/kasclient.kasconversationdetails.md)

# <a name="class-kasconversationdetails"></a>Klasse: KASConversationDetails

Definiert Details der Host-und Quell Unterhaltung
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
* [isHostGroupDiscoverable](kasclient.kasconversationdetails.md#ishostgroupdiscoverable)
* [isSourceGroupDiscoverable](kasclient.kasconversationdetails.md#issourcegroupdiscoverable)
* [sourceConversationId](kasclient.kasconversationdetails.md#sourceconversationid)
* [sourceConversationTitle](kasclient.kasconversationdetails.md#sourceconversationtitle)
* [sourceConversationType](kasclient.kasconversationdetails.md#sourceconversationtype)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasconversationdetails.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="currentuserid"></a>

###  <a name="currentuserid"></a>currentUserId

**● currentUserId**: *`string`* = ""

___
<a id="currentuserroleinhostconversation"></a>

###  <a name="currentuserroleinhostconversation"></a>currentUserRoleInHostConversation

**● currentUserRoleInHostConversation**: *[KASParticipantRole](../enums/kasclient.kasparticipantrole.md)* = KASParticipantRole. None

___
<a id="hostconversationid"></a>

###  <a name="hostconversationid"></a>hostConversationId

**● hostConversationId**: *`string`* = ""

___
<a id="hostconversationparticipantsmap"></a>

###  <a name="hostconversationparticipantsmap"></a>hostConversationParticipantsMap

**● hostConversationParticipantsMap**:*`object`*

#### <a name="type-declaration"></a>Typdeklaration

___
<a id="hostconversationtitle"></a>

###  <a name="hostconversationtitle"></a>hostConversationTitle

**● hostConversationTitle**: *`string`* = ""

___
<a id="hostconversationtype"></a>

###  <a name="hostconversationtype"></a>hostConversationType

**● hostConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType. None

___
<a id="ishostgroupdiscoverable"></a>

###  <a name="ishostgroupdiscoverable"></a>isHostGroupDiscoverable

**● isHostGroupDiscoverable**: *`boolean`* = false

___
<a id="issourcegroupdiscoverable"></a>

###  <a name="issourcegroupdiscoverable"></a>isSourceGroupDiscoverable

**● isSourceGroupDiscoverable**: *`boolean`* = false

___
<a id="sourceconversationid"></a>

###  <a name="sourceconversationid"></a>sourceConversationId

**● sourceConversationId**: *`string`* = ""

___
<a id="sourceconversationtitle"></a>

###  <a name="sourceconversationtitle"></a>sourceConversationTitle

**● sourceConversationTitle**: *`string`* = ""

___
<a id="sourceconversationtype"></a>

###  <a name="sourceconversationtype"></a>sourceConversationType

**● sourceConversationType**: *[KASFormConversationType](../enums/kasclient.kasformconversationtype.md)* = KASFormConversationType. None

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASConversationDetails](kasclient.kasconversationdetails.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASConversationDetails](kasclient.kasconversationdetails.md)

___

