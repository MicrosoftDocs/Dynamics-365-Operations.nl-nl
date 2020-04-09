---
title: Een afschrijvingsjournaal voor een klant maken
description: Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd97f91f1ba53b56150b556fffdfed10a0c8911a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140232"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="04c6c-103">Een afschrijvingsjournaal voor een klant maken</span><span class="sxs-lookup"><span data-stu-id="04c6c-103">Create a write-off journal for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04c6c-104">Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant.</span><span class="sxs-lookup"><span data-stu-id="04c6c-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="04c6c-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="04c6c-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="04c6c-106">De afschrijvingsparameters instellen</span><span class="sxs-lookup"><span data-stu-id="04c6c-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="04c6c-107">Ga naar **navigatievenster > Modules > Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="04c6c-108">Klik op het tabblad **Incasso's**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="04c6c-109">Vouw de sectie **Afschrijven** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="04c6c-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="04c6c-110">Het **afschrijvingsjournaal** is het algemene journaal dat de afschrijvingstransacties bevat die u maakt.</span><span class="sxs-lookup"><span data-stu-id="04c6c-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="04c6c-111">U kunt een redencode koppelen aan elke afschrijving.</span><span class="sxs-lookup"><span data-stu-id="04c6c-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="04c6c-112">U kunt deze standaardinstelling bij de afschrijving overschrijven.</span><span class="sxs-lookup"><span data-stu-id="04c6c-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="04c6c-113">Stel **Btw apart** in op Ja als u de btw van de oorspronkelijke transactie wilt scheiden in de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="04c6c-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="04c6c-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-114">Close the page.</span></span>
5. <span data-ttu-id="04c6c-115">Ga naar **Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="04c6c-116">De afschrijvingsrekening wordt gebruikt als onkostenrekening of reservecorrectie in het algemene journaal.</span><span class="sxs-lookup"><span data-stu-id="04c6c-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="04c6c-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="04c6c-118">Een klantsaldo afschrijven van de pagina met ouderdomssaldi</span><span class="sxs-lookup"><span data-stu-id="04c6c-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="04c6c-119">Ga naar **Crediteringen en aanmaningen > Incasso's > Vervallen saldi**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="04c6c-120">Markeer de rij voor de klant die u wilt afschrijven.</span><span class="sxs-lookup"><span data-stu-id="04c6c-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="04c6c-121">Markeer bijvoorbeeld de regel die Birch Company bevat.</span><span class="sxs-lookup"><span data-stu-id="04c6c-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="04c6c-122">Klik in het **actievenster** op **Incasso**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="04c6c-123">Klik op **Afschrijven**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-123">Click **Write off**.</span></span>
5. <span data-ttu-id="04c6c-124">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-124">Click **OK**.</span></span>
6. <span data-ttu-id="04c6c-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-125">Close the page.</span></span>
7. <span data-ttu-id="04c6c-126">Ga naar **Navigatievenster > Modules > Grootboek > Journaalboekingen > Algemene journalen**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="04c6c-127">Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat.</span><span class="sxs-lookup"><span data-stu-id="04c6c-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="04c6c-128">Er wordt één regel gemaakt om het klantsaldo om te keren.</span><span class="sxs-lookup"><span data-stu-id="04c6c-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="04c6c-129">Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="04c6c-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="04c6c-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-130">Close the page.</span></span>
10. <span data-ttu-id="04c6c-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="04c6c-132">Schrijf transacties af vanuit het formulier Incasso's.</span><span class="sxs-lookup"><span data-stu-id="04c6c-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="04c6c-133">Ga naar **Crediteringen en aanmaningen > Incasso's > Vervallen saldi**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="04c6c-134">Selecteer de naam van de klant die de transacties heeft die u wilt afschrijven.</span><span class="sxs-lookup"><span data-stu-id="04c6c-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="04c6c-135">Selecteer bijvoorbeeld Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="04c6c-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="04c6c-136">Markeer de rij voor de eerste transactie.</span><span class="sxs-lookup"><span data-stu-id="04c6c-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="04c6c-137">Markeer de rij voor de tweede transactie.</span><span class="sxs-lookup"><span data-stu-id="04c6c-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="04c6c-138">Klik op **Afschrijven**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-138">Click **Write off**.</span></span>
6. <span data-ttu-id="04c6c-139">Typ Oninbare vorderingen in het veld **Opmerking reden**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="04c6c-140">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-140">Click **OK**.</span></span>
8. <span data-ttu-id="04c6c-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-141">Close the page.</span></span>
9. <span data-ttu-id="04c6c-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-142">Close the page.</span></span>
10. <span data-ttu-id="04c6c-143">Ga naar **Grootboek > Journaalboekingen > Algemene journalen**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="04c6c-144">Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat.</span><span class="sxs-lookup"><span data-stu-id="04c6c-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="04c6c-145">Er wordt één regel gemaakt om het klantsaldo om te keren.</span><span class="sxs-lookup"><span data-stu-id="04c6c-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="04c6c-146">Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="04c6c-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="04c6c-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-147">Close the page.</span></span>
13. <span data-ttu-id="04c6c-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="04c6c-149">Een factuur afschrijven vanaf de pagina Openstaande klantfacturen</span><span class="sxs-lookup"><span data-stu-id="04c6c-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="04c6c-150">Ga in het navigatievenster naar **Modules > Klanten > Facturen > Openstaande klantfacturen**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="04c6c-151">Markeer de regel voor een factuur.</span><span class="sxs-lookup"><span data-stu-id="04c6c-151">Mark the line for an invoice.</span></span> <span data-ttu-id="04c6c-152">Markeer bijvoorbeeld de regel voor CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="04c6c-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="04c6c-153">Klik in het **actievenster** op **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="04c6c-154">Klik op **Afschrijven**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-154">Click **Write off**.</span></span>
5. <span data-ttu-id="04c6c-155">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-155">Click **OK**.</span></span>
6. <span data-ttu-id="04c6c-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="04c6c-157">Een klantsaldo afschrijven van de klantpagina</span><span class="sxs-lookup"><span data-stu-id="04c6c-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="04c6c-158">Ga naar **Klanten > Klanten > Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="04c6c-159">Een klantrekening selecteren.</span><span class="sxs-lookup"><span data-stu-id="04c6c-159">Select a customer account.</span></span> <span data-ttu-id="04c6c-160">Selecteer bijvoorbeeld US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="04c6c-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="04c6c-161">Klik in het **actievenster** op **Incasso**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="04c6c-162">Klik op **Afschrijven**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-162">Click **Write off**.</span></span>
5. <span data-ttu-id="04c6c-163">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c6c-163">Click **OK**.</span></span>
6. <span data-ttu-id="04c6c-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04c6c-164">Close the page.</span></span>

