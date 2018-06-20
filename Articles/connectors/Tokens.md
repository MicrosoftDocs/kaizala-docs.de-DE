---
title: Authentifizierungsmethode
description: Artikel zum Abrufen von Access-Token für die Abfrage Kaizala Ressourcen
topic: Article
author: nitinjms
ms.openlocfilehash: e46d5ec6e6af4d125c9aef3dead5bc7a8e7e257c
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905313"
---
# <a name="authentication-mechanism"></a>Authentifizierungsmethode

Bevor Sie beginnen, finden Sie in [Setup für die Verwendung der Kaizala-Connectors](setup.md)

## <a name="authentication-for-kaizala-connectors"></a>Authentifizierung für Kaizala Connectors
 
Wir haben einen benutzerdefinierten token basierend Autorisierungsmechanismus implementiert. Dieser Mechanismus wird das Konzept der Aktualisierung und Zugriffstoken zum Verwalten der Autorisierung für die Kaizala-Plattform-APIs verwendet.
*   Aktualisieren von Token sind die erforderlichen Informationen für ein neues Zugriffstoken abzurufen. Sie müssen an den Sicherheitstokendienst übergeben werden, wenn ein Zugriffstoken läuft ab oder ein Zugriffstoken zum ersten Mal generiert werden muss. Aktualisierungstoken für Kaizala Verbinder haben Ablaufzeit 365 Tage. 

*   Zugriffstoken führen die erforderliche Informationen, um eine Ressource Kaizala zuzugreifen. Eine 3rd Partei Clients muss ein Zugriffstoken an der Plattform Kaizala mit jeder API-Anforderung übergeben. Zugriffstoken für Kaizala Verbinder haben Ablaufzeit von 24 Stunden.


|              | Details           | Gewusst wie: Generieren   | Ablaufzeit    |
| :---: | :---: | :---: | :---: |
| Aktualisieren von Token  | Führen Sie die erforderlichen Informationen für ein neues Zugriffstoken abzurufen.     | Im nächsten Abschnitt unten sind unterschiedliche Möglichkeiten zum Generieren von Aktualisierungstoken dokumentiert. | 365 Tage           |
| Zugangs-Token   | Führen Sie die erforderliche Informationen zum Zugriff auf eine Ressource Kaizala  | Entwickler verwendet aktualisieren Token & andere Connector Details zum Abfragen von Kaizala API-Endpunkt um Access Token zu generieren    | 24 Stunden            |

*   Aktualisierungstoken können ungültig vom Server auf zwei Arten – durch Generieren neuer aktualisieren Token für den gleichen Kaizala Connector oder den entsprechenden Kaizala Connector vollständig gelöscht werden.
## <a name="different-types-of-refresh-tokens"></a>Unterschiedliche Typen von Token aktualisieren

Kaizala Connectors ermöglichen die Optionen zum Generieren von zwei verschiedene Types von Token aktualisieren. Benutzertoken kann entweder über Kaizala-Verwaltungsportal oder oAuth generiert werden.

|              |   Tools zum Generieren von  | Umfang des Zugriffs   | Die generiert werden können | Details |
| :---: | :---: | :---: | :---: | :---: |
| Gruppieren von Token  | Kaizala-Verwaltungsportal     | Ausgewählte Gruppe   | Gruppe/Admin-Mandanten |Dieses Token kann Entwickler Vorgänge ausführen, dass ein Gruppe Admin in dieser Gruppe Berechtigungen für verfügt |
| Benutzertoken   | Kaizala-Verwaltungsportal  | Alle Gruppen, bei denen ein Benutzer Mitglied ist | Jeder Benutzer | Wenn Benutzer Administrator ist, wird dieses Token auf Mandantenebene Access ausgeführt. Für andere kann das Token verwendet werden für den Zugriff von Gruppen gemäß seinen Zugriff auf |
| Benutzertoken   | Verwenden von OAuth 2.0 mithilfe von APIs | Alle Gruppen, bei denen ein Benutzer Mitglied ist | Jeder Benutzer |Bei Verwendung dieses Tokens kann Entwickler Vorgänge in allen Gruppen ausführen.|

*   Im Fall eines WAN-Benutzertoken bietet einzelnes Token Zugriff auf alle Gruppen, die, denen ein Benutzer gehört
*   Für einen einzelnen Connector können Entwickler Token für mehrere Gruppen generieren.

Kaizala bietet zwei weitere Methoden zum Aktualisierungstoken Programmgesteuertes generieren
* Verwenden-API (wird bald hinzufügen)
* Verwenden von OAuth (wird bald hinzufügen)

Nachdem Token Aktualisieren von Group-Administrator oder Benutzer dem Entwickler bereitgestellt wird, sollte es zum Generieren von Access-Token verwendet werden.
## <a name="methods-to-generate-access-token"></a>Methoden zum Generieren von Access-Token

Als Entwickler müssen Sie jetzt ein Connector-ID, geheimen Schlüssel und eine Refresh Token, die an Sie weitergeleitet werden sollen. Mit diesem, können Sie ein Zugriffstoken generieren.

Kaizala bietet zwei-Methode, um das Zugriffstoken generieren
* Verwenden von API
* Verwenden von OAuth

### <a name="generate-access-token-using-api"></a>Generieren Sie Access Token mit-API

Die Stammdomäne für das Aufrufen der Kazaila-APIs ist:

    https://api.kaiza.la/v1/

Sie müssen den folgenden Endpunkt zu verwenden, um ein Zugriffstoken (sowohl zuerst Zeit & höher nach Ablauf das Zugriffstoken) abzurufen:

    GET https://{api_root}/accessToken

##### <a name="request-parameters"></a>Anforderungsparameter

|               | Parameter             | Typ      | Optional?     | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| HTTP-Header   | `applicationId`       | String    | Nein            | ID der Connector zugeordnet  |
| HTTP-Header   | `applicationSecret`   | String    | Nein            | Der Connector zugeordneten geheimen Schlüssel |
| HTTP-Header   | `refreshToken`        | String    | Nein            | Wenn der jeweilige Connector Zugriff auf die Gruppe gewährt wurde durch die Kaizala Gruppe Admin freigegeben refreshToken 

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| `accessToken` | String | Erfolgreich Auth ist ein Token Anwendung zurückgegeben, die zum Beschleunigen des weiteren API-Aufrufe verwendet werden können |
| `endpointUrl` | String | Erfolgreiche Auth ist eine Endpunkt-Url zurückgegeben, für nachfolgende API-Aufrufe, die als api-Basis-Url verwendet werden sollten |
| `accessTokenExpiry` | Long | Es gibt die Ablaufzeit für AccessToken in Epoche time(milliseconds) an. |
| `refreshToken` | String | Nach Abschluss der 328 Tage (90 % der Gültigkeit des Tokens aktualisieren) würden sie die neue RefreshToken zurück, die zum Generieren von AccessToken verwendet werden soll. Andernfalls nach Ablauf die Gültigkeit der aktuellen Aktualisierungstoken würde Connector funktionieren. Der Wert ist Null, bis 90 % der Gültigkeit der aktuellen RefreshToken läuft ab |
| `scope` | String | Festlegen von Berechtigungen, denen mit der Connector bereitgestellt wird |

##### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cm46bWljcm9zb2Z0OmNyZWRlbnRpYWxzIjoie1wicGhvbmVOdW1iZXJcIjpcIis5MTk1NTAwMDAxMTZcIixcImNJZFwiOlwiXCIsXCJ0ZXN0U2VuZGVyXCI6XCJmYWxzZVwiLFwiYXBwTmFtZVwiOlwiY29tLm1pY3Jvc29mdC5tb2JpbGUua2FpemFsYWFwaVwiLFwiYXBwbGljYXRpb25JZFwiOlwiOTExMDY3RTE4QUUCJ2ZXIiOiIyIiwibmJmIjoxNTE0ODgxNjg2LCJleHAiOjE1MTg0ODE2ODYsImlhdCI6MTUxNDg4MTY4NiwiaXNzIjoidXJuOm1pY3Jvc29mdDp3aW5kb3dzLWF6dXJlOnp1bW8iLCJhdWQiOiJ1cm46bWljcm9zb2Z0OndpbmRvd3MtYXp1cmU6enVtbyJ9.fHbIHHTdzoDYT-QIPMu6Oit6x3JMT78LSm50o5cA-N8",
    "endpointUrl": "https://kms-alpha.kaiza.la/",
    "accessTokenExpiry": 1518481686294,
    "refreshToken": "",
    "scope": "token.write"
}
```
### <a name="generate-access-token-using-oauth-20"></a>Generieren Sie Access Token mit oAuth 2.0

#### <a name="steps-to-generate-access-token-using-oauth-20"></a>Schritte zum Generieren von Access Token mit oAuth 2.0
*    **Schritt 1:** Erstellen/Aktualisieren eines Verbinders Kaizala-Verwaltungsportal Einbeziehung umleitungs-url
     *    In der Verbindung, die Sie verwenden, stellen Sie sicher, dass Sie eine Umleitung eingegeben haben Url beim Erstellen der Verbindung. Wenn dies nicht der Fall ist, bitte Update umleitungs-url
     *    Für Testzwecke können Sie die unten Postman Callback-URL, einfach und so erhalten Sie eine Seite mit dem Code. 
        
          `https://www.getpostman.com/oauth2/callback`
 
*    **Schritt 2:** Geben Sie unter Url im Browser, und drücken Sie die EINGABETASTE

          `https://ds.kaiza.la/api/Oauth/Authorize?client_id={{ConnectorID}}&redirect_uri={{re-directURL}}`
      
      *   Stellen Sie sicher, dass Sie 'Client_id' und 'Redirect_uri' richtig eingegeben haben
       ##### <a name="request-parameters"></a>Anforderungsparameter

       |                | Parameter             | Typ      | Optional?     | Beschreibung |
       | :---: | :---: | :---: | :---:  | :--- |
       | URL-parameter  | `client_id`       | String    | Nein            | ID der Connector zugeordnet  |
       | URL-parameter  | `redirect_uri`    | String    | Nein            | Der Connector zugeordneten geheimen Schlüssel |

     *    Beispielsweise wäre Beispiel-url
     
            `https://ds.kaiza.la/api/Oauth/Authorize?client_id=2AB9B82044683484EE9D958E7&redirect_uri=https://www.getpostman.com/oauth2/callback`


*    **Schritt 3:** Melden Sie sich Kaizala und generieren "Code"
     *   Sobald Sie drücken, geben Sie in Schritt2, Sie werden sichergestellt, dass Kaizala-Anmeldeseite
     *   Authentifizieren Sie verwenden Sie die Nummer Ihres registrierte Kaizala
     *   Nach der erfolgreichen Anmeldung werden Sie zu dem Url umgeleitet mit "Code" als Abfragezeichenfolgen-Parameter in der Callback-Url umgeleitet werden
     *   Notieren Sie den zurückgegebenen code 
     
*    **Schritt 4:** Verwenden Sie Code zum Generieren von Access Token
     *   Stellen Sie unter API-Aufruf Access Token generieren
     
         `POST https://ds.kaiza.la/api/oauth/token `
     
     ##### <a name="request-parameters"></a>Anforderungsparameter

       |                | Parameter             | Typ      | Optional?     | Beschreibung |
       | :---: | :---: | :---: | :---:  | :--- |
       | HTTP-Header    | `Content-Type`        | String    | Nein            | Zulässige Wert: Application/X-www-form-urlencoded  |
       | Body-Parameter     | `client_id`       | String    | Nein            | ID der Connector zugeordnet  |
       | Body-Parameter     | `client_secret`   | String    | Nein            | Der Connector zugeordneten geheimen Schlüssel |
       | Body-Parameter     | `code`    | String    | Nein            | Code, der die umgeleitet Url-Abfragezeichenfolgen-Parameter zurückgegeben wurden |
     
Sie erhalten AccessToken, EndpointUrl, AccessToken Ablauf als Teil der Antwort.

##### <a name="response-body"></a>Antworttext

| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| `accessToken` | String | Erfolgreich Auth ist ein Token Anwendung zurückgegeben, die zum Beschleunigen des weiteren API-Aufrufe verwendet werden können |
| `endpointUrl` | String | Erfolgreiche Auth ist eine Endpunkt-Url zurückgegeben, für nachfolgende API-Aufrufe, die als api-Basis-Url verwendet werden sollten |
| `accessTokenExpiry` | Long | Es gibt die Ablaufzeit für AccessToken in Epoche time(milliseconds) an. |
| `refreshToken` | String | Nach Abschluss der 328 Tage (90 % der Gültigkeit des Tokens aktualisieren) würden sie die neue RefreshToken zurück, die zum Generieren von AccessToken verwendet werden soll. Andernfalls nach Ablauf die Gültigkeit der aktuellen Aktualisierungstoken würde Connector funktionieren. Der Wert ist Null, bis 90 % der Gültigkeit der aktuellen RefreshToken läuft ab |
| `scope` | String | Festlegen von Berechtigungen, denen mit der Connector bereitgestellt wird |

##### <a name="sample-json-response"></a>Beispiel von JSON-Antwort

```javascript
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cm46bWljcm9zb2Z0OmNyZWRlbnRpYWxzIjoie1wicGhvbmVOdW1iZXJcIjpcIis5MTk1NTAwMDAxMTZcIixcImNJZFwiOlwiXCIsXCJ0ZXN0U2VuZGVyXCI6XCJmYWxzZVwiLFwiYXBwTmFtZVwiOlwiY29tLm1pY3Jvc29mdC5tb2JpbGUua2FpemFsYWFwaVwiLFwiYXBwbGljYXRpb25JZFwiOlwiOTExMDY3RTE4QUUCJ2ZXIiOiIyIiwibmJmIjoxNTE0ODgxNjg2LCJleHAiOjE1MTg0ODE2ODYsImlhdCI6MTUxNDg4MTY4NiwiaXNzIjoidXJuOm1pY3Jvc29mdDp3aW5kb3dzLWF6dXJlOnp1bW8iLCJhdWQiOiJ1cm46bWljcm9zb2Z0OndpbmRvd3MtYXp1cmU6enVtbyJ9.fHbIHHTdzoDYT-QIPMu6Oit6x3JMT78LSm50o5cA-N8",
    "endpointUrl": "https://kms-alpha.kaiza.la/",
    "accessTokenExpiry": 1518481686294,
    "refreshToken": "",
    "scope": "token.write"
}
```

Weiter: [API-Dokumentation](API.md)
