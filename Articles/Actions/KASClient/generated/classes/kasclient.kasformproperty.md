---
ms.openlocfilehash: 6433ecb385d38db201ec8e2733768e9fc095ae8e
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728073"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASFormProperty](../classes/kasclient.kasformproperty.md)

# <a name="class-kasformproperty"></a>Klasse: KASFormProperty

## <a name="hierarchy"></a>Hierarchie

**KASFormProperty**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [name](kasclient.kasformproperty.md#name)
* [type](kasclient.kasformproperty.md#type)
* [value](kasclient.kasformproperty.md#value)
### <a name="methods"></a>Methoden

* [getAPICompatiblePropertyType](kasclient.kasformproperty.md#getapicompatiblepropertytype)
* [toAPICompatibleJSON](kasclient.kasformproperty.md#toapicompatiblejson)
* [toClientJSON](kasclient.kasformproperty.md#toclientjson)
* [toJSON](kasclient.kasformproperty.md#tojson)
* [fromJSON](kasclient.kasformproperty.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="name"></a>

###  <a name="name"></a>name

**● Name**: *`string`* = ""

Name der Metadaten

___

<a id="type"></a>

###  <a name="type"></a>type

**● Typ**: *[KASFormPropertyType](../enums/kasclient.kasformpropertytype.md)* = KASFormPropertyType.Text

Typ der Metadaten

___

<a id="value"></a>

###  <a name="value"></a>Wert

**● Wert**: *`string`* = ""

Wert der Metadaten

___

## <a name="methods"></a>Methoden

<a id="getapicompatiblepropertytype"></a>

###  <a name="getapicompatiblepropertytype"></a>getAPICompatiblePropertyType

▸ **GetAPICompatiblePropertyType**(Typ: *`string`*):`string`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Typ | `string` |

**Gibt:**`string`

___

<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a>toAPICompatibleJSON

▸ **ToAPICompatibleJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="toclientjson"></a>

###  <a name="toclientjson"></a>toClientJSON

▸ **ToClientJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`JSON`*): [KASFormProperty](kasclient.kasformproperty.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `JSON` |

**Gibt:** [KASFormProperty](kasclient.kasformproperty.md)

___

