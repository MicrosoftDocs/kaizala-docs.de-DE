---
title: Kaizala-APIs
description: Liste der APIs, die von Kaizala verfügbar gemacht werden, um die Integration in Drittanbietersysteme zu ermöglichen
topic: Reference
author: nitinjms
ms.openlocfilehash: abedf063f7af73190dd3d5c2c748bc41d253a590
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190722"
---
# <a name="kaizala-api-documentation"></a><span data-ttu-id="c1293-103">Kaizala-API-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c1293-103">Kaizala API Documentation</span></span>

<span data-ttu-id="c1293-104">Bevor Sie beginnen, lesen Sie [Setup für die Verwendung der Kaizala](setup.md) -Connectors</span><span class="sxs-lookup"><span data-stu-id="c1293-104">Before you get started, please refer to [Setup for using the Kaizala Connectors](setup.md)</span></span>

## <a name="root-domain"></a><span data-ttu-id="c1293-105">Stammdomäne</span><span class="sxs-lookup"><span data-stu-id="c1293-105">Root Domain</span></span>

<span data-ttu-id="c1293-106">Die Stammdomäne zum Aufrufen der Kaizala-APIs lautet:</span><span class="sxs-lookup"><span data-stu-id="c1293-106">The root domain for invoking the Kaizala APIs is:</span></span>

    {endpoint-url}
    
|               | <span data-ttu-id="c1293-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1293-107">Parameter</span></span>             | <span data-ttu-id="c1293-108">Typ</span><span class="sxs-lookup"><span data-stu-id="c1293-108">Type</span></span>      | <span data-ttu-id="c1293-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="c1293-109">Optional?</span></span>     | <span data-ttu-id="c1293-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1293-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="c1293-111">Endpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="c1293-111">Endpoint url</span></span>  | `endpoint-url`        | <span data-ttu-id="c1293-112">String</span><span class="sxs-lookup"><span data-stu-id="c1293-112">String</span></span>    | <span data-ttu-id="c1293-113">Nein</span><span class="sxs-lookup"><span data-stu-id="c1293-113">No</span></span>            | <span data-ttu-id="c1293-114">Bei erfolgreicher Authentifizierung beim Generieren von Zugriffstoken wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="c1293-114">On successful auth while generating access tokens, an endpoint url is returned that should be used as api-base-url for making subsequent API calls</span></span>    |

<span data-ttu-id="c1293-115">Beachten Sie, dass beim Schlagen einer Kaizala-API der HTTP-Statuscode: 308 angezeigt wird, dass die Endpunkt-URL des Benutzers geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c1293-115">Please note that while hitting any Kaizala api, you can get Http status code:308 indicating that the user's endpoint-url has changed.</span></span> <span data-ttu-id="c1293-116">In diesem Fall enthält der Speicherort des Antwortheaders die neue Endpunkt-URL.</span><span class="sxs-lookup"><span data-stu-id="c1293-116">In that case, Response header location will contain the new endpoint-url.</span></span>

### <a name="api-end-points"></a><span data-ttu-id="c1293-117">API-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="c1293-117">API End-points</span></span>

<span data-ttu-id="c1293-118">Die Kaizala-API wird in der sicheren Microsoft Azure-Cloud ausgeführt und interagiert mit der Kaizala-Plattform, um verschiedene Aktionen für Endbenutzer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c1293-118">The Kaizala API runs on the secure Microsoft Azure cloud, and interacts with the Kaizala platform to perform various actions for end users.</span></span>
<span data-ttu-id="c1293-119">Die API kann mit den folgenden Kaizala-Ressourcen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="c1293-119">The API works with the following Kaizala resources:</span></span>

*   [<span data-ttu-id="c1293-120">/Groups</span><span class="sxs-lookup"><span data-stu-id="c1293-120">/groups</span></span>](groups.md)
*   [<span data-ttu-id="c1293-121">/subGroups</span><span class="sxs-lookup"><span data-stu-id="c1293-121">/subGroups</span></span>](subGroups.md)
*   [<span data-ttu-id="c1293-122">/Members</span><span class="sxs-lookup"><span data-stu-id="c1293-122">/members</span></span>](members.md)
*   [<span data-ttu-id="c1293-123">/Messages</span><span class="sxs-lookup"><span data-stu-id="c1293-123">/messages</span></span>](messages.md)
*   [<span data-ttu-id="c1293-124">/Media</span><span class="sxs-lookup"><span data-stu-id="c1293-124">/media</span></span>](media.md)
*   [<span data-ttu-id="c1293-125">/Actions</span><span class="sxs-lookup"><span data-stu-id="c1293-125">/actions</span></span>](actions.md)
*   [<span data-ttu-id="c1293-126">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="c1293-126">/subscribers</span></span>](subscribers.md)
*    [<span data-ttu-id="c1293-127">/Reaction</span><span class="sxs-lookup"><span data-stu-id="c1293-127">/reaction</span></span>](reactions.md)

### <a name="webhooks"></a><span data-ttu-id="c1293-128">WebHooks</span><span class="sxs-lookup"><span data-stu-id="c1293-128">WebHooks</span></span>

<span data-ttu-id="c1293-129">Die Microsoft Kaizala-API bietet Entwicklern auch eine Möglichkeit, sich über webHooks für bestimmte Ereignisse innerhalb der Kaizala-Plattform zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c1293-129">The Microsoft Kaizala API also provides a way for developers to register for specific events within the Kaizala platform via WebHooks.</span></span>

*   [<span data-ttu-id="c1293-130">/webhook</span><span class="sxs-lookup"><span data-stu-id="c1293-130">/webhook</span></span>](webHooks.md)

### <a name="postman-collection"></a><span data-ttu-id="c1293-131">Postbote-Sammlung</span><span class="sxs-lookup"><span data-stu-id="c1293-131">Postman Collection</span></span>

<span data-ttu-id="c1293-132">Um unsere APIs zu testen und das Kaizala-API-Schema zu verstehen, können Sie die Postman-Auflistung mit Beispielen und Schema für alle Microsoft Kaizala-APIs importieren:</span><span class="sxs-lookup"><span data-stu-id="c1293-132">In order to test our APIs, as well as understand Kaizala API schema, you can import postman collection containing samples and schema for all the Microsoft Kaizala apis:</span></span>


<span data-ttu-id="c1293-133">[![Ausführen in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span><span class="sxs-lookup"><span data-stu-id="c1293-133">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span></span>

<span data-ttu-id="c1293-134">Legen Sie die folgenden Umgebungsvariablen in "Kaizala-APIs-Environment" vor dem Ausführen des Postman-Projekts fest:</span><span class="sxs-lookup"><span data-stu-id="c1293-134">Please set following environment variables in "Kaizala-APIs-environment" before running the postman project:</span></span>
* <span data-ttu-id="c1293-135">Mobile-Number: Ihre Mobiltelefonnummer, die zum Aufrufen von APIs verwendet wird</span><span class="sxs-lookup"><span data-stu-id="c1293-135">mobile-number : Your mobile number which will be used for invoking apis</span></span>
* <span data-ttu-id="c1293-136">Application-ID: ID, die dem Connector zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="c1293-136">application-id : ID associated with the Connector</span></span>
* <span data-ttu-id="c1293-137">Application-Secret: der Verbindung zugeordneter Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c1293-137">application-secret : Secret associated with the Connector</span></span>

<span data-ttu-id="c1293-138">Andere Umgebungsvariablen werden automatisch ausgefüllt, wenn Sie versuchen, die APIs in der Sequenz Erwähnung in Postman Projekt.</span><span class="sxs-lookup"><span data-stu-id="c1293-138">Other enviroment variables will be auto-populated while trying the apis in sequence mention in Postman Project.</span></span> 

### <a name="getting-started-with-kaizala-rest-apis"></a><span data-ttu-id="c1293-139">Erste Schritte mit Kaizala-REST-APIs</span><span class="sxs-lookup"><span data-stu-id="c1293-139">Getting started with Kaizala REST APIs</span></span> 

[<span data-ttu-id="c1293-140">C#-Beispiel (Shared)</span><span class="sxs-lookup"><span data-stu-id="c1293-140">C# sample (shared)</span></span>](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
