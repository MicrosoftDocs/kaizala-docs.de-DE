# <a name="display-rss-feeds-in-kaizala-groups"></a>Anzeigen von RSS-Feeds in Kaizala Gruppen

Organisationen verwenden RSS-Feeds zu ergänzen ihre e-Mail-Systeme und verbessern die Art und Weise, in der sie Informationen für Mitarbeiter bereitstellen. Organisationen können diese Feeds mit der ersten Zeile und mobile Mitarbeiter jetzt durch Senden der Formularvorlagen als Ankündigungen Kaizala Gruppen nutzen.

Wenige Anwendungsfälle von RSS-Feeds:

1. Neuigkeiten aus der Branche aus externen Websites
2. Nachrichten von internen Websites
3. Füllen Sie die Informationen aus externen Websites
4. Produktupdates
5. Gruppe bestimmte feeds, z. B. Finanzen, Entwurf und Tech 
6. Tipps und Tricks, z. B., DIY, Sportliga und Fotos

In diesem Beispiel hilft Ihnen, ein Administrator die Aktivierung RSS-Feeds zu Kaizala Gruppen hinzufügen. Diese Karte enthält 3 Felder im Chat Karte anzeigen-Karte Titel (z. B., Unternehmensnachrichten), Bild und Feed Titel. Tippen Sie auf der Karte würde der Benutzer auf Webansicht in Kaizala ausführen. 
 
 >Hinweis: Nur White RSS-feed URL öffnen in Kaizala, falls nicht, würde der Inhalt in einem Browser umgeleitet werden.

<img src="GetRSSFeedsOnKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

Hierbei handelt es sich um eine Ankündigung in Form einer Karte und Ablauf wird verwendet, um diese benutzerdefinierte Aktion Karte Kaizala Gruppe zu senden.

<img src="GetRSSFeedsOnKaizalaImages/2.png" width="450" />

## <a name="implementation-steps"></a>Implementierungsschritte

1. Laden Sie die ["GetRSSFeedsOnKaizala SolutionPackage.zip"](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRssFeedsonKaizala-SolutionPackage.zip) (*Dieses Paket enthalten, "RSS-Feed-ActionPackage.zip" und "RSS-Feed-FlowPackage.zip"*)
2. Laden Sie die neueste Version von Kaizala ["ActionSDK.Zip"](https://manage.kaiza.la/MiniApps/DownloadSDK)(*Dies enthält die KASClient.js-Datei*)
3. Bearbeiten der "RSS-Feed-ActionPackage.zip" (*wie unten*)
   1. Entzippen Sie Aktion Paket "RSS-Feed-ActionPackage.zip" in einen Ordner
   2. Ändern Sie die Aktion "Id" und "Anbietername" in package.json
   3. Fügen Sie diesen Ordner KASClient.js-Datei hinzu 
   4. Fügen Sie RSS in Package.json(as below) White-Liste die URL-feed-URL. In diesem Beispiel ist die URL der digitalen Trends White.    
         ```
      "externalUrls": [
      { "url": "https://www.digitaltrends.com" }
      ]  
      ```
   5. ZIP-alle Inhalte in diesen Ordner (*dieser Ordner ist Ihr geänderte Aktion-Paket die Kaizala Management Portal importiert werden soll*)
   
 > Hinweis: Wählen Sie alle Dateien in Ihrem Arbeitsverzeichnis und erstellen Sie eine neue Zip-Datei für Ihr Paket. Stellen Sie sicher, dass alle Dateien im Stammverzeichnis des Pakets vorhanden sind. Dazu zählen u. a. KASClient.js package.json mit neuen "Id", "ProviderName" und White URL
 
4. [Importieren](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) des Pakets bearbeiteten Aktion Kaizala-Verwaltungsportal (*vom aufrufenden API diese Karte gesendet wird, also besteht keine Notwendigkeit, um die Visitenkarte zu einer Gruppe hinzufügen*)
5. [Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) der "RSS-Feed-Flowpackage.zip" Flow Microsoft-Konto

> Hinweis: Wenn Sie RSS- oder Kaizala Verbindungen mit der ersten [Hinzufügen von Verbindungen](https://docs.microsoft.com/en-us/flow/add-manage-connections) noch nie verwendet haben    

6. Bearbeiten der Details in importiert Flow (*wie im folgenden beschrieben*) 
   1. Geben Sie in der erste Block den RSS-feed-URL <img src= "GetRSSFeedsOnKaizalaImages/3.1.PNG" width="600" />
   2. Geben Sie in der zweite Block den Titel der Karte im Feld "Wert" aus. Der Titel der Visitenkarte werden für Benutzer in einer Kartenansicht Chat angezeigt. Z. B. "Unternehmensnachrichten"
   
      <img src= "GetRSSFeedsOnKaizalaImages/3.2.PNG" width="600" />
   3. Geben Sie in der dritte Block die Aktion "Id" im Feld "Wert", die Sie in package.json zugewiesen haben
      <img src="GetRSSFeedsOnKaizalaImages/4.png" width="600" />
   4. In den letzten Block mit den Ablauf
        1. Wählen Sie den Namen der Gruppe aus, oder geben Sie die Gruppen-Id, wo die Karte gesendet werden soll
        2. Wenn Sie die Gruppen-Id erhalten möchten, wechseln Sie an Ihre Gruppe auf https://manage.kaiza.la und wählen Sie die Kennung am Ende der URL.
        
            <img src="GetRSSFeedsOnKaizalaImages/6.PNG" width="600" />
            
        3. Klicken Sie auf Aktion, Aktionstyp als "benutzerdefinierter Wert" aus der Dropdownliste auswählen
        4. Zuordnen von Stelle "ActionBodyJson"
       
       <img src="GetRSSFeedsOnKaizalaImages/5.png" width="600" />
7.  Speichern der RSS-Fluss werden Feeds der ausgewählten Kaizala Gruppe jedes Mal versendet Auslösung Fluss. 

> Hinweis: Sie können nur eine RSS-feed-URL in den Ablauf festlegen. Um mehrere Feeds, demselben zu leiten, müssen verschiedene Abläufe für jeden Feed erstellt werden soll

> Bekanntes Problem: auf iOS, übernehmen die anzeigen den Benutzer aus der Webansicht, da sie nicht weißen Liste enthalten sind

### <a name="useful-links"></a>Hilfreiche links
1. [Gewusst wie: Kaizala Gruppen erstellen](https://docs.microsoft.com/en-us/office365/kaizala/groups)
2. [Konfigurieren der RSS-Feed für die SharePoint-Website](https://support.office.com/en-us/article/create-or-subscribe-to-an-rss-feed-fb35047d-8dbd-412a-a5f3-f1712af14dcb)
