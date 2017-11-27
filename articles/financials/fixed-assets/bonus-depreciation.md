---
title: Bonusafschrijving
description: In dit artikel vindt u een overzicht van de functionaliteit voor bonusafschrijving.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 48d50cbba648beb9831e186cd160853abe79c4e4
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="bonus-depreciation"></a><span data-ttu-id="53da4-103">Bonusafschrijving</span><span class="sxs-lookup"><span data-stu-id="53da4-103">Bonus depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="53da4-104">In dit artikel vindt u een overzicht van de functionaliteit voor bonusafschrijving.</span><span class="sxs-lookup"><span data-stu-id="53da4-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="53da4-105">Voor bonusafschrijving kunt u gedurende het eerste jaar waarin het activum in gebruik wordt genomen en wordt afgeschreven, extra bedragen of bonussen afschrijven.</span><span class="sxs-lookup"><span data-stu-id="53da4-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="53da4-106">De bonusafschrijving moet vóór andere afschrijvingsberekeningen worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="53da4-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="53da4-107">Daarom is het beste om bonusafschrijving met boeken te gebruiken als de functionaliteit Boeken naar grootboek is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="53da4-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="53da4-108">U kunt de optie **Transacties verwijderen die niet zijn geboekt naar grootboek** gebruiken om historische transacties te verwijderen voor boeken die niet naar het grootboek boeken.</span><span class="sxs-lookup"><span data-stu-id="53da4-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="53da4-109">U kunt bonusafschrijving later in de levenscyclus van het activum aanpassen door afschrijvingstransacties te verwijderen die eerder zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="53da4-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="53da4-110">U kunt bonusafschrijving met behulp van het voorstelproces berekenen of zelf transacties voor bonusafschrijving maken.</span><span class="sxs-lookup"><span data-stu-id="53da4-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="53da4-111">U kunt geen transacties voor bonusafschrijving maken als er afschrijvingstransacties of correctietransacties voor afschrijving voor dat activumboek zijn.</span><span class="sxs-lookup"><span data-stu-id="53da4-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="53da4-112">Wanneer u met het voorstelproces de bonusafschrijving berekent, worden alle bestaande bonustransacties in de berekening van de basis opgenomen.</span><span class="sxs-lookup"><span data-stu-id="53da4-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="53da4-113">De berekening omvat ook alle vorige bonusafschrijvingen die u handmatig voor de activa hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="53da4-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="53da4-114">Als er meerdere bonusafschrijvingen voor een activum worden uitgevoerd, wordt rekening gehouden met prioriteit.</span><span class="sxs-lookup"><span data-stu-id="53da4-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="53da4-115">Elke bonus vermindert de activabasis voor de volgende bonus.</span><span class="sxs-lookup"><span data-stu-id="53da4-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="53da4-116">Er wordt in de activabasis voor berekeningen van de bonusafschrijving geen rekening gehouden met de restwaarde. De afschrijvingsconventie geldt niet voor de bonusafschrijving.</span><span class="sxs-lookup"><span data-stu-id="53da4-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="53da4-117">Bepaalde eigendommen komen momenteel in de Verenigde Staten in aanmerking als Section 179-eigendom.</span><span class="sxs-lookup"><span data-stu-id="53da4-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="53da4-118">Door de Section 179-inhouding te gebruiken, kunt de gehele kosten van een bepaald eigendom of een gedeelte van de kosten, tot een bepaald bedrag, terugbetaald krijgen.</span><span class="sxs-lookup"><span data-stu-id="53da4-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="53da4-119">U kunt de kosten terugbetaald krijgen door de kosten af te trekken in het jaar dat u het eigendom in gebruik hebt genomen.</span><span class="sxs-lookup"><span data-stu-id="53da4-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="53da4-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="53da4-120">Example</span></span>
<span data-ttu-id="53da4-121">De volgende bonusafschrijvingen zijn gekoppeld aan een activumboek:</span><span class="sxs-lookup"><span data-stu-id="53da4-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="53da4-122">**Section 179:** 1.000,00, Prioriteit 1</span><span class="sxs-lookup"><span data-stu-id="53da4-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="53da4-123">**Liberty Zone:** 30 procent, Prioriteit 2</span><span class="sxs-lookup"><span data-stu-id="53da4-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="53da4-124">De kosten van de verwerving van de activa zijn 5.000,00.</span><span class="sxs-lookup"><span data-stu-id="53da4-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="53da4-125">Wanneer de bonusafschrijving wordt berekend, is het eerste bedrag van de bonusafschrijving € 1.000,00 voor de Section 179-afschrijving.</span><span class="sxs-lookup"><span data-stu-id="53da4-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="53da4-126">Het volgende bedrag van de bonusafschrijving, voor de afschrijving van de Liberty Zone, wordt als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="53da4-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="53da4-127">Verwervingskosten – 1.000 (Section 179-afschrijving) x 30 procent = € 1.200</span><span class="sxs-lookup"><span data-stu-id="53da4-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="53da4-128">Als het bedrag van de bonusafschrijving meer is dan de overige verwervingskosten, is het bedrag van de bonusafschrijving het resultaat van de bonusafschrijving of de resterende verwervingskosten, welk bedrag van de twee het laagst is.</span><span class="sxs-lookup"><span data-stu-id="53da4-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="53da4-129">Als de resterende verwervingskosten 0 (nul) of minder zijn, worden er geen transacties voor bonusafschrijving gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="53da4-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="53da4-130">Wanneer bonusafschrijving met behulp van het voorstelproces wordt berekend, wordt er een transactie voor bonusafschrijving voor alle van toepassing zijnde bonusafschrijvingsrecords berekend die aan het activumboek zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="53da4-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="53da4-131">U kunt net zoveel bonusafschrijvingsrecords maken als u wilt.</span><span class="sxs-lookup"><span data-stu-id="53da4-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="53da4-132">Als u deze records toewijst aan een activagroepsboek, worden deze records op het activumboek toegepast.</span><span class="sxs-lookup"><span data-stu-id="53da4-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="53da4-133">Bonusafschrijving wordt als een percentage of een vast bedrag ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="53da4-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="53da4-134">Wanneer u afschrijvingsvoorstellen boekt, worden transacties voor bonusafschrijving los van de afschrijvingstransacties naar het boek geboekt.</span><span class="sxs-lookup"><span data-stu-id="53da4-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>




