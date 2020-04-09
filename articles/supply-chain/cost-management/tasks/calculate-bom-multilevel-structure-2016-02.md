---
title: Een stuklijst berekenen met behulp van een structuur met meerdere niveaus (februari 2016)
description: Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op meerdere niveaus, die is gebaseerd op de kostprijsberekening.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c35d2b2d5c0fdd14c7e0a35316d482b2e3ffb49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150424"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="4fe1b-103">Een stuklijst berekenen met behulp van een structuur met meerdere niveaus (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="4fe1b-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fe1b-104">Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op meerdere niveaus, die is gebaseerd op de kostprijsberekening.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="4fe1b-105">Dit is de zevende taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="4fe1b-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4fe1b-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4fe1b-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4fe1b-109">Selecteer het product Stuklijst_1.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="4fe1b-110">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="4fe1b-111">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-111">Click Item price.</span></span>
5. <span data-ttu-id="4fe1b-112">Klik op Artikelkosten berekenen.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="4fe1b-113">Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="4fe1b-114">Typ of selecteer een waarde in het veld Kostprijsberekeningsversie.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="4fe1b-115">Selecteer kostprijsberekening versie 20, omdat dit het type Geplande kosten is, met explosiemodus Meerdere niveaus.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="4fe1b-116">De explosiemodus voor meerdere niveaus is voor geplande kosten en simulaties.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="4fe1b-117">Hij wordt niet gebruikt voor de standaardkostprijzen.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="4fe1b-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-118">Click OK.</span></span>
8. <span data-ttu-id="4fe1b-119">Klik op Berekeningsdetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-119">Click View calculation details.</span></span>
    * <span data-ttu-id="4fe1b-120">Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="4fe1b-121">In dit geval ziet u hoe BOM_2 is berekend, rekening houdend met de grondstoffen, verwerking en overhead met een kostentotaal van 29,40, in plaats van de standaardkosten van 10 die in de eerste taakbegeleider in deze reeks was geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="4fe1b-122">Klik op het tabblad Kostprijsberekening.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="4fe1b-123">Als we verdergaan naar het tabblad Kostprijsberekening, zien we dat de totalen per kostengroep afwijken van de berekening die in de vorige taakbegeleider is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="4fe1b-124">Selecteer in het veld Niveau de waarde 'Meerdere'.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="4fe1b-125">Als u Meerdere niveaus kiest, worden de kosten ingedeeld volgens de samenstelling van Stuklijst_2, waarbij 10 is afgeleid van de kostengroep M1 (Artikel_C), en 15,60 is afgeleid van de productie, waarbij de kostengroep L2 is.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="4fe1b-126">De indirecte kosten zijn ook anders.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="4fe1b-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-127">Close the page.</span></span>
12. <span data-ttu-id="4fe1b-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4fe1b-128">Close the page.</span></span>

