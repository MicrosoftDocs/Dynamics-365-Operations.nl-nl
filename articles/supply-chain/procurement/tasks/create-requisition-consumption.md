--- 
title: Een bestelaanvraag voor verbruik maken
description: Deze procedure begeleidt u door het proces voor het maken van een bestelaanvraag.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07fe007005fcbbac1beecadb14dbd752376a0bd4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="d1569-103">Een bestelaanvraag voor verbruik maken</span><span class="sxs-lookup"><span data-stu-id="d1569-103">Create a requisition for consumption</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1569-104">Deze procedure begeleidt u door het proces voor het maken van een bestelaanvraag.</span><span class="sxs-lookup"><span data-stu-id="d1569-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="d1569-105">Het toont u verschillende manieren om producten in uw aanschaffingscatalogus te zoeken en hoe u een product toevoegt dat niet in uw catalogus staat.</span><span class="sxs-lookup"><span data-stu-id="d1569-105">It shows you different ways to search for products in your procurement catalogue and how to add a product that isn’t in your catalogue.</span></span> <span data-ttu-id="d1569-106">Voordat u deze procedure start, moet u een inkoopbeleid instellen met Verbruik als standaardtype bestelaanvraag.</span><span class="sxs-lookup"><span data-stu-id="d1569-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="d1569-107">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d1569-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="d1569-108">De procedure kan alleen via een gebruikersprofiel worden uitgevoerd dat is ingesteld als werknemer.</span><span class="sxs-lookup"><span data-stu-id="d1569-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="d1569-109">Deze taak moet doorgaans worden uitgevoerd door een werknemer.</span><span class="sxs-lookup"><span data-stu-id="d1569-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="d1569-110">De werknemersrol Werknemer staat toe dat u de taken uitvoert. Als u USMF gebruikt, kunt u zich ook aanmelden als Alicia.</span><span class="sxs-lookup"><span data-stu-id="d1569-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="d1569-111">Een nieuwe bestelaanvraag maken</span><span class="sxs-lookup"><span data-stu-id="d1569-111">Create a new requisition</span></span>
1. <span data-ttu-id="d1569-112">Ga naar Inkoop en sourcing > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten.</span><span class="sxs-lookup"><span data-stu-id="d1569-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="d1569-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1569-113">Click New.</span></span>
3. <span data-ttu-id="d1569-114">Geef de bestelopdracht een naam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d1569-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="d1569-115">Voer in het veld Aangevraagd een datum in.</span><span class="sxs-lookup"><span data-stu-id="d1569-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="d1569-116">De aangevraagde datum en boekhoudingsdatums worden standaard gekopieerd naar de regels van de opdracht tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="d1569-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="d1569-117">Ze kunnen worden gewijzigd op regelniveau.</span><span class="sxs-lookup"><span data-stu-id="d1569-117">They can be changed at the line level.</span></span> <span data-ttu-id="d1569-118">De gevraagde datum is de gevraagde leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="d1569-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="d1569-119">Voer in het veld Boekingsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="d1569-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d1569-120">De boekhoudingsdatum wordt gebruikt om de boeking in het grootboek te registeren en om te valideren dat de budgetfondsen beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="d1569-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="d1569-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d1569-121">Click OK.</span></span>
7. <span data-ttu-id="d1569-122">Klik in het veld Reden op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d1569-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d1569-123">De zakelijke reden die u selecteert, verschijnt standaard voor de regels van de opdracht tot inkoop, maar u kunt deze op regelniveau wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d1569-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="d1569-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d1569-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d1569-125">Selecteer de reden</span><span class="sxs-lookup"><span data-stu-id="d1569-125">Select the reason</span></span>
10. <span data-ttu-id="d1569-126">Voer in het detailveld een meer beschrijvende reden voor de bestelaanvraag in</span><span class="sxs-lookup"><span data-stu-id="d1569-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="d1569-127">Een regel toevoegen aan de bestelaanvraag</span><span class="sxs-lookup"><span data-stu-id="d1569-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="d1569-128">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d1569-128">Click Add line.</span></span>
    * <span data-ttu-id="d1569-129">Er zijn twee manieren om regels aan de opdracht tot inkoop toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d1569-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="d1569-130">Als u het productnummer al kent of al weet dat u een product aanvraagt dat niet in de productcatalogus staat, kunt u de regel direct toevoegen met 'Regel toevoegen'.</span><span class="sxs-lookup"><span data-stu-id="d1569-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalogueue, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="d1569-131">De andere manier is 'Producten toevoegen' gebruiken, waarbij u kunt zoeken en filteren om artikelen in de productcatalogus te vinden.</span><span class="sxs-lookup"><span data-stu-id="d1569-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalogueue.</span></span>    
2. <span data-ttu-id="d1569-132">Klik op de rij die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d1569-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="d1569-133">De aanvrager is de werknemer die de bestelaanvraag heeft gedaan.</span><span class="sxs-lookup"><span data-stu-id="d1569-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="d1569-134">Standaard is de persoon die de bestelaanvraag voorbereidt de werknemer die deze heeft aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="d1569-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="d1569-135">U moet gemachtigd worden om een bestelaanvraagregel voor te bereiden namens een andere werknemer.</span><span class="sxs-lookup"><span data-stu-id="d1569-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="d1569-136">Als u dergelijke machtigingen hebt, worden de andere werknemers in deze zoekopdracht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d1569-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="d1569-137">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="d1569-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d1569-138">De artikelen die u kunt kiezen, worden beperkt door het categorietoegangsbeleid en de aanschaffingscatalogus voor de kopende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d1569-138">The items that are available for you to choose are limited by the category access policy and the procurement catalogue for the buying legal entity.</span></span>   
4. <span data-ttu-id="d1569-139">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="d1569-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="d1569-140">Meer producten toevoegen aan de bestelaanvraag</span><span class="sxs-lookup"><span data-stu-id="d1569-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="d1569-141">Klik op Producten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d1569-141">Click Add products.</span></span>
    * <span data-ttu-id="d1569-142">Dit is de optie waar u producten kunt zoeken in de productcatalogus.</span><span class="sxs-lookup"><span data-stu-id="d1569-142">This is the option where you can search for products in the product catalogueue.</span></span>    
2. <span data-ttu-id="d1569-143">Typ in het veld Aanschaffingscategorieknooppunt zoeken het eerste gedeelte van de naam van de categorie die u zoekt, en klik vervolgens op Enter.</span><span class="sxs-lookup"><span data-stu-id="d1569-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="d1569-144">Typ bijvoorbeeld comput.</span><span class="sxs-lookup"><span data-stu-id="d1569-144">For example, type comput.</span></span>  
3. <span data-ttu-id="d1569-145">Gebruik de InvokeDefaultButton-snelkoppeling.</span><span class="sxs-lookup"><span data-stu-id="d1569-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="d1569-146">Gebruik het filter om de lijst met producten in de geselecteerde categorie te filteren.</span><span class="sxs-lookup"><span data-stu-id="d1569-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="d1569-147">Selecteer de productkaart die u aan de bestelaanvraag wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d1569-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="d1569-148">Klik op Regels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d1569-148">Click Add to lines.</span></span>
7. <span data-ttu-id="d1569-149">Voer een getal in het veld Hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="d1569-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="d1569-150">Typ in het veld Aanschaffingscategorieknooppunt zoeken het eerste gedeelte van de naam van de categorie die u zoekt, en klik vervolgens op Enter.</span><span class="sxs-lookup"><span data-stu-id="d1569-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="d1569-151">Typ bijvoorbeeld Mark (markeerstiften).</span><span class="sxs-lookup"><span data-stu-id="d1569-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="d1569-152">Gebruik de InvokeDefaultButton-snelkoppeling.</span><span class="sxs-lookup"><span data-stu-id="d1569-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="d1569-153">Klik op Niet-vermeld product toevoegen aan regels om een product te voegen dat niet in de aanschaffingscatalogus staat.</span><span class="sxs-lookup"><span data-stu-id="d1569-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalogue.</span></span>
11. <span data-ttu-id="d1569-154">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="d1569-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="d1569-155">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="d1569-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="d1569-156">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d1569-156">Click OK.</span></span>
14. <span data-ttu-id="d1569-157">Voer in het veld Artikelomschrijving een beschrijving van het product in.</span><span class="sxs-lookup"><span data-stu-id="d1569-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="d1569-158">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="d1569-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="d1569-159">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="d1569-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="d1569-160">Als u de prijs weet voor een bepaalde leverancier (die u selecteert in het veld van de leveranciersrekening), kan die prijs worden ingevoerd</span><span class="sxs-lookup"><span data-stu-id="d1569-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="d1569-161">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d1569-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d1569-162">Welke leveranciers in dit veld beschikbaar zijn, is afhankelijk van het inkoopbeleid en de status afdrukken die de leverancier heeft voor de huidige aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="d1569-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="d1569-163">Als alternatief voor het hier selecteren van een leverancier kunt u klikken op de knop Leveranciers voorstellen.</span><span class="sxs-lookup"><span data-stu-id="d1569-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="d1569-164">Selecteer in de lijst de leverancier die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d1569-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="d1569-165">Typ een waarde in het veld Extern-artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="d1569-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="d1569-166">Dit is een verwijzingsnummer voor het product dat bekend is bij de leverancier.</span><span class="sxs-lookup"><span data-stu-id="d1569-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="d1569-167">Het kan bijvoorbeeld het artikelnummer van het product in de eigen catalogus van de leverancier zijn.</span><span class="sxs-lookup"><span data-stu-id="d1569-167">For example, this could be the item number of the product in the vendor's own catalogue.</span></span>  
20. <span data-ttu-id="d1569-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d1569-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="d1569-169">Bedragen verdelen</span><span class="sxs-lookup"><span data-stu-id="d1569-169">Distribute amounts</span></span>
1. <span data-ttu-id="d1569-170">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="d1569-170">Click Financials.</span></span>
2. <span data-ttu-id="d1569-171">Klik op Bedragen verdelen.</span><span class="sxs-lookup"><span data-stu-id="d1569-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="d1569-172">Dit proces toont hoe de kosten voor de eerste regel tussen 2 rekeningen moeten worden gedistribueerd.</span><span class="sxs-lookup"><span data-stu-id="d1569-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="d1569-173">Dit kan ook later worden gedaan wanneer de bestelaanvraag wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d1569-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="d1569-174">Klik op Splitsen om een nieuwe distributieregel te maken.</span><span class="sxs-lookup"><span data-stu-id="d1569-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="d1569-175">Selecteer in het veld Grootboekrekening de eerste kostenplaats die een deel van de kosten moet betalen.</span><span class="sxs-lookup"><span data-stu-id="d1569-175">In the Ledger account field select the first cost centre that should take part of the cost.</span></span>
5. <span data-ttu-id="d1569-176">Selecteer de andere distributieregel.</span><span class="sxs-lookup"><span data-stu-id="d1569-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="d1569-177">Geef in het veld Grootboekrekening de andere kostenplaats op.</span><span class="sxs-lookup"><span data-stu-id="d1569-177">In the Ledger account field specify the other cost centre.</span></span>
7. <span data-ttu-id="d1569-178">Klik op Evenredig verdelen.</span><span class="sxs-lookup"><span data-stu-id="d1569-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="d1569-179">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d1569-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="d1569-180">Regeldetails weergeven</span><span class="sxs-lookup"><span data-stu-id="d1569-180">View line details</span></span>
1. <span data-ttu-id="d1569-181">Schakel de uitbreiding van de sectie Regeldetails om.</span><span class="sxs-lookup"><span data-stu-id="d1569-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="d1569-182">De bestelaanvraag indienen</span><span class="sxs-lookup"><span data-stu-id="d1569-182">Submit the requisition</span></span>
1. <span data-ttu-id="d1569-183">Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="d1569-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="d1569-184">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="d1569-184">Click Submit.</span></span>
3. <span data-ttu-id="d1569-185">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d1569-185">Close the page.</span></span>
4. <span data-ttu-id="d1569-186">Typ in het veld Opmerking een opmerking voor de fiatteur van de bestelaanvraag.</span><span class="sxs-lookup"><span data-stu-id="d1569-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="d1569-187">Klik op Aanbieden.</span><span class="sxs-lookup"><span data-stu-id="d1569-187">Click Submit.</span></span>
6. <span data-ttu-id="d1569-188">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d1569-188">Close the page.</span></span>
7. <span data-ttu-id="d1569-189">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="d1569-189">Refresh the page.</span></span>


