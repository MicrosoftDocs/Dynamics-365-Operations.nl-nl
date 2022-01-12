---
title: Kassafunctionaliteit voor Noorwegen
description: Dit onderwerp biedt een overzicht van de kassafunctionaliteit die beschikbaar is voor Noorwegen in Microsoft Dynamics 365 Commerce en geeft richtlijnen voor het instellen van de functionaliteit.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: bb87b3a7405ef3d8435748813fa66db74b8f0971
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944935"
---
# <a name="cash-register-functionality-for-norway"></a>Kassafunctionaliteit voor Noorwegen

[!include[banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van de kassafunctionaliteit die beschikbaar is voor Noorwegen in Dynamics 365 Commerce. Daarnaast bevat het richtlijnen voor het instellen van de functionaliteit. De functionaliteit bestaat uit de volgende onderdelen:

- Algemene POS-functies (Point-of-Sale) die beschikbaar zijn voor klanten in alle landen of regio's. Een voorbeeld is de optie waarmee u kunt voorkomen dat een kopie van een ontvangstbewijs meerdere keer wordt afgedrukt.
- Specifieke functies voor Noorwegen, zoals digitale handtekeningen voor verkooptransacties.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Overzicht van kassafunctionaliteit voor Noorwegen

### <a name="common-pos-features"></a>Algemene POS-functies

Zie de [Help-resources voor Dynamics 365 Retail](../index.md) voor meer informatie over POS-functies die beschikbaar zijn voor klanten in alle landen of regio's.

De volgende POS-localisatiefuncties die eerder zijn geïmplementeerd en beschikbaar zijn gesteld aan klanten in alle landen of regio's, kunnen nu specifiek voor Noorwegen worden gebruikt:

- **Het afdrukken van tekstvelden op een ontvangstbewijs met een grote tekengrootte.** Met de parameter **Tekengrootte** in de ontwerper voor ontvangstbewijzen kunt u opgeven dat de grote tekengrootte moet worden gebruikt voor een veld in de ontvangstbewijsindeling. (De grote tekengrootte is ongeveer twee keer zo groot als de normale tekengrootte.) U kunt deze parameter bijvoorbeeld gebruiken om in grote tekens de aanduiding Kopie af te drukken op een kopie van een ontvangstbewijs.
- **Het afdrukken van kopieën van ontvangstbewijzen registreren in het gebeurtenislogboek van de POS-controle.** Met de parameter **Controle** in het POS-functionaliteitsprofiel kunt u kopieën van ontvangstbewijzen afdrukken en andere POS-controlegebeurtenissen registreren. De controlegebeurtenissen worden geregistreerd in de kanaaldatabase en in Headquarters. U kunt de controlegebeurtenissen bekijken op de pagina **Controlegebeurtenissen**.
- **Voorkomen dat een kopie van een ontvangstbewijs meerdere keer wordt afgedrukt.** Wanneer de parameter **Controle** in het POS-functionaliteitsprofiel is ingeschakeld, bepaalt de POS-machtiging **Afdrukken van kopieën van ontvangstbewijzen toestaan** of kopieën van ontvangstbewijzen kunnen worden afgedrukt. Er is ook een optie waarmee u kunt voorkomen dat een kopie van een ontvangstbewijs meerdere keer wordt afgedrukt.

Daarnaast is de volgende POS-functie geïmplementeerd voor Noorwegen, maar beschikbaar gemaakt voor klanten in alle landen of regio's:

- **Extra gebeurtenissen registreren in het gebeurtenislogboek van de POS-controle.** Als de parameter **Controle** in het POS-functionaliteitsprofiel is ingeschakeld, worden de volgende gebeurtenissen geregistreerd in het gebeurtenislogboek van de POS-controle:

    - Prijscontroles
    - Btw-overschrijvingen
    - Correcties van regelhoeveelheden
    - Vereffeningstransacties uit de kanaaldatabase

### <a name="norway-specific-pos-features"></a>Specifieke POS-functies voor Noorwegen

De volgende POS-functies die specifiek zijn voor Noorwegen worden ingeschakeld wanneer de parameter **ISO-code** in het POS-functionaliteitsprofiel is ingesteld op **Nee**.

#### <a name="digital-signing-of-sales-transactions"></a>Digitale ondertekening van verkooptransacties

Elke verkooptransactie wordt digitaal ondertekend. De handtekening wordt gemaakt en vastgelegd in het POS-transactiejournaal op het moment dat de transactie wordt afgerond. De handtekening is ook beschikbaar in het journaal dat wordt geëxporteerd voor controledoeleinden.

Alleen transacties voor contante verkopen worden ondertekend. Hieronder staan enkele voorbeelden van transacties die zijn uitgesloten van het ondertekeningsproces:

- Vooruitbetalingen (klantrekeningstorting)
- Vooruitbetalingen voor verkooporders (klantorderstorting)
- Uitgifte van een geschenkbon
- Niet-verkooptransacties (wisselgeldinvoer, verwijdering van wisselgeld enzovoort)

De gegevens die worden ondertekend, zijn een tekstreeks die uit de volgende gegevensvelden bestaat. De gegevensvelden worden gescheiden door puntkomma's.

1. Vorige handtekening voor hetzelfde POS (Er wordt een nul \[**0**\] gebruikt voor de eerste transactie.)
2. Transactiedatum
3. Transactietijd
4. Opeenvolgend ondertekend transactienummer
5. Transactiebedrag inclusief btw
6. Transactiebedrag exclusief btw

Het digitale ondertekeningsproces gebruikt een 1024-bits RSA-code met een SHA-1-hashfunctie (RSA-SHA1-1024). Een certificaat dat is geïnstalleerd op de Commerce Scale Unit wordt gebruikt voor het ondertekenen. De unieke id van het certificaat (footprint) wordt samen met de handtekening vastgelegd.

De handtekening wordt samen met de transactiegegevens opgeslagen in de winkeldatabase en de HQ-database (Headquarters). U kunt de transactiehandtekening, samen met de transactiegegevens die zijn gebruikt om deze te genereren, bekijken op het sneltabblad **Fiscale transacties** van de pagina **Winkeltransacties**.

#### <a name="receipts"></a>Ontvangstbewijzen

Ontvangstbewijzen voor Noorwegen kunnen aanvullende informatie bevatten die is geïmplementeerd via aangepaste velden:

- **Titel ontvangstbewijs**: u kunt een veld toevoegen aan een indeling voor ontvangstbewijzen om het type ontvangstbewijs aan te geven. Een ontvangstbewijs bij verkopen bevat bijvoorbeeld de tekst 'Ontvangstbewijs bij verkopen'.
- **Ondertekend transactienummer**: het opeenvolgende nummer van een ondertekende transactie kan op het ontvangstbewijs worden weergegeven om een afgedrukt ontvangstbewijs aan een digitale handtekening in de database te koppelen.
- **Ontvangsttotalen**: aangepaste velden voor ontvangsttotalen exclusief niet-verkoopbedragen van totale transactiebedragen. Niet-verkoopbedragen omvatten bedragen voor de volgende bewerkingen:

    - Vooruitbetalingen (klantrekeningstorting)
    - Vooruitbetalingen voor verkooporders (klantorderstorting)
    - Uitgifte van een geschenkbon
    - Bedragen toevoegen aan een geschenkbon

#### <a name="x-and-z-reports"></a>X- en Z-rapporten

De informatie op X- en Z-rapporten is gebaseerd op de vereisten voor Noorwegen. De **totale contante verkoopbedragen** omvatten bijvoorbeeld alleen bedragen voor contante verkooptransacties en geen bewerkingen voor de uitgifte van geschenkbonnen en vooruitbetalingen. De totale contante verkoop wordt ook vermeld per artikelgroep en betalingsmethode. Bovendien worden cumulatieve totaalbedragen voor **Eindtotaal verkopen** en **Eindtotaal retouren** onderhouden en afgedrukt.

#### <a name="saf-t-cash-register-audit-file"></a>SAF-T-auditfile voor kassa's

U kunt het POS-transactiejournaal exporteren in de vooraf gedefinieerde indeling Standaard auditfile voor belasting (SAF-T) voor kassa's. Het auditfile bevat informatie over de organisatie, relevante hoofdgegevens (zoals artikelgroepen, artikelen en btw-codes), gegevens over contante verkooptransacties en handtekeningen voor die transacties, gegevens over niet-verkoopgebeurtenissen en gegevens voor eindedagsrapporten.

Het auditfile kan voor de volgende scenario's worden geëxporteerd:

- Per winkel
- Alle winkels
- Per terminal
- Alle terminals

U kunt ook een rapport van een rechtspersoon namens een andere rechtspersoon verzenden. In dit geval moet u de export uitvoeren vanuit de werkende rechtspersoon en de rapporterende rechtspersoon opgeven als de afzender van het rapport.

De SAF-T-indeling voor kassa's is geïmplementeerd in Headquarters met behulp van [Elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Commerce instellen voor Noorwegen

In deze sectie worden de instellingen beschreven die specifiek en aanbevolen zijn voor Noorwegen. Zie [Help-bronnen voor Dynamics 365 Retail](../index.md) voor meer informatie.

Als u de specifieke functionaliteit voor Noorwegen wilt gebruiken, moet u de volgende taken uitvoeren:

- Stel het veld **Land/regio** in op **NOR** (Noorwegen) in het primaire adres van de rechtspersoon.
- Stel het veld **ISO-code** in **NO** (Noorwegen) in het POS-functionaliteitsprofiel van elke winkel die zich in Noorwegen bevindt.

U moet ook de volgende instellingen opgeven voor Noorwegen.

### <a name="set-up-the-legal-entity"></a>De echtspersoon instellen

Zorg ervoor dat de naam van de rechtspersoon is opgegeven. Deze naam wordt afgedrukt op X- en Z-rapporten.

Geef bovendien op het sneltabblad **Bankrekeninggegevens** in het veld **Routenummer** het organisatienummer op.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Belasting toegevoegde waarde (btw) instellen volgens de vereisten voor Noorwegen


U moet btw-codes, btw-groepen en btw-groepen voor artikelen maken. U moet ook btw-gegevens instellen voor producten en services. Zie [Btw-overzicht](../../finance/general-ledger/indirect-taxes-overview.md) voor meer informatie over het instellen en gebruiken van btw.

U moet ook btw-groepen opgeven en de optie **Prijzen zijn inclusief belasting** inschakelen voor winkels in Noorwegen.

### <a name="set-up-functionality-profiles"></a>Functionaliteitsprofielen instellen

U moet controle inschakelen en ontvangstbewijsnummering instellen.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>POS-machtigingsgroepen en afzonderlijke machtigingsinstellingen bijwerken voor winkelmedewerkers

Stel de machtiging **Afdrukken van kopie van ontvangstbewijs toestaan** in op een geschikte waarde:

- **Altijd toestaan**: de operator kan meerdere keren een kopie van een ontvangstbewijs afdrukken.
- **Slechts eenmaal toestaan**: de operator kan slechts eenmaal een kopie van een ontvangstbewijs afdrukken.
- **Slechts één keer toestaan, en alleen als HQ DB beschikbaar is**: de operator kan slechts eenmaal een kopie van een ontvangstbewijs afdrukken en uitsluitend als de HQ-database beschikbaar is via Commerce Data Exchange, zodat het systeem kan verifiëren dat het ontvangstbewijs voorheen in geen enkele winkel is afgedrukt.
- **Nooit**: de operator kan geen kopie van een ontvangstbewijs afdrukken.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Aangepaste velden configureren zodat ze kunnen worden gebruikt in ontvangstbewijsindelingen

Voeg op de pagina **Taaltekst** de volgende records toe voor de labels van de aangepaste velden voor ontvangstbewijsindelingen. De waarden **Taal-id**, **Tekst-ID** en **Tekst** die in de tabel worden weergegeven, zijn slechts voorbeelden. U kunt ze eenvoudig wijzigen zodat ze aan uw behoeften voldoen.

| Taal-ID | Tekst                   | Tekst-id |
|-------------|------------------------|---------|
| nl       | Titel van ontvangstbewijs          | 900011  |
| nl       | Is geschenkbon           | 900012  |
| nl       | Totaal (verkoop)          | 900013  |
| nl       | Totaal btw (verkoop)      | 900014  |
| nl       | Totaal met btw (verkoop) | 900015  |
| nl       | Btw-bedrag (verkoop)     | 900016  |
| nl       | Id contante transactie    | 900017  |

Voeg op de pagina **Aangepaste velden** de volgende records toe voor de aangepaste velden voor ontvangstbewijsindelingen. Opmerking: waarden voor **Bijschrifttekst-id** moeten overeenkomen met de waarden voor **tekst-id's** die u hebt opgegeven op de pagina **Taaltekst**.

| Name                            | Type    | Tekst-id bijschrift |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Ontvangst | 900011          |
| IsGiftCard                      | Ontvangst | 900012          |
| SalesTotalExt                   | Ontvangst | 900013          |
| TaxTotalExt                     | Ontvangst | 900014          |
| TotalWithTaxExt                 | Ontvangst | 900015          |
| AmountPerTaxExt                 | Ontvangst | 900016          |
| CashTransactionSequentialNumber | Ontvangst | 900017          |

> [!NOTE]
> Het is belangrijk dat u de juiste aangepaste veldnamen opgeeft, zoals aangegeven in de bovenstaande tabel. Een onjuiste aangepaste veldnaam veroorzaakt ontbrekende gegevens in ontvangsten.

### <a name="configure-receipt-formats"></a>Indelingen voor ontvangstbewijzen configureren

Wijzig voor alle vereiste indelingen voor ontvangstbewijzen de waarde van het veld **Afdrukgedrag** in **Altijd afdrukken** voor de ontvangstindeling.

Voeg in de ontwerper van de ontvangstbewijsindeling de volgende aangepaste velden toe aan de juiste ontvangstbewijssecties. Opmerking: veldnamen komen overeen met de taalteksten die u in het vorige gedeelte hebt gedefinieerd.

1. Koptekst:

    - **Titel ontvangstbewijs**: dit veld geeft het type ontvangstbewijs aan.
    - **Contante transactie-id**: dit veld drukt het opeenvolgende nummer af van de ondertekende contante transactie.

2. Regels:

    - **Is geschenkbon**: dit veld markeert de ontvangstregel met betrekking tot de bewerking Geschenkbon uitgeven of Toevoegen aan geschenkbon.

3. Voettekst:

    - **Totaal (verkopen)**: dit veld wordt gebruikt om het totale contante verkoopbedrag op het ontvangstbewijs af te drukken. Dit bedrag is exclusief btw. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
    - **Btw-totaal (verkopen)**: dit veld wordt gebruikt om het totale belastingbedrag voor contante verkopen op het ontvangstbewijs af te drukken. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
    - **Totaal met btw (verkopen)**: dit veld wordt gebruikt om het totale contante verkoopbedrag op het ontvangstbewijs af te drukken. Bij dit bedrag is btw inbegrepen. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
    - **Btw-bedrag (verkopen)**: dit veld wordt gebruikt om het belastingbedrag voor contante verkopen per btw-code op het ontvangstbewijs af te drukken. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.

Zie [Ontvangstbewijsindelingen instellen en ontwerpen](../receipt-templates-printing.md) voor meer informatie over het werken met ontvangstbewijsindelingen.

### <a name="configure-the-saf-t-cash-register-export-format"></a>De SAF-T-exportindeling voor kassa's configureren

De configuratie van de SAF-T-indeling voor kassa's kan worden gedownload vanuit Microsoft Dynamics Lifecycle Services (LCS). Zie [Configuraties voor elektronische rapportage importeren](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md) voor meer informatie. U moet de volgende configuratie downloaden:

- **Retail channel data.version.1**: de configuratie van het gegevensmodel.
- **DMM channel data.version.1.14**: de configuratie voor gegevensmodeltoewijzing.
- **NO SAF T Cash Register.version.1.20**: de indelingsconfiguratie.

Nadat u de configuraties hebt geïmporteerd, selecteert u op de pagina **Commerce-parameters** op het tabblad **Elektronische documenten** in het veld **SAF-T-exportindeling voor kassa's** de naam van de geïmporteerde indelingsconfiguratie.

U moet ook de vereiste hoofdgegevens toewijzen aan vooraf gedefinieerde SAF-T-standaardcodes. Zie de documentatie bij de SAF-T-documentatie voor kassa's van de Noorse belastingdienst voor meer informatie. Als u de toewijzing wilt maken, moet u het nieuwe veld **SAF-T-kassacode** instellen op de volgende pagina's:

- Artikelengroepen
- Betalingswijzen
- Btw-codes

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

Als u de functionaliteit die specifiek is voor Noorwegen wilt inschakelen, moet u kanaalonderdelen configureren. Zie de [implementatierichtlijnen](emea-nor-fi-deployment.md) voor meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
