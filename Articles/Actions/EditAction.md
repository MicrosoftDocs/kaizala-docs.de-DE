# <a name="instant-edit-of-actions-in-staged-environment"></a>Sofortige Bearbeitung von Aktionen in einer bereitgestellten Umgebung

Bevor Sie mit der Bearbeitung von Aktionen beginnen, aktivieren Sie den [Status](test.md)

Während der Erstellung einer Aktion werden die HTML-Ansichten und die dazugehörigen Dateien (CSS, js) im Aktionspaket gebündelt und im Kaizala-Verwaltungs Portal importiert. Alle weiteren Änderungen an den Ansichten erfordern, dass das Paket neu erstellt und im Kaizala-Verwaltungs Portal hochgeladen wird.

Um die spätere Bearbeitung der HTML-Ansichten zu vereinfachen, ermöglicht Kaizala die Bearbeitung von HTML-, JavaScript-und CSS-Dateien lokal und zeigt sofort die Updates in der Kaizala-app. Dies beinhaltet das Erstellen eines lokalen HTTP-Servers, der die aktualisierten Dateien hostet, und die Kaizala-App verwendet diese Dateien anstelle der im eigentlichen Paket vorhandenen Dateien.

>  **Hinweis:** Um die sofortige Bearbeitung zu ermöglichen, muss die Aktion auf dem Kaizala-Verwaltungs Portal hochgeladen werden und sich im Status "inszeniert" befinden.

## <a name="enable-instant-edit-in-android-devices"></a>Sofortige Bearbeitung in Android-Geräten aktivieren

### <a name="steps-to-create-local-http-server-in-windows"></a>Schritte zum Erstellen des lokalen HTTP-Servers in Windows

* **Schritt 1: Erstellen einer Kopie des Aktionspakets auf Ihrem lokalen Computer**

  * Erstellen Sie eine Kopie des Aktionspakets an einem Speicherort Ihrer Wahl auf Ihrem Computer. Der Name des Ordners sollte die Aktions-ID sein.
    
* **Schritt 2: Ausführen des python-Befehls**

  *  Öffnen Sie Command Terminal, und navigieren Sie zu dem Ordner, der das Aktionspaket enthält.
  *  Führen Sie den folgenden Befehl aus:`python -m SimpleHTTPServer 8000`
  
      > Die Installation von Python ist eine Voraussetzung für die Ausführung des obigen Skripts.
  
* **Schritt 3: Überprüfen des lokalen Servers**

  * Die URL Ihres lokalen Servers wird nun`http://localhost/<ActionId>:8000`
  * Um Ihren Server zu überprüfen, öffnen Sie einen Browser, und geben Sie oben die URL des lokalen Servers in die Adressleiste ein, und Sie sollten in der Lage sein, den Inhalt des Ordners anzuzeigen, von dem der Server gestartet wurde.
  
### <a name="steps-to-setup-your-android-device"></a>Schritte zum Einrichten Ihres Android-Geräts

> Voraussetzung: Sie müssen den Debugmodus wie [hier](test.md)beschrieben aktivieren. Genehmigte Versionen von Aktionen unterstützen dieses Feature nicht

* **Schritt 1: Verbinden Sie Ihren Computer über eine USB-Verbindung mit dem Gerät**

    * Ihr Gerät muss über USB mit dem Computer verbunden sein.
    
* **Schritt 2: Aktivieren der Diagnose für Kaizala-App** 

    * Wechseln Sie in Kaizala zu Profil-> Einstellungen->. Tippen Sie fünfmal auf "Microsoft Kaziala Logo", um die Diagnoseoption zu aktivieren. * * Drücken Sie Back to Reach Settings page. Klicken Sie unten auf der Seite "Einstellungen" unter "Diagnose" auf "Problembehandlung".
    * Aktivieren Sie die Option "Mini apps Location override", um das Feld "Server-URL" einzuSchalten.
    * Wechseln Sie <chrome://inspect/> zu auf Ihrem Hostcomputer, und aktivieren Sie die Weiterleitung der Portierung. Geben Sie unter Einstellungen für die Portierung die Nummer als "8000" (erste Registerkarte) und IP-Adresse und-Portierung als "localhost: 8000" an (zweite Registerkarte).
    * Mit dieser Änderung ruft Kaizala die HTML/CSS/JS-Dateien Ihrer Aktion vom Server ab, anstatt die gepackten Dateien zu verwenden.
    
* **Schritt 3: vornehmen von Änderungen im Aktions Ordner Ihres Computers**

    * Änderungen an den Dateien können sofort beobachtet werden, indem die Ansicht in der APP neu geladen wird (navigieren Sie weg von der Ansicht und öffnen Sie Sie erneut)
    
Sobald der Bearbeitungsvorgang abgeschlossen ist, können die aktualisierten Dateien gebündelt werden, um das Paket zu erstellen und das im Portal vorhandene Paket zu aktualisieren. Deaktivieren Sie auf der Seite Diagnose die Option Mini App Location override, um das Standardverhalten wiederherzustellen.

