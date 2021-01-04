---
title: Afschrijvingseffecten met omkeringen
description: In dit artikel worden mogelijke implicaties van het terugboeken van een vaste-activatransactie beschreven.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441848"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="6f392-103">Afschrijvingseffecten met omkeringen</span><span class="sxs-lookup"><span data-stu-id="6f392-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f392-104">In dit artikel worden mogelijke implicaties van het terugboeken van een vaste-activatransactie beschreven.</span><span class="sxs-lookup"><span data-stu-id="6f392-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="6f392-105">U kunt vaste-activatransacties omkeren, net als de transacties die zijn gekoppeld aan een vast activum.</span><span class="sxs-lookup"><span data-stu-id="6f392-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="6f392-106">U kunt een omgekeerde transactie ook intrekken.</span><span class="sxs-lookup"><span data-stu-id="6f392-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="6f392-107">U kunt een transactie omkeren of intrekken, zolang als dit niet de meest recente transactie is die is geboekt op het boek voor het activum.</span><span class="sxs-lookup"><span data-stu-id="6f392-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="6f392-108">U moet eerst bepalen of er geen afschrijvingstransacties zijn geboekt na de transactie die u wilt omkeren.</span><span class="sxs-lookup"><span data-stu-id="6f392-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="6f392-109">De reden hiervoor is dat de afschrijving niet opnieuw wordt berekend wanneer u een transactie omkeert.</span><span class="sxs-lookup"><span data-stu-id="6f392-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="6f392-110">Dit betekent dat afschrijvingen vaak te hoog of te laag zijn na de omkering, zoals wordt geïllustreerd in de voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="6f392-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="6f392-111">Als u ervoor wilt zorgen dat de afschrijving juist is wanneer u een transactie omkeert, gaat u niet door met de omkering als u een bericht ontvangt waarin wordt uitgelegd dat de afschrijving niet opnieuw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="6f392-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="6f392-112">Keer in plaats hiervan eerst de afschrijvingstransactie om die is geboekt na de transactie die u wilt omkeren, en ga vervolgens door met de omkering.</span><span class="sxs-lookup"><span data-stu-id="6f392-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="6f392-113">U wordt niet gewaarschuwd voor herberekeningen van de afschrijving en u kunt doorgaan met de omkering.</span><span class="sxs-lookup"><span data-stu-id="6f392-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="6f392-114">In de volgende voorbeelden worden de berekeningen getoond die worden uitgevoerd als u het waarschuwingsbericht negeert en doorgaat zonder de afschrijvingstransacties eerst om te keren.</span><span class="sxs-lookup"><span data-stu-id="6f392-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="6f392-115">Voorbeeld 1: een te hoge afschrijving</span><span class="sxs-lookup"><span data-stu-id="6f392-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="6f392-116">Een activum wordt ingesteld op een levensduur van vijf jaar en een lineaire afschrijving (60 afschrijvingsperioden).</span><span class="sxs-lookup"><span data-stu-id="6f392-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6f392-117">In dit voorbeeld is de afschrijving te hoog.</span><span class="sxs-lookup"><span data-stu-id="6f392-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6f392-118">Activumtransactiehistorie</span><span class="sxs-lookup"><span data-stu-id="6f392-118">Asset transaction history</span></span>

| <span data-ttu-id="6f392-119">Datum</span><span class="sxs-lookup"><span data-stu-id="6f392-119">Date</span></span>       | <span data-ttu-id="6f392-120">Transactietype</span><span class="sxs-lookup"><span data-stu-id="6f392-120">Transaction type</span></span>                                                          | <span data-ttu-id="6f392-121">Bedrag</span><span class="sxs-lookup"><span data-stu-id="6f392-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6f392-122">1 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-122">January 1</span></span>  | <span data-ttu-id="6f392-123">Verwerving</span><span class="sxs-lookup"><span data-stu-id="6f392-123">Acquisition</span></span>                                                               | <span data-ttu-id="6f392-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="6f392-124">59,000.00</span></span>                                 |
| <span data-ttu-id="6f392-125">1 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-125">January 1</span></span>  | <span data-ttu-id="6f392-126">Verwervingscorrectie</span><span class="sxs-lookup"><span data-stu-id="6f392-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="6f392-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6f392-127">1,000.00</span></span>                                  |
| <span data-ttu-id="6f392-128">31 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-128">January 31</span></span> | <span data-ttu-id="6f392-129">Afschrijving (gemaakt met een voorstel voor één afschrijvingsperiode)</span><span class="sxs-lookup"><span data-stu-id="6f392-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6f392-130">1000,00-berekening: boekwaarde (59.000 + 1000 afschrijving) / aantal resterende afschrijvingsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="6f392-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6f392-131">Omkeringsactie</span><span class="sxs-lookup"><span data-stu-id="6f392-131">Reversal action</span></span>

| <span data-ttu-id="6f392-132">Datum</span><span class="sxs-lookup"><span data-stu-id="6f392-132">Date</span></span>      | <span data-ttu-id="6f392-133">Transactietype</span><span class="sxs-lookup"><span data-stu-id="6f392-133">Transaction type</span></span>                | <span data-ttu-id="6f392-134">Bedrag</span><span class="sxs-lookup"><span data-stu-id="6f392-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="6f392-135">1 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-135">January 1</span></span> | <span data-ttu-id="6f392-136">Omkering van verwervingscorrectie</span><span class="sxs-lookup"><span data-stu-id="6f392-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="6f392-137">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="6f392-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6f392-138">Afschrijvingseffect</span><span class="sxs-lookup"><span data-stu-id="6f392-138">Depreciation effect</span></span>

| <span data-ttu-id="6f392-139">Datum</span><span class="sxs-lookup"><span data-stu-id="6f392-139">Date</span></span>        | <span data-ttu-id="6f392-140">Transactietype</span><span class="sxs-lookup"><span data-stu-id="6f392-140">Transaction type</span></span>        | <span data-ttu-id="6f392-141">Bedrag</span><span class="sxs-lookup"><span data-stu-id="6f392-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f392-142">28 februari</span><span class="sxs-lookup"><span data-stu-id="6f392-142">February 28</span></span> | <span data-ttu-id="6f392-143">Afschrijving (voorstel)</span><span class="sxs-lookup"><span data-stu-id="6f392-143">Depreciation (proposal)</span></span> | <span data-ttu-id="6f392-144">983,05-berekening: boekwaarde (59.000 - 1000 afschrijving) / aantal resterende afschrijvingsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="6f392-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6f392-145">De afschrijving is 16,95 (1000 - 983,05) te hoog.</span><span class="sxs-lookup"><span data-stu-id="6f392-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="6f392-146">Voorbeeld 2: een te lage afschrijving</span><span class="sxs-lookup"><span data-stu-id="6f392-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="6f392-147">Een activum wordt ingesteld op een levensduur van vijf jaar en een lineaire afschrijving (60 afschrijvingsperioden).</span><span class="sxs-lookup"><span data-stu-id="6f392-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6f392-148">In dit voorbeeld is de afschrijving te laag.</span><span class="sxs-lookup"><span data-stu-id="6f392-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6f392-149">Activumtransactiehistorie</span><span class="sxs-lookup"><span data-stu-id="6f392-149">Asset transaction history</span></span>

| <span data-ttu-id="6f392-150">Datum</span><span class="sxs-lookup"><span data-stu-id="6f392-150">Date</span></span>       | <span data-ttu-id="6f392-151">Transactietype</span><span class="sxs-lookup"><span data-stu-id="6f392-151">Transaction type</span></span>                                                          | <span data-ttu-id="6f392-152">Bedrag</span><span class="sxs-lookup"><span data-stu-id="6f392-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="6f392-153">1 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-153">January 1</span></span>  | <span data-ttu-id="6f392-154">Verwerving</span><span class="sxs-lookup"><span data-stu-id="6f392-154">Acquisition</span></span>                                                               | <span data-ttu-id="6f392-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="6f392-155">59,000.00</span></span>                                   |
| <span data-ttu-id="6f392-156">1 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-156">January 1</span></span>  | <span data-ttu-id="6f392-157">Afwaarderingscorrectie</span><span class="sxs-lookup"><span data-stu-id="6f392-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="6f392-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6f392-158">1,000.00</span></span>                                    |
| <span data-ttu-id="6f392-159">31 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-159">January 31</span></span> | <span data-ttu-id="6f392-160">Afschrijving (gemaakt met een voorstel voor één afschrijvingsperiode)</span><span class="sxs-lookup"><span data-stu-id="6f392-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6f392-161">966,67-berekening: boekwaarde (59.000 - 1000 afschrijving) / aantal resterende afschrijvingsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="6f392-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6f392-162">Omkeringsactie</span><span class="sxs-lookup"><span data-stu-id="6f392-162">Reversal action</span></span>

| <span data-ttu-id="6f392-163">Datum</span><span class="sxs-lookup"><span data-stu-id="6f392-163">Date</span></span>      | <span data-ttu-id="6f392-164">Transactietype</span><span class="sxs-lookup"><span data-stu-id="6f392-164">Transaction type</span></span>               | <span data-ttu-id="6f392-165">Bedrag</span><span class="sxs-lookup"><span data-stu-id="6f392-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="6f392-166">1 januari</span><span class="sxs-lookup"><span data-stu-id="6f392-166">January 1</span></span> | <span data-ttu-id="6f392-167">Omkering van afwaarderingscorrectie</span><span class="sxs-lookup"><span data-stu-id="6f392-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="6f392-168">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="6f392-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6f392-169">Afschrijvingseffect</span><span class="sxs-lookup"><span data-stu-id="6f392-169">Depreciation effect</span></span>

| <span data-ttu-id="6f392-170">Datum</span><span class="sxs-lookup"><span data-stu-id="6f392-170">Date</span></span>        | <span data-ttu-id="6f392-171">Transactietype</span><span class="sxs-lookup"><span data-stu-id="6f392-171">Transaction type</span></span>        | <span data-ttu-id="6f392-172">Bedrag</span><span class="sxs-lookup"><span data-stu-id="6f392-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f392-173">28 februari</span><span class="sxs-lookup"><span data-stu-id="6f392-173">February 28</span></span> | <span data-ttu-id="6f392-174">Afschrijving (voorstel)</span><span class="sxs-lookup"><span data-stu-id="6f392-174">Depreciation (proposal)</span></span> | <span data-ttu-id="6f392-175">983,62-berekening: boekwaarde (59.000 - 966,67 afschrijving) / aantal resterende afschrijvingsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="6f392-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6f392-176">De afschrijving is 16,95 (983,62 - 966,67) te laag.</span><span class="sxs-lookup"><span data-stu-id="6f392-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="6f392-177">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6f392-177">Additional resources</span></span>
--------

[<span data-ttu-id="6f392-178">Afschrijving vaste activa</span><span class="sxs-lookup"><span data-stu-id="6f392-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



