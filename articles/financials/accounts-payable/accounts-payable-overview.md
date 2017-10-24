---
title: Leveranciers configureren
description: In dit artikel worden de pagina's beschreven die u gebruikt voor het instellen van algemene en optionele functionaliteit voor Leveranciers in Microsoft Dynamics 365 for Finance and Operations. Daarnaast worden de stappen beschreven die u moet uitvoeren voordat u Leveranciers kunt instellen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 49e5c81dda8434a6e02106a8d7ee10233e43d172
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="configure-accounts-payable"></a><span data-ttu-id="cca88-104">Leveranciers configureren</span><span class="sxs-lookup"><span data-stu-id="cca88-104">Configure Accounts payable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cca88-105">In dit artikel worden de pagina's beschreven die u gebruikt voor het instellen van algemene en optionele functionaliteit voor Leveranciers in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cca88-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="cca88-106">Daarnaast worden de stappen beschreven die u moet uitvoeren voordat u Leveranciers kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="cca88-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="cca88-107">Vereisten voor het configureren van Leveranciers</span><span class="sxs-lookup"><span data-stu-id="cca88-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="cca88-108">Voordat u Leveranciers kunt configureren, moet u de volgende instellingen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="cca88-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="cca88-109">In Grootboek</span><span class="sxs-lookup"><span data-stu-id="cca88-109">In General ledger:</span></span>
    -   <span data-ttu-id="cca88-110">Als u betalingsjournalen wilt gebruiken, moet u betalingsjournalen configureren.</span><span class="sxs-lookup"><span data-stu-id="cca88-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="cca88-111">Als u van plan bent wisselkoerscorrecties uit te voeren, moet valutacodes configureren op de pagina Valuta, wisselkoerstypen configureren op de pagina Wisselkoerstypen en de wisselkoersen voor de valuta configureren op de pagina Valutawisselkoersen.</span><span class="sxs-lookup"><span data-stu-id="cca88-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="cca88-112">Stel in Contant- en bankbeheer de bankrekeningen in die u wilt gebruiken in combinatie met bepaalde betalingswijzen.</span><span class="sxs-lookup"><span data-stu-id="cca88-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="cca88-113">Configuratiepagina's voor Leveranciers</span><span class="sxs-lookup"><span data-stu-id="cca88-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="cca88-114">Gebruik de volgende pagina's om de basisfunctionaliteit van Leveranciers in te stellen voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="cca88-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="cca88-115">De pagina's worden weergegeven in de aanbevolen volgorde van configuratie.</span><span class="sxs-lookup"><span data-stu-id="cca88-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="cca88-116">Voor een eenvoudiger configuratieproces kunt u sjablonen maken op basis van de eerste records die u maakt.</span><span class="sxs-lookup"><span data-stu-id="cca88-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="cca88-117">In een sjabloon worden meestal waarden ingevuld in veel velden, die de functies vertegenwoordigen die de organisatie wil implementeren voor een bepaald type leverancier.</span><span class="sxs-lookup"><span data-stu-id="cca88-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="cca88-118">Definieer op de pagina Betalingsvoorwaarden de betalingsvoorwaarden die u toewijst aan verkooporders, inkooporders, klanten en leveranciers, en die de vervaldatums van facturen bepalen.</span><span class="sxs-lookup"><span data-stu-id="cca88-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="cca88-119">Zie [Bijzondere kosten voor leveranciersbetalingen definiëren](tasks/define-vendor-payment-fees.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="cca88-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="cca88-120">Maak en beheer op de pagina Betalingsmethoden - leveranciers informatie over hoe de organisatie zijn leveranciers betaalt.</span><span class="sxs-lookup"><span data-stu-id="cca88-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="cca88-121">Maak en beheer op de pagina Leveranciersgroepen leveranciersgroepen die belangrijke parameters delen voor boeking, vereffening en betaling, rapportage en prognoses.</span><span class="sxs-lookup"><span data-stu-id="cca88-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="cca88-122">Definieer op de pagina Leveranciersboekingsprofiel hoe leverancierstransacties naar het grootboek worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="cca88-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="cca88-123">Configureer op de pagina Parameters van module Leveranciers de standaardinstellingen die worden toegepast als geen specifiekere instelling is opgegeven, parameters voor verschillende typen functionaliteit en de verschillende nummerreeksen voor Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="cca88-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="cca88-124">Definieer op de pagina Formulierinstelling de indeling van verschillende documenten die gerelateerd zijn aan leveranciers en die de organisatie gebruikt om ontvangsten van leveranciers bij te houden en redenen in te voeren voor de betalingsstroom naar leveranciers.</span><span class="sxs-lookup"><span data-stu-id="cca88-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="cca88-125">Maak en beheer op de pagina Leveranciers leverancierrekeningen, waaronder de btw-dienst waarbij uw organisatie btw-aangifte doet</span><span class="sxs-lookup"><span data-stu-id="cca88-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="cca88-126">Optionele instellingspagina´s voor Leveranciers</span><span class="sxs-lookup"><span data-stu-id="cca88-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="cca88-127">Naast de basisfunctionaliteit heeft Leveranciers nog andere functionaliteit die u kunt configureren.</span><span class="sxs-lookup"><span data-stu-id="cca88-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="cca88-128">De aanvullende configuratiepagina's zijn geordend op functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="cca88-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="cca88-129">**Beleid**</span><span class="sxs-lookup"><span data-stu-id="cca88-129">**Policies**</span></span>
-   <span data-ttu-id="cca88-130">Configureer op de pagina Leveranciersfactuurbeleid de beleidsregels voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="cca88-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="cca88-131">**Factuurvereffening**</span><span class="sxs-lookup"><span data-stu-id="cca88-131">**Invoice matching**</span></span>

-   <span data-ttu-id="cca88-132">Configureer op de pagina Toleranties voor factuurtotalen de toleranties voor factuurtotalen.</span><span class="sxs-lookup"><span data-stu-id="cca88-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="cca88-133">Configureer op de pagina Overeenstemmingbeleid het beleid voor tweewegs- of driewegsovereenstemming.</span><span class="sxs-lookup"><span data-stu-id="cca88-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="cca88-134">Configureer op de pagina Prijstoleranties de toleranties voor eenheidsprijzen.</span><span class="sxs-lookup"><span data-stu-id="cca88-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="cca88-135">Configureer op de pagina Tolerantiegroepen voor artikelprijzen de tolerantiegroepen voor artikelprijzen.</span><span class="sxs-lookup"><span data-stu-id="cca88-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="cca88-136">Configureer op de pagina Tolerantiegroepen voor leveranciersprijzen de tolerantiegroepen voor leveranciersprijzen.</span><span class="sxs-lookup"><span data-stu-id="cca88-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="cca88-137">Configureer op de pagina Toeslagentoleranties de toleranties voor toeslagen.</span><span class="sxs-lookup"><span data-stu-id="cca88-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="cca88-138">**Workflow**</span><span class="sxs-lookup"><span data-stu-id="cca88-138">**Workflow**</span></span>

-   <span data-ttu-id="cca88-139">Configureer op de pagina Leveranciersworkflows de workflows voor journaalgoedkeuringen en inkoopopdrachten.</span><span class="sxs-lookup"><span data-stu-id="cca88-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="cca88-140">**Redenen**</span><span class="sxs-lookup"><span data-stu-id="cca88-140">**Reasons**</span></span>

-   <span data-ttu-id="cca88-141">Configureer op de pagina Leveranciersredenen de redencodes.</span><span class="sxs-lookup"><span data-stu-id="cca88-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="cca88-142">**Toeslagen**</span><span class="sxs-lookup"><span data-stu-id="cca88-142">**Charges**</span></span>

-   <span data-ttu-id="cca88-143">Configureer op de pagina Toeslagcode de codes voor de toeslagen die in inkooporders worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cca88-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="cca88-144">Maak en beheer op de pagina Toeslaggroep van leverancier de toeslagengroepen voor leveranciers.</span><span class="sxs-lookup"><span data-stu-id="cca88-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="cca88-145">Maak en beheer op de pagina Toeslaggroepen van artikel de toeslagengroepen voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="cca88-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="cca88-146">Definieer op de pagina Automatische toeslagen de toeslagen die automatisch aan orders worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="cca88-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="cca88-147">**Bijkomende artikelen**</span><span class="sxs-lookup"><span data-stu-id="cca88-147">**Supplementary items**</span></span>

-   <span data-ttu-id="cca88-148">Maak en beheer op de pagina Bijkomende artikelengroepen - Leverancier de bijkomende artikelengroepen voor leveranciers.</span><span class="sxs-lookup"><span data-stu-id="cca88-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="cca88-149">Maak en beheer op de pagina Bijkomende artikelengroepen - Voorraad de bijkomende artikelengroepen voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="cca88-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="cca88-150">**Verdeling**</span><span class="sxs-lookup"><span data-stu-id="cca88-150">**Distribution**</span></span>

-   <span data-ttu-id="cca88-151">Maak en beheer op de pagina Leveringsvoorwaarden de voorwaarden voor overdracht van artikelen van de verkoper aan de koper.</span><span class="sxs-lookup"><span data-stu-id="cca88-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="cca88-152">Maak en beheer op de pagina Leveringsmethoden de transportwijzen die worden gebruikt om artikelen te verzenden van de verkoper naar de koper.</span><span class="sxs-lookup"><span data-stu-id="cca88-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="cca88-153">Maak en beheer op de pagina Bestemmingscodes de ID's en beschrijvingen van bestemmingen voor levering.</span><span class="sxs-lookup"><span data-stu-id="cca88-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="cca88-154">**Formulieren**</span><span class="sxs-lookup"><span data-stu-id="cca88-154">**Forms**</span></span>

-   <span data-ttu-id="cca88-155">Maak op de pagina Formuliernotities de standaardtekst die op verschillende pagina's wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cca88-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="cca88-156">Configureer op de pagina Sorteerparameters voor formulier de sorteervolgorde voor bestelopdrachten, ontvangstlijsten, pakbonnen en facturen.</span><span class="sxs-lookup"><span data-stu-id="cca88-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="cca88-157">Configureer op de pagina Instelling afdrukbeheer de afdrukbeheerinformatie voor originelen en kopieën van pagina's.</span><span class="sxs-lookup"><span data-stu-id="cca88-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="cca88-158">**Betalingen**</span><span class="sxs-lookup"><span data-stu-id="cca88-158">**Payments**</span></span>

-   <span data-ttu-id="cca88-159">Configureer en beheer op de pagina Contantkortingen de voorwaarden voor het verkrijgen van contantkortingen.</span><span class="sxs-lookup"><span data-stu-id="cca88-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="cca88-160">De contantkortingscodes worden gekoppeld aan leveranciers en toegepast op inkooporders.</span><span class="sxs-lookup"><span data-stu-id="cca88-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="cca88-161">Configureer op de pagina Betalingsschema's de betalingsschema's die worden gebruikt om betalingen in termijnen door leveranciers te beheren.</span><span class="sxs-lookup"><span data-stu-id="cca88-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="cca88-162">Definieer op de pagina pagina Betalingsdagen de betalingsdagen die worden gebruikt voor de berekening van vervaldatums, en geef hier de betalingsdagen voor een bepaalde dag van de week of maand.</span><span class="sxs-lookup"><span data-stu-id="cca88-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="cca88-163">Maak en beheer op de pagina Betalingskosten de betalingskosten die zijn gekoppeld aan leveranciers.</span><span class="sxs-lookup"><span data-stu-id="cca88-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="cca88-164">Maak en beheer op de pagina Betalingsopdracht de betalingsinstructies.</span><span class="sxs-lookup"><span data-stu-id="cca88-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="cca88-165">**Statistieken**</span><span class="sxs-lookup"><span data-stu-id="cca88-165">**Statistics**</span></span>

-   <span data-ttu-id="cca88-166">Configureer op de pagina Ouderdomsperiodedefinities door de gebruiker gedefinieerde intervallen om de verdeling van vervallen posten van leverancierrekeningen te analyseren .</span><span class="sxs-lookup"><span data-stu-id="cca88-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="cca88-167">Maak op de pagina Bedrijfstak de bedrijfstakcodes (LOB-codes) die aan leveranciers zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="cca88-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="cca88-168">**1099-belasting**</span><span class="sxs-lookup"><span data-stu-id="cca88-168">**Tax 1099**</span></span>

-   <span data-ttu-id="cca88-169">Verifieer op de pagina **1099-velden** de minimumbedragen die moeten worden opgegeven aan de Internal Revenue Service (IRS), op basis van de meest recente IRS-vereisten. Werk ze bij wanneer nodig.</span><span class="sxs-lookup"><span data-stu-id="cca88-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="cca88-170">**Optionele configuratie voor andere modules**</span><span class="sxs-lookup"><span data-stu-id="cca88-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="cca88-171">**Organisatiebeheer**</span><span class="sxs-lookup"><span data-stu-id="cca88-171">**Organization administration**</span></span>

-   <span data-ttu-id="cca88-172">Configureer op de pagina Nummerreeksen de nummerreeksgroepen voor factuurnummers.</span><span class="sxs-lookup"><span data-stu-id="cca88-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="cca88-173">Configureer op de volgende pagina's de adresgegevens:</span><span class="sxs-lookup"><span data-stu-id="cca88-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="cca88-174">Adresinstelling</span><span class="sxs-lookup"><span data-stu-id="cca88-174">Address setup</span></span>
    -   <span data-ttu-id="cca88-175">NAF-codes</span><span class="sxs-lookup"><span data-stu-id="cca88-175">NAF codes</span></span>
    -   <span data-ttu-id="cca88-176">Postcodes importeren</span><span class="sxs-lookup"><span data-stu-id="cca88-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="cca88-177">**Grootboek**</span><span class="sxs-lookup"><span data-stu-id="cca88-177">**General ledger**</span></span>

-   <span data-ttu-id="cca88-178">Configureer op de pagina Financiële dimensies de financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="cca88-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="cca88-179">Configureer op de volgende pagina's de belastinginformatie:</span><span class="sxs-lookup"><span data-stu-id="cca88-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="cca88-180">Btw-codes</span><span class="sxs-lookup"><span data-stu-id="cca88-180">Sales tax codes</span></span>
    -   <span data-ttu-id="cca88-181">Btw-groepen</span><span class="sxs-lookup"><span data-stu-id="cca88-181">Sales tax groups</span></span>
    -   <span data-ttu-id="cca88-182">Btw-groepen voor artikel</span><span class="sxs-lookup"><span data-stu-id="cca88-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="cca88-183">Rekeninggroep</span><span class="sxs-lookup"><span data-stu-id="cca88-183">Account group</span></span>
    -   <span data-ttu-id="cca88-184">Btw-vrijstellingscodes</span><span class="sxs-lookup"><span data-stu-id="cca88-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="cca88-185">Btw-jurisdictie</span><span class="sxs-lookup"><span data-stu-id="cca88-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="cca88-186">Btw-dienst</span><span class="sxs-lookup"><span data-stu-id="cca88-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="cca88-187">Btw-vereffeningsperioden</span><span class="sxs-lookup"><span data-stu-id="cca88-187">Sales tax settlement periods</span></span>

<span data-ttu-id="cca88-188">**Contanten en bankbeheer**</span><span class="sxs-lookup"><span data-stu-id="cca88-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="cca88-189">Configureer op de pagina Betalingsdoelcodes de betalingsdoelcodes van de centrale bank.</span><span class="sxs-lookup"><span data-stu-id="cca88-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>






