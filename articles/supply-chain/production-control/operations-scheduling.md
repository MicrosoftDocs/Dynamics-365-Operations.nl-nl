---
title: Bewerkingsplanning
description: Dit onderwerp bevat informatie over de planning van bewerkingen. U kunt het plannen van bewerkingen gebruiken om een algemene schatting te geven voor de duur van het productieproces.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e95374e0aebca825f589f13eda389d6612737181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425509"
---
# <a name="operations-scheduling"></a>Bewerkingsplanning

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over de planning van bewerkingen. U kunt het plannen van bewerkingen gebruiken om een algemene schatting te geven voor de duur van het productieproces.

U kunt de productie op het niveau van de bewerking en het taakniveau plannen. In tegenstelling tot het plannen van taken worden bij het plannen van bewerkingen de bewerkingen voor de productieroute niet in taken opgesplitst. Indien u meer details in de planning op wilt nemen, zoals informatie over de huidige capaciteit, kunt u na het plannen van de bewerkingen een taakplanning uitvoeren. U kunt ook alleen een taakplanning uitvoeren. De taakplanning wordt meestal gebruikt voor het plannen van afzonderlijke taken op de werkvloer voor een onmiddellijke of een korte periode.

## <a name="components-of-operations-scheduling"></a>Onderdelen van bewerkingsplanning
De hoofdonderdelen van de bewerkingsplanning zijn de planningsrichting, de broncapaciteit en materiaaloptimalisatie. Met bewerkingsplanning kunt u de volgende doelen bereiken:

-   De planningsmethode beheren door vanaf een bepaalde datum vooruit of terug te plannen.
-   Het gebruik van bronnen optimaliseren door het plannen van producties op basis van de broncapaciteit. Deze aanpak helpt ook bij het identificeren van het moment waarop alternatieve bronnen moeten worden gebruikt.
-   Het gebruik van materiaal optimaliseren door het plannen van producties op basis van de beschikbaarheid van het benodigde materiaal.
-   Referentieproducties plannen en synchroniseren. De datums van de referentieproducties worden aangepast wanneer wijzigingen worden aangebracht in de planning van de productieorder.

U moet de kosten van een productieorder ramen voordat u de planning van de bewerkingen kunt uitvoeren. Als u geen raming hebt uitgevoerd, wordt deze automatisch uitgevoerd voordat de bewerkingsplanning wordt gestart. Een bewerkingsplanning bevat de volgende gegevens:

-   Het product dat voor productie is gepland
-   De configuratie van het product
-   De hoeveelheden die bij de productie betrokken zijn
-   De datums waarop de productie start en eindigt
-   De capaciteitsreserveringen voor de bronnen die de productieactiviteiten uitvoeren

De insteltijd, verwerkingstijd en uitvoeringstijd worden ingesteld voor bewerkingen in de productie. Nadat u de planning van bewerkingen uitvoert, wordt de status van de productieorder **Gepland** en worden alle bewerkingen gepland in de volgorde die in de productieroute is opgegeven. Echter, wordt alleen de duur van de bewerking beschouwd. Begin- en eindtijden worden niet gepland.

## <a name="scheduling-direction-and-date"></a>Richting en datum van planning
De planningsrichting is cruciaal voor het planningsproces. De productie kan vanaf elke datum voorwaarts of achterwaarts worden gepland, afhankelijk van de tijd- en planningsvereisten.

-   **Voorwaarts vanaf de planningsdatum**: u kunt productie zo plannen dat deze zo vroeg mogelijk begint. Er kan vandaag, morgen of op een willekeurige datum in de toekomst met productie worden begonnen. De productie wordt vooruit in de tijd gepland naar de vroegst mogelijke einddatum.
-   **Achterwaarts vanaf de planningsdatum**: u kunt productie zo plannen dat deze zo laat mogelijk begint. Achterwaartse planning is gebaseerd op de datum waarop de productie voltooid moet zijn. De planning telt vanaf die datum terug naar de laatst mogelijke datum waarop de productie kan worden gestart en nog steeds op tijd voltooid kan worden.

## <a name="resource-scheduling"></a>Resourceplanning
Wanneer u een bewerkingsplanning uitvoert, wordt elke bewerking in de productieroute gepland voor de bron die voor de bewerking is opgegeven. Bovendien wordt de duur van elke bewerking opgegeven op de productieroute. Indien een brongroep voor een bewerking is opgegeven, reserveert de planning capaciteit op de groep. Echter, in tegenstelling tot taakplanning, worden er bij de planning van bewerkingen geen specifieke bronnen in de groep geselecteerd. Indien u met een beperkte capaciteit werkt, hangt de planning af van de beschikbaarheid van de bronnen die nodig zijn om de productie te voltooien. Bij bewerkingsplanning wordt de volgorde van de bewerkingen gevolgd die op de productieroute is opgenomen. De planning reserveert capaciteit op de brongroepen op basis van de bewerkingstijden die op de productieroute zijn gedefinieerd. Het totaal van beschikbare capaciteit op de betrokken bronnen bepaalt de capaciteit voor de brongroep. Capaciteitsreserveringen die al voor de bronnen bestaan worden beschouwd als capaciteit die niet beschikbaar is. Indien de beschikbare capaciteit ontoereikend is voor de productie, kunnen de productieorders worden uitgesteld of zelfs gestopt. U kunt ook de efficiëntie opgeven die u verwacht van de bronnen die bij de productie betrokken zijn. U geeft de efficiëntie op als een percentage van de bron. Het efficiëntiepercentage past de doorvoer van de bron aan. Deze correctie heeft invloed op de tijd die wordt gereserveerd voor de bron. De doorlooptijden voor de bewerkingen die de bron gebruiken worden overeenkomstig aangepast.

## <a name="operations-scheduling-and-master-planning"></a>Bewerkingsplanning en hoofdplanning
De bewerkingsplanning vormt ook de basis voor de hoofdplanning, waardoor berekeningen voor materiaalbehoeften worden bepaald. Bij bewerkingsplanning wordt het volgende informatie in overweging genomen:

-   **Reserveproducten** – Producten die zijn gepland, vrijgegeven of gestart
-   **Materiaalbeschikbaarheid**: voorraad, subproductie en leveranciers
-   **Capaciteitsbeschikbaarheid** – Bronnen die voor de productie vereist zijn

> [!NOTE]
> Als u een hoofdplanning met meerdere threads en bewerkingsplanning gebruikt, wordt er geen rekening gehouden met eindige capaciteit. 

## <a name="cancellations"></a>Annuleringen
Wanneer u de planning van bewerkingen uitvoert, kunt u specifieke onderdelen van het bewerkingsplan annuleren. Deze onderdelen omvatten de wachttijd, insteltijd, verwerkingstijd, overlappingstijd en vervoerstijden.

## <a name="finite-materials"></a>Beperkt materiaal
Indien u met beperkt materiaal werkt, hangt de planning ook af van de beschikbaarheid van de materialen die nodig zijn voor de productie. Als er onvoldoende beschikbare onderdelen zijn voor de productie, kan de productie vertraagd worden. U kunt de planning baseren op het gebruik van materialen door de materialen te specificeren die voor de productie beschikbaar moeten zijn. Wanneer u zowel de broncapaciteit als de beschikbaarheid van materialen optimaliseert, wordt de productie berekend volgens deze beperkingen. Een productieorder kan pas ingepland worden om te starten als de capaciteit en de materialen op hetzelfde moment en in de benodigde hoeveelheden beschikbaar zijn.

<a name="additional-resources"></a>Aanvullende resources
--------

[Opties voor het plannen van bewerkingen](operation-scheduling-options.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]