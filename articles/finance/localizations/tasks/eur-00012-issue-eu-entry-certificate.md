---
title: EUR-00012 Een EU-invoercertificaat uitgeven
description: Deze procedure begeleidt u bij het inschakelen van een EU-invoercertificaat, het configureren van een klantrekening om invoercertificaten te gebruiken en het uitgeven van een certificaat.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0091af30b917aab3b8c4572a72a20d8d2d5d52e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408312"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="eb233-103">EUR-00012 Een EU-invoercertificaat uitgeven</span><span class="sxs-lookup"><span data-stu-id="eb233-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="eb233-104">Deze procedure begeleidt u bij het inschakelen van een EU-invoercertificaat, het configureren van een klantrekening om invoercertificaten te gebruiken en het uitgeven van een certificaat.</span><span class="sxs-lookup"><span data-stu-id="eb233-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="eb233-105">Deze procedure is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="eb233-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="eb233-106">Certificaatbeheer inschakelen</span><span class="sxs-lookup"><span data-stu-id="eb233-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="eb233-107">Ga naar Klanten > Instellingen > Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="eb233-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="eb233-108">Klik op het tabblad Zendingen.</span><span class="sxs-lookup"><span data-stu-id="eb233-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="eb233-109">Vouw de sectie Invoercertificaat uit.</span><span class="sxs-lookup"><span data-stu-id="eb233-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="eb233-110">Selecteer Ja in het veld Certificaatbeheer inschakelen.</span><span class="sxs-lookup"><span data-stu-id="eb233-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="eb233-111">Selecteer Ja in het veld Verstrekken van invoercertificaat inschakelen.</span><span class="sxs-lookup"><span data-stu-id="eb233-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="eb233-112">Klik op het tabblad Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="eb233-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="eb233-113">Zoek en selecteer de rij van het invoercertificaat in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eb233-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="eb233-114">Typ of selecteer een waarde in het veld Nummerreekscode.</span><span class="sxs-lookup"><span data-stu-id="eb233-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="eb233-115">Een klant instellen</span><span class="sxs-lookup"><span data-stu-id="eb233-115">Set up a customer</span></span>
1. <span data-ttu-id="eb233-116">Ga naar Klanten > Klanten > Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="eb233-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="eb233-117">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="eb233-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="eb233-118">Filter bijvoorbeeld op het veld Rekening met een waarde van 'DE-015'.</span><span class="sxs-lookup"><span data-stu-id="eb233-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="eb233-119">Open klantrekeninggegevens.</span><span class="sxs-lookup"><span data-stu-id="eb233-119">Open customer account details.</span></span>
4. <span data-ttu-id="eb233-120">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="eb233-120">Click Edit.</span></span>
5. <span data-ttu-id="eb233-121">Vouw de sectie Factuur en levering uit.</span><span class="sxs-lookup"><span data-stu-id="eb233-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="eb233-122">Selecteer Ja in het veld Invoercertificaat vereist.</span><span class="sxs-lookup"><span data-stu-id="eb233-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="eb233-123">Selecteer Ja in het veld Uitgifte van invoercertificaat.</span><span class="sxs-lookup"><span data-stu-id="eb233-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="eb233-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="eb233-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="eb233-125">Automatisch een EU-invoercertificaat maken</span><span class="sxs-lookup"><span data-stu-id="eb233-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="eb233-126">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="eb233-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="eb233-127">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eb233-127">Click New.</span></span>
3. <span data-ttu-id="eb233-128">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="eb233-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="eb233-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-129">Click OK.</span></span>
5. <span data-ttu-id="eb233-130">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="eb233-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="eb233-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="eb233-131">Click Save.</span></span>
7. <span data-ttu-id="eb233-132">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="eb233-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="eb233-133">Klik op Pakbon boeken.</span><span class="sxs-lookup"><span data-stu-id="eb233-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="eb233-134">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="eb233-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="eb233-135">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="eb233-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="eb233-136">Schakel het selectievakje Uitgifte van invoercertificaat uit.</span><span class="sxs-lookup"><span data-stu-id="eb233-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="eb233-137">Een invoercertificaat kan worden uitgegeven tijdens pakbonboeking of orderfacturering.</span><span class="sxs-lookup"><span data-stu-id="eb233-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="eb233-138">Laat het selectievakje Uitgifte van invoercertificaat uitgeschakeld om het certificaat later uit te geven.</span><span class="sxs-lookup"><span data-stu-id="eb233-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="eb233-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-139">Click OK.</span></span>
13. <span data-ttu-id="eb233-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-140">Click OK.</span></span>
14. <span data-ttu-id="eb233-141">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="eb233-142">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-142">Click Invoice.</span></span>
    * <span data-ttu-id="eb233-143">Controleer of de selectievakjes Invoercertificaat vereist en Uitgifte van invoercertificaat in de sectie Overzicht zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="eb233-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="eb233-144">U kunt ook het selectievakje Invoercertificaat afdrukken inschakelen om afdrukken van het certificaat toe te staan.</span><span class="sxs-lookup"><span data-stu-id="eb233-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="eb233-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-145">Click OK.</span></span>
17. <span data-ttu-id="eb233-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-146">Click OK.</span></span>
18. <span data-ttu-id="eb233-147">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="eb233-148">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-148">Click Invoice.</span></span>
20. <span data-ttu-id="eb233-149">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="eb233-150">Klik op Uitgegeven invoercertificaten weergeven.</span><span class="sxs-lookup"><span data-stu-id="eb233-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="eb233-151">Klik op Afdrukken.</span><span class="sxs-lookup"><span data-stu-id="eb233-151">Click Print.</span></span>
23. <span data-ttu-id="eb233-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eb233-152">Close the page.</span></span>
24. <span data-ttu-id="eb233-153">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="eb233-153">Click Change status.</span></span>
25. <span data-ttu-id="eb233-154">Selecteer een optie in het veld Nieuwe status.</span><span class="sxs-lookup"><span data-stu-id="eb233-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="eb233-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-155">Click OK.</span></span>
27. <span data-ttu-id="eb233-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eb233-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="eb233-157">Handmatig een EU-invoercertificaat maken</span><span class="sxs-lookup"><span data-stu-id="eb233-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="eb233-158">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="eb233-159">Klik op Invoercertificaat maken.</span><span class="sxs-lookup"><span data-stu-id="eb233-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="eb233-160">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb233-160">Click OK.</span></span>
4. <span data-ttu-id="eb233-161">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="eb233-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="eb233-162">Klik op Uitgegeven invoercertificaten weergeven.</span><span class="sxs-lookup"><span data-stu-id="eb233-162">Click View issued entry certificates.</span></span>

