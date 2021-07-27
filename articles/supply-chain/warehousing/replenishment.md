---
title: Overzicht van Aanvulling
description: Dit onderwerp beschrijft de aanvullingsstrategieën die beschikbaar zijn voor magazijnen die gebruikmaken van de functionaliteit die beschikbaar is in Magazijnbeheer.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "90043"
- intro-internal
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e381af433eb3041d92ddfe375e6b4c75c1feb7c2
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335815"
---
# <a name="replenishment-overview"></a>Overzicht van Aanvulling

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft de aanvullingsstrategieën die beschikbaar zijn voor magazijnen die gebruikmaken van de functionaliteit die beschikbaar is in Magazijnbeheer. De informatie in dit onderwerp is niet van toepassing op de magazijnoplossing die in Voorraadbeheer beschikbaar is.

De volgende aanvullingsstrategieën zijn beschikbaar:

- **Aanvulling voor wave-vraag** – Deze strategie maakt aanvullingswerk voor uitgaande orders of ladingen als geen voorraad beschikbaar is wanneer werk wordt gemaakt door de wave. Zo kan bijvoorbeeld aanvullingswerk worden gemaakt als de hoeveelheid die is vereist voor een verkooporder niet beschikbaar is wanneer een wave wordt verwerkt.
- **Min./max. aanvulling** – Deze strategie gebruikt minimum- en maximumopslaglimieten om te bepalen wanneer locaties moeten worden aangevuld. De artikel- en locatiecriteria definiëren de voorraad die voor aanvulling wordt beoordeeld. Sjablonen voor Min/Max aanvulling zijn het belangrijkste mechanisme voor het onderhouden van optimale niveaus op orderverzamellocaties. Om te garanderen dat voldoende voorraad voor orderverzamelen beschikbaar is om te voldoen aan wave-vraag, kunt u vraagaanvulling gebruiken als aanvulling tussen cycli voor Min/Max aanvulling.
- **Vraag voor aanvulling laden** – Bij deze strategie wordt de vraag voor verschillende ladingen opgeteld en wordt het aanvullingswerk gemaakt dat is vereist om de relevante orderverzamellocaties te bevoorraden. Deze strategie helpt te garanderen dat de ladingen die zijn gemaakt kunnen worden verzameld in het magazijn nadat ze zijn vrijgegeven.
- **Directe aanvulling**: met deze strategie wordt voorraad aangevuld vóór het uitvoeren van een wave als toewijzing mislukt voor een locatie-instructieregel met een aanvullingssjabloon. 

Alle vier de strategieën maken aanvullingswerk, op basis van een sjabloon voor aanvulling.

## <a name="wave-demand-replenishment"></a>Aanvulling voor wave-vraag
Bij aanvulling voor wave-vraag wordt aanvullingswerk gemaakt op basis van de vraag als de vereiste hoeveelheid voor productieorders, kanbans, uitgaande orders of ladingen niet beschikbaar is wanneer een wave werk maakt. De aanvullingssjabloon bevat informatie over de artikelcriteria, de maateenheid, de toename van de vraag en de locatie. 

Locatie-instructies worden gebruikt om te bepalen welke locatie moet worden aangevuld. U koppelt deze locatie-instructies aan de aanvullingssjabloon met behulp van het veld **Instructiecode**. Als het veld **Instructiecode** niet is ingesteld, worden query's gebruikt om te bepalen welke locatie-instructie moet worden gebruikt. Houd er rekening mee dat als geen instructiecode is opgegeven in de aanvullingssjabloon en de locatie-instructie een instructiecode heeft, wordt de locatie-instructie genegeerd, zelfs als de query op de locatie-instructie correct is. Locatie-instructies voor orderverzamelen worden gebruikt om te bepalen waar u voorraad voor de aanvulling vandaan moet halen. 

Naast een sjabloon maken, moet u enkele aanvullingsinstellingen opgeven in de wave-sjabloon. De wave-sjabloon moet een wave-stap voor aanvulling bevatten die alleen wordt uitgevoerd als toewijzing van een artikel mislukt. Deze wave-stap voor aanvulling gebruikt een wave-stapcode om te bepalen welke aanvullingssjabloon moet worden gebruikt. U moet niet alleen een wave-stap voor aanvulling instellen, maar ook zorgen dat **Aanvullen** is geselecteerd in de sectie **Methoden** van de wave-sjabloon. 

De pagina **Aanvullingssjabloon** bevat een selectievakje **Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan**. Schakel dit selectievakje in als u vraagaanvulling wilt toestaan om niet-gereserveerde hoeveelheden van werk af te trekken van werk dat is gegenereerd op basis van de geselecteerde aanvullingssjabloon. Als u sjablonen voor vraagaanvulling in staat wilt stellen om deze logica te gebruiken, moet u dit selectievakje inschakelen voor elke bestaande aanvullingssjabloon. Wanneer de vraagaanvulling in het magazijn wordt geactiveerd, wordt de vraag afgetrokken van het bestaande aanvullingswerk dat niet-gereserveerde hoeveelheden heeft, als het werk afkomstig is uit aanvullingssjablonen waarbij het selectievakje **Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan** is ingeschakeld.

**Aanvullingseenheid** is de minimum eenheid voor aanvullen. Dit moet een geheel getal zijn dat een veelvoud is van de eenheid. Het systeem voert een afronding uit naar de hoogste eenheid die mogelijk is bij het maken van werk.

Vraagaanvulling wordt ondersteund voor verkooporders, overboekingsorders, productieorders en kanbans. 

## <a name="minmax-replenishment"></a>Min/Max aanvulling
In Min/Max aanvulling wordt voorraad aangevuld zodat deze tussen de minimale en maximale limieten blijft die zijn ingesteld. Dit proces gebeurt meestal eenmaal per dag om te garanderen dat alle orderverzamellocaties tot het maximumniveau zijn gevuld voordat het orderverzamelen van start gaat. 

De minimale en maximale hoeveelheden worden ingesteld in een aanvullingssjabloon. Veel van de andere instellingen in de sjabloon lijken op de instellingen in sjablonen die worden gebruikt in Aanvulling voor wave-vraag. De e sjabloon moet een regel bevatten voor elk artikel en elke locatie. Wanneer u aanvulling uitvoert door de batchtaak te gebruiken, controleert het systeem of aanvulling is vereist bij gebruik van de volgorde waarin de regels zijn ingedeeld. 

Houd er rekening mee dat met de strategie van Min/Max-aanvulling geen lege locatie kan worden aangevuld tenzij de locatie is ingesteld als de vaste locatie voor het artikel. Als de locatie die moet worden aangevuld geen vaste locatie is, kan het systeem niet bepalen welk artikel moet worden aangevuld. Daarom is ten minste enige voorhanden voorraad vereist voordat aanvulling plaatsvindt.

## <a name="load-demand-replenishment"></a>Vraag voor aanvulling laden
Bij Vraag voor aanvulling laden wordt de vraag voor verschillende ladingen opgeteld en wordt het aanvullingswerk gemaakt dat is vereist om de relevante orderverzamellocaties te bevoorraden. Vraag voor aanvulling laden lijkt in veel opzichten op Aanvulling voor wave-vraag. Het belangrijkste verschil is hoe en wanneer Vraag voor aanvulling laden en Aanvulling voor wave-vraag worden uitgevoerd. Net als bij Min/Max-aanvulling, wordt Vraag voor aanvulling laden uitgevoerd met behulp van een batchtaak. Voor het instellen van de batchtaak selecteert u de te gebruiken aanvullingssjabloon op de pagina **Vraag voor aanvulling laden** en stelt u een filterquery in om op te geven welke ladingen worden gebruikt voor het bepalen van de vraag. De locatiequery definieert de locaties waarvan eventuele beschikbare hoeveelheden worden afgetrokken om te voldoen aan de geaggregeerde vraag van de ladingen.

## <a name="immediate-replenishment"></a>Directe aanvulling
In plaats van het totaal van de vraag aan het einde van een toewijzingsproces te bepalen en aan te vullen op basis van de getotaliseerde hoeveelheid, kunt u de strategie Directe aanvulling toepassen. Wanneer u deze strategie gebruikt, kan de voorraad worden aangevuld zodra een locatie-instructieregel mislukt. U kunt de aanvulling dus zo instellen dat deze wordt beperkt door bepaalde eenheden en dat wordt gebruikgemaakt van hoeveelheden die zijn ingesteld voor specifieke locaties.

## <a name="replenishment-prerequisites"></a>Vereisten voor aanvulling

|      Vereiste       |                                                                                                                                Omschrijving                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Artikel           |                                                                                                        Het artikel moet ingeschakeld zijn voor magazijnbeheer processen                                                                                                        |
|        Magazijn        | Het magazijn moet ingeschakeld zijn voor magazijnbeheer processen. Om een magazijn in te schakelen voor magazijnbeheerprocessen, selecteert u het magazijn op de pagina <strong>Magazijnen</strong> en selecteert u vervolgens de optie <strong>Magazijnbeheerprocessen gebruiken</strong>. |
| Aanvullingssjablonen |                                                                   Er moet ten minste één aanvullingssjabloon worden ingesteld voor Min/Max aanvulling, Aanvulling voor wave-vraag of Vraag voor aanvulling laden.                                                                   |
|        Locaties        |                                                                                                       Locaties worden gemaakt en verbonden met een locatieprofiel.                                                                                                       |
|    Locatieprofielen    |                                                                                                        Locatieprofielen zijn vereist om locaties te maken.                                                                                                        |
|   Instructielocatie   |                                                       Locatie-instructies zijn vereist om het werk naar de locaties te leiden waar de aanvulling vereist is en naar de locaties waaruit voorraad afkomstig is.                                                        |
|     Werksjablonen      |                                                   Werksjablonen van het type <strong>Aanvulling</strong> zijn vereist voor het maken van aanvullingswerk zodat de voorraad kan worden verplaatst naar de gewenste locaties.                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]