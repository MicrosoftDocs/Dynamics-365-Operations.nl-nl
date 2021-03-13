---
title: Mobiel werkgebied voor activabeheer instellen
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Supply Chain Management en de mobiele app Finance and Operations (Dynamics 365) kunt instellen voor het uitvoeren van een mobiel werkgebied voor activabeheer waarmee medewerkers taken voor activabeheer kunnen uitvoeren.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9c2410c50b5d289792e2cc364674e1e093653590
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033201"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="a99b7-103">Mobiel werkgebied voor activabeheer instellen</span><span class="sxs-lookup"><span data-stu-id="a99b7-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a99b7-104">In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Supply Chain Management en de mobiele app Finance and Operations (Dynamics 365) kunt instellen voor het uitvoeren van het mobiele werkgebied **Activabeheer** waarmee medewerkers taken voor activabeheer kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a99b7-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="a99b7-105">Onderhoudsmedewerkers instellen in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a99b7-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="a99b7-106">Voer de volgende stappen uit voor elke gebruiker die toegang nodig heeft tot het mobiele werkgebied **Activabeheer**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="a99b7-107">Ga in Supply Chain Management naar **Human resources \> Medewerkers** en zorg ervoor dat er een medewerkersrecord bestaat voor de gebruiker die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="a99b7-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="a99b7-108">Maak desgewenst een nieuwe medewerkersrecord.</span><span class="sxs-lookup"><span data-stu-id="a99b7-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="a99b7-109">Ga naar **Activabeheer \> Instellingen \> Medewerkers \> Medewerkers** en zorg ervoor dat de medewerkersrecord die u in de vorige stap hebt geïdentificeerd (of gemaakt) is toegewezen aan een onderhoudsmedewerkersrecord.</span><span class="sxs-lookup"><span data-stu-id="a99b7-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="a99b7-110">Maak waar nodig een nieuwe record voor de onderhoudsmedewerker en stel het veld **Medewerker** in op de medewerkersrecord uit de vorige stap.</span><span class="sxs-lookup"><span data-stu-id="a99b7-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="a99b7-111">Ga naar **Activabeheer \> Instellingen \> Medewerkers \> Onderhoudsmedewerkersgroepen** en zorg ervoor dat de onderhoudsmedewerkersrecord die u in de vorige stap hebt geïdentificeerd (of gemaakt), behoort tot een onderhoudsmedewerkersgroep.</span><span class="sxs-lookup"><span data-stu-id="a99b7-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="a99b7-112">Ga naar **Systeembeheer \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="a99b7-113">Selecteer de relevante gebruiker in het raster.</span><span class="sxs-lookup"><span data-stu-id="a99b7-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="a99b7-114">Stel op het sneltabblad **Gebruikersgegevens** het veld **Persoon** in op de medewerkersaccount die u aan de huidige gebruikersaccount wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="a99b7-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="a99b7-115">Deze medewerkersaccount moet de medewerkersrecord zijn die u in stap 1 hebt geïdentificeerd (of gemaakt) en die u in stap 2 aan een onderhoudsmedewerkerrecord hebt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a99b7-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="a99b7-116">Gebruikersmachtigingen en beveiligingsrollen zijn van toepassing op de functies van het mobiele werkgebied **Activabeheer**, net zoals deze van toepassing zijn op de functies van de gebruikersinterface Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a99b7-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="a99b7-117">Daarom moet elke gebruiker die u instelt voor toegang tot het mobiele werkgebied **Activabeheer**, de beveiligingsrollen hebben die zijn vereist om vergelijkbare bewerkingen rechtstreeks in Supply Chain Management uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="a99b7-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="a99b7-118">Het mobiele werkgebied Activabeheer publiceren</span><span class="sxs-lookup"><span data-stu-id="a99b7-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="a99b7-119">Als u activabeheerfuncties beschikbaar wilt maken in de mobiele app Finance and Operations (Dynamics 365), moet u het mobiele werkgebied **Activabeheer** publiceren.</span><span class="sxs-lookup"><span data-stu-id="a99b7-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="a99b7-120">Selecteer in Supply Chain Management de knop **Instellingen** (het tandwielsymbool in de rechterbovenhoek) en selecteer vervolgens **Mobiele app** in het menu.</span><span class="sxs-lookup"><span data-stu-id="a99b7-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="a99b7-121">Zoek in het dialoogvenster **Mobiele app beheren** de tegel **Activabeheer**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="a99b7-122">Als het de tekst "In metagegevens - niet gepubliceerd" bevat, is het werkgebied nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="a99b7-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="a99b7-123">Als het de tekst "In metagegevens - gepubliceerd" bevat, is het werkgebied al gepubliceerd en kunt u de rest van deze procedure overslaan.</span><span class="sxs-lookup"><span data-stu-id="a99b7-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="a99b7-124">![Het dialoogvenster Mobiele app beheren](media/mobile-workspaces.png "Het dialoogvenster Mobiele app beheren")</span><span class="sxs-lookup"><span data-stu-id="a99b7-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="a99b7-125">Selecteer de tegel **Activabeheer** en selecteer **Publiceren** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="a99b7-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="a99b7-126">Na enkele seconden ontvangt u een melding dat het werkgebied met succes is gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="a99b7-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="a99b7-127">Daarnaast moet de tekst op de tegel veranderen in 'In metagegevens - gepubliceerd'.</span><span class="sxs-lookup"><span data-stu-id="a99b7-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="a99b7-128">De mobiele app Finance and Operations (Dynamics 365) installeren en instellen</span><span class="sxs-lookup"><span data-stu-id="a99b7-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="a99b7-129">Ga naar een van de volgende app-stores om de app **Microsoft Finance and Operations (Dynamics 365)** op uw mobiele apparaat te installeren:</span><span class="sxs-lookup"><span data-stu-id="a99b7-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="a99b7-130">Voor Google Android-apparaten</span><span class="sxs-lookup"><span data-stu-id="a99b7-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="a99b7-131">Voor Apple iOS-apparaten</span><span class="sxs-lookup"><span data-stu-id="a99b7-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="a99b7-132">Open de app Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="a99b7-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="a99b7-133">De aanmeldingspagina moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a99b7-133">The sign-in page should appear.</span></span> <span data-ttu-id="a99b7-134">Voer in het veld **Aanmelden** uw Supply Chain Management-URL in of selecteer een recente URL in de lijst **Recente omgevingen** en tik op **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="a99b7-135">![Aanmeldingspagina](media/mobile-app-sign-in.png "Aanmeldingspagina")</span><span class="sxs-lookup"><span data-stu-id="a99b7-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="a99b7-136">Als u wordt gevraagd de verbinding te bevestigen, schakelt u het selectievakje **Ik begrijp het** in en tikt u vervolgens op **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="a99b7-137">Gebruik uw Microsoft-account op de pagina **Een rekening kiezen** om u aan te melden bij de mobiele toepassing.</span><span class="sxs-lookup"><span data-stu-id="a99b7-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="a99b7-138">De pagina **Werkgebieden** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a99b7-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="a99b7-139">Op deze pagina worden alle mobiele werkgebieden weergegeven die door uw Supply Chain Management-exemplaar zijn gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="a99b7-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="a99b7-140">![Lijst met werkgebieden](media/mobile-app-workspaces.png "Lijst met werkgebieden")</span><span class="sxs-lookup"><span data-stu-id="a99b7-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="a99b7-141">Als u de rechtspersoon (bedrijf) moet veranderen, tikt u op de menuknop (waarnaar soms wordt verwezen als de hamburger of hamburgerknop) in de linkerbovenhoek en tik vervolgens op **Bedrijf wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="a99b7-142">![De rechtspersoon wijzigen](media/mobile-app-change-comp.png "De rechtspersoon wijzigen")</span><span class="sxs-lookup"><span data-stu-id="a99b7-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="a99b7-143">Selecteer op de pagina **Werkgebieden** het werkgebied waarmee u wilt werken om het te openen.</span><span class="sxs-lookup"><span data-stu-id="a99b7-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="a99b7-144">![Mobiel werkgebied voor activabeheer](media/mobile-app-asset-workspace.png "Mobiel werkgebied voor activabeheer")</span><span class="sxs-lookup"><span data-stu-id="a99b7-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="a99b7-145">Werken met het mobiele werkgebied Activabeheer</span><span class="sxs-lookup"><span data-stu-id="a99b7-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="a99b7-146">Zie [Het mobiele werkgebied Activabeheer gebruiken](asset-management-mobile-workspace.md) voor meer informatie over het werken met het mobiele werkgebied **Activabeheer**.</span><span class="sxs-lookup"><span data-stu-id="a99b7-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="a99b7-147">Zie de [Startpagina van mobiele app](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md) voor meer informatie over de mobiele app Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="a99b7-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>
