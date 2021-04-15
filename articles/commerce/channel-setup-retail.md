---
title: Een detailhandelkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw detailhandelkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 713cbe68c151b6893519843611089941cabf0e70
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800586"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="387c9-103">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="387c9-104">In dit onderwerp wordt beschreven hoe u een nieuw detailhandelkanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="387c9-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="387c9-105">Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen.</span><span class="sxs-lookup"><span data-stu-id="387c9-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="387c9-106">Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd).</span><span class="sxs-lookup"><span data-stu-id="387c9-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="387c9-107">Iedere Retail-winkelkanaal kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="387c9-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="387c9-108">U moet al deze elementen instellen voordat u een Retail-winkelkanaal kunt maken.</span><span class="sxs-lookup"><span data-stu-id="387c9-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="387c9-109">Controleer vóór het maken van een detailhandelkanaal of u de [Vereisten voor afzetkanalen](channels-prerequisites.md) hebt gevolgd.</span><span class="sxs-lookup"><span data-stu-id="387c9-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="387c9-110">Een nieuw detailhandelafzetkanaal maken en configureren</span><span class="sxs-lookup"><span data-stu-id="387c9-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="387c9-111">Ga in het navigatievenster naar **Modules \> Kanalen \> Winkels \> Alle winkels**.</span><span class="sxs-lookup"><span data-stu-id="387c9-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="387c9-112">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="387c9-113">Typ in het veld **Naam** een naam voor het nieuwe kanaal.</span><span class="sxs-lookup"><span data-stu-id="387c9-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="387c9-114">Geef in het veld **Winkelnummer** een uniek winkelnummer op.</span><span class="sxs-lookup"><span data-stu-id="387c9-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="387c9-115">Het nummer kan alfanumeriek zijn met een maximum van 10 tekens.</span><span class="sxs-lookup"><span data-stu-id="387c9-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="387c9-116">Voer in de vervolgkeuzelijst **Rechtspersoon** de toepasselijke rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="387c9-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="387c9-117">Voer in de vervolgkeuzelijst **Magazijn** het juiste magazijn in.</span><span class="sxs-lookup"><span data-stu-id="387c9-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="387c9-118">Selecteer in het veld **Winkeltijdzone** de juiste tijdzone.</span><span class="sxs-lookup"><span data-stu-id="387c9-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="387c9-119">Selecteer in de vervolgkeuzelijst **Btw-groep** een toepasselijke btw-groep voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="387c9-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="387c9-120">Selecteer in het veld **Valuta** de juiste valuta.</span><span class="sxs-lookup"><span data-stu-id="387c9-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="387c9-121">Geef in het veld **Adresboek klant** een geldig adresboek op.</span><span class="sxs-lookup"><span data-stu-id="387c9-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="387c9-122">Geef in het veld **Standaardklant** een geldige standaardklant op.</span><span class="sxs-lookup"><span data-stu-id="387c9-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="387c9-123">Selecteer in het veld **Functionaliteitsprofiel** een functionaliteitsprofiel, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="387c9-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="387c9-124">Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.</span><span class="sxs-lookup"><span data-stu-id="387c9-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="387c9-125">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-125">On the action pane, select **Save**.</span></span>

<span data-ttu-id="387c9-126">De volgende afbeelding toont het maken van een nieuw detailhandelkanaal.</span><span class="sxs-lookup"><span data-stu-id="387c9-126">The following image shows the creation of a new retail channel.</span></span>

![Nieuw detailhandelafzetkanaal](media/channel-setup-retail-1.png)

<span data-ttu-id="387c9-128">In de volgende afbeelding ziet u een voorbeeld van een detailhandelafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="387c9-128">The following image shows an example retail channel.</span></span>

![Voorbeeld van detailhandelafzetkanaal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="387c9-130">Overige instellingen</span><span class="sxs-lookup"><span data-stu-id="387c9-130">Other settings</span></span>

<span data-ttu-id="387c9-131">Er zijn talloze andere optionele instellingen die u op basis van de behoeften van de detailhandelwinkel kunt instellen in de secties **Overzicht/afsluiting** en **Overige**.</span><span class="sxs-lookup"><span data-stu-id="387c9-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="387c9-132">Zie ook [Schermindelingen voor het POS](pos-screen-layouts.md) voor informatie over het instellen van de standaardschermindeling in de sectie **Schermindeling** en [Retail-hardwarestation configureren en installeren](retail-hardware-station-configuration-installation.md) voor informatie het instellen van de sectie **Hardwarestations**.</span><span class="sxs-lookup"><span data-stu-id="387c9-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="387c9-133">In de volgende afbeelding ziet u een voorbeeldconfiguratie van een detailhandelafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="387c9-133">The following image shows an example retail channel setup configuration.</span></span>

![Voorbeeldconfiguratie van detailhandelafzetkanaal](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="387c9-135">Aanvullende kanaalinstellingen</span><span class="sxs-lookup"><span data-stu-id="387c9-135">Additional channel set up</span></span>

<span data-ttu-id="387c9-136">Er zijn nog meer zaken die u moet instellen voor een kanaal. Deze vindt u in de sectie **Instellingen** van het **Actievenster**.</span><span class="sxs-lookup"><span data-stu-id="387c9-136">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="387c9-137">Aanvullende taken die nodig zijn voor het instellen van online kanalen, zijn onder andere het instellen van betalingsmethoden, contantdeclaraties, leveringsmethoden, inkomsten- en onkostenrekeningen, secties, de toewijzing van afhandelingsgroepen en kluizen.</span><span class="sxs-lookup"><span data-stu-id="387c9-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="387c9-138">De volgende afbeelding toont diverse aanvullende opties voor het instellen van detailhandelskanalen op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="387c9-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanaal instellen](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="387c9-140">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-140">Set up payment methods</span></span>

<span data-ttu-id="387c9-141">Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="387c9-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="387c9-142">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="387c9-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="387c9-143">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="387c9-144">Selecteer in het navigatievenster een gewenste betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="387c9-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="387c9-145">Geef in de sectie **Algemeen** een naam op in **Bewerkingsnaam** en configureer eventuele andere instellingen.</span><span class="sxs-lookup"><span data-stu-id="387c9-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="387c9-146">Configureer eventuele aanvullende instellingen voor het betalingstype.</span><span class="sxs-lookup"><span data-stu-id="387c9-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="387c9-147">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="387c9-148">In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.</span><span class="sxs-lookup"><span data-stu-id="387c9-148">The following image shows an example of a cash payment method.</span></span>

![Voorbeeldbetalingsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="387c9-150">Contantdeclaratie instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-150">Set up cash declaration</span></span>

1. <span data-ttu-id="387c9-151">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Contantdeclaratie**.</span><span class="sxs-lookup"><span data-stu-id="387c9-151">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="387c9-152">Selecteer in het actievenster de optie **Nieuw** en maak vervolgens alle **Munt**- en **Coupure**-denominaties die van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="387c9-152">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="387c9-153">In de volgende afbeelding ziet u een voorbeeld van een contantdeclaratie.</span><span class="sxs-lookup"><span data-stu-id="387c9-153">The following image shows an example of a cash declaration.</span></span>

![Contantdeclaraties instellen](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="387c9-155">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-155">Set up modes of delivery</span></span>

<span data-ttu-id="387c9-156">U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="387c9-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="387c9-157">Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.</span><span class="sxs-lookup"><span data-stu-id="387c9-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="387c9-158">Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="387c9-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="387c9-159">Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.</span><span class="sxs-lookup"><span data-stu-id="387c9-159">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="387c9-160">Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="387c9-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="387c9-161">Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="387c9-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="387c9-162">In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="387c9-162">The following image shows an example of a mode of delivery.</span></span>

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="387c9-164">Inkomsten-/uitgavenrekening instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-164">Set up income/expense account</span></span>

<span data-ttu-id="387c9-165">Volg deze stappen om een inkomsten-/uitgavenrekening in te stellen.</span><span class="sxs-lookup"><span data-stu-id="387c9-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="387c9-166">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Inkomsten-/uitgavenrekening**.</span><span class="sxs-lookup"><span data-stu-id="387c9-166">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="387c9-167">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-167">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="387c9-168">Voer een naam in onder **Naam**.</span><span class="sxs-lookup"><span data-stu-id="387c9-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="387c9-169">Voer onder **Zoeknaam** een zoeknaam in.</span><span class="sxs-lookup"><span data-stu-id="387c9-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="387c9-170">Voer onder **Rekeningtype** een type rekening in.</span><span class="sxs-lookup"><span data-stu-id="387c9-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="387c9-171">Voer zo nodig tekst in voor **Berichtregel 1**, **Berichtregel 2**, **Strooktekst 1** en **Strooktekst 2**.</span><span class="sxs-lookup"><span data-stu-id="387c9-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="387c9-172">Voer onder **Boeking** boekingsinformatie in.</span><span class="sxs-lookup"><span data-stu-id="387c9-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="387c9-173">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-173">On the action pane, select **Save**.</span></span>

<span data-ttu-id="387c9-174">De volgende afbeelding toont een voorbeeld van een inkomsten-/uitgavenrekening.</span><span class="sxs-lookup"><span data-stu-id="387c9-174">The following image shows an example of an income/expense account.</span></span>

![Inkomsten-/uitgavenrekeningen instellen](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="387c9-176">Secties instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-176">Set up sections</span></span>

<span data-ttu-id="387c9-177">Volg deze stappen om secties in te stellen.</span><span class="sxs-lookup"><span data-stu-id="387c9-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="387c9-178">Selecteer in het actievenster het tabblad **Instellingen** en klik op **Secties**.</span><span class="sxs-lookup"><span data-stu-id="387c9-178">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="387c9-179">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-179">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="387c9-180">Voer onder **Sectienummer** een sectienummer in.</span><span class="sxs-lookup"><span data-stu-id="387c9-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="387c9-181">Voer onder **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="387c9-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="387c9-182">Voer onder **Sectiegrootte** een sectiegrootte in.</span><span class="sxs-lookup"><span data-stu-id="387c9-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="387c9-183">Configureer naar behoefte aanvullende instellingen voor **Algemeen** en **Verkoopstatistieken**.</span><span class="sxs-lookup"><span data-stu-id="387c9-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="387c9-184">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-184">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="387c9-185">De toewijzing van een afhandelingsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="387c9-186">Volg deze stappen als u de toewijzing van een afhandelingsgroep wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="387c9-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="387c9-187">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Toewijzing afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="387c9-187">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="387c9-188">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-188">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="387c9-189">Selecteer een afhandelingsgroep in de vervolgkeuzelijst **Afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="387c9-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="387c9-190">Voer in de vervolgkeuzelijst **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="387c9-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="387c9-191">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-191">On the action pane, select **Save**</span></span>

<span data-ttu-id="387c9-192">De volgende afbeelding toont een voorbeeld van de instellingen voor de toewijzing van een afhandelingsgroep.</span><span class="sxs-lookup"><span data-stu-id="387c9-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Toewijzingen van een afhandelingsgroep instellen](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="387c9-194">Kluizen instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-194">Set up safes</span></span>

<span data-ttu-id="387c9-195">Volg deze stappen om kluizen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="387c9-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="387c9-196">Selecteer in het actievenster het tabblad **Instellingen** en klik op **Kluizen**.</span><span class="sxs-lookup"><span data-stu-id="387c9-196">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="387c9-197">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-197">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="387c9-198">Voer een naam in voor de kluis.</span><span class="sxs-lookup"><span data-stu-id="387c9-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="387c9-199">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="387c9-199">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="387c9-200">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="387c9-200">Additional resources</span></span>

[<span data-ttu-id="387c9-201">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="387c9-201">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="387c9-202">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="387c9-202">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="387c9-203">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-203">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="387c9-204">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="387c9-204">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
