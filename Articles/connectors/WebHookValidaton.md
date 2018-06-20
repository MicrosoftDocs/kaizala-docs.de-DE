# <a name="callback-url-validation"></a>Callback-URL-Überprüfung

Um sicherzustellen, dass Ihr Dienstendpunkt Webhook authentisch und betriebsbereit ist wird wir Ihr Callback-URL überprüfen, bevor Abonnement erstellen.
Zur Überprüfung werden wir Sie ein Token Validation senden, die Sie uns wieder innerhalb von 5 Sekunden senden müssen. Einen Blick auf den gesamten Prozess:

1.  Fordern Sie Kaizala zum Registrieren Ihrer Webhook [POST /Webhook](webHooks.md)verwenden. 
2.  Kaizala ein Token Validation generieren und senden Sie eine GET-Anforderung an die Webhook mit einem Abfragezeichenfolgen-Parameter "ValidationToken".
3.  Ihren Dienst sollte das Validierung Token (in Anforderung empfangen) zurückgegeben im Antworttext als nur-text
4.  Wenn wir die Antwort innerhalb von 5 Sekunden und der Validierung token empfangenen entspricht erhalten, die Sie in Schritt2 gesendet Webhook erfolgreich registriert wird, sonst es zurückgewiesen. 
