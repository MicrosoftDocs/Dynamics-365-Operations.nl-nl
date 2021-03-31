---
title: Boekingstypen voor lease
description: In dit onderwerp worden de boekingstypen beschreven die worden gebruikt voor activa-leasingtransacties.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b7d8c545c1addaa570d54855bbad6c576783007
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229497"
---
# <a name="lease-posting-types"></a><span data-ttu-id="f350d-103">Boekingstypen voor lease</span><span class="sxs-lookup"><span data-stu-id="f350d-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f350d-104">In dit onderwerp worden de boekingstypen beschreven die worden gebruikt voor activa-leasingtransacties.</span><span class="sxs-lookup"><span data-stu-id="f350d-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="f350d-105">Leaseactivum</span><span class="sxs-lookup"><span data-stu-id="f350d-105">Lease asset</span></span>

<span data-ttu-id="f350d-106">De rekening is gekoppeld aan het RoU-activum (activum met gebruiksrecht).</span><span class="sxs-lookup"><span data-stu-id="f350d-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="f350d-107">Deze rekening wordt gedebiteerd wanneer een lease in eerste instantie wordt toegerekend onder de nieuwe boekhoudstandaarden voor leases, Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="f350d-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="f350d-108">Voor een gewijzigde lease kan deze rekening worden gedebiteerd of gecrediteerd, afhankelijk van het feit of de leaseverplichtingen door de wijziging worden verhoogd of verlaagd.</span><span class="sxs-lookup"><span data-stu-id="f350d-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="f350d-109">**Voorbeeldjournaalposten:** eerste toerekening</span><span class="sxs-lookup"><span data-stu-id="f350d-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="f350d-110">**Debet:** leaseactiva XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f350d-111">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="f350d-112">Leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="f350d-112">Lease liability</span></span>

<span data-ttu-id="f350d-113">De rekening is gekoppeld aan de leaseverplichtingen die zich voordoen wanneer betalingen worden verdisconteerd onder de nieuwe IFRS 16- en ASC 842-standaarden.</span><span class="sxs-lookup"><span data-stu-id="f350d-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="f350d-114">Deze rekening wordt gecrediteerd wanneer een lease in eerste instantie wordt toegerekend onder de nieuwe standaarden.</span><span class="sxs-lookup"><span data-stu-id="f350d-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="f350d-115">Deze wordt gedebiteerd voor leasebetalingen en gecrediteerd voor rentetoerekeningen.</span><span class="sxs-lookup"><span data-stu-id="f350d-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="f350d-116">**Voorbeeldjournaalposten:** eerste toerekening</span><span class="sxs-lookup"><span data-stu-id="f350d-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="f350d-117">**Debet:** leaseactiva XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f350d-118">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="f350d-119">**Voorbeeldjournaalposten:** rentetoerekening</span><span class="sxs-lookup"><span data-stu-id="f350d-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="f350d-120">**Debet:** rentelasten XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="f350d-121">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="f350d-122">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="f350d-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f350d-123">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f350d-124">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="f350d-125">Kortlopende leaseverplichtingen</span><span class="sxs-lookup"><span data-stu-id="f350d-125">Short-term lease liability</span></span>

<span data-ttu-id="f350d-126">De rekening is gekoppeld aan de kortlopende leaseverplichtingen wanneer de herclassificatiejournaalpost voor de kortlopende leaseverplichtingen wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="f350d-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="f350d-127">Deze rekening wordt gecrediteerd voor de kortlopende verplichtingen van de aflossingsplanning op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="f350d-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="f350d-128">Hetzelfde bedrag wordt echter op de eerste dag van de volgende maand gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="f350d-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="f350d-129">**Voorbeeldjournaalposten:** herclassificatie kortlopende leaseverplichtingen</span><span class="sxs-lookup"><span data-stu-id="f350d-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="f350d-130">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f350d-131">**Credit:** kortlopende leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="f350d-132">**Debet:** kortlopende leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="f350d-133">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="f350d-134">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="f350d-134">Depreciation expense</span></span>

<span data-ttu-id="f350d-135">De rekening is gekoppeld aan de kosten die zijn gerelateerd aan de afschrijving van het RoU-activum onder IFRS 16, ASC 842 en financiële leases overeenkomstig IAS 17 en ASC 840.</span><span class="sxs-lookup"><span data-stu-id="f350d-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="f350d-136">Deze rekening wordt gedebiteerd wanneer een RoU-activum elke maand wordt afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="f350d-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="f350d-137">**Voorbeeldjournaalposten:** afschrijvingstoerekening</span><span class="sxs-lookup"><span data-stu-id="f350d-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="f350d-138">**Debet:** afschrijvingskosten XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="f350d-139">**Credit:** samengevoegde afschrijving XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="f350d-140">Winst/verlies bij wijziging van lease</span><span class="sxs-lookup"><span data-stu-id="f350d-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="f350d-141">De rekening is gekoppeld aan winsten of verliezen die voortvloeien uit leasewijzigingen.</span><span class="sxs-lookup"><span data-stu-id="f350d-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="f350d-142">Er kan een winst ontstaan tijdens een leasewijziging als de wijziging de leaseverplichtingen vermindert met een bedrag dat hoger is dan de boekwaarde van het RoU-activum.</span><span class="sxs-lookup"><span data-stu-id="f350d-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="f350d-143">Een lease heeft bijvoorbeeld een actuele boekwaarde van de leaseverplichtingen van $ 150.000 en een boekwaarde van het RoU-activum van $ 100.000.</span><span class="sxs-lookup"><span data-stu-id="f350d-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="f350d-144">De lease wordt gewijzigd en deze wijziging produceert een nieuwe huidige waarde van de toekomstige minimale leasebetalingen (PVFMLP) van $ 40.000.</span><span class="sxs-lookup"><span data-stu-id="f350d-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="f350d-145">Daarom worden de leaseverplichtingen gedebiteerd met $ 110.000 ($ 150.000 – $ 40.000).</span><span class="sxs-lookup"><span data-stu-id="f350d-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="f350d-146">Omdat het RoU-activum slechts $ 100.000 is, zal de verlaging van $ 110.000 het activum voorbij 0 (nul) verlagen.</span><span class="sxs-lookup"><span data-stu-id="f350d-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="f350d-147">Daarom wordt in de boekhoudingsrichtlijnen aangegeven dat het restant moet worden geboekt op een winstrekening.</span><span class="sxs-lookup"><span data-stu-id="f350d-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="f350d-148">In dit geval is de definitieve journaalpost een debet voor de leaseverplichtingen voor $ 110.000, een credit voor het leaseactivum voor $ 100.000 en een credit voor de winstrekening voor $ 10.000.</span><span class="sxs-lookup"><span data-stu-id="f350d-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="f350d-149">**Voorbeeldjournaalposten:** leasewijziging</span><span class="sxs-lookup"><span data-stu-id="f350d-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="f350d-150">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f350d-151">**Credit:** leaseactivum XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="f350d-152">**Credit:** winst XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="f350d-153">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="f350d-153">Accumulated depreciation</span></span>

<span data-ttu-id="f350d-154">De rekening is gekoppeld aan de contra-activumrekening van het RoU-activum.</span><span class="sxs-lookup"><span data-stu-id="f350d-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="f350d-155">Deze rekening wordt gecrediteerd wanneer afschrijvingskosten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="f350d-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="f350d-156">**Voorbeeldjournaalposten:** afschrijvingstoerekening</span><span class="sxs-lookup"><span data-stu-id="f350d-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="f350d-157">**Debet:** afschrijvingskosten XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="f350d-158">**Credit:** samengevoegde afschrijving XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="f350d-159">Ingehouden winst</span><span class="sxs-lookup"><span data-stu-id="f350d-159">Retained earnings</span></span>

<span data-ttu-id="f350d-160">De rekening is gekoppeld aan ingehouden inkomsten.</span><span class="sxs-lookup"><span data-stu-id="f350d-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="f350d-161">Deze rekening kan worden gedebiteerd of gecrediteerd in een journaalpost transitiecorrectie met behulp van de volledige retrospectieve methode of de cumulatieve achterstallige optie A-methode.</span><span class="sxs-lookup"><span data-stu-id="f350d-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="f350d-162">Het verschil tussen het oorspronkelijke RoU-activum en de leaseverplichtingen wordt geboekt op ingehouden winsten.</span><span class="sxs-lookup"><span data-stu-id="f350d-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="f350d-163">In zeldzame gevallen kunnen de ingehouden winsten ook worden beïnvloed tijdens het wijzigen van de lease, als de classificatie van een lease wordt gewijzigd van financieel naar operationeel om het RoU-activum omhoog of omlaag te schrijven, zodat het gelijk is aan de leaseverplichtingen.</span><span class="sxs-lookup"><span data-stu-id="f350d-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="f350d-164">**Voorbeeldjournaalposten:** transitiecorrectie (volledige retrospectieve methode of de cumulatieve achterstallige optie A-methode)</span><span class="sxs-lookup"><span data-stu-id="f350d-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="f350d-165">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f350d-166">**Credit:** leaseactivum XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f350d-167">**Credit:** ingehouden inkomsten XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="f350d-168">Variabele betaling</span><span class="sxs-lookup"><span data-stu-id="f350d-168">Variable payment</span></span>

<span data-ttu-id="f350d-169">De rekening is gekoppeld aan variabele leasebetalingen die worden geproduceerd door een herwaardering van de index onder ASC 842, ASC 840 en IAS 17 leases.</span><span class="sxs-lookup"><span data-stu-id="f350d-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="f350d-170">In het leasebetalingsschema worden variabele betalingen opgenomen in de kolom **Variabele betaling**.</span><span class="sxs-lookup"><span data-stu-id="f350d-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="f350d-171">Deze rekening wordt gedebiteerd wanneer er een factuur wordt gemaakt op basis van een betalingsschemaregel die een variabele betaling bevat.</span><span class="sxs-lookup"><span data-stu-id="f350d-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="f350d-172">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="f350d-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f350d-173">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f350d-174">**Debet:** variabele betaling XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="f350d-175">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="f350d-176">Activum uitgestelde gebruiksvergoeding (verplichtingen)</span><span class="sxs-lookup"><span data-stu-id="f350d-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="f350d-177">De rekening is gekoppeld aan het activum uitgestelde gebruiksvergoeding of de verplichting die wordt geproduceerd door een lease behandeling uitgestelde gebruiksvergoeding.</span><span class="sxs-lookup"><span data-stu-id="f350d-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="f350d-178">Deze rekening wordt gedebiteerd wanneer een factuur wordt geboekt voor een lease behandeling uitgestelde gebruiksvergoeding, als het bedrag van de leasebetaling hoger is dan de lineaire gebruiksvergoeding van de periode.</span><span class="sxs-lookup"><span data-stu-id="f350d-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="f350d-179">Het wordt gecrediteerd als de leasebetaling kleiner is dan de lineaire gebruiksvergoeding van de periode.</span><span class="sxs-lookup"><span data-stu-id="f350d-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="f350d-180">**Voorbeeldjournaalposten:** leasebetaling (lease behandeling uitgestelde gebruiksvergoeding)</span><span class="sxs-lookup"><span data-stu-id="f350d-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="f350d-181">**Debet:** leasekosten XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="f350d-182">**Credit:** verplichtingen uitgestelde gebruiksvergoeding XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="f350d-183">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="f350d-184">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="f350d-184">Lease expense</span></span>

<span data-ttu-id="f350d-185">De rekening is gekoppeld aan de leasekosten als de lease wordt geclassificeerd als een lease behandeling uitgestelde gebruiksvergoeding.</span><span class="sxs-lookup"><span data-stu-id="f350d-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="f350d-186">Deze rekening wordt gedebiteerd wanneer een factuur wordt geboekt voor een lease behandeling uitgestelde gebruiksvergoeding.</span><span class="sxs-lookup"><span data-stu-id="f350d-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="f350d-187">**Voorbeeldjournaalposten:** leasebetaling (lease behandeling uitgestelde gebruiksvergoeding)</span><span class="sxs-lookup"><span data-stu-id="f350d-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="f350d-188">**Debet:** leasekosten XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="f350d-189">**Credit:** verplichtingen uitgestelde gebruiksvergoeding XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="f350d-190">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="f350d-191">Waardeverminderingskosten</span><span class="sxs-lookup"><span data-stu-id="f350d-191">Impairment expense</span></span>

<span data-ttu-id="f350d-192">De rekening wordt tegen geboekt wanneer een lease een waardevermindering heeft ondergaan.</span><span class="sxs-lookup"><span data-stu-id="f350d-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="f350d-193">Deze rekening wordt gedebiteerd, terwijl de RoU-activumrekening rechtstreeks wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="f350d-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="f350d-194">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="f350d-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f350d-195">**Debet:** kosten waardevermindering XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="f350d-196">**Credit:** RoU-activum XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="f350d-197">Leasebetaling</span><span class="sxs-lookup"><span data-stu-id="f350d-197">Lease payment</span></span>

<span data-ttu-id="f350d-198">De rekening wordt tegengeboekt als de parameter **Betaling aan leverancier** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f350d-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="f350d-199">Deze rekening wordt gecrediteerd in plaats van de te betalen leverancier als de parameter is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f350d-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="f350d-200">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="f350d-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f350d-201">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f350d-202">**Credit:** leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="f350d-203">Boekingen onkostentypen</span><span class="sxs-lookup"><span data-stu-id="f350d-203">Expense type postings</span></span>

<span data-ttu-id="f350d-204">De rekening die is geselecteerd voor elk onkostentype wordt gedebiteerd wanneer er een betaling voor dat onkostentype wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="f350d-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="f350d-205">De rekening die is opgegeven voor het onkostentype **Verzekering** bijvoorbeeld wordt gedebiteerd wanneer er een factuur- of betalingsjournaalpost wordt gemaakt van het schema administratieve kosten voor verzekeringskosten.</span><span class="sxs-lookup"><span data-stu-id="f350d-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="f350d-206">**Voorbeeldjournaalposten:** verzekeringsbetaling</span><span class="sxs-lookup"><span data-stu-id="f350d-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="f350d-207">**Debet:** rekening onkostentype verzekering XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="f350d-208">**Credit:** tegenrekening XXX</span><span class="sxs-lookup"><span data-stu-id="f350d-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="f350d-209">De tegenrekening wordt geselecteerd op het leaseniveau op de regels voor het betalingsschema administratieve kosten.</span><span class="sxs-lookup"><span data-stu-id="f350d-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="f350d-210">Deze tegenrekening kan aan de leverancier of aan een grootboekrekening zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f350d-210">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]