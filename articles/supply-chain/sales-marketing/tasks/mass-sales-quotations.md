---
title: Verkoopoffertes massaal maken
description: Deze procedure toont hoe u efficiënt offertes maakt met een reeks producten of services die naar meerdere klanten moeten worden verzonden.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0e9ddf38106fce3ed6a6f908826f2196c97a45a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562110"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="b8603-103">Verkoopoffertes massaal maken</span><span class="sxs-lookup"><span data-stu-id="b8603-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8603-104">Deze procedure toont hoe u efficiënt offertes maakt met een reeks producten of services die naar meerdere klanten moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="b8603-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="b8603-105">Dit groepsgewijs maken van offertes is gebaseerd op offertesjablonen.</span><span class="sxs-lookup"><span data-stu-id="b8603-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="b8603-106">U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="b8603-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="b8603-107">Een offertesjabloon maken</span><span class="sxs-lookup"><span data-stu-id="b8603-107">Create a quotation template</span></span>
1. <span data-ttu-id="b8603-108">Ga naar Verkoop en marketing > Instellen > Offertes > Sjabloongroepen.</span><span class="sxs-lookup"><span data-stu-id="b8603-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="b8603-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b8603-109">Click New.</span></span>
3. <span data-ttu-id="b8603-110">Typ een id van uw keuze in het veld Groep-id.</span><span class="sxs-lookup"><span data-stu-id="b8603-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="b8603-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="b8603-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b8603-112">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b8603-112">Click Save.</span></span>
6. <span data-ttu-id="b8603-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8603-113">Close the page.</span></span>
7. <span data-ttu-id="b8603-114">Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.</span><span class="sxs-lookup"><span data-stu-id="b8603-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="b8603-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b8603-115">Click New.</span></span>
9. <span data-ttu-id="b8603-116">Selecteer in het veld Rekeningtype de optie 'Klant'.</span><span class="sxs-lookup"><span data-stu-id="b8603-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="b8603-117">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="b8603-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="b8603-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b8603-118">Click OK.</span></span>
    * <span data-ttu-id="b8603-119">Een offerte kan alleen een sjabloon worden als u op de offertekoptekst instellingsstappen uitvoert.</span><span class="sxs-lookup"><span data-stu-id="b8603-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="b8603-120">U moet dit doen voordat u regels aan de offerte toevoegt.</span><span class="sxs-lookup"><span data-stu-id="b8603-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="b8603-121">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="b8603-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="b8603-122">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b8603-122">Click Change view.</span></span>
14. <span data-ttu-id="b8603-123">Klik op Weergave kopteksten.</span><span class="sxs-lookup"><span data-stu-id="b8603-123">Click Header view.</span></span>
15. <span data-ttu-id="b8603-124">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="b8603-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="b8603-125">Typ of selecteer een waarde in het veld Groep-id.</span><span class="sxs-lookup"><span data-stu-id="b8603-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="b8603-126">Typ een waarde in het veld Sjabloonnaam.</span><span class="sxs-lookup"><span data-stu-id="b8603-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="b8603-127">Selecteer Ja in het veld Actief.</span><span class="sxs-lookup"><span data-stu-id="b8603-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="b8603-128">U kunt alleen actieve sjablonen gebruiken wanneer u een sjabloon toepast op een nieuwe verkoopofferte.</span><span class="sxs-lookup"><span data-stu-id="b8603-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="b8603-129">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="b8603-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="b8603-130">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b8603-130">Click Change view.</span></span>
21. <span data-ttu-id="b8603-131">Klik op Regelweergave.</span><span class="sxs-lookup"><span data-stu-id="b8603-131">Click Line view.</span></span>
22. <span data-ttu-id="b8603-132">Typ of selecteer een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="b8603-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="b8603-133">Typ een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="b8603-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="b8603-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8603-134">Close the page.</span></span>
25. <span data-ttu-id="b8603-135">Voer in het veld Kortingspercentage een getal in.</span><span class="sxs-lookup"><span data-stu-id="b8603-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="b8603-136">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b8603-136">Click Add line.</span></span>
27. <span data-ttu-id="b8603-137">Typ of selecteer een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="b8603-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="b8603-138">Typ een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="b8603-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="b8603-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8603-139">Close the page.</span></span>
30. <span data-ttu-id="b8603-140">Typ in het veld Eenheidsprijs een nieuwe prijs of wijzig de huidige.</span><span class="sxs-lookup"><span data-stu-id="b8603-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="b8603-141">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b8603-141">Click Add line.</span></span>
32. <span data-ttu-id="b8603-142">Typ of selecteer een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="b8603-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="b8603-143">Typ een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="b8603-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="b8603-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8603-144">Close the page.</span></span>
35. <span data-ttu-id="b8603-145">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="b8603-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="b8603-146">Typ een nummer in het veld Korting.</span><span class="sxs-lookup"><span data-stu-id="b8603-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="b8603-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b8603-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="b8603-148">De sjabloon toepassen om één offerte te maken</span><span class="sxs-lookup"><span data-stu-id="b8603-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="b8603-149">Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.</span><span class="sxs-lookup"><span data-stu-id="b8603-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="b8603-150">De offerte die u zojuist hebt gemaakt is als sjabloon gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="b8603-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="b8603-151">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b8603-151">Click New.</span></span>
3. <span data-ttu-id="b8603-152">Selecteer in het veld Rekeningtype de optie 'Klant'.</span><span class="sxs-lookup"><span data-stu-id="b8603-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="b8603-153">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="b8603-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="b8603-154">Vouw de sectie Sjabloon uit.</span><span class="sxs-lookup"><span data-stu-id="b8603-154">Expand the Template section.</span></span>
6. <span data-ttu-id="b8603-155">Typ of selecteer een waarde in het veld Groep-id.</span><span class="sxs-lookup"><span data-stu-id="b8603-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="b8603-156">Typ of selecteer een waarde in het veld Sjabloonnaam.</span><span class="sxs-lookup"><span data-stu-id="b8603-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="b8603-157">Selecteer 'Op basis van sjabloonwaarden' in het veld Berekeningsmethode.</span><span class="sxs-lookup"><span data-stu-id="b8603-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="b8603-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b8603-158">Click OK.</span></span>
    * <span data-ttu-id="b8603-159">De nieuwe offerte is nu gemaakt, gebaseerd op de gegevens en de voorwaarden van de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="b8603-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="b8603-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8603-160">Close the page.</span></span>
11. <span data-ttu-id="b8603-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8603-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="b8603-162">De sjabloon toepassen om meerdere offertes te maken</span><span class="sxs-lookup"><span data-stu-id="b8603-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="b8603-163">Ga naar Verkoop en marketing > Verkoopoffertes > Bijwerking offerte > Massaal offertes maken.</span><span class="sxs-lookup"><span data-stu-id="b8603-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="b8603-164">Selecteer in het veld Rekeningtype de optie 'Klant'.</span><span class="sxs-lookup"><span data-stu-id="b8603-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="b8603-165">Typ of selecteer een waarde in het veld Groep-id.</span><span class="sxs-lookup"><span data-stu-id="b8603-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="b8603-166">Typ of selecteer een waarde in het veld Sjabloonnaam.</span><span class="sxs-lookup"><span data-stu-id="b8603-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="b8603-167">Selecteer 'Op basis van sjabloonwaarden' in het veld Berekeningsmethode.</span><span class="sxs-lookup"><span data-stu-id="b8603-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="b8603-168">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="b8603-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="b8603-169">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="b8603-169">Click Filter.</span></span>
8. <span data-ttu-id="b8603-170">Stel in het veld Criteria het filter in om een bereik van klanten te dekken die u bij het groepsgewijs maken van deze offerte wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="b8603-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="b8603-171">Gebruik de volgende indeling: 'Klant1. KlantN'.</span><span class="sxs-lookup"><span data-stu-id="b8603-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="b8603-172">U kunt bijvoorbeeld het filter instellen: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="b8603-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="b8603-173">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b8603-173">Click OK.</span></span>
10. <span data-ttu-id="b8603-174">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b8603-174">Click OK.</span></span>
11. <span data-ttu-id="b8603-175">Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.</span><span class="sxs-lookup"><span data-stu-id="b8603-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="b8603-176">Controleer of er offertes zijn gemaakt voor alle klanten die in de routine voor groepsgewijs bijwerken zijn opgegeven, op basis van de geselecteerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="b8603-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

