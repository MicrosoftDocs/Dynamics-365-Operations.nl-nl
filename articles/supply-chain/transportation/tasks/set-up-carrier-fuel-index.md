---
title: Brandstofindex van een vervoerder instellen
description: Deze guide laat zien hoe een regio voor de brandstofindex, een brandstofindex en een index van de vervoerder kan worden gemaakt.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44eda7ff8ddad881e32f7eef1ef4d9203449e19d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986669"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="411f8-103">Brandstofindex van een vervoerder instellen</span><span class="sxs-lookup"><span data-stu-id="411f8-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="411f8-104">Deze guide laat zien hoe een regio voor de brandstofindex, een brandstofindex en een index van de vervoerder kan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="411f8-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="411f8-105">De regio van de brandstofindex bepaalt in welke regio de brandstofindex moet worden toegepast en de brandstofindex geeft een brandstofprijs op voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="411f8-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="411f8-106">U kunt de wijziging in brandstofprijzen in de loop van de tijd weerspiegelen door meerdere brandstofindexen aan een vervoerder te koppelen.</span><span class="sxs-lookup"><span data-stu-id="411f8-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="411f8-107">Deze taken worden gewoonlijk uitgevoerd door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="411f8-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="411f8-108">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="411f8-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="411f8-109">Een brandstofindexregio maken</span><span class="sxs-lookup"><span data-stu-id="411f8-109">Create a fuel index region</span></span>
1. <span data-ttu-id="411f8-110">Ga naar Transportbeheer > Instellingen > Brandstofindexen > Brandstofindexregio's.</span><span class="sxs-lookup"><span data-stu-id="411f8-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="411f8-111">Eerst moet u de verschillende regio's maken waar u verschillende brandstoftoeslagen hanteert en berekent.</span><span class="sxs-lookup"><span data-stu-id="411f8-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="411f8-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="411f8-112">Click New.</span></span>
3. <span data-ttu-id="411f8-113">Typ een waarde in het veld Regio.</span><span class="sxs-lookup"><span data-stu-id="411f8-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="411f8-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="411f8-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="411f8-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="411f8-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="411f8-116">Maak een brandstofindex</span><span class="sxs-lookup"><span data-stu-id="411f8-116">Create a fuel index</span></span>
1. <span data-ttu-id="411f8-117">Ga naar Transportbeheer > Instellingen > Brandstofindexen > Brandstofindexen.</span><span class="sxs-lookup"><span data-stu-id="411f8-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="411f8-118">Voor de regio's die u hebt ingesteld moet u de huidige prijzen voor de brandstof invoeren.</span><span class="sxs-lookup"><span data-stu-id="411f8-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="411f8-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="411f8-119">Click New.</span></span>
3. <span data-ttu-id="411f8-120">Klik in het veld Regio op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="411f8-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="411f8-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="411f8-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="411f8-122">Typ een getal in het veld Prijs per gallon.</span><span class="sxs-lookup"><span data-stu-id="411f8-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="411f8-123">Typ een datum en tijd in het veld Ingangsdatum en -tijd.</span><span class="sxs-lookup"><span data-stu-id="411f8-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="411f8-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="411f8-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="411f8-125">Een brandstofindex voor de vervoerder maken</span><span class="sxs-lookup"><span data-stu-id="411f8-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="411f8-126">Ga naar Transportbeheer > Instellingen > Brandstofindexen > Brandstofindexen van vervoerder.</span><span class="sxs-lookup"><span data-stu-id="411f8-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="411f8-127">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="411f8-127">Click New.</span></span>
3. <span data-ttu-id="411f8-128">Typ een waarde in het veld Brandstofindex vervoerder.</span><span class="sxs-lookup"><span data-stu-id="411f8-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="411f8-129">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="411f8-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="411f8-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="411f8-130">Click New.</span></span>
6. <span data-ttu-id="411f8-131">Typ een datum en tijd in het veld Ingangsdatum en -tijd.</span><span class="sxs-lookup"><span data-stu-id="411f8-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="411f8-132">Typ een getal in het veld PPL van.</span><span class="sxs-lookup"><span data-stu-id="411f8-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="411f8-133">In dit voorbeeld kunt u het veld PPL van instellen op 1,95.</span><span class="sxs-lookup"><span data-stu-id="411f8-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="411f8-134">Typ een getal in het veld PPL tot.</span><span class="sxs-lookup"><span data-stu-id="411f8-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="411f8-135">In dit voorbeeld kunt u het veld PPL tot instellen op 2.</span><span class="sxs-lookup"><span data-stu-id="411f8-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="411f8-136">Voer een getal in het veld Percentage in.</span><span class="sxs-lookup"><span data-stu-id="411f8-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="411f8-137">In dit voorbeeld kunt u het percentage instellen op 3.</span><span class="sxs-lookup"><span data-stu-id="411f8-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="411f8-138">Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="411f8-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="411f8-139">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="411f8-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="411f8-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="411f8-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="411f8-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="411f8-141">Click Save.</span></span>

