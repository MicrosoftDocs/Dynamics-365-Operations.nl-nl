---
title: Journaalboekingen tegenboeken
description: Dit onderwerp beschrijft mogelijkheden waarmee u boekstukken kunt tegenboeken uit de lijst met boekstuktransacties of vanuit financiële journalen.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ab53f4b8888f77cd41ccbd7956ed307ba1b54ff
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897131"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="40e01-103">Journaalboekingen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="40e01-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40e01-104">In dit onderwerp worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven waarmee u een volledig journaal kunt terugboeken of een of meer boekstukken kunt terugboeken uit de lijst met boekstuktransacties, ongeacht de oorsprong.</span><span class="sxs-lookup"><span data-stu-id="40e01-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="40e01-105">Journalen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="40e01-105">Reversing journals</span></span>

<span data-ttu-id="40e01-106">U kunt journaalregels afzonderlijk tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="40e01-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="40e01-107">Bij het terugdraaien van journaalboekingen kunt u ook een heel financieel journaal tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="40e01-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="40e01-108">Een journaal tegenboeken:</span><span class="sxs-lookup"><span data-stu-id="40e01-108">To reverse a journal:</span></span> 

- <span data-ttu-id="40e01-109">Open het financiële journaal en filter op geboekte journalen.</span><span class="sxs-lookup"><span data-stu-id="40e01-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="40e01-110">Selecteer het menu **Terugboeken** bovenaan de pagina.</span><span class="sxs-lookup"><span data-stu-id="40e01-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="40e01-111">Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="40e01-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="40e01-112">Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="40e01-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="40e01-113">In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum voor de terugboeking invoeren.</span><span class="sxs-lookup"><span data-stu-id="40e01-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="40e01-114">Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in.</span><span class="sxs-lookup"><span data-stu-id="40e01-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="40e01-115">Voer een opmerking in die u aan de terugboektransactie wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="40e01-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="40e01-116">Selecteer de knop **Terugboeken**.</span><span class="sxs-lookup"><span data-stu-id="40e01-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="40e01-117">De transacties worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="40e01-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="40e01-118">Als het boekstuk meer dan 100 regels bevat, wordt het terugboekproces uitgevoerd met behulp van het batchproces.</span><span class="sxs-lookup"><span data-stu-id="40e01-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="40e01-119">U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken.</span><span class="sxs-lookup"><span data-stu-id="40e01-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="40e01-120">Transacties die niet kunnen worden teruggeboekt, worden weergegeven in de historie van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="40e01-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="40e01-121">Als het boekstuk 100 regels of minder bevat, wordt het terugboekproces onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40e01-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="40e01-122">De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="40e01-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="40e01-123">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="40e01-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="40e01-124">Boekstukken tegenboeken vanuit de lijst met boekstuktransacties.</span><span class="sxs-lookup"><span data-stu-id="40e01-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="40e01-125">U kunt ook boekstukken omkeren uit de **Lijst met boekstuktransacties** in alle subadministraties.</span><span class="sxs-lookup"><span data-stu-id="40e01-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="40e01-126">Daarnaast kunt u meerdere boekstukken tegelijk tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="40e01-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="40e01-127">Een of meer boekstukken tegenboeken:</span><span class="sxs-lookup"><span data-stu-id="40e01-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="40e01-128">Selecteer het menu **Terugboeken** bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="40e01-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="40e01-129">Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt</span><span class="sxs-lookup"><span data-stu-id="40e01-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="40e01-130">Selecteer **Ja** als u de bestaande transactiedatums wilt gebruiken of **Nee** als u een nieuwe transactiedatum wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="40e01-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="40e01-131">In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en moet u een nieuwe transactiedatum invoeren om de transactie terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="40e01-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="40e01-132">Als u **Nee** selecteert, voert u een transactiedatum voor de terugboeking in.</span><span class="sxs-lookup"><span data-stu-id="40e01-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="40e01-133">Voer een opmerking in om de terugboektransactie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="40e01-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="40e01-134">Selecteer de knop **Terugboeken**.</span><span class="sxs-lookup"><span data-stu-id="40e01-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="40e01-135">De transacties worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="40e01-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="40e01-136">Als er meer dan 100 terugboekregels zijn, wordt het terugboekproces uitgevoerd met behulp van het batchproces.</span><span class="sxs-lookup"><span data-stu-id="40e01-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="40e01-137">U kunt de resultaten controleren door de opmerkingen in de batchtaak te bekijken.</span><span class="sxs-lookup"><span data-stu-id="40e01-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="40e01-138">Transacties die niet kunnen worden teruggeboekt, worden opgenomen in de historie van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="40e01-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="40e01-139">Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het terugboekproces onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="40e01-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="40e01-140">De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk dat niet kon worden teruggeboekt, wordt weergegeven met de reden waarom het niet kon worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="40e01-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="40e01-141">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="40e01-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="40e01-142">Transacties kunnen alleen worden teruggeboekt als ze voldoen aan de bedrijfsregels voor het terugboeken ervan.</span><span class="sxs-lookup"><span data-stu-id="40e01-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="40e01-143">Leveranciersbetalingen kunnen niet worden teruggeboekt met de functie die in dit onderwerp wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="40e01-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="40e01-144">Leveranciersbetalingen moeten worden teruggeboekt door de stappen te volgen in [Een leveranciersbetaling terugboeken](../accounts-payable/reverse-vendor-payment.md).</span><span class="sxs-lookup"><span data-stu-id="40e01-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](../accounts-payable/reverse-vendor-payment.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]