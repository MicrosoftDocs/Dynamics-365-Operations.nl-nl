---
title: Vertragingstolerantie (negatieve dagen)
description: Dit onderwerp bevat informatie over de berekening van vertragingstolerantie en over het effect ervan op het maken van geplande orders in Planningsoptimalisatie.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306458"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="44605-103">Vertragingstolerantie (negatieve dagen)</span><span class="sxs-lookup"><span data-stu-id="44605-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="44605-104">Door de functionaliteit voor vertragingstolerantie kan in Planningsoptimalisatie rekening worden houden met de waarde voor **Negatieve dagen** die is ingesteld voor behoefteplanningsgroepen.</span><span class="sxs-lookup"><span data-stu-id="44605-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="44605-105">Deze wordt gebruikt om de vertragingstolerantieperiode te verlengen die wordt toegepast tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="44605-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="44605-106">Op deze manier voorkomt u dat u nieuwe aanvulorders maakt als het bestaande aanbod na korte tijd aan de vraag kan voldoen.</span><span class="sxs-lookup"><span data-stu-id="44605-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="44605-107">Het doel van de functionaliteit is te bepalen of het zin heeft om een nieuwe aanvulorder voor een bepaalde vraag te maken.</span><span class="sxs-lookup"><span data-stu-id="44605-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="44605-108">De functie inschakelen in uw systeem</span><span class="sxs-lookup"><span data-stu-id="44605-108">Turn on the feature in your system</span></span>

<span data-ttu-id="44605-109">Als u de functionaliteit voor vertragingstolerantie beschikbaar wilt maken in uw systeem, gaat u naar [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Negatieve dagen voor Planningsoptimalisatie* in.</span><span class="sxs-lookup"><span data-stu-id="44605-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="44605-110">Vertragingstolerantie in Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="44605-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="44605-111">Vertragingstolerantie is het aantal dagen na de levertijd die u wilt wachten voordat u nieuwe aanvulling bestelt wanneer een bestaand aanbod al is gepland.</span><span class="sxs-lookup"><span data-stu-id="44605-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="44605-112">Vertragingstolerantie wordt gedefinieerd met behulp van kalenderdagen, niet werkdagen.</span><span class="sxs-lookup"><span data-stu-id="44605-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="44605-113">Wanneer de vertragingstolerantie wordt berekend bij de hoofdplanning, wordt rekening gehouden met de instelling **Negatieve dagen**.</span><span class="sxs-lookup"><span data-stu-id="44605-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="44605-114">U kunt de **Negatieve dagen**-waarde opgeven op de pagina **Behoefteplanningsgroepen** of de pagina **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="44605-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="44605-115">De berekening van de vertragingstolerantie wordt door het systeem aan de *vroegste aanvullingsdatum* gekoppeld. Dit is gelijk aan de datum van vandaag plus de levertijd.</span><span class="sxs-lookup"><span data-stu-id="44605-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="44605-116">De vertragingstolerantie wordt berekend met behulp van de volgende formule, waarbij *max()* het grootste aantal waarden heeft gevonden:</span><span class="sxs-lookup"><span data-stu-id="44605-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="44605-117">*max(Vroegste aanvullingsdatum, Vervaldatum vraag)* – *Vervaldatum vraag* + *Negatieve dagen*</span><span class="sxs-lookup"><span data-stu-id="44605-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="44605-118">Met deze formule wordt gegarandeerd dat er door de hoofdplanning geen nieuwe aanvulorders worden gemaakt wanneer er voldoende aanbod bestaat tijdens de productlevertijd.</span><span class="sxs-lookup"><span data-stu-id="44605-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="44605-119">Bij de berekening van vertragingstolerantie in Planningsoptimalisatie wordt altijd de dynamische, berekening van negatieve dagen gebruikt op basis van de ingebouwde hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="44605-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="44605-120">De instelling **Dynamische, negatieve dagen gebruiken** op de pagina **Parameters hoofdplanning** heeft geen effect op dit gedrag.</span><span class="sxs-lookup"><span data-stu-id="44605-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="44605-121">Als het bestaande aanbod een uitgestelde vraag geeft die kleiner is dan of gelijk is aan de berekende vertragingstolerantie, zorgt Planningsoptimalisatie ervoor dat het bestaande aanbod aan de vraag wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="44605-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="44605-122">In sommige gevallen is het beter de vraag uit te stellen dan te eindigen met een overaanbod.</span><span class="sxs-lookup"><span data-stu-id="44605-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="44605-123">In de volgende subsecties staan voorbeelden die laten zien welke vertragingstolerantie van invloed is op het maken van geplande orders in Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="44605-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="44605-124">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="44605-124">Example 1</span></span>

<span data-ttu-id="44605-125">Een product heeft de volgende configuratie:</span><span class="sxs-lookup"><span data-stu-id="44605-125">A product has the following configuration:</span></span>

- <span data-ttu-id="44605-126">**Levertijd:** *10*</span><span class="sxs-lookup"><span data-stu-id="44605-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="44605-127">**Negatieve dagen:** *2*</span><span class="sxs-lookup"><span data-stu-id="44605-127">**Negative days:** *2*</span></span>

<span data-ttu-id="44605-128">De volgende vraag en aanbod bestaan voor het product:</span><span class="sxs-lookup"><span data-stu-id="44605-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="44605-129">**Vraag voor vandaag:** een verkooporder voor een hoeveelheid van 10</span><span class="sxs-lookup"><span data-stu-id="44605-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="44605-130">**Aanbod in 12 dagen:** een inkooporder voor een hoeveelheid van 10</span><span class="sxs-lookup"><span data-stu-id="44605-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="44605-131">Het bestaande aanbod kan binnen 12 dagen de vraag dekken en deze periode is gelijk aan de vertragingstolerantie.</span><span class="sxs-lookup"><span data-stu-id="44605-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="44605-132">Wanneer de hoofdplanning wordt uitgevoerd, worden er dus geen geplande orders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="44605-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="44605-133">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="44605-133">Example 2</span></span>

<span data-ttu-id="44605-134">Een product heeft de volgende configuratie:</span><span class="sxs-lookup"><span data-stu-id="44605-134">A product has the following configuration:</span></span>

- <span data-ttu-id="44605-135">**Levertijd:** *10*</span><span class="sxs-lookup"><span data-stu-id="44605-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="44605-136">**Negatieve dagen:** *0*</span><span class="sxs-lookup"><span data-stu-id="44605-136">**Negative days:** *0*</span></span>

<span data-ttu-id="44605-137">De volgende vraag en aanbod bestaan voor het product:</span><span class="sxs-lookup"><span data-stu-id="44605-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="44605-138">**Vraag voor vandaag:** een verkooporder voor een hoeveelheid van 10</span><span class="sxs-lookup"><span data-stu-id="44605-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="44605-139">**Aanbod in 12 dagen:** een inkooporder voor een hoeveelheid van 10</span><span class="sxs-lookup"><span data-stu-id="44605-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="44605-140">Bestaand aanbod kan de vraag pas na twaalf 12 dekken.</span><span class="sxs-lookup"><span data-stu-id="44605-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="44605-141">De vertragingstolerantie is echter 10 dagen.</span><span class="sxs-lookup"><span data-stu-id="44605-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="44605-142">Wanneer de hoofdplanning wordt uitgevoerd, wordt daarom een geplande order gemaakt voor een hoeveelheid van 10.</span><span class="sxs-lookup"><span data-stu-id="44605-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="44605-143">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="44605-143">Example 3</span></span>

<span data-ttu-id="44605-144">Een product heeft de volgende configuratie:</span><span class="sxs-lookup"><span data-stu-id="44605-144">A product has the following configuration:</span></span>

- <span data-ttu-id="44605-145">**Levertijd:** *10*</span><span class="sxs-lookup"><span data-stu-id="44605-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="44605-146">**Negatieve dagen:** *2*</span><span class="sxs-lookup"><span data-stu-id="44605-146">**Negative days:** *2*</span></span>

<span data-ttu-id="44605-147">De volgende vraag en aanbod bestaan voor het product:</span><span class="sxs-lookup"><span data-stu-id="44605-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="44605-148">**Vraag in 11 dagen:** een verkooporder voor een hoeveelheid van 10</span><span class="sxs-lookup"><span data-stu-id="44605-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="44605-149">**Aanbod in 14 dagen:** een inkooporder voor een hoeveelheid van 10</span><span class="sxs-lookup"><span data-stu-id="44605-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="44605-150">Bestaand aanbod kan de vraag pas na drie dagen dekken.</span><span class="sxs-lookup"><span data-stu-id="44605-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="44605-151">De vertragingstolerantie is echter twee dagen.</span><span class="sxs-lookup"><span data-stu-id="44605-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="44605-152">(In dit geval omvat de vertragingstolerantie alleen de twee negatieve dagen.</span><span class="sxs-lookup"><span data-stu-id="44605-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="44605-153">De vraagdatum wordt niet opgenomen omdat deze na de levertijd van het product is.) Wanneer de hoofdplanning wordt uitgevoerd, wordt een geplande order gemaakt voor een hoeveelheid van 10.</span><span class="sxs-lookup"><span data-stu-id="44605-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
