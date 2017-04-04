---
title: Op basis van een activiteit uitbesteding
description: Dit onderwerp wordt beschreven, gedetailleerd, het gebruik van uitbestede activiteiten in een productiestroom voor lean manufacturing.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Op basis van een activiteit uitbesteding

Dit onderwerp wordt beschreven, gedetailleerd, het gebruik van uitbestede activiteiten in een productiestroom voor lean manufacturing.

In Microsoft Dynamics 365 voor bewerkingen, worden twee methoden voor uitbesteding: productieorders en lean manufacturing. In de lean manufacturing-methode, wordt de uitbesteding werkzaamheden gemodelleerd als een service die is gerelateerd aan een activiteit van een productiestroom. Een speciaal soort kostengroeptype met de naam **directe uitbesteding** is geïntroduceerd, en de uitbestede services zijn niet langer deel uitmaakt van een stuklijst (BOM). De kostprijsboekhouding van uitbesteed werk is volledig geïntegreerd in de kostprijsberekening voor lean manufacturing-oplossing.

## <a name="production-flows-that-involve-subcontractors"></a>Productiestromen die betrekking hebben op toeleveranciers
Het algemene principe van een productiestroom verandert niet wanneer de activiteiten zijn uitbesteed. Materiaal loopt nog steeds tussen vestigingen, procesactiviteiten materiaal converteren naar producten en overbrengactiviteiten materiaal of producten van de ene locatie naar de andere verplaatsen. U kunt modelleren van locaties en werkcellen als de leverancier wordt beheerd door de leveranciersrekening naar een magazijn of aan een bron van een resourcegroep toewijzen.  

Op basis van deze mogelijkheden, nodig lean manufacturing eventuele specifieke functies ter ondersteuning van de stroom van materialen en producten. Alle mogelijke scenario's die betrekking hebben op leveranciers zoals productie- of dienstverleners kunnen worden gemodelleerd op basis van de architectuur van de productiestroom wordt gelijkgetrokken en activiteiten.  

Een toeleverancier werkt bijvoorbeeld uit een supermarkt dat zich op de toeleverancier. Wanneer materiaalverwerkingseenheden bij de toeleverancier leeggemaakt worden, worden de kanbankaarten teruggestuurd naar de cel assembly samen met de volgende verzending. De supermarkt op de toeleverancier wordt vervolgens aangevuld. De overboekingen naar en van de toeleverancier kunnen worden gemodelleerd als expliciete overbrengactiviteiten ter ondersteuning van een orderverzamellijst en het verzendproces. Als een expliciete registratie is niet vereist voor de ondersteuning van het fysieke transport, kunnen de overbrengactiviteiten worden weggelaten.  

Een toeleverancier kan worden gebruikt voor het verdelen van de totale capaciteit van de productiestroom. Bijvoorbeeld: een productiestroom wordt gemodelleerd met behulp van geplande kanbanregels. De planner gebruikt de planning van de Raad om te plannen en laadniveau kanban beide werkcellen op aanvraag. De planner houdt ook toezicht op de geconsolideerde aanbod planning voor de supermarkt op de **aanbodschema** pagina. Meerdere toeleveranciers kunnen worden gemodelleerd in een of meerdere productiestromen en kunnen er meerdere kanbanregels die kunnen worden gebruikt voor het leveren van hetzelfde product op dezelfde locatie via verschillende activiteiten. De planner kunt kanbans converteren naar een alternatieve kanbanregel te plannen van een kanban die oorspronkelijk is gemaakt voor de interne productie aan een andere proces. De uitbestede aard van de werkcel heeft echter geen gevolgen voor de productiestroom. Hetzelfde geldt werken voor twee parallelle interne werkcellen of voor twee uitbestede cellen.   

Net als elke andere activiteit in een productiestroom uitbestede activiteiten kunnen verbruiken en leveren geïnventariseerde, niet-voorraadartikelen (onderhanden werk \[OHW\]), en half afgewerkte materiaal en producten. In alle gevallen zijn de processen voor het plannen en uitvoeren van uitbestede activiteiten hetzelfde. Bovendien kunnen verwerken deze hetzelfde als de processen voor het interne werkzaamheden.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Inkoopproces voor uitbestede activiteiten (services)
Het inkoopproces voor uitbestede activiteiten is gebaseerd op de fysieke materiaalstroom die is geregistreerd door de kanban taak uitgevoerd, bijvoorbeeld, starten of voltooien. Inkoopbeheer, bijvoorbeeld kosten van uitbesteed werk is een secundaire stroming die volgt op de fysieke stroom. Op het moment is het inkoopproces een onafhankelijke proces waarmee de handmatige correctie van de inkoopdocumenten bij elke stap. Hier wordt het inkoopproces voor uitbestede activiteiten:

1.  Een inkoopovereenkomst maken. De inkoopovereenkomst wordt gemaakt voor de service en gekoppeld aan de activiteit van de productiestroom.
2.  Inkooporder maken. Een vrijgaveorder voor inkoop kan worden gemaakt voor de service wordt op basis van de geplande kanbantaken. Taken voor dezelfde service kunnen worden gegroepeerd inkooporderregels per dag, week of maand. De inkooporderregels kunnen worden gemaakt op elk gewenst moment nadat de kanbantaken zijn gemaakt. Inkooporderregels kunnen zelfs worden gemaakt na het feit. Deze optie is meestal ingeschakeld als een toeleverancier zonder nadere kennisgeving verzorgt, op basis van de kanbans of kanban kaarten waarop de toeleverancier. In dit geval de afwijkingen tussen de inkooporder en de factuur kunnen worden geminimaliseerd.
3.  Genereren kanbankaarten, materiaal en een orderverzamellijst verzenden naar de toeleverancier om voor te bereiden voor verwerking. De voorbereiding wordt op basis van de gedetailleerde modellering van de productiestroom, uitgevoerd op het kanbanbord voor verwerkingsactiviteiten met behulp van de orderverzamellijst en de functie voorbereiden. U kunt ook wordt de voorbereiding op het kanbanbord voor overboekingstaken uitgevoerd met behulp van de orderverzamellijst en begin- of. Voor geïnventariseerde materiaal kunnen beide processen worden ondersteund door een WMS-orderverzameling en het verzendproces. Een vrachtbrief kunnen op verzoek worden gemaakt.
4.  Kanban materiaalverwerkingseenheden en kanbankaarten genereren. Na verwerking, worden bij de toeleverancier kaarten geretourneerd. De kaarten bevatten gewoonlijk een afleveringsbewijs waarmee het fysieke materiaal dat is verzonden. Een verwijzing naar de opgegeven services is niet vereist. De ontvangst van het materiaal of het product bij de klant is geregistreerd op het kanbanbord, afhankelijk van de kanbankaarten. (Het kanbanbord voor procesactiviteiten of het kanbanbord voor overboekingstaken wordt gebruikt, afhankelijk van de opgestelde activiteiten.).
5.  Maak een ontvangstbewijs advies. De ontvangst advies kan worden gebruikt voor het vervangen van een pakbon slip-document voor de ontvangen services. Aanbevelingen op ontvangst kunnen worden gegenereerd op basis van de voltooide kanbantaken voor de uitbesteding activiteit voor een geselecteerde periode. Aanbevelingen worden voor elke ontvangst taak gemaakt voor de verwante inkooporderregel. De ontvangst advies kan worden afgedrukt en verzonden naar de toeleverancier als bevestiging van ontvangst.
6.  Een factuur genereren.

Het proces wordt beëindigd wanneer de toeleverancier voor een periode wordt gefactureerd. De factuur overeenkomst wordt uitgevoerd voor de ontvangst aanbevelingen die zijn gemaakt. Omdat de ontvangst aanbevelingen de exacte fysieke ontvangst van materiaal voorstellen, wordt de drieweg-overeenstemming vereenvoudigd.

## <a name="configuring-activities-for-subcontracting"></a>Activiteiten voor uitbesteding configureren
De volgende secties beschrijven het configureren van activiteiten voor uitbesteding.

### <a name="subcontracted-services"></a>Uitbestede services

Het artikel betaling die wordt gebruikt in uitbesteding op basis van een activiteit moet een product met de volgende eigenschappen:

-   **producttype:** Service
-   **Voorraadmodelgroep:** niet opgeslagen

Deze vereiste zorgt ervoor dat het gebruik van de eerste in de eerste out (FIFO)-voorraadmodel gebruikt. **opmerking:** kostprijsberekening van de producten is vereist dat de standaardkosten van de service worden gedefinieerd. Een inkoopovereenkomst met de leverancier is vereist. Anders wordt kan niet de service worden gebruikt voor uitbestede activiteit is gebaseerd.

### <a name="subcontracted-process-activities"></a>Uitbestede procesactiviteiten

Als u wilt een procesactiviteit configureren als een uitbestede activiteit, de volgende stappen uit.

1.  Een uitbestede werkcel configureren. Als u wilt een werkcel configureren zoals uitbesteed, moet u een bron van de **leverancier** typt en koppelen aan de werkcel (resourcegroep). Een kostencategorie voor uitvoeringstijd van de **directe uitbesteding** kostengroeptype moet worden toegewezen aan de werkcel. De kostencategorieën voor instelling en de hoeveelheid niet verplicht.
2.  Nadat een procesactiviteit gemaakt en betrekking hebben op een cel uitbesteed werk, moet u een service voor de activiteit configureren voordat de productiestroomversie kan worden geactiveerd. U deze stap uitvoert op de **activiteit****details** pagina. Voor activiteiten die gekoppeld aan een cel uitbesteed werk zijn de **Service voorwaarden** sneltabblad wordt weergegeven. Op dit sneltabblad toevoegen een standaardservice die geldig is voor alle artikelen voor uitvoer. Als de uitvoer van bepaalde artikelen vereisen verschillende services of andere service berekeningsparameters (bijvoorbeeld de verhouding van een andere service), kunt u andere services toevoegen aan de activiteit.

## <a name="subcontracted-transfer-activities"></a>Uitbestede overboekingsactiviteiten
Een overbrengactiviteit is geconfigureerd als een uitbestede activiteit, afhankelijk van de **Bevracht door** instellen van de activiteit overboeken. De volgende opties zijn beschikbaar:

-   **Verzender** : de activiteit is uitbesteed als de overdracht van het magazijn wordt beheerd door een leverancier (zoals gedefinieerd door een eigenschap van het magazijn). Alle geselecteerde inkoopovereenkomsten bestaan voor services moeten dezelfde leverancier-ID hebben als het magazijn.
-   **Ontvanger** : de activiteit is uitbesteed als de overboeking naar het magazijn wordt beheerd door een leverancier (zoals gedefinieerd door een eigenschap van het magazijn). Alle geselecteerde inkoopovereenkomsten bestaan voor services moeten dezelfde leverancier-ID hebben als het magazijn.
-   **Vervoerder** : de activiteit is uitbesteed aan een leverancier die de service verzorgt. Geldig een vervoerder moet worden gemaakt voor magazijnbeheer en moet een account toegewezen leverancier hebben.

Als voor verwerkingsactiviteiten, moet u een standaardservice voor uitbestede overbrengactiviteiten op de **Service voorwaarden** sneltabblad van de **activiteit****details** pagina.

## <a name="service-quantity-calculation"></a>Berekening van servicehoeveelheid
Het hele inkoopproces is gebaseerd op de verwijzing naar een item voor een service. De verwijzing naar dit item wordt gemeten in een eenheid van een service. Services worden meestal gemeten in het aantal services (eenheden) of in de tijd. Voor het berekenen van de servicehoeveelheid, op basis van de geregistreerde voltooiing van kanbantaken, kunt u de volgende methoden:

-   **Berekening op basis van het aantal taken** : één kanbantaak is gelijk aan *n* eenheden van de service, ongeacht de hoeveelheid die wordt geleverd. Een taak correspondeert een materiaalverwerkingseenheid in lean manufacturing. Deze methode geldt voor alle services met een vaste prijs per materiaalverwerkingseenheid. Daarom kan deze methode meestal van toepassing op overboekingsactiviteiten. Echter kan worden ook toegepast op procesactiviteiten waarmee de hele materiaalverwerkingseenheden worden verwerkt.
-   **Berekening die is gebaseerd op de producthoeveelheid** : de servicehoeveelheid wordt ten opzichte van de producthoeveelheid die is gepland of geleverd. Wanneer de geleverde hoeveelheid wordt berekend, kunnen slechte hoeveelheden worden opgenomen of uitgesloten. Deze methode geldt voor alle gevallen waarin de serviceprijs per eenheid van het verwerkte product is gekomen.
-   **Berekening die is gebaseerd op de activiteitstijd** : de theoretische Activiteitstijden worden berekend op basis van de verwerkingstijd van de activiteit, de totale hoeveelheid en de doorvoerverhouding van het verwerkte product verwerkt. Deze methode heeft betrekking op services die worden betaald per uur en een afwijking in de tijd per verwerkt product hebben.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostprijsboekhouding van uitbestede services
Wanneer de ontvangst advies of de pakbon op een inkooporder die is gemaakt voor een productiestroom (met andere woorden, een inkooporder die is gegenereerd op basis van kanbantaken voor uitbestede activiteiten) van een leverancier wordt geboekt, is de waarde van de ontvangst is verwerkt in de OHW-rekeningen van de productiestroom. Afwijkingen van facturen worden ook verwerkt aan de productiestroom in. Een kostencategorie voor uitbesteed werk geïntroduceerd. Deze kostencategorie transparante bijhouden van de waarde van uitbesteed werk wordt toegewezen aan OHW en per periode verbruikt inschakelen.  

De kostprijsberekening voor lean manufacturing aan het einde van een periode van de kostprijsberekening via terugwaarts afboeken wordt de werkelijke afwijkingen van de producten die via de productiestroom wordt geproduceerd tijdens de kostprijsberekening periode berekend.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelvariabelen die zijn overgeboekt als uitbestede activiteiten
Mensen zou vaak transport niet-productief en daaraan een toegevoegde geen waarde is te vergelijken. Wanneer de kosten van uitbesteding wordt vergeleken met de kosten van de interne productie, moet u de kosten van extra vervoersactiviteit beschouwd. Een productiestroom waarmee omvat meerdere vestigingen en vervoer vereist, moet de vervoerskosten als onderdeel van de kosten van de producten aan de klant leveren model. 

Op basis van een activiteit uitbesteding in lean manufacturing, kunt u integreren van vervoerders en vervoeren van leveranciers die materiaal en producten tussen de locaties van een productiestroom verplaatsen. U kunt een vervoerder of leverancier toewijzen door het modelleren van een overbrengactiviteit. De activiteiten/transporttaak is gebaseerd op een overeenkomst service- en inkooporders en kunt u inkooporders en aanbevelingen voor ontvangst, op basis van de werkelijke overboekingstaken. Deze functionaliteit is hetzelfde als de functionaliteit voor uitbestede activiteiten.  

Daarom servicekosten Dynamics 365 for Operations nu stuklijstberekening ondersteunt met vervoer, het maken van gerelateerde inkooporders, geïntegreerde ontvangst registratie en de integratie van transport in de productiekosten voor productiestroom.


