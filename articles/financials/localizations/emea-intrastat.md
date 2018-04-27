---
title: Intrastat
description: Dit artikel bevat informatie over Intrastat-rapportage voor de handel van goederen en, in sommige gevallen, diensten tussen landen en regio's van de Europese Unie (EU). Het biedt een overzicht van het rapportageproces en bevat een beschrijving van de vereiste instellingen en vereisten.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2ee60f3d1155b89d342b94832fbdbe898a5063c6
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="intrastat"></a><span data-ttu-id="1396e-104">Intrastat</span><span class="sxs-lookup"><span data-stu-id="1396e-104">Intrastat</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1396e-105">Dit artikel bevat informatie over Intrastat-rapportage voor de handel van goederen en, in sommige gevallen, diensten tussen landen en regio's van de Europese Unie (EU).</span><span class="sxs-lookup"><span data-stu-id="1396e-105">This article provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="1396e-106">Het biedt een overzicht van het rapportageproces en bevat een beschrijving van de vereiste instellingen en vereisten.</span><span class="sxs-lookup"><span data-stu-id="1396e-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="1396e-107">Intrastat is het systeem voor het verzamelen van informatie en genereren van statistieken met betrekking tot de handel in artikelen tussen landen en regio's van de Europese Unie (EU).</span><span class="sxs-lookup"><span data-stu-id="1396e-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="1396e-108">Intrastat-aangifte is vereist wanneer een product de grens van een ander EU-land/regio overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="1396e-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="1396e-109">In sommige landen/regio's is Intrastat-aangifte ook van toepassing op services.</span><span class="sxs-lookup"><span data-stu-id="1396e-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="1396e-110">De verplichte en optionele elementen kunnen in Intrastat-aangiftes worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="1396e-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="1396e-111">De volgende elementen zijn verplicht: het btw-nummer van de partij die de informatie moet verstrekken, de referentieperiode, de stroom (ontvangst of verzending), de achtcijferige basisproductcode, de lidstaat van de partner (lidstaat van verzending voor ontvangsten en lidstaat van bestemming voor verzendingen), de waarde van de goederen, de hoeveelheid goederen (netto massa en bijkomende eenheid) en de aard van de transactie.</span><span class="sxs-lookup"><span data-stu-id="1396e-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="1396e-112">Landen/regio's kunnen ook optionele elementen verzamelen in diverse situaties.</span><span class="sxs-lookup"><span data-stu-id="1396e-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="1396e-113">Sommige optionele elementen zijn het land of de regio van herkomst, de leveringsvoorwaarden, de wijze van transport, een meer gedetailleerde basisproductcode dan CN8, de regio van herkomst voor verzendingen en de regio van bestemming voor ontvangsten, de statistische procedure, de statistische waarde, een omschrijving van de goederen, en de haven/de luchthaven waar het product wordt geladen/gelost.</span><span class="sxs-lookup"><span data-stu-id="1396e-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="1396e-114">Een overzicht van het Intrastat-aangifteproces</span><span class="sxs-lookup"><span data-stu-id="1396e-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="1396e-115">De volgende secties beschrijven de gehele stroom van informatie die wordt gebruikt voor Intrastat-aangifte.</span><span class="sxs-lookup"><span data-stu-id="1396e-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="1396e-116">1. Voer een transactie in die de grens met een ander EU-land/regio overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="1396e-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="1396e-117">Een klantfactuur, een vrije-tektsfactuur, een inkoopfactuur, een projectfactuur, een pakbon van de klant, een productontvangstbon van de leverancier of een transferorder worden alleen overgeboekt naar het Intrastat-journaal als het type land/regio van de bestemming (voor verzendingen) of verzending (op ontvangsten)**EU** is.</span><span class="sxs-lookup"><span data-stu-id="1396e-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="1396e-118">Deze functie is uitgebreid voor Microsoft Dynamics 365 for Operations (1611). Met deze functie kunt u vrachtadressen voor een intracommunautaire transactie opgeven.</span><span class="sxs-lookup"><span data-stu-id="1396e-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="1396e-119">Als een vrachtadres afwijkt van een zakelijk adres van de leverancier (of zakelijk adres van de klant voor retourorder), wordt deze informatie voor de Intrastat-aangifte gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1396e-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="1396e-120">Wanneer u een verkooporder, een vrije-tektsfactuur, een inkooporder, een leveranciersfactuur, een projectfactuur of een transferorder maakt, hebben sommige velden die aan buitenlandse handel zijn gerelateerd, standaardwaarden in de documentkoptekst of op de regel.</span><span class="sxs-lookup"><span data-stu-id="1396e-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="1396e-121">De standaardtransactiecode wordt overgenomen uit het overeenkomstige veld op de pagina **Parameters buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="1396e-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="1396e-122">De standaarbasisproductcode, het land/de regio van herkomst, en staat/provincie van herkomst worden opgehaald van het artikel.</span><span class="sxs-lookup"><span data-stu-id="1396e-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="1396e-123">U kunt de standaardwaarden wijzigen en ook andere aan buitenlandse handel gerelateerde informatie invullen: de statistische procedure, de transportwijze en de haven.</span><span class="sxs-lookup"><span data-stu-id="1396e-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="1396e-124">2. Met het Intrastat-journaal kunt u gegevens genereren over handel tussen landen en regio's van de EU.</span><span class="sxs-lookup"><span data-stu-id="1396e-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="1396e-125">Voor statistische doeleinden genereert u elke maand informatie over handel tussen de landen/regio's van de EU.</span><span class="sxs-lookup"><span data-stu-id="1396e-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="1396e-126">U kunt transacties overboeken van een vrije-tekstfactuur, klantfactuur, klantpakbon, leveranciersfactuur, leverancierspakbon, projectfactuur of transferorder volgens de criteria voor overdracht die zijn geconfigureerd op de pagina **Parameters buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="1396e-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="1396e-127">U kunt er ook voor kiezen transacties handmatig in te voeren.</span><span class="sxs-lookup"><span data-stu-id="1396e-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="1396e-128">Overgeboekte transacties kunt u in het Intrastat-journaal handmatig bijwerken, als updates worden vereist.</span><span class="sxs-lookup"><span data-stu-id="1396e-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="1396e-129">In specifieke omstandigheden die op de pagina **Compressie van Intrastat** worden geconfigureerd, kunt u de transacties in het Intrastat-journaal comprimeren.</span><span class="sxs-lookup"><span data-stu-id="1396e-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="1396e-130">Sommige landen/regio's laten u een lage transactiedrempel toepassen.</span><span class="sxs-lookup"><span data-stu-id="1396e-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="1396e-131">U kunt vervolgens transacties rapporteren die onder de opgegeven basisproductcode beneden deze drempel liggen.</span><span class="sxs-lookup"><span data-stu-id="1396e-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="1396e-132">U kunt de basisproductcode op de bijbehorende Intrastat-journaalregels bijwerken, op basis van de instelling voor **Ondergrens** op de pagina **Parameters buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="1396e-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="1396e-133">U kunt die transacties ook comprimeren, op basis van de instelling **Compressie van Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="1396e-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="1396e-134">U kunt valideren of de transacties in het Intrastat-journaal compleet zijn, op basis van de instelling **Instelling controleren** op de pagina **Parameters buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="1396e-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="1396e-135">De gegevens in bijbehorende velden kunnen op volledigheid worden gecontroleerd: land/regio, staat of provincie, gewicht, basisproductcode, transactiecode, aanvullende eenheid, haven, oorsprong, leveringsvoorwaarden, transportwijze en btw-nummer.</span><span class="sxs-lookup"><span data-stu-id="1396e-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="1396e-136">De transacties die niet zijn voltooid, worden gemarkeerd als zijnde niet geldig.</span><span class="sxs-lookup"><span data-stu-id="1396e-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="1396e-137">3. Met het Intrastat-journaal kunt u gegevens rapporteren over handel tussen landen en regio's van de EU.</span><span class="sxs-lookup"><span data-stu-id="1396e-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="1396e-138">Voor statistische doeleinden rapporteert u elke maand informatie over handel tussen de landen/regio's van de EU.</span><span class="sxs-lookup"><span data-stu-id="1396e-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="1396e-139">U kunt de Intrastat-aangifte afdrukken, op basis van de instellingen **Toewijzing van rapportindeling** op de pagina **Parameters buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="1396e-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="1396e-140">U kunt ook een elektronisch bestand genereren, op basis van de instellingen **Toewijzing van bestandsindeling** op de pagina **Parameters buitenlandse handel**.</span><span class="sxs-lookup"><span data-stu-id="1396e-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="1396e-141">Zie de taakregistraties voor Intrastat-aangifte voor meer informatie over Intrastat-aangifte, waaronder de vereisten:</span><span class="sxs-lookup"><span data-stu-id="1396e-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="1396e-142">Een EU Intrastat-aangifte genereren</span><span class="sxs-lookup"><span data-stu-id="1396e-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="1396e-143">Transacties overboeken naar Intrastat</span><span class="sxs-lookup"><span data-stu-id="1396e-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="1396e-144">Vrachtadres opgeven voor een intracommunautaire transactie</span><span class="sxs-lookup"><span data-stu-id="1396e-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1396e-145">Vereisten</span><span class="sxs-lookup"><span data-stu-id="1396e-145">Prerequisites</span></span>
<span data-ttu-id="1396e-146">In de volgende tabel ziet u de vereisten voor Intrastat-aangifte.</span><span class="sxs-lookup"><span data-stu-id="1396e-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1396e-147">Vereiste</span><span class="sxs-lookup"><span data-stu-id="1396e-147">Prerequisite</span></span></th>
<th><span data-ttu-id="1396e-148">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1396e-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1396e-149">Adresinstelling</span><span class="sxs-lookup"><span data-stu-id="1396e-149">Address setup</span></span></td>
<td><span data-ttu-id="1396e-150">Configureer ISO-codes (International Organization for Standardization) voor de landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="1396e-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-151">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="1396e-151">Legal entity</span></span></td>
<td><span data-ttu-id="1396e-152">Configureer btw-nummers voor import/export, de filiaalnummerextensie voor import/export en de Intrastat-code die aan de rechtspersoon is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1396e-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1396e-153">Productcategoriehiërarchie (verkopenhiërarchie, inkoophiërarchie)</span><span class="sxs-lookup"><span data-stu-id="1396e-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="1396e-154">Wijs de Intrastat-basisproductcodes toe aan de categorieknooppunten op het tabblad <strong>Basisproductcodes</strong> op de pagina <strong>Categoriehiërarchie</strong>.</span><span class="sxs-lookup"><span data-stu-id="1396e-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="1396e-155">Wanneer u een basisproductcode aan een bovenliggende categorieknooppunt toewijst, is die code van toepassing op alle onderliggende categorieknooppunten.</span><span class="sxs-lookup"><span data-stu-id="1396e-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="1396e-156">De geselecteerde basisproductcodes zijn beschikbaar in de weergave <strong>Geselecteerd</strong>, wanneer u een basisproductcode selecteert in de details van een vrijgegeven product, en op regels van verkooporders, inkooporders, en transferorders.</span><span class="sxs-lookup"><span data-stu-id="1396e-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-157">Vrijgegeven productdetails</span><span class="sxs-lookup"><span data-stu-id="1396e-157">Released product details</span></span></td>
<td><span data-ttu-id="1396e-158">Configureer de volgende gegevens voor buitenlandse handel voor vrijgegeven producten:</span><span class="sxs-lookup"><span data-stu-id="1396e-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="1396e-159"><strong>Basisproductcode</strong>: Selecteer deze in de lijst met geselecteerde basisproducten die is opgehaald uit de toegewezen productcategorieën, of in de volledige lijst van Intrastat-basisproductcodes.</span><span class="sxs-lookup"><span data-stu-id="1396e-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="1396e-160"><strong>Statistieken toeslagenpercentage</strong></span><span class="sxs-lookup"><span data-stu-id="1396e-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="1396e-161"><strong>Land/regio van oorsprong</strong>: Selecteer het standaardland/de standaardregio waar de goederen volledig werden verkregen of geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="1396e-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="1396e-162"><strong>Staat/provincie van oorsprong of bestemming</strong>: Selecteerd de standaardstaat/-provincie van bestemming voor ontvangsten en de staat/provincie van verzending.</span><span class="sxs-lookup"><span data-stu-id="1396e-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="1396e-163"><strong>Nettogewicht in kg</strong></span><span class="sxs-lookup"><span data-stu-id="1396e-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1396e-164">Klanten</span><span class="sxs-lookup"><span data-stu-id="1396e-164">Customers</span></span></td>
<td><span data-ttu-id="1396e-165">Configureer het afleveradres van de klant in het EU-land/de EU-regio.</span><span class="sxs-lookup"><span data-stu-id="1396e-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-166">Leveranciers   </span><span class="sxs-lookup"><span data-stu-id="1396e-166">Vendors</span></span></td>
<td><span data-ttu-id="1396e-167">Configureer het adres van de leverancier in het EU-land/de EU-regio.</span><span class="sxs-lookup"><span data-stu-id="1396e-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1396e-168">Diverse toeslagen</span><span class="sxs-lookup"><span data-stu-id="1396e-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="1396e-169">De code voor diverse toeslagen die moet worden opgenomen in het factuurbedrag, het statistische bedrag, of in beide.</span><span class="sxs-lookup"><span data-stu-id="1396e-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="1396e-170">Op de pagina <strong>Toeslagcodes</strong>, op het tabblad <strong>Buitenlandse handel</strong>, schakelt u <strong>Intrastat-facturenwaarde</strong> in om het toeslagenbedrag toe te voegen aan de factuurwaarde, en schakelt u <strong>Statistische Infrastat-waarde</strong> in om het toeslagenbedrag toe te voegen aan de statistische waarde.</span><span class="sxs-lookup"><span data-stu-id="1396e-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-171">Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1396e-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="1396e-172">Stel configuraties voor elektronische aangifte in om Intrastat-gegevens te exporteren in een elektronisch bestand met een door de relevante autoriteit vereiste indeling, en waarmee de Infrastat-gegevens kunnen worden weergegeven in een leesbare (gebruikersvriendelijke) indeling (bijvoorbeeld in Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="1396e-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-173">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="1396e-173">Warehousing</span></span></td>
<td><span data-ttu-id="1396e-174">Koppel leveranciersrekeningen aan magazijncodes voor het invullen van het btw-nummer bij het overboeken van de transferorder.</span><span class="sxs-lookup"><span data-stu-id="1396e-174">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="1396e-175">Instelling</span><span class="sxs-lookup"><span data-stu-id="1396e-175">Setup</span></span>
<span data-ttu-id="1396e-176">De volgende secties beschrijven de instellingen die voor Intrastat-aangifte zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="1396e-176">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="1396e-177">Alle vereiste aan Intrastat gerelateerde lijsten instellen</span><span class="sxs-lookup"><span data-stu-id="1396e-177">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1396e-178">Weergeven</span><span class="sxs-lookup"><span data-stu-id="1396e-178">List</span></span></th>
<th><span data-ttu-id="1396e-179">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="1396e-179">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1396e-180">Basisproductcodes</span><span class="sxs-lookup"><span data-stu-id="1396e-180">Commodity codes</span></span></td>
<td><span data-ttu-id="1396e-181">Stel een categoriehiërarchie in van het type <strong>Basisproductcode</strong> en voer alle basisproductcodes in volgens de gecombineerde nomenclatuurlijst.</span><span class="sxs-lookup"><span data-stu-id="1396e-181">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="1396e-182">Voor elk basisproduct stelt u de volgende gegevens in:</span><span class="sxs-lookup"><span data-stu-id="1396e-182">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="1396e-183">De naam van het basisproduct en de basisproductcode</span><span class="sxs-lookup"><span data-stu-id="1396e-183">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="1396e-184">De beschrijvende naam en/of de vertaalde naam</span><span class="sxs-lookup"><span data-stu-id="1396e-184">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="1396e-185">Instellingen voor het rapporteren van aanvullende (bijkomende) eenheden op het tabblad <strong>Buitenlandse handel</strong> tabblad. U kunt de aanvullende eenheid in de eenheidslijst selecteren.</span><span class="sxs-lookup"><span data-stu-id="1396e-185">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="1396e-186">U kunt ook opgeven of naast de geselecteerde aanvullende eenheid ook het gewicht van basisproducten moet worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="1396e-186">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-187">Transactiecodes</span><span class="sxs-lookup"><span data-stu-id="1396e-187">Transaction codes</span></span></td>
<td><span data-ttu-id="1396e-188">Stel de aard van de transactie in op basis van de vereisten van uw land/regio.</span><span class="sxs-lookup"><span data-stu-id="1396e-188">Set up the nature of the transaction according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="1396e-189">Voor elke transactiecode die u instelt, moet u de regels configureren voor berekening van factuurbedragen en statistische bedragen voor transferorders en verkoop- of inkooporders.</span><span class="sxs-lookup"><span data-stu-id="1396e-189">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="1396e-190">Voor transferorders configureert u een van de volgende regels voor berekening van factuurbedragen en statistische bedragen:</span><span class="sxs-lookup"><span data-stu-id="1396e-190">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="1396e-191"><strong>Leeg</strong>: Het bedrag is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1396e-191"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="1396e-192"><strong>Financiële kostprijs</strong>: Het bedrag is gelijk aan de financiële kosten.</span><span class="sxs-lookup"><span data-stu-id="1396e-192"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="1396e-193"><strong>Totale kosten</strong>: Het bedrag is gelijk aan de totale kosten van de transactie.</span><span class="sxs-lookup"><span data-stu-id="1396e-193"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="1396e-194"><strong>Handmatig</strong>: Het bedrag is gelijk aan het bedrag dat handmatig op de transferorderregel wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="1396e-194"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="1396e-195">Voor verkooporders en inkooporders configureert u een van de volgende regels voor berekening van factuurbedragen en statistische bedragen:</span><span class="sxs-lookup"><span data-stu-id="1396e-195">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="1396e-196"><strong>Leeg</strong>: Het bedrag is 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1396e-196"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="1396e-197"><strong>Factuurbedrag</strong>: Het bedrag is gelijk aan het bedrag dat voor het basisartikel is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="1396e-197"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="1396e-198"><strong>Basisbedrag</strong>: Het bedrag is gelijk aan het bedrag dat zou worden gefactureerd voordat eventuele kortingen zijn toegepast.</span><span class="sxs-lookup"><span data-stu-id="1396e-198"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1396e-199">Transportmethoden</span><span class="sxs-lookup"><span data-stu-id="1396e-199">Transport methods</span></span></td>
<td><span data-ttu-id="1396e-200">Stel de transportwijze in op basis van de vereisten van uw land/regio.</span><span class="sxs-lookup"><span data-stu-id="1396e-200">Set up the transport mode according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="1396e-201">Voor elke leveringsmethode kunt u een standaardtransportmethode configureren op het tabblad <strong>Buitenlandse handel</strong>.</span><span class="sxs-lookup"><span data-stu-id="1396e-201">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-202">Havens/luchthavens</span><span class="sxs-lookup"><span data-stu-id="1396e-202">Ports</span></span></td>
<td><span data-ttu-id="1396e-203">Configureer de haven/luchthaven waar de goederen worden geladen of gelost, als deze informatie door uw land/regio wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="1396e-203">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1396e-204">Statistiekprocedures</span><span class="sxs-lookup"><span data-stu-id="1396e-204">Statistics procedures</span></span></td>
<td><span data-ttu-id="1396e-205">Configureer de statistische procedure als deze informatie door uw land/regio wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="1396e-205">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="1396e-206">Configureer regels voor het comprimeren van Intrastat-transacties</span><span class="sxs-lookup"><span data-stu-id="1396e-206">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="1396e-207">Op de pagina **Compressie van Intrastat** kunt u de velden selecteren die voor compressie moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1396e-207">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="1396e-208">Alle transacties met dezelfde combinatie van waarden voor de geselecteerde velden in het Intrastat-journaal worden in één transactie gecomprimeerd, wanneer u de functie Comprimeren uitvoert in het Intrastat-journaal.</span><span class="sxs-lookup"><span data-stu-id="1396e-208">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="1396e-209">Parameters voor buitenlandse handel instellen</span><span class="sxs-lookup"><span data-stu-id="1396e-209">Set up foreign trade parameters</span></span>

<span data-ttu-id="1396e-210">Gebruik de pagina **Parameters buitenlandse handel** om de parameters in de volgende tabel in te stellen.</span><span class="sxs-lookup"><span data-stu-id="1396e-210">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1396e-211">Tabblad</span><span class="sxs-lookup"><span data-stu-id="1396e-211">Tab</span></span></th>
<th><span data-ttu-id="1396e-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="1396e-212">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1396e-213">Algemeen</span><span class="sxs-lookup"><span data-stu-id="1396e-213">General</span></span></td>
<td><ul>
<li><span data-ttu-id="1396e-214"><strong>Algemeen</strong>: Geef de volgende informatie op:</span><span class="sxs-lookup"><span data-stu-id="1396e-214"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="1396e-215">De standaardtransactiecodes voor verkooporders, inkooporders, creditnota's en transferorders.</span><span class="sxs-lookup"><span data-stu-id="1396e-215">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="1396e-216">De transactiecode die wordt ingesteld voor creditnota's wordt ook gebruikt als de code voor retouren van materiële goederen en voor afwijkende materiële retouren versus corrigerende creditnota's.</span><span class="sxs-lookup"><span data-stu-id="1396e-216">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span></li>
<li><span data-ttu-id="1396e-217">De werknemer die verantwoordelijk is voor het voorbereiden van Intrastat-aangiften.</span><span class="sxs-lookup"><span data-stu-id="1396e-217">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="1396e-218"><strong>Ondergrens</strong>: Geef de instellingen op voor het bijwerken van transacties die onder de drempel liggen:</span><span class="sxs-lookup"><span data-stu-id="1396e-218"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="1396e-219">Bedrag en gewicht van de drempel</span><span class="sxs-lookup"><span data-stu-id="1396e-219">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="1396e-220">De basisproductcode die wordt toegepast op transacties die onder de drempel liggen</span><span class="sxs-lookup"><span data-stu-id="1396e-220">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="1396e-221"><strong>Overboeken</strong>: Geef de criteria voor het overboeken van transacties naar het Intrastat-journaal.</span><span class="sxs-lookup"><span data-stu-id="1396e-221"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="1396e-222">U kunt opgeven dat de transacties alleen mogen worden overgeboekt wanneer de artikelen aan een of alle van de volgende criteria voldoen:</span><span class="sxs-lookup"><span data-stu-id="1396e-222">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="1396e-223">De artikelen zijn geen serviceartikelen.</span><span class="sxs-lookup"><span data-stu-id="1396e-223">The items aren&#39;t service items.</span></span></li>
<li><span data-ttu-id="1396e-224">De artikelen hebben een basisproductcode.</span><span class="sxs-lookup"><span data-stu-id="1396e-224">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="1396e-225">De artikelen hebben een gewicht.</span><span class="sxs-lookup"><span data-stu-id="1396e-225">The items have a weight.</span></span></li>
<li><span data-ttu-id="1396e-226">De artikelen hebben aanvullende eenheden.</span><span class="sxs-lookup"><span data-stu-id="1396e-226">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="1396e-227"><strong>Instelling contoleren</strong>: Geef de regels op voor het valideren van de volledigheid van Intrastat-gegevens.</span><span class="sxs-lookup"><span data-stu-id="1396e-227"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="1396e-228">U kunt selecteren welke gegevens worden gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="1396e-228">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="1396e-229"><strong>Afrondingsregels</strong>: Geef de volgende instellingen op voor afrondingsbedragen en gewichten in Intrastat-aangifte:</span><span class="sxs-lookup"><span data-stu-id="1396e-229"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="1396e-230">De afrondingsregel (precisie)</span><span class="sxs-lookup"><span data-stu-id="1396e-230">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="1396e-231">De afrondingsmethode: naar boven, naar beneden of normaal</span><span class="sxs-lookup"><span data-stu-id="1396e-231">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="1396e-232">Het aantal decimalen voor bedragen en gewichten</span><span class="sxs-lookup"><span data-stu-id="1396e-232">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="1396e-233">Instructies voor het afronden van gewichten die kleiner dan 1 kilogram (kg) zijn: naar 1 kg, normaal of geen afronding</span><span class="sxs-lookup"><span data-stu-id="1396e-233">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="1396e-234"><strong>Elektronische aangifte</strong>: Geef verwijzingen op naar configuraties voor elektronische aangifte, zodat u een elektronisch bestand en een rapport kunt genereren.</span><span class="sxs-lookup"><span data-stu-id="1396e-234"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="1396e-235"><strong>Hiërarchie van basisproductcodes</strong>: Geef de categoriehiërarchie op van het type <strong>basisproductcode</strong> dat Intrastat-basisproductcode CN8 vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="1396e-235"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-236">Contactgegevens van medewerkers</span><span class="sxs-lookup"><span data-stu-id="1396e-236">Agent contact information</span></span></td>
<td><span data-ttu-id="1396e-237">Geef de naam, het adres, btw-nummer, telefoonnummer en faxnummer van de medewerker op.</span><span class="sxs-lookup"><span data-stu-id="1396e-237">Specify the agent&#39;s name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1396e-238">Land-/regio-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="1396e-238">Country/region properties</span></span></td>
<td><span data-ttu-id="1396e-239">Stel het land/de regio van de huidige rechtspersoon in op <strong>Binnenlands</strong>.</span><span class="sxs-lookup"><span data-stu-id="1396e-239">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="1396e-240">Stel het land of de regio van de landen/regio's in de EU, die deelnemen aan EU-handel met de huidige rechtspersoon, in op <strong>EU</strong>.</span><span class="sxs-lookup"><span data-stu-id="1396e-240">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="1396e-241">Voor elk land/regio geeft u ook de land-/regiocode voor buitenlandse handelsdoeleinden op.</span><span class="sxs-lookup"><span data-stu-id="1396e-241">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1396e-242">Nummerreeks</span><span class="sxs-lookup"><span data-stu-id="1396e-242">Number sequence</span></span></td>
<td><span data-ttu-id="1396e-243">Geef het volgnummer op voor het Intrastat-journaal.</span><span class="sxs-lookup"><span data-stu-id="1396e-243">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>






