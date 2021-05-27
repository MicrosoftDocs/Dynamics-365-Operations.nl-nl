---
title: Overzicht Indiase TDS (belasting ingehouden op bron)
description: Dit onderwerp biedt gedetailleerde informatie over Indiase TDS (belasting ingehouden op bron). In de TDS-documentatie wordt de functionaliteit van deze mogelijkheid behandeld.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023161"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="d1ceb-104">Overzicht Indiase TDS (belasting ingehouden op bron)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1ceb-105">Dit onderwerp biedt gedetailleerde informatie over Indiase TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="d1ceb-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="d1ceb-106">In de TDS-documentatie wordt de functionaliteit van deze mogelijkheid behandeld.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="d1ceb-107">Verder wordt uitgelegd hoe u de basisinstellingen voor TDS kunt instellen, TDS voor transacties kunt berekenen, het TDS-vereffeningsproces kunt voltooien, TDS-certificaatnummers kunt registreren en TDS-aanvragen, TDS-overzichten en TDS-certificaten kunt genereren.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="d1ceb-108">De documentatie bevat de volgende onderwerpen:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="d1ceb-109">Basisinstellingen voor TDS</span><span class="sxs-lookup"><span data-stu-id="d1ceb-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="d1ceb-110">Functionaliteit voor het ontwerpen van formules en drempellimieten die voor de TDS-berekening worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="d1ceb-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="d1ceb-111">Berekening van TDS op facturen, betalingen, promessen en intercompany-transacties</span><span class="sxs-lookup"><span data-stu-id="d1ceb-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="d1ceb-112">Periodiek TDS-vereffeningsproces en vereffening van TDS-bedragen aan TDS-dienstleveranciers</span><span class="sxs-lookup"><span data-stu-id="d1ceb-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="d1ceb-113">TDS-certificaatnummers en -datums registreren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="d1ceb-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="d1ceb-114">Inleiding op TDS</span><span class="sxs-lookup"><span data-stu-id="d1ceb-114">Introduction to TDS</span></span>

<span data-ttu-id="d1ceb-115">Volgens de Inkomstenbelasting act, 1961, wordt de inkomstenbelasting door de ontvanger van de service afgetrokken op het moment van vooruitbetaling of creditboeking, afhankelijk van wat zich het eerst voordoet.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="d1ceb-116">Degene die de betaling doet, moet het belastingbedrag aftrekken en moet alleen het nettosaldo aan de leverancier van de service betalen.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="d1ceb-117">TDS wordt toegepast op services die door de overheid zijn opgegeven en de belasting wordt afgetrokken met de tarieven die de overheid voor een periode opgeeft.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="d1ceb-118">Het inhoudingspercentage is gebaseerd op de status van de entiteit die de betaling ontvangt of de service verleent.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="d1ceb-119">De statussen zijn **Afzonderlijk**, **Hindu Undivided Family** (**HUF**), **Bedrijf**, **Firma**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**) en **Lokale dienst**.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="d1ceb-120">In de volgende secties worden de services vermeld waar TDS op wordt toegepast, zoals is opgegeven door de Indiase overheid.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="d1ceb-121">**Ingezetenen**</span><span class="sxs-lookup"><span data-stu-id="d1ceb-121">**Residents**</span></span>

- <span data-ttu-id="d1ceb-122">Inkomsten uit salarissen (onder sectie 192)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="d1ceb-123">Inkomsten uit rente op effecten (onder sectie 193)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="d1ceb-124">Inkomsten uit dividend (onder sectie 194)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="d1ceb-125">Inkomsten uit rente (onder sectie 194A)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="d1ceb-126">Inkomsten uit loterijen of puzzels (onder sectie 194B)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="d1ceb-127">Winst van paardenraces, enz. (onder sectie 194BB)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="d1ceb-128">Contractanten en subcontractanten (onder sectie 194C)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="d1ceb-129">Verzekeringsprovisie (onder sectie 194D)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="d1ceb-130">Inkomsten uit deposito onder nationale spaarregeling (onder sectie 194EE)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="d1ceb-131">Inkomsten uit wederzijdse fonds of UTI (Under section 194F)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="d1ceb-132">Provisie, vergoeding, prijs enzovoort door verkoop of loterij (onder sectie 194G)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="d1ceb-133">Betaling van provisie of bemiddeling (onder sectie 194H)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="d1ceb-134">Huur (onder sectie 194I)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="d1ceb-135">Professionele service (onder sectie 194J)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="d1ceb-136">Inkomsten uit participaties in beleggingsfondsen (onder sectie 194K)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="d1ceb-137">Betaling van compensatie bij aanschaf van bepaalde onroerende zaken (onder sectie 194LA)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="d1ceb-138">**Niet-ingezetenen**</span><span class="sxs-lookup"><span data-stu-id="d1ceb-138">**Non-residents**</span></span>

- <span data-ttu-id="d1ceb-139">Betalingen aan niet-ingezetene sportmensen of sportvereniging (onder sectie 194E)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="d1ceb-140">Overige gelden (onder sectie 195)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="d1ceb-141">Inkomsten betreffende participaties in beleggingsfondsen van niet-ingezetenen (onder sectie 196A)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="d1ceb-142">Inkomsten uit obligaties of aandelen in vreemde valuta van Indiaas bedrijf (onder sectie 196C)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="d1ceb-143">Inkomsten van buitenlandse investeerders uit effecten (onder sectie 196D)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="d1ceb-144">Salaris en alle andere positieve inkomsten onder elke inkomstenbroncategorie (sectie 192)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="d1ceb-145">Rente op effecten (sectie 193)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="d1ceb-146">Andere rente dan rente op effecten (sectie 194A)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="d1ceb-147">Betalingen aan contractanten en subcontractanten (sectie 194C)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="d1ceb-148">Winst van loterijen of kruiswoordpuzzels (sectie 194B)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="d1ceb-149">Winst van paardenraces (sectie 194BB)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="d1ceb-150">Verzekeringscommissie voor alle betalingen voor het aanschaffen van verzekeringsbedrijf (sectie 194D)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="d1ceb-151">Eventuele andere rente dan rente op effecten die aan niet-ingezetenen worden betaald die geen bedrijf of buitenlands bedrijf zijn (sectie 195)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="d1ceb-152">Betaling aan niet-ingezetene sportmensen, met inbegrip van sportvereniging of -instelling.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="d1ceb-153">Als het een niet-ingezetene sporter betreft, is dit inclusief betalingen met betrekking tot advertenties en artikelen over eventuele spelen/sporten in India in dagbladen, tijdschriften en dergelijke</span><span class="sxs-lookup"><span data-stu-id="d1ceb-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="d1ceb-154">(sectie 194E)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="d1ceb-155">Betaling met betrekking tot stortingen onder NSS \[National Savings Scheme, nationale spaarregeling\] (sectie 194EE)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="d1ceb-156">Betaling op basis van terugkoop van participaties door gemeenschappelijk beleggingsfonds of UTI (sectie 194F)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="d1ceb-157">Betaling voor provisie of bemiddeling (sectie 194H)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="d1ceb-158">Betaling van huur (sectie 194I)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="d1ceb-159">Betaling van vergoedingen voor professionele of technische diensten (sectie 194J)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="d1ceb-160">Provisie aan handelaars, distributeurs, inkopers en verkopers van loten inclusief vergoeding of prijs voor dergelijke loten (sectie 194G)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="d1ceb-161">Inkomsten uit ingekochte participaties in vreemde valuta of kapitaalwinst op lange termijn die voortvloeit uit de overboeking van dergelijke participaties in een vreemde valuta (sectie 196B)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="d1ceb-162">Betaling van inkomsten aan niet-ingezetenen betreffende rente of dividend op obligaties en aandelen (sectie 196C)</span><span class="sxs-lookup"><span data-stu-id="d1ceb-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="d1ceb-163">TDS wordt berekend over inkopen, verkopen, verkoopretouren, creditnota's, verwervingen van vaste activa, vooruitbetalingen, voorschotten, promessen, belasting op arbeid en intercompany-transacties.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="d1ceb-164">In het huidige Indiase belastingscenario wordt TDS niet berekend voor verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="d1ceb-165">Het systeem bevat echter een voorziening waarmee TDS kan worden berekend die terugvorderbaar is op verkooptransacties, met name voor intercompany-transacties.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="d1ceb-166">Bij de berekening van TDS wordt altijd rekening houden met de drempel en de uitzonderingsdrempel die voor de TDS-component is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="d1ceb-167">Het periodieke TDS-vereffeningsproces moet worden uitgevoerd en de TDS-betalingen moeten worden vereffend met leveranciers van de TDS-dienst.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="d1ceb-168">De certificaatnummers en -datums voor TDS-certificaten die worden ontvangen van leveranciers of klanten, kunnen worden geregistreerd en bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="d1ceb-169">Daarnaast kunnen Formulier 26Q- en Formulier 27Q-kwartaalopgaven en het Formulier 16A-certificaat voor TDS worden gegenereerd in Finance.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="d1ceb-170">TDS instellen en met TDS werken</span><span class="sxs-lookup"><span data-stu-id="d1ceb-170">Setting up and working with TDS</span></span>

<span data-ttu-id="d1ceb-171">Hieronder wordt een overzicht gegeven van het proces voor het instellen en werken met TDS:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="d1ceb-172">**TDS instellen:**</span><span class="sxs-lookup"><span data-stu-id="d1ceb-172">**TDS setup:**</span></span>

    - <span data-ttu-id="d1ceb-173">Parameters instellen:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-173">Parameter setup:</span></span>

        - <span data-ttu-id="d1ceb-174">Activeer in Grootboekparameters aan TDS gerelateerde parameters.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="d1ceb-175">In Grootboekparameters kunt u de nummerreeks voor bronbelastingbetalingen instellen.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="d1ceb-176">Stel parameters in voor Leveranciers en Klanten.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="d1ceb-177">Basisinstellingen:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-177">Basic setup:</span></span>

        - <span data-ttu-id="d1ceb-178">Stel TDS-registratienummers in voor een bedrijf, klanten en leveranciers.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="d1ceb-179">Stel TDS-componentgroepen in.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="d1ceb-180">Stel TDS-componenten in, koppel er TDS-componentgroepen aan en definieer de drempel en uitzonderingsdrempel voor deze componenten.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="d1ceb-181">Stel TDS-diensten in.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="d1ceb-182">Stel TDS-vereffeningsperioden in.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="d1ceb-183">Stel TDS-belastingcodes in en koppel er TDS-componenten aan.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="d1ceb-184">Stel TDS-belastinggroepen in en koppel er TDS-belastingcodes aan.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="d1ceb-185">Definieer in de formuleontwerper een formule voor het berekenen van TDS voor een TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="d1ceb-186">Registreer TDS-vrijstellingscertificaatnummers.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="d1ceb-187">Instellen van grootboekrekeningen en bedrijf:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="d1ceb-188">Stel TDS-grootboekrekeningen voor leveranciers en klanten in.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="d1ceb-189">Stel een TAN-nummer in voor belastinginhouding en belastinginning en een categorie voor het inhoudertype voor het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="d1ceb-190">Overige instellingen:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-190">Other setup:</span></span>

        - <span data-ttu-id="d1ceb-191">Stel een betalingsschema in inclusief TDS-toewijzing.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="d1ceb-192">Stel een type voor bijzondere betalingskosten in voor betalingen aan de TDS-dienst.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="d1ceb-193">Stel informatie in over TDS-groepen, permanente rekeningnummers (PAN's) en TAN's voor leveranciers en klanten.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="d1ceb-194">**Berekening van TDS in transacties:**</span><span class="sxs-lookup"><span data-stu-id="d1ceb-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="d1ceb-195">Facturen en betalingen</span><span class="sxs-lookup"><span data-stu-id="d1ceb-195">Invoices and payments</span></span>
    - <span data-ttu-id="d1ceb-196">Promessen</span><span class="sxs-lookup"><span data-stu-id="d1ceb-196">Promissory notes</span></span>
    - <span data-ttu-id="d1ceb-197">Voorschotten</span><span class="sxs-lookup"><span data-stu-id="d1ceb-197">Advance payments</span></span>
    - <span data-ttu-id="d1ceb-198">Vooruitbetalingen</span><span class="sxs-lookup"><span data-stu-id="d1ceb-198">Prepayments</span></span>

3. <span data-ttu-id="d1ceb-199">**TDS-vereffening:**</span><span class="sxs-lookup"><span data-stu-id="d1ceb-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="d1ceb-200">Periodiek TDS-vereffeningsproces</span><span class="sxs-lookup"><span data-stu-id="d1ceb-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="d1ceb-201">Vereffening van TDS-betalingen met TDS-dienstleveranciers en genereren van Challan voor TDS</span><span class="sxs-lookup"><span data-stu-id="d1ceb-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="d1ceb-202">**TDS-opvragen, -overzichten en -certificaat:**</span><span class="sxs-lookup"><span data-stu-id="d1ceb-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="d1ceb-203">Registreer TDS-certificaatnummers en -datums en werk ze bij.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="d1ceb-204">Genereer een TDS-opvraag en een geboekte TDS-opvraag.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="d1ceb-205">Genereer Formulier 27A, Formulier 26Q en Formulier 27Q voor TDS- en e-TDS-kwartaalopgave.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="d1ceb-206">Genereer een TDS-certificaat Formulier 27D.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-206">Generate a Form 16A TDS certificate.</span></span>
