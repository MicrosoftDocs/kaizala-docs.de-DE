[](../README.md) > [KASClient](../modules/kasclient.md) > [KASLocation](../classes/kasclient.kaslocation.md)

# <a name="class-kaslocation"></a>Klasse: KASLocation

## <a name="hierarchy"></a>Hierarchie

**KASLocation**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [latitude](kasclient.kaslocation.md#latitude)
* [longitude](kasclient.kaslocation.md#longitude)
* [placeAddress](kasclient.kaslocation.md#placeaddress)
* [Ortsname](kasclient.kaslocation.md#placename)
### <a name="methods"></a>Methoden

* [IsEmpty](kasclient.kaslocation.md#isempty)
* [IsEqual](kasclient.kaslocation.md#isequal)
* [toJSON](kasclient.kaslocation.md#tojson)
* [fromJSON](kasclient.kaslocation.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="latitude"></a>

###  <a name="latitude"></a>latitude

**● Latitude**: *`number`* = 0

Breite des Speicherorts

___
<a id="longitude"></a>

###  <a name="longitude"></a>longitude

**● Längengrad**: *`number`* = 0

Längengrad des Standorts

___
<a id="placeaddress"></a>

###  <a name="placeaddress"></a>placeAddress

**● placeAddress**: *`string`* = ""

Adresse des Speicherorts

___
<a id="placename"></a>

###  <a name="placename"></a>Ortsname

**● Ortsname**: *`string`* = ""

Name des Speicherorts

___

## <a name="methods"></a>Methoden

<a id="isempty"></a>

###  <a name="isempty"></a>IsEmpty

▸ **IsEmpty**():`boolean`

**Gibt Folgendes zurück:**`boolean`

___
<a id="isequal"></a>

###  <a name="isequal"></a>IsEqual

▸ **IsEqual**(Location: *[KASLocation](kasclient.kaslocation.md)*):`boolean`

**Parameter:**

| Name | Typ |
| ------ | ------ |
| location | [KASLocation](kasclient.kaslocation.md) |

**Gibt Folgendes zurück:**`boolean`

___
<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`JSON`*:): [KASLocation](kasclient.kaslocation.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |

**Gibt Folgendes zurück:** [KASLocation](kasclient.kaslocation.md)

___

