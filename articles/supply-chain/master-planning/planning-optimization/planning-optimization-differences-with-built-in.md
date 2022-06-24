---
title: Verschillen tussen ingebouwde hoofdplanning en Planningsoptimalisatie
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
ms.openlocfilehash: cf39166dce860dbd796cb4749175628252ed96ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897569"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Verschillen tussen ingebouwde hoofdplanning en Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

De resultaten van de Planningsoptimalisatie kunnen afwijken van de resultaten van de ingebouwde hoofdplannings-engine. De verschillen kunnen worden veroorzaakt door functies die in behandeling zijn. In dit artikel worden functies weergegeven die nog niet worden ondersteund door Planningsoptimalisatie en die niet worden weergegeven op de pagina **[Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)**.

| Functie | Huidig gedrag in planningsoptimalisatie |
|---|---|
| Catch weight-producten | Catch-weight-producten worden beschouwd als normale producten.|
| Uitbreidbare dimensies | Uitbreidbare dimensies zijn op geplande orders leeg, zelfs wanneer het selectievakje **Dekkingsplan volgens dimensie** is aangevinkt op de pagina **Opslagdimensiegroepen** of **Traceringsdimensiegroepen**. |
| Gefilterde productieruns | Raadpleeg [Productieplanning - filters](production-planning.md#filters) voor meer informatie. |
| Prognoseplanning | Prognoseplanning wordt niet ondersteund. Wij raden aan dat u hoofdplanning gebruikt waarbij een prognosemodel aan het hoofdplan is toegewezen. |
| Nummerreeksen voor geplande orders | Nummerreeksen voor geplande orders worden niet ondersteund. Geplande ordernummers worden aan de servicekant gegenereerd. Het geplande ordernummer wordt normaal gesproken weergegeven met 10 cijfers, maar de reeks wordt gebaseerd op 20 tekens, met 10 cijfers die zijn toegewezen voor de telling van de planningsuitvoering en de andere 10 cijfers voor de telling van geplande orders. |
| Plan kopiëren, plan verwijderen en planversie opschonen | <p>De volgende items zijn uitgeschakeld onder **Hoofdplanning \> Hoofdplanning \> Plannen onderhouden** in het deelvenster voor navigatie:</p><ul><li>Plan kopiëren</li><li>Plan verwijderen</li><li>Versie-opschoning plannen</li></ul> |
| Retourorders | Er wordt geen rekening gehouden met retourorders. |
| Aan planning gerelateerde functies | Raadpleeg [Plannen met onbeperkte capaciteit](infinite-capacity-planning.md#limitations) voor informatie. |
| Afhandeling van veiligheidsvoorraad | Voor planningsoptimalisatie wordt altijd de optie *Datum van vandaag + levertijd* gebruikt voor het veld **Minimum behalen** op de pagina **Artikelbehoefteplanning**. Dit helpt ongewenste geplande orders en andere problemen te voorkomen want als de aanschaffingstijd niet is opgenomen voor de veiligheidsvoorraad, worden geplande orders die zijn gemaakt voor de huidige lage voorhanden voorraad altijd vertraagd vanwege de levertijd. |
| Tracering van veiligheidsvoorraad en nettobehoeften | Het behoeftetyp *Veiligheidsvoorraad* wordt niet opgenomen en wordt niet weergegeven op de pagina **Nettobehoeften**. Veiligheidsvoorraad vertegenwoordigt geen vraag en er is geen behoeftedatum aan gekoppeld. In plaats daarvan stelt u een beperking in voor de voorraad die te allen tijde aanwezig moet zijn. Bij het berekenen van geplande orders tijdens de hoofdplanning wordt echter wel rekening gehouden met de waarde van het veld **Minimum**. We stellen voor dat u de kolom **Geaccumuleerde hoeveelheid** op de pagina **Nettobehoeften** controleert om te kijken of er rekening is gehouden met deze waarde. |
| Transportkalenders | De waarde in de kolom **Transportkalender** op de pagina **Leveringsmethoden** wordt genegeerd. |
| Min/max-behoefteplanningscode zonder waarden| Wanneer u met de ingebouwde planningsengine een min/max-behoefteplanningscode gebruikt waarbij geen minimum- of maximumwaarden zijn ingesteld, wordt de behoefteplanningscode door de planningsengine als een vereiste behandeld en wordt voor elke behoefte één order gemaakt. Bij Planningsoptimalisatie wordt één order per dag gebruikt om het volledige bedrag van die dag te dekken.  |
| Nettovereisten en handmatig gemaakte geplande orders | Met de ingebouwde planningsengine worden handmatig gemaakte aanvulorders voor een artikel automatisch weergegeven tussen de nettovereisten voor dat artikel. Wanneer u bijvoorbeeld een inkooporder maakt vanuit een verkooporder, wordt de inkooporder weergegeven op de pagina **Nettovereisten** zonder dat er voorafgaande acties nodig zijn. Dit komt doordat de ingebouwde planningsengine voorraadtransacties in de tabel `inventLogTTS` registreert en wijzigingen toont op de pagina **Nettovereisten** voor dynamische plannen. Met Planningsoptimalisatie worden handmatig gemaakte orders echter pas gemaakt vanuit de nettovereisten van een artikel wanneer Planningsoptimalisatie is uitgevoerd (met behulp van een plan dat het artikel bevat), of wanneer u in het Actievenster op de pagina **Nettovereisten** de optie **Bijwerken \> Hoofdplanning** selecteert. Meer informatie over hoe u werkt met de pagina **Nettovereisten** vindt u in [Nettovereisten en informatie over tracering van de behoefte met Planningsoptimalisatie](net-requirements.md). |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)
- [Parameters die niet worden gebruikt door Planningsoptimalisatie](not-used-parameters.md)
- [Datum- en tijdparameters die worden gebruikt door Planningsoptimalisatie](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
