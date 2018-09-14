--- 
title: Standaardkosten voor arbeid en onkosten configureren
description: In deze procedure wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="73857-103">Standaardkosten voor arbeid en onkosten configureren</span><span class="sxs-lookup"><span data-stu-id="73857-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73857-104">In deze procedure wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.</span><span class="sxs-lookup"><span data-stu-id="73857-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="73857-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73857-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="73857-106">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Kostprijs (uur).</span><span class="sxs-lookup"><span data-stu-id="73857-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="73857-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="73857-107">Click New.</span></span>
3. <span data-ttu-id="73857-108">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="73857-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="73857-109">Voer in het veld Kostprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="73857-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="73857-110">U kunt een standaardkostprijs voor de projectcategorie instellen of u kunt een kostprijs instellen per werknemernummer, projectnummer, categorie, datum of elke combinatie van deze factoren.</span><span class="sxs-lookup"><span data-stu-id="73857-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="73857-111">De kostprijs met het hoogste detailniveau wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="73857-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="73857-112">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="73857-112">Click Save.</span></span>
6. <span data-ttu-id="73857-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="73857-113">Close the page.</span></span>
7. <span data-ttu-id="73857-114">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Verkoopprijs (uur).</span><span class="sxs-lookup"><span data-stu-id="73857-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="73857-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="73857-115">Click New.</span></span>
9. <span data-ttu-id="73857-116">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="73857-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="73857-117">Selecteer een optie in het veld Geldig voor.</span><span class="sxs-lookup"><span data-stu-id="73857-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="73857-118">Voer in het veld Prijscalculatie een getal in.</span><span class="sxs-lookup"><span data-stu-id="73857-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="73857-119">U kunt een standaardverkoopprijs definiëren voor uurtransacties of voor een projectcategorie.</span><span class="sxs-lookup"><span data-stu-id="73857-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="73857-120">U kunt ook verkoopprijzen instellen per werknemernummer, projectnummer, categorie, transactiedatum of een combinatie van deze.</span><span class="sxs-lookup"><span data-stu-id="73857-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="73857-121">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het Urenjournaal, is de verkoopprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="73857-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="73857-122">Als er bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs is gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73857-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="73857-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="73857-123">Click Save.</span></span>
13. <span data-ttu-id="73857-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="73857-124">Close the page.</span></span>
14. <span data-ttu-id="73857-125">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Kostprijs (onkosten).</span><span class="sxs-lookup"><span data-stu-id="73857-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="73857-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="73857-126">Click New.</span></span>
16. <span data-ttu-id="73857-127">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="73857-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="73857-128">Voer in het veld Kostprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="73857-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="73857-129">Meerdere velden kunnen worden ingevuld, maar dit is het minimum wat nodig is om de record te kunnen opslaan.</span><span class="sxs-lookup"><span data-stu-id="73857-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="73857-130">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="73857-130">Click Save.</span></span>
19. <span data-ttu-id="73857-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="73857-131">Close the page.</span></span>
20. <span data-ttu-id="73857-132">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Verkoopprijs (onkosten).</span><span class="sxs-lookup"><span data-stu-id="73857-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="73857-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="73857-133">Click New.</span></span>
22. <span data-ttu-id="73857-134">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="73857-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="73857-135">Selecteer een optie in het veld Geldig voor.</span><span class="sxs-lookup"><span data-stu-id="73857-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="73857-136">Voer in het veld Prijscalculatie een getal in.</span><span class="sxs-lookup"><span data-stu-id="73857-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="73857-137">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de meest gedetailleerde verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="73857-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="73857-138">Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73857-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="73857-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="73857-139">Click Save.</span></span>


