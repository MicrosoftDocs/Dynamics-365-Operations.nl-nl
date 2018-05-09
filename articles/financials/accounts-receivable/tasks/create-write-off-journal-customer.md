--- 
title: Een afschrijvingsjournaal voor een klant maken
description: Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c90ff4abd343936612866b07577062fe1814085b
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="541d8-103">Een afschrijvingsjournaal voor een klant maken</span><span class="sxs-lookup"><span data-stu-id="541d8-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="541d8-104">Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant.</span><span class="sxs-lookup"><span data-stu-id="541d8-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="541d8-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="541d8-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="541d8-106">De afschrijvingsparameters instellen</span><span class="sxs-lookup"><span data-stu-id="541d8-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="541d8-107">Ga naar Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="541d8-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="541d8-108">Klik op het tabblad Incasso's.</span><span class="sxs-lookup"><span data-stu-id="541d8-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="541d8-109">Vouw de sectie Afschrijven uit of samen.</span><span class="sxs-lookup"><span data-stu-id="541d8-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="541d8-110">Het afschrijvingsjournaal is het algemene journaal dat de afschrijvingstransacties bevat die u maakt.</span><span class="sxs-lookup"><span data-stu-id="541d8-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="541d8-111">U kunt een redencode koppelen aan elke afschrijving.</span><span class="sxs-lookup"><span data-stu-id="541d8-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="541d8-112">U kunt deze standaardinstelling bij de afschrijving overschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="541d8-113">Stel deze optie in op Ja als u de btw van de oorspronkelijke transactie wilt scheiden in de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="541d8-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="541d8-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-114">Close the page.</span></span>
5. <span data-ttu-id="541d8-115">Ga naar Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="541d8-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="541d8-116">De afschrijvingsrekening wordt gebruikt als onkostenrekening of reservecorrectie in het algemene journaal</span><span class="sxs-lookup"><span data-stu-id="541d8-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="541d8-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="541d8-118">Een klantsaldo afschrijven van de pagina met ouderdomssaldi</span><span class="sxs-lookup"><span data-stu-id="541d8-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="541d8-119">Ga naar Crediteringen en aanmaningen > Incasso's > Vervallen saldi.</span><span class="sxs-lookup"><span data-stu-id="541d8-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="541d8-120">Markeer de rij voor de klant die u wilt afschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="541d8-121">Markeer bijvoorbeeld de regel die Birch Company bevat.</span><span class="sxs-lookup"><span data-stu-id="541d8-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="541d8-122">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="541d8-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="541d8-123">Klik op Afschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-123">Click Write off.</span></span>
5. <span data-ttu-id="541d8-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="541d8-124">Click OK.</span></span>
6. <span data-ttu-id="541d8-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-125">Close the page.</span></span>
7. <span data-ttu-id="541d8-126">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="541d8-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="541d8-127">Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat.</span><span class="sxs-lookup"><span data-stu-id="541d8-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="541d8-128">Er wordt één regel gemaakt om het klantsaldo om te keren.</span><span class="sxs-lookup"><span data-stu-id="541d8-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="541d8-129">Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="541d8-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="541d8-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-130">Close the page.</span></span>
10. <span data-ttu-id="541d8-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="541d8-132">Schrijf transacties af vanuit het formulier Incasso's.</span><span class="sxs-lookup"><span data-stu-id="541d8-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="541d8-133">Ga naar Crediteringen en aanmaningen > Incasso's > Vervallen saldi.</span><span class="sxs-lookup"><span data-stu-id="541d8-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="541d8-134">Selecteer de naam van de klant die de transacties heeft die u wilt afschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="541d8-135">Selecteer bijvoorbeeld Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="541d8-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="541d8-136">Markeer de rij voor de eerste transactie.</span><span class="sxs-lookup"><span data-stu-id="541d8-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="541d8-137">Markeer de rij voor de tweede transactie.</span><span class="sxs-lookup"><span data-stu-id="541d8-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="541d8-138">Klik op Afschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-138">Click Write off.</span></span>
6. <span data-ttu-id="541d8-139">Typ "Oninbare vorderingen" in het veld Opmerking reden.</span><span class="sxs-lookup"><span data-stu-id="541d8-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="541d8-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="541d8-140">Click OK.</span></span>
8. <span data-ttu-id="541d8-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-141">Close the page.</span></span>
9. <span data-ttu-id="541d8-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-142">Close the page.</span></span>
10. <span data-ttu-id="541d8-143">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="541d8-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="541d8-144">Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat.</span><span class="sxs-lookup"><span data-stu-id="541d8-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="541d8-145">Er wordt één regel gemaakt om het klantsaldo om te keren.</span><span class="sxs-lookup"><span data-stu-id="541d8-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="541d8-146">Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="541d8-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="541d8-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-147">Close the page.</span></span>
13. <span data-ttu-id="541d8-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="541d8-149">Een factuur afschrijven vanaf de pagina Openstaande klantfacturen</span><span class="sxs-lookup"><span data-stu-id="541d8-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="541d8-150">Ga naar Klanten > Facturen > Openstaande klantfacturen.</span><span class="sxs-lookup"><span data-stu-id="541d8-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="541d8-151">Markeer de regel voor een factuur.</span><span class="sxs-lookup"><span data-stu-id="541d8-151">Mark the line for an invoice.</span></span> <span data-ttu-id="541d8-152">Markeer bijvoorbeeld de regel voor CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="541d8-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="541d8-153">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="541d8-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="541d8-154">Klik op Afschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-154">Click Write off.</span></span>
5. <span data-ttu-id="541d8-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="541d8-155">Click OK.</span></span>
6. <span data-ttu-id="541d8-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="541d8-157">Een klantsaldo afschrijven van de klantpagina</span><span class="sxs-lookup"><span data-stu-id="541d8-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="541d8-158">Ga naar Klanten > Klanten > Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="541d8-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="541d8-159">Een klantrekening selecteren.</span><span class="sxs-lookup"><span data-stu-id="541d8-159">Select a customer account.</span></span> <span data-ttu-id="541d8-160">Selecteer bijvoorbeeld US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="541d8-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="541d8-161">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="541d8-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="541d8-162">Klik op Afschrijven.</span><span class="sxs-lookup"><span data-stu-id="541d8-162">Click Write off.</span></span>
5. <span data-ttu-id="541d8-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="541d8-163">Click OK.</span></span>
6. <span data-ttu-id="541d8-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="541d8-164">Close the page.</span></span>


