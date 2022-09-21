---
title: Hoofdplanning voor producten met een beperkte houdbaarheid
description: In dit artikel wordt beschreven hoe u planningsfuncties kunt instellen en gebruiken die rekening houden met de houdbaarheid van bederfelijke producten.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 68a1ba2bfe90aaf0462917c405d483fa12bf8126
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428216"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Hoofdplanning voor producten met een beperkte houdbaarheid

[!include [banner](../../includes/banner.md)]

Houdbaarheid is de tijd dat een product kan worden opgeslagen totdat het niet meer kan worden gebruikt of verkocht. Voor producten met een beperkte houdbaarheid zult u waarschijnlijk een FEFO-magazijnstrategie (First-Expire, First-Out) gebruiken, waarbij het verbruik en de verkoop van artikelen wordt bepaald op basis van de resterende houdbaarheid. Deze magazijnstrategie is relevant voor voedsel, medicijnen en andere goederen die worden gekenmerkt door een korte opslagtijd. Volgens FEFO worden artikelen in het magazijn opgeslagen als goederen op een plank van een supermarkt: producten met een lange houdbaarheid worden dieper op de planken geplaatst, zodat producten met een korte resterende houdbaarheid het eerst worden verbruikt.

## <a name="using-shelf-life-in-master-planning"></a>Houdbaarheid gebruiken in hoofdplanning

In deze sectie wordt uitgelegd hoe de hoofdplanning het aanbod voor houdbaarheidsartikelen voorstelt.

Wanneer u een hoofdplan uitvoert, worden voorgestelde geplande orders (aanbod) gegenereerd die aan de vraag voldoen en de vertragingen minimaliseren. Als het plan artikelen bevat met een beperkte houdbaarheid, worden planningsberekeningen ingewikkelder omdat het plan niet alleen vertragingen moet minimaliseren, maar ook bestaande voorraad moet gebruiken voordat deze vervalt. Het plan moet proberen om aanbod te gebruiken dat het dichtst bij de vervaldatum ligt vóór aanbod dat later vervalt. De hoofdplanning probeert dus de volgende doelstellingen te behalen, in deze volgorde:

1. Het aantal vertragingen minimaliseren.
1. Het totaal van het FEFO-aanbod maximaliseren.
1. De aanvulling van de voorraad minimaliseren.

In sommige gevallen kan er een conflict zijn tussen de eerste twee doelen en moet u een keuze maken: wilt u een zending uitstellen of wilt u het aanbod gebruiken dat later vervalt in plaats van het aanbod dat sneller vervalt? Om dit conflict op te lossen tijdens de hoofdplanning geeft het systeem prioriteit aan het minimaliseren van de vertragingen met een aanbod dat binnenkort vervalt. In het algemeen treedt dit type conflict op wanneer er vertragingen en dekking per periode kunnen zijn. Daarom is het raadzaam een dekkingsperiode te gebruiken die korter is dan de houdbaarheid van een artikel. Andere typen dekking (zoals een vereiste) hebben waarschijnlijk niet met dit type conflict te maken.

## <a name="set-up-shelf-life"></a>Houdbaarheid instellen

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Elk hoofdplan configureren om rekening te houden met de houdbaarheid

Bij hoofdplannen wordt standaard geen rekening gehouden met de houdbaarheid. Gebruik de volgende procedure om houdbaarheidsberekeningen in te stellen voor hoofdplannen die dit nodig hebben.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een bestaand plan in de het lijstvenster of maak een nieuw plan.
1. Stel op het sneltabblad **Algemeen** de optie **Te gebruiken tot-datums gebruiken** in op *Ja*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Traceringsdimensiegroepen configureren om de batchdimensie bij te houden

De houdbaarheid van een artikel kan alleen worden bijgehouden als dat artikel wordt bijgehouden in de batchdimensie. Dit wil zeggen dat de batchverwijzing en de vereiste datums moeten worden vastgelegd bij ontvangst of productie, en bij elke voorraadtransactie van het artikel. Als u deze optie wilt beheren, stelt u een of meer traceringsdimensiegroepen in voor de vereiste tracering en wijst u de relevante artikelen vervolgens zo nodig aan deze groepen toe.

Met de volgende procedure kunt u een traceringsdimensiegroep instellen om de batchdimensie te traceren.

1. Ga naar **Productgegevensbeheer \> Instellen \> Dimensie- en variantgroepen \> Traceringsdimensiegroepen**.
1. Volg één van deze stappen:

    - Selecteer in het actievenster **Nieuw** om een nieuwe traceringsdimensiegroep te maken. Voer een naam en beschrijving in en selecteer in het actievenster de optie **Opslaan**.
    - Selecteer in het lijstvenster de bestaande traceringsdimensiegroep die u wilt instellen om de batchdimensie te traceren.

1. Schakel in de rij **Batchnummer** op het sneltabblad **Traceringsdimensie** de selectievakjes in de kolommen **Actief** en **Fysieke voorraad** in.

### <a name="set-up-shelf-life-for-a-product"></a>Houdbaarheid voor een product instellen

Met de volgende procedure kunt u de houdbaarheid van een product instellen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Maak het product dat u wilt instellen, of open het.
1. Als u de houdbaarheidsinstellingen wilt gebruiken, stelt u het veld **Traceringsdimensiegroep** op het sneltabblad **Algemeen** in op een traceringsdimensiegroep die is ingesteld om de batchdimensie bij te houden. U kunt dit veld alleen instellen wanneer u voor het eerst een product maakt. U kunt de waarde niet wijzigen voor bestaande producten.
1. Stel op het sneltabblad **Voorraadbeheer** de volgende velden in:

    - **Advies houdbaarheidsperiode (dagen)**: geef de periode (in dagen) op waarna u een batch van dit product wilt controleren om te garanderen dat het geschikt is voor consumptie of verkoop. De waarde van dit veld wordt toegevoegd aan de *fabricagedatum* van een batch om de *adviesdatum voor houdbaarheid* te bepalen. U kunt het systeem configureren om kwaliteitsorders te genereren wanneer de adviesdatum voor houdbaarheid van een batch nadert.
    - **Te gebruiken tot in dagen:** geef het aantal dagen op totdat een batch van dit product vervalt Deze waarde wordt toegevoegd aan de *fabricagedatum* om de *vervaldatum* te bepalen. De batch wordt na deze datum als onbruikbaar beschouwd.
    - **Ten minste houdbaar tot in dagen**: geef de periode (in dagen) op waarna een batch van dit product nog kan worden verkocht, maar sommige oorspronkelijke eigenschappen niet kan behouden. Deze waarde wordt toegevoegd aan de *fabricagedatum* om de *houdbaarheidsdatum* te bepalen. U kunt rapporten uitvoeren om de voorraad aan te geven waarvan de houdbaarheidsdatum is gepasseerd. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Een regel voor verkoopbare dagen voor elke klant instellen

Met de functionaliteit *Verkoopbare dagen* zorgt u dat producten uit een batch die binnenkort vervalt, niet naar klanten verzonden. Bovendien zorgt u hiermee dat wanneer producten naar een klant worden verzonden, er een adequate hoeveelheid verkoopbare dagen blijft na levering.

Als u de functionaliteit voor verkoopbare dagen wilt gebruiken, moet u het aantal verkoopbare dagen definiëren dat van toepassing is op elk product (of groep producten) voor elke klant. U moet dit proces handmatig voltooien omdat er geen gegevensentiteit voor is.

Met de volgende procedure kunt u verkoopbare dagen instellen voor elk product voor elke klant.

1. Ga naar **Verkoop en marketing \> Klanten \> Alle klanten**.
1. Zoek en selecteer de klant waarvoor u dit wilt instellen.
1. Selecteer in het Actievenster op het tabblad **Verkopen** in de groep **Instellen** de optie **Verkopen \> Verkoopbare dagen**.
1. Op de pagina **Verkoopbare dagen voor klant** worden in het raster bestaande regels voor verkoopbare dagen weergegeven voor elk product of elke groep producten. Gebruik de knoppen in het actievenster om indien nodig rijen aan het raster toe te voegen of te bewerken. Gebruik een **Filter** om bestaande rijen te zoeken.
1. Stel voor elke rij de volgende velden in:

    - **Artikelcode**: selecteer een van de volgende waarden om het bereik van artikelen op te geven dat wordt beïnvloed:

        - *Tabel*: de rij is van toepassing op een specifiek artikel.
        - *Groep*: de rij is van toepassing op een specifieke artikelgroep.
        - *Alle*: de rij is van toepassing op alle artikelen.

    - **Artikelrelatie**: selecteer een specifiek artikel als u het veld **Artikelcode** hebt ingesteld op *Tabel*. Als u het veld **Artikelcode** hebt ingesteld op *Groep*, selecteert u een groep voor artikelen. Als u het veld **Artikelcode** instelt op *Alle*, is dit veld niet beschikbaar.
    - **Verkoopbare dagen**: voer het minimumaantal dagen in waarop de klant overeenkomstige producten kan verkopen voordat de batch verloopt. De waarde voor verkoopbare dagen wordt gebaseerd op de aangevraagde ontvangstdatum (of de bevestigde ontvangstdatum, als deze is gedefinieerd) voor de overeenkomende producten op de verkooporder.
    - *(Overige productdimensies)*: als u het bereik van een rij verder wilt beperken, geeft u zo nodig andere dimensiewaarden op (zoals **Grootte** en **Kleur**). Selecteer **Dimensies weergeven** in het actievenster om te bepalen welke dimensies worden weergegeven in het raster.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Alle relevante producten zo instellen dat de FEFO-datum wordt gecontroleerd

Verkoopbare dagen werkt alleen als elk relevant artikel tot een artikelmodelgroep behoort, waarvoor het selectievakje **Gecontroleerde FEFO-datum** is ingeschakeld.

Met de volgende procedure kunt u een artikelmodelgroep instellen zodat de functionaliteit voor verkoopbare dagen wordt ondersteund.

1. Ga naar **Voorraadbeheer \> Instellen \> Voorraad \> Artikelmodelgroepen**.
1. Selecteer een bestaande groep in het lijstvenster of maak een nieuwe groep door **Nieuw** te selecteren in het actievenster.
1. Schakel op het sneltabblad **Voorraadbeleid** het selectievakje **Gecontroleerde FEFO-datum** in.
1. Stel andere velden voor de groep naar wens in.

Met de volgende procedure kunt u de artikelmodelgroep weergeven of instellen waartoe een product hoort.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het product dat u wilt inspecteren of bewerken.
1. Stel op het sneltabblad **Algemeen** het veld **Artikelmodelgroep** in op een groep waarvoor het selectievakje **Gecontroleerde FEFO-datum** is ingeschakeld.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Voorbeeld 1: Eenvoudige FEFO, periode van tien dagen, nul dagen levertijd

Dit is een eenvoudig voorbeeld van de houdbaarheid, waarbij tracering van de behoefte tussen de aanbodorders en de vraag wordt uitgevoerd om aan de volgende systeemdoelen te voldoen:

- Het aantal vertragingen minimaliseren.
- Het totaal van het FEFO-aanbod maximaliseren.
- De aanvulling van de voorraad minimaliseren.

Het systeem heeft de volgende instellingen voor het artikel en het hoofdplan:

- **Dekkingscode (aanvullingsstrategie):** Periode 
- **Dekkingsperiode:** 10 dagen (gelijk aan de houdbaarheid)
- **Houdbaarheid:** 10 dagen
- **Verkoopbare dagen:** 0 dagen
- **Levertijd:** 0 dagen
- **Negatieve dagen:** 0 dagen
- **Type geplande order (standaardorderinstellingen van het artikel):** Inkooporder

De volgende verkooporders voor het artikel bestaan in het systeem:

- **SO1:** Hoeveelheid (hoev) = 2, gevraagde leveringsdatum = vandaag + 1 dag
- **SO2:** hoev = 1, gevraagde leveringsdatum = vandaag + 4 dagen
- **SO3:** hoev = 1, gevraagde leveringsdatum = vandaag + 5 dagen

Al deze verkooporders zorgen voor vraag naar het artikel.

Het artikel heeft de volgende voorraad:

- **Beschikbare voorraad:** hoev = 1, vervaldatum = vandaag + 5 dagen
- **Inkooporder 1 (PO1):** Ontvangstdatum = vandaag + 2 dagen, hoev = 1, vervaldatum = vandaag + 4 dagen

Er wordt een lijst met aanbod gemaakt dat deze vraag kan dekken en de lijst wordt gesorteerd op vervaldatum (met FEFO).

Via de hoofdplanning wordt de vereiste behoefte getraceerd tussen vraag en aanbod. Er wordt ook een eventuele vereiste vraag gemaakt op basis van de aanbodlijst (met FEFO) en er wordt rekening gehouden met de beschikbaarheidsdatum.

- SO1 kan worden vervuld met de beschikbare voorraad, maar kan niet worden vervuld door PO1, omdat de beschikbaarheidsdatum voor PO1 één dag later is dan voor SO1 is vereist. Daarom wordt in SO1 vraag naar één eenheid goederen gegenereerd.
- SO2 kan gedekt worden door PO1, omdat PO1 binnen de gevraagde tijd komt en de vervaldatum nog steeds geldig is. Daarom wordt de SO2-vereiste volledig gedekt door PO1.
- SO3 wordt niet gedekt, omdat resources niet beschikbaar zijn. Daarom wordt in SO3 vraag naar één eenheid goederen gegenereerd.

Voor alle resterende behoeften moet het systeem de volgende geplande inkooporder maken:

- **PPO1:** ontvangstdatum = vandaag, hoev = 2, vervaldatum = vandaag + 10 dagen

De volgende tabel biedt een overzicht van het resultaat.

| Vraag | Tracering van behoefte |
|---|---|
| **SO1:** leveringsdatum = vandaag + 1 dag, hoev = 2 | <p>**Beschikbaar:** hoev = 1, vervaldatum = vandaag + 5 dagen</p><p>**PPO1:** ontvangstdatum = vandaag, hoev = 1, vervaldatum = vandaag + 10 dagen</p> |
| **SO2:** leveringsdatum = vandaag + 4 dagen, hoev = 1 | **PO1:** ontvangstdatum = vandaag + 2 dagen, hoev = 1, vervaldatum = vandaag + 4 dagen |
| **SO3:** leveringsdatum = vandaag + 5 dagen, hoev = 1 | **PPO1:** ontvangstdatum = vandaag, hoev = 2, vervaldatum = vandaag + 10 dagen |

In de volgende afbeelding wordt de tijdlijn voor dit voorbeeld weergegeven.

![Voorbeeld 1: Eenvoudige FEFO, periode van tien dagen, nul dagen levertijd.](media/fefo-example-1.png "Voorbeeld 1: Eenvoudige FEFO, periode van tien dagen, nul dagen levertijd")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Voorbeeld 2: Eenvoudige FEFO, vereiste, drie dagen levertijd

Dit voorbeeld laat zien hoe de poging van het systeem om vertragingen tot een minimum te beperken, soms tot te grote orders kan leiden.

Het systeem heeft de volgende instellingen voor het artikel en het hoofdplan:

- **Dekkingscode (aanvullingsstrategie):** vereiste
- **Houdbaarheid:** 10 dagen
- **Verkoopbare dagen:** 0 dagen
- **Levertijd:** tot stand gebracht door de volgende handelsovereenkomsten voor leveranciers:

    - **Handelsovereenkomst 1:** als hoev = 1, levertijd = 4
    - **Handelsovereenkomst 2:** als hoev = 2, levertijd = 3

- **Negatieve dagen:** 0 dagen
- **Type geplande order (standaardorderinstellingen van het artikel):** Inkooporder

De volgende verkooporder bestaat in het systeem:

- **SO1:** hoev = 2, gevraagde leveringsdatum = vandaag + 3 dagen

Deze vraag wordt gedekt door het bestaande aanbod en een bevestigde inkooporder:

- **Beschikbare voorraad:** beschikbaar = vandaag, hoev = 1, vervaldatum = vandaag + 2 dagen
- **PO1:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 4 dagen

SO1 kan niet worden vervuld door de voorhanden voorraad, omdat de vervaldatum van de voorraad vóór de verzenddatum valt. PO1 kan de SO1-behoefte dekken met een hoeveelheid van slechts 1. Daarom wordt in SO1 vraag naar één eenheid goederen gegenereerd. Om deze behoefte te dekken, maakt het systeem een geplande inkooporder (PPO1).

Het systeem heeft twee handelsovereenkomsten (één voor hoev = 1, levertijd = 4 dagen, en één voor hoev = 2, levertijd = 3 dagen). Hierdoor probeert het systeem om de vertragingen te minimaliseren door een geplande inkooporder (PPO1) te maken die aan de tweede handelsovereenkomst voldoet. Het resultaat is een meerlevering (hoev = 2, vervaldatum = vandaag + 10 dagen).

De volgende tabel biedt een overzicht van het resultaat.

| Vraag | Tracering van behoefte |
|---|---|
| **SO1:** leveringsdatum = vandaag + 3 dagen, hoev = 2 | <p>**PO1:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 4 dagen</p><p>**PPO1:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 10 dagen</p> |

In de volgende afbeelding wordt de tijdlijn voor dit voorbeeld weergegeven.

![Voorbeeld 2: Eenvoudige FEFO, vereiste, drie dagen levertijd.](media/fefo-example-2.png "Voorbeeld 2: Eenvoudige FEFO, vereiste, drie dagen levertijd")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Voorbeeld 3: Eenvoudige FEFO, vereiste, drie dagen levertijd, vijf verkoopbare dagen

In dit voorbeeld ziet u hoe de houdbaarheid werkt wanneer verkoopbare dagen worden toegevoegd voor een artikel.

Het systeem heeft de volgende instellingen voor het artikel en het hoofdplan:

- **Dekkingscode (aanvullingsstrategie):** vereiste
- **Houdbaarheid:** 10 dagen
- **Verkoopbare dagen:** 5 dagen
- **Levertijd:** 5 dagen
- **Negatieve dagen:** 0 dagen
- **Type geplande order (standaardorderinstellingen van het artikel):** Inkooporder

De volgende verkooporders bestaan in het systeem:

- **SO1:** hoev = 2, gevraagde leveringsdatum = vandaag + 2 dagen
- **SO2:** hoev = 1, gevraagde leveringsdatum = vandaag + 3 dagen
- **SO3:** hoev = 1, gevraagde leveringsdatum = vandaag + 5 dagen

Deze vraag kan worden gedekt door het bestaande aanbod en een bevestigde inkooporder:

- **Beschikbare voorraad:** beschikbaar = vandaag, hoev = 1, vervaldatum = vandaag + 6 dagen
- **PO1:** ontvangstdatum = vandaag + 2 dagen, hoev = 3, vervaldatum = vandaag + 10 dagen

Er wordt een lijst met kandidaten voor de tracering van de behoefte gemaakt op basis van de FEFO-lijst (aanbod) en beschikbaarheidsdatums. Dat betekent dat SO1 niet kan worden vervuld door de voorhanden voorraad, omdat de voorraad vervalt vóór het einde van de verkoopbare dagen die de klant nodig heeft (aangevraagde ontvangstdatum + 5 dagen). PO1 kan de SO1-behoefte dekken met twee eenheden en de SO2-behoefte met één eenheid. Daarom heeft alleen SO3 de vraag naar één eenheid goederen nog niet ontdekt. Om deze behoefte te dekken maakt het systeem de volgende geplande inkooporder:

- **PPO1:** ontvangstdatum = vandaag + 5 dagen, hoev = 1, vervaldatum = vandaag + 10 dagen

De volgende tabel biedt een overzicht van het resultaat.

| Vraag | Tracering van behoefte |
|---|---|
| **SO1:** leveringsdatum = vandaag + 2 dagen, hoev = 2 | **PO1:** ontvangstdatum = vandaag + 2 dagen, hoev = 2, vervaldatum = vandaag + 10 dagen |
| **SO2:** leveringsdatum = vandaag + 3 dagen, hoev = 1 | **PO1:** ontvangstdatum = vandaag + 2 dagen, hoev = 1, vervaldatum = vandaag + 10 dagen |
| **SO3:** leveringsdatum = vandaag + 5 dagen, hoev = 1 | **PPO1:** ontvangstdatum = vandaag + 5 dagen, hoev = 1, vervaldatum = vandaag + 10 dagen |

In de volgende afbeelding wordt de tijdlijn voor dit voorbeeld weergegeven.

![Voorbeeld 3: Eenvoudige FEFO, vereiste, drie dagen levertijd, vijf verkoopbare dagen.](media/fefo-example-3.png "Voorbeeld 3: Eenvoudige FEFO, vereiste, drie dagen levertijd, vijf verkoopbare dagen")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Voorbeeld 4: Eenvoudige FEFO, periode, levertijd is afhankelijk van de hoeveelheid

Dit voorbeeld laat zien hoe de poging van het systeem om vertragingen tot een minimum te beperken, soms tot te grote orders kan leiden.

Het systeem heeft de volgende instellingen voor het artikel en het hoofdplan:

- **Dekkingscode (aanvullingsstrategie):** Periode
- **Dekkingsperiode:** 10 dagen (gelijk aan de houdbaarheid)
- **Houdbaarheid:** 10 dagen
- **Verkoopbare dagen:** 0 dagen
- **Levertijd:** tot stand gebracht door de volgende handelsovereenkomsten voor leveranciers:

    - **Handelsovereenkomst 1:** als hoev = 1, levertijd = 5
    - **Handelsovereenkomst 2:** als hoev = 2, levertijd = 0

- **Negatieve dagen:** 0 dagen
- **Type geplande order (standaardorderinstellingen van het artikel):** Inkooporder

De volgende verkooporders bestaan in het systeem:

- **SO1:** hoev = 1, gevraagde leveringsdatum = vandaag
- **SO2:** hoev = 1, gevraagde leveringsdatum = vandaag + 6 dagen

Deze vraag kan gedeeltelijk worden gedekt door het bestaande aanbod uit de volgende bevestigde inkooporders:

- **PO1:** ontvangstdatum = vandaag + 1 dagen, hoev = 1, vervaldatum = vandaag + 2 dagen
- **PO2:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 7 dagen

Het systeem heeft twee handelsovereenkomsten (één voor hoev = 1, levertijd = 5 dagen, en één voor hoev = 2, levertijd = 0 dagen). Hierdoor probeert het systeem om de vertraging te minimaliseren door de volgende geplande inkooporder te maken die aan de tweede handelsovereenkomst voldoet:

- **PPO1:** ontvangstdatum = vandaag, hoev = 2, vervaldatum = vandaag + 10 dagen

SO1 wordt gedekt door één eenheid van PPO1. SO2 wordt gedekt door PO2, omdat PO2 sneller verloopt dan PPO1.

De volgende tabel biedt een overzicht van het resultaat.

| Vraag | Tracering van behoefte |
|---|---|
| **SO1:** leveringsdatum = vandaag, hoev = 1 | **PPO1:** ontvangstdatum = vandaag, hoev = 1, vervaldatum = vandaag + 10 dagen |
| **SO2:** leveringsdatum = vandaag + 6 dagen, hoev = 1 | **PO2:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 7 dagen |

> [!NOTE]
> PO1 wordt niet gebruikt, omdat deze te laat komt voor SO1 en vervalt voordat SO2 wordt geleverd. PPO1 heeft een meerbestelling met één eenheid om de levertijd 0 (nul) mogelijk te maken, per handelsovereenkomst 2.

In de volgende afbeelding wordt de tijdlijn voor dit voorbeeld weergegeven.

![Voorbeeld 4: Eenvoudige FEFO, periode, levertijd is afhankelijk van de hoeveelheid.](media/fefo-example-4.png "Voorbeeld 4: Eenvoudige FEFO, periode, levertijd is afhankelijk van de hoeveelheid")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Voorbeeld 5: Eenvoudige FEFO, vereiste, 10 negatieve dagen

In dit voorbeeld ziet u hoe de houdbaarheid werkt wanneer een groot aantal negatieve dagen wordt toegevoegd voor een artikel. Negatieve dagen zijn het aantal dagen dat u bereid bent om te wachten voordat u een aanvulling van een artikel bestelt waarvoor een negatieve voorraad bestaat. Er wordt geen aanbod gemaakt tenzij het aantal negatieve dagen wordt overschreden.

Het systeem heeft de volgende instellingen voor het artikel en het hoofdplan:

- **Dekkingscode (aanvullingsstrategie):** vereiste
- **Levertijd:** 0 dagen
- **Negatieve dagen:** 10 dagen
- **Type geplande order (standaardorderinstellingen van het artikel):** Inkooporder

De volgende verkooporder bestaat in het systeem:

- **SO1:** hoev = 1, gevraagde leveringsdatum = vandaag

Deze vraag kan worden gedekt door het bestaande aanbod uit de volgende bevestigde inkooporder:

- **PO1:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 5 dagen

Omdat het systeem geconfigureerd is voor het toestaan van 10 negatieve dagen, dekt het de vraag van SO1 met PO1, zelfs als het resultaat een vertraging van drie dagen is omdat door SO1 negatieve voorraad wordt gemaakt totdat PO1 aankomt. Er wordt geen geplande inkooporder gemaakt, hoewel de levertijd 0 (nul) is en het maken van een geplande inkooporder vertragingen zou verminderen.

De volgende tabel biedt een overzicht van het resultaat.

| Vraag | Tracering van behoefte |
|---|---|
| **SO1:** leveringsdatum = vandaag, hoev = 1 | **PO1:** ontvangstdatum = vandaag + 3 dagen, hoev = 1, vervaldatum = vandaag + 5 dagen |

In de volgende afbeelding wordt de tijdlijn voor dit voorbeeld weergegeven.

![Voorbeeld 5: Eenvoudige FEFO, vereiste, 10 negatieve dagen.](media/fefo-example-5.png "Voorbeeld 5: Eenvoudige FEFO, vereiste, 10 negatieve dagen")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Voorbeeld 6: Eenvoudige FEFO, vereiste, vijf negatieve dagen

In dit voorbeeld ziet u hoe de houdbaarheid werkt wanneer het aantal negatieve dagen voor een artikel minder is dan de houdbaarheidsperiode.

Het systeem heeft de volgende instellingen voor het artikel en het hoofdplan:

- **Dekkingscode (aanvullingsstrategie):** vereiste
- **Verkoopbare dagen:** 0 dagen
- **Levertijd:** 0 dagen
- **Negatieve dagen:** 5 dagen
- **Type geplande order (standaardorderinstellingen van het artikel):** Inkooporder

De volgende verkooporder bestaat in het systeem:

- **SO1:** hoev = 2, gevraagde leveringsdatum = vandaag

Deze vraag kan worden gedekt door het bestaande aanbod uit de volgende bevestigde inkooporders:

- **PO1:** ontvangstdatum = vandaag, hoev = 1, vervaldatum = vandaag + 1 dag
- **PO2:** ontvangstdatum = vandaag + 2 dagen, hoev = 1, vervaldatum = vandaag + 3 dagen

Het systeem moet echter wel de beperking respecteren dat verzonden artikelen niet kunnen vervallen op het moment van verzending. Daarom kunnen PO2 en PO1 niet beide worden gebruikt voor SO1, omdat PO1 vervalt voordat PO2 aankomt. Om de behoefte voor SO1 te dekken maakt het systeem de volgende geplande inkooporder:

- **PPO1:** ontvangstdatum = vandaag, hoev = 1, vervaldatum = vandaag + 10 dagen

Het systeem kan profiteren van de vijf negatieve dagen en PO2 en PPO1 gebruiken voor het dekken van SO1. Door deze aanpak wordt de levering echter vertraagd totdat PO2 aankomt en PO1 vervalt in de tussentijd. Het systeem dekt SO1 dus met PPO1 en PO1.

De volgende tabel biedt een overzicht van het resultaat.

| Vraag | Tracering van behoefte |
|---|---|
| **SO1:** leveringsdatum = vandaag, hoev = 2 | <p>**PO1:** ontvangstdatum = vandaag, hoev = 1, vervaldatum = vandaag + 1 dag</p><p>**PPO1:** ontvangstdatum = vandaag, hoev = 1, vervaldatum = vandaag + 10 dagen</p> |

In de volgende afbeelding wordt de tijdlijn voor dit voorbeeld weergegeven.

![Voorbeeld 6: Eenvoudige FEFO, vereiste, vijf negatieve dagen.](media/fefo-example-6.png "Voorbeeld 6: Eenvoudige FEFO, vereiste, vijf negatieve dagen")
