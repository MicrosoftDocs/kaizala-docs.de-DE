---
title: Connectors
description: Artikel zum Bereitstellen von Übersicht über Kaizala connectors
topic: Overview
author: nitinjms
ms.openlocfilehash: 94c6844cfa8f5a85da26c3ab27dc38a366fbc97e
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905314"
---
# <a name="connectors"></a><span data-ttu-id="cf7b4-103">Connectors</span><span class="sxs-lookup"><span data-stu-id="cf7b4-103">Connectors</span></span>

## <a name="overview"></a><span data-ttu-id="cf7b4-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="cf7b4-104">Overview</span></span>
<span data-ttu-id="cf7b4-105">Kaizala Connectors ermöglichen es 3. Partei Entwicklern integrieren Kaizala in ihre Geschäftsprozesse durch bereitstellen, dass die Möglichkeit zum Ausführen einer curated Reihe von Aktionen in Kaizala mithilfe von REST-API-Aufrufe basiert.</span><span class="sxs-lookup"><span data-stu-id="cf7b4-105">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="cf7b4-106">Der Bereich der API ist für externe Systeme zum Aufrufen des Endpunkt und Ausführen von Aktionen auf Abruf.</span><span class="sxs-lookup"><span data-stu-id="cf7b4-106">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="cf7b4-107">D. h., wird dies eine PULL-Modell – sein, in denen einzelne Endpunkte aufgerufen werden, um bestimmte Aktionen Kaizala **[APIs](API.md)** ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="cf7b4-107">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](API.md)**.</span></span> <span data-ttu-id="cf7b4-108">Das PUSH-Modell, in dem Kaizala Plattform Aktionen auslösen kann, kann mithilfe von **[Webhooks](webHooks.md)** konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cf7b4-108">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](webHooks.md)**.</span></span>

<span data-ttu-id="cf7b4-109">Kaizala Verbinder sind derzeit Gruppe-bezogenen – d. h. jeder Kaizala Connector muss explizit Berechtigungen erteilt werden, zu einer Unterhaltung Gruppe - und Aktionen über die API-Endpunkte nur im Kontext der Gruppe dann ausführen können.</span><span class="sxs-lookup"><span data-stu-id="cf7b4-109">Kaizala Connectors are currently group-scoped - i.e. each Kaizala Connector needs to explicitly be granted permissions to a Conversation group - and then can perform actions through the API end-points only within the context of the group.</span></span> <span data-ttu-id="cf7b4-110">Jedoch kann jedes Kaizala Connector Zugriff zu mehreren Gruppen gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="cf7b4-110">However, each Kaizala Connector can be granted access to multiple groups.</span></span>

* [<span data-ttu-id="cf7b4-111">Setup für die Verwendung der Kaizala-Connectors</span><span class="sxs-lookup"><span data-stu-id="cf7b4-111">Setup for using the Kaizala Connectors</span></span>](setup.md)
* [<span data-ttu-id="cf7b4-112">API-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="cf7b4-112">API Documentation</span></span>](API.md)
* [<span data-ttu-id="cf7b4-113">Weitere Informationen zu Connectors</span><span class="sxs-lookup"><span data-stu-id="cf7b4-113">Read more about Connectors</span></span>](https://support.office.com/en-US/article/Kaizala-Connectors-223791c8-718d-4669-8c5e-a76804ae1ddd)
