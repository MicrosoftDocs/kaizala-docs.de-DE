# <a name="anatomy-of-a-kaizala-action-package"></a>Anatomie eines Kaizala-Aktionspakets

Ein Kaizala-Aktionspaket ist eine reguläre ZIP-Datei, die nicht kennwortgeschützt ist und eine maximale Größe von 1MB hat. Die Ressourcen im Paket befinden sich im Stamm der ZIP-Datei und nicht in einer Verzeichnisstruktur. Die Ressourcen können auch nicht auf externe Ressourcen verweisen, die nicht im Paket enthalten sind.

Die grundlegenden Komponenten eines Kaizala-Aktionspakets sind 
*   Eine Manifestdatei im JSON-Format
*   Ein App-Modell für Ihre Kaizala-Aktion im JSON-Format
*   Webressourcen, die ihre Kaizala-Aktion darstellen-HTML-, JS-, CSS-und Bilddateien

## <a name="package-manifest"></a>Paket Manifest

Das Manifest gibt die Einstellungen der Kaizala-Aktion an, wie beispielsweise die folgenden:
*   Der Anzeigename, die Beschreibung, die ID, die Version und das Aktionssymbol der Aktion.
*   Verschiedene Ansichten, die ihre Aktion definieren und ihre jeweiligen Aufruf gibt zurück-Punkte zuordnen
    * Eine Erstellungsansicht, wenn eine Aktion aus der Palette aufgerufen wird
    * Eine Kartenansicht, die im Chatbereich angezeigt wird, wenn eine Instanz der Aktion gesendet wird
    * Eine responderansicht für Benutzer zur Reaktion auf die Kaizala-Aktion
    * Eine Zusammenfassungsansicht zum Anzeigen von aggregierten Antworten
*   Bezeichnungen, die in den systemeigenen Ansichten verwendet werden, die Ihre benutzerdefinierten Ansichten Kapseln

Weitere Informationen finden Sie unter [Paket Manifest-Schema im JSON-Format](package_manifest_schema.md).

## <a name="app-model"></a>App-Modell

Das App-Modell gibt die Funktionen der Kaizala-Aktion an, einschließlich:
*   Das Datenmodell für das Form-Objekt, das verwendet werden soll, um die Kaizala-Aggregations Dienste zu nutzen
*   Eigenschaften für das Form-Objekt
*   Dem Form-Objekt zugeordnete Einstellungen

Weitere Informationen finden Sie unter [App-Modell Schema im JSON-Format](appModel_schema.md).

## <a name="web-resources"></a>WebRessourcen

Wie oben erwähnt, muss das Kaizala-Paket alle Ressourcen enthalten, auf die innerhalb des Pakets verwiesen wird. Dies umfasst alle HTML-, JavaScript-, CSS-und Bildressourcen.

Die einfachste Kaizala-Aktion besteht aus drei HTML-Seiten, die angezeigt werden, wenn
*   Die Kaizal-Aktion wird aus der Aktions Palette in der Client-App-Erstellungsansicht aufgerufen.
*   Ein Benutzer versucht, auf eine auf der Chat-Canvas in der Client-App-Antwort Ansicht veröffentlichte Aktionskarten Instanz zu Antworten
*   Ein Benutzer versucht, die Zusammenfassung aller Antworten anzuzeigen, die für eine bestimmte Aktion veröffentlicht wurden Instanz-Zusammenfassungsansicht

Um mit der Kaizala-Client-App zu interagieren, können Sie die von uns bereitgestellten [JavaScript-API von KASClient. js](KASClient/README.md) verwenden.


