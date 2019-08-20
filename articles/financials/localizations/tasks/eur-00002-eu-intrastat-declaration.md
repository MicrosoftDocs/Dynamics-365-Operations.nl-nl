---
title: EUR-00002 Een EU Intrastat-aangifte genereren
description: Deze procedure begeleidt u bij de stappen die nodig zijn om de Intrastat-aangifte in de elektronische bestandsindeling te exporteren en een voorbeeld te bekijken van de aangiftegegevens in een Excel-indeling.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7ab1d274b527bf5071900940bf53a57a88f482
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848870"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="851d2-103">EUR-00002 Een EU Intrastat-aangifte genereren</span><span class="sxs-lookup"><span data-stu-id="851d2-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="851d2-104">Deze procedure begeleidt u bij de stappen die nodig zijn om de Intrastat-aangifte in de elektronische bestandsindeling te exporteren en een voorbeeld te bekijken van de aangiftegegevens in een Excel-indeling.</span><span class="sxs-lookup"><span data-stu-id="851d2-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="851d2-105">Voordat u deze procedure kunt uitvoeren, moet u transacties overboeken naar Intrastat.</span><span class="sxs-lookup"><span data-stu-id="851d2-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="851d2-106">Deze procedure is gemaakt met het demobedrijf DEMF.</span><span class="sxs-lookup"><span data-stu-id="851d2-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="851d2-107">Configuraties met instellingen importeren</span><span class="sxs-lookup"><span data-stu-id="851d2-107">Import configurations with settings</span></span>
1. <span data-ttu-id="851d2-108">Ga naar Werkruimten > Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="851d2-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="851d2-109">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="851d2-109">Click Set active.</span></span>
3. <span data-ttu-id="851d2-110">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="851d2-110">Click Repositories.</span></span>
4. <span data-ttu-id="851d2-111">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="851d2-111">Click Open.</span></span>
5. <span data-ttu-id="851d2-112">Open de kolomfilter Configuratienaam.</span><span class="sxs-lookup"><span data-stu-id="851d2-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="851d2-113">Pas een filter toe op het veld "Configuratienaam" met de waarde "Intrastat (DE)" met behulp van de filteroperator ´begint met´.</span><span class="sxs-lookup"><span data-stu-id="851d2-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="851d2-114">U moet de configuratienaam selecteren die van toepassing is voor het land van uw rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="851d2-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="851d2-115">In deze procedure wordt de Duitse rechtspersoon (DEMF) als voorbeeld gebruikt. Daarom moet "Intrastat (DE") worden gekozen.</span><span class="sxs-lookup"><span data-stu-id="851d2-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="851d2-116">Klik op Importeren en klik vervolgens op Ja.</span><span class="sxs-lookup"><span data-stu-id="851d2-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="851d2-117">Open de kolomfilter Configuratienaam.</span><span class="sxs-lookup"><span data-stu-id="851d2-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="851d2-118">Pas een filter toe op het veld "Configuratienaam" met de waarde "Intrastat-rapport" met behulp van de filteroperator ´begint met´.</span><span class="sxs-lookup"><span data-stu-id="851d2-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="851d2-119">Klik op Importeren en klik vervolgens op Ja.</span><span class="sxs-lookup"><span data-stu-id="851d2-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="851d2-120">Parameters voor buitenlandse handel instellen</span><span class="sxs-lookup"><span data-stu-id="851d2-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="851d2-121">Ga naar Belasting > Instellingen > Buitenlandse handel > Parameters buitenlandse handel</span><span class="sxs-lookup"><span data-stu-id="851d2-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="851d2-122">Vouw de sectie Elektronische rapportage uit.</span><span class="sxs-lookup"><span data-stu-id="851d2-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="851d2-123">Typ of selecteer een waarde voor Intrastat (DE) in het veld Bestandsindelingstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="851d2-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="851d2-124">Typ of selecteer een waarde voor Intrastat-rapport in het veld Rapportindelingstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="851d2-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="851d2-125">Vouw de sectie Afrondingsregels uit.</span><span class="sxs-lookup"><span data-stu-id="851d2-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="851d2-126">U moet de afrondingsregels instellen die van toepassing zijn in uw land/regio voor Intrastat-rapportage.</span><span class="sxs-lookup"><span data-stu-id="851d2-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="851d2-127">Voer een nummer in het veld Afrondingsregel in.</span><span class="sxs-lookup"><span data-stu-id="851d2-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="851d2-128">Voer de afrondingsprecisie in. Voer bijvoorbeeld '0,01' in.</span><span class="sxs-lookup"><span data-stu-id="851d2-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="851d2-129">Voer een getal in het veld Aantal decimalen voor bedrag in.</span><span class="sxs-lookup"><span data-stu-id="851d2-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="851d2-130">Voer bijvoorbeeld 2 in:</span><span class="sxs-lookup"><span data-stu-id="851d2-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="851d2-131">Selecteer een optie in het veld Afronding onder 1 kg.</span><span class="sxs-lookup"><span data-stu-id="851d2-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="851d2-132">Selecteer bijvoorbeeld Afronden naar 1 kg.</span><span class="sxs-lookup"><span data-stu-id="851d2-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="851d2-133">Voer een nummer in het veld Afrondingsregel in.</span><span class="sxs-lookup"><span data-stu-id="851d2-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="851d2-134">Voer bijvoorbeeld '1' in voor afrondinggewicht op het gehele getal.</span><span class="sxs-lookup"><span data-stu-id="851d2-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="851d2-135">Vouw de sectie Ondergrens uit.</span><span class="sxs-lookup"><span data-stu-id="851d2-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="851d2-136">Voer een getal in het veld Gewicht in.</span><span class="sxs-lookup"><span data-stu-id="851d2-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="851d2-137">Voer bijvoorbeeld '10' als het minimumgewicht in.</span><span class="sxs-lookup"><span data-stu-id="851d2-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="851d2-138">Typ een getal in het veld Bedrag.</span><span class="sxs-lookup"><span data-stu-id="851d2-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="851d2-139">Voer bijvoorbeeld '200' als het minimumbedrag in.</span><span class="sxs-lookup"><span data-stu-id="851d2-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="851d2-140">Typ of selecteer een waarde in het veld Basisproduct.</span><span class="sxs-lookup"><span data-stu-id="851d2-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="851d2-141">Compressie van Intrastat instellen</span><span class="sxs-lookup"><span data-stu-id="851d2-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="851d2-142">Ga naar Belasting > Instellingen > Buitenlandse handel > Compressie van Intrastat.</span><span class="sxs-lookup"><span data-stu-id="851d2-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="851d2-143">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="851d2-143">Click Remove.</span></span>
3. <span data-ttu-id="851d2-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="851d2-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="851d2-145">Selecteer bijvoorbeeld Basisproduct in de sectie Beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="851d2-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="851d2-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="851d2-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="851d2-147">Intrastat-aangifte genereren</span><span class="sxs-lookup"><span data-stu-id="851d2-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="851d2-148">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat</span><span class="sxs-lookup"><span data-stu-id="851d2-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="851d2-149">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="851d2-149">Click Validate.</span></span>
    * <span data-ttu-id="851d2-150">De validatie wordt uitgevoerd op basis van het veld Instelling controleren op de pagina Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="851d2-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="851d2-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="851d2-151">Click OK.</span></span>
4. <span data-ttu-id="851d2-152">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="851d2-152">Click Update.</span></span>
5. <span data-ttu-id="851d2-153">Klik op Ondergrens.</span><span class="sxs-lookup"><span data-stu-id="851d2-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="851d2-154">Voer een datum in het veld Startdatum in.</span><span class="sxs-lookup"><span data-stu-id="851d2-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="851d2-155">Voer bijvoorbeeld 1 januari 2015 in.</span><span class="sxs-lookup"><span data-stu-id="851d2-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="851d2-156">Selecteer Ja in het veld Comprimeren.</span><span class="sxs-lookup"><span data-stu-id="851d2-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="851d2-157">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="851d2-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="851d2-158">Voer bijvoorbeeld 31 januari 2015 in.</span><span class="sxs-lookup"><span data-stu-id="851d2-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="851d2-159">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="851d2-159">Click OK.</span></span>
10. <span data-ttu-id="851d2-160">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="851d2-160">Click Update.</span></span>
11. <span data-ttu-id="851d2-161">Klik op Comprimeren.</span><span class="sxs-lookup"><span data-stu-id="851d2-161">Click Compress.</span></span>
    * <span data-ttu-id="851d2-162">Deze compressie vindt plaats volgens uw instellingen bij de Compressie van Intrastat.</span><span class="sxs-lookup"><span data-stu-id="851d2-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="851d2-163">Voer een datum in het veld Startdatum in.</span><span class="sxs-lookup"><span data-stu-id="851d2-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="851d2-164">Voer bijvoorbeeld 1 januari 2015 in.</span><span class="sxs-lookup"><span data-stu-id="851d2-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="851d2-165">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="851d2-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="851d2-166">Voer bijvoorbeeld 31 januari 2015 in.</span><span class="sxs-lookup"><span data-stu-id="851d2-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="851d2-167">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="851d2-167">Click OK.</span></span>
15. <span data-ttu-id="851d2-168">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="851d2-168">Click Update.</span></span>
16. <span data-ttu-id="851d2-169">Klik op Volgnummers opnieuw genereren.</span><span class="sxs-lookup"><span data-stu-id="851d2-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="851d2-170">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="851d2-170">Click OK.</span></span>
18. <span data-ttu-id="851d2-171">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="851d2-171">Click Output.</span></span>
19. <span data-ttu-id="851d2-172">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="851d2-172">Click Report.</span></span>
20. <span data-ttu-id="851d2-173">Voer in het veld Vanaf de eerste datum van de aangifteperiode in.</span><span class="sxs-lookup"><span data-stu-id="851d2-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="851d2-174">Stel de datum bijvoorbeeld op 1 januari 2015 in.</span><span class="sxs-lookup"><span data-stu-id="851d2-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="851d2-175">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="851d2-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="851d2-176">Voer bijvoorbeeld 31 januari 2015 in.</span><span class="sxs-lookup"><span data-stu-id="851d2-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="851d2-177">Selecteer Ja in het veld Bestand maken.</span><span class="sxs-lookup"><span data-stu-id="851d2-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="851d2-178">Typ een waarde in het veld Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="851d2-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="851d2-179">Selecteer Ja in het veld Rapport maken.</span><span class="sxs-lookup"><span data-stu-id="851d2-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="851d2-180">Typ een waarde in het veld Bestandsnaam van rapport.</span><span class="sxs-lookup"><span data-stu-id="851d2-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="851d2-181">Selecteer een optie in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="851d2-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="851d2-182">Selecteer bijvoorbeeld 'Verzendingen'.</span><span class="sxs-lookup"><span data-stu-id="851d2-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="851d2-183">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="851d2-183">Click OK.</span></span>

