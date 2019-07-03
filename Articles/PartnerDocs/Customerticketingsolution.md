# <a name="customer-ticketing-solution-on-kaizala"></a>Kundenkarten Lösung auf Kaizala
![](Images/Customer%20ticketing%20solution.PNG)
<br>
<br> Lassen Sie uns hier untersuchen, wie Sie ein Ticket Verwaltungssystem für Kundensupport auf Kaizala erhalten. Anstatt mehrere Textnachrichten zu senden, um eine Aktualisierung des Ticket Status zu erhalten, hätten wir nur eine umfangreiche Karte, die den Ticket Status bereitstellt. Wenn sich der Status geändert hat, kann die Karte aktualisiert werden, um den aktuellen Status anzuzeigen.
<br><br>Um dies zu erreichen, sind die folgenden Schritte erforderlich:
<br>1. Erstellen einer Karte mit benutzerdefinierten Chat Karten basierend auf definierten Eigenschaften
<br>2. Rufen Sie eine API auf, um die Karte zu senden (Szenario, in dem das Ticket ausgelöst wird).
<br>3. Aufrufen einer API zum Aktualisieren der Karte (Szenario, in dem sich der Ticket Status ändert)
## <a name="building-card-with-custom-chat-card-view"></a>Erstellen einer Karte mit benutzerdefinierter Chat Kartenansicht
[Kaizala ermöglicht das Erweitern der clientseitigen Funktionalität mithilfe benutzerdefinierter Aktionen/Karten. Die Microsoft-Dokumentation zum Entwickeln einer benutzerdefinierten Aktion finden Sie [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/develop.md).]
<br><br>Für das Erstellen einer Karte mit benutzerdefinierter chatkarte müssen wir die SourceLocation der Chat Ansichtskarten Ansicht in Paket. JSON definieren. Im Gegensatz zur Antwort Ansicht, zur Erstellungsansicht oder zur Ergebnis-/Zusammenfassungsansicht, die auf HTML/js basiert, nimmt die Chat Karte ein deklaratives Schema [mehr dazu [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/ChatCanvasCardView.md)] an.
### <a name="packagejson"></a>Package. JSON
{  <br>"ID": "com. GLS. xyz. Care", <br>"Schemaversion": 1, <br>"DisplayName": "Kunden Support", <br>"ProviderName": "GLS-Test", <br>"Icon": "AppIcon. png", <br>"Version": "1", <br>"MinorVersion": "1", <br>"appModel": "appModel. JSON", <br>"Description": "Paket zum Senden des Kunden Tickets [Test]", <br>"Dials": { <br>"islocaled": false, <br>"isangeheftet": false <br>},  <br>"Views": { <br>"ChatCanvasCardView": { <br>"SourceLocation": "ChatCardView. JSON", <br>"showReceipts": true, <br>"showLikes": false, <br>"showComments": false, <br>"showExpiry": false, <br>"showFooter": true, <br>"Zeilenbereich": false, <br>"showFooter": false, <br>"isResponseEditable": false <br>}
<br> }
<br>}
### <a name="chatcardviewjson"></a>ChatCardView. JSON
Die chatkarte verfügt hier über vier Felder: eine hart codierte "XYZ-Kundenbetreuung" und die anderen 3 Felder, die von den Eigenschaften gefüttert werden: Kundennamen, ticketnumber und Ticketstatus.
<br>{
<br> "Schemaversion": 2, <br>"Schema": {
<br> "Typ": "Container",
<br> "initialHeight": 300,
<br> "Layout": "vertikal",
<br> "Children": [
<br> {  <br>"Typ": "Text", <br>"PaddingLeft": 10, <br>"PaddingRight": 10,
<br> "PaddingTop": 10,
<br> "PaddingBottom": 10,
<br> "String": "XYZ-Kundenbetreuung",
<br> "FontSize": 18,
<br> "FontStyle": "Fett",
<br> "TextColor": "#FFFFFF",
<br> "Background Color": "#fcb72d",
<br> "TextAlignment": "Center",
<br> "maxNumberOfLines": 1,
<br> "MarginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "PaddingLeft": 10,
<br> "PaddingRight": 10,
<br> "String": "$ {Form. Properties [Kundenname]. Value}",
<br> "FontSize": 18,
<br> "FontStyle": "Regular",
<br> "TextColor": "#000000",
<br> "Background Color": "#FFFFFF",
<br> "TextAlignment": "Left",
<br> "maxNumberOfLines": 5,
<br> "MarginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "PaddingLeft": 10,
<br> "PaddingRight": 10,
<br> "String": "$ {Form. Properties [ticketnumber]. Value}",
<br> "FontSize": 18,
<br> "FontStyle": "Regular",
<br> "TextColor": "#000000",
<br> "Background Color": "#FFFFFF",
<br> "TextAlignment": "Left",
<br> "maxNumberOfLines": 2,
<br> "MarginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "PaddingLeft": 10,
<br> "PaddingRight": 10,
<br> "String": "$ {Form. Properties [Ticketstatus]. Value}",
<br> "FontSize": 18,
<br> "FontStyle": "Regular",
<br> "TextColor": "#000000",
<br> "Background Color": "#FFFFFF",
<br> "TextAlignment": "Left",
<br> "maxNumberOfLines": 2,
<br> "MarginBottom": 10
<br> }
<br> ]
<br> }
<br>}
### <a name="appmodeljson"></a>AppModel. JSON
Erstellen Sie einfach ein AppModel mit dem Titel und dem leeren Questions-Array.
<br> {
<br> "Title": "XYZ-Kunden Support",
<br> "Questions": []
<br>}
## <a name="sending-ticket-from-api"></a>Senden von Tickets von API
Um das Ticket über API zu senden, verwenden wir den Actions-Endpunkt wie unten dargestellt. Beachten Sie das Abonnenten-Array – da wir dieses Ziel an den jeweiligen Abonnenten senden müssen (Weitere Informationen finden Sie unter Post- [SMS-Benachrichtigungen an Kaizala](https://kaizala007.wordpress.com/2018/02/07/kaizala-subscriber-message/)).
<br>Durch die Ausführung dieser API erhalten Sie die Referenz-und die Aktions-Nr. Diese Aktions-Nr Zwischenspeichern, wie wir Sie im nächsten Schritt benötigen werden. Im folgenden Beispiel haben wir die Eigenschaften CustomerName, ticketnumber und Ticketstatus auf "Name: John Thomas", "Ticket #: 907050", "Status: Active", festgelegt.

| Methode  |      POST    |
|----------|-------------|
|**URL**|{{Endpunkt-URL}}/v1/Groups/{{Test-Group-ID}}/Actions|
|**Anforderungstext**|{<br>ID: "com. GLS. xyz. Care",<br>Abonnenten: ["{{subscribe-Mobile-Number}}"],<br>sendToAllSubscribers: false,<br>actionBody:{<br>Properties: [<br>{<br>Name: "CustomerName",<br>Wert: "Name: John Thomas",<br>Typ: "Text"<br>},<br>{<br>Name: "ticketnumber",<br>Wert: "Ticket #: 907050",<br>Typ: "Text"<br>},<br>{<br>Name: "Ticketstatus",<br>Wert: "Status: aktiv",<br>Typ: "Text"<br>}<br>]<br>}<br>}|
## <a name="updating-the-ticket-status-using-api"></a>Aktualisieren des Ticket Status mithilfe der API
Wenn sich der Ticket Status ändert, müssen wir den Status auf der Karte aktualisieren, die gesendet wurde. Dafür verwenden wir die Aktionen/<<Action-ID>>/Properties-Endpunkt. Im folgenden Beispiel wird der Ticket Status auf aufgelöst aktualisiert. Beachten Sie, dass die Aktions-ID die ID der Aktion ist, die im vorherigen Schritt gesendet wurde.

| Methode  |      PUT    |
|----------|-------------|
|**URL**|{{Endpunkt-URL}}/v1/Groups/{{Test-Group-ID}}/Actions/{{actionId}}|
|**Anforderungstext**|{<br>{<br>"Version":-1,<br>"updateProperties":<br>[<br>{<br>"Name": "Ticketstatus",<br>"Typ": "Text",<br>"Wert": "Status: aufgelöst"<br>}<br>]<br>}|

## <a name="screenshots-of-the-demo"></a>Screenshots der Demo
### <a name="ticket-sent-from-api"></a>Von API gesendetes Ticket
![](Images/Ticket%20sent%20from%20API.PNG)
### <a name="ticket-after-updating-the-status-from-api"></a>Ticket nach Aktualisierung des Status von API
![](Images/Ticket%20after%20updating%20the%20status%20from%20API.PNG)
<br>Das Paket wird [hier](https://drive.google.com/file/d/1gQb1CpYVd8SLnOOH4PCZWPsUeYhdWehB/view)freigegeben, falls Sie es versuchen möchten. (vergessen Sie nicht, die Paket-ID vor dem Hochladen in Kaizala zu ändern, um Konflikte zu vermeiden)

















