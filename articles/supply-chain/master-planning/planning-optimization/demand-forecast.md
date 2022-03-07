---
title: Hoofdplanning met vraagprognoses
description: In dit onderwerp wordt uitgelegd hoe u vraagprognoses opneemt tijdens de hoofdplanning met Planningsoptimalisatie.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f322dd63cb2dee6a9048e6ed086dc075cc0e1b9
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474839"
---
# <a name="master-planning-with-demand-forecasts"></a>Hoofdplanning met vraagprognoses

[!include [banner](../../includes/banner.md)]

U kunt een vraagprognose gebruiken in combinatie met Planningsoptimalisatie voor de verwerking van verwachte vraag in de hoofdplanning. U kunt handmatig een vraagprognose maken, deze importeren of genereren met behulp van de functionaliteit voor vraagprognoses in Microsoft Dynamics 365 Supply Chain Management. Zie [Overzicht vraagprognose](../introduction-demand-forecasting.md) voor meer informatie over vraagprognoses.

> [!NOTE]
> Afzonderlijke prognoseplanning wordt niet ondersteund met Planningsoptimalisatie. De instelling **Huidig prognoseplan** op de pagina **Parameters hoofdplanning** heeft daarom geen effect wanneer u Planningsoptimalisatie gebruikt.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Een hoofdplan instellen om een vraagprognose op te nemen

Voer de volgende stappen uit om een hoofdplan zo te configureren dat het een vraagprognose bevat.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een bestaand plan of maak een nieuw plan.
1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Prognosemodel**: selecteer het prognosemodel dat moet worden toegepast. Dit model kan worden gebruikt wanneer een aanbodvoorstel wordt gegenereerd voor het huidige hoofdplan.
    - **Vraagprognose opnemen**: stel deze optie in op *Ja* om de vraagprognose in het huidige prognoseplan op te nemen. Bij *Nee* worden vraagprognosetransacties niet opgenomen in het hoofdplan.
    - **Gebruikte methode om prognosebehoeften te verminderen**: selecteer de methode die moet worden gebruikt om prognosebehoeften te verminderen. Zie de sectie [Reductiesleutels van prognose](#reduction-keys) verderop in dit onderwerp voor meer informatie.

1. Op het sneltabblad **Time fence in dagen** kunt u de volgende velden instellen om de periode op te geven waarin de vraagprognose moet worden opgenomen:

    - **Prognoseplan**: stel deze optie in op *Ja* als u de time fence voor prognoseplannen wilt overschrijven die afkomstig is uit de afzonderlijke behoefteplanningsgroepen. Stel deze optie in op *Nee* als u de waarden uit de afzonderlijke behoefteplanningsgroepen voor het huidige hoofdplan wilt gebruiken.
    - **Prognoseperiode**: als u de optie **Prognoseplan** instelt op *Ja*, geeft u het aantal dagen op (vanaf de datum van vandaag) waarop de vraagprognose moet worden toegepast.

    > [!IMPORTANT]
    > De instelling **Prognoseplan** wordt nog niet ondersteund met Planningsoptimalisatie.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Een behoefteplanningsgroep instellen om een vraagprognose op te nemen

Voer de volgende stappen uit om een behoefteplanningsgroep zo te configureren dat deze een vraagprognose bevat.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Behoefteplanningsgroepen**.
1. Selecteer een bestaande behoefteplanningsgroep of maak een nieuwe.
1. Stel op het sneltabblad **Overig** de volgende velden in:

    - **Time fence voor prognoseplan**: voer het aantal dagen in (vanaf de datum van vandaag) waarvoor de vraagprognose moet worden toegepast. Deze waarde kan worden overschreven door de optie **Prognoseplan** in het hoofdplan te gebruiken, zoals wordt beschreven in de vorige sectie.
    - **Reductiesleutel**: selecteer de reductiesleutel die u wilt toepassen. Zie [Een prognosereductiesleutel maken en instellen](#create-reduction-key) en [Een reductiesleutel gebruiken](#use-reduction-key) verderop in dit onderwerp voor meer informatie.
    - **Prognose reduceren met**: voor hoofdplannen waarvoor het veld **Gebruikte methode om prognosebehoeften te verminderen** is ingesteld op *Transacties - reductiesleutel* of *Transacties - dynamische periode*, geeft u welke transacties de prognose moeten verminderen. Selecteer een van de volgende waarden:

        - **Alle transacties**: alle transacties moeten de prognose verminderen.
        - **Orders**: alleen verkooporders moeten de prognose verminderen.

        > [!NOTE]
        > Als u *Alle transacties* selecteert, worden transacties met zowel vraag als aanbod in dezelfde voorraaddimensies beschouwd als neutraal en genegeerd tijdens de prognosereductie. Als de planningsdimensie bijvoorbeeld is ingesteld op alleen site, niet magazijn, wordt een overboekingsorder tussen site 1, magazijn 11 en site 1, magazijn 13 genegeerd en wordt de resterende vraagprognose niet verminderd.

    - **Intercompany-orders opnemen**: stel deze optie in op *Ja* als intercompany-orders moeten worden opgenomen wanneer de prognose wordt verminderd. In het andere geval kiest u voor *Nee*.
    - **Klantprognose opnemen in de vraagprognose**: geef op of een klantprognose moet worden opgenomen in de algemene prognose. Deze optie bepaalt hoe werkelijke vraag de geprognosticeerde vraag verlaagt. U kunt deze optie gebruiken om ervoor te zorgen dat de hoofdplanning de levering van artikelen vervoert die door bepaalde klanten zijn gekocht.

        - Stel deze optie in op *Ja* als u een klantprognose wilt opnemen in de algemene prognose. In dit geval vermindert de werkelijke klantvraag zowel de klantprognose als de algemene prognose. De hoofdplanning genereert geplande orders om alleen de algemene prognosehoeveelheid te dekken.
        - Stel deze optie in op *Nee* als u geen klantprognose wilt opnemen in de algemene prognose. In dit geval vermindert de werkelijke klantvraag alleen de klantprognose. De hoofdplanning genereert geplande orders voor zowel de prognosehoeveelheid als de prognose voor elke klanthoeveelheid.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Reductiesleutels van prognose

Dit gedeelte biedt informatie over de verschillende methoden die worden gebruikt om prognosebehoeften te reduceren. Het bevat voorbeelden van de resultaten van elke methode. Ook wordt uitgelegd hoe u een prognosereductiesleutel kunt maken, instellen en gebruiken. Bij sommige methoden wordt een prognosereductiesleutel gebruikt om prognosebehoeften te reduceren.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Methoden die worden gebruikt om prognosebehoeften te reduceren

Wanneer u een prognose in een hoofdplan opneemt, kunt u selecteren hoe de prognosebehoeften worden gereduceerd wanneer werkelijke vraag wordt opgenomen. In de hoofdplanning worden prognosebehoeften uit het verleden uitgesloten, dat wil zeggen alle prognosebehoeften vóór de huidige datum.

Als u een prognose wilt opnemen in een hoofdplan en de methode wilt selecteren die wordt gebruikt om prognosebehoeften te reduceren, gaat u naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**. Selecteer in het veld **Prognosemodel** een prognosemodel. Selecteer een methode in het veld **Gebruikte methode voor het reduceren van prognosebehoeften**. De volgende opties zijn beschikbaar:

- None
- Percentage - reductiesleutel
- Transacties – reductiesleutel (nog niet ondersteund met Planningsoptimalisatie)
- Transacties - dynamische periode

De volgende secties bevatten meer informatie over elke optie.

#### <a name="none"></a>Geen

Als u **Geen** selecteert, worden de prognosebehoeften niet gereduceerd tijdens de hoofdplanning. In dit geval worden in de hoofdplanning geplande orders gemaakt voor het leveren van de geraamde vraag (prognosebehoeften). Deze geplande orders behouden de voorgestelde hoeveelheid, ongeacht andere soorten vraag. Als bijvoorbeeld verkooporders worden geplaatst, worden in de hoofdplanning extra geplande orders gemaakt voor het leveren van de verkooporders. De hoeveelheid van de prognosebehoeften wordt niet gereduceerd.

#### <a name="percent--reduction-key"></a>Percentage - reductiesleutel

Als u **Percentage - reductiesleutel** selecteert, worden de prognosebehoeften gereduceerd volgens de percentages en perioden die zijn gedefinieerd door de reductiesleutel. In dit geval worden in de hoofdplanning geplande orders gemaakt waarin de hoeveelheid wordt berekend als de geraamde hoeveelheid × reductiesleutel in elke periode. Als er andere soorten vraag zijn, worden in de hoofdplanning ook geplande orders gemaakt voor het leveren van die vraag.

##### <a name="example-percent--reduction-key"></a>Voorbeeld: percentage - reductiesleutel

In dit voorbeeld wordt weergegeven hoe een reductiesleutel vraagprognosebehoeften reduceert overeenkomstig de percentages en perioden die door de reductiesleutel worden gedefinieerd.

Voor dit voorbeeld neemt u de volgende vraagprognose in een hoofdplan op.

| Maand    | Vraagprognose |
|----------|-----------------|
| januari  | 1.000           |
| Februari | 1.000           |
| maart    | 1.000           |
| april    | 1.000           |

Op de pagina **Reductiesleutels** stelt u de volgende regels in.

| Wisselgeld | Eenheid  | Percentage |
|--------|-------|---------|
| 1      | Maand | 100     |
| 2      | Maand | 75      |
| 3      | Maand | 50      |
| 4      | Maand | 25      |

U wijst de reductiesleutel aan de behoefteplanningsgroep van het artikel toe. Selecteer vervolgens op de pagina **Hoofdplannen** in het veld **Methode gebruikt voor het reduceren van prognosebehoeften** **Percentage - reductiesleutel**.

In dit geval worden, als u de prognoseplanning op 1 januari uitvoert, de vraagprognosebehoeften verbruikt volgens de percentages die u instelt op de pagina **Reductiesleutels**. De volgende behoeftehoeveelheden worden naar het hoofdplan overgebracht.

| Maand                | Hoeveelheid geplande order | Berekening    |
|----------------------|------------------------|----------------|
| januari              | 0                      | = 0% × 1.000   |
| Februari             | 250                    | = 25% × 1.000  |
| maart                | 500                    | = 50% × 1.000  |
| april                | 750                    | = 75% × 1.000  |
| Mei tot en met december | 1.000                  | = 100% × 1.000 |

#### <a name="transactions--reduction-key"></a>Transacties - reductiesleutel

Als u het veld **Gebruikte methode om prognosebehoeften te verminderen** instelt op *Transacties - reductiesleutel*, worden de prognosevereisten verminderd met de gekwalificeerde vraagtransacties die plaatsvinden tijdens de perioden die worden gedefinieerd door de reductiesleutel.

De gekwalificeerde vraag wordt gedefinieerd door het veld **Prognose verlagen per** op de pagina **Behoefteplanningsgroepen**. Als u het veld **Prognose verminderen per** instelt op *Orders*, worden alleen verkoopordertransacties als gekwalificeerde vraag beschouwd. Als u het veld instelt op *Alle transacties*, worden alle niet-intercompany-transacties voor uitgifte voorraad als gekwalificeerde vraag beschouwd. Als Intercompany-verkooporders ook als gekwalificeerde vraag moeten worden beschouwd, stel dan de optie **Intercompany-orders opnemen** in op *Ja*.

Prognosereductie begint met de eerste (vroegste) vraagprognoserecord in de reductiesleutelperiode. Als de hoeveelheid gekwalificeerde voorraadtransacties hoger ligt dan de hoeveelheid vraagprognoseregels in dezelfde reductiesleutelperiode, wordt het saldo van de hoeveelheid voorraadtransacties gebruikt om de vraagprognosehoeveelheid in de vorige periode te verminderen (als er niet-geconsumeerde prognose is).

Als er geen niet-geconsumeerde prognose overblijft in de vorige reductiesleutelperiode, wordt het saldo van de hoeveelheid voorraadtransacties gebruikt om de prognosehoeveelheid in de volgende maand te verminderen (als er niet-geconsumeerde prognose is).

De waarde van het veld **Percentage** op de reductiesleutelregels wordt niet gebruikt wanneer het veld **Gebruikte methode om prognosebehoeften te verminderen** wordt ingesteld op *Transacties - reductiesleutel*. Alleen de datums worden gebruikt om de reductiesleutelperiode te definiëren.

> [!NOTE]
> Prognoses die op of voor de datum van vandaag worden geboekt, worden genegeerd en worden niet gebruikt om geplande orders aan te maken. Als uw vraagprognose voor de maand bijvoorbeeld op 1 januari wordt gegenereerd en u op 2 januari de hoofdplanning maakt die vraagprognose bevat, negeert de berekening de vraagprognoseregel met 1 januari.

##### <a name="example-transactions--reduction-key"></a>Voorbeeld: Transacties - reductiesleutel

In dit voorbeeld wordt weergegeven hoe werkelijke orders, die plaatsvinden tijdens de perioden die zijn gedefinieerd door de reductiesleutel, vraagprognosebehoeften reduceren.

[![Werkelijke orders en prognoses voordat de hoofdplanning wordt uitgevoerd.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Voor dit voorbeeld selecteert u *Transacties - reductiesleutel* in het veld **Methode gebruikt voor het reduceren van prognosebehoeften** op de pagina **Hoofdplannen**.

De volgende vraagprognoseregels bestaan op 1 april.

| Datum     | Aantal stuks voorspeld |
|----------|-----------------------------|
| 5 april  | 100                         |
| 12 april | 100                         |
| 19 april | 100                         |
| 26 april | 100                         |
| mei 3    | 100                         |
| mei 10   | 100                         |
| mei 17   | 100                         |

De volgende verkooporderregels bestaan in april.

| Datum     | Aangevraagd aantal stuks |
|----------|----------------------------|
| 27 april | 240                        |

[![Gepland aanbod dat is gegenereerd op basis van orders in april.](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

De volgende vereiste hoeveelheden worden naar het hoofdplan overgebracht wanneer de hoofdplanning op 1 april wordt uitgevoerd. Zoals u ziet, zijn de prognosetransacties voor april verminderd met de vraaghoeveelheid van 240 in een reeks, te beginnen bij de eerste van die transacties.

| Datum     | Benodigd aantal stuks |
|----------|---------------------------|
| 5 april  | 0                         |
| 12 april | 0                         |
| 19 april | 60                        |
| 26 april | 100                       |
| 27 april | 240                       |
| mei 3    | 100                       |
| mei 10   | 100                       |
| mei 17   | 100                       |

Stel nu dat er nieuwe orders zijn geïmporteerd voor de periode van mei.

De volgende verkooporderregels bestaan in mei.

| Datum   | Aangevraagd aantal stuks |
|--------|----------------------------|
| mei 4  | 80                         |
| mei 11 | 130                        |

[![Gepland aanbod dat is gegenereerd op basis van orders in april en mei.](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

De volgende vereiste hoeveelheden worden naar het hoofdplan overgebracht wanneer de hoofdplanning op 1 april wordt uitgevoerd. Zoals u ziet, zijn de prognosetransacties voor april verminderd met de vraaghoeveelheid van 240 in een reeks, te beginnen bij de eerste van die transacties. De prognosetransacties voor mei werden echter met een totaal van 210 verlaagd, te beginnen bij de eerste vraagprognosetransactie in mei. De totalen per periode blijven echter behouden (400 in april en 300 in mei).

| Datum     | Benodigd aantal stuks |
|----------|---------------------------|
| 5 april  | 0                         |
| 12 april | 0                         |
| 19 april | 60                        |
| 26 april | 100                       |
| 27 april | 240                       |
| mei 3    | 0                         |
| mei 4    | 80                        |
| mei 10   | 0                         |
| mei 11   | 130                       |
| mei 17   | 90                        |

#### <a name="transactions--dynamic-period"></a>Transacties - dynamische periode

Als u **Transacties - dynamische periode** selecteert, worden de prognosebehoeften gereduceerd met de werkelijke ordertransacties die tijdens de dynamische periode plaatsvinden. De dynamische periode bestrijkt de huidige prognosedatums en eindigt bij het begin van de volgende prognose. In dit geval worden in de hoofdplanning geplande orders gemaakt voor het leveren van de geraamde vraag (prognosebehoeften). Wanneer echter werkelijke ordertransacties worden geplaatst, worden de prognosebehoeften gereduceerd. De werkelijke transacties verbruiken een gedeelte van de geraamde behoeften.

Wanneer deze optie wordt gebruikt, vindt het volgende gedrag plaats:

- Reductiesleutels worden niet vereist of gebruikt. 
- Als de prognose volledig is gereduceerd, worden de prognosebehoeften voor de huidige prognose 0 (nul).
- Als er geen toekomstige prognose is, worden de prognosebehoeften van de laatste prognose die is ingevoerd, gereduceerd.
- De timefences worden opgenomen in de berekening van de prognosereductie.
- Positieve dagen zijn opgenomen in de berekening van de prognosereductie.
- Als de werkelijke ordertransacties de prognosebehoeften overschrijden, worden de resterende transacties niet naar de volgende prognoseperiode doorgestuurd.

##### <a name="example-1-transactions--dynamic-period"></a>Voorbeeld 1: Transacties - dynamische periode

Hier vindt u een eenvoudig voorbeeld dat laat zien hoe de methode **Transacties - dynamische periode** werkt.

Voor dit voorbeeld neemt u de volgende vraagprognose in een hoofdplan op.

| Datum       | Vraagprognose |
|------------|-----------------|
| 1 januari  | 1.000           |
| 1 februari | 1.000             |

U maakt ook de volgende verkooporders.

| Datum        | Verkooporderhoeveelheid |
|-------------|----------------------|
| 15 januari  | 200                  |
| 15 februari | 400                  |

In dit geval worden de volgende geplande orders gemaakt.

| Vraagprognosedatum | Hoeveelheid | Uitleg                           |
|--------------------- |----------|---------------------------------------|
| 1 januari            | 800      | Prognosebehoeften (= 1.000 – 200) |
| 15 januari           | 200      | Verkooporderbehoeften             |
| 1 februari           | 600      | Prognosebehoeften (= 1.000 – 400) |
| 15 februari          | 400      | Verkooporderbehoeften             |

##### <a name="example-2-transactions--dynamic-period"></a>Voorbeeld 2: Transacties - dynamische periode

In de meeste gevallen worden systemen zo ingesteld dat met transacties vraagprognose worden gereduceerd in specifieke prognoseperioden: weken, maanden enzovoort. Deze perioden worden gedefinieerd in de reductiesleutel. De tijd tussen twee vraagprognoseregels kan echter ook een periode *impliceren*.

Voor dit voorbeeld maakt u een vraagprognose voor de volgende datums en hoeveelheden.

| Datum       | Vraagprognose |
|------------|-----------------|
| 1 januari  | 1.000           |
| 5 januari  | 500             |
| 12 januari | 1.000           |

U ziet dat in deze prognose er geen duidelijke periode tussen de prognosedatums is. Tussen de eerste en tweede datum bevindt zich een periode van vier dagen en tussen de tweede en derde datum bevindt zich een periode van zeven dagen. Deze perioden zijn de dynamische perioden.

U maakt ook de volgende verkooporderregels.

| Datum                             | Verkooporderhoeveelheid |
|----------------------------------|----------------------|
| 15 december in het vorige jaar | 500                  |
| 3 januari                        | 100                  |
| 10 januari                       | 200                  |

In dit geval wordt de prognose op de volgende manier gereduceerd:

- Omdat de eerste verkooporder in geen enkele periode valt, wordt hiermee geen prognose gereduceerd.
- Omdat de tweede verkooporder tussen 1 januari en 5 januari ligt, wordt hiermee de prognose voor 1 januari met 100 gereduceerd.
- Omdat de derde verkooporder tussen 5 januari en 12 januari ligt, wordt hiermee de prognose voor 5 januari met 200 gereduceerd.

Daarom worden de volgende geplande orders gemaakt.

| Vraagprognosedatum             | Hoeveelheid | Uitleg                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15 december in het vorige jaar | 500      | Verkooporderbehoeften                                            |
| 1 januari                        | 900      | Periode van prognosebehoeften 1 januari tot en met 5 januari (= 1.000 - 100) |
| 3 januari                        | 100      | Verkooporderbehoeften                                            |
| 5 januari                        | 300      | Periode van prognosebehoeften 5 januari tot en met 10 januari (= 500 - 200)  |
| 12 januari                       | 1.000    | Periode van prognosebehoeften 12 januari tot einde                      |

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Een prognosereductiesleutel maken en instellen

Een prognosereductiesleutel wordt gebruikt in de methoden **Transacties - reductiesleutel** en **Percentage - reductiesleutel** voor het reduceren van prognosebehoeften. Voer deze stappen uit om een reductiesleutel te maken en in te stellen.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Reductiesleutels**.
2. Selecteer **Nieuw** om een reductiesleutel te maken.
3. Voer in het veld **Reductiesleutel** een unieke id voor de prognosereductiesleutel in. Voer vervolgens in het veld **Naam** een naam in. 
4. Definieer de perioden en het reductiesleutelpercentage in elke periode:

    - Met het veld **Ingangsdatum** wordt de datum aangegeven waarop het maken van de perioden wordt gestart. Wanneer de optie **De ingangsdatum gebruiken** is ingesteld op **Ja**, beginnen de perioden op de ingangsdatum. Als deze is ingesteld op **Nee**, begint de periode op de datum waarop de hoofdplanning wordt uitgevoerd.
    - Definieer de perioden gedurende welke de prognosereductie moet plaatsvinden.
    - Geef voor een bepaalde periode de percentages op waarmee de prognosebehoeften moeten worden gereduceerd. U kunt positieve waarden invoeren om de behoeften te verminderen of negatieve waarden om de behoeften te vergroten.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Een reductiesleutel gebruiken

Een prognosereductiesleutel moet worden toegewezen aan de behoefteplanningsgroep van het artikel. Voer deze stappen uit voor het toewijzen van een reductiesleutel aan de behoefteplanningsgroep van een artikel.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Behoefteplanningsgroepen**.
2. Selecteer in het veld **Reductiesleutel** op het sneltabblad **Overige** de reductiesleutel die u aan de behoefteplanningsgroep wilt toewijzen. De reductiesleutel wordt vervolgens toegepast op alle artikelen van de behoefteplanningsgroep.
3. Als u een reductiesleutel wilt gebruiken om tijdens de hoofdplanning een prognose reductie te berekenen, moet u deze instelling opgeven in de instellingen van het prognoseplan of het hoofdplan. Ga naar een van de volgende locaties:

    - **Hoofdplanning \> Instellen \> Plannen \> Prognoseplannen**
    - **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**

4. Selecteer op de pagina **Prognoseplannen** of **Hoofdplannen** op het sneltabblad **Algemeen** in het veld **Gebruikte methode voor het reduceren van prognosebehoeften** **Percentage - reductiesleutel** of **Transacties - reductiesleutel**.

### <a name="reduce-a-forecast-by-transactions"></a>Een prognose op basis van transacties reduceren

Wanneer u **Transacties - reductiesleutel** of **Transacties - dynamische periode** selecteert als de methode voor het reduceren van prognosebehoeften, kunt u opgeven met welke transacties de prognose wordt gereduceerd. Selecteer op de pagina **Behoefteplanningsgroepen** op het sneltabblad **Overige** in het veld **Prognose reduceren met** **Alle transacties** als de prognose moeten worden gereduceerd met alle transacties of **Orders** als de prognose alleen met verkooporders moet worden gereduceerd.

## <a name="forecast-models-and-submodels"></a>Prognosemodellen en submodellen

In deze sectie wordt beschreven hoe u prognosemodellen maakt en hoe u meerdere prognosemodellen combineert door submodellen in te stellen.

Een *prognosemodel* benoemt en identificeert een bepaalde prognose. Nadat u het prognosemodel hebt gemaakt, kunt u er prognoseregels aan toevoegen. Als u prognoseregels voor meerdere artikelen wilt toevoegen, gebruikt u de pagina **Vraagprognoseregels**. U kunt prognoseregels voor een specifiek geselecteerd artikel toevoegen op de pagina **Vrijgegeven producten**.

Een prognosemodel kan prognoses van andere prognosemodellen bevatten. U bereikt dit resultaat door andere prognosemodellen toe te voegen als *submodellen* van een bovenliggend prognosemodel. U moet elk relevant model maken voordat u dit kunt toevoegen als submodel van een bovenliggend prognosemodel.

De resulterende structuur biedt u een krachtige manier om prognoses te beheren, omdat u hiermee de invoer uit meerdere afzonderlijke prognoses kunt combineren (samengevoegd). Daarom is het vanuit oogpunt van planning eenvoudig om prognoses voor simulaties te combineren. U kunt bijvoorbeeld een simulatie instellen die is gebaseerd op de combinatie van een normale prognose met de prognose voor een lentepromotie.

### <a name="submodel-levels"></a>Submodelniveaus

Er is geen limiet voor het aantal submodellen dat aan een bovenliggend prognosemodel kan worden toegevoegd. De structuur kan echter slechts één niveau diep zijn. Met andere woorden, een prognosemodel dat een submodel is van een ander prognosemodel kan geen eigen submodellen hebben. Wanneer u submodellen aan een prognosemodel toevoegt, controleert het systeem of dat prognosemodel al een submodel of een ander prognosemodel is.

Als er in de hoofdplanning een submodel met eigen submodellen wordt gevonden, wordt een foutbericht weergegeven.

#### <a name="submodel-levels-example"></a>Voorbeeld van submodelniveaus

Prognosemodel A heeft prognosemodel B als submodel. Prognosemodel B kan daarom geen eigen submodellen hebben. Als u een submodel probeert toe te voegen aan prognosemodel B, wordt het volgende foutbericht weergegeven: 'Prognosemodel B is een submodel voor model A'.

### <a name="aggregating-forecasts-across-forecast-models"></a>Prognoses samenvoegen in prognosemodellen

Prognoseregels die op dezelfde dag plaatsvinden, worden samengevoegd in hun prognosemodel en de submodellen.

#### <a name="aggregation-example"></a>Voorbeeld van samenvoeging

Prognosemodel A heeft prognosemodel B en C als submodellen.

- Prognosemodel A bevat een vraagprognose voor 2 stuks op 15 juni.
- Prognosemodel B bevat een vraagprognose voor 3 stuks op 15 juni.
- Prognosemodel C bevat een vraagprognose voor 4 stuks op 15 juni.

De resulterende vraagprognose is één vraag naar 9 stuks (2 + 3 + 4) op 15 juni.

> [!NOTE]
> Elk submodel heeft eigen parameters, niet de parameters van het bovenliggende prognosemodel.

### <a name="create-a-forecast-model"></a>Een prognosemodel maken

Volg deze stappen om een prognosemodel te maken:

1. Ga naar **Hoofdplanning \> Instellen \> Vraagprognose \> Prognosemodellen**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel de volgende velden in voor het nieuwe prognosemodel:

    - **Model**: hier kunt u een unieke ID voor het model invoeren.
    - **Naam**: voer een beschrijvende naam in voor het model.
    - **Gestopt**: u moet deze optie meestal instellen op *Nee*. Stel het alleen in op *Ja* als u wilt voorkomen dat alle prognoseregels die aan het model zijn toegewezen, worden bewerkt.

    > [!NOTE]
    > Het veld **Opnemen in cashflowprognoses** en de velden op het sneltabblad **Project** zijn niet gerelateerd aan de hoofdplanning. Daarom kunt u ze in deze context negeren. U moet ze alleen in overweging nemen wanneer u werkt met prognoses voor de module **Projectbeheer en boekhouding**.

### <a name="assign-submodels-to-a-forecast-model"></a>Submodellen toewijzen aan een prognosemodel

Volg deze stappen om submodellen aan een prognosemodel toe te wijzen.

1. Ga naar **Voorraadbeheer \> Instellen \> Prognose \> Prognosemodellen**.
1. Selecteer in het lijstdeelvenster het prognosemodel waarvoor u een submodel wilt instellen.
1. Selecteer op het sneltabblad **Submodel** de optie **Toevoegen** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende velden in.

    - **Submodel**: selecteer het prognosemodel dat u wilt toevoegen als submodel. Dit prognosemodel moet al bestaan en mag geen eigen submodellen hebben.
    - **Naam**: voer een beschrijvende naam in voor het submodel. Deze naam kan bijvoorbeeld de relatie van het submodel met het bovenliggende prognosemodel aangeven.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

