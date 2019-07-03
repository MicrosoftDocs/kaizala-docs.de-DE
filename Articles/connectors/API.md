---
title: Kaizala-APIs
description: Liste der APIs, die von Kaizala verfügbar gemacht werden, um die Integration mit Drittanbietersystemen zu ermöglichen
topic: Reference
author: nitinjms
ms.openlocfilehash: 221d421feeeb2528f185fa205c7cfa81207a8478
ms.sourcegitcommit: 7f642489150d68013f55d6ad11a6bd6dde185036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "35535684"
---
# <a name="kaizala-api-documentation"></a>Kaizala-API-Dokumentation

Lesen Sie vor dem ersten Start die Informationen unter [Setup für die Verwendung der Kaizala](setup.md) -Connectors.

## <a name="root-domain"></a>Stammdomäne

Die Stammdomäne zum Aufrufen der Kaizala-APIs lautet:

    {endpoint-url}
    
|               | Parameter             | Typ      | Optional?     | Beschreibung |
| :---: | :---: | :---: | :---: | :--- |
| Endpunkt-URL  | `endpoint-url`        | String    | Nein            | Bei erfolgreicher Authentifizierung beim Generieren von Zugriffstoken wird eine Endpunkt-URL zurückgegeben, die als API-base-URL für nachfolgende API-Aufrufe verwendet werden sollte.    |

Beachten Sie, dass Sie beim Treffen einer beliebigen Kaizala-API den HTTP-Statuscode: 308 abrufen können, der angibt, dass die Endpunkt-URL des Benutzers geändert wurde. In diesem Fall wird der Speicherort der Antwort Kopfzeile die neue Endpunkt-URL enthalten.

### <a name="api-end-points"></a>End-Points-API

Die Kaizala-API wird auf der Secure Microsoft Azure Cloud ausgeführt und interagiert mit der Kaizala-Plattform, um verschiedene Aktionen für Endbenutzer auszuführen.
Die API funktioniert mit den folgenden Kaizala-Ressourcen:

*   [/Groups](groups.md)
*   [/subGroups](subGroups.md)
*   [/members](members.md)
*   [/messages](messages.md)
*   [/Media](media.md)
*   [/actions](actions.md)
*   [/subscribers](subscribers.md)
*    [/reaction](reactions.md)

### <a name="webhooks"></a>WebHooks

Die Microsoft Kaizala-API bietet Entwicklern auch die Möglichkeit, sich über webhooks für bestimmte Ereignisse in der Kaizala-Plattform zu registrieren.

*   [/webhook](webHooks.md)

### <a name="postman-collection"></a>Postman-Sammlung

Um unsere APIs zu testen und das Kaizala-API-Schema zu verstehen, können Sie die Postman-Auflistung mit Beispielen und Schema für alle Microsoft Kaizala-APIs importieren:


[![In Postman ausführen](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=)

Legen Sie die folgenden Umgebungsvariablen in "Kaizala-APIs-Environment" fest, bevor Sie das Postman-Projekt ausführen:
* Mobiltelefonnummer: Ihre Mobiltelefonnummer, die zum Aufrufen von APIs verwendet wird
* Application-ID: ID, die dem Connector zugeordnet ist
* Anwendungs Geheimnis: mit dem Connector verknüpfte Verschlüsselungsschlüssel

Andere Umgebungsvariablen werden automatisch aufgefüllt, während Sie die APIs in der Reihenfolge Erwähnung im Postman-Projekt ausprobieren. 

### <a name="getting-started-with-kaizala-rest-apis"></a>Erste Schritte mit Kaizala-Rest-APIs 

[C#-Beispiel (Shared)](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Gettingstartedwith.docx)
