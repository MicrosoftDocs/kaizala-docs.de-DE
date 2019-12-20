---
title: Kaizala-APIs
description: Liste der APIs, die von Kaizala verfügbar gemacht werden, um die Integration mit Drittanbietersystemen zu ermöglichen
topic: Reference
author: nitinjms
ms.openlocfilehash: a271b34747cd849227702765787dfe7c9b0b99fa
ms.sourcegitcommit: 9e57984827280ed977019d33dd78b1ce5e3097fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2019
ms.locfileid: "40809429"
---
# <a name="kaizala-api-documentation"></a><span data-ttu-id="634c7-103">Kaizala-API-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="634c7-103">Kaizala API Documentation</span></span>

<span data-ttu-id="634c7-104">Lesen Sie vor dem ersten Start die Informationen unter [Setup für die Verwendung der Kaizala-Connectors](setup.md) .</span><span class="sxs-lookup"><span data-stu-id="634c7-104">Before you get started, please refer to [Setup for using the Kaizala Connectors](setup.md)</span></span>

## <a name="root-domain"></a><span data-ttu-id="634c7-105">Stammdomäne</span><span class="sxs-lookup"><span data-stu-id="634c7-105">Root Domain</span></span>

<span data-ttu-id="634c7-106">Die Stammdomäne zum Aufrufen der Kaizala-APIs lautet:</span><span class="sxs-lookup"><span data-stu-id="634c7-106">The root domain for invoking the Kaizala APIs is:</span></span>

    {endpoint-url}
    
|               | <span data-ttu-id="634c7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="634c7-107">Parameter</span></span>             | <span data-ttu-id="634c7-108">Typ</span><span class="sxs-lookup"><span data-stu-id="634c7-108">Type</span></span>      | <span data-ttu-id="634c7-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="634c7-109">Optional?</span></span>     | <span data-ttu-id="634c7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="634c7-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="634c7-111">Endpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="634c7-111">Endpoint url</span></span>  | `endpoint-url`        | <span data-ttu-id="634c7-112">String</span><span class="sxs-lookup"><span data-stu-id="634c7-112">String</span></span>    | <span data-ttu-id="634c7-113">Nein</span><span class="sxs-lookup"><span data-stu-id="634c7-113">No</span></span>            | <span data-ttu-id="634c7-114">Bei erfolgreicher Authentifizierung beim Generieren von Zugriffstoken wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="634c7-114">On successful auth while generating access tokens, an endpoint url is returned that should be used as api-base-url for making subsequent API calls</span></span>    |

> <span data-ttu-id="634c7-115">Während Sie auf eine beliebige Kaizala-API treffen, können Sie den HTTP-Statuscode: 308 abrufen, der angibt, dass die Endpunkt-URL des Benutzers geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="634c7-115">While hitting any Kaizala api, you can get Http status code:308 indicating that the user's endpoint-url has changed.</span></span> <span data-ttu-id="634c7-116">In diesem Fall wird der Speicherort der Antwort Kopfzeile die neue Endpunkt-URL enthalten.</span><span class="sxs-lookup"><span data-stu-id="634c7-116">In that case, Response header location will contain the new endpoint-url.</span></span>

> <span data-ttu-id="634c7-117">**Anregung:** Clients können Timeout für den Empfang von Antworten von Kaizala-APIs bei 1 min konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="634c7-117">**Suggestion:** Clients can configure timeout to receive response from Kaizala APIs at 1 min</span></span>

### <a name="api-end-points"></a><span data-ttu-id="634c7-118">End-Points-API</span><span class="sxs-lookup"><span data-stu-id="634c7-118">API End-points</span></span>

<span data-ttu-id="634c7-119">Die Kaizala-API wird auf der Secure Microsoft Azure Cloud ausgeführt und interagiert mit der Kaizala-Plattform, um verschiedene Aktionen für Endbenutzer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="634c7-119">The Kaizala API runs on the secure Microsoft Azure cloud, and interacts with the Kaizala platform to perform various actions for end users.</span></span>
<span data-ttu-id="634c7-120">Die API funktioniert mit den folgenden Kaizala-Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="634c7-120">The API works with the following Kaizala resources:</span></span>

*   [<span data-ttu-id="634c7-121">/Groups</span><span class="sxs-lookup"><span data-stu-id="634c7-121">/groups</span></span>](groups.md)
*   [<span data-ttu-id="634c7-122">/subGroups</span><span class="sxs-lookup"><span data-stu-id="634c7-122">/subGroups</span></span>](subGroups.md)
*   [<span data-ttu-id="634c7-123">/members</span><span class="sxs-lookup"><span data-stu-id="634c7-123">/members</span></span>](members.md)
*   [<span data-ttu-id="634c7-124">/messages</span><span class="sxs-lookup"><span data-stu-id="634c7-124">/messages</span></span>](messages.md)
*   [<span data-ttu-id="634c7-125">/Media</span><span class="sxs-lookup"><span data-stu-id="634c7-125">/media</span></span>](media.md)
*   [<span data-ttu-id="634c7-126">/actions</span><span class="sxs-lookup"><span data-stu-id="634c7-126">/actions</span></span>](actions.md)
*   [<span data-ttu-id="634c7-127">/subscribers</span><span class="sxs-lookup"><span data-stu-id="634c7-127">/subscribers</span></span>](subscribers.md)
*    [<span data-ttu-id="634c7-128">/reaction</span><span class="sxs-lookup"><span data-stu-id="634c7-128">/reaction</span></span>](reactions.md)

> <span data-ttu-id="634c7-129">Die Kaizala-API hat den einschränkungsgrenzwert von **100 Anrufen pro Minute pro Connector**.</span><span class="sxs-lookup"><span data-stu-id="634c7-129">Kaizala API has the throttling limit of **100 calls per min per connector**.</span></span> <span data-ttu-id="634c7-130">Wenn die Einschränkungs Grenze überschritten wird, gibt die API den Wert "Retry-after" zusammen mit HTTP-Statuscode: 429 zurück.</span><span class="sxs-lookup"><span data-stu-id="634c7-130">When throttling limit exceeds, the API will return "Retry-After" value along with Http status code:429.</span></span> <span data-ttu-id="634c7-131">Der Wert "Retry-after" gibt an, wie viele Sekunden gewartet werden soll, bevor eine weitere Anforderung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="634c7-131">The "Retry-After" value specifies how many seconds to wait before making another request.</span></span>

### <a name="webhooks"></a><span data-ttu-id="634c7-132">WebHooks</span><span class="sxs-lookup"><span data-stu-id="634c7-132">WebHooks</span></span>

<span data-ttu-id="634c7-133">Die Microsoft Kaizala-API bietet Entwicklern auch die Möglichkeit, sich über webhooks für bestimmte Ereignisse in der Kaizala-Plattform zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="634c7-133">The Microsoft Kaizala API also provides a way for developers to register for specific events within the Kaizala platform via WebHooks.</span></span>

*   [<span data-ttu-id="634c7-134">/webhook</span><span class="sxs-lookup"><span data-stu-id="634c7-134">/webhook</span></span>](webHooks.md)

### <a name="postman-collection"></a><span data-ttu-id="634c7-135">Postman-Sammlung</span><span class="sxs-lookup"><span data-stu-id="634c7-135">Postman Collection</span></span>

<span data-ttu-id="634c7-136">Um unsere APIs zu testen und das Kaizala-API-Schema zu verstehen, können Sie die Postman-Auflistung mit Beispielen und Schema für alle Microsoft Kaizala-APIs importieren:</span><span class="sxs-lookup"><span data-stu-id="634c7-136">In order to test our APIs, as well as understand Kaizala API schema, you can import postman collection containing samples and schema for all the Microsoft Kaizala apis:</span></span>


<span data-ttu-id="634c7-137">[![In Postman ausführen](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span><span class="sxs-lookup"><span data-stu-id="634c7-137">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span></span>

<span data-ttu-id="634c7-138">Legen Sie die folgenden Umgebungsvariablen in "Kaizala-APIs-Environment" fest, bevor Sie das Postman-Projekt ausführen:</span><span class="sxs-lookup"><span data-stu-id="634c7-138">Please set following environment variables in "Kaizala-APIs-environment" before running the postman project:</span></span>
* <span data-ttu-id="634c7-139">Mobiltelefonnummer: Ihre Mobiltelefonnummer, die zum Aufrufen von APIs verwendet wird</span><span class="sxs-lookup"><span data-stu-id="634c7-139">mobile-number : Your mobile number which will be used for invoking apis</span></span>
* <span data-ttu-id="634c7-140">Application-ID: ID, die dem Connector zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="634c7-140">application-id : ID associated with the Connector</span></span>
* <span data-ttu-id="634c7-141">Anwendungs Geheimnis: mit dem Connector verknüpfte Verschlüsselungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="634c7-141">application-secret : Secret associated with the Connector</span></span>

<span data-ttu-id="634c7-142">Andere Umgebungsvariablen werden automatisch aufgefüllt, während Sie die APIs in der Reihenfolge Erwähnung im Postman-Projekt ausprobieren.</span><span class="sxs-lookup"><span data-stu-id="634c7-142">Other environment variables will be auto-populated while trying the apis in sequence mention in Postman Project.</span></span> 

### <a name="getting-started-with-kaizala-rest-apis"></a><span data-ttu-id="634c7-143">Erste Schritte mit Kaizala-Rest-APIs</span><span class="sxs-lookup"><span data-stu-id="634c7-143">Getting started with Kaizala REST APIs</span></span> 

[<span data-ttu-id="634c7-144">C#-Beispiel (Shared)</span><span class="sxs-lookup"><span data-stu-id="634c7-144">C# sample (shared)</span></span>](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
