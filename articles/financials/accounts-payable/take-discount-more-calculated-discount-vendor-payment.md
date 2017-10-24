---
title: Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling
description: Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 39830014593b7b1bc2868afffcca0f77a0c8a029
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="090a0-104">Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling</span><span class="sxs-lookup"><span data-stu-id="090a0-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="090a0-105">Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="090a0-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="090a0-106">Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.</span><span class="sxs-lookup"><span data-stu-id="090a0-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="090a0-107">Leverancier 3051 laat Fabrikam een contantkorting van 4 procent nemen als een factuur wordt betaald binnen zeven dagen.</span><span class="sxs-lookup"><span data-stu-id="090a0-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="090a0-108">Op 29 jnui voert April een factuur in voor 1000,00.</span><span class="sxs-lookup"><span data-stu-id="090a0-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="090a0-109">De leverancier geeft April een korting van 60,00 in plaats van de standaardkorting van 40,00 die beschikbaar is voor de factuur.</span><span class="sxs-lookup"><span data-stu-id="090a0-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="090a0-110">April registreert een eenmalige betaling door het Leveranciersbetalingsjournaal te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="090a0-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="090a0-111">Ze voert de leverancier voor de betaling in en opent vervolgens de pagina **Transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="090a0-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="090a0-112">Ze ziet de factuur en wijzigt de waarde in het veld **Contantkortingsbedrag** naar **60,00**.</span><span class="sxs-lookup"><span data-stu-id="090a0-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>
| <span data-ttu-id="090a0-113">Markeren</span><span class="sxs-lookup"><span data-stu-id="090a0-113">Mark</span></span>     | <span data-ttu-id="090a0-114">Contantkorting gebruiken</span><span class="sxs-lookup"><span data-stu-id="090a0-114">Use cash discount</span></span> | <span data-ttu-id="090a0-115">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="090a0-115">Voucher</span></span>   | <span data-ttu-id="090a0-116">Rekening</span><span class="sxs-lookup"><span data-stu-id="090a0-116">Account</span></span> | <span data-ttu-id="090a0-117">Datum</span><span class="sxs-lookup"><span data-stu-id="090a0-117">Date</span></span>      | <span data-ttu-id="090a0-118">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="090a0-118">Due date</span></span>  | <span data-ttu-id="090a0-119">Factuur</span><span class="sxs-lookup"><span data-stu-id="090a0-119">Invoice</span></span> | <span data-ttu-id="090a0-120">Bedrag in transactievaluta</span><span class="sxs-lookup"><span data-stu-id="090a0-120">Amount in transaction currency</span></span> | <span data-ttu-id="090a0-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="090a0-121">Currency</span></span> | <span data-ttu-id="090a0-122">Bedrag om te vereffenen</span><span class="sxs-lookup"><span data-stu-id="090a0-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="090a0-123">Geselecteerd</span><span class="sxs-lookup"><span data-stu-id="090a0-123">Selected</span></span> | <span data-ttu-id="090a0-124">Normaal</span><span class="sxs-lookup"><span data-stu-id="090a0-124">Normal</span></span>            | <span data-ttu-id="090a0-125">Factuur-10040</span><span class="sxs-lookup"><span data-stu-id="090a0-125">Inv-10040</span></span> | <span data-ttu-id="090a0-126">3051</span><span class="sxs-lookup"><span data-stu-id="090a0-126">3051</span></span>    | <span data-ttu-id="090a0-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="090a0-127">6/29/2015</span></span> | <span data-ttu-id="090a0-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="090a0-128">7/29/2015</span></span> | <span data-ttu-id="090a0-129">10040</span><span class="sxs-lookup"><span data-stu-id="090a0-129">10040</span></span>   | <span data-ttu-id="090a0-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="090a0-130">1,000.00</span></span>                       | <span data-ttu-id="090a0-131">USD</span><span class="sxs-lookup"><span data-stu-id="090a0-131">USD</span></span>      | <span data-ttu-id="090a0-132">940,00</span><span class="sxs-lookup"><span data-stu-id="090a0-132">940.00</span></span>           |

<span data-ttu-id="090a0-133">Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="090a0-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>
|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="090a0-134">Datum van contantkorting</span><span class="sxs-lookup"><span data-stu-id="090a0-134">Cash discount date</span></span>           | <span data-ttu-id="090a0-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="090a0-135">7/12/2015</span></span> |
| <span data-ttu-id="090a0-136">Contantkortingsbedrag</span><span class="sxs-lookup"><span data-stu-id="090a0-136">Cash discount amount</span></span>         | <span data-ttu-id="090a0-137">60,00</span><span class="sxs-lookup"><span data-stu-id="090a0-137">60.00</span></span>     |
| <span data-ttu-id="090a0-138">Contantkorting gebruiken</span><span class="sxs-lookup"><span data-stu-id="090a0-138">Use cash discount</span></span>            | <span data-ttu-id="090a0-139">Normaal</span><span class="sxs-lookup"><span data-stu-id="090a0-139">Normal</span></span>    |
| <span data-ttu-id="090a0-140">Toegepaste contantkorting</span><span class="sxs-lookup"><span data-stu-id="090a0-140">Cash discount taken</span></span>          | <span data-ttu-id="090a0-141">0,00</span><span class="sxs-lookup"><span data-stu-id="090a0-141">0.00</span></span>      |
| <span data-ttu-id="090a0-142">Contantkortingsbedrag dat moet worden toegepast</span><span class="sxs-lookup"><span data-stu-id="090a0-142">Cash discount amount to take</span></span> | <span data-ttu-id="090a0-143">60,00</span><span class="sxs-lookup"><span data-stu-id="090a0-143">60.00</span></span>     |

<span data-ttu-id="090a0-144">Vervolgens boekt April het betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="090a0-144">April posts the payment journal.</span></span> <span data-ttu-id="090a0-145">De factuur is volledig vereffend met een betaling van 940,00 en een korting van 60,00.</span><span class="sxs-lookup"><span data-stu-id="090a0-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




