[](../README.md) > [KASClient](../modules/kasclient.md) > [KASRichImageAttachment](../classes/kasclient.kasrichimageattachment.md)

# <a name="class-kasrichimageattachment"></a>Klasse: KASRichImageAttachment

## <a name="hierarchy"></a>Hierarchie

↳ [KASImageAttachment](kasclient.kasimageattachment.md)

**↳ KASRichImageAttachment**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentId](kasclient.kasrichimageattachment.md#attachmentid)
* [fileName](kasclient.kasrichimageattachment.md#filename)
* [generateThumbnailServerUrl](kasclient.kasrichimageattachment.md#generatethumbnailserverurl)
* [hasSetThumbnail](kasclient.kasrichimageattachment.md#hassetthumbnail)
* [height](kasclient.kasrichimageattachment.md#height)
* [id](kasclient.kasrichimageattachment.md#id)
* [LocalPath](kasclient.kasrichimageattachment.md#localpath)
* [metadataFetchState](kasclient.kasrichimageattachment.md#metadatafetchstate)
* [ocrData](kasclient.kasrichimageattachment.md#ocrdata)
* [processedOCRData](kasclient.kasrichimageattachment.md#processedocrdata)
* [requireHighResThumbnail](kasclient.kasrichimageattachment.md#requirehighresthumbnail)
* [Direktive ServerPath existiert](kasclient.kasrichimageattachment.md#serverpath)
* [size](kasclient.kasrichimageattachment.md#size)
* [thumbnail](kasclient.kasrichimageattachment.md#thumbnail)
* [thumbnailServerUrl](kasclient.kasrichimageattachment.md#thumbnailserverurl)
* [type](kasclient.kasrichimageattachment.md#type)
* [width](kasclient.kasrichimageattachment.md#width)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasrichimageattachment.md#tojson)
* [fromJSON](kasclient.kasrichimageattachment.md#fromjson)
* [hasLocalPath](kasclient.kasrichimageattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasrichimageattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasrichimageattachment.md#populatemodelfromjson)

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
<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = NULL

___
<a id="localpath"></a>

###  <a name="localpath"></a>LocalPath

**● LocalPath**: *`string`* = ""

___
<a id="metadatafetchstate"></a>

###  <a name="metadatafetchstate"></a>metadataFetchState

**● metadataFetchState**: *[ImageMetadataFetchState](../enums/kasclient.imagemetadatafetchstate.md)* = ImageMetadataFetchState. initiiert

___
<a id="ocrdata"></a>

###  <a name="ocrdata"></a>ocrData

**● ocrData**: *`string`* = NULL

___
<a id="processedocrdata"></a>

###  <a name="processedocrdata"></a>processedOCRData

**● processedOCRData**: *`string`* = NULL

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

▸- **fromJSON**(Objekt *`any`*:): [KASRichImageAttachment](kasclient.kasrichimageattachment.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `any` |

**Gibt Folgendes zurück:** [KASRichImageAttachment](kasclient.kasrichimageattachment.md)

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

▸ **populateModelFromJSON**(Attachment: *[KASRichImageAttachment](kasclient.kasrichimageattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| attachment | [KASRichImageAttachment](kasclient.kasrichimageattachment.md) |
| Objekt | `JSON` |

**Gibt Folgendes zurück:**`void`

___

