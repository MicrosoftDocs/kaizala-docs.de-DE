# <a name="customer-ticketing-solution-on-kaizala"></a>Kunden, die Lösung auf Kaizala Tickets
![](Images/Customer%20ticketing%20solution.PNG)
<br>
<br> Verwenden Sie in diesem, wollen wir uns zum Abrufen eines Kunden Ticket Managementsystem auf Kaizala unterstützen. Anstelle von mehreren Textnachrichten an geben Sie ein Update auf dem Ticket Status senden, konnten wir nur eine rich installiert sein, die den Status Ticket bereitstellt. Und wenn eine Änderung im Status vorhanden ist, konnte die Karte entsprechend den aktuellen Status aktualisiert werden.
<br><br>Um dies zu erreichen, sehen Sie die Schritte, die erforderlich wäre unter:
<br>1. erstellen Sie eine Karte mit benutzerdefinierten Chat Karte basierend auf definierten Eigenschaften
<br>2. Aufrufen einer API zum Senden von der Karte (Szenario, in dem Ticket ausgelöst wird)
<br>3. einen Aufruf an eine API zum Aktualisieren der Karte (Szenario, in dem Ticket Status ändert sich)
## <a name="building-card-with-custom-chat-card-view"></a>Erstellen von Karte mit benutzerdefinierten Chat Kartenansicht
[Kaizala ermöglicht das clientseitige Erweiterung mit benutzerdefinierten Aktionen Funktionen / Karten. Microsoft-Dokumentation für das Entwickeln einer benutzerdefinierten Aktion finden Sie [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/develop.md).]
<br><br>Zum Erstellen von Karten mit benutzerdefinierten Chat Karte, müssen wir die SourceLocation der Chat Zeichenbereich Kartenansicht in package.json definieren. Im Gegensatz zu der Antwort-Ansicht, Erstellung Ansicht oder Ergebnisse / Zusammenfassungsansicht – sind html / JS basiert, die Karte Chat wird eine deklarative Schema [mehr darüber [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/ChatCanvasCardView.md)].
### <a name="packagejson"></a>package.json
{  <br>"Id": "com.gls.xyz.care", <br>"SchemaVersion": 1; <br>"DisplayName": "Customer Support" <br>"ProviderName": "GLS-Test" <br>"Symbol": "AppIcon.png", <br>"Version": "1" <br>"MinorVersion": "1" <br>"AppModel": "AppModel.json", <br>"Beschreibung": "Paket für das Senden von Kunden Ticket [Test]" <br>"wählt": { <br>"IsLocalised": false <br>"IsPinned": false <br>},  <br>"Ansichten": { <br>"ChatCanvasCardView": { <br>"SourceLocation": "ChatCardView.json", <br>"ShowReceipts": "true" <br>"ShowLikes": false <br>"ShowComments": false <br>"ShowExpiry": false <br>"ShowFooter": "true" <br>"ShowHeader": false <br>"ShowFooter": false <br>"IsResponseEditable": false <br>}
<br> }
<br>}
### <a name="chatcardviewjson"></a>ChatCardView.json
Die Chat-Karte verfügt über vier Felder: eine hartcodiert und auf "Kundenbetreuung XYZ" und die anderen 3 Felder aus Eigenschaften zugeführt: Customername, Ticketnumber und Ticketstatus.
<br>{
<br> "SchemaVersion": 2, <br>"Schema": {
<br> "Typ": "Container",
<br> "InitialHeight": 300,
<br> "Layout": "vertical"
<br> "Children": [
<br> {  <br>"Typ": "Text", <br>"PaddingLeft": 10; <br>"PaddingRight": 10;
<br> "PaddingTop": 10;
<br> "PaddingBottom": 10;
<br> "String": "XYZ Kundenbetreuung"
<br> "FontSize": 18;
<br> "FontStyle": "Fett"
<br> "TextColor": "#ffffff",
<br> "BackgroundColor": "#fcb72d",
<br> "TextAlignment": "zentrieren",
<br> "MaxNumberOfLines": 1;
<br> "MarginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "PaddingLeft": 10;
<br> "PaddingRight": 10;
<br> "string":"${Form.properties[customername].value}"
<br> "FontSize": 18;
<br> "FontStyle": "Normal"
<br> "TextColor": "#000000",
<br> "BackgroundColor": "#ffffff",
<br> "TextAlignment": "left",
<br> "MaxNumberOfLines": 5,
<br> "MarginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "PaddingLeft": 10;
<br> "PaddingRight": 10;
<br> "string":"${Form.properties[ticketnumber].value}"
<br> "FontSize": 18;
<br> "FontStyle": "Normal"
<br> "TextColor": "#000000",
<br> "BackgroundColor": "#ffffff",
<br> "TextAlignment": "left",
<br> "MaxNumberOfLines": 2,
<br> "MarginBottom": 10
<br> },
<br> {
<br> "Typ": "Text",
<br> "PaddingLeft": 10;
<br> "PaddingRight": 10;
<br> "string":"${Form.properties[ticketstatus].value}"
<br> "FontSize": 18;
<br> "FontStyle": "Normal"
<br> "TextColor": "#000000",
<br> "BackgroundColor": "#ffffff",
<br> "TextAlignment": "left",
<br> "MaxNumberOfLines": 2,
<br> "MarginBottom": 10
<br> }
<br> ]
<br> }
<br>}
### <a name="appmodeljson"></a>AppModel.json
Erstellen Sie einfach eine AppModel mit dem Titel und leere Fragen Array.
<br> {
<br> "Title": "XYZ Customer Support"
<br> "Fragen":]
<br>}
## <a name="sending-ticket-from-api"></a>Senden von Ticket von API
Damit das Ticket über API gesendet werden, würde den Endpunkt Aktionen wie folgt verwenden. Beachten Sie das Abonnenten-Array – da wir diese gezielt an bestimmten Abonnenten senden müssen (für Weitere Informationen finden Sie im Beitrag [zu Kaizala verschieben SMS-Benachrichtigungen](https://kaizala007.wordpress.com/2018/02/07/kaizala-subscriber-message/)verweisen).
<br>Diese API ausführen würden Sie die ReferenceId und ActionId fest. Nutzen Sie diese ActionId wie wir im nächsten Schritt noch benötigt wird. In der unten Beispiel haben wir Kundenname, Eigenschaften Ticketnumber und Ticketstatus auf "NAME: John Thomas" festzulegen "TICKET #: 907050", "STATUS: aktiv" fest.

| Methode  |      Bereitstellen    |
|----------|-------------|
|**URL**|{{Endpunkt-Url}} / v1/Gruppen / {{Test-Gruppen-Id}} / Aktionen|
|**Anforderungstext**|{<br>ID:"com.GLS.xyz.Care",<br>Abonnenten: ["{{-Mobile-Teilnehmernummer}}"],<br>SendToAllSubscribers:false,<br>ActionBody: {<br>Eigenschaften: [<br>{<br>Name: "Customername",<br>Wert: "NAME: John Thomas",<br>Typ: "Text"<br>},<br>{<br>Name: "Ticketnumber",<br>Wert: "TICKET #: 907050″,<br>Typ: "Text"<br>},<br>{<br>Name: "Ticketstatus",<br>Wert: "STATUS: aktiv",<br>Typ: "Text"<br>}<br>]<br>}<br>}|
## <a name="updating-the-ticket-status-using-api"></a>Aktualisieren des Ticket Status mithilfe der API
Wie der Ticket Status ändert, müssen wir den Status auf der Karte zu aktualisieren, die gesendet wurde. Für diese wir wäre die Verwendung der Aktionen / << Aktions-Id >> / Eigenschaften-Endpunkt. In dem folgenden Beispiel wir würden werden Aktualisieren des Ticket Status in gelöst. Beachten Sie, dass die ActionId die ID der Aktion, die in früheren Schritt gesendet wird.

| Methode  |      PPUT    |
|----------|-------------|
|**URL**|{{Endpunkt-Url}} / v1/Gruppen / {{Test-Gruppen-Id}} /actions/ {{ActionId}}|
|**Anforderungstext**|{<br>{<br>"Version": 1,<br>"UpdateProperties":<br>[<br>{<br>"Name": "Ticketstatus",<br>"Typ": "Text",<br>"Wert": "STATUS: AUFGELÖST"<br>}<br>]<br>}|

## <a name="screenshots-of-the-demo"></a>Screenshots der demo
### <a name="ticket-sent-from-api"></a>Ticket von API gesendet
![](Images/Ticket%20sent%20from%20API.PNG)
### <a name="ticket-after-updating-the-status-from-api"></a>Ticket nach dem Aktualisieren des Status von API
![](Images/Ticket%20after%20updating%20the%20status%20from%20API.PNG)
<br>Freigabe des Pakets über die [hier](https://drive.google.com/file/d/1gQb1CpYVd8SLnOOH4PCZWPsUeYhdWehB/view)für den Fall, dass er einer Aufnahme erhalten soll. (vergessen Sie nicht so ändern Sie die Paket-Id vor dem Hochladen auf Kaizala Konflikte zu vermeiden)

















