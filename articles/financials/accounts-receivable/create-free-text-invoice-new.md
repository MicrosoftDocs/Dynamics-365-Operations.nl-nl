--- 
title: Een vrije-tekstfactuur invoeren
description: In dit artikel wordt beschreven hoe u een vrije-tekstfactuur maakt.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="2d50c-103">Een vrije-tekstfactuur invoeren</span><span class="sxs-lookup"><span data-stu-id="2d50c-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d50c-104">In dit artikel wordt beschreven hoe u een vrije-tekstfactuur maakt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="2d50c-105">Gebruik voor deze procedure het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="2d50c-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="2d50c-106">Een vrije-tekstfactuur invoeren</span><span class="sxs-lookup"><span data-stu-id="2d50c-106">Create a free text invoice</span></span>

1. <span data-ttu-id="2d50c-107">Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.</span><span class="sxs-lookup"><span data-stu-id="2d50c-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2d50c-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2d50c-108">Click New.</span></span>
3. <span data-ttu-id="2d50c-109">Selecteer in het veld Klantrekening een waarde.</span><span class="sxs-lookup"><span data-stu-id="2d50c-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="2d50c-110">De factuurrekening wordt standaard ingesteld op dezelfde rekening als wordt gebruikt voor de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="2d50c-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="2d50c-111">De boekhoudstatus begint met Onderhanden als de factuur niet is geboekt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="2d50c-112">Het factuurnummer wordt toegewezen wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="2d50c-113">Als u SEPA-mandaten gebruikt, wordt het mandaat voor automatische afschrijving automatisch ingevuld met een mandaat wanneer u de klantrekening selecteert.</span><span class="sxs-lookup"><span data-stu-id="2d50c-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="2d50c-114">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="2d50c-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2d50c-115">Geef in het veld Hoofdrekening een rekeningnummer zonder dimensies op.</span><span class="sxs-lookup"><span data-stu-id="2d50c-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="2d50c-116">U kunt ook één of meerdere tekens voor de hoofdrekening invoeren en de zoekopdracht gebruiken om uw rekening te zoeken.</span><span class="sxs-lookup"><span data-stu-id="2d50c-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="2d50c-117">Verderop in deze handleiding voert u dimensies in.</span><span class="sxs-lookup"><span data-stu-id="2d50c-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="2d50c-118">Vouw het sneltabblad Regeldetails uit zodat u dimensies kunt toevoegen aan uw hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="2d50c-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="2d50c-119">Klik op het tabblad Financiële dimensieregel.</span><span class="sxs-lookup"><span data-stu-id="2d50c-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="2d50c-120">De dimensies gelden uitsluitend voor de geselecteerde regel.</span><span class="sxs-lookup"><span data-stu-id="2d50c-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="2d50c-121">De btw-groep wordt ingevuld van de klant.</span><span class="sxs-lookup"><span data-stu-id="2d50c-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="2d50c-122">Als de klant geen btw-groep heeft, wordt de btw-groep van de hoofdrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="2d50c-123">De btw-groep van het artikel wordt ingevuld vanuit de hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="2d50c-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="2d50c-124">Als de hoofdrekening geen btw-groep voor een artikel heeft, wordt de btw-groep voor het artikel in de grootboekparameters voor btw gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="2d50c-125">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="2d50c-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2d50c-126">De hoeveelheid is optioneel.</span><span class="sxs-lookup"><span data-stu-id="2d50c-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="2d50c-127">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="2d50c-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2d50c-128">De eenheidsprijs is optioneel.</span><span class="sxs-lookup"><span data-stu-id="2d50c-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="2d50c-129">Het bedrag wordt berekend als de hoeveelheid keer de eenheidsprijs.</span><span class="sxs-lookup"><span data-stu-id="2d50c-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="2d50c-130">U kunt die berekening echter negeren en een bedrag invoeren.</span><span class="sxs-lookup"><span data-stu-id="2d50c-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="2d50c-131">Klik op Btw om de berekende btw voor uw factuur te bekijken.</span><span class="sxs-lookup"><span data-stu-id="2d50c-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="2d50c-132">Bekijk de btw-bedragen op deze pagina of u kunt de bedragen op het tabblad Correctie negeren.</span><span class="sxs-lookup"><span data-stu-id="2d50c-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="2d50c-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2d50c-133">Click OK.</span></span>
12. <span data-ttu-id="2d50c-134">Klik op Toeslagen om een toeslag aan de factuur toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="2d50c-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="2d50c-135">Typ een waarde in het veld Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="2d50c-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="2d50c-136">Voer een nummer in het veld Waarde van toeslagen in.</span><span class="sxs-lookup"><span data-stu-id="2d50c-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="2d50c-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2d50c-137">Close the page.</span></span>
16. <span data-ttu-id="2d50c-138">Klik op Totalen om de overzichtsfactuurdetails en totalen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2d50c-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="2d50c-139">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="2d50c-139">Click Close.</span></span>
18. <span data-ttu-id="2d50c-140">Klik op Boeken om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="2d50c-140">Click Post to post the invoice.</span></span> <span data-ttu-id="2d50c-141">U kunt annuleren voordat u boekt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="2d50c-142">Als u de timing voor het afdrukken van de facturen wilt wijzigen: Selecteer Huidig om elke factuur af te drukken wanneer deze wordt bijgewerkt of Na om alle facturen af te drukken die zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="2d50c-143">Als u wilt wijzigen hoe de kredietlimiet van de klant wordt gecontroleerd voordat er wordt geboekt, wijzigt u het type kredietlimiet.</span><span class="sxs-lookup"><span data-stu-id="2d50c-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="2d50c-144">Als u de factuur wilt afdrukken, selecteert u Ja.</span><span class="sxs-lookup"><span data-stu-id="2d50c-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="2d50c-145">Als u de factuur wilt boeken, selecteert u Ja.</span><span class="sxs-lookup"><span data-stu-id="2d50c-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="2d50c-146">U kunt de factuur afdrukken zonder te boeken.</span><span class="sxs-lookup"><span data-stu-id="2d50c-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="2d50c-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2d50c-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="2d50c-148">Regels kopiëren</span><span class="sxs-lookup"><span data-stu-id="2d50c-148">Copy lines</span></span>
<span data-ttu-id="2d50c-149">Als u regels in de vrije-tekstfactuur wilt kopiëren, selecteert u een of meer regels en klikt u op Geselecteerde regels kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2d50c-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="2d50c-150">U kunt opgeven hoeveel kopieën u wilt maken en u kunt ook notities en bijlagen kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2d50c-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="2d50c-151">U kunt de verdelingen kopiëren of opnieuw laten maken wanneer u boekt.</span><span class="sxs-lookup"><span data-stu-id="2d50c-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="2d50c-152">Wanneer u de regels hebt gekopieerd, kunt u de gegevens vervolgens zo nodig bewerken.</span><span class="sxs-lookup"><span data-stu-id="2d50c-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="2d50c-153">Een vrije-tekstfactuur maken op basis van een sjabloon</span><span class="sxs-lookup"><span data-stu-id="2d50c-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="2d50c-154">U kunt een vrije-tekstfactuur maken op basis van een sjabloon.</span><span class="sxs-lookup"><span data-stu-id="2d50c-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="2d50c-155">Wanneer u Nieuw van sjabloon op het tabblad Factuur selecteert, kunt u een sjabloonnaam en de klantrekening voor de nieuwe vrije-tekstfactuur selecteren.</span><span class="sxs-lookup"><span data-stu-id="2d50c-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="2d50c-156">U kunt ook kiezen voor de standaardwaarden, zoals de betalingsvoorwaarden en betalingsmethode van de klant, of de waarden gebruiken die zijn opgeslagen met de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="2d50c-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="2d50c-157">Er wordt een nieuwe vrije-tekstfactuur gemaakt en u kunt de waarden in deze factuur bewerken.</span><span class="sxs-lookup"><span data-stu-id="2d50c-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


