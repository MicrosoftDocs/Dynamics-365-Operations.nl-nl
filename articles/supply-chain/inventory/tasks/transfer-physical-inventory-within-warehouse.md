---
title: Fysieke voorraad in het magazijn overboeken
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om verplaatsing van een artikel van een locatie in een magazijn naar een andere locatie te registreren.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: 899701413814ce38a4367618ed72d1039eca0bf8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148165"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="9a40c-103">Fysieke voorraad in het magazijn overboeken</span><span class="sxs-lookup"><span data-stu-id="9a40c-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a40c-104">Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om verplaatsing van een artikel van een locatie in een magazijn naar een andere locatie te registreren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="9a40c-105">U moet een voorraadjournaalnaam hebben ingesteld voor voorraadoverboekingen voordat u hiermee start.</span><span class="sxs-lookup"><span data-stu-id="9a40c-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="9a40c-106">U kunt deze procedure doorlopen in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven, of u kunt uw eigen gegevens gebruiken als u producten en locaties hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9a40c-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="9a40c-107">Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="9a40c-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="9a40c-108">Een voorraadoverboekingsjournaal maken</span><span class="sxs-lookup"><span data-stu-id="9a40c-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="9a40c-109">Ga in het **navigatievenster** naar **Voorraadbeheer > Journaalboekingen > Artikelen > Overboeken**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="9a40c-110">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-110">Click **New**.</span></span>
3. <span data-ttu-id="9a40c-111">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="9a40c-112">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-112">Click **OK**.</span></span> <span data-ttu-id="9a40c-113">Er is de optie om 'Van' en 'Naar' dimensies voor elke journaalregel op te geven.</span><span class="sxs-lookup"><span data-stu-id="9a40c-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="9a40c-114">Deze zijn essentieel voor dit journaaltype.</span><span class="sxs-lookup"><span data-stu-id="9a40c-114">These are essential for this journal type.</span></span> <span data-ttu-id="9a40c-115">U kunt artikelen overboeken naar locaties met verschillende regels.</span><span class="sxs-lookup"><span data-stu-id="9a40c-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="9a40c-116">In dit voorbeeld boeken we een artikel over in hetzelfde magazijn, van een locatie waar nummerplaten worden gecontroleerd naar een locatie waar nummerplaten niet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="9a40c-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="9a40c-117">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="9a40c-117">Create journal lines</span></span>
1. <span data-ttu-id="9a40c-118">Klik op het sneltabblad **Journaalregels** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="9a40c-119">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-120">Als u USMF gebruikt, kunt u 'A0001' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="9a40c-121">Typ of selecteer een waarde in het veld **Van vestiging**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-122">Als u USMF gebruikt, kunt u '2' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="9a40c-123">Typ of selecteer een waarde in het veld **Naar vestiging**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-124">Als u USMF gebruikt, kunt u '2' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="9a40c-125">Typ of selecteer een waarde in het veld **Van magazijn**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-126">Als u USMF gebruikt, kunt u '24' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="9a40c-127">Typ of selecteer een waarde in het veld **Naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-128">Als u USMF gebruikt, kunt u '24' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="9a40c-129">Typ of selecteer een waarde in het veld **Van locatie**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-130">Als u USMF gebruikt, kunt u 'FL-001' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="9a40c-131">Typ of selecteer een waarde in het veld **Naar locatie**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-132">Als u USMF gebruikt, kunt u 'BULK-001' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="9a40c-133">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="9a40c-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="9a40c-134">Klik op het sneltabblad **Regeldetails** op het tabblad **Voorraaddimensies**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="9a40c-135">Typ of selecteer een waarde in **Van voorraaddimensies** in het veld **Nummerplaat**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="9a40c-136">Als u USMF gebruikt, kunt u '24' selecteren.</span><span class="sxs-lookup"><span data-stu-id="9a40c-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="9a40c-137">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="9a40c-138">Het voorraadoverboekingsjournaal boeken</span><span class="sxs-lookup"><span data-stu-id="9a40c-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="9a40c-139">Klik in het **actievenster** op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-139">On the **Action pane**, click **Post**.</span></span>
2. <span data-ttu-id="9a40c-140">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="9a40c-141">Voorraadtransacties weergeven</span><span class="sxs-lookup"><span data-stu-id="9a40c-141">View inventory transactions</span></span>
1. <span data-ttu-id="9a40c-142">Klik op **Voorraad**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="9a40c-143">Klik op **Transacties**.</span><span class="sxs-lookup"><span data-stu-id="9a40c-143">Click **Transactions**.</span></span> <span data-ttu-id="9a40c-144">Hier ziet u de transacties die werden gemaakt toen u uw journaal boekte.</span><span class="sxs-lookup"><span data-stu-id="9a40c-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

