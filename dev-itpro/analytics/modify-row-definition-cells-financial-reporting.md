---
title: Rijdefinitiecellen wijzigen
description: In dit artikel wordt beschreven welke informatie is vereist voor elke cel in een rijdefinitie in een financieel rapport en wordt uitgelegd hoe u die gegevens invoert.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 40ae4e0774c5752d697baba6c8add8aaf44fbb6d
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="modify-row-definition-cells"></a>Rijdefinitiecellen wijzigen

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven welke informatie is vereist voor elke cel in een rijdefinitie in een financieel rapport en wordt uitgelegd hoe u die gegevens invoert. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Een rij in een rijdefinitie opgeven

In rijdefinities bepalen de nummers of labels in de cel **Rijcode** elke regel in de rijdefinitie. U kunt de rijcode opgeven om te verwijzen naar gegevens in berekeningen en totalen.

### <a name="row-code-requirements"></a>Vereisten van rijcode

Een rijcode is vereist voor alle rijen. U kunt numerieke, alfanumerieke en niet-ingestelde (lege) rijcodes mengen in een rijdefinitie. De rijcode kan elk positief geheel getal (onder 100.000.000) zijn of een beschrijvend label dat die rij identificeert. Een beschrijvend label moet aan deze regels voldoen:

-   Het label moet met een alfabetisch teken (a tot en met z of A tot en met Z) beginnen en kan elke combinatie van cijfers en letters tot 16 tekens zijn. 
    > [!NOTE]
    > Een label kan het onderstrepingstekenteken (\_) bevatten. Geen andere speciale tekens zijn toegestaan.
-   Het label mag de volgende voorbehouden woorden niet gebruiken: EN, OF, ALS, TOEN, ANDERS, PERIODEN, TOT, BASISRIJ, EENHEID, NULL, CPO of RPO.

De volgende voorbeelden zijn geldige rijcodes:

-   320
-   TL\_NET\_INKOMSTEN
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Een rijcode in een rijdefinitie wijzigen

1.  Klik in Report Designer op **Rijdefinities** en open vervolgens de rijdefinitie die u wilt wijzigen.
2.  Typ in de juiste rij de nieuwe waarde in de cel in de kolom **Rijcode**.

### <a name="reset-numeric-row-codes"></a>Numerieke rijcodes opnieuw instellen

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2.  Klik in het menu **Bewerken** op **Rijen opnieuw nummeren**.
3.  Geef in het dialoogvenster **Rijen opnieuw nummeren** nieuwe waarden op voor de beginrijcode en de verhogingswaarde van de rijcode. U kunt de numerieke rijcodes opnieuw instellen op waarden met gelijke tussenruimte. De rapportontwerper nummert echter alleen rijcodes opnieuw die met cijfers beginnen (bijvoorbeeld 130 of 246). Rijcodes die met letters beginnen (bijvoorbeeld INCOME\_93 of TP0693) worden niet opnieuw genummerd. 
> [!NOTE]
> Wanneer u rijcodes opnieuw nummert. werkt de rapportontwerper **TOT**- en **CAL**-verwijzingen automatisch bij. Als een **TOT**-rij bijvoorbeeld verwijst naar een reeks die begint met rijcode 100 en u rijen opnieuw nummert, te beginnen met 90, verandert de beginverwijzing **TOT** van 100 in 90.

## <a name="add-a-description"></a>Een omschrijving toevoegen
De omschrijvingscel biedt de omschrijving van de financiële gegevens in de rij van het rapport, zoals 'opbrengst' of 'netto-inkomsten'. De tekst in de cel **Omschrijving** wordt in het rapport precies weergegeven zoals u deze in de rijdefinitie invoert. 
> [!NOTE]
> De breedte van de omschrijvingskolom op het rapport wordt ingesteld in de kolomdefinitie. Als de tekst in de kolom **Omschrijving** in de rijdefinitie lang is, controleert u de breedte van de kolom **DESC**. Wanneer u het dialoogvenster **Rijen invoegen van** gebruikt, zijn de waarden in de kolom **Omschrijving** de segmentwaarden of dimensiewaarden van de financiële gegevens. U kunt rijen invoegen om beschrijvende tekst toe te voegen, zoals een sectiekoptekst of een sectietotaal, en om opmaak toe te voegen, zoals een regel vóór een totaalrij. Als het rapport een rapportagestructuur bevat, kunt u de aanvullende tekst opnemen die is gedefinieerd voor de rapportage-eenheden in de rapportagestructuur. U kunt de aanvullende tekst ook beperken tot een specifieke rapportage-eenheid.

### <a name="add-the-description-for-a-line-on-a-report"></a>De omschrijving voor een regel op een rapport toevoegen

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2.  Selecteer de cel **Omschrijving** en voer vervolgens de naam van de rapportrij in.
3.  Pas de opmaak toe.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Aanvullende tekst van een rapportagestructuur toevoegen aan de omschrijving

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2.  Geef de aanvullende tekstcode en elke andere tekst op in de juiste cel **Omschrijving**.
3.  Pas de opmaak toe.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>De aanvullende tekst beperken tot een specifieke rapportage-eenheid

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2.  Zoek de rij waar de aanvullende tekst moet worden gemaakt en dubbelklik vervolgens op de cel in de kolom **Gerelateerde formules/rijen/eenheden**.
3.  Selecteer een structuur in het dialoogvenster **Selectie van rapportage-eenheid** in het veld **Rapportagestructuur**.
4.  Vouw in het veld **Rapportage-eenheid voor beperking selecteren** de rapportagestructuur uit of samen en selecteer vervolgens een rapportage-eenheid.

## <a name="add-a-format-code"></a>Een opmaakcode toevoegen
De cel **Opmaakcode** biedt een selectie van vooraf opgemaakte keuzes voor de inhoud van die rij. Als de cel **Opmaakcode** leeg is, wordt de rij geïnterpreteerd als een rij met financiële gegevens. 
> [!NOTE]
> Als een rapport opmaakrijen bevat die geen bedragrij en die zijn gerelateerd aan bedragrijen die zijn onderdrukt (bijvoorbeeld omdat hun saldi nul zijn). kunt u de kolom **Gerelateerde formules/rijen/eenheden** gebruiken om te voorkomen dat titel- en opmaakrijen worden afgedrukt.

### <a name="add-a-format-code-to-a-report-row"></a>Een opmaakcode toevoegen aan een rapportrij

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens een rijdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Opmaakcode**.
3.  Selecteer een opmaakcode in de lijst. De volgende tabel beschrijft de opmaakcodes en hun acties.
    | Opmaakcode                   | Interpretatie van de opmaakcode | Actie|
    |---|---|---|
    | (Geen)                        |                                    | Wist de cel **Opmaakcode**.                                                                                                                                                                               |
    | TOT                           | Totaal                              | Identificeert een rij die wiskundige operatoren gebruikt in de kolom **Gerelateerde formules/rijen/eenheden**. De totalen bevatten eenvoudige operatoren, zoals **+** of **-**.                                                      |
    | CAL                           | Berekening                        | Identificeert een rij die wiskundige operatoren gebruikt in de kolom **Gerelateerde formules/rijen/eenheden**. De berekeningen bevatten complexe operatoren, zoals **+**, **-**, **\***, **/** en **IF/THEN/ELSE**-instructies. |
    | DES                           | Omschrijving                        | Identificeert een kopregel of een lege regel op een rapport.                                                                                                                                                        |
    | LFT RGT CEN                   | Links rechts midden                  | Lijnt de tekst van de rijomschrijving op de rapportpagina uit, ongeacht de positie van de tekst in de kolomdefinitie.                                                                                               |
    | CBR                           | Basisrij wijzigen                    | Identificeert een rij die de basisrij voor kolomberekeningen instelt.                                                                                                                                               |
    | COLUMN                        | Kolomeinde                       | Begint een nieuwe kolom in het rapport.                                                                                                                                                                             |
    | PAGE                          | Pagina-einde                         | Begint een nieuwe pagina in het rapport.                                                                                                                                                                               |
    | ---                           | Enkele onderstreping                   | Plaatst één lijn onder alle bedragkolommen op het rapport.                                                                                                                                                     |
    | ===                           | Dubbele onderstreping                   | Plaatst een dubbele lijn onder alle bedragkolommen op het rapport.                                                                                                                                                     |
    | LINE1                         | Dunne lijn                          | Tekent één dunne lijn over de pagina.                                                                                                                                                                      |
    | LINE2                         | Dikke lijn                         | Tekent één dikke lijn over de pagina.                                                                                                                                                                     |
    | LINE3                         | Stippellijn                        | Tekent één stippellijn over de pagina.                                                                                                                                                                    |
    | LINE4                         | Dikke lijn en dunne lijn           | Tekent één dubbele lijn over de pagina. De bovenste lijn is dik en de onderste lijn is dun.                                                                                                                       |
    | LINE5                         | Dunne lijn en dikke lijn           | Tekent één dubbele lijn over de pagina. De bovenste lijn is dun en de onderste lijn is dik.                                                                                                                       |
    | BXB BXC                       | Rij in vakken                          | Trekt een vak rond de rapportrijen die beginnen met de rij **BXB** en eindigen met de rij **BXC**.                                                                                                               |
    | REM                           | Opmerking                             | Identificeert een rij die een opmerkingrij is en niet op het rapport moet worden afgedrukt. Een opmerkingsrij kan bijvoorbeeld uw opmaaktechnieken verklaren.                                                            |
    | SORT ASORT SORTDESC ASORTDESC | Sorteren                               | Sorteert onkosten en opbrengsten, sorteert een werkelijk of budgetafwijkingrapport op de grootste afwijking, of sorteert de rijomschrijvingen op alfabetische volgorde.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>Gerelateerde formules/rijen/eenheden opgeven
De cel **Gerelateerde formules/rijen/eenheden** heeft meerdere doeleinden. Afhankelijk van het type rij, kan een cel **Gerelateerde formules/rijen/eenheden** een van de volgende taken uitvoeren:

-   De rijen bepalen die in een berekening moeten worden opgenomen wanneer u een **TOT**-opmaakcode of een **CAL**-opmaakcode gebruikt.
-   Een opmaakrij koppelen aan een bedragrij, zodat de opmaak alleen wordt afgedrukt als het gerelateerde bedrag wordt afgedrukt.
-   Een rij beperken tot een specifieke rapportage-eenheid.
-   De basisrij voor berekeningen definiëren wanneer u de opmaakcode **BASEROW** gebruikt.
-   De te sorteren rijen definiëren wanneer u de opmaakcodes voor sorteren gebruikt.

### <a name="use-a-row-total-in-a-row-definition"></a>Een rijtotaal gebruiken in een rijdefinitie

Gebruik een rijtotaalformule om bedragen in andere rijen toe te voegen of af te trekken. Een formule voor het maken van een rijtotaal kan de operatoren + en - bevatten om afzonderlijke rijcodes en -bereiken te combineren. De bereiken worden aangeduid door een dubbelepunt (:). De formule kan maximaal 1024 tekens bevatten. Hier is een voorbeeld van een standaard totaalformule: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Onderdelen van een rijtotaalformule

Wanneer u een rijtotaalformule maakt, moet u rijcodes gebruiken om op te geven welke rijen u wilt toevoegen aan of wilt aftrekken van de huidige rijdefinitie en moet u operatoren gebruiken om op te geven hoe de rijen worden gecombineerd. De totaalrijen en bedragrijen kunnen in elke combinatie worden gebruikt. **Opmerking:** Alle totaalrijen binnen een bereik zijn uitgesloten. Om een eindtotaal te maken, kunt u de reeks rijen opgeven. Als de eerste rij van een bereik een totaalrij is, wordt die rij opgenomen in het nieuwe totaal. De volgende tabel beschrijft hoe de operatoren worden gebruikt in rijtotaalformules.

| Operator | Voorbeeld van formule | Omschrijving                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Voegt het bedrag in rij 100 toe aan het bedrag in rij 330.        |
| :        | 100:330         | Voegt de totalen toe van alle rijen tussen rij 100 en rij 330.    |
| -        | 100-330         | Trekt het bedrag in rij 100 af van het bedrag in rij 330. |

### <a name="create-a-row-total"></a>Een rijtotaal maken

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Opmaakcode** in de rijdefinitie en selecteer **TOT**.
3.  Voer in de cel **Gerelateerde formules/rijen/eenheden** de totale formule in.

### <a name="relate-a-format-row-to-an-amount-row"></a>Een opmaakrij koppelen aan een bedragrij

In de kolom **Opmaakcode** in een rijdefinitie passen de opmaakcodes **DES**, **LFT**, **RGT**, **CEN**, **---** en **===** opmaak toe op niet-bedragrijen. Om te voorkomen dat deze opmaak wordt afgedrukt wanneer de bijbehorende bedragrijen worden onderdrukt (bijvoorbeeld omdat de bedragrijen nulwaarden of geen periodeactiviteit bevatten), moet u de opmaakrijen koppelen aan de bijbehorende bedragrijen. Deze functie is handig wanneer u wilt voorkomen dat koptekst of opmaak die is gekoppeld aan subtotalen wordt afgedrukt als er voor de periode geen details af te drukken zijn. 
    > [!NOTE]
    >  You can also prevent the detailed amount rows from being printed by clearing the option to display rows without amounts. This option is located on the **Settings** tab of the report definition. By default, transaction detail accounts that have a zero balance or no period activity are suppressed in reports. To show these transaction detail accounts, select the **Display rows without an amounts** check box on the **Settings** tab of the report definition.

### <a name="relate-a-format-row-to-an-amount-row"></a>Een opmaakrij koppelen aan een bedragrij

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens een rijdefinitie die u wilt wijzigen.
2.  Voer in de opmaakrij in de cel **Gerelateerde formules/rijen/eenheden** de rijcode in van de bedragrij die u wilt onderdrukken. **Opmerking:** Om een bedragrij te onderdrukken, moet het saldo van de rij 0 (nul ) zijn. Een bedragrij met een saldo wordt niet onderdrukt.
3.  Klik in het menu **Bestand** op **Opslaan**.

### <a name="example-of-preventing-printing-of-rows"></a>Voorbeeld van het voorkomen van het afdrukken van rijen

In het volgende voorbeeld wil Phyllis voorkomen dat de koptekst en onderstrepingstekens in de rij **Kastotaal** van haar rapport worden afgedrukt, omdat er geen activiteit in een van de rekeningen van contant geld is. Daarom voert ze in rij 220 (die, zoals de opmaakcode **---** aangeeft, een opmaakrij is) in de cel **Gerelateerde formules/rijen/eenheden** **250** in, wat de rijcode is van de bedragrij die ze wil onderdrukken. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>De basisrij voor een kolomberekening selecteren
Bij relationele rapportage wijst u één of meer basisrijen in de rijdefinitie toe door de opmaakcode **CBR** (basisrij wijzigen) te gebruiken. Een basisrij wordt vervolgens verwezen door een berekening in de kolomdefinitie. Hieronder staan enkele typische voorbeelden van CBR-berekeningen:

-   Percentage van de totale opbrengst wanneer deze is gekoppeld aan afzonderlijke opbrengstartikelen
-   Percentage van de totale onkosten wanneer deze is gekoppeld aan afzonderlijke onkostenartikelen
-   Percentage van brutomarge wanneer deze is gekoppeld aan divisie- of afdelingsdetails.

Een of meer basisrijen worden gedefinieerd in de rijdefinitie, en dan bepaalt de kolomdefinitie de relatie waarin de basisrij wordt gerapporteerd. De code die in de kolomformule wordt gebruikt is **BASEROW**. De volgende wiskundige basisbewerkingen worden gebruikt met **BASEROW**: delen, vermenigvuldigen, optellen of aftrekken. De bewerking die het vaakst wordt gebruikt is delen door **BASEROW**, waarin het resultaat wordt weergegeven als een percentage. De kolomberekeningen die **BASEROW** gebruiken in de formule, gebruiken de rijdefinitie voor de gerelateerde codes van de basisrij. **CBR**-rijen hebben de volgende kenmerken:

-   **CBR**-rijen worden niet afgedrukt op het ingevulde rapport.
-   De **CBR**-opmaakcode en de gerelateerde rijcode worden geplaatst boven de rij of de sectie die gerelateerde berekeningen weergeeft.

In een kolomdefinitie geeft het kolomtype **CALC** een kolom aan die een formule in de rij **Formule** opgeeft. Deze formule werkt op de gegevens voor deze kolom van het rapport en gebruikt het trefwoord 'Baserow' op berekeningen te baseren op de **CBR**-opmaakcodes in de rij. In de rijdefinitie bepaalt de opmaakcode **CBR** de basisrij voor kolommen die een percentage berekenen van of vermenigvuldigen met de basisrij voor elke rij in het rapport. U kunt meerdere **CBR**-opmaakcodes in een rij hebben, zoals één voor nettoverkoop, één voor brutoverkoop en één voor totale onkosten. Meestal wordt de **CBR**-opmaakcode gebruikt om een percentage te maken voor rekeningen die met een totale regel worden vergeleken. Een basisrij wordt gebruikt voor alle berekeningen tot een andere basisrij is gedefinieerd. U moet een **CBR**-beginopmaakcode en **CBR**-eindopmaakcode definiëren. Om bijvoorbeeld onkosten als een percentage van nettoverkoop te bepalen, kunt u de waarde in elke onkostenrij delen door de waarde in de rij met nettoverkoop. In dit geval is de rij met nettoverkoop de basisrij. U kunt een kolomdefinitie definiëren die huidige en eerdere resultaten rapporteert, samen met een basispercentage van elk resultaat, zoals in het onderstaande voorbeeld. Begin met gedetailleerd inkomensoverzicht.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Selecteer de basisrij in een rijdefinitie voor een kolomberekening

1.  Klik in Report Designer op **Kolomdefinities** en open vervolgens de kolomdefinitie voor een inkomensoverzicht.
2.  Voeg een nieuwe kolom toe aan de kolomdefinitie en stel het kolomtype in op **CALC**.
3.  Voer in de cel **Formule** van de nieuwe kolom de formule **X/BASEROW** in, waarbij **X** het kolomtype **FD** is waarvan u een percentage wilt bekijken.
4.  Dubbelklik op de cel **Opmaak/valuta negeren**.
5.  Selecteer in het dialoogvenster **Opmaak negeren** in de lijst **Opmaakcategorie** de optie **Percentage** en klik op **OK**.
6.  Klik in het menu **Bestand** op **Opslaan als** om de kolomdefinitie onder een andere naam op te slaan. Voeg **CBR** toe aan de huidige bestandsnaam (bijvoorbeeld **CUR\_YTD\_CBR**). Deze kolomdefinitie is de kolomdefinitie van uw basisrij.
7.  Klik in Report Designer op **Rijdefinities** en open vervolgens de te wijzigen rijdefinitie door de basisrijberekening te gebruiken.
8.  Voeg een nieuwe rij in boven de rij waar de basisrijberekening moet beginnen.
9.  Dubbelklik op de cel **Opmaakcode** van de rijdefinitie en selecteer vervolgens **CBR**.
10. Voer in de cel **Gerelateerde formules/rijen/eenheden** het rijcodenummer voor de basisrij in.

### <a name="example-of-base-row-calculation"></a>Voorbeeld van basisrijberekening

In het volgende voorbeeld van een rijdefinitie toont rij 100 aan dat de basisrij voor berekeningen rij 280 is. [![Voorbeeld van basisrijberekening](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) In het volgende voorbeeld van een kolomdefinitie gebruikt de berekening de opmaakcode **CBR**. De berekening in kolom C deelt de waarde in kolom B van het rapport door de waarde in rij 280 van kolom B. De opmaakopheffing in kolom B drukt het resultaat van de berekening af als een percentage. Op dezelfde manier is elk bedrag in kolom E het bedrag in kolom D als een percentage van nettoverkoop. [![Voorbeeld van kolomdefinitie.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Het volgende voorbeeld toont een rapport dat kan worden gegenereerd op basis van de vorige berekeningen. [![Voorbeeldrapport op basis van vorige voorbeeldberekeningen.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Een sorteercode selecteren voor een rijdefinitie
Sorteercodes sorteren rekeningen of waarden, sorteren een werkelijk of budgetafwijkingrapport op de grootste afwijking of sorteren de rijomschrijvingen op alfabetische volgorde. De volgende sorteercodes zijn beschikbaar:

-   **SORT** - Sorteert het rapport in oplopende volgorde, op basis van de waarden in de opgegeven kolom.
-   **ASORT** - Sorteert het rapport in oplopende volgorde, op basis van de absolute waarde van de waarden in de opgegeven kolom. Met andere woorden, het teken van elke waarde wordt genegeerd wanneer de waarden worden gesorteerd. Deze opmaakcode rangschikt de waarden volgens de magnitude van de afwijking, ongeacht of de afwijking positief of negatief is.
-   **SORTDESC** - Sorteert het rapport in aflopende volgorde, op basis van de waarden in de opgegeven kolom.
-   **ASORTDESC** - Sorteert het rapport in aflopende volgorde, op basis van de absolute waarde van de waarden in de opgegeven kolom.

### <a name="select-a-sorting-code"></a>Een sorteercode selecteren

1.  Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Opmaakcode** en selecteer vervolgens een sorteercode.
3.  Geef in de cel **Gerelateerde formules/rijen/eenheden** het bereik op van te sorteren rijcodes. Om een bereik op te geven, voert u het volgende in: de eerste rijcode, een dubbelepunt (:) en de laatste rijcode. Voer bijvoorbeeld **160:490** in om op te geven dat het bereik van rij 160 tot rij 490 is.
4.  Voer in de cel **Kolombeperking** de letter in van de rapportkolom die voor het sorteren moet worden gebruikt. 
    > [!NOTE]
    > Neem alleen bedragrijen op in een sorteerberekening.

### <a name="examples-of-ascending-and-descending-column-values"></a>Voorbeelden van oplopende en aflopende kolomwaarden

In het volgende voorbeeld worden de waarden in kolom D van het rapport gesorteerd in oplopende volgorde voor de rijen 160 tot en met 490. Daarnaast worden de absolute waarden in kolom G van het rapport gesorteerd in aflopende volgorde voor de rijen 610 tot en met 940.

| Rijcode | Beschrijving                                         | Opmaakcode | Gerelateerde formules/rijen/eenheden | Normaal saldo | Kolombeperking | Koppeling naar financiële dimensies |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Gesorteerd op maandelijkse afwijking in oplopende volgorde       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Verkoop                                               |             |                             | C              |                    | 4100                         |
| 190      | Verkoopretouren                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Rente inkomen                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Gesorteerd op JTD absolute afwijking in aflopende volgorde | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Verkoop                                               |             |                             | C              |                    | 4100                         |
| 640      | Verkoopretouren                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Rente inkomen                                     |             |                             | C              |                    | 7000                         |

Hier volgt een voorbeeld van het rapport dat wordt gegenereerd.

|||||||||
|---|---|---|---|---|---|---|
|**Afwijkingsanalyse (gesorteerd op afwijking)**|||||||

|**Regio's Beijing en Atlanta**|||||||

|**Voor de zeven maanden die eindigen op 31 juli 2013**|||||||

||**Juli**|**JTH**|||||

||**Werkelijk**|**Budget**|**Afwijking**|**Werkelijk**|**Budget**|**Afwijking**|

|**Gesorteerd op maandelijkse afwijking in oplopende volgorde**|||||||

|COGS|873.872|236.144|(637.728)|4.864.274|1.590.315|(3.273.959)|

|Lonen en salarissen|97.624|65.573|(32.051)|653.884|441.664|(212.220)| |Verkoopkortingen|36.383|24.152|(12.231)|241.562|162.670|(78.892)| |Verkoopretouren|10.917|7.246|(3.671)|62.809|48.803|(14.006)| |Onkosten verhuren|12.052|9.019|(3.033)|80.444|60.748|(19.696)| |Onkosten kantoor|5.023|3.291|(1.732)|33.420|22.098|(11.322)| |Reiskosten|7.656|7.641|(15)|51.062|51.469|407| |Verkoop|1.240.119|410.389|829.730|7.139.288|2.764.549|4.374.739| |**Absolute afwijking JTD in aflopende volgorde gesorteerd**||||||| |Verkoop|1.240.119|410.389|829.730|7.139.288|2.764.549|4.374.739| |Reiskosten|7.656|7.641|(15)|51.062|51.469|407| |Onkosten kantoor|5.023|3.291|(1.732)|33.420|22.098|(11.322)| |Verkoopretouren|10.917|7.246|(3.671)|62.809|48.803|(14.006)| |Onkosten verhuren|12.052|9.019|(3.033)|80.444|60.748|(19.696)| |Verkoopkortingen|36.383|24.152|(12.231)|241.562|162.670|(78.892)| |Lonen en salarissen|97.624|65.573|(32.051)|653.884|441.664|(212.220)| |COGS|873.872|236.144|(637.728)|4.864.274|1.590.315|(3.273.959)|

## <a name="specify-a-format-override-cell"></a>Een cel voor opmaakopheffing opgeven
De cel **Opmaakopheffing** geeft de opmaak op die voor de rij wordt gebruikt wanneer het rapport wordt afgedrukt. Deze opmaak negeert de opmaak die in de kolomdefinitie en de rapportdefinitie is opgegeven. Standaard is valuta de opmaakcode die in deze definities is opgegeven. Als één rij van het rapport het aantal activa, zoals het aantal gebouwen, weergeeft en een andere rij de monetaire waarde van die activa, kunt u de valutaopmaak negeren en een numerieke opmaak invoeren voor de rij die het aantal gebouwen opgeeft. U kunt deze informatie opgeven in het dialoogvenster **Opmaakopheffing**. De beschikbare opties zijn afhankelijk van de opmaakcategorie die u selecteert. Het gebied **Voorbeeld** van het dialoogvenster toont voorbeeldopmaak. De volgende opmaakcategorieën zijn beschikbaar:

-   Valutaopmaak
-   Numerieke opmaak
-   Percentage-opmaak
-   Aangepaste opmaak

### <a name="override-cell-formatting"></a>Celopmaak negeren

1.  Open in Report Designer de rijdefinitie die u wilt wijzigen.
2.  In de rij waar u de opmaak wilt negeren, dubbelklikt u op de cel in de kolom **Opmaakopheffing**.
3.  Selecteer in het dialoogvenster **Opmaakopheffing** de opmaakopties die u voor rij in het rapport wilt gebruiken.
4.  Klik tot slot op **OK**.

### <a name="currency-formatting"></a>Valutaopmaak

Valutaopmaak is van toepassing op een fiscaal bedrag en bevat het valutasymbool. De volgende opties zijn beschikbaar:

-   **Valutasymbool** - Het valutasymbool voor het rapport. Deze waarde overschrijft de instelling **Landinstellingen** voor de bedrijfsgegevens.
-   **Negatieve getallen** - Negatieve getallen kunnen een minteken (-) hebben, tussen haakjes worden weergegeven of een driehoek (∆) hebben.
-   **Aantal decimalen** - Het aantal cijfers dat na de komma moet worden weergegeven.
-   **Tekst voor nulwaardevervanging** - De tekst die in het rapport wordt opgenomen wanneer het bedrag 0 (nul) is. Deze tekst verschijnt als laatste regel in het gebied **Voorbeeld**. 
    > [!NOTE]
    >  Als de afdruk voor nulwaarden of geen periodeactiviteit wordt onderdrukt, wordt deze tekst onderdrukt.

### <a name="numeric-formatting"></a>Numerieke opmaak

Numerieke opmaak is van toepassing op elk bedrag en bevat geen valutasymbool. De volgende opties zijn beschikbaar:

-   **Negatieve getallen** - Negatieve getallen kunnen een minteken (-) hebben, tussen haakjes worden weergegeven of een driehoek (∆) hebben.
-   **Aantal decimalen** - Het aantal cijfers dat na de komma moet worden weergegeven.
-   **Tekst voor nulwaardevervanging** - De tekst die in het rapport wordt opgenomen wanneer het bedrag 0 (nul) is. Deze tekst verschijnt als laatste regel in het gebied **Voorbeeld**. 
    > [!NOTE]
    >  Als de afdruk voor nulwaarden of geen periodeactiviteit wordt onderdrukt, wordt deze tekst onderdrukt.

### <a name="percentage-formatting"></a>Percentage-opmaak

Percentage-opmaak bevat het procentteken (%). De volgende opties zijn beschikbaar:

-   **Negatieve getallen** - Negatieve getallen kunnen een minteken (-) hebben, tussen haakjes worden weergegeven of een driehoek (∆) hebben.
-   **Aantal decimalen** - Het aantal cijfers dat na de komma moet worden weergegeven.
-   **Tekst voor nulwaardevervanging** - De tekst die in het rapport wordt opgenomen wanneer het bedrag 0 (nul) is. Deze tekst verschijnt als laatste regel in het gebied **Voorbeeld**. 
    > [!NOTE]
    >  Als de afdruk voor nulwaarden of geen periodeactiviteit wordt onderdrukt, wordt deze tekst onderdrukt.

### <a name="custom-formatting"></a>Aangepaste opmaak

Gebruik de aangepaste opmaakcategorie om een aangepaste opmaakopheffing te maken. De volgende opties zijn beschikbaar:

-   **Type** – De aangepaste opmaak.
-   **Tekst voor nulwaardevervanging** - De tekst die in het rapport wordt opgenomen wanneer het bedrag 0 (nul) is. Deze tekst verschijnt als laatste regel in het gebied **Voorbeeld**. 
    > [!NOTE]
    >  Als de afdruk voor nulwaarden of geen periodeactiviteit wordt onderdrukt, wordt deze tekst onderdrukt.

Het type moet de positieve waarde en daarna de negatieve waarde vertegenwoordigen. Doorgaans voert u een vergelijkbare opmaak in die positieve en negatieve waarden onderscheidt. Als u bijvoorbeeld wilt aangeven dat zowel positieve als negatieve waarden twee decimalen hebben, maar negatieve waarden tussen haakjes worden weergegeven, voert u **0.00;(0.00)** in. De volgende tabel geeft aangepaste opmaak weer die u kunt gebruiken om de opmaak van uw waarden te beheren. Alle voorbeelden beginnen vanaf de waarde 1234.56.

| Opmaak                         | Positief   | Negatief     | Nul    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1,235      | (1235)      | (Leeg) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1234,56   | (1234,56)   | nul    |
| 0,00%;(0,00%)                  | 123456,00% | (123456,00%) | 0,00%   |

## <a name="specify-a-normal-balance-cell"></a>Een cel Normale saldo opgeven
De cel **Normaal saldo** in een rijdefinitie bepaalt het teken van de bedragen in een rij. Als u het teken van een rij wilt omkeren of als het normale saldo van een rekening een krediet is, typt u een **C** in de cel **Normaal saldo** voor die rij. Report Designer keert het teken om in alle creditsaldorekeningen in die rij. Wanneer de rapportontwerper deze rekeningen converteert, verwijdert deze het debet-/creditkenmerk van alle bedragen, waardoor het berekenen van de totaalbedragen gemakkelijk wordt. Om bijvoorbeeld netto-inkomsten te berekenen, trekt u onkosten af van inkomsten. Doorgaans worden de rijen waarvan het totaal is berekend en de berekende rijen niet beïnvloed door een **C**-code. Het **XCR**-afdrukbeheer in de kolomdefinitie keert echter het teken om van elke rij die een **C** bevat in de kolom **Normaal saldo**. Deze opmaak is vooral belangrijk wanneer u alle ongunstige afwijkingen wilt weergeven als negatieve bedragen. Als een totaal of berekend cijfer het verkeerde teken heeft, typt u een **C** in de cel **Normaal saldo** voor de rij waar het teken moet worden omgekeerd.

## <a name="specify-a-row-modifier-cell"></a>Een cel Rijmodificator opgeven
De inhoud van de cel **Rijmodificator** in een rijdefinitie negeert de fiscale jaren, perioden en andere informatie die zijn opgegeven in de kolomdefinitie voor die rij. De geselecteerde modificator is van toepassing op elke rekening in de rij. U kunt elke rij wijzigen door een of meer van de volgende typen modificators te gebruiken:

-   Rekeningmodificators
-   Boekcodemodificators
-   Rekening- en transactiekenmerken

### <a name="override-a-column-definition"></a>Een kolomdefinitie negeren

1.  Open in Report Designer de rijdefinitie die u wilt wijzigen.
2.  Dubbelklik in de rij waar u de kolomdefinitie wilt negeren op de cel **Rijmodificator**.
3.  Selecteer in het dialoogvenster **Rijmodificator** een optie in het veld **Rekeningmodificator**. Raadpleeg de sectie 'Rekeningmodificators' voor een omschrijving van de opties.
4.  Selecteer in het veld **Boekcodemodificator** de boekcode die u voor de rij wilt gebruiken.
5.  Volg de stappen onder **Kenmerken** om een invoer toe te voegen voor elk kenmerk dat in de rijcode moeten worden opgenomen:
    1.  Dubbelklik op de cel **Kenmerk** en selecteer een kenmerknaam. **Waarschuwing:** Vervang het hekje (\#) door een numerieke waarde.
    2.  Dubbelklik op de cel **Van** en voer de eerste waarde voor het bereik in.
    3.  Dubbelklik op de cel **Tot** en voer de laatste waarde voor het bereik in.

6.  Klik tot slot op **OK**.

### <a name="account-modifiers"></a>Rekeningmodificators

Wanneer u een specifieke rekening selecteert, combineert de rapportontwerper de rekening en de fiscale jaren, perioden en andere informatie die u in de kolomdefinitie opgeeft. U kunt andere informatie, zoals verschillende boekperioden, gebruiken voor specifieke rijen. De volgende tabel geeft de rekeningmodificators weer die beschikbaar zijn. Vervang het hekje (\#) met een waarde die gelijk is aan of kleiner is dan het aantal perioden in een fiscaal jaar.

| Rekeningmodificator | Wat wordt afgedrukt                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Het beginsaldo voor een rekening.                                                     |
| /\#              | Het saldo van de opgegeven periode.                                                     |
| /-\#             | Het saldo voor de periode die \# perioden vóór de huidige periode ligt.                  |
| /+\#             | Het saldo voor de periode die \# perioden na de huidige periode ligt.                   |
| /C               | Het saldo van de huidige periode.                                                       |
| /C-\#            | Het saldo voor de periode die \# perioden vóór de huidige periode ligt.                  |
| /C+\#            | Het saldo voor de periode die \# perioden na de huidige periode ligt.                   |
| /Y               | Het saldo van jaar-tot-datum tot de huidige periode.                                      |
| /Y-\#            | Het saldo voor het jaar tot datum tot de periode die \# perioden vóór de huidige periode ligt. |
| /Y+\#            | Het saldo voor het jaar tot datum tot de periode die \# perioden na de huidige periode ligt.  |

### <a name="book-code-modifiers"></a>Boekcodemodificators

U kunt een rij beperken tot een bestaande boekcode. De kolomdefinitie moet ten minste één **FD**-kolom met een boekcode bevatten. 
> [!NOTE]
> De boekcodebeperking voor een rij negeert de boekcodebeperkingen in de kolomdefinitie voor die rij.

### <a name="account-and-transaction-attributes"></a>Rekening- en transactiekenmerken

Sommige boekhoudsystemen ondersteunen rekeningkenmerken en transactiekenmerken in de financiële gegevens. Deze kenmerken functioneren als virtuele accountsegmenten en kunnen extra informatie over de rekening of transactie dragen. Deze extra informatie kan het volgende zijn: rekening-id's, batch-id's, postcodes of andere kenmerken. Als uw boekhoudsysteem kenmerken ondersteunt, kunt u rekeningkenmerken of transactiekenmerken gebruiken als rijmodificators in de rijdefinitie. Raadpleeg de sectie 'Een kolomdefinitie negeren' eerder in dit artikel voor informatie over hoe u rij-informatie negeert.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Een cel Koppeling naar financiële dimensies opgeven
De cel **Koppeling naar financiële dimensies** bevat koppelingen naar de financiële gegevens die in elke rij van een rapport moeten worden opgenomen. Deze cel bevat dimensiewaarden, maar u kunt in plaats daarvan cellen in een Microsoft Excel-werkblad opgeven, of daarnaast segmentwaarden of dimensiewaarden. Om het dialoogvenster **Dimensies** te openen, dubbelklikt u op de cel **Koppeling naar financiële dimensies**. 
> [!NOTE]
> Report Designer kan geen rekeningen, dimensies of velden uit het Microsoft Dynamics ERP-systeem selecteren die een van de volgende gereserveerde tekens bevatten: &, \*, \[, \], { of }. Om informatie voor een rij op te geven die zich al in de rijdefinitie bevindt, voegt u de informatie toe aan de cel **Koppeling naar financiële dimensies**. Om nieuwe rijen toe te voegen die naar de financiële gegevens koppelen, gebruikt u het dialoogvenster **Rijen invoegen van** om nieuwe rijen in de rapportdefinitie te maken. De kolomtitel wijzigt, afhankelijk van hoe de kolom is geconfigureerd, zoals weergegeven in de volgende tabel.

| Koppelingstype dat is ingeschakeld       | De omschrijving van de Koppelingskolom wijzigt hiernaar |
|----------------------------------|----------------------------------------------------|
| Financiële dimensies             | Koppeling naar financiële dimensies                       |
| Extern werkblad               | Koppeling naar werkblad                                  |
| Financiële dimensies + werkblad | Koppeling naar financiële dimensies + werkblad           |
| Rapport van Management Reporter       | Rapport van Management Reporter                         |

### <a name="specify-a-dimension-or-range"></a>Een dimensie of bereik opgeven

1.  Open in Report Designer de rijdefinitie die u wilt wijzigen.
2.  Dubbelklik op een cel in de kolom **Koppeling naar financiële dimensies**.
3.  Dubbelklik in het dialoogvenster **Dimensies** op een cel onder de dimensienaam.
4.  Selecteer **Persoon of bereik** in het dialoogvenster voor de dimensie.
5.  Voer in het veld **Van** de begindimensie in of klik op ![Bladeren](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Bladeren") om naar beschikbare dimensies te zoeken. Om een bereik van dimensies in te voeren, voert u in het veld **Tot** de einddimensie in.
6.  Klik op **OK** om het dialoogvenster voor de dimensie te sluiten. Het dialoogvenster **Dimensies** geeft de bijgewerkte dimensie of het bijgewerkte bereik weer.
7.  Klik op **OK** om het dialoogvenster **Dimensies** te sluiten.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Rekeningen met nulsaldo weergeven in een rijdefinitie
Standaard drukt de rapportontwerper geen rij af die geen corresponderend saldo in de financiële gegevens bevat. Daarom kunt u één rijdefinitie maken die alle natuurlijk segmentwaarden of alle dimensies bevat en deze rijdefinitie gebruiken voor elk van uw afdelingen.

### <a name="modify-zero-balance-settings"></a>Instellingen van nulsaldo wijzigen

1.  Open in Report Designer de rapportdefinitie die u wilt wijzigen.
2.  Selecteer op het tabblad **Instellingen**, onder **Andere opmaak** opties voor de rijdefinitie die in de rapportdefinitie wordt gebruikt.
3.  Klik op **Opslaan** in het menu **Bestand** om uw wijzigingen op te slaan.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Jokertekens en -bereiken gebruiken in een rijdefinitie
Wanneer u een natuurlijke segmentwaarde invoert in het dialoogvenster **Dimensies**, kunt u een jokerteken (? of \*) gebruiken op elke positie van een segment. Report Designer pakt alle waarden voor de opgegeven posities uit zonder rekening te houden met de jokertekens. De rijdefinitie bevat bijvoorbeeld alleen natuurlijke segmentwaarden. Natuurlijke segmenten hebben vier tekens. Door **6???** in te voeren in een rij, geeft u Report Designer opdracxht om alle rekeningen op te nemen met een natuurlijke segmentwaarde die met een 6 begint. Als u **6\*** invoert, worden dezelfde resultaten geretourneerd, maar de resultaten bevatten ook waarden met variabele breedte zoals **60** en **600000**. De rapportontwerper vervangt elk jokerteken (?) met het volledig bereik van mogelijke waarden, zoals letters en speciale tekens. Bijvoorbeeld, in het bereik van **12?0** tot en met **12?4** wordt het jokerteken in **12?0** vervangen door de laagste waarde in het tekenreeks en wordt het jokerteken in **12?4** vervangen door de hoogste waarde in de tekenreeks. 
> [!NOTE]
> Gebruik jokertekens niet voor de eerste en laatste rekeningen in bereiken. Als u in jokertekens gebruikt in de eerste rekening of de laatste rekening, krijgt u mogelijk onverwachte resultaten.

### <a name="single-segment-or-single-dimension-ranges"></a>Bereiken met één segment of één dimensie

U kunt een bereik opgeven van segmentwaarden of dimensiewaarden. Het voordeel van het opgeven van een bereik is dat u de rijdefinitie niet hoeft bij te werken telkens wanneer een nieuwe segmentwaarde of dimensiewaarde aan de financiële gegevens wordt toegevoegd. Bijvoorbeeld, het bereik **+Account=\[6100:6900\]** trekt de waarden van rekeningen 6100 tot en met 6900 in het rijbedrag. Wanneer een bereik een jokerteken (?) bevat, evalueert de rapportontwerper het bereik niet teken per teken. In plaats daarvan worden de lage en hoge uiteinden van het bereik bepaald en worden vervolgens de eindwaarden en alle waarden daartussen opgenomen. 
> [!NOTE]
> Report Designer kan geen rekeningen, dimensies of velden uit het Microsoft Dynamics ERP-systeem selecteren die een van de volgende gereserveerde tekens bevatten: &, \*, \[, \], { of }. U kunt een en-teken (&) alleen toevoegen wanneer u automatisch rijdefinities samenstelt via het dialoogvenster **Rijen invoegen van dimensies**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Bereiken met meerdere segmenten of meerdere dimensies

Wanneer u een bereik invoert door combinaties van meerdere dimensiewaarden te gebruiken, wordt de bereikvergelijking ..\financial-dimensions\dimensie voor dimensie uitgevoerd. De bereikvergelijking kan niet teken per teken of op basis van een gedeeltelijke segment worden uitgevoerd. Het bereik **+Account=\[5000:6000\], Department=\[1000:2000\], Cost center=\[00\]** bevat bijvoorbeeld alleen de rekeningen die overeenkomen met elk segment. In dit scenario moet de eerste dimensie in het bereik van 5000 tot en met 6000 zijn, de tweede dimensie in het bereik van 1000 tot en met 2000 en moet de laatste dimensie 00 zijn. Zo wordt bijvoorbeeld **+Account=\[5100\], Department=\[1100\], Cost center=\[01\]** niet in het rapport opgenomen, omdat het laatste segment buiten het opgegeven bereik ligt. Als een segmentwaarde spaties bevat, plaatst u die waarde tussen vierkante haakjes (\[ \]). De volgende waarden zijn geldig voor een segment met vier tekens: **\[ 234\], \[123 \], \[1 34\]**. Dimensiewaarden moeten tussen vierkante haakjes (\[ \]) worden geplaatst. Report Designer voegt deze haakjes voor u toe. Wanneer een bereik met meerdere segmenten of meerdere dimensies jokertekens (? of \*) bevat, worden de hoge en lage uiteinden van het hele bereik met meerdere segmenten of meerdere dimensies bepaald en worden de eindwaarden en alle waarden daartussen opgenomen. Als u een groot bereik hebt, zoals de hele reeks rekeningen van 40000 tot en met 99999, moet u waar mogelijk een geldige eerste rekening en laatste rekening opgeven. 
> [!NOTE]
> Report Designer kan geen rekeningen, dimensies of velden uit het Microsoft Dynamics ERP-systeem selecteren die een van de volgende gereserveerde tekens bevatten: &, \*, \[, \], { of }. U kunt een en-teken (&) alleen toevoegen wanneer u automatisch rijdefinities samenstelt via het dialoogvenster **Rijen invoegen van dimensies**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Optellen bij en aftrekken van andere rekeningen in een rijdefinitie
Om de monetaire bedragen in één rekening op te tellen bij of af te trekken van de monetaire bedragen in een andere rekening, kunt u het plusteken (+) en het minteken (-) in de cel **Koppeling naar financiële dimensies** gebruiken. De volgende tabel geeft acceptabele notaties weer voor het optellen bij en aftrekken van koppelingen naar financiële gegevens.

| Bewerking  | Deze opmaak gebruiken  |
|------------|-----------------|
| Voeg twee volledig gekwalificeerd rekeningen toe.                                                       | +Division=\[000\], Account=\[1205\], Department=\[00\]+Division=\[100\], Account=\[1205\], Department=\[00\] |
| Voeg twee segmentwaarden toe.                                                                 | +Account=\[1205\]+Account=\[1210\]                                                                           |
| Voeg segmentwaarden toe die jokertekens bevatten.                                    | +Account=\[120?+Account=\[11??\]                                                                             |
| Voeg een bereik van volledig gekwalificeerd rekeningen toe.                                                | +Division=\[000:100\], Account=\[1205\], Department=\[00\]                                                   |
| Voeg een bereik van segmentwaarden toe.                                                          | +Account=\[1200:1205\]                                                                                       |
| Voeg een bereik van segmentwaarden toe die jokertekens bevatten.                         | +Account=\[120?:130?\]                                                                                       |
| Trek één volledig gekwalificeerde rekening af van een andere volledig gekwalificeerde rekening.              | +Division=\[000\], Account=\[1205\], Department=\[00\]-Division=\[100\], Account=\[1205\], Department=\[00\] |
| Trek één segmentwaarde van een andere segmentwaarde af.                                  | +Account=\[1205\]-Account=\[1210\]                                                                           |
| Trek een segmentwaarde af die een jokerteken van een andere segmentwaarde bevat. | +Account=\[1200\]-Account=\[11??\]                                                                           |
| Trek een bereik van volledig gekwalificeerd rekeningen af.                                           | -Division=\[000:100\], Account=\[1200:1205\], Department=\[00:01\]                                           |
| Trek een bereik van segmentwaarden af.                                                     | -Account=\[1200:1205\]                                                                                       |
| Trek een bereik van segmentwaarden af die jokertekens bevatten.                    | -Account=\[120?:130?\]                                                                                       |

Hoewel u de rekeningen rechtstreeks kunt wijzigen, kunt u ook het dialoogvenster **Dimensies** gebruiken om de juiste opmaak toe te passen op uw koppelingen naar financiële gegevens. Alle waarden mogen jokertekens bevatten (? of \*). Report Designer kan echter geen rekeningen, dimensies of velden uit het Microsoft Dynamics ERP-systeem selecteren die een van de volgende voorbehouden tekens bevatten: &, \*, \[, \], {, of }. 
> [!NOTE]
> Om waarden af te trekken, moet u deze waarden tussen haakjes plaatsen. Als u bijvoorbeeld **450?-(4509)** invoert, wordt dit weergegeven als **+Account=\[4509\]-Account=\[450?\]** en draagt u Report Designer op om het bedrag voor rekeningsegment 4509 af te trekken van het bedrag voor elk rekeningsegment dat begint met 450.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Rekeningen optellen bij of aftrekken van andere rekeningen

1.  Open in Report Designer de rijdefinitie die u wilt wijzigen.
2.  Dubbelklik in de juiste rij op de cel in de kolom **Koppeling naar financiële dimensies**.
3.  Volg in de eerste rij van het dialoogvenster **Dimensies** deze stappen:
    1.  Selecteer on het eerste veld alle dimensies (standaard) of klik om het dialoogvenster **Dimensiesets beheren** te openen, waarin u een set maakt, wijzigt, kopieert of verwijdert.
    2.  Dubbelklik op de cel **Operator +/-** en selecteer de operator plus (**+**) of min (**-**) die van toepassing is op een of meer dimensiewaarden of -sets in de rij.
    3.  Dubbelklik on de kolom van de desbetreffende dimensie op de cel om het dialoogvenster **Dimensies** te openen en selecteer of deze dimensiewaarde voor een persoon of een bereik, een set van dimensiewaarden of het totaalbedrag van rekeningen is. Voor omschrijvingen van de velden in het dialoogvenster **Dimensies** raadpleegt u de sectie 'Dialoogvenster Omschrijving van de dimensies'.
    4.  Voer in de kolommen **Van** en **Tot** segmentwaarden in.

4.  Herhaal stap 2 - 3 als u nog meer bewerkingen wilt toevoegen.

> [!NOTE]
> De operator is van toepassing op alle dimensies in de rij.

## <a name="description-of-the-dimensions-dialog-box"></a>Dialoogvenster Omschrijving van de dimensies
In de volgende tabel worden de velden beschreven in het dialoogvenster **Dimensies**.

| Artikel                | Beschrijving                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Persoon of bereik | Voer in het veld **Van** de naam van een rekening in of klik op de knop **Bladeren** ![Bladeren](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Bladeren") om naar de rekening te bladeren. Om bereik te selecteren, kunt u in het veld **Tot** een waarde typen of zoeken.                                             |
| Set van dimensiewaarden | Geef in het veld **Naam** de naam van een set van dimensiewaarden op. Om een set te maken, wijzigen, kopiëren of verwijderen, klikt u op **Sets van dimensiewaarden beheren**. Het veld **Formule** wordt ingevuld met de formule van de cel **Koppeling naar financiële dimensies** voor deze set van dimensiewaarden die in de rijdefinitie is ingesteld. |
| Totaalrekeningen   | Typ of zoek in het veld **Naam** een dimensie van totaalrekeningen. Het veld **Formule** wordt ingevuld met de formule in de cel **Koppeling naar financiële dimensies** voor deze totaalrekening in de rijdefinitie.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Sets van dimensiewaarden toevoegen aan een rijdefinitie
Een set van de dimensiewaarden is een benoemde groep van dimensiewaarden. Een set van dimensiewaarden kan waarden in slechts één dimensie bevatten, maar u kunt een set van dimensiewaarden gebruiken in meerdere rijdefinities, kolomdefinities, rapportagestructuurdefinities en rapportdefinities. U kunt de verschillende sets van dimensiewaarden ook combineren in een rapportdefinitie. Wanneer een wijziging aan uw financiële gegevens vereist dat u de set van dimensiewaarden wijzigt, kunt u de definitie van de set van dimensiewaarden bijwerken. Die update is van toepassing op alle gebieden die de set van dimensiewaarden gebruiken. Als u bijvoorbeeld vaak een waardebereik opgeeft om te koppelen naar uw financiële gegevens, zoals de waarden van 5100 tot en met 5600, kunt u dit bereik toewijzen aan een rekeningenset met de naam Verkoop. Nadat u een reeks dimensiewaarden hebt gemaakt, kunt u deze selecteren als uw koppeling voor financiële gegevens. Als het waardebereik van 5100 tot en met 5600 bijvoorbeeld aan Verkoop is toegewezen, en 4175 is toegewezen aan Kortingen, kunt u uw totale verkoop bepalen door Kortingen af te trekken van Verkoop. Deze bewerking is aangegeven als **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Een set van dimensiewaarden maken

1.  Open in Report Designer de rij, kolom of structuur die u wilt wijzigen.
2.  Klik in het menu **Bewerken** op **Sets van dimensiewaarden beheren**.
3.  Selecteer in het dialoogvenster **Sets van dimensiewaarden beheren**, in het veld **Dimensie** het type van set van dimensiewaarden dat uw wilt maken en klik vervolgens op **Nieuw**.
4.  Voer in het dialoogvenster **Nieuw** een naam en een beschrijving in voor de set.
5.  Dubbelklik in de kolom **Van** in een cel.
6.  Selecteer in het dialoogvenster **Rekening** de naam van de rekening in de lijst, of zoek naar de invoer in het veld **Zoeken**. Klik vervolgens op **OK**.
7.  Herhaal stappen 5 tot en met 6 in de kolom **Tot** om een formule voor deze operator te ontwerpen.
8.  Als de formule is voltooid, klikt u op **OK**.
9.  Klik in het dialoogvenster **Sets van dimensiewaarden beheren** op **Afsluiten**.

### <a name="update-a-set-of-dimension-values"></a>Een set van dimensiewaarden bijwerken

1.  Open in Report Designer de rij, kolom of structuur die u wilt wijzigen.
2.  Klik in het menu **Bewerken** op **Sets van dimensiewaarden beheren**.
3.  Selecteer het dimensietype in het dialoogvenster **Sets van dimensiewaarden beheren** in het veld **Dimensie**.
4.  Selecteer in de lijst de set van dimensiewaarden die u wilt bijwerken en klik vervolgens op **Wijzigen**.
5.  Open het dialoogvenster **Wijzigen** en wijzig de formulewaarden die in de set moeten worden opgenomen. 
    > [!NOTE]
    >  Als u nieuwe rekeningen of dimensies toevoegt, moet u de bestaande sets van dimensiewaarden wijzigen om de wijzigingen op te nemen.
6.  Dubbelklik op de cel en selecteer de juiste operator, **Van**-rekening en **Naar**-rekening.
7.  Klik op **OK** om het dialoogvenster **Wijzigen** te sluiten en wijzigingen op te slaan.

### <a name="copy-a-dimension-set"></a>Een dimensieset kopiëren

1.  Open in Report Designer de rij, kolom of structuur die u wilt wijzigen.
2.  Klik in het menu **Bewerken** op **Sets van dimensiewaarden beheren**.
3.  Selecteer het dimensietype in het dialoogvenster **Sets van dimensiewaarden beheren** in het veld **Dimensie**.
4.  Selecteer de te kopiëren set in de lijst en klik vervolgens op **Opslaan als**.
5.  Voer een nieuwe naam in voor de gekopieerde set en klik vervolgens op **OK**.

### <a name="delete-a-dimension-set"></a>Een dimensieset verwijderen

1.  Open in Report Designer de rij, kolom of structuur die u wilt wijzigen.
2.  Klik in het menu **Bewerken** op **Sets van dimensiewaarden beheren**.
3.  Selecteer het dimensietype in het dialoogvenster **Sets van dimensiewaarden beheren** in het veld **Dimensie**.
4.  Selecteer de set om te verwijderen en klik vervolgens op **Verwijderen**. Klik op **Ja** om de set van dimensiewaarden definitief te verwijderen.


<a name="see-also"></a>Zie ook
--------

[Financiële rapportage](financial-reporting-intro.md)




