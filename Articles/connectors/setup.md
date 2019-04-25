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
# <a name="setup-for-using-the-kaizala-connectors"></a><span data-ttu-id="c2de5-103">Setup für die Verwendung der Kaizala-Connectors</span><span class="sxs-lookup"><span data-stu-id="c2de5-103">Setup for using the Kaizala Connectors</span></span>

## <a name="personas"></a><span data-ttu-id="c2de5-104">Personas</span><span class="sxs-lookup"><span data-stu-id="c2de5-104">Personas</span></span>

*   <span data-ttu-id="c2de5-105">**Entwickler:** Interne oder Drittanbieter entwickelnde Anwendungen für die Organisation, die Kaizala in die Geschäftsprozesse der Organisation integrieren müssen.</span><span class="sxs-lookup"><span data-stu-id="c2de5-105">**Developer:** In-house or 3rd party developing applications for the organization – who need to integrate Kaizala into the organization’s business processes.</span></span> <span data-ttu-id="c2de5-106">Der Entwickler hat beim Entwickeln der Anwendung keinen Zugriff auf den Endbenutzer (unterscheidet sich von einem Administrator).</span><span class="sxs-lookup"><span data-stu-id="c2de5-106">Developer does not have access to the end-user while developing the application (differs from an Admin).</span></span>
*   <span data-ttu-id="c2de5-107">**Administrator:** Benutzer, der Teil der Endgruppen ist und ein Administrator ist.</span><span class="sxs-lookup"><span data-stu-id="c2de5-107">**Admin:** User who is part of the end-groups and is an administrator.</span></span> <span data-ttu-id="c2de5-108">Es wird erwartet, dass Gruppen Verwaltungsaufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2de5-108">Is expected to perform group management tasks.</span></span>
*   <span data-ttu-id="c2de5-109">**Benutzer:** Kaizala-Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="c2de5-109">**User:** Kaizala end users</span></span>

## <a name="pre-req-to-set-up"></a><span data-ttu-id="c2de5-110">Vorab Anforderung für die Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c2de5-110">Pre-req to set-up</span></span>

*   <span data-ttu-id="c2de5-111">Als **Entwickler:**</span><span class="sxs-lookup"><span data-stu-id="c2de5-111">As a **developer:**</span></span>
    *   <span data-ttu-id="c2de5-112">Ein Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="c2de5-112">An Office365 account</span></span>
    *   <span data-ttu-id="c2de5-113">Eine registrierte Kaizala</span><span class="sxs-lookup"><span data-stu-id="c2de5-113">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="c2de5-114">Entwicklungs-Set-up (jede Plattform) zum Aufrufen der REST-API</span><span class="sxs-lookup"><span data-stu-id="c2de5-114">Dev set-up (any platform) to invoke REST API</span></span>
*   <span data-ttu-id="c2de5-115">Als **Administrator**</span><span class="sxs-lookup"><span data-stu-id="c2de5-115">As an **admin**</span></span>
    *   <span data-ttu-id="c2de5-116">Ein Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="c2de5-116">An Office365 account</span></span>
    *   <span data-ttu-id="c2de5-117">Eine registrierte Kaizala</span><span class="sxs-lookup"><span data-stu-id="c2de5-117">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="c2de5-118">Administrator einer unterhaltungsgruppe innerhalb von Kaizala mit der registrierten Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="c2de5-118">Admin of a conversation group inside Kaizala with the registered phone number</span></span>
*   <span data-ttu-id="c2de5-119">Als **Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c2de5-119">As a **user**</span></span>
    *   <span data-ttu-id="c2de5-120">Eine registrierte Kaizala</span><span class="sxs-lookup"><span data-stu-id="c2de5-120">A Kaizala registered phone number</span></span>
    *   <span data-ttu-id="c2de5-121">Mitglied einer unterhaltungsgruppe innerhalb von Kaizala mit der registrierten Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="c2de5-121">Member of a conversation group inside Kaizala with the registered phone number</span></span>

## <a name="set-up-steps-developer--group-admin"></a><span data-ttu-id="c2de5-122">Einrichten von Schritten (Entwickler-&-Gruppenadministrator)</span><span class="sxs-lookup"><span data-stu-id="c2de5-122">Set-up steps (Developer & Group admin)</span></span>

<span data-ttu-id="c2de5-123">Bei der Arbeit mit der Kaizala-Platt Form-API sind vier wichtige Infrastrukturkomponenten beteiligt:</span><span class="sxs-lookup"><span data-stu-id="c2de5-123">There are four major infrastructure components involved in working with the Kaizala Platform API:</span></span>

*   <span data-ttu-id="c2de5-124">**Connectors:** Alle 3rd-Party-Systeme, die mit Kaizala integriert werden müssen, müssen bei der Kaizala-Plattform als "Connector" registriert werden und erhalten API-Token, die dem Connector entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c2de5-124">**Connectors:** All 3rd party systems that need to integrate with Kaizala need to be registered with the Kaizala platform as a “Connector” and get API Tokens corresponding to the Connector.</span></span>
*   <span data-ttu-id="c2de5-125">**Kaizala-Verwaltungs Portal:** Ein Portal zum Registrieren der jeweiligen Drittanbieter-Connectors – und Zugriff auf Kaizala-Konversationsgruppen.</span><span class="sxs-lookup"><span data-stu-id="c2de5-125">**Kaizala Management Portal:** A portal to register the respective 3rd party Connectors – and provide them access to Kaizala Conversation groups.</span></span>
*   <span data-ttu-id="c2de5-126">**Tokendienst:** Ein Endpunkt der URL, der von Drittanbieter-apps aufgerufen werden muss, um Zugriffstoken zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2de5-126">**Token Service:** A URL end-point which needs to be called by the 3rd party apps to get Access Tokens.</span></span>
*   <span data-ttu-id="c2de5-127">**Plattformdienst:** Ein URL-Endpunkt, der bestimmte Ressourcen für verschiedene Aktionen innerhalb von Kaizala verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="c2de5-127">**Platform Service:** A URL end-point which exposes specific resources to perform various actions inside Kaizala.</span></span>
*   <span data-ttu-id="c2de5-128">**Schritt 1: Registrieren eines Connectors für Entwickler**</span><span class="sxs-lookup"><span data-stu-id="c2de5-128">**Step 1: Developer registers a Connector**</span></span>

    *   <span data-ttu-id="c2de5-129">Entwickler navigiert zu Kaizala Management Portal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="c2de5-129">Developer navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="c2de5-130">Anmelden mit einem vorhandenen Office365-Konto</span><span class="sxs-lookup"><span data-stu-id="c2de5-130">Log in using an existing Office365 account</span></span>
    *   <span data-ttu-id="c2de5-131">Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.</span><span class="sxs-lookup"><span data-stu-id="c2de5-131">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="c2de5-132">Telefonnummer eingeben</span><span class="sxs-lookup"><span data-stu-id="c2de5-132">Enter Phone number</span></span>
        *   <span data-ttu-id="c2de5-133">Tippen Sie auf "PIN generieren".</span><span class="sxs-lookup"><span data-stu-id="c2de5-133">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="c2de5-134">ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="c2de5-134">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="c2de5-135">Tippen Sie im linken Menü auf "Connectors".</span><span class="sxs-lookup"><span data-stu-id="c2de5-135">Tap on “Connectors” in the left menu</span></span>
    *   <span data-ttu-id="c2de5-136">Tippen Sie auf "Connector hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c2de5-136">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="c2de5-137">Registrieren eines Connectors für das Drittanbietersystem, das die API verwendet</span><span class="sxs-lookup"><span data-stu-id="c2de5-137">Register a connector for the 3rd party system that will use the API</span></span>
        *   <span data-ttu-id="c2de5-138">Geben Sie den Namen des Connectors und weitere Details ein.</span><span class="sxs-lookup"><span data-stu-id="c2de5-138">Enter the name of the Connector and other details.</span></span> <span data-ttu-id="c2de5-139">Tippen Sie auf weiter</span><span class="sxs-lookup"><span data-stu-id="c2de5-139">Tap on Continue</span></span>
        *   <span data-ttu-id="c2de5-140">Wählen Sie [Berechtigungen](permission.md) aus, die für den Connector vorgesehen sind, um Zugriff auf</span><span class="sxs-lookup"><span data-stu-id="c2de5-140">Select [permissions](permission.md) that is intended for the Connector to have access to</span></span>
        *   <span data-ttu-id="c2de5-141">Tippen Sie auf Verbinder erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2de5-141">Tap on Create Connector</span></span>
    *   <span data-ttu-id="c2de5-142">Beachten Sie die ID & Secret, die generiert und im Portal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c2de5-142">Note the ID & Secret that get generated and displayed on the portal</span></span>

*   <span data-ttu-id="c2de5-143">**Schritt 2: Gruppenadministrator erteilt den Connector-Zugriff auf seine Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c2de5-143">**Step 2: Group Admin “grants” the Connector access to his/her group**</span></span>

    *   <span data-ttu-id="c2de5-144">Administrator navigiert zu Kaizala Management Portal @https://manage.kaiza.la/</span><span class="sxs-lookup"><span data-stu-id="c2de5-144">Admin navigates to Kaizala Management Portal @ https://manage.kaiza.la/</span></span>
    *   <span data-ttu-id="c2de5-145">Anmelden mit einem vorhandenen Office365-Konto (SKU-festgelegt)</span><span class="sxs-lookup"><span data-stu-id="c2de5-145">Log in using an existing Office365 (SKU TBD) account</span></span>
    *   <span data-ttu-id="c2de5-146">Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.</span><span class="sxs-lookup"><span data-stu-id="c2de5-146">Register a phone number on the portal by tapping on “Add a Phone Number”</span></span>
        *   <span data-ttu-id="c2de5-147">Telefonnummer eingeben</span><span class="sxs-lookup"><span data-stu-id="c2de5-147">Enter Phone number</span></span>
        *   <span data-ttu-id="c2de5-148">Tippen Sie auf "PIN generieren".</span><span class="sxs-lookup"><span data-stu-id="c2de5-148">Tap on “Generate PIN”</span></span>
        *   <span data-ttu-id="c2de5-149">ÜberPrüfen der empfangenen PIN über eine SMS unter der angegebenen Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="c2de5-149">Verify the PIN received via an SMS on the specified phone number</span></span>
    *   <span data-ttu-id="c2de5-150">Tippen Sie im linken Menü auf "Gruppen".</span><span class="sxs-lookup"><span data-stu-id="c2de5-150">Tap on “Groups” in the left menu</span></span>
    *   <span data-ttu-id="c2de5-151">Tippen Sie auf den Gruppennamen, auf den der Connector zugreifen muss.</span><span class="sxs-lookup"><span data-stu-id="c2de5-151">Tap on the group name which needs to be accessed by the Connector</span></span>
    *   <span data-ttu-id="c2de5-152">Tippen Sie auf "Connectors"</span><span class="sxs-lookup"><span data-stu-id="c2de5-152">Tap on “Connectors”</span></span>
    *   <span data-ttu-id="c2de5-153">Wählen Sie in der Dropdownliste den Connector aus, dem Sie Zugriff gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="c2de5-153">In the drop-down, select the Connector that you want to grant access to</span></span>
    *   <span data-ttu-id="c2de5-154">Tippen Sie auf "Connector hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c2de5-154">Tap on “Add Connector”</span></span>
    *   <span data-ttu-id="c2de5-155">Hinweis das Aktualisierungs Token, das generiert und im Portal angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="c2de5-155">Note the Refresh Token that gets generated and displayed on the portal</span></span>

*   <span data-ttu-id="c2de5-156">**Schritt 3: Gruppenadministrator teilt das Aktualisierungs Token mit dem App-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="c2de5-156">**Step 3: Group Admin shares the Refresh Token with the App Developer**</span></span>

    *   <span data-ttu-id="c2de5-157">Der Administrator muss das in Schritt 2 erhaltene Aktualisierungstoken manuell mit dem App-Entwickler freigeben.</span><span class="sxs-lookup"><span data-stu-id="c2de5-157">Admin needs to manually share the refresh token received in Step 2 with the app developer</span></span>

*   <span data-ttu-id="c2de5-158">**Schritt 4: App-Entwickler Ruft die Kaizala-Plattform-Rest-API zum Generieren von Zugriffs Token**</span><span class="sxs-lookup"><span data-stu-id="c2de5-158">**Step 4: App Developer calls the Kaizala Platform Rest API to generate Access Token**</span></span>

    *   <span data-ttu-id="c2de5-159">Entwickler können nun das Aktualisierungstoken verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2de5-159">Developer can now use the Refresh token.</span></span> <span data-ttu-id="c2de5-160">eine Connector-ID und ein Connector Secret, um die REST-API aufzurufen, um Zugriffs Token zu generieren (Weitere Informationen finden Sie weiter unten)</span><span class="sxs-lookup"><span data-stu-id="c2de5-160">a Connector ID and Connector Secret to call the REST API inorder to generate Access Token (more info below)</span></span>


<span data-ttu-id="c2de5-161">Weiter: [Generate Access Token](Tokens.md)</span><span class="sxs-lookup"><span data-stu-id="c2de5-161">Next:  [Generate Access token](Tokens.md)</span></span><br/>
<span data-ttu-id="c2de5-162">Weitere Informationen: [API-Dokumentation](API.md)</span><span class="sxs-lookup"><span data-stu-id="c2de5-162">More:  [API Documentation](API.md)</span></span>
