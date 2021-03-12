---
title: Degressieve afschrijving na een splitsing
description: In dit onderwerp wordt de methode beschreven die wordt gebruikt in vaste activa om de afschrijving te berekenen nadat een activum is gesplitst met de methode degressieve afschrijving.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
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
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea89d54b9b8287d9c81b75a99c5808b5deb05cef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976085"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="eda7f-103">Degressieve afschrijving na een splitsing</span><span class="sxs-lookup"><span data-stu-id="eda7f-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eda7f-104">In dit onderwerp wordt de methode beschreven die wordt gebruikt in vaste activa om de afschrijving te berekenen nadat een activum is gesplitst naar een ander activum met de methode degressieve afschrijving.</span><span class="sxs-lookup"><span data-stu-id="eda7f-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="eda7f-105">Het afschrijvingsjaar dat in het activa boek is geconfigureerd, is het fiscaal jaar.</span><span class="sxs-lookup"><span data-stu-id="eda7f-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="eda7f-106">Zie [Degressieve afschrijving](reduce-balance-depreciation.md) en [Een vast activum splitsen](tasks/split-fixed-asset.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eda7f-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="eda7f-107">Als u een vast activum splitst tijdens een boekperiode die later is dan de periode waarin het activum is aangeschaft, wordt met de degressieve afschrijving rekening gehouden met de netto boekwaarde (NBW) van het activum voor het vorige jaar.</span><span class="sxs-lookup"><span data-stu-id="eda7f-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="eda7f-108">Er wordt ook rekening gehouden met de verwervings- en afschrijvingscorrectietransacties die zijn gegenereerd op basis van de transactie waarmee het activum is gesplitst.</span><span class="sxs-lookup"><span data-stu-id="eda7f-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="eda7f-109">Bij dit gedrag wordt ervan uitgegaan dat het activum in één fiscaal jaar is verworven en in een later fiscaal jaar is opgesplitst.</span><span class="sxs-lookup"><span data-stu-id="eda7f-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="eda7f-110">Het bedrag dat moet worden afgeschreven voor het oorspronkelijke activum na de splitsing weerspiegelt de NBW van het activum voordat het activum is gesplitst, en de verwervings- en afschrijvingscorrectietransactie die voor de splitsing is geboekt.</span><span class="sxs-lookup"><span data-stu-id="eda7f-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="eda7f-111">De volgende voorwaarden zijn bijvoorbeeld van toepassing:</span><span class="sxs-lookup"><span data-stu-id="eda7f-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="eda7f-112">De boekperiode is van 30 juni tot 1 juli.</span><span class="sxs-lookup"><span data-stu-id="eda7f-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="eda7f-113">Het degressieve saldopercentage is 18 procent en een activum wordt verworven in juni 2019 tegen een verwervingsprijs van $10.000,-.</span><span class="sxs-lookup"><span data-stu-id="eda7f-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="eda7f-114">De afschrijving van het eerste fiscale jaar is gelijk aan $18.000,-, de maandelijkse afschrijving is $150,- en het activum wordt vervolgens afgeschreven tot november 2019 in de hoeveelheid $738,75.</span><span class="sxs-lookup"><span data-stu-id="eda7f-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="eda7f-115">In november 2019 wordt 80 procent van het activum opgesplitst in andere vaste activa.</span><span class="sxs-lookup"><span data-stu-id="eda7f-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="eda7f-116">[![Degressieve afschrijving na een splitsing](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="eda7f-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="eda7f-117">Het bedrag dat moet worden afgeschreven voor het oorspronkelijke activum, is $1.822,25.</span><span class="sxs-lookup"><span data-stu-id="eda7f-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="eda7f-118">Dit bedrag is gelijk aan de NBW voordat de gesplitste transactie is geboekt ($9.111,25), plus de verwervingscorrectie die wordt gegenereerd tijdens het boeken van de gesplitste transactie (-$8.000,-), plus de afschrijvingscorrectie die wordt gegenereerd tijdens de gesplitste transactie ($711,-).</span><span class="sxs-lookup"><span data-stu-id="eda7f-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="eda7f-119">Daarom is de afschrijving voor het tweede jaar (1.822,25 × 18 procent) ÷ 12 = $27,33.</span><span class="sxs-lookup"><span data-stu-id="eda7f-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="eda7f-120">Het bedrag dat moet worden afgeschreven voor het nieuwe vaste activum in het eerste jaar is (8.000 × 18 procent) ÷ 12 = $120.</span><span class="sxs-lookup"><span data-stu-id="eda7f-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
