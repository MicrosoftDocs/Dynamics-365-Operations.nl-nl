---
title: Ondersteunde standaarden voor elektronische facturering in Europa
description: In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition in de Europese regio.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.1, Operations, Core
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: 
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c944fd20273623ce3f7d03a24546addbe987084e
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="a4642-103">Ondersteunde standaarden voor elektronische facturering in Europa</span><span class="sxs-lookup"><span data-stu-id="a4642-103">Supported standards for electronic invoicing in Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a4642-104">In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.</span><span class="sxs-lookup"><span data-stu-id="a4642-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="a4642-105">Implementatie en goedkeuring van elektronische facturering binnen de Europese Unie is gereguleerd in [Richtlijn 2010/45/EU van de Raad](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), die geldt in alle EU-lidstaten.</span><span class="sxs-lookup"><span data-stu-id="a4642-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="a4642-106">Bedrijven die elektronisch factureren willen gebruiken, moeten verkooporderfacturen, vrije-tekstfacturen, projectfacturen, verkooporder-creditnota's en projectfactuur-creditnota's indienen als een .XML-bestand aan de overheid of andere handelspartijen die elektronische facturering toestaan.</span><span class="sxs-lookup"><span data-stu-id="a4642-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="a4642-107">Deze .XML-bestanden moeten voldoen aan bepaalde standaarden.</span><span class="sxs-lookup"><span data-stu-id="a4642-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="a4642-108">De landspecifieke vereisten en hun implementatie kunnen verschillen binnen EU-lidstaten, maar gebruiken gewoonlijk Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in verschillende versies met aanpassingen, en [PEPPOL](http://www.peppol.eu)- specificaties en toegangspunten voor validatie en vervoer.</span><span class="sxs-lookup"><span data-stu-id="a4642-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](http://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="a4642-109">Het belangrijkste voordeel van UBL is dat zakelijke documenten kunnen worden gestandaardiseerd voor verschillende doeleinden.</span><span class="sxs-lookup"><span data-stu-id="a4642-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="a4642-110">Omdat UBL een flexibele, internationale standaard is die ondersteuning biedt voor veel zakelijke vereisten, kunnen deze zakelijke documenten worden uitgewisseld over de landsgrenzen.</span><span class="sxs-lookup"><span data-stu-id="a4642-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a><span data-ttu-id="a4642-111">Welke indelingen voor elektronische facturen zijn momenteel beschikbaar in Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="a4642-111">What electronic invoice formats are currently available in Finance and Operations?</span></span>

<span data-ttu-id="a4642-112">De volgende landspecifieke indelingen van elektronische facturen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="a4642-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="a4642-113">OIOUBL v.2.02 voor Denemarken</span><span class="sxs-lookup"><span data-stu-id="a4642-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="a4642-114">EHF v.2.0.8 voor Noorwegen</span><span class="sxs-lookup"><span data-stu-id="a4642-114">EHF v.2.0.8 for Norway</span></span>
-   <span data-ttu-id="a4642-115">PEPPOL BIS v.2 voor Oostenrijk, Frankrijk en België</span><span class="sxs-lookup"><span data-stu-id="a4642-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="a4642-116">UBL-OHNL 1.9 voor Nederland</span><span class="sxs-lookup"><span data-stu-id="a4642-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="a4642-117">FacturaE v.3.2.1 voor Spanje</span><span class="sxs-lookup"><span data-stu-id="a4642-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="a4642-118">FatturaPA v.1.2 voor Italië</span><span class="sxs-lookup"><span data-stu-id="a4642-118">FatturaPA v.1.2 for Italy</span></span>

<span data-ttu-id="a4642-119">Elektronische facturering is gebaseerd op [elektronische rapportage](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).</span><span class="sxs-lookup"><span data-stu-id="a4642-119">Electronic invoicing is based on [electronic reporting](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).</span></span> <span data-ttu-id="a4642-120">Er is een gegevensmodel met een **klantfactuurmodel** en een aantal landspecifieke configuraties voor elektronische rapportopmaken voor Oostenrijk (AT), Denemarken (DK), Italië (IT), Noorwegen (NO), Spanje (ES), Frankrijk (FR), België (BE) en Nederland (NL).</span><span class="sxs-lookup"><span data-stu-id="a4642-120">There is a **Customer invoice model** data model and a number of country-specific electronic reporting format configurations created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), and the Netherlands (NL).</span></span>

-   <span data-ttu-id="a4642-121">OIOUBL Verkoopfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="a4642-121">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a4642-122">OIOUBL Verkoopcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="a4642-122">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a4642-123">OIOUBL Projectfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="a4642-123">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a4642-124">OIOUBL Projectcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="a4642-124">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a4642-125">UBL Verkoopfactuur FR</span><span class="sxs-lookup"><span data-stu-id="a4642-125">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="a4642-126">UBL Verkoopcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="a4642-126">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="a4642-127">UBL Projectfactuur FR</span><span class="sxs-lookup"><span data-stu-id="a4642-127">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="a4642-128">UBL Projectcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="a4642-128">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="a4642-129">UBL Verkoopfactuur BE</span><span class="sxs-lookup"><span data-stu-id="a4642-129">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="a4642-130">UBL Verkoopcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="a4642-130">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="a4642-131">UBL Projectfactuur BE</span><span class="sxs-lookup"><span data-stu-id="a4642-131">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="a4642-132">UBL Projectcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="a4642-132">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="a4642-133">UBL Verkoopfactuur NL</span><span class="sxs-lookup"><span data-stu-id="a4642-133">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="a4642-134">UBL Verkoopcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="a4642-134">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="a4642-135">UBL Projectfactuur NL</span><span class="sxs-lookup"><span data-stu-id="a4642-135">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="a4642-136">UBL Projectcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="a4642-136">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="a4642-137">Verkoopfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="a4642-137">Sales invoice (ES)</span></span>
-   <span data-ttu-id="a4642-138">Verkoopfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="a4642-138">Sales invoice (IT)</span></span>
-   <span data-ttu-id="a4642-139">Projectfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="a4642-139">Project invoice (ES)</span></span>
-   <span data-ttu-id="a4642-140">Projectfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="a4642-140">Project invoice (IT)</span></span>

<span data-ttu-id="a4642-141">De elektronische facturen en creditnota's die u genereert, bevatten vereiste gegevens zoals een EAN-nummer (European Article Numbering), de contactpersoon, het dimensierekeningnummer en adresgegevens van de klant.</span><span class="sxs-lookup"><span data-stu-id="a4642-141">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="a4642-142">Er worden validatieregels worden toegepast wanneer facturen worden gegenereerd om te controleren of de juiste gegevens zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="a4642-142">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="a4642-143">De set met vereiste gegevens kan verschillen van land tot land.</span><span class="sxs-lookup"><span data-stu-id="a4642-143">The set of required information may differ from country to country.</span></span> <span data-ttu-id="a4642-144">Vanwege de vereiste en de ondersteunde landen en indelingen kunnen veranderen, moet u altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.</span><span class="sxs-lookup"><span data-stu-id="a4642-144">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="a4642-145">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="a4642-145">Additional information</span></span>
<span data-ttu-id="a4642-146">Voor meer informatie over het instellen van elektronische facturen, kunt u de volgende [Taakbegeleidingen](/dynamics365/unified-operations/dev-itpro/get-started/help-overview#task-guides) afspelen in het Help-venster:</span><span class="sxs-lookup"><span data-stu-id="a4642-146">For more details about how to set up electronic invoices, you can play the following [Task guides](/dynamics365/unified-operations/dev-itpro/get-started/help-overview#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="a4642-147">OIOUBL elektronische facturen instellen</span><span class="sxs-lookup"><span data-stu-id="a4642-147">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="a4642-148">OIOUBL elektronische factureringsconfiguraties importeren</span><span class="sxs-lookup"><span data-stu-id="a4642-148">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="a4642-149">Klantrekeningen instellen voor elektronische OIOUBL-facturering</span><span class="sxs-lookup"><span data-stu-id="a4642-149">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="a4642-150">Hoewel deze Taakbegeleidingen zijn gemaakt voor de specifieke Deense e-factuurindeling *OIOUBL*, zijn ze met kleine afwijkingen van toepassing op andere ondersteunde landen.</span><span class="sxs-lookup"><span data-stu-id="a4642-150">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>

