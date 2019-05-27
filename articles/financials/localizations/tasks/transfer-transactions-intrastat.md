---
title: Transacties overboeken naar Intrastat
description: Deze procedure begeleidt u bij het instellen van Intrastat-parameters en overboeken van transacties naar Intrastat.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0e332d5cae09c5026a64a4463e301a008860bd9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538186"
---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="b4979-103">Transacties overboeken naar Intrastat</span><span class="sxs-lookup"><span data-stu-id="b4979-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4979-104">Deze procedure begeleidt u bij het instellen van Intrastat-parameters en overboeken van transacties naar Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b4979-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="b4979-105">Deze procedure is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="b4979-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="b4979-106">Nieuwe basisproductcodes maken en bestaande basisproductcodes bijwerken</span><span class="sxs-lookup"><span data-stu-id="b4979-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="b4979-107">Ga naar Productgegevensbeheer > Instellingen > Categorieën en kenmerken > Categoriehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="b4979-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="b4979-108">Zoek of selecteer in de lijst de record "Intrastat-basisproductcodes".</span><span class="sxs-lookup"><span data-stu-id="b4979-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="b4979-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b4979-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b4979-110">Selecteer 'een record' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="b4979-111">Selecteer bijvoorbeeld 'Luidspreker van Intrastat'.</span><span class="sxs-lookup"><span data-stu-id="b4979-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="b4979-112">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b4979-112">Click Edit.</span></span>
6. <span data-ttu-id="b4979-113">Vouw de sectie Buitenlandse handel uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="b4979-114">Typ of selecteer een waarde in het veld Extra eenheden.</span><span class="sxs-lookup"><span data-stu-id="b4979-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-115">Kies bijvoorbeeld 'stuks'.</span><span class="sxs-lookup"><span data-stu-id="b4979-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="b4979-116">Selecteer Ja in het veld Gewicht niet van toepassing.</span><span class="sxs-lookup"><span data-stu-id="b4979-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="b4979-117">Selecteer 'Intrastat' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="b4979-118">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="b4979-118">Click New category node.</span></span>
11. <span data-ttu-id="b4979-119">Voer de naam van het basisproduct in het veld Naam in.</span><span class="sxs-lookup"><span data-stu-id="b4979-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="b4979-120">Typ bijvoorbeeld 'Ander basisproduct'.</span><span class="sxs-lookup"><span data-stu-id="b4979-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="b4979-121">Voer de basisproductcode in het veld Code in.</span><span class="sxs-lookup"><span data-stu-id="b4979-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="b4979-122">Typ bijvoorbeeld '995 00 00'.</span><span class="sxs-lookup"><span data-stu-id="b4979-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="b4979-123">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="b4979-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="b4979-124">Typ bijvoorbeeld 'Overige'.</span><span class="sxs-lookup"><span data-stu-id="b4979-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="b4979-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b4979-125">Click Save.</span></span>
15. <span data-ttu-id="b4979-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b4979-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="b4979-127">Basisproductcodes toewijzen aan producthiërarchie en vrijgegeven product</span><span class="sxs-lookup"><span data-stu-id="b4979-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="b4979-128">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="b4979-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b4979-129">Filter bijvoorbeeld op het veld Naam met de waarde 'verkoop'.</span><span class="sxs-lookup"><span data-stu-id="b4979-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="b4979-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b4979-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b4979-131">Vouw 'een categorieknooppunt' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="b4979-132">Vouw bijvoorbeeld 'Verkoophiërarchie\Home audio' uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="b4979-133">Selecteer 'de categorie om aan de basisproductcode toe te wijzen' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="b4979-134">Selecteer bijvoorbeeld 'Verkoophiërarchie\Home audio\Luidsprekers'.</span><span class="sxs-lookup"><span data-stu-id="b4979-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="b4979-135">Vouw de sectie Basisproductcodes uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="b4979-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b4979-136">Click Add.</span></span>
7. <span data-ttu-id="b4979-137">Selecteer 'Intrastat' in het veld Hiërarchie selecteren.</span><span class="sxs-lookup"><span data-stu-id="b4979-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="b4979-138">Zoek en selecteer de basisproductcode in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b4979-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="b4979-139">Selecteer bijvoorbeeld 'Luidspreker van 920 20 34'.</span><span class="sxs-lookup"><span data-stu-id="b4979-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="b4979-140">Klik op SelectCodes.</span><span class="sxs-lookup"><span data-stu-id="b4979-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="b4979-141">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-141">Click OK.</span></span>
11. <span data-ttu-id="b4979-142">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="b4979-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="b4979-143">Kies in de lijst het vrijgegeven product dat u aan de basisproductcode toewijst.</span><span class="sxs-lookup"><span data-stu-id="b4979-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="b4979-144">Kies bijvoorbeeld 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="b4979-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="b4979-145">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b4979-145">Click Edit.</span></span>
14. <span data-ttu-id="b4979-146">Vouw de sectie Buitenlandse handel uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="b4979-147">Voer de basisproductcode in het veld Basisproduct in.</span><span class="sxs-lookup"><span data-stu-id="b4979-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="b4979-148">Selecteer bijvoorbeeld de waarde 'Luidspreker 920 20 34'.</span><span class="sxs-lookup"><span data-stu-id="b4979-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="b4979-149">Voer een getal in het veld Percentage van toeslagen in.</span><span class="sxs-lookup"><span data-stu-id="b4979-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="b4979-150">Voer bijvoorbeeld '3' in:</span><span class="sxs-lookup"><span data-stu-id="b4979-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="b4979-151">Typ of selecteer in het veld Land/regio een land of regio van herkomst</span><span class="sxs-lookup"><span data-stu-id="b4979-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="b4979-152">Selecteer bijvoorbeeld 'AUT'.</span><span class="sxs-lookup"><span data-stu-id="b4979-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="b4979-153">Vouw de sectie Voorraad beheren uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="b4979-154">Voer een gewicht in kg in het veld Nettogewicht in.</span><span class="sxs-lookup"><span data-stu-id="b4979-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="b4979-155">Voer bijvoorbeeld '2,5' in:</span><span class="sxs-lookup"><span data-stu-id="b4979-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="b4979-156">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b4979-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="b4979-157">Intrastat-transactiecodes en parameters voor buitenlandse handel instellen</span><span class="sxs-lookup"><span data-stu-id="b4979-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="b4979-158">Ga naar Belasting > Instellingen > Buitenlandse handel > Transactiecodes</span><span class="sxs-lookup"><span data-stu-id="b4979-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="b4979-159">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b4979-159">Click New.</span></span>
3. <span data-ttu-id="b4979-160">Typ een waarde in het veld Transactiecode.</span><span class="sxs-lookup"><span data-stu-id="b4979-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="b4979-161">Voer bijvoorbeeld '21' in voor de transactiecode die is gebruikt als retour.</span><span class="sxs-lookup"><span data-stu-id="b4979-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="b4979-162">Typ de naam van de transactiecode in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b4979-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="b4979-163">Voer bijvoorbeeld 'Retour' in.</span><span class="sxs-lookup"><span data-stu-id="b4979-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="b4979-164">Selecteer een optie in het veld Statistisch bedrag.</span><span class="sxs-lookup"><span data-stu-id="b4979-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="b4979-165">Selecteer bijvoorbeeld 'Leeg' waarmee wordt aangegeven dat de statistische waarde die voor transacties met transactiecode "21" moet worden gerapporteerd, altijd nul is.</span><span class="sxs-lookup"><span data-stu-id="b4979-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="b4979-166">Ga naar Belasting > Instellingen > Buitenlandse handel > Parameters buitenlandse handel</span><span class="sxs-lookup"><span data-stu-id="b4979-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="b4979-167">Typ of selecteer een waarde in het veld Transactiecode.</span><span class="sxs-lookup"><span data-stu-id="b4979-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-168">Selecteer bijvoorbeeld '11'.</span><span class="sxs-lookup"><span data-stu-id="b4979-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="b4979-169">Typ of selecteer een waarde in het veld Creditnota.</span><span class="sxs-lookup"><span data-stu-id="b4979-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-170">Met deze waarde wordt ook de fysieke retour geïdentificeerd.</span><span class="sxs-lookup"><span data-stu-id="b4979-170">This value also identifies the physical return.</span></span> <span data-ttu-id="b4979-171">De creditnota voor de fysieke retour wordt in het Intrastat-journaal in tegengestelde richting overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="b4979-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="b4979-172">De retour van aankomst wordt bijvoorbeeld overgeboekt als verzending.</span><span class="sxs-lookup"><span data-stu-id="b4979-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="b4979-173">Anders wordt de creditnota als een correctie beschouwd en wordt deze in dezelfde richting en met het tegengesteld teken overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="b4979-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="b4979-174">De correctie van aankomst wordt overgeboekt als een aankomst met negatief bedrag en de actieve markering wordt ingesteld op "Correctie".</span><span class="sxs-lookup"><span data-stu-id="b4979-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="b4979-175">Vouw de sectie Overboeken uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="b4979-176">Selecteer Ja in het veld Artikelen met basisproductcode.</span><span class="sxs-lookup"><span data-stu-id="b4979-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="b4979-177">Selecteer deze optie om alleen de transacties met een toegewezen basisproductcode over te boeken.</span><span class="sxs-lookup"><span data-stu-id="b4979-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="b4979-178">Transacties zonder een basisproductcode worden niet overgeboekt naar Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b4979-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="b4979-179">Selecteer een optie in het veld Overboeken bij overeenkomst met criterium voor.</span><span class="sxs-lookup"><span data-stu-id="b4979-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="b4979-180">Selecteer bijvoorbeeld 'Een van de geselecteerde elementen'.</span><span class="sxs-lookup"><span data-stu-id="b4979-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="b4979-181">Vouw de sectie Hiërarchie van basisproductcodes uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="b4979-182">Klik op het tabblad Land-/regio-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="b4979-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="b4979-183">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b4979-183">Click New.</span></span>
15. <span data-ttu-id="b4979-184">Typ of selecteer een waarde in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="b4979-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-185">Selecteer bijvoorbeeld de waarde 'FRA'.</span><span class="sxs-lookup"><span data-stu-id="b4979-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="b4979-186">Voer in het veld Intrastat-code de ISO-code voor het land in.</span><span class="sxs-lookup"><span data-stu-id="b4979-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="b4979-187">Typ bijvoorbeeld 'FR'.</span><span class="sxs-lookup"><span data-stu-id="b4979-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="b4979-188">Selecteer 'EU' in het veld Land-/regiotype.</span><span class="sxs-lookup"><span data-stu-id="b4979-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="b4979-189">Klik op het tabblad Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="b4979-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="b4979-190">Leveringsmethoden en regels instellen voor opname van toeslagen in Intrastat</span><span class="sxs-lookup"><span data-stu-id="b4979-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="b4979-191">Ga naar Verkoop en marketing > Instellingen > Distributie > Leveringsmethoden</span><span class="sxs-lookup"><span data-stu-id="b4979-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="b4979-192">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b4979-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b4979-193">Selecteer bijvoorbeeld '20 Air'.</span><span class="sxs-lookup"><span data-stu-id="b4979-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="b4979-194">Vouw de sectie Buitenlandse handel uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="b4979-195">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b4979-195">Click Edit.</span></span>
5. <span data-ttu-id="b4979-196">Typ of selecteer een waarde in het veld Transport.</span><span class="sxs-lookup"><span data-stu-id="b4979-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-197">Selecteer bijvoorbeeld '02'.</span><span class="sxs-lookup"><span data-stu-id="b4979-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="b4979-198">Ga naar Klanten > Instelling van toeslagen > Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="b4979-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="b4979-199">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="b4979-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b4979-200">Filter bijvoorbeeld op het veld Toeslagcode met de waarde 'vracht'.</span><span class="sxs-lookup"><span data-stu-id="b4979-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="b4979-201">Vouw de sectie Buitenlandse handel uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="b4979-202">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b4979-202">Click Edit.</span></span>
10. <span data-ttu-id="b4979-203">Selecteer Ja in het veld Intrastat-factuurwaarde.</span><span class="sxs-lookup"><span data-stu-id="b4979-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="b4979-204">Het bedrag wordt overgeboekt naar het veld Factuurtoeslagen en wordt samengevat met het bedrag dat in het veld Factuurbedrag is overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="b4979-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="b4979-205">Selecteer Ja in het veld Statistische Intrastat-waarde als het bedrag van wijzigingen naar het veld Statistische toeslagen moet worden overgeboekt en samengevat met het statistische bedrag.</span><span class="sxs-lookup"><span data-stu-id="b4979-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="b4979-206">Producten verkopen voor klanten in de EU</span><span class="sxs-lookup"><span data-stu-id="b4979-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="b4979-207">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="b4979-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b4979-208">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b4979-208">Click New.</span></span>
3. <span data-ttu-id="b4979-209">Selecteer een EU-klant in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="b4979-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="b4979-210">Selecteer bijvoorbeeld "DE-012 Litware Retail".</span><span class="sxs-lookup"><span data-stu-id="b4979-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="b4979-211">Vouw de sectie Levering uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="b4979-212">Typ of selecteer een waarde in het veld Leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="b4979-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-213">Selecteer bijvoorbeeld '20 Air'.</span><span class="sxs-lookup"><span data-stu-id="b4979-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="b4979-214">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-214">Click OK.</span></span>
7. <span data-ttu-id="b4979-215">Plaats de cursor op de eerste rij van verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="b4979-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="b4979-216">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="b4979-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-217">Selecteer bijvoorbeeld D001.</span><span class="sxs-lookup"><span data-stu-id="b4979-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="b4979-218">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="b4979-219">Klik op het tabblad Buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="b4979-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="b4979-220">Het transport wordt automatisch ingevuld op basis van de gekozen leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="b4979-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="b4979-221">Typ of selecteer een waarde in het veld Haven.</span><span class="sxs-lookup"><span data-stu-id="b4979-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="b4979-222">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="b4979-222">Click Financials.</span></span>
    * <span data-ttu-id="b4979-223">Op basis van de instellingen wordt dit bedrag opgenomen in de Intrastat-factuurwaarde.</span><span class="sxs-lookup"><span data-stu-id="b4979-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="b4979-224">Klik op Toeslagen onderhouden.</span><span class="sxs-lookup"><span data-stu-id="b4979-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="b4979-225">Typ of selecteer een waarde in het veld Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="b4979-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-226">Selecteer bijvoorbeeld 'VRACHT'.</span><span class="sxs-lookup"><span data-stu-id="b4979-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="b4979-227">Schakel het selectievakje Behouden in.</span><span class="sxs-lookup"><span data-stu-id="b4979-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="b4979-228">Voer een nummer in het veld Waarde van toeslagen in.</span><span class="sxs-lookup"><span data-stu-id="b4979-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="b4979-229">Voer bijvoorbeeld 10 in:</span><span class="sxs-lookup"><span data-stu-id="b4979-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="b4979-230">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b4979-230">Click Save.</span></span>
18. <span data-ttu-id="b4979-231">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b4979-231">Close the page.</span></span>
19. <span data-ttu-id="b4979-232">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="b4979-233">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-233">Click Invoice.</span></span>
21. <span data-ttu-id="b4979-234">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="b4979-235">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="b4979-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="b4979-236">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="b4979-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="b4979-237">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="b4979-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="b4979-238">Voer bijvoorbeeld '2015-01-31' in.</span><span class="sxs-lookup"><span data-stu-id="b4979-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="b4979-239">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-239">Click OK.</span></span>
26. <span data-ttu-id="b4979-240">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-240">Click OK.</span></span>
27. <span data-ttu-id="b4979-241">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b4979-241">Close the page.</span></span>
28. <span data-ttu-id="b4979-242">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b4979-242">Click New.</span></span>
29. <span data-ttu-id="b4979-243">Selecteer een EU-klant in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="b4979-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="b4979-244">Selecteer bijvoorbeeld 'DE-013 Trey Wholesales'</span><span class="sxs-lookup"><span data-stu-id="b4979-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="b4979-245">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-245">Click OK.</span></span>
31. <span data-ttu-id="b4979-246">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="b4979-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b4979-247">Selecteer bijvoorbeeld 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="b4979-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="b4979-248">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b4979-248">Click Save.</span></span>
33. <span data-ttu-id="b4979-249">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-249">Click Invoice.</span></span>
34. <span data-ttu-id="b4979-250">Voer een datum in het veld Factuurdatum in.</span><span class="sxs-lookup"><span data-stu-id="b4979-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="b4979-251">Typ of selecteer bijvoorbeeld de datum '31-01-2015'.</span><span class="sxs-lookup"><span data-stu-id="b4979-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="b4979-252">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-252">Click OK.</span></span>
36. <span data-ttu-id="b4979-253">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="b4979-254">Transacties overboeken naar Intrastat</span><span class="sxs-lookup"><span data-stu-id="b4979-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="b4979-255">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b4979-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="b4979-256">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="b4979-256">Click Transfer.</span></span>
3. <span data-ttu-id="b4979-257">Selecteer Ja in het veld Klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="b4979-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="b4979-258">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="b4979-258">Click Filter.</span></span>
5. <span data-ttu-id="b4979-259">Markeer in de lijst de rij met Datum.</span><span class="sxs-lookup"><span data-stu-id="b4979-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="b4979-260">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="b4979-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b4979-261">Voer bijvoorbeeld het filter voor de periode januari 2015 in (de exacte waarde is afhankelijk van uw datumnotatie): 1-1-2015..31-1-2015</span><span class="sxs-lookup"><span data-stu-id="b4979-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="b4979-262">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-262">Click OK.</span></span>
8. <span data-ttu-id="b4979-263">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4979-263">Click OK.</span></span>
9. <span data-ttu-id="b4979-264">Zoek en selecteer de overgeboekte record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b4979-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="b4979-265">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="b4979-265">Click the General tab.</span></span>
    * <span data-ttu-id="b4979-266">Controleer de overgeboekte gegevens, waaronder land/regio van bestemming/verzending, land van oorsprong, gewicht, hoeveelheid, hoeveelheid in extra eenheden, basisproduct, transactiecode, factuurbedragen en statistische bedragen.</span><span class="sxs-lookup"><span data-stu-id="b4979-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="b4979-267">U kunt gegevens indien nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b4979-267">You can modify data if necessary.</span></span>  

