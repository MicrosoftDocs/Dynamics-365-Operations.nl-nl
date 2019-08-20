---
title: Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling
description: Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843260"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="e7ad1-104">Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling</span><span class="sxs-lookup"><span data-stu-id="e7ad1-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7ad1-105">Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="e7ad1-106">Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="e7ad1-107">Leverancier 3051 laat Fabrikam een contantkorting van 4 procent nemen als een factuur wordt betaald binnen zeven dagen.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="e7ad1-108">Op 29 jnui voert April een factuur in voor 1000,00.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="e7ad1-109">De leverancier geeft April een korting van 60,00 in plaats van de standaardkorting van 40,00 die beschikbaar is voor de factuur.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="e7ad1-110">April registreert een eenmalige betaling door het Leveranciersbetalingsjournaal te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="e7ad1-111">Ze voert de leverancier voor de betaling in en opent vervolgens de pagina **Transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="e7ad1-112">Ze ziet de factuur en wijzigt de waarde in het veld **Contantkortingsbedrag** naar **60,00**.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="e7ad1-113">Markeren</span><span class="sxs-lookup"><span data-stu-id="e7ad1-113">Mark</span></span>     | <span data-ttu-id="e7ad1-114">Contantkorting gebruiken</span><span class="sxs-lookup"><span data-stu-id="e7ad1-114">Use cash discount</span></span> | <span data-ttu-id="e7ad1-115">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="e7ad1-115">Voucher</span></span>   | <span data-ttu-id="e7ad1-116">Rekening</span><span class="sxs-lookup"><span data-stu-id="e7ad1-116">Account</span></span> | <span data-ttu-id="e7ad1-117">Datum</span><span class="sxs-lookup"><span data-stu-id="e7ad1-117">Date</span></span>      | <span data-ttu-id="e7ad1-118">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="e7ad1-118">Due date</span></span>  | <span data-ttu-id="e7ad1-119">Factuur</span><span class="sxs-lookup"><span data-stu-id="e7ad1-119">Invoice</span></span> | <span data-ttu-id="e7ad1-120">Bedrag in transactievaluta</span><span class="sxs-lookup"><span data-stu-id="e7ad1-120">Amount in transaction currency</span></span> | <span data-ttu-id="e7ad1-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="e7ad1-121">Currency</span></span> | <span data-ttu-id="e7ad1-122">Bedrag om te vereffenen</span><span class="sxs-lookup"><span data-stu-id="e7ad1-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="e7ad1-123">Geselecteerd</span><span class="sxs-lookup"><span data-stu-id="e7ad1-123">Selected</span></span> | <span data-ttu-id="e7ad1-124">Normaal</span><span class="sxs-lookup"><span data-stu-id="e7ad1-124">Normal</span></span>            | <span data-ttu-id="e7ad1-125">Factuur-10040</span><span class="sxs-lookup"><span data-stu-id="e7ad1-125">Inv-10040</span></span> | <span data-ttu-id="e7ad1-126">3051</span><span class="sxs-lookup"><span data-stu-id="e7ad1-126">3051</span></span>    | <span data-ttu-id="e7ad1-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="e7ad1-127">6/29/2015</span></span> | <span data-ttu-id="e7ad1-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="e7ad1-128">7/29/2015</span></span> | <span data-ttu-id="e7ad1-129">10040</span><span class="sxs-lookup"><span data-stu-id="e7ad1-129">10040</span></span>   | <span data-ttu-id="e7ad1-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ad1-130">1,000.00</span></span>                       | <span data-ttu-id="e7ad1-131">USD</span><span class="sxs-lookup"><span data-stu-id="e7ad1-131">USD</span></span>      | <span data-ttu-id="e7ad1-132">940,00</span><span class="sxs-lookup"><span data-stu-id="e7ad1-132">940.00</span></span>           |

<span data-ttu-id="e7ad1-133">Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="e7ad1-134">Datum van contantkorting</span><span class="sxs-lookup"><span data-stu-id="e7ad1-134">Cash discount date</span></span>           | <span data-ttu-id="e7ad1-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="e7ad1-135">7/12/2015</span></span> |
| <span data-ttu-id="e7ad1-136">Contantkortingsbedrag</span><span class="sxs-lookup"><span data-stu-id="e7ad1-136">Cash discount amount</span></span>         | <span data-ttu-id="e7ad1-137">60,00</span><span class="sxs-lookup"><span data-stu-id="e7ad1-137">60.00</span></span>     |
| <span data-ttu-id="e7ad1-138">Contantkorting gebruiken</span><span class="sxs-lookup"><span data-stu-id="e7ad1-138">Use cash discount</span></span>            | <span data-ttu-id="e7ad1-139">Normaal</span><span class="sxs-lookup"><span data-stu-id="e7ad1-139">Normal</span></span>    |
| <span data-ttu-id="e7ad1-140">Toegepaste contantkorting</span><span class="sxs-lookup"><span data-stu-id="e7ad1-140">Cash discount taken</span></span>          | <span data-ttu-id="e7ad1-141">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ad1-141">0.00</span></span>      |
| <span data-ttu-id="e7ad1-142">Contantkortingsbedrag dat moet worden toegepast</span><span class="sxs-lookup"><span data-stu-id="e7ad1-142">Cash discount amount to take</span></span> | <span data-ttu-id="e7ad1-143">60,00</span><span class="sxs-lookup"><span data-stu-id="e7ad1-143">60.00</span></span>     |

<span data-ttu-id="e7ad1-144">Vervolgens boekt April het betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-144">April posts the payment journal.</span></span> <span data-ttu-id="e7ad1-145">De factuur is volledig vereffend met een betaling van 940,00 en een korting van 60,00.</span><span class="sxs-lookup"><span data-stu-id="e7ad1-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



