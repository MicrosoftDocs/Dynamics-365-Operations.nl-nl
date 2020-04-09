---
title: Suggesties voor kanbanhoeveelheid berekenen
description: Deze procedure is gericht op optimaliseren van de kanbangrootte en -hoeveelheden voor een specifieke kanbanregel door gebruik te maken van de berekening van de kanbanhoeveelheid.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6769eb1c971b4641aee7cae9dd710a856b3c8fb
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149361"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="456bc-103">Suggesties voor kanbanhoeveelheid berekenen</span><span class="sxs-lookup"><span data-stu-id="456bc-103">Calculate kanban quantity suggestions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="456bc-104">Deze procedure is gericht op optimaliseren van de kanbangrootte en -hoeveelheden voor een specifieke kanbanregel door gebruik te maken van de berekening van de kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="456bc-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="456bc-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="456bc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="456bc-106">Deze procedure is bedoeld voor de waardestroombeheerder.</span><span class="sxs-lookup"><span data-stu-id="456bc-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="456bc-107">Het is een vereiste dat u de procedure Een beleid voor berekening van de kanbanhoeveelheid toevoegen aan een kanbanregel hebt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="456bc-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="456bc-108">Een berekening van een kanbanhoeveelheid maken</span><span class="sxs-lookup"><span data-stu-id="456bc-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="456bc-109">Ga naar Productiebeheer > Periodieke taken > Berekening kanbanhoeveelheid > Kanbanhoeveelheid berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="456bc-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="456bc-110">Click New.</span></span>
3. <span data-ttu-id="456bc-111">Typ "Speaker2016" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="456bc-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="456bc-112">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="456bc-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="456bc-113">Selecteer het beleid dat u hebt gemaakt in de procedure Een beleid voor berekening van de kanbanhoeveelheid toevoegen aan een kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="456bc-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="456bc-114">Bijvoorbeeld Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="456bc-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="456bc-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="456bc-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="456bc-116">Stel in het veld "Regel actief vanaf datum" de datum en tijd in op "2012-12-17T08:00:00".</span><span class="sxs-lookup"><span data-stu-id="456bc-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="456bc-117">Deze datum dient als basis om te bepalen welke vaste kanbanregels in de kanbanberekening worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="456bc-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="456bc-118">Stel in het veld "Begindatum behaalde vraagperiode" de datum en tijd in op "2012-11-17T09:00:00".</span><span class="sxs-lookup"><span data-stu-id="456bc-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="456bc-119">De datum vanaf wanneer voorbije aanvraagtransacties worden opgenomen om de kanbanhoeveelheid te berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="456bc-120">Stel in het veld "Einddatum behaalde vraagperiode" de datum en tijd in op "2012-12-17T07:59:59".</span><span class="sxs-lookup"><span data-stu-id="456bc-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="456bc-121">De datum tot wanneer voorbije transacties worden opgenomen om de kanbanhoeveelheid te berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="456bc-122">Stel in het veld "Begindatum vraagperiode" de datum en tijd in op "2012-12-17T08:00:00".</span><span class="sxs-lookup"><span data-stu-id="456bc-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="456bc-123">De datum vanaf wanneer huidige vraagtransacties worden opgenomen om de kanbanhoeveelheid te berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="456bc-124">Stel in het veld "Einddatum vraagperiode" de datum en tijd in op "2013-01-16T07:59:59".</span><span class="sxs-lookup"><span data-stu-id="456bc-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="456bc-125">De datum tot wanneer huidige vraagtransacties worden opgenomen om de kanbanhoeveelheid te berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="456bc-126">Voorstel voor kanbanhoeveelheid genereren</span><span class="sxs-lookup"><span data-stu-id="456bc-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="456bc-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="456bc-127">Click Save.</span></span>
2. <span data-ttu-id="456bc-128">Klik op Genereren.</span><span class="sxs-lookup"><span data-stu-id="456bc-128">Click Generate.</span></span>
    * <span data-ttu-id="456bc-129">Hiermee wordt een voorstelregel voor de kanbanhoeveelheid gegenereerd voor kanbanregel 000020.</span><span class="sxs-lookup"><span data-stu-id="456bc-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="456bc-130">Berekening van kanbanhoeveelheid uitvoeren</span><span class="sxs-lookup"><span data-stu-id="456bc-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="456bc-131">Klik op Berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-131">Click Calculate.</span></span>
    * <span data-ttu-id="456bc-132">Hiermee wordt het voorstel voor de kanbanhoeveelheid berekend.</span><span class="sxs-lookup"><span data-stu-id="456bc-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="456bc-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="456bc-133">Click OK.</span></span>
3. <span data-ttu-id="456bc-134">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="456bc-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="456bc-135">De voorgestelde kanbanhoeveelheid is 2.</span><span class="sxs-lookup"><span data-stu-id="456bc-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="456bc-136">Producthoeveelheid wijzigen en opnieuw berekenen</span><span class="sxs-lookup"><span data-stu-id="456bc-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="456bc-137">Stel Producthoeveelheid in op "5".</span><span class="sxs-lookup"><span data-stu-id="456bc-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="456bc-138">Klik op Berekenen.</span><span class="sxs-lookup"><span data-stu-id="456bc-138">Click Calculate.</span></span>
3. <span data-ttu-id="456bc-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="456bc-139">Click OK.</span></span>
    * <span data-ttu-id="456bc-140">Merk op dat bij een kanbanhoeveelheid van 5, het voorstel wordt gewijzigd in een kanbanhoeveelheid van 4.</span><span class="sxs-lookup"><span data-stu-id="456bc-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="456bc-141">Dit wordt veroorzaakt door het feit dat er bij een lagere producthoeveelheid meer kanbans nodig zijn om aan de vraag te voldoen.</span><span class="sxs-lookup"><span data-stu-id="456bc-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="456bc-142">Kanbanregel bijwerken</span><span class="sxs-lookup"><span data-stu-id="456bc-142">Update kanban rule</span></span>
1. <span data-ttu-id="456bc-143">Voer in het veld Datum regel van kracht een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="456bc-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="456bc-144">Stel de datum bij "Regel actief vanaf datum" in op een datum in de toekomst.</span><span class="sxs-lookup"><span data-stu-id="456bc-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="456bc-145">Bijvoorbeeld, vandaag + één jaar.</span><span class="sxs-lookup"><span data-stu-id="456bc-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="456bc-146">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="456bc-146">Click Update.</span></span>
3. <span data-ttu-id="456bc-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="456bc-147">Click OK.</span></span>
4. <span data-ttu-id="456bc-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="456bc-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="456bc-149">Wijziging op kanbanregel valideren</span><span class="sxs-lookup"><span data-stu-id="456bc-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="456bc-150">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="456bc-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="456bc-151">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="456bc-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="456bc-152">Selecteer de kanbanregel die in de vorige deeltaak is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="456bc-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="456bc-153">Dit moet de eerste kanbanregel in de lijst zijn die is gesorteerd op nummer.</span><span class="sxs-lookup"><span data-stu-id="456bc-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="456bc-154">Schakel de uitbreiding van de sectie Details om.</span><span class="sxs-lookup"><span data-stu-id="456bc-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="456bc-155">Let op de ingangsdatum, die betekent dat deze regel niet vóór deze datum wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="456bc-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="456bc-156">Schakel de uitbreiding van de sectie Hoeveelheden om.</span><span class="sxs-lookup"><span data-stu-id="456bc-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="456bc-157">Merk op dit de standaardhoeveelheid is die u bij de berekening van de kanbanhoeveelheid hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="456bc-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="456bc-158">Merk op dit de vaste kanbanhoeveelheid van 4 is van de berekening van de kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="456bc-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="456bc-159">Klik op het tabblad Lijstpaneel.</span><span class="sxs-lookup"><span data-stu-id="456bc-159">Click the ListPanel tab.</span></span>

