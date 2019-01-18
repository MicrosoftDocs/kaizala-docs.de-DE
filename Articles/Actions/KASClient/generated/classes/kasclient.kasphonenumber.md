---
ms.openlocfilehash: 83bf0eada0674bea5a6cbe1e346a5f6aefac8121
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728054"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASPhoneNumber](../classes/kasclient.kasphonenumber.md)

# <a name="class-kasphonenumber"></a>Klasse: KASPhoneNumber

## <a name="hierarchy"></a>Hierarchie

**KASPhoneNumber**

## <a name="index"></a>Index 

### <a name="constructors"></a>Konstruktoren

* [Konstruktor](kasclient.kasphonenumber.md#constructor)
### <a name="properties"></a>Eigenschaften

* [countryPhoneCode](kasclient.kasphonenumber.md#countryphonecode)
* ["PhoneNumber"](kasclient.kasphonenumber.md#phonenumber)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasphonenumber.md#tojson)
* [toString](kasclient.kasphonenumber.md#tostring)
* [fromJSON](kasclient.kasphonenumber.md#fromjson)

---

## <a name="constructors"></a>Konstruktoren

<a id="constructor"></a>

###  <a name="constructor"></a>constructor

⊕ **neue KASPhoneNumber**(CountryPhoneCode?: *`number`*, PhoneNumber?: *`string`*): [KASPhoneNumber](kasclient.kasphonenumber.md)

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| `Default value`countryPhoneCode | `number` | 0 |
| `Default value`"PhoneNumber" | `string` | &quot;&quot; |

**Gibt:** [KASPhoneNumber](kasclient.kasphonenumber.md)

___

## <a name="properties"></a>Eigenschaften

<a id="countryphonecode"></a>

###  <a name="countryphonecode"></a>countryPhoneCode

**● CountryPhoneCode**: *`number`* = 0

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a>PhoneNumber

**● PhoneNumber**: *`string`* = ""

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **ToJSON**():`JSON`

**Gibt:**`JSON`

___

<a id="tostring"></a>

###  <a name="tostring"></a>toString

▸ **ToString**():`string`

**Gibt:**`string`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(PhoneNumberReponseJSON: *`any`*): [KASPhoneNumber](kasclient.kasphonenumber.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| phoneNumberReponseJSON | `any` |

**Gibt:** [KASPhoneNumber](kasclient.kasphonenumber.md)

___

