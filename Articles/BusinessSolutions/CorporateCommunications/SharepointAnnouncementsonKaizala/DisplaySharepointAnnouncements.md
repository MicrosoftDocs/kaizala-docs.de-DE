# <a name="display-sharepoint-announcements-in-kaizala-groups"></a>Anzeigen von SharePoint-anSagen in Kaizala-Gruppen 
Organisationen verwenden SharePoint-Ansage-App zum Freigeben von Nachrichten, Status und anderen kurzen Informationen zu Mitarbeitern. SharePoint-Ansage-APP, die mit einer Liste geliefert wird, ist ein spezieller Listentyp, mit dem Sie Ankündigungen erstellen können.

Mithilfe dieses Beispiels können Organisationen SharePoint-Ankündigungen mit der ersten und mobilen Arbeitskräften in Kaizala freigeben. Diese Karte hat 3 Felder in der Chat Kartenansicht-Anlagen (in diesem Beispiel Fotostory von Bildern), Titel und Ansagetext (Beschreibung). Diese wird an eine Kaizala-Gruppe als out-of-Box-Ansage Karte gesendet.

Die Chat Kartenansicht ist wie folgt.

<img src="SharepointAnnouncementImages/1.png" alt="Chat card view Logo" width="340" />

Beim Tippen auf die Karte ist die immersive Ansicht wie folgt.

<img src="SharepointAnnouncementImages/2.png" alt="immersive view Logo" width="180" />

Dieses Szenario kann grob in zwei Schritte unterteilt werden:
1. Erstellen einer Ankündigungsliste mit Spalten-Titel, Anlagen und Ansagetext (Beschreibung) 

    > Hinweis: Rich-Text wird nicht von einer Vorankündigungs Karte unterstützt. Deaktivieren Sie Rich-Text für SharePoint-Kolumnen mit dem Ankündigungstext (Beschreibung) beim Erstellen dieser Spalte.

    <img src="SharepointAnnouncementImages/3.5.png" width="200" />

2. Konfigurieren Sie Flow so, dass bei der Erstellung eines neuen Elements oder eines vorhandenen Elements in der Ankündigungsliste eine Out-of-Box-Ansage Karte an eine Kaizala-Gruppe gesendet wird.

    <img src="SharepointAnnouncementImages/3.png" alt="Sharepoint&Flow Logo" width="400" />

## <a name="implementation-steps"></a>Implementierungsschritte


1. [Hinzufügen](https://docs.microsoft.com/en-us/sharepoint/administration/add-apps-for-sharepoint-to-a-sharepoint-site) einer Ankündigungs-App zur SharePoint-Website (siehe*unten*)
     1. Klicken Sie auf das Symbol "Einstellungen"
     2.  Klicken Sie auf app hinzufügen. 
     3.  Wählen Sie Ansage-App aus der Liste der verfügbaren Apps aus.
2. Verwenden des [hervorgehobenen Inhalts](https://support.office.com/en-us/article/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd) Webparts (*Falls erforderlich, zur Visualisierung*)
3. Laden Sie die [SharepointAnnouncementOnKaizala-SolutionPackage. zip](https://aka.ms/SharepointAnnouncementOnKaizala-SolutionPackage.zip) (*Dies ist ein Flow-Paket*)
4. [Importieren](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) SharepointAnnouncementOnKaizala-SolutionPackage. zip zu Ihrem Microsoft Flow-Konto
   
   > Hinweis: Wenn Sie die SharePoint-oder Kaizala-Verbindung noch nie verwendet haben, fügen Sie zunächst [Verbindungen hinzu](https://docs.microsoft.com/en-us/flow/add-manage-connections) .
   
5. Bearbeiten des Flusses (nach*folgend*)
    1. Im ersten Block des Flusses
    
         1. Geben Sie die Websiteadresse ein.
         2. Geben Sie den Namen der Liste ein (*Schritte zum Abrufen des Listen namens ist wie folgt*)
            - Klicken Sie in der linken Ecke des Bildschirms auf die Registerkarte Websiteinhalte.
            - Wählen Sie die Ankündigungsliste aus, an die Sie Ankündigungen an Kaizala senden möchten.
            - Klicken Sie auf das Symbol "Einstellungen" in der oberen rechten Ecke des Bildschirms.
            - Wechseln zu Listeneinstellungen
            - Kopieren Sie die URL der Liste aus dem Browser.
            - DeCodieren Sie die URL (Sie können die URL [hier](https://www.url-encode-decode.com/) decodieren)
        <img src="SharepointAnnouncementImages/4.PNG" alt="" width="500" />
      
    2. Im zweiten Block des Flusses
   
        Ordnen Sie das Feld Wert mit dem Spaltentitel der Ankündigungsliste zu, der den Text der Ansage (Beschreibung) aus dem dynamischen Inhalt enthält. Im folgenden Beispiel lautet der Spaltentitel "Ansagetext". <img src="SharepointAnnouncementImages/5.png" alt="" width="600" />
       
    3. Im letzten Block des Flusses
    
       Wählen Sie den Gruppennamen aus Dropdown aus. In diesem Beispiel lautet "jeder @ Fabrikam"
       <img src="SharepointAnnouncementImages/6.png" alt="" width="450" />
6. Speichern des Flusses

Die Ansage wird an die ausgewählte Kaizala-Gruppe gesendet, und jeder Zeitablauf wird ausgelöst.

> Hinweis: Textdatei wird als Anlage nicht unterstützt
