[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachment](../classes/kasclient.kasattachment.md)

# <a name="class-kasattachment"></a>Klasse: KASAttachment

## <a name="hierarchy"></a>Hierarchie

**KASAttachment**

↳ [KASAudioAttachment](kasclient.kasaudioattachment.md)

↳ [KASImageAttachment](kasclient.kasimageattachment.md)

↳ [KASVideoAttachment](kasclient.kasvideoattachment.md)

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentId](kasclient.kasattachment.md#attachmentid)
* [fileName](kasclient.kasattachment.md#filename)
* [hasSetThumbnail](kasclient.kasattachment.md#hassetthumbnail)
* [localPath](kasclient.kasattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasattachment.md#requirehighresthumbnail)
* [Direktive ServerPath existiert](kasclient.kasattachment.md#serverpath)
* [size](kasclient.kasattachment.md#size)
* [thumbnail](kasclient.kasattachment.md#thumbnail)
* [type](kasclient.kasattachment.md#type)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasattachment.md#tojson)
* [fromJSON](kasclient.kasattachment.md#fromjson)
* [hasLocalPath](kasclient.kasattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● Attachment**-Nr *`string`* .: = ""

___

<a id="filename"></a>

###  <a name="filename"></a>fileName

**● filename**: *`string`* = ""

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● hasSetThumbnail**: *`boolean`* = false

___

<a id="localpath"></a>

###  <a name="localpath"></a>localPath

**● LocalPath**: *`string`* = ""

___

<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a>requireHighResThumbnail

**● requireHighResThumbnail**: *`boolean`* = false

___

<a id="serverpath"></a>

###  <a name="serverpath"></a>Direktive ServerPath existiert

**● Direktive ServerPath existiert**: *`string`* = ""

___

<a id="size"></a>

###  <a name="size"></a>size

**● Größe**: *`number`* = 0

___

<a id="thumbnail"></a>

###  <a name="thumbnail"></a>Miniaturansicht

**● Miniaturansicht**: *`string`* = ""

___

<a id="type"></a>

###  <a name="type"></a>Typ

**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType. Image

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

Die folgenden Zeichenfolgenschlüssel ("Ty", "AFN", "ASB" usw.) MUSS mit der Darstellung des Attachment-Objektmodells in iOS-und Android-Code synchronisiert sein. Dies ist für eine ordnungsgemäße Serialisierung und Deserialisierung über die KAS-Brücke unerlässlich.

**Gibt Folgendes zurück:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`any`*): [KASAttachment](kasclient.kasattachment.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASAttachment](kasclient.kasattachment.md)

___

<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a>`<Static>`hasLocalPath

▸ **hasLocalPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| obj | [KASAttachment](kasclient.kasattachment.md) |

**Gibt Folgendes zurück:**`boolean`

___

<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a>`<Static>`hasServerPath

▸ **hasServerPath**(obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| obj | [KASAttachment](kasclient.kasattachment.md) |

**Gibt Folgendes zurück:**`boolean`

___

<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a>`<Static>`populateModelFromJSON

▸ **populateModelFromJSON**(Attachment: *[KASAttachment](kasclient.kasattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| attachment | [KASAttachment](kasclient.kasattachment.md) |
| Objekt | `JSON` |

**Gibt Folgendes zurück:**`void`

___

