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
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Overzicht Indiase TDS (belasting ingehouden op bron)

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt gedetailleerde informatie over Indiase TDS (belasting ingehouden op bron).

In de TDS-documentatie wordt de functionaliteit van deze mogelijkheid behandeld. Verder wordt uitgelegd hoe u de basisinstellingen voor TDS kunt instellen, TDS voor transacties kunt berekenen, het TDS-vereffeningsproces kunt voltooien, TDS-certificaatnummers kunt registreren en TDS-aanvragen, TDS-overzichten en TDS-certificaten kunt genereren. De documentatie bevat de volgende onderwerpen:

- [Basisinstellingen voor TDS](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Functionaliteit voor het ontwerpen van formules en drempellimieten die voor de TDS-berekening worden gebruikt](apac-ind-TDS-Formula-designer.md)
- [Berekening van TDS op facturen, betalingen, promessen en intercompany-transacties](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Periodiek TDS-vereffeningsproces en vereffening van TDS-bedragen aan TDS-dienstleveranciers](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS-certificaatnummers en -datums registreren en bijwerken](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Inleiding op TDS

Volgens de Inkomstenbelasting act, 1961, wordt de inkomstenbelasting door de ontvanger van de service afgetrokken op het moment van vooruitbetaling of creditboeking, afhankelijk van wat zich het eerst voordoet. Degene die de betaling doet, moet het belastingbedrag aftrekken en moet alleen het nettosaldo aan de leverancier van de service betalen. TDS wordt toegepast op services die door de overheid zijn opgegeven en de belasting wordt afgetrokken met de tarieven die de overheid voor een periode opgeeft. Het inhoudingspercentage is gebaseerd op de status van de entiteit die de betaling ontvangt of de service verleent. De statussen zijn **Afzonderlijk**, **Hindu Undivided Family** (**HUF**), **Bedrijf**, **Firma**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**) en **Lokale dienst**.

In de volgende secties worden de services vermeld waar TDS op wordt toegepast, zoals is opgegeven door de Indiase overheid.

**Ingezetenen**

- Inkomsten uit salarissen (onder sectie 192)
- Inkomsten uit rente op effecten (onder sectie 193)
- Inkomsten uit dividend (onder sectie 194)
- Inkomsten uit rente (onder sectie 194A)
- Inkomsten uit loterijen of puzzels (onder sectie 194B)
- Winst van paardenraces, enz. (onder sectie 194BB)
- Contractanten en subcontractanten (onder sectie 194C)
- Verzekeringsprovisie (onder sectie 194D)
- Inkomsten uit deposito onder nationale spaarregeling (onder sectie 194EE)
- Inkomsten uit wederzijdse fonds of UTI (Under section 194F)
- Provisie, vergoeding, prijs enzovoort door verkoop of loterij (onder sectie 194G)
- Betaling van provisie of bemiddeling (onder sectie 194H)
- Huur (onder sectie 194I)
- Professionele service (onder sectie 194J)
- Inkomsten uit participaties in beleggingsfondsen (onder sectie 194K)
- Betaling van compensatie bij aanschaf van bepaalde onroerende zaken (onder sectie 194LA)

**Niet-ingezetenen**

- Betalingen aan niet-ingezetene sportmensen of sportvereniging (onder sectie 194E)
- Overige gelden (onder sectie 195)
- Inkomsten betreffende participaties in beleggingsfondsen van niet-ingezetenen (onder sectie 196A)

    - Inkomsten uit obligaties of aandelen in vreemde valuta van Indiaas bedrijf (onder sectie 196C)
    - Inkomsten van buitenlandse investeerders uit effecten (onder sectie 196D)
    - Salaris en alle andere positieve inkomsten onder elke inkomstenbroncategorie (sectie 192)
    - Rente op effecten (sectie 193)
    - Andere rente dan rente op effecten (sectie 194A)
    - Betalingen aan contractanten en subcontractanten (sectie 194C)
    - Winst van loterijen of kruiswoordpuzzels (sectie 194B)
    - Winst van paardenraces (sectie 194BB)
    - Verzekeringscommissie voor alle betalingen voor het aanschaffen van verzekeringsbedrijf (sectie 194D)
    - Eventuele andere rente dan rente op effecten die aan niet-ingezetenen worden betaald die geen bedrijf of buitenlands bedrijf zijn (sectie 195)
    - Betaling aan niet-ingezetene sportmensen, met inbegrip van sportvereniging of -instelling. Als het een niet-ingezetene sporter betreft, is dit inclusief betalingen met betrekking tot advertenties en artikelen over eventuele spelen/sporten in India in dagbladen, tijdschriften en dergelijke (sectie 194E)
    - Betaling met betrekking tot stortingen onder NSS \[National Savings Scheme, nationale spaarregeling\] (sectie 194EE)
    - Betaling op basis van terugkoop van participaties door gemeenschappelijk beleggingsfonds of UTI (sectie 194F)
    - Betaling voor provisie of bemiddeling (sectie 194H)
    - Betaling van huur (sectie 194I)
    - Betaling van vergoedingen voor professionele of technische diensten (sectie 194J)
    - Provisie aan handelaars, distributeurs, inkopers en verkopers van loten inclusief vergoeding of prijs voor dergelijke loten (sectie 194G)
    - Inkomsten uit ingekochte participaties in vreemde valuta of kapitaalwinst op lange termijn die voortvloeit uit de overboeking van dergelijke participaties in een vreemde valuta (sectie 196B)
    - Betaling van inkomsten aan niet-ingezetenen betreffende rente of dividend op obligaties en aandelen (sectie 196C)

TDS wordt berekend over inkopen, verkopen, verkoopretouren, creditnota's, verwervingen van vaste activa, vooruitbetalingen, voorschotten, promessen, belasting op arbeid en intercompany-transacties.

> [!NOTE]
> In het huidige Indiase belastingscenario wordt TDS niet berekend voor verkooptransacties. Het systeem bevat echter een voorziening waarmee TDS kan worden berekend die terugvorderbaar is op verkooptransacties, met name voor intercompany-transacties.

Bij de berekening van TDS wordt altijd rekening houden met de drempel en de uitzonderingsdrempel die voor de TDS-component is gedefinieerd.

Het periodieke TDS-vereffeningsproces moet worden uitgevoerd en de TDS-betalingen moeten worden vereffend met leveranciers van de TDS-dienst.

De certificaatnummers en -datums voor TDS-certificaten die worden ontvangen van leveranciers of klanten, kunnen worden geregistreerd en bijgewerkt. Daarnaast kunnen Formulier 26Q- en Formulier 27Q-kwartaalopgaven en het Formulier 16A-certificaat voor TDS worden gegenereerd in Finance.

## <a name="setting-up-and-working-with-tds"></a>TDS instellen en met TDS werken

Hieronder wordt een overzicht gegeven van het proces voor het instellen en werken met TDS:

1. **TDS instellen:**

    - Parameters instellen:

        - Activeer in Grootboekparameters aan TDS gerelateerde parameters.
        - In Grootboekparameters kunt u de nummerreeks voor bronbelastingbetalingen instellen.
        - Stel parameters in voor Leveranciers en Klanten.

    - Basisinstellingen:

        - Stel TDS-registratienummers in voor een bedrijf, klanten en leveranciers.
        - Stel TDS-componentgroepen in.
        - Stel TDS-componenten in, koppel er TDS-componentgroepen aan en definieer de drempel en uitzonderingsdrempel voor deze componenten.
        - Stel TDS-diensten in.
        - Stel TDS-vereffeningsperioden in.
        - Stel TDS-belastingcodes in en koppel er TDS-componenten aan.
        - Stel TDS-belastinggroepen in en koppel er TDS-belastingcodes aan.
        - Definieer in de formuleontwerper een formule voor het berekenen van TDS voor een TDS-groep.
        - Registreer TDS-vrijstellingscertificaatnummers.

    - Instellen van grootboekrekeningen en bedrijf:

        - Stel TDS-grootboekrekeningen voor leveranciers en klanten in.
        - Stel een TAN-nummer in voor belastinginhouding en belastinginning en een categorie voor het inhoudertype voor het bedrijf.

    - Overige instellingen:

        - Stel een betalingsschema in inclusief TDS-toewijzing.
        - Stel een type voor bijzondere betalingskosten in voor betalingen aan de TDS-dienst.
        - Stel informatie in over TDS-groepen, permanente rekeningnummers (PAN's) en TAN's voor leveranciers en klanten.

2. **Berekening van TDS in transacties:**

    - Facturen en betalingen
    - Promessen
    - Voorschotten
    - Vooruitbetalingen

3. **TDS-vereffening:**

    - Periodiek TDS-vereffeningsproces
    - Vereffening van TDS-betalingen met TDS-dienstleveranciers en genereren van Challan voor TDS

4. **TDS-opvragen, -overzichten en -certificaat:**

    - Registreer TDS-certificaatnummers en -datums en werk ze bij.
    - Genereer een TDS-opvraag en een geboekte TDS-opvraag.
    - Genereer Formulier 27A, Formulier 26Q en Formulier 27Q voor TDS- en e-TDS-kwartaalopgave.
    - Genereer een TDS-certificaat Formulier 27D.
