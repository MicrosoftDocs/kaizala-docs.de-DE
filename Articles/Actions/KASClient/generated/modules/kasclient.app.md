[](../README.md) > [KASClient](../modules/kasclient.md) > -[App](../modules/kasclient.app.md)

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

▸ **cancelAttachmentDownloadAsync**(Attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Callback: *`function`*):`void`

Abbrechen eines in der Warteschlange befindlichen Downloadvorgangs für eine Anlage

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| attachment | [KASAttachment](../classes/kasclient.kasattachment.md) |  \- |
| callback | `function` |  mit Fehler-param-Error-Zeichenfolge im Fehlerfall; andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="dismisscurrentscreen"></a>

###  <a name="dismisscurrentscreen"></a>dismissCurrentScreen

▸ **dismissCurrentScreen**():`void`

Schließen des Bildschirms der aktuell geöffneten Aktion (Erstellung, Antwort oder Zusammenfassung)

**Gibt Folgendes zurück:**`void`

___

<a id="downloadattachmentasync"></a>

###  <a name="downloadattachmentasync"></a>downloadAttachmentAsync

▸ **downloadAttachmentAsync**(Attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Callback: *`function`*):`void`

Herunterladen der angegebenen Anlage

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| attachment | [KASAttachment](../classes/kasclient.kasattachment.md) |  Anlage mit einem gültigen Serverpfad zum herunterladen |
| callback | `function` |  Rückruf beim Herunterladen mit unter params<br><br>\*@param {KASAttachment} downloadedAttachment die heruntergeladene Anlage<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="generatebase64thumbnailasync"></a>

###  <a name="generatebase64thumbnailasync"></a>generateBase64ThumbnailAsync

▸ **generateBase64ThumbnailAsync**(LocalPath: *`string`*, Callback: *`function`*):`void`

Erstellt eine Base64-Miniaturansicht für ein Bild, dessen localPath angegeben ist.

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| localPath | `string` |  localPath für die imageAttachment, deren Miniaturansicht generiert werden muss |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} Thumbnail der Base64-Wert<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="generateuuidasync"></a>

###  <a name="generateuuidasync"></a>generateUUIDAsync

▸ **generateUUIDAsync**(Callback: *`function`*):`void`

Ruft die neue UUID ab.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
 KASClient.App.generateUUIDAsync(function (uuid, error) {
    console.log("generatedUUIDAsync", uuid);
    ...
 });
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} UUID neu generierte UUID<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getapplocaleasync"></a>

###  <a name="getapplocaleasync"></a>getAppLocaleAsync

▸ **getAppLocaleAsync**(Callback: *`function`*):`void`

Ruft das aktuelle App-Gebietsschema, die Sprache, in der die APP gerendert wird, zur Lokalisierung von MiniApp-Zeichenfolgen ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string}-Gebietsschema kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getcalendarnameasync"></a>

###  <a name="getcalendarnameasync"></a>getCalendarNameAsync

▸ **getCalendarNameAsync**(Callback: *`function`*):`void`

Ruft die aktuelle Systemkalender Einstellung ab. Dies ist hauptsächlich für iOS, um den in der Telefoneinstellung festgelegten Kalendernamen wie gregorianisches oder japanisches oder Buddhisten zu identifizieren.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} calendarname kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getconversationdetailsasync"></a>

###  <a name="getconversationdetailsasync"></a>getConversationDetailsAsync

▸ **getConversationDetailsAsync**(Callback: *`function`*):`void`

Ruft Konversations bezogene Eigenschaften ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASConversationDetails} Ergebnis Unterhaltung-Eigenschaften<br><br>\*@param {String}-Fehler-JSON-Zeichenfolge für das KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___

<a id="getcurrentdevicelocationasync"></a>

###  <a name="getcurrentdevicelocationasync"></a>getCurrentDeviceLocationAsync

▸ **getCurrentDeviceLocationAsync**(Callback: *`function`*):`void`

Ruft den aktuellen Geräte Speicherort ab.

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} Speicherort kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getcurrentlocale"></a>

###  <a name="getcurrentlocale"></a>getCurrentLocale

▸ **getCurrentLocale**():`string`

**Gibt Folgendes zurück:**`string`

___

<a id="getdeviceidasync"></a>

###  <a name="getdeviceidasync"></a>getDeviceIdAsync

▸ **getDeviceIdAsync**(Callback: *`function`*):`void`

Ruft die Geräte-Nr ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string}-Geräte-Nr. vom ganzzahligen Dienst<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getdevicelocationasync"></a>

###  <a name="getdevicelocationasync"></a>getDeviceLocationAsync

▸ **getDeviceLocationAsync**(Callback: *`function`*):`void`

Ruft den Speicherort des zuvor gespeicherten Geräts ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} Speicherort kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getfontsizemultiplierasync"></a>

###  <a name="getfontsizemultiplierasync"></a>getFontSizeMultiplierAsync

▸ **getFontSizeMultiplierAsync**(Callback: *`function`*):`void`

Ruft den Schriftgrad Multiplikator für großen Text ab. Current nur für iOS erforderlich.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit unter params<br><br>\*@param {string} Multiplikator<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getforwardcontextasync"></a>

###  <a name="getforwardcontextasync"></a>getForwardContextAsync

▸ **getForwardContextAsync**(Callback: *`function`*):`void`

Ruft vorwärts Kontext Details wie: Kartenerstellung befindet sich im weitergeleiteten Modus

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {JSON} gibt die Kontext Details in der JSON-Struktur zurück. |

**Gibt Folgendes zurück:**`void`

___

<a id="getisapptimeformat24hoursasync"></a>

###  <a name="getisapptimeformat24hoursasync"></a>getIsAppTimeFormat24HoursAsync

▸ **getIsAppTimeFormat24HoursAsync**(Callback: *`function`*):`void`

Ruft das aktuelle App-Zeitformat ist 24 Stunden oder nicht, das vom Benutzer ausgewählte Zeitformat, nützlich für die Formatierung von Datum Zeichenfolgen ordnungsgemäß

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} isAppTimeFormat24Hours kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getlocalizedstringsasync"></a>

###  <a name="getlocalizedstringsasync"></a>getLocalizedStringsAsync

▸ **getLocalizedStringsAsync**(Callback: *`function`*):`void`

Ruft das Wörterbuch der lokalisierten Zeichenfolgen basierend auf dem aktuellen App-Gebietsschema ab. Zeichenfolgen müssen innerhalb des Pakets mit Namen wie: Strings\_en. JSON, Strings\_Hi. JSON usw. angegeben werden.

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {JSON}-Zeichenfolgen können im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getlocationaddressasync"></a>

###  <a name="getlocationaddressasync"></a>getLocationAddressAsync

▸ **getLocationAddressAsync**(params: *[KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md)*, Callback: *`function`*):`void`

Adresszeichenfolge für angegebene Koordinaten abrufen

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| callback | `function` |  Callback on Address FETCH with below params<br><br>\*@param {JSON} Speicherort eine JSON mit latitute Längen-und anderen Informaion<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getmapimageasbase64async"></a>

###  <a name="getmapimageasbase64async"></a>getMapImageAsBase64Async

▸ **getMapImageAsBase64Async**(params: *[KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md)*, Callback: *`function`*):`void`

Herunterladen des Basis 64-Bild der Karte für die angegebenen Koordinaten

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| callback | `function` |  beim Herunterladen mit unter params<br><br>\*@param {string} AttachmentType Base64-Wert der Anlage<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="geto365userdetailsasync"></a>

###  <a name="geto365userdetailsasync"></a>getO365UserDetailsAsync

▸ **getO365UserDetailsAsync**(Callback: *`function`*):`void`

Ruft Details des aktuellen angemeldeten O365-Benutzers ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {JSON} gibt die UserDetails in der JSON-Struktur zurück. |

**Gibt Folgendes zurück:**`void`

___

<a id="getpackagecustomsettingsasync"></a>

###  <a name="getpackagecustomsettingsasync"></a>getPackageCustomSettingsAsync

▸ **getPackageCustomSettingsAsync**(Callback: *`function`*):`void`

Ruft alle Anpassungseinstellungen für ein Paket ab (wird bei Type-4-Paketen und deren Basis verwendet).

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {JSON}-Einstellungen können im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="getusersdetailsasync"></a>

###  <a name="getusersdetailsasync"></a>getUsersDetailsAsync

▸- **getUsersDetailsAsync**(userids: * `string`[]*, Callback *`function`*:):`void`

Ruft Benutzer Details (Name, PIC, Telefonnummer usw.) gegen ihre IDs ab.

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| UserIds | `string`[] |  Array von Benutzer-IDs |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Dictionary<UserId: String, Infor: KASUser>} userIdToInfoMap (Benutzer Details gegen ihre IDs) können im Fehlerfall NULL sein.<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="hideprogressbar"></a>

###  <a name="hideprogressbar"></a>hideProgressBar

▸ **hideProgressBar**():`void`

Blendet die aktuelle Statusanzeige aus, falls vorhanden.

**Gibt Folgendes zurück:**`void`

___

<a id="isattachmentdownloadingasync"></a>

###  <a name="isattachmentdownloadingasync"></a>isAttachmentDownloadingAsync

▸ **isAttachmentDownloadingAsync**(Attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Callback: *`function`*):`void`

Herunterladen der angegebenen Anlage

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| attachment | [KASAttachment](../classes/kasclient.kasattachment.md) |  Anlage mit einem gültigen Serverpfad zum herunterladen |
| callback | `function` |  Rückruf beim Herunterladen mit unter params<br><br>\*@param {Boolean} isAttachmentDownloadingOrDownLoaded-Flag, das angibt, ob die Anlage heruntergeladen<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="isauthenticationtyepsupportedasync"></a>

###  <a name="isauthenticationtyepsupportedasync"></a>isAuthenticationTyepSupportedAsync

▸ **isAuthenticationTyepSupportedAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, Callback: *`function`*):`void`

Überprüft, ob die Authentifizierung vom Typ möglich ist oder nicht.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType. None |  Typ der Authentifizierung. |
| callback | `function` | - |  mit folgenden Parametern:<br><br>\*@param {Boolean} isSuccessable true, wenn Fingerdruck möglich ist<br><br>\*@param {string} reasonCode Reason Code Why Fingerprint is not possible |

**Gibt Folgendes zurück:**`void`

___

<a id="istalkbackenabledasync"></a>

###  <a name="istalkbackenabledasync"></a>isTalkBackEnabledAsync

▸ **isTalkBackEnabledAsync**(Callback: *`function`*):`void`

Ruft ab, ob die Kommandofunktion aktiviert ist oder nicht

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} talkBackEnabled true, wenn die Kommandos aktiviert ist |

**Gibt Folgendes zurück:**`void`

___

<a id="logtoreport"></a>

###  <a name="logtoreport"></a>logToReport

▸ **logToReport**(Data: *`string`*):`void`

Protokolliert Daten für "Bericht senden".

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| data | `string` |  string |

**Gibt Folgendes zurück:**`void`

___

<a id="openattachmentimmersiveview"></a>

###  <a name="openattachmentimmersiveview"></a>openAttachmentImmersiveView

▸ **openAttachmentImmersiveView**(AttachmentObj: *[KASAttachment](../classes/kasclient.kasattachment.md)*):`void`

Anlage in immersiver Ansicht öffnen.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| attachmentObj | [KASAttachment](../classes/kasclient.kasattachment.md) |   |

**Gibt Folgendes zurück:**`void`

___

<a id="openimmersiveviewforattachmentlist"></a>

###  <a name="openimmersiveviewforattachmentlist"></a>openImmersiveViewForAttachmentList

▸ **openImmersiveViewForAttachmentList**(attachmentlist: * [KASAttachment](../classes/kasclient.kasattachment.md)[]*, atIndex?: *`number`*):`void`

Anlage in immersiver Ansicht öffnen.

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| attachmentlist | [KASAttachment](../classes/kasclient.kasattachment.md) [] | - |
| `Default value`atIndex | `number` | 0 |

**Gibt Folgendes zurück:**`void`

___

<a id="performauthenticationasync"></a>

###  <a name="performauthenticationasync"></a>performAuthenticationAsync

▸ **performAuthenticationAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, Callback: *`function`*):`void`

Wenn der Authentifizierungstyp zulässig ist, führt diese API die Authentifizierung durch und gibt Success/false Status else zurück, wobei eine Fehlerzeichenfolge mit der Ursache für die Authentifizierung nicht möglich ist.

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| `Default value`authenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType. None |  Typ der Authentifizierung. |
| callback | `function` | - |  mit folgenden Parametern:<br><br>\*@param {Boolean} isSuccessable true, wenn das Formular noch nicht abgelaufen ist<br><br>\*@param {string} reasonCode-Grund Code im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="performhttprequest"></a>

###  <a name="performhttprequest"></a>performHTTPRequest

▸ **performHTTPRequest**(URL: *`string`*, parametersJSON: *`string`*, Callback: *`function`*):`void`

führt eine HTTP-Anforderung aus und gibt die Antwort wie folgt zurück:

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| url | `string` |  zu öffnende Basis-URL |
| parametersJSON | `string` |  JSON String mit Parametern kann als NULL angegeben werden.<br><br> Bei Angabe von NULL wird eine Anforderung an die oben angegebene URL gestellt. Zu den Parametern gehört der Anforderungsheader, die Abfrageparameter (standardmäßig leer), die Request-Methode (Standard Abruf) und der Anforderungstext (der Text, der bereitgestellt wird, wenn die Request-Methode POST ist. Standard leer.) Die Schlüssel für Parameter sind:<br><br> a.) "Methode": Request-Methode. Beispiel: "POST". Standardwert ist "GET".<br><br> b.) "requestBody": Text der Anforderung im Fall von "POST". Standardwert ist leer.<br><br> c.) "requestHeaders": Kopfzeilen, die mit der Anforderung gesendet werden sollen. sollte eine JSON mit<br> Schlüssel als Anforderungsheader und-Wert als den gewünschten Wert. Standardwert ist leer.<br><br> d.) "queryParameters": Abfrageparameter. wird in der URL codiert. sollte eine JSON mit<br> Schlüssel als Parameter Name und Wert als Wert. Standardwert ist leer.<br><br> e.) "requestResourcePath": wird der Basis-URL angefügt. der Standardwert ist leer. |
| callback | `function` |  Callback mit folgenden Parametern:<br><br>\*@param {string} Antworttext zurückgegeben<br><br> Dies kann zwei mögliche Konfigurationsmöglichkeiten haben:<br><br> Wenn die Anforderung erfolgreich war, wird JSON mit den folgenden Schlüsseln zurückgegeben:<br><br> a.) "HttpResponseCode": der Antwortcode der Anforderung.<br><br> b.) "HttpResponseHeader": die Antwort-HTTP-Header<br><br> c.) "HttpResponseBody": der für die Anforderung zurückgegebene Antworttext.<br><br> Wenn ein Netzwerkfehler vorliegt, wird Folgendes zurückgegeben:<br><br> a.) "HttpErrorCode": der Fehlercode<br><br> b.) "HttpErrorMessage": die Fehlermeldung EG. Ungültige URL, keine Verbindung zum Host etc.<br><br>\*@param {string} Error Error if any: Dies umfasst den standardmäßigen Fehlercode, der in der KASClient-Dokumentation definiert ist. |

**Gibt Folgendes zurück:**`void`

___

<a id="printf"></a>

###  <a name="printf"></a>printf

▸ **printf**(Main: *`string`*,... args: * `any`[]*):`string`

Gibt eine Zeichenfolge zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| Haupt | `string` |
| `Rest`args | `any`[] |  Array von Argumenten. |

**Gibt Folgendes zurück:**`string`

___

<a id="readtalkbackmessage"></a>

###  <a name="readtalkbackmessage"></a>readTalkBackMessage

▸ **readTalkBackMessage**(talkBackMessage: *`string`*):`void`

Liest den Text, wenn die Kommandozeile/VoiceOver aktiviert ist.

**Parameter:**

| Name | Typ |
| ------ | ------ |
| talkBackMessage | `string` |

**Gibt Folgendes zurück:**`void`

___

<a id="registerhardwarebackpresscallback"></a>

###  <a name="registerhardwarebackpresscallback"></a>registerHardwareBackPressCallback

▸ **registerHardwareBackPressCallback**(callback?: *`function`*):`void`

Registriert einen Rückruf, der auf Hardware-Schaltflächen drücken (für Android) ausgeführt werden soll

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`Rückruf | `function` |  null |  auszuführende Methode |

**Gibt Folgendes zurück:**`void`

___

<a id="setnativetoolbarproperties"></a>

###  <a name="setnativetoolbarproperties"></a>setNativeToolbarProperties

▸ **setNativeToolbarProperties**(Properties: *[KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md)*):`void`

Legt wenige Eigenschaften fest, wenn die systemeigene Symbolleiste verwendet wird

#### <a name="sample-usage"></a>Beispiel Verwendung

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

**Gibt Folgendes zurück:**`void`

___

<a id="setuserstrings"></a>

###  <a name="setuserstrings"></a>setUserStrings

▸ **setUserStrings**(strings?: *`JSON`*):`void`

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| `Default value`Strings | `JSON` |  null |

**Gibt Folgendes zurück:**`void`

___

<a id="showattachmentpickerasync"></a>

###  <a name="showattachmentpickerasync"></a>showAttachmentPickerAsync

▸ **showAttachmentPickerAsync**(SupportedTypes: * [KASAttachmentType](../enums/kasclient.kasattachmenttype.md)[]*, Props *`JSON`*:, Callback *`function`*:):`void`

Zeigt eine Anlagenauswahl in der systemeigenen Ebene an.

#### <a name="sample-usage"></a>Beispiel Verwendung

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
| supportedTypes | [KASAttachmentType](../enums/kasclient.kasattachmenttype.md) [] |  Array unterstützter Anlagentypen für die Auswahl. |
| Eigenschaften | `JSON` |  zusätzliche Requisiten zum Konfigurieren der Auswahl |
| callback | `function` |  mit den folgenden Parametern<br><br>\*@param {KASAttachment\[\]} selectedAttachments-zeichenfolge ausgewählter anlagen<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="showbarcodescannerasync"></a>

###  <a name="showbarcodescannerasync"></a>showBarcodeScannerAsync

▸ **showBarcodeScannerAsync**(Callback: *`function`*):`void`

Starten des Barcodescanners und Zurückgeben des gescannten Objekts

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} barcodeInfo kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="showcontactpickerasync"></a>

###  <a name="showcontactpickerasync"></a>showContactPickerAsync

▸ **showContactPickerAsync**(Title: *`string`*, selectedMutableUser: * `string`[]*, selectedImmutableUser: * `string`[]*, isSingleSelection: *`boolean`*, Callback: *`function`*):`void`

Zeigt eine systemeigene Kontaktauswahl an und gibt ein Array mit allen Details der ausgewählten Benutzer zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| title | `string` |  der Kontaktauswahl |
| selectedMutableUser | `string`[] |  Array ausgewählter Benutzer-IDs |
| selectedImmutableUser | `string`[] |  Array fester ausgewählter Benutzer-IDs |
| isSingleSelection | `boolean` |  einzelne Auswahl in der Kontaktauswahl |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASUser\[\]} selectedUsers (array von benutzer details) kann im fehlerfall null sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:** `void` Array aller Details der ausgewählten Benutzer (Array von JSON)
#### <a name="sample-usage"></a>Beispiel Verwendung
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

▸ **showDurationPickerAsync**(defaultDurationInMinutes: *`number`*, Callback: *`function`*):`void`

Zeigt eine systemeigene Dauer Auswahl mit Tag/Stunde/Minute an.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| defaultDurationInMinutes | `number` |  die Standarddauer, die bei der Auswahl angezeigt werden soll. |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Zahl} durationInMinutes ausgewählte Dauer in Minuten<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="showimageimmersiveview"></a>

###  <a name="showimageimmersiveview"></a>showImageImmersiveView

▸ **showImageImmersiveView**(urls?: * `string`[]*, currentImageIndex?: *`number`*):`void`

Zeigt das Bild in der immersiven Ansicht an.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var urlArray = ["path1", "path2"];
KASClient.App.showImageImmersiveView(urlArray);
```

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`URLs | `string`[] |  [] |  Array der Bild-URL: |
| `Default value`currentImageIndex | `number` | 0 |

**Gibt Folgendes zurück:**`void`

___

<a id="showimagepickerasync"></a>

###  <a name="showimagepickerasync"></a>showImagePickerAsync

▸ **showImagePickerAsync**(Callback: *`function`*):`void`

Zeigt eine systemeigene Bildauswahl an und gibt den ausgewählten Bild Pfad zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} selectedImagePath kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:** `void` Ausgewählte Bildposition

___

<a id="showlocationonmap"></a>

###  <a name="showlocationonmap"></a>showLocationOnMap

▸ **showLocationOnMap**(Location: *[KASLocation](../classes/kasclient.kaslocation.md)*):`void`

zeigt einen bestimmten Speicherort an, wie in KASLocation

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| location | [KASLocation](../classes/kasclient.kaslocation.md) |   |

**Gibt Folgendes zurück:**`void`

___

<a id="shownativeerrormessage"></a>

###  <a name="shownativeerrormessage"></a>showNativeErrorMessage

▸ **showNativeErrorMessage**(Message: *`string`*):`void`

Zeigt eine systemeigene Warnung (für iOS) oder einen Toast (für Android) mit der Nachricht

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| message | `string` |   |

**Gibt Folgendes zurück:**`void`

___

<a id="showplacepickerasync"></a>

###  <a name="showplacepickerasync"></a>showPlacePickerAsync

▸ **showPlacePickerAsync**(Callback: *`function`*):`void`

Zeigt eine systemeigene Ortsauswahl an und gibt die ausgewählte Stelle zurück (lt, LG, n)

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {KASLocation} selectedLocation kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="showprogressbar"></a>

###  <a name="showprogressbar"></a>showProgressBar

▸ **showProgressBar**(Text: *`string`*):`void`

Zeigt eine systemeigene vollständige Sreen-Statusanzeige mit dem angegebenen Text an.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| text | `string` |   |

**Gibt Folgendes zurück:**`void`

___

<a id="showqrcodescannerasync"></a>

###  <a name="showqrcodescannerasync"></a>showQRcodeScannerAsync

▸ **showQRcodeScannerAsync**(Callback: *`function`*):`void`

Startet den QR-Code Scanner und gibt das gescannte Objekt zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {string} qrCodeInfo kann im Fehlerfall NULL sein<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="showuserprofileasync"></a>

###  <a name="showuserprofileasync"></a>showUserProfileAsync

▸ **showUserProfileAsync**(UserID: *`string`*, isMiniProfile: *`boolean`*, Callback: *`function`*):`void`

Zeigt die Profilseite/Details eines Benutzers

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  des Benutzers, dessen Profil angezeigt werden soll |
| isMiniProfile | `boolean` |  ob das Miniprofil zuerst angezeigt werden soll |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} Erfolg true, wenn erfolgreich, andernfalls false<br><br>\*@param {string}-Fehlermeldung im Fehlerfall, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

<a id="startchatasync"></a>

###  <a name="startchatasync"></a>startChatAsync

▸ **startChatAsync**(UserID: *`string`*, Callback: *`function`*):`void`

Startet den Chat mit einem Benutzer

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  des Benutzers |
| callback | `function` |  mit folgenden Parametern:<br><br>\*@param {Boolean} Erfolg<br><br>\*@param {String}-Fehler |

**Gibt Folgendes zurück:**`void`

___

