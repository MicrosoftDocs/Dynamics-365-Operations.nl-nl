---
title: Verkoopprovisies registreren
description: In dit onderwerp wordt beschreven hoe verkoopprovisies worden berekend en geregistreerd.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83cea952f4883d49621a9f7d16440927a8eddb98
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830550"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="9e29c-103">Verkoopprovisies registreren</span><span class="sxs-lookup"><span data-stu-id="9e29c-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e29c-104">In dit onderwerp wordt beschreven hoe verkoopprovisies worden berekend en geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="9e29c-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="9e29c-105">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="9e29c-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9e29c-106">Voordat u deze handleiding start, voert u de handleiding 'Regels voor verkoopprovisie instellen' uit om ervoor te zorgen dat u alle vereiste instellingen van de provisieberekening hebt.</span><span class="sxs-lookup"><span data-stu-id="9e29c-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="9e29c-107">Noteer de klant- en artikelnummers die u voor het provisieproces hebt geselecteerd en gebruik deze wanneer u wordt aangevraagd om een verkooporder in deze handleiding te maken.</span><span class="sxs-lookup"><span data-stu-id="9e29c-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="9e29c-108">Een verkooporder factureren die een verkoper in aanmerking brengt voor provisie</span><span class="sxs-lookup"><span data-stu-id="9e29c-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="9e29c-109">Ga in het navigatievenster naar **Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="9e29c-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-110">Select **New**.</span></span>
3. <span data-ttu-id="9e29c-111">Selecteer in het veld **Klantrekening** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="9e29c-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="9e29c-112">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-112">Select **OK**.</span></span>
5. <span data-ttu-id="9e29c-113">Selecteer **Opties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9e29c-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="9e29c-114">Selecteer **Weergave wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-114">Select **Change view**.</span></span>
7. <span data-ttu-id="9e29c-115">Selecteer **Weergave kopteksten**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-115">Select **Header view**.</span></span>
8. <span data-ttu-id="9e29c-116">Vouw de sectie **Instellingen** uit.</span><span class="sxs-lookup"><span data-stu-id="9e29c-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="9e29c-117">De waarde in het veld **Verkoopgroep** vertegenwoordigt een groep waaraan een of meer verkopers zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9e29c-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="9e29c-118">De personen in de groep zijn diegene die provisies zullen ontvangen wanneer de order wordt gefactureerd, volgens vooraf gedefinieerde tarieven en distributie.</span><span class="sxs-lookup"><span data-stu-id="9e29c-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="9e29c-119">De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9e29c-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="9e29c-120">De verkoopgroep wordt ook gekopieerd naar de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="9e29c-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="9e29c-121">U kunt deze wijzigen zodat deze verschilt van deze in de koptekst en/of tussen de regels.</span><span class="sxs-lookup"><span data-stu-id="9e29c-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="9e29c-122">De waarde in het veld **Provisiegroep** vertegenwoordigt een groep die u voor een of meer klanten hebt gemaakt om provisies bij te houden.</span><span class="sxs-lookup"><span data-stu-id="9e29c-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="9e29c-123">De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9e29c-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="9e29c-124">Selecteer **Opties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9e29c-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="9e29c-125">Selecteer **Weergave wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-125">Select **Change view**.</span></span>
11. <span data-ttu-id="9e29c-126">Selecteer **Regelweergave**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-126">Select **Line view**.</span></span>
12. <span data-ttu-id="9e29c-127">Selecteer in de vervolgkeuzelijst van het veld **Artikelnummer** het artikel dat u voor commissies hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9e29c-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="9e29c-128">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="9e29c-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="9e29c-129">Let op het nettobedrag van de regel.</span><span class="sxs-lookup"><span data-stu-id="9e29c-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="9e29c-130">Dit vertegenwoordigt de verkoopopbrengst, die in dit voorbeeld de basis voor provisieberekening is.</span><span class="sxs-lookup"><span data-stu-id="9e29c-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="9e29c-131">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-131">Select **Save**.</span></span>
15. <span data-ttu-id="9e29c-132">Selecteer **Factuur** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9e29c-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="9e29c-133">Selecteer **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="9e29c-134">Vouw de sectie **Parameters** uit.</span><span class="sxs-lookup"><span data-stu-id="9e29c-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="9e29c-135">Selecteer in het veld **Hoeveelheid** de optie **Alle**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="9e29c-136">Selecteer **Ja** in het veld **Boeking**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="9e29c-137">Selecteer **OK** en selecteer **OK** in het volgende venster.</span><span class="sxs-lookup"><span data-stu-id="9e29c-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="9e29c-138">Het kan even duren om de transactie te boeken.</span><span class="sxs-lookup"><span data-stu-id="9e29c-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="9e29c-139">Wacht tot de verwerking is voltooid en sluit de pagina niet.</span><span class="sxs-lookup"><span data-stu-id="9e29c-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="9e29c-140">De geregistreerde verkoopprovisies controleren</span><span class="sxs-lookup"><span data-stu-id="9e29c-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="9e29c-141">Selecteer **Factuur** in het actievenster en selecteer vervolgens opnieuw **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="9e29c-142">Selecteer **Factuur** in het actievenster en selecteer vervolgens **Provisietransacties**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="9e29c-143">Het tabblad **Overzicht** geeft regels weer die de provisiebedragen vertegenwoordigen die aan vertegenwoordigers moeten worden betaald die aan de gefactureerde verkooporder zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9e29c-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="9e29c-144">Laten we de gegevens bekijken.</span><span class="sxs-lookup"><span data-stu-id="9e29c-144">Let's review the details.</span></span>  
    - <span data-ttu-id="9e29c-145">Als u de handleiding 'Regels voor verkoopprovisie instellen' gebruikte om de groep **Provisieverkoop** in te stellen, zullen twee verkopers een verkoopprovisie ontvangen en is de provisie onder hen gelijk verdeeld.</span><span class="sxs-lookup"><span data-stu-id="9e29c-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="9e29c-146">In dit voorbeeld wordt het totaalbedrag van de provisie berekend als een percentage van de verkoopopbrengst (het nettobedrag van de orderregel).</span><span class="sxs-lookup"><span data-stu-id="9e29c-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="9e29c-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9e29c-147">Close the page.</span></span>
4. <span data-ttu-id="9e29c-148">Selecteer **Boekstuk**.</span><span class="sxs-lookup"><span data-stu-id="9e29c-148">Select **Voucher**.</span></span> <span data-ttu-id="9e29c-149">U kunt de boekstuktransacties voor de provisiebedragen controleren die op de vooraf gedefinieerde rekeningen voor provisie-uitgave en te betalen provisie zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="9e29c-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

