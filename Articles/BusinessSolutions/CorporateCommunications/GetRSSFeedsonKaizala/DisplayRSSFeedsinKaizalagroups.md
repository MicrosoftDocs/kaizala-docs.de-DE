# <a name="display-rss-feeds-in-kaizala-groups"></a>Anzeigen von RSS-Feeds in Kaizala Gruppen

Organisationen verwenden RSS-Feeds zu ergänzen ihre e-Mail-Systeme und verbessern die Art und Weise, in der sie Informationen für Mitarbeiter bereitstellen. Organisationen können diese Feeds mit der ersten Zeile und mobile Mitarbeiter jetzt durch Senden der Formularvorlagen als Ankündigungen Kaizala Gruppen nutzen.

Wenige Anwendungsfälle von RSS-feeds

1. Neuigkeiten aus der Branche aus externen Websites
2. Nachrichten von internen Websites
3. Füllen Sie die Informationen aus externen Websites
4. Produktupdates
5. Gruppe bestimmte feeds, Ex - Finance, Entwurf und Tech 
6. Tipps und Tricks, Ex-DIY, Sportliga und Fotos

In diesem Beispiel hilft Ihnen, ein Administrator die Aktivierung RSS-Feeds zu Kaizala Gruppen hinzufügen.  Diese Karte enthält 3 Felder in Chat Karte anzeigen-Karte Titel (Ex - Unternehmensnachrichten), Bild, Feed Titel (Titel des der Newsfeed). Tippen Sie auf der Karte gelangen Sie zur Webansicht innerhalb Kaizala. 
 
 >Hinweis: Nur White RSS-feed URL öffnen in Kaizala, falls nicht, würde der Inhalt in einem Browser umgeleitet werden.

<img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/1.png" alt="Chat card view Logo" width="400" />

Hierbei handelt es sich um eine Ankündigung in Form einer Karte und Microsoft Flow wird verwendet, um diese benutzerdefinierte Aktion Karte Kaizala Gruppe zu senden.

<img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/2.png" width="450" />

## <a name="implementation-steps"></a>Implementierungsschritte

1. Laden Sie die ["GetRSSFeedsOnKaizala SolutionPackage.zip"](/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRssFeedsonKaizala-SolutionPackage.zip) (*Dieses Paket enthalten, "RSS-Feed-ActionPackage.zip" und "RSS-Feed-FlowPackage.zip"*)
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
           
   5. Zip all the contents in this folder (*This folder is your modified Action package which should be imported to kaizala management portal*)
   
 > Note: Select all the files in your working directory and create a new zip file for your package. Ensure that all files are present in the root directory of the package. This should include KASClient.js, package.json with new "id", "provider name" and whitelisted URL
    
4. [Import](https://docs.microsoft.com/en-us/kaizala/actions/publish#import-kaizala-action) the edited action package to kaizala management portal (*This card is sent by calling API, so there is no need to add the card to a group*)

5. [Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the "RSS-feed-Flowpackage.zip" to your Microsoft Flow account

> Note- If you have never used RSS or Kaizala connections, first [add connections](https://docs.microsoft.com/en-us/flow/add-manage-connections)
    
6. Edit details in Imported Flow (*See steps below*) 
   1. In the First block , enter the RSS feed URL
  
       <img src= "/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/3.1.PNG" width="600" />
   
   2. In the second block, enter the card title in "value" field. The card title will be visible to users in chat card view. Ex- "Business News"

      <img src= "/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/3.2.PNG" width="600" />

   3. In the third block, enter the Action "id" in "value" field, that you have given in package.json
   
      <img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/4.png" width="600" />
   
   4. In the Last block of the Flow
        1. Select the group name or enter the group id where you want to send the card
        2. To get the group id, go to your group on https://manage.kaiza.la and select the identifier at the end of the URL.

      <img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/6.PNG" width="600" />
   
       3. Click on action, to select action type as "custom value" from the dropdown
       4. Map action body to "ActionBodyJson"
       
       <img src="/Articles/BusinessSolutions/CorporateCommunications/GetRSSFeedsonKaizala/GetRSSFeedsOnKaizalaImages/5.png" width="600" />

7.  Save the Flow

RSS feeds will be sent to the selected Kaizala group, each time flow is triggered. 



> Note: You can only set one RSS feed URL in the Flow. To direct multiple feeds to same group, different Flows have to be created for each feed

> Known issue: On iOS, the ads take the user out of the webview since they are not whitelisted

### Useful links

1. [How to create Kaizala Groups](https://docs.microsoft.com/en-us/office365/kaizala/groups)
2. [Configure RSS Feed to SharePoint site](https://support.office.com/en-us/article/create-or-subscribe-to-an-rss-feed-fb35047d-8dbd-412a-a5f3-f1712af14dcb)
