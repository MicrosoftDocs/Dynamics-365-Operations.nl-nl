---
title: Meer dan de berekende korting voor een leveranciersbetaling nemen
description: Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810241"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="741bb-104">Meer dan de berekende korting voor een leveranciersbetaling nemen</span><span class="sxs-lookup"><span data-stu-id="741bb-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="741bb-105">Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="741bb-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="741bb-106">Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.</span><span class="sxs-lookup"><span data-stu-id="741bb-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="741bb-107">Leverancier 3051 laat Fabrikam een contantkorting van 4 procent nemen als een factuur wordt betaald binnen zeven dagen.</span><span class="sxs-lookup"><span data-stu-id="741bb-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="741bb-108">Op 29 jnui voert April een factuur in voor 1000,00.</span><span class="sxs-lookup"><span data-stu-id="741bb-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="741bb-109">De leverancier geeft April een korting van 60,00 in plaats van de standaardkorting van 40,00 die beschikbaar is voor de factuur.</span><span class="sxs-lookup"><span data-stu-id="741bb-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="741bb-110">April registreert een eenmalige betaling door het Leveranciersbetalingsjournaal te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="741bb-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="741bb-111">Ze voert de leverancier voor de betaling in en opent vervolgens de pagina **Transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="741bb-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="741bb-112">Ze ziet de factuur en wijzigt de waarde in het veld **Contantkortingsbedrag** naar **60,00**.</span><span class="sxs-lookup"><span data-stu-id="741bb-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="741bb-113">Markeren</span><span class="sxs-lookup"><span data-stu-id="741bb-113">Mark</span></span>     | <span data-ttu-id="741bb-114">Contantkorting gebruiken</span><span class="sxs-lookup"><span data-stu-id="741bb-114">Use cash discount</span></span> | <span data-ttu-id="741bb-115">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="741bb-115">Voucher</span></span>   | <span data-ttu-id="741bb-116">Rekening</span><span class="sxs-lookup"><span data-stu-id="741bb-116">Account</span></span> | <span data-ttu-id="741bb-117">Datum</span><span class="sxs-lookup"><span data-stu-id="741bb-117">Date</span></span>      | <span data-ttu-id="741bb-118">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="741bb-118">Due date</span></span>  | <span data-ttu-id="741bb-119">Factuur</span><span class="sxs-lookup"><span data-stu-id="741bb-119">Invoice</span></span> | <span data-ttu-id="741bb-120">Bedrag in transactievaluta</span><span class="sxs-lookup"><span data-stu-id="741bb-120">Amount in transaction currency</span></span> | <span data-ttu-id="741bb-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="741bb-121">Currency</span></span> | <span data-ttu-id="741bb-122">Bedrag om te vereffenen</span><span class="sxs-lookup"><span data-stu-id="741bb-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="741bb-123">Geselecteerd</span><span class="sxs-lookup"><span data-stu-id="741bb-123">Selected</span></span> | <span data-ttu-id="741bb-124">Normaal</span><span class="sxs-lookup"><span data-stu-id="741bb-124">Normal</span></span>            | <span data-ttu-id="741bb-125">Factuur-10040</span><span class="sxs-lookup"><span data-stu-id="741bb-125">Inv-10040</span></span> | <span data-ttu-id="741bb-126">3051</span><span class="sxs-lookup"><span data-stu-id="741bb-126">3051</span></span>    | <span data-ttu-id="741bb-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="741bb-127">6/29/2015</span></span> | <span data-ttu-id="741bb-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="741bb-128">7/29/2015</span></span> | <span data-ttu-id="741bb-129">10040</span><span class="sxs-lookup"><span data-stu-id="741bb-129">10040</span></span>   | <span data-ttu-id="741bb-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="741bb-130">1,000.00</span></span>                       | <span data-ttu-id="741bb-131">USD</span><span class="sxs-lookup"><span data-stu-id="741bb-131">USD</span></span>      | <span data-ttu-id="741bb-132">940,00</span><span class="sxs-lookup"><span data-stu-id="741bb-132">940.00</span></span>           |

<span data-ttu-id="741bb-133">Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="741bb-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="741bb-134">Veld</span><span class="sxs-lookup"><span data-stu-id="741bb-134">Field</span></span>                        | <span data-ttu-id="741bb-135">Waarde</span><span class="sxs-lookup"><span data-stu-id="741bb-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="741bb-136">Datum voor contantkorting</span><span class="sxs-lookup"><span data-stu-id="741bb-136">Cash discount date</span></span>           | <span data-ttu-id="741bb-137">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="741bb-137">7/12/2015</span></span> |
| <span data-ttu-id="741bb-138">Contantkortingsbedrag</span><span class="sxs-lookup"><span data-stu-id="741bb-138">Cash discount amount</span></span>         | <span data-ttu-id="741bb-139">60.00</span><span class="sxs-lookup"><span data-stu-id="741bb-139">60.00</span></span>     |
| <span data-ttu-id="741bb-140">Contantkorting gebruiken</span><span class="sxs-lookup"><span data-stu-id="741bb-140">Use cash discount</span></span>            | <span data-ttu-id="741bb-141">Normaal</span><span class="sxs-lookup"><span data-stu-id="741bb-141">Normal</span></span>    |
| <span data-ttu-id="741bb-142">Toegepaste contantkorting</span><span class="sxs-lookup"><span data-stu-id="741bb-142">Cash discount taken</span></span>          | <span data-ttu-id="741bb-143">0,00</span><span class="sxs-lookup"><span data-stu-id="741bb-143">0.00</span></span>      |
| <span data-ttu-id="741bb-144">Contantkortingsbedrag dat moet worden toegepast</span><span class="sxs-lookup"><span data-stu-id="741bb-144">Cash discount amount to take</span></span> | <span data-ttu-id="741bb-145">60,00</span><span class="sxs-lookup"><span data-stu-id="741bb-145">60.00</span></span>     |

<span data-ttu-id="741bb-146">Vervolgens boekt April het betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="741bb-146">April posts the payment journal.</span></span> <span data-ttu-id="741bb-147">De factuur is volledig vereffend met een betaling van 940,00 en een korting van 60,00.</span><span class="sxs-lookup"><span data-stu-id="741bb-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]