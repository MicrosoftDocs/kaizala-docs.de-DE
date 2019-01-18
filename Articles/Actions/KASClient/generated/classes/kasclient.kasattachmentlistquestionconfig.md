---
ms.openlocfilehash: e2101c72f8bcbc3156b5322139bdea66df77add9
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728098"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASAttachmentListQuestionConfig](../classes/kasclient.kasattachmentlistquestionconfig.md)

# <a name="class-kasattachmentlistquestionconfig"></a>Klasse: KASAttachmentListQuestionConfig

## <a name="hierarchy"></a>Hierarchie

 [KASQuestionConfig](kasclient.kasquestionconfig.md)

**↳ KASAttachmentListQuestionConfig**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [attachmentListType](kasclient.kasattachmentlistquestionconfig.md#attachmentlisttype)
* [defaultCameraFilterMode](kasclient.kasattachmentlistquestionconfig.md#defaultcamerafiltermode)
* [imageSource](kasclient.kasattachmentlistquestionconfig.md#imagesource)
* [maxImageCount](kasclient.kasattachmentlistquestionconfig.md#maximagecount)
* [pageBreakEnabled](kasclient.kasattachmentlistquestionconfig.md#pagebreakenabled)
* [ATTACHMENT_LIST_TYPE](kasclient.kasattachmentlistquestionconfig.md#attachment_list_type)
* [DEFAULT_CAMERA_FILTER_MODE](kasclient.kasattachmentlistquestionconfig.md#default_camera_filter_mode)
* [IMAGE_SOURCE_KEY](kasclient.kasattachmentlistquestionconfig.md#image_source_key)
* [MAX_IMAGE_COUNT_KEY](kasclient.kasattachmentlistquestionconfig.md#max_image_count_key)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasattachmentlistquestionconfig.md#tojson)
* [fromJSON](kasclient.kasattachmentlistquestionconfig.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="attachmentlisttype"></a>

###  <a name="attachmentlisttype"></a>attachmentListType

**● AttachmentListType**: *[AttachmentListResponseType](../enums/kasclient.attachmentlistresponsetype.md)* = AttachmentListResponseType.GENERIC

___

<a id="defaultcamerafiltermode"></a>

###  <a name="defaultcamerafiltermode"></a>defaultCameraFilterMode

**● DefaultCameraFilterMode**: *[CameraFilterMode](../enums/kasclient.camerafiltermode.md)* = CameraFilterMode.Photo

___

<a id="imagesource"></a>

###  <a name="imagesource"></a>imageSource

**● ImageSource**: *[ImagePickerSource](../enums/kasclient.imagepickersource.md)* = ImagePickerSource.All

___

<a id="maximagecount"></a>

###  <a name="maximagecount"></a>maxImageCount

**● MaxImageCount**: *`number`* = 10

___

<a id="pagebreakenabled"></a>

###  <a name="pagebreakenabled"></a>pageBreakEnabled

**● PageBreakEnabled**: *`boolean`* = True

___

<a id="attachment_list_type"></a>

### <a name="static-attachmentlisttype"></a>`<Static>`ATTACHMENT_LIST_TYPE

**● ATTACHMENT_LIST_TYPE**: *`string`* = "Alt"

___

<a id="default_camera_filter_mode"></a>

### <a name="static-defaultcamerafiltermode"></a>`<Static>`DEFAULT_CAMERA_FILTER_MODE

**● DEFAULT_CAMERA_FILTER_MODE**: *`string`* = "Dcfm"

___

<a id="image_source_key"></a>

### <a name="static-imagesourcekey"></a>`<Static>`IMAGE_SOURCE_KEY

**● IMAGE_SOURCE_KEY**: *`string`* = "ist"

___

<a id="max_image_count_key"></a>

### <a name="static-maximagecountkey"></a>`<Static>`MAX_IMAGE_COUNT_KEY

**● MAX_IMAGE_COUNT_KEY**: *`string`* = "Mikrofon"

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`any`*): [KASAttachmentListQuestionConfig](kasclient.kasattachmentlistquestionconfig.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `any` |

**Gibt:** [KASAttachmentListQuestionConfig](kasclient.kasattachmentlistquestionconfig.md)

___

