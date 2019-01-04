# <a name="display-sharepoint-announcements-in-kaizala-groups"></a>Anzeigen von SharePoint-Ankündigungen in Kaizala Gruppen 
Organisationen verwenden SharePoint Ankündigung app Neuigkeiten, Status und andere kurze Informationen zu Mitarbeitern gemeinsam. Ankündigung der SharePoint-app, die mit einer Liste stammen, ist eine spezielle Art von Liste, die Sie Ankündigungen erstellen kann.

In diesem Beispiel verwenden, können Organisationen SharePoint Ankündigungen für die erste Zeile und mobile Mitarbeiter auf Kaizala freigeben. Diese Karte hat 3 Felder in Chat Karte-Anlagen anzeigen (In diesem Beispiel Fotostory mit Bildern), Titel und die Ankündigung Body (Beschreibung). Dies wird als eine Karte Out-of-Box-Ankündigung an eine Gruppe Kaizala gesendet.

Die Kartenansicht Chat ist als unten

<img src="SharepointAnnouncementImages/1.png" alt="Chat card view Logo" width="340" />

Klicken Sie auf die Karte tippen fesselnden Ansicht ist, als unter

<img src="SharepointAnnouncementImages/2.png" alt="immersive view Logo" width="180" />

In diesem Szenario kann sich grob in 2 Schritte unterteilt werden:
1. Erstellen Sie eine Ankündigungsliste mit Spalten - Titel, Anlagen und Ankündigung body(description) 

    > Hinweis: Rich-Text wird von Out-of-Box-Ankündigung Karte nicht unterstützt. Schalten Sie rich-Text für Sharepoint-Spalte, die Ankündigung body(description) beim Erstellen der Spalte hat.

    <img src="SharepointAnnouncementImages/3.5.png" width="200" />

2. Konfigurieren Sie Fluss so, dass, wenn ein neues Element erstellt oder vorhandenes Element wird in der Ankündigungsliste geändert, eine Karte Out-of-Box-Ankündigung an eine Gruppe Kaizala gesendet wird

    <img src="SharepointAnnouncementImages/3.png" alt="Sharepoint&Flow Logo" width="400" />

## <a name="implementation-steps"></a>Implementierungsschritte


1. [Ankündigung hinzufügen app](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) für SharePoint-Website (*wie unten*)
     1. Klicken Sie auf das einstellungssymbol
     2.  Klicken Sie auf App hinzufügen 
     3.  Wählen Sie aus der Liste der verfügbaren Apps Ankündigung-App
2. Verwenden Sie das [hervorgehobene Content-Webpart](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) (*bei Bedarf für Visualisierung*)
3. Laden Sie die [SharepointAnnouncementOnKaizala SolutionPackage.zip](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/BusinessSolutions/CorporateCommunications/SharepointAnnouncementsonKaizala/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*Dies ist ein Flow-Paket*)
4. [Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage.zip Flow Microsoft-Konto
   
   > Hinweis: Wenn Sie noch nie, Sharepoint oder Kaizala Verbindung mit der ersten [Hinzufügen von Verbindungen verwendet haben](https://docs.microsoft.com/en-us/flow/add-manage-connections)
   
5. Bearbeiten Sie den Ablauf (*wie unten*)
    1. In der erste Block des Datenflusses
    
         1. Geben Sie die Websiteadresse
         2. Geben Sie den Namen der Liste (*Schritte zur Liste Name ist wie im folgenden*)
            - Klicken Sie auf der Registerkarte der Website Inhalt auf der linken Ecke des Bildschirms
            - Wählen Sie die Ankündigung aus, aus der Sie Ansagen an Kaizala senden möchten
            - Klicken Sie auf das einstellungssymbol für in der oberen rechten Ecke des Bildschirms
            - Wechseln Sie zu Einstellungen für die Liste
            - Kopieren Sie die URL der Liste im Browser.
            - Die URL decodieren (Sie können die URL decodieren [hier](https://www.url-encode-decode.com/) )
        <img src="SharepointAnnouncementImages/4.PNG" alt="" width="500" />
      
    2. In der zweite Block des Datenflusses
   
        Ordnen Sie "Wert" Feld mit der Spaltentitel der Ankündigungsliste, die Ankündigung body(description) von dynamischen Inhalten hat. In den unten Beispiel ist der Spaltentitel "Ankündigung Body" <img src="SharepointAnnouncementImages/5.png" alt="" width="600" />
       
    3. In den letzten Block mit den Ablauf
    
       Wählen Sie den Namen der Gruppe aus der Dropdownliste aus. In diesem Beispiel ist "Everyone@Fabrikam"
       <img src="SharepointAnnouncementImages/6.png" alt="" width="450" />
6. Speichern Sie den Ablauf

Ankündigung an gesendet der ausgewählten Gruppe Kaizala jedes Mal Flow ausgelöst wird.

> Hinweis: Textdatei wird als Anlage nicht unterstützt.
