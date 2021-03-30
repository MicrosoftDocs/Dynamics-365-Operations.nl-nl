---
title: Evenwichtige journalen voor interunit-boekhouding
description: Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5f73606708b8c32a7a8ebc364af6ba57c4c343
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205518"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="88d02-103">Evenwichtige journalen voor interunit-boekhouding</span><span class="sxs-lookup"><span data-stu-id="88d02-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88d02-104">Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina.</span><span class="sxs-lookup"><span data-stu-id="88d02-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="88d02-105">Als boekingen niet in evenwicht zijn op het niveau van de financiële dimensiewaarden, worden automatisch extra boekingen gemaakt om het journaal automatisch in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="88d02-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="88d02-106">Deze boekingen gebruiken de boekingstypen **Inter-unit - debet** en **Inter-unit - credit** op de pagina **Rekeningen voor automatische transacties** om de hoofdrekening te bepalen.</span><span class="sxs-lookup"><span data-stu-id="88d02-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="88d02-107">Bijvoorbeeld, Bedrijfseenheid, het tweede segment van de grootboekrekening, wordt geselecteerd als de financiële tegendimensie en de volgende boekingsregels staan op het punt om te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="88d02-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="88d02-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="88d02-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="88d02-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="88d02-109">100.00 DR</span></span> |
| <span data-ttu-id="88d02-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="88d02-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="88d02-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="88d02-111">100.00 DR</span></span> |
| <span data-ttu-id="88d02-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="88d02-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="88d02-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="88d02-113">200.00 CR</span></span> |

<span data-ttu-id="88d02-114">In dit geval worden de volgende saldi gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="88d02-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="88d02-115">Voor Bedrijfseenheid MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="88d02-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="88d02-116">Voor Bedrijfseenheid MSP = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="88d02-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="88d02-117">Daarom worden de volgende posten automatisch gemaakt om het journaal op het niveau van de financiële dimensiewaarden in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="88d02-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="88d02-118">(Inter-unit debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="88d02-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="88d02-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="88d02-119">100.00 DR</span></span> |
| <span data-ttu-id="88d02-120">(Inter-unit credit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="88d02-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="88d02-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="88d02-121">100.00 CR</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]