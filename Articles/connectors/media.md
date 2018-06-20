---
title: /Media
description: Referenzartikel für API zum Senden von Anlagen von Medien zu Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 0b74ce931344407b6e2962f447a0b2c8e721275e
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905348"
---
# <a name="apis-to-query-media-resources"></a>APIs für die Abfrage Media-Ressourcen
## <a name="media"></a>/Media
API-Endpunkt zu Unterhaltungsgruppen innerhalb Kaizala Media Dateianhänge.

Dateiformate werden unterstützt:

| Medientyp | ActionType | Erweiterung |
|---|---|---|
| Bilder | Image | JPG, JPEG, PNG |
| Album | Album | JPG, JPEG, PNG |
| Audiodateien | Audio |MP3, WAV |
| Dokumente | Document | doc-, DOCX-, xls, XLSX, PPT-, PPTX-Format, PDF |
| Videos | Video | MP4, .3gpp |

Dateianhängen Medien zu Kaizala erfolgt in zwei Schritten. Zunächst müssen Sie die Mediendatei in einem Repository mit den Endpunkt /media hochladen und verwenden Sie die Ressource URL höher als Aktion innerhalb der Kaizala für die Bereitstellung.

Entsprechende Inhalte-Type(mime type) muss in der Kopfzeile der Mediendatei festgelegt werden soll. Ohne diese api wird nicht unterstützte Media(415) Fehler ausgelöst. 

### <a name="post-media"></a>POST-/media

    POST {endpoint-url}/v1/media

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Um anzugeben, dass eine Datei hochgeladen wird. Wert: Multipart/Formulardaten |

##### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| POST-Text | files | Media-Datei in einem Format Multipart/Formulardaten hochgeladen werden |

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| mediaResource | String | Codierte Media-Daten in den nachfolgenden Send-Aktion Anrufe verwendet werden |

### <a name="post-groupsgroupidactions"></a>POST-/groups/ {GroupId} / Aktionen

Nachdem Sie die Mediendatei hochgeladen haben, können Sie eine Mediendatei in einer Gruppe veröffentlichen, mithilfe von unten API

    POST {endpoint-url}/v1/groups/{groupId}/actions

##### <a name="request-parameters"></a>Anforderungsparameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad-Parameter | groupId | String | Nein | GUID, die die GroupId der Ressource bestimmte Gruppe darstellt. |
| HTTP-Header | accessToken | String | Nein | Access Token vom Auth Endpunkt |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/Json |

##### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionType | String | ID der Kaizala Aktion senden. Finden Sie in der Tabelle oben unterstützten Dateiformaten und ihren jeweiligen ActionType. |
| actionBody | JSON-Objekt | Ein Objekt, für die entsprechende Aktion erforderliche Daten darstellt. Für jede der unterstützten MediaType nachstehend definierten Parameter. |

###### <a name="actionbody-for-media-files"></a>ActionBody für Media-Dateien

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| mediaResource | String | Nein | MediaResource Zeichenfolge aus einem vorherigen Aufruf von /media, in dem Sie müssen die Anlage hochladen |
| Beschriftung | String | Ja | Text Zeichenfolge, die die Mediendatei als Teil der Nachricht dargestellt mit |


###### <a name="sample-json-request-for-a-media-action"></a>Beispiel für eine Anforderung für eine Aktion Media JSON

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

###### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


