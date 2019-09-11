---
title: " Basisprijs en handelsovereenkomsten"
description: Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8138b6144cc6ba09834f2bfb61cc7334767307d6
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916548"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="f540d-103"> Basisprijs en handelsovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="f540d-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f540d-104">Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="f540d-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="f540d-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="f540d-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="f540d-106">Ga in het **navigatievenster** naar **Modules > Detailhandel en commerce > Prijzen- en kortingbeheer > Prijsgroepen > Alle prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="f540d-106">In the **Navigation pane**, go to **Modules > Retail and commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="f540d-107">Prijsgroepen bepalen hoe handelsovereenkomsten aan specifieke kanalen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f540d-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="f540d-108">Als u prijsgroepen gebruikt om handelsovereenkomsten aan een kanaal toe te wijzen, worden kanaalspecifieke prijzen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f540d-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="f540d-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f540d-109">Click **New**.</span></span>
3. <span data-ttu-id="f540d-110">Typ een waarde in het veld **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="f540d-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="f540d-111">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="f540d-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f540d-112">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f540d-112">Click **Save**.</span></span>
6. <span data-ttu-id="f540d-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f540d-113">Close the page.</span></span>
7. <span data-ttu-id="f540d-114">Ga in het **navigatievenster** naar **Modules >Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels**.</span><span class="sxs-lookup"><span data-stu-id="f540d-114">In the **Navigation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
8. <span data-ttu-id="f540d-115">Selecteer 'New York' in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f540d-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="f540d-116">Klik in het actievenster op **Winkel**.</span><span class="sxs-lookup"><span data-stu-id="f540d-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="f540d-117">Klik op **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="f540d-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="f540d-118">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f540d-118">Click **New**.</span></span>
12. <span data-ttu-id="f540d-119">Klik in het veld **Prijsgroepen** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f540d-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f540d-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f540d-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f540d-121">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f540d-121">Click **Save**.</span></span>
15. <span data-ttu-id="f540d-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f540d-122">Close the page.</span></span>
16. <span data-ttu-id="f540d-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f540d-123">Close the page.</span></span>
17. <span data-ttu-id="f540d-124">Ga in het **navigatievenster** naar **Modules > Detailhandel en commerce > Producten en categorieën > Vrijgegeven producten per categorie**.</span><span class="sxs-lookup"><span data-stu-id="f540d-124">In the **Navigation pane**, go to **Modules > Retail and commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="f540d-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f540d-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="f540d-126">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f540d-126">Click **Edit**.</span></span>
20. <span data-ttu-id="f540d-127">Vouw het sneltabblad **Verkopen** uit.</span><span class="sxs-lookup"><span data-stu-id="f540d-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="f540d-128">Voer een getal in het veld **Prijs** in.</span><span class="sxs-lookup"><span data-stu-id="f540d-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="f540d-129">Deze prijs wordt gebruikt als er geen toepasselijke handelsovereenkomsten worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="f540d-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="f540d-130">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f540d-130">Click **Save**.</span></span>
23. <span data-ttu-id="f540d-131">Klik in het **actievenster** op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="f540d-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="f540d-132">Klik op **Handelsovereenkomsten maken**.</span><span class="sxs-lookup"><span data-stu-id="f540d-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="f540d-133">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f540d-133">Click **New**.</span></span>
26. <span data-ttu-id="f540d-134">Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f540d-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="f540d-135">Selecteer 'Detailhandel' in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f540d-135">In the list, select 'Retail'.</span></span> <span data-ttu-id="f540d-136">In de demogegevens heeft de journaalnaam 'Detailhandel' de standaardrelatie 'Prijs (verkoop)'.</span><span class="sxs-lookup"><span data-stu-id="f540d-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="f540d-137">Dat betekent dat alle nieuw gemaakte regels standaard verkoopprijshandelsovereenkomsten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f540d-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="f540d-138">Klik in het **actievenster** op **Regels**.</span><span class="sxs-lookup"><span data-stu-id="f540d-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="f540d-139">Selecteer Groep in het veld **Rekeningcode**.</span><span class="sxs-lookup"><span data-stu-id="f540d-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="f540d-140">Klik in het veld **Rekening selecteren** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f540d-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="f540d-141">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f540d-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="f540d-142">Dit voltooit de koppeling van Kanaal naar Prijsgroep naar Handelsovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="f540d-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="f540d-143">Typ een waarde in het veld **Artikelrelatie**.</span><span class="sxs-lookup"><span data-stu-id="f540d-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="f540d-144">Typ een getal in het veld **Bedrag in valuta**.</span><span class="sxs-lookup"><span data-stu-id="f540d-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="f540d-145">Schakel op het sneltabblad **Details** het selectievakje **Volgende zoeken** in of uit.</span><span class="sxs-lookup"><span data-stu-id="f540d-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="f540d-146">Wanneer **Volgende zoeken** is ingesteld op Ja, zoekt de prijsengine door naar toepasselijke handelsovereenkomsten met een lagere verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="f540d-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="f540d-147">Wanneer **Volgende zoeken** is ingesteld op Nee, stopt het zoeken en wordt de handelsovereenkomst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f540d-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="f540d-148">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="f540d-148">Click **Post**.</span></span>
36. <span data-ttu-id="f540d-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="f540d-149">Click **OK**.</span></span>
37. <span data-ttu-id="f540d-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f540d-150">Close the page.</span></span>
38. <span data-ttu-id="f540d-151">Klik in het actievenster op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="f540d-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="f540d-152">Klik op **Verkoopprijs**.</span><span class="sxs-lookup"><span data-stu-id="f540d-152">Click **Sales price**.</span></span>

