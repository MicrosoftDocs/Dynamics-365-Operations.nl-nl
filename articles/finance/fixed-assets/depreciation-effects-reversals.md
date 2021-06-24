---
title: Afschrijvingseffecten met omkeringen
description: In dit artikel worden mogelijke implicaties van het terugboeken van een vaste-activatransactie beschreven.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d47a25835eab16438ea47bf3960132debc8c975
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187887"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="c4209-103">Afschrijvingseffecten met omkeringen</span><span class="sxs-lookup"><span data-stu-id="c4209-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4209-104">In dit artikel worden mogelijke implicaties van het terugboeken van een vaste-activatransactie beschreven.</span><span class="sxs-lookup"><span data-stu-id="c4209-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="c4209-105">U kunt vaste-activatransacties omkeren, net als de transacties die zijn gekoppeld aan een vast activum.</span><span class="sxs-lookup"><span data-stu-id="c4209-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="c4209-106">U kunt een omgekeerde transactie ook intrekken.</span><span class="sxs-lookup"><span data-stu-id="c4209-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="c4209-107">U kunt een transactie omkeren of intrekken, zolang als dit niet de meest recente transactie is die is geboekt op het boek voor het activum.</span><span class="sxs-lookup"><span data-stu-id="c4209-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="c4209-108">U moet eerst bepalen of er geen afschrijvingstransacties zijn geboekt na de transactie die u wilt omkeren.</span><span class="sxs-lookup"><span data-stu-id="c4209-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="c4209-109">De reden hiervoor is dat de afschrijving niet opnieuw wordt berekend wanneer u een transactie omkeert.</span><span class="sxs-lookup"><span data-stu-id="c4209-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="c4209-110">Dit betekent dat afschrijvingen vaak te hoog of te laag zijn na de omkering, zoals wordt geïllustreerd in de voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="c4209-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="c4209-111">Als u ervoor wilt zorgen dat de afschrijving juist is wanneer u een transactie omkeert, gaat u niet door met de omkering als u een bericht ontvangt waarin wordt uitgelegd dat de afschrijving niet opnieuw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="c4209-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="c4209-112">Keer in plaats hiervan eerst de afschrijvingstransactie om die is geboekt na de transactie die u wilt omkeren, en ga vervolgens door met de omkering.</span><span class="sxs-lookup"><span data-stu-id="c4209-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="c4209-113">U wordt niet gewaarschuwd voor herberekeningen van de afschrijving en u kunt doorgaan met de omkering.</span><span class="sxs-lookup"><span data-stu-id="c4209-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="c4209-114">In de volgende voorbeelden worden de berekeningen getoond die worden uitgevoerd als u het waarschuwingsbericht negeert en doorgaat zonder de afschrijvingstransacties eerst om te keren.</span><span class="sxs-lookup"><span data-stu-id="c4209-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="c4209-115">Voorbeeld 1: een te hoge afschrijving</span><span class="sxs-lookup"><span data-stu-id="c4209-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="c4209-116">Een activum wordt ingesteld op een levensduur van vijf jaar en een lineaire afschrijving (60 afschrijvingsperioden).</span><span class="sxs-lookup"><span data-stu-id="c4209-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="c4209-117">In dit voorbeeld is de afschrijving te hoog.</span><span class="sxs-lookup"><span data-stu-id="c4209-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="c4209-118">Activumtransactiehistorie</span><span class="sxs-lookup"><span data-stu-id="c4209-118">Asset transaction history</span></span>

| <span data-ttu-id="c4209-119">Datum</span><span class="sxs-lookup"><span data-stu-id="c4209-119">Date</span></span>       | <span data-ttu-id="c4209-120">Transactietype</span><span class="sxs-lookup"><span data-stu-id="c4209-120">Transaction type</span></span>                                                          | <span data-ttu-id="c4209-121">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c4209-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c4209-122">1 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-122">January 1</span></span>  | <span data-ttu-id="c4209-123">Verwerving</span><span class="sxs-lookup"><span data-stu-id="c4209-123">Acquisition</span></span>                                                               | <span data-ttu-id="c4209-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="c4209-124">59,000.00</span></span>                                 |
| <span data-ttu-id="c4209-125">1 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-125">January 1</span></span>  | <span data-ttu-id="c4209-126">Verwervingscorrectie</span><span class="sxs-lookup"><span data-stu-id="c4209-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="c4209-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4209-127">1,000.00</span></span>                                  |
| <span data-ttu-id="c4209-128">31 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-128">January 31</span></span> | <span data-ttu-id="c4209-129">Afschrijving (gemaakt met een voorstel voor één afschrijvingsperiode)</span><span class="sxs-lookup"><span data-stu-id="c4209-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="c4209-130">1000,00-berekening: boekwaarde (59.000 + 1000 afschrijving) / aantal resterende afschrijvingsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="c4209-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="c4209-131">Omkeringsactie</span><span class="sxs-lookup"><span data-stu-id="c4209-131">Reversal action</span></span>

| <span data-ttu-id="c4209-132">Datum</span><span class="sxs-lookup"><span data-stu-id="c4209-132">Date</span></span>      | <span data-ttu-id="c4209-133">Transactietype</span><span class="sxs-lookup"><span data-stu-id="c4209-133">Transaction type</span></span>                | <span data-ttu-id="c4209-134">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c4209-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="c4209-135">1 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-135">January 1</span></span> | <span data-ttu-id="c4209-136">Omkering van verwervingscorrectie</span><span class="sxs-lookup"><span data-stu-id="c4209-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="c4209-137">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4209-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="c4209-138">Afschrijvingseffect</span><span class="sxs-lookup"><span data-stu-id="c4209-138">Depreciation effect</span></span>

| <span data-ttu-id="c4209-139">Datum</span><span class="sxs-lookup"><span data-stu-id="c4209-139">Date</span></span>        | <span data-ttu-id="c4209-140">Transactietype</span><span class="sxs-lookup"><span data-stu-id="c4209-140">Transaction type</span></span>        | <span data-ttu-id="c4209-141">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c4209-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4209-142">28 februari</span><span class="sxs-lookup"><span data-stu-id="c4209-142">February 28</span></span> | <span data-ttu-id="c4209-143">Afschrijving (voorstel)</span><span class="sxs-lookup"><span data-stu-id="c4209-143">Depreciation (proposal)</span></span> | <span data-ttu-id="c4209-144">983,05-berekening: boekwaarde (59.000 - 1000 afschrijving) / aantal resterende afschrijvingsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="c4209-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="c4209-145">De afschrijving is 16,95 (1000 - 983,05) te hoog.</span><span class="sxs-lookup"><span data-stu-id="c4209-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="c4209-146">Voorbeeld 2: een te lage afschrijving</span><span class="sxs-lookup"><span data-stu-id="c4209-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="c4209-147">Een activum wordt ingesteld op een levensduur van vijf jaar en een lineaire afschrijving (60 afschrijvingsperioden).</span><span class="sxs-lookup"><span data-stu-id="c4209-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="c4209-148">In dit voorbeeld is de afschrijving te laag.</span><span class="sxs-lookup"><span data-stu-id="c4209-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="c4209-149">Activumtransactiehistorie</span><span class="sxs-lookup"><span data-stu-id="c4209-149">Asset transaction history</span></span>

| <span data-ttu-id="c4209-150">Datum</span><span class="sxs-lookup"><span data-stu-id="c4209-150">Date</span></span>       | <span data-ttu-id="c4209-151">Transactietype</span><span class="sxs-lookup"><span data-stu-id="c4209-151">Transaction type</span></span>                                                          | <span data-ttu-id="c4209-152">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c4209-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="c4209-153">1 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-153">January 1</span></span>  | <span data-ttu-id="c4209-154">Verwerving</span><span class="sxs-lookup"><span data-stu-id="c4209-154">Acquisition</span></span>                                                               | <span data-ttu-id="c4209-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="c4209-155">59,000.00</span></span>                                   |
| <span data-ttu-id="c4209-156">1 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-156">January 1</span></span>  | <span data-ttu-id="c4209-157">Afwaarderingscorrectie</span><span class="sxs-lookup"><span data-stu-id="c4209-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="c4209-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4209-158">1,000.00</span></span>                                    |
| <span data-ttu-id="c4209-159">31 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-159">January 31</span></span> | <span data-ttu-id="c4209-160">Afschrijving (gemaakt met een voorstel voor één afschrijvingsperiode)</span><span class="sxs-lookup"><span data-stu-id="c4209-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="c4209-161">966,67-berekening: boekwaarde (59.000 - 1000 afschrijving) / aantal resterende afschrijvingsperioden (60)</span><span class="sxs-lookup"><span data-stu-id="c4209-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="c4209-162">Omkeringsactie</span><span class="sxs-lookup"><span data-stu-id="c4209-162">Reversal action</span></span>

| <span data-ttu-id="c4209-163">Datum</span><span class="sxs-lookup"><span data-stu-id="c4209-163">Date</span></span>      | <span data-ttu-id="c4209-164">Transactietype</span><span class="sxs-lookup"><span data-stu-id="c4209-164">Transaction type</span></span>               | <span data-ttu-id="c4209-165">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c4209-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="c4209-166">1 januari</span><span class="sxs-lookup"><span data-stu-id="c4209-166">January 1</span></span> | <span data-ttu-id="c4209-167">Omkering van afwaarderingscorrectie</span><span class="sxs-lookup"><span data-stu-id="c4209-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="c4209-168">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4209-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="c4209-169">Afschrijvingseffect</span><span class="sxs-lookup"><span data-stu-id="c4209-169">Depreciation effect</span></span>

| <span data-ttu-id="c4209-170">Datum</span><span class="sxs-lookup"><span data-stu-id="c4209-170">Date</span></span>        | <span data-ttu-id="c4209-171">Transactietype</span><span class="sxs-lookup"><span data-stu-id="c4209-171">Transaction type</span></span>        | <span data-ttu-id="c4209-172">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c4209-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4209-173">28 februari</span><span class="sxs-lookup"><span data-stu-id="c4209-173">February 28</span></span> | <span data-ttu-id="c4209-174">Afschrijving (voorstel)</span><span class="sxs-lookup"><span data-stu-id="c4209-174">Depreciation (proposal)</span></span> | <span data-ttu-id="c4209-175">983,62-berekening: boekwaarde (59.000 - 966,67 afschrijving) / aantal resterende afschrijvingsperioden (59)</span><span class="sxs-lookup"><span data-stu-id="c4209-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="c4209-176">De afschrijving is 16,95 (983,62 - 966,67) te laag.</span><span class="sxs-lookup"><span data-stu-id="c4209-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



## <a name="additional-resources"></a><span data-ttu-id="c4209-177">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c4209-177">Additional resources</span></span>

[<span data-ttu-id="c4209-178">Afschrijving vaste activa</span><span class="sxs-lookup"><span data-stu-id="c4209-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]