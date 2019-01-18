---
ms.openlocfilehash: de0df75d7a62fda9ea6ff5625fbef94774069cfd
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727719"
---
## <a name="kas-client"></a>KAS Client

KAS Client-SDK stellt eine Brücke zwischen der Kaizala app native-Schnittstelle (Objective-C für iOS, Java für Android) und die Kaizala Aktion Javascript.

Im Allgemeinen gibt es werden KASClient APIs in zwei Kategorien unterteilt:
1.  **Formular-APIs**: jede Aktion Unterhaltung Karte ein Form-Objekt zugeordnet ist. Ein Formular definiert das Verhalten der Aktion. Um eine Aktionsinstanz erstellen, die Sie ein Form-Objekt zu initialisieren müssen, tragen Sie erforderlichen Informationen und übergeben sie dann als eine Anforderung an den jeweiligen Unterhaltung. Teilnehmer an der Unterhaltung können auf das Formular Antworten oder finden Sie unter der aggregierten Zusammenfassung aller Antworten. Diese APIs wurden zum Umgang mit alles im Zusammenhang mit Formularen erstellt. Basierend auf verschiedenen fließt, können diese weiter Unterseite kategorisierten in sein:
    *   **Erstellung Fluss APIs**: durch Tippen auf die Aktion-Symbol in der Palette seiner Erstellung Flow startet. Verwenden diese APIs können Sie ein Form-Objekt zu initialisieren, es bearbeiten und als Anforderung zu übermitteln.
    *   **Antwort Fluss APIs**: durch Tippen auf die Schaltfläche Respond einer Aktion Karte seine Antwort Flow startet. Mit diesen APIs können Sie das zugeordnete Form-Objekt, die vorherigen Antworten abrufen und übermitteln eine neue Antwort.
    *   **Zusammenfassung flow APIs**: durch Tippen auf die Schaltfläche "Zusammenfassung", einer Aktion Karte startet Zusammenfassung Fluss. Mit diesen APIs können Sie das zugeordnete Form-Objekt, die aggregierten Antworten von den Teilnehmern abrufen und wählen Sie zum Schließen des Formulars, damit weitere Antworten nicht zulässig sind.
    
2.  **App-APIs**: Hierbei handelt es sich um APIs, die für die Interaktion mit systemeigenen der Kaizala-Client-Schnittstelle und Abrufen von erforderlichen Informationen verwendet werden kann. Dazu gehören generischen APIs, wie Kontaktauswahl, anzeigen Bildauswahl, Pfad für aktuellen Get, app Gebietsschema. Diese APIs können in einem der oben genannten Datenflüsse verwendet werden.

Sie können [hier](https://manage.kaiza.la/MiniApps/DownloadSDK) die aktuelle KASClient Javascript-Datei herunterladen.

## <a name="api-reference"></a>API-Referenz

*   [Formular Erstellung Fluss APIs](generated/modules/kasclient.form.md#creation)
*   [Formular Antwort Fluss APIs](generated/modules/kasclient.form.md#response)
*   [Formular Zusammenfassung flow APIs](generated/modules/kasclient.form.md#summary)
*   [App-APIs](generated/modules/kasclient.app.md)

## <a name="object-reference"></a>Objektverweis

Verweise auf alle Objekte im SDK stehen [hier](objects.md).
