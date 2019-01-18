---
ms.openlocfilehash: 7bc58e96d292d72dd01e77d55d38f07450021e6b
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728075"
---
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
* [localPath](kasclient.kasaudioattachment.md#localpath)
* [requireHighResThumbnail](kasclient.kasaudioattachment.md#requirehighresthumbnail)
* [serverPath](kasclient.kasaudioattachment.md#serverpath)
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

▸ **PopulateModelFromJSON**(Anlage: *[KASAudioAttachment](kasclient.kasaudioattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Anlage | [KASAudioAttachment](kasclient.kasaudioattachment.md) |
| object | `JSON` |

**Gibt:**`void`

___

