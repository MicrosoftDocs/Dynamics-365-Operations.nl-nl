--- 
title: "Kanbanschemagroepen definiëren"
description: Kanbanschemagroepen zijn gedefinieerd om producten te groeperen en te onderscheiden in kanbanplanning.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e07fa270b47be3527c572dc53ca30a7bcde5ba6
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="6ce98-103">Kanbanschemagroepen definiëren</span><span class="sxs-lookup"><span data-stu-id="6ce98-103">Define lean schedule groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ce98-104">Kanbanschemagroepen zijn gedefinieerd om producten te groeperen en te onderscheiden in kanbanplanning.</span><span class="sxs-lookup"><span data-stu-id="6ce98-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="6ce98-105">Het groeperen kan als algemene koppeling per bedrijf of specifiek voor een werkcel worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6ce98-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="6ce98-106">Elke groep heeft een kleurencode voor grafische indicatie in de lijstpagina van kanbanplanning.</span><span class="sxs-lookup"><span data-stu-id="6ce98-106">Each group has a color code assigned for visual indication in the kanban scheduling list page.</span></span> <span data-ttu-id="6ce98-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="6ce98-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="6ce98-108">Kanbanschemagroep definiëren</span><span class="sxs-lookup"><span data-stu-id="6ce98-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="6ce98-109">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanschemagroepen.</span><span class="sxs-lookup"><span data-stu-id="6ce98-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="6ce98-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6ce98-110">Click New.</span></span>
3. <span data-ttu-id="6ce98-111">Typ een waarde in het veld Planningsgroep.</span><span class="sxs-lookup"><span data-stu-id="6ce98-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="6ce98-112">Een planningsgroep kan worden gedefinieerd als globale groep of specifiek voor een werkcel.</span><span class="sxs-lookup"><span data-stu-id="6ce98-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="6ce98-113">In dit eenvoudige voorbeeld definiëren we een globale groep en blijft de werkcel leeg.</span><span class="sxs-lookup"><span data-stu-id="6ce98-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="6ce98-114">De instellingen van deze groep zijn van toepassing op alle werkcellen die geen specifieke planningsgroepen hebben.</span><span class="sxs-lookup"><span data-stu-id="6ce98-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="6ce98-115">Selecteer een kleur uit de kleurselectie.</span><span class="sxs-lookup"><span data-stu-id="6ce98-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="6ce98-116">De kleuren worden gebruikt om de taken te markeren in de lijstpagina van de kanbanplanning of het bord van het kanbanproces.</span><span class="sxs-lookup"><span data-stu-id="6ce98-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="6ce98-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ce98-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6ce98-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ce98-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="6ce98-119">Product koppelen</span><span class="sxs-lookup"><span data-stu-id="6ce98-119">Associate product</span></span>
1. <span data-ttu-id="6ce98-120">Een specifiek product koppelen</span><span class="sxs-lookup"><span data-stu-id="6ce98-120">Associate a specific product</span></span>
    * <span data-ttu-id="6ce98-121">Er zijn twee manieren om producten aan lean planningsgroepen te koppelen: als een specifiek product (type artikelrelatie = Artikel) of als onderdeel van een artikeltoewijzingssleutel (type artikelrelatie = groep).</span><span class="sxs-lookup"><span data-stu-id="6ce98-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="6ce98-122">Selecteer Artikel in het veld Type artikelrelatie.</span><span class="sxs-lookup"><span data-stu-id="6ce98-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="6ce98-123">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="6ce98-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="6ce98-124">Typ een nummer in het veld Doorvoerverhouding.</span><span class="sxs-lookup"><span data-stu-id="6ce98-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="6ce98-125">De standaarddoorvoerverhouding is 1, wat wil dat zeggen dat de gerelateerde producten precies de capaciteit verbruiken die is opgegeven in de procesactiviteiten van de productiestromen.</span><span class="sxs-lookup"><span data-stu-id="6ce98-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activities of the production flows.</span></span> <span data-ttu-id="6ce98-126">Doorvoerverhouding > 1 bepaalt een hoger resourceverbruik, doorvoerverhouding < 1 definieert een lager resourceverbruik.</span><span class="sxs-lookup"><span data-stu-id="6ce98-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="6ce98-127">De verhouding wordt gebruikt in de kostprijsberekening en in de berekening van het kanbantaakverbruik.</span><span class="sxs-lookup"><span data-stu-id="6ce98-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="6ce98-128">Artikeltoewijzingssleutel koppelen</span><span class="sxs-lookup"><span data-stu-id="6ce98-128">Associate item allocation key</span></span>
1. <span data-ttu-id="6ce98-129">Een artikeltoewijzingssleutel koppelen</span><span class="sxs-lookup"><span data-stu-id="6ce98-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="6ce98-130">Voeg een koppeling toe aan een artikeltoewijzingssleutel door het type artikelrelatie Groep te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6ce98-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="6ce98-131">Voor dit proces moet u een artikeltoewijzingssleutel voor prognoses in uw gegevens hebben gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="6ce98-131">Note that for this process, you need a forecast item allocation key defined in your data.</span></span>  
2. <span data-ttu-id="6ce98-132">Selecteer Groep in het veld Type artikelrelatie.</span><span class="sxs-lookup"><span data-stu-id="6ce98-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="6ce98-133">Klik in het veld Artikeltoewijzingssleutel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6ce98-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6ce98-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6ce98-134">In the list, click the link in the selected row.</span></span>


