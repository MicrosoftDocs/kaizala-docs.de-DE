[](../README.md) > [KASClient](../modules/kasclient.md) > [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)

# <a name="class-kasactionlocalcacheprop"></a>Klasse: KASActionLocalCacheProp

## <a name="hierarchy"></a>Hierarchie

**KASActionLocalCacheProp**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [cacheScope](kasclient.kasactionlocalcacheprop.md#cachescope)
* [cacheVisibility](kasclient.kasactionlocalcacheprop.md#cachevisibility)
* [key](kasclient.kasactionlocalcacheprop.md#key)
* [value](kasclient.kasactionlocalcacheprop.md#value)
### <a name="methods"></a>Methoden

* [toJSON](kasclient.kasactionlocalcacheprop.md#tojson)
* [fromJSON](kasclient.kasactionlocalcacheprop.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="cachescope"></a>

###  <a name="cachescope"></a>cacheScope

**● cacheScope**: *[cacheScope](../enums/kasclient.cachescope.md)* = cacheScope. Global

cacheScope gibt an, dass die Daten auf globaler oder converastion Ebene gespeichert werden.

___
<a id="cachevisibility"></a>

###  <a name="cachevisibility"></a>cacheVisibility

**● cacheVisibility**: *[cacheVisibility](../enums/kasclient.cachevisibility.md)* = cacheVisibility. app

cacheVisibility gibt an, dass die Daten für andere apps sichtbar sind oder nicht.

___
<a id="key"></a>

###  <a name="key"></a>Schlüssel

**● Taste**: *`string`* = ""

Schlüssel des im Cache gespeicherten Werts

___
<a id="value"></a>

###  <a name="value"></a>Wert

**● Wert**: *`string`* = ""

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___
<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸- **fromJSON**(Objekt *`JSON`*:): [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |

**Gibt Folgendes zurück:** [KASActionLocalCacheProp](kasclient.kasactionlocalcacheprop.md)

___

