## <a name="integrating-kaizala-data-to-your-existing-dashboards"></a>Integrieren von Kaizala Daten an die vorhandenen dashboards

Erstellen Sie benutzerdefinierten Bericht, oder schließen Sie Daten aus dem Kaizala der vorhandenen Dashboards mithilfe von Kaizala-APIs. 
<br>Als Organisation Drittanbieter - Sie Kaizala Daten zum vorhandenen Dashboard schließen möchten, und führen Sie mithilfe der folgenden Methoden:
<br>1. abzurufen Sie Kaizala Daten über Power BI-Inhalten Pack und erstellen Sie einen benutzerdefinierten Bericht PowerBI
<br>2.Wählen Datenzugriff Kaizala über Connectors, und übergeben Sie auf vorhandenen Dashboard im Format, das ihn versteht. Sie können Daten mithilfe von Kaizala Connecters zugreifen:  
<br>a.[APIs](https://docs.microsoft.com/en-us/kaizala/connectors/api) - Kaizala Connectors aktivieren 3. Partei Entwickler Kaizala in ihre Geschäftsprozesse durch bereitstellen, dass die Möglichkeit zum Ausführen einer curated Reihe von Aktionen in Kaizala mithilfe von REST-API-Aufrufe basierend integrieren. Der Bereich der API ist für externe Systeme zum Aufrufen des Endpunkt und Ausführen von Aktionen auf Abruf. D. h., wird dies eine PULL-Modell sein, in denen einzelne Endpunkte aufgerufen werden, um bestimmte Aktionen mit Kaizala-API ausführen müssen. 
<br>B.[Webhooks](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks) - der PUSH-Modell, in dem Kaizala-Plattform von Aktionen ausgelöst werden kann, können mithilfe von Webhooks konfiguriert werden.  
<br> Kaizala Connectors ermöglichen es 3. Partei Entwicklern integrieren Kaizala in ihre Geschäftsprozesse durch bereitstellen, dass die Möglichkeit zum Ausführen einer curated Reihe von Aktionen in Kaizala mithilfe von REST-API-Aufrufe basiert. Der Bereich der API ist für externe Systeme zum Aufrufen des Endpunkt und Ausführen von Aktionen auf Abruf. D. h., wird dies eine PULL-Modell – sein, in denen einzelne Endpunkte aufgerufen werden, um bestimmte Aktionen Kaizala [APIs](https://docs.microsoft.com/en-us/kaizala/connectors/api)ausführen müssen. Das PUSH-Modell, in dem Kaizala Plattform Aktionen auslösen kann, kann mithilfe von [Webhooks](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks)konfiguriert werden. 
![](Images/GetImage.png)
### <a name="integration-using-webhooks"></a>Integration mit Webhooks: 
<br>Dies ist eine Grundlage PUSH-Mechanismus. Sobald Webhook auf bestimmten Aktion registriert ist, wenn der Benutzer Daten von dieser Aktion auf Kaizala-Anwendung – übermittelt sendet Kaizala Server eine Benachrichtigung (Nachricht HTTP POST) mit Antwort Nutzlast (JSON-Format) an den konfigurierten URL-Endpunkt. Nachdem Daten für Kunden Endpunkt informiert werden, Logik für die Analyse der Antwort Nutzlast sollte auslösen und Einfügen von Daten in den jeweiligen Tabellen im Speicher (Datenbank oder Sharepoint...), und Visualisierungen von Abfragen von Daten aus dem Speicher erstellt werden können. Vorteil besteht darin, dass jede Organisation Kaizala für ihre benutzerdefinierte Dashboards Abrufen von Daten kann ohne Beeinträchtigung ihrer vorhandenen Arbeitsabläufe. 
### <a name="lets-drill-down-in-to-the-above-process-and-see-it-in-detail"></a>Können an den oben beschriebenen Prozess Ausführen eines Drilldowns und im Detail angezeigt: 
#### <a name="how-to-register-a-webhook-on-endpoint"></a>Wie Sie eine Webhook für Endpunkt registrieren? 
<br> Nachdem Sie einen URL-Endpunkt konfigurieren, auf dem die Kaizala Ereignisse benachrichtigt werden möchten, können Sie für eine Benachrichtigung auf die Gruppe oder eine bestimmte Aktion abonnieren. Sie können die 3. Partei Rest-API-Clients wie Postman / erweiterter Rest Client usw., eine Webhook zu abonnieren. Signatur der Registrierung einer Webhook auf bestimmte Aktion wird unten angezeigt:![](Images/GetImage_2.png)
<br>Wechseln Sie zu [Kaizala API-Dokumentation!](https://docs.microsoft.com/en-us/kaizala/connectors/api) und klicken Sie auf der![](Images/GetImage%20_1.png)
<br>Durchlaufen Sie die Schritte zum Abrufen der AccessToken und eine Wekbhook registrieren. 
 
<br>Wie Sie jetzt eine Webhook registriert haben, wird Kaizala Server benachrichtigen lassen Sie die Ereignisse auf der registrierten URL jedem Ereignis tritt auf. Ereignis Antwort befindet sich in der folgenden JSON-Format: 
 
<br> Beispiel-Ereignis Antwort im JSON:
<br> {   
<br> "objectId":"com.microsoft.kaizala.OrderFormDemo",
<br> "ObjectType": "ActionPackage",
<br> "EventType": "ActionResponse",
<br> "EventId": "75609730-f5d2-4f07-XXXX-ccca96dd9e76,"
<br>"Daten": {   
<br> "ActionId": "eb40446b-3dc7-4e8e-XXXX-44ccc5ae760c,"
<br> "actionPackageId":"com.microsoft.kaizala.OrderFormDemo",
<br> "packageId":"com.microsoft.kaizala.OrderFormDemo",
<br> "GroupId": "af461a3c-49cf-47cf-XXXX-83b5d348318d,"
<br> "ResponseId": "75609730-f5d2-4f07-XXXX-ccca96dd9e76,"
<br> "IsUpdateResponse": false
<br> "Responder": "+911234567890",
<br> "ResponderName": "FooName",
<br> "ResponderProfilePic": "",
<br> "IsAnonymous": false
<br> "ResponseDetails": {   
<br> "ResponseWithQuestions": [   
<br> {   
<br>"Title": "Händler Steckdose",
<br>"Typ": "SingleOption",
<br> "Optionen": [   
<br>{   
<br> "Title": "ABC Traders"
<br>},
<br> {   
<br>"Title": "BCD Händler"
<br>},
<br>{   
<br>"Title": "EFG groß-"
<br>}
<br>],
<br> "Antwort": [   
<br>"ABC Traders"
<br>]
<br> },
<br> {   
<br> "Title": "Reis 1KG",
<br> "Typ": "Numerische"
<br>"Optionen": [   
<br> ],
<br> "Antworten Sie":1.0
<br>},
<br> {   
<br>"Title": "Reis 5KG",
<br> "Typ": "Numerische"
<br>"Optionen": [   
<br>],
<br> "Antworten Sie":2.0
<br> },
<br> {   
<br> "Title": "Gemischten Fruchtsaft 250ml",
<br> "Typ": "Numerische"
<br> "Optionen": [   
<br> ],
<br> "Antworten Sie":4.0
<br> },
<br> {   
<br> "Title": "Speicherort"
<br> "Typ": "Speicherort"
<br>"Optionen": [   
 
<br> ],
<br> "Antwort": {   
<br> "Lt":99.1234567,
<br>"Lg":88.1234567,
<br> "n": "FooAddress"
<br>}
<br>}
<br> ]
<br> }
<br> },
<br> "Kontext": "alle Daten der Rückruf zurückgegeben werden sollen, erforderlich ist.Aktuellen Webhook Daten durch Aktualisieren angezeigt werden können:[: https://requestb.in/12786un1?inspect!](https://requestb.in/12786un1?inspect)
<br> "FromUser": "+911234567890",
<br> "FromUserName": "FooName",
<br>"FromUserProfilePic": ""
<br> }
<br> **Klicken Sie auf der registrierten Endpunkt** - Geschäftslogik zu analysieren, die Antwort Ereignis einfügen von Daten in den jeweiligen Speicher Tabellen haben. Wie Daten jetzt an Ihrem Ende verfügbar sind, Abfragen von Daten aus dem Speicher und Visualisierungen auf der vorhandenen Dashboards anzeigen. Bei diesem Ansatz - können Sie die Visualisierungen Kaizala Daten auf vorhandene Dashboards erstellen. Bei diesem Ansatz werden Sie die Daten in Echtzeit benachrichtigt abrufen werden mithilfe der Webhook-Endpunkt.  
#### <a name="how-to-pull-data-using-kaizala-apis"></a>Wie kann ich PULL-Daten mit Kaizala-API? 
Wenn Sie, Pull-Daten aus Kaizala in regelmäßigen Abständen möchten und Aktualisieren von Daten in Dashboard - Sie aufrufen können Kaizala API mit dem Verbinder und nicht ausgewählte Pull Daten für das gewünschte Aktion Paket aktualisieren von Daten in den Speicher und Dashboard zu aktualisieren. 
<br><br>
**Für das Abfragen eines Pakets Aktion der Antworten**- können Sie finden die Signatur API und die Antwort durch das Aufrufen der oben genannten Postman-Auflistung und Content-Abfrage-API--> Fetch Aktion Antworten in einer Gruppe, und Ersetzen Sie mit Ihrer Aktion-Gruppe Details zum Lösungspaket <br>
![](Images/GetImage_3.png)
