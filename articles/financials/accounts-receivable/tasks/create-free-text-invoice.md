--- 
title: Een vrije-tekstfactuur invoeren
description: Deze taakbegeleiding toont het maken van een vrije-tekstfactuur.
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="42758-103">Een vrije-tekstfactuur invoeren</span><span class="sxs-lookup"><span data-stu-id="42758-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42758-104">Deze taakbegeleiding toont het maken van een vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="42758-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="42758-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42758-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="42758-106">Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.</span><span class="sxs-lookup"><span data-stu-id="42758-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="42758-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="42758-107">Click New.</span></span>
3. <span data-ttu-id="42758-108">Selecteer in het veld Klantrekening een waarde.</span><span class="sxs-lookup"><span data-stu-id="42758-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="42758-109">De factuurrekening wordt standaard ingesteld op dezelfde rekening als wordt gebruikt voor de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="42758-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="42758-110">De boekhoudstatus begint met Onderhanden als de factuur niet is geboekt.</span><span class="sxs-lookup"><span data-stu-id="42758-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="42758-111">Het factuurnummer wordt toegewezen wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="42758-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="42758-112">Als u SEPA-mandaten gebruikt, wordt het mandaat voor automatische afschrijving automatisch ingevuld met een mandaat wanneer u de klantrekening selecteert.</span><span class="sxs-lookup"><span data-stu-id="42758-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="42758-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="42758-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="42758-114">Geef in het veld Hoofdrekening een rekeningnummer zonder dimensies op.</span><span class="sxs-lookup"><span data-stu-id="42758-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="42758-115">U kunt ook één of meerdere tekens voor de hoofdrekening invoeren en de zoekopdracht gebruiken om uw rekening te zoeken.</span><span class="sxs-lookup"><span data-stu-id="42758-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="42758-116">Verderop in deze handleiding voert u dimensies in.</span><span class="sxs-lookup"><span data-stu-id="42758-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="42758-117">Vouw het sneltabblad Regeldetails uit zodat u dimensies kunt toevoegen aan uw hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="42758-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="42758-118">Klik op het tabblad Financiële dimensieregel.</span><span class="sxs-lookup"><span data-stu-id="42758-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="42758-119">De dimensies gelden uitsluitend voor de geselecteerde regel.</span><span class="sxs-lookup"><span data-stu-id="42758-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="42758-120">De btw-groep wordt ingevuld van de klant.</span><span class="sxs-lookup"><span data-stu-id="42758-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="42758-121">Als de klant geen btw-groep heeft, wordt de btw-groep van de hoofdrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42758-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="42758-122">De btw-groep van het artikel wordt ingevuld vanuit de hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="42758-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="42758-123">Als de hoofdrekening geen btw-groep voor het artikel heeft, wordt de btw-groep voor het artikel in de grootboekparameters voor btw gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42758-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="42758-124">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="42758-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="42758-125">De hoeveelheid is optioneel.</span><span class="sxs-lookup"><span data-stu-id="42758-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="42758-126">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="42758-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="42758-127">De eenheidsprijs is optioneel.</span><span class="sxs-lookup"><span data-stu-id="42758-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="42758-128">Het bedrag wordt berekend als de hoeveelheid keer de eenheidsprijs.</span><span class="sxs-lookup"><span data-stu-id="42758-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="42758-129">U kunt die berekening echter negeren en een bedrag invoeren.</span><span class="sxs-lookup"><span data-stu-id="42758-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="42758-130">Klik op Btw om de berekende btw voor uw factuur te bekijken.</span><span class="sxs-lookup"><span data-stu-id="42758-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="42758-131">Bekijk de btw-bedragen op deze pagina of u kunt de bedragen op het tabblad Correctie negeren.</span><span class="sxs-lookup"><span data-stu-id="42758-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="42758-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42758-132">Click OK.</span></span>
12. <span data-ttu-id="42758-133">Klik op Toeslagen om een toeslag aan de factuur toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="42758-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="42758-134">Typ een waarde in het veld Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="42758-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="42758-135">Voer een nummer in het veld Waarde van toeslagen in.</span><span class="sxs-lookup"><span data-stu-id="42758-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="42758-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="42758-136">Close the page.</span></span>
16. <span data-ttu-id="42758-137">Klik op Totalen om de overzichtsfactuurdetails en totalen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="42758-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="42758-138">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="42758-138">Click Close.</span></span>
18. <span data-ttu-id="42758-139">Klik op Boeken om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="42758-139">Click Post to post the invoice.</span></span> <span data-ttu-id="42758-140">U kunt annuleren voordat u boekt.</span><span class="sxs-lookup"><span data-stu-id="42758-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="42758-141">Als u de timing voor het afdrukken van de facturen wilt wijzigen: Selecteer Huidig om elke factuur af te drukken wanneer deze wordt bijgewerkt of Na om alle facturen af te drukken die zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="42758-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="42758-142">Als u wilt wijzigen hoe de kredietlimiet van de klant wordt gecontroleerd voordat er wordt geboekt, wijzigt u het type kredietlimiet.</span><span class="sxs-lookup"><span data-stu-id="42758-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="42758-143">Als u de factuur wilt afdrukken, selecteert u Ja.</span><span class="sxs-lookup"><span data-stu-id="42758-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="42758-144">Als u de factuur wilt boeken, selecteert u Ja.</span><span class="sxs-lookup"><span data-stu-id="42758-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="42758-145">U kunt de factuur afdrukken zonder te boeken.</span><span class="sxs-lookup"><span data-stu-id="42758-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="42758-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42758-146">Click OK.</span></span>


