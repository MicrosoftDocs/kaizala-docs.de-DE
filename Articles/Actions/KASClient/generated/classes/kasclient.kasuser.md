[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)

# <a name="class-kasuser"></a>Klasse: KASUser

## <a name="hierarchy"></a>Hierarchie

**KASUser**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [id](kasclient.kasuser.md#id)
* [name](kasclient.kasuser.md#name)
* [Originalname](kasclient.kasuser.md#originalname)
* [phoneNumber](kasclient.kasuser.md#phonenumber)
* [pictureBGColor](kasclient.kasuser.md#picturebgcolor)
* [pictureInitials](kasclient.kasuser.md#pictureinitials)
* [pictureUrl](kasclient.kasuser.md#pictureurl)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasuser.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="id"></a>

###  <a name="id"></a>id

**● ID**: *`string`* = ""

Eindeutige Benutzer-ID

___

<a id="name"></a>

###  <a name="name"></a>name

**● Name**: *`string`* = ""

Name des Benutzers ("Sie" für den aktuellen Benutzer)

___

<a id="originalname"></a>

###  <a name="originalname"></a>Originalname

**● Originalname**: *`string`* = ""

"Sie" nicht in Betracht ziehen

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a>PhoneNumber

**●**Telefonnummer *`string`* : = ""

Telefonnummer des Benutzers

___

<a id="picturebgcolor"></a>

###  <a name="picturebgcolor"></a>pictureBGColor

**● pictureBGColor**: *`string`* = ""

Falls das PictureUrl nicht vorhanden ist, sollten wir die Benutzerinitialen als Profilbild verwenden, darunter zwei Mitglieder sind dafür

___

<a id="pictureinitials"></a>

###  <a name="pictureinitials"></a>pictureInitials

**● pictureInitials**: *`string`* = ""

___

<a id="pictureurl"></a>

###  <a name="pictureurl"></a>pictureUrl

**● pictureUrl**: *`string`* = ""

Profilbild-URL des Benutzers

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **fromJSON**(Object: *`JSON`*): [KASUser](kasclient.kasuser.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| Objekt | `JSON` |

**Gibt Folgendes zurück:** [KASUser](kasclient.kasuser.md)

___

