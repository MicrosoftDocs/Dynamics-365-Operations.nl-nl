---
title: Standaardkosten voor arbeid en onkosten configureren
description: In deze procedure wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845878"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="6e1f9-103">Standaardkosten voor arbeid en onkosten configureren</span><span class="sxs-lookup"><span data-stu-id="6e1f9-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e1f9-104">In deze procedure wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="6e1f9-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6e1f9-106">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Kostprijs (uur).</span><span class="sxs-lookup"><span data-stu-id="6e1f9-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="6e1f9-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-107">Click New.</span></span>
3. <span data-ttu-id="6e1f9-108">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="6e1f9-109">Voer in het veld Kostprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="6e1f9-110">U kunt een standaardkostprijs voor de projectcategorie instellen of u kunt een kostprijs instellen per werknemernummer, projectnummer, categorie, datum of elke combinatie van deze factoren.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="6e1f9-111">De kostprijs met het hoogste detailniveau wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="6e1f9-112">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-112">Click Save.</span></span>
6. <span data-ttu-id="6e1f9-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-113">Close the page.</span></span>
7. <span data-ttu-id="6e1f9-114">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Verkoopprijs (uur).</span><span class="sxs-lookup"><span data-stu-id="6e1f9-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="6e1f9-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-115">Click New.</span></span>
9. <span data-ttu-id="6e1f9-116">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="6e1f9-117">Selecteer een optie in het veld Geldig voor.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="6e1f9-118">Voer in het veld Prijscalculatie een getal in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="6e1f9-119">U kunt een standaardverkoopprijs definiëren voor uurtransacties of voor een projectcategorie.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="6e1f9-120">U kunt ook verkoopprijzen instellen per werknemernummer, projectnummer, categorie, transactiedatum of een combinatie van deze.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="6e1f9-121">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het Urenjournaal, is de verkoopprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6e1f9-122">Als er bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs is gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="6e1f9-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-123">Click Save.</span></span>
13. <span data-ttu-id="6e1f9-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-124">Close the page.</span></span>
14. <span data-ttu-id="6e1f9-125">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Kostprijs (onkosten).</span><span class="sxs-lookup"><span data-stu-id="6e1f9-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="6e1f9-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-126">Click New.</span></span>
16. <span data-ttu-id="6e1f9-127">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="6e1f9-128">Voer in het veld Kostprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="6e1f9-129">Meerdere velden kunnen worden ingevuld, maar dit is het minimum wat nodig is om de record te kunnen opslaan.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="6e1f9-130">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-130">Click Save.</span></span>
19. <span data-ttu-id="6e1f9-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-131">Close the page.</span></span>
20. <span data-ttu-id="6e1f9-132">Ga naar Projectbeheer en boekhouding > Instellen > Prijzen > Verkoopprijs (onkosten).</span><span class="sxs-lookup"><span data-stu-id="6e1f9-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="6e1f9-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-133">Click New.</span></span>
22. <span data-ttu-id="6e1f9-134">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="6e1f9-135">Selecteer een optie in het veld Geldig voor.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="6e1f9-136">Voer in het veld Prijscalculatie een getal in.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="6e1f9-137">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de meest gedetailleerde verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6e1f9-138">Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="6e1f9-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-139">Click Save.</span></span>

