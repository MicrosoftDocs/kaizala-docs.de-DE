---
title: Kaizala-APIs
description: Liste der APIs, die von Kaizala verfügbar gemacht werden, um die Integration in Drittanbietersysteme zu ermöglichen
topic: Reference
author: nitinjms
ms.openlocfilehash: abedf063f7af73190dd3d5c2c748bc41d253a590
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190722"
---
# <a name="kaizala-api-documentation"></a>Kaizala-API-Dokumentation

Bevor Sie beginnen, lesen Sie [Setup für die Verwendung der Kaizala](setup.md) -Connectors

## <a name="root-domain"></a>Stammdomäne

Die Stammdomäne zum Aufrufen der Kaizala-APIs lautet:

    {endpoint-url}
    
|               | Parameter             | Typ      | Optional?     | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| Endpunkt-URL  | `endpoint-url`        | String    | Nein            | Bei erfolgreicher Authentifizierung beim Generieren von Zugriffstoken wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte.    |

Beachten Sie, dass beim Schlagen einer Kaizala-API der HTTP-Statuscode: 308 angezeigt wird, dass die Endpunkt-URL des Benutzers geändert wurde. In diesem Fall enthält der Speicherort des Antwortheaders die neue Endpunkt-URL.

### <a name="api-end-points"></a>API-Endpunkte

Die Kaizala-API wird in der sicheren Microsoft Azure-Cloud ausgeführt und interagiert mit der Kaizala-Plattform, um verschiedene Aktionen für Endbenutzer durchzuführen.
Die API kann mit den folgenden Kaizala-Ressourcen verwendet werden:

*   [/Groups](groups.md)
*   [/subGroups](subGroups.md)
*   [/Members](members.md)
*   [/Messages](messages.md)
*   [/Media](media.md)
*   [/Actions](actions.md)
*   [/Subscribers](subscribers.md)
*    [/Reaction](reactions.md)

### <a name="webhooks"></a>WebHooks

Die Microsoft Kaizala-API bietet Entwicklern auch eine Möglichkeit, sich über webHooks für bestimmte Ereignisse innerhalb der Kaizala-Plattform zu registrieren.

*   [/webhook](webHooks.md)

### <a name="postman-collection"></a>Postbote-Sammlung

Um unsere APIs zu testen und das Kaizala-API-Schema zu verstehen, können Sie die Postman-Auflistung mit Beispielen und Schema für alle Microsoft Kaizala-APIs importieren:


[![Ausführen in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)

Legen Sie die folgenden Umgebungsvariablen in "Kaizala-APIs-Environment" vor dem Ausführen des Postman-Projekts fest:
* Mobile-Number: Ihre Mobiltelefonnummer, die zum Aufrufen von APIs verwendet wird
* Application-ID: ID, die dem Connector zugeordnet ist
* Application-Secret: der Verbindung zugeordneter Schlüssel

Andere Umgebungsvariablen werden automatisch ausgefüllt, wenn Sie versuchen, die APIs in der Sequenz Erwähnung in Postman Projekt. 

### <a name="getting-started-with-kaizala-rest-apis"></a>Erste Schritte mit Kaizala-REST-APIs 

[C#-Beispiel (Shared)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
