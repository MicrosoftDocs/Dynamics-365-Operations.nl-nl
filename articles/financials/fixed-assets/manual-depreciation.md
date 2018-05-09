---
title: Handmatige afschrijving
description: Dit artikel biedt een overzicht van de methode voor handmatige afschrijving.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0bef7a0b74b4dc671cc926ed247268c9b1f1d755
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="manual-depreciation"></a><span data-ttu-id="b9d57-103">Handmatige afschrijving</span><span class="sxs-lookup"><span data-stu-id="b9d57-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9d57-104">Dit artikel biedt een overzicht van de methode voor handmatige afschrijving.</span><span class="sxs-lookup"><span data-stu-id="b9d57-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="b9d57-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en **Handmatig** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, wordt de afschrijving van vaste activa die aan het afschrijvingsprofiel zijn toegewezen, bepaald door het percentage dat u opgeeft voor elk interval in het kalenderjaar.</span><span class="sxs-lookup"><span data-stu-id="b9d57-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="b9d57-106">De intervallen waarvoor u percentages instelt, worden geboekt volgens de waarde die u selecteert in het veld **Periodefrequentie** op het sneltabblad **Algemeen** van de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b9d57-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="b9d57-107">U kunt kiezen uit de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="b9d57-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="b9d57-108">Jaarlijks</span><span class="sxs-lookup"><span data-stu-id="b9d57-108">Yearly</span></span>
-   <span data-ttu-id="b9d57-109">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="b9d57-109">Monthly</span></span>
-   <span data-ttu-id="b9d57-110">Per kwartaal</span><span class="sxs-lookup"><span data-stu-id="b9d57-110">Quarterly</span></span>
-   <span data-ttu-id="b9d57-111">Zesmaandelijks</span><span class="sxs-lookup"><span data-stu-id="b9d57-111">Half-Yearly</span></span>
-   <span data-ttu-id="b9d57-112">Dagelijks</span><span class="sxs-lookup"><span data-stu-id="b9d57-112">Daily</span></span>

<span data-ttu-id="b9d57-113">Nadat u een periodefrequentie hebt geselecteerd, klikt u op **Handmatige schema's** en stelt u percentages in voor elk van de boekingsintervallen.</span><span class="sxs-lookup"><span data-stu-id="b9d57-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="b9d57-114">Het afschrijvingsbedrag wordt door de combinatie van handmatige schema's en de boekingsintervallen gedefinieerd, zoals in de voorbeelden verderop in dit artikel wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="b9d57-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="b9d57-115">De handmatige afschrijving wordt altijd berekend als een percentage van de aanschafprijs.</span><span class="sxs-lookup"><span data-stu-id="b9d57-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="b9d57-116">Voor handmatige afschrijving hoeven de percentages die u invoert in de intervallen van de afschrijving niet samen 100 procent te zijn.</span><span class="sxs-lookup"><span data-stu-id="b9d57-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="b9d57-117">Handmatige afschrijving is een flexibele afschrijvingsmethode, die vaak wordt gebruikt om een buitengewoon afschrijvingsprofiel te definiëren op de pagina **Boeken**, zoals een niet-periodieke afschrijving voor speciale doeleinden (bijvoorbeeld belastingen).</span><span class="sxs-lookup"><span data-stu-id="b9d57-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="b9d57-118">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="b9d57-118">Examples</span></span>
<span data-ttu-id="b9d57-119">Aanschafprijs: 11.000.00 Verwachte restwaarde: 1.000,00 In de volgende tabel worden de intervallen en percentages weergeven die u instelt op de pagina **Schema's afschrijvingsprofiel vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="b9d57-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="b9d57-120">Intervalnummer</span><span class="sxs-lookup"><span data-stu-id="b9d57-120">Interval number</span></span> | <span data-ttu-id="b9d57-121">Percentage</span><span class="sxs-lookup"><span data-stu-id="b9d57-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="b9d57-122">1</span><span class="sxs-lookup"><span data-stu-id="b9d57-122">1</span></span>               | <span data-ttu-id="b9d57-123">10,00</span><span class="sxs-lookup"><span data-stu-id="b9d57-123">10.00</span></span>      |
| <span data-ttu-id="b9d57-124">2</span><span class="sxs-lookup"><span data-stu-id="b9d57-124">2</span></span>               | <span data-ttu-id="b9d57-125">50,00</span><span class="sxs-lookup"><span data-stu-id="b9d57-125">50.00</span></span>      |
| <span data-ttu-id="b9d57-126">3</span><span class="sxs-lookup"><span data-stu-id="b9d57-126">3</span></span>               | <span data-ttu-id="b9d57-127">8,00</span><span class="sxs-lookup"><span data-stu-id="b9d57-127">8.00</span></span>       |

<span data-ttu-id="b9d57-128">In de volgende tabel ziet u hoe de afschrijving voor alle intervallen wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b9d57-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="b9d57-129">Intervalnummer</span><span class="sxs-lookup"><span data-stu-id="b9d57-129">Interval number</span></span> | <span data-ttu-id="b9d57-130">Berekening van het jaarlijkse afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="b9d57-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="b9d57-131">Nettoboekwaarde aan het einde van het interval</span><span class="sxs-lookup"><span data-stu-id="b9d57-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b9d57-132">1</span><span class="sxs-lookup"><span data-stu-id="b9d57-132">1</span></span>                | <span data-ttu-id="b9d57-133">(11.000 – 1.000) × 10% = 1.000</span><span class="sxs-lookup"><span data-stu-id="b9d57-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="b9d57-134">10.000 (11.000 – 1.000)</span><span class="sxs-lookup"><span data-stu-id="b9d57-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="b9d57-135">2</span><span class="sxs-lookup"><span data-stu-id="b9d57-135">2</span></span>                | <span data-ttu-id="b9d57-136">(11.000 – 1.000) × 50% = 5.000</span><span class="sxs-lookup"><span data-stu-id="b9d57-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="b9d57-137">5.000 (10.000 – 5.000)</span><span class="sxs-lookup"><span data-stu-id="b9d57-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="b9d57-138">3</span><span class="sxs-lookup"><span data-stu-id="b9d57-138">3</span></span>                | <span data-ttu-id="b9d57-139">(11.000 – 1.000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="b9d57-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="b9d57-140">4.200 (5.000 – 800)</span><span class="sxs-lookup"><span data-stu-id="b9d57-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="b9d57-141">Als u **Maandelijks** selecteert in het veld **Periodefrequentie**, moet u 12 handmatige planningsintervallen instellen.</span><span class="sxs-lookup"><span data-stu-id="b9d57-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="b9d57-142">In de volgende tabel ziet u de afschrijvingsbedragen voor de eerste twee intervallen.</span><span class="sxs-lookup"><span data-stu-id="b9d57-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="b9d57-143">Interval</span><span class="sxs-lookup"><span data-stu-id="b9d57-143">Interval</span></span> | <span data-ttu-id="b9d57-144">Afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="b9d57-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="b9d57-145">januari</span><span class="sxs-lookup"><span data-stu-id="b9d57-145">January</span></span>  | <span data-ttu-id="b9d57-146">(11.000 – 1.000) × 10% = 1.000</span><span class="sxs-lookup"><span data-stu-id="b9d57-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="b9d57-147">februari</span><span class="sxs-lookup"><span data-stu-id="b9d57-147">February</span></span> | <span data-ttu-id="b9d57-148">(11.000 – 1.000) × 50% = 5.000</span><span class="sxs-lookup"><span data-stu-id="b9d57-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="b9d57-149">Als u <strong>Zesmaandelijks</strong> selecteert in het veld *<strong><em>Periodefrequentie</em>*</strong>, stelt u twee handmatige planningsintervallen in.</span><span class="sxs-lookup"><span data-stu-id="b9d57-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="b9d57-150">In de volgende tabel ziet u de afschrijvingsbedragen voor deze twee intervallen.</span><span class="sxs-lookup"><span data-stu-id="b9d57-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="b9d57-151">Interval</span><span class="sxs-lookup"><span data-stu-id="b9d57-151">Interval</span></span>    | <span data-ttu-id="b9d57-152">Afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="b9d57-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="b9d57-153">30 juni</span><span class="sxs-lookup"><span data-stu-id="b9d57-153">June 30</span></span>     | <span data-ttu-id="b9d57-154">(11.000 – 1.000) × 10% = 1.000</span><span class="sxs-lookup"><span data-stu-id="b9d57-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="b9d57-155">31 december</span><span class="sxs-lookup"><span data-stu-id="b9d57-155">December 31</span></span> | <span data-ttu-id="b9d57-156">(11.000 – 1.000) × 50% = 5.000</span><span class="sxs-lookup"><span data-stu-id="b9d57-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="b9d57-157">Het totaal van de percentages voor alle intervallen hoeft niet gelijk te zijn aan 100.</span><span class="sxs-lookup"><span data-stu-id="b9d57-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="b9d57-158">U ontvangt echter een bericht als de waarde in het veld **Cumulatief percentage** op de pagina **Schema's afschrijvingsprofiel vaste activa** niet **100** is.</span><span class="sxs-lookup"><span data-stu-id="b9d57-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




