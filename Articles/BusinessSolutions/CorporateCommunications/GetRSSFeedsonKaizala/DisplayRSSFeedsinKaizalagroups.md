# <a name="display-rss-feeds-in-kaizala-groups"></a>Anzeigen von RSS-Feeds in Kaizala-Gruppen

Organisationen verwenden RSS-Feeds, um Ihre e-Mail-Systeme zu ergänzen und die Art der Bereitstellung von Informationen für Mitarbeiter zu verbessern. Organisationen können diese Feeds jetzt mit der ersten und mobilen Arbeitskraft nutzen, indem Sie Sie als Ankündigungen an Kaizala-Gruppen senden.

Einige Anwendungsfälle von RSS-Feeds:

1. Branchennachrichten von externen Websites
2. Unternehmensnachrichten von internen Websites
3. Konkurrieren von Informationen von externen Websites
4. Produkt Updates
5. Gruppenspezifische Feeds, z. b. Finance, Design und Tech 
6. Tipps und Tricks, beispielsweise DIY, Sport und Fotografie

Dieses Beispiel hilft einem Administrator Benutzer, RSS-Feeds zu Kaizala-Gruppen hinzuzufügen. Diese Karte hat 3 Felder in der Chat Kartenansicht-Kartentitel (z. b. Business News), Bild und Feed. Durch Tippen auf die Karte würde der Benutzer in der Webansicht in Kaizala. 
 
 >Hinweis: nur whitelisted RSS Feed URL es in Kaizala geöffnet, wenn nicht, würde der Inhalt an einen Browser weitergeleitet werden.

<img src="GetRSSFeedsOnKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

Dies ist eine Ansage in Form einer Karte, und Flow wird verwendet, um diese benutzerdefinierte Aktionskarte an die Kaizala-Gruppe zu senden.

<img src="GetRSSFeedsOnKaizalaImages/2.png" width="450" />

## <a name="implementation-steps"></a>Implementierungsschritte

1. Laden Sie die Datei ["GetRSSFeedsOnKaizala-SolutionPackage. zip](https://aka.ms/GetRssFeedsonKaizala-SolutionPackage.zip) " herunter (*Dieses Paket enthält "RSS-Feed-ActionPackage. zip" und "RSS-Feed-FlowPackage. zip"*).
2. Laden Sie die neueste Version von Kaizala ["ActionSDK. zip"](https://manage.kaiza.la/MiniApps/DownloadSDK)(*Diese enthält die Datei KASClient. js*).
3. Bearbeiten Sie den "RSS-feed-ActionPackage. zip" (*wie unten*)
   1. Unzip-Aktionspaket "RSS-feed-ActionPackage. zip" in einen Ordner
   2. Ändern der Aktion "ID" und "Anbietername" in Package. JSON
   3. KASClient. js-Datei zu diesem Ordner hinzufügen 
   4. Fügen Sie die RSS-Feed-URL in Package. JSON (wie unten) zur Whitelist dieser URL hinzu. In diesem Beispiel wird die URL für digitale Trends in der Whitelist dargestellt.    
         ```
      "externalUrls": [
      { "url": "https://www.digitaltrends.com" }
      ]  
      ```
   5. ZIP alle Inhalte in diesem Ordner (*dieser Ordner ist Ihr geändertEs Aktionspaket, das in das kaizala-Verwaltungsportal importiert werden sollte*)
   
 > Hinweis: Wählen Sie alle Dateien im Arbeitsverzeichnis aus, und erstellen Sie eine neue ZIP-Datei für Ihr Paket. Stellen Sie sicher, dass alle Dateien im Stammverzeichnis des Pakets vorhanden sind. Hierzu sollten KASClient. js, Package. JSON mit neuem "ID", "ProviderName" und whitelisted URL gehört.
 
4. [Importieren](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) des bearbeiteten Aktionspakets in das kaizala-Verwaltungsportal (*diese Karte wird von der Anruf-API gesendet, sodass die Karte nicht einer Gruppe hinzugefügt werden muss*)
5. [Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) des "RSS-Feed-Flowpackage. zip" in Ihr Microsoft Flow-Konto

    > Hinweis: Wenn Sie noch nie RSS-oder Kaizala-Verbindungen verwendet haben, fügen Sie zunächst [Verbindungen hinzu](https://docs.microsoft.com/en-us/flow/add-manage-connections) .    

6. Bearbeiten von Details in importiertem Flow (*siehe Schritte unten*) 
   1. Geben Sie im ersten Block die URL des RSS-Feeds ein. <img src= "GetRSSFeedsOnKaizalaImages/3.1.PNG" width="600" />
   2. Geben Sie im zweiten Block den Kartentitel in das Feld Wert ein. Der Kartentitel ist für Benutzer in der Chat Kartenansicht sichtbar. Z. b. "Business News"
   
      <img src= "GetRSSFeedsOnKaizalaImages/3.2.PNG" width="600" />
   3. Geben Sie im dritten Block die Aktion "ID" in das Feld "Wert" ein, die Sie in Package. JSON angegeben haben.
      <img src="GetRSSFeedsOnKaizalaImages/4.png" width="600" />
   4. Im letzten Block des Flusses
        1. Wählen Sie den Gruppennamen aus, oder geben Sie die Gruppen-ID ein, an die die Karte gesendet werden soll.
        2. Um die Gruppen-ID abzurufen, wechseln Sie zu Ihrer https://manage.kaiza.la Gruppe und wählen Sie den Bezeichner am Ende der URL aus.
        
            <img src="GetRSSFeedsOnKaizalaImages/6.PNG" width="600" />
            
        3. Klicken Sie auf Aktion, um die Aktionsart als "benutzerdefinierter Wert" aus der Dropdownliste auszuwählen.
        4. Körper "ActionBodyJson" zuordnen
       
       <img src="GetRSSFeedsOnKaizalaImages/5.png" width="600" />
7.  Speichern des Flusses

 RSS-Feeds werden an die ausgewählte Kaizala-Gruppe gesendet, und jeder Zeitablauf wird ausgelöst. 

> Hinweis: Sie können nur eine RSS-Feed-URL im Flow festlegen. Um mehrere Feeds zur gleichen Gruppe zu leiten, müssen für jeden Feed unterschiedliche Flows erstellt werden.

> Bekanntes Problem: die anzeigen führen den Benutzer über die WebView aus, da Sie nicht in der Whitelist enthalten sind.

### <a name="useful-links"></a>Nützliche Links
1. [Erstellen von Kaizala-Gruppen](https://docs.microsoft.com/en-us/office365/kaizala/groups)
2. [Konfigurieren des RSS-Feeds auf SharePoint-Website](https://support.office.com/en-us/article/create-or-subscribe-to-an-rss-feed-fb35047d-8dbd-412a-a5f3-f1712af14dcb)
