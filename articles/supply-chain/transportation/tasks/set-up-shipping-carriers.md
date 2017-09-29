--- 
title: Vervoerders instellen
description: Deze procedure laat zien hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief.
author: BibiSp
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
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="c8d5b-103">Vervoerders instellen</span><span class="sxs-lookup"><span data-stu-id="c8d5b-103">Set up shipping carriers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8d5b-104">Deze procedure laat zien hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="c8d5b-105">Een transportcoördinator kan vervolgens een vervoerder toewijzen aan een inkomende of uitgaande lading.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="c8d5b-106">Een nieuwe vervoerder maken</span><span class="sxs-lookup"><span data-stu-id="c8d5b-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="c8d5b-107">Ga naar Transportbeheer > Instellingen > Vervoerders > Vervoerders.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="c8d5b-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-108">Click New.</span></span>
3. <span data-ttu-id="c8d5b-109">Typ een waarde in het veld Vervoerder.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="c8d5b-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c8d5b-111">Klik in het veld Modus op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c8d5b-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c8d5b-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="c8d5b-114">De algemene informatie voor de vervoerder invullen</span><span class="sxs-lookup"><span data-stu-id="c8d5b-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="c8d5b-115">Schakel de uitbreiding van de sectie Overzicht om.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="c8d5b-116">Schakel het selectievakje Vervoerder activeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="c8d5b-117">Klik in het veld Leverancier op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8d5b-118">Selecteer de leverancierrekening waaraan de vervoerder moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="c8d5b-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c8d5b-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c8d5b-121">Selecteer een optie in het veld Type betalingsmethode transport.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="c8d5b-122">Selecteer Handmatig om de pagina Transportbetalingsmethode te gebruiken of selecteer EDI om de betalingsmethode bij te werken met Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="c8d5b-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="c8d5b-123">Schakel het selectievakje Vervoerdersbeoordeling activeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="c8d5b-124">De nodige services voor de vervoerder maken</span><span class="sxs-lookup"><span data-stu-id="c8d5b-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="c8d5b-125">Schakel de uitbreiding van de sectie Services om.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="c8d5b-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-126">Click New.</span></span>
3. <span data-ttu-id="c8d5b-127">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c8d5b-128">Typ een waarde in het veld Vervoerdersservice.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="c8d5b-129">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="c8d5b-130">Klik in het veld Transportmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c8d5b-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c8d5b-132">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="c8d5b-133">Het adres voor de vervoerder instellen (optioneel)</span><span class="sxs-lookup"><span data-stu-id="c8d5b-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="c8d5b-134">Schakel de uitbreiding van de sectie Adressen om.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="c8d5b-135">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-135">Click New.</span></span>
3. <span data-ttu-id="c8d5b-136">Typ een waarde in het veld Naam of omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="c8d5b-137">Klik in het veld Land/regio op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c8d5b-138">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c8d5b-139">Klik in het veld Postcode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c8d5b-140">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c8d5b-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c8d5b-142">Typ een waarde in het veld Straat.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="c8d5b-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="c8d5b-144">Het tariefprofiel voor de vervoerder instellen</span><span class="sxs-lookup"><span data-stu-id="c8d5b-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="c8d5b-145">Schakel de uitbreiding van de sectie Beoordelingsprofielen om.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="c8d5b-146">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-146">Click New.</span></span>
3. <span data-ttu-id="c8d5b-147">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c8d5b-148">Typ een waarde in het veld Beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="c8d5b-149">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="c8d5b-150">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c8d5b-151">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c8d5b-152">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c8d5b-153">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c8d5b-154">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c8d5b-155">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c8d5b-156">Klik in het veld Tariefengine op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8d5b-157">Selecteer de tariefengine die in overeenstemming is met het contract dat u hebt met de vervoerder.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="c8d5b-158">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c8d5b-159">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c8d5b-160">Klik in het veld Tariefmodel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="c8d5b-161">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="c8d5b-162">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c8d5b-163">Klik in het veld Engine voor transittijd op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="c8d5b-164">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="c8d5b-165">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c8d5b-165">Click Save.</span></span>


