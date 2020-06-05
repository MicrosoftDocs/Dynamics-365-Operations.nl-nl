---
title: Werkorders plannen
description: In dit onderwerp wordt uitgelegd hoe u werkorders plant in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e98a30a03856f5532d420e516cb35d66acffb278
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383476"
---
# <a name="schedule-work-orders"></a>Werkorders plannen

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u werkorders plant in Activabeheer. 

Het vereiste aantal uren voor een werkorder wordt gedefinieerd op basis van het totaal aan voorspelde uren min de geboekte uren. Als er meer tijd nodig is, moet de prognose dienovereenkomstig worden aangepast. In **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders** kunt u prognoses in een werkorder weergeven of bewerken door de werkorder te selecteren en te klikken op **Prognose** op het tabblad **Werkorder**. Wanneer werkorders zijn gemaakt en geraamd, moeten de vereiste onderhoudsmedewerkers en hulpmiddelen worden toegewezen om de werkorders te voltooien.

Alleen werkorders met een levenscyclusstatus voor werkorders die planning toestaat, kunnen worden gepland. U kunt planning toestaan via **Activabeheer** > **Instellingen** > **Werkorders** > **Levenscyclusstatussen** > het sneltabblad **Algemeen** > de wisselknop **Planning toestaan**.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders**.

2. Selecteer in de lijst de werkorders die u wilt plannen. U kunt de lijst bijvoorbeeld sorteren op **Huidige levenscyclusstatus**.

3. Klik op het tabblad **Algemeen** op **Plannen**.

4. In het dialoogvenster **Werkorders plannen** kunt u zo nodig selecties toevoegen met betrekking tot de verwachte begindatum en het serviceniveau. Als in het planningsproces capaciteitsbeperkingen in acht moeten worden genomen voor resources die al zijn gepland voor andere taken, moet u ervoor zorgen dat de wisselknoppen **Activum**, **Hulpmiddel** en **Medewerker** zijn ingesteld op Ja.

    [!NOTE]
    Als u de wisselknoppen **Activum**, **Hulpmiddel** en **Medewerker** instelt op Nee, worden bestaande reserveringen genegeerd. In het infologboek wordt een lijst met overlappende werkorderplanningen weergegeven en u kunt op de berichten klikken om een werkorder te openen en opnieuw te plannen, indien nodig.

5. Als u gedetailleerde informatie over het planningsproces wilt weergeven, stelt u de wisselknop in op **Uitgebreid**. Dit betekent dat er gedetailleerde informatie over de berekende scores voor de werkorders en onderhoudsmedewerkers wordt weergegeven in het infologboek.

6. Klik op **OK** om het planningsproces te starten.

7. Wanneer de planning is voltooid, wordt in een infologboek het aantal geplande werkorders weergegeven. Als de wisselknop **Uitgebreid** is ingesteld op Ja, wordt er meer gedetailleerde informatie weergegeven.

>[!NOTE]
>Werkorders worden gepland in één cyclus per werkorder, niet per werkordertaak. U kunt het dialoogvenster **Werkorders plannen** ook rechtstreeks openen via **Activabeheer** > **Periodiek** > **Werkorders** > **Werkorders plannen**. Selecteer de gewenste opties en klik op **OK** om de planning van werkorders te starten. Het is mogelijk om werkorderplanning in te stellen als een batchtaak in het dialoog venster **Werkorders plannen** (via het sneltabblad **Op de achtergrond uitvoeren**).

*Voorbeeld*: in de volgende afbeelding genereert de formule ingevoegd in het veld **Verwachte begindatum** de planning van de werkorder voor alle werkorders met een verwachte begindatum een week vanaf nu en later. Deze formule kan handig zijn wanneer u voortdurend werkorders plant, maar er zeker van wilt zijn dat de geplande werkorders voor de komende 5-6 dagen niet opnieuw worden gepland.

![Figuur 1](media/03-work-order-scheduling.png)

Voor het werkordertype dat aan werkorders is gekoppeld, kan de planning voor één onderhoudsmedewerker worden ingesteld (**Activabeheer** > **Instellingen** > **Werkorders** > **Werkordertypen** > **Eén onderhoudsmedewerker** ingesteld op Ja). Als het werkordertype wordt gebruikt voor een werkorder, wordt de wisselknop **Eén onderhoudsmedewerker** dus automatisch ingesteld op Ja op de detailpagina **Alle werkorders** > weergave **Koptekst** > sneltabblad **Plannen**. Bij de planning van werkorders worden alle werkordertaken die in de werkorder zijn gemaakt gepland voor dezelfde onderhoudsmedewerker. Indien nodig kunt u de selectie bewerken met de wisselknop **Eén onderhoudsmedewerker** in **Alle werkorders** om verschillende medewerkers of één medewerker te plannen voor de werkordertaken.

Het planningsproces in Activabeheer omvat verschillende factoren in de planningsberekening:

- De berekening van scores voor werkorders en onderhoudsmedewerkers. Scores voor werkorders en onderhoudsmedewerkers worden ingesteld in **Parameters voor activabeheer**. 
- Het controleren op overeenkomende competenties (vaardigheden en certificaten) die vereist zijn om de taak uit te voeren. Vaardigheden en certificaten worden voor onderhoudsmedewerkers ingesteld in de module **Human Resources** (**Human Resources** > **Medewerkers** > **Medewerkers** > selecteer een medewerker in de lijst > het tabblad **Medewerker** > de sectie **Competenties** > de knoppen **Vaardigheden** en **Certificaten**). Daarnaast kunnen vaardigheden en certificaten worden toegevoegd aan typen onderhoudstaken en onderhoudstaakspecialismen. In [Categorieën van onderhoudstaaktypen en onderhoudstaaktypen, varianten van onderhoudstaaktypen, onderhoudstaakspecialismen en onderhoudscontrolelijsten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) vindt u meer informatie over competenties en onderhoudstaaktypen.  

## <a name="scores-used-in-work-order-scheduling"></a>Scores die worden gebruikt bij het plannen van werkorders

De berekening van scores voor een werkordertaak is gebaseerd op de verwachte begindatum en het serviceniveau van de werkorder.

Berekening van **begindatum**: voor elke toekomstige datum die wordt berekend op basis van de verwachte begindatum, wordt de score van de begindatum afgetrokken en vermenigvuldigd met de score, die 10 is in de onderstaande voorbeelden.

Berekening van **kritieke eigenschap**: de score voor de kritieke eigenschap vermenigvuldigd met de kritieke eigenschap van de werkorder.

Berekening van **serviceniveau**: de score voor het serviceniveau gedeeld door het serviceniveau van de werkorder.

In de onderstaande voorbeelden is de score voor de kritieke eigenschap 2 en zijn de scores voor het serviceniveau 5 en 100.

**Voorbeeld 1:**

| Werkorder-id | Verwachte begindatum | Kritieke eigenschap van werkorder | Serviceniveau van werkorder | Berekening               | Score      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Morgen            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Over twee dagen   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Over twee dagen   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

De werkorders worden in de volgende volgorde gepland: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**Voorbeeld 2:**

| Werkorder-id | Verwachte begindatum | Kritieke eigenschap van werkorder | Serviceniveau van werkorder | Berekening                 | Score    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Morgen            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Over twee dagen   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Over twee dagen   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Als de score voor het serviceniveau wordt verhoogd naar 100 in plaats van 5, is de planningsvolgorde: WO-000108**18**, WO-000108**16**, WO-000108**17**.

De beoordelingsscores die betrekking hebben op de berekening van onderhoudsmedewerkers die aan de werkorders moeten werken, worden allemaal ingesteld als aantallen, die tijdens de planning van werkorders worden opgeteld bij elke berekening van onderhoudsmedewerkers. De onderhoudsmedewerker met de hoogste score wordt geselecteerd voor de werkorder. Hier volgt een korte omschrijving van de scores van de onderhoudsmedewerker:

| Score onderhoudsmedewerker| Beschrijving |
|---|---|
| Verantwoordelijke medewerker | Als de onderhoudsmedewerker wordt geselecteerd als verantwoordelijke medewerker voor de werkorder, wordt de score toegevoegd. |
| Verantwoordelijke onderhoudsmedewerkersgroep | Als de onderhoudsmedewerker deel uitmaakt van de verantwoordelijke groep onderhoudsmedewerkers voor de werkorder, wordt de score toegevoegd. |
| Onderhoudsmedewerker van voorkeur         | Als de medewerker wordt geselecteerd als onderhoudsmedewerker van voorkeur voor het activum, wordt de score toegevoegd. |
| Onderhoudsmedewerkersgroep van voorkeur   | Als de medewerker deel uitmaakt van de onderhoudsmedewerkergroep van voorkeur voor het activum, wordt de score toegevoegd.  |
| Locatie  | Als uw bedrijf gebruikmaakt van functionele locaties, krijgen onderhoudsmedewerkers een volledige score als ze zich op de functionele locatie bevinden die betrekking heeft op het activum. Als de functionele locatie van het activum een bovenliggende locatie heeft, krijgen onderhoudsmedewerkers op die functionele locatie 1/2 score. Als die locatie ook een bovenliggend item heeft, krijgen onderhoudsmedewerkers op die locatie 1/3 score. Als die locatie ook een bovenliggend item heeft, krijgen onderhoudsmedewerkers op die locatie 1/4 score. Als uw bedrijf activalocatie gebruikt, wat we niet aanbevelen, worden locatie, gebied en zone gebruikt om locatiescores te berekenen. Werknemers krijgen een volledige score als ze zich op de locatie en in het gebied en de zone bevinden die verband houdt met het activum. Als de locatie van de medewerker alleen overeenkomt met locatie en gebied, is de beoordelingsscore voor de onderhoudsmedewerker 2/3 van de volledige score. Als de locatie van de onderhoudsmedewerker alleen overeenkomt met locatie, is de beoordelingsscore voor de onderhoudsmedewerker 1/3 van de volledige score. |
| Begindatum van medewerker  | Voor elke dag dat de geplande begindatum later is dan de verwachte begindatum, wordt de score afgetrokken.  |

>[!NOTE]
>Als een score is ingesteld op 0, wordt deze score niet berekend. Dit is handig als u bijvoorbeeld geen verantwoordelijke medewerker wilt opnemen in de planning.

## <a name="competencies-used-in-work-order-scheduling"></a>Competenties die worden gebruikt bij het plannen van werkorders

Er kunnen vaardigheden en certificaatvereisten worden ingesteld voor onderhoudstaaktypen (**Activabeheer** > **Instellingen** > **Taken** > **Onderhoudstaaktypen**) en onderhoudstaakspecialismen (**Activabeheer** > **Instellingen** > **Taken** > **Specialisme onderhoudstaak**). 

Voor werkordertaken worden typen onderhoudstaken en onderhoudstaakspecialismen geselecteerd. Als vaardigheden of certificaten zijn geselecteerd voor een type onderhoudstaak of een onderhoudstaakspecialisme en dat type onderhoudstaak of onderhoudstaakspecialisme wordt gebruikt voor een werkorder, worden alleen onderhoudsmedewerkers met overeenkomende vaardigheden en certificaten ingepland voor werk aan de werkorder.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Werken met geplande werkorders met behulp van een Gantt-diagram

Het **Gantt-diagram Geplande werkorders** biedt een grafische interface waarin u uw werkorders kunt weergeven en opnieuw kunt plannen.

U kunt het Gantt-diagram als volgt weergeven en gebruiken:

1. Ga naar **Asset management > Werkorders > Gantt-diagram Geplande werkorders**.

1. Gebruik de vervolgkeuzelijsten en velden in de sectie **Instellingen** om functionele locatie, tijdsduur en tijdschaal in te stellen die in het Gantt-diagram moeten worden weergegeven.

1. Selecteer **Toepassing**.

    - Het Gantt-diagram wordt bijgewerkt om de geplande werkorders weer te geven die overeenkomen met uw instellingen. Elke werkorder wordt aangeduid met een blauwe rechthoek.
    - Als u een weergegeven werkorder opnieuw wilt plannen, selecteert u deze en sleept u de werkorder naar de gewenste nieuwe datum en tijd.

1. Als u wijzigingen hebt aangebracht, selecteert u **Opslaan** in het actievenster om ze op te slaan.
