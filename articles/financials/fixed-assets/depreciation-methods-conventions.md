---
title: Afschrijvingsmethoden en conventies
description: Dit artikel geeft een overzicht van de afschrijvingsconventies en afschrijvingsmethoden die door Microsoft Dynamics 365 for Finance and Operations worden ondersteund.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: be8e05a386178b9172a906109e015269dc72b32e
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="1ea2f-103">Afschrijvingsmethoden en conventies</span><span class="sxs-lookup"><span data-stu-id="1ea2f-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ea2f-104">Dit artikel geeft een overzicht van de afschrijvingsconventies en afschrijvingsmethoden die door Microsoft Dynamics 365 for Finance and Operations worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="1ea2f-105">U kunt verscheidene afschrijvingsmethoden en -conventies selecteren.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="1ea2f-106">Het doel van de methoden is het toewijzen van de afschrijfbare waarde van het vaste activum in boekperioden.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="1ea2f-107">De afschrijfbare waarde van het vaste activum is de verwervingsprijs, verminderd met een eventuele restwaarde.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="1ea2f-108">Als u afschrijvingsconventies gebruikt en de uitvoeringsdatum van de laatste afschrijving voor een activum wijzigt, waardoor dan enkele afschrijvingen worden overgeslagen, kan de afschrijving voor het afgelopen jaar hoger of lager zijn dan verwacht.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="1ea2f-109">De afschrijving wordt aangepast met het aantal afschrijvingsperioden dat werd beïnvloed door de aanpassing van de uitvoeringsdatum van de laatste afschrijving.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="1ea2f-110">Als u bijvoorbeeld de afschrijvingsconventie Half jaar voor drie jaar gebruikt, vindt de afschrijving doorgaans in 3 1/2 jaar plaats.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="1ea2f-111">Als u de uitvoeringsdatum van de laatste afschrijving wijzigt tijdens die 3 1/2 jaar, wordt het aantal perioden dat wordt beïnvloed vergroot door het laatste jaar van de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="1ea2f-112">Als u de datum drie maanden verschuift, heeft het laatste jaar negen maanden afschrijving, terwijl er normaal gesproken zes maanden afschrijving zou zijn.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="1ea2f-113">U kunt uit de volgende afschrijvingsconventies kiezen.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="1ea2f-114">Half jaar</span><span class="sxs-lookup"><span data-stu-id="1ea2f-114">Half year</span></span>
-   <span data-ttu-id="1ea2f-115">Hele maand</span><span class="sxs-lookup"><span data-stu-id="1ea2f-115">Full month</span></span>
-   <span data-ttu-id="1ea2f-116">Midden kwartaal</span><span class="sxs-lookup"><span data-stu-id="1ea2f-116">Mid quarter</span></span>
-   <span data-ttu-id="1ea2f-117">Midden maand (1ste van de maand)</span><span class="sxs-lookup"><span data-stu-id="1ea2f-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="1ea2f-118">Midden maand (15e van de maand)</span><span class="sxs-lookup"><span data-stu-id="1ea2f-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="1ea2f-119">Half jaar (begin van het jaar)</span><span class="sxs-lookup"><span data-stu-id="1ea2f-119">Half year (start of year)</span></span>
-   <span data-ttu-id="1ea2f-120">Halfjaar (volgend jaar)</span><span class="sxs-lookup"><span data-stu-id="1ea2f-120">Half year (next year)</span></span>

<span data-ttu-id="1ea2f-121">U kunt uit de volgende afschrijvingsmethoden kiezen.</span><span class="sxs-lookup"><span data-stu-id="1ea2f-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="1ea2f-122">Levensduur lineaire</span><span class="sxs-lookup"><span data-stu-id="1ea2f-122">Straight line service life</span></span>
-   <span data-ttu-id="1ea2f-123">Degressief</span><span class="sxs-lookup"><span data-stu-id="1ea2f-123">Reducing balance</span></span>
-   <span data-ttu-id="1ea2f-124">Handmatig</span><span class="sxs-lookup"><span data-stu-id="1ea2f-124">Manual</span></span>
-   <span data-ttu-id="1ea2f-125">Factor</span><span class="sxs-lookup"><span data-stu-id="1ea2f-125">Factor</span></span>
-   <span data-ttu-id="1ea2f-126">Verbruik</span><span class="sxs-lookup"><span data-stu-id="1ea2f-126">Consumption</span></span>
-   <span data-ttu-id="1ea2f-127">Resterende levensduur lineaire</span><span class="sxs-lookup"><span data-stu-id="1ea2f-127">Straight line life remaining</span></span>
-   <span data-ttu-id="1ea2f-128">200% degressief</span><span class="sxs-lookup"><span data-stu-id="1ea2f-128">200% reducing balance</span></span>
-   <span data-ttu-id="1ea2f-129">175% degressief</span><span class="sxs-lookup"><span data-stu-id="1ea2f-129">175% reducing balance</span></span>
-   <span data-ttu-id="1ea2f-130">150% degressief</span><span class="sxs-lookup"><span data-stu-id="1ea2f-130">150% reducing balance</span></span>
-   <span data-ttu-id="1ea2f-131">125% degressief</span><span class="sxs-lookup"><span data-stu-id="1ea2f-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="1ea2f-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1ea2f-132">Additional resources</span></span>
--------

[<span data-ttu-id="1ea2f-133">Afschrijving vaste activa</span><span class="sxs-lookup"><span data-stu-id="1ea2f-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="1ea2f-134">Lineaire afschrijving van levensduur</span><span class="sxs-lookup"><span data-stu-id="1ea2f-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="1ea2f-135">Degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="1ea2f-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="1ea2f-136">Handmatige afschrijving</span><span class="sxs-lookup"><span data-stu-id="1ea2f-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="1ea2f-137">Factorafschrijving</span><span class="sxs-lookup"><span data-stu-id="1ea2f-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="1ea2f-138">Afschrijving naar rato van verbruik</span><span class="sxs-lookup"><span data-stu-id="1ea2f-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="1ea2f-139">Lineaire afschrijving restlevensduur</span><span class="sxs-lookup"><span data-stu-id="1ea2f-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="1ea2f-140">Degressieve afschrijving van 125 procent</span><span class="sxs-lookup"><span data-stu-id="1ea2f-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="1ea2f-141">Degressieve afschrijving van 150 procent</span><span class="sxs-lookup"><span data-stu-id="1ea2f-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="1ea2f-142">Degressieve afschrijving van 175 procent</span><span class="sxs-lookup"><span data-stu-id="1ea2f-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="1ea2f-143">Degressieve afschrijving van 200 procent</span><span class="sxs-lookup"><span data-stu-id="1ea2f-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)




