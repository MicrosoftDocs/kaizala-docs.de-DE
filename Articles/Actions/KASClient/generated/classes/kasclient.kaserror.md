[](../README.md) > [KASClient](../modules/kasclient.md) > [KASError](../classes/kasclient.kaserror.md)

# <a name="class-kaserror"></a>Klasse: KASError

## <a name="hierarchy"></a>Hierarchie

**KASError**

## <a name="index"></a>Index 

### <a name="constructors"></a>Konstruktoren

* [Konstruktor](kasclient.kaserror.md#constructor)
### <a name="properties"></a>Eigenschaften

* [description](kasclient.kaserror.md#description)
* [ErrorCode](kasclient.kaserror.md#errorcode)
### <a name="methods"></a>Methoden

* [ToString](kasclient.kaserror.md#tostring)
* [fromErrorString](kasclient.kaserror.md#fromerrorstring)
* [fromString](kasclient.kaserror.md#fromstring)

---

## <a name="constructors"></a>Konstruktoren

<a id="constructor"></a>

###  <a name="constructor"></a>constructor

⊕ **New KASError**(ErrorCode: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)*, Description: *`string`*): [KASError](kasclient.kaserror.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| errorCode | [KASErrorCode](../enums/kasclient.kaserrorcode.md) |
| description | `string` |

**Gibt Folgendes zurück:** [KASError](kasclient.kaserror.md)

___

## <a name="properties"></a>Eigenschaften

<a id="description"></a>

###  <a name="description"></a>description

**● Description**: *`String`* = ""

___
<a id="errorcode"></a>

###  <a name="errorcode"></a>errorCode

**● errorCode**: *[KASErrorCode](../enums/kasclient.kaserrorcode.md)* = KASErrorCode. None

___

## <a name="methods"></a>Methoden

<a id="tostring"></a>

###  <a name="tostring"></a>ToString

▸ **ToString**():`string`

**Gibt Folgendes zurück:**`string`

___
<a id="fromerrorstring"></a>

### <a name="static-fromerrorstring"></a>`<Static>`fromErrorString

▸ **fromErrorString**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| stringifyError | `string` |  stringified-Wörterbuch des Fehlers mit Code und Beschreibung |

**Gibt Folgendes zurück:** [KASError](kasclient.kaserror.md) gibt KASError-Objekt zurück, das aus stringified-Fehler gemacht wurde. Für NULL-Zeichenfolge wird NULL-Objekt zurückgegeben.

___
<a id="fromstring"></a>

### <a name="static-fromstring"></a>`<Static>`fromString

▸ **fromtype**(stringifyError: *`string`*): [KASError](kasclient.kaserror.md)

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| stringifyError | `string` |  stringified-Wörterbuch des Fehlers mit Code und Beschreibung |

**Gibt Folgendes zurück:** [KASError](kasclient.kaserror.md) gibt KASError-Objekt zurück, das aus stringified-Fehler gemacht wurde. Bei NULL-Zeichenfolge wird auch ungleich NULL-Fehlercode zurückgegeben.

___

