---
title: Een callcenterkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057874"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="c7160-103">Een callcenterkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="c7160-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c7160-104">In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7160-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c7160-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="c7160-105">Overview</span></span>

<span data-ttu-id="c7160-106">In Dynamics 365 Commerce is een callcenter een type afzetkanaal dat kan worden gedefinieerd in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="c7160-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="c7160-107">Door een afzetkanaal voor uw callcenter-entiteiten te definiëren, kan het systeem specifieke gegevens en orderverwerkingsinstellingen koppelen aan verkooporders.</span><span class="sxs-lookup"><span data-stu-id="c7160-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="c7160-108">Een bedrijf kan meerdere callcenterkanalen definiëren in Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7160-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="c7160-109">Controleer vóór het maken van een nieuw callcenterkanaal of u de [Vereisten voor het instellen van kanalen](channels-prerequisites.md) hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="c7160-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="c7160-110">Een nieuw callcenterafzetkanaal maken en configureren</span><span class="sxs-lookup"><span data-stu-id="c7160-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="c7160-111">Voer de volgende stappen uit om een nieuw callcenterafzetkanaal te maken en te configureren.</span><span class="sxs-lookup"><span data-stu-id="c7160-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="c7160-112">Ga in het navigatievenster naar **Modules \> Kanalen \> Callcenters \> Alle callcenters**.</span><span class="sxs-lookup"><span data-stu-id="c7160-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="c7160-113">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c7160-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c7160-114">Typ in het veld **Naam** een naam voor het nieuwe kanaal.</span><span class="sxs-lookup"><span data-stu-id="c7160-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="c7160-115">Selecteer de juiste **Rechtspersoon** in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="c7160-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="c7160-116">Selecteer de juiste **Magazijn**locatie in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="c7160-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="c7160-117">Geef in het veld **Standaardklant** een geldige standaardklant op.</span><span class="sxs-lookup"><span data-stu-id="c7160-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="c7160-118">Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.</span><span class="sxs-lookup"><span data-stu-id="c7160-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="c7160-119">Geef een infocode op voor **Prijsoverschrijving**.</span><span class="sxs-lookup"><span data-stu-id="c7160-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="c7160-120">Het is mogelijk dat u hiervoor eerst een informatiecode moet maken.</span><span class="sxs-lookup"><span data-stu-id="c7160-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="c7160-121">Geef een infocode op voor **Wachtstandcode**.</span><span class="sxs-lookup"><span data-stu-id="c7160-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="c7160-122">Het is mogelijk dat u hiervoor eerst een informatiecode moet maken.</span><span class="sxs-lookup"><span data-stu-id="c7160-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="c7160-123">Een infocode op voor **Krediet**.</span><span class="sxs-lookup"><span data-stu-id="c7160-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="c7160-124">Het is mogelijk dat u hiervoor eerst een informatiecode moet maken.</span><span class="sxs-lookup"><span data-stu-id="c7160-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="c7160-125">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c7160-125">Select **Save**.</span></span>

<span data-ttu-id="c7160-126">De volgende afbeelding toont het maken van een nieuw callcenterafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="c7160-126">The following image shows the creation of a new call center channel.</span></span>

![Nieuw callcenterafzetkanaal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="c7160-128">In de volgende afbeelding ziet u een voorbeeld van een callcenterafzetkanaal.</span><span class="sxs-lookup"><span data-stu-id="c7160-128">The following image shows an example call center channel.</span></span>

![Voorbeeld van callcenterafzetkanaal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="c7160-130">Aanvullende afzetkanaalinstellingen</span><span class="sxs-lookup"><span data-stu-id="c7160-130">Additional channel setup</span></span>

<span data-ttu-id="c7160-131">Aanvullende taken die nodig zijn voor het instellen van callcenterkanalen, zijn onder andere het instellen van betalingsmethoden en leveringsmethoden.</span><span class="sxs-lookup"><span data-stu-id="c7160-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="c7160-132">De volgende afbeelding toont de instellingsopties voor **Leveringsmethoden** en **Betalingsmethoden** op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c7160-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Aanvullende acties voor het instellen van een callcenterkanaal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="c7160-134">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="c7160-134">Set up payment methods</span></span>

<span data-ttu-id="c7160-135">Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="c7160-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="c7160-136">Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="c7160-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="c7160-137">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c7160-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c7160-138">Selecteer in het navigatievenster een gewenste betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="c7160-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="c7160-139">Geef in de sectie **Algemeen** een naam op in **Bewerkingsnaam** en configureer eventuele andere instellingen.</span><span class="sxs-lookup"><span data-stu-id="c7160-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="c7160-140">Configureer eventuele aanvullende instellingen voor het betalingstype.</span><span class="sxs-lookup"><span data-stu-id="c7160-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="c7160-141">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c7160-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c7160-142">In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.</span><span class="sxs-lookup"><span data-stu-id="c7160-142">The following image shows an example of a cash payment method.</span></span>

![Voorbeeldbetalingsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="c7160-144">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="c7160-144">Set up modes of delivery</span></span>

<span data-ttu-id="c7160-145">U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="c7160-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="c7160-146">Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c7160-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="c7160-147">Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="c7160-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="c7160-148">Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.</span><span class="sxs-lookup"><span data-stu-id="c7160-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="c7160-149">Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7160-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="c7160-150">Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="c7160-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="c7160-151">In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="c7160-151">The following image shows an example of a mode of delivery.</span></span>

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="c7160-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c7160-153">Additional resources</span></span>

[<span data-ttu-id="c7160-154">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="c7160-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c7160-155">Verkoopfunctionaliteit callcenter</span><span class="sxs-lookup"><span data-stu-id="c7160-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="c7160-156">Orderverwerkingsopties voor callcenter instellen</span><span class="sxs-lookup"><span data-stu-id="c7160-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="c7160-157">Callcentercatalogi</span><span class="sxs-lookup"><span data-stu-id="c7160-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="c7160-158">Instellen en werken met fraudewaarschuwingen</span><span class="sxs-lookup"><span data-stu-id="c7160-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="c7160-159">Continuïteitsprogramma's instellen voor callcenters</span><span class="sxs-lookup"><span data-stu-id="c7160-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
