# <a name="frequently-asked-questions"></a>Häufig gestellte Fragen: 

## <a name="kaizala-rest-based-apis"></a>REST-basierte Kaizala-APIs

**1. wie fange ich mit Kaizala APIs?**</br></br>
Zum Starten Kaizalas REST-basierte API verwenden, müssen Sie
 
-   Erste [festlegen Kaizala Connector einrichten und zum Generieren von Token aktualisieren](https://docs.microsoft.com/en-in/kaizala/connectors/setup).
-   Als Nächstes müssen Sie [Access Token generieren](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)
-   und klicken Sie dann [mithilfe von APIs starten](https://docs.microsoft.com/en-in/kaizala/connectors/api)

<br/>

**2. wie programmgesteuert generiert Token aktualisieren?**</br></br>
  Es gibt zwei Arten von Token zu aktualisieren.
  - Benutzertoken
  - Gruppieren von Token
  
  **Benutzertoken** generiert werden mit Detailseite (a) Connectors in Kaizala-Verwaltungsportal, (b) Using-API (GeneratePin und LoginWithPinAndApplicationId api (Details im Postman Auflistung shared [hier](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=) ) (c) Kaizala oAuth. <br/>
  **Gruppe Token** können mit generiert werden Connectors Detailseite im Kaizala-Verwaltungsportal.

Weitere Informationen zu [Token](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)
<br/><br/>

**3. wie stellen Sie diese Ablauf sicher RefreshToken nicht beendet die Verbindung zwischen Kaizala und Meine System-app**</br></br>
 Läuft in der Regel nach 365 Tage Token zu aktualisieren. Damit können 3. Partei Systeme zur Aufrechterhaltung der Verbindungs, selbst wenn RefreshToken der Testzeitraum läuft, wird Kaizala sendet, die seit 90 % der Gültigkeit der Aktualisierung neue Refresh Token mit jedem Zugriff Token aufruft, Token erreicht. System sollte daher Lesen dieses RefreshToken und diese RefreshToken für nachfolgende AccessTokens verwenden können. [Erfahren Sie mehr](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)

**4. Wie erstelle ich eine Gruppe mithilfe der API?**</br></br>
  Kaizala Unterseite Gruppen von APIs & ermöglicht die Erstellung von Gruppen. Lesen Sie mehr zum [Erstellen einer Gruppe](https://docs.microsoft.com/en-in/kaizala/connectors/groups). 
  >Hinweis: Wenn Sie Benutzer Ebene aktualisieren Token verwenden, werden neue Gruppe erstellt werden. Aber wenn Gruppe Ebene Token zum Erstellen einer Gruppe verwendet wird, wird eine Untergruppe der betreffenden Gruppe erstellt.
<br/><br/>

**5. wie kann ich eine Nachricht über APIs in Kaizala senden?**</br></br>
  Kaizala macht eine API verwenden, die Sie eine Nachricht an eine beliebige Gruppe senden können. Hier erhalten Sie weitere [hier](https://docs.microsoft.com/en-gb/kaizala/connectors/messages).
<br/><br/>


**6. gibt es Beispiel verfügbar online für verschiedene Kaizala Features wie APIs, Webhooks?**</br></br>
  Finden Sie im Beispielcode in c# [hier](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)

**7. wie finde ich die Telefonnummern der alle Mitglieder/Abonnenten in einer Gruppe?**</br></br>
  Kaizala macht API, um die Details aller Elemente in einer Gruppe zu erhalten. Hier erhalten Sie weitere [hier](https://docs.microsoft.com/en-gb/kaizala/connectors/members) , um die Details der Member, get müssen Sie die Kaizala Connectors einrichten. [Erfahren Sie mehr](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/connectors/README.md) 
<br/><br/>


**8 wie können wir Mitglied einer Gruppe über Kaizala APIs hinzufügen?**</br></br>
  Kaizala macht API, um Elemente in einer Gruppe hinzufügen. Hier erhalten Sie weitere [hier](https://docs.microsoft.com/en-gb/kaizala/connectors/members).     Damit ein Member einer Gruppe ein Administrator ist, finden Sie unter Beispiel: 
````  
PUT {endpoint-url}/v1/groups/{groupId}/members/{memberId} 

Header: 
accessToken 

Body 
{"role":"Admin"} 
````

**9. ist es möglich, erstellen Sie eine Webhook die mitteilen kann auf Gruppe erstellen?**</br></br>
  Es ist nicht möglich, erstellen eine Webhook um Benachrichtigungen zu Gruppe Kreationen zu erhalten, da alle Webhooks derzeit im Kontext einer Gruppe verwendet werden. Sie können im Kontext einer Gruppe Webhooks um erhalten Sie Benachrichtigungen zu Nachrichten-Aktionen, die werden gesendet/empfangen, Hinzufügen von Mitglied und löschen usw. erstellen.  
<br/><br/>

**10. müssen Connectors manuell in jeder Gruppe hinzugefügt werden?**</br></br>
  Wenn Sie der Connector aus Mandantenadministrator erstellt wird, müssen Sie nicht den Connector manuell in jeder Gruppe hinzufügen. 
<br/><br/>


**11. wie kann ich vollständige Antworten von allen Teilnehmern in einer Umfrage unter den abrufen?**</br></br>
Verwenden Sie die folgenden API zum Abrufen aller Antworten für eine bestimmte Umfrage in einer Gruppe:
````
{{endpoint-url}}/v1/groups/{{group-id}}/actions/{{survey-id}}?getDetails=true 
 
Headers: 
accessToken : {{access-token}} 
```` 
<br/><br/>

**12 werden können eine Nachricht in einer Unterhaltung 1-1 in Kaizala über APIs gesendet?**</br></br>  Alle Kaizala-APIs im Kontext einer Gruppe ausgeführt werden. So ist es nicht möglich, eine Nachricht in einer 1-1-Unterhaltung mithilfe einer API zu senden. Folgende Funktionen werden unterstützt:
-   Senden der Nachricht an einen bestimmten Abonnenten in einer öffentlichen Gruppe 
-   Erstellen eine Gruppe mit der Benutzer und die Nachricht an die Gruppe senden.

<br/>
    
**13. ist es möglich, eine Nachricht nur an bestimmten Element in einer Gruppe senden?**</br></br>
  Nur bei einer öffentlichen Gruppe ist es möglich, eine Nachricht an bestimmten Abonnenten senden. In einer normalen Gruppe ist dies nicht möglich. Entnehmen Sie den folgenden Link Weitere Informationen über die zugehörige API: https://docs.microsoft.com/en-gb/kaizala/connectors/messages. <br/>
<br/><br/>

**14. ist es möglich, eine Nachricht nur an bestimmten Element in einer Gruppe senden?**</br></br>
  Alle Kaizala-APIs im Kontext einer Gruppe ausgeführt werden. Es ist also nicht möglich, eine Aktion in einem 1-1-Unterhaltung mithilfe einer API zu senden.  
<br/><br/>

## <a name="kaizala-actions"></a>Kaizala Aktionen

**1. wie kann ich benutzerdefinierte Aktion Entwicklung Einstieg? Gibt es Dokumentation zur Verfügung?**</br></br>
  Benutzerdefinierte Aktion Entwicklung und die zugehörige Dokumentation ist unter Vorschau und NDA abgedeckt ist. Sie können [diese](Actions/README.md)Beitrag starten. </br>
  Falls Sie Fragen haben, können Sie [Kontakt zu uns auf](feedback.md).
<br/><br/>

**2. wie finde ich das aktuelle Kaizala Aktion SDK?**</br></br>

  Das aktuelle Aktion SDK finden Sie [hier]()
<br/><br/> 

 **3. wie kann ich Test/eine benutzerdefinierte Aktion Debug ohne ein Paket jedes Mal hochladen zu müssen?**</br></br>

  Um eine benutzerdefinierte Aktion zu testen, lesen Sie mehr über die Schritte/Prozess [hier](Actions/test.md) 
<br/><br/>


 **4. Was sind Richtlinien, die Aktion Paket einhalten müssen?**</br></br>
Als Entwickler müssen eingehalten werden Richtlinien beim Entwickeln einer benutzerdefiniertes Aktion Package.Please finden sie [hier](Actions/validation.md). Microsoft Kaizala können Ihre Aktion von der app entfernen alle Inkonsistenzen findet.
<br/><br/>

**5., wo kann ich meine benutzerdefinierte Aktionen auf Kaizala-Verwaltungsportal für Berichte zugreifen?**</br></br>
 Kaizala-Verwaltungsportal ermöglicht Benutzern das Erstellen von benutzerdefinierten Aktionen, Formulare, Feedback Karten. Aktionen und werden können, Ihren Gruppen zugeordnet sind, wiederholt zum Nachverfolgen wichtiger geschäftlicher Metriken gesendet. Klicken Sie im Portal werden diese Daten unter "Wiederkehrenden Umfrage Berichte" angezeigt. Als zusätzliche Funktion aggregiert der Bericht Antworten auf diese Karten mit der Zeit und Instanzen. 
<br/><br/>

**6. wie können externen Inhalte in Meine Aktionsseite werden geladen?**</br></br>
Sie können externe Inhalte in Ihrer Aktion durch mithilfe die URL laden, der die Daten enthält. Finden Sie Schritte für die URL mithilfe [hier](Actions/UrlWhitelisting.md).
<br/><br/>

## <a name="integration-with-microsoft-apps"></a>Integration mit Microsoft-Apps

**1. wie können wir einen Kaizala Connector in PowerApps erstellen?**</br></br>
  Microsoft Kaizala wurde als Connector auf Microsoft Flow & PowerApps freigegeben. Weitere [hier](https://support.office.com/en-us/article/Integrate-your-workflow-in-Kaizala-using-Microsoft-Flow-883343d0-6b16-4725-a23d-bc69fb264356)
<br/><br/>

**2. wie kann ich hinzufügen und das Excel-Add-in für Kaizala verwenden?**</br></br>

  Das Excel-Add-in für Kaizala können alle Tabellen in Excel als einer Umfrage zu Kaizala verfügbar gemacht werden. Alle Antworten auf die Umfrage werden automatisch ausgefüllt werden, in der Excel-Tabelle. Weitere [hier](https://support.office.com/en-us/article/Kaizala-Office-Add-in-4cd01439-5da2-4a9f-b493-8f2e23e2fd91?ui=en-US&rs=en-US&ad=US) 

<br/><br/> 



