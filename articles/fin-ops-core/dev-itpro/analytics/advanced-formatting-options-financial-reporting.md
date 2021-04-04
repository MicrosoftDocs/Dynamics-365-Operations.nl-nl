---
title: Geavanceerde opmaakopties in financiële rapportage
description: In dit onderwerp worden functies voor geavanceerde opmaak beschreven, waaronder filters, beperkingen, niet-afdrukrijen en voorwaardelijke instructies in berekeningen.
author: panolte
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 08659bac84b07f6e95a83b84612cb035b51cf28d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568461"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>Geavanceerde opmaakopties in financiële rapportage

[!include [banner](../includes/banner.md)]

Wanneer u een rapport in financiële rapportage maakt, zijn aanvullende opmaakfuncties beschikbaar, zoals filters voor dimensies, beperkingen voor kolommen en rapporteringseenheden, niet-afdrukbare rijen en IF/THEN/ELSE-instructies in berekeningen.

In de volgende tabel worden de geavanceerde opmaakfuncties uitgelegd die beschikbaar zijn wanneer u rapporten ontwerpt.

| Functie                   | Beschrijving |
|----------------------------|-------------|
| Dimensiefilter           | Om specifieke sets van gegevens te openen, kunt u dimensies in de rijdefinitie en kolomdefinitie gebruiken. Veel rapporten gebruiken alleen het natuurlijke segment in de rij-opmaak. Rijen kunnen echter worden gewijzigd zodat deze dimensiewaarden bevatten. Dimensiefilters in de kolomdefinitie worden gebruikt om specifieke dimensiewaarden te openen. |
| Beperking van rapportage-eenheid | U kunt een rapportrij instellen zodat deze alleen informatie weergeeft die aan een specifieke rapportage-eenheid is gekoppeld. |
| Niet af te drukken rijen (NP)     | Niet af te drukken rijen zijn handig in veel rapporten. Als verschillende berekeningen zijn vereist om een waarde te verkrijgen, kunnen deze berekeningen in het afgedrukte rapport worden verborgen. Niet af te drukken rijen zijn ook nuttig voor het oplossen van problemen met rapportontwerpen en voor geavanceerde celplaatsing. |
| Kolombeperking         | De kolombeperking in de rijdefinitie is handig om waarden te verbergen die alleen op sommige rijen van het rapport relevant zijn. Wanneer de percentageberekeningen op een rij zijn uitgevoerd, voorkomt de kolombeperking dat totaalkolommen of andere kolommen worden afgedrukt wanneer die cijfers niet van toepassing zijn. |
| Kolomeinde               | U kunt kolomeinden toevoegen aan een rijdefinitie om rapportinformatie naast elkaar weer te geven. U kunt meerdere kolomeinden in één rijdefinitie toevoegen. De kolomkoppen worden dan herhaald boven aan elke kolom na het kolomeinde. Opmerkingen voor een rapport worden tussen de kolomeinden weergegeven. |
| IF/THEN/ELSE-constructies     | U kunt berekeningen in een rijdefinitie of kolomdefinitie wijzigen. |
| Enkele aanhalingstekens (' ') en een ampersand (&) gebruiken voor dimensiewaarden | U kunt dimensiewaarden gebruiken, inclusief het &-teken voor het ontwerpen van een rapport. |

## <a name="advanced-cell-placement"></a>Geavanceerde celplaatsing

Geavanceerde celplaatsing, of *forcering* is het plaatsen van specifieke waarden in specifieke cellen. Forcering wordt bijvoorbeeld vaak gebruikt om het juiste saldo in een cashflowoverzicht te plaatsen. U kunt forcering voor de volgende doeleinden gebruiken:

- Waarden te verplaatsen vanuit Microsoft Excel in specifieke cellen.
- Specifieke waarden vastleggen in een rapport.
- Tekens wijzigen door een waarde van een vorige cel te kopiëren en die waarde te vermenigvuldigen door -1.

> [!NOTE]
> In veel gevallen moet u uw rapportdefinitie configureren zodat de kolomberekeningen vóór rijberekeningen worden uitgevoerd. Volg deze stappen om deze configuratie te voltooien.
>
> 1. Open in Report Designer de rapportdefinitie.
> 2. Selecteer op het tabblad **Instellingen**, onder **Berekeningsprioriteit** de optie **Eerst kolomberekening en daarna rij uitvoeren**.

## <a name="designing-the-report"></a>Het rapport ontwerpen

Wanneer u een rapport ontwerpt, moet u alle detailrijen eerst maken om ervoor te zorgen dat de waarden er zoals u verwacht in worden getrokken. Voeg vervolgens opmaakopheffingen van het type **NP** (No Print) toe om het detail te onderdrukken dat de eindwaarden bevat.

> [!IMPORTANT]
> Wanneer u de opmaakcode **CAL** in de rijdefinitie gebruikt, kunt u geen detailgegevens weergeven voor de transacties.

Voor forcering gebruiken formules de volgende opmaak: &lt;bestemmingskolom&gt;=&lt;oorspronkelijke kolom&gt;.&lt;rijcode&gt; Scheid eventuele aanvullende plaatsingen voor een rij door een komma en een spatie. Een voorbeeld: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Voorbeelden van geavanceerde opmaakopties

De volgende voorbeelden geven aan hoe u de rijdefinitie en kolomdefinitie opmaakt om een basiscashflowrapport (voorbeeld 1) en een statistisch rapport (voorbeeld 2) te forceren.

### <a name="example-1-basic-forcing"></a>Voorbeeld 1: Basisfocering

De volgende tabel toont een voorbeeld van een rijdefinitie die basisforcering gebruikt.

| Rijcode |           Omschrijving            | Opmaakcode | Verwante formules/rijen/eenheden |        Rijmodificator        | Koppeling naar financiële dimensies |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | Contanten aan het begin van periode (NP) |             |                             | Rekeningmodificator = \[/BB\] | +Segment2 = \[1100\]         |
| 130      | Kas aan begin van periode      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> Lege kolommen zijn verwijderd uit de vorige tabel voor presentatiedoeleinden: de kolommen Opmaak negeren, Normaal saldo, Afdrukbeheer, Kolombeperking worden niet weergegeven.

De volgende tabel toont een voorbeeld van een kolomdefinitie die basisforcering in de rij gebruikt.

|           Format             | V   | B    | C        | D      | E      | Vr    |
|------------------------------|-----|------|----------|--------|--------|------|
| Koptekst 1                     |     |      |          |        |        |      |
| Koptekst 2                     | V   | B    | C        | D      | E      | Vr    |
| Koptekst 3                     |     |      |          |        |        |      |
| Kolomtype                  | ROW | DESC | FD       | FD     | FD     | CALC |
| Categorie boekcode/-kenmerk |     |      | WERKELIJK   | WERKELIJK | WERKELIJK |      |
| Fiscaal jaar                  |     |      | BASE     | BASE   | BASE   |      |
| Periode                       |     |      | BASE     | BASE   | BASE   |      |
| Behandelde perioden              |     |      | PERIODIEK | YTD/BB | YTD    |      |
| Formule                      |     |      |          |        |        | E-D  |
| Kolombreedte                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Voorbeeld 2: statistische rapporten

De volgende tabel toont een voorbeeld van een rijdefinitie die forcering voor een statistisch rapport gebruikt.

| Rijcode | Beschrijving               | Opmaakcode | Verwante formules/rijen/eenheden     | Opmaak negeren      | Normaal saldo | Koppeling naar financiële dimensies               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | Statistische gegevens   | REM         |                                 |                      |                |                                            |
| 100      | Aantal werknemers - VS.            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | Aantal werknemers - internationaal | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 130      |                           |             |                                 |                      |                |                                            |
| 190      | Verkoop VS                  |             |                                 |                      | C              | +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Internationale verkoop       |             |                                 |                      | C              | +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | Verkoop VS                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | Internationale verkoop       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> Lege kolommen zijn verwijderd uit de vorige tabel voor presentatiedoeleinden: de kolommen Opmaak negeren, Kolombeperking en Rijmodificator worden niet weergegeven.

De volgende tabel toont een voorbeeld van een kolomdefinitie die forcering voor een statistisch rapport gebruikt.

|    Format                    | V   | B    | C      | D            | E     | Vr            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Koptekst 1                     | V   | B    | C      | D            | E     | Vr            |
| Koptekst 2                     | -   | -    | JTD    | Jaarlijkse verkoop | Medewerker | $ per persoon |
| Koptekst 3                     |     |      |        |              |       |              |
| Kolomtype                  | ROW | DESC | FD     | CALC         | CALC  | CALC         |
| Categorie boekcode/-kenmerk |     |      | WERKELIJK |              |       |              |
| Fiscaal jaar                  |     |      | BASE   |              |       |              |
| Periode                       |     |      | BASE   |              |       |              |
| Behandelde perioden              |     |      | YTD    |              |       |              |
| Formule                      |     |      |        |              |       | E-D          |
| Kolombreedte                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Een rij beperken tot een specifieke rapportage-eenheid

Wanneer een rapportrij beperkt is tot een specifieke rapportage-eenheid, geeft die rij alleen de bijbehorende gegevens voor de genoemde rapportage-eenheid weer en negeert deze de gegevens voor andere rapportage-eenheden in de rapportagestructuur. U kunt bijvoorbeeld een rij maken die gegevens voor de totale bedrijfskosten voor een specifieke afdeling bevat. Uw rapport bevat mogelijk dubbele gegevens als het rapport zowel een rapportagestructuur als een rijdefinitie bevat met meer dan alleen de natuurlijke rekening. U hebt bijvoorbeeld een rapportagestructuur van de zes afdelingen in uw organisatie en u hebt ook een rijdefinitie die een specifieke combinatie van een rekening en een afdeling in de rij vermeldt. Wanneer u het rapport genereert, wordt de specifieke combinatie van een rekening en een afdeling afgedrukt op elk niveau van de rapportagestructuur, hoewel die afdeling misschien niet overeenkomt met wat zich in de structuur bevindt. Dit gedrag treedt op doordat de rij negeert wat meestal door de rapportdefinitie wordt uitgefilterd. Een manier waarop u verdubbeling van gegevens kunt voorkomen is door een rij te beperken tot een specifieke rapportage-eenheid.

> [!NOTE]
> Als een rij dimensies bevat en u die rij beperkt tot een onderliggende rapportage-eenheid, wordt het rijbedrag voor die onderliggende eenheid en voor de bovenliggende eenheden opgenomen, maar treedt geen duplicatie op.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Een rij beperken tot een rapportage-eenheid

1. Klik in Report Designer op **Rijdefinities** en selecteer vervolgens een rijdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Verwante formules/rijen/eenheden**.
3. Selecteer in het dialoogvenster **Rapporteringseenheden selecteren** in het veld **Rapporteringsstructuur** de structuur die is toegewezen in de rapportdefinitie.
4. Selecteer een rapportage-eenheid en klik op **OK**. De beperking wordt weergegeven in de cel van de rijdefinitie.
5. Dubbelklik op de cel in de kolom **Koppeling naar financiële dimensies** van de beperkte rij en voer vervolgens een koppeling naar het financiële gegevenssysteem in.

## <a name="selecting-print-control-in-a-row-definition"></a>Afdrukbeheer in een rijdefinitie selecteren

U kunt voor elke kolom afdrukbeheercodes opgeven met de cel **Afdrukbeheer**.

### <a name="add-print-control-codes-to-a-report-row"></a>Afdrukcontrolecodes toevoegen aan een rapportrij

1. Open in Report Designer de rijdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Afdrukbeheer**.
3. Selecteer in het dialoogvenster **Afdrukbeheer** een afdrukbeheercode of houd de toets Ctrl ingedrukt om meerdere codes te selecteren. U kunt afdrukbeheercodes ook rechtstreeks in de cel **Afdrukbeheer** typen. Gebruik komma's om meerdere afdrukbeheercodes te scheiden.
4. Selecteer een van de voorwaardelijke afdrukopties.
5. Klik tot slot op **OK**.

### <a name="regular-print-control-codes"></a>Normale afdrukcontrolecodes

De volgende tabel beschrijft de normale afdrukbeheercodes voor een rijdefinitie.

| Afdrukcontrolecode | Interpretatie van de afdrukbeheercode         | Beschrijving |
|--------------------|--------------------------------------------------|-------------|
| NP                 | Niet af te drukken rij                                 | Voorkom dat de bedragen in de rij op het rapport worden afgedrukt en sluit de bedragen van berekeningen uit. Om een niet af te drukken kolom in een berekening op te nemen, raadpleegt u de kolom rechtstreeks in de berekeningsformule. De niet af te drukken rij 240 is bijvoorbeeld opgenomen in de volgende berekening: **230+240+250**. De niet af te drukken rij 240 is echter niet opgenomen in de volgende berekening: **230:250**. |
| CS                 | Valutasymbool; gebruik de valuta-opmaak in deze rij | Neem het valutasymbool op in alle niet-percentagebedragen. Percentagewaarden krijgen nooit een valutasymbool. |
| XD                 | Rij onderdrukken in het rapport met rekeningdetails            | Onderdruk de weergave van rekeningen op rapporten met rekeningdetails en rapporten met transactiedetails. Deze afdrukbeheeroptie is handig wanneer een rij meerdere rekeningen bevat die niet in het rapport met rekeningdetails of rapport met transactiedetails mogen worden weergegeven. |
| X0                 | Rijen onderdrukken indien allemaal nullen                        | Sluit een rij uit van het rapport als alle cellen in die rij leeg zijn of nullen bevatten. Deze afdrukbeheeroptie is alleen zinvol wanneer de optie om nulsaldi te onderdrukken niet in de rapportdefinitie is geselecteerd. |
| B0                 | Nulkolommen leeg laten                         | Laat kolommen leeg in een rij die nulbedragen bevat. |
| XR                 | Samentelling onderdrukken                                  | Onderdruk een samentelling. Als het rapport een rapportagestructuur gebruikt, worden de bedragen in deze rij niet samengeteld in volgende bovenliggende knooppunten. |
| SR                 | Afronding onderdrukken                                | Voorkom dat de bedragen in deze rij worden afgerond. |
| XT                 | Rij onderdrukken in het rapport met transactiedetails        | Onderdruk de weergave van transacties in rapporten met transactiedetails. Deze afdrukbeheeroptie is handig wanneer een rij meerdere rekeningen bevat die niet in een rapport met transactiedetails mogen worden weergegeven. |

### <a name="conditional-print-control-codes"></a>Voorwaardelijke afdrukcontrolecodes

De volgende tabel beschrijft de voorwaardelijke afdrukbeheercodes voor een rijdefinitie.

| Afdrukcontrolecode | Beschrijving                                  |
|--------------------|----------------------------------------------|
| (geen)             | Wis de voorwaardelijke afdrukselectie.       |
| DR                 | Druk alleen de debetsaldi voor deze rij af.  |
| CR                 | Druk alleen de creditsaldi voor deze rij af. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Cel Kolombeperking in een rijdefinitie

De cel **Kolombeperking** in een rijdefinitie heeft meerdere doeleinden. Afhankelijk van het type van rij kunt u de cel **Kolombeperking** gebruiken om een van de volgende functies op te geven:

- De cel kan de afdruk van rijbedragen beperken tot een specifieke kolom. Deze functie is handig als u een balans in tabelvorm maakt.
- De cel kan de kolom van bedragen opgeven die moet worden gesorteerd.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Een berekeningsformule gebruiken in een rijdefinitie

Een berekeningsformule in een rijdefinitie kan de operatoren **+**, **-**, **\**_ en _*/** bevatten en ook **IF/THEN/ELSE**-constructies. Bovendien kan een berekening afzonderlijke cellen en absolute bedragen (werkelijke cijfers die in de formule zijn opgenomen) bevatten. De formule kan maximaal 1024 tekens bevatten. De berekeningen kunnen niet worden toegepast op rijen die cellen bevatten van het type **Koppeling naar financiële dimensies** (FD). U kunt echter berekeningen in opeenvolgende rijen opnemen, het afdrukken van die rijen onderdrukken en vervolgens het totaal van de berekeningsrijen berekenen.

### <a name="operators-in-a-calculation-formula"></a>Operatoren in een berekeningsformule

Een berekeningsformule gebruikt complexere operatoren dan een rijtotaalformule. U kunt echter de operatoren **\**_ en _*/** samen met de extra operatoren gebruiken om bedragen te vermenigvuldigen (\*) en te delen (/). Om een bereik of som in een berekeningsformule te gebruiken, moet u een @-teken gebruiken voor de rijcode, tenzij u een kolom in de rijdefinitie gebruikt. Om bijvoorbeeld het bedrag in rij 100 op te tellen bij het bedrag in rij 330, kunt u de rijtotaalformule **100+330** of de berekeningsformule **@100+@330** gebruiken.

> [!NOTE]
> U moet een @-teken gebruiken voor elke rijcode die u in een berekeningsformule gebruikt. Anders wordt het cijfer gelezen als een absoluut bedrag. De formule **@100+330** voegt bijvoorbeeld EUR 330 toe aan het bedrag in rij 100. Wanneer u verwijst naar een kolom in een berekeningsformule, is een @-teken niet vereist.

### <a name="create-a-calculation-formula"></a>Een berekeningsformule maken

1. Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Opmaakcode** en selecteer vervolgens **CAL**.
3. Typ de berekeningsformule in de cel **Gerelateerde formules/rijen/eenheden**.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Voorbeeld van een berekeningsformule voor specifieke rijen

In dit voorbeeld betekent de berekeningsformule **@100+@330** dat het bedrag in rij 100 wordt opgeteld bij het bedrag in rij 330. Met de rijtotaalformule **340 + 370** wordt het bedrag in rij 340 opgeteld bij het bedrag in rij 370. (Het bedrag in rij 370 is het bedrag van de berekeningsformule.)

| Rijcode | Beschrijving                 | Opmaakcode | Gerelateerde formules/rijen/eenheid | Afdrukbeheer | Rijmodificator | Koppeling naar financiële dimensies |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Kas aan begin van periode |             |                            | NP            | BB           | +Account=\[1100:1110\]       |
| 370      | Kas aan begin van jaar   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Kas aan begin van periode | TOT         | 340+370                    |               |              |                              |

Wanneer de rij in een rijdefinitie de opmaakcode **CAL** heeft en u een rekenkundige berekening in de cel **Gerelateerde formules/rijen/eenheden** invoert, moet u de letter van de gekoppelde kolom en rij ook invoeren op het rapport. Voer bijvoorbeeld **A.120** in voor kolom A, rij 120. U kunt ook een apenstaartje (@) gebruiken om alle kolommen aan te geven. Voer bijvoorbeeld **@120** in voor alle kolommen in rij 120. Een wiskundige berekening die geen kolomletter of een apenstaartje (@) bevat, wordt beschouwd als een reëel getal.

> [!NOTE]
> Als u een labelrijcode gebruikt om naar een rij te verwijzen, moet u een punt (.) gebruiken als scheidingsteken tussen de kolomletter en het label (bijvoorbeeld **A.GROSSMARGIN\_A.SALES**). Als u een @-teken gebruikt, is een scheidingsteken niet vereist (bijvoorbeeld **\@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Voorbeeld van een berekeningsformule voor een specifieke kolom

In dit voorbeeld houdt de berekeningsformule **E=C.340** in dat de berekening in de cel in kolom C, rij 340, alleen wordt toegepast op kolom E.

> [!NOTE]
> Wanneer u verwijst naar een kolom in een berekeningsformule, is een @-teken niet vereist.

| Rijcode | Beschrijving                 | Opmaakcode | Gerelateerde formules/rijen/eenheid | Afdrukbeheer | Rijmodificator | Koppeling naar financiële dimensies |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Contanten aan het begin van periode |             |                            | NP            | BB           | +Account=\[1100:1110\]       |
| 370      | Contanten aan het begin van jaar   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Contanten aan het begin van periode | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Een cijfer wijzigen in geselecteerde kolommen

Als u een cijfer of berekening in een kolom van een bepaalde rij wijzigt, zonder invloed op andere kolommen op het rapport, kunt u **CAL** (Berekening) opgeven in de kolom **Opmaakcode** van de rijdefinitie.

- Als u een berekening wilt uitvoeren voor alle kolommen (**FD**) van het rapport, voert u geen kolomtoewijzing in.
- Als u een formule tot specifieke kolommen wilt beperken, voert u de kolomletter, een gelijkteken (**=**) en de formule in.
- U kunt meerdere kolommen opgeven. Wanneer u een @-teken met specifieke kolomplaatsing gebruikt, wordt het @-teken gekoppeld aan de rij.
- U kunt meerdere kolomformules in één rij invoeren. Scheid de formules met behulp van komma's.

### <a name="calculation-examples"></a>Voorbeelden van berekening

| Berekening            | Actie die is gemaakt                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Voor elke kolom wordt de waarde in rij 130 vermenigvuldigd met 0,75. Het resultaat wordt dan in de huidige rij van elke kolom geplaatst. |
| B=@130\*.75            | Dezelfde berekening wordt alleen uitgevoerd op kolom B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*,75 B=(B.100/B.130)\*,75 C=(C.100/C.130)\*,75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE-constructies in een rijdefinitie

**IF/THEN/ELSE**-constructies kunnen aan elke geldige berekening worden toegevoegd en met de **CAL**-opmaak worden gebruikt. U voert **IF/THEN/ELSE**-berekeningsformules in de cel in de kolom **Gerelateerde formules/rijen/eenheden** in. **IF/THEN/ELSE**-berekeningsformules gebruiken de volgende opmaak: IF &lt;true/false statement&gt; THEN &lt;formula&gt; ELSE &lt;formula&gt;. Het gedeelte **ELSE &lt;formula&gt;** van de constructie is optioneel.

#### <a name="if-statements"></a>IF-constructies

De constructie die de **IF**-constructie volgt kan elke constructie zijn die kan worden beoordeeld als waar of onwaar. De constructie die de **IF**-constructie volgt kan een eenvoudige evaluatie bevatten of kan een complexe constructie zijn die meerdere expressies bevat. Hieronder vindt u enkele voorbeelden:

- **IF A.200&gt;0** (Eenvoudige evaluatie)
- **IF A.200&gt;0 AND A.200&lt;10.000** (Complexe constructie)
- **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (Complexe constructie die meerdere expressies bevat)

De term **Perioden** in een **IF**-constructie geeft het aantal perioden voor het rapport weer. Deze term wordt meestal gebruikt om een jaar-tot-datum gemiddelde te berekenen. Wanneer u bijvoorbeeld een rapport voor periode 7 JTD uitvoert, betekent de **B.150/Periods**-constructie dat de waarde in rij 150 van kolom B is gedeeld door 7.

#### <a name="then-and-else-formulas"></a>THEN- en ELSE-formules

De **THEN**- en **ELSE**-formules kunnen elke geldige berekening zijn, van zeer eenvoudige waardetoewijzingen tot complexe formules. De constructie **IF A.200&gt;0 THEN A=B.200** betekent bijvoorbeeld: 'Als de waarde in de cel in kolom A van rij 200 meer is dan 0 (nul), plaats dan de waarde van de cel in kolom B van rij 200 in de cel in kolom A van de huidige rij.' De voorafgaande **IF/THEN**-constructie plaatst een waarde in één kolom van de huidige rij. U kunt echter ook een @-teken gebruiken in waar/onwaar-evaluaties of de formule om alle kolommen te vertegenwoordigen. Hier volgen enkele voorbeelden die in de volgende secties worden beschreven:

- **IF A.200 &gt;0 THEN B.200**: Als de waarde in cel A.200 positief is, wordt de waarde van cel B.200 in elke kolom van de huidige rij geplaatst.
- **IF A.200 &gt;0 THEN @200**: Als de waarde in cel A.200 positief is, wordt de waarde van elke kolom in rij 200 in de overeenkomstige kolom in de huidige rij geplaatst.
- **IF @200 &gt;0 THEN @200**: Als de waarde in rij 200 van de huidige kolom positief is, wordt de waarde van rij 200 in dezelfde kolom in de huidige rij geplaatst.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Een berekening beperken tot een rapportage-eenheid in een rijdefinitie

Als u een berekening wilt beperken tot één rapportage-eenheid in een rapportagestructuur, zodat het resulterende bedrag niet wordt opgeteld bij een eenheid op een hoger niveau, kunt u de **\@Unit**-code in de cel **Gerelateerde formules/rijen/eenheden** gebruiken in de rijdefinitie. De **\@Unit**-code wordt vermeld in kolom B van de rapportagestructuur, **Naam van eenheid**. Wanneer u de **\@Unit**-code gebruikt, worden de waarden niet opgeteld, maar wordt de berekening beoordeeld op elk niveau van de rapportagestructuur.

> [!NOTE]
> Als u deze functie wilt gebruiken, moet u een rapportagestructuur koppelen aan de rijdefinitie.

De berekeningsrij kan naar een berekeningsrij of een financiële gegevensrij verwijzen. De berekening is geregistreerd in de cel **Gerelateerde formules/rijen/eenheden** van de rijdefinitie en de beperking van het type Financiële gegevens. De berekening moet een voorwaardelijke berekening gebruiken die begint met een **IF \@Unit**-constructie. Een voorbeeld: IF @Unit(SALES) THEN @100 ELSE 0 Deze berekening bevat het bedrag van rij 100 in elke kolom van het rapport, maar alleen voor de verkoopeenheid. Als meerdere eenheden de naam VERKOOP hebben, wordt het bedrag in elk van die eenheden weergegeven. Bovendien kan rij 100 een financiële gegevensrij zijn en als niet af te drukken rij worden gedefinieerd. In dit geval wordt voorkomen dat het bedrag in alle eenheden in de structuur wordt weergeven. U kunt het bedrag ook beperken tot één kolom van het rapport, zoals kolom H, door een kolombeperking te gebruiken om de waarde alleen in die kolom van het rapport af te drukken. U kunt **OR**-combinaties opnemen in een **IF**-constructie. Hier is een voorbeeld: **IF @Unit(VERKOOP) OR @Unit(SALESWEST) THEN 5 ELSE @100**. U kunt op een van de volgende manieren een eenheid in een beperking van het type berekening opgeven:

- Voer een eenheidsnaam in om eenheden op te nemen die overeenkomen. Zo schakelt **IF \@Unit(VERKOOP)** de berekening in voor elke eenheid met de naam VERKOOP, zelfs als zich verschillende eenheden VERKOOP in de rapportagestructuur bevinden.
- Voer de naam van het bedrijf en de eenheidnaam in om de berekening te beperken tot specifieke eenheden in een specifiek bedrijf. Voer bijvoorbeeld **IF @Unit (ACME:VERKOOP)** in om de berekening in eenheden VERKOOP in het ACME-bedrijf te beperken.
- Voer de volledige hiërarchiecode van de rapportagestructuur in om de berekening te beperken tot een specifieke eenheid. Voer bijvoorbeeld **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)** in.

> [!NOTE]
> Als u de volledige hiërarchische code zoekt, klikt u met de rechtermuisknop in de rapporteringsstructuurdefinitie en selecteert u vervolgens **Rapporteringseenheid-id kopiëren (H-code)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Een berekening beperken tot een rapporteringseenheid

1. Klik in Rapportontwerper op **Rijdefinities** en open vervolgens de rijdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Opmaakcode** en selecteer vervolgens **CAL**.
3. Klik op de cel **Gerelateerde formules/rijen/eenheden** en voer vervolgens een voorwaardelijke berekening in die begint met een **IF \@Unit**-constructie.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE-constructies in een kolomdefinitie

Een **IF/THEN/ELSE**-constructie zorgt ervoor dat elke berekening kan afhangen van de resultaten van een andere kolom. U kunt naar andere kolommen verwijzen, maar u kunt niet naar een rapportcel in de **IF**-constructie verwijzen. Elke berekening moet op de hele kolom worden toegepast. De constructie **IF B&gt;100 THEN B ELSE C\*1.25** betekent bijvoorbeeld 'als het bedrag in kolom B meer is dan 100, plaats dan de waarde van kolom B in de kolom **CALC**. Als het bedrag in kolom B niet meer dan 100 is, vermenigvuldig de waarde in kolom C met 1,25 en plaats het resultaat in de kolom **CALC**.' Volg altijd de **IF**-instructie met een logische instructie die kan worden beoordeeld als waar of onwaar. Formules die u voor zowel de **THEN**-constructie als de **ELSE**-constructie kunt gebruiken, bevat verwijzingen naar elk cijfer van de kolommen. Deze formules kunnen zo complex zijn als u ze wilt maken.

> [!NOTE]
> U kunt de resultaten van een berekening niet in een andere kolom plaatsen. De resultaten moeten in de kolom zijn die de formule bevat.

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>Enkele aanhalingstekens en een ampersand gebruiken voor dimensiewaarden in een rij, kolom of structuur

U kunt rapporten ontwerpen met behulp van dimensiewaarden die een ampersand (&) bevatten.

In een veld **Koppeling naar financiële dimensies** kunt u een waarde invoeren zoals **'W&V'**. Het opnemen van enkele aanhalingstekens (' ') aan beide zijden van de dimensiewaarde geeft aan dat u de letterlijke waarde gebruikt, zoals bijvoorbeeld het ampersand-teken (&).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
