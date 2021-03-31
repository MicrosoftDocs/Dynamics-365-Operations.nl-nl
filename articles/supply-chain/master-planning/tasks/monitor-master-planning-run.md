---
title: Een hoofdplanningsuitvoering controleren
description: In dit onderwerp wordt beschreven hoe de productieplanner kan zien of een hoofdplanning wordt uitgevoerd.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2dea87ac106e79339b8cb6bb2c28e36e35de4a1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226094"
---
# <a name="monitor-a-master-planning-run"></a>Een hoofdplanningsuitvoering controleren

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Een Gantt-diagram gebruiken om de voortgang van de hoofdplanning te visualiseren

Op de pagina **Voortgang van hoofdplanning weergeven** kunt u details van historische hoofdplanningsuitvoeringen als een Gantt-diagram weergeven. Deze functionaliteit kan u helpen om te begrijpen hoeveel tijd wordt besteed aan de verschillende fasen van de hoofdplanning. Voor een huidige actieve planningstaak kan de pagina **Voortgang van hoofdplanning weergeven** worden gebruikt om de voortgang bij te houden en de geschatte resterende tijd weer te geven.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>De functie voor visualisatie van de voortgang van de hoofdplanning inschakelen en gebruiken

Volg deze stappen om deze functionaliteit te gebruiken.

1. Selecteer **Visualisatie van voortgang van hoofdplanning** in de lijst op het tabblad **Nieuw** van het werkgebied **Functiebeheer**. Als de functie niet wordt weergegeven op het tabblad **Nieuw**, kijkt u op de tabbladen **Niet ingeschakeld** en **Alle**.
1. Selecteer **Nu inschakelen**. U kunt ook **Planning** selecteren en vervolgens het tijdstip selecteren waarop u de functie wilt inschakelen.

Op de pagina **Voortgang van hoofdplanning weergeven** kunnen zowel historische planningstaken als actieve planningstaken worden weergegeven. 

Er zijn twee opties voor het weergeven van historische planningstaken. 

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen** en selecteer in het actievenster de optie **Historie**. Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.
1. Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning** en klik op de tegel Hoofdplanning op **Historie**. Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.

Er zijn twee opties voor het weergeven van actieve planningstaken. 
1. Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning** en selecteer in het actievenster de optie **Onvoltooid planningsproces**. Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.
1. Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning** en klik op de tegel Hoofdplanning op **Voortgang weergeven**. Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.

U kunt actieve taken alleen weergeven wanneer een planningstaak wordt verwerkt.

### <a name="analyze-a-master-planning-job"></a>Een hoofdplanningstaak analyseren

In het Gantt-diagram kunt u elk van de volgende planningsprocessen uitvouwen om extra details weer te geven over de tijd die wordt besteed:

- Bezig met initialiseren
- Gegevens verwijderen en invoegen
- Behoefteplan
- Vertragingen
- Actieberichten
- Voltooiing
- Automatische fiattering

Het Gantt-diagram is een handige tool als u de gevolgen van het gebruik van actieberichten wilt bekijken.

#### <a name="navigation-in-the-gantt-chart"></a>Navigatie in het Gantt-diagram

- Als u de geselecteerde groep wilt uitvouwen en de details wilt weergeven, selecteert u het plusteken (**+**) in de structuurweergave.
- Als u de geselecteerde groep wilt samenvouwen, selecteert u het minteken (**–**) in de structuurweergave.
- U kunt het toetsenbord gebruiken voor navigatie. Gebruik de toetsen **Pijl-omhoog** en **Pijl-omlaag** om tussen rijen te navigeren. Gebruik de toetsen **Pijl-rechts** en **Pijl-links** om groepen uit en samen te vouwen.
- Als u alle niveaus in het Gantt-diagram wilt openen of sluiten, selecteert u **Alles uitvouwen** of **Alles samenvouwen**.
- Als u de bijbehorende verwerkingstijd wilt weergeven, plaatst u de muisaanwijzer op een taak. (Taken zijn het laagste niveau in het Gantt-diagram.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Een extra hoofdplanningsuitvoering weergeven om taken te vergelijken

Door een hoofdplanningstaak te selecteren in het veld **Extra hoofdplanningsuitvoering weergeven**, kunt u een extra hoofdplanningsuitvoering weergeven in het Gantt-diagram en de twee taken met elkaar vergelijken.

#### <a name="bom-level-display"></a>Weergave op stuklijstniveau

Stuklijstniveaus worden anders weer gegeven voor behoefteplanningen, vertragingen, acties en fiatteringen.

- **Behoefteplan**: stuklijstniveaus worden zoals verwacht weergegeven. Ze worden van boven naar beneden berekend.

    **Voorbeeld**: stuklijstniveau 0, 1, 2

- **Vertragingen**: stuklijstniveaus worden weer gegeven als de stuklijstniveaus van de behoefteplanning vermenigvuldigd met –1. (Met andere woorden, ze hebben een minteken.)

    **Voorbeeld**: stuklijstniveau –2, –1, 0

- **Actiebericht**: stuklijstniveaus worden zoals verwacht weergegeven. Ze worden van boven naar beneden berekend.

    **Voorbeeld**: stuklijstniveau 0, 1, 2

- **Automatische fiattering**: stuklijstniveaus worden weergegeven als 999 min het stuklijstniveau van de behoefteplanning.

    **Voorbeeld**: stuklijstniveau 999, 998, 997

De volgende tabel biedt een overzicht van het gedrag.

| Stuklijstniveau dat wordt weergegeven | Eindartikel | Subonderdeel | Grondstoffen |
|---|---|---|---|
| Behoefteplan | 0 | 1 | 2 |
| Vertragingen | 0 | –1 | –2 |
| Actiebericht | 0 | 1 | 2 |
| Automatische fiattering | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Voortgang visualiseren

Als u een hoofdplanningstaak bekijkt die momenteel wordt uitgevoerd, wordt de voortgang met kleuren weergegeven in het Gantt-diagram. De volgende kleuren zijn van toepassing op het blauwe thema: Voor andere kleurenthema's zijn de kleuren anders.

- **Donkerblauw**: voltooide planningstaken.
- **Oranje**: de taak die momenteel wordt uitgevoerd.
- **Lichtblauw**: de raming voor de resterende taken.

De kleur wordt alleen weergegeven op het laagste niveau in het Gantt-diagram. Selecteer **Alles uitvouwen** om alle taken in de hoofdplanningstaak weer te geven. De raming van de resterende taken is gebaseerd op historische hoofdplanningstaken.

## <a name="run-master-planning-and-track-processing-time"></a>De hoofdplanning uitvoeren en verwerkingstijd bijhouden

1. Selecteer **Hoofdplanning** in het standaarddashboard.
1. Typ of selecteer een waarde in het veld **Plannen**.
1. Selecteer **Uitvoeren**.
1. Stel de optie **Verwerkingstijd traceren** in op **Ja**.
1. Voer een getal in het veld **Aantal threads** in.
1. Selecteer **Filter** op het sneltabblad **Op te nemen records**.
1. Selecteer in het raster de rij waarin het veld **Veld** is ingesteld op **Artikelnummer**.
1. Voer een waarde in het veld **Criteria** in.
1. Selecteer **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]