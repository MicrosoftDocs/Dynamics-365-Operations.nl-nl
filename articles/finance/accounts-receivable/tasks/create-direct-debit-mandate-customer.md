---
title: Een mandaat voor automatische afschrijving maken voor een klant
description: Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177206"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="110ca-103">Een mandaat voor automatische afschrijving maken voor een klant</span><span class="sxs-lookup"><span data-stu-id="110ca-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="110ca-104">Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="110ca-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="110ca-105">Een bankrekening maken</span><span class="sxs-lookup"><span data-stu-id="110ca-105">Create a bank account</span></span>
1. <span data-ttu-id="110ca-106">Ga in het **navigatiedeelvenster** naar **Modules > Klanten > Klanten > Alle klanten.**</span><span class="sxs-lookup"><span data-stu-id="110ca-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="110ca-107">Selecteer een record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="110ca-107">In the list, select a record.</span></span> <span data-ttu-id="110ca-108">Selecteer bijvoorbeeld US-001</span><span class="sxs-lookup"><span data-stu-id="110ca-108">For example, select US-001</span></span>
3. <span data-ttu-id="110ca-109">Klik in het actievenster op **Klant**.</span><span class="sxs-lookup"><span data-stu-id="110ca-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="110ca-110">Klik op **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="110ca-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="110ca-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="110ca-111">Click **New**.</span></span>
6. <span data-ttu-id="110ca-112">Typ een waarde in het veld **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="110ca-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="110ca-113">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="110ca-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="110ca-114">Typ een waarde in het veld **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="110ca-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="110ca-115">Typ een waarde in het veld **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="110ca-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="110ca-116">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="110ca-116">Click **Save**.</span></span>
11. <span data-ttu-id="110ca-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="110ca-117">Close the page.</span></span>
12. <span data-ttu-id="110ca-118">Ga in het **navigatievenster** naar **Modules > Contanten en bankbeheer > Bankrekeningen > Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="110ca-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="110ca-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="110ca-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="110ca-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="110ca-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="110ca-121">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="110ca-121">Click **Edit**.</span></span>
16. <span data-ttu-id="110ca-122">Vouw het sneltabblad **Aanvullende identificatie** uit.</span><span class="sxs-lookup"><span data-stu-id="110ca-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="110ca-123">Typ een waarde in het veld **ID automatische afschrijving**.</span><span class="sxs-lookup"><span data-stu-id="110ca-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="110ca-124">Typ een waarde in het veld **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="110ca-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="110ca-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="110ca-125">Close the page.</span></span>
20. <span data-ttu-id="110ca-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="110ca-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="110ca-127">De elektronische betalingsmethode definiëren</span><span class="sxs-lookup"><span data-stu-id="110ca-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="110ca-128">Ga in het **navigatievenster** naar **Modules > Klanten > Instelling van betalingen > Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="110ca-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="110ca-129">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="110ca-129">Click **New**.</span></span>
3. <span data-ttu-id="110ca-130">Typ een waarde in het veld **Betalingsmethode**.</span><span class="sxs-lookup"><span data-stu-id="110ca-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="110ca-131">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="110ca-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="110ca-132">Typ Elektronische betaling in het veld **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="110ca-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="110ca-133">Het betalingstype bij een betalingsmethode voor het mandaat voor automatische afschrijving moet Elektronische betaling zijn.</span><span class="sxs-lookup"><span data-stu-id="110ca-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="110ca-134">Selecteer Ja in het veld **Mandaat vereisen**.</span><span class="sxs-lookup"><span data-stu-id="110ca-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="110ca-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="110ca-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="110ca-136">Voeg een mandaat voor automatische afschrijving toe aan een klant.</span><span class="sxs-lookup"><span data-stu-id="110ca-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="110ca-137">Ga in het **navigatiedeelvenster** naar **Modules > Klanten > Klanten > Alle klanten.**</span><span class="sxs-lookup"><span data-stu-id="110ca-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="110ca-138">Selecteer een record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="110ca-138">In the list, select a record.</span></span> <span data-ttu-id="110ca-139">Selecteer bijvoorbeeld US-001</span><span class="sxs-lookup"><span data-stu-id="110ca-139">For example, select US-001</span></span>
3. <span data-ttu-id="110ca-140">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="110ca-140">Click **Edit**.</span></span>
4. <span data-ttu-id="110ca-141">Vouw het sneltabblad **Standaardwaarden betaling** uit.</span><span class="sxs-lookup"><span data-stu-id="110ca-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="110ca-142">Typ of selecteer een waarde in het veld **Betalingsmethode.**</span><span class="sxs-lookup"><span data-stu-id="110ca-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="110ca-143">Vouw het sneltabblad **Standaardwaarden betaling** uit.</span><span class="sxs-lookup"><span data-stu-id="110ca-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="110ca-144">Vouw het sneltabblad **Mandaten voor automatische afschrijving** uit.</span><span class="sxs-lookup"><span data-stu-id="110ca-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="110ca-145">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="110ca-145">Click **Add**.</span></span>
9. <span data-ttu-id="110ca-146">Typ of selecteer een waarde in het veld **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="110ca-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="110ca-147">Typ of selecteer een waarde in het veld **Bankrekening van crediteur**.</span><span class="sxs-lookup"><span data-stu-id="110ca-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="110ca-148">Voer in het veld **Betalingsfrequentie** het aantal betalingen in dat u voor dit mandaat verwacht te verwerken.</span><span class="sxs-lookup"><span data-stu-id="110ca-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="110ca-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="110ca-149">Click **OK**.</span></span>
13. <span data-ttu-id="110ca-150">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="110ca-150">Click **Print**.</span></span>
14. <span data-ttu-id="110ca-151">Klik op **Mandaatrapport**.</span><span class="sxs-lookup"><span data-stu-id="110ca-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="110ca-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="110ca-152">Close the page.</span></span>
16. <span data-ttu-id="110ca-153">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="110ca-153">Click **Edit**.</span></span>
17. <span data-ttu-id="110ca-154">Voer een datum in het veld **Datum handtekening** in.</span><span class="sxs-lookup"><span data-stu-id="110ca-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="110ca-155">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="110ca-155">Click **Yes**.</span></span>
19. <span data-ttu-id="110ca-156">Voer de locatie in waar het mandaat is ondertekend.</span><span class="sxs-lookup"><span data-stu-id="110ca-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="110ca-157">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="110ca-157">Click **OK**.</span></span>
21. <span data-ttu-id="110ca-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="110ca-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="110ca-159">Een vrije-tekstfactuur met mandaat maken</span><span class="sxs-lookup"><span data-stu-id="110ca-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="110ca-160">Ga in het **navigatievenster** naar **Modules > Klanten > Facturen > Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="110ca-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="110ca-161">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="110ca-161">Click **New**.</span></span>
3. <span data-ttu-id="110ca-162">Selecteer de klant aan wie u het mandaat hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="110ca-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="110ca-163">Typ of selecteer een waarde in het veld **Mandaat-id voor automatische afschrijving**.</span><span class="sxs-lookup"><span data-stu-id="110ca-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>
