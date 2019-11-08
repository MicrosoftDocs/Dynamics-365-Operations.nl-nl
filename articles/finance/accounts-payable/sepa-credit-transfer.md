---
title: Overzicht SEPA-kredietoverdracht
description: Dit artikel geeft algemene informatie over ISO 20022-overschrijvingen, waaronder SEPA-overschrijvingen (Single euro Payments Area) en andere elektronische betalingen voor leveranciers. Een SEPA-kredietoverdracht is een specifiek type betaling in euro's van een persoon of bedrijf aan een andere persoon of bedrijf. In dit onderwerp wordt ook beschreven hoe u een kredietoverdrachtbetalingsbestand kunt instellen en verzenden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0fc01508bd206f750a4101521cd9dff7b647656
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177231"
---
# <a name="sepa-credit-transfer-overview"></a><span data-ttu-id="dcd9c-105">Overzicht SEPA-kredietoverdracht</span><span class="sxs-lookup"><span data-stu-id="dcd9c-105">SEPA credit transfer overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcd9c-106">Dit artikel geeft algemene informatie over ISO 20022-overschrijvingen, waaronder SEPA-overschrijvingen (Single euro Payments Area) en andere elektronische betalingen voor leveranciers.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-106">This article provides general information about ISO 20022 credit transfers, which include Single Euro Payments Area (SEPA) credit transfers and any other electronic payments for vendors.</span></span> <span data-ttu-id="dcd9c-107">Een SEPA-kredietoverdracht is een specifiek type betaling in euro's van een persoon of bedrijf aan een andere persoon of bedrijf.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-107">A SEPA credit transfer is a specific type of payment in euros from one company or individual to another company or individual.</span></span> <span data-ttu-id="dcd9c-108">In dit onderwerp wordt ook beschreven hoe u een kredietoverdrachtbetalingsbestand kunt instellen en verzenden.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-108">The topic also explains how to set up and transmit a credit transfer payment file.</span></span>

## <a name="what-is-a-credit-transfer-message"></a><span data-ttu-id="dcd9c-109">Wat is een kredietoverdrachtsbericht?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-109">What is a credit transfer message?</span></span>
<span data-ttu-id="dcd9c-110">Het kredietoverdrachtbericht is een aanvraag die een initiërende partij (uw bedrijf) verzendt om fondsen van een eigen rekening naar een crediteur over te maken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-110">The credit transfer message is a request that an initiating party (your company) sends to move funds from its own account to a creditor.</span></span> <span data-ttu-id="dcd9c-111">Er zijn veel land- of regio-specifieke en bank-specifieke implementaties van kredietoverdrachtberichten.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-111">There are many country/region-specific and bank-specific implementations of credit transfer messages.</span></span> <span data-ttu-id="dcd9c-112">Enkele daarvan worden gebruikt in een bepaald land/regio en sommige worden standaarden.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-112">Some of them are used within one country/region, and some are becoming standards.</span></span> <span data-ttu-id="dcd9c-113">Een algemeen aanvaarde internationale standaard is ISO 20022 en het initiatiebericht, zoals kredietoverdracht.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-113">One well-established global standard is ISO 20022 and its initiation messages, such as Credit transfer.</span></span> <span data-ttu-id="dcd9c-114">In de volgende afbeelding ziet u de relaties en dekking voor geselecteerde kredietoverdrachtberichten</span><span class="sxs-lookup"><span data-stu-id="dcd9c-114">The following illustration shows the relations and coverage for selected credit transfer messages.</span></span> 
<span data-ttu-id="dcd9c-115">![Kredietoverdracht](./media/credit-transfer.jpg) Kredietoverdrachtberichten</span><span class="sxs-lookup"><span data-stu-id="dcd9c-115">![Credit tansfer](./media/credit-transfer.jpg) Credit transfer messages</span></span> 

## <a name="what-are-iso-20022-and-sepa-payments"></a><span data-ttu-id="dcd9c-116">Wat zijn ISO 20022- en SEPA-betalingen?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-116">What are ISO 20022 and SEPA payments?</span></span>
<span data-ttu-id="dcd9c-117">De gemeenschappelijke betalingsruimte voor de euro (SEPA) is ingesteld door de Europese Commissie en dicteert dat alle elektronische betalingen als binnenlands worden beschouwd, ongeacht het land/de regio waar de persoon, het bedrijf of organisatie en de bank zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-117">The Single Euro Payments Area (SEPA) is set up by the European Commission and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located.</span></span> <span data-ttu-id="dcd9c-118">Er is geen verschil tussen nationale en grensoverschrijdende betalingen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-118">There is no difference between national payments and cross-border payments.</span></span> <span data-ttu-id="dcd9c-119">De SEPA omvat de 28 lidstaten van de Europese Unie (EU) plus IJsland, Liechtenstein, Noorwegen, Zwitserland, Monaco en San Marino.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-119">The SEPA includes the 28 member states of the European Union (EU), and also Iceland, Liechtenstein, Norway, Switzerland, Monaco, and San Marino.</span></span> <span data-ttu-id="dcd9c-120">De SEPA helpt met de opbouw van een markt voor betalingstransacties in de Europese Economische Ruimte (EEA).</span><span class="sxs-lookup"><span data-stu-id="dcd9c-120">The SEPA helps form a single market for payment transactions within the European Economic Area (EEA).</span></span> <span data-ttu-id="dcd9c-121">Uiteindelijk moet SEPA het aantal betaalindelingen verminderen waar banken, bedrijven en personen mee moeten werken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-121">Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.</span></span> <span data-ttu-id="dcd9c-122">De Europese Commissie vestigde de wettelijke basis voor SEPA-betalingen via de Richtlijn betaaldiensten (PSD, Payment Services Directive).</span><span class="sxs-lookup"><span data-stu-id="dcd9c-122">The European Commission established the legal foundation for SEPA payments through the Payment Services Directive (PSD).</span></span> <span data-ttu-id="dcd9c-123">De European Payments Council (EPC) ondersteunt SEPA met de volgende activiteiten:</span><span class="sxs-lookup"><span data-stu-id="dcd9c-123">The European Payments Council (EPC) supports the SEPA through the following activities:</span></span>

-   <span data-ttu-id="dcd9c-124">De EPC bepaalt de standaarden voor elektronische SEPA-betalingen met behulp van de ISO 20022 UNIFI (Universal financial industry message scheme) XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-124">It sets the standards for SEPA electronic payments by using the ISO 20022 Universal financial industry message scheme XML format.</span></span>
-   <span data-ttu-id="dcd9c-125">De EPC ontwikkelt regels en richtlijnen over het afhandelen van eurobetalingen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-125">It establishes rules and guidelines about the handling of euro payments.</span></span>

<span data-ttu-id="dcd9c-126">De EPC, die bestaat uit Europese banken, ontwikkelt commerciële en technische raamwerken voor SEPA-betaalmiddelen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-126">The EPC, which consists of European banks, develops the commercial and technical frameworks for SEPA payment instruments.</span></span> <span data-ttu-id="dcd9c-127">Er worden drie typen SEPA-betalingen gebruikt:</span><span class="sxs-lookup"><span data-stu-id="dcd9c-127">Three types of SEPA payments are used:</span></span>

-   <span data-ttu-id="dcd9c-128">Kredietoverdrachten</span><span class="sxs-lookup"><span data-stu-id="dcd9c-128">Credit transfers</span></span>
-   <span data-ttu-id="dcd9c-129">Automatische afschrijvingen</span><span class="sxs-lookup"><span data-stu-id="dcd9c-129">Direct debits</span></span>
-   <span data-ttu-id="dcd9c-130">Kaarten</span><span class="sxs-lookup"><span data-stu-id="dcd9c-130">Cards</span></span>

## <a name="what-is-a-sepa-credit-transfer"></a><span data-ttu-id="dcd9c-131">Wat is een SEPA-kredietoverdracht?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-131">What is a SEPA credit transfer?</span></span>
<span data-ttu-id="dcd9c-132">Een SEPA-kredietoverdracht is een betaling van een persoon of bedrijf aan een andere persoon of bedrijf.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-132">A SEPA credit transfer is a payment from one company or individual to another company or individual.</span></span> <span data-ttu-id="dcd9c-133">De betalingen moeten in euro's zijn en moeten het Internationale Bankrekeningnummer (IBAN) en de BIC (Bank Identifier Code) voor beide partijen bevatten</span><span class="sxs-lookup"><span data-stu-id="dcd9c-133">Payments must be in euros, and must include the International Bank Account Number (IBAN) and the Bank Identifier Code (BIC) for both parties.</span></span> <span data-ttu-id="dcd9c-134">De BIC wordt ook wel SWIFT-code genoemd \[Society for Worldwide Interbank Financial Telecommunication SWIFT\]. Bovendien moeten transactiekosten worden gedeeld door de beide partijen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-134">(The BIC is also known as the Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] code.) Additionally, transaction costs must be shared between both parties.</span></span> <span data-ttu-id="dcd9c-135">Voor kredietoverdrachten tussen partijen moeten XML-bestanden worden gebruikt die voldoen aan de ISO 20022 betalingsverwerkingsstandaarden en de XML-indeling voldoen, zoals opgegeven door de EPC.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-135">Credit transfers that occur between parties should use XML files that comply with ISO 20022 payment processing standards and the XML format, as specified by the EPC.</span></span>

## <a name="how-is-a-credit-transfer-implemented"></a><span data-ttu-id="dcd9c-136">Hoe wordt een kredietoverdracht uitgevoerd?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-136">How is a credit transfer implemented?</span></span>
<span data-ttu-id="dcd9c-137">De indeling voor kredietoverdrachtbetaling voor Europese landen wordt uitgevoerd met behulp van de functionaliteit voor Elektronische Rapportage en Betalingsmethoden in Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-137">The credit transfer payment format for European countries is implemented by using the Electronic reporting (ER) and Methods of payment functionality in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="dcd9c-138">Enkele kredietoverdrachtindelingen die in andere regio's worden gebruikt, gebruiken nog het oude framework voor betalingen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-138">A few credit transfer formats that are used in other regions still use the legacy payment framework.</span></span> <span data-ttu-id="dcd9c-139">Er zijn vele andere indelingen beschikbaar, waaronder twaalf ISO 20022-bestandsindelingen voor kredietoverdracht.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-139">Among many other formats, there are twelve ISO 20022 credit transfer file formats that are available.</span></span> <span data-ttu-id="dcd9c-140">Deze exportindelingen voldoen aan de XML-standaard ISO 20022 voor SEPA.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-140">These export formats conform to the SEPA ISO 20022 XML standard.</span></span> <span data-ttu-id="dcd9c-141">Zij zijn bedoeld om betalingsoverschrijvingen in andere valuta dan euro te genereren, voor de landen/regio's waar ze worden gebruikt, en betalingen in euro zoals opgegeven in versie 8.2 van het SEPA Credit Transfer Scheme Rulebook dat de EPC uitgeeft.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-141">They are used to generate non-euro payment transfers for countries/regions where they are used and euro payments as specified in version 8.2 of the SEPA Credit Transfer Scheme Rulebook that the EPC releases.</span></span> <span data-ttu-id="dcd9c-142">Voordat u kredietoverdrachten kunt uitvoeren, moet u contact opnemen met uw bank om software te krijgen die vereist is voor het uploaden van bestanden voor elektronisch bankieren.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-142">Before you can implement credit transfers, you must contact your bank to obtain the software that is required in order to upload electronic banking files.</span></span> <span data-ttu-id="dcd9c-143">U kunt die software gebruiken om de XML-bestanden met betalingsopdrachten naar uw bank over te zetten.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-143">You will use that software to transfer the XML files that contain payment orders to your bank.</span></span>

## <a name="what-credit-transfer-formats-are-currently-supported"></a><span data-ttu-id="dcd9c-144">Welke kredietoverdracht-indelingen worden momenteel ondersteund?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-144">What credit transfer formats are currently supported?</span></span>
<span data-ttu-id="dcd9c-145">U moet altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-145">You should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="dcd9c-146">In de volgende sectie, 'Wat moet ik instellen?' vindt u een koppeling naar het onderwerp met informatie over het maken van een LCS-opslagplaats voor het controleren van de beschikbare configuraties en het importeren van geselecteerde configuraties.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-146">The next section, "What do I have to set up?", provides a link to the topic that explains how to create an LCS repository to review available configurations and import selected configurations.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="dcd9c-147">Wat moet ik instellen?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-147">What do I have to set up?</span></span>
-   <span data-ttu-id="dcd9c-148">Voordat u kredietoverdrachtbestanden kunt maken, moet tenminste één actieve kredietoverdrachtconfiguratie in uw ER-configuraties worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-148">Before you can create credit transfer files, at least one active credit transfer configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="dcd9c-149">Zie voor instructies het onderwerp [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="dcd9c-149">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
-   <span data-ttu-id="dcd9c-150">Wanneer u betalingsmethoden voor leveranciers configureert, selecteert u het selectievakje **Algemene elektronische rapportage**. Selecteer vervolgens de gewenste kredietoverdrachtindeling (bijvoorbeeld **ISO 20022 Kredietoverdracht**) als exportindelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-150">When you configure Accounts payable methods of payment, select the **Generic electronic reporting** check box, and select the appropriate credit transfer format (for example, **ISO 20022 Credit transfer (AT)**) as an export format configuration.</span></span>
-   <span data-ttu-id="dcd9c-151">U moet ook de rechtspersoon en bankrekeninggegevens instellen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-151">You must also set up the legal entity and bank account information.</span></span>
-   <span data-ttu-id="dcd9c-152">Bankrekeningnummers, IBAN's en soms SWIFT-codes (BIC's) of andere id's zijn vereist om geldige kredietoverdracht betalingen te kunnen maken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-152">Bank account numbers, IBANs, and sometimes SWIFT codes (BICs) or other IDs are required in order to create valid credit transfer payments.</span></span> <span data-ttu-id="dcd9c-153">Daarom moet u deze instellen voor de bankrekening van de leverancier en de bankrekening van de organisatie die de overdracht aanvraagt.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-153">Therefore, you must set up them for the vendor bank account and the bank account for the organization that is requesting the transfer.</span></span>
-   <span data-ttu-id="dcd9c-154">Mogelijk is aanvullende informatie vereist, zoals btw-nummers voor de partijen waarnaar wordt verwezen in het kredietoverdrachtbericht.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-154">Additional information might be required, such as value-added tax (VAT) numbers for the parties that are referred to in the credit transfer message.</span></span> <span data-ttu-id="dcd9c-155">Deze informatie moet worden ingesteld voor leveranciers en voor de rechtspersoon wanneer daarom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-155">This information must be set up for vendors and for the legal entity when it's requested.</span></span>
-   <span data-ttu-id="dcd9c-156">Sommige leveranciersbetalingsmethoden, meestal de betalingsmethoden op basis van ISO 20022, kunnen aanvullende instellingen vereisen voor **Codesets van de betalingsindeling**, zoals **Servicetype** = **SLEV**.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-156">Some Accounts payable methods of payment, mostly ISO 20022–based methods of payment, might require additional setup for **Payment format code sets**, such as **Service type** = **SLEV**.</span></span> <span data-ttu-id="dcd9c-157">Deze codes worden gebruikt als extra labels voor betalingstransacties tijdens de verwerking van betalingen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-157">Those codes are used as additional tagging for payment transactions during payment processing.</span></span> <span data-ttu-id="dcd9c-158">Standaardwaarden van betalingscodes, zoals **Categoriedoel**, **Aansprakelijke voor de kosten**, **Lokaal instrument** en **Serviceniveau** kunnen worden ingesteld op twee plaatsen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-158">Default values of Payment codes, like **Category purpose**, **Charge bearer**, **Local instrument** and **Service level** can be set in two places.</span></span> <span data-ttu-id="dcd9c-159">De eerste plaats is **Journaalkoptekst voor leveranciersbetalingen** en de tweede is **Betalingsmethoden voor leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-159">The first place is **Accounts payable payment journal header** and the second is **Accounts payable methods for payments**.</span></span> <span data-ttu-id="dcd9c-160">Bij het maken van regels in een betalingsjournaal, worden de waarden van betalingscodes die zijn ingesteld op de betalingsjournaalkoptekst overgebracht naar een journaalregel. Als ze niet zijn ingesteld, worden de waarden uit Betalingsmethoden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-160">Upon payment journal lines creation, Payment code values set on payment journal header are transferred to a journal line, if not set, the values from Methods of payment are used.</span></span>

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a><span data-ttu-id="dcd9c-161">Welke parameters zijn beschikbaar voor het genereren van kredietoverdrachtbetalingen?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-161">What parameters are available for generating credit transfer payments?</span></span>
<span data-ttu-id="dcd9c-162">De lijst met specifieke parameters is afhankelijk van de indeling van de kredietoverdracht.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-162">The list of specific parameters depends on the credit transfer format.</span></span> <span data-ttu-id="dcd9c-163">In de volgende tabel staan de parameters die beschikbaar zijn wanneer u een ISO 20022-kredietoverdrachtbetalingsbestand voor Duitsland in een leveranciersbetalingsjournaal genereert.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-163">The following table shows the parameters that are available when you generate a ISO 20022 credit transfer payment file for Germany in a vendor payment journal.</span></span> <span data-ttu-id="dcd9c-164">Met de opties op het tabblad **Op de achtergrond uitvoeren** kunt u betalingen genereren in batchmodus.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-164">By using the options that are available on the **Run in the background** tab, you can run payment generation in batch mode.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dcd9c-165">Veld</span><span class="sxs-lookup"><span data-stu-id="dcd9c-165">Field</span></span></th>
<th><span data-ttu-id="dcd9c-166">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="dcd9c-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dcd9c-167">Batch boeken</span><span class="sxs-lookup"><span data-stu-id="dcd9c-167">Batch booking</span></span></td>
<td><span data-ttu-id="dcd9c-168">Schakel dit selectievakje in om het batchboekingslabel in het XML-bestand op te nemen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-168">Select this check box to include the batch booking tag in the XML file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcd9c-169">Verwerking van datum</span><span class="sxs-lookup"><span data-stu-id="dcd9c-169">Processing date</span></span></td>
<td><span data-ttu-id="dcd9c-170">Voer de datum in waarop de bank de betalingen moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-170">Enter the date when the bank should process the payments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcd9c-171">Opmaak</span><span class="sxs-lookup"><span data-stu-id="dcd9c-171">Format</span></span></td>
<td><span data-ttu-id="dcd9c-172">Selecteer de indeling voor remisegegevens, afhankelijk van de vereisten van uw land/regio of bank:</span><span class="sxs-lookup"><span data-stu-id="dcd9c-172">Select the format for remittance information, depending on the requirements of your country/region or bank:</span></span>
<ul>
<li><span data-ttu-id="dcd9c-173"><strong>Strd:</strong> Selecteer deze optie om de gestructureerde indeling te gebruiken wanneer één betalingsregel wordt vereffend met één factuur.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-173"><strong>Strd</strong> – Select this option to use the structured format when one payment line is settled against one invoice.</span></span> <span data-ttu-id="dcd9c-174">Deze optie is niet beschikbaar voor de land-/regiospecifieke exportindelingen voor Frankrijk, Duitsland of Nederland.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-174">This option isn&#39;t available for the country/region-specific export formats for France, Germany, or the Netherlands.</span></span></li>
<li><span data-ttu-id="dcd9c-175"><strong>Ustrd</strong> - Selecteer deze optie om de ongestructureerde indeling te gebruiken wanneer de betaling wordt vereffend met meerdere facturen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-175"><strong>Ustrd</strong> – Select this option to use the unstructured format when the payment is settled against multiple invoices.</span></span> <span data-ttu-id="dcd9c-176">De factuurnummers voor de vereffende facturen worden aaneengeschakeld en als remisegegevens gebruikt.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-176">The invoice numbers for the settled invoices are concatenated and used as the remittance information.</span></span> <span data-ttu-id="dcd9c-177">Overeenkomstig de ISO 20022-richtlijnen zijn de ongestructureerde remisegegevens beperkt tot 140 tekens.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-177">In compliance with ISO 20022 guidelines, unstructured remittance information is limited to 140 characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcd9c-178">Aantal facturen</span><span class="sxs-lookup"><span data-stu-id="dcd9c-178">Number of invoices</span></span></td>
<td><span data-ttu-id="dcd9c-179">Voer het aantal facturen in waarvoor het rapport <strong>Betalingsadvies</strong> wordt afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-179">Enter the number of invoices that the <strong>Payment advice</strong> report is printed from.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcd9c-180">Volgnummer</span><span class="sxs-lookup"><span data-stu-id="dcd9c-180">Sequence number</span></span></td>
<td><span data-ttu-id="dcd9c-181">Voer een volgnummer invoeren om het bestand te identificeren.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-181">Enter a sequence number to identify the file.</span></span> <span data-ttu-id="dcd9c-182">Het volgnummer wordt weergegeven op het rapport <strong>Bijbehorende notitie</strong>.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-182">The sequence number appears on the <strong>Attending note</strong> report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcd9c-183">Bijbehorende notitie afdrukken</span><span class="sxs-lookup"><span data-stu-id="dcd9c-183">Print attending note</span></span></td>
<td><span data-ttu-id="dcd9c-184">schakel dit selectievakje in om het rapport <strong>Bijbehorende notitie</strong> af te drukken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-184">Select this check box to print the <strong>Attending note</strong> report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcd9c-185">Controlerapport afdrukken</span><span class="sxs-lookup"><span data-stu-id="dcd9c-185">Print control report</span></span></td>
<td><span data-ttu-id="dcd9c-186">schakel dit selectievakje in om een rapport met de betalingsgegevens af te drukken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-186">Select this check box to print a report that contains the payment information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcd9c-187">Begeleidend schrijven afdrukken</span><span class="sxs-lookup"><span data-stu-id="dcd9c-187">Print covering letter</span></span></td>
<td><span data-ttu-id="dcd9c-188">Schakel dit selectievakje in om het rapport <strong>Betalingsadvies</strong> af te drukken.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-188">Select this check box to print the <strong>Payment advice</strong> report.</span></span></td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a><span data-ttu-id="dcd9c-189">Wat zijn IBAN en BIC?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-189">What are IBANs and BICs?</span></span>
<span data-ttu-id="dcd9c-190">Het IBAN-nummer (International Bank Account Number) en de BIC (Bank Identifier Code) worden gebruikt om alle rekeningen in vele landen/regio's over de hele wereld te identificeren.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-190">The International Bank Account Number (IBAN) and Bank Identifier Code (BIC) are used to identify any account in many countries/regions worldwide.</span></span> <span data-ttu-id="dcd9c-191">Deze omvatten onder meer de 34 SEPA-landen/-regio's.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-191">These include the 34 SEPA countries/regions.</span></span> <span data-ttu-id="dcd9c-192">Voer de BIC in in het veld **SWIFT-code** en de IBAN in het veld **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-192">Enter the BIC in the **SWIFT code** field and the IBAN in the **IBAN** field.</span></span> <span data-ttu-id="dcd9c-193">Voor zowel de bankrekening van de crediteur als de bankrekening van de klant bevinden deze velden zich op het sneltabblad **Aanvullende identificatie** op het tabblad **Bankrekening** op de pagina **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-193">For both the creditor’s bank account and the customer’s bank account, these fields are located on the **Additional identification** FastTab on the **Bank account** tab of the **Bank accounts** page.</span></span> <span data-ttu-id="dcd9c-194">Het gebruik van BIC voor SEPA-betalingen wordt niet langer afgedwongen.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-194">The use of BIC for SEPA payments is no longer enforced.</span></span>

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a><span data-ttu-id="dcd9c-195">Hoe verzend ik een betalingsbestand naar de bank?</span><span class="sxs-lookup"><span data-stu-id="dcd9c-195">How do I transmit a payment file to the bank?</span></span>
<span data-ttu-id="dcd9c-196">Wanneer u betalingen genereert, wordt het betalingsbestand gegenereerd, en u wordt gevraagd het vanaf uw webbrowser op te slaan op een beschikbare locatie.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-196">When you generate payments, the payment file is generated, and you're asked to save it from your web browser to any available location.</span></span> <span data-ttu-id="dcd9c-197">De volgende stap is het verzenden van het XML-bestand naar uw bank.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-197">The next step is to send the XML file to your bank.</span></span> <span data-ttu-id="dcd9c-198">Dit proces verschilt van bank tot bank.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-198">This process varies from bank to bank.</span></span> <span data-ttu-id="dcd9c-199">Volg de instructies van uw bank om de bestanden voor verwerking naar de bank te verzenden.</span><span class="sxs-lookup"><span data-stu-id="dcd9c-199">Follow the instructions from your bank to submit the files to the bank for processing.</span></span>


