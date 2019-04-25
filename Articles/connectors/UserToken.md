# <a name="generate-tenant-level-user-token"></a>Generieren eines Benutzertokens auf Mandantenebene

Ein Benutzer Aktualisierungstoken auf Mandantenebene kann verwendet werden, um Zugriff auf alle Gruppen des Benutzers zu gewähren, in denen der Benutzer ein Administrator ist. Für einen Mandanten Benutzer gewährt dieses Token Zugriff auf alle Gruppen für eine Organisation.

## <a name="steps-to-generate-tenant-level-user-token"></a>Schritte zum Generieren des Benutzertokens auf Mandantenebene
*   **Schritt 1: Registrieren eines Connectors für Entwickler**

    *   Entwickler navigiert zu Kaizala Management Portal @https://manage.kaiza.la/
    *   Anmelden mit einem vorhandenen Office365-Konto
    *   Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.
        *   Telefonnummer eingeben
        *   Tippen Sie auf "PIN generieren".
        *   ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer
    *   Tippen Sie im linken Menü auf "Connectors".
    *   Tippen Sie auf "Connector hinzufügen".
    *   Registrieren eines Connectors für das Drittanbietersystem, das die API verwendet
        *   Geben Sie den Namen des Connectors und weitere Details ein. Tippen Sie auf weiter
        *   Wählen Sie Berechtigungen aus, die für den Connector vorgesehen sind, um Zugriff auf
        *   Tippen Sie auf Verbinder erstellen.
    *   Beachten Sie die ID & Secret, die generiert und im Portal angezeigt werden.

*   **Schritt 2: Mandanten Benutzer "erteilt" den Connector-Zugriff auf alle Gruppen, für die er Administrator ist**

    *   Benutzer navigiert zu Kaizala Management Portal @https://manage.kaiza.la/
    *   Anmelden mit einem vorhandenen Office365-Konto (SKU-festgelegt)
    *   Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.
        *   Telefonnummer eingeben
        *   Tippen Sie auf "PIN generieren".
        *   ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer
    *   Tippen Sie im linken Menü auf "Connectors".
    *   Tippen Sie auf den Namen des Connectors, auf den der Connector zugreifen muss.
    *   Tippen Sie auf "Benutzertoken generieren".
    *   Hinweis das Aktualisierungs Token, das generiert und im Portal angezeigt wird

*   **Schritt 3: Benutzer Freigabe des Aktualisierungs Tokens mit dem App-Entwickler**

    *   Der Administrator muss das in Schritt 2 erhaltene Aktualisierungstoken manuell mit dem App-Entwickler freigeben.

*   **Schritt 4: App-Entwickler Ruft die Kaizala-Plattform-Rest-API zum Generieren von Zugriffs Token**

    *   Entwickler können nun das Aktualisierungstoken verwenden. eine Connector-ID und ein Connector Secret, um die REST-API aufzurufen, um Zugriffs Token zu generieren (Weitere Informationen finden Sie weiter unten)

