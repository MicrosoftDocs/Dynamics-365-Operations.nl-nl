---
title: Een retour- en restitutiebeleid voor een kanaal maken en bijwerken
description: In dit onderwerp wordt uitgelegd hoe u een retour- en restitutiebeleid instelt voor een kanaal.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 89e8fe78414e73053317ebe19e3afcc89231d440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979698"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="8eaf2-103">Een retour- en restitutiebeleid voor een kanaal maken en bijwerken</span><span class="sxs-lookup"><span data-stu-id="8eaf2-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="8eaf2-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="8eaf2-104">Overview</span></span>

<span data-ttu-id="8eaf2-105">Via het kanaalretourbeleid in Dynamics 365 Commerce kunnen detailhandelaren voorwaarden instellen voor het toestaan van betalingsmethoden voor het verwerken van een retour op een POS-apparaat (Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="8eaf2-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="8eaf2-106">In dit onderwerp worden de stappen beschreven voor het instellen van een retour- en restitutiebeleid voor een kanaal.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="8eaf2-107">De reikwijdte van het beleid is momenteel beperkt tot het instellen van de betalingsmethoden die kunnen worden toegestaan voor een kanaal.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="8eaf2-108">De lijst 'toegestaan' is gebaseerd op de betalingsmethoden die zijn gebruikt voor het doen van de aankoop.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="8eaf2-109">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="8eaf2-109">For example:</span></span>

- <span data-ttu-id="8eaf2-110">Als er een aankoop heeft plaatsgevonden met een geschenkbon, is het winkelbeleid dat alleen restitutie kan plaatsvinden via een nieuwe geschenkbon of dat winkelkrediet wordt verleend.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="8eaf2-111">Als een verkoop wordt gedaan met contant geld, zijn de opties voor terugbetaling contant, geschenkbon en klantrekening, maar niet creditcard.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="8eaf2-112">Retourbeleid inschakelen</span><span class="sxs-lookup"><span data-stu-id="8eaf2-112">Enable return policy</span></span>

<span data-ttu-id="8eaf2-113">Ga als volgt te werk om de functionaliteit voor kanaalretourbeleid in te schakelen:</span><span class="sxs-lookup"><span data-stu-id="8eaf2-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="8eaf2-114">Ga naar het werkgebied **Functiebeheer** in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="8eaf2-115">Zoek naar de functie **Kanaalretourbeleid inschakelen** in de lijst met functienamen.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="8eaf2-116">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="8eaf2-117">Retourbeleid configureren</span><span class="sxs-lookup"><span data-stu-id="8eaf2-117">Configure return policy</span></span>

<span data-ttu-id="8eaf2-118">Voer de volgende stappen uit om een retourbeleid te configureren voor een detailhandelwinkel of online detailhandelkanaal.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="8eaf2-119">Ga naar **Retail en Commerce** \> **Kanaalinstelling** \> **Retouren** \> **Kanaalretourbeleid**.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="8eaf2-120">Selecteer **Nieuw** om een nieuwe sjabloon voor retourbeleid te maken.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="8eaf2-121">Als u een bestaande sjabloon wilt gebruiken, selecteert u de sjabloon in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="8eaf2-122">Voor nieuwe sjablonen voegt u een naam en een beschrijving toe aan de hand waarvan u het beleid kunt identificeren wanneer dit op het kanaal wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="8eaf2-123">![Nieuw retourbeleid toevoegen](media/Return-policy-page1.png "Nieuw retourbeleid toevoegen")</span><span class="sxs-lookup"><span data-stu-id="8eaf2-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="8eaf2-124">Definieer in de sectie **Toegestane betalingsmethoden voor restitutie** de optie **Toegestaan** voor betalingsmethoden voor retourbetalingen die specifiek zijn voor elke betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="8eaf2-125">![Betalingsmethoden toevoegen](media/Return-policy-page2.PNG "Toegestane betalingsmethoden per betalingstype instellen")</span><span class="sxs-lookup"><span data-stu-id="8eaf2-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="8eaf2-126">De betalingsmethoden worden afgeleid van de betalingsmethoden die zijn ingesteld voor de organisatie.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="8eaf2-127">Door een toegestane betalingsmethode voor restitutie toe te voegen voor elke vermelde betalingsmethode, zorgt u ervoor dat er restitutie kan plaatsvinden naar de toegestane type retourbetalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="8eaf2-128">Koppel de sjabloon voor retourbeleid aan de winkels waar deze wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="8eaf2-129">Selecteer **Toevoegen** op het tabblad **Detailhandelkanalen** en koppel de beschikbare kanalen.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="8eaf2-130">Selecteer in het dialoogvenster **Organisatieknooppunten kiezen** de winkels, regio's en organisaties waaraan de sjabloon moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="8eaf2-131">Er kan slechts één sjabloon voor retourbeleid aan elke winkel worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="8eaf2-132">Gebruik de pijlknoppen om winkels, regio's of organisaties te selecteren.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="8eaf2-133">De ingangsdatum van het beleid is de datum waarop het beleid op de kanalen wordt toegepast en de kanaaltaken worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="8eaf2-134">![Dialoogvenster Organisatieknooppunten kiezen](media/Return-policy-page3.PNG "Dialoogvenster Organisatieknooppunten kiezen")</span><span class="sxs-lookup"><span data-stu-id="8eaf2-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="8eaf2-135">Voer op de pagina **Distributieschema** de taak **1070** uit om het kanaalretourbeleid beschikbaar te maken voor het POS.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="8eaf2-136">Een voorbeeld van het kanaalretourbeleid bekijken in het POS</span><span class="sxs-lookup"><span data-stu-id="8eaf2-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="8eaf2-137">Volg de stappen in een van de volgende voorbeelden om de toegestane typen retourbetalingsmethoden in POS weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="8eaf2-138">Meld u als kassier of manager aan bij het POS.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="8eaf2-139">Selecteer onder **Ploeg en lade** de optie **Journaal weergeven**.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="8eaf2-140">Selecteer de transactie die deel uitmaakt van de retour.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="8eaf2-141">Selecteer de artikelen die u wilt terugbetalen en kies de betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="8eaf2-142">Als de geselecteerde betalingsmethode in de lijst met toegestane typen betalingsmethoden voorkomt, kan de kassier de transactie voltooien.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="8eaf2-143">Als de geselecteerde betalingsmethode niet is toegestaan, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="8eaf2-144">Selecteer **Verschuldigd bedrag** om een lijst weer te geven met alle toegestane typen betalingsmethoden voor retouren.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="8eaf2-145">– of –</span><span class="sxs-lookup"><span data-stu-id="8eaf2-145">-or-</span></span>

1. <span data-ttu-id="8eaf2-146">Meld u als kassier of manager aan bij het POS.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="8eaf2-147">Selecteer **Retourtransactie** en voer de ontvangst-id in met behulp van een streepjescodescan of handmatige invoer.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="8eaf2-148">Selecteer de transactie die deel uitmaakt van de retour.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="8eaf2-149">Selecteer de artikelen die u wilt terugbetalen en kies de betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="8eaf2-150">Als de geselecteerde betalingsmethode in de lijst met toegestane typen betalingsmethoden voorkomt, kan de kassier de transactie voltooien.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="8eaf2-151">Als de geselecteerde betalingsmethode niet is toegestaan, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="8eaf2-152">Selecteer **Verschuldigd bedrag** om een lijst weer te geven met alle toegestane typen betalingsmethoden voor retouren.</span><span class="sxs-lookup"><span data-stu-id="8eaf2-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="8eaf2-153">![Restitutie niet toegestaan](media/Return-policy-page6.png "Type restitutie niet toegestaan")</span><span class="sxs-lookup"><span data-stu-id="8eaf2-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="8eaf2-154">![Lijst met betalingsmethoden](media/Return-policy-page5.PNG "Typen restitutie toegestaan")</span><span class="sxs-lookup"><span data-stu-id="8eaf2-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
