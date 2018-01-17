---
title: "Voorraadniveaus in het magazijn initiëren"
description: Deze procedure laat zien hoe u de voorhanden voorraad handmatig bijwerkt met behulp van een voorraadmutatiejournaal.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 5baea2a0f194012406d378effbc0ae5d4062fd65
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="b090c-103">Voorraadniveaus in het magazijn initiëren</span><span class="sxs-lookup"><span data-stu-id="b090c-103">Initialize stock levels in the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b090c-104">Deze procedure laat zien hoe u de voorhanden voorraad handmatig bijwerkt met behulp van een voorraadmutatiejournaal.</span><span class="sxs-lookup"><span data-stu-id="b090c-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="b090c-105">(Het is ook mogelijk om voorhanden voorraad bij te werken door transacties in gegevensentiteiten te importeren.) U kunt deze handleiding in het demobedrijf USMF uitvoeren, waar alle vereisten zoals journaalnaam, artikelinstelling, boekingsprofielen en rekeningen beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="b090c-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="b090c-106">De handleiding suggereert specifieke waarden voor het artikel en de dimensies die worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b090c-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="b090c-107">Als u een ander artikel kiest, moet u mogelijk waarden voor andere dimensies invoeren.</span><span class="sxs-lookup"><span data-stu-id="b090c-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="b090c-108">Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Mutatie.</span><span class="sxs-lookup"><span data-stu-id="b090c-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="b090c-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b090c-109">Click New.</span></span>
3. <span data-ttu-id="b090c-110">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b090c-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b090c-111">Selecteer IMov.</span><span class="sxs-lookup"><span data-stu-id="b090c-111">Select IMov.</span></span>
    * <span data-ttu-id="b090c-112">Het is een goed idee om verschillende journaalnaamsjablonen te gebruiken voor verschillende bedrijfsdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="b090c-112">It’s a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="b090c-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b090c-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b090c-114">Geef in het veld Tegenrekening de waarden '140200' op.</span><span class="sxs-lookup"><span data-stu-id="b090c-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="b090c-115">Dit is de tegenrekening die de standaardrekening is op de journaalregels.</span><span class="sxs-lookup"><span data-stu-id="b090c-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="b090c-116">Het is mogelijk om de standaardwaarde te negeren om verschillende tegenrekeningen per regel toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="b090c-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="b090c-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b090c-117">Click OK.</span></span>
8. <span data-ttu-id="b090c-118">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b090c-118">Click New.</span></span>
9. <span data-ttu-id="b090c-119">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b090c-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b090c-120">Selecteer artikel A0001.</span><span class="sxs-lookup"><span data-stu-id="b090c-120">Select item A0001.</span></span>
11. <span data-ttu-id="b090c-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b090c-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b090c-122">Klik op het tabblad Voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="b090c-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="b090c-123">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b090c-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b090c-124">Selecteer site 1.</span><span class="sxs-lookup"><span data-stu-id="b090c-124">Select site 1.</span></span>
15. <span data-ttu-id="b090c-125">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b090c-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="b090c-126">Selecteer magazijn 13.</span><span class="sxs-lookup"><span data-stu-id="b090c-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="b090c-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b090c-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b090c-128">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b090c-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b090c-129">Selecteer locatie 13.</span><span class="sxs-lookup"><span data-stu-id="b090c-129">Select location 13.</span></span>
20. <span data-ttu-id="b090c-130">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="b090c-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="b090c-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b090c-131">Click Save.</span></span>
22. <span data-ttu-id="b090c-132">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="b090c-132">Click Post.</span></span>
23. <span data-ttu-id="b090c-133">Schakel het selectievakje Alle boekingsfouten overboeken naar een nieuw journaal in of uit.</span><span class="sxs-lookup"><span data-stu-id="b090c-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="b090c-134">Als u deze optie inschakelt, worden eventuele regels die er niet in slagen te boeken, naar een nieuw journaal gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b090c-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="b090c-135">Deze procedure gebruikt de informatie in het logboek om de problemen te corrigeren en boekt vervolgens de regels opnieuw.</span><span class="sxs-lookup"><span data-stu-id="b090c-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="b090c-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b090c-136">Click OK.</span></span>
25. <span data-ttu-id="b090c-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b090c-137">Close the page.</span></span>
26. <span data-ttu-id="b090c-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b090c-138">Close the page.</span></span>

