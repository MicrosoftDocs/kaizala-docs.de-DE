---
ms.openlocfilehash: 20daed268b67eea07a8185c84086587dcf1f1aeb
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728092"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)

# <a name="class-kasuser"></a>Klasse: KASUser

## <a name="hierarchy"></a>Hierarchie

**KASUser**

## <a name="index"></a>Index 

### <a name="properties"></a>Eigenschaften

* [id](kasclient.kasuser.md#id)
* [name](kasclient.kasuser.md#name)
* [originalName](kasclient.kasuser.md#originalname)
* ["PhoneNumber"](kasclient.kasuser.md#phonenumber)
* [pictureBGColor](kasclient.kasuser.md#picturebgcolor)
* [pictureInitials](kasclient.kasuser.md#pictureinitials)
* [Bild-URL](kasclient.kasuser.md#pictureurl)
### <a name="methods"></a>Methoden

* [fromJSON](kasclient.kasuser.md#fromjson)

---

## <a name="properties"></a>Eigenschaften

<a id="id"></a>

###  <a name="id"></a>id

**●-Id**: *`string`* = ""

Eindeutige Benutzer-id

___

<a id="name"></a>

###  <a name="name"></a>name

**● Name**: *`string`* = ""

Name des Benutzers ("Sie" für den aktuellen Benutzer)

___

<a id="originalname"></a>

###  <a name="originalname"></a>originalName

**● OriginalName**: *`string`* = ""

Berücksichtigung nicht "Sie"

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a>PhoneNumber

**● PhoneNumber**: *`string`* = ""

Telefonnummer des Benutzers

___

<a id="picturebgcolor"></a>

###  <a name="picturebgcolor"></a>pictureBGColor

**● PictureBGColor**: *`string`* = ""

Für den Fall, dass die Bild-URL nicht vorhanden ist, sollten wir die Benutzer verwenden die Initialen als Pic Profil unter zwei Elemente für, die sind

___

<a id="pictureinitials"></a>

###  <a name="pictureinitials"></a>pictureInitials

**● PictureInitials**: *`string`* = ""

___

<a id="pictureurl"></a>

###  <a name="pictureurl"></a>Bild-URL

**● Bild-URL**: *`string`* = ""

Bild-Url Profil des Benutzers

___

## <a name="methods"></a>Methoden

<a id="fromjson"></a>

### <a name="static-fromjson"></a>`<Static>`fromJSON

▸ **FromJSON**(Objekt: *`JSON`*): [KASUser](kasclient.kasuser.md)

**Parameter:**

| Name | Typ |
| ------ | ------ |
| object | `JSON` |

**Gibt:** [KASUser](kasclient.kasuser.md)

___

