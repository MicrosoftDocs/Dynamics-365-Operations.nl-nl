---
title: EUR-00011 Rapport van ICL-lijst instellen
description: Deze taak begeleidt u door een overzicht van de vereisten voor rapportage van de EU-verkooplijst.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b44d439bf1e991380fb7273a70e1f69f807c8b25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174684"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="58bef-103">EUR-00011 Rapport van ICL-lijst instellen</span><span class="sxs-lookup"><span data-stu-id="58bef-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58bef-104">Deze taak begeleidt u door een overzicht van de vereisten voor rapportage van de EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="58bef-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="58bef-105">Raadpleeg voor meer informatie over EU-verkooplijstrapportage, met inbegrip van vereisten, de Help.</span><span class="sxs-lookup"><span data-stu-id="58bef-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="58bef-106">Deze taak is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="58bef-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="58bef-107">De handleiding werd gemaakt met de demogegevens van het bedrijf DEMF en dus Duitsland als voorbeeld voor land/regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="58bef-108">De handleiding maakt ook gebruik van Portugal als voorbeeld van EU-land/-regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="58bef-109">Deze taken zijn bedoeld voor systeembeheerders.</span><span class="sxs-lookup"><span data-stu-id="58bef-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="58bef-110">Configuraties van elektronische rapportage importeren voor rapportage van EU-verkooplijst</span><span class="sxs-lookup"><span data-stu-id="58bef-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="58bef-111">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="58bef-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="58bef-112">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="58bef-112">Click Set active.</span></span>
3. <span data-ttu-id="58bef-113">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="58bef-113">Click Repositories.</span></span>
4. <span data-ttu-id="58bef-114">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="58bef-114">Click Open.</span></span>
5. <span data-ttu-id="58bef-115">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="58bef-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="58bef-116">Klik op Geavanceerd filteren/sorteren.</span><span class="sxs-lookup"><span data-stu-id="58bef-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="58bef-117">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="58bef-117">Click Add.</span></span>
8. <span data-ttu-id="58bef-118">Selecteer 'Configuratienaam' in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="58bef-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="58bef-119">Typ in het veld Criteria 'EU-verkooplijst (DE)'.</span><span class="sxs-lookup"><span data-stu-id="58bef-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="58bef-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="58bef-120">Click OK.</span></span>
11. <span data-ttu-id="58bef-121">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="58bef-121">Click Import.</span></span>
12. <span data-ttu-id="58bef-122">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="58bef-122">Click Yes.</span></span>
13. <span data-ttu-id="58bef-123">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="58bef-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="58bef-124">Klik op Geavanceerd filteren/sorteren.</span><span class="sxs-lookup"><span data-stu-id="58bef-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="58bef-125">Klik op Opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="58bef-125">Click Reset.</span></span>
16. <span data-ttu-id="58bef-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="58bef-126">Click Add.</span></span>
17. <span data-ttu-id="58bef-127">Selecteer 'Configuratienaam' in het veld Veld.</span><span class="sxs-lookup"><span data-stu-id="58bef-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="58bef-128">Typ in het veld Criteria 'Rapport van EU-verkooplijst per rij'.</span><span class="sxs-lookup"><span data-stu-id="58bef-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="58bef-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="58bef-129">Click OK.</span></span>
20. <span data-ttu-id="58bef-130">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="58bef-130">Click Import.</span></span>
21. <span data-ttu-id="58bef-131">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="58bef-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="58bef-132">Btw-codes voor rapportage van EU-verkooplijst instellen</span><span class="sxs-lookup"><span data-stu-id="58bef-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="58bef-133">Ga naar Btw > Indirecte belastingen > Btw > Btw-codes.</span><span class="sxs-lookup"><span data-stu-id="58bef-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="58bef-134">Gebruik het snelfilter om op het veld Btw-code te filteren met de waarde 'VAT19'.</span><span class="sxs-lookup"><span data-stu-id="58bef-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="58bef-135">Vouw de sectie Rapport instellen uit.</span><span class="sxs-lookup"><span data-stu-id="58bef-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="58bef-136">Controleer of de selectie Uitgesloten op Nee is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="58bef-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="58bef-137">U moet mogelijk de taakbegeleiding ontgrendelen om deze instelling te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="58bef-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="58bef-138">Btw-groepen voor rapportage van EU-verkooplijst instellen</span><span class="sxs-lookup"><span data-stu-id="58bef-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="58bef-139">Ga naar Btw > Indirecte belastingen > Btw > Btw-groepen.</span><span class="sxs-lookup"><span data-stu-id="58bef-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="58bef-140">Gebruik het snelfilter om op het veld Btw-groep te filteren met de waarde 'AR-DOM'.</span><span class="sxs-lookup"><span data-stu-id="58bef-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="58bef-141">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="58bef-141">Click Edit.</span></span>
4. <span data-ttu-id="58bef-142">Vouw de sectie Instellingen uit.</span><span class="sxs-lookup"><span data-stu-id="58bef-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="58bef-143">Selecteer de eerste rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="58bef-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="58bef-144">Selecteer het selectievakje Vrijstelling.</span><span class="sxs-lookup"><span data-stu-id="58bef-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="58bef-145">Selecteer de tweede rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="58bef-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="58bef-146">Selecteer het selectievakje Vrijstelling.</span><span class="sxs-lookup"><span data-stu-id="58bef-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="58bef-147">Selecteer de derde rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="58bef-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="58bef-148">Selecteer het selectievakje Vrijstelling.</span><span class="sxs-lookup"><span data-stu-id="58bef-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="58bef-149">Btw-groepen voor artikel voor rapportage van EU-verkooplijst instellen</span><span class="sxs-lookup"><span data-stu-id="58bef-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="58bef-150">Ga naar Btw > Indirecte belastingen > Btw > Btw-groepen voor artikel.</span><span class="sxs-lookup"><span data-stu-id="58bef-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="58bef-151">Gebruik het snelfilter om op het veld -groep voor artikel te filteren met de waarde 'FULL'.</span><span class="sxs-lookup"><span data-stu-id="58bef-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="58bef-152">Controleer of de selectie Rapporteringstype op 'Artikel' is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="58bef-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="58bef-153">U moet mogelijk de taakbegeleiding ontgrendelen om de waarde in dit veld te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="58bef-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="58bef-154">Gebruik het snelfilter om op het veld -groep voor artikel te filteren met de waarde 'RED'.</span><span class="sxs-lookup"><span data-stu-id="58bef-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="58bef-155">Controleer of de selectie Rapporteringstype op 'Service' is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="58bef-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="58bef-156">U moet mogelijk de taakbegeleiding ontgrendelen om de waarde in dit veld te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="58bef-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="58bef-157">Parameters van land/regio voor rapportage van EU-verkooplijst instellen</span><span class="sxs-lookup"><span data-stu-id="58bef-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="58bef-158">Ga naar Btw > Instellen > Btw > Parameters land/regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="58bef-159">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="58bef-159">Click New.</span></span>
3. <span data-ttu-id="58bef-160">Typ 'PRT' in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="58bef-161">Typ 'PT' in het Btw-veld.</span><span class="sxs-lookup"><span data-stu-id="58bef-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="58bef-162">Btw-vrijstellingsnummers maken</span><span class="sxs-lookup"><span data-stu-id="58bef-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="58bef-163">Ga naar Btw > Instellen > Btw > Nummers van belastingvrijstelling.</span><span class="sxs-lookup"><span data-stu-id="58bef-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="58bef-164">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="58bef-164">Click New.</span></span>
3. <span data-ttu-id="58bef-165">Typ 'PRT' in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="58bef-166">Typ 'PT12345' in het veld Nummers van belastingvrijstelling.</span><span class="sxs-lookup"><span data-stu-id="58bef-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="58bef-167">Parameters van rapportage van EU-verkooplijst instellen</span><span class="sxs-lookup"><span data-stu-id="58bef-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="58bef-168">Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="58bef-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="58bef-169">Klik op het tabblad EU-verkooplijst.</span><span class="sxs-lookup"><span data-stu-id="58bef-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="58bef-170">Selecteer Ja in het veld Inkopen overboeken.</span><span class="sxs-lookup"><span data-stu-id="58bef-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="58bef-171">Vouw de sectie Afrondingsregels uit.</span><span class="sxs-lookup"><span data-stu-id="58bef-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="58bef-172">Stel Afrondingsregel in op '0.1'.</span><span class="sxs-lookup"><span data-stu-id="58bef-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="58bef-173">Selecteer Ja in het veld Minimumwaarde gebruiken.</span><span class="sxs-lookup"><span data-stu-id="58bef-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="58bef-174">Typ '2' in het veld Aantal decimalen.</span><span class="sxs-lookup"><span data-stu-id="58bef-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="58bef-175">Vouw de sectie Elektronische rapportage uit.</span><span class="sxs-lookup"><span data-stu-id="58bef-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="58bef-176">Selecteer 'EU-verkooplijst (DE)' in het veld Toewijzing van bestandsindeling.</span><span class="sxs-lookup"><span data-stu-id="58bef-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="58bef-177">Selecteer 'Rapport van EU-verkooplijst per rij' in het veld Toewijzing van rapportindeling.</span><span class="sxs-lookup"><span data-stu-id="58bef-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="58bef-178">Klik op het tabblad Land-/regio-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="58bef-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="58bef-179">Controleer of het veld Land-/regiotype op 'Binnenlands' is ingesteld voor Land/regio DEU.</span><span class="sxs-lookup"><span data-stu-id="58bef-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="58bef-180">U moet mogelijk de taakbegeleiding ontgrendelen om de waarde in dit veld te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="58bef-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="58bef-181">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="58bef-181">Click New.</span></span>
13. <span data-ttu-id="58bef-182">Typ 'PRT' in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="58bef-183">Typ 'PT' in het veld Intrastatcode.</span><span class="sxs-lookup"><span data-stu-id="58bef-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="58bef-184">Selecteer 'EU' in het veld Land-/regiotype.</span><span class="sxs-lookup"><span data-stu-id="58bef-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="58bef-185">Klik op het tabblad Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="58bef-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="58bef-186">Controleer of er een Nummerreekscode is opgegeven voor de referentie 'EU-verkooplijst'.</span><span class="sxs-lookup"><span data-stu-id="58bef-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="58bef-187">Een klant maken voor demodoeleinden van rapportage van EU-verkooplijst</span><span class="sxs-lookup"><span data-stu-id="58bef-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="58bef-188">Ga naar Klanten > Klanten > Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="58bef-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="58bef-189">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="58bef-189">Click New.</span></span>
3. <span data-ttu-id="58bef-190">Typ 'PRT-001' in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="58bef-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="58bef-191">Typ 'Een klant uit Portugal' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="58bef-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="58bef-192">Selecteer '10' in het veld Klantgroep.</span><span class="sxs-lookup"><span data-stu-id="58bef-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="58bef-193">Selecteer 'AR-DOM' in het veld Btw-groep.</span><span class="sxs-lookup"><span data-stu-id="58bef-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="58bef-194">Selecteer 'PT12345' in het veld Nummers van belastingvrijstelling.</span><span class="sxs-lookup"><span data-stu-id="58bef-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="58bef-195">Typ 'PRT' in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="58bef-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="58bef-196">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="58bef-196">Click Save.</span></span>
