---
title: Bewerkingen voor niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u bewerkingen voor niet-conformeringen maakt en gebruikt.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956615"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="d0a2a-103">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0a2a-104">In dit onderwerp wordt beschreven hoe u bewerkingen voor niet-conformeringen maakt en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="d0a2a-105">U kunt de pagina **Bewerkingen** gebruiken om een classificaties te definiëren van het werk dat kan worden uitgevoerd voor een goedgekeurde niet-conformering.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="d0a2a-106">Wanneer u een gerelateerde bewerking toewijst aan een niet-conformering, kunt u details opgeven, zoals het bijbehorende materiaal, werkuren en diverse toeslagen die zijn vereist om de bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="d0a2a-107">Het systeem gebruikt deze informatie om een de geraamde kosten voor de bewerking te berekenen.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="d0a2a-108">De gedetailleerde informatie en de kostenraming dienen ter referentie.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="d0a2a-109">De gerelateerde bewerkingen voor kwaliteit verschillen van de bewerkingen die kunnen worden gedefinieerd voor een productieroute.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="d0a2a-110">Hoewel u kosten, tijd en artikelen kunt bijhouden die in een bewerking worden gebruikt die is gerelateerd aan een niet-conformering, zijn de gegevens die u invoert, alleen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="d0a2a-111">De gegevens worden niet automatisch geïntegreerd met het grootboek, het voorraadsubjournaal of de module **Tijd en aanwezigheid**.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="d0a2a-112">Voorbeelden van bewerkingen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-112">Examples of operations</span></span>

<span data-ttu-id="d0a2a-113">U werkt voor een productiebedrijf.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-113">You work for a manufacturing company.</span></span> <span data-ttu-id="d0a2a-114">Er is een niet-conformering gemaakt en goedgekeurd voor artikelen die niet zijn geslaagd voor een kwaliteitstest.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="d0a2a-115">Er is een correctie gemaakt om aan te geven dat het probleem te maken heeft met een slecht lager in een machine.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="d0a2a-116">Er zijn verscheidene stappen vereist om het lager te vervangen en de verantwoordelijkheid voor elke bewerking wordt bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="d0a2a-117">De volgende stappen kunnen bijvoorbeeld vereist zijn:</span><span class="sxs-lookup"><span data-stu-id="d0a2a-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="d0a2a-118">De productielijn wordt gestopt en de opschoonroutine wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="d0a2a-119">Onderhoudspersoneel vervangt het lager.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="d0a2a-120">Medewerkers van de kwaliteitsgarantie controleren de machine voordat deze weer wordt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="d0a2a-121">In dit voorbeeld kunnen de volgende bewerkingen worden gemaakt om het werk aan te geven dat moet worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="d0a2a-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="d0a2a-122">De productielijn stoppen.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-122">Stop the production line.</span></span>
- <span data-ttu-id="d0a2a-123">De productielijn opschonen.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-123">Clean out the production line.</span></span>
- <span data-ttu-id="d0a2a-124">Machineonderhoud uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="d0a2a-125">De machine inspecteren.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="d0a2a-126">Een bewerking maken</span><span class="sxs-lookup"><span data-stu-id="d0a2a-126">Create an operation</span></span>

1. <span data-ttu-id="d0a2a-127">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="d0a2a-128">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d0a2a-129">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="d0a2a-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d0a2a-130">**Bewerking**: Voer een unieke id of naam voor de bewerking in.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="d0a2a-131">**Beschrijving**: voer een gedetailleerde beschrijving van de bewerking in.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="d0a2a-132">**Type** als de bewerking alleen kan worden gebruikt voor niet-conformeringen die zijn gerelateerd aan een bepaald type order, selecteert u het ordertype (*Inkooporder* of *Verkooporder*).</span><span class="sxs-lookup"><span data-stu-id="d0a2a-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="d0a2a-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0a2a-134">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-134">Additional resources</span></span>

- [<span data-ttu-id="d0a2a-135">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="d0a2a-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="d0a2a-136">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="d0a2a-137">Niet-conformeringen maken en verwerken</span><span class="sxs-lookup"><span data-stu-id="d0a2a-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="d0a2a-138">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="d0a2a-139">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="d0a2a-140">Typen diagnosen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="d0a2a-141">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="d0a2a-142">Typen problemen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="d0a2a-143">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="d0a2a-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
