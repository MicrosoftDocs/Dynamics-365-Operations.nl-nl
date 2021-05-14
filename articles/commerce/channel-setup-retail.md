---
title: Een detailhandelkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw detailhandelkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937529"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="26ca0-103">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="26ca0-104">In dit onderwerp wordt beschreven hoe u een nieuw detailhandelkanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26ca0-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="26ca0-105">Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="26ca0-106">Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd).</span><span class="sxs-lookup"><span data-stu-id="26ca0-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="26ca0-107">Iedere Retail-winkelkanaal kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben.</span><span class="sxs-lookup"><span data-stu-id="26ca0-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="26ca0-108">U moet al deze elementen instellen voordat u een Retail-winkelkanaal kunt maken.</span><span class="sxs-lookup"><span data-stu-id="26ca0-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="26ca0-109">Controleer vóór het maken van een detailhandelkanaal of u de [Vereisten voor afzetkanalen](channels-prerequisites.md) hebt gevolgd.</span><span class="sxs-lookup"><span data-stu-id="26ca0-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="26ca0-110">Een nieuw detailhandelafzetkanaal maken en configureren</span><span class="sxs-lookup"><span data-stu-id="26ca0-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="26ca0-111">Ga in het navigatievenster naar **Modules \> Kanalen \> Winkels \> Alle winkels**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="26ca0-112">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="26ca0-113">Typ in het veld **Naam** een naam voor het nieuwe kanaal.</span><span class="sxs-lookup"><span data-stu-id="26ca0-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="26ca0-114">Geef in het veld **Winkelnummer** een uniek winkelnummer op.</span><span class="sxs-lookup"><span data-stu-id="26ca0-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="26ca0-115">Het nummer kan alfanumeriek zijn met een maximum van 10 tekens.</span><span class="sxs-lookup"><span data-stu-id="26ca0-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="26ca0-116">Voer in de vervolgkeuzelijst **Rechtspersoon** de toepasselijke rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="26ca0-117">Voer in de vervolgkeuzelijst **Magazijn** het juiste magazijn in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="26ca0-118">Selecteer in het veld **Winkeltijdzone** de juiste tijdzone.</span><span class="sxs-lookup"><span data-stu-id="26ca0-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="26ca0-119">Selecteer in de vervolgkeuzelijst **Btw-groep** een toepasselijke btw-groep voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="26ca0-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="26ca0-120">Selecteer in het veld **Valuta** de juiste valuta.</span><span class="sxs-lookup"><span data-stu-id="26ca0-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="26ca0-121">Geef in het veld **Adresboek klant** een geldig adresboek op.</span><span class="sxs-lookup"><span data-stu-id="26ca0-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="26ca0-122">Geef in het veld **Standaardklant** een geldige standaardklant op.</span><span class="sxs-lookup"><span data-stu-id="26ca0-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="26ca0-123">Selecteer in het veld **Functionaliteitsprofiel** een functionaliteitsprofiel, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="26ca0-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="26ca0-124">Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.</span><span class="sxs-lookup"><span data-stu-id="26ca0-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="26ca0-125">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="26ca0-126">De volgende afbeelding toont het maken van een nieuw detailhandelkanaal.</span><span class="sxs-lookup"><span data-stu-id="26ca0-126">The following image shows the creation of a new retail channel.</span></span>

![Nieuw detailhandelafzetkanaal](media/channel-setup-retail-1.png)

<span data-ttu-id="26ca0-128">In de volgende afbeelding ziet u een voorbeeld van een detailhandelafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="26ca0-128">The following image shows an example retail channel.</span></span>

![Voorbeeld van detailhandelafzetkanaal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="26ca0-130">Overige instellingen</span><span class="sxs-lookup"><span data-stu-id="26ca0-130">Other settings</span></span>

<span data-ttu-id="26ca0-131">Er zijn talloze andere optionele instellingen die u op basis van de behoeften van de detailhandelwinkel kunt instellen in de secties **Overzicht/afsluiting** en **Overige**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="26ca0-132">Zie ook [Schermindelingen voor het POS](pos-screen-layouts.md) voor informatie over het instellen van de standaardschermindeling in de sectie **Schermindeling** en [Retail-hardwarestation configureren en installeren](retail-hardware-station-configuration-installation.md) voor informatie het instellen van de sectie **Hardwarestations**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="26ca0-133">In de volgende afbeelding ziet u een voorbeeldconfiguratie van een detailhandelafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="26ca0-133">The following image shows an example retail channel setup configuration.</span></span>

![Voorbeeldconfiguratie van detailhandelafzetkanaal](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="26ca0-135">Aanvullende kanaalinstellingen</span><span class="sxs-lookup"><span data-stu-id="26ca0-135">Additional channel set up</span></span>

<span data-ttu-id="26ca0-136">Er zijn nog meer zaken die u moet instellen voor een kanaal. Deze vindt u in de sectie **Instellingen** van het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="26ca0-137">Aanvullende taken die nodig zijn voor het instellen van online kanalen, zijn onder andere het instellen van betalingsmethoden, contantdeclaraties, leveringsmethoden, inkomsten- en onkostenrekeningen, secties, de toewijzing van afhandelingsgroepen en kluizen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="26ca0-138">De volgende afbeelding toont diverse aanvullende opties voor het instellen van detailhandelskanalen op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanaal instellen](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="26ca0-140">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-140">Set up payment methods</span></span>

<span data-ttu-id="26ca0-141">Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="26ca0-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="26ca0-142">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="26ca0-143">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="26ca0-144">Selecteer in het navigatievenster een gewenste betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="26ca0-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="26ca0-145">Geef in de sectie **Algemeen** een naam op in **Bewerkingsnaam** en configureer eventuele andere instellingen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="26ca0-146">Configureer eventuele aanvullende instellingen voor het betalingstype.</span><span class="sxs-lookup"><span data-stu-id="26ca0-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="26ca0-147">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="26ca0-148">In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.</span><span class="sxs-lookup"><span data-stu-id="26ca0-148">The following image shows an example of a cash payment method.</span></span>

![Voorbeeldbetalingsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="26ca0-150">Contantdeclaratie instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-150">Set up cash declaration</span></span>

1. <span data-ttu-id="26ca0-151">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Contantdeclaratie**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="26ca0-152">Selecteer in het actievenster de optie **Nieuw** en maak vervolgens alle **Munt**- en **Coupure**-denominaties die van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="26ca0-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="26ca0-153">In de volgende afbeelding ziet u een voorbeeld van een contantdeclaratie.</span><span class="sxs-lookup"><span data-stu-id="26ca0-153">The following image shows an example of a cash declaration.</span></span>

![Contantdeclaraties instellen](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="26ca0-155">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-155">Set up modes of delivery</span></span>

<span data-ttu-id="26ca0-156">U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="26ca0-157">Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="26ca0-158">Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="26ca0-159">Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.</span><span class="sxs-lookup"><span data-stu-id="26ca0-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="26ca0-160">Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="26ca0-161">Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="26ca0-162">In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="26ca0-162">The following image shows an example of a mode of delivery.</span></span>

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="26ca0-164">Inkomsten-/uitgavenrekening instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-164">Set up income/expense account</span></span>

<span data-ttu-id="26ca0-165">Volg deze stappen om een inkomsten-/uitgavenrekening in te stellen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="26ca0-166">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Inkomsten-/uitgavenrekening**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="26ca0-167">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="26ca0-168">Voer een naam in onder **Naam**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="26ca0-169">Voer onder **Zoeknaam** een zoeknaam in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="26ca0-170">Voer onder **Rekeningtype** een type rekening in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="26ca0-171">Voer zo nodig tekst in voor **Berichtregel 1**, **Berichtregel 2**, **Strooktekst 1** en **Strooktekst 2**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="26ca0-172">Voer onder **Boeking** boekingsinformatie in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="26ca0-173">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="26ca0-174">De volgende afbeelding toont een voorbeeld van een inkomsten-/uitgavenrekening.</span><span class="sxs-lookup"><span data-stu-id="26ca0-174">The following image shows an example of an income/expense account.</span></span>

![Inkomsten-/uitgavenrekeningen instellen](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="26ca0-176">Secties instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-176">Set up sections</span></span>

<span data-ttu-id="26ca0-177">Volg deze stappen om secties in te stellen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="26ca0-178">Selecteer in het actievenster het tabblad **Instellingen** en klik op **Secties**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="26ca0-179">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="26ca0-180">Voer onder **Sectienummer** een sectienummer in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="26ca0-181">Voer onder **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="26ca0-182">Voer onder **Sectiegrootte** een sectiegrootte in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="26ca0-183">Configureer naar behoefte aanvullende instellingen voor **Algemeen** en **Verkoopstatistieken**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="26ca0-184">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="26ca0-185">De toewijzing van een afhandelingsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="26ca0-186">Volg deze stappen als u de toewijzing van een afhandelingsgroep wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="26ca0-187">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Toewijzing afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="26ca0-188">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="26ca0-189">Selecteer een afhandelingsgroep in de vervolgkeuzelijst **Afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="26ca0-190">Voer in de vervolgkeuzelijst **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="26ca0-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="26ca0-191">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="26ca0-192">De volgende afbeelding toont een voorbeeld van de instellingen voor de toewijzing van een afhandelingsgroep.</span><span class="sxs-lookup"><span data-stu-id="26ca0-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Toewijzingen van een afhandelingsgroep instellen](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="26ca0-194">Kluizen instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-194">Set up safes</span></span>

<span data-ttu-id="26ca0-195">Volg deze stappen om kluizen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="26ca0-196">Selecteer in het actievenster het tabblad **Instellingen** en klik op **Kluizen**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="26ca0-197">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="26ca0-198">Voer een naam in voor de kluis.</span><span class="sxs-lookup"><span data-stu-id="26ca0-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="26ca0-199">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="26ca0-200">Zorgen dat unieke transactie-id's worden gemaakt</span><span class="sxs-lookup"><span data-stu-id="26ca0-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="26ca0-201">Vanaf Commerce versie 10.0.18 zijn transactie-id's die zijn gegenereerd voor het POS opeenvolgend en bevatten de volgende delen:</span><span class="sxs-lookup"><span data-stu-id="26ca0-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="26ca0-202">Een vast deel, dat een samenvoeging is van een winkel-id en een terminal-id.</span><span class="sxs-lookup"><span data-stu-id="26ca0-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="26ca0-203">Een volgnummer, dat uit een nummerreeks wordt genomen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="26ca0-204">Specifiek gezegd is de indeling *{store}{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="26ca0-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="26ca0-205">Aangezien transactie-id's kunnen worden gegenereerd in offline en online modi, zijn er ook wel eens dubbele transactie-id's gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="26ca0-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="26ca0-206">Het verwijderen van dubbele transactie-id's vereist veel handmatig herstel van gegevens.</span><span class="sxs-lookup"><span data-stu-id="26ca0-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="26ca0-207">In Commerce versie 10.0.19 is de transactie-id-indeling bijgewerkt: het nummerreeksdeel is verwijderd en in plaats daarvan wordt een nummer van 13 cijfers gebruikt dat is gegenereerd door de tijd sinds het jaar 1970 te berekenen in milliseconden.</span><span class="sxs-lookup"><span data-stu-id="26ca0-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="26ca0-208">Met deze wijziging is de nieuwe transactie-ID-indeling nu *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="26ca0-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="26ca0-209">Vanaf deze update is de transactie-id niet-sequentieel en dus altijd uniek.</span><span class="sxs-lookup"><span data-stu-id="26ca0-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="26ca0-210">Transactie-id's zijn alleen bedoeld voor intern systeemgebruik, dus hoeven ze niet opeenvolgend te zijn.</span><span class="sxs-lookup"><span data-stu-id="26ca0-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="26ca0-211">In veel landen moeten kassabon-id's echter wel opeenvolgend zijn.</span><span class="sxs-lookup"><span data-stu-id="26ca0-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="26ca0-212">De nieuwe functie voor de indeling van transactie-id's kan worden ingeschakeld vanuit het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="26ca0-213">Als u het gebruik van nieuwe transactie-id's wilt inschakelen, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="26ca0-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="26ca0-214">Ga in Commerce Headquarters naar **Systeembeheer \> Werkgebieden \> Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="26ca0-215">Filter op de module Retail en Commerce.</span><span class="sxs-lookup"><span data-stu-id="26ca0-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="26ca0-216">Zoek de functienaam **Nieuwe transactie-id inschakelen om dubbele transactie-id's te voorkomen**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="26ca0-217">Selecteer de functie en selecteer vervolgens **Nu inschakelen** in het het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="26ca0-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="26ca0-218">Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="26ca0-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="26ca0-219">Voer de taken **1070 (Kanaalconfiguratie)** en **1170 POS-taakregistratie** uit om de ingeschakelde functie te synchroniseren met de winkels.</span><span class="sxs-lookup"><span data-stu-id="26ca0-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="26ca0-220">Nadat de wijzigingen naar de winkels zijn verzonden, moeten POS-terminals worden gesloten en opnieuw worden geopend om de nieuwe transactie-id-indeling te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="26ca0-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="26ca0-221">Nadat de functie voor de nieuwe transactie-id-indeling is ingeschakeld, kunt u deze functie niet meer uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="26ca0-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="26ca0-222">Als deze echt moet worden uitgeschakeld, neem dan contact op met de Commerce-ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="26ca0-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26ca0-223">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="26ca0-223">Additional resources</span></span>

[<span data-ttu-id="26ca0-224">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="26ca0-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="26ca0-225">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="26ca0-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="26ca0-226">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="26ca0-227">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="26ca0-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
