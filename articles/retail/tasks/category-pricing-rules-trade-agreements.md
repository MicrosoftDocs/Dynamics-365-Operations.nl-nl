--- 
title: " Categorieprijsregels om handelsovereenkomsten te maken"
description: Deze procedure toont aan hoe u handelsovereenkomsten voor verkoopprijzen maakt met een categorieprijsregel.
author: scott-tucker
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 454f74627bd4811fa657b0c6b06003a8fdbdb599
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="e477b-103"> Categorieprijsregels om handelsovereenkomsten te maken</span><span class="sxs-lookup"><span data-stu-id="e477b-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e477b-104">Deze procedure toont aan hoe u handelsovereenkomsten voor verkoopprijzen maakt met een categorieprijsregel.</span><span class="sxs-lookup"><span data-stu-id="e477b-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="e477b-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="e477b-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="e477b-106">Deze taak is bedoeld voor de rol Merchandisingbeheerder detailhandel.</span><span class="sxs-lookup"><span data-stu-id="e477b-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="e477b-107">Klik op Prijzen- en kortingsbeheer.</span><span class="sxs-lookup"><span data-stu-id="e477b-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="e477b-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e477b-108">Click New.</span></span>
3. <span data-ttu-id="e477b-109">Klik op Prijsregel van categorie.</span><span class="sxs-lookup"><span data-stu-id="e477b-109">Click Category price rule.</span></span>
4. <span data-ttu-id="e477b-110">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e477b-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e477b-111">Selecteer een optie in het veld Rekeningcode.</span><span class="sxs-lookup"><span data-stu-id="e477b-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="e477b-112">Een rekeningcode van het type 'Groep' wordt gebruikt om de handelsovereenkomsten voor verkoopprijzen in te stellen die specifiek zijn voor kanalen, loyaliteitsprogramma's, catalogi en aansluitingen.</span><span class="sxs-lookup"><span data-stu-id="e477b-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="e477b-113">Typ of selecteer een waarde in het veld Rekening selecteren.</span><span class="sxs-lookup"><span data-stu-id="e477b-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="e477b-114">Typ of selecteer een waarde in het veld Categorie.</span><span class="sxs-lookup"><span data-stu-id="e477b-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="e477b-115">Typ een getal in het veld Bedrag/percentage.</span><span class="sxs-lookup"><span data-stu-id="e477b-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="e477b-116">Typ of selecteer een waarde in het veld Afrondingsversie.</span><span class="sxs-lookup"><span data-stu-id="e477b-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="e477b-117">Klik op Handelsovereenkomsten genereren.</span><span class="sxs-lookup"><span data-stu-id="e477b-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="e477b-118">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="e477b-118">Click Next.</span></span>
12. <span data-ttu-id="e477b-119">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="e477b-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="e477b-120">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="e477b-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="e477b-121">Selecteer Ja in het veld Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="e477b-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="e477b-122">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="e477b-122">Click Next.</span></span>
16. <span data-ttu-id="e477b-123">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="e477b-123">Click Finish.</span></span>
    * <span data-ttu-id="e477b-124">Hiermee maakt u een Handelsovereenkomstjournaal en opent u dit voor uw beoordeling.</span><span class="sxs-lookup"><span data-stu-id="e477b-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="e477b-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e477b-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e477b-126">De handelsovereenkomstjournalen die met de categorieprijsregels zijn gemaakt, worden niet geboekt.</span><span class="sxs-lookup"><span data-stu-id="e477b-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="e477b-127">U kunt de gegenereerde prijzen controleren en bewerken voordat deze worden boeken.</span><span class="sxs-lookup"><span data-stu-id="e477b-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="e477b-128">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="e477b-128">Click Edit.</span></span>
19. <span data-ttu-id="e477b-129">Typ een getal in het veld Bedrag in valuta.</span><span class="sxs-lookup"><span data-stu-id="e477b-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="e477b-130">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="e477b-130">Click Post.</span></span>
21. <span data-ttu-id="e477b-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e477b-131">Click OK.</span></span>
22. <span data-ttu-id="e477b-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e477b-132">Close the page.</span></span>
23. <span data-ttu-id="e477b-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e477b-133">Close the page.</span></span>
24. <span data-ttu-id="e477b-134">Klik op het tabblad Categorieprijsregels.</span><span class="sxs-lookup"><span data-stu-id="e477b-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="e477b-135">Kanaalspecifieke categorieprijsregels worden in deze lijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e477b-135">Channel specific Category pricing rules will show in this list.</span></span>  


