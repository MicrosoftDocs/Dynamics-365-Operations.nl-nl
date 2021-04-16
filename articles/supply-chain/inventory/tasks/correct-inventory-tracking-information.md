---
title: Voorraadtraceringsinformatie corrigeren
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om voorraadtraceringsinformatie te corrigeren.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d7bbb1f2e6128b1dea2be8dc737d5ae526195f08
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834068"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="27e8d-103">Voorraadtraceringsinformatie corrigeren</span><span class="sxs-lookup"><span data-stu-id="27e8d-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27e8d-104">Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om voorraadtraceringsinformatie te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="27e8d-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="27e8d-105">In dit voorbeeld werken we de informatie van een batchartikel bij door een verkeerd geregistreerde batch in een andere batch te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="27e8d-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="27e8d-106">U kunt deze procedure met het demobedrijf USPI uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="27e8d-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="27e8d-107">Als u uw eigen gegevens gebruikt, moet u een artikel hebben dat voor batchverwerking ingesteld is en mag de locatie niet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="27e8d-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="27e8d-108">U moet ook een voorraadjournaalnaam hebben ingesteld voor voorraadoverboekingen.</span><span class="sxs-lookup"><span data-stu-id="27e8d-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="27e8d-109">Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="27e8d-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="27e8d-110">Een voorraadoverboekingsjournaal maken</span><span class="sxs-lookup"><span data-stu-id="27e8d-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="27e8d-111">Ga naar Overboeken.</span><span class="sxs-lookup"><span data-stu-id="27e8d-111">Go to Transfer.</span></span>
2. <span data-ttu-id="27e8d-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="27e8d-112">Click New.</span></span>
3. <span data-ttu-id="27e8d-113">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="27e8d-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="27e8d-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="27e8d-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="27e8d-115">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="27e8d-115">Create journal lines</span></span>
1. <span data-ttu-id="27e8d-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="27e8d-116">Click New.</span></span>
2. <span data-ttu-id="27e8d-117">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="27e8d-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="27e8d-118">Als u USPI gebruikt, selecteert u artikel M5003.</span><span class="sxs-lookup"><span data-stu-id="27e8d-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="27e8d-119">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="27e8d-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="27e8d-120">Klik op het tabblad Voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="27e8d-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="27e8d-121">Typ of selecteer een waarde in het veld Batchnummer.</span><span class="sxs-lookup"><span data-stu-id="27e8d-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="27e8d-122">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="27e8d-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="27e8d-123">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="27e8d-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="27e8d-124">Typ of selecteer een waarde in het veld Batchnummer.</span><span class="sxs-lookup"><span data-stu-id="27e8d-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="27e8d-125">Het journaal boeken</span><span class="sxs-lookup"><span data-stu-id="27e8d-125">Post the journal</span></span>
1. <span data-ttu-id="27e8d-126">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="27e8d-126">Click Post.</span></span>
2. <span data-ttu-id="27e8d-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="27e8d-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="27e8d-128">Traceringsinformatie controleren</span><span class="sxs-lookup"><span data-stu-id="27e8d-128">Check tracing information</span></span>
1. <span data-ttu-id="27e8d-129">Klik op Voorraad.</span><span class="sxs-lookup"><span data-stu-id="27e8d-129">Click Inventory.</span></span>
2. <span data-ttu-id="27e8d-130">Klik op Traceren.</span><span class="sxs-lookup"><span data-stu-id="27e8d-130">Click Trace.</span></span>
3. <span data-ttu-id="27e8d-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="27e8d-131">Click OK.</span></span>
    * <span data-ttu-id="27e8d-132">Met deze traceringinformatie kunt u terug traceren van welke batch u voorraad corrigeerde.</span><span class="sxs-lookup"><span data-stu-id="27e8d-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="27e8d-133">U kunt de pagina Traceren artikel ook gebruiken om deze informatie te bekijken.</span><span class="sxs-lookup"><span data-stu-id="27e8d-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="27e8d-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="27e8d-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="27e8d-135">Voorraadtransacties controleren</span><span class="sxs-lookup"><span data-stu-id="27e8d-135">Check inventory transactions</span></span>
1. <span data-ttu-id="27e8d-136">Klik op Voorraad.</span><span class="sxs-lookup"><span data-stu-id="27e8d-136">Click Inventory.</span></span>
2. <span data-ttu-id="27e8d-137">Klik op Transacties.</span><span class="sxs-lookup"><span data-stu-id="27e8d-137">Click Transactions.</span></span>
    * <span data-ttu-id="27e8d-138">Hier ziet u de transacties die werden gemaakt toen u uw journaal boekte.</span><span class="sxs-lookup"><span data-stu-id="27e8d-138">Here you can see the transactions that were created when you posted your journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]