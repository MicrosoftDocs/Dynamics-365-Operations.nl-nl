---
title: Automatische toeslagen per kanaal inschakelen en configureren
description: In dit onderwerp wordt uitgelegd hoe u automatische toeslagen per kanaal kunt inschakelen en configureren in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 1be07c754e563298d82f6ca54f09ae3aa9118602
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411355"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="f7f06-103">Automatische toeslagen per kanaal inschakelen en configureren</span><span class="sxs-lookup"><span data-stu-id="f7f06-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="f7f06-104">In dit onderwerp wordt uitgelegd hoe u automatische toeslagen per kanaal kunt inschakelen en configureren in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7f06-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f7f06-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="f7f06-105">Overview</span></span>

<span data-ttu-id="f7f06-106">U kunt bijvoorbeeld scenario's hebben waarbij recyclingkosten of andere kosten moeten worden toegepast op een groep producten die worden verkocht in alle of een aantal winkels in een bepaalde staat (bijvoorbeeld Californië).</span><span class="sxs-lookup"><span data-stu-id="f7f06-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="f7f06-107">Met de functie **Automatische toeslagen per kanaal inschakelen** in Commerce kunt u automatische toeslagen per kanaal opgeven (bijvoorbeeld voor een bepaald winkelkanaal).</span><span class="sxs-lookup"><span data-stu-id="f7f06-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="f7f06-108">Deze functie is beschikbaar in Dynamics 365 Commerce versie 10.0.10 en hoger.</span><span class="sxs-lookup"><span data-stu-id="f7f06-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="f7f06-109">Als u automatische toeslagen per kanaal wilt inschakelen en configureren, moet u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="f7f06-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="f7f06-110">Schakel de functie **Automatische toeslagen per kanaal inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="f7f06-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="f7f06-111">Configureer de organisatiehiërarchiedoelstelling.</span><span class="sxs-lookup"><span data-stu-id="f7f06-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="f7f06-112">Definieer automatische toeslagen per kanaal.</span><span class="sxs-lookup"><span data-stu-id="f7f06-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="f7f06-113">De functie **Automatische toeslagen per kanaal inschakelen** werkt alleen als de functie voor geavanceerde automatische toeslagen is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f7f06-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="f7f06-114">Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md) voor informatie over het inschakelen van de functie voor geavanceerde automatische toeslagen.</span><span class="sxs-lookup"><span data-stu-id="f7f06-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="f7f06-115">De functie Automatische toeslagen per kanaal inschakelen</span><span class="sxs-lookup"><span data-stu-id="f7f06-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="f7f06-116">Voer de volgende stappen uit om automatische toeslagen per kanaal in te schakelen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7f06-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f7f06-117">Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="f7f06-118">Ga op het tabblad **Niet ingeschakeld** naar de lijst **Functienaam** en selecteer **Automatische toeslagen per kanaal inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="f7f06-119">Selecteer rechtsonder **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="f7f06-120">Nadat de functie is ingeschakeld, wordt deze weergegeven in de lijst op het tabblad **Alles**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="f7f06-121">Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="f7f06-122">Zoek en selecteer in het linkerdeelvenster de taak **1110** (**Algemene configuratie**).</span><span class="sxs-lookup"><span data-stu-id="f7f06-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="f7f06-123">Selecteer **Nu uitvoeren** in het actievenster om de configuratiewijzigingen door te voeren.</span><span class="sxs-lookup"><span data-stu-id="f7f06-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="f7f06-124">Als u de functie **Automatische toeslagen per kanaal inschakelen** hebt uitgeschakeld nadat u deze al hebt gebruikt, wordt het veld **Relatie detailhandelskanaal** onder **Automatische toeslagen** niet meer weergegeven en verliest u alle bestaande configuraties.</span><span class="sxs-lookup"><span data-stu-id="f7f06-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="f7f06-125">Als het verwijderen van de configuraties voor **Relatie detailhandelskanaal** ertoe leidt dat de automatische toeslagregels worden gedupliceerd, zal een poging om de functie uit te schakelen mislukken.</span><span class="sxs-lookup"><span data-stu-id="f7f06-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="f7f06-126">Voordat u de functie uitschakelt, moet u alle regels voor automatische toeslagen controleren en eventueel vereiste wijzigingen aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="f7f06-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="f7f06-127">De organisatiehiërarchiedoelstelling configureren</span><span class="sxs-lookup"><span data-stu-id="f7f06-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="f7f06-128">Een nieuwe organisatiehiërarchiedoelstelling met de naam **Automatische toeslagen detailhandel** is gemaakt om de hiërarchie voor automatische toeslagen per kanaal te beheren.</span><span class="sxs-lookup"><span data-stu-id="f7f06-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="f7f06-129">Voer de volgende stappen uit om een standaardhiërarchie toe te wijzen aan een organisatiehiërarchiedoelstelling in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7f06-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="f7f06-130">Ga naar **Organisatiebeheer \> Organisaties \> Organisatiehiërarchiedoelstellingen**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="f7f06-131">Selecteer in het linkerdeelvenster de optie **Automatische toeslagen detailhandel**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="f7f06-132">Selecteer **Toevoegen** onder **Toegewezen hiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="f7f06-133">Selecteer in het dialoogvenster **Organisatiehiërarchieën** een organisatiehiërarchie (bijvoorbeeld **Detailhandelwinkels per regio**) en selecteer **OK.**</span><span class="sxs-lookup"><span data-stu-id="f7f06-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="f7f06-134">Selecteer **Als standaard instellen** onder **Toegewezen hiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="f7f06-135">Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="f7f06-136">Zoek en selecteer in het linkerdeelvenster de taak **1040** (**Producten**).</span><span class="sxs-lookup"><span data-stu-id="f7f06-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="f7f06-137">Selecteer **Nu uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f7f06-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="f7f06-138">Herhaal de voorgaande twee stappen om de taken **1070** (**Kanaalconfiguratie**) en **1110** (**Algemene configuratie**) uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f7f06-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Configuratie van de organisatiehiërarchiedoelstelling Automatische toeslagen detailhandel](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="f7f06-140">Automatische toeslagen per kanaal definiëren</span><span class="sxs-lookup"><span data-stu-id="f7f06-140">Define auto charges by channel</span></span>

<span data-ttu-id="f7f06-141">Nadat u de functie **Automatische toeslagen per kanaal inschakelen** hebt ingeschakeld en de organisatiehiërarchiedoelstelling **Automatische toeslagen detailhandel** hebt geconfigureerd, kunnen automatische toeslagen per kanaal worden gedefinieerd op het niveau van de orderkoptekst of het niveau van de orderregel.</span><span class="sxs-lookup"><span data-stu-id="f7f06-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="f7f06-142">Voer de volgende stappen uit om automatische toeslagen per kanaal te definiëren in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7f06-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f7f06-143">Ga naar  **Klanten \> Instelling van toeslagen \> Automatische toeslagen**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="f7f06-144">Selecteer in het linkerdeelvenster in het veld **Niveau** de optie **Koptekst** of **Regel**, afhankelijk van uw zakelijke vereisten.</span><span class="sxs-lookup"><span data-stu-id="f7f06-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="f7f06-145">Selecteer in het veld **Code detailhandelskanaal** de toepasselijke kanaalcode (bijvoorbeeld **Tabel** of **Groep**).</span><span class="sxs-lookup"><span data-stu-id="f7f06-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="f7f06-146">Als de standaardinstelling **Alle** wordt gebruikt, worden toeslagregels op alle kanalen toegepast.</span><span class="sxs-lookup"><span data-stu-id="f7f06-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="f7f06-147">Als u **Groep** selecteert, moet u ervoor zorgen dat er een toeslagengroep voor een detailhandelskanaal wordt gemaakt in **Detailhandel en commerce \> Afzetkanaalinstellingen \> Toeslagen \> Toeslaggroepen voor detailhandelkanaal**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="f7f06-148">Als u **Tabel** selecteert, kunt u een specifiek kanaal selecteren (bijvoorbeeld **San Francisco**) in het veld **Relatie detailhandelkanaal**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="f7f06-149">Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="f7f06-150">Zoek en selecteer in het linkerdeelvenster de taak **1040** (**Producten**).</span><span class="sxs-lookup"><span data-stu-id="f7f06-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="f7f06-151">Selecteer **Nu uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f7f06-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="f7f06-152">Herhaal de voorgaande twee stappen om de taken **1070** (**Kanaalconfiguratie**) en **1110** (**Algemene configuratie**) uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f7f06-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automatische toeslagen gedefinieerd per kanaal](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="f7f06-154">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="f7f06-154">Example scenario</span></span>

<span data-ttu-id="f7f06-155">In het volgende voorbeeld vindt u een overzicht van de stappen die nodig zijn om een product te configureren, zodat recyclingkosten in rekening worden gebracht wanneer het product wordt verkocht via een winkelafzetkanaal voor San Francisco.</span><span class="sxs-lookup"><span data-stu-id="f7f06-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="f7f06-156">In het voorbeeld ziet u ook hoe de automatische toeslagen worden weergegeven in de POS-toepassing (Commerce Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="f7f06-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="f7f06-157">De organisatie definieert een toeslagcode met de naam **RECYCLE**, zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="f7f06-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Toeslagcode RECYCLE](media/Auto-charges-charge-code.png)

<span data-ttu-id="f7f06-159">Er wordt op regelniveau een automatische toeslag gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f7f06-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="f7f06-160">Deze heeft de volgende configuratie:</span><span class="sxs-lookup"><span data-stu-id="f7f06-160">It has the following configuration:</span></span>

- <span data-ttu-id="f7f06-161">Het veld **Rekeningcode** wordt ingesteld op **Alle**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="f7f06-162">Het veld **Artikelcode** wordt ingesteld op **Tafel**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="f7f06-163">Het veld **Artikelrelatie** wordt ingesteld op product-id **91001**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="f7f06-164">Het veld **Code van leveringsmethode** wordt ingesteld op **Alle**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="f7f06-165">Het veld **Code detailhandelskanaal** wordt ingesteld op **Tafel**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="f7f06-166">Het veld **Relatie detailhandelskanaal** wordt ingesteld op de winkel in **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="f7f06-167">Er wordt een regel met automatische toeslagen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f7f06-167">An auto charges line is created.</span></span> <span data-ttu-id="f7f06-168">Deze heeft de volgende configuratie:</span><span class="sxs-lookup"><span data-stu-id="f7f06-168">It has the following configuration:</span></span>

- <span data-ttu-id="f7f06-169">Het veld **Valuta** wordt ingesteld op **USD**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="f7f06-170">Het veld **Toeslagcode** wordt ingesteld op **RECYCLE**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="f7f06-171">Het veld **Categorie** wordt ingesteld op **Vast**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="f7f06-172">Het veld **Toeslagen** wordt ingesteld op **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-172">The **Charges** field is set to **$6.25**.</span></span>

![Configuratie van de automatische toeslag op regelniveau en de automatische toeslagregel](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="f7f06-174">In de POS-toepassing wordt een verkooporder gemaakt in het detailhandelskanaal **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="f7f06-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="f7f06-175">Op de regel **Toeslagen** worden de recyclingkosten van **$6,25** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f7f06-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="f7f06-176">Selecteer **Transactieopties \> Toeslagen \> Toeslagen beheren** in de POS-toepassing als u de toeslagcode en de omschrijving voor de recyclingkosten wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="f7f06-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Recyclingkosten in de POS-toepassing](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="f7f06-178">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f7f06-178">Additional resources</span></span>

[<span data-ttu-id="f7f06-179">Geavanceerde automatische toeslagen voor meerdere kanalen</span><span class="sxs-lookup"><span data-stu-id="f7f06-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="f7f06-180">Toeslagen voor koptekst naar rato verdelen voor overeenkomende verkoopregels</span><span class="sxs-lookup"><span data-stu-id="f7f06-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)
