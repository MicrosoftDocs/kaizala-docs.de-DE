---
title: AuthentifizierungsMechanismus
description: Artikel zum Abrufen von Zugriffstoken zum Abfragen von Kaizala-Ressourcen
topic: Article
author: nitinjms
ms.openlocfilehash: e46d5ec6e6af4d125c9aef3dead5bc7a8e7e257c
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190808"
---
# <a name="authentication-mechanism"></a>AuthentifizierungsMechanismus

Bevor Sie beginnen, lesen Sie [Setup für die Verwendung der Kaizala](setup.md) -Connectors

## <a name="authentication-for-kaizala-connectors"></a>Authentifizierung für Kaizala-Connectors
 
Wir haben einen benutzerdefinierten Token-basierten Autorisierungsmechanismus implementiert. Dieser Mechanismus verwendet das Konzept der Aktualisierungs-und Zugriffstoken, um die Zugriffsautorisierung für die Kaizala-Platt Form-APIs zu verwalten.
*   Aktualisierungstoken enthalten die erforderlichen Informationen, um ein neues Zugriffstoken zu erhalten. Sie müssen an den Tokendienst übergeben werden, wenn ein Zugriffstoken abläuft oder wenn zum ersten Mal ein Zugriffstoken generiert werden muss. Aktualisierungstoken für Kaizala-Connectors weisen eine Ablaufzeit von 365 Tagen auf. 

*   Zugriffstoken tragen die erforderlichen Informationen für den Zugriff auf eine Kaizala-Ressource. Ein Drittanbieter-Client muss mit jeder API-Anforderung ein Zugriffstoken an die Kaizala-Plattform weiterleiten. Zugriffstoken für Kaizala-Connectors haben eine Ablaufzeit von 24 Stunden.


|              | Details           | So generieren Sie   | Ablaufzeit    |
| :---: | :---: | :---: | :---: |
| Aktualisierungs Token  | Übertragen der erforderlichen Informationen zum Abrufen eines neuen Zugriffstokens     | Unterschiedliche Methoden zum Generieren des Aktualisierungs Tokens werden im nächsten Abschnitt beschrieben. | 365 Tage           |
| Zugangs-Token   | Übertragen der erforderlichen Informationen für den Zugriff auf eine Kaizala-Ressource  | Der Entwickler verwendet das Aktualisierungstoken & anderen Connector Details zum Abfragen des Kaizala-API-Endpunkts, um Zugriffstoken zu generieren.    | 24 Stunden            |

*   Aktualisierungstoken können vom Server auf zweierlei Weise für ungültig erklärt werden: durch Generieren neuer Aktualisierungstoken für den gleichen Kaizala-Konnektor oder durch Löschen des entsprechenden Kaizala-Konnektors.
## <a name="different-types-of-refresh-tokens"></a>Verschiedene Typen von Aktualisierungstoken

Kaizala-Connectors ermöglichen es, zwei verschiedene Typen von Aktualisierungs Token zu generieren. Benutzertoken können entweder über Kaizala-Verwaltungs Portal oder oAuth generiert werden.

|              |   Zu generierende Tools  | Zugriffsbereich   | Wer generieren kann | Details |
| :---: | :---: | :---: | :---: | :---: |
| Gruppen Token  | Kaizala-Verwaltungs Portal     | Ausgewählte Gruppe   | Gruppen-/MandantenAdministrator |Mithilfe dieses Tokens können Entwickler Vorgänge ausführen, für die ein Gruppenadministrator über Berechtigungen in dieser Gruppe verfügt. |
| Benutzer Token   | Kaizala-Verwaltungs Portal  | Alle Gruppen, bei denen ein Benutzer Mitglied ist | Beliebiger Benutzer | Wenn der Benutzer MandantenAdministrator ist, hat dieses Token Zugriff auf Mandantenebene. Für andere Benutzer kann das Token für den Zugriff auf Gruppen gemäß seinem Zugriff verwendet werden. |
| Benutzer Token   | Verwenden von OAuth 2,0, verwenden von APIs | Alle Gruppen, bei denen ein Benutzer Mitglied ist | Beliebiger Benutzer |Mithilfe dieses Tokens können Entwickler Vorgänge für alle Gruppen ausführen.|

*   Im Fall von Benutzertoken ermöglicht ein einzelnes Token den Zugriff auf alle Gruppen, zu denen ein Benutzer gehört
*   Für einen einzelnen Connector können Entwickler Token für mehrere Gruppen generieren.

Kaizala bietet zwei weitere Methoden zum Generieren von Aktualisierungstoken programatically
* Using API (wird bald hinzugefügt)
* Verwenden von OAuth (wird bald hinzugefügt)

Sobald das Aktualisierungstoken entweder vom Gruppenadministrator oder vom Benutzer für den Entwickler bereitgestellt wird, sollte es zum Generieren des Zugriffstokens verwendet werden.
## <a name="methods-to-generate-access-token"></a>Methoden zum Generieren von Zugriffs Token

Als Entwickler haben Sie jetzt eine Connector-ID, einen geHeimen Schlüssel und ein Aktualisierungs Token, die an Sie weitergeleitet werden sollen. Mithilfe dieses können Sie ein Zugriffstoken generieren.

Kaizala bietet zwei Methoden zum Generieren von Zugriffstoken
* Verwenden der API
* Verwenden von OAuth

### <a name="generate-access-token-using-api"></a>Generieren eines Zugriffstokens mithilfe der API

Die Stammdomäne zum Aufrufen der Kazaila-APIs lautet:

    https://api.kaiza.la/v1/

Sie müssen den folgenden Endpunkt verwenden, um ein Zugriffstoken zu erhalten (sowohl beim ersten & später, wenn das Zugriffstoken abläuft):

    GET https://{api_root}/accessToken

##### <a name="request-parameters"></a>AnforderungsParameter

|               | Parameter             | Typ      | Optional?     | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header   | `applicationId`       | String    | Nein            | Der Verbindung zugeordnete ID  |
| HTTP-Header   | `applicationSecret`   | String    | Nein            | Dem Verbinder zugeordneter Schlüssel |
| HTTP-Header   | `refreshToken`        | String    | Nein            | refreshToken, die vom Kaizala-Gruppenadministrator freigegeben wurden, wenn dem jeweiligen Connector der Zugriff auf die Gruppe gewährt wurde 

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| `accessToken` | String | Bei erfolgreicher Authentifizierung wird ein Anwendungs Token zurückgegeben, das für nachfolgende API-Aufrufe verwendet werden kann. |
| `endpointUrl` | String | Bei erfolgreicher Authentifizierung wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte. |
| `accessTokenExpiry` | Long | Es gibt die Ablaufzeit für Access Token in Epoch time (Millisekunden) an. |
| `refreshToken` | String | Nach Abschluss von 328 Tagen (90% der Gültigkeit des Aktualisierungs Tokens) würde die neue refreshToken zurückgegeben, die zum Generieren von Access Token verwendet werden soll. Andernfalls würde Connector nicht mehr funktionieren, nachdem die Gültigkeit des aktuellen Aktualisierungs Tokens abgelaufen ist. Der Wert ist NULL, bis 90% der Gültigkeit des aktuellen refreshToken abgelaufen ist. |
| `scope` | String | Berechtigungssatz, mit dem der Connector bereitgestellt wird |

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

#### <a name="steps-to-generate-access-token-using-oauth-20"></a>Schritte zum Generieren eines Zugriffstokens mit oAuth 2,0
*    **Schritt 1:** Erstellen/Aktualisieren eines Connectors im Kaizala-Verwaltungs Portal mit Umleitungs-URL
     *    Stellen Sie sicher, dass Sie im Connector, den Sie verwenden, beim Erstellen des Connectors eine Umleitungs-URL eingegeben haben. Falls nicht, aktualisieren Sie die Umleitungs-URL
     *    Zu Testzwecken können Sie die below Postman-Rückruf-URL verwenden, die Ihnen nur eine Seite mit dem Code gibt. 
        
          `https://www.getpostman.com/oauth2/callback`
 
*    **Schritt 2:** Geben Sie unter URL im Browser ein, und drücken Sie die EINGABETASTE.

          `https://ds.kaiza.la/api/Oauth/Authorize?client_id={{ConnectorID}}&redirect_uri={{re-directURL}}`
      
      *   Stellen Sie sicher, dass Sie ' client_id ' & ' redirect_uri ' richtig eingegeben haben.
       ##### <a name="request-parameters"></a>AnforderungsParameter

       |                | Parameter             | Typ      | Optional?     | Beschreibung |
       | :---: | :---: | :---: | :---:  | :--- |
       | URL-Parameter  | `client_id`       | String    | Nein            | Der Verbindung zugeordnete ID  |
       | URL-Parameter  | `redirect_uri`    | String    | Nein            | Dem Verbinder zugeordneter Schlüssel |

     *    Beispiel-URL wäre beispielsweise
     
            `https://ds.kaiza.la/api/Oauth/Authorize?client_id=2AB9B82044683484EE9D958E7&redirect_uri=https://www.getpostman.com/oauth2/callback`


*    **Schritt 3:** Melden Sie sich bei Kaizala an, und generieren Sie "Code"
     *   Sobald Sie in Schritt 2 die EINGABETASTE drücken, werden Sie zur Kaizala-Anmeldeseite weitergeleitet.
     *   Authentifizieren Sie sich mit Ihrer registrierten Kaizala-Nummer
     *   Nachdem Sie sich erfolgreich angemeldet haben, werden Sie an die Re-Direct-URL mit "Code" als Abfrageparameter in der Rückruf-URL umgeleitet.
     *   NoTieren Sie sich den zurückgegebenen "Code" 
     
*    **Schritt 4:** Verwenden von Code zum Generieren eines Zugriffstokens
     *   Make below API-Aufruf zum Generieren von Zugriffs Token
     
         `POST https://ds.kaiza.la/api/oauth/token `
     
     ##### <a name="request-parameters"></a>AnforderungsParameter

       |                | Parameter             | Typ      | Optional?     | Beschreibung |
       | :---: | :---: | :---: | :---:  | :--- |
       | HTTP-Header    | `Content-Type`        | String    | Nein            | Zulässiger Wert: Application/x-www-form-urlencoded  |
       | Body-Parameter     | `client_id`       | String    | Nein            | Der Verbindung zugeordnete ID  |
       | Body-Parameter     | `client_secret`   | String    | Nein            | Dem Verbinder zugeordneter Schlüssel |
       | Body-Parameter     | `code`    | String    | Nein            | Code, der im Abfrageparameter der Umleitungs-URL zurückgegeben wurde |
     
Sie erhalten Access Token, endpointUrl, Access Token Ablaufdatum als Teil der Antwort.

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| `accessToken` | String | Bei erfolgreicher Authentifizierung wird ein Anwendungs Token zurückgegeben, das für nachfolgende API-Aufrufe verwendet werden kann. |
| `endpointUrl` | String | Bei erfolgreicher Authentifizierung wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte. |
| `accessTokenExpiry` | Long | Es gibt die Ablaufzeit für Access Token in Epoch time (Millisekunden) an. |
| `refreshToken` | String | Nach Abschluss von 328 Tagen (90% der Gültigkeit des Aktualisierungs Tokens) würde die neue refreshToken zurückgegeben, die zum Generieren von Access Token verwendet werden soll. Andernfalls würde Connector nicht mehr funktionieren, nachdem die Gültigkeit des aktuellen Aktualisierungs Tokens abgelaufen ist. Der Wert ist NULL, bis 90% der Gültigkeit des aktuellen refreshToken abgelaufen ist. |
| `scope` | String | Berechtigungssatz, mit dem der Connector bereitgestellt wird |

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
