---
title: " Basisprijs en handelsovereenkomsten"
description: Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.
author: josaw1
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df4d0042e51524c1d50568e969b59923a7ba4a65
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789799"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="ec0c3-103"> Basisprijs en handelsovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="ec0c3-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec0c3-104">Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="ec0c3-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="ec0c3-106">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Prijzen- en kortingbeheer > Prijsgroepen > Alle prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="ec0c3-107">Prijsgroepen bepalen hoe handelsovereenkomsten aan specifieke kanalen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="ec0c3-108">Als u prijsgroepen gebruikt om handelsovereenkomsten aan een kanaal toe te wijzen, worden kanaalspecifieke prijzen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="ec0c3-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-109">Click **New**.</span></span>
3. <span data-ttu-id="ec0c3-110">Typ een waarde in het veld **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="ec0c3-111">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ec0c3-112">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-112">Click **Save**.</span></span>
6. <span data-ttu-id="ec0c3-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-113">Close the page.</span></span>
7. <span data-ttu-id="ec0c3-114">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Kanalen > Winkels > Alle detailhandelwinkels**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="ec0c3-115">Selecteer 'New York' in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="ec0c3-116">Klik in het actievenster op **Winkel**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="ec0c3-117">Klik op **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="ec0c3-118">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-118">Click **New**.</span></span>
12. <span data-ttu-id="ec0c3-119">Klik in het veld **Prijsgroepen** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="ec0c3-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="ec0c3-121">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-121">Click **Save**.</span></span>
15. <span data-ttu-id="ec0c3-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-122">Close the page.</span></span>
16. <span data-ttu-id="ec0c3-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-123">Close the page.</span></span>
17. <span data-ttu-id="ec0c3-124">Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Producten en categorieën > Vrijgegeven producten per categorie**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="ec0c3-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="ec0c3-126">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-126">Click **Edit**.</span></span>
20. <span data-ttu-id="ec0c3-127">Vouw het sneltabblad **Verkopen** uit.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="ec0c3-128">Voer een getal in het veld **Prijs** in.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="ec0c3-129">Deze prijs wordt gebruikt als er geen toepasselijke handelsovereenkomsten worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="ec0c3-130">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-130">Click **Save**.</span></span>
23. <span data-ttu-id="ec0c3-131">Klik in het **actievenster** op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="ec0c3-132">Klik op **Handelsovereenkomsten maken**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="ec0c3-133">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-133">Click **New**.</span></span>
26. <span data-ttu-id="ec0c3-134">Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="ec0c3-135">Selecteer **Commerce** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="ec0c3-136">In de demogegevens heeft de **Commerce**-journaalnaam de standaardrelatie **Prijs (verkoop)**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="ec0c3-137">Dat betekent dat alle nieuw gemaakte regels standaard verkoopprijshandelsovereenkomsten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="ec0c3-138">Klik in het **actievenster** op **Regels**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="ec0c3-139">Selecteer 'Groep' in het veld **Type partijcode**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-139">In the **Party code type** field, select 'Group'.</span></span>
30. <span data-ttu-id="ec0c3-140">Klik in het veld **Rekening selecteren** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="ec0c3-141">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="ec0c3-142">Dit voltooit de koppeling van Kanaal naar Prijsgroep naar Handelsovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="ec0c3-143">Typ een waarde in het veld **Artikelrelatie**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="ec0c3-144">Typ een getal in het veld **Bedrag in valuta**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="ec0c3-145">Schakel op het sneltabblad **Details** het selectievakje **Volgende zoeken** in of uit.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="ec0c3-146">Wanneer **Volgende zoeken** is ingesteld op Ja, zoekt de prijsengine door naar toepasselijke handelsovereenkomsten met een lagere verkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="ec0c3-147">Wanneer **Volgende zoeken** is ingesteld op Nee, stopt het zoeken en wordt de handelsovereenkomst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="ec0c3-148">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-148">Click **Post**.</span></span>
36. <span data-ttu-id="ec0c3-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-149">Click **OK**.</span></span>
37. <span data-ttu-id="ec0c3-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-150">Close the page.</span></span>
38. <span data-ttu-id="ec0c3-151">Klik in het actievenster op **Verkopen**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="ec0c3-152">Klik op **Verkoopprijs**.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-152">Click **Sales price**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]