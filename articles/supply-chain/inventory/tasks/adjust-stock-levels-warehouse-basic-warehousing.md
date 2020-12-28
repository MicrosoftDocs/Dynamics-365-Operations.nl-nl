---
title: Voorraadniveaus in het magazijn aanpassen (basale magazijnen)
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9678dffd84e9e4032510811731a67da953b40431
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425714"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="cea8c-103">Voorraadniveaus in het magazijn aanpassen (basale magazijnen)</span><span class="sxs-lookup"><span data-stu-id="cea8c-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cea8c-104">Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="cea8c-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="cea8c-105">U moet een voorraadjournaalnaam hebben ingesteld voor voorraadcorrecties voordat u hiermee start.</span><span class="sxs-lookup"><span data-stu-id="cea8c-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="cea8c-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cea8c-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="cea8c-107">Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="cea8c-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="cea8c-108">Een voorraadcorrectiejournaal maken</span><span class="sxs-lookup"><span data-stu-id="cea8c-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="cea8c-109">Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Voorraadcorrectie.</span><span class="sxs-lookup"><span data-stu-id="cea8c-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="cea8c-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cea8c-110">Click New.</span></span>
3. <span data-ttu-id="cea8c-111">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cea8c-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cea8c-112">Klik in de lijst op de naam van het voorraadcorrectiejournaal dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cea8c-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="cea8c-113">Enkele andere velden worden ingevuld op basis van de instelling van de naam voor het journaal voor voorraadcorrectie die u selecteert.</span><span class="sxs-lookup"><span data-stu-id="cea8c-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="cea8c-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cea8c-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="cea8c-115">Journaalregels maken</span><span class="sxs-lookup"><span data-stu-id="cea8c-115">Create journal lines</span></span>
1. <span data-ttu-id="cea8c-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cea8c-116">Click New.</span></span>
2. <span data-ttu-id="cea8c-117">Markeer in de lijst het veld met het artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="cea8c-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="cea8c-118">Selecteer een artikel in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="cea8c-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="cea8c-119">Als u het demobedrijf USMF gebruikt, typt u 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="cea8c-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="cea8c-120">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cea8c-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cea8c-121">Selecteer een locatie in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cea8c-121">In the list, select a site.</span></span>
6. <span data-ttu-id="cea8c-122">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cea8c-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cea8c-123">Selecteer een magazijn in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cea8c-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="cea8c-124">Als u een artikel met Locatie als verplichte dimensie hebt geselecteerd, moet u de locatie hier opgeven.</span><span class="sxs-lookup"><span data-stu-id="cea8c-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="cea8c-125">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="cea8c-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cea8c-126">Het kostprijsveld geeft de kosten per eenheid voor voorraadontvangsten op.</span><span class="sxs-lookup"><span data-stu-id="cea8c-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="cea8c-127">Als de kosten niet voor het artikelnummer zijn opgegeven of als u deze handmatig wilt wijzigen, doet u dat hier.</span><span class="sxs-lookup"><span data-stu-id="cea8c-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="cea8c-128">Het voorraadcorrectiejournaal valideren en boeken</span><span class="sxs-lookup"><span data-stu-id="cea8c-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="cea8c-129">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="cea8c-129">Click Validate.</span></span>
2. <span data-ttu-id="cea8c-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cea8c-130">Click OK.</span></span>
3. <span data-ttu-id="cea8c-131">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="cea8c-131">Click Post.</span></span>
    * <span data-ttu-id="cea8c-132">Wanneer u dit soort journaal boekt, wordt een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="cea8c-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="cea8c-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cea8c-133">Click OK.</span></span>
5. <span data-ttu-id="cea8c-134">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="cea8c-134">Close the form.</span></span>
6. <span data-ttu-id="cea8c-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cea8c-135">Close the page.</span></span>

