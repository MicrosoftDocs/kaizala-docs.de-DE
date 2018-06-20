# <a name="breaking-changes-communication"></a>Informationen zum Unterteilen Änderungen Kommunikation

Abonnieren Sie [Kaizala Developer verbinden](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) aus Ihrer mobilen app zum Empfang von neueste Änderungen Kommunikation in Kaizala Developer-Plattform.

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

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a>Verwaltete öffentliche Gruppen können nur auf Mandantenebene Benutzertoken in 'Gruppe erstellen' API mit erstellt werden

||Details|
|--|--|
|**Auswirkung Bereich**| APIs |
|**Zusammenfassung der Auswirkungen**| Frühere öffentliche Gruppe durfte erstellt werden, ohne es zu einer Organisation zugeordnet wird. Nun können Sie öffentliche Gruppen verwaltet über '[Gruppe erstellen](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)', erstellt werden nur, wenn auf Mandantenebene Benutzertoken in API verwendet wird. Lesen [hier](connectors/UserToken.md) weitere für den Prozess zum Generieren von Benutzertoken |
|**Datum der Kommunikation**|06-06-2018|
|**Datum der Auswirkungen**|22-06-2018|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a>Überprüfung der registrierten CallBackUrl Wenn Webhook erstellt wird

||Details|
|--|--|
|**Auswirkung Bereich**| Webhooks |
|**Zusammenfassung der Auswirkungen**| Während der Erstellung von Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)) und sollte im voraus, würde eingetragene CallBackUrl überprüft werden. Nach erfolgreicher Überprüfung würde eine Webhook erstellt werden |
|**Erforderliche Aktion**| Ältere Webhook-Abonnements werden weiterhin über die Datum Auswirkungen arbeiten. Neue Webhook Abonnement Anfragen müssten Sie um sicherzustellen, dass Ihre Service folgt den Prozess erwähnten [hier](connectors/WebHookValidaton.md) |
|**Datum der Kommunikation**|09-05-2018|
|**Datum der Auswirkungen**|15-06-2018|

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


