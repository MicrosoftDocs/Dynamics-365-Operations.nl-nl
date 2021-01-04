---
title: Klanten terugbetalen
description: In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten. Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644532"
---
# <a name="reimburse-customers"></a><span data-ttu-id="6a27c-104">Klanten terugbetalen</span><span class="sxs-lookup"><span data-stu-id="6a27c-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a27c-105">In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten.</span><span class="sxs-lookup"><span data-stu-id="6a27c-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="6a27c-106">Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen.</span><span class="sxs-lookup"><span data-stu-id="6a27c-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="6a27c-107">De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.</span><span class="sxs-lookup"><span data-stu-id="6a27c-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="6a27c-108">Vereiste</span><span class="sxs-lookup"><span data-stu-id="6a27c-108">Prerequisite</span></span>                                                            | <span data-ttu-id="6a27c-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6a27c-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="6a27c-110">Geef het minimale terugbetalingsbedrag voor de rechtspersoon op.</span><span class="sxs-lookup"><span data-stu-id="6a27c-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="6a27c-111">Voer op de pagina **Parameters van module Klanten** in het gebied **Algemeen** in het veld **Minimum voor terugbetaling** het minimumbedrag in dat voor de klant kan worden terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="6a27c-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="6a27c-112">Optioneel: voeg een leveranciersrekening toe voor elke klant die kan worden terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="6a27c-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="6a27c-113">Selecteer op de pagina **Klanten** op het sneltabblad **Overige details** in het veld **Leveranciersrekening** de leveranciersrekening voor de klant.</span><span class="sxs-lookup"><span data-stu-id="6a27c-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="6a27c-114">Wanneer u terugbetalingstransacties maakt, wordt een leveranciersfactuur gemaakt voor het bedrag van het creditsaldo.</span><span class="sxs-lookup"><span data-stu-id="6a27c-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="6a27c-115">Met het terugbetalingsproces wordt het creditsaldo voor de klantrekening verwijderd en wordt een te betalen saldo voor de leveranciersrekening gemaakt die met de klant overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="6a27c-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="6a27c-116">Voer in Klanten het proces **Terugbetalings** (**Klanten \> Periodieke taken \> Terugbetalen**).</span><span class="sxs-lookup"><span data-stu-id="6a27c-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="6a27c-117">Als u alle transacties wilt groeperen, ongeacht de grootboekdimensies, stelt u de optie **Klant samenvatten** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6a27c-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="6a27c-118">Als u alleen transacties met vergelijkbare grootboekdimensies wilt groeperen, stelt u de optie in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="6a27c-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="6a27c-119">Selecteer **Klanten met openstaande debettransacties opnemen** om klanten te selecteren met openstaande debetbedragen.</span><span class="sxs-lookup"><span data-stu-id="6a27c-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="6a27c-120">Als u specifieke klantrekeningen wilt terugbetalen, selecteert op het sneltabblad **Records die u wilt opnemen** de optie **Filter** en geeft u vervolgens de klantrekeningen op in de query.</span><span class="sxs-lookup"><span data-stu-id="6a27c-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="6a27c-121">De creditbedragen worden overgebracht naar de leveranciersrekeningen van de klanten en worden verwerkt als normale betalingen.</span><span class="sxs-lookup"><span data-stu-id="6a27c-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="6a27c-122">Als een klant geen leverancierrekening heeft, wordt automatisch een eenmalige leverancierrekening voor de klant gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6a27c-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="6a27c-123">Als u de gemaakte terugbetalingstransacties wilt weergeven, gebruikt u het rapport **Terugbetaling** (**Klanten \> Query's en rapporten \> Terugbetalingsrapport**).</span><span class="sxs-lookup"><span data-stu-id="6a27c-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="6a27c-124">In Leveranciers maakt u een betaling voor de leveranciersfacturen die met het terugbetalingsproces zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6a27c-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="6a27c-125">Zie [Overzicht van leveranciersbetalingen](../accounts-payable/Vendor-payments-workspace.md) voor informatie over het betalen van leverancers.</span><span class="sxs-lookup"><span data-stu-id="6a27c-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
