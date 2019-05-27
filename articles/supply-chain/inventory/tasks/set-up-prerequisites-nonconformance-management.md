---
title: Vereisten voor niet-conformeringsbeheer instellen
description: Met deze procedure kunt u de processen van het niet-conformeringsbeheer inschakelen.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554209"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="22bf8-103">Vereisten voor niet-conformeringsbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="22bf8-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22bf8-104">Met deze procedure kunt u de processen van het niet-conformeringsbeheer inschakelen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="22bf8-105">Met een niet-conformering wordt een artikel met kwaliteitsproblemen beschreven, waarbij de omschrijvende informatie de bron en het type probleem bevat.</span><span class="sxs-lookup"><span data-stu-id="22bf8-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="22bf8-106">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="22bf8-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="22bf8-107">Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsmanager.</span><span class="sxs-lookup"><span data-stu-id="22bf8-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="22bf8-108">Kwaliteitsbeheerprocessen binnen het bedrijf inschakelen</span><span class="sxs-lookup"><span data-stu-id="22bf8-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="22bf8-109">Ga naar Voorraadbeheer > Instellingen > Parameters voor voorraad- en magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="22bf8-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="22bf8-110">Klik op het tabblad Kwaliteitsbeheer.</span><span class="sxs-lookup"><span data-stu-id="22bf8-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="22bf8-111">Selecteer Ja in het veld Kwaliteitsbeheer gebruiken.</span><span class="sxs-lookup"><span data-stu-id="22bf8-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="22bf8-112">Selecteer deze parameter om kwaliteitsbeheerprocessen voor het bedrijf in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="22bf8-113">Voer een getal in het veld Uurtarief in.</span><span class="sxs-lookup"><span data-stu-id="22bf8-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="22bf8-114">Gebruik het veld Uurtarief om een uurtarief in de lokale valuta in te voeren.</span><span class="sxs-lookup"><span data-stu-id="22bf8-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="22bf8-115">Het uurtarief wordt gebruikt voor het berekenen van de kosten voor bewerkingen die zijn gerelateerd aan een non-conformiteit.</span><span class="sxs-lookup"><span data-stu-id="22bf8-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="22bf8-116">Het uurtarief en de berekende kosten vormen referentiegegevens voor een non-conformiteit en ze worden niet gebruikt door andere functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="22bf8-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="22bf8-117">Klik op Rapportinstellingen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-117">Click Report setup.</span></span>
    * <span data-ttu-id="22bf8-118">Op deze pagina definieert u de notitietypen voor kwaliteitsrapporten die worden gebruikt in verschillende typen kwaliteitsbeheerrapporten.</span><span class="sxs-lookup"><span data-stu-id="22bf8-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="22bf8-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-119">Close the page.</span></span>
7. <span data-ttu-id="22bf8-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="22bf8-121">Gebruiker voor niet-conformeringsverwerking inschakelen</span><span class="sxs-lookup"><span data-stu-id="22bf8-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="22bf8-122">Ga naar Systeembeheer > Gebruikers > Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="22bf8-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="22bf8-123">Om de goedkeuring van een niet-conformering te verwerken, moet aan de gebruiker die niet-conformeringen goedkeurt of afwijst, de waarde 'Naam' worden toegewezen op de pagina Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="22bf8-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="22bf8-124">Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="22bf8-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="22bf8-125">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="22bf8-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="22bf8-126">Filter bijvoorbeeld op het veld Naam met de waarde 'Ricardo'.</span><span class="sxs-lookup"><span data-stu-id="22bf8-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="22bf8-127">Gebruik het filter om de gebruiker te zoeken die de niet-conformeringsrecords goedkeurt of afwijst.</span><span class="sxs-lookup"><span data-stu-id="22bf8-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="22bf8-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="22bf8-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="22bf8-129">Om de goedkeuring van een niet-conformering te verwerken, moet u ervoor zorgen dat aan de gebruiker die niet-conformeringen goedkeurt of afwijst, de waarde 'Naam' is toegewezen op de pagina Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="22bf8-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="22bf8-130">Klik op Gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="22bf8-130">Click User options.</span></span>
5. <span data-ttu-id="22bf8-131">Klik op het tabblad Voorkeuren.</span><span class="sxs-lookup"><span data-stu-id="22bf8-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="22bf8-132">Selecteer Ja in het veld Documentverwerking inschakelen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="22bf8-133">Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="22bf8-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="22bf8-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-134">Close the page.</span></span>
8. <span data-ttu-id="22bf8-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-135">Close the page.</span></span>
9. <span data-ttu-id="22bf8-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="22bf8-137">Typen diagnose voor niet-conformeringsverwerking definiëren</span><span class="sxs-lookup"><span data-stu-id="22bf8-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="22bf8-138">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Typen diagnose.</span><span class="sxs-lookup"><span data-stu-id="22bf8-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="22bf8-139">Gebruik de pagina Diagnosetypen om een classificatie van diagnostische acties te definiëren.</span><span class="sxs-lookup"><span data-stu-id="22bf8-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="22bf8-140">Met een correctie definieert u welk type diagnostische actie moet worden uitgevoerd voor een goedgekeurde non-conformiteit, wie deze moet uitvoeren en wat de aangevraagde en geplande voltooiingsdatum is.</span><span class="sxs-lookup"><span data-stu-id="22bf8-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="22bf8-141">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22bf8-141">Click New.</span></span>
3. <span data-ttu-id="22bf8-142">Typ een waarde in het veld Diagnose.</span><span class="sxs-lookup"><span data-stu-id="22bf8-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="22bf8-143">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="22bf8-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22bf8-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="22bf8-145">Kwaliteitstoeslagen voor niet-conformeringsverwerking definiëren</span><span class="sxs-lookup"><span data-stu-id="22bf8-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="22bf8-146">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitstoeslagen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="22bf8-147">Gebruik de pagina van Kwaliteitstoeslagen om een classificatie van toeslagen te definiëren die wordt gebruikt in bewerkingen die zijn gerelateerd aan niet-conformeringen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="22bf8-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22bf8-148">Click New.</span></span>
3. <span data-ttu-id="22bf8-149">Typ een waarde in het veld Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="22bf8-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="22bf8-150">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="22bf8-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22bf8-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="22bf8-152">De bewerkingen voor niet-conformeringsverwerking definiëren</span><span class="sxs-lookup"><span data-stu-id="22bf8-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="22bf8-153">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="22bf8-154">Gebruik de pagina Bewerkingen om een classificatie te definiëren voor het werk dat kan worden uitgevoerd voor een goedgekeurde niet-conformering.</span><span class="sxs-lookup"><span data-stu-id="22bf8-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="22bf8-155">Wanneer u een bewerking relateert aan een niet-conformering, kunt u informatie over het bijbehorende materiaal, gekoppelde werkuren en diverse toeslagen definiëren die vereist zijn om de bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="22bf8-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="22bf8-156">Deze informatie vormt de basis voor het berekenen van de geschatte kosten voor de uitvoering van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="22bf8-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="22bf8-157">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22bf8-157">Click New.</span></span>
3. <span data-ttu-id="22bf8-158">Typ een waarde in het veld Bewerking.</span><span class="sxs-lookup"><span data-stu-id="22bf8-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="22bf8-159">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="22bf8-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22bf8-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="22bf8-161">Probleemtypen voor niet-conformeringsverwerking definiëren</span><span class="sxs-lookup"><span data-stu-id="22bf8-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="22bf8-162">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Probleemtypen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="22bf8-163">Gebruik de pagina Probleemtypen om een classificatie te definiëren van de kwaliteitsproblemen die zich voordoen in de verschillende niet-conformeringstypen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="22bf8-164">De niet-conformeringstypen omvatten Intern, Klant, Leverancier, Serviceaanvraag, Productie en Productie van coproducten.</span><span class="sxs-lookup"><span data-stu-id="22bf8-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="22bf8-165">Één probleemtype kan aan meerdere niet-conformeringstypen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="22bf8-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="22bf8-166">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22bf8-166">Click New.</span></span>
3. <span data-ttu-id="22bf8-167">Typ een waarde in het veld Probleemtype.</span><span class="sxs-lookup"><span data-stu-id="22bf8-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="22bf8-168">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="22bf8-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22bf8-169">Klik op Niet-conformeringstypen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="22bf8-170">Gebruik de pagina Niet-conformeringstypen om het gebruik van een probleemtype te autoriseren voor een of meer niet-conformeringstypen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="22bf8-171">Een probleemtype voor een defectcode kan bijvoorbeeld van toepassing zijn op alle non-conformiteitstypen, terwijl een probleemtype voor klachten van klanten alleen van toepassing is op de non-conformiteitstypen voor klanten en serviceaanvragen.</span><span class="sxs-lookup"><span data-stu-id="22bf8-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="22bf8-172">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22bf8-172">Click New.</span></span>
7. <span data-ttu-id="22bf8-173">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="22bf8-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="22bf8-174">Selecteer een optie in het veld Niet-conformeringstype.</span><span class="sxs-lookup"><span data-stu-id="22bf8-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="22bf8-175">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-175">Close the page.</span></span>
10. <span data-ttu-id="22bf8-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="22bf8-177">Quarantainezones voor niet-conformeringsverwerking definiëren</span><span class="sxs-lookup"><span data-stu-id="22bf8-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="22bf8-178">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Quarantainezones.</span><span class="sxs-lookup"><span data-stu-id="22bf8-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="22bf8-179">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22bf8-179">Click New.</span></span>
3. <span data-ttu-id="22bf8-180">Typ een waarde in het veld Quarantainezone.</span><span class="sxs-lookup"><span data-stu-id="22bf8-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="22bf8-181">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="22bf8-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22bf8-182">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="22bf8-182">Close the page.</span></span>

