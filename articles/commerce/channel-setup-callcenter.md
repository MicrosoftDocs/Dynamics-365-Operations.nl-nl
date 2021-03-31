---
title: Een callcenterkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 878774c8e5485211525e7e7b63973173f6874b26
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218364"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="d8776-103">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="d8776-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d8776-104">In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8776-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8776-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d8776-105">Overview</span></span>


<span data-ttu-id="d8776-106">In Dynamics 365 Commerce is een callcenter een type handelsafzetkanaal dat kan worden gedefinieerd in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="d8776-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="d8776-107">Door een afzetkanaal voor uw callcenter-entiteiten te definiëren, kan het systeem specifieke gegevens en orderverwerkingsinstellingen koppelen aan verkooporders.</span><span class="sxs-lookup"><span data-stu-id="d8776-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="d8776-108">Een bedrijf kan meerdere callcenterkanalen in Commerce definiëren, maar het is belangrijk om te weten dat een individuele gebruiker slechts aan één callcenterkanaal kan worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d8776-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="d8776-109">Controleer vóór het maken van een nieuw callcenterkanaal of u de [Vereisten voor het instellen van kanalen](channels-prerequisites.md) hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="d8776-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="d8776-110">Een nieuw callcenterafzetkanaal maken en configureren</span><span class="sxs-lookup"><span data-stu-id="d8776-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="d8776-111">Voer de volgende stappen uit om een nieuw callcenterafzetkanaal te maken en te configureren.</span><span class="sxs-lookup"><span data-stu-id="d8776-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="d8776-112">Ga op de navigatiepagina naar **Detailhandel en commerce \> Kanalen \> Callcenters \> Alle callcenters**.</span><span class="sxs-lookup"><span data-stu-id="d8776-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="d8776-113">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d8776-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d8776-114">Typ in het veld **Naam** een naam voor het nieuwe kanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d8776-115">Selecteer de juiste **Rechtspersoon** in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="d8776-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="d8776-116">Selecteer de juiste **Magazijn** locatie in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="d8776-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="d8776-117">Deze locatie wordt gebruikt als standaardwaarde voor verkooporders die zijn gemaakt voor dit callcenterkanaal, tenzij er andere standaardwaarden zijn gedefinieerd op het niveau van de klant of het artikel.</span><span class="sxs-lookup"><span data-stu-id="d8776-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="d8776-118">Geef in het veld **Standaardklant** een geldige standaardklant op.</span><span class="sxs-lookup"><span data-stu-id="d8776-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="d8776-119">Deze gegevens worden gebruikt om te helpen bij het automatisch vullen van standaardwaarden wanneer er nieuwe klantrecords worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d8776-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="d8776-120">Bij het maken van callcenterorders is het niet raadzaam orders voor de standaardklant te maken.</span><span class="sxs-lookup"><span data-stu-id="d8776-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="d8776-121">Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.</span><span class="sxs-lookup"><span data-stu-id="d8776-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="d8776-122">Wanneer orders in het callcenter worden gemaakt en verwerkt, wordt het e-mailprofiel gebruikt om automatische e-mailmeldingen naar klanten te activeren met informatie over hun orderstatus.</span><span class="sxs-lookup"><span data-stu-id="d8776-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="d8776-123">Geef een infocode op voor **Prijsoverschrijving**.</span><span class="sxs-lookup"><span data-stu-id="d8776-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="d8776-124">Mogelijk moet u hiervoor eerst een informatiecode maken.</span><span class="sxs-lookup"><span data-stu-id="d8776-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="d8776-125">Deze informatiecode bevat de set met redencodes die de gebruiker moet kiezen bij het gebruik van de functie voor prijsoverschrijving op een callcenterorder.</span><span class="sxs-lookup"><span data-stu-id="d8776-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="d8776-126">Geef een infocode op voor **Wachtstandcode**.</span><span class="sxs-lookup"><span data-stu-id="d8776-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="d8776-127">Mogelijk moet u hiervoor eerst een informatiecode maken.</span><span class="sxs-lookup"><span data-stu-id="d8776-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="d8776-128">Deze informatiecode bevat de set met optionele redencodes die de gebruiker moet kiezen bij het in de wacht plaatsen van een order.</span><span class="sxs-lookup"><span data-stu-id="d8776-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="d8776-129">Een infocode op voor **Krediet**.</span><span class="sxs-lookup"><span data-stu-id="d8776-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="d8776-130">Mogelijk moet u hiervoor eerst een informatiecode maken.</span><span class="sxs-lookup"><span data-stu-id="d8776-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="d8776-131">Deze informatiecode bevat de set met redencodes waaruit de gebruiker kan kiezen bij gebruik van de orderkredietfunctionaliteit van het callcenter om de klant terug te betalen vanwege redenen van de klantenservice.</span><span class="sxs-lookup"><span data-stu-id="d8776-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="d8776-132">Optioneel: financiële dimensies instellen op het sneltabblad **Financiële dimensies**.</span><span class="sxs-lookup"><span data-stu-id="d8776-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="d8776-133">De dimensies die hier worden ingevoerd, worden standaard uitgevoerd op alle verkooporders die in dit callcenterkanaal zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d8776-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="d8776-134">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d8776-134">Click **Save**.</span></span>

<span data-ttu-id="d8776-135">De volgende afbeelding toont het maken van een nieuw callcenterafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-135">The following image shows the creation of a new call center channel.</span></span>

![Nieuw callcenterafzetkanaal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="d8776-137">In de volgende afbeelding ziet u een voorbeeld van een callcenterafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-137">The following image shows an example call center channel.</span></span>

![Voorbeeld van callcenterafzetkanaal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="d8776-139">Aanvullende afzetkanaalinstellingen</span><span class="sxs-lookup"><span data-stu-id="d8776-139">Additional channel setup</span></span>

<span data-ttu-id="d8776-140">Aanvullende taken die nodig zijn voor het instellen van callcenterkanalen, zijn onder andere het instellen van betalingsmethoden en leveringsmethoden.</span><span class="sxs-lookup"><span data-stu-id="d8776-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="d8776-141">De volgende afbeelding toont de instellingsopties voor **Leveringsmethoden** en **Betalingsmethoden** op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="d8776-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Aanvullende acties voor het instellen van een callcenterkanaal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d8776-143">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="d8776-143">Set up payment methods</span></span>

<span data-ttu-id="d8776-144">Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d8776-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="d8776-145">Gebruikers moeten een keuze maken uit vooraf gedefinieerde betalingsmethoden om ze te koppelen aan het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="d8776-146">Voordat u uw betalingsmethoden voor callcenters gaat instellen, moet u eerst uw hoofdbetalingsmethoden instellen in **Detailhandel en commerce \> Afzetkanaalinstellingen \> Betalingsmethoden \> Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="d8776-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="d8776-147">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="d8776-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="d8776-148">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d8776-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d8776-149">Selecteer in het navigatievenster een betalingsmethode van de beschikbare vooraf gedefinieerde betalingen.</span><span class="sxs-lookup"><span data-stu-id="d8776-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="d8776-150">Configureer eventuele aanvullende instellingen voor het betalingstype.</span><span class="sxs-lookup"><span data-stu-id="d8776-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="d8776-151">Voor creditcards, geschenkbonnen of loyaliteitskaarten is aanvullende instelling vereist via de functie **Kaart instellen**.</span><span class="sxs-lookup"><span data-stu-id="d8776-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="d8776-152">Configureer de juiste boekingsrekeningen voor het betalingstype in de sectie **Boeking**.</span><span class="sxs-lookup"><span data-stu-id="d8776-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="d8776-153">Klik in het actievenster op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d8776-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="d8776-154">In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.</span><span class="sxs-lookup"><span data-stu-id="d8776-154">The following image shows an example of a cash payment method.</span></span>

![Voorbeeldbetalingsmethoden](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d8776-156">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="d8776-156">Set up modes of delivery</span></span>

<span data-ttu-id="d8776-157">U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="d8776-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d8776-158">Voer de volgende stappen uit om een leveringsmethode te wijzigen of toe te voegen aan het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="d8776-159">Selecteer **Leveringsmethoden beheren** in het formulier Leveringsmethoden van het callcenter</span><span class="sxs-lookup"><span data-stu-id="d8776-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="d8776-160">Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.</span><span class="sxs-lookup"><span data-stu-id="d8776-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d8776-161">Klik in de sectie **Detailhandelkanalen** op **Regel toevoegen** om het callcenterkanaal toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d8776-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="d8776-162">Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="d8776-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="d8776-163">Zorg ervoor dat de leveringsmethode is geconfigureerd met gegevens op het sneltabblad **Producten** en op het sneltabblad **Adressen**.</span><span class="sxs-lookup"><span data-stu-id="d8776-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="d8776-164">Als er geen producten of leveringsadressen geldig zijn voor de leveringsmethode, wordt bij het invoeren van de order fouten geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d8776-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="d8776-165">Nadat er wijzigingen zijn aangebracht in de callcentermodus voor leveringsconfiguraties, moet de taak **Leveringsmethoden verwerken** worden uitgevoerd om de wijzigingsmatrix uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="d8776-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="d8776-166">U vindt deze taak via **Detailhandel en commerce \> IT detailhandel en commerce \> Leveringsmethoden verwerken**.</span><span class="sxs-lookup"><span data-stu-id="d8776-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="d8776-167">In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="d8776-167">The following image shows an example of a mode of delivery.</span></span>

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="d8776-169">Kanaalgebruikers instellen</span><span class="sxs-lookup"><span data-stu-id="d8776-169">Set up channel users</span></span>

<span data-ttu-id="d8776-170">Als u een verkooporder wilt maken die is gekoppeld aan het callcenterkanaal vanuit Commerce-hoofdkantoor, moet de gebruiker die de verkooporder maakt, zijn gekoppeld aan het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="d8776-171">De gebruiker kan een verkooporder die in Commerce-hoofdkantoor is gemaakt niet handmatig koppelen aan het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="d8776-172">De koppeling is systematisch en is gebaseerd op de gebruiker en de relatie van de gebruiker met het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="d8776-173">Een gebruiker kan slechts aan één callcenterkanaal worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d8776-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="d8776-174">Selecteer in het actievenster het tabblad **Kanaal** en selecteer **Kanaalgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="d8776-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="d8776-175">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d8776-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d8776-176">Kies een bestaande **gebruikers-id** uit de vervolgkeuzelijst om deze gebruiker aan het callcenterkanaal te koppelen</span><span class="sxs-lookup"><span data-stu-id="d8776-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="d8776-177">Nadat de instellingen voor de kanaalgebruiker zijn ingevoerd en de gebruiker een nieuwe verkooporder maakt in Commerce-hoofdkantoor, moet de verkooporder worden gekoppeld aan het bijbehorende callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="d8776-178">Alle configuraties voor dit kanaal worden systematisch op de verkooporder toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8776-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="d8776-179">Een gebruiker kan bevestigen aan welk callcenterkanaal de verkooporder is gekoppeld door de kanaalnaamverwijzing in de verkooporderkop weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d8776-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="d8776-180">Prijsgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="d8776-180">Set up price groups</span></span>

<span data-ttu-id="d8776-181">Prijsgroepen zijn optioneel, maar als deze worden gebruikt, kunnen ze bepalen welke verkoopprijzen worden aangeboden aan klanten die orders plaatsen in het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="d8776-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="d8776-182">Als er geen prijsgroep voor de klant is geconfigureerd of als er geen prijsgroepen op de verkooporder worden toegepast (met het veld **Broncode-id** in de koptekst van de callcenterorder), wordt de afzetkanaalprijsgroep gebruikt om artikelprijzen te zoeken.</span><span class="sxs-lookup"><span data-stu-id="d8776-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="d8776-183">Als er geen prijsgroep wordt gevonden op het callcenterkanaal, worden de standaardprijzen voor de artikelmodellen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d8776-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="d8776-184">Ga als volgt te werk om een prijsgroep in te stellen.</span><span class="sxs-lookup"><span data-stu-id="d8776-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="d8776-185">Klik in het actievenster op het tabblad **Kanaal** en selecteer **Prijsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="d8776-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="d8776-186">Klik in het actievenster op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d8776-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="d8776-187">Selecteer een **detailhandelsprijsgroep** in de keuzelijst.</span><span class="sxs-lookup"><span data-stu-id="d8776-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8776-188">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d8776-188">Additional resources</span></span>

[<span data-ttu-id="d8776-189">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="d8776-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d8776-190">Verkoopfunctionaliteit callcenter</span><span class="sxs-lookup"><span data-stu-id="d8776-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="d8776-191">Orderverwerkingsopties voor callcenter instellen</span><span class="sxs-lookup"><span data-stu-id="d8776-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="d8776-192">Callcentercatalogi</span><span class="sxs-lookup"><span data-stu-id="d8776-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="d8776-193">Instellen en werken met fraudewaarschuwingen</span><span class="sxs-lookup"><span data-stu-id="d8776-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="d8776-194">Continuïteitsprogramma's instellen voor callcenters</span><span class="sxs-lookup"><span data-stu-id="d8776-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]