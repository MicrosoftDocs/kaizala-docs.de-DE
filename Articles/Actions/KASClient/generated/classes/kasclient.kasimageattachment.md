[](../README.md) > [KASClient](../modules/kasclient.md) > [KASImageAttachment](../classes/kasclient.kasimageattachment.md)

# <a name="class-kasimageattachment"></a>Klasse: KASImageAttachment

## <a name="hierarchy"></a>Hierarchie

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASImageAttachment**

↳ [KASRichImageAttachment](kasclient.kasrichimageattachment.md)

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentId](kasclient.kasimageattachment.md#attachmentid)
* [fileName](kasclient.kasimageattachment.md#filename)
* [generateThumbnailServerUrl](kasclient.kasimageattachment.md#generatethumbnailserverurl)
* [hasSetThumbnail](kasclient.kasimageattachment.md#hassetthumbnail)
* [height](kasclient.kasimageattachment.md#height)
* [LocalPath](kasclient.kasimageattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasimageattachment.md#requirehighresthumbnail)
* [Direktive ServerPath existiert](kasclient.kasimageattachment.md#serverpath)
* [size](kasclient.kasimageattachment.md#size)
* [thumbnail](kasclient.kasimageattachment.md#thumbnail)
* [thumbnailServerUrl](kasclient.kasimageattachment.md#thumbnailserverurl)
* [type](kasclient.kasimageattachment.md#type)
* [width](kasclient.kasimageattachment.md#width)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasimageattachment.md#tojson)
* [fromJSON](kasclient.kasimageattachment.md#fromjson)
* [hasLocalPath](kasclient.kasimageattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasimageattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasimageattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● Attachment**-Nr *`string`* : = ""

___
<a id="filename"></a>

###  <a name="filename"></a>fileName

**● filename**: *`string`* = ""

___
<a id="generatethumbnailserverurl"></a>

###  <a name="generatethumbnailserverurl"></a>generateThumbnailServerUrl

**● generateThumbnailServerUrl**: *`boolean`* = false

___
<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● hasSetThumbnail**: *`boolean`* = false

___
<a id="height"></a>

###  <a name="height"></a>height

**● Höhe**: *`number`* = 0

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
<a id="thumbnailserverurl"></a>

###  <a name="thumbnailserverurl"></a>thumbnailServerUrl

**● thumbnailServerUrl**: *`string`* = ""

___
<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType. Image

___
<a id="width"></a>

###  <a name="width"></a>width

**● Breite**: *`number`* = 0

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`any`*:): [KASImageAttachment](kasclient.kasimageattachment.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASImageAttachment](kasclient.kasimageattachment.md)

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

▸ **populateModelFromJSON**(Attachment: *[KASImageAttachment](kasclient.kasimageattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| attachment | [KASImageAttachment](kasclient.kasimageattachment.md) |
| Objekt | `JSON` |

**Gibt Folgendes zurück:**`void`

___

