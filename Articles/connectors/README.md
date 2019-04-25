---
title: Connectors
description: Artikel zur Bereitstellung der Übersicht über Kaizala-Connectors
topic: Overview
author: nitinjms
ms.openlocfilehash: 94c6844cfa8f5a85da26c3ab27dc38a366fbc97e
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190796"
---
# <a name="connectors"></a><span data-ttu-id="371fe-103">Connectors</span><span class="sxs-lookup"><span data-stu-id="371fe-103">Connectors</span></span>

## <a name="overview"></a><span data-ttu-id="371fe-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="371fe-104">Overview</span></span>
<span data-ttu-id="371fe-105">Kaizala-Connectors ermöglichen Drittanbieterentwicklern, Kaizala in Ihre Geschäftsprozesse zu integrieren, indem Sie die Möglichkeit bieten, eine kuratierte Reihe von Aktionen in Kaizala mithilfe von REST-basierten API-aufrufen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="371fe-105">Kaizala Connectors enable 3rd party developers to integrate Kaizala into their business processes by providing the ability to perform a curated set of actions in Kaizala using REST based API calls.</span></span> <span data-ttu-id="371fe-106">Der Anwendungsbereich der API ist für externe Systeme zum Aufrufen des Endpunkts und zum Ausführen von Aktionen bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="371fe-106">The scope of the API is for external systems to call the end-point and perform actions on-demand.</span></span> <span data-ttu-id="371fe-107">Das heißt, es handelt sich dabei um ein PULL-Modell, bei dem einzelne Endpunkte aufgerufen werden müssen, um bestimmte Aktionen mithilfe von Kaizala- **[APIs](API.md)** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="371fe-107">That is, this will be a PULL model – where individual endpoints need to be called to perform specific actions using Kaizala **[APIs](API.md)**.</span></span> <span data-ttu-id="371fe-108">Das PUSH-Modell, mit dem die Kaizala-Plattform Aktionen auslösen **[](webHooks.md)** kann, kann mit webhooks konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="371fe-108">The PUSH model where Kaizala platform can trigger actions can be configured using **[webhooks](webHooks.md)**.</span></span>

<span data-ttu-id="371fe-109">Kaizala-Connectors sind derzeit Gruppen bezogen, d. h., jeder Kaizala-Connector muss explizit Berechtigungen für eine Konversationsgruppe erhalten und kann dann nur innerhalb des Kontexts der Gruppe Aktionen über die Endpunkte der API ausführen.</span><span class="sxs-lookup"><span data-stu-id="371fe-109">Kaizala Connectors are currently group-scoped - i.e. each Kaizala Connector needs to explicitly be granted permissions to a Conversation group - and then can perform actions through the API end-points only within the context of the group.</span></span> <span data-ttu-id="371fe-110">Jedem Kaizala-Connector kann jedoch der Zugriff auf mehrere Gruppen gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="371fe-110">However, each Kaizala Connector can be granted access to multiple groups.</span></span>

* [<span data-ttu-id="371fe-111">Setup für die Verwendung der Kaizala-Connectors</span><span class="sxs-lookup"><span data-stu-id="371fe-111">Setup for using the Kaizala Connectors</span></span>](setup.md)
* [<span data-ttu-id="371fe-112">API-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="371fe-112">API Documentation</span></span>](API.md)
* [<span data-ttu-id="371fe-113">Weitere Informationen zu Connectors</span><span class="sxs-lookup"><span data-stu-id="371fe-113">Read more about Connectors</span></span>](https://support.office.com/en-US/article/Kaizala-Connectors-223791c8-718d-4669-8c5e-a76804ae1ddd)
