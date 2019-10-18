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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186320"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="82354-103">Btw-betalingen en afrondingsregels</span><span class="sxs-lookup"><span data-stu-id="82354-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82354-104">In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="82354-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="82354-105">Periodiek moet btw worden aangegeven en betaald aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="82354-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="82354-106">Dit kan worden uitgevoerd door het proces Btw vereffenen en boeken op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="82354-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="82354-107">Btw voor een periode wordt vereffend voor de btw-rekeningen en het btw-saldo wordt naar de rekening Btw-vereffening geboekt.</span><span class="sxs-lookup"><span data-stu-id="82354-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="82354-108">Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="82354-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="82354-109">Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.</span><span class="sxs-lookup"><span data-stu-id="82354-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="82354-110">Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.</span><span class="sxs-lookup"><span data-stu-id="82354-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="82354-111">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="82354-111">Examples</span></span>

<span data-ttu-id="82354-112">De totale btw voor een periode toont een creditsaldo van -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="82354-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="82354-113">De rechtspersoon inde meer btw dan dat betaald werd.</span><span class="sxs-lookup"><span data-stu-id="82354-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="82354-114">Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst.</span><span class="sxs-lookup"><span data-stu-id="82354-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="82354-115">De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00.</span><span class="sxs-lookup"><span data-stu-id="82354-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="82354-116">De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="82354-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="82354-117">Klik op Btw &gt; Indirecte belastingen &gt; Btw &gt; Btw-diensten</span><span class="sxs-lookup"><span data-stu-id="82354-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="82354-118">Selecteer op het sneltabblad Algemeen in het veld Afrondingstype de optie Normaal.</span><span class="sxs-lookup"><span data-stu-id="82354-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="82354-119">Typ 1,00 in het veld Afronden.</span><span class="sxs-lookup"><span data-stu-id="82354-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="82354-120">Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="82354-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="82354-121">(Klik op Btw &gt; Aangiften &gt; Btw &gt; Btw vereffenen en boeken.)</span><span class="sxs-lookup"><span data-stu-id="82354-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="82354-122">Op de btw-vereffeningsrekening is het bedrag van uw btw-belastingschuld van 98.765,43 afgerond naar 98.765.</span><span class="sxs-lookup"><span data-stu-id="82354-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="82354-123">In de volgende tabel ziet u hoe een bedrag van 98.765,43 wordt afgerond met behulp van elke afrondingsmethode die beschikbaar is in het veld Afrondingstype op de pagina Btw-dienst.</span><span class="sxs-lookup"><span data-stu-id="82354-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="82354-124">Optie Afrondingstype</span><span class="sxs-lookup"><span data-stu-id="82354-124">Rounding form option</span></span>                | <span data-ttu-id="82354-125">Afrondingswaarde = 0,01</span><span class="sxs-lookup"><span data-stu-id="82354-125">Round-off value = 0.01</span></span> | <span data-ttu-id="82354-126">Afrondingswaarde = 0,10</span><span class="sxs-lookup"><span data-stu-id="82354-126">Round-off value = 0.10</span></span> | <span data-ttu-id="82354-127">Afrondingswaarde = 1,00</span><span class="sxs-lookup"><span data-stu-id="82354-127">Round-off value = 1.00</span></span> | <span data-ttu-id="82354-128">Afrondingswaarde = 100,00</span><span class="sxs-lookup"><span data-stu-id="82354-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="82354-129">Normaal</span><span class="sxs-lookup"><span data-stu-id="82354-129">Normal</span></span>                              | <span data-ttu-id="82354-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="82354-130">98,765.43</span></span>              | <span data-ttu-id="82354-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="82354-131">98,765.40</span></span>              | <span data-ttu-id="82354-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="82354-132">98,765.00</span></span>              | <span data-ttu-id="82354-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="82354-133">98,800.00</span></span>                |
| <span data-ttu-id="82354-134">Naar beneden afronden</span><span class="sxs-lookup"><span data-stu-id="82354-134">Downward</span></span>                            | <span data-ttu-id="82354-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="82354-135">98,765.43</span></span>              | <span data-ttu-id="82354-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="82354-136">98,765.40</span></span>              | <span data-ttu-id="82354-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="82354-137">98,765.00</span></span>              | <span data-ttu-id="82354-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="82354-138">98,700.00</span></span>                |
| <span data-ttu-id="82354-139">Naar boven afronden</span><span class="sxs-lookup"><span data-stu-id="82354-139">Rounding-up</span></span>                         | <span data-ttu-id="82354-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="82354-140">98,765.43</span></span>              | <span data-ttu-id="82354-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="82354-141">98,765.50</span></span>              | <span data-ttu-id="82354-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="82354-142">98,766.00</span></span>              | <span data-ttu-id="82354-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="82354-143">98,800.00</span></span>                |
| <span data-ttu-id="82354-144">Eigen voordeel, voor een creditsaldo</span><span class="sxs-lookup"><span data-stu-id="82354-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="82354-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="82354-145">98,765.43</span></span>              | <span data-ttu-id="82354-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="82354-146">98,765.40</span></span>              | <span data-ttu-id="82354-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="82354-147">98,765.00</span></span>              | <span data-ttu-id="82354-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="82354-148">98,700.00</span></span>                |
| <span data-ttu-id="82354-149">Eigen voordeel, voor een debitsaldo</span><span class="sxs-lookup"><span data-stu-id="82354-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="82354-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="82354-150">98,765.43</span></span>              | <span data-ttu-id="82354-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="82354-151">98,765.50</span></span>              | <span data-ttu-id="82354-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="82354-152">98,766.00</span></span>              | <span data-ttu-id="82354-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="82354-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="82354-154">Helemaal geen afronding, omdat de afronding 0,00 is</span><span class="sxs-lookup"><span data-stu-id="82354-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="82354-155">afronding (1,0151, 0,00) = 1,0151 afronding (1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="82354-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="82354-156">Normale afronding en afrondingsprecisie is 0,01</span><span class="sxs-lookup"><span data-stu-id="82354-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="82354-157">Afronding</span><span class="sxs-lookup"><span data-stu-id="82354-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="82354-158">Berekeningsproces</span><span class="sxs-lookup"><span data-stu-id="82354-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="82354-159">afronding (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="82354-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="82354-160">afronding (1,015 / 0,01, 0) = afronding (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="82354-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="82354-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="82354-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="82354-162">afronding (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="82354-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="82354-163">afronding (1,014 / 0,01, 0) = afronding (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="82354-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="82354-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="82354-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="82354-165">afronding (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="82354-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="82354-166">afronding (1,011 / 0,02, 0) = afronding (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="82354-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="82354-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="82354-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="82354-168">afronding (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="82354-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="82354-169">afronding (1,009 / 0,02, 0) = afronding (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="82354-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="82354-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="82354-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="82354-171">Als u Eigen voordeel selecteert, is de afronding altijd in het voordeel van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="82354-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="82354-172">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="82354-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="82354-173">Btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="82354-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="82354-174">Een btw-betaling maken</span><span class="sxs-lookup"><span data-stu-id="82354-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="82354-175">Verkooptransacties maken in documenten</span><span class="sxs-lookup"><span data-stu-id="82354-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="82354-176">Geboekte btw-transacties weergeven</span><span class="sxs-lookup"><span data-stu-id="82354-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="82354-177">Afrondingsfunctie</span><span class="sxs-lookup"><span data-stu-id="82354-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


