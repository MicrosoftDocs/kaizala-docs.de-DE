---
ms.openlocfilehash: a9a9a2cd7e5b561360668982dfcbba4e74bfe834
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728079"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASImageAttachment](../classes/kasclient.kasimageattachment.md)

# <a name="class-kasimageattachment"></a>Klasse: KASImageAttachment

## <a name="hierarchy"></a>Hierarchie

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASImageAttachment**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentId](kasclient.kasimageattachment.md#attachmentid)
* [fileName](kasclient.kasimageattachment.md#filename)
* [generateThumbnailServerUrl](kasclient.kasimageattachment.md#generatethumbnailserverurl)
* [hasSetThumbnail](kasclient.kasimageattachment.md#hassetthumbnail)
* [height](kasclient.kasimageattachment.md#height)
* [localPath](kasclient.kasimageattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasimageattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasimageattachment.md#serverpath)
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

**● AttachmentId**: *`string`* = ""

___

<a id="filename"></a>

###  <a name="filename"></a>fileName

**● FileName**: *`string`* = ""

___

<a id="generatethumbnailserverurl"></a>

###  <a name="generatethumbnailserverurl"></a>generateThumbnailServerUrl

**● GenerateThumbnailServerUrl**: *`boolean`* = False

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● HasSetThumbnail**: *`boolean`* = False

___

<a id="height"></a>

###  <a name="height"></a>height

**● Höhe**: *`number`* = 0

___

<a id="localpath"></a>

###  <a name="localpath"></a>localPath

**● LocalPath**: *`string`* = ""

___

<a id="requirehighresthumbnail"></a>

###  <a name="requirehighresthumbnail"></a>requireHighResThumbnail

**● RequireHighResThumbnail**: *`boolean`* = False

___

<a id="serverpath"></a>

###  <a name="serverpath"></a>serverPath

**● ServerPath**: *`string`* = ""

___

<a id="size"></a>

###  <a name="size"></a>size

**● Größe**: *`number`* = 0

___

<a id="thumbnail"></a>

###  <a name="thumbnail"></a>Miniaturansicht

**● Miniaturansicht**: *`string`* = ""

___

<a id="thumbnailserverurl"></a>

###  <a name="thumbnailserverurl"></a>thumbnailServerUrl

**● ThumbnailServerUrl**: *`string`* = ""

___

<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType.Image

___

<a id="width"></a>

###  <a name="width"></a>width

**● Breite**: *`number`* = 0

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASImageAttachment](kasclient.kasimageattachment.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASImageAttachment](kasclient.kasimageattachment.md)

___

<a id="haslocalpath"></a>

### <a name="static-haslocalpath"></a>`<Static>`hasLocalPath

▸ **HasLocalPath**(Obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| obj | [KASAttachment](kasclient.kasattachment.md) |

**Gibt:**`boolean`

___

<a id="hasserverpath"></a>

### <a name="static-hasserverpath"></a>`<Static>`hasServerPath

▸ **HasServerPath**(Obj: *[KASAttachment](kasclient.kasattachment.md)*):`boolean`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| obj | [KASAttachment](kasclient.kasattachment.md) |

**Gibt:**`boolean`

___

<a id="populatemodelfromjson"></a>

### <a name="static-populatemodelfromjson"></a>`<Static>`populateModelFromJSON

▸ **PopulateModelFromJSON**(Anlage: *[KASImageAttachment](kasclient.kasimageattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Anlage | [KASImageAttachment](kasclient.kasimageattachment.md) |
| object | `JSON` |

**Gibt:**`void`

___

