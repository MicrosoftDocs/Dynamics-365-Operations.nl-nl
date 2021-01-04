---
title: EUR-00011 Genereren van het rapport ICL-lijst.
description: Deze procedure begeleidt u bij het genereren van het rapport van de EU-verkooplijst.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 37f1a6e3bf39e16702d1367a325134ec84369945
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408314"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="a255e-103">EUR-00011 Genereren van het rapport ICL-lijst.</span><span class="sxs-lookup"><span data-stu-id="a255e-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a255e-104">Deze procedure begeleidt u bij het genereren van het rapport van de EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="a255e-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="a255e-105">Dit omvat het overboeken van intracommunautaire handelstransacties naar de EU-verkooplijst en het uitvoeren van het rapport.</span><span class="sxs-lookup"><span data-stu-id="a255e-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="a255e-106">Deze procedure omvat ook het maken van een intracommunautair handelstransactie voor demodoeleinden.</span><span class="sxs-lookup"><span data-stu-id="a255e-106">This procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="a255e-107">Raadpleeg voor meer informatie over EU-verkooplijstrapportage, met inbegrip van vereisten, de Help.</span><span class="sxs-lookup"><span data-stu-id="a255e-107">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="a255e-108">Deze procedure is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="a255e-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="a255e-109">De procedure werd gemaakt met de demogegevens van het bedrijf DEMF en dus Duitsland als voorbeeld voor land/regio.</span><span class="sxs-lookup"><span data-stu-id="a255e-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="a255e-110">De procedure maakt ook gebruik van Portugal als voorbeeld van EU-land/-regio.</span><span class="sxs-lookup"><span data-stu-id="a255e-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="a255e-111">Voordat u deze procedure kunt uitvoeren, moet u het rapporteren van de EU-verkooplijst configureren.</span><span class="sxs-lookup"><span data-stu-id="a255e-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="a255e-112">Deze procedure is alleen bedoeld voor accountants.</span><span class="sxs-lookup"><span data-stu-id="a255e-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="a255e-113">Een intracommunautaire verkooptransactie voor demodoeleinden maken</span><span class="sxs-lookup"><span data-stu-id="a255e-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="a255e-114">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="a255e-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a255e-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a255e-115">Click New.</span></span>
3. <span data-ttu-id="a255e-116">Typ 'PRT-001' in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="a255e-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="a255e-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a255e-117">Click OK.</span></span>
5. <span data-ttu-id="a255e-118">Typ in het veld Artikelnummer de waarde 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="a255e-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="a255e-119">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="a255e-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="a255e-120">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="a255e-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="a255e-121">Typ 'VOL' in het veld Btw-groep voor artikel.</span><span class="sxs-lookup"><span data-stu-id="a255e-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="a255e-122">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a255e-122">Click Add line.</span></span>
10. <span data-ttu-id="a255e-123">Typ in het veld Artikelnummer de waarde 'D0003'.</span><span class="sxs-lookup"><span data-stu-id="a255e-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="a255e-124">Typ 'ROOD' in het veld Btw-groep voor artikel.</span><span class="sxs-lookup"><span data-stu-id="a255e-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="a255e-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a255e-125">Click Save.</span></span>
13. <span data-ttu-id="a255e-126">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="a255e-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="a255e-127">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="a255e-127">Click Invoice.</span></span>
15. <span data-ttu-id="a255e-128">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="a255e-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="a255e-129">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="a255e-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="a255e-130">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="a255e-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="a255e-131">Stel de datum in het veld Factuurdatum in op '01/11/2016'.</span><span class="sxs-lookup"><span data-stu-id="a255e-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="a255e-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a255e-132">Click OK.</span></span>
20. <span data-ttu-id="a255e-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a255e-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="a255e-134">Intracommunautaire handelstransacties naar de EU-verkooplijst overboeken</span><span class="sxs-lookup"><span data-stu-id="a255e-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="a255e-135">Ga naar Belasting > Aangiften > Buitenlandse handel > ICL-lijst.</span><span class="sxs-lookup"><span data-stu-id="a255e-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="a255e-136">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="a255e-136">Click Transfer.</span></span>
3. <span data-ttu-id="a255e-137">Selecteer Ja in het veld Artikel om artikeltransacties over te boeken.</span><span class="sxs-lookup"><span data-stu-id="a255e-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="a255e-138">Selecteer Ja in het veld Service om servicetransacties over te boeken.</span><span class="sxs-lookup"><span data-stu-id="a255e-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="a255e-139">U kunt ook extra filters op intracommunautair handelstransacties opgeven voor overboeking.</span><span class="sxs-lookup"><span data-stu-id="a255e-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="a255e-140">Klik op Overbrengen.</span><span class="sxs-lookup"><span data-stu-id="a255e-140">Click Transfer.</span></span>
    * <span data-ttu-id="a255e-141">Controleer of de intracommunautaire verkooptransactie goed is overgeboekt naar de EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="a255e-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="a255e-142">Het rapport van de EU-verkooplijst genereren</span><span class="sxs-lookup"><span data-stu-id="a255e-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="a255e-143">Klik op Rapportage.</span><span class="sxs-lookup"><span data-stu-id="a255e-143">Click Reporting.</span></span>
2. <span data-ttu-id="a255e-144">Selecteer 'Maandelijks' in het veld Aangifteperiode.</span><span class="sxs-lookup"><span data-stu-id="a255e-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="a255e-145">Stel in het veld Begindatum de datum in op '01/01/2016'.</span><span class="sxs-lookup"><span data-stu-id="a255e-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="a255e-146">Selecteer Ja in het veld Bestand maken.</span><span class="sxs-lookup"><span data-stu-id="a255e-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="a255e-147">Selecteer Ja in het veld Rapport maken.</span><span class="sxs-lookup"><span data-stu-id="a255e-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="a255e-148">Typ 'EUSalesList' in het veld Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="a255e-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="a255e-149">Typ 'EUSalesList' in het veld Bestandsnaam van rapport.</span><span class="sxs-lookup"><span data-stu-id="a255e-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="a255e-150">Typ '123' in het veld Registratie-id van EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="a255e-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="a255e-151">Dit veld is alleen beschikbaar voor Duitsland.</span><span class="sxs-lookup"><span data-stu-id="a255e-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="a255e-152">U kunt ook extra filters op intracommunautair handelstransacties opgeven om in het rapport op te nemen.</span><span class="sxs-lookup"><span data-stu-id="a255e-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="a255e-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a255e-153">Click OK.</span></span>
    * <span data-ttu-id="a255e-154">Controleer of de pop-upvensters worden weergegeven om te bevestigen dat het bestand en het controlerapport worden gedownload.</span><span class="sxs-lookup"><span data-stu-id="a255e-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="a255e-155">Regels van EU-verkooplijst markeren als Gerapporteerd</span><span class="sxs-lookup"><span data-stu-id="a255e-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="a255e-156">Klik op Markeren.</span><span class="sxs-lookup"><span data-stu-id="a255e-156">Click Mark.</span></span>
2. <span data-ttu-id="a255e-157">Klik op Markeren als gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="a255e-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="a255e-158">Selecteer in de lijst de rij voor het veld Factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="a255e-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="a255e-159">Typ '01/01/2016..01/31/2016' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a255e-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="a255e-160">Selecteer in de lijst de rij voor het veld Rapportagestatus.</span><span class="sxs-lookup"><span data-stu-id="a255e-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="a255e-161">Selecteer 'Opgenomen' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a255e-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="a255e-162">U kunt ook extra filters op intracommunautair handelstransacties opgeven om te markeren als Gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="a255e-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="a255e-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a255e-163">Click OK.</span></span>
8. <span data-ttu-id="a255e-164">Selecteer 'Gerapporteerd' in het veld Selectie.</span><span class="sxs-lookup"><span data-stu-id="a255e-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="a255e-165">Regels van EU-verkooplijst markeren als Afgesloten</span><span class="sxs-lookup"><span data-stu-id="a255e-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="a255e-166">Klik op Markeren.</span><span class="sxs-lookup"><span data-stu-id="a255e-166">Click Mark.</span></span>
2. <span data-ttu-id="a255e-167">Klik op Markeren als afgesloten.</span><span class="sxs-lookup"><span data-stu-id="a255e-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="a255e-168">Markeer in de lijst de rij voor het veld Factuurnummer.</span><span class="sxs-lookup"><span data-stu-id="a255e-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="a255e-169">Typ '01/01/2016..01/31/2016' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a255e-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="a255e-170">Markeer in de lijst de rij voor het veld Rapportagestatus.</span><span class="sxs-lookup"><span data-stu-id="a255e-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="a255e-171">Selecteer 'Gerapporteerd' in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a255e-171">In the Criteria field, select 'Reported'.</span></span>
    * <span data-ttu-id="a255e-172">U kunt ook extra filters op intracommunautair handelstransacties opgeven om te markeren als Afgesloten.</span><span class="sxs-lookup"><span data-stu-id="a255e-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="a255e-173">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a255e-173">Click OK.</span></span>
8. <span data-ttu-id="a255e-174">Selecteer 'Afgesloten' in het veld Selectie.</span><span class="sxs-lookup"><span data-stu-id="a255e-174">In the Selection field, select 'Closed'.</span></span>

