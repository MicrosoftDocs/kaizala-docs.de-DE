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
# <a name="connectors"></a>Connectors

## <a name="overview"></a>Übersicht
Kaizala Connectors ermöglichen es 3. Partei Entwicklern integrieren Kaizala in ihre Geschäftsprozesse durch bereitstellen, dass die Möglichkeit zum Ausführen einer curated Reihe von Aktionen in Kaizala mithilfe von REST-API-Aufrufe basiert. Der Bereich der API ist für externe Systeme zum Aufrufen des Endpunkt und Ausführen von Aktionen auf Abruf. D. h., wird dies eine PULL-Modell – sein, in denen einzelne Endpunkte aufgerufen werden, um bestimmte Aktionen Kaizala **[APIs](API.md)** ausführen müssen. Das PUSH-Modell, in dem Kaizala Plattform Aktionen auslösen kann, kann mithilfe von **[Webhooks](webHooks.md)** konfiguriert werden.

Kaizala Verbinder sind derzeit Gruppe-bezogenen – d. h. jeder Kaizala Connector muss explizit Berechtigungen erteilt werden, zu einer Unterhaltung Gruppe - und Aktionen über die API-Endpunkte nur im Kontext der Gruppe dann ausführen können. Jedoch kann jedes Kaizala Connector Zugriff zu mehreren Gruppen gewährt werden.

* [Setup für die Verwendung der Kaizala-Connectors](setup.md)
* [API-Dokumentation](API.md)
* [Weitere Informationen zu Connectors](https://support.office.com/en-US/article/Kaizala-Connectors-223791c8-718d-4669-8c5e-a76804ae1ddd)
