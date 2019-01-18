---
ms.openlocfilehash: 94efbe6f80d643bdc930e2c23de6197d8b20d7ad
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728072"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormResponseNotificationModel](../classes/kasclient.kasformresponsenotificationmodel.md)

# <a name="class-kasformresponsenotificationmodel"></a>Klasse: KASFormResponseNotificationModel

## <a name="hierarchy"></a>Hierarchie

**KASFormResponseNotificationModel**

## <a name="index"></a>Index 

### <a name="constructors"></a>Konstruktoren

* [Konstruktor](kasclient.kasformresponsenotificationmodel.md#constructor)
### <a name="properties"></a>Eigenschaften

* [messagePreview](kasclient.kasformresponsenotificationmodel.md#messagepreview)
* [messageTarget](kasclient.kasformresponsenotificationmodel.md#messagetarget)
* [pushTarget](kasclient.kasformresponsenotificationmodel.md#pushtarget)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasformresponsenotificationmodel.md#tojson)
* [fromJson](kasclient.kasformresponsenotificationmodel.md#fromjson)

---

## <a name="constructors"></a>Konstruktoren

<a id="constructor"></a>

###  <a name="constructor"></a>constructor

⊕ **neue KASFormResponseNotificationModel**(MessageTarget?: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, PushTarget?: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, MessagePreview?: *`String`*): [ KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| `Default value`messageTarget | [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) [] |  null |
| `Default value`pushTarget | [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) [] |  null |
| `Default value`messagePreview | `String` |  null |

**Gibt:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

___

## <a name="properties"></a>Eigenschaften

<a id="messagepreview"></a>

###  <a name="messagepreview"></a>messagePreview

**● MessagePreview**: *`String`* = ""

___

<a id="messagetarget"></a>

###  <a name="messagetarget"></a>messageTarget

**● MessageTarget**: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)]*

___

<a id="pushtarget"></a>

###  <a name="pushtarget"></a>pushTarget

**● PushTarget**: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)]*

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJson

▸ **FromJson**(Objekt: *`JSON`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `JSON` |

**Gibt:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

___

