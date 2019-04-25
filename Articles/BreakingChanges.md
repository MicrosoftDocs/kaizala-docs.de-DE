# <a name="breaking-changes-communication"></a><span data-ttu-id="5e4cf-101">Kommunikation unterBrechende Änderungen</span><span class="sxs-lookup"><span data-stu-id="5e4cf-101">Breaking Changes communication</span></span>

<span data-ttu-id="5e4cf-102">Abonnieren Sie [Kaizala Developer Connect](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) von Ihrer mobilen App aus, um wichtige Änderungen in der Kaizala-Entwicklerplattform zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-102">Subscribe to [Kaizala Developer Connect](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) from your mobile app to receive Breaking changes communication in Kaizala Developer Platform.</span></span>

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

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a><span data-ttu-id="5e4cf-103">Verwaltete öffentliche Gruppen können nur mithilfe von Benutzertoken auf Mandantenebene in der API "Create Group" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-103">Managed Public groups can only be created using Tenant-level user token in 'Create Group' API</span></span>

||<span data-ttu-id="5e4cf-104">Details</span><span class="sxs-lookup"><span data-stu-id="5e4cf-104">Details</span></span>|
|--|--|
|<span data-ttu-id="5e4cf-105">**AusWirkungs Bereich**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-105">**Impact Area**</span></span>| <span data-ttu-id="5e4cf-106">APIs</span><span class="sxs-lookup"><span data-stu-id="5e4cf-106">APIs</span></span> |
|<span data-ttu-id="5e4cf-107">**Zusammenfassung der Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-107">**Impact Summary**</span></span>| <span data-ttu-id="5e4cf-108">Frühere öffentliche Gruppe durfte erstellt werden, ohne dass Sie einer Organisation zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-108">Earlier Public group was allowed to be created without it being mapped to an Organization.</span></span> <span data-ttu-id="5e4cf-109">Verwaltete öffentliche Gruppen können fortan über "[Create Group](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)" erstellt werden, nur wenn Benutzertoken auf Mandantenebene in der API verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-109">Henceforth, Managed Public Groups can be created through '[Create group](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)', only when tenant-level user token is used in API.</span></span> <span data-ttu-id="5e4cf-110">[Hier](connectors/UserToken.md) finden Sie weitere Informationen zum Prozess zum Generieren des Benutzertokens</span><span class="sxs-lookup"><span data-stu-id="5e4cf-110">Read [here](connectors/UserToken.md) more for the process to generate user token</span></span> |
|<span data-ttu-id="5e4cf-111">**Kommunikations Datum**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-111">**Date of Communication**</span></span>|<span data-ttu-id="5e4cf-112">06-06-2018</span><span class="sxs-lookup"><span data-stu-id="5e4cf-112">06-06-2018</span></span>|
|<span data-ttu-id="5e4cf-113">**Datum der Auswirkung**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-113">**Date of Impact**</span></span>|<span data-ttu-id="5e4cf-114">22-06-2018</span><span class="sxs-lookup"><span data-stu-id="5e4cf-114">22-06-2018</span></span>|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a><span data-ttu-id="5e4cf-115">Validierung registrierter callBackUrl bei der Erstellung von webhook</span><span class="sxs-lookup"><span data-stu-id="5e4cf-115">Validation of registered callBackUrl when webhook is created</span></span>

||<span data-ttu-id="5e4cf-116">Details</span><span class="sxs-lookup"><span data-stu-id="5e4cf-116">Details</span></span>|
|--|--|
|<span data-ttu-id="5e4cf-117">**AusWirkungs Bereich**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-117">**Impact Area**</span></span>| <span data-ttu-id="5e4cf-118">Webhooks</span><span class="sxs-lookup"><span data-stu-id="5e4cf-118">Webhooks</span></span> |
|<span data-ttu-id="5e4cf-119">**Zusammenfassung der Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-119">**Impact Summary**</span></span>| <span data-ttu-id="5e4cf-120">Bei der Erstellung von webhook ([Post/webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)) würden registrierte callBackUrl überprüft.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-120">Going ahead, during creation of Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), registered callBackUrl would be validated.</span></span> <span data-ttu-id="5e4cf-121">Nach erfolgreicher Validierung würde ein webhook erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-121">After successful validation, a webhook would be created</span></span> |
|<span data-ttu-id="5e4cf-122">**Erforderliche Aktion**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-122">**Required Action**</span></span>| <span data-ttu-id="5e4cf-123">Ältere webhook-Abonnements funktionieren weiterhin über das Datum hinaus.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-123">Older Webhook subscriptions will continue to work beyond the Date of Impact.</span></span> <span data-ttu-id="5e4cf-124">Für neue webhook-Abonnementanforderungen müssen Sie sicherstellen, dass der Dienst dem [hier](connectors/WebHookValidaton.md) genannten Prozess folgt.</span><span class="sxs-lookup"><span data-stu-id="5e4cf-124">New Webhook subscription requests would require you to ensure your service follows the process mentioned [here](connectors/WebHookValidaton.md)</span></span> |
|<span data-ttu-id="5e4cf-125">**Kommunikations Datum**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-125">**Date of Communication**</span></span>|<span data-ttu-id="5e4cf-126">09-05-2018</span><span class="sxs-lookup"><span data-stu-id="5e4cf-126">09-05-2018</span></span>|
|<span data-ttu-id="5e4cf-127">**Datum der Auswirkung**</span><span class="sxs-lookup"><span data-stu-id="5e4cf-127">**Date of Impact**</span></span>|<span data-ttu-id="5e4cf-128">15-06-2018</span><span class="sxs-lookup"><span data-stu-id="5e4cf-128">15-06-2018</span></span>|

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


