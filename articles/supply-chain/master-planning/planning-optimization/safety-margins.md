---
title: Veiligheidsmarges
description: In dit onderwerp wordt beschreven hoe u veiligheidsmarges kunt gebruiken met de invoegtoepassing Planningsoptimalisatie voor Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b66951b9c742af4aa11f681af8f9583a2d97d8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841858"
---
# <a name="safety-margins"></a>Veiligheidsmarges

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veiligheidsmarges kunt gebruiken met de invoegtoepassing Planningsoptimalisatie voor Microsoft Dynamics 365 Supply Chain Management.

## <a name="safety-margins-overview"></a>Overzicht van veiligheidsmarges

De veiligheidsmarges zijn bedoeld om een instelling mogelijk te maken die een bepaalde buffertijd na de normale doorloop tijd biedt. Wanneer materiaal bijvoorbeeld moet worden uitgepakt of geïnspecteerd nadat het van de leverancier is binnengekomen, kunt u niet alleen de extra tijd aan de inkoopdoorlooptijd toevoegen omdat bij deze aanpak de extra buffertijd aan de leverancier wordt gegeven. In dit voorbeeld kan de ontvangstmarge worden gebruikt om ervoor te zorgen dat de leverancier eerder levert. Deze benadering zorgt voor buffertijd zodat de goederen intern kunnen worden verwerkt.

Er zijn drie typen veiligheidsmarges:

- **Bestelmarge**: de buffertijd voor het plaatsen van de leveringsorder
- **Ontvangstmarge**: de buffertijd voor het verwerken van binnenkomende leveringen
- **Uitgiftemarge**: de buffertijd voor het verwerken van zendingen

In de volgende afbeelding ziet u hoe deze veiligheidsmarges in de loop der tijd van toepassing zijn.

![Veiligheidsmarges](media/safety-margins-1.png)

Alle marges worden gedefinieerd in dagen. De standaardwaarde *0* (nul) geeft aan dat geen marge wordt toegepast. Als u meerdere marges instelt, worden deze allemaal opgeteld bij de totale tijd tussen de *orderdatum* van de levering en de *behoeftedatum* van de vraag. Er kan bijvoorbeeld een configuratie met een doorlooptijd van nul worde gebruikt waarbij alle drie de margetypen zijn ingesteld op één dag. In dit geval zijn er drie dagen tussen de orderdatum van de levering en de behoeftedatum van de vraag, dus als de orderdatum 1 juli is, is de behoeftedatum 4 juli.

### <a name="receipt-margin"></a>Ontvangstmarge

De ontvangstmarge is waarschijnlijk de meest gebruikte veiligheidsmarge. Deze wordt toegepast op de *leveringsdatum* en loopt terug in de tijd vanaf de *behoeftedatum*. De producten moeten dus het opgegeven aantal dagen voor de ontvangstmarge worden ontvangen voordat ze nodig zijn.

In de volgende afbeelding wordt de ontvangstmarge benadrukt.

![Ontvangstmarge](media/safety-margins-2.png)

De ontvangstmarge wordt doorgaans gebruikt als buffer om voor tijd te garanderen voor magazijnregistratie of andere tijdrovende processen die niet zijn vastgelegd als onderdeel van de algemene doorlooptijd in het systeem. Voor inkopen is één voordeel dat de *leveringsdatum* van de inkooporder dienovereenkomstig naar voren wordt verplaatst. Als u de doorlooptijd verhoogt in plaats van een veiligheidsmarge te gebruiken, wordt de leverancier op het laatste moment nog steeds gevraagd te leveren.

U ziet dat de ontvangstmarge de *behoeftedatum* van de levering niet wijzigt. Daarom is de ontvangstmarge niet direct zichtbaar wanneer behoeftedatums voor vraag en aanbod worden vergeleken (bijvoorbeeld op de pagina **Nettobehoeften**). Als de ontvangstmarge bijvoorbeeld is ingesteld op vier dagen en een inkooporderregel is gepland voor ontvangst op de vijftiende van de maand, wordt in de hoofdplanning de negentiende van de maand als ontvangstdatum berekend.

Er wordt geen ontvangstmarge toegepast wanneer voorhanden voorraad wordt gebruikt als de levering. Er wordt aangenomen dat alle voorhanden voorraad direct beschikbaar is, ongeacht de werkelijke ontvangst.

### <a name="reorder-margin"></a>Bestelmarge

> [!NOTE]
> **Binnenkort:** deze functie wordt nog niet ondersteund voor Planningsoptimalisatie. Tot deze wordt ondersteund, worden alle ingevoerde waarden voor **Bestelmarge opgeteld bij doorlooptijd van artikel** behandeld als *0* (nul).

In de volgende afbeelding wordt de bestelmarge benadrukt.

![Bestelmarge](media/safety-margins-3.png)

De bestelmarge wordt opgeteld vóór de doorlooptijd van het artikel voor alle geplande orders tijdens de hoofdplanning. Op deze manier wordt extra tijd gegarandeerd voor het plaatsen van een leveringsorder. Deze marge wordt meestal gebruikt als buffer om tijd in te plannen voor goedkeuringsprocessen of andere interne processen die nodig zijn tijdens het maken van leveringsorders. De bestelmarge wordt tussen de *orderdatum* van de levering en de *begindatum* geplaatst.

### <a name="issue-margin"></a>Uitgiftemarge

> [!NOTE]
> **Binnenkort:** deze functie wordt nog niet ondersteund voor Planningsoptimalisatie. Tot deze wordt ondersteund, worden alle ingevoerde waarden voor **Uitgiftemarge afgetrokken van behoeftedatum** behandeld als *0* (nul).

In de volgende afbeelding wordt de uitgiftemarge benadrukt.

![Uitgiftemarge](media/safety-margins-4.png)

De uitgiftemarge wordt afgetrokken van de behoeftedatum van de vraag tijdens de hoofdplanning. Zo zorgt u ervoor dat u tijd hebt om te reageren op binnenkomende vraagorders en deze te verzenden. Deze marge wordt meestal gebruikt als buffer om ervoor te zorgen dat er tijd is voor verzending en gerelateerde uitgaande magazijnprocessen.

Wanneer een uitgiftemarge wordt toegepast, komen gerelateerde leverings- en behoeftedatums niet overeen. Het verschil is de uitgiftemarge, omdat de uitgiftemarge wordt toegevoegd tussen de *behoeftedatum* van de voorraad en de *behoeftedatum* van de vraag.

## <a name="set-up-safety-margins"></a>Veiligheidsmarges instellen

### <a name="turn-on-safety-margins-in-feature-management"></a>Veiligheidsmarges inschakelen in Functiebeheer

Voordat u deze functie kunt gebruiken met Planningsoptimalisatie, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** _Hoofdplanning_
- **Functienaam:** _Marges voor Planningsoptimalisatie_

### <a name="define-safety-margins"></a>Veiligheidsmarges definiëren

Veiligheidsmarges hebben een flexibele instelling. Deze kunnen worden ingesteld voor de *behoefteplanningsgroep* en het *hoofdplan*. Het is belangrijk dat u begrijpt dat de marges bij elkaar worden opgeteld. Een ontvangstmarge van twee dagen voor de behoefteplanningsgroep en drie dagen voor het hoofdplan levert bijvoorbeeld een effectieve ontvangstmarge van vijf dagen op.

De mogelijkheid om de marge voor het hoofdplan in te stellen kan nuttig zijn wanneer u langere doorlooptijden of onzekerheid voor een specifiek plan wilt simuleren, zonder dat dit van invloed is op de dagelijkse planning.

#### <a name="coverage-group-safety-margins"></a>Veiligheidsmarges voor behoefteplanningsgroep

Voer de volgende stappen uit om een veiligheidsmarge toe te passen op een behoefteplanningsgroep.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanningsgroepen**.
1. Selecteer de gewenste behoefteplanningsgroep in het lijstvenster.
1. Gebruik op het sneltabblad **Overige** in de sectie **Veiligheidsmarges in dagen** de volgende velden om de vereiste veiligheidsmarges in te stellen (in dagen):

    - Ontvangstmarge opgeteld bij behoeftedatum
    - Uitgiftemarge afgetrokken van behoeftedatum
    - Bestelmarge opgeteld bij doorlooptijd van artikel

#### <a name="master-plan-safety-margins"></a>Veiligheidsmarges voor hoofdplan

Voer de volgende stappen uit om een veiligheidsmarge toe te passen op een hoofdplan.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer het gewenste hoofdplan in het lijstvenster.
1. Gebruik op het sneltabblad **Veiligheidsmarges in dagen** de volgende velden om de vereiste veiligheidsmarges in te stellen (in dagen):

    - Ontvangstmarge opgeteld bij behoeftedatum
    - Uitgiftemarge afgetrokken van behoeftedatum
    - Bestelmarge opgeteld bij doorlooptijd van artikel

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Definiëren of berekeningen zijn gebaseerd op kalender- of werkdagen

U kunt alle veiligheidsmarges zo instellen dat deze worden berekend op basis van kalender- of werkdagen.

1. Ga naar **Hoofdplanning \> Instellen \> Parameters hoofdplanning**.
1. Stel op het tabblad **Algemeen** in de sectie **Veiligheidsmarges in dagen** de optie **Werkdagen** in op *Ja* als u de marges wilt berekenen op basis van werkdagen. Stel de optie in op *Nee* als u de marges wilt berekenen op basis van kalenderdagen.

Een kalender is bijvoorbeeld geopend van maandag tot en met vrijdag en gesloten van zaterdag tot en met zondag. Als er een ontvangstmarge van één dag is, produceert een behoeftedatum op een maandag een leveringsdatum op de voorgaande vrijdag, omdat zaterdag en zondag geen werkdagen zijn.

Welke kalender wordt gebruikt om de werkdagen te bepalen, is afhankelijk van de instelling en het type levering. Het kan worden beheerd door de kalenders van de behoefteplanningsgroep, het magazijn en de leverancier.

> [!NOTE]
> Als *magazijn* geen deel uitmaakt van de behoefteplanningsdimensie (planning is alleen gebaseerd op *locatie*), wordt de magazijnkalender niet gebruikt.

Het systeem kan een instelling verwerken waarbij een of meer kalenders worden gedefinieerd. In de volgende subsecties worden de mogelijke combinaties beschreven die kunnen worden gebruikt om het resultaat te bepalen.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kalender die wordt gebruikt voor de duur

De gedefinieerde kalenders bepalen de werkelijke totale doorlooptijd in kalenderdagen, van de orderdatum van de levering tot de behoeftedatum van de vraag. De volgende prioriteitstelling voor kalenders wordt gebruikt:

- **Inkoopdoorlooptijd**: er wordt alleen rekening gehouden met de kalender van de behoefteplanningsgroep.
- **Ontvangstmarge**: de kalender van de behoefteplanningsgroep wordt gebruikt als deze is gedefinieerd. Anders wordt de magazijnkalender gebruikt.
- **Uitgiftemarge**: de kalender van de behoefteplanningsgroep wordt gebruikt als deze is gedefinieerd. Anders wordt de magazijnkalender gebruikt.
- **Bestelmarge**: er wordt alleen rekening gehouden met de kalender van de behoefteplanningsgroep.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Kalender die wordt gebruikt voor de laatste datum

De volgende regels worden toegepast om te bepalen of de planningsengine een bepaalde datum voor een bepaald datumtype kan gebruiken:

- **Ontvangstdatum inkoop**: de leverancierskalender wordt gebruikt als deze is gedefinieerd. Anders wordt de kalender van de behoefteplanningsgroep gebruikt als deze is gedefinieerd. Als geen van deze kalenders is gedefinieerd, wordt de magazijnkalender gebruikt.
- **Ontvangstdatum transfer**: de kalender van de behoefteplanningsgroep wordt gebruikt als deze is gedefinieerd. Anders wordt de magazijnkalender gebruikt.
- **Productieontvangstdatum**: de kalender van de behoefteplanningsgroep wordt gebruikt als deze is gedefinieerd. Anders wordt de magazijnkalender gebruikt.
- **Openstaande dag vraaguitgifte**: de magazijnkalender wordt gebruikt als deze is gedefinieerd. Anders wordt de kalender van de behoefteplanningsgroep gebruikt.
- **Openstaande dag order**: er wordt een combinatie (snijpunt) van de kalender van de behoefteplanningsgroep en de leverancierskalender gebruikt. Beide kalenders moeten zijn geopend om de datum te kunnen gebruiken. Als slechts een van de kalenders is gedefinieerd, wordt alleen die kalender gebruikt.

#### <a name="calendar-setup-overview-matrix"></a>Matrix voor overzicht van kalenderinstellingen

De volgende afbeelding bevat een matrix waarin wordt samengevat welke kalenders van toepassing zijn wanneer veiligheidsmarges worden berekend. (Selecteer de afbeelding om een versie in hoge resolutie te openen.) De volgende afkortingen en kleuren worden gebruikt om aan te geven waar elk type kalender wordt opgegeven:

- **Behoefteplanningsgroep (CG):** groen
- **Magazijn (WH):** geel
- **Leverancier (V):** blauw

[![Matrix voor overzicht van kalenderinstellingen](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Vertragingen berekenen

Alle drie de typen veiligheidsmarges worden opgenomen wanneer het systeem bepaalt of een order is vertraagd.

Een artikel heeft bijvoorbeeld een doorlooptijd van één dag en een ontvangstmarge van drie dagen. Een verkooporder voor dit artikel is ingesteld als vandaag vereist. In dit geval wordt de vertraging berekend als *doorlooptijd* + *ontvangstmarge* = vier dagen. Als vandaag 14 augustus is, levert een vertraging van vier dagen dus een levering op 18 augustus op. In de volgende afbeelding ziet u dit voorbeeld.

![Voorbeeld van vertragingsberekening](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]