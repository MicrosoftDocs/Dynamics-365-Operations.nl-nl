---
title: Journaalboekingen tegenboeken
description: Dit onderwerp beschrijft mogelijkheden waarmee u boekstukken kunt tegenboeken uit de lijst met boekstuktransacties of vanuit financiële journalen.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc2ff30ef5d08759af700d683c207b0f5ed65d5b
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658968"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="aa3d0-103">Journaalboekingen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="aa3d0-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="aa3d0-104">In dit onderwerp worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven waarmee u een volledig journaal kunt terugboeken of een of meer boekstukken kunt terugboeken uit de lijst met boekstuktransacties, ongeacht de oorsprong.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="aa3d0-105">Journalen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="aa3d0-105">Reversing journals</span></span>

<span data-ttu-id="aa3d0-106">U kunt journaalregels afzonderlijk tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="aa3d0-107">Bij het terugdraaien van journaalboekingen kunt u ook een heel financieel journaal tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="aa3d0-108">Een journaal tegenboeken:</span><span class="sxs-lookup"><span data-stu-id="aa3d0-108">To reverse a journal:</span></span> 

- <span data-ttu-id="aa3d0-109">Open het financiële journaal en filter op geboekte journalen.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="aa3d0-110">Selecteer het menu **Terugboeken** bovenaan de pagina.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="aa3d0-111">Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="aa3d0-112">Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="aa3d0-113">In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum voor de terugboeking invoeren.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="aa3d0-114">Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="aa3d0-115">Voer een opmerking in die u aan de terugboektransactie wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="aa3d0-116">Selecteer de knop **Terugboeken**.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="aa3d0-117">De transacties worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="aa3d0-118">Als het boekstuk meer dan 100 regels bevat, wordt het terugboekproces uitgevoerd met behulp van het batchproces.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="aa3d0-119">U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="aa3d0-120">Transacties die niet kunnen worden teruggeboekt, worden weergegeven in de historie van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="aa3d0-121">Als het boekstuk 100 regels of minder bevat, wordt het terugboekproces onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="aa3d0-122">De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="aa3d0-123">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="aa3d0-124">Boekstukken tegenboeken vanuit de lijst met boekstuktransacties.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="aa3d0-125">U kunt ook boekstukken omkeren uit de **Lijst met boekstuktransacties** in alle subadministraties.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="aa3d0-126">Daarnaast kunt u meerdere boekstukken tegelijk tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="aa3d0-127">Een of meer boekstukken tegenboeken:</span><span class="sxs-lookup"><span data-stu-id="aa3d0-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="aa3d0-128">Selecteer het menu **Terugboeken** bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="aa3d0-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="aa3d0-129">Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt</span><span class="sxs-lookup"><span data-stu-id="aa3d0-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="aa3d0-130">Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="aa3d0-131">In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum invoeren om de transactie terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="aa3d0-132">Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="aa3d0-133">Voer een opmerking in om de terugboektransactie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="aa3d0-134">Selecteer de knop **Terugboeken**.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="aa3d0-135">De transacties worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="aa3d0-136">Als er meer dan 100 terugboekregels zijn, wordt het terugboekproces uitgevoerd met behulp van het batchproces.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="aa3d0-137">U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="aa3d0-138">Transacties die niet kunnen worden teruggeboekt, worden opgenomen in de historie van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="aa3d0-139">Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het terugboekproces onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="aa3d0-140">De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="aa3d0-141">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="aa3d0-142">Transacties kunnen alleen worden teruggeboekt als ze voldoen aan de bedrijfsregels voor het terugboeken ervan.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="aa3d0-143">Leveranciersbetalingen kunnen niet worden teruggeboekt met de functie die in dit onderwerp wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="aa3d0-144">Leveranciersbetalingen moeten worden teruggeboekt door de stappen te volgen in [Een leveranciersbetaling terugboeken](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="aa3d0-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

