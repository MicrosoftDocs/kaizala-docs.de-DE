# <a name="developing-a-new-kaizala-action"></a>Entwickeln einer neuen Kaizala-Aktion

Ein Kaizala-Aktionspaket ist eine ZIP-Datei, die alle requried-Manifest-und-Ressourcendateien im Stammverzeichnis enthält.

Erstellen Sie zunächst einen neuen Ordner auf Ihrem PC, um ihn zu Ihrem Arbeitsverzeichnis zu machen.

Sie benötigen einen Code-Editor, um mit verschiedenen Arten von Webressourcen & Manifestdateien arbeiten.

>   Wir empfehlen den Code-Editor von Visual Studio. Sie können es von [hier](https://code.visualstudio.com/) herunterladen.

## <a name="defining-the-app-model"></a>Definieren des App-Modells

Die Kaizala-Aktionen unterstützen derzeit formularbasierte Datenmodelle, die zum Erstellen, sammeln und Aggregieren von Daten mithilfe der Kaizala-Aggregations Dienste verwendet werden können.

Daher müssen Sie zunächst die "Fragen" definieren, die Sie zum Erstellen eines Form-Objekts hinzufügen müssen.

Verwenden Sie das [JSON-Schema des App-Modells](appModel_schema.md) , um das App-Modell Ihrer Aktion zu erstellen.

## <a name="define-the-creation-view"></a>Definieren der ErstellungsAnsicht

Wenn eine neue Instanz der Kaizala-Aktion aus der Aktions Palette der app aufgerufen wird, wird die als CreationView gekennzeichnete HTML-Ressource gerendert. Das Ziel dieser Erstellungsansicht besteht darin, eine neue Instanz des Form-Objekts zu erstellen, wie im App-Modell definiert. 

Um mit den Kaizala-Aggregations Diensten zu interagieren und die neue Formularinstanz zu erstellen, können Sie auf die APIs im [KASCLIENT js SDK](KASClient/README.md)verweisen. Sie müssen die [KASCLIENT JS-Datei](https://manage.kaiza.la/MiniApps/DownloadSDK) herunterladen und in Ihr Paket aufnehmen.

Erstellen Sie eine neue HTML-Datei, die diese Erstellungsansicht darstellt. Rufen Sie in der entsprechenden JavaScript-Datei das KASClient JS-SDK auf, und erstellen Sie ein Form-Objekt.

## <a name="create-the-package-manifest-file"></a>Erstellen der Paket Manifestdatei

Nachdem Sie nun einen Anschein haben, was Sie erreichen möchten und eine Ansicht erfolgreich erstellt haben, können Sie mit dem Erstellen Ihrer Paket Manifestdatei beginnen.

Die Kaizala-Paket Manifestdatei enthält wichtige Informationen für die Kaizala-Plattform, damit Sie Ihre benutzerdefinierte Kaizala-Aktion erkennen und ausführen kann.

Weitere Informationen finden Sie unter [JSON-Schema des paketmanifests](package_manifest_schema.md) , um das Paketmanifest ihrer Aktion zu erstellen.

An diesem Punkt sollten Sie auch eine Symboldatei für die benutzerdefinierte Aktion in das Paket einbeziehen.

Verweisen Sie im Paketmanifest auf die HTML-Datei für die Erstellungsansicht, und ordnen Sie Sie dem entsprechenden Parameter-Objekt zu.

## <a name="configure-the-card-that-appears-on-the-conversation-canvas"></a>Konfigurieren der Karte, die auf der Unterhaltungs Leinwand angezeigt wird

Wenn eine neue Instanz einer Kaizala-Aktion erstellt und in einer Unterhaltung bereitgestellt wird, wird eine Aktionskarte auf dem Arbeitsbereich angezeigt, damit andere Benutzer in der Unterhaltung ihre Antworten anzeigen und senden können.

Informationen zum Anpassen der Chat Kartenansicht finden Sie unter [Customizing ChatCardView](ChatCanvasCardView.md) 
## <a name="define-the-response--summary-views"></a>Definieren der Reaktions-&-ZusammenfassungsAnsichten

Wenn Benutzer versuchen, Details anzuzeigen und auf eine Instanz der Kaizala-Aktion zu antworten, die in einer Unterhaltung veröffentlicht wurde, können zwei Arten von Ansichten angezeigt werden.
*   Antwort Ansicht, wenn Sie auf die primäre Schaltfläche "Call-to-Action" tippen und eine reponsse veröffentlichen möchten
*   Zusammenfassungsansicht, wenn Sie auf den Karten Kopf tippen und die aggregierte Ansicht aller gebuchten reesponses anzeigen möchten

Erstellen Sie mindestens eine HTML-Datei, die Sie zum Definieren der Aktion benötigen, und ordnen Sie Sie den relevante-Parametern in der Paket Manifestdatei zu.

Wenn Sie mit den Kaizala-Aggregations Diensten und dem nativen Client von Kaizala interagieren möchten, um Informationen abzurufen, eine Antwort zu senden oder aggregierte Antworten abzurufen, können Sie sich auf die APIs im [KASCLIENT js SDK](KASClient/README.md)beziehen.


## <a name="create-the-zip-file"></a>Erstellen der ZIP-Datei

Wählen Sie alle Dateien in Ihrem Arbeitsverzeichnis aus, und erstellen Sie eine neue ZIP-Datei für Ihr Paket. Stellen Sie sicher, dass alle Dateien im Stammverzeichnis des Pakets vorhanden sind.

*   Weiter: [Publish](publish.md)
