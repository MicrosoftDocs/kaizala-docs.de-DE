---
title: Übersicht
description: Übersicht über Microsoft Kaizala Developer-Plattform
topic: overview
author: nitinjms
ms.openlocfilehash: 74d0cb957b81354c6f9d7c359eccf554910d283d
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905338"
---
# <a name="microsoft-kaizala-developer-documentation"></a><span data-ttu-id="aaae5-103">Microsoft Kaizala-Entwicklerdokumentation</span><span class="sxs-lookup"><span data-stu-id="aaae5-103">Microsoft Kaizala Developer Documentation</span></span>

<span data-ttu-id="aaae5-104">Kaizala ist eine messaging und Produktivität app, mit denen mobile Benutzer mehr erreichen können.</span><span class="sxs-lookup"><span data-stu-id="aaae5-104">Kaizala is a messaging and productivity app that enable your mobile users to achieve more.</span></span> <span data-ttu-id="aaae5-105">Mit Kaizala können Sie 1:1 chatten mit Personen, mit Ihren Teams Gruppenchat haben und sogar Hinzufügen von Gruppen zu Ihrer vorhandenen Gruppen in großen Organisationen oder Communitys kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="aaae5-105">With Kaizala, you can have 1:1 chat with individuals, group chat with your teams, and even add groups to your existing groups to communicate within large organizations or communities.</span></span>

> <span data-ttu-id="aaae5-106">**Sie haben keinen Kaizala? Jetzt herunterladen der app für Windows Phone, Android & iOS. [Sieht wie](install.md).**</span><span class="sxs-lookup"><span data-stu-id="aaae5-106">**Don't have Kaizala? Download the app now for Windows Phone, Android & iOS. [Here's how](install.md).**</span></span>

## <a name="microsoft-kaizala-developer-platform"></a><span data-ttu-id="aaae5-107">Blog des Microsoft Kaizala-Plattform</span><span class="sxs-lookup"><span data-stu-id="aaae5-107">Microsoft Kaizala Developer Platform</span></span> 
<span data-ttu-id="aaae5-108">Die Kaizala Developer-Plattform bietet mehrere Methoden zum integrieren und Kaizala, um den Bedürfnissen Ihrer Organisation zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aaae5-108">The Kaizala Developer Platform offers multiple ways to integrate and extend Kaizala to suit your organizational needs.</span></span> <span data-ttu-id="aaae5-109">Mit der Preview für Entwickler können Sie Connectors zum Integrieren von Kaizala in Ihre Geschäftsprozesse und Entwerfen benutzerdefinierte Aktionen über dem Kaizala-Verwaltungsportal.</span><span class="sxs-lookup"><span data-stu-id="aaae5-109">With the developer preview, you can use Connectors to integrate Kaizala with your business processes and design custom Actions through the Kaizala Management Portal.</span></span>

## <a name="connectors"></a><span data-ttu-id="aaae5-110">Connectors</span><span class="sxs-lookup"><span data-stu-id="aaae5-110">Connectors</span></span>

<span data-ttu-id="aaae5-111">Kaizala Connectors ermöglichen es 3. Partei Entwicklern integrieren Kaizala in ihre Geschäftsprozesse durch bereitstellen, dass die Möglichkeit zum Ausführen einer curated Reihe von Aktionen in Kaizala mithilfe von REST-API-Aufrufe basiert.</span><span class="sxs-lookup"><span data-stu-id="aaae5-111">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="aaae5-112">Der Bereich der API ist für externe Systeme zum Aufrufen des Endpunkt und Ausführen von Aktionen auf Abruf.</span><span class="sxs-lookup"><span data-stu-id="aaae5-112">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="aaae5-113">D. h., wird dies eine PULL-Modell – sein, in denen einzelne Endpunkte aufgerufen werden, um bestimmte Aktionen Kaizala **[APIs](connectors/API.md)** ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="aaae5-113">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](connectors/API.md)**.</span></span> <span data-ttu-id="aaae5-114">Das PUSH-Modell, in dem Kaizala Plattform Aktionen auslösen kann, kann mithilfe von **[Webhooks](connectors/webHooks.md)** konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="aaae5-114">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](connectors/webHooks.md)**.</span></span>

[<span data-ttu-id="aaae5-115">Erste Schritte mit Connectors</span><span class="sxs-lookup"><span data-stu-id="aaae5-115">Get started with Connectors</span></span>](connectors/README.md)

## <a name="kaizala-actions"></a><span data-ttu-id="aaae5-116">Kaizala Aktionen</span><span class="sxs-lookup"><span data-stu-id="aaae5-116">Kaizala Actions</span></span>

<span data-ttu-id="aaae5-117">Kaizala Aktionen sind grundlegende 'Arbeitseinheiten', mit denen Benutzer in einem Unterhaltungskontext innerhalb Kaizala Arbeit vermitteln.</span><span class="sxs-lookup"><span data-stu-id="aaae5-117">Kaizala Actions are basic 'units of work' that help users get work done within a conversation context inside Kaizala.</span></span> <span data-ttu-id="aaae5-118">Einige dieser Aktionen wie Auftrag, Umfrage, Umfrage usw. sind gelieferten Out-of-the-Box und verfügen über dieselbe Funktionalität bereichsbezogenen.</span><span class="sxs-lookup"><span data-stu-id="aaae5-118">Some of these Actions like Job, Survey, Poll, etc. are shipped out-of-the-box and provide scoped functionality.</span></span> <span data-ttu-id="aaae5-119">Diese Aktionen innerhalb der app Kaizala ermittelt werden können und in einem Unterhaltungskontext aus der Palette Aktion aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="aaae5-119">These Actions can be discovered within the Kaizala app and can be invoked in a conversation context from the Action Palette.</span></span>

[<span data-ttu-id="aaae5-120">Erste Schritte mit Kaizala Aktionen</span><span class="sxs-lookup"><span data-stu-id="aaae5-120">Get started with Kaizala Actions</span></span>](Actions/README.md)

## <a name="submit-your-questions-bugs-feature-requests-and-contributions"></a><span data-ttu-id="aaae5-121">Senden Sie Ihre Fragen, Fehlern, Anfragen zu Features und Beiträge</span><span class="sxs-lookup"><span data-stu-id="aaae5-121">Submit your questions, bugs, feature requests, and contributions</span></span>

<span data-ttu-id="aaae5-122">Wir hören über [mehrere Kanäle](feedback.md)für die Entwicklercommunity.</span><span class="sxs-lookup"><span data-stu-id="aaae5-122">We listen to the developer community across [several channels](feedback.md).</span></span>
