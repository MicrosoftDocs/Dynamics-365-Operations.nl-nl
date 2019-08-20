---
title: Een voorafgaande taak toevoegen aan een productiestroomactiviteit
description: In een productiestroomversie moeten alle activiteiten worden gerangschikt.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 346dca110fde9ff7600f3e4606529c27289dfc97
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838770"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="f477e-103">Een voorafgaande taak toevoegen aan een productiestroomactiviteit</span><span class="sxs-lookup"><span data-stu-id="f477e-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f477e-104">In een productiestroomversie moeten alle activiteiten worden gerangschikt.</span><span class="sxs-lookup"><span data-stu-id="f477e-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="f477e-105">Een activiteit kan een of meerdere voorafgaande taken of opvolgende taken hebben.</span><span class="sxs-lookup"><span data-stu-id="f477e-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="f477e-106">Deze procedure laat zien hoe u een voorafgaande taak aan een activiteit koppelt.</span><span class="sxs-lookup"><span data-stu-id="f477e-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="f477e-107">Voor deze taak hebt u een productiestroom nodig met de Conceptversie waaraan minimaal twee activiteiten kunnen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f477e-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="f477e-108">Zie voor meer informatie de whitepaper "Production flows and activities in lean manufacturing".</span><span class="sxs-lookup"><span data-stu-id="f477e-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="f477e-109">De productiestroom en versie vinden</span><span class="sxs-lookup"><span data-stu-id="f477e-109">Find the production flow and version</span></span>
1. <span data-ttu-id="f477e-110">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="f477e-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f477e-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f477e-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f477e-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f477e-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f477e-113">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f477e-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f477e-114">Klik op Activiteiten.</span><span class="sxs-lookup"><span data-stu-id="f477e-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="f477e-115">Een activiteit selecteren en een voorafgaande taak toevoegen</span><span class="sxs-lookup"><span data-stu-id="f477e-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="f477e-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f477e-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f477e-117">Klik op Voorafgaande taak toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f477e-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="f477e-118">Typ of selecteer een waarde in het veld Activiteit.</span><span class="sxs-lookup"><span data-stu-id="f477e-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="f477e-119">Voer in het veld Cyclusduurverhouding een nummer in.</span><span class="sxs-lookup"><span data-stu-id="f477e-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="f477e-120">De standaard cyclusduurverhouding van een activiteitrelatie is 1.</span><span class="sxs-lookup"><span data-stu-id="f477e-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="f477e-121">Hierbij wordt ervan uitgegaan dat beide activiteiten op dezelfde snelheid of takttijd worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f477e-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="f477e-122">Als de voorafgaande taak met een hoger tempo (lagere takttijd) wordt uitgevoerd, moet de verhouding lager zijn dan 1. Als de voorafgaande taak met een langzamer tempo (hogere takttijd) wordt uitgevoerd, is de cyclusduurverhouding groter is dan 1.</span><span class="sxs-lookup"><span data-stu-id="f477e-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="f477e-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f477e-123">Click OK.</span></span>

