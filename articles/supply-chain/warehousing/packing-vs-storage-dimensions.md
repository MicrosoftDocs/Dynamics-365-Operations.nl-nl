---
title: Verschillende dimensies voor verpakking en opslag instellen
description: In dit onderwerp wordt aangegeven voor welk proces (verpakking, opslag of geneste verpakking) elke opgegeven dimensie wordt gebruikt.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: aa5cbf807e809238489c539d3ad8c0bc34421774
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501289"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="ec30e-103">Verschillende dimensies voor verpakking en opslag instellen</span><span class="sxs-lookup"><span data-stu-id="ec30e-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ec30e-104">Sommige artikelen worden verpakt of opgeslagen op een manier die u mogelijk nodig hebt om fysieke dimensies op een andere manier bij te houden voor elk van de verschillende processen.</span><span class="sxs-lookup"><span data-stu-id="ec30e-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="ec30e-105">Met de functie *Verpakkingsproductdimensie* kunt u voor elk product een of meer typen dimensies instellen.</span><span class="sxs-lookup"><span data-stu-id="ec30e-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="ec30e-106">Elk dimensietype biedt een reeks fysieke afmetingen (gewicht, breedte, diepte en hoogte) en legt het proces vast waarin deze fysieke metingwaarden van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="ec30e-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="ec30e-107">Wanneer deze functie is ingeschakeld, ondersteunt het systeem de volgende typen dimensies:</span><span class="sxs-lookup"><span data-stu-id="ec30e-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="ec30e-108">*Opslag*: opslagdimensies worden samen met locatievolumemaatstaven gebruikt om te bepalen hoeveel van elk artikel op diverse magazijnlocaties kan worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="ec30e-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="ec30e-109">*Verpakking*: verpakkingsdimensies worden gebruikt tijdens de containervorming en het handmatige verpakkingsproces om te bepalen hoeveel van elk artikel in de verschillende containertypen past.</span><span class="sxs-lookup"><span data-stu-id="ec30e-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="ec30e-110">*Geneste verpakking*: geneste verpakkingsdimensies worden gebruikt wanneer het verpakkingsproces meerdere niveaus bevat.</span><span class="sxs-lookup"><span data-stu-id="ec30e-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="ec30e-111">*Opslag*: dimensies worden zelfs ondersteund wanneer de functie *Verpakkingsproductdimensie* niet is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ec30e-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="ec30e-112">U stelt deze in via de pagina **Fysieke dimensie** in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec30e-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="ec30e-113">Deze dimensies worden gebruikt door alle processen waarbij geen verpakkings- en geneste verpakkingsdimensies zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ec30e-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="ec30e-114">*Verpakkings*- en *geneste verpakkings* dimensies worden ingesteld met de pagina **Fysieke productdimensies** die wordt toegevoegd wanneer u de functie *Verpakkingsproductdimensie* inschakelt.</span><span class="sxs-lookup"><span data-stu-id="ec30e-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="ec30e-115">In dit onderwerp vindt u een scenario dat laat zien hoe u deze functie moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ec30e-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="ec30e-116">De functie Verpakkingsproductdimensie inschakelen</span><span class="sxs-lookup"><span data-stu-id="ec30e-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="ec30e-117">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="ec30e-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ec30e-118">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ec30e-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ec30e-119">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="ec30e-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ec30e-120">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="ec30e-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ec30e-121">**Functienaam:** *Verpakkingsproductdimensies*</span><span class="sxs-lookup"><span data-stu-id="ec30e-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ec30e-122">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="ec30e-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="ec30e-123">Het scenario configureren</span><span class="sxs-lookup"><span data-stu-id="ec30e-123">Set up the scenario</span></span>

<span data-ttu-id="ec30e-124">Voordat u het voorbeeldscenario kunt uitvoeren, moet u het systeem voorbereiden zoals beschreven in deze sectie.</span><span class="sxs-lookup"><span data-stu-id="ec30e-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="ec30e-125">Demogegevens inschakelen</span><span class="sxs-lookup"><span data-stu-id="ec30e-125">Enable demo data</span></span>

<span data-ttu-id="ec30e-126">Als u dit scenario wilt doorlopen met de hier opgegeven demorecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="ec30e-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ec30e-127">U moet daarnaast ook de rechtspersoon *USMF* selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="ec30e-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="ec30e-128">Een nieuwe fysieke dimensie aan een product toevoegen</span><span class="sxs-lookup"><span data-stu-id="ec30e-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="ec30e-129">Voeg als volgt een nieuwe fysieke dimensie voor een product toe:</span><span class="sxs-lookup"><span data-stu-id="ec30e-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="ec30e-130">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ec30e-131">Selecteer het product met **Artikelnummer** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="ec30e-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="ec30e-132">Open in het actievenster het tabblad **Voorraad beheren** en selecteer in de groep **Magazijn** de optie **Fysieke productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="ec30e-133">De pagina **Fysieke productdimensies** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="ec30e-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="ec30e-134">Selecteer in het actievenster **Nieuw** om een nieuwe dimensie toe te voegen aan het raster met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="ec30e-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="ec30e-135">**Type fysieke dimensie** - *Verpakking*</span><span class="sxs-lookup"><span data-stu-id="ec30e-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="ec30e-136">**Fysieke eenheid** - *stuks*</span><span class="sxs-lookup"><span data-stu-id="ec30e-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="ec30e-137">**Gewicht** - *4*</span><span class="sxs-lookup"><span data-stu-id="ec30e-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="ec30e-138">**Gewichtseenheid** - *kg*</span><span class="sxs-lookup"><span data-stu-id="ec30e-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="ec30e-139">**Diepte** - *3*</span><span class="sxs-lookup"><span data-stu-id="ec30e-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="ec30e-140">**Hoogte** - *4*</span><span class="sxs-lookup"><span data-stu-id="ec30e-140">**Height** - *4*</span></span>
    - <span data-ttu-id="ec30e-141">**Breedte** - *3*</span><span class="sxs-lookup"><span data-stu-id="ec30e-141">**Width** - *3*</span></span>
    - <span data-ttu-id="ec30e-142">**Lengte** - *cm*</span><span class="sxs-lookup"><span data-stu-id="ec30e-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="ec30e-143">**Volume-eenheid** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="ec30e-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="ec30e-144">Het veld **Volume** wordt automatisch berekend op basis van de instellingen **Diepte**, **Hoogte** en **Breedte**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="ec30e-145">Een nieuw containertype maken</span><span class="sxs-lookup"><span data-stu-id="ec30e-145">Create a new container type</span></span>

<span data-ttu-id="ec30e-146">Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containertypen** en maak een nieuwe record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="ec30e-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="ec30e-147">**Containertypecode** - *kleine doos*</span><span class="sxs-lookup"><span data-stu-id="ec30e-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="ec30e-148">**Beschrijving** - *kleine doos*</span><span class="sxs-lookup"><span data-stu-id="ec30e-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="ec30e-149">**Maximaal nettogewicht** - *50*</span><span class="sxs-lookup"><span data-stu-id="ec30e-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="ec30e-150">**Volume** - *144*</span><span class="sxs-lookup"><span data-stu-id="ec30e-150">**Volume** - *144*</span></span>
- <span data-ttu-id="ec30e-151">**Lengte** - *6*</span><span class="sxs-lookup"><span data-stu-id="ec30e-151">**Length** - *6*</span></span>
- <span data-ttu-id="ec30e-152">**Breedte** - *6*</span><span class="sxs-lookup"><span data-stu-id="ec30e-152">**Width** - *6*</span></span>
- <span data-ttu-id="ec30e-153">**Hoogte** - *4*</span><span class="sxs-lookup"><span data-stu-id="ec30e-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="ec30e-154">Een containergroep maken</span><span class="sxs-lookup"><span data-stu-id="ec30e-154">Create a container group</span></span>

<span data-ttu-id="ec30e-155">Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containergroepen** en maak een nieuwe record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="ec30e-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="ec30e-156">**Containergroep-id** - *kleine doos*</span><span class="sxs-lookup"><span data-stu-id="ec30e-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="ec30e-157">**Beschrijving** - *kleine doos*</span><span class="sxs-lookup"><span data-stu-id="ec30e-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="ec30e-158">Voeg een nieuwe regel aan de sectie **Details** toe.</span><span class="sxs-lookup"><span data-stu-id="ec30e-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="ec30e-159">Stel het **Containertype** in op *Kleine doos*.</span><span class="sxs-lookup"><span data-stu-id="ec30e-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="ec30e-160">Een containervormingsjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="ec30e-160">Set up a container build template</span></span>

<span data-ttu-id="ec30e-161">Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containervormingssjablonen** en selecteer **Dozen**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="ec30e-162">Wijzig de **Containergroep-id** in *Kleine doos*.</span><span class="sxs-lookup"><span data-stu-id="ec30e-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="ec30e-163">Het scenario uitvoeren</span><span class="sxs-lookup"><span data-stu-id="ec30e-163">Run the scenario</span></span>

<span data-ttu-id="ec30e-164">Nadat u het systeem hebt voorbereid zoals beschreven in de vorige sectie, kunt u het scenario uitvoeren zoals beschreven in de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="ec30e-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="ec30e-165">Een verkooporder maken en een zending maken</span><span class="sxs-lookup"><span data-stu-id="ec30e-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="ec30e-166">In dit proces maakt u een zending op basis van de *verpakkings* dimensie van het artikel, waarvan de hoogte minder dan 3 is.</span><span class="sxs-lookup"><span data-stu-id="ec30e-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="ec30e-167">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ec30e-168">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ec30e-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ec30e-169">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ec30e-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ec30e-170">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ec30e-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ec30e-171">**Magazijn:** *63*</span><span class="sxs-lookup"><span data-stu-id="ec30e-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="ec30e-172">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="ec30e-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ec30e-173">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="ec30e-173">The new sales order is opened.</span></span> <span data-ttu-id="ec30e-174">Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ec30e-175">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ec30e-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="ec30e-176">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ec30e-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ec30e-177">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="ec30e-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="ec30e-178">Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ec30e-179">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.</span><span class="sxs-lookup"><span data-stu-id="ec30e-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="ec30e-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ec30e-180">Close the page.</span></span>
1. <span data-ttu-id="ec30e-181">Open in het actievenster het tabblad **Magazijn** en selecteer de optie **Vrijgeven aan magazijn** om werk voor het magazijn te maken.</span><span class="sxs-lookup"><span data-stu-id="ec30e-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="ec30e-182">Selecteer op het sneltabblad **Verkooporderregels** **Magazijn \> Details van zending**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="ec30e-183">Open in het actievenster het tabblad **Transport** en selecteer **Containers weergeven**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="ec30e-184">Bevestig dat het artikel is verpakt in de twee containers van het type *Kleine doos*.</span><span class="sxs-lookup"><span data-stu-id="ec30e-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="ec30e-185">Een artikel in de opslag plaatsen</span><span class="sxs-lookup"><span data-stu-id="ec30e-185">Place an item into storage</span></span>

1. <span data-ttu-id="ec30e-186">Open het mobiele apparaat, meld u aan bij magazijn 63 en ga naar **Voorraad \> Aanpassen in**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="ec30e-187">Voer **Loc** = *SHORT-01* in.</span><span class="sxs-lookup"><span data-stu-id="ec30e-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="ec30e-188">Maak een nieuwe nummerplaat met **Artikel** = *A0001* en **Hoeveelheid** = *1 st*.</span><span class="sxs-lookup"><span data-stu-id="ec30e-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="ec30e-189">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec30e-189">Select **OK**.</span></span> <span data-ttu-id="ec30e-190">U ontvangt de fout "Locatie SHORT-01 is mislukt omdat artikel A0001 niet in de opgegeven dimensies van de locatie past".</span><span class="sxs-lookup"><span data-stu-id="ec30e-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="ec30e-191">Dit komt omdat de dimensies van het type *Opslag* van het product groter zijn dan de dimensies die in het locatieprofiel zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ec30e-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]