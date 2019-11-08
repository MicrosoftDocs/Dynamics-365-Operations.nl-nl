---
title: Tijdinvoer voor project voor mobiel werkgebied
description: Dit onderwerp biedt informatie over het mobiele werkgebied voor invoer van projecturen. In dit werkgebied kunnen gebruikers tijd invoeren en opslaan voor een project met behulp van hun mobiele apparaat.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250364"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="b8927-104">Tijdinvoer voor project voor mobiel werkgebied</span><span class="sxs-lookup"><span data-stu-id="b8927-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8927-105">Dit onderwerp biedt informatie over het mobiele werkgebied **Projecttijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="b8927-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="b8927-106">In dit werkgebied kunnen gebruikers tijd invoeren en opslaan voor een project met behulp van hun mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="b8927-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="b8927-107">Dit mobiele werkgebied is bedoeld om te worden gebruikt met de app Dynamics 365 Unified Ops Mobile.</span><span class="sxs-lookup"><span data-stu-id="b8927-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="b8927-108">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b8927-108">Overview</span></span>
<span data-ttu-id="b8927-109">Als onderdeel van hun dagelijkse werkzaamheden zijn projectresources vaak on-site of onderweg.</span><span class="sxs-lookup"><span data-stu-id="b8927-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="b8927-110">Het mobiele werkgebied **Invoer van projecturen** stelt gebruikers in staat hun factureerbaar of niet-factureerbare tijd voor een project in te voeren op het mobiele apparaat van hun keuze.</span><span class="sxs-lookup"><span data-stu-id="b8927-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="b8927-111">Daarom kunnen projectresources altijd en overal tijdinvoer vastleggen.</span><span class="sxs-lookup"><span data-stu-id="b8927-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="b8927-112">Zij kunnen ook tijdinvloer bekijken die al is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="b8927-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="b8927-113">Specifiek kunnen gebruikers in het mobiele werkgebied **Projecttijdinvoer** deze taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="b8927-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="b8927-114">Voer voor elke geselecteerde datum het aantal uren in dat u hebt besteed aan een bepaalde taak.</span><span class="sxs-lookup"><span data-stu-id="b8927-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="b8927-115">Zoek op projectnaam of klant om het project te vinden waarvoor u tijd wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="b8927-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="b8927-116">Geef de categorie en de activiteit op voor de tijd die u hebt besteed.</span><span class="sxs-lookup"><span data-stu-id="b8927-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="b8927-117">Leg de tijd vast als factureerbaar of niet-factureerbaar voor het project.</span><span class="sxs-lookup"><span data-stu-id="b8927-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="b8927-118">Voer desgewenst externe of interne opmerkingen toe.</span><span class="sxs-lookup"><span data-stu-id="b8927-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b8927-119">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b8927-119">Prerequisites</span></span>
<span data-ttu-id="b8927-120">De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die voor uw organisatie is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="b8927-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="b8927-121">Vereisten als u Dynamics 365 Finance gebruikt</span><span class="sxs-lookup"><span data-stu-id="b8927-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="b8927-122">Als Finance is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Projecttijdinvoer** publiceren.</span><span class="sxs-lookup"><span data-stu-id="b8927-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="b8927-123">Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="b8927-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="b8927-124">Vereisten als u versie 1611 met platformupdate 3 of hoger gebruikt</span><span class="sxs-lookup"><span data-stu-id="b8927-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="b8927-125">Als versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder de volgende vereisten uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b8927-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b8927-126">Vereiste</span><span class="sxs-lookup"><span data-stu-id="b8927-126">Prerequisite</span></span></th>
<th><span data-ttu-id="b8927-127">Rol</span><span class="sxs-lookup"><span data-stu-id="b8927-127">Role</span></span></th>
<th><span data-ttu-id="b8927-128">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="b8927-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="b8927-129">KB 4018050 implementeren.</span><span class="sxs-lookup"><span data-stu-id="b8927-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="b8927-130">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="b8927-130">System administrator</span></span></td>
<td><span data-ttu-id="b8927-131">KB 4018050 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Invoer van projecturen</strong> bevat.</span><span class="sxs-lookup"><span data-stu-id="b8927-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="b8927-132">Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="b8927-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="b8927-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metagegevens-hotfix downloaden uit  Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="b8927-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="b8927-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</span><span class="sxs-lookup"><span data-stu-id="b8927-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="b8927-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Maak een implementeerbaar pakket</a> dat de <strong>ApplicationSuite</strong> en <strong>ProjectMobile</strong>-modellen bevat en upload het implementeerbare pakket vervolgens naar LCS.</span><span class="sxs-lookup"><span data-stu-id="b8927-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="b8927-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></span><span class="sxs-lookup"><span data-stu-id="b8927-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8927-137">Het mobiele werkgebied <strong>Projecttijdinvoer</strong> publiceren.</span><span class="sxs-lookup"><span data-stu-id="b8927-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="b8927-138">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="b8927-138">System administrator</span></span></td>
<td><span data-ttu-id="b8927-139">Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</span><span class="sxs-lookup"><span data-stu-id="b8927-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="b8927-140">De mobiele app downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="b8927-140">Download and install the mobile app</span></span>

<span data-ttu-id="b8927-141">Download en installeer de mobiele app van Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b8927-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="b8927-142">Voor Android-telefoons</span><span class="sxs-lookup"><span data-stu-id="b8927-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="b8927-143">Voor iPhones</span><span class="sxs-lookup"><span data-stu-id="b8927-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="b8927-144">Aanmelden bij de mobiele app</span><span class="sxs-lookup"><span data-stu-id="b8927-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="b8927-145">Start de app op uw mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="b8927-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="b8927-146">Voer uw Dynamics 365-URL in.</span><span class="sxs-lookup"><span data-stu-id="b8927-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="b8927-147">De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren.</span><span class="sxs-lookup"><span data-stu-id="b8927-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="b8927-148">Voer uw referenties in.</span><span class="sxs-lookup"><span data-stu-id="b8927-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="b8927-149">Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b8927-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="b8927-150">Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="b8927-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="b8927-151">[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="b8927-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="b8927-152">Tijd invoeren met behulp van het mobiele werkgebied Invoer van projecturen</span><span class="sxs-lookup"><span data-stu-id="b8927-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="b8927-153">Selecteer op uw mobiele apparaat het werkgebied **Invoer van projecturen**.</span><span class="sxs-lookup"><span data-stu-id="b8927-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="b8927-154">Selecteer **Tijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="b8927-154">Select **Time entry**.</span></span> <span data-ttu-id="b8927-155">De kalenderdatums voor de huidige week worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b8927-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="b8927-156">Selecteer voor een geselecteerde datum **Acties** &gt; **Nieuwe invoer**.</span><span class="sxs-lookup"><span data-stu-id="b8927-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="b8927-157">Voer het aantal uren te registreren uren in.</span><span class="sxs-lookup"><span data-stu-id="b8927-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="b8927-158">Selecteer het project voor de tijdinvoer.</span><span class="sxs-lookup"><span data-stu-id="b8927-158">Select the project for the time entry.</span></span> <span data-ttu-id="b8927-159">In een lijst ziet u de projecten die in uw app zijn geladen voor offline gebruik.</span><span class="sxs-lookup"><span data-stu-id="b8927-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="b8927-160">Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b8927-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="b8927-161">Zie voor meer informatie [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="b8927-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="b8927-162">Als uw project niet in de lijst staat, selecteert u **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="b8927-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="b8927-163">Zoek op naam of schakel over naar zoeken op projectnaam of klant.</span><span class="sxs-lookup"><span data-stu-id="b8927-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="b8927-164">Een categorie selecteren.</span><span class="sxs-lookup"><span data-stu-id="b8927-164">Select a category.</span></span> <span data-ttu-id="b8927-165">In een lijst ziet u de categorieën die in uw app zijn geladen voor offline gebruik.</span><span class="sxs-lookup"><span data-stu-id="b8927-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="b8927-166">Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b8927-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="b8927-167">Zie voor meer informatie [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="b8927-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="b8927-168">Als uw categorie niet in de lijst staat, selecteert u **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="b8927-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="b8927-169">Zoek op categorie of schakel over naar zoeken op categorienaam.</span><span class="sxs-lookup"><span data-stu-id="b8927-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="b8927-170">Een activiteit selecteren.</span><span class="sxs-lookup"><span data-stu-id="b8927-170">Select an activity.</span></span> <span data-ttu-id="b8927-171">In een lijst ziet u de activiteiten die in uw app zijn geladen voor offline gebruik.</span><span class="sxs-lookup"><span data-stu-id="b8927-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="b8927-172">Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b8927-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="b8927-173">Zie voor meer informatie [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="b8927-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="b8927-174">Als uw activiteit niet in de lijst staat, selecteert u **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="b8927-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="b8927-175">Zoeken op activiteitnummer of schakel over als u wilt zoeken op doel.</span><span class="sxs-lookup"><span data-stu-id="b8927-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="b8927-176">Selecteer de regeleigenschap.</span><span class="sxs-lookup"><span data-stu-id="b8927-176">Select the line property.</span></span>
12. <span data-ttu-id="b8927-177">Optioneel: voer eventueel externe en interne opmerkingen toe.</span><span class="sxs-lookup"><span data-stu-id="b8927-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="b8927-178">Selecteer **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="b8927-178">Select **Done**.</span></span>