---
ms.openlocfilehash: 7cdf9928a0c6bc5312d2a29a31190b9374664d09
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728060"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASVideoAttachment](../classes/kasclient.kasvideoattachment.md)

# <a name="class-kasvideoattachment"></a>Klasse: KASVideoAttachment

## <a name="hierarchy"></a>Hierarchie

 [KASAttachment](kasclient.kasattachment.md)

**↳ KASVideoAttachment**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentId](kasclient.kasvideoattachment.md#attachmentid)
* [duration](kasclient.kasvideoattachment.md#duration)
* [fileName](kasclient.kasvideoattachment.md#filename)
* [hasSetThumbnail](kasclient.kasvideoattachment.md#hassetthumbnail)
* [localPath](kasclient.kasvideoattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasvideoattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasvideoattachment.md#serverpath)
* [size](kasclient.kasvideoattachment.md#size)
* [streamingPath](kasclient.kasvideoattachment.md#streamingpath)
* [thumbnail](kasclient.kasvideoattachment.md#thumbnail)
* [type](kasclient.kasvideoattachment.md#type)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasvideoattachment.md#tojson)
* [fromJSON](kasclient.kasvideoattachment.md#fromjson)
* [hasLocalPath](kasclient.kasvideoattachment.md#haslocalpath)
* [hasServerPath](kasclient.kasvideoattachment.md#hasserverpath)
* [populateModelFromJSON](kasclient.kasvideoattachment.md#populatemodelfromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentid"></a>

###  <a name="attachmentid"></a>attachmentId

**● AttachmentId**: *`string`* = ""

___

<a id="duration"></a>

###  <a name="duration"></a>duration

**● Dauer**: *`number`* = 0

___

<a id="filename"></a>

###  <a name="filename"></a>fileName

**● FileName**: *`string`* = ""

___

<a id="hassetthumbnail"></a>

###  <a name="hassetthumbnail"></a>hasSetThumbnail

**● HasSetThumbnail**: *`boolean`* = False

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

<a id="streamingpath"></a>

###  <a name="streamingpath"></a>streamingPath

**● StreamingPath**: *`string`* = ""

___

<a id="thumbnail"></a>

###  <a name="thumbnail"></a>Miniaturansicht

**● Miniaturansicht**: *`string`* = ""

___

<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASAttachmentType](../enums/kasclient.kasattachmenttype.md)* = KASAttachmentType.Image

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASAttachment](kasclient.kasattachment.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASAttachment](kasclient.kasattachment.md)

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

▸ **PopulateModelFromJSON**(Anlage: *[KASVideoAttachment](kasclient.kasvideoattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Anlage | [KASVideoAttachment](kasclient.kasvideoattachment.md) |
| object | `JSON` |

**Gibt:**`void`

___

