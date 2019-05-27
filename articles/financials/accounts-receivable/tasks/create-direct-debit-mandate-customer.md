---
title: Een mandaat voor automatische afschrijving maken voor een klant
description: Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572530"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="4d76b-103">Een mandaat voor automatische afschrijving maken voor een klant</span><span class="sxs-lookup"><span data-stu-id="4d76b-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d76b-104">Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d76b-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="4d76b-105">Een bankrekening maken</span><span class="sxs-lookup"><span data-stu-id="4d76b-105">Create a bank account</span></span>
1. <span data-ttu-id="4d76b-106">Ga naar Klanten > Klanten > Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="4d76b-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="4d76b-107">Selecteer bijvoorbeeld US-001</span><span class="sxs-lookup"><span data-stu-id="4d76b-107">For example, select US-001</span></span>
3. <span data-ttu-id="4d76b-108">Klik in het actievenster op Klant.</span><span class="sxs-lookup"><span data-stu-id="4d76b-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="4d76b-109">Klik op Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="4d76b-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="4d76b-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4d76b-110">Click New.</span></span>
6. <span data-ttu-id="4d76b-111">Typ een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="4d76b-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="4d76b-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4d76b-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="4d76b-113">Typ een waarde in het veld IBAN.</span><span class="sxs-lookup"><span data-stu-id="4d76b-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="4d76b-114">Typ een waarde in het veld Valuta.</span><span class="sxs-lookup"><span data-stu-id="4d76b-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="4d76b-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4d76b-115">Click Save.</span></span>
11. <span data-ttu-id="4d76b-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d76b-116">Close the page.</span></span>
12. <span data-ttu-id="4d76b-117">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="4d76b-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="4d76b-118">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4d76b-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="4d76b-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4d76b-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="4d76b-120">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4d76b-120">Click Edit.</span></span>
16. <span data-ttu-id="4d76b-121">Vouw de sectie Aanvullende identificatie uit.</span><span class="sxs-lookup"><span data-stu-id="4d76b-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="4d76b-122">Typ een waarde in het veld ID automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="4d76b-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="4d76b-123">Typ een waarde in het veld IBAN.</span><span class="sxs-lookup"><span data-stu-id="4d76b-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="4d76b-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d76b-124">Close the page.</span></span>
20. <span data-ttu-id="4d76b-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d76b-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="4d76b-126">De elektronische betalingsmethode definiëren</span><span class="sxs-lookup"><span data-stu-id="4d76b-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="4d76b-127">Ga naar Klanten > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="4d76b-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="4d76b-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4d76b-128">Click New.</span></span>
3. <span data-ttu-id="4d76b-129">Typ een waarde in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="4d76b-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="4d76b-130">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4d76b-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4d76b-131">Het betalingstype bij een betalingsmethode voor het mandaat voor automatische afschrijving moet Elektronische betaling zijn.</span><span class="sxs-lookup"><span data-stu-id="4d76b-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="4d76b-132">Selecteer Ja in het veld Mandaat vereisen.</span><span class="sxs-lookup"><span data-stu-id="4d76b-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="4d76b-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d76b-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="4d76b-134">Voeg een mandaat voor automatische afschrijving toe aan een klant.</span><span class="sxs-lookup"><span data-stu-id="4d76b-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="4d76b-135">Ga naar Klanten > Klanten > Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="4d76b-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="4d76b-136">Selecteer bijvoorbeeld US-001</span><span class="sxs-lookup"><span data-stu-id="4d76b-136">For example, select US-001</span></span>
3. <span data-ttu-id="4d76b-137">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4d76b-137">Click Edit.</span></span>
4. <span data-ttu-id="4d76b-138">Vouw de sectie van Standaardwaarden betaling uit.</span><span class="sxs-lookup"><span data-stu-id="4d76b-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="4d76b-139">Typ of selecteer een waarde in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="4d76b-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="4d76b-140">Vouw de sectie van Standaardwaarden betaling uit.</span><span class="sxs-lookup"><span data-stu-id="4d76b-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="4d76b-141">Vouw de sectie Mandaten voor automatische afschrijving uit.</span><span class="sxs-lookup"><span data-stu-id="4d76b-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="4d76b-142">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4d76b-142">Click Add.</span></span>
9. <span data-ttu-id="4d76b-143">Typ of selecteer een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="4d76b-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="4d76b-144">Typ of selecteer een waarde in het veld Bankrekening van crediteur.</span><span class="sxs-lookup"><span data-stu-id="4d76b-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="4d76b-145">Voer het aantal betalingen in dat u voor dit mandaat verwacht te verwerken.</span><span class="sxs-lookup"><span data-stu-id="4d76b-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="4d76b-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4d76b-146">Click OK.</span></span>
13. <span data-ttu-id="4d76b-147">Klik op Afdrukken.</span><span class="sxs-lookup"><span data-stu-id="4d76b-147">Click Print.</span></span>
14. <span data-ttu-id="4d76b-148">Klik op Mandaatrapport.</span><span class="sxs-lookup"><span data-stu-id="4d76b-148">Click Mandate report.</span></span>
15. <span data-ttu-id="4d76b-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d76b-149">Close the page.</span></span>
16. <span data-ttu-id="4d76b-150">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4d76b-150">Click Edit.</span></span>
17. <span data-ttu-id="4d76b-151">Voer een datum in het veld Handtekening in.</span><span class="sxs-lookup"><span data-stu-id="4d76b-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="4d76b-152">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="4d76b-152">Click Yes.</span></span>
19. <span data-ttu-id="4d76b-153">Voer de locatie in waar het mandaat is ondertekend.</span><span class="sxs-lookup"><span data-stu-id="4d76b-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="4d76b-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4d76b-154">Click OK.</span></span>
21. <span data-ttu-id="4d76b-155">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d76b-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="4d76b-156">Een vrije-tekstfactuur met mandaat maken</span><span class="sxs-lookup"><span data-stu-id="4d76b-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="4d76b-157">Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.</span><span class="sxs-lookup"><span data-stu-id="4d76b-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="4d76b-158">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4d76b-158">Click New.</span></span>
3. <span data-ttu-id="4d76b-159">Selecteer de klant aan wie u het mandaat hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4d76b-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="4d76b-160">Typ of selecteer een waarde in het veld Mandaat-id voor automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="4d76b-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

