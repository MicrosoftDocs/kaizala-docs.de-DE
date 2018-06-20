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
# <a name="setup-for-using-the-kaizala-connectors"></a><span data-ttu-id="e6061-103">Setup für die Verwendung der Kaizala-Connectors</span><span class="sxs-lookup"><span data-stu-id="e6061-103">Setup for using the Kaizala Connectors</span></span>

## <a name="personas"></a><span data-ttu-id="e6061-104">Personas</span><span class="sxs-lookup"><span data-stu-id="e6061-104">Personas</span></span>

*   <span data-ttu-id="e6061-105">**Developer:** Interne oder 3. Partei Entwickeln von Anwendungen für die Organisation –, die in der Organisation von Geschäftsprozessen Kaizala integrieren müssen.</span><span class="sxs-lookup"><span data-stu-id="e6061-105">**Developer:** In-house or 3rd party developing applications for the organization – who need to integrate Kaizala into the organization’s business processes.</span></span> <span data-ttu-id="e6061-106">Entwickler hat keinen Zugriff auf die Endbenutzer bei der Entwicklung der Anwendung (unterscheidet sich von einem Administrator).</span><span class="sxs-lookup"><span data-stu-id="e6061-106">Developer does not have access to the end-user while developing the application (differs from an Admin).</span></span>
*   <span data-ttu-id="e6061-107">**Admin:** Benutzer, der ist Bestandteil der End-Gruppen und ein Administrator ist.</span><span class="sxs-lookup"><span data-stu-id="e6061-107">**Admin:** User who is part of the end-groups and is an administrator.</span></span> <span data-ttu-id="e6061-108">Wird zum Ausführen von Verwaltungsaufgaben für die Gruppe erwartet.</span><span class="sxs-lookup"><span data-stu-id="e6061-108">Is expected to perform group management tasks.</span></span>
*   <span data-ttu-id="e6061-109">**Benutzer:** Endbenutzer Kaizala</span><span class="sxs-lookup"><span data-stu-id="e6061-109">**User:** Kaizala end users</span></span>

## <a name="pre-req-to-set-up"></a><span data-ttu-id="e6061-110">Voraussetzung einwahlseite</span><span class="sxs-lookup"><span data-stu-id="e6061-110">Pre-req to set-up</span></span>

*   <span data-ttu-id="e6061-111">Als eine **Developer:**</span><span class="sxs-lookup"><span data-stu-id="e6061-111">As a **developer:**</span></span>
    *   <span data-ttu-id="e6061-112">Ein Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="e6061-112">An Office365 account</span></span>
    *   <span data-ttu-id="e6061-113">Eine Kaizala registriert Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-113">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="e6061-114">Dev Einrichtung (allen Plattformen) zum Aufrufen der REST-API</span><span class="sxs-lookup"><span data-stu-id="e6061-114">Dev set-up (any platform) to invoke REST API</span></span>
*   <span data-ttu-id="e6061-115">Als **Administrator**</span><span class="sxs-lookup"><span data-stu-id="e6061-115">As an **admin**</span></span>
    *   <span data-ttu-id="e6061-116">Ein Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="e6061-116">An Office365 account</span></span>
    *   <span data-ttu-id="e6061-117">Eine Kaizala registriert Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-117">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="e6061-118">Admin einer Unterhaltung Gruppe innerhalb Kaizala mit der registrierten Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-118">Admin of a conversation group inside Kaizala with the registered phone number</span></span>
*   <span data-ttu-id="e6061-119">Als **Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e6061-119">As a **user**</span></span>
    *   <span data-ttu-id="e6061-120">Eine Kaizala registriert Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-120">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="e6061-121">Mitglied der Gruppe innerhalb Kaizala Unterhaltung mit der registrierten Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-121">Member of a conversation group inside Kaizala with the registered phone number</span></span>

## <a name="set-up-steps-developer--group-admin"></a><span data-ttu-id="e6061-122">Installationsschritte (für Entwickler & Gruppe Admin)</span><span class="sxs-lookup"><span data-stu-id="e6061-122">Set-up steps (Developer & Group admin)</span></span>

<span data-ttu-id="e6061-123">Es gibt vier wichtigsten Infrastrukturkomponenten Arbeitens mit Kaizala Platform-API:</span><span class="sxs-lookup"><span data-stu-id="e6061-123">There are four major infrastructure components involved in working with the Kaizala Platform API:</span></span>

*   <span data-ttu-id="e6061-124">**Connectors:** Alle 3. Partei Systeme, die mit Kaizala integrieren müssen müssen mit der Kaizala-Plattform als "Connector" registriert werden, und erhalten Sie API-Token an den Konnektor entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6061-124">**Connectors:** All 3rd party systems that need to integrate with Kaizala need to be registered with the Kaizala platform as a “Connector” and get API Tokens corresponding to the Connector.</span></span>
*   <span data-ttu-id="e6061-125">**Kaizala-Verwaltungsportal:** Portal zum Registrieren der jeweiligen 3. Partei Connectors – und stellen Sie ihnen den Zugriff auf Kaizala Unterhaltungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="e6061-125">**Kaizala Management Portal:** A portal to register the respective 3rd party Connectors – and provide them access to Kaizala Conversation groups.</span></span>
*   <span data-ttu-id="e6061-126">**-Tokens-Diensts:** Ein URL-Endpunkt, die von der 3. Partei apps abzurufenden Zugriffstoken aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="e6061-126">**Token Service:** A URL end-point which needs to be called by the 3rd party apps to get Access Tokens.</span></span>
*   <span data-ttu-id="e6061-127">**Platform Service:** Ein URL-Endpunkt die bestimmte Ressourcen, um verschiedene Aktionen innerhalb Kaizala verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="e6061-127">**Platform Service:** A URL end-point which exposes specific resources to perform various actions inside Kaizala.</span></span>
*   <span data-ttu-id="e6061-128">**Schritt 1: Entwickler registriert einen Connector**</span><span class="sxs-lookup"><span data-stu-id="e6061-128">**Step 1: Developer registers a Connector**</span></span>

    *   <span data-ttu-id="e6061-129">Entwickler navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="e6061-129">Developer navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="e6061-130">Melden Sie sich mit einem vorhandenen Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="e6061-130">Log in using an existing Office365 account</span></span>
    *   <span data-ttu-id="e6061-131">Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal</span><span class="sxs-lookup"><span data-stu-id="e6061-131">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="e6061-132">Geben Sie Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-132">Enter Phone number</span></span>
        *   <span data-ttu-id="e6061-133">Tippen Sie auf "PIN generieren"</span><span class="sxs-lookup"><span data-stu-id="e6061-133">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="e6061-134">Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen</span><span class="sxs-lookup"><span data-stu-id="e6061-134">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="e6061-135">Tippen Sie auf "Connectors" im linken Menü</span><span class="sxs-lookup"><span data-stu-id="e6061-135">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="e6061-136">Tippen Sie auf "Connector hinzufügen"</span><span class="sxs-lookup"><span data-stu-id="e6061-136">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="e6061-137">Registrieren Sie einen Connector für das 3. Partei-System, das die API verwenden</span><span class="sxs-lookup"><span data-stu-id="e6061-137">Register a connector for the 3rd party system that will use the API</span></span>
        *   <span data-ttu-id="e6061-138">Geben Sie den Namen des Connectors und andere Details.</span><span class="sxs-lookup"><span data-stu-id="e6061-138">Enter the name of the Connector and other details.</span></span> <span data-ttu-id="e6061-139">Tippen Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="e6061-139">Tap on Continue</span></span>
        *   <span data-ttu-id="e6061-140">Wählen Sie Berechtigungen, mit denen bestimmt ist für den Zugriff auf den Connector</span><span class="sxs-lookup"><span data-stu-id="e6061-140">Select permissions that is intended for the Connector to have access to</span></span>
        *   <span data-ttu-id="e6061-141">Tippen Sie auf Connector erstellen</span><span class="sxs-lookup"><span data-stu-id="e6061-141">Tap on Create Connector</span></span>
    *   <span data-ttu-id="e6061-142">Beachten Sie die ID & geheimen Schlüssel, die generiert abrufen und auf dem Portal angezeigt</span><span class="sxs-lookup"><span data-stu-id="e6061-142">Note the ID & Secret that get generated and displayed on the portal</span></span>

*   <span data-ttu-id="e6061-143">**Schritt 2: Gruppe Admin "gewährt" Connector seinen Gruppe**</span><span class="sxs-lookup"><span data-stu-id="e6061-143">**Step 2: Group Admin “grants” the Connector access to his/her group**</span></span>

    *   <span data-ttu-id="e6061-144">Admin navigiert zu Kaizala-Verwaltungsportal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="e6061-144">Admin navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="e6061-145">Melden Sie sich mit einer vorhandenen Office365 Konto (SKU TBD)</span><span class="sxs-lookup"><span data-stu-id="e6061-145">Log in using an existing Office365 (SKU TBD) account</span></span>
    *   <span data-ttu-id="e6061-146">Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal</span><span class="sxs-lookup"><span data-stu-id="e6061-146">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="e6061-147">Geben Sie Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e6061-147">Enter Phone number</span></span>
        *   <span data-ttu-id="e6061-148">Tippen Sie auf "PIN generieren"</span><span class="sxs-lookup"><span data-stu-id="e6061-148">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="e6061-149">Überprüfen Sie die PIN über eine SMS auf die angegebene Telefonnummer an empfangen</span><span class="sxs-lookup"><span data-stu-id="e6061-149">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="e6061-150">Tippen Sie auf "Groups" im linken Menü</span><span class="sxs-lookup"><span data-stu-id="e6061-150">Tap on “Groups” in the left menu</span></span>
    *   <span data-ttu-id="e6061-151">Tippen Sie auf den Namen der Gruppe, die vom Connector zugegriffen werden muss</span><span class="sxs-lookup"><span data-stu-id="e6061-151">Tap on the group name which needs to be accessed by the Connector</span></span>
    *   <span data-ttu-id="e6061-152">Tippen Sie auf "Connectors"</span><span class="sxs-lookup"><span data-stu-id="e6061-152">Tap on “Connectors”</span></span>
    *   <span data-ttu-id="e6061-153">Wählen Sie in der Dropdownliste den Konnektor, der Sie Zugriff zu gewähren möchten</span><span class="sxs-lookup"><span data-stu-id="e6061-153">In the drop-down, select the Connector that you want to grant access to</span></span>
    *   <span data-ttu-id="e6061-154">Tippen Sie auf "Connector hinzufügen"</span><span class="sxs-lookup"><span data-stu-id="e6061-154">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="e6061-155">Beachten Sie die Refresh Token, die generiert dient zum Abrufen und auf dem Portal angezeigt</span><span class="sxs-lookup"><span data-stu-id="e6061-155">Note the Refresh Token that gets generated and displayed on the portal</span></span>

*   <span data-ttu-id="e6061-156">**Schritt 3: Gruppe Admin teilt Token aktualisieren, mit der App-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="e6061-156">**Step 3: Group Admin shares the Refresh Token with the App Developer**</span></span>

    *   <span data-ttu-id="e6061-157">Admin muss manuell freigeben der Aktualisierungstoken erhalten in Schritt2 mit dem app-Entwickler</span><span class="sxs-lookup"><span data-stu-id="e6061-157">Admin needs to manually share the refresh token received in Step 2 with the app developer</span></span>

*   <span data-ttu-id="e6061-158">**Schritt 4: App-Entwickler ruft der Kaizala Plattform Rest-API zum Generieren von Access-Token**</span><span class="sxs-lookup"><span data-stu-id="e6061-158">**Step 4: App Developer calls the Kaizala Platform Rest API to generate Access Token**</span></span>

    *   <span data-ttu-id="e6061-159">Entwickler kann nun die Aktualisierungstoken verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6061-159">Developer can now use the Refresh token.</span></span> <span data-ttu-id="e6061-160">eine Connector-ID und geheimen Schlüssel Connector aufrufen, die REST-API Bankkontodaten zum Generieren von Access Token (Weitere Informationen weiter unten)</span><span class="sxs-lookup"><span data-stu-id="e6061-160">a Connector ID and Connector Secret to call the REST API inorder to generate Access Token (more info below)</span></span>


<span data-ttu-id="e6061-161">Weiter: [generieren Zugriffstoken](Tokens.md)</span><span class="sxs-lookup"><span data-stu-id="e6061-161">Next:  [Generate Access token](Tokens.md)</span></span><br/>
<span data-ttu-id="e6061-162">Mehr: [API-Dokumentation](API.md)</span><span class="sxs-lookup"><span data-stu-id="e6061-162">More:  [API Documentation](API.md)</span></span>
