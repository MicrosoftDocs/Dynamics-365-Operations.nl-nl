---
title: Resultaten vragenlijst analyseren
description: Vragenlijststatistieken kunnen worden gebruikt voor het berekenen van gemiddelden, totalen en percentages op basis van een set demografische gegevens.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8f9c2fcf0be117f8fcde5113c0d42f11786679
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177275"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="03294-103">Resultaten vragenlijst analyseren</span><span class="sxs-lookup"><span data-stu-id="03294-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03294-104">Vragenlijststatistieken kunnen worden gebruikt voor het berekenen van gemiddelden, totalen en percentages op basis van een set demografische gegevens.</span><span class="sxs-lookup"><span data-stu-id="03294-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="03294-105">Begin met deze procedure door naar Vragenlijst > Resultaten weergeven en analyseren > Vragenlijststatistieken te gaan.</span><span class="sxs-lookup"><span data-stu-id="03294-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="03294-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="03294-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="03294-107">Een record voor vragenlijststatistieken maken</span><span class="sxs-lookup"><span data-stu-id="03294-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="03294-108">Ga naar Vragenlijststatistieken.</span><span class="sxs-lookup"><span data-stu-id="03294-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="03294-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="03294-109">Click New.</span></span>
3. <span data-ttu-id="03294-110">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="03294-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="03294-111">Typ een waarde in het veld Statistieken.</span><span class="sxs-lookup"><span data-stu-id="03294-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="03294-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="03294-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="03294-113">Klik in het veld Vragenlijst op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="03294-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="03294-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="03294-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="03294-115">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="03294-115">Click the General tab.</span></span>
    * <span data-ttu-id="03294-116">Selecteer of u anonieme resultaten of resultaten van werknemers, contactpersonen en sollicitanten wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="03294-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="03294-117">Schakel het selectievakje Werknemer in of uit.</span><span class="sxs-lookup"><span data-stu-id="03294-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="03294-118">Als u de resultaten gaat bekijken op anciënniteit of leeftijd, geeft u de intervallen op die u wilt gebruiken voor het groeperen van de resultaten.</span><span class="sxs-lookup"><span data-stu-id="03294-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="03294-119">Als u een 5 invoert voor het ouderdomsinterval worden de resultaten gegroepeerd op basis van ouderdomsintervallen van vijf jaar.</span><span class="sxs-lookup"><span data-stu-id="03294-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="03294-120">Voer een getal in het veld Leeftijd in.</span><span class="sxs-lookup"><span data-stu-id="03294-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="03294-121">Selecteer of u de berekening wilt uitvoeren voor de hele vragenlijst, voor elke resultaatgroep, voor elke vraag of voor elke vraagrij.</span><span class="sxs-lookup"><span data-stu-id="03294-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="03294-122">Selecteer hoe u de resultaten wilt groeperen.</span><span class="sxs-lookup"><span data-stu-id="03294-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="03294-123">Als u bijvoorbeeld het gemiddelde aantal punten per vraag berekent, wilt u wellicht de vragen gegroepeerd zien per resultaatgroep.</span><span class="sxs-lookup"><span data-stu-id="03294-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="03294-124">Selecteer de gegevens waarop u de berekening wilt baseren.</span><span class="sxs-lookup"><span data-stu-id="03294-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="03294-125">Als u bijvoorbeeld het gemiddelde ontvangen percentage in de vragenlijst voor uw werknemers wilt afzetten tegen het gemiddelde aantal behaalde punten voor al uw werknemers.</span><span class="sxs-lookup"><span data-stu-id="03294-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="03294-126">Klik op het tabblad Bereik.</span><span class="sxs-lookup"><span data-stu-id="03294-126">Click the Range tab.</span></span>
    * <span data-ttu-id="03294-127">Gebruik bereiken om uw resultaatset te beperken tot alleen de gegevens die aan de bereikcriteria voldoen.</span><span class="sxs-lookup"><span data-stu-id="03294-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="03294-128">Klik op het tabblad Groeperen op.</span><span class="sxs-lookup"><span data-stu-id="03294-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="03294-129">Gebruik Groeperingen om te bepalen hoe de resultaten moeten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="03294-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="03294-130">Groepeer bijvoorbeeld eerst de resultaten op geslacht en vervolgens op ouderdom.</span><span class="sxs-lookup"><span data-stu-id="03294-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="03294-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="03294-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="03294-132">Verplaats de groeperingen naar de kant Geselecteerd en plaats ze in de gewenste volgorde.</span><span class="sxs-lookup"><span data-stu-id="03294-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="03294-133">De statistieken berekenen</span><span class="sxs-lookup"><span data-stu-id="03294-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="03294-134">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="03294-134">Click Execute.</span></span>
    * <span data-ttu-id="03294-135">Selecteer welke berekeningsfunctie u wilt uitvoeren op de resultaten.</span><span class="sxs-lookup"><span data-stu-id="03294-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="03294-136">Bereken bijvoorbeeld de gemiddelde percentages in de hele vragenlijst voor de geselecteerde groeperingen of tel het totale aantal punten van de resultaatgroepen voor de geselecteerde groeperingen bij elkaar op.</span><span class="sxs-lookup"><span data-stu-id="03294-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="03294-137">Schakel het selectievakje Vorige zoekopdrachten verwijderen in of uit.</span><span class="sxs-lookup"><span data-stu-id="03294-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="03294-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="03294-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="03294-139">Bekijk de resultaten van de uitvoering van de vragenlijststatistieken.</span><span class="sxs-lookup"><span data-stu-id="03294-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="03294-140">Klik op Resultaat.</span><span class="sxs-lookup"><span data-stu-id="03294-140">Click Result.</span></span>
2. <span data-ttu-id="03294-141">Klik op Resultaat.</span><span class="sxs-lookup"><span data-stu-id="03294-141">Click Result.</span></span>
3. <span data-ttu-id="03294-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03294-142">Close the page.</span></span>
