---
title: Ondersteunde standaarden voor elektronische facturering in Europa
description: In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
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
ms.openlocfilehash: 2fb188498705dcbad841645ced43e6a1715cbbd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915161"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="1494f-103">Ondersteunde standaarden voor elektronische facturering in Europa</span><span class="sxs-lookup"><span data-stu-id="1494f-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1494f-104">In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.</span><span class="sxs-lookup"><span data-stu-id="1494f-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="1494f-105">Implementatie en goedkeuring van elektronische facturering binnen de Europese Unie is gereguleerd in [Richtlijn 2010/45/EU van de Raad](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), die geldt in alle EU-lidstaten.</span><span class="sxs-lookup"><span data-stu-id="1494f-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="1494f-106">Bedrijven die elektronisch factureren willen gebruiken, moeten verkooporderfacturen, vrije-tekstfacturen, projectfacturen, verkooporder-creditnota's en projectfactuur-creditnota's indienen als een .XML-bestand aan de overheid of andere handelspartijen die elektronische facturering toestaan.</span><span class="sxs-lookup"><span data-stu-id="1494f-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="1494f-107">Deze .XML-bestanden moeten voldoen aan bepaalde standaarden.</span><span class="sxs-lookup"><span data-stu-id="1494f-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="1494f-108">De landspecifieke vereisten en hun implementatie kunnen verschillen binnen EU-lidstaten, maar gebruiken gewoonlijk Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in verschillende versies met aanpassingen, en [PEPPOL](https://www.peppol.eu)- specificaties en toegangspunten voor validatie en vervoer.</span><span class="sxs-lookup"><span data-stu-id="1494f-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="1494f-109">Het belangrijkste voordeel van UBL is dat zakelijke documenten kunnen worden gestandaardiseerd voor verschillende doeleinden.</span><span class="sxs-lookup"><span data-stu-id="1494f-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="1494f-110">Omdat UBL een flexibele, internationale standaard is die ondersteuning biedt voor veel zakelijke vereisten, kunnen deze zakelijke documenten worden uitgewisseld over de landsgrenzen.</span><span class="sxs-lookup"><span data-stu-id="1494f-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="1494f-111">Welke elektronische factuurindelingen zijn momenteel beschikbaar in Dynamics 365 Finance?</span><span class="sxs-lookup"><span data-stu-id="1494f-111">What electronic invoice formats are currently available in Dynamics 365 Finance?</span></span>

<span data-ttu-id="1494f-112">De volgende landspecifieke indelingen van elektronische facturen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="1494f-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="1494f-113">OIOUBL v.2.02 voor Denemarken</span><span class="sxs-lookup"><span data-stu-id="1494f-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="1494f-114">EHF v. 3.0 voor Noorwegen</span><span class="sxs-lookup"><span data-stu-id="1494f-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="1494f-115">PEPPOL BIS v.2 voor Oostenrijk, Frankrijk en België</span><span class="sxs-lookup"><span data-stu-id="1494f-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="1494f-116">UBL-OHNL 1.9 voor Nederland</span><span class="sxs-lookup"><span data-stu-id="1494f-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="1494f-117">FacturaE v.3.2.1 voor Spanje</span><span class="sxs-lookup"><span data-stu-id="1494f-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="1494f-118">FatturaPA v.1.2 voor Italië</span><span class="sxs-lookup"><span data-stu-id="1494f-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="1494f-119">xRechnung v. 1.2 voor Duitsland</span><span class="sxs-lookup"><span data-stu-id="1494f-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="1494f-120">Open PEPPOL BIS Billing v.3.0 voor de Europese Unie</span><span class="sxs-lookup"><span data-stu-id="1494f-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>

<span data-ttu-id="1494f-121">Elektronische facturering is gebaseerd op [ER (Elektronische rapportage)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="1494f-121">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="1494f-122">Er is een gegevensmodel met een **klantfactuurmodel** en een aantal land-/regiospecifieke configuraties voor ER-indelingen voor Oostenrijk (AT), Denemarken (DK), Italië (IT), Noorwegen (NO), Spanje (ES), Frankrijk (FR), België (BE) en Nederland (NL).</span><span class="sxs-lookup"><span data-stu-id="1494f-122">A **Customer invoice model** data model and several country/region-specific ER format configurations have been created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), the Netherlands (NL), Germany (DE), and the European Union (EU).</span></span>

-   <span data-ttu-id="1494f-123">OIOUBL Verkoopfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="1494f-123">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="1494f-124">OIOUBL Verkoopcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="1494f-124">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="1494f-125">OIOUBL Projectfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="1494f-125">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="1494f-126">OIOUBL Projectcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="1494f-126">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="1494f-127">UBL Verkoopfactuur FR</span><span class="sxs-lookup"><span data-stu-id="1494f-127">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="1494f-128">UBL Verkoopcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="1494f-128">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="1494f-129">UBL Projectfactuur FR</span><span class="sxs-lookup"><span data-stu-id="1494f-129">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="1494f-130">UBL Projectcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="1494f-130">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="1494f-131">UBL Verkoopfactuur BE</span><span class="sxs-lookup"><span data-stu-id="1494f-131">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="1494f-132">UBL Verkoopcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="1494f-132">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="1494f-133">UBL Projectfactuur BE</span><span class="sxs-lookup"><span data-stu-id="1494f-133">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="1494f-134">UBL Projectcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="1494f-134">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="1494f-135">UBL Verkoopfactuur NL</span><span class="sxs-lookup"><span data-stu-id="1494f-135">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="1494f-136">UBL Verkoopcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="1494f-136">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="1494f-137">UBL Projectfactuur NL</span><span class="sxs-lookup"><span data-stu-id="1494f-137">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="1494f-138">UBL Projectcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="1494f-138">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="1494f-139">Verkoopfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="1494f-139">Sales invoice (ES)</span></span>
-   <span data-ttu-id="1494f-140">Verkoopfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="1494f-140">Sales invoice (IT)</span></span>
-   <span data-ttu-id="1494f-141">Projectfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="1494f-141">Project invoice (ES)</span></span>
-   <span data-ttu-id="1494f-142">Projectfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="1494f-142">Project invoice (IT)</span></span>
-   <span data-ttu-id="1494f-143">Verkoopfactuur DE</span><span class="sxs-lookup"><span data-stu-id="1494f-143">Sales Invoice DE</span></span>
-   <span data-ttu-id="1494f-144">Projectfactuur DE</span><span class="sxs-lookup"><span data-stu-id="1494f-144">Project Invoice DE</span></span>
-   <span data-ttu-id="1494f-145">Peppol-verkoopfactuur - voor EU</span><span class="sxs-lookup"><span data-stu-id="1494f-145">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="1494f-146">Peppol-verkoopcreditnota - voor EU</span><span class="sxs-lookup"><span data-stu-id="1494f-146">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="1494f-147">Peppol-projectfactuur - voor EU</span><span class="sxs-lookup"><span data-stu-id="1494f-147">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="1494f-148">Peppol-projectcreditnota - voor EU</span><span class="sxs-lookup"><span data-stu-id="1494f-148">Peppol Project Credit Note - for EU</span></span>

<span data-ttu-id="1494f-149">De elektronische facturen en creditnota's die u genereert, bevatten vereiste gegevens zoals een EAN-nummer (European Article Numbering), de contactpersoon, het dimensierekeningnummer en adresgegevens van de klant.</span><span class="sxs-lookup"><span data-stu-id="1494f-149">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="1494f-150">Er worden validatieregels worden toegepast wanneer facturen worden gegenereerd om te controleren of de juiste gegevens zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="1494f-150">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="1494f-151">De set met vereiste gegevens kan verschillen van land tot land.</span><span class="sxs-lookup"><span data-stu-id="1494f-151">The set of required information may differ from country to country.</span></span> <span data-ttu-id="1494f-152">Omdat de vereiste en de ondersteunde landen en indelingen kunnen veranderen, moet u altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.</span><span class="sxs-lookup"><span data-stu-id="1494f-152">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="1494f-153">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="1494f-153">Additional information</span></span>
<span data-ttu-id="1494f-154">Voor meer informatie over het instellen van elektronische facturen, kunt u de volgende [Taakbegeleidingen](../../fin-and-ops/get-started/help-overview.md#task-guides) afspelen in het Help-venster:</span><span class="sxs-lookup"><span data-stu-id="1494f-154">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="1494f-155">OIOUBL elektronische facturen instellen</span><span class="sxs-lookup"><span data-stu-id="1494f-155">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="1494f-156">OIOUBL elektronische factureringsconfiguraties importeren</span><span class="sxs-lookup"><span data-stu-id="1494f-156">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="1494f-157">Klantrekeningen instellen voor elektronische OIOUBL-facturering</span><span class="sxs-lookup"><span data-stu-id="1494f-157">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="1494f-158">Hoewel deze Taakbegeleidingen zijn gemaakt voor de specifieke Deense e-factuurindeling *OIOUBL*, zijn ze met kleine afwijkingen van toepassing op andere ondersteunde landen.</span><span class="sxs-lookup"><span data-stu-id="1494f-158">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>
