---
title: Taakplanning
description: Dit artikel biedt informatie over taakplanning. Dit is een gedetailleerdere vorm van planning dan bewerkingsplanning. U kunt taakplanning gebruiken om afzonderlijke taken of winkelorders te plannen en om de productieomgeving te beheren.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8162797256e221192dc3e1a12aa145e28d5bc0f5
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="job-scheduling"></a>Taakplanning

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over taakplanning. Dit is een gedetailleerdere vorm van planning dan bewerkingsplanning. U kunt taakplanning gebruiken om afzonderlijke taken of winkelorders te plannen en om de productieomgeving te beheren.

U kunt taakplanning gebruiken om afzonderlijke taken of winkelorders te plannen en om de productieomgeving te beheren. Taakplanning verdeelt elke bewerking onder in de afzonderlijke taken. Deze taken worden vervolgens toegewezen de bronnen voor bedrijfsactiviteiten die deze zullen uitvoeren. Met taakplanning kunt u ook alle taken synchroniseren waarnaar wordt verwezen door de geselecteerde taak. U kunt een begindatum en -tijd en een einddatum en -tijd opgeven voor de taak en vervolgens de planning uitvoeren. De tijd die u hebt opgegeven kan de begintijd of eindtijd zijn, afhankelijk van de planningsrichting. Deze functionaliteit is bijvoorbeeld handig wanneer een taak enkel kan worden uitgevoerd op één machine tegelijk of wanneer u de uitgevoerde taak voor elke resource wilt optimaliseren.

## <a name="tasks-in-the-job-scheduling-process"></a>Taken tijdens het taakplanningsproces
Het taakplanningsproces omvat de volgende taken:

-   Bewerkingen opsplitsen in taken.
-   Taken plannen op basis van de datums en tijden voor de resources die zijn opgegeven voor de bijbehorende bewerking.
-   Begintijd en eindtijd berekenen voor elke taak. Met eindige capaciteit kunt u ervoor zorgen dat er geen overlappende tijden zijn.
-   Bepalen met welke resources in de resourcegroep de taak wordt uitgevoerd. Voor deze taak moet een resourcegroep worden opgegeven voor een bewerking. Taakplanning selecteert de resources of resourcegroepen op basis van de kortste levertijd en houdt ook rekening met alle vorige reserveringen op de resources.
-   Bewerkingen in taken exploderen wanneer u taakplanning uitvoert. De taken worden gepland op datum en tijd, afhankelijk van de volgorde die is opgegeven in de productieroute. De instellingen van de bewerking bepalen de taken die worden geëxplodeerd tijdens het planningsproces. De routegroep die is toegewezen aan de bewerking, bepaalt of taken worden gegenereerd. Een taak wordt alleen gegenereerd als deze een bepaalde duur heeft. Een transporttijdtaak wordt bijvoorbeeld gegenereerd als er een transporttijd is opgegeven voor de geselecteerde bewerking.

## <a name="scheduling-direction"></a>Planningsrichting
U kunt taken voorwaarts of achterwaarts plannen.

-   **Voorwaarts** – Gebruik de planningsmethode voorwaarts om de productie zo vroeg mogelijk te starten. Dit wordt ook wel de pushmethode genoemd, omdat de productie doorheen het productieproces wordt gedreven. De begin- en einddata van de productie worden zo vroeg mogelijk gepland.
-   **Achterwaarts** – Gebruik de planningsmethode achterwaarts om de productie zo laat mogelijk te starten. Dit wordt ook wel de pullmethode genoemd, omdat deze wordt gestuurd door de datum waarop de productie voltooid moet zijn. Achterwaartse planning telt achterwaarts naar de laatst mogelijke datum dat de productie kan worden begonnen zonder de gestelde deadline te missen.

## <a name="finite-capacity"></a>Eindige capaciteit
U kunt taken ook plannen met behulp van eindige capaciteit. Wanneer u met een eindige capaciteit werkt, mag de capaciteit die is gepland niet groter zijn dan de capaciteit die beschikbaar is voor de resource. De beschikbare tijd wordt gedefinieerd als het interval wanneer de resource beschikbaar is en er geen andere reserveringen van capaciteit voorkomen. Door te plannen met beperkte capaciteit wordt gegarandeerd dat de begin- en eindtijd van een bewerking op een specifieke datum elkaar niet overlappen. Er wordt ook rekening gehouden met resourcecapaciteit die al gereserveerd is evenals overlappingen tussen de begin- en eindtijden. Eindige capaciteit bepaalt de hoeveelheid capaciteit die voor een resource beschikbaar moet zijn om optimaal gebruik van die resource te bereiken. Deze bepaling wordt afgewogen tegen een berekening van de kortste mogelijke doorlooptijd tussen bewerkingen.

## <a name="finite-materials"></a>Beperkt materiaal
In de taakplanning met beperkte materialen wordt gegarandeerd dat de benodigde materialen bij het starten van de bewerking beschikbaar zijn. De regels van de dekking voor items definiëren deze limieten. Planning gebruikt behoefte-explosie om te bepalen wanneer de componentartikelen beschikbaar zijn. Als u een planning maakt zonder beperkte materialen in te stellen, neemt het systeem aan dat alle artikelen beschikbaar zijn zodra deze nodig zijn.

## <a name="finite-properties"></a>Eigenschappen beperkingen
In de taakplanning met speciale eigenschappen moeten eigenschappen worden opgegeven voor de bewerkingen van de productieroute. Er wordt alleen capaciteit gereserveerd als deze eigenschappen van toepassing zijn.

## <a name="references"></a>Verwijzingen
In de taakplanning worden alle producties gepland die aan de huidige productie zijn gekoppeld. Als een productie een of meer subproducties heeft, moeten de subproducties tegelijk met de hoofdproductie worden gepland, omdat de hoofdproductie pas kan worden gestart nadat de subproducties zijn voltooid.

## <a name="schedule-resources"></a>Resources plannen
De planningsengine controleert combinaties van resources om na te gaan of deze combinaties voldoen aan de vereisten. U kunt selectiecriteria opgeven door een van de volgende waarden te selecteren in het veld **Selectie van primaire resource** op de pagina **Planningsparameters**:

-   **Duur** - De planningsengine kiest de resource met de kortste doorlooptijd. **Opmerking:** Plannen op duur kan ervoor zorgen dat de prestaties minder zijn als dezelfde resourcegroep veel resources bevat en secundaire bewerkingen worden gebruikt. Er kunnen maximaal 32 resources worden ingepland per bewerking. Als u meer resources inplant, wordt een infologboek weergegeven en wordt bij de taakplanning niet de beste alternatieve resource gevonden.
-   **Prioriteit** – De planningsengine kiest de resource met de hoogste prioriteit als er twee of meer resources zijn met identieke mogelijkheden en niveaus. De bron met de laagste numerieke waarde in dit veld heeft de hoogste prioriteit.

Wanneer u taakplanning uitvoert, plant het systeem de resources op basis van de beperkingen die u in de resourceparameters definieert. De capaciteit van resources kunt u bepalen met behulp van de agenda-instellingen. Het systeem rekent de belasting voor resources tijdens het planningsproces. **Opmerking:** Voor producties waarvoor de bewerkingsplanningsfunctie wordt gebruikt, kunt u de taakplanning uitvoeren na de bewerkingsplanning. Als u de bewerkingsplanning niet gebruikt, kunt u de taakplanning afzonderlijk uitvoeren.

## <a name="maximum-capacities-for-resources-per-job-order"></a>De maximumcapaciteit van resources per taakorder
Tijdens het taakplanningsproces worden taken aan resources toegewezen. U kunt de maximumcapaciteit van resources per taakorder vaststellen. U kunt het systeem bijvoorbeeld instellen met de beperking dat er niet meer dan 50% van de totale capaciteit mag worden gepland voor een productieorder. Deze instellingen bieden u meer controle over het plannen van resources op niveau van de taak. Dit helpt problemen te voorkomen als er niet voldoende capaciteit beschikbaar is om gelijktijdige producties uit te voeren.

## <a name="resource-efficiency"></a>Efficiëntie van resources
In de taakplanning wordt ook gebruikgemaakt van de efficiëntiepercentages die voor de resources zijn opgegeven. Met efficiëntiepercentages neemt de tijd toe of af die voor de resource is gereserveerd. Als gevolg daarvan neemt ook de doorlooptijd toe of af. De volgende formule wordt gebruikt voor de berekening: Planningstijd = Tijd × 100 ÷ Efficiëntiepercentage. In deze formule omvat *Tijd* zowel de uitvoerings- als insteltijd.




