---
title: Werkgebied voor betalingen aan leveranciers
description: Dit onderwerp biedt informatie over het werkgebied Leveranciersbetalingen. In het werkgebied Leveranciersbetalingen wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersbetalingen.
author: abruer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89ba0d68bd52413328dd583e87b09b01fd523d6f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177239"
---
# <a name="vendor-payments-workspace"></a><span data-ttu-id="848d8-104">Werkgebied voor betalingen aan leveranciers</span><span class="sxs-lookup"><span data-stu-id="848d8-104">Vendor payments workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="848d8-105">In het werkgebied **Leveranciersbetalingen** wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersbetalingen.</span><span class="sxs-lookup"><span data-stu-id="848d8-105">The **Vendor payments** workspace shows information that is related to the processing of vendor payments.</span></span> <span data-ttu-id="848d8-106">Dit werkgebied bevat een weergave **Mijn werk** en een pagina **Analyses**.</span><span class="sxs-lookup"><span data-stu-id="848d8-106">This workspace includes a **My work** view and an **Analytics** page.</span></span> <span data-ttu-id="848d8-107">In de weergave **Mijn werk** vindt u overzichtstegels, rasters met leverancierstransacties en gerelateerde leveranciersgegevens.</span><span class="sxs-lookup"><span data-stu-id="848d8-107">The **My work** view shows summary tiles, vendor transaction grids, and related vendor information.</span></span> <span data-ttu-id="848d8-108">De pagina **Analyses** gebruikt de mogelijkheden van Microsoft Power BI om visuals te tonen die te maken hebben met betalingen aan leveranciers.</span><span class="sxs-lookup"><span data-stu-id="848d8-108">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to vendor payments.</span></span>

## <a name="setup-needed-to-view-power-bi-content"></a><span data-ttu-id="848d8-109">Instellingen die nodig zijn om Power BI-inhoud weer te geven</span><span class="sxs-lookup"><span data-stu-id="848d8-109">Setup needed to view Power BI content</span></span>

<span data-ttu-id="848d8-110">De volgende instellingen moeten worden geconfigureerd om gegevens te kunnen weergeven in de visuele Power BI-elementen van **Leveranciersbetalingen**.</span><span class="sxs-lookup"><span data-stu-id="848d8-110">The following setup needs to be completed for data to display in **Vendor payments** Power BI visuals.</span></span>
1. <span data-ttu-id="848d8-111">Ga naar **Systeembeheer > Instellen > Systeemparameters** om **Systeemvaluta** en **Systeemwisselkoers** in te stellen.</span><span class="sxs-lookup"><span data-stu-id="848d8-111">Go to **System administration > Setup > System Parameters** to set **System currency** and **System Exchange Rate**.</span></span>
2. <span data-ttu-id="848d8-112">Ga naar **Grootboek > Instellen > Grootboek** en stel **Valuta voor boekhouding** en **Wisselkoerstype** in.</span><span class="sxs-lookup"><span data-stu-id="848d8-112">Go to **General Ledger > Setup > Ledger**  to set **Accounting Currency** and **Exchange Rate Type**.</span></span> 
2. <span data-ttu-id="848d8-113">Definieer wisselkoersen tussen transactievaluta's en valuta voor boekhouding, en valuta voor boekhouding en systeemvaluta.</span><span class="sxs-lookup"><span data-stu-id="848d8-113">Define exchange rates between Transaction currencies and Accounting currency, Accounting currency and System currency.</span></span> <span data-ttu-id="848d8-114">Ga hiervoor naar **Grootboek > Valuta's > Valutawisselkoersen**.</span><span class="sxs-lookup"><span data-stu-id="848d8-114">To do this, go to **General Ledger > Currencies > Currency exchange rates**.</span></span>
3. <span data-ttu-id="848d8-115">Ga naar **Systeembeheer > Instellen > Entiteitopslag** > om de samengevoegde meting **VendPaymentBIMeasure** te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="848d8-115">Go to **System administration > Setup > Entity Store** to refresh the **VendPaymentBIMeasure** aggregate measurement.</span></span> 

## <a name="my-work-view"></a><span data-ttu-id="848d8-116">Weergave Mijn werk</span><span class="sxs-lookup"><span data-stu-id="848d8-116">My work view</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="848d8-117">Overzichtstegels</span><span class="sxs-lookup"><span data-stu-id="848d8-117">Summary tiles</span></span>

<span data-ttu-id="848d8-118">De tegels in de sectie **Overzicht** geven een overzicht van de status van uw betalingsinformatie.</span><span class="sxs-lookup"><span data-stu-id="848d8-118">The tiles in the **Summary** section give an overview of the state of your payment information.</span></span> <span data-ttu-id="848d8-119">U ziet hier betalingsjournalen die nog niet zijn geboekt, achterstallige facturen, alle leveranciers en leveranciers die in de wachtstand staan.</span><span class="sxs-lookup"><span data-stu-id="848d8-119">You can see payment journals that aren't yet posted, invoices that are past due, all vendors, and vendors that are on hold.</span></span> <span data-ttu-id="848d8-120">Vanuit de sectie **Overzicht** kunt u een nieuwe betalingsronde maken.</span><span class="sxs-lookup"><span data-stu-id="848d8-120">From the **Summary** section, you can create a new pay run.</span></span>

<span data-ttu-id="848d8-121">De informatie in de sectie **Overzicht** is voor het bedrijf waarbij u zich hebt aangemeld</span><span class="sxs-lookup"><span data-stu-id="848d8-121">The information in the **Summary** section is for the company that you're signed in to.</span></span>

### <a name="vendor-transactions-grids"></a><span data-ttu-id="848d8-122">Leverancierstransactierasters</span><span class="sxs-lookup"><span data-stu-id="848d8-122">Vendor transactions grids</span></span>

<span data-ttu-id="848d8-123">De sectie **Leverancierstransacties** bevat rasters waarin u de facturen ziet die achterstalling zijn en betalingen die niet zijn vereffend.</span><span class="sxs-lookup"><span data-stu-id="848d8-123">The **Vendor transactions** section contains grids that show the invoices that are past due and payments that aren't settled.</span></span> <span data-ttu-id="848d8-124">Vanuit het raster **Achterstallige facturen** kunt u de vereffeningshistorie voor een geselecteerde factuur bekijken.</span><span class="sxs-lookup"><span data-stu-id="848d8-124">From the **Invoices past due** grid, you can view the settlement history for a selected invoice.</span></span> <span data-ttu-id="848d8-125">Vanuit het raster **Betalingen niet vereffend** kunt u de vereffeningshistorie voor een geselecteerde factuur bekijken en deze vereffenen.</span><span class="sxs-lookup"><span data-stu-id="848d8-125">From the **Payments not settled** grid, you can view the settlement history for a selected invoice and settle an invoice.</span></span>

<span data-ttu-id="848d8-126">Medewerkers die gecentraliseerd betalingen afhandelen, kunnen met een filter bovenaan elk raster een bedrijf selecteren.</span><span class="sxs-lookup"><span data-stu-id="848d8-126">Centralized payment clerks can use a filter that appears at the top of each grid to select a company.</span></span> <span data-ttu-id="848d8-127">Het raster wordt vervolgens zo gefilterd dat het veld alleen die bedrijven weergeeft die zijn gedefinieerd in de organisatiehiërarchie voor gecentraliseerde betalingen waarvoor de medewerker rechten heeft.</span><span class="sxs-lookup"><span data-stu-id="848d8-127">The grid is then filtered so that it shows only those companies that are defined in the centralized payment organizational hierarchy that the centralized payment clerk has rights to view.</span></span>

<span data-ttu-id="848d8-128">Op het tabblad **Transacties vinden** in de sectie **Leverancierstransacties** kunt u naar leverancierstransacties zoeken.</span><span class="sxs-lookup"><span data-stu-id="848d8-128">The **Find transactions** tab in the **Vendor transactions** section lets you search for a vendor transaction.</span></span>

### <a name="related-information"></a><span data-ttu-id="848d8-129">Verwante informatie</span><span class="sxs-lookup"><span data-stu-id="848d8-129">Related information</span></span>

<span data-ttu-id="848d8-130">U kunt het rapport **Leverancier naar ouderdom gerangschikt** en het rapport **Betalingsoverzicht per datum** weergeven met de koppelingen in de sectie **Gerelateerde informatie** van het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="848d8-130">You can view the **Vendor aging** report and the **Payment summary by date** report by using the links in the **Related information** section of the workspace.</span></span>

## <a name="analytics-page"></a><span data-ttu-id="848d8-131">Pagina Analyses</span><span class="sxs-lookup"><span data-stu-id="848d8-131">Analytics page</span></span>

<span data-ttu-id="848d8-132">De pagina **Analyses** bevat belangrijke metrics, zoals achterstallige leveranciersfacturen en leveranciersfacturen die in de toekomst moeten betaald worden.</span><span class="sxs-lookup"><span data-stu-id="848d8-132">The **Analytics** page provides important metrics, such as vendor invoices that are past due and vendor invoices that are due in the future.</span></span> <span data-ttu-id="848d8-133">Deze pagina bevat negen rapportpagina's.</span><span class="sxs-lookup"><span data-stu-id="848d8-133">This page contains nine report pages.</span></span> <span data-ttu-id="848d8-134">Eén pagina bevat een overzicht en de andere acht pagina's bieden informatie over betalingsmetrics uit Crediteuren.</span><span class="sxs-lookup"><span data-stu-id="848d8-134">One page provides an overview, and the other eight pages provide details about Accounts payable payment metrics.</span></span>

<span data-ttu-id="848d8-135">In de volgende tabel ziet u de visualisaties die op elke rapportpagina beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="848d8-135">The following table shows the visualizations that are available on each report page.</span></span>


|            <span data-ttu-id="848d8-136">Rapportpagina</span><span class="sxs-lookup"><span data-stu-id="848d8-136">Report page</span></span>            |                                                                                                                                                                                <span data-ttu-id="848d8-137">Visualisatie</span><span class="sxs-lookup"><span data-stu-id="848d8-137">Visualization</span></span>                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="848d8-138">Overzicht van leveranciersbetalingen</span><span class="sxs-lookup"><span data-stu-id="848d8-138">Vendor payments overview</span></span>      | <ul><li><span data-ttu-id="848d8-139">Verschuldigde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-139">Invoices past due</span></span></li><li><span data-ttu-id="848d8-140">Facturen met vervaldatum vandaag</span><span class="sxs-lookup"><span data-stu-id="848d8-140">Invoices due today</span></span></li><li><span data-ttu-id="848d8-141">Benutte kortingen versus gemiste kortingen</span><span class="sxs-lookup"><span data-stu-id="848d8-141">Discounts taken to discounts lost</span></span></li><li><span data-ttu-id="848d8-142">In de toekomst verschuldigde facturen op datum contantkorting</span><span class="sxs-lookup"><span data-stu-id="848d8-142">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="848d8-143">In de toekomst verschuldigde facturen op vervaldatum</span><span class="sxs-lookup"><span data-stu-id="848d8-143">Invoices due in future by due date</span></span></li><li><span data-ttu-id="848d8-144">Te laat betaalde facturen versus op tijd betaalde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-144">Invoices paid late to invoices paid on time</span></span></li><li><span data-ttu-id="848d8-145">Betalingsworkflowtoewijzing</span><span class="sxs-lookup"><span data-stu-id="848d8-145">Payment workflow assignment</span></span></li><li><span data-ttu-id="848d8-146">Saldo verkoper/klant</span><span class="sxs-lookup"><span data-stu-id="848d8-146">Vendor to customer balance</span></span></li><li><span data-ttu-id="848d8-147">Openstaande facturen met geblokkeerde betaling</span><span class="sxs-lookup"><span data-stu-id="848d8-147">Open invoices with payment hold</span></span></li></ul> |
|         <span data-ttu-id="848d8-148">Verschuldigde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-148">Invoices past due</span></span>         |                                                                                             <ul><li><span data-ttu-id="848d8-149">Verschuldigde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-149">Invoices past due</span></span></li><li><span data-ttu-id="848d8-150">Details achterstallige facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-150">Invoices past due details</span></span></li><li><span data-ttu-id="848d8-151">Totaal openstaande facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-151">Total open invoices</span></span></li><li><span data-ttu-id="848d8-152">Achterstallige facturen op leveranciergroep</span><span class="sxs-lookup"><span data-stu-id="848d8-152">Invoices past due per vendor group</span></span></li><li><span data-ttu-id="848d8-153">Achterstallige facturen op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-153">Invoices past due per company</span></span></li></ul>                                                                                              |
|        <span data-ttu-id="848d8-154">Facturen met vervaldatum vandaag</span><span class="sxs-lookup"><span data-stu-id="848d8-154">Invoices due today</span></span>         |                                                                                                         <ul><li><span data-ttu-id="848d8-155">Facturen met vervaldatum vandaag</span><span class="sxs-lookup"><span data-stu-id="848d8-155">Invoices due today</span></span></li><li><span data-ttu-id="848d8-156">Details facturen met vervaldatum vandaag</span><span class="sxs-lookup"><span data-stu-id="848d8-156">Invoices due today details</span></span></li><li><span data-ttu-id="848d8-157">Facturen met vervaldatum vandaag op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-157">Invoices due today per company</span></span></li><li><span data-ttu-id="848d8-158">Facturen met vervaldatum vandaag op leveranciergroep</span><span class="sxs-lookup"><span data-stu-id="848d8-158">Invoices due today per vendor group</span></span></li></ul>                                                                                                          |
| <span data-ttu-id="848d8-159">Benutte kortingen versus gemiste kortingen</span><span class="sxs-lookup"><span data-stu-id="848d8-159">Discounts taken to discounts lost</span></span> |                                                                             <ul><li><span data-ttu-id="848d8-160">Benutte kortingen versus gemiste kortingen</span><span class="sxs-lookup"><span data-stu-id="848d8-160">Discounts taken to discount lost</span></span></li><li><span data-ttu-id="848d8-161">Details benutte kortingen versus gemiste kortingen</span><span class="sxs-lookup"><span data-stu-id="848d8-161">Discounts taken to discount lost details</span></span></li><li><span data-ttu-id="848d8-162">Benutte kortingen versus gemiste kortingen op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-162">Discounts taken to discount lost per company</span></span></li><li><span data-ttu-id="848d8-163">Benutte kortingen versus gemiste kortingen op leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="848d8-163">Discounts taken to discount lost per vendor group</span></span></li></ul>                                                                              |
|      <span data-ttu-id="848d8-164">In de toekomst verschuldigde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-164">Invoices due in future</span></span>       |                                                 <ul><li><span data-ttu-id="848d8-165">In de toekomst verschuldigde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-165">Invoices due in future</span></span></li><li><span data-ttu-id="848d8-166">Details in de toekomst verschuldigde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-166">Invoices due in future details</span></span></li><li><span data-ttu-id="848d8-167">In de toekomst verschuldigde facturen op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-167">Invoices due in future per company</span></span></li><li><span data-ttu-id="848d8-168">In de toekomst verschuldigde facturen op leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="848d8-168">Invoices due in future per vendor group</span></span></li><li><span data-ttu-id="848d8-169">In de toekomst verschuldigde facturen op datum contantkorting</span><span class="sxs-lookup"><span data-stu-id="848d8-169">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="848d8-170">In de toekomst verschuldigde facturen op vervaldatum</span><span class="sxs-lookup"><span data-stu-id="848d8-170">Invoices due in future by due date</span></span></li></ul>                                                  |
|        <span data-ttu-id="848d8-171">Te laat betaalde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-171">Invoices paid late</span></span>         |                                                         <ul><li><span data-ttu-id="848d8-172">Na vervaldatum betaalde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-172">Invoices paid after due date</span></span></li><li><span data-ttu-id="848d8-173">Details na vervaldatum betaalde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-173">Invoices paid after due date details</span></span></li><li><span data-ttu-id="848d8-174">Na vervaldatum betaalde facturen op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-174">Invoices paid after due date per company</span></span></li><li><span data-ttu-id="848d8-175">Na vervaldatum betaalde facturen op leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="848d8-175">Invoices paid after due date per vendor group</span></span></li><li><span data-ttu-id="848d8-176">Te laat betaalde facturen versus op tijd betaalde facturen</span><span class="sxs-lookup"><span data-stu-id="848d8-176">Invoices paid late versus invoices paid on time</span></span></li></ul>                                                          |
|         <span data-ttu-id="848d8-177">Betalingsworkflow</span><span class="sxs-lookup"><span data-stu-id="848d8-177">Payment workflow</span></span>          |                                                                                <ul><li><span data-ttu-id="848d8-178">Workflowexemplaren leverancierbetalingen</span><span class="sxs-lookup"><span data-stu-id="848d8-178">Vendor payment workflow instances</span></span></li><li><span data-ttu-id="848d8-179">Workflowexemplaren leverancierbetalingen op fiatteur</span><span class="sxs-lookup"><span data-stu-id="848d8-179">Vendor payment workflow instances per approver</span></span></li><li><span data-ttu-id="848d8-180">Workflowexemplaren leverancierbetalingen op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-180">Vendor payment workflow instances per company</span></span></li><li><span data-ttu-id="848d8-181">Gemiddeld aantal dagen in workflow op fiatteur</span><span class="sxs-lookup"><span data-stu-id="848d8-181">Average days in workflow by approver</span></span></li></ul>                                                                                |
|    <span data-ttu-id="848d8-182">Saldo verkoper/klant</span><span class="sxs-lookup"><span data-stu-id="848d8-182">Vendor to customer balance</span></span>     |                                                                                                                   <ul><li><span data-ttu-id="848d8-183">Saldo verkoper/klant</span><span class="sxs-lookup"><span data-stu-id="848d8-183">Vendor to customer balance</span></span></li><li><span data-ttu-id="848d8-184">Saldo verkoper/klant op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-184">Vendor to customer balance per company</span></span></li><li><span data-ttu-id="848d8-185">Details saldo verkoper/klant</span><span class="sxs-lookup"><span data-stu-id="848d8-185">Vendor to customer balance details</span></span></li></ul>                                                                                                                    |
|    <span data-ttu-id="848d8-186">Facturen met geblokkeerde betaling</span><span class="sxs-lookup"><span data-stu-id="848d8-186">Invoices with payment hold</span></span>     |                                                                                         <ul><li><span data-ttu-id="848d8-187">Facturen met geblokkeerde betaling</span><span class="sxs-lookup"><span data-stu-id="848d8-187">Invoices with payment hold</span></span></li><li><span data-ttu-id="848d8-188">Details facturen met geblokkeerde betaling</span><span class="sxs-lookup"><span data-stu-id="848d8-188">Invoices with payment hold details</span></span></li><li><span data-ttu-id="848d8-189">Facturen met geblokkeerde betaling op bedrijf</span><span class="sxs-lookup"><span data-stu-id="848d8-189">Invoices with payment hold per company</span></span></li><li><span data-ttu-id="848d8-190">Facturen met geblokkeerde betaling op leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="848d8-190">Invoices with payment hold per vendor group</span></span></li></ul>                                                                                          |
