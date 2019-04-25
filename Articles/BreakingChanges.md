# <a name="breaking-changes-communication"></a>Kommunikation unterBrechende Änderungen

Abonnieren Sie [Kaizala Developer Connect](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) von Ihrer mobilen App aus, um wichtige Änderungen in der Kaizala-Entwicklerplattform zu erhalten.

<!---

## Deprecating Mobile Number data from Kaizala APIs & Webhooks
||Details|
|--|--|
|**Impact Area**| APIs & Webhooks |
|**Impact Summary**|Kaizala APIs & Webhooks will stop returning Mobile Number as part of reponse. It will return Kaizala userIDs, which can be used to identify unique users. List of APIs & Webhook impacted:<br> <ol><li></li>|
|**Requires Action**|3rd party developers should make necessary changes to avoid break in their solutions. During the time period between 'Date of communication' & 'Date of Impact', Kaizala APIs will return both Mobile numbers and User IDs|
|**Date of Communication**| 18-04-2018 |
|**Date of Impact**| 15-05-2018|

-->

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a>Verwaltete öffentliche Gruppen können nur mithilfe von Benutzertoken auf Mandantenebene in der API "Create Group" erstellt werden.

||Details|
|--|--|
|**AusWirkungs Bereich**| APIs |
|**Zusammenfassung der Auswirkungen**| Frühere öffentliche Gruppe durfte erstellt werden, ohne dass Sie einer Organisation zugeordnet wurde. Verwaltete öffentliche Gruppen können fortan über "[Create Group](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)" erstellt werden, nur wenn Benutzertoken auf Mandantenebene in der API verwendet werden. [Hier](connectors/UserToken.md) finden Sie weitere Informationen zum Prozess zum Generieren des Benutzertokens |
|**Kommunikations Datum**|06-06-2018|
|**Datum der Auswirkung**|22-06-2018|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a>Validierung registrierter callBackUrl bei der Erstellung von webhook

||Details|
|--|--|
|**AusWirkungs Bereich**| Webhooks |
|**Zusammenfassung der Auswirkungen**| Bei der Erstellung von webhook ([Post/webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)) würden registrierte callBackUrl überprüft. Nach erfolgreicher Validierung würde ein webhook erstellt werden. |
|**Erforderliche Aktion**| Ältere webhook-Abonnements funktionieren weiterhin über das Datum hinaus. Für neue webhook-Abonnementanforderungen müssen Sie sicherstellen, dass der Dienst dem [hier](connectors/WebHookValidaton.md) genannten Prozess folgt. |
|**Kommunikations Datum**|09-05-2018|
|**Datum der Auswirkung**|15-06-2018|

<!---

## Webhook subscription will be cancelled, if 10 consecutive failures are received

||Details|
|--|--|
|**Impact Area**| Webhooks |
|**Impact Summary**| Subscription of WebHooks would be suspended, if Kaizala server doesn't receive success for 10 consecutive attempts. Developer will get communication regarding the same on Kaizala Developer Connect. Click here to join [Kaizala Developer Connect]()|
|**Required Action**||
|**Date of Communication**| 18-04-2018 |
|**Date of Impact**| 01-06-2018 |
-->


