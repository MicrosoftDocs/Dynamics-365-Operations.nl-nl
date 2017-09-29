---
title: Evenwichtige journalen voor interunit-boekhouding
description: "Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: nl-nl
ms.lasthandoff: 06/29/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="c89aa-103">Evenwichtige journalen voor interunit-boekhouding</span><span class="sxs-lookup"><span data-stu-id="c89aa-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c89aa-104">Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina.</span><span class="sxs-lookup"><span data-stu-id="c89aa-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="c89aa-105">Als boekingen niet in evenwicht zijn op het niveau van de financiële dimensiewaarden, worden automatisch extra boekingen gemaakt om het journaal automatisch in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="c89aa-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="c89aa-106">Deze boekingen gebruiken de boekingstypen **Inter-unit - debet** en**Inter-unit - credit** op de pagina **Rekeningen voor automatische transacties** om de hoofdrekening te bepalen.</span><span class="sxs-lookup"><span data-stu-id="c89aa-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="c89aa-107">Bijvoorbeeld, Vestiging, het tweede segment van de grootboekrekening, wordt geselecteerd als de financiële tegendimensie en de volgende boekingsregels staan op het punt om te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c89aa-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="c89aa-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="c89aa-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="c89aa-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c89aa-109">100.00 DR</span></span> |
| <span data-ttu-id="c89aa-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="c89aa-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="c89aa-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c89aa-111">100.00 DR</span></span> |
| <span data-ttu-id="c89aa-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="c89aa-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="c89aa-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="c89aa-113">200.00 CR</span></span> |

<span data-ttu-id="c89aa-114">In dit geval worden de volgende saldi gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="c89aa-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="c89aa-115">Voor Vestiging MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="c89aa-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="c89aa-116">Voor Vestiging NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c89aa-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="c89aa-117">Daarom worden de volgende posten automatisch gemaakt om het journaal op het niveau van de financiële dimensiewaarden in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="c89aa-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="c89aa-118">(Inter-unit debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="c89aa-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="c89aa-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c89aa-119">100.00 DR</span></span> |
| <span data-ttu-id="c89aa-120">(Inter-unit credit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="c89aa-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="c89aa-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="c89aa-121">100.00 CR</span></span> |






