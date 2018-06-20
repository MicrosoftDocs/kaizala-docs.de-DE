---
title: Kaizala-APIs
description: Liste der APIs, Kaizala verfügbar macht, um die Integration mit 3. Partei Systemen ermöglichen
topic: Reference
author: nitinjms
ms.openlocfilehash: 06cb4b8d4883d0d9a50479cf9c9da048cc42e3a7
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905303"
---
# <a name="kaizala-api-documentation"></a>Kaizala API-Dokumentation

Bevor Sie beginnen, finden Sie in [Setup für die Verwendung der Kaizala-Connectors](setup.md)

## <a name="root-domain"></a>Stammdomäne

Die Stammdomäne für das Aufrufen der Kaizala-APIs ist:

    {endpoint-url}
    
|               | Parameter             | Typ      | Optional?     | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| Endpunkt-url  | `endpoint-url`        | String    | Nein            | Erfolgreiche Authentifizierung beim Generieren von Zugriffstoken ist eine Endpunkt-Url zurückgegeben, für nachfolgende API-Aufrufe, die als api-Basis-Url verwendet werden sollten    |

Beachten Sie, dass beim Drücken einer beliebigen Kaizala-api, Sie HTTP-Status Code: 308 zurück, der angibt, dass der Benutzer Endpunkt-Url geändert hat abrufen können. In diesem Fall wird Antwort Kopfzeile Speicherort die neue Endpunkt-Url enthalten.

### <a name="api-end-points"></a>API-Endgeräte

Die Kaizala-API auf der sicheren Microsoft Azure-Cloud ausgeführt wird, und mit der Kaizala-Plattform für verschiedene Aktionen für Endbenutzer interagiert.
Die API funktioniert mit den folgenden Kaizala Ressourcen:

*   [Locations](groups.md)
*   [/subGroups](subGroups.md)
*   [/Members](members.md)
*   [/Messages](messages.md)
*   [/Media](media.md)
*   [/Actions](actions.md)
*   [/Subscribers](subscribers.md)

### <a name="webhooks"></a>WebHooks

Die Microsoft Kaizala API bietet ebenfalls eine Möglichkeit für Entwickler für bestimmte Ereignisse in der Kaizala-Plattform über WebHooks registriert.

*   [/webhook](webHooks.md)

### <a name="postman-collection"></a>Postman-Auflistung

Um unsere APIs testen als auch Kaizala API-Schema kennen, können Sie Postman-Auflistung enthält Beispiele und das Schema für die Microsoft Kaizala-apis importieren:


[![Führen Sie im Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)

Legen Sie folgende Umgebungsvariablen in "Kaizala-APIs-Umgebung" vor dem Ausführen des Projekts Postman:
* Telefon (Mobil): Ihre Mobiltelefonnummer handelt, die für das Aufrufen von apis verwendet wird
* Id der Anwendung: ID der Verbindung zugeordnet ist
* Anwendung-Schlüssel: geheimen Schlüssel den Connector zugeordnet

Andere Umgebungsvariablen werden automatisch aufgefüllt beim Versuch der apis in Sequenz Erwähnung in Postman Projekt. 

### <a name="getting-started-with-kaizala-rest-apis"></a>Erste Schritte mit Kaizala REST-APIs 

[C#-Beispiel (freigegeben)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)
