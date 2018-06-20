---
title: /Actions
description: Referenzartikel für API zum Senden/Action-Instanzen abrufen
topic: Reference
author: nitinjms
ms.openlocfilehash: 6f58e45b9eb5d4a4987c3aeb36ff8fe1862fe7bc
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905326"
---
# <a name="api-to-sendretrieve-action-instances"></a>API zum Senden/Action-Instanzen abrufen
## <a name="actions"></a>/Actions
API-Endpunkt zu senden oder Instanzen von Kaizala Aktionen zu/aus der Unterhaltungsgruppen innerhalb Kaizala abgerufen. Aktuellen Bereich besteht darin, folgende Aktivitätstypen unterstützen:

| Aktion | ERSTE unterstützt | POST unterstützt. | Id |
| :---: | :---: | :---: | :---: |
| Bild Anlage | Ja | Ja | Abbildung |
| Audio-Anlage | Nein | Ja | audio |
| Dokument-Anlage | Nein | Ja | document |
| Kontakt in der Anlage | Nein | Nein | N/V |
| Auftrag | Ja | Ja | Auftrag |
| Umfrage | Ja | Ja | Umfrage |
| Foto mit Speicherort | Ja | Nein | photoWithLocation |
| Treffen wir uns | Ja | Ja | letsmeet |
| Schnelle Umfrage | Ja | Ja | Umfrage |
| Speicherort freigeben | Ja | Nein | shareLocation |
| Speicherort der Anforderung | Nein | Nein | N/V |
| Live-Speicherort | Nein | Nein | N/V |
| Announcement | Nein | Nein | N/V |


*   API zum Abrufen von [Aktionen](actions_get.md) und [Aktionsdetails](actionDetails.md)
*   [API neue Instanzen des Objekts Aktionen für die Bereitstellung](actions_post.md)
*   [API neue Aktion Antworten/bearbeiten vorhandene Aktion Antworten für die Bereitstellung](action_responses.md)
