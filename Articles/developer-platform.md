---
title: Übersicht
description: Übersicht über die Microsoft Kaizala-Entwicklerplattform
topic: overview
author: nitinjms
ms.openlocfilehash: 74d0cb957b81354c6f9d7c359eccf554910d283d
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190700"
---
# <a name="microsoft-kaizala-developer-documentation"></a><span data-ttu-id="995e7-103">Microsoft Kaizala-Entwicklerdokumentation</span><span class="sxs-lookup"><span data-stu-id="995e7-103">Microsoft Kaizala Developer Documentation</span></span>

<span data-ttu-id="995e7-104">Kaizala ist eine APP für Messaging und Produktivität, mit deren Hilfe Mobile Benutzer mehr erreichen können.</span><span class="sxs-lookup"><span data-stu-id="995e7-104">Kaizala is a messaging and productivity app that enable your mobile users to achieve more.</span></span> <span data-ttu-id="995e7-105">Mit Kaizala können Sie 1:1 Chat mit Einzelpersonen, Gruppenchat mit ihren Teams und sogar Gruppen zu Ihren vorhandenen Gruppen hinzufügen, um in größeren Organisationen oder Gemeinden zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="995e7-105">With Kaizala, you can have 1:1 chat with individuals, group chat with your teams, and even add groups to your existing groups to communicate within large organizations or communities.</span></span>

> <span data-ttu-id="995e7-106">**Sie haben keine Kaizala? Laden Sie die APP jetzt für Windows Phone, Android & iOS. [So wird es gemacht](install.md).**</span><span class="sxs-lookup"><span data-stu-id="995e7-106">**Don't have Kaizala? Download the app now for Windows Phone, Android & iOS. [Here's how](install.md).**</span></span>

## <a name="microsoft-kaizala-developer-platform"></a><span data-ttu-id="995e7-107">Microsoft Kaizala-Entwicklerplattform</span><span class="sxs-lookup"><span data-stu-id="995e7-107">Microsoft Kaizala Developer Platform</span></span> 
<span data-ttu-id="995e7-108">Die Kaizala-Entwicklerplattform bietet mehrere Möglichkeiten zum integrieren und Erweitern von Kaizala für die Anforderungen Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="995e7-108">The Kaizala Developer Platform offers multiple ways to integrate and extend Kaizala to suit your organizational needs.</span></span> <span data-ttu-id="995e7-109">Mit der Entwicklervorschau können Sie Connectors verwenden, um Kaizala in Ihre Geschäftsprozesse zu integrieren und benutzerdefinierte Aktionen über das Kaizala-Verwaltungs Portal zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="995e7-109">With the developer preview, you can use Connectors to integrate Kaizala with your business processes and design custom Actions through the Kaizala Management Portal.</span></span>

## <a name="connectors"></a><span data-ttu-id="995e7-110">Connectors</span><span class="sxs-lookup"><span data-stu-id="995e7-110">Connectors</span></span>

<span data-ttu-id="995e7-111">Kaizala-Connectors ermöglichen Drittanbieterentwicklern, Kaizala in Ihre Geschäftsprozesse zu integrieren, indem Sie die Möglichkeit bieten, eine kuratierte Reihe von Aktionen in Kaizala mithilfe von REST-basierten API-aufrufen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="995e7-111">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="995e7-112">Der Anwendungsbereich der API ist für externe Systeme zum Aufrufen des Endpunkts und zum Ausführen von Aktionen bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="995e7-112">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="995e7-113">Das heißt, es handelt sich dabei um ein PULL-Modell, bei dem einzelne Endpunkte aufgerufen werden müssen, um bestimmte Aktionen mithilfe von Kaizala- **[APIs](connectors/API.md)** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="995e7-113">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](connectors/API.md)**.</span></span> <span data-ttu-id="995e7-114">Das PUSH-Modell, mit dem die Kaizala-Plattform Aktionen auslösen **[](connectors/webHooks.md)** kann, kann mit webhooks konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="995e7-114">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](connectors/webHooks.md)**.</span></span>

[<span data-ttu-id="995e7-115">Erste Schritte mit Connectors</span><span class="sxs-lookup"><span data-stu-id="995e7-115">Get started with Connectors</span></span>](connectors/README.md)

## <a name="kaizala-actions"></a><span data-ttu-id="995e7-116">Kaizala-Aktionen</span><span class="sxs-lookup"><span data-stu-id="995e7-116">Kaizala Actions</span></span>

<span data-ttu-id="995e7-117">Kaizala-Aktionen sind einfache "Arbeitseinheiten", die Benutzern bei der Arbeit innerhalb eines Unterhaltungs Kontexts innerhalb von Kaizala helfen.</span><span class="sxs-lookup"><span data-stu-id="995e7-117">Kaizala Actions are basic 'units of work' that help users get work done within a conversation context inside Kaizala.</span></span> <span data-ttu-id="995e7-118">Einige dieser Aktionen wie Job, Umfrage, Umfrage usw. werden in der Box ausgeliefert und bieten eine umfangreichere Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="995e7-118">Some of these Actions like Job, Survey, Poll, etc. are shipped out-of-the-box and provide scoped functionality.</span></span> <span data-ttu-id="995e7-119">Diese Aktionen können innerhalb der Kaizala-App ermittelt werden und können in einem Unterhaltungs Kontext aus der Aktions Palette aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="995e7-119">These Actions can be discovered within the Kaizala app and can be invoked in a conversation context from the Action Palette.</span></span>

[<span data-ttu-id="995e7-120">Erste Schritte mit Kaizala-Aktionen</span><span class="sxs-lookup"><span data-stu-id="995e7-120">Get started with Kaizala Actions</span></span>](Actions/README.md)

## <a name="submit-your-questions-bugs-feature-requests-and-contributions"></a><span data-ttu-id="995e7-121">ÜberMitteln von Fragen, Bugs, Feature-Anfragen und Beiträgen</span><span class="sxs-lookup"><span data-stu-id="995e7-121">Submit your questions, bugs, feature requests, and contributions</span></span>

<span data-ttu-id="995e7-122">Wir hören der Entwicklercommunity über [mehrere Kanäle](feedback.md)zu.</span><span class="sxs-lookup"><span data-stu-id="995e7-122">We listen to the developer community across [several channels](feedback.md).</span></span>
