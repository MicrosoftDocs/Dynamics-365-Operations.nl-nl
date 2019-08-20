---
title: Voorraad in een magazijn tellen
description: In dit onderwerp wordt beschreven hoe u een voorraadtellingsjournaal maakt en boekt om een specifiek artikel op een locatie in het magazijn te tellen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0909625f31d15fe6b1387ff9ab7fd5d9a9135f4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836438"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="5ee42-103">Voorraad in een magazijn tellen</span><span class="sxs-lookup"><span data-stu-id="5ee42-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ee42-104">In dit onderwerp wordt beschreven hoe u een voorraadtellingsjournaal maakt en boekt om een specifiek artikel op een locatie in het magazijn te tellen.</span><span class="sxs-lookup"><span data-stu-id="5ee42-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="5ee42-105">De procedure is van toepassing op de functie 'basale magazijnen' die beschikbaar is in de module Voorraadbeheer, niet op de magazijnfunctionaliteit die beschikbaar is in de module magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="5ee42-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="5ee42-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5ee42-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="5ee42-107">Als u uw eigen gegevens gebruikt, moet u ervoor zorgen dat u producten en locaties hebt ingesteld en dat u een voorraadjournaalnaam voor tellingsjournalen hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5ee42-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="5ee42-108">Voorraadtelling wordt normaal uitgevoerd door een magazijnwerknemer.</span><span class="sxs-lookup"><span data-stu-id="5ee42-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="5ee42-109">Een voorraadtellingsjournaal maken</span><span class="sxs-lookup"><span data-stu-id="5ee42-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="5ee42-110">Ga naar **Navigatievenster > Modules > Voorraadbeheer > Journaalboekingen > Artikeltelling > Tellen**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="5ee42-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-111">Select **New**.</span></span>
3. <span data-ttu-id="5ee42-112">Selecteer in de vervolgkeuzelijst in het veld **Naam** de naam van het voorraadtellingsjournaal dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5ee42-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="5ee42-113">Enkele andere velden worden ingevuld op basis van de instellingen van de naam voor het standaardjournaal voor voorraadtelling die u selecteert.</span><span class="sxs-lookup"><span data-stu-id="5ee42-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="5ee42-114">Selecteer in het veld **Medewerker** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="5ee42-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5ee42-115">**Selecteer** in de lijst de medewerker die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5ee42-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="5ee42-116">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="5ee42-117">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="5ee42-117">Create journal lines</span></span>
1. <span data-ttu-id="5ee42-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-118">Select **New**.</span></span>
2. <span data-ttu-id="5ee42-119">Selecteer in het veld **Artikelnummer** de gewenste record in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="5ee42-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="5ee42-120">Als u het demobedrijf USMF gebruikt, selecteert u **A0001**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="5ee42-121">Selecteer in het veld **Vestiging** de gewenste record in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="5ee42-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="5ee42-122">Als u het demobedrijf USMF gebruikt, selecteert u site **2**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="5ee42-123">Selecteer in het veld **Magazijn** de gewenste record in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="5ee42-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="5ee42-124">Als u het demobedrijf USMF gebruikt, selecteert u magazijn **24**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="5ee42-125">Selecteer in het veld **Locatie** de gewenste record in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="5ee42-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="5ee42-126">Als u het demobedrijf USMF gebruikt, selecteert u locatie **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="5ee42-127">Voer in het veld Geteld een getal in.</span><span class="sxs-lookup"><span data-stu-id="5ee42-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="5ee42-128">Als u een geteld aantal invoert dat verschilt van de waarde die in het veld **Voorhanden** wordt weergegeven, wordt het veld **Hoeveelheid** bijgewerkt om het verschil aan te geven.</span><span class="sxs-lookup"><span data-stu-id="5ee42-128">If you enter a counted number that’s different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="5ee42-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="5ee42-130">Het voorraadtellingsjournaal boeken</span><span class="sxs-lookup"><span data-stu-id="5ee42-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="5ee42-131">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-131">Select **Post**.</span></span> <span data-ttu-id="5ee42-132">Als u een voorraadtellingsjournaal boekt en het getelde bedrag afwijkt van het aantal dat in het veld **Voorhanden** wordt vermeld, wordt er een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="5ee42-132">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="5ee42-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="5ee42-134">Voorraadtransacties weergeven</span><span class="sxs-lookup"><span data-stu-id="5ee42-134">View inventory transactions</span></span>
1. <span data-ttu-id="5ee42-135">Selecteer **Voorraadmodel**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="5ee42-136">Selecteer **Transacties**.</span><span class="sxs-lookup"><span data-stu-id="5ee42-136">Select **Transactions**.</span></span> <span data-ttu-id="5ee42-137">Hier kunt u de verwante transacties bekijken die worden gemaakt wanneer u uw voorraadtellingsjournaal boekt.</span><span class="sxs-lookup"><span data-stu-id="5ee42-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

