---
title: Functies voor factureringsplanningen
description: In dit artikel worden de functies van factureringsplanningen uitgelegd, zoals prijsbepalingsmethoden, escalaties en kortingen, afstemmingsdatums, betalingen naar rato, omkeren van facturering en het splitsen van artikelgroepen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b6cfebc2bbfe06e118bfc96f9ae0df6323805e39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853578"
---
# <a name="billing-schedule-features"></a>Functies voor factureringsplanningen

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies van factureringsplanningen en factureringsplanningsregels uitgelegd. Hierin worden de verschillende gebruikte methoden voor prijzen beschreven en wordt aangegeven hoe u escalaties en kortingen gebruikt en een factureringsperiode omkeert. Daarnaast vindt u hier voorbeelden van berekeningen van betalingen naar rato en gesplitste artikelgroepen.

## <a name="pricing-methods"></a>Prijsbepalingsmethoden

Met een van de volgende prijsbepalingsmethoden kunt u de eenheidsprijs van een artikel berekenen:

* Vast
* Standaard
* Niveau
* Vast niveau

### <a name="flat-pricing"></a>Vaste prijzen

Wanneer de methode voor vaste prijzen wordt gebruikt, kan de eenheidsprijs voor een artikel in een factureringsplanningsregel op de pagina **Alle factureringsplanningen** worden bewerkt in elke gewenste waarde. De waarde voor **Prijseenheid** is altijd **1**. Daarom komen de waarden voor **Eenheidsprijs** en **Nettobedrag** voor een artikel overeen.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standaardprijzen (zonder handelsovereenkomst)

Wanneer de standaardprijsstellingsmethode wordt gebruikt zonder handelsovereenkomst, stelt u de eenheidsprijs in voor een artikel op een factureringsplanningsregel in door **Productgegevensbeheer** te selecteren op de pagina **Productgegevens vrijgeven**. De eenheidsprijs wordt weergegeven in de sectie **Basisverkoopprijs**. Deze wordt berekend als *Prijs* &divide; *Prijshoeveelheid*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standaardprijzen (met een handelsovereenkomst)

In de volgende voorbeelden worden de standaardprijsberekeningen bij een handelsovereenkomst weergegeven. U kunt handelsovereenkomsten maken via de pagina **Productgegevens vrijgeven**.

Bij beide voorbeelden wordt gebruikgemaakt van een artikel met de volgende prijsklassen.

| Van (hoev.) | Tot (hoev.) | Maateenheid | Prijs | Prijseenheid |
|---|---|---|---|---|
| 0 | 100 | Elk | 1.50 | 1 |
| 100 | 200 | Elk | 1.25 | 1 |
| 200 | 999999 | Elk | 1.00 | 1 |

**Voorbeeld 1**

De factuurhoeveelheid is 250 en de standaardprijsstellingsmethode wordt gebruikt. Aangezien de hoeveelheid zich in het prijshoeveelheidsbereik 200 tot 999.999 bevindt, is de eenheidsprijs 1,00. 

Het nettobedrag wordt als volgt berekend:

*Nettobedrag* = (*Hoeveelheid* &times; *Prijs*) &divide; *Prijseenheid* = (250 &times; 1,00) &divide; 1 = 250

**Voorbeeld 2**

De factuurhoeveelheid is 100 en de standaardprijsstellingsmethode wordt gebruikt. Aangezien de factuurhoeveelheid zich in het prijshoeveelheidsbereik 0 tot 100 bevindt, is de eenheidsprijs 1,50.

> [!NOTE]
> De factuurhoeveelheid ligt in het bereik 0-100 in plaats van het bereik 100-200 omdat, bij standaardgedrag voor hoeveelheidsvereffening, een hoeveelheid overeenkomt als deze *groter dan of gelijk is aan* de hoeveelheid bij Van en *kleiner is dan* de hoeveelheid bij Tot.

Het nettobedrag wordt als volgt berekend:

*Nettobedrag* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Niveauprijzen

Voor het volgende voorbeeld heeft een artikel de volgende prijsklassen.

| Van (hoev.) | Tot (hoev.) | Maateenheid | Prijs | Prijseenheid |
|---|---|---|---|---|
| 0 | 100 | Elk | 1.50 | 10 |
| 100 | 200 | Elk | 1.25 | 10 |
| 200 | 999999 | Elk | 1.00 | 10 |

Als de factuurhoeveelheid 250 is en de methode voor niveauprijzen wordt gebruikt, worden de prijzen van de artikelen als volgt berekend, op basis van de prijsklassen:

- **Eerste 100 artikelen:** 100 &times; 1,50 = 150,00
- **Tweede 100 artikelen:** 100 &times; 1,25 = 125,00
- **Resterende artikelen:** 50 &times; 1,00 = 50,00

Het nettobedrag wordt als volgt berekend:

*Nettobedrag* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Nadat het nettobedrag is berekend, wordt de eenheidsprijs berekend door het nettobedrag door de hoeveelheid te delen:

*Eenheidsprijs* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Vaste niveauprijzen

Voor het volgende voorbeeld heeft een artikel de volgende prijsklassen.

| Van (hoev.) | Tot (hoev.) | Maateenheid | Vast niveaubedrag | Prijseenheid |
|---|---|---|---|---|
| 0 | 50 | Elk | 100.00 | 50 |
| 50 | 200 | Elk | 150.00 | 200 |

In de volgende tabel ziet u de facturen en de eenheidsprijzen voor de verschillende hoeveelheden die worden gekocht. Het nettobedrag wordt eerst berekend en vervolgens wordt de eenheidsprijs berekend.

| Factuur | Ingekochte hoeveelheid | Eenheidsprijs | Nettobedrag |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Escalaties en kortingen

Een *escalatie* is een prijsverhoging voor een toekomstige factureringsperiode waarvoor de factuur nog niet is gemaakt. Een *korting* is een prijsverlaging voor een toekomstige factureringsperiode waarvoor de factuur nog niet is gemaakt.

In Facturering van abonnementen kunnen escalaties en kortingen niet met terugwerkende kracht op een factureringsplanning worden toegepast. U kunt bijvoorbeeld geen escalatie toepassen op een factureringsplanning van drie maanden geleden en deze verwerken. U kunt dus geen prijsverhoging toepassen die drie maanden geleden heeft plaatsgevonden.

U kunt op een van de volgende locaties een escalatie of korting toepassen op een factureringsplanning of factureringsplanningsregel:

- De lijstpagina **Alle/Actieve factureringsplanningen**
- Een specifieke factureringsplanning
- Een specifieke factureringsplanningsregel

### <a name="apply-an-escalation-or-discount"></a>Een escalatie of korting toepassen

Volg deze stappen om een escalatie of korting toe te passen op een factureringsplanning.

1. Selecteer een factureringsplanning of een factureringsplanningsregel.
2. Selecteer **Escalatie en korting** op het tabblad **Escalatie en korting** of op de factureringsplanningsregel.
3. Als een consumentenprijsindex wordt gebruikt om de escalatie of korting te berekenen, selecteert u een waarde in het veld **Berekening van consumentenprijsindex**.
4. Selecteer **Nieuw** om een escalatie- of kortingsregel toe te voegen.
5. Schakel het selectievakje **Korting** in voor een korting. Voor een escalatie laat u het selectievakje **Korting** uitgeschakeld.
6. Stel de velden **Begindatum** en **Frequentie** in.
7. Stel het veld **Einddatum** in voor uitstelartikelen die de functie voor niet-gefactureerde opbrengst gebruiken.
8. Stel het veld **Percentage**, **Bedrag** of **Planning voor consumentenprijsindex** in.
9. Stel het veld **Einddatum** in.
10. Selecteer **OK**.
11. Herhaal stap 4 tot en met 10 voor elke extra escalatie- of kortingsregel die u nodig hebt.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Velden op de pagina Factureringsplanningsregels

De pagina **Factureringsplanningsregels** bevat de volgende velden.

| Veld | Description |
|---|---|
| Artikelnummer | Het artikelnummer voor de factureringsplanningsregel. Dit veld is alleen beschikbaar wanneer de pagina wordt geopend vanuit een regelartikel voor factureringsplanningen. |
| Berekening van consumentenprijsindex | <p>Selecteer de methode die wordt gebruikt om de escalatie van de consumentenprijsindex te berekenen:</p><ul><li>**Vorige consumentenprijsindex**: gebruik de vorige waarde van de consumentenprijsindex voor de escalatieberekening.</li><li>**Basisconsumentenprijsindex**: gebruik de basiswaarde van de consumentenprijsindex voor de escalatieberekening.</li></ul> |
| Raster **Regel** | |
| Korting | <p>Gebruik dit selectievakje om in stellen of de wijziging in het bedrag een escalatie of korting is:</p><ul><li>**Ingeschakeld**: de wijziging past een korting toe op de factureringsplanning of factureringsplanningsregel.</li><li>**Uitgeschakeld**: de wijziging past een escalatie toe op een factureringsplanning of planningsregel.</li></ul><p>De instelling van dit selectievakje kan niet worden gewijzigd voor artikelen die gebruikmaken van de functie voor niet-gefactureerde opbrengst. Bovendien kunnen kortingen niet worden toegepast op artikelen die gebruikmaken van opbrengstsplitsing.</p> |
| Begindatum | Selecteer de begindatum van de escalatie of korting. |
| Frequentie | Selecteer de frequentie van de escalatie of korting: **Geen**, **Maandelijks**, **Driemaandelijks**, **Halfjaarlijks** of **Jaarlijks**. |
| Percentage | Geef het percentage van de escalatie of korting op. |
| Bedrag | Geef het bedrag van de escalatie of korting op. |
| Planning van consumentenprijsindex | Selecteer de planning voor de consumentenprijsindex op die wordt gebruikt voor de berekeningen. |
| Einddatum | <p>Selecteer de einddatum van de escalatie of korting.</p><p>**Opmerking:** dit veld is vereist voor artikelen die gebruikmaken van de functie voor niet-gefactureerde opbrengst.</p> |
| Nummer van uitstelplanning | <p>Het nummer van de uitstelplanning.</p><p>Dit veld is alleen beschikbaar wanneer de pagina wordt geopend vanuit een regel voor factureringsplanningen.</p> |
| Batchnummer journaal | <p>Het batchnummer van het journaal.</p><p>Dit veld is alleen beschikbaar wanneer de pagina wordt geopend vanuit een regel voor factureringsplanningen.</p> |
| Totaal kortingsbedrag | <p>De som van kortingsbedragen voor alle regels in het raster.</p><p>Dit veld is alleen beschikbaar wanneer de pagina wordt geopend vanuit een regel voor factureringsplanningen.</p> |
| Huidig kortlopend niet-gefactureerd opbrengstbedrag | <p>Het huidige kortlopende niet-gefactureerde opbrengstbedrag.</p><p>Dit bedrag wordt weergegeven wanneer een methode voor uitstel voor de korte termijn is geselecteerd op de pagina **Factureringsparameters voor terugkerende contracten** en de rekeningen voor het regelartikel zijn ingesteld op de instellingspagina **Niet-gefactureerde opbrengst**.</p> |
| Huidig langlopend niet-gefactureerd opbrengstbedrag | <p>Het huidige langlopende niet-gefactureerde opbrengstbedrag.</p><p>Dit bedrag wordt weergegeven wanneer een methode voor uitstel voor de korte termijn is geselecteerd op de pagina **Factureringsparameters voor terugkerende contracten** en de rekeningen voor het regelartikel zijn ingesteld op de instellingspagina **Niet-gefactureerde opbrengst**.</p> |

## <a name="proration-examples"></a>Voorbeelden van betalingen naar rato

Berekeningen voor betalingen naar rato kunnen worden gebaseerd op het aantal dagen of het aantal maanden. De methode die wordt gebruikt voor de berekening van betalingen naar rato wordt ingesteld op de pagina **Factureringsparameters voor terugkerende contracten**. De methode voor betaling naar rato is van invloed op de wijze waarop de bedragen voor een factureringsplanning worden berekend in de volgende situaties:

- Initiële aanmaak
- Toepassing van een escalatie of korting
- Beëindiging
- Plaatsing of verwijdering van een blokkering
- Toevoeging van ondersteuning of verlenging

De methode voor betaling naar rato heeft ook invloed op de berekeningen voor het maandelijkse rapport voor terugkerende opbrengsten.

### <a name="example-1"></a>Voorbeeld 1

Het jaarlijkse bedrag van een factureringsplanning wordt € 5000. De begindatum is 12 augustus 2019 en de einddatum is 22 december 2019. De factureringsfrequentie is jaarlijks. Het bedrag naar rato wordt op de volgende manieren berekend, afhankelijk van het gebruik van een dagelijkse of maandelijkse berekeningsmethode:

- **Dagelijks**

    - *Aantal dagen* = *Einddatum* – *Begindatum* + 1 = 133 dagen
    - *Aantal dagen in het jaar* = 11 augustus 2020 – 12 augustus 2019 + 1 = 366 dagen
    - *Bedrag naar rato* = 5000 &times; (133 &divide; 366) = 1816,94

- **Maandelijks**

    - *Eerste maanden* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Middelste maanden* = 3
    - *Laatste maanden* = 22 &divide; 31
    - Bedrag naar rato = 5000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Voorbeeld 2

Het jaarlijkse bedrag van een factureringsplanning wordt € 12.000. De begindatum is 1 augustus 2019 en de einddatum is 31 december 2019. De factureringsfrequentie is jaarlijks. Het bedrag naar rato wordt op de volgende manieren berekend, afhankelijk van de berekeningsmethode:

- **Dagelijks**

    - *Aantal dagen* = *Einddatum* – *Begindatum* + 1 = 153 dagen
    - *Aantal dagen in het jaar* = 31 juli 2020 – 1 augustus 2019 + 1 = 366 dagen
    - *Bedrag naar rato* = 12.000 &times; (153 &divide; 366) = 5016,39

- **Maandelijks (hele maand)**

    - *Aantal maanden* = 5
    - *Totaal aantal maanden* = 12
    - *Bedrag naar rato* = (12.000 &times; 5) &divide; 12 = 5000

## <a name="reversing-a-period-billing"></a>Een periodefacturering omkeren

In dit voorbeeld bevat een factureringsplanning slechts één regel:

- Er wordt gedurende twaalf maanden, van januari tot en met december, maandelijks gefactureerd.
- Er zijn facturen gemaakt voor alle perioden tot en met april.

U wilt de factuur omkeren voor de factureringsperiode voor april.

Als er nog geen verkoopfactuur is gemaakt voor de factureringsperiode voor april, kunt u de verkooporder verwijderen. In dit geval wordt de status **Gefactureerd** voor de gegevens verwijderd. Aangezien er een factuur is gemaakt voor de factureringsperiode, kan de status **Gefactureerd** voor de gegevens echter niet worden gewist. Als u de facturering voor april wilt omkeren, moet u daarom een tegenrekening voor de creditnota maken voor de regel.

1. Maak een planningsregel voor hetzelfde artikel op de pagina **Alle factureringsplanningen**.
2. Wijzig de waarde voor **Hoeveelheid** voor het artikel in de negatieve hoeveelheid van de oorspronkelijke hoeveelheid.
3. Stel het veld **Factureringsfrequentie** in op **Eenmalig**.
4. Werk de begin- en einddatums bij zodat deze overeenkomen met de datums van de factureringsdetailregel waarvoor u een creditnota wilt maken. Stel in dit voorbeeld de begindatum in op 1 april 2019 en de einddatum op 30 april 2019.
5. Sla de wijzigingen op.
6. Open de pagina **Factuur genereren** en maak de verkooporder met de creditnota voor de opgegeven periode.
7. Optioneel: boek de factuur.

Wanneer u de regels voor de factureringsplanning controleert, ziet u dat de nieuwe regel een koppeling naar de creditnota bevat. De oorspronkelijke regel bevat nog steeds een koppeling naar de oorspronkelijke factuur voor april.

## <a name="split-item-group-examples"></a>Voorbeelden van gesplitste artikelgroepen

Voor dit voorbeeld zijn de volgende instellingen gemaakt:

- Op de pagina **Factureringsparameters voor terugkerende contracten** is de optie **Splitsen op artikelgroep** geselecteerd en het veld **Uniek planningstype** is ingesteld op **Klant**.
- Er zijn drie artikelgroepen gemaakt: **PREFIX**, **DATAHUB** en **SPP**.
- Klant US-001 heeft meerdere factureringsplanningen waarin de artikelgroep PREFIX of DATAHUB is.
- Klant US-002 heeft meerdere factureringsplanningen waarin de artikelgroep PREFIX of SPP is.

| Nummer factureringsplanning | Klant | Artikelengroep |
|---|---|---|
| SCH001 | US-001 | PREFIX |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | PREFIX |
| SCH004 | US-002 | SPP |

Klant US-001 koopt een verleningsartikel dat bij de artikelgroep PREFIX hoort. Deze transactie is een nieuwe verkooporder.

| Nummer van verkooporder | Klant | Hoofdartikel | Verlengingsartikel | Verlengingsartikelgroep | Nummer factureringsplanning |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PREFIX | SCH001 |

Wanneer de factuur voor de verkooporder wordt geboekt, wordt het verlengingsartikel toegevoegd aan de bestaande factureringsplanning (SCH001) voor de klant. Deze factureringsplanning gebruikt de artikelgroep PREFIX. Alle verlengingsartikelen die tot dezelfde artikelgroep behoren, worden in dezelfde factureringsplanning geplaatst.

**Koptekst**
 
| Nummer factureringsplanning | Klant | Artikelengroep |
|---|---|---| 
| SCH001 | US-001 | PREFIX |

**Regel**

| Nummer factureringsplanning | Klant | Artikelengroep |
|---|---|---|
| SCH001 | US-001 | D0002 |

Klant US-001 koopt nu een verleningsartikel dat bij de artikelgroep SPP hoort. Deze transactie is een nieuwe verkooporder.

| Nummer van verkooporder | Klant | Hoofdartikel | Verlengingsartikel | Verlengingsartikelgroep | Nummer factureringsplanning |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

Momenteel heeft de klant US-001 geen factureringsplanning die de SPP-artikelgroep gebruikt. Daarom wordt een nieuwe factureringsplanning gemaakt.

**Koptekst**

| Nummer factureringsplanning| Klant | Artikelengroep |
|---|---|---|
| SCH005 | US-001 | SPP |

**Regel**

| Nummer factureringsplanning | Klant | Artikelengroep |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Meerdere factureringsplanningen voor dezelfde eindgebruiker en klant

Voor dit voorbeeld zijn de volgende instellingen gemaakt:

- Op de pagina **Factureringsparameters voor terugkerende contracten** is de optie **Splitsen op artikelgroep** geselecteerd en het veld **Uniek planningstype** is ingesteld op **Eindgebruiker**.
- Op de pagina **Eindgebruikers** is de volgende klant- en eindgebruikersrelatie ingesteld.

    | Klantrekening | Rekening van eindgebruiker |
    |---|---|
    | US-001 | US-221 |

Er zijn meerdere factureringsplanningen gemaakt voor de combinatie van klant en eindgebruiker. Aangezien **Splitsen op artikelgroep** is geselecteerd op de pagina **Parameters voor facturering terugkerende contract**, kunnen er meerdere factureringsplanningen worden gemaakt voor dezelfde klant- en eindgebruikerrelatie.

| Nummer factureringsplanning | Klant | Rekening van eindgebruiker | Artikelgroep header |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

Op de pagina **Artikelinstellingen** maakt u relaties tussen ondersteunings- en verlengingsartikelen.

| Artikelcode | Artikelrelatie | Ondersteuningsartikel | Verlengingsartikel | Verlengingsartikelgroep |
|---|---|---|---|---|
| Tabel | D001 | ITEM27 | D007 | IG1 |
| Tabel | D002 | ITEM28 | D005 | IG2 |
| Tabel | D003 | ITEM29 | D006 | IG3 |

U maat nu een verkooporder voor de klant US-001. Deze verkooporder heeft artikelen van de pagina **Artikelinstellingen**. Wanneer u de verkooporder maakt, wordt de de pagina **Ondersteunings- en verlengingsproces** geopend en kunt u het veld **Eindgebruikersrekening** en andere vereiste informatie voor het verlengingsartikel instellen.

Wanneer de factuur voor de transactie wordt gemaakt en geboekt, worden er verschillende factureringsplanningen gemaakt voor de combinatie van klant/eindgebruiker en artikelgroep. Meerdere regels in dezelfde verkooporder kunnen aan dezelfde factureringsplanning worden toegewezen.

| Nummer van verkooporder | Klant | Rekening van eindgebruiker | Hoofdartikel | Ondersteuningsartikel | Verlengingsartikel | Nummer factureringsplanning |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
