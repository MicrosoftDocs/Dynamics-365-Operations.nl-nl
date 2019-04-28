---
title: Btw-betalingen en afrondingsregels
description: In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/14/2019
ms.locfileid: "842433"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="58ddc-103">Btw-betalingen en afrondingsregels</span><span class="sxs-lookup"><span data-stu-id="58ddc-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58ddc-104">In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="58ddc-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="58ddc-105">Periodiek moet btw worden aangegeven en betaald aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="58ddc-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="58ddc-106">Dit kan worden uitgevoerd door het proces Btw vereffenen en boeken op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="58ddc-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="58ddc-107">Btw voor een periode wordt vereffend voor de btw-rekeningen en het btw-saldo wordt naar de rekening Btw-vereffening geboekt.</span><span class="sxs-lookup"><span data-stu-id="58ddc-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="58ddc-108">Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="58ddc-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="58ddc-109">Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.</span><span class="sxs-lookup"><span data-stu-id="58ddc-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="58ddc-110">Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.</span><span class="sxs-lookup"><span data-stu-id="58ddc-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="58ddc-111">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="58ddc-111">Examples</span></span>

<span data-ttu-id="58ddc-112">De totale btw voor een periode toont een creditsaldo van -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="58ddc-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="58ddc-113">De rechtspersoon inde meer btw dan dat betaald werd.</span><span class="sxs-lookup"><span data-stu-id="58ddc-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="58ddc-114">Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst.</span><span class="sxs-lookup"><span data-stu-id="58ddc-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="58ddc-115">De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00.</span><span class="sxs-lookup"><span data-stu-id="58ddc-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="58ddc-116">De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="58ddc-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="58ddc-117">Klik op Btw &gt; Indirecte belastingen &gt; Btw &gt; Btw-diensten</span><span class="sxs-lookup"><span data-stu-id="58ddc-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="58ddc-118">Selecteer op het sneltabblad Algemeen in het veld Afrondingstype de optie Normaal.</span><span class="sxs-lookup"><span data-stu-id="58ddc-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="58ddc-119">Typ 1,00 in het veld Afronden.</span><span class="sxs-lookup"><span data-stu-id="58ddc-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="58ddc-120">Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="58ddc-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="58ddc-121">(Klik op Btw &gt; Aangiften &gt; Btw &gt; Btw vereffenen en boeken.)</span><span class="sxs-lookup"><span data-stu-id="58ddc-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="58ddc-122">Op de btw-vereffeningsrekening is het bedrag van uw btw-belastingschuld van 98.765,43 afgerond naar 98.765.</span><span class="sxs-lookup"><span data-stu-id="58ddc-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="58ddc-123">In de volgende tabel ziet u hoe een bedrag van 98.765,43 wordt afgerond met behulp van elke afrondingsmethode die beschikbaar is in het veld Afrondingstype op de pagina Btw-dienst.</span><span class="sxs-lookup"><span data-stu-id="58ddc-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="58ddc-124">Optie Afrondingstype</span><span class="sxs-lookup"><span data-stu-id="58ddc-124">Rounding form option</span></span>                | <span data-ttu-id="58ddc-125">Afrondingswaarde = 0,01</span><span class="sxs-lookup"><span data-stu-id="58ddc-125">Round-off value = 0.01</span></span> | <span data-ttu-id="58ddc-126">Afrondingswaarde = 0,10</span><span class="sxs-lookup"><span data-stu-id="58ddc-126">Round-off value = 0.10</span></span> | <span data-ttu-id="58ddc-127">Afrondingswaarde = 1,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-127">Round-off value = 1.00</span></span> | <span data-ttu-id="58ddc-128">Afrondingswaarde = 100,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="58ddc-129">Normaal</span><span class="sxs-lookup"><span data-stu-id="58ddc-129">Normal</span></span>                              | <span data-ttu-id="58ddc-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="58ddc-130">98,765.43</span></span>              | <span data-ttu-id="58ddc-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="58ddc-131">98,765.40</span></span>              | <span data-ttu-id="58ddc-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-132">98,765.00</span></span>              | <span data-ttu-id="58ddc-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-133">98,800.00</span></span>                |
| <span data-ttu-id="58ddc-134">Naar beneden afronden</span><span class="sxs-lookup"><span data-stu-id="58ddc-134">Downward</span></span>                            | <span data-ttu-id="58ddc-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="58ddc-135">98,765.43</span></span>              | <span data-ttu-id="58ddc-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="58ddc-136">98,765.40</span></span>              | <span data-ttu-id="58ddc-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-137">98,765.00</span></span>              | <span data-ttu-id="58ddc-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-138">98,700.00</span></span>                |
| <span data-ttu-id="58ddc-139">Naar boven afronden</span><span class="sxs-lookup"><span data-stu-id="58ddc-139">Rounding-up</span></span>                         | <span data-ttu-id="58ddc-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="58ddc-140">98,765.43</span></span>              | <span data-ttu-id="58ddc-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="58ddc-141">98,765.50</span></span>              | <span data-ttu-id="58ddc-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-142">98,766.00</span></span>              | <span data-ttu-id="58ddc-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-143">98,800.00</span></span>                |
| <span data-ttu-id="58ddc-144">Eigen voordeel, voor een creditsaldo</span><span class="sxs-lookup"><span data-stu-id="58ddc-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="58ddc-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="58ddc-145">98,765.43</span></span>              | <span data-ttu-id="58ddc-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="58ddc-146">98,765.40</span></span>              | <span data-ttu-id="58ddc-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-147">98,765.00</span></span>              | <span data-ttu-id="58ddc-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-148">98,700.00</span></span>                |
| <span data-ttu-id="58ddc-149">Eigen voordeel, voor een debitsaldo</span><span class="sxs-lookup"><span data-stu-id="58ddc-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="58ddc-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="58ddc-150">98,765.43</span></span>              | <span data-ttu-id="58ddc-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="58ddc-151">98,765.50</span></span>              | <span data-ttu-id="58ddc-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="58ddc-152">98,766.00</span></span>              | <span data-ttu-id="58ddc-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="58ddc-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="58ddc-154">Helemaal geen afronding, omdat de afronding 0,00 is</span><span class="sxs-lookup"><span data-stu-id="58ddc-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="58ddc-155">afronding (1,0151, 0,00) = 1,0151 afronding (1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="58ddc-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="58ddc-156">Normale afronding en afrondingsprecisie is 0,01</span><span class="sxs-lookup"><span data-stu-id="58ddc-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="58ddc-157">Afronding</span><span class="sxs-lookup"><span data-stu-id="58ddc-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="58ddc-158">Berekeningsproces</span><span class="sxs-lookup"><span data-stu-id="58ddc-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="58ddc-159">afronding (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="58ddc-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="58ddc-160">afronding (1,015 / 0,01, 0) = afronding (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="58ddc-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="58ddc-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="58ddc-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="58ddc-162">afronding (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="58ddc-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="58ddc-163">afronding (1,014 / 0,01, 0) = afronding (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="58ddc-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="58ddc-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="58ddc-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="58ddc-165">afronding (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="58ddc-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="58ddc-166">afronding (1,011 / 0,02, 0) = afronding (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="58ddc-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="58ddc-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="58ddc-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="58ddc-168">afronding (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="58ddc-169">afronding (1,009 / 0,02, 0) = afronding (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="58ddc-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="58ddc-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="58ddc-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="58ddc-171">Als u Eigen voordeel selecteert, is de afronding altijd in het voordeel van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="58ddc-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="58ddc-172">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="58ddc-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="58ddc-173">Btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="58ddc-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="58ddc-174">Een btw-betaling maken</span><span class="sxs-lookup"><span data-stu-id="58ddc-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="58ddc-175">Verkooptransacties maken in documenten</span><span class="sxs-lookup"><span data-stu-id="58ddc-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="58ddc-176">Geboekte btw-transacties weergeven</span><span class="sxs-lookup"><span data-stu-id="58ddc-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="58ddc-177">Afrondingsfunctie</span><span class="sxs-lookup"><span data-stu-id="58ddc-177">round Function</span></span>](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


