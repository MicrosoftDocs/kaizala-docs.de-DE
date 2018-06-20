# <a name="instant-edit-of-actions-in-staged-environment"></a>Sofortnachrichten Bearbeiten von Aktionen in phasenweise-Umgebung

Bevor Sie Bearbeitungsaktionen beginnen, aktivieren Sie [Mehrstufige Zustand](test.md)

Beim Erstellen einer Aktion, die HTML-Ansichten und die zugehörigen Dateien (Css, Js) in dem Paket Aktion gebündelt sind und auf dem Kaizala-Verwaltungsportal importiert. Alle weiteren Änderungen an Ansichten erfordern das Paket neu erstellt und auf dem Kaizala-Verwaltungsportal hochgeladen werden.

Ermöglicht das Bearbeiten von HTML, JavaScript, um die nachfolgenden Bearbeitung der HTML-Ansichten zu vereinfachen, Kaizala und CSS-Dateien lokal und sofort finden im Updates in der Kaizala-App. Dieser Schritt umfasst das Erstellen eines lokalen HTTP-Servers, das aktualisierten Dateien gehostet wird und Kaizala App wird diese Dateien verwenden, anstatt die Dateien in das aktuelle Paket vorhanden.

>  **Hinweis:** Um instant bearbeiten zu aktivieren, muss Aktion muss auf Kaizala-Verwaltungsportal hochgeladen werden und im mehrstufige Zustand

## <a name="enable-instant-edit-in-android-devices"></a>Aktivieren von Sofortnachrichten bearbeiten im Android-Geräte

### <a name="steps-to-create-local-http-server-in-windows"></a>Schritte zum Erstellen von lokalen HTTP-Server in Windows

* **Schritt 1: Erstellen Sie eine Kopie des Action-Pakets in Ihrem lokalen Computer**

  * Erstellen Sie eine Kopie des Action-Pakets an einem Speicherort Ihrer Wahl auf Ihrem Computer. Der Name des Ordners sollte die Aktion-Id.
    
* **Schritt 2: Python Befehl**

  *  Öffnen Sie Befehl Terminal, und navigieren Sie zu dem Ordner mit der Aktion-Paket.
  *  Führen Sie diesen Befehl:`python -m SimpleHTTPServer 8000`
  
      > Installation von Python ist eine Voraussetzung für das obige Skript ausführen.
  
* **Schritt 3: Überprüfen Sie lokalen server**

  * Die lokale Server-URL jetzt.`http://localhost/<ActionId>:8000`
  * Überprüfen Sie Ihre Server Öffnen eines Browsers, und geben über dem lokalen Server Url in der Adressleiste und Sie sollte können Sie den Inhalt des Ordners, in dem der Server gestartet wurde.
  
### <a name="steps-to-setup-your-android-device"></a>Schritte zum Einrichten Ihrer Android-Geräts

> Voraussetzung: Sie müssen Debugmodus, wie weiter oben erwähnt [hier](test.md)aktivieren. Genehmigte Versionen der Aktionen unterstützt dieses Feature nicht

* **Schritt 1: Verbinden von Ihrem Computer auf über ein Usb-Gerät**

    * Ihr Gerät muss eine Verbindung mit der Ihrem Computer über Usb
    
* **Schritt 2: Aktivieren von Diagnose für Kaizala App** 

    * In Kaizala, navigieren Sie zur Benutzerprofildienst-Einstellungen > -> zu. Tippen Sie auf auf "Microsoft Kaziala Logo" fünfmaliges um Diagnose-Option zu aktivieren. ** Drücken Sie wieder auf der um Seite Einstellungen zu erreichen. Klicken Sie auf "Problembehandlung" unter "Diagnostics" Label am unteren Rand der Seite Einstellungen option
    * Aktivieren Sie die Option "Mini Apps Speicherort Override" So aktivieren Sie im Feld Server URL.
    * Wechseln Sie zu <chrome://inspect/> auf dem Hostcomputer und Port-Weiterleitung aktivieren. Geben Sie unter weiterleitungseinstellungen Port die Portnummer als "8000"(first tab) und IP-Adresse und Port als "Localhost:8000" (zweite Tab-Objekt)
    * Mit dieser Änderung wird Kaizala Ihrer Aktion die HTML/Css/JS-Dateien auf dem Server, anstatt die Paketdateien abrufen.
    
* **Schritt 3: Ändern Sie im Ordner "Aktion" des Computers**

    * Alle Änderungen an den Dateien können durch Neuladen der Ansicht in der app sofort beobachtet (Navigieren Weg von der Ansicht und anschließend wieder geöffnet)
    
Nach Abschluss der Bearbeitung können die aktualisierten Dateien gebündelt werden, um das Paket zu erstellen und aktualisieren das Paket im Portal vorhanden. Deaktivieren Sie die Option Mini App Speicherort außer Kraft setzen, in der Diagnose-Seite, um das Standardverhalten wiederherzustellen.


## <a name="enable-instant-edit-in-ios-devices"></a>Aktivieren von Sofortnachrichten bearbeiten in iOS-Geräte

### <a name="steps-to-create-local-http-server-in-mac"></a>Schritte zum Erstellen von lokalen HTTP-Server in MAC

* **Schritt 1: Erstellen Sie eine Kopie des Action-Pakets in Ihrem lokalen Computer**

  * Erstellen Sie eine Kopie des Action-Pakets an einem Speicherort Ihrer Wahl auf Ihrem Computer. Der Name des Ordners sollte die Aktion-Id.

* **Schritt 2: Führen Sie eine Skript**

    * Ein Skript Python wird verwendet, um einen lokalen Server zu erstellen. Hier wird die script(noCacheServer.py) angefügt. Kopieren Sie diese Skriptdatei im gleichen Ordner, der den oben erstellten MiniApp Paketordner enthält. 
                
      > Installation von Python ist eine Voraussetzung für das obige Skript ausführen.

* **Schritt 3: Starten Sie lokalen server**

    * Öffnen Sie Befehl Terminal, und navigieren Sie zu dem Ordner mit der Aktion-Pakets und des Serverskripts. 
    * Zum Starten der Server den folgenden Befehl eingeben:`python noCacheServer.py 8000`
    
    Die lokale Server-URL jetzt.`http://<IP Address of your machine>:8000`

    * Überprüfen Sie Ihre Server Öffnen eines Browsers, und geben über dem lokalen Server Url in der Adressleiste und Sie sollte können Sie den Inhalt des Ordners, in dem der Server gestartet wurde.


### <a name="steps-to-setup-your-ios-device"></a>Schritte zum Einrichten Ihrer iOS-Geräte

> Voraussetzung: Sie müssen Debugmodus, wie weiter oben erwähnt [hier](test.md)aktivieren. Genehmigte Versionen der Aktionen unterstützt dieses Feature nicht
* **Schritt 1: Verbinden Sie mit demselben Netzwerk auf Gerät wie Ihrem Computer**

    * Ihr Gerät müssen eine Verbindung mit demselben Netzwerk wie Ihr Computer (oder im Netzwerk an Ihren Computer freigeben und eine Verbindung damit herzustellen vom Gerät)
     
* **Schritt 2: Aktivieren von Diagnose für Kaizala App** 

    * In Kaizala navigieren Sie zur Benutzerprofildienst -> Einstellungen. Tippen Sie auf den Titel Einstellungen fünf Arbeitszeiten um Diagnose-Option zu aktivieren. Navigieren Sie zur Seite Diagnose durch Tippen auf die Option Diagnose
    * Aktivieren Sie die Option Mini App Speicherort außer Kraft setzen, aktivieren Sie im Feld Server URL. Geben Sie die URL des Servers wie folgt die oben erstellte,`http://<IP Address>:8000`
    * Mit dieser Änderung wird Kaizala Ihrer Aktion die HTML/Css/JS-Dateien auf dem Server, anstatt die Paketdateien abrufen.
    
* **Schritt 3: Ändern Sie im Ordner "Aktion" des Computers**

    * Alle Änderungen an den Dateien können durch Neuladen der Ansicht in der app sofort beobachtet (Navigieren Weg von der Ansicht und anschließend wieder geöffnet)
    
Nach Abschluss der Bearbeitung können die aktualisierten Dateien gebündelt werden, um das Paket zu erstellen und aktualisieren das Paket im Portal vorhanden. Deaktivieren Sie die Option Mini App Speicherort außer Kraft setzen, in der Diagnose-Seite, um das Standardverhalten wiederherzustellen.

