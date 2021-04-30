---
title: Kleine pakketten verzenden
description: Dit onderwerp bevat informatie over de functie voor verzending van kleine pakketten. Met deze functie kan Microsoft Dynamics 365 Supply Chain Management gegevens over een verpakte container naar de vervoerder verzenden en vervolgens een verzendlabel, verzendtarief en traceringsnummer terugkrijgen van die vervoerder.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910204"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="e57f5-104">Kleine pakketten verzenden</span><span class="sxs-lookup"><span data-stu-id="e57f5-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e57f5-105">Met de functie voor verzending van kleine pakketten kan Microsoft Dynamics 365 Supply Chain Management rechtstreeks met vervoerders communiceren door een raamwerk te bieden voor communicatie via vervoerders-API's.</span><span class="sxs-lookup"><span data-stu-id="e57f5-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="e57f5-106">Deze functionaliteit is handig wanneer u afzonderlijke verkooporders verzendt via commerciële vervoerders in plaats van containerverzending of LTL-verzending (Geen volledige vrachtwagen/Less Than Truckload).</span><span class="sxs-lookup"><span data-stu-id="e57f5-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="e57f5-107">Met de functie voor verzending van kleine pakketten wordt via een speciale *tarief-engine* met uw vervoerder gecommuniceerd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="e57f5-108">Uw organisatie moet deze tarief-engine ontwikkelen in samenwerking met uw vervoerder of vervoerdershubservice.</span><span class="sxs-lookup"><span data-stu-id="e57f5-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="e57f5-109">Met de tarief-engine kan Supply Chain Management gegevens over een verpakte container naar uw vervoerder verzenden en vervolgens een verzendlabel, verzendtarief en traceringsnummer terugkrijgen van die vervoerder.</span><span class="sxs-lookup"><span data-stu-id="e57f5-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="e57f5-110">Het verzendtarief dat wordt geretourneerd, wordt als een diverse toeslag aan de gekoppelde verkooporder toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="e57f5-111">Het verzendlabel dat wordt geretourneerd, kan vervolgens automatisch worden afgedrukt met een ZPL-printer (Zebra Programming Language) en op de zending worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e57f5-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="e57f5-112">De vervoerder scant dit verzendlabel wanneer de pakketten in uw magazijn worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="e57f5-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="e57f5-113">Uw systeem voorbereiden op ondersteuning van verzending van kleine pakketten</span><span class="sxs-lookup"><span data-stu-id="e57f5-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="e57f5-114">Voordat u de functie voor verzending van kleine pakketten kunt gaan gebruiken, moet u deze functie in Functiebeheer inschakelen, uw tarief-engine toevoegen en de modules **Transportbeheer** en **Magazijnbeheer** instellen om deze te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="e57f5-115">De functie voor verzending van kleine pakketten inschakelen</span><span class="sxs-lookup"><span data-stu-id="e57f5-115">Turn on the SPS feature</span></span>

<span data-ttu-id="e57f5-116">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="e57f5-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="e57f5-117">Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en de functie desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e57f5-118">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="e57f5-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e57f5-119">**Module:** *Transportbeheer*</span><span class="sxs-lookup"><span data-stu-id="e57f5-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="e57f5-120">**Functienaam:** *Verzending van kleine pakketten*</span><span class="sxs-lookup"><span data-stu-id="e57f5-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="e57f5-121">Tarief-engines implementeren en instellen</span><span class="sxs-lookup"><span data-stu-id="e57f5-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="e57f5-122">Supply Chain Management bevat geen tarief-engines.</span><span class="sxs-lookup"><span data-stu-id="e57f5-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="e57f5-123">U moet zoveel tarief-engines verkrijgen of maken die u nodig hebt, en ze vervolgens aan uw systeem toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="e57f5-124">Microsoft bevat echter een demonstratietarief-engine die u kunt gebruiken voor testen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="e57f5-125">De demonstratietarief-engine downloaden en implementeren</span><span class="sxs-lookup"><span data-stu-id="e57f5-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="e57f5-126">Voer de volgende stappen uit om de demonstratietarief-engine op te halen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="e57f5-127">Download in GitHub de [DLL (Dynamic-Link Library) voor de demonstratietarief-engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="e57f5-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="e57f5-128">Sla de DLL op uw Supply Chain Management-server op in de map **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="e57f5-129">Functionele tarief-engines maken en implementeren</span><span class="sxs-lookup"><span data-stu-id="e57f5-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="e57f5-130">Zie de volgende onderwerpen voor informatie over het maken en implementeren van functionele tarief-engines zodat deze kunnen worden gebruikt in een productie- of testomgeving:</span><span class="sxs-lookup"><span data-stu-id="e57f5-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="e57f5-131">Een nieuwe transportbeheerengine maken</span><span class="sxs-lookup"><span data-stu-id="e57f5-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="e57f5-132">Engines voor transportbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="e57f5-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="e57f5-133">Zie het volgende blogbericht: [Verzending van kleine pakketten: de functie voor verzending van kleine pakketten gebruiken in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5) voor meer informatie over het maken van een tarief-engine voor verzending van kleine pakketten.</span><span class="sxs-lookup"><span data-stu-id="e57f5-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="e57f5-134">Een tarief-engine instellen in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e57f5-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="e57f5-135">Nadat u een tarief-engine voor verzending van kleine pakketten hebt gemaakt en geïmplementeerd, voert u de volgende stappen uit om deze in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="e57f5-136">Ga naar **Transportbeheer \> Instellingen \> Engines \> Tarief-engine**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="e57f5-137">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="e57f5-138">Stel in de nieuwe rij de volgende velden in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="e57f5-139">**Tarief-engine**: voer een unieke naam voor de tarief-engine in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="e57f5-140">Als u de demonstratietarief-engine gebruikt, voert u *Demonstratie-tariefengine* in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="e57f5-141">**Naam**: voer een korte omschrijving van de tarief-engine in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="e57f5-142">Als u de demonstratietarief-engine gebruikt, voert u *Demonstratie-tariefengine* in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="e57f5-143">**Id metagegevens beoordeling**: selecteer de basis die moet worden gebruikt om uw tarief te berekenen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="e57f5-144">Uw tarief kan bijvoorbeeld worden berekend op basis van afstand.</span><span class="sxs-lookup"><span data-stu-id="e57f5-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="e57f5-145">Als u de demonstratietarief-engine gebruikt, kunt u dit veld leeg laten.</span><span class="sxs-lookup"><span data-stu-id="e57f5-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="e57f5-146">**Engine-assembly**: voer de bestandsnaam in van het DLL-pakket dat u hebt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="e57f5-147">Als u de demonstratietarief-engine gebruikt, voert u *TMSSmallParcelShippingEngine.dll* in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="e57f5-148">**Engine-klasse**: voer de klassenaam in die voor uw tarief-engine is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="e57f5-149">Als u de demonstratietarief-engine gebruikt, voert u *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e57f5-150">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="e57f5-150">Example scenario</span></span>

<span data-ttu-id="e57f5-151">In dit voorbeeldscenario wordt getoond hoe u de functie voor verzending van kleine pakketten kunt instellen en gebruiken nadat u het systeem hebt voorbereid, zoals eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="e57f5-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="e57f5-152">Dit scenario gebruikt de eerder genoemde demonstratietarief-engine.</span><span class="sxs-lookup"><span data-stu-id="e57f5-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e57f5-153">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="e57f5-153">Make demo data available</span></span>

<span data-ttu-id="e57f5-154">Als u dit scenario wilt doorlopen met de hier opgegeven demorecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="e57f5-155">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="e57f5-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="e57f5-156">Het scenario configureren</span><span class="sxs-lookup"><span data-stu-id="e57f5-156">Set up the scenario</span></span>

<span data-ttu-id="e57f5-157">Voor dit voorbeeldscenario moet u een vervoerder, vervoerdersgroep, verpakkingsbeleid en verpakkingsprofiel hebben.</span><span class="sxs-lookup"><span data-stu-id="e57f5-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="e57f5-158">In de volgende subsecties wordt uitgelegd hoe u de vereiste records voor het scenario voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="e57f5-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="e57f5-159">In een productiescenario lijkt het instellingsproces meestal op het proces dat hier wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="e57f5-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="e57f5-160">U stelt echter andere waarden in.</span><span class="sxs-lookup"><span data-stu-id="e57f5-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="e57f5-161">Vervoerders instellen</span><span class="sxs-lookup"><span data-stu-id="e57f5-161">Set up carriers</span></span>

<span data-ttu-id="e57f5-162">Voer de volgende stappen uit om een vervoerder in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="e57f5-163">Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Vervoerders**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="e57f5-164">Selecteer **Nieuw** in het actievenster om een vervoerder toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="e57f5-165">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="e57f5-166">**Vervoerder:** *Demovervoerder*</span><span class="sxs-lookup"><span data-stu-id="e57f5-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e57f5-167">**Naam:** *Demovervoerder*</span><span class="sxs-lookup"><span data-stu-id="e57f5-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e57f5-168">**Methode:** *Grond*</span><span class="sxs-lookup"><span data-stu-id="e57f5-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="e57f5-169">Stel op het sneltabblad **Overzicht** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e57f5-170">**Vervoerder activeren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="e57f5-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="e57f5-171">**Beoordeling vervoerder activeren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="e57f5-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="e57f5-172">Selecteer op het sneltabblad **Services** **Nieuw** om een service toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="e57f5-173">Stel de volgende waarden voor de nieuwe service in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="e57f5-174">**Vervoerdersservice:** *Demovervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="e57f5-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e57f5-175">**Naam:** *Demovervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="e57f5-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e57f5-176">**Transportmethode:** *Grond*</span><span class="sxs-lookup"><span data-stu-id="e57f5-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="e57f5-177">Voer indien nodig willekeurige waarden in voor alle andere velden.</span><span class="sxs-lookup"><span data-stu-id="e57f5-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="e57f5-178">(Wanneer u de nieuwe vervoerdersrecord opslaat, wordt een nieuwe leveringsmethode gemaakt en wordt het veld **Leveringsmethode** automatisch ingesteld.)</span><span class="sxs-lookup"><span data-stu-id="e57f5-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="e57f5-179">Selecteer op het sneltabblad **Beoordelingsprofielen** de optie **Nieuw** om een beoordelingsprofiel aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="e57f5-180">Stel de volgende waarden voor het nieuwe profiel in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="e57f5-181">**Beoordelingsprofiel:** *Demovervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="e57f5-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e57f5-182">**Naam:** *Demovervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="e57f5-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e57f5-183">**Tarief-engine:** *Demonstratietarief-engine*</span><span class="sxs-lookup"><span data-stu-id="e57f5-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="e57f5-184">Voer indien nodig willekeurige waarden in voor alle andere velden.</span><span class="sxs-lookup"><span data-stu-id="e57f5-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="e57f5-185">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="e57f5-186">Zie [Vervoerders instellen](../transportation/tasks/set-up-shipping-carriers.md) voor meer informatie over het instellen van vervoerders.</span><span class="sxs-lookup"><span data-stu-id="e57f5-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="e57f5-187">Serviceaccounts voor vervoerders instellen</span><span class="sxs-lookup"><span data-stu-id="e57f5-187">Set up carrier service accounts</span></span>

<span data-ttu-id="e57f5-188">Voer de volgende stappen uit om een serviceaccount voor vervoerders in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="e57f5-189">Ga naar **Transportbeheer \> Instellingen \> Beoordeling \> Serviceaccount voor vervoerder**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="e57f5-190">Selecteer in het actievenster de optie **Nieuw** om een serviceaccount voor vervoerders toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="e57f5-191">Stel de volgende waarden voor de nieuwe account in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="e57f5-192">**Vervoerder:** *Demovervoerder*</span><span class="sxs-lookup"><span data-stu-id="e57f5-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e57f5-193">**Vervoerdersservice:** *Demovervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="e57f5-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e57f5-194">**Klantrekeningnummer vervoerder**: het klantrekeningnummer vervoerder dat wordt gebruikt om de verbinding met de vervoerder te controleren en te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="e57f5-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="e57f5-195">Deze waarde wordt door uw vervoerder verstrekt.</span><span class="sxs-lookup"><span data-stu-id="e57f5-195">Your carrier will provide this value.</span></span> <span data-ttu-id="e57f5-196">Als u de demonstratieservice gebruikt, kunt u een willekeurige waarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="e57f5-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="e57f5-197">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="e57f5-197">**Site:** *6*</span></span>
    - <span data-ttu-id="e57f5-198">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="e57f5-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="e57f5-199">Vaak is de waarde van **Klantrekeningnummer vervoerder** de enige waarde die nodig is om de verbinding te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="e57f5-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="e57f5-200">Als uw vervoerder echter extra verificatieparameters vereist, moet uw organisatie deze pagina aanpassen om indien nodig extra velden toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="e57f5-201">Inpakbeleid voor containers instellen</span><span class="sxs-lookup"><span data-stu-id="e57f5-201">Set up a container packing policy</span></span>

<span data-ttu-id="e57f5-202">Voer de volgende stappen uit om een inpakbeleid voor containers in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="e57f5-203">Als u nog geen ZPL-printerdefinitie hebt ingesteld, gebruikt u de toepassing Documentrouteringsagent om deze in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="e57f5-204">Zie [Overzicht van Documenten afdrukken](../../fin-ops-core/dev-itpro/analytics/print-documents.md) en gerelateerde onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e57f5-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="e57f5-205">Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Inpakbeleid voor container**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="e57f5-206">Selecteer in het actievenster de optie **Nieuw** om een inpakbeleid voor containers toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="e57f5-207">Stel in de koptekst van het nieuwe beleid de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="e57f5-208">**Inpakbeleid voor container:** *Demonstratie-inpakbeleid*</span><span class="sxs-lookup"><span data-stu-id="e57f5-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="e57f5-209">**Beschrijving:** een omschrijving van het beleid</span><span class="sxs-lookup"><span data-stu-id="e57f5-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="e57f5-210">Stel op het sneltabblad **Overzicht** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e57f5-211">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="e57f5-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e57f5-212">**Standaardlocatie voor uiteindelijke zending:** *laaddeur*</span><span class="sxs-lookup"><span data-stu-id="e57f5-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="e57f5-213">**Gewichtseenheid:** *kg*</span><span class="sxs-lookup"><span data-stu-id="e57f5-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="e57f5-214">**Beleid van de containerafsluiting:** *automatische vrijgave*</span><span class="sxs-lookup"><span data-stu-id="e57f5-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="e57f5-215">**Vrijgavebeleid voor container:** *Beschikbaar maken op uiteindelijke verzendlocatie*</span><span class="sxs-lookup"><span data-stu-id="e57f5-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="e57f5-216">Stel op het sneltabblad **Containermanifest** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e57f5-217">**Automatisch manifest bij sluiten van container:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="e57f5-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="e57f5-218">**Manifestvereisten voor container:** *Transportbeheer*</span><span class="sxs-lookup"><span data-stu-id="e57f5-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="e57f5-219">**Containerinhoud afdrukken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="e57f5-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="e57f5-220">Stel op het sneltabblad **Vervoerderslabel afdrukken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e57f5-221">**Verzendlabel container afdrukken:** *Altijd*</span><span class="sxs-lookup"><span data-stu-id="e57f5-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="e57f5-222">**Printernaam:** de naam van de ZPL-printer waarmee verzendlabels moeten worden afgedrukt</span><span class="sxs-lookup"><span data-stu-id="e57f5-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="e57f5-223">Een verpakkingsprofiel instellen</span><span class="sxs-lookup"><span data-stu-id="e57f5-223">Set up a packing profile</span></span>

<span data-ttu-id="e57f5-224">Voer de volgende stappen uit om een verpakkingsprofiel in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="e57f5-225">Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="e57f5-226">Selecteer in het actievenster de optie **Nieuw** om een verpakkingsprofiel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="e57f5-227">Stel de volgende waarden voor het nieuwe profiel in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="e57f5-228">**Verpakkingsprofiel-id:** *Demonstratieverpakkingsprofiel*</span><span class="sxs-lookup"><span data-stu-id="e57f5-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="e57f5-229">**Beschrijving:** een omschrijving van het profiel</span><span class="sxs-lookup"><span data-stu-id="e57f5-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="e57f5-230">**Inpakbeleid voor container:** *Demonstratie-inpakbeleid*</span><span class="sxs-lookup"><span data-stu-id="e57f5-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="e57f5-231">**Modus container-id:** *automatisch*</span><span class="sxs-lookup"><span data-stu-id="e57f5-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="e57f5-232">**Containertype:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="e57f5-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="e57f5-233">Een klant instellen voor gebruik van de vervoerder voor verzending van kleine pakketten</span><span class="sxs-lookup"><span data-stu-id="e57f5-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="e57f5-234">Voer de volgende stappen uit om een klant in te stellen zodat deze de vervoerder kan gebruiken die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e57f5-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="e57f5-235">Ga naar **Klanten \> Klanten \> Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="e57f5-236">Zoek en selecteer klant *US-027* in het raster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="e57f5-237">Selecteer in het actievenster op het tabblad **Algemeen** in de groep **Instellen** de optie **Klantrekeningen vervoerder**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="e57f5-238">Selecteer in het actievenster **Nieuw** om een rekening aan het raster toe te voegen op de pagina **Klantrekeningen vervoerder**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="e57f5-239">Stel de volgende waarden voor de nieuwe account in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="e57f5-240">**Vervoerder:** *Demovervoerder*</span><span class="sxs-lookup"><span data-stu-id="e57f5-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e57f5-241">**Klantrekeningnummer vervoerder:** *12345* (de waarde voor dit scenario is niet belangrijk, maar in de volgende sectie wordt ernaar verwezen.)</span><span class="sxs-lookup"><span data-stu-id="e57f5-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="e57f5-242">Het voorbeeldscenario doornemen</span><span class="sxs-lookup"><span data-stu-id="e57f5-242">Go through the example scenario</span></span>

<span data-ttu-id="e57f5-243">Nadat u alle voorbeeldgegevens hebt ingesteld, zoals beschreven in de vorige sectie, kunt u het voorbeeldscenario gaan gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e57f5-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="e57f5-244">Een verkooporder maken en het werk verwerken</span><span class="sxs-lookup"><span data-stu-id="e57f5-244">Create a sales order and process the work</span></span>

<span data-ttu-id="e57f5-245">Voer de volgende stappen uit om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="e57f5-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="e57f5-246">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e57f5-247">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="e57f5-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="e57f5-248">Stel in het dialoogvenster **Verkooporder maken** het veld **Klantrekening** in op de waarde *US-027*.</span><span class="sxs-lookup"><span data-stu-id="e57f5-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="e57f5-249">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="e57f5-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="e57f5-250">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="e57f5-250">The new sales order is opened.</span></span> <span data-ttu-id="e57f5-251">Stel op het sneltabblad **Koptekst verkooporder** het veld **Klantrekeningnummer vervoerder** in op de waarde die u eerder voor deze klant hebt geselecteerd (*12345*).</span><span class="sxs-lookup"><span data-stu-id="e57f5-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="e57f5-252">Voeg in de sectie **Verkooporderregels** een verkoopregel toe en stel de volgende waarden voor de regel in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="e57f5-253">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e57f5-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="e57f5-254">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="e57f5-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e57f5-255">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="e57f5-255">**Site:** *6*</span></span>
    - <span data-ttu-id="e57f5-256">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="e57f5-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e57f5-257">Schakel over naar de weergave **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e57f5-258">Stel op het sneltabblad **Levering** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e57f5-259">**Vervoerder:** *Demovervoerder*</span><span class="sxs-lookup"><span data-stu-id="e57f5-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e57f5-260">**Vervoerdersservice:** *Demovervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="e57f5-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="e57f5-261">Ga terug naar de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="e57f5-262">Als u wordt gevraagd de leveringsmethode voor de verkoopregels bij te werken, selecteert u **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="e57f5-263">Selecteer in de sectie **Verkooporderregels** de orderregel die u eerder hebt ingesteld, en selecteer vervolgens **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="e57f5-264">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="e57f5-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="e57f5-265">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="e57f5-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e57f5-266">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e57f5-267">Er wordt werk gemaakt om artikelen van de orderverzamellocatie naar het inpakstation te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="e57f5-268">Selecteer in de sectie **Verkooporderregels** **Magazijn \> Details van zending**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="e57f5-269">Maak op de pagina **Details van zending** een notitie van de zendings-ID.</span><span class="sxs-lookup"><span data-stu-id="e57f5-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="e57f5-270">U hebt deze nodig wanneer u de zending verpakt in het inpakstation.</span><span class="sxs-lookup"><span data-stu-id="e57f5-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="e57f5-271">Sluit de pagina **Details van zending** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="e57f5-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="e57f5-272">Maak een notitie van het verkoopordernummer en ga vervolgens naar **Magazijnbebeer \> Werk \> Alle werkzaamheden**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="e57f5-273">Gebruik het verkoopordernummer om het werk te zoeken en te selecteren dat voor de order is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e57f5-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="e57f5-274">Selecteer in het actievenster op het tabblad **Werk** de optie **Werk voltooien**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="e57f5-275">Selecteer een gebruikers-id op de pagina **Werkvoltooiing** in het veld **Gebruikers-id**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="e57f5-276">Selecteer vervolgens in het actievenster **Werk valideren**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="e57f5-277">Als het werk is gevalideerd, selecteert u **Werk voltooien** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="e57f5-278">Het werk is gemarkeerd als voltooid om de verplaatsing van artikelen naar het inpakstation te simuleren.</span><span class="sxs-lookup"><span data-stu-id="e57f5-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="e57f5-279">De zending inpakken</span><span class="sxs-lookup"><span data-stu-id="e57f5-279">Pack the shipment</span></span>

<span data-ttu-id="e57f5-280">Voer de volgende stappen uit om de zending in te pakken.</span><span class="sxs-lookup"><span data-stu-id="e57f5-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="e57f5-281">Ga naar **Magazijnbeheer \> Instellingen \> Medewerker** en zorg ervoor dat uw gebruikersaccount is gekoppeld aan een medewerkersaccount voor magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="e57f5-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="e57f5-282">Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Verpakken**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="e57f5-283">Stel in het dialoogvenster **Inpakstation selecteren** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e57f5-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e57f5-284">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="e57f5-284">**Site:** *6*</span></span>
    - <span data-ttu-id="e57f5-285">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="e57f5-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e57f5-286">**Locatie:** *Verpakken*</span><span class="sxs-lookup"><span data-stu-id="e57f5-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="e57f5-287">**Verpakkingsprofiel-id:** *Demonstratieverpakkingsprofiel*</span><span class="sxs-lookup"><span data-stu-id="e57f5-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="e57f5-288">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-288">Select **OK**.</span></span>
1. <span data-ttu-id="e57f5-289">De pagina **Verpakken** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e57f5-289">The **Pack** page appears.</span></span> <span data-ttu-id="e57f5-290">In een productiescenario scant een medewerker een nummerplaat of zendings-ID.</span><span class="sxs-lookup"><span data-stu-id="e57f5-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="e57f5-291">In dit scenario opent u echter de pagina **Alle zendingen** en zoekt u het zendingsnummer voor de zending die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e57f5-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="e57f5-292">Voer vervolgens deze waarde in het veld **Nummerplaat of zending** in op de pagina **Verpakken**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="e57f5-293">U kunt ook de zendings-id invoeren die u eerder hebt genoteerd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="e57f5-294">Selecteer **Nieuwe container** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e57f5-295">In het dialoogvenster dat wordt weergegeven, worden details over de nieuwe container weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e57f5-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="e57f5-296">Laat de standaardwaarden staan en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="e57f5-297">Selecteer *A0002* om het artikel te verpakken op de pagina **Verpakken** op het sneltabblad **Artikel verpakken** in het veld **Id**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="e57f5-298">Het artikel wordt aan de container toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-298">The item is added to the container.</span></span>
1. <span data-ttu-id="e57f5-299">Selecteer in het actievenster de optie **Containers voor zending**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="e57f5-300">De pagina **Containers voor zending** die wordt weergegeven, heeft een rij voor de container die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e57f5-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="e57f5-301">Het veld **Containermanifest-id** in die rij is echter momenteel leeg, omdat u het verzendlabel en traceringsnummer nog niet van de vervoerder hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="e57f5-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="e57f5-302">Selecteer **Container sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e57f5-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e57f5-303">Stel in het dialoogvenster **Container sluiten** het veld **Brutogewicht** in op *1 kg* en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e57f5-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="e57f5-304">Het verzendlabel moet nu worden afgedrukt op de ZPL-printer die u eerder hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e57f5-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="e57f5-305">Het resultaat moet lijken op het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="e57f5-305">It should resemble the following example.</span></span>

    <span data-ttu-id="e57f5-306">![Voorbeeldverzendlabel](media/sps-label-example.png "Voorbeeldverzendlabel")</span><span class="sxs-lookup"><span data-stu-id="e57f5-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="e57f5-307">De waarden **Containermanifest-id** en **Totale vrachtkosten** zijn toegevoegd als ontvangen van de vervoerder.</span><span class="sxs-lookup"><span data-stu-id="e57f5-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]