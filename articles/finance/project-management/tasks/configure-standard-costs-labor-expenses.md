---
title: Standaardkosten voor arbeid en onkosten configureren
description: In dit onderwerp wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140088"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="8cbad-103">Standaardkosten voor arbeid en onkosten configureren</span><span class="sxs-lookup"><span data-stu-id="8cbad-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8cbad-104">In dit onderwerp wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.</span><span class="sxs-lookup"><span data-stu-id="8cbad-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="8cbad-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8cbad-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8cbad-106">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Kostprijs (uur)**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="8cbad-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-107">Select **New**.</span></span>
3. <span data-ttu-id="8cbad-108">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="8cbad-109">Voer in het veld **Kostprijs** een getal in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8cbad-110">U kunt een standaardkostprijs voor de projectcategorie instellen of u kunt een kostprijs instellen per werknemernummer, projectnummer, categorie, datum of elke combinatie van deze factoren.</span><span class="sxs-lookup"><span data-stu-id="8cbad-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="8cbad-111">De kostprijs met het hoogste detailniveau wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="8cbad-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="8cbad-112">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-112">Select **Save**.</span></span>
6. <span data-ttu-id="8cbad-113">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Verkoopprijs (uur)**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="8cbad-114">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-114">Select **New**.</span></span>
8. <span data-ttu-id="8cbad-115">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="8cbad-116">Selecteer een optie in het veld **Geldig voor**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="8cbad-117">Voer in het veld **Prijscalculatie** een getal in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8cbad-118">U kunt een standaardverkoopprijs definiëren voor uurtransacties of voor een projectcategorie.</span><span class="sxs-lookup"><span data-stu-id="8cbad-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="8cbad-119">U kunt ook verkoopprijzen instellen per werknemernummer, projectnummer, categorie, transactiedatum of een combinatie van deze.</span><span class="sxs-lookup"><span data-stu-id="8cbad-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="8cbad-120">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het Urenjournaal, is de verkoopprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="8cbad-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8cbad-121">Als er bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs is gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8cbad-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="8cbad-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-122">Select **Save**.</span></span>
12. <span data-ttu-id="8cbad-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8cbad-123">Close the page.</span></span>
13. <span data-ttu-id="8cbad-124">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Kostprijs (onkosten)**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="8cbad-125">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-125">Select **New**.</span></span>
15. <span data-ttu-id="8cbad-126">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="8cbad-127">Voer in het veld **Kostprijs** een getal in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8cbad-128">Meerdere velden kunnen worden ingevuld, maar dit is het minimum wat nodig is om de record te kunnen opslaan.</span><span class="sxs-lookup"><span data-stu-id="8cbad-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="8cbad-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-129">Select **Save**.</span></span>
18. <span data-ttu-id="8cbad-130">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Verkoopprijs (onkosten)**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="8cbad-131">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-131">Select **New**.</span></span>
20. <span data-ttu-id="8cbad-132">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="8cbad-133">Selecteer een optie in het veld **Geldig voor**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="8cbad-134">Voer in het veld **Prijscalculatie** een getal in.</span><span class="sxs-lookup"><span data-stu-id="8cbad-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8cbad-135">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de meest gedetailleerde verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="8cbad-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8cbad-136">Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8cbad-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="8cbad-137">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8cbad-137">Select **Save**.</span></span>

