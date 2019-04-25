# <a name="customer-ticketing-solution-on-kaizala"></a>Kundenticket Lösung auf Kaizala
![](Images/Customer%20ticketing%20solution.PNG)
<br>
<br> Hier erfahren Sie, wie Sie ein Kundensupport-Ticket Verwaltungssystem auf Kaizala erhalten. Anstatt mehrere Textnachrichten zu senden, um eine Aktualisierung des Ticket Status zu erhalten, können wir nur eine Rich-Card haben, die den Status des Tickets bereitstellt. Bei einer Änderung des Status kann die Karte entsprechend dem aktuellen Status aktualisiert werden.
<br><br>Um dies zu erreichen, sind die folgenden Schritte erforderlich:
<br>1. Erstellen einer Karte mit benutzerdefinierter chatkarte basierend auf definierten Eigenschaften
<br>2. Aufrufen einer API zum Senden der Karte (Szenario, in dem Ticket ausgelöst wird)
<br>3. Aufrufen einer API zum Aktualisieren der Karte (Szenario, in dem sich der Ticket Status ändert)
## <a name="building-card-with-custom-chat-card-view"></a>Gebäude Karte mit benutzerdefinierter Chat Kartenansicht
[Kaizala ermöglicht das Erweitern der clientseitigen Funktionalität mithilfe von benutzerdefinierten Aktionen/Karten. Die Microsoft-Dokumentation zum Entwickeln einer benutzerdefinierten Aktion finden Sie [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/develop.md).]
<br><br>Zum Erstellen einer Karte mit benutzerdefinierter Chat Karte müssen wir die sourceLocation der Ansicht der Chat Leinwand Karte in Package. JSON definieren. Im Gegensatz zur Antwort Ansicht, Erstellungsansicht oder Ergebnis-/Zusammenfassungsansicht, die auf HTML/JS basiert, nimmt die Chat Karte ein deklaratives Schema [mehr darüber [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/ChatCanvasCardView.md)].
### <a name="packagejson"></a>Package. JSON
{  <br>"ID": "com. GLS. xyz. Care", <br>"schemaVersion": 1, <br>"displayName": "Kunden Support", <br>"providerName": "GLS-Test", <br>"Icon": "AppIcon. png", <br>"Version": "1", <br>"minorVersion": "1", <br>"appModel": "AppModel. JSON", <br>"Description": "Paket zum Senden eines Kunden Tickets [Test]", <br>"Dials": { <br>"isLocalized": false, <br>"isAngeheftet": falsch <br>},  <br>"Views": { <br>"ChatCanvasCardView": { <br>"sourceLocation": "ChatCardView. JSON", <br>"showReceipts": true, <br>"showLikes": false, <br>"showComments": false, <br>"showExpiry": false, <br>"showFooter": true, <br>"Zeilenbereich": false, <br>"showFooter": false, <br>"isResponseEditable": falsch <br>}
<br> }
<br>}
### <a name="chatcardviewjson"></a>ChatCardView. JSON
Die Chat Karte hat vier Felder: eine, die auf "XYZ CUSTOMER CARE" fest codiert ist, und die anderen 3 Felder, die von Eigenschaften gespeist werden: CustomerName, ticketnumber und Ticketstatus.
<br>{
<br> "schemaVersion": 2, <br>"Schema": {
<br> "Type": "Container",
<br> "initialHeight": 300,
<br> "Layout": "vertikal",
<br> "Children": [
<br> {  <br>"Typ": "Text", <br>"paddingLeft": 10, <br>"paddingRight": 10,
<br> "paddingTop": 10,
<br> "paddingBottom": 10,
<br> "String": "XYZ-Kundendienst",
<br> "fontSize": 18,
<br> "fontStyle": "Bold",
<br> "TextColor": "#ffffff",
<br> "Background Color": "#fcb72d",
<br> "textAlignment": "Center",
<br> "maxNumberOfLines": 1,
<br> "marginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "paddingLeft": 10,
<br> "paddingRight": 10,
<br> "String": "$ {Form. Properties [Kundenname]. Value}",
<br> "fontSize": 18,
<br> "fontStyle": "Regular",
<br> "TextColor": "#000000",
<br> "Background Color": "#ffffff",
<br> "textAlignment": "Left",
<br> "maxNumberOfLines": 5,
<br> "marginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "paddingLeft": 10,
<br> "paddingRight": 10,
<br> "String": "$ {Form. Properties [ticketnumber]. Value}",
<br> "fontSize": 18,
<br> "fontStyle": "Regular",
<br> "TextColor": "#000000",
<br> "Background Color": "#ffffff",
<br> "textAlignment": "Left",
<br> "maxNumberOfLines": 2,
<br> "marginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "paddingLeft": 10,
<br> "paddingRight": 10,
<br> "String": "$ {Form. Properties [Ticketstatus]. Value}",
<br> "fontSize": 18,
<br> "fontStyle": "Regular",
<br> "TextColor": "#000000",
<br> "Background Color": "#ffffff",
<br> "textAlignment": "Left",
<br> "maxNumberOfLines": 2,
<br> "marginBottom": 10
<br> }
<br> ]
<br> }
<br>}
### <a name="appmodeljson"></a>AppModel. JSON
Erstellen Sie einfach ein AppModel-Array mit den Themen Title und Empty Questions.
<br> {
<br> "Title": "XYZ-Kunden Support",
<br> "Fragen": []
<br>}
## <a name="sending-ticket-from-api"></a>Senden von Tickets von der API
Um das Ticket über die API zu senden, verwenden wir den Endpunkt "Aktionen" wie unten gezeigt. Beachten Sie das subscribers-Array – da wir dieses Ziel an den jeweiligen Teilnehmer senden müssen (Weitere Informationen finden Sie in den Post- [Move-SMS-Benachrichtigungen an Kaizala](https://kaizala007.wordpress.com/2018/02/07/kaizala-subscriber-message/)).
<br>Beim Ausführen dieser API würden Sie die Referenz-und Aktions-Nr. Cachen Sie diese Aktions-Nr, wie wir Sie im nächsten Schritt benötigen. Im folgenden Beispiel haben wir die Eigenschaften CustomerName, ticketnumber und Ticketstatus auf "NAME: John Thomas", "TICKET #: 907050", "STATUS: ACTIVE" festgelegt.

| Methode  |      POST    |
|----------|-------------|
|**URL**|{{Endpunkt-URL}}/v1/Groups/{{Test-Group-ID}}/Actions|
|**AnforderungsText**|{<br>ID: "com. GLS. xyz. Care",<br>Abonnenten: ["{{Subscriber-Mobile-Number}}"],<br>sendToAllSubscribers: false,<br>actionBody: {<br>Eigenschaften: [<br>{<br>Name: "CustomerName",<br>Wert: "NAME: John Thomas",<br>Typ: "Text"<br>},<br>{<br>Name: "ticketnumber",<br>Wert: "TICKET #: 907050",<br>Typ: "Text"<br>},<br>{<br>Name: "Ticketstatus",<br>Wert: "STATUS: ACTIVE",<br>Typ: "Text"<br>}<br>]<br>}<br>}|
## <a name="updating-the-ticket-status-using-api"></a>Aktualisieren des Ticket Status mithilfe der API
Wenn sich der Ticket Status ändert, müssen wir den Status der gesendeten Karte aktualisieren. Dafür verwenden wir den Endpunkt Actions/<<action-id>>/Properties. Im folgenden Beispiel wird der Ticket Status auf "AUFGELÖST" aktualisiert. Beachten Sie, dass die Aktions Kennung die ID der im vorherigen Schritt gesendeten Aktion ist.

| Method  |      PPUT    |
|----------|-------------|
|**URL**|{{Endpunkt-URL}}/v1/groups/{{test-group-id}}/actions/{{actionId}}|
|**AnforderungsText**|{<br>{<br>"Version":-1,<br>"updateProperties":<br>[<br>{<br>"Name": "Ticketstatus",<br>"Typ": "Text",<br>"Wert": "STATUS: AUFGELÖST"<br>}<br>]<br>}|

## <a name="screenshots-of-the-demo"></a>Screenshots der Demo
### <a name="ticket-sent-from-api"></a>Von der API gesendetes Ticket
![](Images/Ticket%20sent%20from%20API.PNG)
### <a name="ticket-after-updating-the-status-from-api"></a>Ticket nach der Aktualisierung des Status von der API
![](Images/Ticket%20after%20updating%20the%20status%20from%20API.PNG)
<br>Teilen Sie das Paket [hier](https://drive.google.com/file/d/1gQb1CpYVd8SLnOOH4PCZWPsUeYhdWehB/view), falls Sie es einen Versuch geben möchten. (vergessen Sie nicht, die Paket-ID vor dem Hochladen in Kaizala zu ändern, um Konflikte zu vermeiden).

















