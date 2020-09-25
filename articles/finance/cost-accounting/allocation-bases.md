---
title: Toewijzingsgrondslagen
description: Dit onderwerp bevat informatie over toewijzingsgrondslagen. Toewijzingsgrondslagen zijn belangrijke onderdelen in Kostprijsboekhouding en worden meestal gebruikt voor de toewijzing van overheadkosten.
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMAllocationBaseDetail, CAMFormulaAllocationBaseDetail, CAMAllocationBasePreview, CAMAllocationBase, CAMCostAllocationRule, CAMPredefinedMemberAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a871eef822140f028832aa1be39372f07668d79
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759587"
---
# <a name="allocation-bases"></a>Toewijzingsgrondslagen 

[!include [banner](../includes/banner.md)]

Een toewijzingsgrondslag vormt de basis waarop overheadkosten in Kostprijsboekhouding worden toegewezen. Een toewijzingsgrondslag kan een hoeveelheid worden, zoals gebruikte machine-uren, verbruikte kilowattuur (kWh) of vierkante meters die in beslag worden genomen. Toewijzingsgrondslagen worden meestal gebruikt voor het toewijzen van overheadkosten aan voorraad die wordt geproduceerd. Een IT-afdeling wijst bijvoorbeeld de onkosten van de afdeling toe op basis van het aantal computers dat op elke afdeling wordt gebruikt.

Er zijn drie typen toewijzingsgrondslagen in Kostprijsboekhouding:

- Vooraf gedefinieerde toewijzingsgrondslagen van dimensieleden
- Toewijzingsgrondslagen van hiërarchie
- Toewijzingsgrondslagen van formule

## <a name="predefined-dimension-member-allocation-bases"></a>Vooraf gedefinieerde toewijzingsgrondslagen van dimensieleden

De vooraf gedefinieerde toewijzingsgrondslagen voor dimensieleden worden automatisch gemaakt wanneer een dimensielid wordt gemaakt dat een van de volgende typen heeft:

- Statistische dimensieleden
- Dimensieleden van kostenelement

> [!NOTE]
> In de toewijzingsgrondslagen van vooraf gedefinieerde dimensieleden, die zijn gebaseerd op een dimensielid voor een kostenelement, worden alleen de waarden van de gegevensbronprovider meegenomen, zoals het grootboek of budget.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Voorbeeld 1: een dimensielid voor kostenelementen gebruiken als de toewijzingsgrondslag
In dit voorbeeld wordt getoond hoe met een regel voor kostprijstoewijzing kostenelement 10002 (werknemersverzekering) wordt gemaakt om het saldo dat wordt vastgelegd voor kostenelement 10001 (salarissen) toe te wijzen. De toewijzingsregel wordt gedefinieerd op basis van de verhouding van de salarissen van elke afdeling ten opzichte van de totale salarissen. (Controle vereist!)

In het grootboek wordt het rekeningschema als volgt gedefinieerd.

| Rekeningschema | Hoofdrekening | Omschrijving        | Hoofdrekeningtype |
|------------------|--------------|--------------------|-------------------|
| Gedeeld           | 10001        | Salarissen           | Uitgaven           |
| Gedeeld           | 10002        | Werknemersverzekering | Uitgaven           |

Definieer een kostenelementdimensie en configureer de gegevensconnector. Nadat de gegevens zijn geïmporteerd, worden de volgende items gemaakt in Kostprijsboekhouding.

**Dimensieleden van kostenelement**

| Naam van dimensie van kostenelement | Kostenelement |  Omschrijving       | Type    |
|-----------------------------|--------------|--------------------|---------|
| Kostenelementen               | 10001        | Salarissen           | Primair |
| Kostenelementen               | 10002        | Werknemersverzekering | Primair |

**Toewijzingsgrondslagen van vooraf gedefinieerde dimensieleden** 

| Naam  | Omschrijving        | Dimensie van kostenelement |
|-------|--------------------|------------------------|
| 10001 | Salarissen           | Kostenelementen          |
| 10002 | Werknemersverzekering | Kostenelementen          |

In het grootboek zijn de volgende posten geboekt:

- De posten die de hoofdrekening Salarissen weergeven, zijn afkomstig uit de salarisadministratie en worden naar kostenplaatsen geboekt.
- De kosten voor verzekering van de werknemer worden handmatig naar een standaardkostenplaats geboekt.

| Grootboekdatum | Kostenplaats |  Omschrijving        | Hoofdrekening |  Omschrijving       | Bedrag in valuta voor boekhouding |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03-01-2017      | CC001       | HR                  | 10001        | Salarissen           | 2.000,00                      |
| 03-01-2017      | CC002       | FI                  | 10001        | Salarissen           | 5.000,00                      |
| 03-01-2017      | CC003       | VOB                  | 10001        | Salarissen           | 3000,00                      |
| 03-01-2017      | CC099       | Standaardkostenplaats | 10002        | Werknemersverzekering | 1.000,00                      |

Nadat de brongegevens van het grootboek zijn verwerkt, worden de volgende posten gemaakt in Kostprijsboekhouding.

**Kosteninvoer**

| Kostenobject |  Omschrijving        | Kostenelement  |  Omschrijving       | Kostengedrag   |Bedrag|Grootboekdatum|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | HR                  | 10001         | Salarissen           | Ongeclassificeerd    |2.000,00|  03-01-2017    |
| CC002       | FI                  | 10001         | Salarissen           | Ongeclassificeerd    |5.000,00|     03-01-2017         |
| CC003       | VOB                  | 10001         | Salarissen           | Ongeclassificeerd    |3000,00|      03-01-2017        |
| CC099       | Standaardkostenplaats | 10002         | Werknemersverzekering | Ongeclassificeerd    |1.000,00|      03-01-2017       |

In dit vereenvoudigde voorbeeld wordt met een regel voor kostprijstoewijzing kostenelement 10002 (werknemersverzekering) gemaakt in verhouding tot het saldo dat wordt vastgelegd voor kostenelement 10001 (salarissen).

**Kostenverdelingsregel**

| Dimensiehiërarchieknooppunt van een kostenobject | Dimensiehiërarchieknooppunt van een kostenelement | Kostengedrag | Toewijzingsgrondslag |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Ongeclassificeerd  | 10001           |

**Overheadberekening uitvoeren**

Nadat het kostenelement 10001 (salarissen) wordt toegepast als de toewijzingsgrondlag, is het resultaat van de overheadberekening als volgt.

| Kostenobject | Omschrijving | Magnitude |   Toewijzingsfactor         | Bedrag |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | HR          | 2.000     | (2.000 ÷ 10.000) × 1.000,00 | 200,00 |
| CC002       | FI          | 5.000     | (5.000 ÷ 10.000) × 1.000,00 | 500,00 |
| CC003       | VOB          | 3000     | (3.000 ÷ 10.000) × 1.000,00 | 300,00 |

**Journaal**

| Journaal | Type journaal                          | Fiscale kalenderperiode | Jaar | Periode   | Versie                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Berekeningsjournaal voor kostenverdeling | Fiscaal                 | 2017 | Periode 1 | Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1 |

**Journaalboekingen voor kostenobjectsaldo**

| Grootboekdatum | Kostenobject | Omschrijving         | Kostenelement | Omschrijving        | Kostengedrag |  Bedrag  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31-01-2017      | CC099       | Standaardkostenplaats | 10002        | Werknemersverzekering | Ongeclassificeerd  | 1.000,00 |

**Kosteninvoer**

| Kostenobject |  Omschrijving        | Kostenelement |    Omschrijving     | Kostengedrag | Bedrag    | Grootboekdatum |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Standaardkostenplaats | 10002        | Werknemersverzekering | Ongeclassificeerd  | -1.000,00 | 31-01-2017      |
| CC001       | HR                  | 10002        | Werknemersverzekering | Ongeclassificeerd  | 200,00    | 31-01-2017      |
| CC002       | FI                  | 10002        | Werknemersverzekering | Ongeclassificeerd  | 500,00    | 31-01-2017      |
| CC099       | VOB                  | 10002        | Werknemersverzekering | Ongeclassificeerd  | 300,00    | 31-01-2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Voorbeeld 2: een statistisch dimensielid gebruiken als de toewijzingsgrondslag

Statistische dimensieleden kunnen worden gebruikt als toewijzingsgrondslagen om beleid te definiëren of niet-monetair verbruik op basis van kostenobjecten te rapporteren. U kunt handmatig statistische dimensieleden maken of uit een bestand importeren met behulp van het hulpprogramma voor importeren/exporteren van gegevensbeheer.

**Statistische dimensieleden**

| Statistische dimensienaam | Statistisch element | Omschrijving               | Eenheid |
|----------------------------|---------------------|---------------------------|------|
| Statistische elementen       | FTE                 | Voltijdse werknemers       | St.   |
| Statistische elementen       | Elektriciteit         | Elektriciteitsverbruik   | kWh  |

Wanneer een statistisch dimensielid wordt opgeslagen, wordt een overeenkomende record in de toewijzingsgrondslagen van vooraf gedefinieerde dimensieleden gemaakt.

**Toewijzingsgrondslagen van vooraf gedefinieerde dimensieleden**

| Naam        | Omschrijving             | Statistische elementdimensie |
|-------------|-------------------------|-------------------------------|
| FTE         | Voltijdse werknemers     | Statistische elementen          |
| Elektriciteit | Elektriciteitsverbruik | Statistische elementen          |

Statistische maateenheden kunnen afkomstig zijn uit verschillende bronnen:

- Elektriciteitsverbruik kan worden gemeten op basis van meters die zijn geïnstalleerd in verschillende gebieden van het bedrijf.
- Tabellen bevatten statistische maateenheden. Bijvoorbeeld de tabel HcmEmployment bevat een lijst met alle werknemers en de kostenplaatsen waarvoor ze werken.

| Naam       | Kostenplaats |  Omschrijving  | Type medewerker |
|------------|-------------|----|-------------|
| Werknemer A | CC001       | HR | Werknemer    |
| Werknemer B | CC002       | FI | Werknemer    |
| Werknemer C | CC002       | FI | Werknemer    |
| Werknemer D | CC003       | VOB | Werknemer    |
| Werknemer F | CC003       | VOB | Werknemer    |

> [!NOTE]
> Alle tabellen met financiële dimensies kunnen worden gebruikt als bronnen voor statistische maateenheden.

Kostprijsboekhouding ondersteunt een verzameling van statistische maateenheden met behulp van de volgende gegevensverbindingen:

- Hulpprogramma voor importeren/exporteren van gegevensbeheer
- Statistische maateenheden

Als u statistische maateenheden uit het systeem wilt halen, is een sjabloon van de provider voor statistische maateenheden vereist. Zie Sjabloon van provider van statistische maateenheden voor meer informatie (Er wordt een koppeling toegevoegd zodra dit onderwerp is geschreven.)

**Sjablonen van provider van statistische maateenheden**

| Naam  | Functie | Brontabel  | Somveld      | Datumveld     |
|-------|----------|---------------|----------------|----------------|
| FTE´s | Aantal    | HcmEmployment | Niet van toepassing | Niet van toepassing |

Nadat de brongegevens van de statistische maateenheden zijn verwerkt, worden de volgende posten gemaakt in Kostprijsboekhouding.

**Statistische boekingen**

| Kostenobject | Omschrijving      | Grootboekdatum | Statistisch dimensielid | Omschrijving         | Magnitude |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR               | 31-01-2017      | FTE´s                        | Voltijdse werknemers | 1,00      |
| CC002       | FI               | 31-01-2017      | FTE´s                        | Voltijdse werknemers | 2.00      |
| CC003       | VOB               | 31-01-2017      | FTE´s                        | Voltijdse werknemers | 2.00      |

Hier volgt een voorbeeld van een kostenverdelingsregel als de toewijzingsgrondslag van het vooraf gedefinieerde dimensielid FTE´s wordt toegewezen als de toewijzingsgrondslag erin.

| Kostenobject | Omschrijving  | Magnitude | Toewijzingsfactor |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1,00      | (1/5) × bedrag    |
| CC002       | FI   | 2.00      | (2/5) × bedrag    |
| CC003       | VOB   | 2.00      | (2/5) × bedrag    |

U kunt de geïmporteerde gegevensentiteit voor statistische maateenheden gebruiken om statistische maateenheden in kostprijsboekhouding te importeren. U kunt ook het hulpprogramma voor importeren/exporteren van gegevensbeheer gebruiken. In Excel wordt het verbruik van elektriciteit als volgt vastgelegd.

| Grootboekdatum | Dimensielid | Magnitude | Bron-id |
|-----------------|------------------|-----------|-------------------|
| 31-01-2017      | CC001            | 2,450.00  | Elektriciteit       |
| 31-01-2017      | CC002            | 4,100.00  | Elektriciteit       |
| 31-01-2017      | CC003            | 15.000,00 | Elektriciteit       |

Nadat de brongegevens van de statistische maateenheden zijn verwerkt, worden de volgende posten gemaakt in Kostprijsboekhouding.

**Statistische boekingen**

| Kostenobject |    | Grootboekdatum | Statistisch dimensielid |    Omschrijving          | Magnitude |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 2,450.00  |
| CC002       | FI | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 4,100.00  |
| CC003       | VOB | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 15.000,00 |

Hier volgt een voorbeeld van een kostenverdelingsregel als de toewijzingsgrondslag van het vooraf gedefinieerde dimensielid Elektriciteit wordt toegewezen als de toewijzingsgrondslag erin.

| Kostenobject | Omschrijving  | Magnitude | Toewijzingsfactor          |
|-------------|------|-----------|----------------------------|
| CC001       | HR   | 2,450.00  | (2.450 ÷ 21.550) × bedrag  |
| CC002       | FI   | 4,100.00  | (4.100 ÷ 21.550) × bedrag  |
| CC003       | VOB   | 15.000,00 | (15.000 ÷ 21.550) × bedrag |

## <a name="hierarchy-allocation-bases"></a>Toewijzingsgrondslagen van hiërarchie

Kostenaccountants kunnen handmatig de hiërarchietoewijzingsgrondslagen maken door een hiërarchieknooppunt voor dimensieobjecten toe te passen op een bestaande toewijzingsgrondslag. Op deze manier kunt u het bereik van de toewijzingsgrondslag van het oorspronkelijke vooraf gedefinieerde dimensielid beperken. Eén toewijzingsgrondslag van het vooraf gedefinieerde dimensielid kan worden gebruikt voor het maken van verschillende hiërarchietoewijzingsgrondslagen. Bereiken kunnen worden beheerd in de dimensiehiërarchie voor kostenobjecten, die is gekoppeld aan de hiërarchietoewijzingsgrondslagen.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Voorbeeld: hiërarchietoewijzingsgrondslagen die worden gebaseerd op voltijdse werknemers in de organisatie
Hier volgt een voorbeeld van een dimensiehiërarchie voor kostenobjecten, die kan worden gemaakt om een vereenvoudigde organisatie te beschrijven.

| Hiërarchienaam | Knooppuntniveau 0 | Knooppuntniveau 1 | Knooppuntniveau 2 | Dimensieleden |
|----------------|--------------|--------------|--------------|-------------------|
| Organisatie   | CEO          | CFO          | FICO         | CC001             |
| Organisatie   | CEO          | CFO          | HR           | CC002             |
| Organisatie   | CEO          | CIO          | VOB           | CC003             |

De toewijzingsgrondslag van het vooraf gedefinieerde dimensielid FTE´s, die in het vorige gedeelte is gemaakt, bevat de volgende items.

**Statistische boekingen**

| Kostenobject | Omschrijving  | Grootboekdatum | Statistisch dimensielid | Omschrijving | Magnitude |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR   | 31-01-2017      | FTE´s                        | Voltijdse werknemers | 1,00      |
| CC002       | FI   | 31-01-2017      | FTE´s                        | Voltijdse werknemers | 2.00      |
| CC003       | VOB   | 31-01-2017      | FTE´s                        | Voltijdse werknemers | 2.00      |

Kosten moet worden verdeeld tussen kostenplaatsen die aan de financieel directeur (CFO) van de organisatie worden gerapporteerd. Het wordt bevestigd dat de juiste verdeelsleutel het aantal voltijdse werknemers (FTE´s) per kostenplaats is.

**Toewijzingsgrondslagen van hiërarchie**

| Naam                  | Toewijzingsgrondslag | Dimensiehiërarchie van een kostenobject | Dimensiehiërarchieknooppunt van een kostenobject |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Aantal FTE's in CFO | FTE´s           | Organisatie                    | CFO                                  |

Met een voorbeeldfunctie kunt u de hiërarchietoewijzingsgrondslag valideren die is gemaakt op basis van statistische gegevens in het systeem.

**Details van toewijzingsgrondslag**

| Kostenobject | Omschrijving  |  Magnitude |
|-------------|------|------------|
| CC001       | HR   | 1,00       |
| CC002       | FI   | 2.00       |

Hier volgt een voorbeeld van een kostenverdelingsregel als het aantal FTE´s in de CFO-hiërarchietoewijzingsgrondslag wordt toegewezen als de toewijzingsgrondslag erin.

| Kostenobject | Omschrijving  | Magnitude | Toewijzingsfactor |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1,00      | (1/3) × bedrag    |
| CC002       | FI   | 2.00      | (2/3) × bedrag    |

## <a name="formula-allocation-bases"></a>Toewijzingsgrondslagen van formule

Met formuletoewijzingsgrondslagen kunt u geavanceerde formules definiëren voor het bereiken van de juiste toewijzingsgrondslag. U kunt formuletoewijzingsgrondslagen handmatig maken.

Wanneer u een formuletoewijzingsgrondslag maakt, selecteert u welke statistische dimensie en kostenelementdimensie de basis moeten vormen voor de formule. Alle toewijzingsgrondslagen die afkomstig zijn van de eerder geselecteerde dimensies, kunnen worden gebruikt in een formuletoewijzingsgrondslag.

> [!NOTE]
> Eerder gedefinieerde formuletoewijzingsgrondslagen kunnen worden gebruikt voor het definiëren van een nieuwe formuletoewijzingsgrondslag.

In de formuletoewijzingsgrondslagfactoren kunt u een alias maken en koppelen aan een toewijzingsgrondslag of een constante. De aliassen worden vervolgens gebruikt voor het definiëren van de formule.

U kunt de volgende operatoren gebruiken voor het definiëren van uw formule.

| Symbolen | Tekst           |
|---------|----------------|
| ( )     | Haakjes    |
| \<      | Kleiner dan   |
| \>      | Groter dan    |
| +       | Optelling       |
| –       | Aftrekken    |
| \*      | Vermenigvuldigen |

Traditionele **IF**-instructies worden niet ondersteund. U kunt echter instructies maken en nagaan of deze waar zijn.

| Overzicht | Validatie | Resultaat |
|-----------|------------|--------|
| a \> b    | Waar       | 1      |
| a \> b    | Onwaar      | 0      |

### <a name="example-1-a-simple-formula"></a>Voorbeeld 1: een eenvoudige formule

Elektriciteitrekeningen bestaan vaak uit twee delen:

- Een vast tarief voor verbinding met het raster
- Kosten die zijn gekoppeld aan het verbruik per kWh

De toewijzingsgrondslag van het vooraf gedefinieerde dimensielid Elektriciteit is al gedefinieerd en bevat deze waarden.

**Statistische boekingen**

| Kostenobject | Naam | Grootboekdatum | Statistisch dimensielid | Omschrijving             | Magnitude |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR   | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 2,450.00  |
| CC002       | FI   | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 4,100.00  |
| CC003       | VOB   | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 15.000,00 |

Als de vaste kosten nu gelijkmatig moeten worden verdeeld over kostenobjecten die elektriciteit verbruiken, hebt u twee opties voor het toewijzen van de kosten:

- Maak een nieuwe vooraf gedefinieerde toewijzingsgrondslag, Elektriciteit vast, en pas vervolgens een statistische maateenheid van 1,00 toe voor elk kostenobject dat elektriciteit verbruikt.
- Maak een formuletoewijzingsgrondslag, Elektriciteit vast, die gebruikmaakt van de vooraf gedefinieerde toewijzingsgrondslag Elektriciteit die al in het systeem is gedefinieerd. Het voordeel van deze optie is dat gegevens in Kostprijsboekhouding voor slechts één statistisch Elektriciteit-dimensielid moeten worden geladen.

**Toewijzingsgrondslag van formule** 

| Naam              | Dimensie van kostenelement | Statistische dimensie | Formule |
|-------------------|------------------------|-----------------------|---------|
| Elektriciteit vast |                        | Statistische elementen  |         |

Voordat het veld **Formule** kan worden ingevuld, moet u de alias opgeven die in de formule moet worden gebruikt.

**Factoren van toewijzingsgrondslag van formule**

| Alias | Constante | Toewijzingsgrondslag |
|-------|----------|-----------------|
| a     |          | Elektriciteit     |
| b     | 0,01     |                 |

Houd er rekening mee dat 0 (nul) niet wordt ondersteund als een constante.

**Toewijzingsgrondslag van formule**

| Naam              | Dimensie van kostenelement | Statistische dimensie | Formule |
|-------------------|------------------------|-----------------------|---------|
| Elektriciteit vast |                        | Statistische elementen  | a \> b  |

Met een voorbeeldfunctie kunt u de formuletoewijzingsgrondslag valideren die is gemaakt op basis van statistische gegevens in het systeem.

**Details van toewijzingsgrondslag**

| Kostenobject | Omschrijving  | Formule           | Magnitude |
|-------------|------|-------------------|-----------|
| CC001       | HR   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | VOB   | 15.000,00 \> 0,01 | 1,00      |

Hier volgt een voorbeeld van een kostenverdelingsregel als de formuletoewijzingsgrondslag Elektriciteit wordt toegewezen als de toewijzingsgrondslag erin.

**Toewijzingsfactor van grootte van kostenobject**

| Kostenobject | Naam | Magnitude |  Toewijzingsfactor |
|-------------|------|-----------|--------------------|
| CC001       | HR   | 1,00      | (1/3) × bedrag     |
| CC002       | FI   | 1,00      | (1/3) × bedrag     |
| CC003       | VOB   | 1,00      | (1/3) × bedrag     |

### <a name="example-2-an-advanced-formula"></a>Voorbeeld 2: een geavanceerde formule
Voor dit voorbeeld moeten de kosten van elektriciteit niet alleen de werkelijke elektriciteit volgen die wordt verbruikt in kWh. Het management wil een beloning opnemen voor het verlagen van het elektriciteitsverbruik. 

| Regel              | Tarief | 
|-------------------|------|
| a <= 10000.00 kWh | 0.75 |
| a > 10000.00 kWh  | 1.15 |

Een nieuwe formuletoewijzingsgrondslag, Elektriciteitgebruik, wordt gemaakt.

**Toewijzingsgrondslag van formule**

| Naam              | Dimensie van kostenelement | Statistische dimensie | Formule |
|-------------------|------------------------|-----------------------|---------|
| Elektriciteitsgebruik |                        | Statistische elementen  |         |

Voordat het veld **Formule** kan worden ingevuld, moet u de alias opgeven die in de formule moet worden gebruikt.

**Factoren van toewijzingsgrondslag van formule**

| Alias | Constante  | Toewijzingsgrondslag |
|-------|-----------|-----------------|
| a     |           | Elektriciteit     |
| b     | 10.000,00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Toewijzingsgrondslag van formule**

| Naam              | Dimensie van kostenelement | Statistische dimensie | Formule                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Elektriciteit vast |                        | Statistische elementen  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Met een voorbeeldfunctie kunt u de formuletoewijzingsgrondslag valideren die is gemaakt op basis van statistische gegevens in het systeem.

**Details van toewijzingsgrondslag**

| Kostenobject |    | Formule                                                                                                                             | Magnitude |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | HR | ((2.450,00 \> 10,000,00) × ((10.000,00 × 0,75) + (2.450,00 – 10.000,00) × 1,15)) + ((2.450,00 \<= 10.000,00) × 2.450,00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4.100,00 \> 10,000,00) × ((10.000,00 × 0,75) + (4.100,00 – 10.000,00) × 1,15)) + ((4.100,00 \<= 10.000,00) × 4.100,00 × 0,75)     | 3,075.00  |
| CC003       | VOB | ((15.000,00 \> 10,000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) | 1,3250.00 |

Hier wordt de formule voor CC003 (IT) nader bekeken:

((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) = 13.250,00

(1 × (7.500,00 + 5.000,00 × 1,15)) + (0 × 15.000,00 × 0,75)            

1 × 7.500,00 + 5.750,00 + 0 

Hier volgt een voorbeeld van een kostenverdelingsregel als de formuletoewijzingsgrondslag Elektriciteit vast wordt toegewezen als de toewijzingsgrondslag erin.


| Kostenobject | Omschrijving | Magnitude |        Toewijzingsfactor         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     HR      | 1,837.50  | (1,837.50 ÷ 18,162.50) × bedrag  |
|    CC002    |     FI      | 3,075.00  | (3,075.00 ÷ 18,162.50) × bedrag  |
|    CC003    |     VOB      | 13,250.00 | (13,250.00 ÷ 18,162.50) × bedrag |

