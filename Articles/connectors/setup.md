---
title: Einrichten von Kaizala-Connectors
description: In diesem Artikel werden die Schritte zum Erstellen von Kaizala-Connectors und zum Generieren von Berechtigungstoken beschrieben.
topic: get-started-article
author: nitinjms
ms.openlocfilehash: e9f6551f4ae824a6da0ee4ee39f32cd2237486b6
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190798"
---
# <a name="setup-for-using-the-kaizala-connectors"></a>Setup für die Verwendung der Kaizala-Connectors

## <a name="personas"></a>Personas

*   **Entwickler:** Interne oder Drittanbieter entwickelnde Anwendungen für die Organisation, die Kaizala in die Geschäftsprozesse der Organisation integrieren müssen. Der Entwickler hat beim Entwickeln der Anwendung keinen Zugriff auf den Endbenutzer (unterscheidet sich von einem Administrator).
*   **Administrator:** Benutzer, der Teil der Endgruppen ist und ein Administrator ist. Es wird erwartet, dass Gruppen Verwaltungsaufgaben ausgeführt werden.
*   **Benutzer:** Kaizala-Endbenutzer

## <a name="pre-req-to-set-up"></a>Vorab Anforderung für die Einrichtung

*   Als **Entwickler:**
    *   Ein Office365-Konto
    *   Eine registrierte Kaizala
    *   Entwicklungs-Set-up (jede Plattform) zum Aufrufen der REST-API
*   Als **Administrator**
    *   Ein Office365-Konto
    *   Eine registrierte Kaizala
    *   Administrator einer unterhaltungsgruppe innerhalb von Kaizala mit der registrierten Telefonnummer
*   Als **Benutzer**
    *   Eine registrierte Kaizala
    *   Mitglied einer unterhaltungsgruppe innerhalb von Kaizala mit der registrierten Telefonnummer

## <a name="set-up-steps-developer--group-admin"></a>Einrichten von Schritten (Entwickler-&-Gruppenadministrator)

Bei der Arbeit mit der Kaizala-Platt Form-API sind vier wichtige Infrastrukturkomponenten beteiligt:

*   **Connectors:** Alle 3rd-Party-Systeme, die mit Kaizala integriert werden müssen, müssen bei der Kaizala-Plattform als "Connector" registriert werden und erhalten API-Token, die dem Connector entsprechen.
*   **Kaizala-Verwaltungs Portal:** Ein Portal zum Registrieren der jeweiligen Drittanbieter-Connectors – und Zugriff auf Kaizala-Konversationsgruppen.
*   **Tokendienst:** Ein Endpunkt der URL, der von Drittanbieter-apps aufgerufen werden muss, um Zugriffstoken zu erhalten.
*   **Plattformdienst:** Ein URL-Endpunkt, der bestimmte Ressourcen für verschiedene Aktionen innerhalb von Kaizala verfügbar macht.
*   **Schritt 1: Registrieren eines Connectors für Entwickler**

    *   Entwickler navigiert zu Kaizala Management Portal @https://manage.kaiza.la/
    *   Anmelden mit einem vorhandenen Office365-Konto
    *   Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.
        *   Telefonnummer eingeben
        *   Tippen Sie auf "PIN generieren".
        *   ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer
    *   Tippen Sie im linken Menü auf "Connectors".
    *   Tippen Sie auf "Connector hinzufügen".
    *   Registrieren eines Connectors für das Drittanbietersystem, das die API verwendet
        *   Geben Sie den Namen des Connectors und weitere Details ein. Tippen Sie auf weiter
        *   Wählen Sie [Berechtigungen](permission.md) aus, die für den Connector vorgesehen sind, um Zugriff auf
        *   Tippen Sie auf Verbinder erstellen.
    *   Beachten Sie die ID & Secret, die generiert und im Portal angezeigt werden.

*   **Schritt 2: Gruppenadministrator erteilt den Connector-Zugriff auf seine Gruppe**

    *   Administrator navigiert zu Kaizala Management Portal @https://manage.kaiza.la/
    *   Anmelden mit einem vorhandenen Office365-Konto (SKU-festgelegt)
    *   Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.
        *   Telefonnummer eingeben
        *   Tippen Sie auf "PIN generieren".
        *   ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer
    *   Tippen Sie im linken Menü auf "Gruppen".
    *   Tippen Sie auf den Gruppennamen, auf den der Connector zugreifen muss.
    *   Tippen Sie auf "Connectors"
    *   Wählen Sie in der Dropdownliste den Connector aus, dem Sie Zugriff gewähren möchten.
    *   Tippen Sie auf "Connector hinzufügen".
    *   Hinweis das Aktualisierungs Token, das generiert und im Portal angezeigt wird

*   **Schritt 3: Gruppenadministrator teilt das Aktualisierungs Token mit dem App-Entwickler**

    *   Der Administrator muss das in Schritt 2 erhaltene Aktualisierungstoken manuell mit dem App-Entwickler freigeben.

*   **Schritt 4: App-Entwickler Ruft die Kaizala-Plattform-Rest-API zum Generieren von Zugriffs Token**

    *   Entwickler können nun das Aktualisierungstoken verwenden. eine Connector-ID und ein Connector Secret, um die REST-API aufzurufen, um Zugriffs Token zu generieren (Weitere Informationen finden Sie weiter unten)


Weiter: [Generate Access Token](Tokens.md)<br/>
Weitere Informationen: [API-Dokumentation](API.md)
