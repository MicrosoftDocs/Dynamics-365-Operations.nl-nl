---
title: Uw lokale rekeningschema plannen
description: Dit onderwerp bevat informatie die u helpt om het rekeningschema te plannen wanneer u vereisten hebt voor wettelijke/lokale vereisten voor uw organisatie.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798291"
---
# <a name="plan-your-local-chart-of-accounts"></a>Uw lokale rekeningschema plannen

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie die u helpt om het rekeningschema te plannen wanneer uw organisatie rechtspersonen omvat die moeten voldoen aan vereisten voor specifieke locaties waar ze zaken doen. In dit onderwerp worden de volgende termen gebruikt om rekeningschema's te beschrijven:

- **Globaal**: het rekeningschema dat de organisatie globaal gebruikt. In de meeste gevallen consolideert u naar dit rekeningschema.
- **Lokaal**: een rekeningschema dat door rechtspersonen in een bepaald land of een bepaalde regio wordt gebruikt.
- **Gedeeld**: een rekeningschema dat door meerdere rechtspersonen kan worden gebruikt. Zowel het globale rekeningschema als het lokale rekeningschema kunnen worden gedeeld.

U kunt meerdere rekeningschema's maken en delen. Een gedeeld rekeningschema kan door meer dan één rechtspersoon worden gebruikt, maar er kan slechts één rekeningschema aan elke rechtspersoon worden toegewezen. Het rekeningschema dat door een rechtspersoon wordt gebruikt, wordt gedefinieerd op de pagina **Grootboek**.

Wanneer ze het rekeningschema ontwerpen, willen veel organisaties een globaal rekeningschema maken. Met het gedeelde rekeningschema kan een globaal rekeningschema worden gemaakt. Het maken en gebruiken van één rekeningschema heeft voordelen. Governance, beheer, onderhoud en rapportage zijn bijvoorbeeld eenvoudiger.

De meeste organisaties geven de voorkeur aan een globaal rekeningschema en het is het gemakkelijkst te implementeren. Sommige rechtspersonen vereisen echter een lokaal rekeningschema om de volgende redenen:

- Lokale wettelijke vereisten
- Vereisten van lokale boekhoudregels
- Branchevereisten
- Bedrijfsspecifieke rapportage- en analysevereisten

Als uw organisatie vereist dat een rechtspersoon een lokaal rekeningschema gebruikt, zijn er twee opties beschikbaar om dit te implementeren:

- Wijs het globale rekeningschema toe en definieer andere middelen om aan de lokale vereisten te voldoen.
- Wijs een lokaal rekeningschema aan de rechtspersoon toe en definieer relaties met het globale rekeningschema.

De gebruikte optie wordt bepaald door de organisatiestructuur en de rapportagestructuur.

[![Diagram waarin wordt weergegeven hoe de organisatiestructuur bepaalt of een globaal of lokaal rekeningschema moet worden gebruikt](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Als het globale rekeningschema aan de rechtspersoon is toegewezen, zijn de volgende opties beschikbaar om aan lokale rapportagevereisten te voldoen:

- Voer lokale consolidatie uit.
- Gebruik een financiële dimensie om het lokale rekeningschema bij te houden.
- Maak lokale hoofdrekeningen in het globale rekeningschema.
- Voer een externe toewijzing aan het lokale rekeningschema uit.

Als er een lokaal rekeningschema aan de rechtspersoon wordt toegewezen, is momenteel alleen de optie voor globale consolidatie beschikbaar om aan de globale rapportagevereisten te voldoen.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Globaal rekeningschema dat aan een rechtspersoon is toegewezen

Als u het globale rekeningschema aan een rechtspersoon moet toewijzen, zijn er vier opties beschikbaar voor het configureren van het systeem, zoals eerder is beschreven. Voor alle vier opties wordt één rekeningschema geconfigureerd en aan elke rechtspersoon gekoppeld op de pagina **Grootboek**. Bij elke optie wordt vervolgens een andere benadering om aan de lokalisatievereisten te voldoen. In de volgende secties worden de stappen op hoog niveau beschreven om het systeem voor de lokalisatievereisten te configureren. In de secties wordt ook beschreven wat de voordelen en nadelen van elke optie zijn.

### <a name="do-local-consolidation"></a>Lokale consolidatie uitvoeren.

Lokale consolidatie is de aanbevolen methode om aan de vereisten van lokale rekeningschema's te voldoen en om te profiteren van de systeemfunctionaliteit die voor dit doel is ontworpen.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Consolidatie instellen voor een lokaal rekeningschema

1. Maak één globaal rekeningschema met alle vereiste hoofdrekeningen.
2. Wijs in elke rechtspersoon het globale rekeningschema toe op de pagina **Grootboek**.
3. Maak een consolidatierechtspersoon voor elke benodigde lokalisatie.
4. Volg één van deze stappen:

    - Als er slechts één lokalisatie is vereist, configureert u de consolidatierekening op de pagina **Hoofdrekening** of gebruikt u de pagina's **Consolidatiegroepen** en **Aanvullende consolidatierekeningen**.
    - Als er meer dan een lokalisatie is vereist of als zowel het rekeningnummer als de rekeningnaam moeten worden omgezet, gebruikt u de pagina's **Consolidatiegroepen** en **Aanvullende consolidatierekeningen** om de lokalisatievereisten te vertegenwoordigen.

5. Voer het consolidatieproces uit om de waarde om te zetten van de bronrechtspersoon die het globale rekeningschema gebruikt naar het consolidatiebedrijf dat het lokale rekeningschema gebruikt.

#### <a name="advantages"></a>Voordelen

- Deze benadering biedt een consistente manier van werken in de hele organisatie.
- Er wordt één omzetting van de lokale positie uitgevoerd.
- Deze benadering ondersteunt de omzetting van zowel de hoofdrekening-id als de naam van elke hoofdrekening.
- De benadering ondersteunt meerdere lokalisaties.

#### <a name="disadvantages"></a>Nadelen

- Er wordt een extra consolidatiebedrijf gemaakt.
- Er wordt een extra consolidatieproces voltooid.
- Deze benadering kan alleen over het gelokaliseerde diagram rapporteren nadat het consolidatieproces is voltooid.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Een financiële dimensie gebruiken om het lokale rekeningschema bij te houden

Bij deze benadering wordt een financiële dimensie gebruikt waarbij de waarden van financiële dimensies de lokale hoofdrekeningen vertegenwoordigen die voor de lokalisatie zijn vereist. Deze benadering werkt goed als er slechts één lokalisatie is vereist. De benadering wordt echter minder bruikbaar naarmate u meer lokalisaties en financiële dimensies toevoegt.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Een financiële dimensie instellen voor een lokaal rekeningschema

1. Maak één globaal rekeningschema met alle vereiste hoofdrekeningen.
2. Wijs in elke rechtspersoon het globale rekeningschema toe op de pagina **Grootboek**.
3. Maak een financiële dimensie die het lokale rekeningschema vertegenwoordigt.
4. Maak waarden voor financiële dimensies die de hoofdrekeningen in het lokale rekeningschema vertegenwoordigen.
5. Werk de rekeningstructuur bij zodat deze de financiële dimensie van het 'lokale rekeningschema' bevat.
6. Zorg ervoor dat de financiële dimensie van het 'lokale rekeningschema' altijd een waarde heeft en dat er geen lege waarde is toegestaan. U kunt ook afgeleide dimensies of vaste dimensies overwegen.
7. Maak een set met financiële dimensies waarbij de financiële dimensie 'lokaal rekeningschema' de eerste geselecteerde financiële dimensie is. De set met financiële dimensies kan worden gebruikt wanneer de proefbalans wordt gegenereerd.

#### <a name="advantages"></a>Voordelen

- De hoofdrekeningen van zowel globale als lokale rekeningschema's bestaan op transactieniveau. De hoofdrekening is globaal en de waarde van de financiële dimensie is lokaal.
- Deze benadering biedt realtime rapportage en weergaven van zowel de globale financiële positie als de lokale financiële positie.

#### <a name="disadvantages"></a>Nadelen

- In Grootboekparameters worden, als het veld **Waarden gebruikt voor totaalrekening** is ingesteld op **Boekhoudingsverdelingen**, de financiële dimensies die de hoofdrekening voor de onkosten/activa/opbrengsten vertegenwoordigen, niet goed gebruikt voor de totaalrekeningen Klanten en Leveranciers. We raden u aan om in plaats daarvan het veld in te stellen op een brondocument om er zeker van te zijn dat de juiste waarden voor financiële dimensies worden gebruikt.
- Als er een groot aantal lokale rekeningschema's zijn vereist zijn en er wordt één financiële dimensie voor al deze schema's gebruikt, kan de lijst met waarden van financiële dimensies die worden gebruikt lang worden en moeilijk om mee te werken.
- Als er een groot aantal lokale rekeningschema's vereist is en er een afzonderlijke financiële dimensie wordt gebruikt om elk schema te vertegenwoordigen, kan dit van invloed zijn op de bruikbaarheid en prestaties van het systeem wanneer er financiële dimensies en sets met financiële dimensies worden toegevoegd.
- We raden u aan om goed na te gaan hoeveel financiële dimensies u nodig hebt, hoeveel waarden u aan elke dimensie toevoegt en hoeveel sets met financiële dimensies u toevoegt, omdat al deze factoren de systeemprestaties kunnen beïnvloeden.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Lokale hoofdrekeningen maken in het globale rekeningschema

*Waar de kopie-editor om heeft gevraagd*: in deze benadering omvatten de lokale hoofdrekeningen in het globale rekeningschema de hoofdrekeningen in het lokale rekeningschema in het globale rekeningschema.

*Oorspronkelijke versie*: de lokale hoofdrekeningen in de globale CoA-benadering is dat de lokale CoA-hoofdrekeningen worden opgenomen in de globale CoA.

*Moet het dit zijn*: bij deze benadering worden de lokale hoofdrekeningen in het lokale rekeningschema opgenomen in het globale rekeningschema.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Lokale hoofdrekeningen instellen in het globale rekeningschema

1. Maak één rekeningschema met de hoofdrekeningen voor zowel het globale rekeningschema als het lokale rekeningschema.
2. Wijs in elke rechtspersoon het rekeningschema toe op de pagina **Grootboek**.
3. Maak totaalrekeningen in het rekeningschema om de hoofdrekeningen met hetzelfde doel op te tellen.
4. Maak overschrijvingen van rechtspersonen voor elke lokale rekening om transacties te voorkomen van andere rechtspersonen waarvoor de lokale rekening niet is ontworpen.
5. Maak overschrijvingen van rechtspersonen voor elke globale rekening om transacties van de rechtspersonen van lokalisaties te voorkomen.

#### <a name="advantages"></a>Voordelen

- Een realtime weergave van zowel de globale financiële positie als de lokale financiële positie is beschikbaar in specifieke rapporten en in specifieke weergaven in het systeem, zoals een financieel rapport van de balans. De weergave kan ook worden geopend via de knop **Periode** op de totaalrekening.
- U hebt geen extra segment in de grootboekrekening.

#### <a name="disadvantages"></a>Nadelen

- Gebruik en zichtbaarheid van totaalrekening zijn beperkt. Totaalrekeningen zijn bijvoorbeeld niet zichtbaar op de lijstpagina **Proefbalans**.
- Onderhoud vereist extra inspanning.
- Het maken van financiële rapporten vereist extra handmatige inzet.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Externe toewijzing uitvoeren aan het lokale rekeningschema

Bij ingebruikname van een globaal rekeningschema wordt aangenomen dat u de toewijzing en lokalisaties buiten het systeem beheert. Bij deze benadering maakt u slechts één globaal rekeningschema in Microsoft Dynamics 365 Finance en verwerkt u de vereisten buiten het systeem.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Externe toewijzing instellen aan een lokaal rekeningschema

1. Maak één globaal rekeningschema met alle vereiste hoofdrekeningen.
2. Wijs in elke rechtspersoon het globale rekeningschema toe op de pagina **Grootboek**.
3. Voer de toewijzing aan het lokale rekeningschema uit buiten Finance

#### <a name="advantages"></a>Voordelen

- Deze benadering biedt consistente manieren van werken in de hele organisatie.

#### <a name="disadvantages"></a>Nadelen

- Er is geen lokale rapportage beschikbaar vanuit het systeem.
- Deze benadering is foutgevoelig bij het maken van financiële rapporten.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Lokaal rekeningschema dat aan een rechtspersoon is toegewezen

Als uw organisatie besluit om geen globaal rekeningschema voor alle rechtspersonen te gebruiken, wordt er een afzonderlijk rekeningschema gemaakt voor elk unieke, lokale rekeningschema. Elke rechtspersoon wordt vervolgens gekoppeld aan het bijbehorende rekeningschema op de pagina **Grootboek**.

### <a name="do-global-consolidation"></a>Globale consolidatie uitvoeren

Bij deze benadering wordt een consolidatiebedrijf gebruikt om de saldi van elk lokaal bronbedrijf te totaliseren en te combineren in het gecombineerde globale rekeningschema in het consolidatiebedrijf. Bij deze benadering moet u een toewijzing onderhouden van elk lokale rekeningschema aan het globale rekeningschema in het consolidatiebedrijf.

#### <a name="set-up-global-consolidation"></a>Globale consolidatie instellen

1. Maak een afzonderlijk rekeningschema voor elke rechtspersoon met een ander lokaal rekeningschema. Als rechtspersonen hetzelfde lokale rekeningschema hebben, is slechts één lokaal rekeningschema vereist en dit schema kan worden gedeeld.
2. Wijs in elke rechtspersoon het juiste rekeningschema toe op de pagina **Grootboek**.
3. Optioneel: maak een rekeningschema voor het globale rekeningschema van elk consolidatiebedrijf met een ander globaal rekeningschema.
4. Maak een consolidatierechtspersoon voor elk consolidatieniveau dat is vereist en wijs het juiste rekeningschema toe aan de pagina **Grootboek**.
5. Volg één van deze stappen:

    - Als er slechts één consolidatie nodig is, configureert u de consolidatierekening op de pagina **Hoofdrekening**.
    - Als er meer dan een consolidatie is vereist of als zowel het rekeningnummer als de rekeningnaam moeten worden omgezet, gebruikt u de pagina's **Consolidatiegroepen** en **Aanvullende consolidatierekeningen** om de vereisten voor het globale rekeningschema te vertegenwoordigen.

6. Voer het consolidatieproces uit om de saldi van de lokale rechtspersonen over te brengen naar de geconsolideerde rechtspersoon. Deze geconsolideerde rechtspersoon gebruikt de consolidatierekeningen die u in stap 5 hebt gedefinieerd.

#### <a name="advantages"></a>Voordelen

- De indeling voor lokale boekhoudregels wordt toegepast.
- Met deze aanpak kan het lokale financiële team gemakkelijker werken.

#### <a name="disadvantages"></a>Nadelen

- Er is geen realtime weergave van de globale positie beschikbaar.
- Het consolidatieproces wordt mogelijk vaker uitgevoerd.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Uw rekeningschema plannen](plan-chart-of-accounts.md)
- [Grootboeken configureren](configure-ledger.md)
- [Financiële dimensies en boeken](Default-dimensions.md#balancing-dimension)
- [Financiële-dimensiesets](financial-dimension-sets.md)
- [Overzicht van consolidatie en schrapping](../budgeting/consolidation-elimination-overview.md)
- [Groep met consolidatierekeningen en extra consolidatierekeningen](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
