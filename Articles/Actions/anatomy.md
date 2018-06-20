# <a name="anatomy-of-a-kaizala-action-package"></a>Anatomie einer Aktion Kaizala-Paket

Ein Paket Kaizala-Aktion ist eine regulären Zipdatei, die nicht mit Kennwortschutz versehen ist und weist eine maximale Größe von 1MB. Die Ressourcen im Paket werden im Stammverzeichnis der Zip-Datei und nicht in eine beliebige Verzeichnisstruktur. Die Ressourcen können nicht auch alle externen Ressourcen anwesenden im Paket verweisen.

Sind die grundlegenden Komponenten eines Pakets Kaizala Aktion 
*   Eine Manifestdatei im JSON-format
*   Eine app-Modell für die Aktion Kaizala im JSON-format
*   Webressourcen, die Ihre Aktion Kaizala - HTML, JS, CSS bilden und Bilddateien

## <a name="package-manifest"></a>Paketmanifest

Mit dem Manifest werden Einstellungen der Aktion Kaizala wie die folgenden:
*   Der Aktion angezeigter Name, Beschreibung, ID, Version und Aktionssymbol.
*   Verschiedene Ansichten, die die Aktion und ihre jeweiligen Invokation Punkt zuordnen definieren
    * Eine Ansicht erstellen, wenn eine Aktion aus der Palette aufgerufen wird.
    * Eine Kartenansicht, die auf die Zeichenbereich Chat, wenn eine Instanz der Aktion angezeigt wird, wird gesendet.
    * Eine Ansicht Responder für Benutzer an die Kaizala-Aktion
    * Eine Zusammenfassung zusammengefasster zum Anzeigen Antworten
*   Über die systemeigenen Ansichten verwendet werden, die Ihre benutzerdefinierten Ansichten kapseln Etiketten

Weitere Informationen finden Sie unter [Package-Manifestschema im JSON-Format](package_manifest_schema.md).

## <a name="app-model"></a>App-Modell

Das App-Modell gibt an, das die Funktionen des die Kaizala Aktion, einschließlich:
*   Das Datenmodell für das Form-Objekt verwendet werden, um die Kaizala Aggregation Dienste nutzen
*   Eigenschaften für das Form-Objekt
*   Einstellungen für das Form-Objekt

Weitere Informationen finden Sie unter [App Modellschema im JSON-Format](appModel_schema.md).

## <a name="web-resources"></a>Webressourcen

Wie bereits erwähnt, muss das Paket Kaizala alle Ressourcen im Paket referenzierten enthalten. Dazu gehören alle HTML, JavaScript, CSS- und Bild-Ressourcen.

Grundlegende Kaizala Aktion besteht aus drei HTML-Seiten, die angezeigt wird, wenn
*   Die Kaizal-Aktion wird aus der Palette-Aktion in der Client-app - Erstellung Ansicht aufgerufen.
*   Ein Benutzer versucht, eine Aktion Karte-Instanz auf die Chat Zeichenbereich in der Client-app - Antwort Ansicht gebucht beantworten
*   Ein Benutzer versucht, die Zusammenfassung aller Antworten für eine bestimmte Aktion Instanz - Zusammenfassungsansicht veröffentlicht anzeigen

Zur Interaktion mit der Kaizala-Client-app können Sie die [KASClient.js JavaScript-API](KASClient/README.md) verwenden, die wir bereitstellen.


