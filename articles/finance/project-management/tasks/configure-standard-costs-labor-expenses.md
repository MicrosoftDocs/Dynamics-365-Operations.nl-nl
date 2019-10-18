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
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185400"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="c26ec-103">Standaardkosten voor arbeid en onkosten configureren</span><span class="sxs-lookup"><span data-stu-id="c26ec-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c26ec-104">In dit onderwerp wordt beschreven hoe u de standaardkosten voor arbeid en onkosten voor een project instelt.</span><span class="sxs-lookup"><span data-stu-id="c26ec-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="c26ec-105">In deze taak wordt de gegevensset van USSI gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c26ec-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c26ec-106">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Kostprijs (uur)**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="c26ec-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-107">Select **New**.</span></span>
3. <span data-ttu-id="c26ec-108">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="c26ec-109">Voer in het veld **Kostprijs** een getal in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c26ec-110">U kunt een standaardkostprijs voor de projectcategorie instellen of u kunt een kostprijs instellen per werknemernummer, projectnummer, categorie, datum of elke combinatie van deze factoren.</span><span class="sxs-lookup"><span data-stu-id="c26ec-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="c26ec-111">De kostprijs met het hoogste detailniveau wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c26ec-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="c26ec-112">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-112">Select **Save**.</span></span>
6. <span data-ttu-id="c26ec-113">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Verkoopprijs (uur)**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="c26ec-114">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-114">Select **New**.</span></span>
8. <span data-ttu-id="c26ec-115">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="c26ec-116">Selecteer een optie in het veld **Geldig voor**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="c26ec-117">Voer in het veld **Prijscalculatie** een getal in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c26ec-118">U kunt een standaardverkoopprijs definiëren voor uurtransacties of voor een projectcategorie.</span><span class="sxs-lookup"><span data-stu-id="c26ec-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="c26ec-119">U kunt ook verkoopprijzen instellen per werknemernummer, projectnummer, categorie, transactiedatum of een combinatie van deze.</span><span class="sxs-lookup"><span data-stu-id="c26ec-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="c26ec-120">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het Urenjournaal, is de verkoopprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="c26ec-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c26ec-121">Als er bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs is gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c26ec-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="c26ec-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-122">Select **Save**.</span></span>
12. <span data-ttu-id="c26ec-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c26ec-123">Close the page.</span></span>
13. <span data-ttu-id="c26ec-124">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Kostprijs (onkosten)**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="c26ec-125">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-125">Select **New**.</span></span>
15. <span data-ttu-id="c26ec-126">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="c26ec-127">Voer in het veld **Kostprijs** een getal in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c26ec-128">Meerdere velden kunnen worden ingevuld, maar dit is het minimum wat nodig is om de record te kunnen opslaan.</span><span class="sxs-lookup"><span data-stu-id="c26ec-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="c26ec-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-129">Select **Save**.</span></span>
18. <span data-ttu-id="c26ec-130">Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Instellingen > Prijzen > Verkoopprijs (onkosten)**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="c26ec-131">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-131">Select **New**.</span></span>
20. <span data-ttu-id="c26ec-132">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="c26ec-133">Selecteer een optie in het veld **Geldig voor**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="c26ec-134">Voer in het veld **Prijscalculatie** een getal in.</span><span class="sxs-lookup"><span data-stu-id="c26ec-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c26ec-135">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de meest gedetailleerde verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="c26ec-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c26ec-136">Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn gedefinieerd, wordt de werknemerspecifieke prijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c26ec-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="c26ec-137">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-137">Select **Save**.</span></span>
