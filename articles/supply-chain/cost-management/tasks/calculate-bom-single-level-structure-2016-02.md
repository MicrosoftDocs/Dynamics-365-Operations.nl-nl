--- 
title: Een stuklijst berekenen met behulp van een structuur met een enkel niveau (uitsluitend februari 2016)
description: Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op een enkel niveau, die is gebaseerd op de kostprijsberekening.
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0e6829238b244cc01b070fde6acdf37bdaeb9670
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a><span data-ttu-id="f391c-103">Een stuklijst berekenen met behulp van een structuur met een enkel niveau (uitsluitend februari 2016)</span><span class="sxs-lookup"><span data-stu-id="f391c-103">Calculate a BOM by using a single level structure (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f391c-104">Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op een enkel niveau, die is gebaseerd op de kostprijsberekening.</span><span class="sxs-lookup"><span data-stu-id="f391c-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="f391c-105">Dit is de zesde taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f391c-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="f391c-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f391c-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f391c-107">Ga naar Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="f391c-107">Go to Released products.</span></span>
2. <span data-ttu-id="f391c-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f391c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f391c-109">Selecteer het product Stuklijst_1.</span><span class="sxs-lookup"><span data-stu-id="f391c-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="f391c-110">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="f391c-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="f391c-111">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="f391c-111">Click Item price.</span></span>
5. <span data-ttu-id="f391c-112">Klik op Artikelkosten berekenen.</span><span class="sxs-lookup"><span data-stu-id="f391c-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="f391c-113">Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.</span><span class="sxs-lookup"><span data-stu-id="f391c-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="f391c-114">Klik in het veld Kostprijsberekeningsversie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f391c-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f391c-115">Selecteer voor deze demonstratie 10.</span><span class="sxs-lookup"><span data-stu-id="f391c-115">For this demo, select 10.</span></span> <span data-ttu-id="f391c-116">Dit is de dezelfde kostprijsberekeningsversie die is gebruikt om de kostprijs aan de onderdelen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="f391c-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="f391c-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f391c-117">Click OK.</span></span>
8. <span data-ttu-id="f391c-118">Klik op Berekeningsdetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="f391c-118">Click View calculation details.</span></span>
    * <span data-ttu-id="f391c-119">Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.</span><span class="sxs-lookup"><span data-stu-id="f391c-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="f391c-120">Zo zijn de kosten samengesteld: • 10 is afgeleid van ITEM_A, 10 van ITEM_B, 10 van BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f391c-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="f391c-121">In dit geval zijn er geen details voor Artikel_2, omdat deze is ingevoerd als een standaardkostprijs van 10, maar niet is verkregen door berekening.</span><span class="sxs-lookup"><span data-stu-id="f391c-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="f391c-122">•  7 is afgeleid van de insteltijd, die een constante kostenfactor is, en nog eens 7 is afgeleid van de uitvoeringstijdbewerking (Proces).</span><span class="sxs-lookup"><span data-stu-id="f391c-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="f391c-123">•  Daarnaast zijn er nog andere bedragen, die met de indirecte kosten overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="f391c-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


