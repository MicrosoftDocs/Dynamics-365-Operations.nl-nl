---
title: Vervoerders instellen
description: In dit onderwerp wordt beschreven hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief.
author: ShylaThompson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c292470e6c70af4dfe11bbe324ebcf93438e29d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840456"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="283bc-103">Vervoerders instellen</span><span class="sxs-lookup"><span data-stu-id="283bc-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="283bc-104">In dit onderwerp wordt beschreven hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief.</span><span class="sxs-lookup"><span data-stu-id="283bc-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="283bc-105">Een transportcoördinator kan vervolgens een vervoerder toewijzen aan een inkomende of uitgaande lading.</span><span class="sxs-lookup"><span data-stu-id="283bc-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="283bc-106">Een nieuwe vervoerder maken</span><span class="sxs-lookup"><span data-stu-id="283bc-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="283bc-107">Ga naar **Navigatievenster > Modules > Transportbeheer > Instellingen > Vervoerders > Vervoerders**.</span><span class="sxs-lookup"><span data-stu-id="283bc-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="283bc-108">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="283bc-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="283bc-109">Typ een waarde in het veld **Vervoerder**.</span><span class="sxs-lookup"><span data-stu-id="283bc-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="283bc-110">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="283bc-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="283bc-111">Selecteer in het veld **Modus** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="283bc-112">De algemene informatie voor de vervoerder invullen</span><span class="sxs-lookup"><span data-stu-id="283bc-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="283bc-113">Schakel de uitbreiding van de sectie **Overzicht** om.</span><span class="sxs-lookup"><span data-stu-id="283bc-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="283bc-114">Schakel het selectievakje **Vervoerder activeren** in of uit.</span><span class="sxs-lookup"><span data-stu-id="283bc-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="283bc-115">Selecteer in het veld **Leveranciersrekening** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="283bc-116">Selecteer de leverancierrekening waaraan de vervoerder moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="283bc-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="283bc-117">Selecteer een optie in het veld **Type betalingsmethode transport**.</span><span class="sxs-lookup"><span data-stu-id="283bc-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="283bc-118">Selecteer **Handmatig** om de pagina Transportbetalingsmethode te gebruiken of selecteer **EDI** om de betalingsmethode bij te werken met Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="283bc-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="283bc-119">Schakel het selectievakje **Vervoerdersbeoordeling** activeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="283bc-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="283bc-120">De nodige services voor de vervoerder maken</span><span class="sxs-lookup"><span data-stu-id="283bc-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="283bc-121">Schakel de uitbreiding van de sectie **Services** om.</span><span class="sxs-lookup"><span data-stu-id="283bc-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="283bc-122">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="283bc-122">Select **New**.</span></span>
3. <span data-ttu-id="283bc-123">Typ een waarde in het veld **Vervoerdersservice**.</span><span class="sxs-lookup"><span data-stu-id="283bc-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="283bc-124">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="283bc-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="283bc-125">Selecteer in het veld **Transportmethode** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="283bc-126">Het adres voor de vervoerder instellen (optioneel)</span><span class="sxs-lookup"><span data-stu-id="283bc-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="283bc-127">Schakel de uitbreiding van de sectie **Adressen** om.</span><span class="sxs-lookup"><span data-stu-id="283bc-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="283bc-128">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="283bc-128">Select **New**.</span></span>
3. <span data-ttu-id="283bc-129">Typ een waarde in het veld **Naam of omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="283bc-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="283bc-130">Selecteer in het veld **Land/regio** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="283bc-131">Selecteer in het veld **Postcode** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="283bc-132">Typ een waarde in het veld **Straat**.</span><span class="sxs-lookup"><span data-stu-id="283bc-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="283bc-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="283bc-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="283bc-134">Het tariefprofiel voor de vervoerder instellen</span><span class="sxs-lookup"><span data-stu-id="283bc-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="283bc-135">Schakel de uitbreiding van de sectie **Beoordelingsprofielen** om.</span><span class="sxs-lookup"><span data-stu-id="283bc-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="283bc-136">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="283bc-136">Select **New**.</span></span>
3. <span data-ttu-id="283bc-137">Typ een waarde in het veld **Beoordelingsprofiel**.</span><span class="sxs-lookup"><span data-stu-id="283bc-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="283bc-138">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="283bc-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="283bc-139">Selecteer in het veld **Locatie** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="283bc-140">Selecteer in het veld **Magazijn** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="283bc-141">Selecteer in het veld **Tarief-engine** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="283bc-142">Selecteer de tariefengine die in overeenstemming is met het contract dat u hebt met de vervoerder.</span><span class="sxs-lookup"><span data-stu-id="283bc-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="283bc-143">Selecteer in het veld **Tariefmodel** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="283bc-144">Selecteer in het veld **Engine voor transittijd** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="283bc-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="283bc-145">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="283bc-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]