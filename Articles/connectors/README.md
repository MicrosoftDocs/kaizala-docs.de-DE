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
# <a name="connectors"></a>Connectors

## <a name="overview"></a>Übersicht
Kaizala-Connectors ermöglichen Drittanbieterentwicklern, Kaizala in Ihre Geschäftsprozesse zu integrieren, indem Sie die Möglichkeit bieten, eine kuratierte Reihe von Aktionen in Kaizala mithilfe von REST-basierten API-aufrufen durchzuführen. Der Anwendungsbereich der API ist für externe Systeme zum Aufrufen des Endpunkts und zum Ausführen von Aktionen bei Bedarf. Das heißt, es handelt sich dabei um ein PULL-Modell, bei dem einzelne Endpunkte aufgerufen werden müssen, um bestimmte Aktionen mithilfe von Kaizala- **[APIs](API.md)** auszuführen. Das PUSH-Modell, mit dem die Kaizala-Plattform Aktionen auslösen **[](webHooks.md)** kann, kann mit webhooks konfiguriert werden.

Kaizala-Connectors sind derzeit Gruppen bezogen, d. h., jeder Kaizala-Connector muss explizit Berechtigungen für eine Konversationsgruppe erhalten und kann dann nur innerhalb des Kontexts der Gruppe Aktionen über die Endpunkte der API ausführen. Jedem Kaizala-Connector kann jedoch der Zugriff auf mehrere Gruppen gewährt werden.

* [Setup für die Verwendung der Kaizala-Connectors](setup.md)
* [API-Dokumentation](API.md)
* [Weitere Informationen zu Connectors](https://support.office.com/en-US/article/Kaizala-Connectors-223791c8-718d-4669-8c5e-a76804ae1ddd)
