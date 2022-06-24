---
title: Niet-gefactureerde opbrengst
description: In dit artikel wordt uitgelegd hoe u artikelen en rekeningen instelt voor gebruik van de functie Niet-gefactureerde opbrengst in Facturering van abonnementen.
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
ms.openlocfilehash: b3fe58fc06df3f61433c8457b337ae895283e12b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879677"
---
# <a name="unbilled-revenue"></a>Niet-gefactureerde opbrengst

In dit artikel wordt de functie Niet-gefactureerde opbrengst beschreven waarmee u de bedragen voor volledige factureringsplanningen op de balans kunt opnemen. Deze bedragen worden opgenomen in een rekening voor niet-gefactureerde opbrengst en een tegenrekening voor niet-gefactureerde opbrengst en het contract wordt gefactureerd in termijnen.

## <a name="set-up-unbilled-revenue"></a>Niet-gefactureerde opbrengst configureren

Voer de onderstaande stappen uit om niet-gefactureerde opbrengst te configureren:

- Stel op de pagina **Factureringsparameters voor terugkerende contracten** de velden in de sectie **Niet-gefactureerde opbrengst** in.
- De functie voor niet-gefactureerde opbrengsten kan worden gebruikt voor artikelen waarbij het veld **Artikeltype** is ingesteld op **Standaard**. Het kan ook worden gebruikt voor uitstelartikelen. Als u niet-gefactureerde opbrengst wilt gebruiken voor de functionaliteit voor de korte termijn, stelt u de opties voor de korte termijn in op de pagina **Terugkerende contractfactureringsparameters**.

Voer de onderstaande stappen uit om artikelen te configureren voor gebruik van niet-gefactureerde opbrengst:

1. Ga naar de pagina **Instellingen voor niet-gefactureerde opbrengst** en selecteer op het tabblad **Artikelen** de optie **Toevoegen**.
2. Selecteer op de nieuwe regel in het veld **Artikelcode** de artikelcode.
3. Selecteer de artikelrelatie in het veld **Artikelrelatie**.
4. Herhaal deze stappen om meer regels toe te voegen.
5. Selecteer **Opslaan**.

Voer de onderstaande stappen uit om artikelen en de rekeningen voor niet-gefactureerde opbrengst te configureren:

1. Ga naar de pagina **Instellingen voor niet-gefactureerde opbrengst** en selecteer op het tabblad **Rekeningen** de optie **Toevoegen**.
2. Selecteer op de nieuwe regel in het veld **Artikelcode** de artikelcode.
3. Selecteer de artikelrelatie in het veld **Artikelrelatie**.
4. Selecteer de rekeningen voor de niet-gefactureerde opbrengst, niet-gefactureerde korting en de tegenrekening voor niet-gefactureerde opbrengst. Als u de korte-termijnrekeningen wilt gebruiken, moet u het veld **Methode korte termijn voor niet-gefactureerd** instellen op **Voortschrijdende perioden** of **Vast jaar** op de pagina **Terugkerende contractfactureringsparameters**.
5. Herhaal deze stappen om meer regels toe te voegen.
6. Selecteer **Opslaan**.

## <a name="use-unbilled-revenue"></a>Niet-gefactureerde opbrengst gebruiken

1. Maak een factureringsplanning aan op de pagina **Alle factureringsplanningen**.
2. Als het artikel niet is ingesteld voor gebruik van niet-gefactureerde opbrengst, schakel u het selectievakje **Niet-gefactureerde opbrengst** in op de factureringsplanningsregel.
3. Stel de optie **Niet-gefactureerde opbrengst** in op **Ja**. Controleer de rekeningen voor de niet-gefactureerde opbrengst, korting en de tegenrekening voor niet-gefactureerde opbrengst en werk deze zo nodig bij.
4. Selecteer in de factureringsplanning onder **Verwerking van niet-gefactureerde opbrengst** de optie **Journaalpost maken** om de eerste journaalboeking voor niet-gefactureerde opbrengst te maken. Deze stap moet worden voltooid voordat de factureringsplanning wordt gefactureerd.
5. Nadat de eerste journaalboeking is gemaakt, selecteert u **Factuur genereren** om verkooporders te maken en de facturen voor de factureringsplanningen te verzenden.
6. Nadat de facturen zijn geboekt, kunt u de auditgegevens controleren op het tabblad **Verlengingen** van de pagina **Alle factureringsplanningen**.

### <a name="milestone-billing"></a>Facturering van mijlpalen

Facturering van mijlpalen werkt in de volgende situaties met niet-gefactureerde opbrengst:

- Als het bovenliggende mijlpaalartikel niet wordt gefactureerd (het selectievakje **Niet gefactureerde opbrengst** is ingeschakeld) en de onderliggende mijlpaalartikelen worden gefactureerd (het selectievakje **Niet gefactureerde opbrengst** is uitgeschakeld), moeten de begin- en einddatums voor het bovenliggende artikel worden opgegeven. Deze datums worden gebruikt om de eerste journaalboeking te maken.
- Als het bovenliggende mijlpaalartikel wordt gefactureerd (het selectievakje **Niet gefactureerde opbrengst** is uitgeschakeld) en de onderliggende mijlpaalartikelen niet worden gefactureerd (het selectievakje **Niet gefactureerde opbrengst** is ingeschakeld), moet de einddatum alleen worden opgegeven voor de onderliggende artikelen waarvoor u de initiële journaalboeking wilt maken.

Elk onderliggend mijlpaalartikel kan afzonderlijk worden verwerkt. De einddatums kunnen worden opgegeven wanneer u klaar bent om de eerste journaalboeking te maken.

> [!NOTE]
> Als de eerste journaalboeking voor het bovenliggende artikel of de onderliggende artikelen van een mijlpaal al is gemaakt of als er een factuur is gemaakt, kunnen de begin- en einddatums niet worden bewerkt.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Niet-gefactureerd opbrengsten met lineaire uitstel

Volg deze stappen om niet-gefactureerde opbrengst met een planning voor lineaire uitstel te gebruiken.

1. Maak een factureringsplanning aan op de pagina **Alle factureringsplanningen**.
2. Voeg een artikel toe aan de planningsfactureringsregels.
3. Selecteer **Uitstel** voor de regel.
4. Voer de volgende stappen uit op de pagina **Transactie-uitstel**:

    1. Stel de optie **Uitgesteld** in op **Ja**.
    2. Wijzig de rekeningen waar nodig.
    3. Selecteer in de sectie **Planning** de waarde **Lineair** en bewerk zo nodig andere waarden.
    4. Selecteer **OK**.

5. Selecteer voor de regel de waarde **Niet-gefactureerde opbrengst** en voer vervolgens de volgende stappen uit:

    1. Stel de optie **Niet-gefactureerde opbrengst** in op **Ja**.
    2. Selecteer de rekeningen die u wilt gebruiken voor de opbrengst, korting en de tegenrekening voor niet-gefactureerde opbrengst.

6. Selecteer onder de factureringsplanning onder **Verwerking van niet-gefactureerde opbrengsten** de optie **Journaalboeking maken**. U kunt de journaalboeking desgewenst ook maken op de pagina **Massale verwerking van niet-gefactureerde opbrengsten**.
7. De uitstelplanning wordt gemaakt. U kunt de details bekijken op de pagina **Alle uitstelplanningen**. Nadat u de uitstelplanning hebt gemaakt, kunt u verschillende waarden bewerken voor het regelartikel van de factureringsplanning. U kunt bijvoorbeeld de stuksprijs, hoeveelheid of datums bewerken.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Niet-gefactureerde opbrengsten met uitstel op basis van gebeurtenissen

Volg deze stappen om niet-gefactureerde opbrengst te gebruiken met een planning voor uitstel op basis van gebeurtenissen.

1. Maak een factureringsplanning aan op de pagina **Alle factureringsplanningen**.
2. Voeg een artikel toe aan de planningsfactureringsregels.
3. Selecteer **Uitstel** voor de regel.
4. Voer de volgende stappen uit op de pagina **Transactie-uitstel**:

    1. Stel de optie **Uitgesteld** in op **Ja**.
    2. Wijzig de rekeningen waar nodig.
    3. Selecteer in de sectie **Planning** de opties **Op basis van gebeurtenis**, **Sjabloon**, **Toewijzingstype** en **Vervalrekening**.
    4. Selecteer **OK**.

5. Selecteer voor de regel de waarde **Niet-gefactureerde opbrengst** en voer vervolgens de volgende stappen uit:

    - Stel de optie **Niet-gefactureerde opbrengst** in op **Ja**.
    - Selecteer de rekeningen die u wilt gebruiken voor de opbrengst, korting en de tegenrekening voor niet-gefactureerde opbrengst.

6. Selecteer onder de factureringsplanning onder **Verwerking van niet-gefactureerde opbrengsten** de optie **Journaalboeking maken**. U kunt de journaalboeking desgewenst ook maken op de pagina **Massale verwerking van niet-gefactureerde opbrengsten**.
7. De uitstelplanning wordt gemaakt. U kunt de details bekijken op de pagina **Alle uitstelplanningen**. Nadat u de uitstelplanning hebt gemaakt, kunt u verschillende waarden bewerken voor het regelartikel van de factureringsplanning. U kunt bijvoorbeeld de stuksprijs, hoeveelheid of datums bewerken. De uitstelplanning wordt opnieuw berekend op basis van de nieuwe waarden.

De verdelingen worden opnieuw berekend op basis van het geselecteerde toewijzingstype (**Percentage**, **Voltooiingspercentage** of **Gelijke bedragen**). Voor het toewijzingstype **Variabele bedragen** wordt de verdeling opnieuw berekend op basis van het equivalente percentage van de beginwaarde voor de gebeurtenis. Stel dat de oorspronkelijke eenheidsprijs bijvoorbeeld $100,00 is en het percentage van de beginwaarde is $55,00 (55 procent). Als de eenheidsprijs wordt gewijzigd in $200,00, wordt het variabele bedrag van de gebeurtenis $110,00 (nog steeds 55 procent).

> [!NOTE]
> Als regels van de uitstelplanning zijn toegerekend, kan het regelartikel van de factureringsplanning niet worden bewerkt. Als u het regelartikel wilt bewerken, moet u eerst de herkende regels terugboeken. Daarna kunt u factureringsplanningsregel bijwerken.

### <a name="unbilled-revenue-and-top-billing"></a>Niet-gefactureerde opbrengsten en topfacturering

Een factureringsplanning wordt ingevoerd voor drie jaar en de facturen worden jaarlijks uitgegeven gedurende een periode van drie jaar. Het volledige contractbedrag wordt vastgelegd in de rekening voor niet-gefactureerde opbrengsten van waaruit de jaarfacturen worden gemaakt. De tegenrekening is de opbrengstrekening of de rekening voor uitgestelde opbrengsten.

Houd er rekening mee dat topfacturering en niet-gefactureerde opbrengsten niet samenwerken, omdat dit kan leiden tot reconciliatieproblemen in het grootboek. Op de pagina **Instellingen voor artikelgroep** is bijvoorbeeld artikelgroep A zodanig geconfigureerd dat het veld **Aantal regels bovenaan** is ingesteld op **2**. Op de pagina **Factureringsplanningen** worden drie artikelen toegevoegd. Alle drie de artikelen horen bij artikelgroep A. Wanneer de eerste journaalboeking voor de functie Niet-gefactureerde opbrengst wordt gemaakt, wordt het bedrag voor alle drie de artikelen naar de niet-gefactureerde rekening verwerkt. Wanneer de factuur voor de factureringsplanning wordt gemaakt, worden alleen de bedragen voor de bovenste twee artikelen opgenomen. Daarom komt het factuurbedrag niet overeen met het bedrag dat is verwerkt in de rekening voor niet-gefactureerde opbrengsten en leidt dit tot reconciliatieproblemen in het grootboek.

Als u niet-gefactureerde opbrengst wilt gebruiken, laat u de pagina **Instellingen voor artikelgroep** leeg of stelt u alle artikelgroepen in zodat het veld **Aantal regels bovenaan** wordt ingesteld op **0** (nul). Als u topfacturering wilt gebruiken, zijn er geen acties voor niet-gefactureerde opbrengsten beschikbaar.

### <a name="examples"></a>Voorbeelden

Vanaf versie 10.0.27 wordt een nieuwe rekening geïntroduceerd wanneer niet-gefactureerde opbrengst wordt gebruikt. Wanneer het initiële proces **Journaalpost maken** wordt geboekt, wordt het krediet uitgevoerd op een nieuwe tegenrekening voor niet-gefactureerde opbrengsten. Deze rekening wordt gebruikt in plaats van de opbrengstrekening, omdat dezelfde waarde moet worden teruggeboekt wanneer de factureringsplanning wordt gefactureerd. Als er wisselkoers- of afrondingsverschillen optreden, kunnen er tijdens het proces **Factuur genereren** verschillende bedragen worden berekend. Dit gedrag garandeert dat het nettobedrag van de rekeningen 0 (nul) is.

Dit voorbeeld laat zien hoe niet-gefactureerde opbrengsten worden gebruikt om het gehele bedrag van een contract op de balans toe te rekenen als niet-gefactureerde opbrengsten. Tegenover de invoer staat de tegenboeking van ongefactureerde opbrengst. Wanneer u de klant factureert, worden de niet-gefactureerde opbrengsten en de tegenrekening voor niet-gefactureerde opbrengsten tegengeboekt. De toerekening van opbrengsten vindt plaats op het moment van facturatie of volgens de geconfigureerde planning voor toerekening van uitstel.

#### <a name="assumptions"></a>Aannames

- Op 1 januari van het huidige jaar tekent een klant een contract voor drie jaar t.w.v. $390.
- Het contract bevat twee gedeelten: licenties en een onderhoudsovereenkomst.
- De verkoopprijs van de licentiekosten is $300 en de klant krijgt op 1 januari van elk contractjaar een factuur voor $100. De licentiekosten t.w.v. $300 worden ingevoerd als opbrengsten wanneer het contract wordt ondertekend.
- De verkoopprijs van de onderhoudskosten is $90 en de klant krijgt op 1 januari van elk contractjaar een factuur voor $30. De $90 aan onderhoudskosten worden uitgesteld en elke maand van de looptijd van het contract wordt $2,50 toegerekend.
- De klant krijgt aan het begin (1 januari) van elk van de drie contractjaren een factuur voor $130.

#### <a name="steps"></a>Stappen

1. Stel de twee vrijgegeven artikelen in als niet-gefactureerde artikelen. Op de pagina **Instellingen voor niet-gefactureerde opbrengst** kunt u de artikelen en rekeningen configureren die gebruikmaken van niet-gefactureerde opbrengst.
2. In dit voorbeeld worden de onderhoudskosten uitgesteld. Voor het artikel is een uitstelsjabloon nodig, die op de pagina **Uitstelsjablonen** is geconfigureerd. De sjabloon heeft als periodefrequentie **Maandelijks** en een toerekeningsperiode die 36 maanden lang is. Daarom bedraagd de opbrengst per maand $2,50.
3. Stel op de pagina **Artikelen die standaard worden uitgesteld** het veld **Onderhoudskosten** in op **Uitstelbaar artikel**. Deze stap en de volgende zorgen ervoor dat het onderhoudskostenartikel wordt uitgesteld als het wordt verkocht of opgenomen in een factureringsplanning.
4. Selecteer **Standaardwaarden voor uitstel** \> **Sjabloon** en voeg het artikel voor de onderhoudskosten en de lineaire sjabloon uit stap 2 toe. Het artikel voor de onderhoudskosten wordt gekoppeld aan een uitstelplanning van 36 maanden.
5. Maak een factureringsplanning met de twee niet-gefactureerde artikelen. De factureringsplanning voor het contract wordt geconfigureerd met de volgende artikelen.

    | Item | Begindatum | Einddatum | Bedrag | Factureringsfrequentie | Uitstelartikel | Niet-gefactureerde opbrengst | Description |
    |---|---|---|---|---|---|---|---|
    | Licentie | 1 januari, CJ | 31 december CJ +2 | $100,00 | Jaarlijks | Nr. | Ja | Aan de klant wordt elk jaar $100,00 in rekening gesteld. Het totaal van $300,00 wordt vooraf geregistreerd als niet-gefactureerde opbrengst op de balans en als opbrengst in winst en verlies. Elke factuur vermindert het niet-gefactureerde bedrag. |
    | Onderhoud | 1 januari, CJ | 31 december CJ +2 | $30,00 | Jaarlijks | Ja | Ja | Aan de klant wordt elk jaar $30,00 in rekening gesteld. Het totaal van $90,00 wordt vooraf geregistreerd als niet-gefactureerde opbrengst en als uitgestelde opbrengst op de balans. Elke factuur vermindert het niet-gefactureerde bedrag. De uitgestelde opbrengst wordt maandelijks toegerekend over 36 maanden. |

6. Met de optie **Journaalpost maken** op de pagina **Alle factureringsplanningen** kunt u de contractwaarde op de balans boeken als niet-gefactureerde opbrengst.

Er worden twee journaalposten gemaakt, één voor elke regel in de factureringsplanning.

| Rekening voor niet-gefactureerde opbrengst | Tegenrekening niet-gefactureerde opbrengst | Debetbedrag | Kredietbedrag |
|---|---|---|---|
| Rekening voor niet-gefactureerde opbrengst | | $300,00 | |
| | Tegenrekening niet-gefactureerde opbrengst | | $300,00 |

| Rekening voor niet-gefactureerde opbrengst | Uitgestelde opbrengst | Debetbedrag | Kredietbedrag |
|---|---|---|---|
| Rekening voor niet-gefactureerde opbrengst | | $90,00 | |
| |Uitgestelde opbrengst voor onderhoud | | $90,00 |

De eerste journaalboeking wordt geboekt naar een tegenrekening voor niet-gefactureerde opbrengsten en de tweede naar een rekening voor uitgestelde opbrengsten. Als de factureringsregel zowel niet-gefactureerde opbrengsten als uitgestelde opbrengsten bevat, wordt de rekening voor uitgestelde opbrengsten gebruikt, niet de tegenrekening voor niet-gefactureerde opbrengsten. Het contract vereist dat de factuur voor de klant aan het begin van elk jaar wordt opgesteld. U kunt de factuur maken met het proces **Factuur genereren**. Wanneer de factuur is gemaakt, worden de volgende journaalboekingen gemaakt.

| Hoofdrekening | Rekening voor niet-gefactureerde opbrengst | Debetbedrag | Kredietbedrag |
|---|---|---|---|
| Tegenrekening voor niet-gefactureerde opbrengst | | $100,00 | |
| | Rekening voor niet-gefactureerde opbrengst | | $100,00 |
| Debiteuren | | $100,00 | |
| | Opbrengstrekening | | $100,00 |

| Hoofdrekening | Rekening voor niet-gefactureerde opbrengst | Debetbedrag | Kredietbedrag |
|---|---|---|---|
| Rekening voor uitgestelde opbrengst voor onderhoud | | $30,00 | |
| | Rekening voor niet-gefactureerde opbrengst | | $30,00 |
| Debiteuren | | $30,00 | |
| | Rekening voor uitgestelde opbrengst voor onderhoud | | $30,00 |

Dezelfde journaalboeking wordt gemaakt door facturen die aan het begin van de volgende twee jaren worden geboekt. Het nettobedrag van de rekening voor uitgestelde opbrengsten is 0 (nul) omdat er geen afrondings- of wisselkoersverschillen zijn. De uitgestelde opbrengst moet exact worden teruggeboekt zoals deze is gecrediteerd tijdens het proces **Journaalpost maken**. Aangezien de opbrengst nog steeds is uitgesteld en later wordt toegerekend, wordt de rekening voor uitgestelde opbrengsten opnieuw gekrediteerd.

In de laatste stap wordt elke maand de journaalboeking voor het toerekeningsjournaal gemaakt om de uitgestelde opbrengst voor de onderhoudskosten toe te rekenen. De journaalboeking kan worden gemaakt op de pagina **Verwerking van toerekening**. U kunt de optie ook maken door op de pagina's **Uitstelplanning** de optie **Toerekenen** te selecteren voor de regels.

| Rekening voor uitgestelde opbrengst | Opbrengstrekening | Debetbedrag | Kredietbedrag |
|---|---|---|---|
| Uitgestelde opbrengst voor onderhoud | | $2,50 | |
| | Opbrengsten uit onderhoud | | $2,50 |

Deze journaalboeking wordt telkens gemaakt wanneer het toerekeningsproces wordt uitgevoerd voor dit uitgestelde artikel (in totaal 36 keer).

#### <a name="short-term-fixed-year"></a>Korte termijn: Vast jaar

U kunt niet-gefactureerde opbrengst samen met de functionaliteit voor de korte termijn gebruiken door op de pagina **Terugkerende contractfactureringsparameters** het veld **Korte termijn voor niet-gefactureerd** te configureren. In het volgende voorbeeld ziet u de berekeningen die worden uitgevoerd wanneer niet-gefactureerde opbrengsten worden gebruikt samen met de methode korte termijn voor niet-gefactureerd **Vast jaar**.

Een factureringsplanning wordt gemaakt met de volgende criteria:

- **Begindatum:** 1 juni 2020
- **Einddatum:** 31 december 2021
- **Eenheidsprijs:** $100
- **Frequentie:** Maandelijks

Op de pagina **Alle factureringsplanningen** wordt de eerste journaalboeking gemaakt via het proces **Journaalpost maken**. De huidige bedragen voor korte en lange termijn worden als volgt berekend:

- **Huidig kortlopend niet-gefactureerd opbrengstbedrag:** $700
- **Huidig langlopend niet-gefactureerd opbrengstbedrag:** $1200

De factuur wordt gemaakt voor de factureringsperiode van 1 juni 2020 tot en met 30 november 2020. De huidige bedragen voor korte en lange termijn worden als volgt berekend:

- **Huidig kortlopend niet-gefactureerd opbrengstbedrag:** $100
- **Huidig langlopend niet-gefactureerd opbrengstbedrag:** $1200

De factuur wordt gemaakt voor de factureringsperiode van 1 december 2020 tot en met 31 december 2020. De huidige bedragen voor korte en lange termijn worden als volgt berekend:

- **Huidig kortlopend niet-gefactureerd opbrengstbedrag:** $1200
- **Huidig langlopend niet-gefactureerd opbrengstbedrag:** $0

#### <a name="short-term-rolling-periods"></a>Korte termijn: Voortschrijdende perioden

U kunt niet-gefactureerde opbrengst samen met de functionaliteit voor de korte termijn gebruiken door op de pagina **Terugkerende contractfactureringsparameters** de methode Niet-gefactureerd voor korte termijn te configureren. In het volgende voorbeeld ziet u de berekeningen die worden uitgevoerd wanneer niet-gefactureerde opbrengsten worden gebruikt samen met de methode korte termijn voor niet-gefactureerd **Voortschrijdende perioden**.

Een factureringsplanning wordt gemaakt met de volgende criteria:

- **Begindatum:** 1 juni 2020
- **Einddatum:** 31 december 2021
- **Eenheidsprijs:** $100
- **Frequentie:** Maandelijks

Op de pagina **Alle factureringsplanningen** wordt de eerste journaalboeking gemaakt via het proces **Journaalpost maken**. De huidige bedragen voor korte en lange termijn worden als volgt berekend:

- **Huidig kortlopend niet-gefactureerd opbrengstbedrag:** $1200
- **Huidig langlopend niet-gefactureerd opbrengstbedrag:** $700

De factuur wordt gemaakt voor de factureringsperiode van 1 juni 2020 tot en met 30 november 2020. De huidige bedragen voor korte en lange termijn worden als volgt berekend:

- **Huidig kortlopend niet-gefactureerd opbrengstbedrag:** $1200
- **Huidig langlopend niet-gefactureerd opbrengstbedrag:** $100

De factuur wordt gemaakt voor de factureringsperiode van 1 december 2020 tot en met 31 december 2020. De huidige bedragen voor korte en lange termijn worden als volgt berekend:

- **Huidig kortlopend niet-gefactureerd opbrengstbedrag:** $1200
- **Huidig langlopend niet-gefactureerd opbrengstbedrag:** $0

### <a name="items-with-revenue-allocation"></a>Artikelen met opbrengsttoerekening

Twee artikelen met verschillende factureringsfrequenties worden toegevoegd aan een factureringsplanning. Beide maken gebruik van niet-gefactureerde opbrengsten en zijn uitstelbare artikelen.

- **Artikelnummer 1000:** Surface Pro 128KEN

    - **Factureringsfrequentie:** Eenmalig
    - **Eenheidsprijs:** $1500
    - **Zelfstandige verkoopprijs:** $1600
    - **Contractopbrengsten:** $1465,26

- **Artikelnummer S0021:** Verzekering die wordt verkocht samen met artikelnummer 1000

    - **Factureringsfrequentie:** Maandelijks gedurende 12 maanden
    - **Eenheidsprijs:** $20 per maand
    - **Zelfstandige verkoopprijs:** $25
    - **Contractopbrengsten:** $264,74

Omdat beide artikelen gebruik maken van niet-gefactureerde opbrengst en opbrengsttoerekening, is het totale contractbedrag op de verlengingsregel 0 (nul). De kolom **Contractopbrengsten** wordt toegevoegd en toont het bedrag van de contractopbrengsten.

In de volgende tabel ziet u de eerste journaalboeking voor de artikelen en de factuur.

| Rekening voor niet-gefactureerde opbrengst | Rekening voor uitgestelde opbrengst | Debetbedrag | Kredietbedrag |
|---|---|---|---|
| **Journaalboeking voor artikel 1000** | | | |
| Debetrekening voor niet-gefactureerde opbrengsten (401250) | | $1465,26 | |
| | Kredietrekening voor uitgestelde opbrengst (250600) | | $1465,26 |
| **Journaalboeking voor artikel 0021** | | | |
| Debetrekening voor niet-gefactureerde opbrengsten (401250) | | $274,74 | |
| | Kredietrekening voor uitgestelde opbrengst (250600) | | $274,74 |
| **Factuur** | | | |
| | Kredietrekening voor niet-gefactureerde opbrengst | | $1465,26 |
| | Kredietrekening voor niet-gefactureerde opbrengst | | $274,74 |
| Debetrekening leveranciers (130100) | | $1488,16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Wijzigingen in de factureringsplanningsregel, factuurdetailregel of opbrengsttoerekening

Wanneer de eenheidsprijs of de hoeveelheid wordt gewijzigd, moet het contractopbrengstbedrag worden bijgewerkt voor elk artikel dat deel uitmaakt van de opbrengsttoerekening. Daarom wordt de journaalboeking opnieuw berekend.

Stel dat de eenheidsprijs voor artikel 1000 wordt gewijzigd van $1500 naar $1600. In dit geval wordt het contractopbrengstbedrag automatisch opnieuw berekend op $1549,47. De contractopbrengsten voor artikel S0021 worden opnieuw berekend op $290,53.

Wanneer de wijziging wordt bevestigd en vastgelegd, worden de eerste journaalboekingen voor beide artikelen teruggeboekt en worden nieuwe journaalboekingen gemaakt:

- **Artikel 1000:** de oorspronkelijke oorspronkelijke journaalboeking van $1465,26 wordt teruggeboekt. Een nieuwe journaalboeking voor $1549,47 wordt gemaakt.
- **Artikel S0021:** de oorspronkelijke oorspronkelijke journaalboeking van $274,74 wordt teruggeboekt. Een nieuwe journaalboeking voor $290,53 wordt gemaakt.

#### <a name="termination"></a>Beëindiging

Artikel S0021 heeft een begindatum in januari 2020 en een einddatum in december 2020, maar wordt beëindigd in juni 2020. Het contractopbrengstbedrag voor beide artikelen moet opnieuw worden berekend:

- **Artikel 1000:** de contractopbrengsten worden opnieuw berekend op $1567,67.
- **Artikel S0021:** de contractopbrengsten worden opnieuw berekend op $124,00.

Er wordt een correctiejournaalboeking gemaakt voor de regel die is beëindigd. De journaalboeking voor de regel die bij hetzelfde MEA-nummer (multiple element arrangement) hoort, wordt teruggeboekt en er wordt een nieuwe journaalboeking gemaakt:

- **Artikel 1000:** de oorspronkelijke oorspronkelijke journaalboeking van $1465,26 wordt teruggeboekt. Een correctiejournaalboeking voor $1549,47 wordt gemaakt.
- **Artikel S0021:** de oorspronkelijke oorspronkelijke journaalboeking van $274,74 wordt teruggeboekt. Een nieuwe journaalboeking voor $124,00 wordt gemaakt.
