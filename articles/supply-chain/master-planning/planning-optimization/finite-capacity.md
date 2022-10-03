---
title: Eindige capaciteitsplanning
description: Eindige capaciteitsplanning helpt u inzicht te krijgen in hoeveel werk kan worden geproduceerd tijdens een specifieke periode wanneer rekening wordt gehouden met beperkingen voor verschillende resources.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c5eebe9ef6258b43daa7c7007ee28b0278fe5b09
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573132"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Eindige capaciteitsplanning

[!include [banner](../../includes/banner.md)]

Eindige capaciteit is een methode die u helpt inzicht te krijgen in hoeveel werk kan worden geproduceerd tijdens een specifieke periode wanneer rekening wordt gehouden met beperkingen voor verschillende resources. Het doel van eindige capaciteitsplanning is ervoor te zorgen dat werk in een gelijkmatig en efficiënt tempo wordt uitgevoerd in de hele fabriek.

Eindige capaciteitsplanning zorgt voor een realistischere planning voor de productieprocessen dan de methode van oneindig laden doet. Als de resources onvoldoende capaciteit hebben, wordt de leveringsdatum verlegd en wordt de taak gepland als er voldoende capaciteit is.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Planningsoptimalisatie-ondersteuning voor eindige capaciteitsplanning

Eindige capaciteitsplanning werkt op vrijwel dezelfde manier, ongeacht of u Planningsoptimalisatie of de ingebouwde planningsengine gebruikt. Bij Planningsoptimalisatie wordt de parameter **Tijdlimiet bottleneck** echter niet gebruikt. Wanneer u Planningsoptimalisatie gebruikt, worden bottleneck resources altijd gepland met dezelfde tijdlimiet als niet-bottleneck resources (zoals wordt aangegeven door de tijdlimiet van eindige capaciteit).

## <a name="set-up-finite-capacity-functionality"></a>Functionaliteit voor eindige capaciteit instellen

Als u de functionaliteit van eindige capaciteit wilt gebruiken, moet u capaciteitsplanning globaal inschakelen en moet u de eindige capaciteitsplanning inschakelen voor zowel het hoofdplan waarin u het wilt gebruiken als voor elke resource waarvoor deze van toepassing is. Voor plannen en resources waarvoor eindige capaciteit wordt ingeschakeld, wordt bij de planning van geplande productieorders rekening gehouden met capaciteit die al is gereserveerd. Geplande productieorders worden vanaf de behoeftedatum terug in de tijd gepland. Als capaciteit niet beschikbaar is om te voldoen aan de optimale planning, probeert het systeem componentartikelen op een eerdere datum te vereisen. Als uw capaciteit kan veranderen wanneer behoeften veranderen (bijvoorbeeld als er in ploegen wordt gewerkt), moet u de functionaliteit van eindige capaciteit niet gebruiken, omdat de berekende verwerkingstijden dan niet correct zijn. Bij de planning wordt alleen rekening gehouden met capaciteit die al is gereserveerd voor resources waarvoor eindige capaciteit is ingeschakeld. Door eindige capaciteit voor een resource in te schakelen, maakt u het mogelijk om de tijdlimiet van eindige capaciteit te wijzigen.

### <a name="activate-master-planning-parameters"></a>Parameters hoofdplanning activeren

Als u de functionaliteit van eindige capaciteit wilt gebruiken, moet u capaciteitsplanning inschakelen op de pagina **Parameters hoofdplanning**.

1. Ga naar **Hoofdplanning \> Instellen \> Parameters hoofdplanning**.
1. Stel op het tabblad **Geplande orders** in de sectie **Capaciteitsplanning** de optie **Productie** in op *Ja*.

### <a name="activate-a-master-plan"></a>Een hoofdplan activeren

U moet eindige capaciteitsplanning inschakelen voor elk hoofdplan waarin u deze wilt gebruiken.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer in het lijstdeelvenster een hoofdplan dat u wilt instellen voor gebruik van eindige capaciteitsplanning.
1. Stel op het sneltabblad **Algemeen** in de sectie **Geplande productieorders** de optie **Eindige capaciteit** in op *Ja*.
1. Herhaal stap 2 en 3 voor elk extra hoofdplan dat u wilt instellen.

### <a name="activate-resources"></a>Resources activeren

U moet eindige capaciteitsplanning inschakelen voor elke resource waarin u deze wilt gebruiken.

1. Ga naar **Productiebeheer \> Instellen \> Resources \> Resources**.
1. Selecteer in het lijstdeelvenster een resource die u wilt instellen voor gebruik van eindige capaciteitsplanning.
1. Stel op het sneltabblad **Bewerking** in de sectie **Capaciteit** de optie **Eindige capaciteit** in op *Ja*.
1. Herhaal stap 2 en 3 voor elke extra resource die u wilt instellen.

## <a name="examples"></a>Voorbeelden

In deze sectie vindt u de volgende voorbeelden die laten zien hoe u kunt werken met zowel oneindige als eindige capaciteitsplanning:

- Voorbeeld 1: oneindige capaciteitsplanning
- Voorbeeld 2: eindige capaciteitsplanning met een tijdlimiet van één dag
- Voorbeeld 3: eindige capaciteitsplanning met een tijdlimiet van twee dagen

### <a name="preconditions"></a>Voorwaarden vooraf

Voor alle drie de voorbeelden wordt ervan uit gaan dat de voorwaarden vooraf in deze sectie worden beschreven.

Product *Product1* heeft een route die de volgende bewerkingen bevat.

| Bewerkingsnummer | Bewerkingsnaam | Bron        | Uitvoeringstijd | Verwerkingshoeveelheid | Volgende |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Lassen        | Laslijn    | 1        | 2            | 20   |
| 20            | Assembleren     | Montagelijn | 1        | 4            |      |

Werknemers van uw bedrijf werken in één ploegendienst gedurende acht uur (8:00-16:00).

Er is een geplande productieorder voor *24 stuks* van *Product1*. De leveringsdatum is *Vandaag + 3 dagen*.

Als resultaat van de planning worden de resources op de volgende manier geladen:

- **Laslijn**: deze resource wordt geladen van *Vandaag om 8:00* tot *Vandaag + 1 om 12:00*.
- **Montagelijn**: deze resource wordt geladen van *Vandaag + 1 om 12:00* tot *Vandaag + 2 om 10:00*.

In de volgende afbeelding ziet u het resulterende Gantt-diagram (selecteer dit diagram voor een grotere weergave).

[![Gantt-diagram met voorwaarden vooraf.](media/finite-examples-conditions-small.png "Gantt-diagram met voorwaarden vooraf")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Voorbeeld 1: oneindige capaciteitsplanning

In dit voorbeeld ziet u de planningsresultaten wanneer u gebruikmaakt van oneindige capaciteitsplanning in plaats van eindige capaciteitsplanning.

Het hoofdplan heeft de volgende relevante instelling, waarmee eindige capaciteitsplanning voor het plan wordt uitgeschakeld:

- **Eindige capaciteit:** *Nee*

De optie **Eindige capaciteit** wordt ook ingesteld op *Nee* voor beide relevante resources om eindige capaciteitsplanning ervoor uit te schakelen:

- Laslijn
- Montagelijn

U voegt nu een nieuwe verkooporder toe voor *8 stuks* van *Product1* en voert het plan uit. Hierdoor wordt de laslijn geladen van *Vandaag om 8:00* tot *Vandaag om 12:00*. Nadat bewerkingen op de montagelijn zijn voltooid, wordt de montagelijn geladen van *Vandaag om 12:00* tot *Vandaag om 14:00*.

In de volgende afbeelding ziet u het resulterende Gantt-diagram (selecteer dit diagram voor een grotere weergave).

[![Gantt-diagram met een voorbeeld van oneindige capaciteitsplanning.](media/finite-examples-example1-small.png "Gantt-diagram met een voorbeeld van oneindige capaciteitsplanning")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Voorbeeld 2: eindige capaciteitsplanning met een tijdlimiet van één dag

In dit voorbeeld ziet u de planningsresultaten wanneer u gebruikmaakt van eindige capaciteitsplanning en een tijdlimiet van één dag.

Het hoofdplan heeft de volgende relevante instellingen, waarmee eindige capaciteitsplanning wordt ingeschakeld en een tijdlimiet voor het plan wordt ingesteld:

- **Eindige capaciteit:** *Ja*
- **Tijdlimiet eindige capaciteit:** *1*

De optie **Eindige capaciteit** wordt ook ingesteld op *Ja* voor beide relevante resources om eindige capaciteitsplanning ervoor in te schakelen:

- Laslijn
- Montagelijn

U voegt nu een nieuwe verkooporder toe voor *8 stuks* van *Product1* en voert het plan uit. Hierdoor wordt de laslijn geladen van *Vandaag + 1 om 8:00* tot *Vandaag + 1 om 12:00*. Nadat bewerkingen op de laslijn zijn voltooid, wordt de montagelijn geladen van *Vandaag + 1 om 12:00* tot *Vandaag + 1 om 14:00*. Er wordt slechts voor één dag rekening met de eindige capaciteit gehouden.

In de volgende afbeelding ziet u het resulterende Gantt-diagram (selecteer dit diagram voor een grotere weergave).

[![Gantt-diagram waarin eindige capaciteitsplanning met een tijdlimiet van één dag wordt getoond.](media/finite-examples-example2-small.png "Gantt-diagram waarin eindige capaciteitsplanning met een tijdlimiet van één dag wordt getoond")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Voorbeeld 3: eindige capaciteitsplanning met een tijdlimiet van twee dagen

In dit voorbeeld ziet u de planningsresultaten wanneer u gebruikmaakt van eindige capaciteitsplanning en een tijdlimiet van twee dagen.

Het hoofdplan heeft de volgende relevante instellingen, waarmee eindige capaciteitsplanning wordt ingeschakeld en een tijdlimiet voor het plan wordt ingesteld:

- **Eindige capaciteit:** *Ja*
- **Tijdlimiet eindige capaciteit:** *2*

De optie **Eindige capaciteit** wordt ook ingesteld op *Ja* voor beide relevante resources om eindige capaciteitsplanning ervoor in te schakelen:

- Laslijn
- Montagelijn

U voegt nu een nieuwe verkooporder toe voor *8 stuks* van *Product1* en voert het plan uit. Hierdoor wordt de laslijn geladen van *Vandaag + 1 om 12:00* tot *Vandaag + 1 om 16:00*. Nadat bewerkingen op de laslijn zijn voltooid, wordt de montagelijn geladen van *Vandaag + 2 om 8:00* tot *Vandaag + 2 om 10:00*. Er wordt slechts voor twee dagen rekening met de eindige capaciteit gehouden.

In de volgende afbeelding ziet u het resulterende Gantt-diagram (selecteer dit diagram voor een grotere weergave).

[![Gantt-diagram waarin eindige capaciteitsplanning met een tijdlimiet van twee dagen wordt getoond.](media/finite-examples-example3-small.png "Gantt-diagram waarin eindige capaciteitsplanning met een tijdlimiet van twee dagen wordt getoond")](media/finite-examples-example3.png)

> [!IMPORTANT]
> U moet de tijdlimiet van eindige capaciteit altijd aanpassen aan uw bedrijfsvereisten. De voorbeelden in dit artikel illustreren alleen de functionaliteit. In de praktijk is een tijdlimiet van één dag waarschijnlijk te kort voor de meeste fabrikanten die eindige capaciteitsplanning gebruiken.
