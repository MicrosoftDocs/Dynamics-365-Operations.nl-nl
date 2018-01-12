---
title: Overzicht van transitorische posten
description: In dit artikel worden toerekeningen beschreven en wordt aangegeven hoe u deze instelt en transacties maakt.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 47336a19899b1fad0e63265173fd7fd02fc74ec3
ms.openlocfilehash: 4fa27cbfe6129aa78b5e05de704894da173d853b
ms.contentlocale: nl-nl
ms.lasthandoff: 01/12/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="c1876-103">Overzicht van transitorische posten</span><span class="sxs-lookup"><span data-stu-id="c1876-103">Accruals overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c1876-104">In dit artikel worden toerekeningen beschreven en wordt aangegeven hoe u deze instelt en transacties maakt.</span><span class="sxs-lookup"><span data-stu-id="c1876-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="c1876-105">Transitorische posten worden gebruikt in periodetoerekeningsboekhouding om opbrengst bij te houden die wordt verantwoord in de periode waarin deze wordt verdiend en niet wanneer de betaling wordt ontvangen, en om onkosten (kosten) bij te houden die worden verantwoord wanneer ze worden gemaakt en niet wanneer de betaling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1876-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="c1876-106">Toerekeningsschema's</span><span class="sxs-lookup"><span data-stu-id="c1876-106">Accrual schemes</span></span>
<span data-ttu-id="c1876-107">Toerekeningsschema's worden gebruikt om de uitgestelde opbrengst en de kosten in te stellen en hetzelfde toerekeningsschema kan zowel voor opbrengsten als voor kosten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c1876-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="c1876-108">Met transitorische grootboekposten worden de kosten of opbrengsten van een journaalregel zo verdeeld dat de kosten en opbrengsten in de betreffende perioden worden verantwoord.</span><span class="sxs-lookup"><span data-stu-id="c1876-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="c1876-109">Op de pagina **Toerekeningsschema** geeft u de debet- en creditrekeningen op die worden gebruikt wanneer het toerekeningsschema wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c1876-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="c1876-110">**Debet**: met de hoofdrekening die u definieert, wordt de debethoofdrekening op de journaalboekstukregel vervangen.</span><span class="sxs-lookup"><span data-stu-id="c1876-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="c1876-111">Deze rekening wordt ook gebruikt voor de terugboeking van het uitstel op basis van de transitorische grootboekposttransacties.</span><span class="sxs-lookup"><span data-stu-id="c1876-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="c1876-112">**Credit**: met de hoofdrekening die u definieert, wordt de credithoofdrekening op de journaalboekstukregel vervangen.</span><span class="sxs-lookup"><span data-stu-id="c1876-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="c1876-113">Deze rekening wordt ook gebruikt voor de terugboeking van het uitstel op basis van de transitorische grootboekposttransacties.</span><span class="sxs-lookup"><span data-stu-id="c1876-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="c1876-114">Nadat u hebt bepaald welke rekeningen moeten worden gebruikt, kunt u opgeven hoe het boekstuknummer wordt gemaakt wanneer de transitorische posten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c1876-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="c1876-115">U kunt ook opgeven hoe vaak de transacties plaatsvinden, het aantal keren dat de transacties worden gemaakt en wanneer de transacties worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="c1876-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="c1876-116">Nadat het toerekeningsschema is gemaakt, kunt u het in sommige journalen gebruiken met behulp van de functie Transitorische grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="c1876-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="c1876-117">Transitorische grootboekposten</span><span class="sxs-lookup"><span data-stu-id="c1876-117">Ledger accruals</span></span>
<span data-ttu-id="c1876-118">Wanneer u een journaal invoert, kunt u klikken op **Transitorische grootboekposten** in het menu **Functies**.</span><span class="sxs-lookup"><span data-stu-id="c1876-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="c1876-119">Wanneer u vervolgens het toerekeningsschema selecteert, ziet u het basisbedrag van het journaal dat over de periode wordt verspreid, zoals bepaald door het toerekeningsschema.</span><span class="sxs-lookup"><span data-stu-id="c1876-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="c1876-120">Als u bijvoorbeeld de verzekering van een werknemer voor het hele jaar in januari betaalt en het bedrag is 12.000, moet u die onkosten elke maand verantwoorden.</span><span class="sxs-lookup"><span data-stu-id="c1876-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="c1876-121">U kunt de begindatum selecteren.</span><span class="sxs-lookup"><span data-stu-id="c1876-121">You can select the start date.</span></span> <span data-ttu-id="c1876-122">U kunt ook opgeven of het bedrag dat wordt toegerekend, wordt gebaseerd op de rekening of de tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="c1876-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="c1876-123">Nadat u uw selecties hebt gemaakt, klikt u op **Transacties** om alle transacties weer te geven die zijn gemaakt op basis van het toerekeningsschema.</span><span class="sxs-lookup"><span data-stu-id="c1876-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="c1876-124">Bijvoorbeeld: als u het bedrag van 12.000 aan verzekeringsonkosten over het jaar verspreid, ziet u een bedrag van 1000 voor elke maand.</span><span class="sxs-lookup"><span data-stu-id="c1876-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="c1876-125">Nadat u het journaal hebt geboekt, kunt u de transacties bekijken met behulp van de querypagina **Boekstuktransacties**.</span><span class="sxs-lookup"><span data-stu-id="c1876-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="c1876-126">Als een toerekeningsschema niet kan worden toegepast (bijvoorbeeld in geval van een verkooporderfactuur of inkooporderfactuur), kunt u het vooruitbetaalde bedrag crediteren en het onkostenbedrag debiteren.</span><span class="sxs-lookup"><span data-stu-id="c1876-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="c1876-127">Vervolgens kunt u **Tegenrekening** selecteren wanneer u het toerekeningsschema toepast.</span><span class="sxs-lookup"><span data-stu-id="c1876-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="c1876-128">Zie voor meer informatie [Toerekeningsschema's maken](tasks/create-accrual-schemes.md) en [Toenametransacties voor grootboek maken](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="c1876-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

