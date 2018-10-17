--- 
title: Een eindproduct maken (februari 2016)
description: Deze taak is gericht op het maken van een eindproduct.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="90b39-103">Een eindproduct maken (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="90b39-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90b39-104">Deze taak is gericht op het maken van een eindproduct.</span><span class="sxs-lookup"><span data-stu-id="90b39-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="90b39-105">Dit is de eerste taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="90b39-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="90b39-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="90b39-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="90b39-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="90b39-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="90b39-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="90b39-108">Click New.</span></span>
3. <span data-ttu-id="90b39-109">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="90b39-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="90b39-110">Typ voor de demonstratie: 'Stuklijst_1'.</span><span class="sxs-lookup"><span data-stu-id="90b39-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="90b39-111">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="90b39-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-112">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="90b39-112">Select STD.</span></span> <span data-ttu-id="90b39-113">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="90b39-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="90b39-114">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="90b39-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-115">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="90b39-115">For example, select Audio.</span></span> <span data-ttu-id="90b39-116">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="90b39-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="90b39-117">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="90b39-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-118">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="90b39-118">Select SiteWH.</span></span> <span data-ttu-id="90b39-119">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="90b39-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="90b39-120">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="90b39-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-121">Traceringsdimensies worden niet voor dit voorbeeld gebruikt. Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="90b39-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="90b39-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="90b39-122">Click OK.</span></span>
9. <span data-ttu-id="90b39-123">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="90b39-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="90b39-124">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="90b39-124">Click Default order settings.</span></span>
11. <span data-ttu-id="90b39-125">Selecteer in het veld Standaardordertype: 'Productie'.</span><span class="sxs-lookup"><span data-stu-id="90b39-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="90b39-126">Omdat dit een eindproduct is dat wordt geproduceerd, selecteert u 'Productie'.</span><span class="sxs-lookup"><span data-stu-id="90b39-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="90b39-127">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="90b39-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-128">Selecteer voor de demonstratie: 'Locatie 1'.</span><span class="sxs-lookup"><span data-stu-id="90b39-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="90b39-129">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="90b39-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-130">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="90b39-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="90b39-131">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="90b39-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="90b39-132">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="90b39-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="90b39-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="90b39-133">Close the page.</span></span>

