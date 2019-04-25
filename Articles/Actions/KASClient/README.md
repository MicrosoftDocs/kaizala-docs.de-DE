## <a name="kas-client"></a>KAS-Client

Das KAS-Client-SDK bietet eine Brücke zwischen der nativen Schnittstelle der Kaizala-app (Objective-C für iOS, Java für Android) und dem JavaScript ihrer Kaizala-Aktion.

Allgemein KASClient APIs sind in zwei Kategorien unterteilt:
1.  **Formular-APIs**: die Unterhaltungs Karte jeder Aktion ist einem Form-Objekt zugeordnet. Ein Formular definiert das Verhalten der Aktion. Um eine Aktionsinstanz zu erstellen, müssen Sie ein Form-Objekt initialisieren, die erforderlichen Informationen darin einfügen und es dann als Anforderung an die jeweilige Unterhaltung übermitteln. Teilnehmer an der Unterhaltung können auf das Formularantworten oder die aggregierte Zusammenfassung aller Antworten anzeigen. Diese APIs wurden für alle Aufgaben im Zusammenhang mit Formularen erstellt. Basierend auf verschiedenen Flows können diese weiter unter kategorisiert werden:
    *   **Erstellungs Fluss-APIs**: beim Tippen auf das Symbol der Aktion in der Palette wird der Erstellungs Fluss gestartet. Mithilfe dieser APIs können Sie ein Form-Objekt initialisieren, es bearbeiten und als Anforderung übermitteln.
    *   **Antwort Fluss-APIs**: beim Tippen auf die Schaltfläche Antworten einer Aktionskarte wird der Antwort Fluss gestartet. Mithilfe dieser APIs können Sie das zugehörige Form-Objekt, alle vorherigen Antworten abrufen und eine neue Antwort übermitteln.
    *   **Zusammenfassungs-Fluss-APIs**: beim Tippen auf die Schaltfläche Zusammenfassung einer Aktionskarte wird der Zusammenfassungs Fluss gestartet. Mithilfe dieser APIs können Sie das zugehörige Form-Objekt, alle aggregierten Antworten der Teilnehmer abrufen und das Formular schließen, sodass keine weiteren Antworten zulässig sind.
    
2.  **App-APIs**: Dies sind APIs, die verwendet werden können, um mit der nativen Schnittstelle des Kaizala-Clients zu interagieren und die erforderlichen Informationen abzurufen. Hierzu gehören generische APIs, wie beispielsweise Kontaktauswahl anzeigen, Bildauswahl, Speicherort des aktuellen Geräts, App-Gebietsschema usw. Diese APIs können in jedem der oben genannten Abläufe verwendet werden.

Sie können die aktuelle KASClient-JavaScript-Datei von [hier](https://manage.kaiza.la/MiniApps/DownloadSDK) herunterladen.

## <a name="api-reference"></a>API-Referenz

*   [Formular Erstellungs Fluss-APIs](generated/modules/kasclient.form.md#creation)
*   [Formular Antwort Fluss-APIs](generated/modules/kasclient.form.md#response)
*   [Fluss-APIs für Formularzusammenfassung](generated/modules/kasclient.form.md#summary)
*   [App-APIs](generated/modules/kasclient.app.md)

## <a name="object-reference"></a>Objektverweis

Verweise aller Objekte im SDK stehen [hier](objects.md)zur Verfügung.
