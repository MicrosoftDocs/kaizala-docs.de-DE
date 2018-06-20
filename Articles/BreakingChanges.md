# <a name="breaking-changes-communication"></a><span data-ttu-id="9a9d0-101">Informationen zum Unterteilen Änderungen Kommunikation</span><span class="sxs-lookup"><span data-stu-id="9a9d0-101">Breaking Changes communication</span></span>

<span data-ttu-id="9a9d0-102">Abonnieren Sie [Kaizala Developer verbinden](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) aus Ihrer mobilen app zum Empfang von neueste Änderungen Kommunikation in Kaizala Developer-Plattform.</span><span class="sxs-lookup"><span data-stu-id="9a9d0-102">Subscribe to [Kaizala Developer Connect](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) from your mobile app to receive Breaking changes communication in Kaizala Developer Platform.</span></span>

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

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a><span data-ttu-id="9a9d0-103">Verwaltete öffentliche Gruppen können nur auf Mandantenebene Benutzertoken in 'Gruppe erstellen' API mit erstellt werden</span><span class="sxs-lookup"><span data-stu-id="9a9d0-103">Managed Public groups can only be created using Tenant-level user token in 'Create Group' API</span></span>

||<span data-ttu-id="9a9d0-104">Details</span><span class="sxs-lookup"><span data-stu-id="9a9d0-104">Details</span></span>|
|--|--|
|<span data-ttu-id="9a9d0-105">**Auswirkung Bereich**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-105">**Impact Area**</span></span>| <span data-ttu-id="9a9d0-106">APIs</span><span class="sxs-lookup"><span data-stu-id="9a9d0-106">APIs</span></span> |
|<span data-ttu-id="9a9d0-107">**Zusammenfassung der Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-107">**Impact Summary**</span></span>| <span data-ttu-id="9a9d0-108">Frühere öffentliche Gruppe durfte erstellt werden, ohne es zu einer Organisation zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="9a9d0-108">Earlier Public group was allowed to be created without it being mapped to an Organization.</span></span> <span data-ttu-id="9a9d0-109">Nun können Sie öffentliche Gruppen verwaltet über '[Gruppe erstellen](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)', erstellt werden nur, wenn auf Mandantenebene Benutzertoken in API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a9d0-109">Henceforth, Managed Public Groups can be created through '[Create group](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)', only when tenant-level user token is used in API.</span></span> <span data-ttu-id="9a9d0-110">Lesen [hier](connectors/UserToken.md) weitere für den Prozess zum Generieren von Benutzertoken</span><span class="sxs-lookup"><span data-stu-id="9a9d0-110">Read [here](connectors/UserToken.md) more for the process to generate user token</span></span> |
|<span data-ttu-id="9a9d0-111">**Datum der Kommunikation**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-111">**Date of Communication**</span></span>|<span data-ttu-id="9a9d0-112">06-06-2018</span><span class="sxs-lookup"><span data-stu-id="9a9d0-112">06-06-2018</span></span>|
|<span data-ttu-id="9a9d0-113">**Datum der Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-113">**Date of Impact**</span></span>|<span data-ttu-id="9a9d0-114">22-06-2018</span><span class="sxs-lookup"><span data-stu-id="9a9d0-114">22-06-2018</span></span>|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a><span data-ttu-id="9a9d0-115">Überprüfung der registrierten CallBackUrl Wenn Webhook erstellt wird</span><span class="sxs-lookup"><span data-stu-id="9a9d0-115">Validation of registered callBackUrl when webhook is created</span></span>

||<span data-ttu-id="9a9d0-116">Details</span><span class="sxs-lookup"><span data-stu-id="9a9d0-116">Details</span></span>|
|--|--|
|<span data-ttu-id="9a9d0-117">**Auswirkung Bereich**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-117">**Impact Area**</span></span>| <span data-ttu-id="9a9d0-118">Webhooks</span><span class="sxs-lookup"><span data-stu-id="9a9d0-118">Webhooks</span></span> |
|<span data-ttu-id="9a9d0-119">**Zusammenfassung der Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-119">**Impact Summary**</span></span>| <span data-ttu-id="9a9d0-120">Während der Erstellung von Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)) und sollte im voraus, würde eingetragene CallBackUrl überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9a9d0-120">Going ahead, during creation of Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), registered callBackUrl would be validated.</span></span> <span data-ttu-id="9a9d0-121">Nach erfolgreicher Überprüfung würde eine Webhook erstellt werden</span><span class="sxs-lookup"><span data-stu-id="9a9d0-121">After successful validation, a webhook would be created</span></span> |
|<span data-ttu-id="9a9d0-122">**Erforderliche Aktion**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-122">**Required Action**</span></span>| <span data-ttu-id="9a9d0-123">Ältere Webhook-Abonnements werden weiterhin über die Datum Auswirkungen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9a9d0-123">Older Webhook subscriptions will continue to work beyond the Date of Impact.</span></span> <span data-ttu-id="9a9d0-124">Neue Webhook Abonnement Anfragen müssten Sie um sicherzustellen, dass Ihre Service folgt den Prozess erwähnten [hier](connectors/WebHookValidaton.md)</span><span class="sxs-lookup"><span data-stu-id="9a9d0-124">New Webhook subscription requests would require you to ensure your service follows the process mentioned [here](connectors/WebHookValidaton.md)</span></span> |
|<span data-ttu-id="9a9d0-125">**Datum der Kommunikation**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-125">**Date of Communication**</span></span>|<span data-ttu-id="9a9d0-126">09-05-2018</span><span class="sxs-lookup"><span data-stu-id="9a9d0-126">09-05-2018</span></span>|
|<span data-ttu-id="9a9d0-127">**Datum der Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="9a9d0-127">**Date of Impact**</span></span>|<span data-ttu-id="9a9d0-128">15-06-2018</span><span class="sxs-lookup"><span data-stu-id="9a9d0-128">15-06-2018</span></span>|

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


