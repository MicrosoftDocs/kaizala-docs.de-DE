---
title: /Actions
description: Referenzartikel zur API zum Senden/Abrufen von Aktionsinstanzen
topic: Reference
author: nitinjms
ms.openlocfilehash: da96b8dc40d10a8ff2a6ca05e493677bf236fd84
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190774"
---
# <a name="actions"></a>/Actions
API-Endpunkt zum Senden/Abrufen von Instanzen von Kaizala-Aktionen an/aus Konversationsgruppen innerhalb von Kaizala. Aktueller Bereich ist die Unterstützung der folgenden Aktionstypen:

| Aktion | Unterstützt | Unterstützte POST | Id |
| :---: | :---: | :---: | :---: |
| Bild Anlage | Ja | Ja | Abbildung |
| AudioAnlage | Nein | Ja | audio |
| Dokument Anlage | Nein | Ja | document |
| Kontakt Anlage | Nein | Nein | n/v |
| Auftrag | Ja | Ja | Job |
| Umfrage | Ja | Ja | Umfrage |
| Foto mit Standort | Ja | Nein | photoWithLocation |
| Let es Meet | Ja | Ja | letsmeet |
| Kurzumfrage | Ja | Ja | Abfragen |
| Freigabespeicherort | Ja | Nein | shareLocation |
| Anforderungs Speicherort | Nein | Nein | n/v |
| Live-Speicherort | Nein | Nein | n/v |
| Ankündigung | Nein | Nein | n/v |


*   API zum Abrufen von [Aktionen](actions_get.md) und [Aktionsdetails](actionDetails.md)
*   [API zum Bereitstellen neuer Instanzen von Aktionen](actions_post.md)
*   [API zum Veröffentlichen neuer Aktions Antworten/Bearbeiten vorhandener Aktions Antworten](action_responses.md)
