# <a name="generate-tenant-level-user-token"></a>Benutzertoken auf Mandantenebene generieren

Aktualisierungstoken auf Mandantenebene Benutzer kann verwendet werden, gewähren Zugriff zu Gruppen des Benutzers, in dem Benutzer Administrator ist Für einen Benutzer Mandanten gewährt dieses Token Zugriff auf alle Gruppen für eine Organisation.

## <a name="steps-to-generate-tenant-level-user-token"></a>Schritte zum Generieren von Benutzertoken auf Mandantenebene
*   **Schritt 1: Entwickler registriert einen Connector**

    *   Entwickler navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/
    *   Melden Sie sich mit einem vorhandenen Office365-Konto
    *   Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal
        *   Geben Sie Telefonnummer
        *   Tippen Sie auf "PIN generieren"
        *   Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen
    *   Tippen Sie auf "Connectors" im linken Menü
    *   Tippen Sie auf "Connector hinzufügen"
    *   Registrieren Sie einen Connector für das 3. Partei-System, das die API verwenden
        *   Geben Sie den Namen des Connectors und andere Details. Tippen Sie auf Weiter.
        *   Wählen Sie Berechtigungen, mit denen bestimmt ist für den Zugriff auf den Connector
        *   Tippen Sie auf Connector erstellen
    *   Beachten Sie die ID & geheimen Schlüssel, die generiert abrufen und auf dem Portal angezeigt

*   **Schritt 2: Benutzer Mandanten "gewährt" den Connector Zugriff auf alle Gruppen, denen er Administrator ist**

    *   Benutzer navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/
    *   Melden Sie sich mit einer vorhandenen Office365 Konto (SKU TBD)
    *   Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal
        *   Geben Sie Telefonnummer
        *   Tippen Sie auf "PIN generieren"
        *   Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen
    *   Tippen Sie auf "Connectors" im linken Menü
    *   Tippen Sie auf den Namen des Connectors ein, die vom Connector zugegriffen werden muss
    *   Tippen Sie auf "Benutzertoken generieren"
    *   Beachten Sie die Refresh Token, die generiert dient zum Abrufen und auf dem Portal angezeigt

*   **Schritt 3: Benutzer teilt Token aktualisieren, mit der App-Entwickler**

    *   Admin muss manuell freigeben der Aktualisierungstoken erhalten in Schritt2 mit dem app-Entwickler

*   **Schritt 4: App-Entwickler ruft der Kaizala Plattform Rest-API zum Generieren von Access-Token**

    *   Entwickler kann nun die Aktualisierungstoken verwenden. eine Connector-ID und geheimen Schlüssel Connector aufrufen, die REST-API Bankkontodaten zum Generieren von Access Token (Weitere Informationen weiter unten)

