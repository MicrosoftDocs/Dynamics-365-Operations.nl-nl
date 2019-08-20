---
title: Fysieke voorraad in het magazijn overboeken
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om verplaatsing van een artikel van een locatie in een magazijn naar een andere locatie te registreren.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7344bfa3be0d7345d3ac68202c7bc26bcac8ebb9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845252"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="f0352-103">Fysieke voorraad in het magazijn overboeken</span><span class="sxs-lookup"><span data-stu-id="f0352-103">Transfer physical inventory within the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0352-104">Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om verplaatsing van een artikel van een locatie in een magazijn naar een andere locatie te registreren.</span><span class="sxs-lookup"><span data-stu-id="f0352-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="f0352-105">U moet een voorraadjournaalnaam hebben ingesteld voor voorraadoverboekingen voordat u hiermee start.</span><span class="sxs-lookup"><span data-stu-id="f0352-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="f0352-106">U kunt deze procedure doorlopen in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven, of u kunt uw eigen gegevens gebruiken als u producten en locaties hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f0352-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="f0352-107">Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="f0352-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="f0352-108">Een voorraadoverboekingsjournaal maken</span><span class="sxs-lookup"><span data-stu-id="f0352-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="f0352-109">Ga naar Overboeken.</span><span class="sxs-lookup"><span data-stu-id="f0352-109">Go to Transfer.</span></span>
2. <span data-ttu-id="f0352-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f0352-110">Click New.</span></span>
3. <span data-ttu-id="f0352-111">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f0352-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="f0352-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f0352-112">Click OK.</span></span>
    * <span data-ttu-id="f0352-113">Er is de optie om 'Van' en 'Naar' dimensies voor elke journaalregel op te geven.</span><span class="sxs-lookup"><span data-stu-id="f0352-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="f0352-114">Deze zijn essentieel voor dit journaaltype.</span><span class="sxs-lookup"><span data-stu-id="f0352-114">These are essential for this journal type.</span></span> <span data-ttu-id="f0352-115">U kunt artikelen overboeken naar locaties met verschillende regels.</span><span class="sxs-lookup"><span data-stu-id="f0352-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="f0352-116">In dit voorbeeld boeken we een artikel over in hetzelfde magazijn, van een locatie waar nummerplaten worden gecontroleerd naar een locatie waar nummerplaten niet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="f0352-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="f0352-117">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="f0352-117">Create journal lines</span></span>
1. <span data-ttu-id="f0352-118">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f0352-118">Click New.</span></span>
2. <span data-ttu-id="f0352-119">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="f0352-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-120">Als u USMF gebruikt, kunt u 'A0001' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="f0352-121">Typ of selecteer een waarde in het veld Van vestiging.</span><span class="sxs-lookup"><span data-stu-id="f0352-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-122">Als u USMF gebruikt, kunt u '2' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="f0352-123">Typ of selecteer een waarde in het veld Naar vestiging.</span><span class="sxs-lookup"><span data-stu-id="f0352-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-124">Als u USMF gebruikt, kunt u '2' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="f0352-125">Typ of selecteer een waarde in het veld Van magazijn.</span><span class="sxs-lookup"><span data-stu-id="f0352-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-126">Als u USMF gebruikt, kunt u '24' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="f0352-127">Typ of selecteer een waarde in het veld Naar magazijn.</span><span class="sxs-lookup"><span data-stu-id="f0352-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-128">Als u USMF gebruikt, kunt u '24' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="f0352-129">Typ of selecteer een waarde in het veld Van locatie.</span><span class="sxs-lookup"><span data-stu-id="f0352-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-130">Als u USMF gebruikt, kunt u 'FL-001' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="f0352-131">Typ of selecteer een waarde in het veld Naar locatie.</span><span class="sxs-lookup"><span data-stu-id="f0352-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-132">Als u USMF gebruikt, kunt u 'BULK-001' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="f0352-133">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="f0352-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="f0352-134">Klik op het tabblad Voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="f0352-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="f0352-135">Typ of selecteer een waarde in het veld Nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="f0352-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="f0352-136">Als u USMF gebruikt, kunt u '24' selecteren.</span><span class="sxs-lookup"><span data-stu-id="f0352-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="f0352-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f0352-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="f0352-138">Het voorraadoverboekingsjournaal boeken</span><span class="sxs-lookup"><span data-stu-id="f0352-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="f0352-139">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="f0352-139">Click Post.</span></span>
2. <span data-ttu-id="f0352-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f0352-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="f0352-141">Voorraadtransacties weergeven</span><span class="sxs-lookup"><span data-stu-id="f0352-141">View inventory transactions</span></span>
1. <span data-ttu-id="f0352-142">Klik op Voorraad.</span><span class="sxs-lookup"><span data-stu-id="f0352-142">Click Inventory.</span></span>
2. <span data-ttu-id="f0352-143">Klik op Transacties.</span><span class="sxs-lookup"><span data-stu-id="f0352-143">Click Transactions.</span></span>
    * <span data-ttu-id="f0352-144">Hier ziet u de transacties die werden gemaakt toen u uw journaal boekte.</span><span class="sxs-lookup"><span data-stu-id="f0352-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

