---
title: Authentifizierungsmechanismus
description: Artikel zum Abrufen von Zugriffstoken zum Abfragen von Kaizala-Ressourcen
topic: Article
author: nitinjms
ms.openlocfilehash: e67686d2aaf92efad27a36246f1444be69e520dd
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535676"
---
# <a name="authentication-mechanism"></a>Authentifizierungsmechanismus

Lesen Sie vor dem ersten Start die Informationen unter [Setup für die Verwendung der Kaizala](setup.md) -Connectors.

## <a name="authentication-for-kaizala-connectors"></a>Authentifizierung für Kaizala-Connectors
 
Wir haben einen benutzerdefinierten Token-basierten Autorisierungsmechanismus implementiert. Dieser Mechanismus verwendet das Konzept der Aktualisierungs-und Zugriffstoken, um die Zugriffsautorisierung für die Kaizala-Platt Form APIs zu verwalten.
*   Aktualisierungstoken tragen die Informationen, die zum Abrufen eines neuen Zugriffstokens erforderlich sind. Sie müssen an den Tokendienst übergeben werden, wenn ein Zugriffstoken abläuft oder wenn ein Zugriffstoken zum ersten Mal generiert werden muss. Aktualisierungstoken für Kaizala-Konnektoren haben eine Ablaufzeit von 365 Tagen. 

*   Zugriffstoken tragen die erforderlichen Informationen für den Zugriff auf eine Kaizala-Ressource. Ein 3rd Party-Client muss ein Zugriffstoken an die Kaizala-Plattform mit jeder API-Anforderung übergeben. Zugriffstoken für Kaizala-Connectors weisen eine Ablaufzeit von 24 Stunden auf.


|              | Details           | Vorgehensweise generieren   | Ablaufzeit    |
| :---: | :---: | :---: | :---: |
| Aktualisierungs Token  | Übertragen der erforderlichen Informationen zum Abrufen eines neuen Zugriffstokens     | Im nächsten Abschnitt werden verschiedene Methoden zum Generieren eines Aktualisierungs Tokens dokumentiert. | 365 Tage           |
| Zugangs-Token   | Übertragen der erforderlichen Informationen für den Zugriff auf eine Kaizala-Ressource  | Entwickler verwendet Aktualisierungstoken #a0 andere Connector Details zum Abfragen des Kaizala-API-Endpunkts zum Generieren des Zugriffstokens    | 24 Stunden            |

*   Aktualisierungstoken können vom Server auf zwei Arten für ungültig erklärt werden, indem neue Aktualisierungstoken für denselben Kaizala-Konnektor generiert oder der entsprechende Kaizala-Connector ganz gelöscht wird.
## <a name="different-types-of-refresh-tokens"></a>Verschiedene Typen von Aktualisierungstoken

Kaizala-Konnektoren ermöglichen es Optionen, zwei verschiedene Typen von Aktualisierungs Token zu generieren. Das Benutzertoken kann entweder über das Kaizala-Verwaltungs Portal oder über oAuth generiert werden.

|              |   Zu generierende Tools  | Umfang des Zugriffs   | Wer kann generieren | Details |
| :---: | :---: | :---: | :---: | :---: |
| Gruppen Token  | Kaizala-Verwaltungs Portal     | Ausgewählte Gruppe   | Gruppe/mandantenadministrator |Mithilfe dieses Tokens kann Entwickler Vorgänge ausführen, für die ein Gruppenadministrator Berechtigungen für diese Gruppe besitzt. |
| Benutzer Token   | Kaizala-Verwaltungs Portal  | Alle Gruppen, denen ein Benutzer angehört | Jeder Benutzer | Wenn der Benutzer mandantenadministrator ist, führt dieses Token Zugriff auf Mandantenebene. Für andere kann das Token für den Zugriff auf Gruppen gemäß seinem/ihrem Zugriff verwendet werden. |
| Benutzer Token   | Verwenden von OAuth 2,0 mithilfe von APIs | Alle Gruppen, denen ein Benutzer angehört | Jeder Benutzer |Mithilfe dieses Tokens kann Entwickler Vorgänge in allen Gruppen durchführen.|

*   Bei Benutzertoken bietet ein einzelnes Token Zugriff auf alle Gruppen, zu denen ein Benutzer gehört.
*   Für einen einzelnen Connector können Entwickler Token für mehrere Gruppen generieren.

Kaizala stellt zwei weitere Methoden zum Generieren von Aktualisierungstoken bereit Programmgesteuertes
* Verwenden von API (wird bald hinzugefügt)
* Verwenden von OAuth (wird bald hinzugefügt)

Sobald das Aktualisierungstoken von einem Gruppenadministrator oder Benutzer dem Entwickler zur Verfügung gestellt wurde, sollte es zum Generieren des Zugriffstokens verwendet werden.
## <a name="methods-to-generate-access-token"></a>Methoden zum Generieren des Zugriffstokens

Als Entwickler verfügen Sie nun über eine Connector-ID, einen geheimen Schlüssel und ein Aktualisierungs Token, das an Sie übergeben werden sollte. Mit dieser können Sie ein Zugriffstoken generieren.

Kaizala bietet zwei Methoden zum Generieren von Zugriffstoken
* Verwenden der API
* Verwenden von OAuth

### <a name="generate-access-token-using-api"></a>Generieren eines Zugriffstokens mithilfe von API

Die Stammdomäne zum Aufrufen der Kaizala-APIs lautet:

    https://api.kaiza.la/v1/

Sie müssen den folgenden Endpunkt verwenden, um ein Zugriffstoken abzurufen (beim Ablaufen des Zugriffstokens zum ersten Mal #a0):

    GET https://{api_root}/accessToken

##### <a name="request-parameters"></a>Anforderungsparameter

|               | Parameter             | Typ      | Optional?     | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header   | `applicationId`       | String    | Nein            | Dem Connector zugeordnete ID  |
| HTTP-Header   | `applicationSecret`   | String    | Nein            | Dem Connector zugeordnete geheime Schlüssel |
| HTTP-Header   | `refreshToken`        | String    | Nein            | vom Kaizala-Gruppenadministrator freigegebene refreshToken, wenn dem jeweiligen Connector Zugriff auf die Gruppe gewährt wurde 

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| `accessToken` | String | Bei erfolgreicher Authentifizierung wird ein Anwendungs Token zurückgegeben, das zum Erstellen von nachfolgenden API-Aufrufen verwendet werden kann. |
| `endpointUrl` | String | Bei erfolgreicher Authentifizierung wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte. |
| `accessTokenExpiry` | Long | Es gibt die Ablaufzeit für Access Token in Epoch time (Millisekunden) |
| `refreshToken` | String | Nach Abschluss von 328 Tagen (90% der Gültigkeit des Aktualisierungs Tokens) würde die neue refreshToken zurückgegeben werden, die zum Generieren von Access Token verwendet werden soll. Andernfalls würde Connector nach Ablauf der Gültigkeit des aktuellen Aktualisierungs Tokens nicht mehr funktionieren. Der Wert ist NULL, bis 90% der Gültigkeit des aktuellen refreshToken abgelaufen sind. |
| `scope` | String | Gruppe von Berechtigungen, mit denen der Connector bereitgestellt wird |

##### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cm46bWljcm9zb2Z0OmNyZWRlbnRpYWxzIjoie1wicGhvbmVOdW1iZXJcIjpcIis5MTk1NTAwMDAxMTZcIixcImNJZFwiOlwiXCIsXCJ0ZXN0U2VuZGVyXCI6XCJmYWxzZVwiLFwiYXBwTmFtZVwiOlwiY29tLm1pY3Jvc29mdC5tb2JpbGUua2FpemFsYWFwaVwiLFwiYXBwbGljYXRpb25JZFwiOlwiOTExMDY3RTE4QUUCJ2ZXIiOiIyIiwibmJmIjoxNTE0ODgxNjg2LCJleHAiOjE1MTg0ODE2ODYsImlhdCI6MTUxNDg4MTY4NiwiaXNzIjoidXJuOm1pY3Jvc29mdDp3aW5kb3dzLWF6dXJlOnp1bW8iLCJhdWQiOiJ1cm46bWljcm9zb2Z0OndpbmRvd3MtYXp1cmU6enVtbyJ9.fHbIHHTdzoDYT-QIPMu6Oit6x3JMT78LSm50o5cA-N8",
    "endpointUrl": "https://kms-alpha.kaiza.la/",
    "accessTokenExpiry": 1518481686294,
    "refreshToken": "",
    "scope": "token.write"
}
```
### <a name="generate-access-token-using-oauth-20"></a>Generieren eines Zugriffstokens mit oAuth 2,0

#### <a name="steps-to-generate-access-token-using-oauth-20"></a>Schritte zum Generieren des Zugriffstokens mit oAuth 2,0
*    **Schritt 1:** Erstellen/Aktualisieren eines Connectors im Kaizala-Verwaltungs Portal zum Einschließen der Umleitungs-URL
     *    Stellen Sie sicher, dass Sie in dem von Ihnen verwendeten Connector eine Umleitungs-URL beim Erstellen des Connectors eingegeben haben. Wenn nicht, aktualisieren Sie die Umleitungs-URL
     *    Zu Testzwecken können Sie die unten gezeigte Poster Callback-URL verwenden, die Ihnen lediglich eine Seite mit dem Code zur Verfügung stellt. 
        
          `https://www.getpostman.com/oauth2/callback`
 
*    **Schritt 2:** Geben Sie unter URL im Browser ein, und drücken Sie die EINGABETASTE.

          `https://ds.kaiza.la/api/Oauth/Authorize?client_id={{ConnectorID}}&redirect_uri={{re-directURL}}`
      
      *   Stellen Sie sicher, dass Sie "client_id" #a0 "redirect_uri" korrekt eingegeben haben.
       ##### <a name="request-parameters"></a>Anforderungsparameter

       |                | Parameter             | Typ      | Optional?     | Beschreibung |
       | :---: | :---: | :---: | :---:  | :--- |
       | URL-Parameter  | `client_id`       | String    | Nein            | Dem Connector zugeordnete ID  |
       | URL-Parameter  | `redirect_uri`    | String    | Nein            | Dem Connector zugeordnete geheime Schlüssel |

     *    Beispiel-URL wäre beispielsweise
     
            `https://ds.kaiza.la/api/Oauth/Authorize?client_id=2AB9B82044683484EE9D958E7&redirect_uri=https://www.getpostman.com/oauth2/callback`


*    **Schritt 3:** Anmeldung bei Kaizala und Generieren von "Code"
     *   Sobald Sie in Schritt 2 die EINGABETASTE drücken, müssen Sie zur Kaizala-Anmeldeseite weitergeleitet werden.
     *   Authentifizieren Sie sich mit Ihrer registrierten Kaizala-Nummer
     *   Nachdem Sie sich erfolgreich angemeldet haben, werden Sie erneut an die URL mit dem Namen "Code" als Abfrageparameter in der Rückruf-URL umgeleitet.
     *   Notieren Sie den zurückgegebenen "Code" 
     
*    **Schritt 4:** Verwenden von Code zum Generieren von Zugriffs Token
     *   Erstellen eines Zugriffstokens unter API-Aufruf
     
         `POST https://ds.kaiza.la/api/oauth/token `
     
     ##### <a name="request-parameters"></a>Anforderungsparameter

       |                | Parameter             | Typ      | Optional?     | Beschreibung |
       | :---: | :---: | :---: | :---:  | :--- |
       | HTTP-Header    | `Content-Type`        | String    | Nein            | Zulässiger Wert: Application/x-www-form-urlencoded  |
       | Body-Parameter     | `client_id`       | String    | Nein            | Dem Connector zugeordnete ID  |
       | Body-Parameter     | `client_secret`   | String    | Nein            | Dem Connector zugeordnete geheime Schlüssel |
       | Body-Parameter     | `code`    | String    | Nein            | Code, der im Abfrageparameter der Umleitungs-URL zurückgegeben wurde |
     
Sie erhalten Access Token, endpointUrl, Access Token Ablaufdatum als Teil der Antwort.

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| `accessToken` | String | Bei erfolgreicher Authentifizierung wird ein Anwendungs Token zurückgegeben, das zum Erstellen von nachfolgenden API-Aufrufen verwendet werden kann. |
| `endpointUrl` | String | Bei erfolgreicher Authentifizierung wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte. |
| `accessTokenExpiry` | Long | Es gibt die Ablaufzeit für Access Token in Epoch time (Millisekunden) |
| `refreshToken` | String | Nach Abschluss von 328 Tagen (90% der Gültigkeit des Aktualisierungs Tokens) würde die neue refreshToken zurückgegeben werden, die zum Generieren von Access Token verwendet werden soll. Andernfalls würde Connector nach Ablauf der Gültigkeit des aktuellen Aktualisierungs Tokens nicht mehr funktionieren. Der Wert ist NULL, bis 90% der Gültigkeit des aktuellen refreshToken abgelaufen sind. |
| `scope` | String | Gruppe von Berechtigungen, mit denen der Connector bereitgestellt wird |

##### <a name="sample-json-response"></a>JSON-Beispielantwort

```javascript
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cm46bWljcm9zb2Z0OmNyZWRlbnRpYWxzIjoie1wicGhvbmVOdW1iZXJcIjpcIis5MTk1NTAwMDAxMTZcIixcImNJZFwiOlwiXCIsXCJ0ZXN0U2VuZGVyXCI6XCJmYWxzZVwiLFwiYXBwTmFtZVwiOlwiY29tLm1pY3Jvc29mdC5tb2JpbGUua2FpemFsYWFwaVwiLFwiYXBwbGljYXRpb25JZFwiOlwiOTExMDY3RTE4QUUCJ2ZXIiOiIyIiwibmJmIjoxNTE0ODgxNjg2LCJleHAiOjE1MTg0ODE2ODYsImlhdCI6MTUxNDg4MTY4NiwiaXNzIjoidXJuOm1pY3Jvc29mdDp3aW5kb3dzLWF6dXJlOnp1bW8iLCJhdWQiOiJ1cm46bWljcm9zb2Z0OndpbmRvd3MtYXp1cmU6enVtbyJ9.fHbIHHTdzoDYT-QIPMu6Oit6x3JMT78LSm50o5cA-N8",
    "endpointUrl": "https://kms-alpha.kaiza.la/",
    "accessTokenExpiry": 1518481686294,
    "refreshToken": "",
    "scope": "token.write"
}
```

Weiter: [API Documentation](API.md)
