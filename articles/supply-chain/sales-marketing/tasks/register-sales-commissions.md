---
title: Verkoopprovisies registreren
description: Deze procedure toont hoe verkoopprovisies worden berekend en geregistreerd.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "355145"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="31b0b-103">Verkoopprovisies registreren</span><span class="sxs-lookup"><span data-stu-id="31b0b-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31b0b-104">Deze procedure toont hoe verkoopprovisies worden berekend en geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="31b0b-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="31b0b-105">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="31b0b-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="31b0b-106">Voordat u deze handleiding start, voert u de handleiding 'Regels voor verkoopprovisie instellen' uit om ervoor te zorgen dat u alle vereiste instellingen van de provisieberekening hebt.</span><span class="sxs-lookup"><span data-stu-id="31b0b-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="31b0b-107">Noteer de klant- en artikelnummers die u voor het provisieproces hebt geselecteerd en gebruik deze wanneer u wordt aangevraagd om een verkooporder in deze handleiding te maken.</span><span class="sxs-lookup"><span data-stu-id="31b0b-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="31b0b-108">Een verkooporder factureren die een verkoper in aanmerking brengt voor provisie</span><span class="sxs-lookup"><span data-stu-id="31b0b-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="31b0b-109">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="31b0b-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="31b0b-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="31b0b-110">Click New.</span></span>
3. <span data-ttu-id="31b0b-111">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="31b0b-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="31b0b-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="31b0b-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="31b0b-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="31b0b-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31b0b-114">Click OK.</span></span>
7. <span data-ttu-id="31b0b-115">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="31b0b-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="31b0b-116">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-116">Click Change view.</span></span>
9. <span data-ttu-id="31b0b-117">Klik op Weergave kopteksten.</span><span class="sxs-lookup"><span data-stu-id="31b0b-117">Click Header view.</span></span>
10. <span data-ttu-id="31b0b-118">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="31b0b-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="31b0b-119">De waarde in het veld Verkoopgroep vertegenwoordigt een groep waaraan een of meer verkopers zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="31b0b-120">De personen in de groep zijn diegene die provisies zullen ontvangen wanneer de order wordt gefactureerd, volgens vooraf gedefinieerde tarieven en distributie.</span><span class="sxs-lookup"><span data-stu-id="31b0b-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="31b0b-121">De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="31b0b-122">De verkoopgroep wordt ook gekopieerd naar de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="31b0b-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="31b0b-123">U kunt deze wijzigen zodat deze verschilt van deze in de koptekst en/of tussen de regels.</span><span class="sxs-lookup"><span data-stu-id="31b0b-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="31b0b-124">De waarde in het veld Provisiegroep vertegenwoordigt een groep die u voor een of meer klanten hebt gemaakt om provisies bij te houden.</span><span class="sxs-lookup"><span data-stu-id="31b0b-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="31b0b-125">De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="31b0b-126">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="31b0b-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="31b0b-127">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-127">Click Change view.</span></span>
13. <span data-ttu-id="31b0b-128">Klik op Regelweergave.</span><span class="sxs-lookup"><span data-stu-id="31b0b-128">Click Line view.</span></span>
14. <span data-ttu-id="31b0b-129">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="31b0b-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="31b0b-130">Selecteer in de lijst het artikel waarvoor u provisies hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="31b0b-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="31b0b-131">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="31b0b-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="31b0b-132">Let op het nettobedrag van de regel.</span><span class="sxs-lookup"><span data-stu-id="31b0b-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="31b0b-133">Dit vertegenwoordigt de verkoopopbrengst, die in dit voorbeeld de basis voor provisieberekening is.</span><span class="sxs-lookup"><span data-stu-id="31b0b-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="31b0b-134">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="31b0b-134">Click Save.</span></span>
18. <span data-ttu-id="31b0b-135">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31b0b-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="31b0b-136">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31b0b-136">Click Invoice.</span></span>
20. <span data-ttu-id="31b0b-137">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="31b0b-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="31b0b-138">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="31b0b-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="31b0b-139">Selecteer Ja in het veld Boeking.</span><span class="sxs-lookup"><span data-stu-id="31b0b-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="31b0b-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31b0b-140">Click OK.</span></span>
24. <span data-ttu-id="31b0b-141">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="31b0b-141">Click OK.</span></span>
    * <span data-ttu-id="31b0b-142">Het kan even duren om de transactie te boeken.</span><span class="sxs-lookup"><span data-stu-id="31b0b-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="31b0b-143">Wacht tot de verwerking is voltooid en sluit de pagina niet.</span><span class="sxs-lookup"><span data-stu-id="31b0b-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="31b0b-144">De geregistreerde verkoopprovisies controleren</span><span class="sxs-lookup"><span data-stu-id="31b0b-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="31b0b-145">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31b0b-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="31b0b-146">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31b0b-146">Click Invoice.</span></span>
3. <span data-ttu-id="31b0b-147">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="31b0b-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="31b0b-148">Klik op Provisietransacties.</span><span class="sxs-lookup"><span data-stu-id="31b0b-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="31b0b-149">Het tabblad Overzicht geeft regels weer die de provisiebedragen vertegenwoordigen die aan vertegenwoordigers moeten worden betaald die aan de gefactureerde verkooporder zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="31b0b-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="31b0b-150">Laten we de gegevens bekijken.</span><span class="sxs-lookup"><span data-stu-id="31b0b-150">Let's review the details.</span></span>     
    * <span data-ttu-id="31b0b-151">Als u de handleiding 'Regels voor verkoopprovisie instellen' gebruikte om de provisieverkoopgroep in te stellen, zullen twee verkopers een verkoopprovisie ontvangen en is de provisie onder hen gelijk verdeeld.</span><span class="sxs-lookup"><span data-stu-id="31b0b-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="31b0b-152">In dit voorbeeld wordt het totaalbedrag van de provisie berekend als een percentage van de verkoopopbrengst (het nettobedrag van de orderregel).</span><span class="sxs-lookup"><span data-stu-id="31b0b-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="31b0b-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="31b0b-153">Close the page.</span></span>
6. <span data-ttu-id="31b0b-154">Klik op Boekstuk.</span><span class="sxs-lookup"><span data-stu-id="31b0b-154">Click Voucher.</span></span>
    * <span data-ttu-id="31b0b-155">U kunt de boekstuktransacties voor de provisiebedragen controleren die op de vooraf gedefinieerde rekeningen voor provisie-uitgave en te betalen provisie zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="31b0b-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

