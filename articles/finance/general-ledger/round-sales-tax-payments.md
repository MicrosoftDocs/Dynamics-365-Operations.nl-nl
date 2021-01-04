---
title: Btw-betalingen en afrondingsregels
description: In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
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
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998dbd01352d3fa5040187e81b564d14133464db
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4442132"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="dbf32-103">Btw-betalingen en afrondingsregels</span><span class="sxs-lookup"><span data-stu-id="dbf32-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbf32-104">In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="dbf32-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="dbf32-105">Periodiek moet btw worden aangegeven en betaald aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="dbf32-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="dbf32-106">Dit kan worden uitgevoerd door het proces Btw vereffenen en boeken op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="dbf32-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="dbf32-107">Btw voor een periode wordt vereffend voor de btw-rekeningen en het btw-saldo wordt naar de rekening Btw-vereffening geboekt.</span><span class="sxs-lookup"><span data-stu-id="dbf32-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="dbf32-108">Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="dbf32-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="dbf32-109">Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.</span><span class="sxs-lookup"><span data-stu-id="dbf32-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="dbf32-110">Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.</span><span class="sxs-lookup"><span data-stu-id="dbf32-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="dbf32-111">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="dbf32-111">Examples</span></span>

<span data-ttu-id="dbf32-112">De totale btw voor een periode toont een creditsaldo van -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="dbf32-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="dbf32-113">De rechtspersoon inde meer btw dan dat betaald werd.</span><span class="sxs-lookup"><span data-stu-id="dbf32-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="dbf32-114">Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst.</span><span class="sxs-lookup"><span data-stu-id="dbf32-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="dbf32-115">De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00.</span><span class="sxs-lookup"><span data-stu-id="dbf32-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="dbf32-116">De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="dbf32-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="dbf32-117">Klik op **Belasting** > **Indirecte belastingen** > **Btw** > **Btw-dienst**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="dbf32-118">Selecteer op het sneltabblad **Algemeen** in het veld **Afrondingstype** de optie **Normaal**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="dbf32-119">Typ 1,00 in het veld **Afronden**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="dbf32-120">Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina **Belasting** > **Aangiften** > **Btw** > **Btw vereffenen en boeken**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="dbf32-121">Op de btw-vereffeningsrekening ziet u dat het bedrag van uw btw-belastingschuld van **98.765,43** is afgerond naar **98.765**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="dbf32-122">In de volgende tabel ziet u hoe een bedrag van 98.765,43 wordt afgerond met behulp van elke afrondingsmethode die beschikbaar is in het veld **Afrondingstype** op de pagina **Btw-dienst**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="dbf32-123">Als de afrondingswaarde is ingesteld op 0,00, geldt het volgende:</span><span class="sxs-lookup"><span data-stu-id="dbf32-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="dbf32-124">Voor normale afronding werkt het afronden hetzelfde als voor **afronden = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="dbf32-125">Voor de **opties Afrondingstype** **Omlaag**, **Omhoog** en **Eigen voordeel** is het gedrag hetzelfde als voor **Afronden = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="dbf32-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="dbf32-126">Optie Afrondingstype</span><span class="sxs-lookup"><span data-stu-id="dbf32-126">Rounding form option</span></span>                | <span data-ttu-id="dbf32-127">Afrondingswaarde = 0,01</span><span class="sxs-lookup"><span data-stu-id="dbf32-127">Round-off value = 0.01</span></span> | <span data-ttu-id="dbf32-128">Afrondingswaarde = 0,10</span><span class="sxs-lookup"><span data-stu-id="dbf32-128">Round-off value = 0.10</span></span> | <span data-ttu-id="dbf32-129">Afrondingswaarde = 1,00</span><span class="sxs-lookup"><span data-stu-id="dbf32-129">Round-off value = 1.00</span></span> | <span data-ttu-id="dbf32-130">Afrondingswaarde = 100,00</span><span class="sxs-lookup"><span data-stu-id="dbf32-130">Round-off value = 100.00</span></span> | <span data-ttu-id="dbf32-131">Afrondingswaarde = 0,00</span><span class="sxs-lookup"><span data-stu-id="dbf32-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="dbf32-132">Normaal</span><span class="sxs-lookup"><span data-stu-id="dbf32-132">Normal</span></span>                              | <span data-ttu-id="dbf32-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="dbf32-133">98,765.43</span></span>              | <span data-ttu-id="dbf32-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="dbf32-134">98,765.40</span></span>              | <span data-ttu-id="dbf32-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-135">98,765.00</span></span>              | <span data-ttu-id="dbf32-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-136">98,800.00</span></span>                | <span data-ttu-id="dbf32-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="dbf32-137">98,765.43</span></span>                |
| <span data-ttu-id="dbf32-138">Naar beneden afronden</span><span class="sxs-lookup"><span data-stu-id="dbf32-138">Downward</span></span>                            | <span data-ttu-id="dbf32-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="dbf32-139">98,765.43</span></span>              | <span data-ttu-id="dbf32-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="dbf32-140">98,765.40</span></span>              | <span data-ttu-id="dbf32-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-141">98,765.00</span></span>              | <span data-ttu-id="dbf32-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-142">98,700.00</span></span>                | <span data-ttu-id="dbf32-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-143">98,765.00</span></span>                |
| <span data-ttu-id="dbf32-144">Naar boven afronden</span><span class="sxs-lookup"><span data-stu-id="dbf32-144">Rounding-up</span></span>                         | <span data-ttu-id="dbf32-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="dbf32-145">98,765.43</span></span>              | <span data-ttu-id="dbf32-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="dbf32-146">98,765.50</span></span>              | <span data-ttu-id="dbf32-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-147">98,766.00</span></span>              | <span data-ttu-id="dbf32-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-148">98,800.00</span></span>                | <span data-ttu-id="dbf32-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-149">98,766.00</span></span>                |
| <span data-ttu-id="dbf32-150">Eigen voordeel, voor een creditsaldo</span><span class="sxs-lookup"><span data-stu-id="dbf32-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="dbf32-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="dbf32-151">98,765.43</span></span>              | <span data-ttu-id="dbf32-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="dbf32-152">98,765.40</span></span>              | <span data-ttu-id="dbf32-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-153">98,765.00</span></span>              | <span data-ttu-id="dbf32-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-154">98,700.00</span></span>                | <span data-ttu-id="dbf32-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-155">98,765.00</span></span>                |
| <span data-ttu-id="dbf32-156">Eigen voordeel, voor een debitsaldo</span><span class="sxs-lookup"><span data-stu-id="dbf32-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="dbf32-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="dbf32-157">98,765.43</span></span>              | <span data-ttu-id="dbf32-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="dbf32-158">98,765.50</span></span>              | <span data-ttu-id="dbf32-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-159">98,766.00</span></span>              | <span data-ttu-id="dbf32-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-160">98,800.00</span></span>                | <span data-ttu-id="dbf32-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="dbf32-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="dbf32-162">Normale afronding en afrondingsprecisie is 0,01</span><span class="sxs-lookup"><span data-stu-id="dbf32-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="dbf32-163">Afronding</span><span class="sxs-lookup"><span data-stu-id="dbf32-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="dbf32-164">Berekeningsproces</span><span class="sxs-lookup"><span data-stu-id="dbf32-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="dbf32-165">afronding (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="dbf32-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="dbf32-166">afronding (1,015 / 0,01, 0) = afronding (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="dbf32-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="dbf32-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="dbf32-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="dbf32-168">afronding (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="dbf32-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="dbf32-169">afronding (1,014 / 0,01, 0) = afronding (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="dbf32-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="dbf32-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="dbf32-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="dbf32-171">afronding (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="dbf32-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="dbf32-172">afronding (1,011 / 0,02, 0) = afronding (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="dbf32-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="dbf32-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="dbf32-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="dbf32-174">afronding (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="dbf32-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="dbf32-175">afronding (1,009 / 0,02, 0) = afronding (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="dbf32-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="dbf32-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="dbf32-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="dbf32-177">Als u Eigen voordeel selecteert, is de afronding altijd in het voordeel van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="dbf32-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="dbf32-178">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="dbf32-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="dbf32-179">Btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="dbf32-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="dbf32-180">Een btw-betaling maken</span><span class="sxs-lookup"><span data-stu-id="dbf32-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="dbf32-181">Btw-transacties maken in documenten</span><span class="sxs-lookup"><span data-stu-id="dbf32-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="dbf32-182">Geboekte btw-transacties weergeven</span><span class="sxs-lookup"><span data-stu-id="dbf32-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="dbf32-183">Afrondingsfunctie</span><span class="sxs-lookup"><span data-stu-id="dbf32-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


