---
title: Onderhoudsstatus
description: In dit onderwerp wordt uitgelegd hoe u de onderhoudsstatus berekent in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889572"
---
# <a name="maintenance-status"></a><span data-ttu-id="d1bb0-103">Onderhoudsstatus</span><span class="sxs-lookup"><span data-stu-id="d1bb0-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d1bb0-104">In Activabeheer kunt u een berekening uitvoeren om een overzicht weer te geven voor een specifieke periode van nieuwe, actieve en voltooide onderhoudsverzoeken, werkorders en activiteiten voor uitvaltijd voor onderhoud.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="d1bb0-105">U kunt ook het aantal voltooide evaluaties van voorwaarden voor dezelfde periode weergeven.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="d1bb0-106">Gebruik deze berekening om een overzicht te krijgen van de werkbelasting voor inkomende en voltooide onderhoudsverzoeken en werkorders.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="d1bb0-107">Een berekening van de onderhoudsstatus uitvoeren</span><span class="sxs-lookup"><span data-stu-id="d1bb0-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="d1bb0-108">Klik op **Activabeheer** > **Query's** > **Onderhoudsstatus**.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="d1bb0-109">Selecteer in het dialoogvenster **Status berekenen** in de velden **Begindatum** en **Einddatum** het periodebereik waarvoor u de berekening wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="d1bb0-110">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor onderhoud moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="d1bb0-111">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kan de status op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="d1bb0-112">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor onderhoud weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="d1bb0-113">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="d1bb0-114">Klik op de knoppen **Groeperen op** om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d1bb0-115">De geselecteerde knoppen **Groeperen op** worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="d1bb0-116">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="d1bb0-117">Klik op de knop **Bijwerken** om de berekening telkens bij te werken wanneer u wijzigingen aanbrengt door knoppen **Groeperen op** te activeren of te deactiveren of door een berekening voor een nieuwe periode uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="d1bb0-118">Klik op **Status** als u een nieuwe berekening van de onderhoudsstatus wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="d1bb0-119">De weergegeven resultaten in **Onderhoudsstatus** omvatten alleen onderhoudsverzoeken en werkorders met een werkelijke begindatum en -tijd.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="d1bb0-120">De einddatum en -tijd kunnen leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="d1bb0-121">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="d1bb0-121">Example 1</span></span>

<span data-ttu-id="d1bb0-122">In de volgende afbeelding zijn de knoppen **Jaar** en **Maand** geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="d1bb0-123">Als deze opties voor **Groeperen op** zijn geselecteerd, krijgt u een algemeen overzicht op maandelijkse basis van de werkbelasting en doorvoer met betrekking tot onderhoudsverzoeken en werkorders.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Voorbeeld van maandelijkse werkbelasting](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="d1bb0-125">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="d1bb0-125">Example 2</span></span>

<span data-ttu-id="d1bb0-126">In de volgende afbeelding is informatie over functionele locaties toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="d1bb0-127">Nu is het mogelijk om de werkbelasting en doorvoer te vergelijken tussen verschillende functionele locaties, die geografische locaties, fabrieken of werkgebieden kunnen voorstellen.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Voorbeeld van maandelijkse werkbelasting met functionele locaties](media/14-controlling-and-reporting.png)

