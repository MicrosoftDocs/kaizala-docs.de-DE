[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAudioAttachment](../classes/kasclient.kasaudioattachment.md)

# <a name="class-kasaudioattachment"></a>Klasse: KASAudioAttachment

## <a name="hierarchy"></a>Hierarchie

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASAudioAttachment**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentId](kasclient.kasaudioattachment.md#attachmentid)
* [duration](kasclient.kasaudioattachment.md#duration)
* [fileName](kasclient.kasaudioattachment.md#filename)
* [hasSetThumbnail](kasclient.kasaudioattachment.md#hassetthumbnail)
* [LocalPath](kasclient.kasaudioattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasaudioattachment.md#requirehighresthumbnail)
* [Direktive ServerPath existiert](kasclient.kasaudioattachment.md#serverpath)
* [size](kasclient.kasaudioattachment.md#size)
* [thumbnail](kasclient.kasaudioattachment.md#thumbnail)
* [type](kasclient.kasaudioattachment.md#type)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasaudioattachment.md#tojson)
* [fromJSON](kasclient.kasaudioattachment.md#fromjson)
* [hasLocalPath](kasclient.kasaudioattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasaudioattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasaudioattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● Attachment**-Nr *`string`* : = ""

___
<a id="duration"></a>

###  <a name="duration"></a>duration

**● Dauer**: *`number`* = 0

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

###  <a name="localpath"></a>LocalPath

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

**● Thumbnail**: *`string`* = ""

___
<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType. Image

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASAttachment](kasclient.kasattachment.md)

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

▸ **populateModelFromJSON**(Attachment: *[KASAudioAttachment](kasclient.kasaudioattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| attachment | [KASAudioAttachment](kasclient.kasaudioattachment.md) |
| Objekt | `JSON` |

**Gibt Folgendes zurück:**`void`

___

