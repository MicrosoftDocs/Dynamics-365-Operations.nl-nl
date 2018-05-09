--- 
title: Een inkoopovereenkomst maken
description: Deze procedure begeleidt u door het maken van een inkoopovereenkomst.
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f060346308e7ee1191d0769664648cfe72c22b21
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="2cb32-103">Een inkoopovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="2cb32-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cb32-104">Deze procedure begeleidt u door het maken van een inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="2cb32-105">Dit wordt gewoonlijk gedaan door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="2cb32-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="2cb32-106">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="2cb32-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="2cb32-107">U moet de classificaties van inkoopovereenkomsten hebben ingesteld voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="2cb32-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="2cb32-108">Nadat u een overeenkomst hebt gemaakt, kunt u deze gebruiken wanneer u een inkooporder maakt. De voorwaarden van de inkoopovereenkomst worden dan gekopieerd naar de koptekst en naar regels in de order die door de overeenkomst worden beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="2cb32-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="2cb32-109">Een nieuwe inkoopovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="2cb32-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="2cb32-110">Ga naar Inkoop en sourcing > Inkoopovereenkomsten > Inkoopovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="2cb32-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="2cb32-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2cb32-111">Click New.</span></span>
3. <span data-ttu-id="2cb32-112">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2cb32-113">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2cb32-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2cb32-115">Klik in het veld Classificatie van inkoopovereenkomst op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2cb32-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2cb32-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2cb32-118">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="2cb32-118">Expand the General section.</span></span>
10. <span data-ttu-id="2cb32-119">Voer een datum in het veld Vervaldatum in.</span><span class="sxs-lookup"><span data-stu-id="2cb32-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="2cb32-120">Deze vervaldatum wordt de standaardwaarde voor alle toezeggingsregels zijn en bepaalt hoe lang elke specifieke toezegging geldig is.</span><span class="sxs-lookup"><span data-stu-id="2cb32-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="2cb32-121">Typ in het veld Documenttitel een naam voor uw inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="2cb32-122">Laat het veld Standaardtoezegging ingesteld op Toezegging producthoeveelheid (of wijzig het als het hier niet op is ingesteld).</span><span class="sxs-lookup"><span data-stu-id="2cb32-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="2cb32-123">De waarde van de standaardtoezegging bepaalt uw opties op de overeenkomstregels.</span><span class="sxs-lookup"><span data-stu-id="2cb32-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="2cb32-124">Als u een nieuw toezeggingstype nodig hebt wanneer u de overeenkomstregels maakt, moet u de standaardtoezegging in de koptekst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="2cb32-125">Er zijn 4 typen toezeggingen: Toezegging producthoeveelheid - voor een bepaalde hoeveelheid van een product; Toezegging productwaarde - voor een specifiek valutabedrag van een product; Waardetoezegging productcategorie - voor een specifiek valutabedrag in een aanschaffingscategorie waar het bedrag voor een catalogusartikel of een niet-catalogus artikel kan zijn; Waardetoezegging - voor een specifiek valutabedrag dat kan worden afgehandeld door elk product of elke aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="2cb32-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="2cb32-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2cb32-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="2cb32-127">Een toezegging toevoegen</span><span class="sxs-lookup"><span data-stu-id="2cb32-127">Add a commitment</span></span>
1. <span data-ttu-id="2cb32-128">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-128">Click Add line.</span></span>
2. <span data-ttu-id="2cb32-129">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2cb32-130">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2cb32-131">Selecteer het product waarvoor u een toezegging wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="2cb32-132">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2cb32-133">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="2cb32-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2cb32-134">Dit is de totale hoeveelheid die u bent overeengekomen te kopen van uw leverancier.</span><span class="sxs-lookup"><span data-stu-id="2cb32-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="2cb32-135">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="2cb32-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="2cb32-136">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="2cb32-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="2cb32-137">Stel de optie Max is afgedwongen in op Ja.</span><span class="sxs-lookup"><span data-stu-id="2cb32-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="2cb32-138">De optie Max is afgedwongen beperkt het gebruik van de toezegging.</span><span class="sxs-lookup"><span data-stu-id="2cb32-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="2cb32-139">U kunt slechts maximaal de hoeveelheid kopen die is opgegeven in het veld Hoeveelheid voor de regel.</span><span class="sxs-lookup"><span data-stu-id="2cb32-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="2cb32-140">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="2cb32-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="2cb32-141">Koptekstvoorwaarden toevoegen</span><span class="sxs-lookup"><span data-stu-id="2cb32-141">Add header conditions</span></span>
1. <span data-ttu-id="2cb32-142">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="2cb32-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="2cb32-143">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-143">Click Change view.</span></span>
3. <span data-ttu-id="2cb32-144">Klik op Weergave kopteksten.</span><span class="sxs-lookup"><span data-stu-id="2cb32-144">Click Header view.</span></span>
4. <span data-ttu-id="2cb32-145">Vouw de sectie Voorwaarden uit.</span><span class="sxs-lookup"><span data-stu-id="2cb32-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="2cb32-146">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2cb32-147">De betalingsvoorwaarden van de leverancierrekening worden hier standaard weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2cb32-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="2cb32-148">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2cb32-149">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2cb32-150">Klik in het veld Leveringsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2cb32-151">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2cb32-152">Klik in het veld Levering op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2cb32-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2cb32-153">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2cb32-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="2cb32-154">De verkoopovereenkomst bevestigen en activeren</span><span class="sxs-lookup"><span data-stu-id="2cb32-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="2cb32-155">Klik in het actievenster op Inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="2cb32-156">Klik op Bevestiging.</span><span class="sxs-lookup"><span data-stu-id="2cb32-156">Click Confirmation.</span></span>
    * <span data-ttu-id="2cb32-157">Stel de optie Overeenkomst als effectief markeren in op Ja.</span><span class="sxs-lookup"><span data-stu-id="2cb32-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="2cb32-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2cb32-158">Click OK.</span></span>
4. <span data-ttu-id="2cb32-159">Klik in het actievenster op Inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="2cb32-160">Klik op Bevestigingen van inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="2cb32-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="2cb32-161">Met de optie Voorbeeld/afdrukken kunt u een document voor de inkoopovereenkomst genereren dat u vervolgens kunt afdrukken of naar de leverancier kunt verzenden.</span><span class="sxs-lookup"><span data-stu-id="2cb32-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="2cb32-162">Als u de overeenkomst later wilt bijwerken en opnieuw wilt bevestigen, worden hier beide versies weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2cb32-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="2cb32-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2cb32-163">Close the page.</span></span>


