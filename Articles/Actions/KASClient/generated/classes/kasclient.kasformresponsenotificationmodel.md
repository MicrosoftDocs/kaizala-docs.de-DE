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

⊕ **New KASFormResponseNotificationModel**(MessageTarget?: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, pushTarget?: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*, messagePreview?: *`String`*): [ KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| `Default value`messageTarget | [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) [] |  null |
| `Default value`pushTarget | [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md) [] |  null |
| `Default value`messagePreview | `String` |  null |

**Gibt Folgendes zurück:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

___

## <a name="properties"></a>Eigenschaften

<a id="messagepreview"></a>

###  <a name="messagepreview"></a>messagePreview

**● messagePreview**: *`String`* = ""

___

<a id="messagetarget"></a>

###  <a name="messagetarget"></a>messageTarget

**● messageTarget**: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*

___

<a id="pushtarget"></a>

###  <a name="pushtarget"></a>pushTarget

**● pushTarget**: * [KASFormResponseNotificationTarget](../enums/kasclient.kasformresponsenotificationtarget.md)[]*

___

## <a name="methods"></a>Methoden

<a id="tojson"></a>

###  <a name="tojson"></a>toJSON

▸ **tojson**():`JSON`

**Gibt Folgendes zurück:**`JSON`

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJson

▸ **fromJson**(Object: *`JSON`*): [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |

**Gibt Folgendes zurück:** [KASFormResponseNotificationModel](kasclient.kasformresponsenotificationmodel.md)

___

