---
ms.openlocfilehash: 20daed268b67eea07a8185c84086587dcf1f1aeb
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728092"
---
<span data-ttu-id="07fff-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)</span><span class="sxs-lookup"><span data-stu-id="07fff-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASUser](../classes/kasclient.kasuser.md)</span></span>

# <a name="class-kasuser"></a><span data-ttu-id="07fff-102">Klasse: KASUser</span><span class="sxs-lookup"><span data-stu-id="07fff-102">Class: KASUser</span></span>

## <a name="hierarchy"></a><span data-ttu-id="07fff-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="07fff-103">Hierarchy</span></span>

<span data-ttu-id="07fff-104">**KASUser**</span><span class="sxs-lookup"><span data-stu-id="07fff-104">**KASUser**</span></span>

## <a name="index"></a><span data-ttu-id="07fff-105">Index </span><span class="sxs-lookup"><span data-stu-id="07fff-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="07fff-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07fff-106">Properties</span></span>

* [<span data-ttu-id="07fff-107">id</span><span class="sxs-lookup"><span data-stu-id="07fff-107">id</span></span>](kasclient.kasuser.md#id)
* [<span data-ttu-id="07fff-108">name</span><span class="sxs-lookup"><span data-stu-id="07fff-108">name</span></span>](kasclient.kasuser.md#name)
* [<span data-ttu-id="07fff-109">originalName</span><span class="sxs-lookup"><span data-stu-id="07fff-109">originalName</span></span>](kasclient.kasuser.md#originalname)
* [<span data-ttu-id="07fff-110">"PhoneNumber"</span><span class="sxs-lookup"><span data-stu-id="07fff-110">phoneNumber</span></span>](kasclient.kasuser.md#phonenumber)
* [<span data-ttu-id="07fff-111">pictureBGColor</span><span class="sxs-lookup"><span data-stu-id="07fff-111">pictureBGColor</span></span>](kasclient.kasuser.md#picturebgcolor)
* [<span data-ttu-id="07fff-112">pictureInitials</span><span class="sxs-lookup"><span data-stu-id="07fff-112">pictureInitials</span></span>](kasclient.kasuser.md#pictureinitials)
* [<span data-ttu-id="07fff-113">Bild-URL</span><span class="sxs-lookup"><span data-stu-id="07fff-113">pictureUrl</span></span>](kasclient.kasuser.md#pictureurl)
### <a name="methods"></a><span data-ttu-id="07fff-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="07fff-114">Methods</span></span>

* [<span data-ttu-id="07fff-115">fromJSON</span><span class="sxs-lookup"><span data-stu-id="07fff-115">fromJSON</span></span>](kasclient.kasuser.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="07fff-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07fff-116">Properties</span></span>

<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="07fff-117">id</span><span class="sxs-lookup"><span data-stu-id="07fff-117">id</span></span>

<span data-ttu-id="07fff-118">**●-Id**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-118">**● id**: *`string`* = ""</span></span>

<span data-ttu-id="07fff-119">Eindeutige Benutzer-id</span><span class="sxs-lookup"><span data-stu-id="07fff-119">Unique user id</span></span>

___

<a id="name"></a>

###  <a name="name"></a><span data-ttu-id="07fff-120">name</span><span class="sxs-lookup"><span data-stu-id="07fff-120">name</span></span>

<span data-ttu-id="07fff-121">**● Name**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-121">**● name**: *`string`* = ""</span></span>

<span data-ttu-id="07fff-122">Name des Benutzers ("Sie" für den aktuellen Benutzer)</span><span class="sxs-lookup"><span data-stu-id="07fff-122">Name of the user ("You" for the current user)</span></span>

___

<a id="originalname"></a>

###  <a name="originalname"></a><span data-ttu-id="07fff-123">originalName</span><span class="sxs-lookup"><span data-stu-id="07fff-123">originalName</span></span>

<span data-ttu-id="07fff-124">**● OriginalName**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-124">**● originalName**: *`string`* = ""</span></span>

<span data-ttu-id="07fff-125">Berücksichtigung nicht "Sie"</span><span class="sxs-lookup"><span data-stu-id="07fff-125">Not considering "You"</span></span>

___

<a id="phonenumber"></a>

###  <a name="phonenumber"></a><span data-ttu-id="07fff-126">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="07fff-126">phoneNumber</span></span>

<span data-ttu-id="07fff-127">**● PhoneNumber**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-127">**● phoneNumber**: *`string`* = ""</span></span>

<span data-ttu-id="07fff-128">Telefonnummer des Benutzers</span><span class="sxs-lookup"><span data-stu-id="07fff-128">Phone number of the user</span></span>

___

<a id="picturebgcolor"></a>

###  <a name="picturebgcolor"></a><span data-ttu-id="07fff-129">pictureBGColor</span><span class="sxs-lookup"><span data-stu-id="07fff-129">pictureBGColor</span></span>

<span data-ttu-id="07fff-130">**● PictureBGColor**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-130">**● pictureBGColor**: *`string`* = ""</span></span>

<span data-ttu-id="07fff-131">Für den Fall, dass die Bild-URL nicht vorhanden ist, sollten wir die Benutzer verwenden die Initialen als Pic Profil unter zwei Elemente für, die sind</span><span class="sxs-lookup"><span data-stu-id="07fff-131">In case the PictureUrl is not there, we should use the users initials as the profile pic, below two members are for that</span></span>

___

<a id="pictureinitials"></a>

###  <a name="pictureinitials"></a><span data-ttu-id="07fff-132">pictureInitials</span><span class="sxs-lookup"><span data-stu-id="07fff-132">pictureInitials</span></span>

<span data-ttu-id="07fff-133">**● PictureInitials**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-133">**● pictureInitials**: *`string`* = ""</span></span>

___

<a id="pictureurl"></a>

###  <a name="pictureurl"></a><span data-ttu-id="07fff-134">Bild-URL</span><span class="sxs-lookup"><span data-stu-id="07fff-134">pictureUrl</span></span>

<span data-ttu-id="07fff-135">**● Bild-URL**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="07fff-135">**● pictureUrl**: *`string`* = ""</span></span>

<span data-ttu-id="07fff-136">Bild-Url Profil des Benutzers</span><span class="sxs-lookup"><span data-stu-id="07fff-136">Profile picture url of the user</span></span>

___

## <a name="methods"></a><span data-ttu-id="07fff-137">Methoden</span><span class="sxs-lookup"><span data-stu-id="07fff-137">Methods</span></span>

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="07fff-138">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="07fff-138">`<Static>` fromJSON</span></span>

<span data-ttu-id="07fff-139">▸ **FromJSON**(Objekt: *`JSON`*): [KASUser](kasclient.kasuser.md)</span><span class="sxs-lookup"><span data-stu-id="07fff-139">▸ **fromJSON**(object: *`JSON`*): [KASUser](kasclient.kasuser.md)</span></span>

<span data-ttu-id="07fff-140">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="07fff-140">**Parameters:**</span></span>

| <span data-ttu-id="07fff-141">Name</span><span class="sxs-lookup"><span data-stu-id="07fff-141">Name</span></span> | <span data-ttu-id="07fff-142">Typ</span><span class="sxs-lookup"><span data-stu-id="07fff-142">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="07fff-143">object</span><span class="sxs-lookup"><span data-stu-id="07fff-143">object</span></span> | `JSON` |

<span data-ttu-id="07fff-144">**Gibt:** [KASUser](kasclient.kasuser.md)</span><span class="sxs-lookup"><span data-stu-id="07fff-144">**Returns:** [KASUser](kasclient.kasuser.md)</span></span>

___

