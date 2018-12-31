---
title: Kaizala-APIs
description: Liste der APIs, Kaizala verfügbar macht, um die Integration mit 3. Partei Systemen ermöglichen
topic: Reference
author: nitinjms
ms.openlocfilehash: abedf063f7af73190dd3d5c2c748bc41d253a590
ms.sourcegitcommit: 58839035fca768f92eda40974029208eb31dda7f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/31/2018
ms.locfileid: "27465703"
---
# <a name="kaizala-api-documentation"></a><span data-ttu-id="52223-103">Kaizala API-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="52223-103">Kaizala API Documentation</span></span>

<span data-ttu-id="52223-104">Bevor Sie beginnen, finden Sie in [Setup für die Verwendung der Kaizala-Connectors](setup.md)</span><span class="sxs-lookup"><span data-stu-id="52223-104">Before you get started, please refer to [Setup for using the Kaizala Connectors](setup.md)</span></span>

## <a name="root-domain"></a><span data-ttu-id="52223-105">Stammdomäne</span><span class="sxs-lookup"><span data-stu-id="52223-105">Root Domain</span></span>

<span data-ttu-id="52223-106">Die Stammdomäne für das Aufrufen der Kaizala-APIs ist:</span><span class="sxs-lookup"><span data-stu-id="52223-106">The root domain for invoking the Kaizala APIs is:</span></span>

    {endpoint-url}
    
|               | <span data-ttu-id="52223-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="52223-107">Parameter</span></span>             | <span data-ttu-id="52223-108">Typ</span><span class="sxs-lookup"><span data-stu-id="52223-108">Type</span></span>      | <span data-ttu-id="52223-109">Optional?</span><span class="sxs-lookup"><span data-stu-id="52223-109">Optional?</span></span>     | <span data-ttu-id="52223-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52223-110">Description</span></span> |
| :---: | :---: | :---: | :---: | :--- |
| <span data-ttu-id="52223-111">Endpunkt-url</span><span class="sxs-lookup"><span data-stu-id="52223-111">Endpoint url</span></span>  | `endpoint-url`        | <span data-ttu-id="52223-112">String</span><span class="sxs-lookup"><span data-stu-id="52223-112">String</span></span>    | <span data-ttu-id="52223-113">Nein</span><span class="sxs-lookup"><span data-stu-id="52223-113">No</span></span>            | <span data-ttu-id="52223-114">Erfolgreiche Authentifizierung beim Generieren von Zugriffstoken ist eine Endpunkt-Url zurückgegeben, für nachfolgende API-Aufrufe, die als api-Basis-Url verwendet werden sollten</span><span class="sxs-lookup"><span data-stu-id="52223-114">On successful auth while generating access tokens, an endpoint url is returned that should be used as api-base-url for making subsequent API calls</span></span>    |

<span data-ttu-id="52223-115">Beachten Sie, dass beim Drücken einer beliebigen Kaizala-api, Sie HTTP-Status Code: 308 zurück, der angibt, dass der Benutzer Endpunkt-Url geändert hat abrufen können.</span><span class="sxs-lookup"><span data-stu-id="52223-115">Please note that while hitting any Kaizala api, you can get Http status code:308 indicating that the user's endpoint-url has changed.</span></span> <span data-ttu-id="52223-116">In diesem Fall wird Antwort Kopfzeile Speicherort die neue Endpunkt-Url enthalten.</span><span class="sxs-lookup"><span data-stu-id="52223-116">In that case, Response header location will contain the new endpoint-url.</span></span>

### <a name="api-end-points"></a><span data-ttu-id="52223-117">API-Endgeräte</span><span class="sxs-lookup"><span data-stu-id="52223-117">API End-points</span></span>

<span data-ttu-id="52223-118">Die Kaizala-API auf der sicheren Microsoft Azure-Cloud ausgeführt wird, und mit der Kaizala-Plattform für verschiedene Aktionen für Endbenutzer interagiert.</span><span class="sxs-lookup"><span data-stu-id="52223-118">The Kaizala API runs on the secure Microsoft Azure cloud, and interacts with the Kaizala platform to perform various actions for end users.</span></span>
<span data-ttu-id="52223-119">Die API funktioniert mit den folgenden Kaizala Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="52223-119">The API works with the following Kaizala resources:</span></span>

*   [<span data-ttu-id="52223-120">Locations</span><span class="sxs-lookup"><span data-stu-id="52223-120">/groups</span></span>](groups.md)
*   [<span data-ttu-id="52223-121">/subGroups</span><span class="sxs-lookup"><span data-stu-id="52223-121">/subGroups</span></span>](subGroups.md)
*   [<span data-ttu-id="52223-122">/Members</span><span class="sxs-lookup"><span data-stu-id="52223-122">/members</span></span>](members.md)
*   [<span data-ttu-id="52223-123">/Messages</span><span class="sxs-lookup"><span data-stu-id="52223-123">/messages</span></span>](messages.md)
*   [<span data-ttu-id="52223-124">/Media</span><span class="sxs-lookup"><span data-stu-id="52223-124">/media</span></span>](media.md)
*   [<span data-ttu-id="52223-125">/Actions</span><span class="sxs-lookup"><span data-stu-id="52223-125">/actions</span></span>](actions.md)
*   [<span data-ttu-id="52223-126">/Subscribers</span><span class="sxs-lookup"><span data-stu-id="52223-126">/subscribers</span></span>](subscribers.md)
*    [<span data-ttu-id="52223-127">/Reaction</span><span class="sxs-lookup"><span data-stu-id="52223-127">/reaction</span></span>](reactions.md)

### <a name="webhooks"></a><span data-ttu-id="52223-128">WebHooks</span><span class="sxs-lookup"><span data-stu-id="52223-128">WebHooks</span></span>

<span data-ttu-id="52223-129">Die Microsoft Kaizala API bietet ebenfalls eine Möglichkeit für Entwickler für bestimmte Ereignisse in der Kaizala-Plattform über WebHooks registriert.</span><span class="sxs-lookup"><span data-stu-id="52223-129">The Microsoft Kaizala API also provides a way for developers to register for specific events within the Kaizala platform via WebHooks.</span></span>

*   [<span data-ttu-id="52223-130">/webhook</span><span class="sxs-lookup"><span data-stu-id="52223-130">/webhook</span></span>](webHooks.md)

### <a name="postman-collection"></a><span data-ttu-id="52223-131">Postman-Auflistung</span><span class="sxs-lookup"><span data-stu-id="52223-131">Postman Collection</span></span>

<span data-ttu-id="52223-132">Um unsere APIs testen als auch Kaizala API-Schema kennen, können Sie Postman-Auflistung enthält Beispiele und das Schema für die Microsoft Kaizala-apis importieren:</span><span class="sxs-lookup"><span data-stu-id="52223-132">In order to test our APIs, as well as understand Kaizala API schema, you can import postman collection containing samples and schema for all the Microsoft Kaizala apis:</span></span>


<span data-ttu-id="52223-133">[![Führen Sie im Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span><span class="sxs-lookup"><span data-stu-id="52223-133">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)</span></span>

<span data-ttu-id="52223-134">Legen Sie folgende Umgebungsvariablen in "Kaizala-APIs-Umgebung" vor dem Ausführen des Projekts Postman:</span><span class="sxs-lookup"><span data-stu-id="52223-134">Please set following environment variables in "Kaizala-APIs-environment" before running the postman project:</span></span>
* <span data-ttu-id="52223-135">Telefon (Mobil): Ihre Mobiltelefonnummer handelt, die für das Aufrufen von apis verwendet wird</span><span class="sxs-lookup"><span data-stu-id="52223-135">mobile-number : Your mobile number which will be used for invoking apis</span></span>
* <span data-ttu-id="52223-136">Id der Anwendung: ID der Verbindung zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="52223-136">application-id : ID associated with the Connector</span></span>
* <span data-ttu-id="52223-137">Anwendung-Schlüssel: geheimen Schlüssel den Connector zugeordnet</span><span class="sxs-lookup"><span data-stu-id="52223-137">application-secret : Secret associated with the Connector</span></span>

<span data-ttu-id="52223-138">Andere Umgebungsvariablen werden automatisch aufgefüllt beim Versuch der apis in Sequenz Erwähnung in Postman Projekt.</span><span class="sxs-lookup"><span data-stu-id="52223-138">Other enviroment variables will be auto-populated while trying the apis in sequence mention in Postman Project.</span></span> 

### <a name="getting-started-with-kaizala-rest-apis"></a><span data-ttu-id="52223-139">Erste Schritte mit Kaizala REST-APIs</span><span class="sxs-lookup"><span data-stu-id="52223-139">Getting started with Kaizala REST APIs</span></span> 

[<span data-ttu-id="52223-140">C#-Beispiel (freigegeben)</span><span class="sxs-lookup"><span data-stu-id="52223-140">C# sample (shared)</span></span>](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
