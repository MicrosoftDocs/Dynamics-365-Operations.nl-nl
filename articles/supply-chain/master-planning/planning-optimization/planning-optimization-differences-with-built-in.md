---
title: Verschillen tussen Planningsoptimalisatie en de verouderde hoofdplanningsengine
description: In dit artikel worden functies weergegeven die nog niet worden ondersteund door Planningsoptimalisatie en die niet worden weergegeven op de pagina voor het aanpassen van de analyse aan Planningsoptimalisatie.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745356"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Verschillen tussen Planningsoptimalisatie en de verouderde hoofdplanningsengine

[!include [banner](../../includes/banner.md)]

De resultaten van Planningsoptimalisatie kunnen afwijken van de resultaten van de afgeschafte hoofdplanningsengine. De verschillen kunnen worden veroorzaakt door functies die in behandeling zijn. In dit artikel worden functies weergegeven die nog niet worden ondersteund door Planningsoptimalisatie en die niet worden weergegeven op de pagina **[Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)**.

| Functie | Huidig gedrag in planningsoptimalisatie |
|---|---|
| Catch weight-producten | Catch-weight-producten worden beschouwd als normale producten.|
| Uitbreidbare dimensies | Uitbreidbare dimensies worden niet ondersteund door Planningsoptimalisatie. Wanneer u Planningoptimalisatie gebruikt, zijn uitbreidbare dimensies op geplande orders leeg, zelfs wanneer het selectievakje **Dekkingsplan volgens dimensie** is aangevinkt op de pagina **Opslagdimensiegroepen** of **Traceringsdimensiegroepen**. |
| Gefilterde productieruns | Raadpleeg [Productieplanning - filters](production-planning.md#filters) voor meer informatie. |
| Prognoseplanning | Prognoseplanning wordt niet ondersteund. Wij raden aan dat u hoofdplanning gebruikt waarbij een prognosemodel aan het hoofdplan is toegewezen. |
| Nummerreeksen voor geplande orders | Nummerreeksen voor geplande orders worden niet ondersteund. Geplande ordernummers worden aan de servicekant gegenereerd. Het geplande ordernummer wordt normaal gesproken weergegeven met 10 cijfers, maar de reeks wordt gebaseerd op 20 tekens, met 10 cijfers die zijn toegewezen voor de telling van de planningsuitvoering en de andere 10 cijfers voor de telling van geplande orders. |
| Plan kopiëren, plan verwijderen en planversie opschonen | <p>De volgende items zijn uitgeschakeld onder **Hoofdplanning \> Hoofdplanning \> Plannen onderhouden** in het deelvenster voor navigatie:</p><ul><li>Plan kopiëren</li><li>Plan verwijderen</li><li>Versie-opschoning plannen</li></ul> |
| Retourorders | Er wordt geen rekening gehouden met retourorders. |
| Aan planning gerelateerde functies | Raadpleeg [Plannen met onbeperkte capaciteit](infinite-capacity-planning.md#limitations) voor informatie. |
| Afhandeling van veiligheidsvoorraad | Voor planningsoptimalisatie wordt altijd de optie *Datum van vandaag + levertijd* gebruikt voor het veld **Minimum behalen** op de pagina **Artikelbehoefteplanning**. Dit helpt ongewenste geplande orders en andere problemen te voorkomen want als de aanschaffingstijd niet is opgenomen voor de veiligheidsvoorraad, worden geplande orders die zijn gemaakt voor de huidige lage voorhanden voorraad altijd vertraagd vanwege de levertijd. |
| Tracering van veiligheidsvoorraad en nettobehoeften | Het behoeftetyp *Veiligheidsvoorraad* wordt niet opgenomen en wordt niet weergegeven op de pagina **Nettobehoeften**. Veiligheidsvoorraad vertegenwoordigt geen vraag en er is geen behoeftedatum aan gekoppeld. In plaats daarvan stelt u een beperking in voor de voorraad die te allen tijde aanwezig moet zijn. Bij het berekenen van geplande orders tijdens de hoofdplanning wordt echter wel rekening gehouden met de waarde van het veld **Minimum**. We stellen voor dat u de kolom **Geaccumuleerde hoeveelheid** op de pagina **Nettobehoeften** controleert om te kijken of er rekening is gehouden met deze waarde. Aangezien de tracering van de behoefte verschillend is, kunnen verschillende acties worden voorgesteld. |
| Transportkalenders | De waarde in de kolom **Transportkalender** op de pagina **Leveringsmethoden** wordt genegeerd. |
| Min/max-behoefteplanningscode zonder waarden| Wanneer u met de afgeschafte hoofdplanningsengine een min/max-behoefteplanningscode gebruikt waarbij geen minimum- of maximumwaarden zijn ingesteld, wordt de behoefteplanningscode door de planningsengine als een vereiste behandeld en wordt voor elke behoefte één order gemaakt. Bij Planningsoptimalisatie wordt één order per dag gebruikt om het volledige bedrag van die dag te dekken.  |
| Nettovereisten en handmatig gemaakte geplande orders | Met de afgeschafte hoofdplanningsengine worden handmatig gemaakte aanvulorders voor een artikel automatisch weergegeven tussen de nettovereisten voor dat artikel. Wanneer u bijvoorbeeld een inkooporder maakt vanuit een verkooporder, wordt de inkooporder weergegeven op de pagina **Nettovereisten** zonder dat er voorafgaande acties nodig zijn. Dit komt doordat de afgeschafte hoofdplanningsengine voorraadtransacties in de tabel `inventLogTTS` registreert en wijzigingen toont op de pagina **Nettovereisten** voor dynamische plannen. Met Planningsoptimalisatie worden handmatig gemaakte orders echter pas gemaakt vanuit de nettovereisten van een artikel wanneer Planningsoptimalisatie is uitgevoerd (met behulp van een plan dat het artikel bevat), of wanneer u in het Actievenster op de pagina **Nettovereisten** de optie **Bijwerken \> Hoofdplanning** selecteert. Meer informatie over hoe u werkt met de pagina **Nettovereisten** vindt u in [Nettovereisten en informatie over tracering van de behoefte](net-requirements.md). |
| Resourcetoewijzing | Wanneer er met onbeperkte capaciteit wordt gewerkt, worden door de afgeschafte hoofdplanningsengine alle geplande orders aan dezelfde resource toegewezen op een bepaalde resourcegroep. Zo wordt de optimalisatie van de planning verbeterd door willekeurig resources te selecteren, zodat verschillende productieorders gebruik kunnen maken van verschillende resources. Als u dezelfde resource wilt gebruiken voor alle geplande orders, moet u die resource in de route opgeven. |
| Uitgebreide-gegevenstypen | Planningsoptimalisatie biedt geen ondersteuning voor wijzigingen in de nauwkeurigheid van EDT's. Dit betekent dat dit proces niet officieel wordt ondersteund en de werking niet wordt gegarandeerd. |
| Afhandeling van veiligheidsvoorraad | Planningsoptimalisatie gebruikt altijd **Datum van vandaag + levertijd** voor *Minimum behalen*. Deze wijziging wordt doorgevoerd om een vereenvoudigde planningsinstelling in de toekomst voor te bereiden en om een actieresultaat te kunnen bieden. Als de aanschaffingstijd niet is opgenomen voor de veiligheidsvoorraad, worden geplande orders die zijn gemaakt voor de lage voorhanden voorraad altijd vertraagd vanwege de levertijd. Dit gedrag kan leiden tot belangrijke ruis en ongewenste geplande orders. De beste manier is om de instelling te wijzigen zodat *Datum van vandaag + levertijd* wordt gebruikt. Werk hoofdgegevens bij om waarschuwingen te voorkomen. |
| Statisch plan kopiëren naar dynamisch plan | Met Planningsoptimalisatie worden statische plannen niet naar dynamische plannen gekopieerd, ongeacht de instelling op de pagina **Parameters hoofdplanning**. Over het algemeen is deze bewerking minder relevant vanwege de snelheid en de volledige regeneratie die door Planningsoptimalisatie wordt geleverd. Als er twee of meer plannen worden gebruikt, moet de hoofdplanning worden geactiveerd voor elk plan. |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)
- [Parameters die niet worden gebruikt door Planningsoptimalisatie](not-used-parameters.md)
- [Datum- en tijdparameters die worden gebruikt door Planningsoptimalisatie](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
