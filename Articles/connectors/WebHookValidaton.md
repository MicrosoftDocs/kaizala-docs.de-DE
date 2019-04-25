# <a name="callback-url-validation"></a>ÜberPrüfung der Callback-URL

Um sicherzustellen, dass Ihr webhook-Dienstendpunkt authentisch ist und funktioniert, überprüfen wir Ihre Rückruf-URL, bevor Sie ein Abonnement erstellen.
Zur Überprüfung senden wir Ihnen ein Validierungs Token zu, das Sie innerhalb von 5 Sekunden zurücksenden müssen. Ein Blick auf den gesamten Prozess:

1.  Fordern Sie Kaizala auf, um Ihren webhook mit [Post/Webhook](webHooks.md)zu registrieren. 
2.  Kaizala generiert ein Validierungs Token und sendet eine GET-Anforderung an den webhook mit einem Abfrageparameter "validationToken".
3.  Ihr Dienst soll das Überprüfungstoken (empfangen in Anforderung) im Antworttext als nur-Text zurückgeben.
4.  Wenn die Antwort innerhalb von 5 Sekunden empfangen wird und das empfangene Validierungs Token mit dem in Schritt 2 gesendeten übereinstimmt, wird der webhook erfolgreich registriert, andernfalls wird er zurückgewiesen. 
