---
title: Mobiel werkgebied Goedkeuring van facturen
description: Dit onderwerp biedt informatie over het mobiele werkgebied Goedkeuring van facturen. Dit werkgebied geeft een lijst met facturen die aan u zijn toegewezen via het workflowproces voor de koptekst van de leveranciersfactuur.
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 24818afbbdf328c8fd3eea691634db24e443b07b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="609ac-104">Mobiel werkgebied Goedkeuring van facturen</span><span class="sxs-lookup"><span data-stu-id="609ac-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="609ac-105">Dit onderwerp biedt informatie over het mobiele werkgebied **Goedkeuring van facturen**.</span><span class="sxs-lookup"><span data-stu-id="609ac-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="609ac-106">Dit werkgebied geeft een lijst met facturen die aan u zijn toegewezen via het workflowproces voor de koptekst van de leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="609ac-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="609ac-107">Dit mobiele werkgebied is bedoeld om te worden gebruikt met de mobiele app Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="609ac-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="609ac-108">Overzicht</span><span class="sxs-lookup"><span data-stu-id="609ac-108">Overview</span></span>

<span data-ttu-id="609ac-109">In het mobiele werkgebied **Goedkeuring van facturen** kunnen medewerkers en managers van de afdeling Crediteuren facturen weergeven die zijn toegewezen aan hen als onderdeel van het workflowproces voor de koptekst van de leverancierfactuur.</span><span class="sxs-lookup"><span data-stu-id="609ac-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="609ac-110">U kunt de factuurgegevens en zelfs de regel en distributiedetails weergeven, zodat u weloverwogen kunt besluiten over goedkeuring of afwijzing.</span><span class="sxs-lookup"><span data-stu-id="609ac-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="609ac-111">Vanuit het werkgebied kunt u actie ondernemen om de factuur door het workflowproces te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="609ac-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="609ac-112">Vereisten</span><span class="sxs-lookup"><span data-stu-id="609ac-112">Prerequisites</span></span>

<span data-ttu-id="609ac-113">Voordat u dit mobiele werkgebied kunt gebruiken, moet aan de volgende voorwaarden worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="609ac-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="609ac-114">Vereiste</span><span class="sxs-lookup"><span data-stu-id="609ac-114">Prerequisite</span></span></th>
<th><span data-ttu-id="609ac-115">Rol</span><span class="sxs-lookup"><span data-stu-id="609ac-115">Role</span></span></th>
<th><span data-ttu-id="609ac-116">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="609ac-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="609ac-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, update juli 2017, moet zijn geïmplementeerd in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="609ac-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="609ac-118">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="609ac-118">System administrator</span></span></td>
<td><span data-ttu-id="609ac-119">Zie <a href="../deployment/deploy-demo-environment.md">Een demo-omgeving implementeren</a></span><span class="sxs-lookup"><span data-stu-id="609ac-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="609ac-120">Het mobiele werkgebied <strong>Goedkeuring van facturen</strong> moet worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="609ac-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="609ac-121">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="609ac-121">System administrator</span></span></td>
<td><span data-ttu-id="609ac-122">Zie <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiel werkgebied publiceren</a>.</span><span class="sxs-lookup"><span data-stu-id="609ac-122">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="609ac-123">De mobiele app downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="609ac-123">Download and install the mobile app</span></span>

<span data-ttu-id="609ac-124">Download en installeer de mobiele app Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="609ac-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="609ac-125">Voor Android-telefoons</span><span class="sxs-lookup"><span data-stu-id="609ac-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="609ac-126">Voor iPhones</span><span class="sxs-lookup"><span data-stu-id="609ac-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="609ac-127">Aanmelden bij de mobiele app</span><span class="sxs-lookup"><span data-stu-id="609ac-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="609ac-128">Start de app op uw mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="609ac-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="609ac-129">Voer uw Microsoft Dynamics 365-URL in.</span><span class="sxs-lookup"><span data-stu-id="609ac-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="609ac-130">De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren.</span><span class="sxs-lookup"><span data-stu-id="609ac-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="609ac-131">Voer uw referenties in.</span><span class="sxs-lookup"><span data-stu-id="609ac-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="609ac-132">Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven.</span><span class="sxs-lookup"><span data-stu-id="609ac-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="609ac-133">Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="609ac-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="609ac-134">[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="609ac-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="609ac-135">Facturen goedkeuren met behulp van het mobiele werkgebied Goedkeuring van facturen</span><span class="sxs-lookup"><span data-stu-id="609ac-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="609ac-136">Selecteer op uw mobiele apparaat het werkgebied **Goedkeuring van facturen**.</span><span class="sxs-lookup"><span data-stu-id="609ac-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="609ac-137">Selecteer de factuur die aan u is toegewezen door het workflowproces voor de koptekst van de leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="609ac-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="609ac-138">Controleer op de pagina **Factuurdetails** de koptekstinformatie, zoals informatie over de leverancier en datum.</span><span class="sxs-lookup"><span data-stu-id="609ac-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="609ac-139">Selecteer een regel op de factuur met meer gedetailleerde informatie over de factuur in de weergave **Details van factuurregel**.</span><span class="sxs-lookup"><span data-stu-id="609ac-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="609ac-140">Selecteer in de weergave **Details van factuurregel** de waarde **Distributies** om de regeldistributies op te roepen.</span><span class="sxs-lookup"><span data-stu-id="609ac-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="609ac-141">Hier kunt u de boekhouding voor de factuurregel weergeven.</span><span class="sxs-lookup"><span data-stu-id="609ac-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="609ac-142">De getoonde informatie bevat de financiële dimensies en de hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="609ac-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="609ac-143">Selecteer op de pagina **Factuurdetails** **Distributies** om alle distributies op te roepen.</span><span class="sxs-lookup"><span data-stu-id="609ac-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="609ac-144">Hier kunt u de boekhouding voor de gehele factuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="609ac-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="609ac-145">De getoonde informatie bevat de financiële dimensies en de hoofdrekeningen.</span><span class="sxs-lookup"><span data-stu-id="609ac-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="609ac-146">Selecteer **Bijlagen** om eventuele notities of bestanden weer te geven, die zijn gekoppeld aan de factuur.</span><span class="sxs-lookup"><span data-stu-id="609ac-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="609ac-147">Selecteer op de pagina **Factuurdetails** de juiste workflowactie uit om uw beoordelingsproces te voltooien.</span><span class="sxs-lookup"><span data-stu-id="609ac-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="609ac-148">Selecteer **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="609ac-148">Select **Done**.</span></span>

