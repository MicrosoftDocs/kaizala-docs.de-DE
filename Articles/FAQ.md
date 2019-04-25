# <a name="frequently-asked-questions"></a>Häufig gestellte Fragen: 

## <a name="kaizala-rest-based-apis"></a>Kaizala-REST-basierte APIs

**1. Wie fange ich mit der Verwendung von Kaizala-APIs an?**</br></br>
Um mit der Verwendung der REST-basierten API von Kaizala zu beginnen, müssen Sie
 
-   [Richten Sie zuerst Kaizala-Connector ein, und generieren Sie ein Aktualisierungs Token](https://docs.microsoft.com/en-in/kaizala/connectors/setup).
-   Als nächstes müssen Sie [Zugriffs Token generieren](https://docs.microsoft.com/en-in/kaizala/connectors/tokens) .
-   und starten Sie dann [mit APIs](https://docs.microsoft.com/en-in/kaizala/connectors/api)

<br/>

**2. Programmgesteuertes Generieren von Aktualisierungstoken**</br></br>
  Es gibt zwei Arten von Aktualisierungs Token.
  - Benutzer Token
  - Gruppen Token
  
  **Benutzer Token** kann mithilfe einer (a) Connectors-Detailseite im Kaizala-Verwaltungsportal (b) mithilfe der API (GeneratePin und LoginWithPinAndApplicationId-API (Details in der [hier](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=) freigegebenen Postman-Sammlung) (c) Kaizala oAuth generiert werden. <br/>
  **Gruppen Token** kann mithilfe der Konnektor-Detailseite im Kaizala-Verwaltungsportal generiert werden.

Weitere Informationen zu [Token](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)
<br/><br/>

**3. wie stelle ich sicher, dass das Ablaufdatum von refreshToken die Verbindung zwischen Kaizala und meinem System/App nicht beendet**</br></br>
 Im Allgemeinen wird das Aktualisierungs Token nach 365 Tagen ablaufen. Damit Drittanbietersysteme die Verbindung auch dann beibehalten können, wenn refreshToken demnächst abläuft, sendet Kaizala ein neues Aktualisierungstoken mit allen Zugriffstoken-aufrufen, da 90% der Gültigkeit des Aktualisierungs Tokens erreicht ist. Daher sollte System in der Lage sein, diese refreshToken zu lesen und diese refreshToken für nachfolgende accessTokens zu verwenden. [Weitere Informationen](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)

**4. wie erstelle ich eine Gruppe mithilfe der API?**</br></br>
  Kaizala ermöglicht das Erstellen von Gruppen & Untergruppen mithilfe von APIs. Lesen Sie mehr, um [eine Gruppe zu erstellen](https://docs.microsoft.com/en-in/kaizala/connectors/groups). 
  >Hinweis: Wenn Sie das Aktualisierungs Token auf Benutzerebene verwenden, wird eine neue Gruppe erstellt. Wenn zum Erstellen einer Gruppe jedoch ein Gruppenstufen Token verwendet wird, wird eine Untergruppe für die betroffene Gruppe erstellt.
<br/><br/>

**5. wie kann ich eine Nachricht über APIs in Kaizala senden?**</br></br>
  Kaizala macht eine API verfügbar, mit der Sie eine Nachricht an eine beliebige Gruppe senden können. Weitere Informationen [finden Sie hier](https://docs.microsoft.com/en-gb/kaizala/connectors/messages).
<br/><br/>


**6. gibt es Beispiel Online für verschiedene Kaizala-Features wie APIs, webhooks?**</br></br>
  Den Beispielcode finden Sie [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx) in C#.

**7. wie erhalte ich die Telefonnummern aller Mitglieder/Teilnehmer in einer Gruppe?**</br></br>
  Kaizala macht API verfügbar, um die Details aller Mitglieder in einer Gruppe abzurufen. Weitere Details [hier](https://docs.microsoft.com/en-gb/kaizala/connectors/members) um Informationen zu den Gruppenmitgliedern zu erhalten, müssen Sie die Kaizala-Connectors einrichten. [Weitere Informationen](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/connectors/README.md) 
<br/><br/>


**8. wie können wir ein Mitglied über Kaizala-APIs zu einer Gruppe hinzufügen?**</br></br>
  Kaizala macht API verfügbar, um Mitglieder in einer Gruppe hinzuzufügen. Weitere Informationen [finden Sie hier](https://docs.microsoft.com/en-gb/kaizala/connectors/members).     Wenn Sie ein Gruppenmitglied zu einem Administrator machen möchten, finden Sie unter Beispiel: 
````  
PUT {endpoint-url}/v1/groups/{groupId}/members/{memberId} 

Header: 
accessToken 

Body 
{"role":"Admin"} 
````

**9. ist es möglich, einen webhook zu erstellen, der bei der Gruppenerstellung benachrichtigt werden kann?**</br></br>
  Es ist nicht möglich, einen webhook zum Abrufen von Benachrichtigungen zu Gruppen Kreationen zu erstellen, da alle webhooks derzeit innerhalb des Kontexts einer Gruppe ausgeführt werden. Im Kontext einer Gruppe können Sie webhooks erstellen, um Benachrichtigungen zu Nachrichten/Aktionen zu erhalten, die gesendet/empfangen wurden, hinzufügen und Löschen von Mitgliedern usw.  
<br/><br/>

**10. müssen Connectors manuell zu jeder Gruppe hinzugefügt werden?**</br></br>
  Wenn der Connector über den MandantenAdministrator erstellt wird, müssen Sie den Connector nicht jeder Gruppe manuell hinzufügen. 
<br/><br/>


**11. wie kann ich vollständige Antworten aller Teilnehmer an einer Umfrage abrufen?**</br></br>
Verwenden Sie die folgende API, um alle Antworten für eine bestimmte Umfrage in einer Gruppe abzurufen:
````
{{endpoint-url}}/v1/groups/{{group-id}}/actions/{{survey-id}}?getDetails=true 
 
Headers: 
accessToken : {{access-token}} 
```` 
<br/><br/>

**12. kann ich eine Nachricht in einer 1-1-Unterhaltung in Kaizala über APIs senden?**</br></br>  Alle APIs in Kaizala funktionieren innerhalb des Kontexts einer Gruppe. Daher ist es nicht möglich, eine Nachricht in einer 1-1-Unterhaltung mithilfe einer API zu senden. Folgende Funktionen werden unterstützt:
-   Senden von Nachrichten an einen bestimmten Teilnehmer in einer öffentlichen Gruppe 
-   Erstellen einer Gruppe mit dem Benutzer und Senden einer Nachricht an die Gruppe

<br/>
    
**13. ist es möglich, eine Nachricht nur an bestimmte Mitglieder in einer Gruppe zu senden?**</br></br>
  Nur bei einer öffentlichen Gruppe ist es möglich, eine Nachricht an einen bestimmten Teilnehmer zu senden. In einer normalen Gruppe ist dies nicht möglich. Weitere Informationen zur zugehörigen API finden Sie unter dem folgenden Link: https://docs.microsoft.com/en-gb/kaizala/connectors/messages. <br/>
<br/><br/>

**14. ist es möglich, eine Nachricht nur an bestimmte Mitglieder in einer Gruppe zu senden?**</br></br>
  Alle APIs in Kaizala funktionieren innerhalb des Kontexts einer Gruppe. Daher ist es nicht möglich, eine Aktion in einer 1-1-Unterhaltung mithilfe einer API zu senden.  
<br/><br/>

## <a name="kaizala-actions"></a>Kaizala-Aktionen

**1. wie kann ich mit der Entwicklung von benutzerdefinierten Aktionen beginnen? Ist eine Dokumentation verfügbar?**</br></br>
  Die Entwicklung von benutzerdefinierten Aktionen und die dazugehörige Dokumentation finden Sie unter NDA. Sie können mit [dieser](Actions/README.md)Lektüre beginnen. </br>
  Falls Sie Fragen haben, können Sie [uns kontaktieren](feedback.md).
<br/><br/>

**2. wie erhalte ich das neueste Kaizala Action SDK?**</br></br>

  Das neueste Action SDK finden Sie [hier]() .
<br/><br/> 

 **3. wie kann ich eine benutzerdefinierte Aktion testen/Debuggen, ohne jedes Mal ein Paket hochladen zu müssen?**</br></br>

  Um eine benutzerdefinierte Aktion zu testen, lesen Sie mehr über die Schritte/Prozess [hier](Actions/test.md) 
<br/><br/>


 **4. Was sind Richtlinien, denen das Aktionspaket folgen muss?**</br></br>
Als Entwickler müssen Sie die Richtlinien einhalten, während Sie ein benutzerdefiniertes Aktionspaket entwickeln. finden Sie diese [hier](Actions/validation.md). Microsoft Kaizala kann Ihre Aktion aus der APP entfernen, wenn Sie Inkonsistenzen feststellt.
<br/><br/>

**5. wo kann ich auf die Berichte zugreifen, die meinen benutzerdefinierten Aktionen im Kaizala-Verwaltungs Portal entsprechen?**</br></br>
 Kaizala-Verwaltungs Portal ermöglicht Benutzern das Erstellen benutzerdefinierter Aktionen, Formulare, Feedback Karten usw. Solche Aktionen können dann Ihren Gruppen zugeordnet und wiederholt gesendet werden, um wichtige geschäftliche Metriken nachzuverfolgen. Im Portal werden diese Daten unter "wiederkehrende Umfrageberichte" angezeigt. Als zusätzliches Feature aggregiert der Bericht Antworten auf diese Karten im Laufe der Zeit und über Instanzen hinweg. 
<br/><br/>

**6. wie kann ich externe Inhalte in meine Aktionsseite laden?**</br></br>
Sie können externe Inhalte in Ihre Aktion laden, indem Sie die URL, die die Daten enthält, in der Whitelist auflisten. [Hier](Actions/UrlWhitelisting.md)finden Sie die Schritte zur URL-Whitelist.
<br/><br/>

## <a name="integration-with-microsoft-apps"></a>Integration in Microsoft-apps

**1. wie kann ein Kaizala-Konnektor in PowerApps erstellt werden?**</br></br>
  Microsoft Kaizala wurde als Connector auf Microsoft Flow & PowerApps veröffentlicht. Weitere Informationen [finden Sie hier](https://support.office.com/en-us/article/Integrate-your-workflow-in-Kaizala-using-Microsoft-Flow-883343d0-6b16-4725-a23d-bc69fb264356)
<br/><br/>

**2. wie kann ich das Excel-Add-in für Kaizala hinzufügen und verwenden?**</br></br>

  Das Excel-Add-in für Kaizala ermöglicht, dass jede Tabelle in Excel als Umfrage auf Kaizala verfügbar gemacht wird. Alle Antworten auf die Umfrage werden automatisch in der Excel-Tabelle ausgefüllt. Weitere Informationen [finden Sie hier](https://support.office.com/en-us/article/Kaizala-Office-Add-in-4cd01439-5da2-4a9f-b493-8f2e23e2fd91?ui=en-US&rs=en-US&ad=US) 

<br/><br/> 



