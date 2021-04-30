---
title: Boekingstypen voor lease
description: In dit onderwerp worden de boekingstypen beschreven die worden gebruikt voor activa-leasingtransacties.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881127"
---
# <a name="lease-posting-types"></a><span data-ttu-id="05c3c-103">Boekingstypen voor lease</span><span class="sxs-lookup"><span data-stu-id="05c3c-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05c3c-104">In dit onderwerp worden de boekingstypen beschreven die worden gebruikt voor activa-leasingtransacties.</span><span class="sxs-lookup"><span data-stu-id="05c3c-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="05c3c-105">Leaseactivum</span><span class="sxs-lookup"><span data-stu-id="05c3c-105">Lease asset</span></span>

<span data-ttu-id="05c3c-106">De rekening is gekoppeld aan het RoU-activum (activum met gebruiksrecht).</span><span class="sxs-lookup"><span data-stu-id="05c3c-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="05c3c-107">Deze rekening wordt gedebiteerd wanneer een lease in eerste instantie wordt toegerekend onder de nieuwe boekhoudstandaarden voor leases, Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="05c3c-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="05c3c-108">Voor een gewijzigde lease kan deze rekening worden gedebiteerd of gecrediteerd, afhankelijk van het feit of de leaseverplichtingen door de wijziging worden verhoogd of verlaagd.</span><span class="sxs-lookup"><span data-stu-id="05c3c-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="05c3c-109">**Voorbeeldjournaalposten:** eerste toerekening</span><span class="sxs-lookup"><span data-stu-id="05c3c-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="05c3c-110">**Debet:** leaseactiva XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="05c3c-111">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="05c3c-112">Leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="05c3c-112">Lease liability</span></span>

<span data-ttu-id="05c3c-113">De rekening is gekoppeld aan de leaseverplichtingen die zich voordoen wanneer betalingen worden verdisconteerd onder de nieuwe IFRS 16- en ASC 842-standaarden.</span><span class="sxs-lookup"><span data-stu-id="05c3c-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="05c3c-114">Deze rekening wordt gecrediteerd wanneer een lease in eerste instantie wordt toegerekend onder de nieuwe standaarden.</span><span class="sxs-lookup"><span data-stu-id="05c3c-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="05c3c-115">Deze wordt gedebiteerd voor leasebetalingen en gecrediteerd voor rentetoerekeningen.</span><span class="sxs-lookup"><span data-stu-id="05c3c-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="05c3c-116">**Voorbeeldjournaalposten:** eerste toerekening</span><span class="sxs-lookup"><span data-stu-id="05c3c-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="05c3c-117">**Debet:** leaseactiva XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="05c3c-118">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="05c3c-119">**Voorbeeldjournaalposten:** rentetoerekening</span><span class="sxs-lookup"><span data-stu-id="05c3c-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="05c3c-120">**Debet:** rentelasten XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="05c3c-121">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="05c3c-122">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="05c3c-123">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-124">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="05c3c-125">Kortlopende leaseverplichtingen</span><span class="sxs-lookup"><span data-stu-id="05c3c-125">Short-term lease liability</span></span>

<span data-ttu-id="05c3c-126">De rekening is gekoppeld aan de kortlopende leaseverplichtingen wanneer de herclassificatiejournaalpost voor de kortlopende leaseverplichtingen wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="05c3c-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="05c3c-127">Deze rekening wordt gecrediteerd voor de kortlopende verplichtingen van de aflossingsplanning op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="05c3c-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="05c3c-128">Hetzelfde bedrag wordt echter op de eerste dag van de volgende maand gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="05c3c-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="05c3c-129">**Voorbeeldjournaalposten:** herclassificatie kortlopende leaseverplichtingen</span><span class="sxs-lookup"><span data-stu-id="05c3c-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="05c3c-130">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-131">**Credit:** kortlopende leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-132">**Debet:** kortlopende leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-133">**Credit:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="05c3c-134">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="05c3c-134">Depreciation expense</span></span>

<span data-ttu-id="05c3c-135">De rekening is gekoppeld aan de kosten die zijn gerelateerd aan de afschrijving van het RoU-activum onder IFRS 16, ASC 842 en financiële leases overeenkomstig IAS 17 en ASC 840.</span><span class="sxs-lookup"><span data-stu-id="05c3c-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="05c3c-136">Deze rekening wordt gedebiteerd wanneer een RoU-activum elke maand wordt afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="05c3c-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="05c3c-137">**Voorbeeldjournaalposten:** afschrijvingstoerekening</span><span class="sxs-lookup"><span data-stu-id="05c3c-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="05c3c-138">**Debet:** afschrijvingskosten XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="05c3c-139">**Credit:** samengevoegde afschrijving XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="05c3c-140">Winst/verlies bij wijziging van lease</span><span class="sxs-lookup"><span data-stu-id="05c3c-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="05c3c-141">De rekening is gekoppeld aan winsten of verliezen die voortvloeien uit leasewijzigingen.</span><span class="sxs-lookup"><span data-stu-id="05c3c-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="05c3c-142">Er kan een winst ontstaan tijdens een leasewijziging als de wijziging de leaseverplichtingen vermindert met een bedrag dat hoger is dan de boekwaarde van het RoU-activum.</span><span class="sxs-lookup"><span data-stu-id="05c3c-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="05c3c-143">Een lease heeft bijvoorbeeld een actuele boekwaarde van de leaseverplichtingen van $ 150.000 en een boekwaarde van het RoU-activum van $ 100.000.</span><span class="sxs-lookup"><span data-stu-id="05c3c-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="05c3c-144">De lease wordt gewijzigd en deze wijziging produceert een nieuwe huidige waarde van de toekomstige minimale leasebetalingen (PVFMLP) van $ 40.000.</span><span class="sxs-lookup"><span data-stu-id="05c3c-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="05c3c-145">Daarom worden de leaseverplichtingen gedebiteerd met $ 110.000 ($ 150.000 – $ 40.000).</span><span class="sxs-lookup"><span data-stu-id="05c3c-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="05c3c-146">Omdat het RoU-activum slechts $ 100.000 is, zal de verlaging van $ 110.000 het activum voorbij 0 (nul) verlagen.</span><span class="sxs-lookup"><span data-stu-id="05c3c-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="05c3c-147">Daarom wordt in de boekhoudingsrichtlijnen aangegeven dat het restant moet worden geboekt op een winstrekening.</span><span class="sxs-lookup"><span data-stu-id="05c3c-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="05c3c-148">In dit geval is de definitieve journaalpost een debet voor de leaseverplichtingen voor $ 110.000, een credit voor het leaseactivum voor $ 100.000 en een credit voor de winstrekening voor $ 10.000.</span><span class="sxs-lookup"><span data-stu-id="05c3c-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="05c3c-149">**Voorbeeldjournaalposten:** leasewijziging</span><span class="sxs-lookup"><span data-stu-id="05c3c-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="05c3c-150">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-151">**Credit:** leaseactivum XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="05c3c-152">**Credit:** winst XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="05c3c-153">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="05c3c-153">Accumulated depreciation</span></span>

<span data-ttu-id="05c3c-154">De rekening is gekoppeld aan de contra-activumrekening van het RoU-activum.</span><span class="sxs-lookup"><span data-stu-id="05c3c-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="05c3c-155">Deze rekening wordt gecrediteerd wanneer afschrijvingskosten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="05c3c-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="05c3c-156">**Voorbeeldjournaalposten:** afschrijvingstoerekening</span><span class="sxs-lookup"><span data-stu-id="05c3c-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="05c3c-157">**Debet:** afschrijvingskosten XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="05c3c-158">**Credit:** samengevoegde afschrijving XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="05c3c-159">Variabele betaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-159">Variable payment</span></span>

<span data-ttu-id="05c3c-160">De rekening is gekoppeld aan variabele leasebetalingen die worden geproduceerd door een herwaardering van de index onder ASC 842, ASC 840 en IAS 17 leases.</span><span class="sxs-lookup"><span data-stu-id="05c3c-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="05c3c-161">In het leasebetalingsschema worden variabele betalingen opgenomen in de kolom **Variabele betaling**.</span><span class="sxs-lookup"><span data-stu-id="05c3c-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="05c3c-162">Deze rekening wordt gedebiteerd wanneer er een factuur wordt gemaakt op basis van een betalingsschemaregel die een variabele betaling bevat.</span><span class="sxs-lookup"><span data-stu-id="05c3c-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="05c3c-163">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="05c3c-164">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-165">**Debet:** variabele betaling XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="05c3c-166">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="05c3c-167">Activum uitgestelde gebruiksvergoeding (verplichtingen)</span><span class="sxs-lookup"><span data-stu-id="05c3c-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="05c3c-168">De rekening is gekoppeld aan het activum uitgestelde gebruiksvergoeding of de verplichting die wordt geproduceerd door een lease behandeling uitgestelde gebruiksvergoeding.</span><span class="sxs-lookup"><span data-stu-id="05c3c-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="05c3c-169">Deze rekening wordt gedebiteerd wanneer een factuur wordt geboekt voor een lease behandeling uitgestelde gebruiksvergoeding, als het bedrag van de leasebetaling hoger is dan de lineaire gebruiksvergoeding van de periode.</span><span class="sxs-lookup"><span data-stu-id="05c3c-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="05c3c-170">Het wordt gecrediteerd als de leasebetaling kleiner is dan de lineaire gebruiksvergoeding van de periode.</span><span class="sxs-lookup"><span data-stu-id="05c3c-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="05c3c-171">**Voorbeeldjournaalposten:** leasebetaling (lease behandeling uitgestelde gebruiksvergoeding)</span><span class="sxs-lookup"><span data-stu-id="05c3c-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="05c3c-172">**Debet:** leasekosten XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="05c3c-173">**Credit:** verplichtingen uitgestelde gebruiksvergoeding XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="05c3c-174">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="05c3c-175">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="05c3c-175">Lease expense</span></span>

<span data-ttu-id="05c3c-176">De rekening is gekoppeld aan de leasekosten als de lease wordt geclassificeerd als een lease behandeling uitgestelde gebruiksvergoeding.</span><span class="sxs-lookup"><span data-stu-id="05c3c-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="05c3c-177">Deze rekening wordt gedebiteerd wanneer een factuur wordt geboekt voor een lease behandeling uitgestelde gebruiksvergoeding.</span><span class="sxs-lookup"><span data-stu-id="05c3c-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="05c3c-178">**Voorbeeldjournaalposten:** leasebetaling (lease behandeling uitgestelde gebruiksvergoeding)</span><span class="sxs-lookup"><span data-stu-id="05c3c-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="05c3c-179">**Debet:** leasekosten XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="05c3c-180">**Credit:** verplichtingen uitgestelde gebruiksvergoeding XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="05c3c-181">**Credit:** te betalen leverancier/leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="05c3c-182">Waardeverminderingskosten</span><span class="sxs-lookup"><span data-stu-id="05c3c-182">Impairment expense</span></span>

<span data-ttu-id="05c3c-183">De rekening wordt tegen geboekt wanneer een lease een waardevermindering heeft ondergaan.</span><span class="sxs-lookup"><span data-stu-id="05c3c-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="05c3c-184">Deze rekening wordt gedebiteerd, terwijl de RoU-activumrekening rechtstreeks wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="05c3c-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="05c3c-185">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="05c3c-186">**Debet:** kosten waardevermindering XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="05c3c-187">**Credit:** RoU-activum XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="05c3c-188">Leasebetaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-188">Lease payment</span></span>

<span data-ttu-id="05c3c-189">De rekening wordt tegengeboekt als de parameter **Betaling aan leverancier** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="05c3c-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="05c3c-190">Deze rekening wordt gecrediteerd in plaats van de te betalen leverancier als de parameter is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="05c3c-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="05c3c-191">**Voorbeeldjournaalposten:** leasebetaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="05c3c-192">**Debet:** leaseverplichtingen XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="05c3c-193">**Credit:** leasebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="05c3c-194">Boekingen onkostentypen</span><span class="sxs-lookup"><span data-stu-id="05c3c-194">Expense type postings</span></span>

<span data-ttu-id="05c3c-195">De rekening die is geselecteerd voor elk onkostentype wordt gedebiteerd wanneer er een betaling voor dat onkostentype wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="05c3c-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="05c3c-196">De rekening die is opgegeven voor het onkostentype **Verzekering** bijvoorbeeld wordt gedebiteerd wanneer er een factuur- of betalingsjournaalpost wordt gemaakt van het schema administratieve kosten voor verzekeringskosten.</span><span class="sxs-lookup"><span data-stu-id="05c3c-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="05c3c-197">**Voorbeeldjournaalposten:** verzekeringsbetaling</span><span class="sxs-lookup"><span data-stu-id="05c3c-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="05c3c-198">**Debet:** rekening onkostentype verzekering XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="05c3c-199">**Credit:** tegenrekening XXX</span><span class="sxs-lookup"><span data-stu-id="05c3c-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="05c3c-200">De tegenrekening wordt geselecteerd op het leaseniveau op de regels voor het betalingsschema administratieve kosten.</span><span class="sxs-lookup"><span data-stu-id="05c3c-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="05c3c-201">Deze tegenrekening kan aan de leverancier of aan een grootboekrekening zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="05c3c-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
