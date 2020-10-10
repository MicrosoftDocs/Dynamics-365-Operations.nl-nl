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
ms.openlocfilehash: 44dc059f7bfc3ba83a375c197ce67f1378a9bc9b
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899344"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="fcb26-103"> Basisprijs en handelsovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="fcb26-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcb26-104">Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="fcb26-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="fcb26-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="fcb26-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="fcb26-106">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Prijzen- en kortingbeheer > Prijsgroepen > Alle prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="fcb26-107">Prijsgroepen bepalen hoe handelsovereenkomsten aan specifieke kanalen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="fcb26-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="fcb26-108">Als u prijsgroepen gebruikt om handelsovereenkomsten aan een kanaal toe te wijzen, worden kanaalspecifieke prijzen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="fcb26-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="fcb26-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-109">Click **New**.</span></span>
3. <span data-ttu-id="fcb26-110">Typ een waarde in het veld **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="fcb26-111">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fcb26-112">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-112">Click **Save**.</span></span>
6. <span data-ttu-id="fcb26-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fcb26-113">Close the page.</span></span>
7. <span data-ttu-id="fcb26-114">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Kanalen > Winkels > Alle detailhandelwinkels**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="fcb26-115">Selecteer 'New York' in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fcb26-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="fcb26-116">Klik in het actievenster op **Winkel**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="fcb26-117">Klik op **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="fcb26-118">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-118">Click **New**.</span></span>
12. <span data-ttu-id="fcb26-119">Klik in het veld **Prijsgroepen** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcb26-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="fcb26-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fcb26-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="fcb26-121">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-121">Click **Save**.</span></span>
15. <span data-ttu-id="fcb26-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fcb26-122">Close the page.</span></span>
16. <span data-ttu-id="fcb26-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fcb26-123">Close the page.</span></span>
17. <span data-ttu-id="fcb26-124">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Producten en categorieën > Vrijgegeven producten per categorie**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="fcb26-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fcb26-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="fcb26-126">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-126">Click **Edit**.</span></span>
20. <span data-ttu-id="fcb26-127">Vouw het sneltabblad **Verkopen** uit.</span><span class="sxs-lookup"><span data-stu-id="fcb26-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="fcb26-128">Voer een getal in het veld **Prijs** in.</span><span class="sxs-lookup"><span data-stu-id="fcb26-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="fcb26-129">Deze prijs wordt gebruikt als er geen toepasselijke handelsovereenkomsten worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="fcb26-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="fcb26-130">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-130">Click **Save**.</span></span>
23. <span data-ttu-id="fcb26-131">Klik in het **actievenster** op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="fcb26-132">Klik op **Handelsovereenkomsten maken**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="fcb26-133">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-133">Click **New**.</span></span>
26. <span data-ttu-id="fcb26-134">Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcb26-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="fcb26-135">Selecteer **Commerce** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fcb26-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="fcb26-136">In de demogegevens heeft de **Commerce**-journaalnaam de standaardrelatie **Prijs (verkoop)**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="fcb26-137">Dat betekent dat alle nieuw gemaakte regels standaard verkoopprijshandelsovereenkomsten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fcb26-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="fcb26-138">Klik in het **actievenster** op **Regels**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="fcb26-139">Selecteer 'Groep' in het veld **Type partijcode**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-139">In the **Party code type** field, select 'Group'.</span></span>
30. <span data-ttu-id="fcb26-140">Klik in het veld **Rekening selecteren** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcb26-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="fcb26-141">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fcb26-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="fcb26-142">Dit voltooit de koppeling van Kanaal naar Prijsgroep naar Handelsovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="fcb26-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="fcb26-143">Typ een waarde in het veld **Artikelrelatie**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="fcb26-144">Typ een getal in het veld **Bedrag in valuta**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="fcb26-145">Schakel op het sneltabblad **Details** het selectievakje **Volgende zoeken** in of uit.</span><span class="sxs-lookup"><span data-stu-id="fcb26-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="fcb26-146">Wanneer **Volgende zoeken** is ingesteld op Ja, zoekt de prijsengine door naar toepasselijke handelsovereenkomsten met een lagere verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="fcb26-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="fcb26-147">Wanneer **Volgende zoeken** is ingesteld op Nee, stopt het zoeken en wordt de handelsovereenkomst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fcb26-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="fcb26-148">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-148">Click **Post**.</span></span>
36. <span data-ttu-id="fcb26-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-149">Click **OK**.</span></span>
37. <span data-ttu-id="fcb26-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fcb26-150">Close the page.</span></span>
38. <span data-ttu-id="fcb26-151">Klik in het actievenster op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="fcb26-152">Klik op **Verkoopprijs**.</span><span class="sxs-lookup"><span data-stu-id="fcb26-152">Click **Sales price**.</span></span>

