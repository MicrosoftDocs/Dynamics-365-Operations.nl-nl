---
title: Projectcontracten
description: Dit onderwerp bevat voorbeelden van de projectcontracten die u voor diverse typen projecten en financieringsbronnen kunt maken. Daarnaast wordt aangegeven hoe u contracten en factuurprojectklanten kunt beheren.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185561"
---
# <a name="project-contracts"></a><span data-ttu-id="12240-103">Projectcontracten</span><span class="sxs-lookup"><span data-stu-id="12240-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12240-104">Dit artikel bevat voorbeelden van de projectcontracten die u voor diverse typen projecten en financieringsbronnen kunt maken. Daarnaast wordt aangegeven hoe u contracten en factuurprojectklanten kunt beheren.</span><span class="sxs-lookup"><span data-stu-id="12240-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="12240-105">Het type project dat u maakt voor een projectcontract bepaalt de wijze waarop projectklanten gefactureerd worden.</span><span class="sxs-lookup"><span data-stu-id="12240-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="12240-106">U kunt een projectcontract en het gerelateerde project wijzigen, maar u kunt het projecttype niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="12240-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="12240-107">Als u een projectcontract gebruikt, kunt u meerdere projecten tegelijkertijd factureren.</span><span class="sxs-lookup"><span data-stu-id="12240-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="12240-108">Het projectcontract zorgt ook voor een consistente factureringsprocedure voor elk subproject in een projectstructuur.</span><span class="sxs-lookup"><span data-stu-id="12240-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="12240-109">Elk project dat wordt gefactureerd, moet worden gekoppeld aan een projectcontract.</span><span class="sxs-lookup"><span data-stu-id="12240-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="12240-110">De instellingen voor een projectcontract gelden voor alle projecten en subprojecten die gekoppeld zijn aan het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="12240-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="12240-111">In een projectcontract kunnen meerdere financieringsbronnen worden gespecificeerd.</span><span class="sxs-lookup"><span data-stu-id="12240-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="12240-112">Hierdoor kunt u facturering tussen meerdere financiers instellen, financieringslimieten instellen zodat financieringsbronnen voor niet meer dan een bepaald bedrag worden gefactureerd, en kunt u financieringsregels instellen voor in rekening gebrachte uitgaven.</span><span class="sxs-lookup"><span data-stu-id="12240-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="12240-113">Financieren van projectcontracten</span><span class="sxs-lookup"><span data-stu-id="12240-113">Funding for project contracts</span></span>
<span data-ttu-id="12240-114">Bepaalde projectcontracten kunnen bepalen dat meerdere partijen de financieringsverantwoordelijkheden voor de projectkosten delen.</span><span class="sxs-lookup"><span data-stu-id="12240-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="12240-115">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="12240-115">Here are some examples:</span></span>

-   <span data-ttu-id="12240-116">Een grote klant kan bijvoorbeeld vragen om de financiering van een project te splitsen onder meerdere divisies.</span><span class="sxs-lookup"><span data-stu-id="12240-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="12240-117">Uw bedrijf deelt de kosten van een groot project met een externe organisatie.</span><span class="sxs-lookup"><span data-stu-id="12240-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="12240-118">Een wegenplan wordt medegefinancierd door twee gemeenten.</span><span class="sxs-lookup"><span data-stu-id="12240-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="12240-119">Een brugproject wordt gefinancierd door een overheidssubsidie en een particulier bedrijf.</span><span class="sxs-lookup"><span data-stu-id="12240-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="12240-120">In Dynamics 365 Finance kunt u de facturering voor één transactie of een volledig project splitsen tussen meerdere klanten, subsidies of organisaties.</span><span class="sxs-lookup"><span data-stu-id="12240-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="12240-121">Bij projecten met meerdere financiers, worden alle partijen die bijdragen tot de financiering van een geavanceerd financieringsproject financieringsbronnen genoemd.</span><span class="sxs-lookup"><span data-stu-id="12240-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="12240-122">Nadat een klant, organisatie of subsidie als financieringsbron is gedefinieerd, kan deze aan één of meer financieringsregels worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="12240-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="12240-123">De financieringsregels bevatten de criteria die bepalen hoe kosten aan verschillende financieringsbronnen voor een project moeten worden toegekend.</span><span class="sxs-lookup"><span data-stu-id="12240-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="12240-124">Omdat voorraadartikelen, zoals de artikelen op opdrachten tot inkoop en inkooporders, niet kunnen worden opgesplitst, kan het kostenbedrag bij de distributie ook niet worden opgesplitst tussen meerdere financieringsbronnen.</span><span class="sxs-lookup"><span data-stu-id="12240-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="12240-125">Daarom blijft de financieringsbronwaarde 0 (nul) tot de voorraaduitgifte wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="12240-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="12240-126">Wanneer de voorraaduitgifte wordt geboekt, wordt het kostenbedrag verdeeld volgens de rekeningdistributieregels voor het project.</span><span class="sxs-lookup"><span data-stu-id="12240-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="12240-127">U kunt het volgende doen om het gemakkelijker te maken om de facturering tussen meerdere financieringsbronnen te splitsen:</span><span class="sxs-lookup"><span data-stu-id="12240-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="12240-128">Specificeer dat alle transacties die voor een project worden ingevoerd, dezelfde verkoopvaluta gebruiken als het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="12240-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="12240-129">Stel financieringslimieten in zodat een financieringsbron niet meer wordt gefactureerd dan een opgegeven bedrag voor een project.</span><span class="sxs-lookup"><span data-stu-id="12240-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="12240-130">Configureer financieringsregels en financieringslimieten voor elke werknemer, artikel, categorie, categoriegroep en transactietype (of voor alle transactietypes).</span><span class="sxs-lookup"><span data-stu-id="12240-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="12240-131">Selecteer optionele start- en einddatums om de periode te definiëren waarvoor elke financieringsregel geldt.</span><span class="sxs-lookup"><span data-stu-id="12240-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="12240-132">Specificeer het percentage waarvoor elke financieringsbron verantwoordelijk is.</span><span class="sxs-lookup"><span data-stu-id="12240-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="12240-133">Specificeer welke financieringsbron verantwoordelijk is voor afrondingsverschillen als gevolg van financieringstoewijzingsberekeningen.</span><span class="sxs-lookup"><span data-stu-id="12240-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="12240-134">Stel regels in voor de wijze waarop projectkosten aan externe klanten worden gefactureerd en aan interne organisaties in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="12240-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="12240-135">Registreer transacties in een financieringsrekening in wachtstand tot extra financiering kan worden verkregen of u beslist om de kosten intern te dragen.</span><span class="sxs-lookup"><span data-stu-id="12240-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="12240-136">Om te bepalen welke btw-groep aan een transactie moet worden gekoppeld, wordt het project doorzocht op een btw-groepstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="12240-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="12240-137">Als er geen btw-groepstoewijzing is uitgevoerd op projectniveau, wordt het projectcontract doorzocht.</span><span class="sxs-lookup"><span data-stu-id="12240-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="12240-138">Voorbeeld: meerdere financieringsbronnen (eenvoudig)</span><span class="sxs-lookup"><span data-stu-id="12240-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="12240-139">De volgende tabel bevat scenario's voor het beheren van financieringstoewijzingen over meerdere financieringsbronnen.</span><span class="sxs-lookup"><span data-stu-id="12240-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="12240-140">Deze scenario's zijn gebaseerd op de volgende veronderstellingen:</span><span class="sxs-lookup"><span data-stu-id="12240-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="12240-141">Prioriteitsinstellingen worden toegepast in de toewijzing van middelen, voordat de andere financieringsregels worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="12240-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="12240-142">Er is geen datumbereik opgegeven voor de periode wanneer de financieringsregel geldt.</span><span class="sxs-lookup"><span data-stu-id="12240-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12240-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="12240-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="12240-144"><strong>Financieringsbron </strong></span><span class="sxs-lookup"><span data-stu-id="12240-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="12240-145"><strong>Toewijzingspercentage </strong></span><span class="sxs-lookup"><span data-stu-id="12240-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="12240-146"><strong>Toewijzingsprioriteit </strong></span><span class="sxs-lookup"><span data-stu-id="12240-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12240-147">U wilt kosten toewijzen aan een financieringsbron totdat de middelen zijn uitgeput, kosten toewijzen aan een tweede financieringsbron totdat de middelen zijn uitgeput en ten slotte de resterende kosten toewijzen aan een derde financieringsbron toewijzen.</span><span class="sxs-lookup"><span data-stu-id="12240-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-148">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="12240-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="12240-149">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="12240-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="12240-150">Financieringsbron 3</span><span class="sxs-lookup"><span data-stu-id="12240-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-151">100%</span><span class="sxs-lookup"><span data-stu-id="12240-151">100%</span></span></li>
<li><span data-ttu-id="12240-152">100%</span><span class="sxs-lookup"><span data-stu-id="12240-152">100%</span></span></li>
<li><span data-ttu-id="12240-153">100%</span><span class="sxs-lookup"><span data-stu-id="12240-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-154">1</span><span class="sxs-lookup"><span data-stu-id="12240-154">1</span></span></li>
<li><span data-ttu-id="12240-155">2</span><span class="sxs-lookup"><span data-stu-id="12240-155">2</span></span></li>
<li><span data-ttu-id="12240-156">3</span><span class="sxs-lookup"><span data-stu-id="12240-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12240-157">U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="12240-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="12240-158">Wanneer een van deze financieringsbronnen is opgebruikt, wilt u de resterende kosten betalen van een derde financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="12240-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-159">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="12240-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="12240-160">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="12240-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="12240-161">Financieringsbron 3</span><span class="sxs-lookup"><span data-stu-id="12240-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-162">75%</span><span class="sxs-lookup"><span data-stu-id="12240-162">75%</span></span></li>
<li><span data-ttu-id="12240-163">25%</span><span class="sxs-lookup"><span data-stu-id="12240-163">25%</span></span></li>
<li><span data-ttu-id="12240-164">100%</span><span class="sxs-lookup"><span data-stu-id="12240-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-165">1</span><span class="sxs-lookup"><span data-stu-id="12240-165">1</span></span></li>
<li><span data-ttu-id="12240-166">1</span><span class="sxs-lookup"><span data-stu-id="12240-166">1</span></span></li>
<li><span data-ttu-id="12240-167">2</span><span class="sxs-lookup"><span data-stu-id="12240-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12240-168">U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="12240-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="12240-169">Wanneer een van beide financieringsbronnen is opgebruikt, wilt u de resterende kosten delen tussen een derde en vierde financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="12240-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-170">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="12240-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="12240-171">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="12240-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="12240-172">Financieringsbron 3</span><span class="sxs-lookup"><span data-stu-id="12240-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="12240-173">Financieringsbron 4</span><span class="sxs-lookup"><span data-stu-id="12240-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-174">75%</span><span class="sxs-lookup"><span data-stu-id="12240-174">75%</span></span></li>
<li><span data-ttu-id="12240-175">25%</span><span class="sxs-lookup"><span data-stu-id="12240-175">25%</span></span></li>
<li><span data-ttu-id="12240-176">50%</span><span class="sxs-lookup"><span data-stu-id="12240-176">50%</span></span></li>
<li><span data-ttu-id="12240-177">50%</span><span class="sxs-lookup"><span data-stu-id="12240-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-178">1</span><span class="sxs-lookup"><span data-stu-id="12240-178">1</span></span></li>
<li><span data-ttu-id="12240-179">1</span><span class="sxs-lookup"><span data-stu-id="12240-179">1</span></span></li>
<li><span data-ttu-id="12240-180">2</span><span class="sxs-lookup"><span data-stu-id="12240-180">2</span></span></li>
<li><span data-ttu-id="12240-181">2</span><span class="sxs-lookup"><span data-stu-id="12240-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12240-182">U wilt de eerste 25 procent van de kosten toewijzen aan één financieringsbron en de rest aan een andere.</span><span class="sxs-lookup"><span data-stu-id="12240-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-183">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="12240-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="12240-184">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="12240-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-185">25%</span><span class="sxs-lookup"><span data-stu-id="12240-185">25%</span></span></li>
<li><span data-ttu-id="12240-186">100%</span><span class="sxs-lookup"><span data-stu-id="12240-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="12240-187">1</span><span class="sxs-lookup"><span data-stu-id="12240-187">1</span></span></li>
<li><span data-ttu-id="12240-188">2</span><span class="sxs-lookup"><span data-stu-id="12240-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="12240-189">Voorbeeld: meerdere financieringsbronnen (complex)</span><span class="sxs-lookup"><span data-stu-id="12240-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="12240-190">U hebt drie financieringsbronnen en u wilt ze gebruiken in de volgende volgorde:</span><span class="sxs-lookup"><span data-stu-id="12240-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="12240-191">Financieringsbron 2 en 3 financieringsbron 3 evenveel gebruiken tot financieringsbron 2 is uitgeput.</span><span class="sxs-lookup"><span data-stu-id="12240-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="12240-192">Financieringsbron 3 verder gebruiken totdat deze is uitgeput.</span><span class="sxs-lookup"><span data-stu-id="12240-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="12240-193">Financieringsbron 1 gebruiken nadat financieringsbron 3 is uitgeput.</span><span class="sxs-lookup"><span data-stu-id="12240-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="12240-194">Om dit doel te bereiken, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="12240-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="12240-195">Stel financieringslimieten in voor financieringsbron 2 en financieringsbron 3 voor hun respectieve bedragen.</span><span class="sxs-lookup"><span data-stu-id="12240-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="12240-196">Maak de volgende financieringsregels:</span><span class="sxs-lookup"><span data-stu-id="12240-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="12240-197">Regel 1 (prioriteit 1): Wijs 50 procent van de transacties toe aan financieringsbron 2 en 50 procent aan financieringsbron 3.</span><span class="sxs-lookup"><span data-stu-id="12240-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="12240-198">Regel 2 (prioriteit 2): Wijs 100 procent van de transacties toe aan financieringsbron 3.</span><span class="sxs-lookup"><span data-stu-id="12240-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="12240-199">Regel 3 (prioriteit 3): Wijs 100 procent van de transacties toe aan financieringsbron 1.</span><span class="sxs-lookup"><span data-stu-id="12240-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="12240-200">Deze configuratie werkt omdat de transacties worden vergeleken met de regels en limieten om te zien of deze van toepassing zijn op de transactie.</span><span class="sxs-lookup"><span data-stu-id="12240-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="12240-201">Als u er geen specifieke regels of limieten van toepassing zijn op de transactie, geldt de regel alle transacties.</span><span class="sxs-lookup"><span data-stu-id="12240-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="12240-202">De regel Alle transacties stemt overeen met alle transacties.</span><span class="sxs-lookup"><span data-stu-id="12240-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="12240-203">Als een regel wordt gevonden die overeenkomt met een transactie, wordt het percentage dat is toegewezen in die regel eerst toegepast, maar alleen nadat de overeenkomsten zijn gecontroleerd op eventuele limieten die zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="12240-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="12240-204">Als een limiet is bereikt en een financieringsbron is uitgeput, wordt de financieringsregel die is gekoppeld aan de financieringslimiet genegeerd en controleert het programma de volgende regel die van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="12240-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="12240-205">In sommige gevallen kan slechts een deel van een transactie onder een regel worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="12240-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="12240-206">Dit kan gebeuren omdat een limiet wordt bereikt wanneer de transactie wordt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="12240-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="12240-207">In dit geval wordt alleen een bepaald bedrag toegewezen volgens die regel, bijvoorbeeld 50 procent aan elke financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="12240-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="12240-208">Dit is het geval in regel 1, zoals eerder in dit gedeelte wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="12240-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="12240-209">De rest wordt toegewezen volgens de volgende regel in de reeks.</span><span class="sxs-lookup"><span data-stu-id="12240-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="12240-210">In de volgende tabel wordt dit scenario nader onderzocht.</span><span class="sxs-lookup"><span data-stu-id="12240-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12240-211"><strong>Focus</strong></span><span class="sxs-lookup"><span data-stu-id="12240-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="12240-212"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="12240-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12240-213">Financieringsregels</span><span class="sxs-lookup"><span data-stu-id="12240-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-214">Regel 1 (prioriteit 1): Alle transacties.</span><span class="sxs-lookup"><span data-stu-id="12240-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="12240-215">Financieringsbron 2 bij 50% en financieringsbron 3 bij 50%.</span><span class="sxs-lookup"><span data-stu-id="12240-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="12240-216">Regel 2 (prioriteit 2): Alle transacties.</span><span class="sxs-lookup"><span data-stu-id="12240-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="12240-217">Financieringsbron 3 toewijzen bij 100%.</span><span class="sxs-lookup"><span data-stu-id="12240-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="12240-218">Regel 3 (prioriteit 2): Alle transacties.</span><span class="sxs-lookup"><span data-stu-id="12240-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="12240-219">Financieringsbron 1 toewijzen bij 100%.</span><span class="sxs-lookup"><span data-stu-id="12240-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12240-220">Financieringslimieten</span><span class="sxs-lookup"><span data-stu-id="12240-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-221">Limiet financieringsbron 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="12240-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="12240-222">Limiet financieringsbron 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="12240-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="12240-223">Limiet financieringsbron 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="12240-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12240-224">Transactie 1</span><span class="sxs-lookup"><span data-stu-id="12240-224">Transaction 1</span></span></td>
<td><span data-ttu-id="12240-225"><strong>Transactiebedrag:</strong> 100,00<strong>Financiering:</strong> De transactie wordt alleen betaald volgens regel 1, aangezien de transactie volledig is betaald nadat regel 1 is toegepast.</span><span class="sxs-lookup"><span data-stu-id="12240-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="12240-226">De transactie wordt gelijk verdeeld tussen financieringsbron 2 en 3.</span><span class="sxs-lookup"><span data-stu-id="12240-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="12240-227">Financieringsbron 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="12240-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="12240-228">Financieringsbron 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="12240-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12240-229">Transactie 2</span><span class="sxs-lookup"><span data-stu-id="12240-229">Transaction 2</span></span></td>
<td><span data-ttu-id="12240-230"><strong>Transactiebedrag:</strong> 5000,00<strong>Financiering:</strong> De transactie is betaald volgens alle drie de regels.</span><span class="sxs-lookup"><span data-stu-id="12240-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="12240-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="12240-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="12240-232">Financieringsbron 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="12240-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="12240-233">Financieringsbron 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="12240-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="12240-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="12240-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="12240-235">Financieringsbron: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="12240-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="12240-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="12240-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="12240-237">Financieringsbron 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="12240-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12240-238">Totale middelen die worden verdeeld voor elke financieringsbron</span><span class="sxs-lookup"><span data-stu-id="12240-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="12240-239">Financieringsbron 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="12240-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="12240-240">Financieringsbron 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="12240-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="12240-241">Financieringsbron 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="12240-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="12240-242">Factureringsregels</span><span class="sxs-lookup"><span data-stu-id="12240-242">Billing rules</span></span>
<span data-ttu-id="12240-243">Wanneer u over een projectcontract met een klant onderhandelt, definieert u hoe en wanneer u de klant kunt factureren voor werkzaamheden aan een project.</span><span class="sxs-lookup"><span data-stu-id="12240-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="12240-244">Nadat u het projectcontract en het project hebt ingesteld, kunt u factureringsregels voor het project instellen.</span><span class="sxs-lookup"><span data-stu-id="12240-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="12240-245">De factureringsregels zijn gebaseerd op de projectvoorwaarden die in het projectcontract zijn gespecificeerd.</span><span class="sxs-lookup"><span data-stu-id="12240-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="12240-246">De factureringsregels die u kunt maken, hangen af van de voorwaarden in het projectcontract en het type project dat u aan de factureringsregel koppelt, bijvoorbeeld tijd en materiaal of vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="12240-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="12240-247">Voor een projectcontract kunnen meerdere factureringsregels worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="12240-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="12240-248">U kunt ook een factureringsregel toewijzen aan meerdere projecten die zijn gekoppeld aan hetzelfde projectcontract en soortgelijke facturatievoorwaarden hebben.</span><span class="sxs-lookup"><span data-stu-id="12240-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="12240-249">U kunt de volgende soorten factureringsregels instellen:</span><span class="sxs-lookup"><span data-stu-id="12240-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="12240-250">**Leveringseenheid** – Factureer een klant wanneer u een leveringseenheid hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="12240-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="12240-251">U bepaalt de leveringseenheden in het contract.</span><span class="sxs-lookup"><span data-stu-id="12240-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="12240-252">**Voortgang** – Factureer een klant wanneer u een gespecificeerd percentage van het project hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="12240-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="12240-253">U kunt een factureringsregel instellen die automatisch het percentage voltooid werk berekent, of u kunt handmatig het percentage voltooid werk en het te factureren bedrag aan de klant berekenen.</span><span class="sxs-lookup"><span data-stu-id="12240-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="12240-254">**Mijlpaal** – Factureer een klant voor het volledige bedrag van een mijlpaal wanneer een projectmijlpaal wordt bereikt.</span><span class="sxs-lookup"><span data-stu-id="12240-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="12240-255">**Kosten** – Factureer een klant voor uw diensten plus een beheertarief. Dit beheertarief betreft gewoonlijk een percentage van de kosten van diensten.</span><span class="sxs-lookup"><span data-stu-id="12240-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="12240-256">**Tijd en materiaal** – Factureer een klant voor de waarde van tijd en materiaal die voor een project wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12240-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="12240-257">Voor alle typen factureringsregels kunt u een inhoudingspercentage opgeven om van klantfacturen af te trekken tot een project een vooraf overeengekomen fase bereikt.</span><span class="sxs-lookup"><span data-stu-id="12240-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="12240-258">Het betalingsinhoudingspercentage is opgegeven in het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="12240-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="12240-259">Het bedrag wordt berekend voor en afgetrokken van de totale waarde van de regels in een klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="12240-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="12240-260">Voor de factureringsregels **Tijd en materiaal** en **Voortgang** kunt u toerekenbare categorieën toewijzen.</span><span class="sxs-lookup"><span data-stu-id="12240-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="12240-261">Toerekenbare categorieën geven de transacties aan die in klantfacturen opgenomen moeten worden.</span><span class="sxs-lookup"><span data-stu-id="12240-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="12240-262">Wanneer u klaar bent om de klant te factureren, wordt het te factureren bedrag voor het project berekend op basis van de factureringsregels en wordt er een projectfactuurvoorstel gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="12240-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="12240-263">De volgende secties bieden voorbeelden ter illustratie van het instellen en beheren van factureringregels voor een project.</span><span class="sxs-lookup"><span data-stu-id="12240-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="12240-264">Voorbeeld: Een factureringsregel maken die is gebaseerd op het aantal geleverde eenheden</span><span class="sxs-lookup"><span data-stu-id="12240-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="12240-265">Uw organisatie gaat een overeenkomst aan om in totaal vijf trainingssessies aan de werknemers van een klant te leveren met een waarde van 10.000 per trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="12240-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="12240-266">U factureert de klant na elke trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="12240-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="12240-267">Stel de factureringsregels voor het contract in met de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="12240-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="12240-268">De leveringseenheid is één trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="12240-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="12240-269">De eenheidsprijs is 10.000 per trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="12240-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="12240-270">Het totale aantal eenheden bedraagt vijf trainingssessies.</span><span class="sxs-lookup"><span data-stu-id="12240-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="12240-271">Wanneer u een trainingssessie hebt voltooid, kunt u een factuur voor 10.000 maken voor de eerste geleverde eenheid en deze naar de klant verzenden.</span><span class="sxs-lookup"><span data-stu-id="12240-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="12240-272">Voorbeeld: Een factureringsregel maken op basis van een gespecificeerd voltooiingspercentage (handmatige berekening)</span><span class="sxs-lookup"><span data-stu-id="12240-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="12240-273">Uw organisatie, een bedrijf op het gebied van softwareadvies, gaat een overeenkomst aan met een klant voor het ontwikkelen van een deel van een product dat door de klant wordt ontwikkeld.</span><span class="sxs-lookup"><span data-stu-id="12240-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="12240-274">Uw organisatie stemt ermee in om de softwarecode in de loop van een periode van zes maanden te leveren.</span><span class="sxs-lookup"><span data-stu-id="12240-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="12240-275">De klant stemt ermee in om uw organisatie in totaal 100.000 te betalen voor de werkzaamheden.</span><span class="sxs-lookup"><span data-stu-id="12240-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="12240-276">U maakt een factureringsregel om de klant te factureren op basis van een percentage voltooide werkzaamheden voor het project, zoals aangegeven in het contract.</span><span class="sxs-lookup"><span data-stu-id="12240-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="12240-277">Aan het einde van de eerste maand ontmoet u de klant om te bepalen welk percentage van de werkzaamheden is voltooid.</span><span class="sxs-lookup"><span data-stu-id="12240-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="12240-278">Na evaluatie van het project besluiten u en uw klant dat 15% van het project is voltooid.</span><span class="sxs-lookup"><span data-stu-id="12240-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="12240-279">U maakt een factuur voor een bedrag van 15.000 (15% van 100.000) en stuurt deze naar uw klant.</span><span class="sxs-lookup"><span data-stu-id="12240-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="12240-280">Voorbeeld: Een factureringsregel maken op basis van een gespecificeerd voltooiingspercentage (automatische berekening)</span><span class="sxs-lookup"><span data-stu-id="12240-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="12240-281">Uw organisatie, een bedrijf dat zich bezighoudt met het ontwikkelen van software, komt met een klant overeen om een salarisadministratiepakket te ontwikkelen voor een bedrag van 30.000.</span><span class="sxs-lookup"><span data-stu-id="12240-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="12240-282">De klant stemt ermee in om uw organisatie te betalen op basis van het percentage van de werkzaamheden dat is voltooid.</span><span class="sxs-lookup"><span data-stu-id="12240-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="12240-283">U schat dat de projectkosten 20.000 bedragen.</span><span class="sxs-lookup"><span data-stu-id="12240-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="12240-284">In het projectcontract zijn de categorieën werkzaamheden gespecificeerd die u in het factureringsproces kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="12240-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="12240-285">U stelt factureringsregels in die automatisch de factuurbedragen berekenen voor het percentage voltooide werkzaamheden voor de afzonderlijke categorieën.</span><span class="sxs-lookup"><span data-stu-id="12240-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="12240-286">U stelt voor elke categorie een budget in:</span><span class="sxs-lookup"><span data-stu-id="12240-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="12240-287">**Ontwikkeling** – De kosten bedragen 15.000 en de opbrengsten 20.000.</span><span class="sxs-lookup"><span data-stu-id="12240-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="12240-288">**Installatie** – De kosten bedragen 5.000 en de opbrengsten 10.000.</span><span class="sxs-lookup"><span data-stu-id="12240-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="12240-289">Wanneer u de klant voor de eerste keer factureert, wordt het factuurbedrag automatisch berekend op basis van de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="12240-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="12240-290">De werknemer op het project dient na een maand een urenstaat voor het project in.</span><span class="sxs-lookup"><span data-stu-id="12240-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="12240-291">De kosten van de werknemersuren bedragen 5.000 voor ontwikkeling en 1.000 voor installatie.</span><span class="sxs-lookup"><span data-stu-id="12240-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="12240-292">De ontwikkelingswerkzaamheden zijn voor 33% voltooid (5000 daadwerkelijke kosten/15.000 budgetkosten) en de installatiewerkzaamheden zijn voor 20% voltooid (1000 daadwerkelijke kosten/5000 budgetkosten).</span><span class="sxs-lookup"><span data-stu-id="12240-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="12240-293">Het factuurbedrag van 8667 wordt automatisch berekend (33 procent van 20.000 + 20 procent van 10.000).</span><span class="sxs-lookup"><span data-stu-id="12240-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="12240-294">U maakt een factuur voor een bedrag van 8667 en stuurt deze naar de klant.</span><span class="sxs-lookup"><span data-stu-id="12240-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="12240-295">Voorbeeld: Een factureringsregel maken op basis van afgesproken mijlpalen</span><span class="sxs-lookup"><span data-stu-id="12240-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="12240-296">Uw organisatie, een bedrijf op het gebied van beheeradvies, stemt ermee in diensten op het vlak van het uitvoeren van marktonderzoek te leveren voor een consumentenproduct dat uw klant wil gaan verkopen.</span><span class="sxs-lookup"><span data-stu-id="12240-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="12240-297">U komt met de klant overeen dat deze uw diensten met ingang van maart zal gaan gebruiken voor een periode van drie maanden en dat de klant uw organisatie hiervoor een bedrag van 50.000 verschuldigd is.</span><span class="sxs-lookup"><span data-stu-id="12240-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="12240-298">Het project heeft drie mijlpalen:</span><span class="sxs-lookup"><span data-stu-id="12240-298">The project has three milestones:</span></span>

-   <span data-ttu-id="12240-299">Mijlpaal 1: Verzamelen consumentgegevens – 31 maart</span><span class="sxs-lookup"><span data-stu-id="12240-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="12240-300">Mijlpaal 2: Analyseren consumentgegevens – 30 april</span><span class="sxs-lookup"><span data-stu-id="12240-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="12240-301">Mijlpaal 3: Een voorstel presenteren met betrekking tot de levensvatbaarheid van het product – 31 mei</span><span class="sxs-lookup"><span data-stu-id="12240-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="12240-302">U komt met de klant overeen dat deze uw organisatie 10.000 betaalt voor de eerste mijlpaal en 20.000 voor elk van de volgende twee mijlpalen.</span><span class="sxs-lookup"><span data-stu-id="12240-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="12240-303">U spreekt bij het opstellen van het projectcontract met de klant af dat u telkens factureert op basis van een voltooide mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="12240-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="12240-304">Het instellen van de factureringsregel omvat de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="12240-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="12240-305">Definieer de projectmijlpalen.</span><span class="sxs-lookup"><span data-stu-id="12240-305">Define the project milestones.</span></span>
-   <span data-ttu-id="12240-306">Definieer het bedrag waarvoor de klant moet worden gefactureerd wanneer elke projectmijlpaal wordt behaald.</span><span class="sxs-lookup"><span data-stu-id="12240-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="12240-307">Nadat u de eerste mijlpaal op 31 maart hebt voltooid, markeert u de mijlpaal als voltooid en maakt u een factuur voor een bedrag van 10.000 om naar de klant te sturen.</span><span class="sxs-lookup"><span data-stu-id="12240-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="12240-308">U kunt pas een factuur voor een mijlpaal maken als u de mijlpaal als voltooid hebt gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="12240-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="12240-309">Voorbeeld: Een factureringsregel maken op basis van diensten plus een beheertarief</span><span class="sxs-lookup"><span data-stu-id="12240-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="12240-310">Uw organisatie, een bedrijf op het gebied van beheeradvies, stemt ermee in marktonderzoek uit te voeren om de levensvatbaarheid te beoordelen van een product dat de klant, een retailbedrijf, in ontwikkeling heeft.</span><span class="sxs-lookup"><span data-stu-id="12240-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="12240-311">Volgens de bepalingen van de overeenkomst levert u de diensten van uw drie belangrijkste beheerconsultants voor het uitvoeren van onderzoek op een tijd-en-materialen-basis.</span><span class="sxs-lookup"><span data-stu-id="12240-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="12240-312">U komt met de klant overeen dat deze 100 per uur betaalt, plus een managementtarief van 10% voor de adviesuren die voor het project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="12240-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="12240-313">U maakt tijdens het instellen van het projectcontract een factureringsregel om het managementtarief van 10% toe te voegen aan de adviesuren die voor het project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="12240-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="12240-314">Wanneer u een factuur voor de klant maakt, factureert u een managementtarief van 10% plus de kosten van de adviesuren.</span><span class="sxs-lookup"><span data-stu-id="12240-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="12240-315">Wanneer de drie consultants in totaal bijvoorbeeld 200 uur aan het project hebben gewerkt, wordt er een factuur gemaakt voor het bedrag van 22.000 op basis van de volgende berekening:</span><span class="sxs-lookup"><span data-stu-id="12240-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="12240-316">200 uur tegen een tarief van 100 per uur = 20.000</span><span class="sxs-lookup"><span data-stu-id="12240-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="12240-317">10 procent managementtarief = 2.000</span><span class="sxs-lookup"><span data-stu-id="12240-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="12240-318">Totaal factuurbedrag = 22.000</span><span class="sxs-lookup"><span data-stu-id="12240-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="12240-319">Als de kosten voor een klant belastbaar zijn, en u selecteert een btw-groep in het projectcontract, wordt de btw-groep automatisch ingevoerd in een factureringsregel voor kosten.</span><span class="sxs-lookup"><span data-stu-id="12240-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="12240-320">Voorbeeld: Een factureringsregel voor de waarde van de tijd en de materialen maken</span><span class="sxs-lookup"><span data-stu-id="12240-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="12240-321">Uw organisatie, een bedrijf dat zich bezighoudt met diensten op het gebied van softwareadvies, is overeengekomen dat u voorziet in vijf technische consultants die de komende zes maanden voor een klant aan een softwareontwikkelingsproject zullen werken.</span><span class="sxs-lookup"><span data-stu-id="12240-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="12240-322">U komt met de klant overeen dat deze 150 betaalt voor elk adviesuur plus de kosten van kantoorbenodigdheden.</span><span class="sxs-lookup"><span data-stu-id="12240-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="12240-323">Uw organisatie stuurt aan het einde van elke maand een factuur aan de klant.</span><span class="sxs-lookup"><span data-stu-id="12240-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="12240-324">Wanneer u het projectcontract instelt, gaat u ermee akkoord dat u de klant maandelijks de tijd en het materiaal voor het project in rekening brengt.</span><span class="sxs-lookup"><span data-stu-id="12240-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="12240-325">U maakt een factureringsregel die de volgende informatie bevat:</span><span class="sxs-lookup"><span data-stu-id="12240-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="12240-326">De contractperiode is zes maanden.</span><span class="sxs-lookup"><span data-stu-id="12240-326">The contract period is six months.</span></span>
-   <span data-ttu-id="12240-327">De adviestijd wordt berekend op basis van een tarief van 150 per uur.</span><span class="sxs-lookup"><span data-stu-id="12240-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="12240-328">Kantoorbenodigdheden worden gefactureerd tegen de kosten, maar de totale kosten voor het project mogen niet hoger zijn dan 10.000.</span><span class="sxs-lookup"><span data-stu-id="12240-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="12240-329">U maakt gedurende het project aan het einde van elke kalendermaand een klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="12240-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="12240-330">Tijdens de eerste maand worden er door de adviseurs in totaal 800 uren voor het project geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="12240-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="12240-331">De kosten van kantoorbenodigdheden die voor het project in rekening worden gebracht, zijn 2000.</span><span class="sxs-lookup"><span data-stu-id="12240-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="12240-332">Daarom maakt u aan het eind van de maand een factuur voor 122.000, berekend als 800 uur tegen 150 per uur, plus 2000 voor kantoorbenodigdheden.</span><span class="sxs-lookup"><span data-stu-id="12240-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



