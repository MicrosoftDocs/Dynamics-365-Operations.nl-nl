---
title: Verkoopoffertes maken en bewerken
description: Deze procedure toont hoe u een verkoopofferte maakt en bijwerkt.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f66ec29cc0afd6e1ba5a65b241e3aac42a3c59b5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835623"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="c9662-103">Verkoopoffertes maken en bewerken</span><span class="sxs-lookup"><span data-stu-id="c9662-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9662-104">Deze procedure toont hoe u een verkoopofferte maakt en bijwerkt.</span><span class="sxs-lookup"><span data-stu-id="c9662-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="c9662-105">U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="c9662-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="c9662-106">Een verkoopofferte maken</span><span class="sxs-lookup"><span data-stu-id="c9662-106">Create a sales quotation</span></span>
1. <span data-ttu-id="c9662-107">Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.</span><span class="sxs-lookup"><span data-stu-id="c9662-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="c9662-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c9662-108">Click New.</span></span>
3. <span data-ttu-id="c9662-109">Selecteer 'Prospect' in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="c9662-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="c9662-110">Typ of selecteer een waarde in het veld Prospect.</span><span class="sxs-lookup"><span data-stu-id="c9662-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="c9662-111">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="c9662-111">Expand the General section.</span></span>
    * <span data-ttu-id="c9662-112">Omdat u ervoor koos om een offerte te maken vanuit het gebied Verkoop en marketing, wordt het type automatisch ingesteld op Verkoopofferte.</span><span class="sxs-lookup"><span data-stu-id="c9662-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="c9662-113">Om een offerte voor een project te maken, moet u deze openen vanuit de module Projectbeheer en boekhouding.</span><span class="sxs-lookup"><span data-stu-id="c9662-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="c9662-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c9662-114">Click OK.</span></span>
    * <span data-ttu-id="c9662-115">De velden en acties op de offerteregels zijn vergelijkbaar met deze op de verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="c9662-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="c9662-116">Net als verkooporders kunnen de offertes voor een specifiek artikel wordt gemaakt of, wanneer het artikelnummer niet bekend is of niet bestaat op het moment waarop de offerte wordt gemaakt, kunnen offertes voor een verkoopcategorie worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c9662-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="c9662-117">Typ of selecteer een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="c9662-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="c9662-118">Typ een waarde in het veld Artikel.</span><span class="sxs-lookup"><span data-stu-id="c9662-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="c9662-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c9662-119">Close the page.</span></span>
10. <span data-ttu-id="c9662-120">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="c9662-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c9662-121">Als er geldige handelsovereenkomsten zijn voor het geselecteerde artikel op de regel, worden de toepasselijke prijs en kortingen automatisch gekopieerd naar de offerteregel.</span><span class="sxs-lookup"><span data-stu-id="c9662-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="c9662-122">Zorg ervoor dat het veld Eenheidsprijs een waarde bevat en u ook kortingwaarden kunt invoeren als u dat wilt.</span><span class="sxs-lookup"><span data-stu-id="c9662-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="c9662-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c9662-123">Click Save.</span></span>
12. <span data-ttu-id="c9662-124">Klik in het actievenster op Verkoopofferte.</span><span class="sxs-lookup"><span data-stu-id="c9662-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="c9662-125">Klik op Totalen.</span><span class="sxs-lookup"><span data-stu-id="c9662-125">Click Totals.</span></span>
14. <span data-ttu-id="c9662-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c9662-126">Click OK.</span></span>
15. <span data-ttu-id="c9662-127">Klik op Verkoopofferteregel.</span><span class="sxs-lookup"><span data-stu-id="c9662-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="c9662-128">Klik op Prijzen.</span><span class="sxs-lookup"><span data-stu-id="c9662-128">Click Prices.</span></span>
    * <span data-ttu-id="c9662-129">Op de pagina Prijssimulatie uitvoeren kunt u experimenteren bij het aanpassen van de verwachte omzet of rentabiliteit van uw offerte op basis van de gewenste eenheidsprijzen, kortingsbedragen, kortingspercentages, totale bedragen, marges of bijdrageverhoudingen.</span><span class="sxs-lookup"><span data-stu-id="c9662-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="c9662-130">Wanneer u tevreden bent met de streefcijfers, past u de suggestie op de offerteregel toe. De prijsgerelateerde velden worden overeenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="c9662-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="c9662-131">U kunt zoveel prijssimulaties maken als u dit nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="c9662-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="c9662-132">Wanneer u op Nieuw klikt, worden de prijscoorwaarden van de huidige offerteregel gekopieerd naar de pagina.</span><span class="sxs-lookup"><span data-stu-id="c9662-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="c9662-133">U kunt dan in alle prijsgerelateerde velden waarden wijzigen in de doelwaarden.</span><span class="sxs-lookup"><span data-stu-id="c9662-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="c9662-134">Door een wijziging in een van de velden worden alle andere velden herberekend.</span><span class="sxs-lookup"><span data-stu-id="c9662-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="c9662-135">Opdat het systeem de verkoopmarge en bijdrageverhouding berekent, moeten de eenheidskosten van het product bekend zijn.</span><span class="sxs-lookup"><span data-stu-id="c9662-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="c9662-136">Gebruik het tabblad Gesimuleerde prijzen voor een gedetailleerde weergave van de oorspronkelijke prijzen, de voorgestelde wijzigingen en hun effect op de totalen van de offerte.</span><span class="sxs-lookup"><span data-stu-id="c9662-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="c9662-137">In het algemeen geldt dat als een simulatie die een nieuw bedrag instelt wordt toegepast op de offerteregel, het systeem een nieuwe waarde berekent en invoert in het veld Eenheidsprijs.</span><span class="sxs-lookup"><span data-stu-id="c9662-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="c9662-138">Als de simulatie is gebaseerd op een nieuwe marge of een nieuwe bijdrageverhouding, wordt alleen het veld Nettobedrag bijgewerkt en is de Eenheidsprijs leeg.</span><span class="sxs-lookup"><span data-stu-id="c9662-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="c9662-139">In beide gevallen worden eventuele kortingen verwijderd die vóór de simulatie op de offerteregel waren toegepast.</span><span class="sxs-lookup"><span data-stu-id="c9662-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="c9662-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c9662-140">Close the page.</span></span>
18. <span data-ttu-id="c9662-141">Klik in het actievenster op Offecte.</span><span class="sxs-lookup"><span data-stu-id="c9662-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="c9662-142">Klik op Offerte verzenden.</span><span class="sxs-lookup"><span data-stu-id="c9662-142">Click Send quotation.</span></span>
20. <span data-ttu-id="c9662-143">Selecteer Ja in het veld Offerte afdrukken.</span><span class="sxs-lookup"><span data-stu-id="c9662-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="c9662-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c9662-144">Click OK.</span></span>
    * <span data-ttu-id="c9662-145">Het kan enkele minuten duren om het rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="c9662-145">The report may take a minute to generate.</span></span> <span data-ttu-id="c9662-146">Sluit de pagina niet voor dit is gebeurd.</span><span class="sxs-lookup"><span data-stu-id="c9662-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="c9662-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c9662-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="c9662-148">Een verkoopofferte bijwerken</span><span class="sxs-lookup"><span data-stu-id="c9662-148">Update a sales quotation</span></span>
1. <span data-ttu-id="c9662-149">Klik in het actievenster op Opvolgen.</span><span class="sxs-lookup"><span data-stu-id="c9662-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="c9662-150">Klik op Omzetten in klant.</span><span class="sxs-lookup"><span data-stu-id="c9662-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="c9662-151">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="c9662-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="c9662-152">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="c9662-152">Click Check.</span></span>
    * <span data-ttu-id="c9662-153">Zorg ervoor u een bericht zeit dat het rekeningnummer dat u typte vrij is voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="c9662-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="c9662-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c9662-154">Click OK.</span></span>
    * <span data-ttu-id="c9662-155">Het systeem heeft nu een nieuwe klantrekening gemaakt voor de prospect op de offerte.</span><span class="sxs-lookup"><span data-stu-id="c9662-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="c9662-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c9662-156">Close the page.</span></span>
7. <span data-ttu-id="c9662-157">Klik in het actievenster op Opvolgen.</span><span class="sxs-lookup"><span data-stu-id="c9662-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="c9662-158">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="c9662-158">Click Confirm.</span></span>
9. <span data-ttu-id="c9662-159">Typ of selecteer een waarde in het veld Reden.</span><span class="sxs-lookup"><span data-stu-id="c9662-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="c9662-160">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c9662-160">Click OK.</span></span>
11. <span data-ttu-id="c9662-161">Klik in het actievenster op Algemeen.</span><span class="sxs-lookup"><span data-stu-id="c9662-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="c9662-162">Klik op Verkooporders.</span><span class="sxs-lookup"><span data-stu-id="c9662-162">Click Sales orders.</span></span>
13. <span data-ttu-id="c9662-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c9662-163">Close the page.</span></span>

