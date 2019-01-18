---
ms.openlocfilehash: 5ea10ec4a326c6ae1ceaae4db8a2994d25e17fce
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728078"
---
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
* [serverPath](kasclient.kasattachment.md#serverpath)
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

**● AttachmentId**: *`string`* = ""

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

Die folgenden Zeichenfolgenschlüssel ("Ty", "Afn", "Asb" usw.) MUSS mit der Attachment-Objektmodell Darstellung in iOS und Android Code synchronisiert werden. Dies ist für die ordnungsgemäße Serialisierung und Deserialisierung wichtiger über die KAS-Brücke.

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

▸ **PopulateModelFromJSON**(Anlage: *[KASAttachment](kasclient.kasattachment.md)*, Object: *`JSON`*):`void`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Anlage | [KASAttachment](kasclient.kasattachment.md) |
| object | `JSON` |

**Gibt:**`void`

___

