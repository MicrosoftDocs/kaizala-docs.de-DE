---
title: /Media
description: Referenzartikel zur API zum Senden von Medien Anlagen an Gruppen
topic: Reference
author: nitinjms
ms.openlocfilehash: 3cf1e6b235d6bf324011f0b054408eb418eb0871
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190694"
---
# <a name="media"></a>/Media
API-Endpunkt zum Senden von Medien Anlagen an unterhaltungsgruppen innerhalb von Kaizala.

Unterstützte Dateiformate sind:

| Medientyp | ActionType | Erweiterung |
|---|---|---|
| Bilder | Image | . jpg,. JPEG,. png |
| Album | Album | . jpg,. JPEG,. png |
| AudioDateien | Audio |. MP3,. wav |
| Dokumente | Dokument | . doc,. docx,. xls,. xlsx,. ppt,. pptx,. PDF |
| Videos | Video | . MP4,. 3GPP |

Das Veröffentlichen von Medien Anlagen an Kaizala erfolgt in zwei Schritten. Zunächst müssen Sie die Mediendatei mithilfe des/Media-Endpunkts in ein Repository hochladen und dann später die Ressourcen-URL als Aktion innerhalb von Kaizala bereitstellen.

Der entsprechende Inhaltstyp (MIME-Typ) muss in der Inhalts Kopfzeile der Mediendatei festgelegt werden. Ohne diese API werden nicht unterstützte Medien (415) Fehler ausgelöst. 

## <a name="post-media"></a>POST/Media

    POST {endpoint-url}/v1/media

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | , Um anzugeben, dass eine Datei hochgeladen wird. Wert: Multipart/Form-Data |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| POST-Textkörper | files | Mediendatei, die in einem mehrteiligen/Formular-Datenformat hochgeladen werden soll |

### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| mediaResource | String | Codierte Mediendaten, die bei nachfolgenden Sende Aktionsaufrufen verwendet werden sollen |

## <a name="post-groupsgroupidactions"></a>POST/groups/{groupId}/actions

Nachdem Sie die Mediendatei hochgeladen haben, können Sie mithilfe der folgenden API eine Mediendatei in einer Gruppe veröffentlichen.

    POST {endpoint-url}/v1/groups/{groupId}/actions

### <a name="request-parameters"></a>AnforderungsParameter

|  | Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| URL-Pfad Parameter | groupId | String | Nein | GUID, die die Gruppen-ID der bestimmten Gruppenressource darstellt |
| HTTP-Header | accessToken | String | Nein | Vom Endpunkt auth empfangenes Zugriffs Token |
| HTTP-Header | Content-Type | String | Nein | Wert: Application/JSON |

### <a name="request-body"></a>Anforderungstext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionType | String | ID der zu sendenden Kaizala-Aktion. Unterstützte Dateiformate und deren jeweiliger Action Type finden Sie in der obigen Tabelle. |
| actionBody | JSON-Objekt | Objekt, das die für die jeweilige Aktion erforderlichen Daten darstellt. Die unten definierten Parameter für jeden der unterstützten MediaType. |

#### <a name="actionbody-for-media-files"></a>actionBody für Mediendateien

| Parameter | Typ | Optional? | Beschreibung |
| :---: | :---: | :---: | :--- |
| mediaResource | String | Nein | MediaResource-Zeichenfolge aus einem vorherigen Aufruf an/Media, in dem Sie die Anlage hochladen müssen |
| Beschriftung | String | Ja | Text Zeichenfolge, die alongwith der Mediendatei als Teil der Nachricht angezeigt wird |


#### <a name="sample-json-request-for-a-media-action"></a>JSON-Beispielanforderung für eine Medienaktion

```javascript
{
    actionType:"Image",
    actionBody: {
                mediaResource: "{{MediaResource return in response of /media api call}}",
                caption: "Sample test caption"
                }
}

```

#### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "referenceId": "6007fe3a-cb7c-4eef-bb88-934273aabc1e"
}
```


