[](../README.md) > [KASClient](../modules/kasclient.md) > -[App](../modules/kasclient.app.md)

# <a name="module-app"></a>Modul: App

## <a name="index"></a>Index 

### <a name="functions"></a>Funktionen

* [cancelAttachmentDownloadAsync](kasclient.app.md#cancelattachmentdownloadasync)
* [deleteActionLocalCacheAsync](kasclient.app.md#deleteactionlocalcacheasync)
* [deleteDataFromTmpDirAsync](kasclient.app.md#deletedatafromtmpdirasync)
* [dismissCurrentScreen](kasclient.app.md#dismisscurrentscreen)
* [downloadAttachmentAsync](kasclient.app.md#downloadattachmentasync)
* [fetchTenantUserAttributeDetailsAsync](kasclient.app.md#fetchtenantuserattributedetailsasync)
* [fetchTenantUserProfilesAsync](kasclient.app.md#fetchtenantuserprofilesasync)
* [generateBase64ThumbnailAsync](kasclient.app.md#generatebase64thumbnailasync)
* [generateUUIDAsync](kasclient.app.md#generateuuidasync)
* [getActionLocalCacheAsync](kasclient.app.md#getactionlocalcacheasync)
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
* [readDataFromTmpDirAsync](kasclient.app.md#readdatafromtmpdirasync)
* [readTalkBackMessage](kasclient.app.md#readtalkbackmessage)
* [registerHardwareBackPressCallback](kasclient.app.md#registerhardwarebackpresscallback)
* [saveDataInTmpDirAsync](kasclient.app.md#savedataintmpdirasync)
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
* [updateActionLocalCacheAsync](kasclient.app.md#updateactionlocalcacheasync)
* [updateTenantUserProfileAsync](kasclient.app.md#updatetenantuserprofileasync)

---

## <a name="functions"></a>Funktionen

<a id="cancelattachmentdownloadasync"></a>

###  <a name="cancelattachmentdownloadasync"></a>cancelAttachmentDownloadAsync

▸ **cancelAttachmentDownloadAsync**(Attachment: *[KASAttachment](../classes/kasclient.kasattachment.md)*, Callback: *`function`*):`void`

Abbrechen eines Downloadvorgangs in der Warteschlange für eine Anlage

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
| callback | `function` |  mit Fehler-param-Error-Zeichenfolge im Falle eines Fehlers; andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="deleteactionlocalcacheasync"></a>

###  <a name="deleteactionlocalcacheasync"></a>deleteActionLocalCacheAsync

▸ **deleteActionLocalCacheAsync**(actionLocalCacheProps: *[KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)*, Callback: *`function`*):`void`

Löschen des angegebenen Schlüssels aus dem lokalen Datencache

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionLocalCacheProps | [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md) |  Eigenschaft von Daten, die aus dem Cache gelöscht werden sollen |
| callback | `function` |  Rückruf mit den folgenden para \* \* Metern: @param {Boolean} Success gibt an, ob das Update \* \* erfolgreich war oder nicht @param {string} Error JSON String for the KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___
<a id="deletedatafromtmpdirasync"></a>

###  <a name="deletedatafromtmpdirasync"></a>deleteDataFromTmpDirAsync

▸ **deleteDataFromTmpDirAsync**(filePath: *`string`*, Callback: *`function`*):`void`

Löscht die Datei aus dem temporären Cachespeicher. Wird in Verbindung mit API-saveDataInTmpDirAsync für die Dateien verwendet, die mit dieser API gespeichert werden.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.App.deleteDataFromTmpDirAsync(filePath, function (success, error) {
    if (error == null && success) {
       // Action's code in success case
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| FilePath | `string` |  Dateipfad, der gelesen werden sollte |
| callback | `function` |  mit den folgenden Parametern: |

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
| callback | `function` |  Rückruf beim Herunterladen abgeschlossen mit unter Parameter<br><br>\*@param {KASAttachment} downloadedAttachment der Anlage, die heruntergeladen wurde<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="fetchtenantuserattributedetailsasync"></a>

###  <a name="fetchtenantuserattributedetailsasync"></a>fetchTenantUserAttributeDetailsAsync

▸ **fetchTenantUserAttributeDetailsAsync**(Callback: *`function`*):`void`

Ruft die Details des Mandanten Attributs ab. Der Mandant der Unterhaltung im Kontext wird hierfür verwendet.
#### <a name="note"></a>Hinweis

Die Aktion sollte zum gleichen Mandanten der Unterhaltung gehören, und der Benutzer muss bei diesem Mandanten angemeldet sein, damit diese API funktioniert.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.App.fetchTenantUserAttributeDetailsAsync(function(tenantAttributes, error) {
    if (error == null && tenantAttributes.length > 0) {
        var tenantAttribute = tenantAttributes[0]; // TenantAttribute
        console.log(tenantAttribute.id + " : " + tenantAttribute.name);
    }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {mandantattribute\[\]} tenantAttributes Array von Mandanten Attributen<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="fetchtenantuserprofilesasync"></a>

###  <a name="fetchtenantuserprofilesasync"></a>fetchTenantUserProfilesAsync

▸ **fetchTenantUserProfilesAsync**(userids: * `string`[]*, Callback: *`function`*):`void`

Ruft die Mandanten Attribute der angegebenen Benutzer ab. Der Mandant der Unterhaltung im Kontext wird hierfür verwendet.
#### <a name="note"></a>Hinweis

Die Aktion sollte zum gleichen Mandanten der Unterhaltung gehören, und der Benutzer muss bei diesem Mandanten angemeldet sein, damit diese API funktioniert.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
// Fetch current user's tenant profile
KASClient.App.fetchTenantUserProfilesAsync(null, function(tenantUserProfiles, error) {
    if (error == null && tenantUserProfiles.length > 0) {
        var userProfile = tenantUserProfiles[0]; // TenantUserProfile
        var tenantAttributeData = userProfile.tenantAttributeDataList[0]; // TenantAttributeData
        console.log(tenantAttributeData.attributeId + " : " + tenantAttributeData.attributeValue);
    }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| UserIds | `string`[] |  Array von Benutzer-IDs; Wenn er NULL oder leer ist, wird das Mandanten Profil des aktuellen Benutzers abgerufen. |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {TenantUserProfile\[\]} tenantUserProfiles-Array der Mandanten Profile der Benutzer (Attribut-ID-Wert-Paare)<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="generatebase64thumbnailasync"></a>

###  <a name="generatebase64thumbnailasync"></a>generateBase64ThumbnailAsync

▸ **generateBase64ThumbnailAsync**(LocalPath: *`string`*, Callback: *`function`*):`void`

Generiert eine Base64-Miniaturansicht für ein Bild, dessen LocalPath angegeben ist.

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
| LocalPath | `string` |  LocalPath für die imageattachment, deren Miniaturansicht generiert werden muss |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} Thumbnail der Base64-Wert<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

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
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} UUID neu generierte UUID<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getactionlocalcacheasync"></a>

###  <a name="getactionlocalcacheasync"></a>getActionLocalCacheAsync

▸ **getActionLocalCacheAsync**(actionLocalCacheProps: *[KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)*, Callback: *`function`*):`void`

Ruft den angegebenen Schlüssel für den lokalen Datencache Wert wird auf der in KASActionLocalCacheProp genannten Ebene entsprechend gespeichert.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionLocalCacheProps | [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md) |  Eigenschaft von Daten, die aus dem Cache abgerufen werden sollen |
| callback | `function` |  Rückruf mit den folgenden para \* \* Metern: @param {KASActionLocalCacheProp} actionLocalCacheProps gibt an, ob das Update \* \* erfolgreich war oder nicht @param {string} Error JSON String for the KASError-Objekt mit Fehlercode und/ oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___
<a id="getapplocaleasync"></a>

###  <a name="getapplocaleasync"></a>getAppLocaleAsync

▸ **getAppLocaleAsync**(Callback: *`function`*):`void`

Ruft das aktuelle App-Gebietsschema ab, die Sprache, in der die APP gerendert wird, nützlich zum Lokalisieren von MiniApp-Zeichenfolgen.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Zeichenfolgen} Gebietsschema kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getcalendarnameasync"></a>

###  <a name="getcalendarnameasync"></a>getCalendarNameAsync

▸ **getCalendarNameAsync**(Callback: *`function`*):`void`

Ruft die aktuelle Systemkalender Einstellung ab. Dies ist vor allem für IOS, um den Kalendernamen festzulegen, der in der Telefoneinstellung wie gregorianisches oder Japanisch oder Buddhisten festgelegt wurde.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} calendarname kann im Fehlerfall NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getconversationdetailsasync"></a>

###  <a name="getconversationdetailsasync"></a>getConversationDetailsAsync

▸ **getConversationDetailsAsync**(Callback: *`function`*):`void`

Ruft Konversations bezogene Eigenschaften ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASConversationDetails} Ergebnis Unterhaltungseigenschaften<br><br>\*@param {string} Error JSON-Zeichenfolge für das KASError-Objekt, das den Fehlercode und/oder die Beschreibung enthält. |

**Gibt Folgendes zurück:**`void`

___
<a id="getcurrentdevicelocationasync"></a>

###  <a name="getcurrentdevicelocationasync"></a>getCurrentDeviceLocationAsync

▸ **getCurrentDeviceLocationAsync**(Callback: *`function`*, canUseCachedLocation?: *`boolean`*):`void`

Ruft den aktuellen Geräte Speicherort ab.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
 KASClient.App.getCurrentDeviceLocationAsync(function (location, error){
     if(error != null) {
          return;
     }
     //use location(KASLocation) as the device location
 }, false);
```

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| callback | `function` | - |  mit den folgenden Parametern:<br><br>\*@param {Zeichenfolge} Speicherort kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |
| `Default value`canUseCachedLocation | `boolean` | false |  (optional, Standard, wenn false) Wenn dieses Flag auf true festgelegt ist, kann Platform einen zwischengespeicherten Speicherort von bis zu 30Min alt zurückgeben, falls beim Abrufen des aktuellen Standorts ein Fehler auftritt. |

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
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Zeichenfolge} Device-Wert aus dem ganzzahligen Dienst erhalten<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getdevicelocationasync"></a>

###  <a name="getdevicelocationasync"></a>getDeviceLocationAsync

▸ **getDeviceLocationAsync**(Callback: *`function`*):`void`

Ruft den Speicherort des zuvor gespeicherten Geräts ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Zeichenfolge} Speicherort kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getfontsizemultiplierasync"></a>

###  <a name="getfontsizemultiplierasync"></a>getFontSizeMultiplierAsync

▸ **getFontSizeMultiplierAsync**(Callback: *`function`*):`void`

Ruft den Schriftgrad Multiplikator für großen Text ab. Aktuell nur für IOS erforderlich.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit unter Parameter<br><br>\*@param {string}-Multiplikator<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getforwardcontextasync"></a>

###  <a name="getforwardcontextasync"></a>getForwardContextAsync

▸ **getForwardContextAsync**(Callback: *`function`*):`void`

Ruft vorwärts Kontext Details wie: Kartenerstellung befindet sich im weitergeleiteten Modus

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {JSON} gibt die Kontext Details in der JSON-Struktur zurück. |

**Gibt Folgendes zurück:**`void`

___
<a id="getisapptimeformat24hoursasync"></a>

###  <a name="getisapptimeformat24hoursasync"></a>getIsAppTimeFormat24HoursAsync

▸ **getIsAppTimeFormat24HoursAsync**(Callback: *`function`*):`void`

Ruft das aktuelle App-Zeitformat ist 24 Stunden oder nicht, das vom Benutzer ausgewählte Zeitformat, nützlich für die Formatierung von Datum Uhrzeit Zeichenfolgen ordnungsgemäß

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} isAppTimeFormat24Hours kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getlocalizedstringsasync"></a>

###  <a name="getlocalizedstringsasync"></a>getLocalizedStringsAsync

▸ **getLocalizedStringsAsync**(Callback: *`function`*):`void`

Ruft das lokalisierte Zeichenfolgenwörterbuch basierend auf dem aktuellen App-Gebietsschema ab. Zeichenfolgen müssen innerhalb des Pakets mit Namen wie: Strings\_en. JSON, Strings\_Hi. JSON, etc. bereitgestellt werden.

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
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {JSON} Zeichenfolgen können im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getlocationaddressasync"></a>

###  <a name="getlocationaddressasync"></a>getLocationAddressAsync

▸ **getLocationAddressAsync**(params: *[KASLocationAddressParams](../classes/kasclient.kaslocationaddressparams.md)*, Callback: *`function`*):`void`

Abrufen der Adresszeichenfolge für angegebene Koordinaten

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
| callback | `function` |  Rückruf bei Adress Abruf mit unter Parameter<br><br>\*@param {JSON} Speicherort eine JSON, die latitute Längengrad und andere informaungen enthält<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getmapimageasbase64async"></a>

###  <a name="getmapimageasbase64async"></a>getMapImageAsBase64Async

▸ **getMapImageAsBase64Async**(params: *[KASLocationStaticMapImageParams](../classes/kasclient.kaslocationstaticmapimageparams.md)*, Callback: *`function`*):`void`

Laden Sie das Base 64-Image von Map für die angegebenen Koordinaten herunter.

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
| callback | `function` |  beim Herunterladen abgeschlossen mit unter Parameter<br><br>\*@param {string} Attachment String Base64-Wert der Anlage<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="geto365userdetailsasync"></a>

###  <a name="geto365userdetailsasync"></a>getO365UserDetailsAsync

▸ **getO365UserDetailsAsync**(Callback: *`function`*):`void`

Ruft Details des aktuellen angemeldeten O365-Benutzers ab.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {JSON} gibt die UserDetails in der JSON-Struktur zurück. |

**Gibt Folgendes zurück:**`void`

___
<a id="getpackagecustomsettingsasync"></a>

###  <a name="getpackagecustomsettingsasync"></a>getPackageCustomSettingsAsync

▸ **getPackageCustomSettingsAsync**(Callback: *`function`*):`void`

Ruft alle Anpassungseinstellungen für ein Paket ab (wird für den Fall von Typ-4-Paketen und deren Basis verwendet).

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
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {JSON}-Einstellungen können im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="getusersdetailsasync"></a>

###  <a name="getusersdetailsasync"></a>getUsersDetailsAsync

▸ **getUsersDetailsAsync**(userids: * `string`[]*, Callback: *`function`*):`void`

Ruft die Details der Benutzer (Name, PIC, Telefonnummer, usw.) anhand ihrer IDs ab.

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
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Wörterbuch<UserID: String, InfoInfo: KASUser>} userIdToInfoMap (Benutzer Details mit Ihren IDs) können im Falle eines Fehlers NULL sein.<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="hideprogressbar"></a>

###  <a name="hideprogressbar"></a>hideProgressBar

▸ **hideProgressBar**():`void`

Blendet den aktuellen Statusbalken aus, falls vorhanden

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
| callback | `function` |  Rückruf beim Herunterladen abgeschlossen mit unter Parameter<br><br>\*@param {Boolean} isAttachmentDownloadingOrDownLoaded-Flag, das angibt, ob Attachment heruntergeladen/heruntergeladen wird<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="isauthenticationtyepsupportedasync"></a>

###  <a name="isauthenticationtyepsupportedasync"></a>isAuthenticationTyepSupportedAsync

▸ **isAuthenticationTyepSupportedAsync**(AuthenticationType?: *[KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md)*, Callback: *`function`*):`void`

Überprüft, ob die Authentifizierung vom Typ möglich ist oder nicht.

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`AuthenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType. None |  Typ der Authentifizierung. |
| callback | `function` | - |  mit den folgenden Parametern:<br><br>\*@param {Boolean} issuccessable true, wenn Fingerabdruck möglich ist<br><br>\*@param {string} reasonCode Ursachencode Warum Fingerabdruck nicht möglich |

**Gibt Folgendes zurück:**`void`

___
<a id="istalkbackenabledasync"></a>

###  <a name="istalkbackenabledasync"></a>isTalkBackEnabledAsync

▸ **isTalkBackEnabledAsync**(Callback: *`function`*):`void`

Ruft ab, ob die Kommandofunktion aktiviert ist oder nicht

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} talkBackEnabled true, wenn die Kommandooption aktiviert ist |

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

▸ **openAttachmentImmersiveView**(attachmentObj: *[KASAttachment](../classes/kasclient.kasattachment.md)*):`void`

Öffnen Sie die Anlage in der immersiven Ansicht.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| attachmentObj | [KASAttachment](../classes/kasclient.kasattachment.md) |   |

**Gibt Folgendes zurück:**`void`

___
<a id="openimmersiveviewforattachmentlist"></a>

###  <a name="openimmersiveviewforattachmentlist"></a>openImmersiveViewForAttachmentList

▸ **openImmersiveViewForAttachmentList**(attachmentlist: * [KASAttachment](../classes/kasclient.kasattachment.md)[]*, atIndex?: *`number`*):`void`

Öffnen Sie die Anlage in der immersiven Ansicht.

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

Wenn der Authentifizierungstyp zulässig ist, führt diese API die Authentifizierung durch und gibt Success/false zurück, andernfalls wird eine Fehlerzeichenfolge mit dem Grund zurückgegeben, warum die Authentifizierung nicht möglich ist.

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
| `Default value`AuthenticationType | [KASAuthenticationType](../enums/kasclient.kasauthenticationtype.md) |  KASAuthenticationType. None |  Typ der Authentifizierung. |
| callback | `function` | - |  mit den folgenden Parametern:<br><br>\*@param {Boolean} issuccessable true, wenn das Formular noch nicht abgelaufen ist<br><br>\*@param {string} reasonCode Reason Code im Fall eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="performhttprequest"></a>

###  <a name="performhttprequest"></a>performHTTPRequest

▸ **performHTTPRequest**(URL: *`string`*, parametersJSON: *`string`*, Callback: *`function`*):`void`

führt eine HTTP-Anforderung aus und gibt die Antwort wie unten angegeben zurück:

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
| parametersJSON | `string` |  JSON String mit Parametern kann als NULL angegeben werden.<br><br> Bei Angabe als NULL wird eine Anforderung an die oben angegebene URL gestellt. Parameter umfassen Anforderungsheader, Abfrageparameter (Standard leer), Anforderungsmethode (Standard Get) und Anforderungstext (der Text, der bereitgestellt werden soll, wenn die Anforderungsmethode bereit ist. Standard leer.) Die Schlüssel für Parameter sind:<br><br> a.) "Method": Request-Methode. Beispiel: "Post". Standardwert "Get".<br><br> b.) "requestBody": Anforderungstext im Fall von "Post". Standardwert ist leer.<br><br> c.) "requestHeaders": Kopfzeilen, die mit Request gesendet werden sollen. sollte eine JSON mit<br> Key als Anforderungsheader und Wert als den gewünschten Wert. Standardwert ist leer.<br><br> d.) "queryParameters": Abfrageparameter. wird in der URL codiert. sollte eine JSON mit<br> Key als Parameter Name und Wert als Wert. Standardwert ist leer.<br><br> e.) "requestResourcePath": wird an die Basis-URL angehängt. der Standardwert ist leer. |
| callback | `function` |  Rückruf mit den folgenden Parametern:<br><br>\*@param {string} Antwort Antworttext zurückgegeben<br><br> Dies könnte zwei mögliche Konfigurationen haben:<br><br> Wenn die Anforderung erfolgreich verlaufen ist, wird JsonType mit den folgenden Schlüsseln zurückgegeben:<br><br> a.) "HttpResponseCode": der Antwortcode der Anforderung.<br><br> b.) "HttpResponseHeader": die Antwort-HTTP-Header<br><br> c.) "HttpResponseBody": der Antworttext, der für die Anforderung zurückgegeben wurde.<br><br> Wenn ein Netzwerkfehler aufgetreten ist, wird Folgendes zurückgegeben:<br><br> a.) "HttpErrorCode": der Fehlercode<br><br> b.) "HttpErrorMessage": die Fehlermeldung zB. Fehlerhafte URL, keine Verbindung zum Host usw.<br><br>\*@param {string} Error Error if any: Dies schließt den in der KASClient-Dokumentation definierten Standardfehler Code ein. |

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
<a id="readdatafromtmpdirasync"></a>

###  <a name="readdatafromtmpdirasync"></a>readDataFromTmpDirAsync

▸ **readDataFromTmpDirAsync**(filePath: *`string`*, Callback: *`function`*):`void`

Liest Dateiinhalt als Base64 aus dem temporären Cachespeicher. Wird in Verbindung mit API-saveDataInAppCacheAsync für die Dateien verwendet, die mit dieser API gespeichert werden.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.App.readDataFromTmpDirAsync(filePath, function (base64Data, error) {
    if (error == null) {
       // Action's code in success case
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| FilePath | `string` |  Dateipfad, der gelesen werden sollte |
| callback | `function` |  mit den folgenden Parametern: |

**Gibt Folgendes zurück:**`void`

___
<a id="readtalkbackmessage"></a>

###  <a name="readtalkbackmessage"></a>readTalkBackMessage

▸ **readTalkBackMessage**(talkBackMessage: *`string`*):`void`

Liest den Text, wenn der Link für "VoiceOver" aktiviert ist.

**Parameter:**

| Name | Typ |
| ------ | ------ |
| talkBackMessage | `string` |

**Gibt Folgendes zurück:**`void`

___
<a id="registerhardwarebackpresscallback"></a>

###  <a name="registerhardwarebackpresscallback"></a>registerHardwareBackPressCallback

▸ **registerHardwareBackPressCallback**(Callback?: *`function`*):`void`

Registriert einen Rückruf für die Ausführung auf der Hardware-Back-Schaltfläche (für Android)

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`Rückruf | `function` |  null |  auszuführende Methode |

**Gibt Folgendes zurück:**`void`

___
<a id="savedataintmpdirasync"></a>

###  <a name="savedataintmpdirasync"></a>saveDataInTmpDirAsync

▸ **saveDataInTmpDirAsync**(base64Data: *`string`*, filename: *`string`*, Callback: *`function`*):`void`

Speichert Base64-Daten auf dem Gerät mit dem angegebenen Dateinamen. Aktionen können diese API verwenden, um Daten temporär auf dem Gerätespeicher zu speichern, die in der Aktualisierungs Nutzlast von Form/Antwort/Eigenschaften in dieser Sitzung referenziert werden können. Beachten Sie, dass diese Daten im lokalen Temp-Cacheverzeichnis gespeichert werden und von einem Gerätebetriebssystem ohne Warnung in Szenarien mit geringem Speicherplatz gelöscht werden können. Die maximale Lebensdauer dieses Speichers befindet sich innerhalb einer Sitzung der Aktion. Sobald der Bildschirm geschlossen wird, werden diese Daten deaktiviert. Normalerweise kann Action diesen Speicher zum Speichern von Base64-Bild-/-Audiodaten auf dem Speicher verwenden und diesen Pfad in der Umfrage JSON/Response und Client wird sicherstellen, dass es hochgeladen wird, um in den Nachrichten Sende Fluss in Dienst zu finden.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
KASClient.App.saveDataInTmpDirAsync(base64Data, fileName, function (filePath, error) {
    if (error == null) {
       // Action's code in success case
     }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| base64Data | `string` |  Base64-Daten, die gespeichert werden sollen. |
| fileName | `string` |  fileName einschließlich der entsprechenden Erweiterung, die zum Speichern der Daten verwendet werden soll. Dateiname maximal zulässige Länge beträgt 15 und darf nur alphanumerische Zeichen, Unterstriche, hifen und Punkte enthalten, also "a-Za-z0-9\_.-". Beispiel: Datei1. MP3 |
| callback | `function` |  mit den folgenden Parametern: |

**Gibt Folgendes zurück:**`void`

___
<a id="setnativetoolbarproperties"></a>

###  <a name="setnativetoolbarproperties"></a>setNativeToolbarProperties

▸ **setNativeToolbarProperties**(Properties: *[KASNativeToolbarProperties](../classes/kasclient.kasnativetoolbarproperties.md)*):`void`

Legt bei Verwendung der systemeigenen Symbolleiste einige Eigenschaften fest

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

▸ **setUserStrings**(Strings? *`JSON`*:):`void`

**Parameter:**

| Name | Typ | Standardwert |
| ------ | ------ | ------ |
| `Default value`Zeichenfolgen | `JSON` |  null |

**Gibt Folgendes zurück:**`void`

___
<a id="showattachmentpickerasync"></a>

###  <a name="showattachmentpickerasync"></a>showAttachmentPickerAsync

▸ **showAttachmentPickerAsync**(supportedTypes: * [KASAttachmentType](../enums/kasclient.kasattachmenttype.md)[]*, Props *`JSON`*:, Callback *`function`*:):`void`

Zeigt eine Anlagenauswahl auf der systemeigenen Ebene an.

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
| callback | `function` |  mit den folgenden Parametern<br><br>\*@param {KASAttachment\[\]} selectedAttachments-Zeichenfolge ausgewählter Anlagen<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="showbarcodescannerasync"></a>

###  <a name="showbarcodescannerasync"></a>showBarcodeScannerAsync

▸ **showBarcodeScannerAsync**(Callback: *`function`*):`void`

Startet den Barcode Scanner und gibt das überprüfte Objekt zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} barcodeInfo kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="showcontactpickerasync"></a>

###  <a name="showcontactpickerasync"></a>showContactPickerAsync

▸ **showContactPickerAsync**(Title: *`string`*, selectedMutableUser: * `string`[]*, selectedImmutableUser: * `string`[]*, isSingleSelection: *`boolean`*, Callback: *`function`*):`void`

Zeigt eine systemeigene Kontaktauswahl an und gibt ein Array aller Details der ausgewählten Benutzer zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| title | `string` |  der Kontaktauswahl |
| selectedMutableUser | `string`[] |  Array ausgewählter userids |
| selectedImmutableUser | `string`[] |  Array fester ausgewählter userids |
| isSingleSelection | `boolean` |  einzelne Auswahl in der Kontaktauswahl |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASUser\[\]} selectedUsers (Array von Benutzer Details) kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

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

Zeigt eine systemeigene Dauer Auswahl mit Tag/Stunde/Minute

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| defaultDurationInMinutes | `number` |  die Standarddauer, die für die Auswahl angezeigt werden soll. |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Number} durationInMinutes ausgewählte Dauer in Minuten<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="showimageimmersiveview"></a>

###  <a name="showimageimmersiveview"></a>showImageImmersiveView

▸ **showImageImmersiveView**(URLs?: * `string`[]*, currentImageIndex?: *`number`*):`void`

Zeigt das Bild in der immersiven Ansicht an.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var urlArray = ["path1", "path2"];
KASClient.App.showImageImmersiveView(urlArray);
```

**Parameter:**

| Name | Typ | Standardwert | Beschreibung |
| ------ | ------ | ------ | ------ |
| `Default value`URLs | `string`[] |  [] |  Array der Bilder-URL: |
| `Default value`currentImageIndex | `number` | 0 |

**Gibt Folgendes zurück:**`void`

___
<a id="showimagepickerasync"></a>

###  <a name="showimagepickerasync"></a>showImagePickerAsync

▸ **showImagePickerAsync**(Callback: *`function`*):`void`

Zeigt eine systemeigene Bildauswahl und gibt den ausgewählten Bild Pfad zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} selectedImagePath kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:** `void` Ausgewählter Bildspeicherort

___
<a id="showlocationonmap"></a>

###  <a name="showlocationonmap"></a>showLocationOnMap

▸ **showLocationOnMap**(Location: *[KASLocation](../classes/kasclient.kaslocation.md)*):`void`

zeigt einen bestimmten Standort wie in KASLocation erwähnt

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| location | [KASLocation](../classes/kasclient.kaslocation.md) |   |

**Gibt Folgendes zurück:**`void`

___
<a id="shownativeerrormessage"></a>

###  <a name="shownativeerrormessage"></a>showNativeErrorMessage

▸ **showNativeErrorMessage**(Nachricht: *`string`*):`void`

Zeigt eine systemeigene Warnung (für IOS) oder einen Toast (für Android) mit der Nachricht

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| message | `string` |   |

**Gibt Folgendes zurück:**`void`

___
<a id="showplacepickerasync"></a>

###  <a name="showplacepickerasync"></a>showPlacePickerAsync

▸ **showPlacePickerAsync**(Callback: *`function`*):`void`

Zeigt eine systemeigene Ortsauswahl an und gibt die ausgewählte Stelle (lt, LG, n) zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {KASLocation} selectedLocation kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="showprogressbar"></a>

###  <a name="showprogressbar"></a>showProgressBar

▸ **showProgressBar**(Text: *`string`*):`void`

Zeigt eine systemeigene vollständige Sreen-Statusleiste mit dem angegebenen Text an.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| text | `string` |   |

**Gibt Folgendes zurück:**`void`

___
<a id="showqrcodescannerasync"></a>

###  <a name="showqrcodescannerasync"></a>showQRcodeScannerAsync

▸ **showQRcodeScannerAsync**(Callback: *`function`*):`void`

Startet den QR-Code Scanner und gibt das überprüfte Objekt zurück.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {string} qrCodeInfo kann im Falle eines Fehlers NULL sein<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___
<a id="showuserprofileasync"></a>

###  <a name="showuserprofileasync"></a>showUserProfileAsync

▸ **showUserProfileAsync**(UserID: *`string`*, isMiniProfile: *`boolean`*, Callback: *`function`*):`void`

Zeigt die Profilseite/Details eines Benutzers an.

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| userId | `string` |  des Benutzers, dessen Profil angezeigt werden soll |
| isMiniProfile | `boolean` |  ob das Miniprofil zuerst angezeigt werden soll |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} Success true, wenn erfolgreich, andernfalls false<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

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
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} Success<br><br>\*@param {String}-Fehler |

**Gibt Folgendes zurück:**`void`

___
<a id="updateactionlocalcacheasync"></a>

###  <a name="updateactionlocalcacheasync"></a>updateActionLocalCacheAsync

▸ **updateActionLocalCacheAsync**(actionLocalCacheProps: *[KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md)*, Callback: *`function`*):`void`

Aktualisiert/speichert den angegebenen Wert für den Schlüssel in den lokalen Datencache

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| actionLocalCacheProps | [KASActionLocalCacheProp](../classes/kasclient.kasactionlocalcacheprop.md) |  Eigenschaft der Daten, die im Cache gespeichert werden sollen |
| callback | `function` |  Rückruf mit den folgenden para \* \* Metern: @param {Boolean} Success gibt an, ob das Update \* \* erfolgreich war oder nicht @param {string} Error JSON String for the KASError-Objekt mit Fehlercode und/oder Beschreibung. |

**Gibt Folgendes zurück:**`void`

___
<a id="updatetenantuserprofileasync"></a>

###  <a name="updatetenantuserprofileasync"></a>updateTenantUserProfileAsync

▸ **updateTenantUserProfileAsync**(attributeDataList: * [TenantAttributeData](../classes/kasclient.tenantattributedata.md)[]*, Callback: *`function`*):`void`

Aktualisiert die Mandanten Attribute des aktuellen Benutzers. Der Mandant der Unterhaltung im Kontext wird hierfür verwendet.
#### <a name="note"></a>Hinweis

Die Aktion sollte zum gleichen Mandanten der Unterhaltung gehören, und der Benutzer muss bei diesem Mandanten angemeldet sein, damit diese API funktioniert.

#### <a name="sample-usage"></a>Beispiel Verwendung

```
var tenantAttributeDataList = [
    new KASClient.TenantAttributeData("attribute_id_1", "AttributeValue1"),
    new KASClient.TenantAttributeData("attribute_id_2", "AttributeValue2")
];
KASClient.App.updateTenantUserProfileAsync(tenantAttributeDataList, function(success, error) {
    if (error == null && success) {
        console.log("SUCCESS");
    }
});
```

**Parameter:**

| Name | Typ | Beschreibung |
| ------ | ------ | ------ |
| attributeDataList | [TenantAttributeData](../classes/kasclient.tenantattributedata.md) [] |  Mandanten Attribut-ID-Wert-Paare |
| callback | `function` |  mit den folgenden Parametern:<br><br>\*@param {Boolean} Success true, wenn erfolgreich, andernfalls false<br><br>\*@param {string} Fehlermeldung im Falle eines Fehlers, andernfalls NULL |

**Gibt Folgendes zurück:**`void`

___

