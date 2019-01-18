---
ms.openlocfilehash: f725f55c2e7e0c8c75d71275c7217497090b4f1a
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728163"
---
[](../README.md) > [KASClient](../modules/kasclient.md) > [App](../modules/kasclient.app.md)

# <a name="module-app"></a>Modul: App

## <a name="index"></a>Index 

### <a name="functions"></a>Funktionen

* [cancelAttachmentDownloadAsync](kasclient.app.md#cancelattachmentdownloadasync)
* [dismissCurrentScreen](kasclient.app.md#dismisscurrentscreen)
* [downloadAttachmentAsync](kasclient.app.md#downloadattachmentasync)
* [generateBase64ThumbnailAsync](kasclient.app.md#generatebase64thumbnailasync)
* [generateUUIDAsync](kasclient.app.md#generateuuidasync)
* [getAppLocaleAsync](kasclient.app.md#getapplocaleasync)
* [getCalendarNameAsync](kasclient.app.md#getcalendarnameasync)
* [getConversationDetailsAsync](kasclient.app.md#getconversationdetailsasync)
* [getCurrentDeviceLocationAsync](kasclient.app.md#getcurrentdevicelocationasync)
* [getCurrentLocale](kasclient.app.md#getcurrentlocale)
* [getDeviceIdAsync](kasclient.app.md#getdeviceidasync)
* [getDeviceLocationAsync](kasclient.app.md#getdevicelocationasync)
* [getFontSizeMultiplierAsync](kasclient.app.md#getfontsizemultiplierasync)
* [getForwardContextAsync](kasclient.app.md#getforwardcontextasync)
* [getIsAppTimeFormat24HoursAsync](kasclient.app.md#getisapptimeformat24hoursasync)
* [getLocalizedStringsAsync](kasclient.app.md#getlocalizedstringsasync)
* [getLocationAddressAsync](kasclient.app.md#getlocationaddressasync)
* [getMapImageAsBase64Async](kasclient.app.md#getmapimageasbase64async)
* [getO365UserDetailsAsync](kasclient.app.md#geto365userdetailsasync)
* [getPackageCustomSettingsAsync](kasclient.app.md#getpackagecustomsettingsasync)
* [getUsersDetailsAsync](kasclient.app.md#getusersdetailsasync)
* [hideProgressBar](kasclient.app.md#hideprogressbar)
* [isAttachmentDownloadingAsync](kasclient.app.md#isattachmentdownloadingasync)
* [isAuthenticationTyepSupportedAsync](kasclient.app.md#isauthenticationtyepsupportedasync)
* [isTalkBackEnabledAsync](kasclient.app.md#istalkbackenabledasync)
* [logToReport](kasclient.app.md#logtoreport)
* [openAttachmentImmersiveView](kasclient.app.md#openattachmentimmersiveview)
* [openImmersiveViewForAttachmentList](kasclient.app.md#openimmersiveviewforattachmentlist)
* [performAuthenticationAsync](kasclient.app.md#performauthenticationasync)
* [performHTTPRequest](kasclient.app.md#performhttprequest)
* [printf](kasclient.app.md#printf)
* [readTalkBackMessage](kasclient.app.md#readtalkbackmessage)
* [registerHardwareBackPressCallback](kasclient.app.md#registerhardwarebackpresscallback)
* [setNativeToolbarProperties](kasclient.app.md#setnativetoolbarproperties)
* [setUserStrings](kasclient.app.md#setuserstrings)
* [showAttachmentPickerAsync](kasclient.app.md#showattachmentpickerasync)
* [showBarcodeScannerAsync](kasclient.app.md#showbarcodescannerasync)
* [showContactPickerAsync](kasclient.app.md#showcontactpickerasync)
* [showDurationPickerAsync](kasclient.app.md#showdurationpickerasync)
* [showImageImmersiveView](kasclient.app.md#showimageimmersiveview)
* [showImagePickerAsync](kasclient.app.md#showimagepickerasync)
* [showLocationOnMap](kasclient.app.md#showlocationonmap)
* [showNativeErrorMessage](kasclient.app.md#shownativeerrormessage)
* [showPlacePickerAsync](kasclient.app.md#showplacepickerasync)
* [showProgressBar](kasclient.app.md#showprogressbar)
* [showQRcodeScannerAsync](kasclient.app.md#showqrcodescannerasync)
* [showUserProfileAsync](kasclient.app.md#showuserprofileasync)
* [startChatAsync](kasclient.app.md#startchatasync)

---

## <a name="functions"></a>Funktionen

<a id="cancelattachmentdownloadasync"></a>

###  <a name="cancelattachmentdownloadasync"></a>cancelAttachmentDownloadAsync

▸ **CancelAttachmentDownloadAsync**(Anlage: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Rückruf: *`function`*):`void`

Abbrechen eines Downloadvorgangs in der Warteschlange für eine Anlage

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
 var attachmentsList = JSON.parse(form.properties[0].value);
 for (var i = 0; i < attachmentsList.length; i++)
 {
      var attachmentItem = attachmentsList[i];
      var attachment = KASClient.KASAttachment.fromJSON(attachmentItem);
      KASClient.App.cancelAttachmentDownloadAsync(attachment);
 }
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Anlage | [KASAttachment](../classes/kasclient.kasattachment.md) |  \- |
| callback | `function` |  mit Fehler Param - Fehlerzeichenfolge bei einem Fehler; andernfalls NULL |

**Gibt:**`void`

___

<a id="dismisscurrentscreen"></a>

###  <a name="dismisscurrentscreen"></a>dismissCurrentScreen

▸ **DismissCurrentScreen**():`void`

Schließen Sie die aktuelle geöffnete Aktion Bildschirm (Erstellung,-Antwort oder Zusammenfassung)

**Gibt:**`void`

___

<a id="downloadattachmentasync"></a>

###  <a name="downloadattachmentasync"></a>downloadAttachmentAsync

▸ **DownloadAttachmentAsync**(Anlage: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Rückruf: *`function`*):`void`

Laden Sie das angegebene Attachment-Objekt

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var imageAttachment =  new KASClient.KASAttachment();
imageAttachment.type = KASClient.KASAttachmentType.Image;
imageAttachment.serverPath = "<server path>";
imageAttachment.fileName = "<file name>";
KASClient.App.downloadAttachmentAsync(imageAttachment, function(downloadedAttachment, error){
     if (!error) {
        console.log(downloadedAttachment); //KASAttachment
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Anlage | [KASAttachment](../classes/kasclient.kasattachment.md) |  Anlage mit einem gültigen Serverpfad zum Herunterladen |
| callback | `function` |  Rückruf Download nach Abschluss mit unter params<br><br>\*{KASAttachment} @param DownloadedAttachment die Anlage, die heruntergeladen haben<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="generatebase64thumbnailasync"></a>

###  <a name="generatebase64thumbnailasync"></a>generateBase64ThumbnailAsync

▸ **generateBase64ThumbnailAsync**(LocalPath: *`string`*, Rückruf: *`function`*):`void`

Generiert Base64-Miniaturansicht für ein Bild, dessen LocalPath erfolgt ist

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
KASClient.App.generateBase64ThumbnailAsync(localPath, function (thumbnail, error) {
    if (error == null && thumbnail != null) {
       //use the thumbnail data and update required dom
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| localPath | `string` |  LocalPath für die ImageAttachment, deren Miniaturansicht generiert werden muss |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param Miniaturansicht base64-Wert<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="generateuuidasync"></a>

###  <a name="generateuuidasync"></a>generateUUIDAsync

▸ **GenerateUUIDAsync**(Rückruf: *`function`*):`void`

Ruft die neue UUID

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
 KASClient.App.generateUUIDAsync(function (uuid, error) {
    console.log("generatedUUIDAsync", uuid);
    ...
 });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param Uuid neu generiert uuid<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getapplocaleasync"></a>

###  <a name="getapplocaleasync"></a>getAppLocaleAsync

▸ **GetAppLocaleAsync**(Rückruf: *`function`*):`void`

Ruft das aktuelle Gebietsschema der app, die Sprache aus, in dem die app gerenderten, hilfreich für die Lokalisierung von Zeichenfolgen MiniApp des

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param Gebietsschema kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getcalendarnameasync"></a>

###  <a name="getcalendarnameasync"></a>getCalendarNameAsync

▸ **GetCalendarNameAsync**(Rückruf: *`function`*):`void`

Ruft die aktuelle Einstellung der System Calendar ab. Dies ist vor allem für iOS identifiziert den Namen des Kalenders in Telefon Einstellung wie gregorianischen oder Japanisch oder Buddhists festgelegt.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param CalendarName kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getconversationdetailsasync"></a>

###  <a name="getconversationdetailsasync"></a>getConversationDetailsAsync

▸ **GetConversationDetailsAsync**(Rückruf: *`function`*):`void`

Ruft Unterhaltung bezogenen Eigenschaften

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASConversationDetails} @param Ergebniseigenschaften Unterhaltung<br><br>\*{Zeichenfolge} @param Json Fehlerzeichenfolge für das KASError-Objekt, das mit Fehlercode und/oder Beschreibung. |

**Gibt:**`void`

___

<a id="getcurrentdevicelocationasync"></a>

###  <a name="getcurrentdevicelocationasync"></a>getCurrentDeviceLocationAsync

▸ **GetCurrentDeviceLocationAsync**(Rückruf: *`function`*):`void`

Ruft den aktuellen Speicherort des Geräts

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
 KASClient.App.getCurrentDeviceLocationAsync(function (location, error){
     if(error != null) {
          return;
     }
     //use location(KASLocation) as the device location
 });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param Speicherort kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getcurrentlocale"></a>

###  <a name="getcurrentlocale"></a>getCurrentLocale

▸ **GetCurrentLocale**():`string`

**Gibt:**`string`

___

<a id="getdeviceidasync"></a>

###  <a name="getdeviceidasync"></a>getDeviceIdAsync

▸ **GetDeviceIdAsync**(Rückruf: *`function`*):`void`

Ruft die Geräte-ID

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*haben Sie @param {Zeichenfolge} Geräte-ID aus Integeration-Dienst<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getdevicelocationasync"></a>

###  <a name="getdevicelocationasync"></a>getDeviceLocationAsync

▸ **GetDeviceLocationAsync**(Rückruf: *`function`*):`void`

Ruft den Ort für die zuvor gespeicherte Geräte ab

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param Speicherort kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getfontsizemultiplierasync"></a>

###  <a name="getfontsizemultiplierasync"></a>getFontSizeMultiplierAsync

▸ **GetFontSizeMultiplierAsync**(Rückruf: *`function`*):`void`

Ruft die Schriftart Größe Multiplikator für große Text ab. Aktuelle nur von iOS erforderlich.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit unten Params<br><br>\*Multiplikator für @param {Zeichenfolge}<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getforwardcontextasync"></a>

###  <a name="getforwardcontextasync"></a>getForwardContextAsync

▸ **GetForwardContextAsync**(Rückruf: *`function`*):`void`

Ruft vorwärts Kontext Details wie etwa: Karte Erstellung befindet sich im weitergeleitete Modus

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Json} @param gibt die Kontext-Details im Json-Struktur |

**Gibt:**`void`

___

<a id="getisapptimeformat24hoursasync"></a>

###  <a name="getisapptimeformat24hoursasync"></a>getIsAppTimeFormat24HoursAsync

▸ **getIsAppTimeFormat24HoursAsync**(Rückruf: *`function`*):`void`

Dient zum Abrufen des aktuellen app Mal Format 24hours oder nicht ist, das vom Benutzer, für die Formatierung von Datum-Uhrzeit-Zeichenfolgen ordnungsgemäß nützlich ausgewählten Zeitformat

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param isAppTimeFormat24Hours kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getlocalizedstringsasync"></a>

###  <a name="getlocalizedstringsasync"></a>getLocalizedStringsAsync

▸ **GetLocalizedStringsAsync**(Rückruf: *`function`*):`void`

Ruft die lokalisierten Zeichenfolgen Wörterbuch basierend auf aktuellen Gebietsschema der app ab. Zeichenfolgen müssen in das Paket mit dem Namen wie bereitgestellt werden: Zeichenfolgen\_en.json, Zeichenfolgen\_hi.json usw..

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
KASClient.App.getLocalizedStringsAsync(function (strings, error) {
    if (error != null) {
        return;
    }
    //use the localized strings array
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{JSON} @param Zeichenfolgen können bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getlocationaddressasync"></a>

###  <a name="getlocationaddressasync"></a>getLocationAddressAsync

▸ **GetLocationAddressAsync**(Params: *[KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md)*, Rückruf: *`function`*):`void`

Get-Adresszeichenfolge für den angegebenen Koordinaten

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var params = new KASClient.KASLocationAddressParams();
params.latitude =  <latitude value>;
params.longitude =  <longitude value>;
KASClient.App.getLocationAddressAsync(params,
    function (address, error) {
        if (!error) {
           // do something with address - a JSON returned by google structure can be found at https://developers.google.com/maps/documentation/geocoding/intro#GeocodingResponses
        }
    }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| params | [KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md) |  KASLocationAddressParams |
| callback | `function` |  Rückruf für Adresse Abruf mit unter params<br><br>\*{JSON} @param Speicherort eine Json mit Latitute Längengrad und andere informaion<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getmapimageasbase64async"></a>

###  <a name="getmapimageasbase64async"></a>getMapImageAsBase64Async

▸ **getMapImageAsBase64Async**(Params: *[KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md)*, Rückruf: *`function`*):`void`

Laden Sie die Basis-64 Image der Zuordnung für den angegebenen Koordinaten

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
KASClient.App.getMapImageAsBase64Async(params, function (attachmentString, error) {
        if (!error) {
            blobString = "data:image/jpeg;base64," + attachmentString;
            //use blobString as base64 data
        }
 });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| params | [KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md) |  KASLocationStaticMapImageParams |
| callback | `function` |  nach Abschluss der Download mit unter params<br><br>\*{Zeichenfolge} @param AttachmentString base64-Wert der Anlage<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="geto365userdetailsasync"></a>

###  <a name="geto365userdetailsasync"></a>getO365UserDetailsAsync

▸ **getO365UserDetailsAsync**(Rückruf: *`function`*):`void`

Ruft die Details des aktuellen angemeldeten Office 365-Benutzers

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Json} @param gibt die UserDetails im Json-Struktur |

**Gibt:**`void`

___

<a id="getpackagecustomsettingsasync"></a>

###  <a name="getpackagecustomsettingsasync"></a>getPackageCustomSettingsAsync

▸ **GetPackageCustomSettingsAsync**(Rückruf: *`function`*):`void`

Ruft die Anpassung der Einstellungen für ein Paket (im Fall eines WAN-Typ-4-Paketen und deren Base Used) ab.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
KASClient.App.getPackageCustomSettingsAsync(function (settings, error) {
      if (error != null) {
          return;
      }
     //settings contains the settings json defined at the package level
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{JSON} @param Einstellungen können bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="getusersdetailsasync"></a>

###  <a name="getusersdetailsasync"></a>getUsersDetailsAsync

▸ **GetUsersDetailsAsync**(Benutzer-IDs: * `string`[]*, Rückruf: *`function`*):`void`

Ruft den Benutzer Details (Name, Pic, Telefonnummer usw.) vor deren ids

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var userIds = ["<uid1>", "<uid2>",...];
KASClient.App.getUsersDetailsAsync(userIds, function (users, error) {
      if (error != null) {
          return;
      }
      var userInfo1 = users[<uid1>];
      var userInfo2 = users[<uid2>];
      ...
  });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Benutzer-IDs | `string`[] |  Array von Benutzer-ids |
| callback | `function` |  mit folgenden Parameter:<br><br>\*@param {Dictionary<UserId: string, UserInfo: KASUser>} UserIdToInfoMap (Benutzer Details vor deren Ids) kann bei einem Fehler null sein<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="hideprogressbar"></a>

###  <a name="hideprogressbar"></a>hideProgressBar

▸ **HideProgressBar**():`void`

Die aktuellen Statusanzeige ausgeblendet, sofern vorhanden

**Gibt:**`void`

___

<a id="isattachmentdownloadingasync"></a>

###  <a name="isattachmentdownloadingasync"></a>isAttachmentDownloadingAsync

▸ **IsAttachmentDownloadingAsync**(Anlage: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Rückruf: *`function`*):`void`

Laden Sie das angegebene Attachment-Objekt

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var attachmentJson = {
  ty: 3,
  afn: "131490_Desert (1) (4).pdf",
  lpu: "",
  spu: '<server path>',
  asb: 846941,
  id:''
};
var attachment = KASClient.KASAttachment.fromJSON(attachmentJson);
KASClient.App.isAttachmentDownloadingAsync(attachment, function(isAttachmentDownloadingOrDownLoaded, error){
     if (!error) {
        console.log(isAttachmentDownloadingOrDownLoaded); //boolean
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Anlage | [KASAttachment](../classes/kasclient.kasattachment.md) |  Anlage mit einem gültigen Serverpfad zum Herunterladen |
| callback | `function` |  Rückruf Download nach Abschluss mit unter params<br><br>\*@param {Boolean} IsAttachmentDownloadingOrDownLoaded Kennzeichnung, darstellt, wenn Anlage herunterladen/heruntergeladen wird.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="isauthenticationtyepsupportedasync"></a>

###  <a name="isauthenticationtyepsupportedasync"></a>isAuthenticationTyepSupportedAsync

▸ **IsAuthenticationTyepSupportedAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, Rückruf: *`function`*):`void`

Überprüft, ob die Authentifizierung des Typs möglich ist.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType.None |  die Art der Authentifizierung. |
| callback | `function` | - |  mit folgenden Parameter:<br><br>\*@param {Boolean} IsSuccessful true zurück, wenn mit dem Finger Drucken möglich ist.<br><br>\*{Zeichenfolge} @param Ursachencode Grund Code Warum Finger print nicht möglich ist |

**Gibt:**`void`

___

<a id="istalkbackenabledasync"></a>

###  <a name="istalkbackenabledasync"></a>isTalkBackEnabledAsync

▸ **IsTalkBackEnabledAsync**(Rückruf: *`function`*):`void`

Ruft ab, ob Talkback oder nicht aktiviert ist

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param TalkBackEnabled true zurück, wenn Talkback aktiviert ist |

**Gibt:**`void`

___

<a id="logtoreport"></a>

###  <a name="logtoreport"></a>logToReport

▸ **LogToReport**(Daten: *`string`*):`void`

Protokolliert die Daten für "Senden Bericht"

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| data | `string` |  string |

**Gibt:**`void`

___

<a id="openattachmentimmersiveview"></a>

###  <a name="openattachmentimmersiveview"></a>openAttachmentImmersiveView

▸ **OpenAttachmentImmersiveView**(AttachmentObj: *[KASAttachment](../classes/kasclient.kasattachment.md)*):`void`

Die Anlage in fesselnden Ansicht öffnen.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| attachmentObj | [KASAttachment](../classes/kasclient.kasattachment.md) |   |

**Gibt:**`void`

___

<a id="openimmersiveviewforattachmentlist"></a>

###  <a name="openimmersiveviewforattachmentlist"></a>openImmersiveViewForAttachmentList

▸ **OpenImmersiveViewForAttachmentList**(AttachmentList: * [KASAttachment](../classes/kasclient.kasattachment.md)[]*, AtIndex?: *`number`*):`void`

Die Anlage in fesselnden Ansicht öffnen.

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| attachmentList | [KASAttachment](../classes/kasclient.kasattachment.md) [] | - |
| `Default value`atIndex | `number` | 0 |

**Gibt:**`void`

___

<a id="performauthenticationasync"></a>

###  <a name="performauthenticationasync"></a>performAuthenticationAsync

▸ **PerformAuthenticationAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, Rückruf: *`function`*):`void`

Wenn Authentifizierungstyp zulässig ist, wird diese API führt die Authentifizierung und Status Erfolg/False zurückgegeben else gibt eine Fehlerzeichenfolge mit Grund, warum Authentifizierung nicht möglich ist.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
KASClient.App.performAuthenticationAsync(KASAuthenticationType.Password, function (isSuccessful, reasonCode) {
      if (!isSuccessful) {
          console.log(resonCode);
      }
});
```

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType.None |  die Art der Authentifizierung. |
| callback | `function` | - |  mit folgenden Parameter:<br><br>\*{Boolean} @param IsSuccessful true zurück, wenn das Formular noch nicht abgelaufen ist<br><br>\*{Zeichenfolge} @param Ursachencode Grund Code bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="performhttprequest"></a>

###  <a name="performhttprequest"></a>performHTTPRequest

▸ **PerformHTTPRequest**(Url: *`string`*, ParametersJSON: *`string`*, Rückruf: *`function`*):`void`

führt eine http-Anforderung aus und gibt die Antwort als unten angegeben:

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var url = "<url>";
var parametersJson = JSON.stringify({ "method" : "GET" });
KASClient.App.performHTTPRequest(url, parametersJson, function (response, error) {
      if (!error) {
          //use the response
      }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| url | `string` |  Basis-Url zum Öffnen |
| parametersJSON | `string` |  Jsonstring mit Parametern kann als null angegeben werden.<br><br> Wenn Sie als Null wird eine Anforderung an den oben angegebenen Url hergestellt werden. Parameter umfassen Anforderungsheaders, Abfrageparametern (Standard leer), fordern-Methode (GET Standard) und Anforderungstext (der Nachrichtentext gebucht, wenn die Anforderungsmethode POST ist. Standardmäßig leer.) Die Schlüssel für Parameter sind:<br><br> a.) "Methode": request-Methode. Beispiel: "POST". Der Standardwert ist "GET".<br><br> b) "RequestBody": Text der Anforderung im Fall eines WAN-"POST". Der Standardwert ist leer.<br><br> c.) "RequestHeaders": Kopfzeilen mit Anforderung gesendet werden. soll ein Json mit<br> der Schlüssel als Anforderungsheader und den Wert als den gewünschten Wert. Der Standardwert ist leer.<br><br> d.) "QueryParameters": Abfrageparametern. wird in der Url codiert werden. soll ein Json mit<br> der Schlüssel als Parametername und als Wert Value. Der Standardwert ist leer.<br><br> e.) "RequestResourcePath": Basis-Url angefügt werden soll. Standardeinstellung ist leer. |
| callback | `function` |  Rückruf mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param Antwort Antworttext zurückgegeben<br><br> Dies kann zwei mögliche Config verfügen:<br><br> Wenn die Anforderung erfolgreich war gibt Jsonstring mit folgenden Schlüssel zurück:<br><br> a.) "HttpResponseCode": der Antwortcode der Anforderung.<br><br> b) "HttpResponseHeader": die HTTP-Antwortheader<br><br> c.) "HttpResponseBody": der Antworttext für Anforderung zurückgegeben.<br><br> Wenn es ein Fehler wurde zurückgegeben:<br><br> a.) "Das Format HttpErrorCode": der Fehlercode<br><br> b) "HttpErrorMessage": die Fehlermeldung eg. Fehlerhafte URL ist, kann keine Verbindung zum Hosten von usw. herstellen.<br><br>\*{Zeichenfolge} @param Fehler Fehler, wenn: Dies umfasst den Standardfehler Code KASClient-Dokumentation. |

**Gibt:**`void`

___

<a id="printf"></a>

###  <a name="printf"></a>printf

▸ **Printf**(Hauptfenster: *`string`*,... Args: * `any`[]*):`string`

Gibt eine Zeichenfolge zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Hauptfenster | `string` |
| `Rest`args | `any`[] |  Array von Argumenten. |

**Gibt:**`string`

___

<a id="readtalkbackmessage"></a>

###  <a name="readtalkbackmessage"></a>readTalkBackMessage

▸ **ReadTalkBackMessage**(TalkBackMessage: *`string`*):`void`

Liest den Text, wenn TalkBack/VoiceOver aktiviert

**Parameter:**

| Name | Typ |
| ------ | ------ |
| talkBackMessage | `string` |

**Gibt:**`void`

___

<a id="registerhardwarebackpresscallback"></a>

###  <a name="registerhardwarebackpresscallback"></a>registerHardwareBackPressCallback

▸ **RegisterHardwareBackPressCallback**(Callback?: *`function`*):`void`

Registriert einen Rückruf in Hardware drücken Sie die zurück-Schaltfläche (für Android) ausgeführt werden

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`Rückruf | `function` |  null |  Methode ausführen |

**Gibt:**`void`

___

<a id="setnativetoolbarproperties"></a>

###  <a name="setnativetoolbarproperties"></a>setNativeToolbarProperties

▸ **SetNativeToolbarProperties**(Eigenschaften: *[KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md)*):`void`

Einige Eigenschaften festgelegt, wenn Sie mithilfe von systemeigenen Symbolleiste

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var nativeToolbarProps = new KASClient.KASNativeToolbarProperties();
nativeToolbarProps.icon = "<image>"
nativeToolbarProps.title = "<title>";
nativeToolbarProps.subtitle = "<subtitle>";
KASClient.App.setNativeToolbarProperties(nativeToolbarProps);
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| properties | [KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md) |   |

**Gibt:**`void`

___

<a id="setuserstrings"></a>

###  <a name="setuserstrings"></a>setUserStrings

▸ **SetUserStrings**(Strings?: *`JSON`*):`void`

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| `Default value`Zeichenfolgen | `JSON` |  null |

**Gibt:**`void`

___

<a id="showattachmentpickerasync"></a>

###  <a name="showattachmentpickerasync"></a>showAttachmentPickerAsync

▸ **ShowAttachmentPickerAsync**(SupportedTypes: * [KASAttachmentType](../enums/kasclient.kasattachmenttype.md)[]*, Eigenschaften: *`JSON`*, Rückruf: *`function`*):`void`

Zeigt eine Anlage Personenauswahl in der systemeigenen Ebene

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var attachmentsTypesToShow = [];
attachmentsTypesToShow.push(KASClient.KASAttachmentType.Image);
attachmentsTypesToShow.push(KASClient.KASAttachmentType.Document);
attachmentsTypesToShow.push(KASClient.KASAttachmentType.Audio);
KASClient.App.showAttachmentPickerAsync(attachmentsTypesToShow, null, function (selectedAttachments, error) {
      if (error != null) {
                      return;
      }
      if (selectedAttachments && selectedAttachments.length > 0) {
          for (var i = 0; i < selectedAttachments.length; i++) {
              if (selectedAttachments[i].type == KASClient.KASAttachmentType.Image) {
                    this.imageAttachmentList.push(selectedAttachments[i]);
              }
              ...
           }...
      }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| supportedTypes | [KASAttachmentType](../enums/kasclient.kasattachmenttype.md) [] |  Array von Anlagen in unterstützten Typen der Auswahl. |
| Eigenschaften | `JSON` |  zusätzliche Eigenschaften zum Konfigurieren der Personenauswahl |
| callback | `function` |  mit folgenden Parametern<br><br>\*@param {KASAttachment\[\]} SelectedAttachments Zeichenfolge des ausgewählten Anlagen<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="showbarcodescannerasync"></a>

###  <a name="showbarcodescannerasync"></a>showBarcodeScannerAsync

▸ **ShowBarcodeScannerAsync**(Rückruf: *`function`*):`void`

Startet den Barcode Scanner und gibt das Objekt überprüften zurück

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param BarcodeInfo kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="showcontactpickerasync"></a>

###  <a name="showcontactpickerasync"></a>showContactPickerAsync

▸ **ShowContactPickerAsync**(Titel: *`string`*, SelectedMutableUser: * `string`[]*, SelectedImmutableUser: * `string`[]*, IsSingleSelection: *`boolean`*, Rückruf: *`function`*):`void`

Zeigt eine systemeigene kontaktauswahlfunktion und gibt ein Array von Details für alle ausgewählten Benutzer

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| title | `string` |  der Kontaktauswahlfunktion |
| selectedMutableUser | `string`[] |  Array von ausgewählten Benutzer-IDs |
| selectedImmutableUser | `string`[] |  Array mit fester ausgewählten Benutzer-IDs |
| isSingleSelection | `boolean` |  Einfachauswahl in Kontakt Personenauswahl |
| callback | `function` |  mit folgenden Parameter:<br><br>\*@param {KASUser\[\]} SelectedUsers (Array von Benutzerdetails) kann bei einem Fehler null sein<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:** `void` Array von alle ausgewählten Benutzer Details (Array von JSON)
#### <a name="sample-usage"></a>Beispiel für die Verwendung
```
var alreadySelectedUserIds = [];
KASClient.App.showContactPickerAsync("<picker title>", alreadySelectedUserIds, [], true, function (selectedUsers, error) {
    if (error == null && selectedUsers != null && selectedUsers.length > 0) {
        var selectedUser = selectedUsers[0]; //KASUser
        console.log(selectedUser.id);
    }
});
```

___

<a id="showdurationpickerasync"></a>

###  <a name="showdurationpickerasync"></a>showDurationPickerAsync

▸ **ShowDurationPickerAsync**(DefaultDurationInMinutes: *`number`*, Rückruf: *`function`*):`void`

Zeigt eine systemeigene Dauer Personenauswahl mit Tag, Stunde, minute

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| defaultDurationInMinutes | `number` |  die standardmäßige Dauer auf Personenauswahl angezeigt werden |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Anzahl} @param DurationInMinutes ausgewählt Dauer in Minuten<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="showimageimmersiveview"></a>

###  <a name="showimageimmersiveview"></a>showImageImmersiveView

▸ **ShowImageImmersiveView**(Urls?: * `string`[]*, CurrentImageIndex?: *`number`*):`void`

Bild in fesselnden Ansicht zeigt.

#### <a name="sample-usage"></a>Beispiel für die Verwendung

```
var urlArray = ["path1", "path2"];
KASClient.App.showImageImmersiveView(urlArray);
```

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`URLs | `string`[] |  [] |  Array von Bildern Url: |
| `Default value`currentImageIndex | `number` | 0 |

**Gibt:**`void`

___

<a id="showimagepickerasync"></a>

###  <a name="showimagepickerasync"></a>showImagePickerAsync

▸ **ShowImagePickerAsync**(Rückruf: *`function`*):`void`

Zeigt eine systemeigene Bildauswahl und gibt den Pfad des ausgewählten Bildes

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param SelectedImagePath kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:** `void` Bildspeicherort ausgewählt

___

<a id="showlocationonmap"></a>

###  <a name="showlocationonmap"></a>showLocationOnMap

▸ **ShowLocationOnMap**(Speicherort: *[KASLocation](../classes/kasclient.kaslocation.md)*):`void`

Zeigt einen bestimmten Standort wie unter KASLocation

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| location | [KASLocation](../classes/kasclient.kaslocation.md) |   |

**Gibt:**`void`

___

<a id="shownativeerrormessage"></a>

###  <a name="shownativeerrormessage"></a>showNativeErrorMessage

▸ **ShowNativeErrorMessage**(Nachricht: *`string`*):`void`

Zeigt eine systemeigene Warnung (für iOS) oder ein Toast (für Android) mit der Meldung

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| message | `string` |   |

**Gibt:**`void`

___

<a id="showplacepickerasync"></a>

###  <a name="showplacepickerasync"></a>showPlacePickerAsync

▸ **ShowPlacePickerAsync**(Rückruf: *`function`*):`void`

Zeigt eine systemeigene Place Personenauswahl und gibt die ausgewählte Stelle (Lt, Lg, n)

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{KASLocation} @param SelectedLocation kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="showprogressbar"></a>

###  <a name="showprogressbar"></a>showProgressBar

▸ **ShowProgressBar**(Text: *`string`*):`void`

Zeigt eine systemeigene vollständige Sreen Statusanzeige mit dem angegebenen text

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| text | `string` |   |

**Gibt:**`void`

___

<a id="showqrcodescannerasync"></a>

###  <a name="showqrcodescannerasync"></a>showQRcodeScannerAsync

▸ **ShowQRcodeScannerAsync**(Rückruf: *`function`*):`void`

Startet den QR Code Scanner und gibt das Objekt überprüften zurück

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Zeichenfolge} @param QrCodeInfo kann bei einem Fehler null sein.<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="showuserprofileasync"></a>

###  <a name="showuserprofileasync"></a>showUserProfileAsync

▸ **ShowUserProfileAsync**(Benutzer-ID: *`string`*, IsMiniProfile: *`boolean`*, Rückruf: *`function`*):`void`

Zeigt Profil Seite/Details eines Benutzers

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  des Benutzers, dessen Profil angezeigt werden soll |
| isMiniProfile | `boolean` |  ob Mini Profil ersten angezeigt |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param Erfolg true, wenn der Vorgang erfolgreich war, False andernfalls<br><br>\*{Zeichenfolge} @param Fehlermeldung bei einem Fehler, null, andernfalls |

**Gibt:**`void`

___

<a id="startchatasync"></a>

###  <a name="startchatasync"></a>startChatAsync

▸ **StartChatAsync**(Benutzer-ID: *`string`*, Rückruf: *`function`*):`void`

Startet Chat mit einem Benutzer

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  des Benutzers |
| callback | `function` |  mit folgenden Parameter:<br><br>\*{Boolean} @param Erfolg<br><br>\*{Zeichenfolge} @param Fehler |

**Gibt:**`void`

___

