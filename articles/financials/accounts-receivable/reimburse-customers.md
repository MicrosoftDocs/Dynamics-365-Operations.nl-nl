---
title: Klanten terugbetalen
description: In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten. Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36e7e684e207e13baffa7eefd13e8e4a29d99914
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549647"
---
# <a name="reimburse-customers"></a><span data-ttu-id="5f9f6-104">Klanten terugbetalen</span><span class="sxs-lookup"><span data-stu-id="5f9f6-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f9f6-105">In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="5f9f6-106">Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="5f9f6-107">De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="5f9f6-108">Vereiste</span><span class="sxs-lookup"><span data-stu-id="5f9f6-108">Prerequisite</span></span>                                                            | <span data-ttu-id="5f9f6-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5f9f6-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9f6-110">Geef het minimale terugbetalingsbedrag voor de rechtspersoon op.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="5f9f6-111">Voer op de pagina **Parameters van module Klanten** in het gebied **Algemeen** in het veld **Minimum voor terugbetaling** het minimumbedrag in dat voor de klant kan worden terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="5f9f6-112">Optioneel: voeg een leveranciersrekening toe voor elke klant die kan worden terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="5f9f6-113">Selecteer op de pagina **Klanten** op het sneltabblad **Overige details** in het veld **Leveranciersrekening** de leveranciersrekening voor de klant.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="5f9f6-114">Wanneer u terugbetalingstransacties maakt, wordt een leveranciersfactuur gemaakt voor het bedrag van het creditsaldo.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="5f9f6-115">Met het terugbetalingsproces wordt het creditsaldo voor de klantrekening verwijderd en wordt een te betalen saldo voor de leveranciersrekening gemaakt die met de klant overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="5f9f6-116">Voer in Klanten het proces **Terugbetaling** uit.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="5f9f6-117">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="5f9f6-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="5f9f6-118">Als u wilt terugbetalen aan specifieke klantrekeningen, klikt u op **Selecteren** en geeft u de klantrekeningen in de query op.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="5f9f6-119">Klik op **OK** als u wilt terugbetalen aan alle klantrekeningen.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="5f9f6-120">De creditbedragen worden overgebracht naar de leveranciersrekeningen van de klanten en worden verwerkt als normale betalingen.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="5f9f6-121">Als een klant geen leverancierrekening heeft, wordt automatisch een eenmalige leverancierrekening voor de klant gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="5f9f6-122">Als u de terugbetalingstransacties wilt weergeven die zijn gemaakt, gebruikt u de pagina **Terugbetaling**.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="5f9f6-123">In Leveranciers maakt u een betaling voor de leveranciersfacturen die met het terugbetalingsproces zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5f9f6-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>




