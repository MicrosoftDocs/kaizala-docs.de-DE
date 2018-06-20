# <a name="developing-a-new-kaizala-action"></a>Entwickeln eine neue Kaizala-Aktion

Ein Paket Kaizala-Aktion ist eine Zip-Datei, die alle benötigte Manifest und Resource-Dateien im Stammverzeichnis enthält.

Erstellen Sie zunächst einen neuen Ordner auf Ihrem PC zu vereinfachen Ihre Arbeit Dorectory.

Sie benötigen einen Code-Editor zum Arbeiten mit verschiedenen Arten von Webressourcen & Manifestdateien.

>   Es wird empfohlen, den Visual Studio-Code-Editor. Sie können es [hier](https://code.visualstudio.com/) herunterladen.

## <a name="defining-the-app-model"></a>Definieren das App-Modell

Die Kaizala Aktionen unterstützt derzeit Formular basiert von Datenmodellen, die zum Erstellen, erfassen und das Aggregieren von Daten mithilfe der Kaizala Aggregation Dienste verwendet werden können.

Daher müssen Sie zunächst die müssen Sie ein Form-Objekt erstellen, um Fragen zu definieren.

Verweisen Sie auf die [app Modellschema JSON](appModel_schema.md) , um Ihre Aktion app-Modell erstellen.

## <a name="define-the-creation-view"></a>Definieren der Ansicht erstellen

Wenn eine neue Instanz der Kaizala Aktion aus der app-Aktion Palette aufgerufen wird, die HTML-Ressource gekennzeichnet, wie die CreationView gerendert wird. Das Ziel dieser Ansicht erstellen ist, erstellen Sie eine neue Instanz des Form-Objekts wie in der app-Modell definiert. 

Zur Interaktion mit der Kaizala Aggregation-Dienste und erstellen neue Formularinstanz, können Sie auf die APIs im [KASClient JS SDK](KASClient/README.md)verweisen. Sie müssen die [KASClient JS-Datei](https://manage.kaiza.la/MiniApps/DownloadSDK) herunterladen und es in Ihr Paket aufnehmen.

Erstellen Sie eine neue HTML-Datei, die in dieser Ansicht Erstellung darstellt. In der entsprechenden Javascript-Datei Aufrufen des KASClient JS-SDK, und erstellen Sie ein Form-Objekt.

## <a name="create-the-package-manifest-file"></a>Erstellen Sie die Paket-Manifestdatei

Nun, Sie haben eine Semblance der verfügbare zu erreichen und eine Ansicht – erfolgreich erstellt haben können Sie mit dem Erstellen Ihrer Paket-Manifestdatei.

Die Manifestdatei Kaizala Paket enthält wichtige Informationen für die Plattform Kaizala dafür zu erkennen und die benutzerdefinierte Kaizala-Aktion ausführen.

Verweisen Sie auf das [Paket JSON-Manifestschemas](package_manifest_schema.md) Manifest für Ihre Aktion-Paket zu erstellen.

Zu diesem Zeitpunkt sollten Sie auch eine Symboldatei für die benutzerdefinierte Aktion im Paket einschließen.

Verweisen auf Ihre Erstellung Ansicht HTML-Datei in der Paketmanifest-, und ordnen sie die entsprechenden Parameter-Objekt.

## <a name="configure-the-card-that-appears-on-the-conversation-canvas"></a>Konfigurieren Sie die Karte, die angezeigt wird, klicken Sie auf die Unterhaltung Zeichenbereich

Wenn eine neue Instanz einer Aktion Kaizala erstellt und in einer Unterhaltung gebucht, wird eine Aktion Karte auf den Zeichenbereich für andere Benutzer in der Unterhaltung anzeigen und senden ihre Antworten angezeigt.

Um die Kartenansicht Chat anpassen, finden Sie unter [Anpassen von ChatCardView](ChatCanvasCardView.md) 
## <a name="define-the-response--summary-views"></a>Definieren der Antwort & Übersichten

Wenn Benutzer versuchen, Details anzeigen und reagieren auf eine Instanz der Kaizala-Aktion in einer Unterhaltung gebucht, können sie zwei Arten von Ansichten anzeigen.
*   Antwort Ansicht beim Tippen Sie auf die primäre Taste Call-to-Action und eine Antwort bereitstellen möchten
*   Ansicht "Zusammenfassung" beim Tippen Sie auf der Karte Kopfzeile und die Aggregierte Ansicht der alle gebucht Reesponses anzeigen möchten

Erstellen Sie eine oder mehrere HTML-Dateien nach Bedarf, definieren Sie die Aktion, und ordnen sie Sie in der Manifestdatei Paket die Grundlage-Parameter.

Zur Interaktion mit der Kaizala Aggregation Dienste und die Kaizala Native Client zum Abrufen von Informationen, senden eine Antwort oder aggregierte Antworten erhalten möchten, können Sie auf die APIs im [JS-SDK KASClient](KASClient/README.md)verweisen.


## <a name="create-the-zip-file"></a>Erstellen Sie die ZIP-Datei

Wählen Sie alle Dateien im Arbeitsverzeichnis, und erstellen Sie eine neue Zip-Datei für Ihr Paket. Stellen Sie sicher, dass alle Dateien im Stammverzeichnis des Pakets vorhanden sind.

*   Weiter: [Veröffentlichen](publish.md)
