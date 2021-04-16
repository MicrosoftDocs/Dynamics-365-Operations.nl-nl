---
title: EUR-00011 Genereren van het rapport ICL-lijst.
description: Deze procedure begeleidt u bij het genereren van het rapport van de EU-verkooplijst.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce3fa3eaae48499e58228d9d6dbf7ce7e97d2bd8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821828"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="3ede3-103">EUR-00011 Genereren van het rapport ICL-lijst.</span><span class="sxs-lookup"><span data-stu-id="3ede3-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ede3-104">Deze procedure begeleidt u bij het genereren van het rapport van de EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="3ede3-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="3ede3-105">Dit omvat het overboeken van intracommunautaire handelstransacties naar de EU-verkooplijst en het uitvoeren van het rapport.</span><span class="sxs-lookup"><span data-stu-id="3ede3-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="3ede3-106">Deze procedure omvat ook het maken van een intracommunautair handelstransactie voor demodoeleinden.</span><span class="sxs-lookup"><span data-stu-id="3ede3-106">This procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="3ede3-107">Raadpleeg voor meer informatie over EU-verkooplijstrapportage, met inbegrip van vereisten, de Help.</span><span class="sxs-lookup"><span data-stu-id="3ede3-107">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="3ede3-108">Deze procedure is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="3ede3-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="3ede3-109">De procedure werd gemaakt met de demogegevens van het bedrijf DEMF en dus Duitsland als voorbeeld voor land/regio.</span><span class="sxs-lookup"><span data-stu-id="3ede3-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="3ede3-110">De procedure maakt ook gebruik van Portugal als voorbeeld van EU-land/-regio.</span><span class="sxs-lookup"><span data-stu-id="3ede3-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="3ede3-111">Voordat u deze procedure kunt uitvoeren, moet u het rapporteren van de EU-verkooplijst configureren.</span><span class="sxs-lookup"><span data-stu-id="3ede3-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="3ede3-112">Deze procedure is alleen bedoeld voor accountants.</span><span class="sxs-lookup"><span data-stu-id="3ede3-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="3ede3-113">Een intracommunautaire verkooptransactie voor demodoeleinden maken</span><span class="sxs-lookup"><span data-stu-id="3ede3-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="3ede3-114">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="3ede3-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="3ede3-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3ede3-115">Click New.</span></span>
3. <span data-ttu-id="3ede3-116">Typ 'PRT-001' in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="3ede3-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="3ede3-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-117">Click OK.</span></span>
5. <span data-ttu-id="3ede3-118">Typ in het veld Artikelnummer de waarde 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="3ede3-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="3ede3-119">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="3ede3-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="3ede3-120">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="3ede3-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="3ede3-121">Typ 'VOL' in het veld Btw-groep voor artikel.</span><span class="sxs-lookup"><span data-stu-id="3ede3-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="3ede3-122">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3ede3-122">Click Add line.</span></span>
10. <span data-ttu-id="3ede3-123">Typ in het veld Artikelnummer de waarde 'D0003'.</span><span class="sxs-lookup"><span data-stu-id="3ede3-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="3ede3-124">Typ 'ROOD' in het veld Btw-groep voor artikel.</span><span class="sxs-lookup"><span data-stu-id="3ede3-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="3ede3-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3ede3-125">Click Save.</span></span>
13. <span data-ttu-id="3ede3-126">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="3ede3-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="3ede3-127">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="3ede3-127">Click Invoice.</span></span>
15. <span data-ttu-id="3ede3-128">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="3ede3-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="3ede3-129">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="3ede3-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="3ede3-130">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="3ede3-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="3ede3-131">Stel de datum in het veld Factuurdatum in op '01/11/2016'.</span><span class="sxs-lookup"><span data-stu-id="3ede3-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="3ede3-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-132">Click OK.</span></span>
20. <span data-ttu-id="3ede3-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="3ede3-134">Intracommunautaire handelstransacties naar de EU-verkooplijst overboeken</span><span class="sxs-lookup"><span data-stu-id="3ede3-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="3ede3-135">Ga naar Belasting > Aangiften > Buitenlandse handel > ICL-lijst.</span><span class="sxs-lookup"><span data-stu-id="3ede3-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="3ede3-136">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="3ede3-136">Click Transfer.</span></span>
3. <span data-ttu-id="3ede3-137">Selecteer Ja in het veld Artikel om artikeltransacties over te boeken.</span><span class="sxs-lookup"><span data-stu-id="3ede3-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="3ede3-138">Selecteer Ja in het veld Service om servicetransacties over te boeken.</span><span class="sxs-lookup"><span data-stu-id="3ede3-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="3ede3-139">U kunt ook extra filters op intracommunautair handelstransacties opgeven voor overboeking.</span><span class="sxs-lookup"><span data-stu-id="3ede3-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="3ede3-140">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="3ede3-140">Click Transfer.</span></span>
    * <span data-ttu-id="3ede3-141">Controleer of de intracommunautaire verkooptransactie goed is overgeboekt naar de EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="3ede3-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="3ede3-142">Het rapport van de EU-verkooplijst genereren</span><span class="sxs-lookup"><span data-stu-id="3ede3-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="3ede3-143">Klik op Rapportage.</span><span class="sxs-lookup"><span data-stu-id="3ede3-143">Click Reporting.</span></span>
2. <span data-ttu-id="3ede3-144">Selecteer 'Maandelijks' in het veld Aangifteperiode.</span><span class="sxs-lookup"><span data-stu-id="3ede3-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="3ede3-145">Stel in het veld Begindatum de datum in op '01/01/2016'.</span><span class="sxs-lookup"><span data-stu-id="3ede3-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="3ede3-146">Selecteer Ja in het veld Bestand maken.</span><span class="sxs-lookup"><span data-stu-id="3ede3-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="3ede3-147">Selecteer Ja in het veld Rapport maken.</span><span class="sxs-lookup"><span data-stu-id="3ede3-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="3ede3-148">Typ 'EUSalesList' in het veld Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="3ede3-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="3ede3-149">Typ 'EUSalesList' in het veld Bestandsnaam van rapport.</span><span class="sxs-lookup"><span data-stu-id="3ede3-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="3ede3-150">Typ '123' in het veld Registratie-id van EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="3ede3-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="3ede3-151">Dit veld is alleen beschikbaar voor Duitsland.</span><span class="sxs-lookup"><span data-stu-id="3ede3-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="3ede3-152">U kunt ook extra filters op intracommunautair handelstransacties opgeven om in het rapport op te nemen.</span><span class="sxs-lookup"><span data-stu-id="3ede3-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="3ede3-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-153">Click OK.</span></span>
    * <span data-ttu-id="3ede3-154">Controleer of de pop-upvensters worden weergegeven om te bevestigen dat het bestand en het controlerapport worden gedownload.</span><span class="sxs-lookup"><span data-stu-id="3ede3-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="3ede3-155">Regels van EU-verkooplijst markeren als Gerapporteerd</span><span class="sxs-lookup"><span data-stu-id="3ede3-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="3ede3-156">Klik op Markeren.</span><span class="sxs-lookup"><span data-stu-id="3ede3-156">Click Mark.</span></span>
2. <span data-ttu-id="3ede3-157">Klik op Markeren als gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="3ede3-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="3ede3-158">Selecteer in de lijst de rij voor het veld Factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="3ede3-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="3ede3-159">Typ '01/01/2016..01/31/2016' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="3ede3-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="3ede3-160">Selecteer in de lijst de rij voor het veld Rapportagestatus.</span><span class="sxs-lookup"><span data-stu-id="3ede3-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="3ede3-161">Selecteer 'Opgenomen' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="3ede3-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="3ede3-162">U kunt ook extra filters op intracommunautair handelstransacties opgeven om te markeren als Gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="3ede3-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="3ede3-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-163">Click OK.</span></span>
8. <span data-ttu-id="3ede3-164">Selecteer 'Gerapporteerd' in het veld Selectie.</span><span class="sxs-lookup"><span data-stu-id="3ede3-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="3ede3-165">Regels van EU-verkooplijst markeren als Afgesloten</span><span class="sxs-lookup"><span data-stu-id="3ede3-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="3ede3-166">Klik op Markeren.</span><span class="sxs-lookup"><span data-stu-id="3ede3-166">Click Mark.</span></span>
2. <span data-ttu-id="3ede3-167">Klik op Markeren als afgesloten.</span><span class="sxs-lookup"><span data-stu-id="3ede3-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="3ede3-168">Markeer in de lijst de rij voor het veld Factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="3ede3-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="3ede3-169">Typ '01/01/2016..01/31/2016' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="3ede3-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="3ede3-170">Markeer in de lijst de rij voor het veld Rapportagestatus.</span><span class="sxs-lookup"><span data-stu-id="3ede3-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="3ede3-171">Selecteer 'Gerapporteerd' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="3ede3-171">In the Criteria field, select 'Reported'.</span></span>
    * <span data-ttu-id="3ede3-172">U kunt ook extra filters op intracommunautair handelstransacties opgeven om te markeren als Afgesloten.</span><span class="sxs-lookup"><span data-stu-id="3ede3-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="3ede3-173">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-173">Click OK.</span></span>
8. <span data-ttu-id="3ede3-174">Selecteer 'Afgesloten' in het veld Selectie.</span><span class="sxs-lookup"><span data-stu-id="3ede3-174">In the Selection field, select 'Closed'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]