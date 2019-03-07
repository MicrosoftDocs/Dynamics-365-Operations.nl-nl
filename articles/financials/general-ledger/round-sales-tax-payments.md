---
title: Btw-betalingen en afrondingsregels
description: In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
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
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "367841"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="d4638-103">Btw-betalingen en afrondingsregels</span><span class="sxs-lookup"><span data-stu-id="d4638-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4638-104">In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="d4638-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="d4638-105">Periodiek moet btw worden aangegeven en betaald aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="d4638-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="d4638-106">Dit kan worden uitgevoerd door het proces Btw vereffenen en boeken op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="d4638-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="d4638-107">Btw voor een periode wordt vereffend voor de btw-rekeningen en het btw-saldo wordt naar de rekening Btw-vereffening geboekt.</span><span class="sxs-lookup"><span data-stu-id="d4638-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="d4638-108">Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw.</span><span class="sxs-lookup"><span data-stu-id="d4638-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="d4638-109">Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.</span><span class="sxs-lookup"><span data-stu-id="d4638-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="d4638-110">Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.</span><span class="sxs-lookup"><span data-stu-id="d4638-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="d4638-111">    Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d4638-111">Example:</span></span>

<span data-ttu-id="d4638-112">De totale btw voor een periode toont een creditsaldo van -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="d4638-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="d4638-113">De rechtspersoon inde meer btw dan dat betaald werd.</span><span class="sxs-lookup"><span data-stu-id="d4638-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="d4638-114">Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst.</span><span class="sxs-lookup"><span data-stu-id="d4638-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="d4638-115">De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00.</span><span class="sxs-lookup"><span data-stu-id="d4638-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="d4638-116">De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="d4638-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="d4638-117">Klik op Btw &gt; Indirecte belastingen &gt; Btw &gt; Btw-diensten</span><span class="sxs-lookup"><span data-stu-id="d4638-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="d4638-118">Selecteer op het sneltabblad Algemeen in het veld Afrondingstype de optie Normaal.</span><span class="sxs-lookup"><span data-stu-id="d4638-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="d4638-119">Typ 1,00 in het veld Afronden.</span><span class="sxs-lookup"><span data-stu-id="d4638-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="d4638-120">Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="d4638-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="d4638-121">(Klik op Btw &gt; Aangiften &gt; Btw &gt; Btw vereffenen en boeken.)</span><span class="sxs-lookup"><span data-stu-id="d4638-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="d4638-122">Op de btw-vereffeningsrekening is het bedrag van uw btw-belastingschuld van 98.765,43 afgerond naar 98.765.</span><span class="sxs-lookup"><span data-stu-id="d4638-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="d4638-123">In de volgende tabel ziet u hoe een bedrag van 98.765,43 wordt afgerond met behulp van elke afrondingsmethode die beschikbaar is in het veld Afrondingstype op de pagina Btw-dienst.</span><span class="sxs-lookup"><span data-stu-id="d4638-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="d4638-124">Optie Afrondingstype</span><span class="sxs-lookup"><span data-stu-id="d4638-124">Rounding form option</span></span>                | <span data-ttu-id="d4638-125">Afrondingswaarde = 0,01</span><span class="sxs-lookup"><span data-stu-id="d4638-125">Round-off value = 0.01</span></span> | <span data-ttu-id="d4638-126">Afrondingswaarde = 0,10</span><span class="sxs-lookup"><span data-stu-id="d4638-126">Round-off value = 0.10</span></span> | <span data-ttu-id="d4638-127">Afrondingswaarde = 1,00</span><span class="sxs-lookup"><span data-stu-id="d4638-127">Round-off value = 1.00</span></span> | <span data-ttu-id="d4638-128">Afrondingswaarde = 100,00</span><span class="sxs-lookup"><span data-stu-id="d4638-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="d4638-129">Normaal</span><span class="sxs-lookup"><span data-stu-id="d4638-129">Normal</span></span>                              | <span data-ttu-id="d4638-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d4638-130">98,765.43</span></span>              | <span data-ttu-id="d4638-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="d4638-131">98,765.40</span></span>              | <span data-ttu-id="d4638-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="d4638-132">98,765.00</span></span>              | <span data-ttu-id="d4638-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="d4638-133">98,800.00</span></span>                |
| <span data-ttu-id="d4638-134">Naar beneden afronden</span><span class="sxs-lookup"><span data-stu-id="d4638-134">Downward</span></span>                            | <span data-ttu-id="d4638-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d4638-135">98,765.43</span></span>              | <span data-ttu-id="d4638-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="d4638-136">98,765.40</span></span>              | <span data-ttu-id="d4638-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="d4638-137">98,765.00</span></span>              | <span data-ttu-id="d4638-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="d4638-138">98,700.00</span></span>                |
| <span data-ttu-id="d4638-139">Naar boven afronden</span><span class="sxs-lookup"><span data-stu-id="d4638-139">Rounding-up</span></span>                         | <span data-ttu-id="d4638-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d4638-140">98,765.43</span></span>              | <span data-ttu-id="d4638-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="d4638-141">98,765.50</span></span>              | <span data-ttu-id="d4638-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="d4638-142">98,766.00</span></span>              | <span data-ttu-id="d4638-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="d4638-143">98,800.00</span></span>                |
| <span data-ttu-id="d4638-144">Eigen voordeel, voor een creditsaldo</span><span class="sxs-lookup"><span data-stu-id="d4638-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="d4638-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d4638-145">98,765.43</span></span>              | <span data-ttu-id="d4638-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="d4638-146">98,765.40</span></span>              | <span data-ttu-id="d4638-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="d4638-147">98,765.00</span></span>              | <span data-ttu-id="d4638-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="d4638-148">98,700.00</span></span>                |
| <span data-ttu-id="d4638-149">Eigen voordeel, voor een debitsaldo</span><span class="sxs-lookup"><span data-stu-id="d4638-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="d4638-150">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d4638-150">98,765.43</span></span>              | <span data-ttu-id="d4638-151">98.765,50</span><span class="sxs-lookup"><span data-stu-id="d4638-151">98,765.50</span></span>              | <span data-ttu-id="d4638-152">98.766,00</span><span class="sxs-lookup"><span data-stu-id="d4638-152">98,766.00</span></span>              | <span data-ttu-id="d4638-153">98.800,00</span><span class="sxs-lookup"><span data-stu-id="d4638-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="d4638-154">Als u Eigen voordeel selecteert, is de afronding altijd in het voordeel van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d4638-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="d4638-155">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="d4638-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="d4638-156">Btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="d4638-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="d4638-157">Een btw-betaling maken</span><span class="sxs-lookup"><span data-stu-id="d4638-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="d4638-158">Verkooptransacties maken in documenten</span><span class="sxs-lookup"><span data-stu-id="d4638-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="d4638-159">Geboekte btw-transacties weergeven</span><span class="sxs-lookup"><span data-stu-id="d4638-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)


