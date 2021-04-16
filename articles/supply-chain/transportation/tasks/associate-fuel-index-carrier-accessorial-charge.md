---
title: Een brandstofindex aan een vervoerder koppelen als bijkomende toeslag
description: Deze guide laat zien hoe u een bijkomende toewijzing, een bijkomende toeslag van vervoerder en een bijkomend model voor brandstoftoeslag kunt maken en een brandstofindex vervoerder kunt koppelen aan een vervoerder.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf588517930260eaf23a2b917267a44aec479fcc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831525"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="f411d-103">Een brandstofindex aan een vervoerder koppelen als bijkomende toeslag</span><span class="sxs-lookup"><span data-stu-id="f411d-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f411d-104">Deze guide laat zien hoe u een bijkomende toewijzing, een bijkomende toeslag van vervoerder en een bijkomend model voor brandstoftoeslag kunt maken en een brandstofindex vervoerder kunt koppelen aan een vervoerder.</span><span class="sxs-lookup"><span data-stu-id="f411d-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="f411d-105">U moet een brandstofindex van vervoerder instellen voordat u deze guide uitvoert.</span><span class="sxs-lookup"><span data-stu-id="f411d-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="f411d-106">U kunt de guide 'Brandstofindex van een vervoerder instellen' gebruiken om dit te doen.</span><span class="sxs-lookup"><span data-stu-id="f411d-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="f411d-107">Deze instellingstaken worden gewoonlijk uitgevoerd door een logistiek manager.</span><span class="sxs-lookup"><span data-stu-id="f411d-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="f411d-108">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f411d-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="f411d-109">Een model van extra's maken</span><span class="sxs-lookup"><span data-stu-id="f411d-109">Create an accessorial master</span></span>
1. <span data-ttu-id="f411d-110">Ga naar Transportbeheer > Instellingen > Beoordeling > Modellen van extra's.</span><span class="sxs-lookup"><span data-stu-id="f411d-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="f411d-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f411d-111">Click New.</span></span>
3. <span data-ttu-id="f411d-112">Typ een waarde in het veld Model van extra's.</span><span class="sxs-lookup"><span data-stu-id="f411d-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="f411d-113">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f411d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f411d-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f411d-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="f411d-115">Een bijkomende toeslag van vervoerder maken</span><span class="sxs-lookup"><span data-stu-id="f411d-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="f411d-116">Ga naar Transportbeheer > Instellingen > Beoordeling > Bijkomende toeslagen van vervoerder.</span><span class="sxs-lookup"><span data-stu-id="f411d-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="f411d-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f411d-117">Click New.</span></span>
3. <span data-ttu-id="f411d-118">Typ een waarde in het veld Id extra's vervoerder.</span><span class="sxs-lookup"><span data-stu-id="f411d-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="f411d-119">Klik in het veld Vervoerder op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f411d-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f411d-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f411d-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f411d-121">In dit voorbeeld, kiest u vervoer per vrachtwagen.</span><span class="sxs-lookup"><span data-stu-id="f411d-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="f411d-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f411d-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f411d-123">Klik in het veld Vervoerdersservice op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f411d-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f411d-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f411d-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f411d-125">Klik in het veld Model van extra's op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f411d-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f411d-126">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f411d-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f411d-127">In dit voorbeeld, kiest u het nieuw gemaakte Model van extra's.</span><span class="sxs-lookup"><span data-stu-id="f411d-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="f411d-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f411d-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="f411d-129">Een toewijzing van extra's maken</span><span class="sxs-lookup"><span data-stu-id="f411d-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="f411d-130">Klik op Bijkomende toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="f411d-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="f411d-131">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f411d-131">Click New.</span></span>
3. <span data-ttu-id="f411d-132">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f411d-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f411d-133">Schakel de uitbreiding van de sectie Criteria om.</span><span class="sxs-lookup"><span data-stu-id="f411d-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="f411d-134">In de criteria kunt u altijd de brandstoftoeslag toepassen of bijvoorbeeld ervoor kiezen dat deze alleen binnen een bepaalde regio van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="f411d-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="f411d-135">Typ een waarde in het veld Postcode vanaf.</span><span class="sxs-lookup"><span data-stu-id="f411d-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="f411d-136">Typ een waarde in het veld Postcode tot.</span><span class="sxs-lookup"><span data-stu-id="f411d-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="f411d-137">Schakel de uitbreiding van de sectie Berekening om.</span><span class="sxs-lookup"><span data-stu-id="f411d-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="f411d-138">In de berekeningssectie kunt u opgeven hoe de brandstoftoeslag wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="f411d-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="f411d-139">Deze berekening hangt van de eenheid voor extra's die u als basis voor de berekening hebt gekozen.</span><span class="sxs-lookup"><span data-stu-id="f411d-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="f411d-140">Selecteer in het veld Type van kosten van extra's de optie "Brandstoftoeslag".</span><span class="sxs-lookup"><span data-stu-id="f411d-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="f411d-141">Selecteer "Kilometerstand" in het veld Eenheid voor extra's.</span><span class="sxs-lookup"><span data-stu-id="f411d-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="f411d-142">Klik in het veld Regio op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f411d-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f411d-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f411d-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f411d-144">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f411d-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="f411d-145">Het beoordelingsprofiel vervoerder bijwerken</span><span class="sxs-lookup"><span data-stu-id="f411d-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="f411d-146">Ga naar Transportbeheer > Instellingen > Vervoerders > Vervoerders.</span><span class="sxs-lookup"><span data-stu-id="f411d-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="f411d-147">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f411d-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f411d-148">Schakel de uitbreiding van de sectie Beoordelingsprofielen om.</span><span class="sxs-lookup"><span data-stu-id="f411d-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="f411d-149">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="f411d-149">Click Edit.</span></span>
5. <span data-ttu-id="f411d-150">Klik in het veld Brandstofindex vervoerder op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f411d-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f411d-151">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f411d-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f411d-152">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f411d-152">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]