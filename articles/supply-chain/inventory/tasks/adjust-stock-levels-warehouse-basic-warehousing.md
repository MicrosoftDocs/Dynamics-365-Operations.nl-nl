--- 
title: Voorraadniveaus in het magazijn aanpassen (basale magazijnen)
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn.
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 75ff53872fd81d5b25964c1ba65127f9feaf2b45
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="c01d5-103">Voorraadniveaus in het magazijn aanpassen (basale magazijnen)</span><span class="sxs-lookup"><span data-stu-id="c01d5-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c01d5-104">Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="c01d5-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="c01d5-105">U moet een voorraadjournaalnaam hebben ingesteld voor voorraadcorrecties voordat u hiermee start.</span><span class="sxs-lookup"><span data-stu-id="c01d5-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="c01d5-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c01d5-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="c01d5-107">Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="c01d5-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="c01d5-108">Een voorraadcorrectiejournaal maken</span><span class="sxs-lookup"><span data-stu-id="c01d5-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="c01d5-109">Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Voorraadcorrectie.</span><span class="sxs-lookup"><span data-stu-id="c01d5-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="c01d5-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c01d5-110">Click New.</span></span>
3. <span data-ttu-id="c01d5-111">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c01d5-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c01d5-112">Klik in de lijst op de naam van het voorraadcorrectiejournaal dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c01d5-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="c01d5-113">Enkele andere velden worden ingevuld op basis van de instelling van de naam voor het journaal voor voorraadcorrectie die u selecteert.</span><span class="sxs-lookup"><span data-stu-id="c01d5-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="c01d5-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c01d5-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="c01d5-115">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="c01d5-115">Create journal lines</span></span>
1. <span data-ttu-id="c01d5-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c01d5-116">Click New.</span></span>
2. <span data-ttu-id="c01d5-117">Markeer in de lijst het veld met het artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="c01d5-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="c01d5-118">Selecteer een artikel in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="c01d5-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="c01d5-119">Als u het demobedrijf USMF gebruikt, typt u 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="c01d5-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="c01d5-120">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c01d5-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c01d5-121">Selecteer een locatie in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c01d5-121">In the list, select a site.</span></span>
6. <span data-ttu-id="c01d5-122">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c01d5-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c01d5-123">Selecteer een magazijn in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c01d5-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="c01d5-124">Als u een artikel met Locatie als verplichte dimensie hebt geselecteerd, moet u de locatie hier opgeven.</span><span class="sxs-lookup"><span data-stu-id="c01d5-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="c01d5-125">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="c01d5-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c01d5-126">Het kostprijsveld geeft de kosten per eenheid voor voorraadontvangsten op.</span><span class="sxs-lookup"><span data-stu-id="c01d5-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="c01d5-127">Als de kosten niet voor het artikelnummer zijn opgegeven of als u deze handmatig wilt wijzigen, doet u dat hier.</span><span class="sxs-lookup"><span data-stu-id="c01d5-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="c01d5-128">Het voorraadcorrectiejournaal valideren en boeken</span><span class="sxs-lookup"><span data-stu-id="c01d5-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="c01d5-129">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="c01d5-129">Click Validate.</span></span>
2. <span data-ttu-id="c01d5-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c01d5-130">Click OK.</span></span>
3. <span data-ttu-id="c01d5-131">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="c01d5-131">Click Post.</span></span>
    * <span data-ttu-id="c01d5-132">Wanneer u dit soort journaal boekt, wordt een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c01d5-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="c01d5-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c01d5-133">Click OK.</span></span>
5. <span data-ttu-id="c01d5-134">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="c01d5-134">Close the form.</span></span>
6. <span data-ttu-id="c01d5-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c01d5-135">Close the page.</span></span>


