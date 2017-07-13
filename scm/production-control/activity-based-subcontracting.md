---
title: Werkuitbesteding op basis van een activiteit
description: In dit onderwerp wordt tot in detail beschreven hoe u uitbestede activiteiten in een productiestroom voor lean manufacturing kunt gebruiken.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 43c95c8ab8599a048b1c8c732d6dcac1c3e8b9e9
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="activity-based-subcontracting"></a>Werkuitbesteding op basis van een activiteit

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt tot in detail beschreven hoe u uitbestede activiteiten in een productiestroom voor lean manufacturing kunt gebruiken.

Microsoft Dynamics 365 for Finance and Operations bevat twee methoden voor uitbesteding: productieorders en lean manufacturing. In de lean manufacturing-methode worden de uitbestedingswerkzaamheden gemodelleerd als een service die is gerelateerd aan een activiteit van een productiestroom. Een speciaal soort kostengroeptype met de naam **Rechtstreekse uitbesteding** is geïntroduceerd, en de uitbestedingsservices zijn niet langer onderdeel van een stuklijst. De kostprijsboekhouding van uitbesteed werk is volledig geïntegreerd in de kostprijsberekeningsoplossing voor lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Productiestromen die betrekking hebben op toeleveranciers
Het basisprincipe van een productiestroom verandert niet wanneer activiteiten worden uitbesteed. Materiaal wordt nog steeds verplaatst tussen vestigingen, met procesactiviteiten wordt materiaal omgezet in producten en met overboekingsactiviteiten worden producten of materiaal van de ene locatie naar de andere verplaatst. U kunt locaties en werkcellen modelleren als door een leverancier beheerd door de leverancierrekening aan een magazijn of aan een resource van een resourcegroep toe te wijzen.  

Op basis van deze mogelijkheden zijn voor lean manufacturing geen specifieke functies vereist ter ondersteuning van de stroom van materialen en producten. Alle mogelijke scenario's die betrekking hebben op leveranciers als aanbieders van productie- of transportservices kunnen worden gemodelleerd op basis van de architectuur van productiestroom en activiteiten.  

Een toeleverancier werkt bijvoorbeeld vanuit een supermarkt die zich op de locatie van de toeleverancier bevindt. Wanneer materiaalverwerkingseenheden bij de toeleverancier leeg worden gemaakt, worden de kanbankaarten met de volgende verzending teruggestuurd naar de assembly-cel. De supermarkt van de toeleverancier wordt vervolgens aangevuld. De overboekingen naar en van de toeleverancier kunnen worden gemodelleerd als expliciete overboekingsactiviteiten ter ondersteuning van een orderverzamel- en verzendproces. Als geen expliciete registratie vereist is ter ondersteuning van het fysieke transport, kunnen de overboekingsactiviteiten worden weggelaten.  

Een toeleverancier kan worden gebruikt voor het verdelen van de totale capaciteit van de productiestroom. Bijvoorbeeld: een productiestroom wordt gemodelleerd met behulp van geplande kanbanregels. De planner gebruikt het kanbanplanningbord voor planning en effening van de belasting van beide werkcellen op aanvraag. De planner houdt ook toezicht op het geconsolideerde voorraadschema voor de supermarkt op de pagina **Voorraadschema**. Meerdere toeleveranciers kunnen worden gemodelleerd in een of meerdere productiestromen en er kunnen meerdere kanbanregels worden gebruikt voor het leveren van hetzelfde product op dezelfde locatie via verschillende activiteiten. De planner kan kanbans converteren naar een alternatieve kanbanregel om een kanban die oorspronkelijk is gemaakt voor interne productie, opnieuw te plannen voor een alternatief proces. De uitbestede aard van de werkcel heeft eigenlijk geen gevolgen voor de productiestroom. Hetzelfde principe geldt voor twee parallelle interne werkcellen of voor twee uitbestede cellen.   

Net als elke andere activiteit in een productiestroom kunnen uitbestede activiteiten geïnventariseerde, niet-geïnventariseerde (onderhanden werk \[OHW\]) en half afgewerkte materialen en producten verbruiken en leveren. In alle gevallen zijn de processen voor het plannen en uitvoeren van uitbestede activiteiten hetzelfde. Bovendien zijn deze processen hetzefde als de processen voor interne werkzaamheden.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Inkoopproces voor uitbestede activiteiten (services)
Het inkoopproces voor uitbestede activiteiten is gebaseerd op de fysieke materiaalstroom die wordt geregistreerd door de kanbantaakvoortgang, bijvoorbeeld Starten of Voltooien. De financiële stroom, bijvoorbeeld kosten van uitbesteed werk, is een secundaire stroom die volgt op de fysieke stroom. Tegelijkertijd is het inkoopproces een onafhankelijk proces dat handmatige correctie van de inkoopdocumenten bij elke stap mogelijk maakt. Het inkoopproces voor uitbestede activiteiten is als volgt:

1.  Maak een inkoopovereenkomst. De inkoopovereenkomst wordt gemaakt voor de service en wordt gekoppeld aan de activiteit van de productiestroom.
2.  Inkooporder maken. Een inkooporder voor vrijgave kan worden gemaakt voor de service op basis van de geplande kanbantaken. Taken voor dezelfde service kunnen worden gegroepeerd in inkooporderregels per dag, week of maand. De inkooporderregels kunnen op elk gewenst moment worden gemaakt nadat de kanbantaken zijn gemaakt. Inkooporderregels kunnen zelfs erna worden gemaakt. Deze optie wordt meestal ingeschakeld als een toeleverancier zonder nadere kennisgeving services verleent op basis van de kanbans of kanbankaarten die de toeleverancier ontvangt. In dit geval kunnen de afwijkingen tussen de inkooporder en de factuur worden geminimaliseerd.
3.  Genereer kanbankaarten, materiaal en een orderverzamellijst om naar de toeleverancier te verzenden ter voorbereiding van de verwerking. De voorbereiding wordt op basis van de gedetailleerde modellering van de productiestroom uitgevoerd op het kanbanbord voor procesactiviteiten met behulp van de orderverzamellijst en de voorbereidingsfunctie. De voorbereiding kan ook op het kanbanbord worden uitgevoerd voor overboekingstaken met behulp van de orderverzamellijst en aan het begin of bij voltooiing. Voor geïnventariseerde materiaal kunnen beide processen worden ondersteund door een orderverzamel- en verzendproces van WMS. Een vrachtbrief kan op aanvraag worden gemaakt.
4.  Genereer Kanban-materiaalverwerkingseenheden en kanbankaarten. Na verwerking worden kaarten van de toeleverancier teruggestuurd. De kaarten bevatten gewoonlijk een afleveringsbewijs waarmee het fysieke materiaal wordt opgegeven dat is verzonden. Een verwijzing naar de verleende services is niet vereist. De aankomst van het materiaal of het product bij de klant wordt geregistreerd op het kanbanbord, afhankelijk van de kanbankaarten. (Afhankelijk van de gemodelleerde activiteiten wordt het kanbanbord voor procesactiviteiten of het kanbanbord voor overboekingstaken gebruikt.)
5.  Maak een ontvangstadvies. Het ontvangstadvies kan worden gebruikt voor het vervangen van een pakbondocument voor de ontvangen services. Ontvangstadviezen kunnen worden gegenereerd op basis van de voltooide kanbantaken voor de uitbestedingsactiviteit voor een geselecteerde periode. Voor elke taakontvangst worden adviezen gemaakt voor de gerelateerde inkooporderregel. Het ontvangstadvies kan worden afgedrukt en verzonden naar de toeleverancier als bevestiging van ontvangst.
6.  Genereer een factuur.

Het proces wordt beëindigd wanneer de toeleverancier voor een periode wordt gefactureerd. De factuurvereffening wordt uitgevoerd voor de ontvangstadviezen die worden gemaakt. Omdat de ontvangstadviezen de exacte fysieke ontvangst van materiaal voorstellen, wordt de drieweg-overeenstemming vereenvoudigd.

## <a name="configuring-activities-for-subcontracting"></a>Activiteiten voor uitbesteding configureren
In de volgende secties wordt beschreven hoe u activiteiten voor uitbesteding kunt configureren.

### <a name="subcontracted-services"></a>Uitbestede services

Het betalingsitem dat wordt gebruikt in uitbesteding op basis van een activiteit, moet een product zijn dat de volgende eigenschappen heeft:

-   **Producttype:** service
-   **Voorraadmodelgroep:** niet op voorraad

Deze vereiste zorgt ervoor dat het gebruik van het FIFO-voorraadmodel (First In, First Out) wordt gebruikt. **Opmerking:** kostprijsberekening van de producten vereist dat de standaardkosten van de service worden gedefinieerd. Een inkoopovereenkomst met de leverancier is vereist. Anders kan de service niet worden gebruikt voor uitbesteding op basis van een activiteit.

### <a name="subcontracted-process-activities"></a>Uitbestede procesactiviteiten

Als u een procesactiviteit wilt configureren als een uitbestede activiteit, voert u de volgende stappen uit.

1.  Configureer een uitbestede werkcel. Als u een werkcel wilt configureren als uitbesteed, moet u een resource van het type **Leverancier** maken en deze koppelen aan de werkcel (resourcegroep). Aan de werkcel moet een runtime kostencategorie van het kostengroeptype **Rechtstreekse uitbesteding** worden toegewezen. De kostencategorieën voor instelling en hoeveelheid zijn niet verplicht.
2.  Nadat een procesactiviteit is gemaakt en is verbonden aan een uitbestede werkcel, moet u een service voor de activiteit configureren voordat de productiestroomversie kan worden geactiveerd. U voert deze stap uit op de pagina **Activiteit****gegevens**. Voor activiteiten die zijn gekoppeld aan een uitbestede werkcel, wordt het sneltabblad **Servicevoorwaarden** weergegeven. Voeg op dit sneltabblad een standaardservice toe die geldig is voor alle uitvoerartikelen. Als specifieke uitvoerartikelen verschillende services of verschillende parameters voor serviceberekening vereisen (bijvoorbeeld een andere serviceverhouding), kunt u andere services toevoegen aan de activiteit.

## <a name="subcontracted-transfer-activities"></a>Uitbestede overboekingsactiviteiten
Een overboekingsactiviteit wordt geconfigureerd als een uitbestede activiteit, afhankelijk van de instelling **Bevracht door** van de overboekingsactiviteit. De volgende opties zijn beschikbaar:

-   **Verzender** : de activiteit wordt uitbesteed als de overboeking van het magazijn wordt beheerd door een leverancier (zoals gedefinieerd door een eigenschap van het magazijn). Alle geselecteerde inkoopovereenkomsten voor services moeten dezelfde leverancier-ID hebben als het magazijn.
-   **Ontvanger** : de activiteit wordt uitbesteed als de overboeking naar het magazijn wordt beheerd door een leverancier (zoals gedefinieerd door een eigenschap van het magazijn). Alle geselecteerde inkoopovereenkomsten voor services moeten dezelfde leverancier-ID hebben als het magazijn.
-   **Vervoerder** : de activiteit wordt uitbesteed aan een leverancier die de service verleent. Een vervoerder is alleen geldig als deze voor magazijnbeheer wordt gemaakt en als deze een leverancierrekening krijgt toegewezen.

Net als voor procesactiviteiten moet u een standaardservice voor uitbestede overboekingsactiviteiten configureren op het sneltabblad **Servicevoorwaarden** van de pagina **Activiteit****gegevens**.

## <a name="service-quantity-calculation"></a>Berekening van servicehoeveelheid
Het gehele inkoopproces is gebaseerd op een artikelverwijzing voor een service. De artikelverwijzing wordt gemeten in een maateenheid voor een service. Services worden meestal gemeten in het aantal services (eenheden) of in tijd. Voor het berekenen van de servicehoeveelheid op basis van de geregistreerde voltooiing van kanbantaken, kunt u de volgende methoden gebruiken:

-   **Berekening op basis van het aantal taken**: één kanbantaak is gelijk aan *n* service-eenheden, ongeacht de producthoeveelheid die wordt geleverd. In lean manfacturing correspondeert één taak met één materiaalverwerkingseenheid. Deze berekeningsmethode geldt voor alle services met een vaste prijs per materiaalverwerkingseenheid. Daarom is deze methode meestal van toepassing op overboekingsactiviteiten. Deze methode kan echter ook worden toegepast op procesactiviteiten waarmee gehele materiaalverwerkingseenheden worden verwerkt.
-   **Berekening op basis van de producthoeveelheid** : de servicehoeveelheid is gerelateerd aan de producthoeveelheid die is gepland of geleverd. Wanneer de geleverde producthoeveelheid wordt berekend, kunnen slechte hoeveelheden worden opgenomen of uitgesloten. Deze berekeningsmethode geldt voor alle gevallen waarin de prijs per eenheid voor de service van het verwerkte product is overeengekomen.
-   **Berekening op basis van de activiteitstijd**: de theoretische activiteitstijden worden berekend op basis van de verwerkingstijd van de activiteit, de totale verwerkte hoeveelheid en de doorvoerverhouding van het verwerkte product. Deze berekeningsmethode is van toepassing op services die per uur worden betaald en een afwijking in tijd per verwerkt product hebben.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostprijsboekhouding van uitbestede services
Wanneer het ontvangstadvies of de pakbon van een leverancier op een inkooporder die is gemaakt voor een productiestroom (met andere woorden, een inkooporder die is gegenereerd op basis van kanbantaken voor uitbestede activiteiten) wordt geboekt, wordt de waarde van de ontvangst verwerkt in de OHW-rekeningen van de productiestroom. Afwijkingen van facturen worden ook verwerkt in de productiestroom. Er is een kostencategorie voor uitbesteed werk geïntroduceerd. Met deze kostencategorie kan de waarde van uitbesteed werk dat wordt toegewezen aan OHW en per periode wordt verbruikt, transparant worden bijgehouden.  

De kostprijsberekening via terugwaarts afboeken voor lean manufacturing aan het einde van een kostprijsberekeningsperiode berekent de werkelijke afwijkingen van de producten die via de productiestroom worden geproduceerd tijdens de kostprijsberekeningsperiode.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Overboekingen als uitbestede activiteiten modelleren
Transport wordt vaak gezien als niet-productief en zonder toegevoegde waarde. Als de kosten van uitbesteding worden vergeleken met de kosten van interne productie, moeten de kosten van extra transportactiviteiten echter worden meegenomen. In een productiestroom die meerdere locaties omvat en transportservices vereist, moeten de transportkosten als onderdeel van de kosten voor levering van de producten aan de klant worden gemodelleerd. 

Met uitbesteding op basis van een activiteit in lean manufacturing kunt u vervoerders en transportleveranciers integreren die materiaal en producten tussen de locaties van een productiestroom verplaatsen. U kunt een vervoerder of leverancier toewijzen door een overboekingsactiviteit te modelleren. De overboekingsactiviteiten/-taak zijn gebaseerd op een service- en inkoopovereenkomst en u kunt inkooporders en ontvangstadviezen maken op basis van de werkelijke overboekingstaken. Deze functionaliteit is hetzelfde als de functionaliteit voor uitbestede procesactiviteiten.  

Daarom wordt Finance and Operations nu stuklijstberekening ondersteund waarin transportservices, het maken van gerelateerde inkooporders, geïntegreerde ontvangstregistratie en de integratie van transportservicekosten zijn opgenomen in de kostprijsberekening van de productiestroom.




