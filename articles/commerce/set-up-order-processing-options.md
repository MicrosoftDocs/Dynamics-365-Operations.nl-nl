---
title: Callcenterkanalen instellen
description: Dit onderwerp biedt informatie over het verwerken van procesorders voor callcenters met gebruik van Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28954eab857a06da3978ca362081dfc3c525354d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022144"
---
# <a name="set-up-call-center-channels"></a><span data-ttu-id="287d1-103">Callcenterkanalen instellen</span><span class="sxs-lookup"><span data-stu-id="287d1-103">Set up call center channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="287d1-104">Een bedrijf kan meerdere callcenterkanalen definiëren in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="287d1-104">A company can define multiple call center channels in Dynamics 365 Commerce.</span></span> <span data-ttu-id="287d1-105">Callcenterkanalen worden geconfigureerd via **Detailhandel en commerce** \> **Kanalen** \> **Callcenters** \> **Alle callcenters**, en zijn specifiek voor een rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="287d1-105">Call center channels are configured at **Retail and Commerce** \> **Channels** \> **Call centers** \> **All call centers**, and they are specific to a legal entity.</span></span>

<span data-ttu-id="287d1-106">Wanneer een nieuwe callcenterkanaal wordt gemaakt, wordt hieraan systematisch een nummer van een operationele eenheid toegewezen.</span><span class="sxs-lookup"><span data-stu-id="287d1-106">When a new call center channel is created, it's systematically assigned an operating unit number.</span></span> <span data-ttu-id="287d1-107">Omdat callcenters worden gemaakt als operationele eenheden, kunnen gebruikers het callcenterkanaal koppelen aan verschillende Commerce-functies, zoals assortimenten, catalogi en specifieke leveringsmethoden.</span><span class="sxs-lookup"><span data-stu-id="287d1-107">Because call centers are created as operating units, users can link the call center channel to various Commerce features, such as assortments, catalogs, and specific modes of delivery.</span></span>

<span data-ttu-id="287d1-108">Een standaardmagazijn kan worden geconfigureerd voor het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-108">A default warehouse can be configured on the call center channel.</span></span> <span data-ttu-id="287d1-109">Wanneer verkooporders worden gemaakt voor dat kanaal, wordt het standaardmagazijn automatisch ingevoerd in de verkooporderkoptekst, tenzij een ander magazijn is gedefinieerd voor de klant die is geselecteerd voor de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="287d1-109">Then, when sales orders are created in that channel, the default warehouse is automatically entered on the sales order header, unless another warehouse has been defined on the customer that is selected for the sales order.</span></span> <span data-ttu-id="287d1-110">Standaard wordt in dat geval het magazijn van de klant ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="287d1-110">In that case, the customer's warehouse is entered by default.</span></span>

<span data-ttu-id="287d1-111">Gebruikers moeten worden gekoppeld aan een callcenterkanaal om de functies van het callcenter te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="287d1-111">Users must be linked to a call center channel to use the features of call center.</span></span> <span data-ttu-id="287d1-112">Een verkooporder die door een gebruiker wordt gemaakt, wordt automatisch gekoppeld aan het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-112">Any sales order that a user creates is automatically linked to that user's call center channel.</span></span> <span data-ttu-id="287d1-113">Op dit moment kan er niet één gebruiker worden gekoppeld aan meerdere callcenterkanalen tegelijk.</span><span class="sxs-lookup"><span data-stu-id="287d1-113">Currently, a single user may not be linked to multiple call center channels at the same time.</span></span>

<span data-ttu-id="287d1-114">Ook kan een profiel voor e-mailmelding worden geconfigureerd op het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-114">An email notification profile can also be configured on the call center channel.</span></span> <span data-ttu-id="287d1-115">Het profiel definieert de set met e-mailsjablonen die wordt gebruikt wanneer e-mail wordt verzonden aan klanten die orders plaatsen via het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-115">The profile defines the set of email templates that is used when email is sent to customers who place orders through the call center channel.</span></span> <span data-ttu-id="287d1-116">Het activeren van de e-mail kan worden geconfigureerd voor systeemgebeurtenissen, zoals het indienen van de order of een zending.</span><span class="sxs-lookup"><span data-stu-id="287d1-116">The email triggers can be configured against system events, such as order submission or order shipment.</span></span>

<span data-ttu-id="287d1-117">Voor het correct verwerken van verkopen via een callcenterkanaal, moeten de juiste [betalingsmethoden](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) en leveringsmethoden worden gedefinieerd voor het kanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-117">Before sales can be correctly process through a call center channel, correct [payment methods](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) and delivery modes must be defined for the channel.</span></span>

<span data-ttu-id="287d1-118">U kunt op het niveau van het callcenterkanaal andere standaardwaarden definiëren die zijn gerelateerd aan de financiële dimensies die wordt gekoppeld aan orders die zijn gemaakt door dat kanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-118">At the level of the call center channel, you can define other default values that are related to the financial dimensions that will be linked to orders that are created by that channel.</span></span>

## <a name="options-for-order-processing-behavior"></a><span data-ttu-id="287d1-119">Opties voor gedrag bij orderverwerking</span><span class="sxs-lookup"><span data-stu-id="287d1-119">Options for order processing behavior</span></span>

<span data-ttu-id="287d1-120">Drie instellingen van de configuratie van een callcenter hebben veel invloed op de voorzieningen en functies die beschikbaar zijn voor verkooporders die zijn gemaakt voor dat callcenter: **Ordervoltooiing inschakelen**, **Rechtstreekse verkoop inschakelen** en **Orderprijscontrole inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="287d1-120">Three settings in the configuration of a call center have a major effect on the features and functions that are available for sales orders that are created against that call center: **Enable order completion**, **Enable direct selling**, and **Enable order price control**.</span></span>

### <a name="enable-order-completion"></a><span data-ttu-id="287d1-121">Ordervoltooiing inschakelen</span><span class="sxs-lookup"><span data-stu-id="287d1-121">Enable order completion</span></span>

<span data-ttu-id="287d1-122">De instelling **Ordervoltooiing inschakelen** voor het callcenterkanaal heeft een groot effect voor de orderverwerkingstroom van verkooporders die zijn ingevoerd voor dat kanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-122">The **Enable order completion** setting on the call center channel has a major effect on the order processing flow of sales orders that are entered for that channel.</span></span> <span data-ttu-id="287d1-123">Als deze instelling is ingeschakeld, moeten alle verkooporders een set validatieregels doorlopen voordat deze kunnen worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="287d1-123">When this setting is turned on, all sales orders must go through a set of validation rules before they can be confirmed.</span></span> <span data-ttu-id="287d1-124">U voert deze regels uit door het selecteren van de knop **Voltooien** die wordt toegevoegd aan het actievenster van de verkooporderpagina.</span><span class="sxs-lookup"><span data-stu-id="287d1-124">You run these rules by selecting the **Complete** button that is added on the Action Pane of the sales order page.</span></span> <span data-ttu-id="287d1-125">Alle verkooporders die worden gemaakt als de instelling **Ordervoltooiing inschakelen** is ingeschakeld, moeten het ordervoltooiingsproces doorlopen.</span><span class="sxs-lookup"><span data-stu-id="287d1-125">All sales orders that are created when the **Enable order completion** setting is turned on must go through the order completion process.</span></span> <span data-ttu-id="287d1-126">Dit proces zorgt voor de opname van betalingen en validatielogica voor betalingen.</span><span class="sxs-lookup"><span data-stu-id="287d1-126">This process enforces the capture of payment and payment validation logic.</span></span> <span data-ttu-id="287d1-127">Naast het uitvoeren van de betaling activeert het orderverzendproces [fraudecontroles](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts) die u in het systeem configureert.</span><span class="sxs-lookup"><span data-stu-id="287d1-127">In addition to payment enforcement, the order submission process can trigger [fraud checks](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts) that you configure in the system.</span></span> <span data-ttu-id="287d1-128">Orders waarvoor de betaling mislukt of frauduleuze validaties worden in de wachtstand geplaatst en kunnen niet worden vrijgegeven voor verdere verwerking (zoals orderverzamelen of verzending) totdat het probleem van de blokkering opgelost is.</span><span class="sxs-lookup"><span data-stu-id="287d1-128">Orders that fail payment or fraud validations are put on hold and can't be released to further processing (such as picking or shipping) until the issue that caused the hold is resolved.</span></span>

<span data-ttu-id="287d1-129">Wanneer de instelling **Ordervoltooiing inschakelen** is ingeschakeld voor het callcenterkanaal en er regelitems zijn ingevoerd op een verkooporder, en de gebruiker van het kanaal het verkooporderformulier wil sluiten of verlaten zonder dat **Voltooid** is geselecteerd, zorgt het ordervoltooiingsporces dat de pagina Samenvatting van verkooporder wordt geopend en moet de gebruiker de order correct indienen.</span><span class="sxs-lookup"><span data-stu-id="287d1-129">When the **Enable order completion** setting is turned on for the call center channel, if line items are entered on a sales order and the channel user tries to close or navigate away from the sales order form without first selecting **Complete**, the system enforces the order completion process by opening the sales order recap page and requiring that the user correctly submit the order.</span></span> <span data-ttu-id="287d1-130">Als de order niet correct kan worden ingediend met de betaling, kan de gebruiker de functie [Orderwachtstanden](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) toepassen om de order in de wachtstand te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="287d1-130">If the order can't be correctly submitted together with payment, the user can use the [order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) functionality to put the order on hold.</span></span> <span data-ttu-id="287d1-131">Als de gebruiker de order wil annuleren, moet hij of zij juist deze annuleren met behulp van de functie Annuleren of Verwijderen, afhankelijk van de functie die wordt toegestaan door de beveiliging.</span><span class="sxs-lookup"><span data-stu-id="287d1-131">If the user is trying to cancel the order, he or she must correctly cancel it by using either the Cancel function or the Delete function, depending on the function that the user's security allows.</span></span>

<span data-ttu-id="287d1-132">Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld voor het callcenterkanaal, wordt het veld **Betalingsstatus** bijgehouden op de order.</span><span class="sxs-lookup"><span data-stu-id="287d1-132">If the **Enable order completion** setting is turned on for the call center channel, the **Payment status** field will be tracked on the order.</span></span> <span data-ttu-id="287d1-133">Het systeem berekent de **betalingsstatus** wanneer de verkooporder wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="287d1-133">The system calculates the **Payment status** when the sales order is submitted.</span></span> <span data-ttu-id="287d1-134">Alleen orders met een goedgekeurde betalingsstatus mogen verdergaan naar extra orderverwerkingsstappen, zoals verzamelen en verzenden.</span><span class="sxs-lookup"><span data-stu-id="287d1-134">Only orders that have an approved payment status are allowed to move through the system for additional order processing steps, such as picking and shipping.</span></span> <span data-ttu-id="287d1-135">Als betalingen worden geweigerd, wordt de markering **Niet verwerken** ingeschakeld voor de gedetailleerde orderstatus, waarmee deze order wordt geblokkeerd totdat het betalingsprobleem is opgelost.</span><span class="sxs-lookup"><span data-stu-id="287d1-135">If payments are declined, the **do not process** flag will be enabled on the detailed order status, this puts the order on hold until the payment issue is resolved.</span></span>

<span data-ttu-id="287d1-136">Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld wanneer gebruikers verkooporders maken en in de invoermodus regelartikel zijn, is het veld **Bron** beschikbaar op de koptekst van de hoofdverkooporder.</span><span class="sxs-lookup"><span data-stu-id="287d1-136">Additionally, if the **Enable order completion** setting is turned on, when users create sales orders and are in line item entry mode, the **Source** field will be available on the main sales order header.</span></span> <span data-ttu-id="287d1-137">het veld **Bron** wordt gebruikt een [catalogusbroncode](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) vast te leggen in een verkoopscenario voor direct marketing.</span><span class="sxs-lookup"><span data-stu-id="287d1-137">The **Source** field is used to capture a [catalog source code](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) in a direct marketing selling scenario.</span></span> <span data-ttu-id="287d1-138">Deze code kan vervolgens speciale prijzen en promoties opgeven.</span><span class="sxs-lookup"><span data-stu-id="287d1-138">This code can then drive special prices and promotions.</span></span>

<span data-ttu-id="287d1-139">Zelfs als de instelling **Ordervoltooiingi inschakelen** is uitgeschakeld, kunnen gebruikers nog steeds een broncode toepassen op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="287d1-139">Even if the **Enable order completion** setting is turned off, users can still apply a source code to a sales order.</span></span> <span data-ttu-id="287d1-140">Maar ze moeten eerst de koptekstgegevens van de verkooporder openen voor toegang tot het veld **Bron**.</span><span class="sxs-lookup"><span data-stu-id="287d1-140">However, they must first open the sales order header details to access the **Source** field.</span></span> <span data-ttu-id="287d1-141">Er zijn dus een aantal aanvullende muisklikken nodig.</span><span class="sxs-lookup"><span data-stu-id="287d1-141">In other words, some additional clicks are required.</span></span> <span data-ttu-id="287d1-142">Dezelfde situatie is van toepassing op functies zoals zending voltooid en afgehandelde orders.</span><span class="sxs-lookup"><span data-stu-id="287d1-142">The same behavior applies to features such as ship complete and expedited orders.</span></span> <span data-ttu-id="287d1-143">Deze functies zijn beschikbaar voor alle orders die zijn gemaakt in het callcenter.</span><span class="sxs-lookup"><span data-stu-id="287d1-143">These features are available for all orders that are created in the call center.</span></span> <span data-ttu-id="287d1-144">Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld, kunnen gebruikers de configuratie van deze functies zien in de verkoopkoptekst in de weergave voor regelinvoer.</span><span class="sxs-lookup"><span data-stu-id="287d1-144">However, when the **Enable order completion** setting is turned on, users can see the configuration of these features on the sales header while they are in the line entry view.</span></span> <span data-ttu-id="287d1-145">Ze hoeven niet in te zoommen naar de koptekstgegevens van de verkooporder om de gewenste instellingen en velden te zien.</span><span class="sxs-lookup"><span data-stu-id="287d1-145">They don't have to drill into the sales order header details to find the appropriate settings and fields.</span></span>

### <a name="enable-direct-selling"></a><span data-ttu-id="287d1-146">Rechtstreekse verkoop inschakelen</span><span class="sxs-lookup"><span data-stu-id="287d1-146">Enable direct selling</span></span>

<span data-ttu-id="287d1-147">Als de instelling **Rechtstreekse verkoop inschakelen** is ingeschakeld voor het callcenterkanaal, kunnen gebruikers profiteren van de functies Meerverkoop/bijverkoop van Commerce.</span><span class="sxs-lookup"><span data-stu-id="287d1-147">If the **Enable direct selling** setting is turned for the call center channel, users can take advantage of the upsell and cross-sell features of Commerce.</span></span> <span data-ttu-id="287d1-148">In dit geval verschijnen pop-upvensters tijdens het invoeren van orders en worden andere producten voorgesteld die de callcentergebruiker aan de klant kan aanbieden.</span><span class="sxs-lookup"><span data-stu-id="287d1-148">In this case, pop-up windows appear during order entry and suggest other products that the call center user can offer to the customer.</span></span> <span data-ttu-id="287d1-149">De producten die worden voorgesteld, zijn gebaseerd op het product dat op de verkooporderregel is besteld.</span><span class="sxs-lookup"><span data-stu-id="287d1-149">The products that are suggested are based on the product that was just ordered on the sales order line.</span></span> <span data-ttu-id="287d1-150">Op dit moment worden de suggesties voor meerverkoop/bijverkoop geconfigureerd op artikelniveau voor producten of catalogi.</span><span class="sxs-lookup"><span data-stu-id="287d1-150">Currently, the upsell and cross-sell suggestions are configured at the item level on products or catalogs.</span></span> <span data-ttu-id="287d1-151">Als de instelling **Rechtstreekse verkoop inschakelen** is uitgeschakeld voor het callcenterkanaal, worden geen pop-upvensters weergegeven tijdens het invoeren van orders, zelfs niet als een geldige meerverkoop/bijverkoop is gedefinieerd voor een artikel dat wordt besteld.</span><span class="sxs-lookup"><span data-stu-id="287d1-151">If the **Enable direct selling** setting is turned off for the call center channel, pop-up windows don't appear during order entry, even if a valid upsell or cross-sell was defined for an item that is being ordered.</span></span>

<span data-ttu-id="287d1-152">Wanneer de **Rechtstreekse verkoop inschakelen** is ingeschakeld, worden ook de functies voor scripts en afbeeldingen op de invoerpagina voor de verkooporder ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="287d1-152">When the **Enable direct selling** setting is turned on, the scripts and images features of the sales order entry page are also turned on.</span></span> <span data-ttu-id="287d1-153">In dit geval is een informatiedeelvenster beschikbaar aan de rechterkant van de pagina tijdens het invoeren van orders.</span><span class="sxs-lookup"><span data-stu-id="287d1-153">In this case, an information panel is available on right side of the page during order entry.</span></span> <span data-ttu-id="287d1-154">Dit deelvenster kan scripts bevatten die zijn gerelateerd aan het generieke orderinvoerproces, de catalogusbroncode die is toegepast of scripts die zijn gerelateerd aan de bestelde artikelen.</span><span class="sxs-lookup"><span data-stu-id="287d1-154">This panel can show scripts that are related to the generic order entry process, the catalog source code that was applied, or scripts that are related to the items that are being ordered.</span></span> <span data-ttu-id="287d1-155">Het deelvenster met afbeeldingen kan bovendien een productafbeelding voor de bestelde artikelen weergeven als een afbeelding is gedefinieerd voor het artikel in de productinstellingen.</span><span class="sxs-lookup"><span data-stu-id="287d1-155">Additionally, the images panel can show a product image for the items that are being ordered, if an image has been defined for the item in the product setup.</span></span>

### <a name="enable-order-price-control"></a><span data-ttu-id="287d1-156">Orderprijscontrole inschakelen</span><span class="sxs-lookup"><span data-stu-id="287d1-156">Enable order price control</span></span>

<span data-ttu-id="287d1-157">Wanneer de instelling **Orderprijscontrole inschakelen** wordt ingeschakeld, kunnen alleen geautoriseerde gebruikers de verkoopprijs van een artikel wijzen tijdens het invoeren van orders.</span><span class="sxs-lookup"><span data-stu-id="287d1-157">When the **Enable order price control** setting is turned, only authorized users can change the sales price of an item during order entry.</span></span> <span data-ttu-id="287d1-158">De wijzigingen moet binnen de gedefinieerde marges liggen.</span><span class="sxs-lookup"><span data-stu-id="287d1-158">The changes must be within defined tolerances.</span></span> <span data-ttu-id="287d1-159">Gebruikers die niet de juiste machtiging hebben, moeten in plaats daarvan een aanvraag voor een prijswijziging indienen.</span><span class="sxs-lookup"><span data-stu-id="287d1-159">Users who don't have the proper authorization must submit a request for a price change instead.</span></span> <span data-ttu-id="287d1-160">De aanvraag wordt vervolgens verwerkt via systeemwerkstromen voor beoordeling en goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="287d1-160">The request will then be processed through system workflows for review and approval.</span></span>

## <a name="channel-users"></a><span data-ttu-id="287d1-161">Kanaalgebruikers</span><span class="sxs-lookup"><span data-stu-id="287d1-161">Channel users</span></span>

<span data-ttu-id="287d1-162">Wanneer u het callcenterkanaal definieert, moet u kanaalgebruikers koppelen aan hun callcenter.</span><span class="sxs-lookup"><span data-stu-id="287d1-162">When you define the call center channel, you must link channel users to the call center.</span></span> <span data-ttu-id="287d1-163">Anders kan het callcenter niet worden gebruikt in het systeem.</span><span class="sxs-lookup"><span data-stu-id="287d1-163">Otherwise, the call center can't be used in the system.</span></span> <span data-ttu-id="287d1-164">Wanneer gebruikers zich bij Commerce aanmelden en verkooporders of retourorders invoeren op een pagina die is gerelateerd aan het invoeren van orders, wordt hun gebruikers-id gevalideerd op basis van de configuratie van het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-164">When users sign in to Commerce and enter sales orders or return orders on a page that is related to order entry, their user ID is validated against the configuration of the call center channel.</span></span> <span data-ttu-id="287d1-165">Als een gebruiker is gekoppeld aan een specifiek callcenterkanaal, krijgen de orders die de gebruiker maakt, de eigenschappen en standaardwaarden van dat kanaal.</span><span class="sxs-lookup"><span data-stu-id="287d1-165">If a user is linked to a specific call center channel, orders that the user creates inherit the traits and default values of that channel.</span></span>

<span data-ttu-id="287d1-166">Standaard wordt de markering **Verkoop** in de verkooporderkoptekst is ingeschakeld voor alle orders die callcentergebruikers maken.</span><span class="sxs-lookup"><span data-stu-id="287d1-166">By default, the **Sale** flag on the sales order header is turned on for all orders that call center users create.</span></span> <span data-ttu-id="287d1-167">De orders kunnen vervolgens profiteren van de handelsspecifieke prijs- en promotiefuncties van het systeem.</span><span class="sxs-lookup"><span data-stu-id="287d1-167">The orders can then take advantage of the system's commerce-specific price and promotions features.</span></span>


<span data-ttu-id="287d1-168">Gebruikers die niet zijn gekoppeld aan een callcenterkanaal gebruiken de standaardfuncties voor orderinvoer van Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="287d1-168">Users who aren't linked to a call center channel use the standard order entry features of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="287d1-169">Orders die deze gebruikers invoeren via het formulier Verkooporderinvoer, worden niet systematisch aangemerkt als Commerce-orders.</span><span class="sxs-lookup"><span data-stu-id="287d1-169">Orders that these users enter through the sales order entry form will not be systematically identified as Commerce orders.</span></span> <span data-ttu-id="287d1-170">Ook worden orders die zijn ingevoerd door deze gebruikers, niet onderworpen aan voltooiingsregels voor orderverwerking, logica voor prijzen of andere ordervalidaties die kunnen worden gedefinieerd in de configuratie van het callcenterkanaal of systeemparameters voor het callcenter.</span><span class="sxs-lookup"><span data-stu-id="287d1-170">Additionally, these orders entered by these users will not be subject to any of the order completion processing rules, pricing logic, or other order validations that can be defined in the call center channel configuration or call center system parameters.</span></span>

<span data-ttu-id="287d1-171">Nadat u het callcenterkanaal hebt geconfigureerd en kanaalgebruikers hebt gedefinieerd, kunt u het gewenste systeemgedrag bevorderen door te zorgen dat alle vereiste callcenterparameters zijn gedefinieerd in **Detailhandel en commerce** \> **Kanaalinstelling** \> **Instellingen van callcenter** \> **Parameters van callcenter**.</span><span class="sxs-lookup"><span data-stu-id="287d1-171">After you've finished configuring the call center channel and defining channel users, to help ensure the desired system behavior, make sure that all required Call center parameters are defined at **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Call center parameters**.</span></span> <span data-ttu-id="287d1-172">Zorg ook dat gerelateerde nummerreeksen zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="287d1-172">Make sure that related number sequences are also defined.</span></span>

> [!NOTE]
> <span data-ttu-id="287d1-173">Als u de functionaliteit voor callcenters wilt gebruiken, moet de configuratiesleutel voor **Meerdere verzendadressen** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="287d1-173">To use call center functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="287d1-174">Deze configuratiesleutel kunt u vinden in de **handelsconfiguratiesleutels** onder **Systeembeheer**\> **Instellingen** \> **Licentieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="287d1-174">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="287d1-175">Dit is vereist vanwege de callcenterfunctionaliteit die verschillende validaties uitvoert op basis van het afleveradres dat is geconfigureerd op het niveau van de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="287d1-175">This is required due to call center functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span> 
