---
title: Ondersteunde standaarden voor elektronische facturering in Europa
description: In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.
author: mrolecki
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3ed98c268af841b1625f547c79f271f3e3a81b74
ms.sourcegitcommit: 3d16522c00ba2d30aa43befbf1b7b3eaad377325
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4592464"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="2a187-103">Ondersteunde standaarden voor elektronische facturering in Europa</span><span class="sxs-lookup"><span data-stu-id="2a187-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a187-104">In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.</span><span class="sxs-lookup"><span data-stu-id="2a187-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="2a187-105">Implementatie en goedkeuring van elektronische facturering binnen de Europese Unie is gereguleerd in [Richtlijn 2010/45/EU van de Raad](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), die geldt in alle EU-lidstaten.</span><span class="sxs-lookup"><span data-stu-id="2a187-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="2a187-106">Bedrijven die elektronisch factureren willen gebruiken, moeten verkooporderfacturen, vrije-tekstfacturen, projectfacturen, verkooporder-creditnota's en projectfactuur-creditnota's indienen als een .XML-bestand aan de overheid of andere handelspartijen die elektronische facturering toestaan.</span><span class="sxs-lookup"><span data-stu-id="2a187-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="2a187-107">Deze .XML-bestanden moeten voldoen aan bepaalde standaarden.</span><span class="sxs-lookup"><span data-stu-id="2a187-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="2a187-108">De landspecifieke vereisten en hun implementatie kunnen verschillen binnen EU-lidstaten, maar gebruiken gewoonlijk Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in verschillende versies met aanpassingen, en [PEPPOL](https://www.peppol.eu)- specificaties en toegangspunten voor validatie en vervoer.</span><span class="sxs-lookup"><span data-stu-id="2a187-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="2a187-109">Het belangrijkste voordeel van UBL is dat zakelijke documenten kunnen worden gestandaardiseerd voor verschillende doeleinden.</span><span class="sxs-lookup"><span data-stu-id="2a187-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="2a187-110">Omdat UBL een flexibele, internationale standaard is die ondersteuning biedt voor veel zakelijke vereisten, kunnen deze zakelijke documenten worden uitgewisseld over de landsgrenzen.</span><span class="sxs-lookup"><span data-stu-id="2a187-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="2a187-111">Elektronische factuurindelingen die momenteel beschikbaar zijn in Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="2a187-111">Electronic invoice formats currently available in Dynamics 365 Finance</span></span>

<span data-ttu-id="2a187-112">De volgende landspecifieke indelingen van elektronische facturen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="2a187-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="2a187-113">OIOUBL v.2.02 voor Denemarken</span><span class="sxs-lookup"><span data-stu-id="2a187-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="2a187-114">EHF v. 3.0 voor Noorwegen</span><span class="sxs-lookup"><span data-stu-id="2a187-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="2a187-115">PEPPOL BIS v.2 voor Oostenrijk, Frankrijk en België</span><span class="sxs-lookup"><span data-stu-id="2a187-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="2a187-116">UBL-OHNL 1.9 voor Nederland</span><span class="sxs-lookup"><span data-stu-id="2a187-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="2a187-117">FacturaE v.3.2.1 voor Spanje</span><span class="sxs-lookup"><span data-stu-id="2a187-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="2a187-118">FatturaPA v.1.2 voor Italië</span><span class="sxs-lookup"><span data-stu-id="2a187-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="2a187-119">xRechnung v. 1.2 voor Duitsland</span><span class="sxs-lookup"><span data-stu-id="2a187-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="2a187-120">Open PEPPOL BIS Billing v.3.0 voor de Europese Unie</span><span class="sxs-lookup"><span data-stu-id="2a187-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>
-   <span data-ttu-id="2a187-121">Specifieke Estse indelingsversie 1.2</span><span class="sxs-lookup"><span data-stu-id="2a187-121">Estonian specific format version 1.2</span></span>
-   <span data-ttu-id="2a187-122">Finvoice 3.0 voor Finland</span><span class="sxs-lookup"><span data-stu-id="2a187-122">Finvoice 3.0 for Finland</span></span>

<span data-ttu-id="2a187-123">Elektronische facturering is gebaseerd op [ER (Elektronische rapportage)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="2a187-123">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="2a187-124">Een gegevensmodel **Factuurmodel**, factuurmodeltoewijzing en verschillende land-/regiospecifieke ER-indelingsconfiguraties zijn gemaakt voor de volgende landen/regio's:</span><span class="sxs-lookup"><span data-stu-id="2a187-124">An **Invoice model** data model, invoice model mapping, and several country/region-specific ER format configurations have been created for the following countries/regions:</span></span> 

- <span data-ttu-id="2a187-125">Oostenrijk (AT)</span><span class="sxs-lookup"><span data-stu-id="2a187-125">Austria (AT)</span></span>
- <span data-ttu-id="2a187-126">Denemarken (DK)</span><span class="sxs-lookup"><span data-stu-id="2a187-126">Denmark (DK)</span></span>
- <span data-ttu-id="2a187-127">Italië (IT)</span><span class="sxs-lookup"><span data-stu-id="2a187-127">Italy (IT)</span></span>
- <span data-ttu-id="2a187-128">Noorwegen (NO)</span><span class="sxs-lookup"><span data-stu-id="2a187-128">Norway (NO)</span></span>
- <span data-ttu-id="2a187-129">Spanje (ES)</span><span class="sxs-lookup"><span data-stu-id="2a187-129">Spain (ES)</span></span>
- <span data-ttu-id="2a187-130">Frankrijk (FR)</span><span class="sxs-lookup"><span data-stu-id="2a187-130">France (FR)</span></span>
- <span data-ttu-id="2a187-131">België (BE)</span><span class="sxs-lookup"><span data-stu-id="2a187-131">Belgium (BE)</span></span>
- <span data-ttu-id="2a187-132">Nederland (NL)</span><span class="sxs-lookup"><span data-stu-id="2a187-132">The Netherlands (NL)</span></span>
- <span data-ttu-id="2a187-133">Duitsland (DE)</span><span class="sxs-lookup"><span data-stu-id="2a187-133">Germany (DE)</span></span>
- <span data-ttu-id="2a187-134">Estland (EE)</span><span class="sxs-lookup"><span data-stu-id="2a187-134">Estonia (EE)</span></span>
- <span data-ttu-id="2a187-135">Finland (FI)</span><span class="sxs-lookup"><span data-stu-id="2a187-135">Finland (FI)</span></span>
- <span data-ttu-id="2a187-136">De Europese Unie (EU)</span><span class="sxs-lookup"><span data-stu-id="2a187-136">The European Union (EU)</span></span>

<span data-ttu-id="2a187-137">Het gegevensmodel **Factuurmodel**, factuurmodeltoewijzing en land/regio-specifieke ER-indelingsconfiguraties zijn:</span><span class="sxs-lookup"><span data-stu-id="2a187-137">The **Invoice model** data model, invoice model mapping, and country/region-specific ER format configurations include:</span></span>

-   <span data-ttu-id="2a187-138">OIOUBL Verkoopfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="2a187-138">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="2a187-139">OIOUBL Verkoopcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="2a187-139">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="2a187-140">OIOUBL Projectfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="2a187-140">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="2a187-141">OIOUBL Projectcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="2a187-141">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="2a187-142">UBL Verkoopfactuur FR</span><span class="sxs-lookup"><span data-stu-id="2a187-142">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="2a187-143">UBL Verkoopcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="2a187-143">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="2a187-144">UBL Projectfactuur FR</span><span class="sxs-lookup"><span data-stu-id="2a187-144">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="2a187-145">UBL Projectcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="2a187-145">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="2a187-146">UBL Verkoopfactuur BE</span><span class="sxs-lookup"><span data-stu-id="2a187-146">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="2a187-147">UBL Verkoopcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="2a187-147">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="2a187-148">UBL Projectfactuur BE</span><span class="sxs-lookup"><span data-stu-id="2a187-148">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="2a187-149">UBL Projectcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="2a187-149">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="2a187-150">UBL Verkoopfactuur NL</span><span class="sxs-lookup"><span data-stu-id="2a187-150">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="2a187-151">UBL Verkoopcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="2a187-151">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="2a187-152">UBL Projectfactuur NL</span><span class="sxs-lookup"><span data-stu-id="2a187-152">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="2a187-153">UBL Projectcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="2a187-153">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="2a187-154">Verkoopfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="2a187-154">Sales invoice (ES)</span></span>
-   <span data-ttu-id="2a187-155">Verkoopfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="2a187-155">Sales invoice (IT)</span></span>
-   <span data-ttu-id="2a187-156">Projectfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="2a187-156">Project invoice (ES)</span></span>
-   <span data-ttu-id="2a187-157">Projectfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="2a187-157">Project invoice (IT)</span></span>
-   <span data-ttu-id="2a187-158">Verkoopfactuur DE</span><span class="sxs-lookup"><span data-stu-id="2a187-158">Sales Invoice DE</span></span>
-   <span data-ttu-id="2a187-159">Projectfactuur DE</span><span class="sxs-lookup"><span data-stu-id="2a187-159">Project Invoice DE</span></span>
-   <span data-ttu-id="2a187-160">Peppol-verkoopfactuur - voor EU</span><span class="sxs-lookup"><span data-stu-id="2a187-160">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="2a187-161">Peppol-verkoopcreditnota - voor EU</span><span class="sxs-lookup"><span data-stu-id="2a187-161">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="2a187-162">Peppol-projectfactuur - voor EU</span><span class="sxs-lookup"><span data-stu-id="2a187-162">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="2a187-163">Peppol-projectcreditnota - voor EU</span><span class="sxs-lookup"><span data-stu-id="2a187-163">Peppol Project Credit Note - for EU</span></span>
-   <span data-ttu-id="2a187-164">Verkoopfactuur (EE)</span><span class="sxs-lookup"><span data-stu-id="2a187-164">Sales invoice (EE)</span></span>
-   <span data-ttu-id="2a187-165">Projectfactuur (EE)</span><span class="sxs-lookup"><span data-stu-id="2a187-165">Project invoice (EE)</span></span>
-   <span data-ttu-id="2a187-166">Verkoopfactuur (FI)</span><span class="sxs-lookup"><span data-stu-id="2a187-166">Sales invoice (FI)</span></span>
-   <span data-ttu-id="2a187-167">Projectfactuur (FI)</span><span class="sxs-lookup"><span data-stu-id="2a187-167">Project invoice (FI)</span></span>

<span data-ttu-id="2a187-168">De elektronische facturen en creditnota's die u genereert, bevatten vereiste gegevens zoals een EAN-nummer (European Article Numbering), de contactpersoon, het dimensierekeningnummer en adresgegevens van de klant.</span><span class="sxs-lookup"><span data-stu-id="2a187-168">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="2a187-169">Er worden validatieregels worden toegepast wanneer facturen worden gegenereerd om te controleren of de juiste gegevens zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="2a187-169">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="2a187-170">De set met vereiste gegevens kan verschillen van land tot land.</span><span class="sxs-lookup"><span data-stu-id="2a187-170">The set of required information may differ from country to country.</span></span> <span data-ttu-id="2a187-171">Omdat de vereiste en de ondersteunde landen en indelingen kunnen veranderen, moet u altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.</span><span class="sxs-lookup"><span data-stu-id="2a187-171">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle Services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="electronic-invoice-configuration"></a><span data-ttu-id="2a187-172">Een elektronische factuur configureren</span><span class="sxs-lookup"><span data-stu-id="2a187-172">Electronic invoice configuration</span></span>
<span data-ttu-id="2a187-173">De instellingen en details van elektronische facturen zijn afhankelijk van het land of de regio waarvoor deze zijn geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="2a187-173">The setup and specifics of electronic invoices depend on the country/region that it's implemented for.</span></span> <span data-ttu-id="2a187-174">Zie de verwante landspecifieke onderwerpen voor meer informatie over het instellen en gebruiken van elektronische facturen voor klanten:</span><span class="sxs-lookup"><span data-stu-id="2a187-174">For more information about how to set up and use customer electronic invoices, see the related country-specific topics:</span></span>

- [<span data-ttu-id="2a187-175">Italië</span><span class="sxs-lookup"><span data-stu-id="2a187-175">Italy</span></span>](emea-ita-e-invoices.md)
- [<span data-ttu-id="2a187-176">Noorwegen</span><span class="sxs-lookup"><span data-stu-id="2a187-176">Norway</span></span>](emea-nor-e-invoices.md)
- [<span data-ttu-id="2a187-177">Duitsland</span><span class="sxs-lookup"><span data-stu-id="2a187-177">Germany</span></span>](emea-deu-e-invoices.md)
- [<span data-ttu-id="2a187-178">Finland</span><span class="sxs-lookup"><span data-stu-id="2a187-178">Finland</span></span>](https://support.microsoft.com/help/4559937)
- [<span data-ttu-id="2a187-179">Estland</span><span class="sxs-lookup"><span data-stu-id="2a187-179">Estonia</span></span>](https://support.microsoft.com/help/4552679)
- [<span data-ttu-id="2a187-180">PEPPOL</span><span class="sxs-lookup"><span data-stu-id="2a187-180">PEPPOL</span></span>](https://support.microsoft.com/help/4490320)

## <a name="additional-resources"></a><span data-ttu-id="2a187-181">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="2a187-181">Additional resources</span></span>
<span data-ttu-id="2a187-182">Voor meer informatie over het instellen van elektronische facturen, kunt u de volgende [Taakbegeleidingen](../../fin-and-ops/get-started/help-overview.md#task-guides) afspelen in het Help-venster:</span><span class="sxs-lookup"><span data-stu-id="2a187-182">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="2a187-183">OIOUBL elektronische facturen instellen</span><span class="sxs-lookup"><span data-stu-id="2a187-183">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="2a187-184">OIOUBL elektronische factureringsconfiguraties importeren</span><span class="sxs-lookup"><span data-stu-id="2a187-184">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="2a187-185">Klantrekeningen instellen voor elektronische OIOUBL-facturering</span><span class="sxs-lookup"><span data-stu-id="2a187-185">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="2a187-186">Hoewel deze taakbegeleidingen zijn gemaakt voor de specifieke Deense e-factuurindeling *OIOUBL*, zijn ze met kleine afwijkingen van toepassing op andere ondersteunde landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="2a187-186">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries/regions with minor deviations.</span></span>
