---
title: Voorraad in een magazijn tellen
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadtellingsjournaal om een artikel op een specifieke locatie in het magazijn te tellen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549886"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="eb60f-103">Voorraad in een magazijn tellen</span><span class="sxs-lookup"><span data-stu-id="eb60f-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb60f-104">Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadtellingsjournaal om een artikel op een specifieke locatie in het magazijn te tellen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="eb60f-105">De procedure is van toepassing op de functie 'basale magazijnen' die beschikbaar is in de module Voorraadbeheer, niet op de magazijnfunctionaliteit die beschikbaar is in de module magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="eb60f-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="eb60f-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eb60f-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="eb60f-107">Als u uw eigen gegevens gebruikt, moet u ervoor zorgen dat u producten en locaties hebt ingesteld en dat u een voorraadjournaalnaam voor tellingsjournalen hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eb60f-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="eb60f-108">Voorraadtelling wordt normaal uitgevoerd door een magazijnwerknemer.</span><span class="sxs-lookup"><span data-stu-id="eb60f-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="eb60f-109">Een voorraadtellingsjournaal maken</span><span class="sxs-lookup"><span data-stu-id="eb60f-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="eb60f-110">Ga naar Voorraadbeheer > Journaalboekingen > Artikeltelling > Tellen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="eb60f-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eb60f-111">Click New.</span></span>
3. <span data-ttu-id="eb60f-112">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="eb60f-113">Klik in de lijst op de naam van het voorraadtellingsjournaal dat u wilt gebruiken</span><span class="sxs-lookup"><span data-stu-id="eb60f-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="eb60f-114">Enkele andere velden worden ingevuld op basis van de instellingen van de naam voor het standaardjournaal voor voorraadtelling die u selecteert.</span><span class="sxs-lookup"><span data-stu-id="eb60f-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="eb60f-115">Klik in het veld Medewerker op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="eb60f-116">Selecteer in de lijst de medewerker die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eb60f-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="eb60f-117">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="eb60f-117">Click Select.</span></span>
8. <span data-ttu-id="eb60f-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb60f-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="eb60f-119">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="eb60f-119">Create journal lines</span></span>
1. <span data-ttu-id="eb60f-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eb60f-120">Click New.</span></span>
2. <span data-ttu-id="eb60f-121">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="eb60f-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eb60f-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb60f-123">Als u het demobedrijf USMF gebruikt, selecteert u 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="eb60f-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="eb60f-124">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="eb60f-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eb60f-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb60f-126">Als u het demobedrijf USMF gebruikt, selecteert u site '2'.</span><span class="sxs-lookup"><span data-stu-id="eb60f-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="eb60f-127">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="eb60f-128">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eb60f-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb60f-129">Als u het demobedrijf USMF gebruikt, selecteert u magazijn '24'.</span><span class="sxs-lookup"><span data-stu-id="eb60f-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="eb60f-130">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="eb60f-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="eb60f-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eb60f-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb60f-132">Als u het demobedrijf USMF gebruikt, selecteert u locatie 'BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="eb60f-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="eb60f-133">Voer in het veld Geteld een getal in.</span><span class="sxs-lookup"><span data-stu-id="eb60f-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="eb60f-134">Als u een geteld aantal invoert dat verschilt van het nummer dat in het veld In Voorhanden wordt weergegeven, wordt het Veld Hoeveelheid bijgewerkt om het verschil aan te geven.</span><span class="sxs-lookup"><span data-stu-id="eb60f-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="eb60f-135">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="eb60f-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="eb60f-136">Het voorraadtellingsjournaal boeken</span><span class="sxs-lookup"><span data-stu-id="eb60f-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="eb60f-137">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="eb60f-137">Click Post.</span></span>
    * <span data-ttu-id="eb60f-138">Wanneer u een voorraadtellingsjournaal boekt en als het getelde bedrag afwijkt van het bedrag dat in het veld Voorhanden wordt vermeld, wordt een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="eb60f-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="eb60f-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eb60f-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="eb60f-140">Voorraadtransacties weergeven</span><span class="sxs-lookup"><span data-stu-id="eb60f-140">View inventory transactions</span></span>
1. <span data-ttu-id="eb60f-141">Klik op Voorraad.</span><span class="sxs-lookup"><span data-stu-id="eb60f-141">Click Inventory.</span></span>
2. <span data-ttu-id="eb60f-142">Klik op Transacties.</span><span class="sxs-lookup"><span data-stu-id="eb60f-142">Click Transactions.</span></span>
    * <span data-ttu-id="eb60f-143">Hier kunt u de verwante transacties bekijken die worden gemaakt wanneer u uw voorraadtellingsjournaal boekt.</span><span class="sxs-lookup"><span data-stu-id="eb60f-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

