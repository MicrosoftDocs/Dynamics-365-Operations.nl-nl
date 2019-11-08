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
ms.openlocfilehash: c1d1ec695626404389dec2b07dd6e34358cd2d5a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176151"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="37991-103">Ondersteunde standaarden voor elektronische facturering in Europa</span><span class="sxs-lookup"><span data-stu-id="37991-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37991-104">In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.</span><span class="sxs-lookup"><span data-stu-id="37991-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="37991-105">Implementatie en goedkeuring van elektronische facturering binnen de Europese Unie is gereguleerd in [Richtlijn 2010/45/EU van de Raad](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), die geldt in alle EU-lidstaten.</span><span class="sxs-lookup"><span data-stu-id="37991-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="37991-106">Bedrijven die elektronisch factureren willen gebruiken, moeten verkooporderfacturen, vrije-tekstfacturen, projectfacturen, verkooporder-creditnota's en projectfactuur-creditnota's indienen als een .XML-bestand aan de overheid of andere handelspartijen die elektronische facturering toestaan.</span><span class="sxs-lookup"><span data-stu-id="37991-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="37991-107">Deze .XML-bestanden moeten voldoen aan bepaalde standaarden.</span><span class="sxs-lookup"><span data-stu-id="37991-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="37991-108">De landspecifieke vereisten en hun implementatie kunnen verschillen binnen EU-lidstaten, maar gebruiken gewoonlijk Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in verschillende versies met aanpassingen, en [PEPPOL](https://www.peppol.eu)- specificaties en toegangspunten voor validatie en vervoer.</span><span class="sxs-lookup"><span data-stu-id="37991-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="37991-109">Het belangrijkste voordeel van UBL is dat zakelijke documenten kunnen worden gestandaardiseerd voor verschillende doeleinden.</span><span class="sxs-lookup"><span data-stu-id="37991-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="37991-110">Omdat UBL een flexibele, internationale standaard is die ondersteuning biedt voor veel zakelijke vereisten, kunnen deze zakelijke documenten worden uitgewisseld over de landsgrenzen.</span><span class="sxs-lookup"><span data-stu-id="37991-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="37991-111">Welke elektronische factuurindelingen zijn momenteel beschikbaar in Dynamics 365 Finance?</span><span class="sxs-lookup"><span data-stu-id="37991-111">What electronic invoice formats are currently available in Dynamics 365 Finance?</span></span>

<span data-ttu-id="37991-112">De volgende landspecifieke indelingen van elektronische facturen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="37991-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="37991-113">OIOUBL v.2.02 voor Denemarken</span><span class="sxs-lookup"><span data-stu-id="37991-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="37991-114">EHF v.2.0.8 voor Noorwegen</span><span class="sxs-lookup"><span data-stu-id="37991-114">EHF v.2.0.8 for Norway</span></span>
-   <span data-ttu-id="37991-115">PEPPOL BIS v.2 voor Oostenrijk, Frankrijk en België</span><span class="sxs-lookup"><span data-stu-id="37991-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="37991-116">UBL-OHNL 1.9 voor Nederland</span><span class="sxs-lookup"><span data-stu-id="37991-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="37991-117">FacturaE v.3.2.1 voor Spanje</span><span class="sxs-lookup"><span data-stu-id="37991-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="37991-118">FatturaPA v.1.2 voor Italië</span><span class="sxs-lookup"><span data-stu-id="37991-118">FatturaPA v.1.2 for Italy</span></span>

<span data-ttu-id="37991-119">Elektronische facturering is gebaseerd op [elektronische rapportage](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="37991-119">Electronic invoicing is based on [electronic reporting](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="37991-120">Er is een gegevensmodel met een **klantfactuurmodel** en een aantal landspecifieke configuraties voor elektronische rapportopmaken voor Oostenrijk (AT), Denemarken (DK), Italië (IT), Noorwegen (NO), Spanje (ES), Frankrijk (FR), België (BE) en Nederland (NL).</span><span class="sxs-lookup"><span data-stu-id="37991-120">There is a **Customer invoice model** data model and a number of country-specific electronic reporting format configurations created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), and the Netherlands (NL).</span></span>

-   <span data-ttu-id="37991-121">OIOUBL Verkoopfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="37991-121">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="37991-122">OIOUBL Verkoopcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="37991-122">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="37991-123">OIOUBL Projectfactuur - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="37991-123">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="37991-124">OIOUBL Projectcreditnota - voor AT, DK en NO</span><span class="sxs-lookup"><span data-stu-id="37991-124">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="37991-125">UBL Verkoopfactuur FR</span><span class="sxs-lookup"><span data-stu-id="37991-125">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="37991-126">UBL Verkoopcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="37991-126">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="37991-127">UBL Projectfactuur FR</span><span class="sxs-lookup"><span data-stu-id="37991-127">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="37991-128">UBL Projectcreditnota FR</span><span class="sxs-lookup"><span data-stu-id="37991-128">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="37991-129">UBL Verkoopfactuur BE</span><span class="sxs-lookup"><span data-stu-id="37991-129">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="37991-130">UBL Verkoopcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="37991-130">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="37991-131">UBL Projectfactuur BE</span><span class="sxs-lookup"><span data-stu-id="37991-131">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="37991-132">UBL Projectcreditnota BE</span><span class="sxs-lookup"><span data-stu-id="37991-132">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="37991-133">UBL Verkoopfactuur NL</span><span class="sxs-lookup"><span data-stu-id="37991-133">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="37991-134">UBL Verkoopcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="37991-134">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="37991-135">UBL Projectfactuur NL</span><span class="sxs-lookup"><span data-stu-id="37991-135">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="37991-136">UBL Projectcreditnota NL</span><span class="sxs-lookup"><span data-stu-id="37991-136">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="37991-137">Verkoopfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="37991-137">Sales invoice (ES)</span></span>
-   <span data-ttu-id="37991-138">Verkoopfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="37991-138">Sales invoice (IT)</span></span>
-   <span data-ttu-id="37991-139">Projectfactuur (ES)</span><span class="sxs-lookup"><span data-stu-id="37991-139">Project invoice (ES)</span></span>
-   <span data-ttu-id="37991-140">Projectfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="37991-140">Project invoice (IT)</span></span>

<span data-ttu-id="37991-141">De elektronische facturen en creditnota's die u genereert, bevatten vereiste gegevens zoals een EAN-nummer (European Article Numbering), de contactpersoon, het dimensierekeningnummer en adresgegevens van de klant.</span><span class="sxs-lookup"><span data-stu-id="37991-141">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="37991-142">Er worden validatieregels worden toegepast wanneer facturen worden gegenereerd om te controleren of de juiste gegevens zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="37991-142">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="37991-143">De set met vereiste gegevens kan verschillen van land tot land.</span><span class="sxs-lookup"><span data-stu-id="37991-143">The set of required information may differ from country to country.</span></span> <span data-ttu-id="37991-144">Omdat de vereiste en de ondersteunde landen en indelingen kunnen veranderen, moet u altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.</span><span class="sxs-lookup"><span data-stu-id="37991-144">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="37991-145">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="37991-145">Additional information</span></span>
<span data-ttu-id="37991-146">Voor meer informatie over het instellen van elektronische facturen, kunt u de volgende [Taakbegeleidingen](../../fin-and-ops/get-started/help-overview.md#task-guides) afspelen in het Help-venster:</span><span class="sxs-lookup"><span data-stu-id="37991-146">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="37991-147">OIOUBL elektronische facturen instellen</span><span class="sxs-lookup"><span data-stu-id="37991-147">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="37991-148">OIOUBL elektronische factureringsconfiguraties importeren</span><span class="sxs-lookup"><span data-stu-id="37991-148">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="37991-149">Klantrekeningen instellen voor elektronische OIOUBL-facturering</span><span class="sxs-lookup"><span data-stu-id="37991-149">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="37991-150">Hoewel deze Taakbegeleidingen zijn gemaakt voor de specifieke Deense e-factuurindeling *OIOUBL*, zijn ze met kleine afwijkingen van toepassing op andere ondersteunde landen.</span><span class="sxs-lookup"><span data-stu-id="37991-150">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>