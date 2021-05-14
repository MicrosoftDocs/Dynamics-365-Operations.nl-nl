---
title: Een online afzetkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw online afzetkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 07/02/2020
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
ms.openlocfilehash: f0f1e0f3e7145c66b8f2b082b44ad7035c57d947
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936939"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="28862-103">Een online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="28862-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="28862-104">In dit onderwerp wordt beschreven hoe u een nieuw online afzetkanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="28862-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="28862-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="28862-105">Overview</span></span>

<span data-ttu-id="28862-106">Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen.</span><span class="sxs-lookup"><span data-stu-id="28862-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="28862-107">Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd).</span><span class="sxs-lookup"><span data-stu-id="28862-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="28862-108">Een online winkel biedt klanten de mogelijkheid om producten zowel in de online winkel als in de fysieke winkel van de detailhandelaar te kopen.</span><span class="sxs-lookup"><span data-stu-id="28862-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="28862-109">Als u een online winkel in Commerce wilt maken, moet u eerst een online kanaal maken.</span><span class="sxs-lookup"><span data-stu-id="28862-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="28862-110">Controleer vóór het maken van een nieuw online kanaal of u de [Vereisten voor het instellen van kanalen](channels-prerequisites.md) hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="28862-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="28862-111">Voordat u een nieuwe site kunt maken, moet er minimaal één online winkel zijn gemaakt in Commerce.</span><span class="sxs-lookup"><span data-stu-id="28862-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="28862-112">Zie voor meer informatie [Een e-commerce-site maken](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="28862-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="28862-113">Een nieuw online afzetkanaal maken en configureren</span><span class="sxs-lookup"><span data-stu-id="28862-113">Create and configure a new online channel</span></span>

<span data-ttu-id="28862-114">Voer de volgende stappen uit om een nieuw online afzetkanaal te maken en te configureren.</span><span class="sxs-lookup"><span data-stu-id="28862-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="28862-115">Ga in het navigatievenster naar **Modules \> Kanalen \> Online winkels**.</span><span class="sxs-lookup"><span data-stu-id="28862-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="28862-116">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="28862-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="28862-117">Typ in het veld **Naam** een naam voor het nieuwe kanaal.</span><span class="sxs-lookup"><span data-stu-id="28862-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="28862-118">Voer in de vervolgkeuzelijst **Rechtspersoon** de toepasselijke rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="28862-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="28862-119">Voer in de vervolgkeuzelijst **Magazijn** het juiste magazijn in.</span><span class="sxs-lookup"><span data-stu-id="28862-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="28862-120">Selecteer in het veld **Winkeltijdzone** de juiste tijdzone.</span><span class="sxs-lookup"><span data-stu-id="28862-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="28862-121">Selecteer in het veld **Valuta** de juiste valuta.</span><span class="sxs-lookup"><span data-stu-id="28862-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="28862-122">Geef in het veld **Standaardklant** een geldige standaardklant op.</span><span class="sxs-lookup"><span data-stu-id="28862-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="28862-123">Geef in het veld **Adresboek klant** een geldig adresboek op.</span><span class="sxs-lookup"><span data-stu-id="28862-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="28862-124">Selecteer in het veld **Functionaliteitsprofiel** een functionaliteitsprofiel, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="28862-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="28862-125">Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.</span><span class="sxs-lookup"><span data-stu-id="28862-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="28862-126">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="28862-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="28862-127">De volgende afbeelding toont het maken van een nieuw online afzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="28862-127">The following image shows the creation of a new online channel.</span></span>

![Nieuw online afzetkanaal](media/channel-setup-online-1.png)

<span data-ttu-id="28862-129">In de volgende afbeelding ziet u een voorbeeld van een online afzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="28862-129">The following image shows an example online channel.</span></span>

![Voorbeeld van online afzetkanaal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="28862-131">Talen instellen</span><span class="sxs-lookup"><span data-stu-id="28862-131">Set up languages</span></span>

<span data-ttu-id="28862-132">Als uw e-Commerce site ondersteuning biedt voor meerdere talen, vouwt u de sectie **Talen** uit en voegt u de toepasselijke extra talen toe.</span><span class="sxs-lookup"><span data-stu-id="28862-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="28862-133">Betalingsrekening instellen</span><span class="sxs-lookup"><span data-stu-id="28862-133">Set up payment account</span></span>

<span data-ttu-id="28862-134">In de sectie **Betalingsrekening** kunt u een externe betalingsverschaffer toevoegen.</span><span class="sxs-lookup"><span data-stu-id="28862-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="28862-135">Zie [Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md) voor meer informatie over het instellen van een Adyen-betalingsconnector.</span><span class="sxs-lookup"><span data-stu-id="28862-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="28862-136">Aanvullende afzetkanaalinstellingen</span><span class="sxs-lookup"><span data-stu-id="28862-136">Additional channel setup</span></span>

<span data-ttu-id="28862-137">Aanvullende taken die nodig zijn voor het instellen van online kanalen, zijn onder andere het instellen van betalingsmethoden, leveringsmethoden en de toewijzing van afhandelingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="28862-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="28862-138">De volgende afbeelding toont de instellingsopties voor **Leveringsmethoden**, **Betalingsmethoden** en **Toewijzing van afhandelingsgroepen** op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="28862-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Aanvullende acties voor het instellen van een online kanaal](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="28862-140">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="28862-140">Set up payment methods</span></span>

<span data-ttu-id="28862-141">Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="28862-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="28862-142">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="28862-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="28862-143">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="28862-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="28862-144">Selecteer in het navigatievenster een gewenste betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="28862-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="28862-145">Geef in de sectie **Algemeen** een naam op in **Bewerkingsnaam** en configureer eventuele andere instellingen.</span><span class="sxs-lookup"><span data-stu-id="28862-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="28862-146">Configureer eventuele aanvullende instellingen voor het betalingstype.</span><span class="sxs-lookup"><span data-stu-id="28862-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="28862-147">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="28862-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="28862-148">In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.</span><span class="sxs-lookup"><span data-stu-id="28862-148">The following image shows an example of a cash payment method.</span></span>

![Voorbeeldbetalingsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="28862-150">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="28862-150">Set up modes of delivery</span></span>

<span data-ttu-id="28862-151">U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="28862-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="28862-152">Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.</span><span class="sxs-lookup"><span data-stu-id="28862-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="28862-153">Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="28862-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="28862-154">Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.</span><span class="sxs-lookup"><span data-stu-id="28862-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="28862-155">Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="28862-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="28862-156">Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="28862-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="28862-157">In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="28862-157">The following image shows an example of a mode of delivery.</span></span>

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="28862-159">De toewijzing van een afhandelingsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="28862-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="28862-160">Volg deze stappen als u de toewijzing van een afhandelingsgroep wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="28862-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="28862-161">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Toewijzing afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="28862-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="28862-162">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="28862-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="28862-163">Selecteer een afhandelingsgroep in de vervolgkeuzelijst **Afhandelingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="28862-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="28862-164">Voer in de vervolgkeuzelijst **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="28862-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="28862-165">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="28862-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="28862-166">De volgende afbeelding toont een voorbeeld van de instellingen voor de toewijzing van een afhandelingsgroep.</span><span class="sxs-lookup"><span data-stu-id="28862-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Toewijzing van een afhandelingsgroep instellen](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="28862-168">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="28862-168">Additional resources</span></span>

[<span data-ttu-id="28862-169">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="28862-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="28862-170">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="28862-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="28862-171">Een detailhandelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="28862-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="28862-172">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="28862-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="28862-173">Dynamics 365-betalingsconnector voor Adyen</span><span class="sxs-lookup"><span data-stu-id="28862-173">Dynamics 365 Payment Connector for Adyen</span></span>](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]