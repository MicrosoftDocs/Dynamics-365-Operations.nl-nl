---
title: 'Activiteitsrelatie maken: opvolgende activiteit'
description: De stroom van activiteiten in lean productiestroom wordt gedocumenteerd door middel van activiteitsrelaties.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f10ecb8e579975327440ede6ea383226645c8cf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255296"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="e1da2-103">Activiteitsrelatie maken: opvolgende activiteit</span><span class="sxs-lookup"><span data-stu-id="e1da2-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1da2-104">De stroom van activiteiten in lean productiestroom wordt gedocumenteerd door middel van activiteitsrelaties.</span><span class="sxs-lookup"><span data-stu-id="e1da2-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="e1da2-105">Deze registratie toont aan hoe een activiteitsrelatie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1da2-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="e1da2-106">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="e1da2-106">Prerequisites:</span></span>

- <span data-ttu-id="e1da2-107">Een productiestroom en versie in conceptmodus.</span><span class="sxs-lookup"><span data-stu-id="e1da2-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="e1da2-108">Twee activiteiten die elkaar opvolgen in de productiestroom worden gemaakt maar zijn niet gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="e1da2-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="e1da2-109">De productiestroomversie vinden</span><span class="sxs-lookup"><span data-stu-id="e1da2-109">Find the production flow version</span></span> 
1. <span data-ttu-id="e1da2-110">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="e1da2-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="e1da2-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1da2-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e1da2-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1da2-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e1da2-113">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1da2-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e1da2-114">Selecteer een conceptversie in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1da2-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="e1da2-115">Activiteitsrelaties kunnen worden toegevoegd aan zowel conceptversies of actieve versies van een productiestroom.</span><span class="sxs-lookup"><span data-stu-id="e1da2-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="e1da2-116">Het overzicht van activiteiten openen</span><span class="sxs-lookup"><span data-stu-id="e1da2-116">Open the activity overview</span></span>
1. <span data-ttu-id="e1da2-117">Klik op Activiteiten.</span><span class="sxs-lookup"><span data-stu-id="e1da2-117">Click Activities.</span></span>
    * <span data-ttu-id="e1da2-118">Het formulier geeft alle activiteiten van de productiestroom weer die zijn toegewezen aan de Versie van de productiestromen waarin u werkt.</span><span class="sxs-lookup"><span data-stu-id="e1da2-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="e1da2-119">Een opvolgende activiteit toevoegen</span><span class="sxs-lookup"><span data-stu-id="e1da2-119">Add a Successor</span></span>
1. <span data-ttu-id="e1da2-120">Klik op Opvolgende activiteit.</span><span class="sxs-lookup"><span data-stu-id="e1da2-120">Click Add successor.</span></span>
2. <span data-ttu-id="e1da2-121">Klik in het veld Activiteit op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e1da2-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e1da2-122">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e1da2-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e1da2-123">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1da2-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e1da2-124">Schakel het selectievakje Beperking in.</span><span class="sxs-lookup"><span data-stu-id="e1da2-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="e1da2-125">Voer in het veld Waarde van beperking een waarde in.</span><span class="sxs-lookup"><span data-stu-id="e1da2-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="e1da2-126">De beperkingtijd is de tijd die moet worden gepland tussen het geplande einde van de voorafgaande activiteit (vervaldatum en tijd) en het geplande begin van de opvolgende activiteit.</span><span class="sxs-lookup"><span data-stu-id="e1da2-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="e1da2-127">Typ een waarde in het veld Eenheden.</span><span class="sxs-lookup"><span data-stu-id="e1da2-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="e1da2-128">Voer in het veld Cyclusduurverhouding een nummer in.</span><span class="sxs-lookup"><span data-stu-id="e1da2-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="e1da2-129">Als beide activiteiten met dezelfde snelheid worden uitgevoerd, moet de cyclusduurverhouding 1 zijn.</span><span class="sxs-lookup"><span data-stu-id="e1da2-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="e1da2-130">Als de voorgaande taak twee keer zo snel wordt uitgevoerd als de opvolgende taak, moet de verhouding 2 zijn.</span><span class="sxs-lookup"><span data-stu-id="e1da2-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="e1da2-131">De cyclusduurverhouding wordt gebruikt om de afzonderlijke cyclustijden te berekenen voor activiteiten van de productiestroom.</span><span class="sxs-lookup"><span data-stu-id="e1da2-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="e1da2-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e1da2-132">Click OK.</span></span>
10. <span data-ttu-id="e1da2-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1da2-133">Close the page.</span></span>
11. <span data-ttu-id="e1da2-134">Klik op het tabblad Rasterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="e1da2-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="e1da2-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1da2-135">Close the page.</span></span>
13. <span data-ttu-id="e1da2-136">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="e1da2-136">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]