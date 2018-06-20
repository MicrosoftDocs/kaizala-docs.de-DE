---
title: Einrichten von Kaizala Connectors
description: In diesem Artikel beschreiben die Schritte zum Erstellen Kaizala Connectors und zum Generieren der Permission-Token
topic: get-started-article
author: nitinjms
ms.openlocfilehash: f55d09c4619d6d17a997935ff937ae82cc560ceb
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905235"
---
# <a name="setup-for-using-the-kaizala-connectors"></a>Setup für die Verwendung der Kaizala-Connectors

## <a name="personas"></a>Personas

*   **Developer:** Interne oder 3. Partei Entwickeln von Anwendungen für die Organisation –, die in der Organisation von Geschäftsprozessen Kaizala integrieren müssen. Entwickler hat keinen Zugriff auf die Endbenutzer bei der Entwicklung der Anwendung (unterscheidet sich von einem Administrator).
*   **Admin:** Benutzer, der ist Bestandteil der End-Gruppen und ein Administrator ist. Wird zum Ausführen von Verwaltungsaufgaben für die Gruppe erwartet.
*   **Benutzer:** Endbenutzer Kaizala

## <a name="pre-req-to-set-up"></a>Voraussetzung einwahlseite

*   Als eine **Developer:**
    *   Ein Office365-Konto
    *   Eine Kaizala registriert Telefonnummer
    *   Dev Einrichtung (allen Plattformen) zum Aufrufen der REST-API
*   Als **Administrator**
    *   Ein Office365-Konto
    *   Eine Kaizala registriert Telefonnummer
    *   Admin einer Unterhaltung Gruppe innerhalb Kaizala mit der registrierten Telefonnummer
*   Als **Benutzer**
    *   Eine Kaizala registriert Telefonnummer
    *   Mitglied der Gruppe innerhalb Kaizala Unterhaltung mit der registrierten Telefonnummer

## <a name="set-up-steps-developer--group-admin"></a>Installationsschritte (für Entwickler & Gruppe Admin)

Es gibt vier wichtigsten Infrastrukturkomponenten Arbeitens mit Kaizala Platform-API:

*   **Connectors:** Alle 3. Partei Systeme, die mit Kaizala integrieren müssen müssen mit der Kaizala-Plattform als "Connector" registriert werden, und erhalten Sie API-Token an den Konnektor entspricht.
*   **Kaizala-Verwaltungsportal:** Portal zum Registrieren der jeweiligen 3. Partei Connectors – und stellen Sie ihnen den Zugriff auf Kaizala Unterhaltungsgruppen.
*   **-Tokens-Diensts:** Ein URL-Endpunkt, die von der 3. Partei apps abzurufenden Zugriffstoken aufgerufen werden muss.
*   **Platform Service:** Ein URL-Endpunkt die bestimmte Ressourcen, um verschiedene Aktionen innerhalb Kaizala verfügbar macht.
*   **Schritt 1: Entwickler registriert einen Connector**

    *   Entwickler navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/
    *   Melden Sie sich mit einem vorhandenen Office365-Konto
    *   Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal
        *   Geben Sie Telefonnummer
        *   Tippen Sie auf "PIN generieren"
        *   Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen
    *   Tippen Sie auf "Connectors" im linken Menü
    *   Tippen Sie auf "Connector hinzufügen"
    *   Registrieren Sie einen Connector für das 3. Partei-System, das die API verwenden
        *   Geben Sie den Namen des Connectors und andere Details. Tippen Sie auf Weiter.
        *   Wählen Sie Berechtigungen, mit denen bestimmt ist für den Zugriff auf den Connector
        *   Tippen Sie auf Connector erstellen
    *   Beachten Sie die ID & geheimen Schlüssel, die generiert abrufen und auf dem Portal angezeigt

*   **Schritt 2: Gruppe Admin "gewährt" Connector seinen Gruppe**

    *   Admin navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/
    *   Melden Sie sich mit einer vorhandenen Office365 Konto (SKU TBD)
    *   Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal
        *   Geben Sie Telefonnummer
        *   Tippen Sie auf "PIN generieren"
        *   Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen
    *   Tippen Sie auf "Groups" im linken Menü
    *   Tippen Sie auf den Namen der Gruppe, die vom Connector zugegriffen werden muss
    *   Tippen Sie auf "Connectors"
    *   Wählen Sie in der Dropdownliste den Konnektor, der Sie Zugriff zu gewähren möchten
    *   Tippen Sie auf "Connector hinzufügen"
    *   Beachten Sie die Refresh Token, die generiert dient zum Abrufen und auf dem Portal angezeigt

*   **Schritt 3: Gruppe Admin teilt Token aktualisieren, mit der App-Entwickler**

    *   Admin muss manuell freigeben der Aktualisierungstoken erhalten in Schritt2 mit dem app-Entwickler

*   **Schritt 4: App-Entwickler ruft der Kaizala Plattform Rest-API zum Generieren von Access-Token**

    *   Entwickler kann nun die Aktualisierungstoken verwenden. eine Connector-ID und geheimen Schlüssel Connector aufrufen, die REST-API Bankkontodaten zum Generieren von Access Token (Weitere Informationen weiter unten)


Weiter: [generieren Zugriffstoken](Tokens.md)<br/>
Mehr: [API-Dokumentation](API.md)
