---
title: Overzicht van productieproces
description: In dit artikel vindt u een overzicht van de productieprocessen. De verschillende fasen van productieorders, batchorders en kanbans worden beschreven, van het maken van de order tot het afsluiten van de boekperiode.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdStatusListPage, JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 6a33117f454b5b0d109c8a5c460fa218eab5c0f7
ms.lasthandoff: 03/31/2017


---

# <a name="production-process-overview"></a>Overzicht van productieproces

[!include[banner](../includes/banner.md)]


In dit artikel vindt u een overzicht van de productieprocessen. De verschillende fasen van productieorders, batchorders en kanbans worden beschreven, van het maken van de order tot het afsluiten van de boekperiode. 

De vervaardiging van producten, soms ook wel bekend als de productiecyclus, volgt specifieke stappen die vereist zijn voor het maken van een artikel. De levenscyclus begint met het opstellen van de productieorder, batchorder of kanban. Het eindigt met een voltooid, gefabriceerd artikel dat gereed is voor een klant of een andere productiefase. Elke stap in de levenscyclus vereist verschillende soorten informatie om het proces te voltooien. Bij elke stap die is voltooid, ondergaat de productieorder, batchorder of kanban een wijziging in de productiestatus. Verschillende typen producten vereisen verschillende productieprocessen.  

De module **Productiecontrole** is gekoppeld aan andere modules, zoals **Productgegevensbeheer**, **Voorraadbeheer**, **Grootboek**, **Magazijnbeheer**, **Projectadministratie** en ** Organisatiebeheer**. Door deze integratie wordt de informatiestroom ondersteund die is vereist om de productie van een afgewerkt artikel te voltooien.  

Het productieproces wordt doorgaans beïnvloed door de kostprijsboekhouding en voorraadwaarderingsmethoden die voor een bepaald productieproces worden gekozen. Dynamics 365 for Operations ondersteunt zowel werkelijke kosten (first in, first out \[FIFO\]; last in, first out \[LIFO\]; zwevend gemiddelde en periodiek gewogen gemiddelde) als standaardmethoden voor kostprijsberekening. Lean manufacturing wordt geïmplementeerd op basis van het principe van kostprijsberekening via terugwaarts afboeken.  

De keuze van de methoden voor kostenmeting bepaalt ook de vereisten voor rapportage over materiaal- en resourceverbruik tijdens het productieproces. Doorgaans vereisen methoden voor de berekening van werkelijke kosten nauwkeurige rapportage op taakniveau, terwijl methoden voor periodieke kostprijsberekening minder gedetailleerde rapportage van materiaal- en resourceverbruik toestaan.

## <a name="mixed-mode-manufacturing"></a>Gemengde productie
Verschillende producten en de productietopologieën vereisen het gebruik van verschillende ordertypen. Dynamics 365 for Operations kan de diverse ordertypen in een gemengde modus toepassen. Met andere woorden, alle ordertypen kunnen voorkomen tijdens het totale proces van het vervaardigen van één afgewerkt product.

-   **Productieorder** - Dit is het klassieke ordertype om een specifiek product of een productvariant te vervaardigen in een bepaalde hoeveelheid op een specifieke datum. Productieorders zijn gebaseerd op stuklijsten en routes.
-   **Batchorder** – Dit ordertype wordt gebruikt voor procesbedrijfstakken en afzonderlijke processen waarbij de productieconversie op een formule is gebaseerd of waarbij de co- en bijproducten eindproducten kunnen zijn, naast of in plaats van het hoofdproduct. Batchorders gebruiken stuklijsten en routes van het type **Formule**.
-   **Kanban** – Kanbans worden gebruikt om herhaalde processen in lean manufacturing te signaleren die zijn gebaseerd op productiestromen, kanbanregels en stuklijsten.
-   **Project** - Een productieproject combineert producten en services aan een bepaalde planning en een budget. Het productiedeel van een project kan via elk van de andere ordertypen worden geleverd.

## <a name="manufacturing-principles"></a>Productieprincipes
Om het productieprincipe te selecteren dat het beste past bij een bepaald product en een gerelateerde markt, moet u de behoeften van productie en logistiek in overweging nemen, alsmede de klantverwachtingen over levertijden.

-   **Maken naar voorraad** - Dit is het klassieke productieprincipe, waarbij producten voor voorraad worden geproduceerd op basis van prognose of minimumvoorraadaanvulling (de laatstgenoemde wordt meestal berekend op basis van prognose of historisch verbruik).
-   **Maken naar order** - Standaardproducten worden gemaakt naar order of voltooid naar order. Hoewel de voorproductie kan worden uitgevoerd met behulp van het principe Maken naar voorraad, worden dure stappen in de waardeketen of stappen waarbij varianten worden gemaakt, geactiveerd door een verkooporder of een transferorder.
-   **Configureren naar order** - Zoals bij het principe Makeren naar order, worden de laatste bewerkingen van de waardeketen naar order gemaakt. De werkelijke productvariant die wordt geproduceerd is niet vooraf gedefinieerd, maar wordt gemaakt op het moment van orderinvoer, op basis van het configuratiemodel van het verkoopproduct. Het principe Configureren naar order vereist een bepaald niveau van proceseenmaking voor een bepaalde productregel.
-   **Engineer naar order** - Processen voor Engineer naar order worden meestal uitgevoerd via een project en beginnen meestal met de engineeringfase. Tijdens de engineeringfase worden de werkelijke producten die zijn vereist voor het vervullen van de order ontworpen en beschreven. Vervolgens kunnen productieorders, batchorders of kanbans worden gemaakt om de producten te vervaardigen.

## <a name="overview-of-the-production-life-cycle"></a>Overzicht van de productielevenscyclus
De volgende stappen in de productiecyclus kunnen plaatsvinden voor alle ordertypen voor gemengde productie. Ze worden echter niet allemaal weergegeven als een expliciete orderstatus.

1.  **Gemaakt** - U kunt een productieorder, batchorder of kanban handmatig maken, of u kunt het systeem zodanig configureren dat deze worden gegenereerd op basis van verschillende vraagsignalen. De hoofdplanning maakt productieorders, batchorders of kanbans door geplande orders te fiatteren. Andere vraagsignalen zijn verkooporders of getraceerde leveringssignalen van andere productieorders of kanbans. Voor kanbans met vaste hoeveelheid worden vraagsignalen gegenereerd wanneer kanbans als leeg worden geregistreerd.
2.  **Geschat** – U kunt ramingen voor materiaal- en resourceverbruik berekenen. De raming genereert voorraadtransacties voor grondstoffen die de status **In bestelling** hebben. De ontvangsten voor hoofdproducten, co- en bijproducten worden gegenereerd wanneer productieorders of batchorders worden geraamd. Als de stuklijst regels van het type **Getraceerd aanbod** bevat, worden inkooporders voor materialen of uitbestede bewerkingservices gegenereerd en getraceerd voor de productieorder of batchorder. Artikelen of orders worden gereserveerd volgens de reserveringstrategie van de productieorder, en de prijs van de voltooide goederen wordt berekend op basis van parameterinstellingen.
3.  **Gepland** – U kunt de productie plannen op basis van bewerkingen, afzonderlijke taken of beide.
    -   **Bewerkingsplanning** – Deze planningsmethode biedt een grof plan voor de lange termijn. Via deze methode kunt u de begin- en einddatums toewijzen aan productieorders. Als de productieorders aan routebewerkingen zijn gekoppeld, kunt u deze toewijzen aan kostenplaatsgroepen.
    -   **Taakplanning** – Deze planningsmethode biedt een gedetailleerd plan. Elke operatie wordt opgesplitst in individuele taken die specifieke datums, tijden en toegewezen bronnen voor bedrijfsactiviteiten hebben. Als eindige capaciteit wordt gebruikt, worden taken toegewezen aan resources op basis van beschikbaarheid. U kunt het schema in een Gantt-diagram weergeven en wijzigen.
    -   **Kanbanplanning** – Kanbantaken worden gepland op het kanbanplanningsbord of automatisch gepland op basis van de automatische planningsconfiguratie van de kanbanregels.

4.  **Vrijgegeven** – U kunt de productieorder of batchorder vrijgeven wanneer de planning is voltooid en het materiaal beschikbaar is om te worden verzameld of voorbereid. De beschikbaarheidscontrole voor materialen helpt de supervisor op de werkvloer bij het beoordelen van de beschikbaarheid van materiaal voor de productieorders of batchorders. U kunt ook de productieorderdocumenten afdrukken, zoals de orderverzamellijsten, projectkaart, routekaart en routetaak. Wanneer de productieorder wordt vrijgegeven, verandert de status van de order om aan te geven dat de productie kan beginnen. Als magazijnbeheer wordt gebruikt, worden bij vrijgave van de productieorder of batchorder productiestuklijstregels vrijgegeven aan het magazijnbeheer. Magazijnwaves en magazijnwerkzaamheden worden vervolgens gegenereerd volgens de instellingen van het magazijn.
5.  **Voorbereid**/**Verzameld** – Wanneer alle materialen en resources in de productielocatie zijn gefaseerd, worden de productiestuklijstregels of kanbanregels bijgewerkt naar de status **Verzameld**. Getraceerde aanbodorders en bijbehorende magazijnwerkzaamheden worden meestal in deze fase voltooid. De kanbankaarten of taakkaarten die zijn vereist om de productievoortgang te rapporteren moeten worden toegewezen en afgedrukt.
6.  **Begonnen** – Wanneer een productieorder, batchorder of kanban wordt gestart, kunt u materiaal- en resourceverbruik rapporteren voor de order. Het systeem kan worden geconfigureerd om het materiaal- en resourceverbruik dat is toegewezen aan de order automatisch te boeken wanneer de order wordt gestart. Deze toewijzing staat bekend als preflushing, vooraf wissen of autoconsumption. U kunt materialen handmatig toewijzen aan productieorders of batchorders door op extra orderverzamellijstjournalen te maken. U kunt ook handmatig arbeidskosten en overige routekosten aan de order toewijzen. Als u bewerkingsplanning gebruikt, kunt u deze kosten toewijzen door een routekaartjournaal te maken. Als u taakplanning gebruikt, kunt u de kosten toewijzen door een taakkaartjournaal te maken. De productieorders of batchorders kunnen in batches van de aangevraagde laatste hoeveelheid worden gestart. Binnen een productieorder, batchorder of kanban, kunnen de taken die worden gemaakt afzonderlijk wordtn gestart en gerapporteerd via journalen, de productie-uitvoeringsterminal (MES-terminal) of de kanbanborden.
7.  Voortgang melden/**Voltooide** taken – Gebruik de MES-terminal, productiejournalen, kanbanborden of mobiele scanmogelijkheden om de productievoortgang te rapporteren per taak of bron. Materiaal- en resourceverbruik wordt geboekt en de status van de bijbehorende kanbans, productieorders en batchorders kan worden bijgewerkt naar **Ontvangen** of **Gereedgemeld**. Mogelijk wordt weggezet werk gemaakt voor het magazijn, afhankelijk van de magazijnconfiguratie.
8.  **Gereedgemeld** (de productontvangst) – Wanneer een productieorder of batchorder wordt gereedgemeld, wordt de hoeveelheid afgewerkte goederen die zijn voltooid bijgewerkt in voorraad. Deze hoeveelheid omvat de hoeveelheid relevante co- en bijproducten. Als u werk in uitvoering (OHW)-boekhouding gebruikt, wordt een grootboekjournaal gegenereerd om de OHW-rekeningen te verlagen en de voorraad van afgewerkte producten te verhogen. Wanneer de kostprijs van een productieorder wordt berekend, worden de werkelijke kosten van de productie geboekt. Als de kosten voor materiaal en arbeid die gekoppeld zijn aan een productieorder, nog niet zijn toegewezen in een journaal of door preflushing, kunnen ze automatisch worden toegewezen via backflushing. De toewijzing via backflushing omvat het aftrekken achteraf van voorraadtransactieprocessen. Als de productieorder is voltooid, schakelt u het selectievakje **Eindtaak** in om de resterende status te wijzigen in **Beëindigd**. Laat het veld anders leeg om de rapportage van extra hoeveelheden die worden geproduceerd mogelijk te maken.
9.  **Kwaliteitsbeoordeling** - Een productontvangst kan het maken van kwaliteitsorders activeren, afhankelijk van de configuratie van testprocessen en de kwaliteitsregels die voor specifieke producten zijn vastgesteld. Omdat een kwaliteitsorder de voorraadstatus of de batchkenmerken van de geteste producten kan bijwerken, is de kwaliteitsbeoordeling een verplicht proces in veel bedrijfstakken.
10. **Wegzetten** en **Verzenden naar order** – Na productontvangst en kwaliteitsbeoordeling, leidt optioneel wegzetwerk de ontvangen producten naar het volgende verbruikspunt, een magazijn voor eindproducten of een leverzone als er vereisten voor verzending naar order zijn.
11. **Beëindigd** – Voordat de productie wordt beëindigd, worden de werkelijke kosten berekend voor de hoeveelheid die is geproduceerd. Alle geraamde kosten van materiaal, arbeid en overhead worden teruggeboekt en worden vervangen door de werkelijke kosten. Als u het selectievakje **Eindtaak** inschakelt bij het uitvoeren van de kostenberekening, wijzigt de status van de productieorder in **Beëindigd**. Deze status voorkomt dat eventuele extra kosten naar een voltooide productieorder worden geboekt.
12. **Periodesluiting** – Sommige principes voor kostprijsboekhouding, zoals periodiek gemiddelde, kostprijsberekening via terugwaarts afboeken, FIFO of LIFO vereisen periodieke activiteiten om de voorraad of de financiële periode te sluiten. Doorgaans probeert het systeem alle materiaal- en resourceverbruik te rapporteren, terwijl tevens correcties van voorraad en uitval worden uitgevoerd voordat de perioden worden afgesloten. Deze rapportage wordt gewoonlijk uitgevoerd door voorraadmutatiejournalen of correctiejournalen te gebruiken. Het doel is de economische prestaties van operationele eenheden per periode te beoordelen. In sommige gevallen, wanneer langlopende productieorders worden gebruikt die de hele financiële rapportageperiode omvatten, worden productiejournalen gebruikt om de productievoortgang en het resourceverbruik te rapporteren aan het eind van de periode.


<a name="see-also"></a>Zie ook
--------

[Productiefeedback](production-feedback.md)

[Productconfiguratiemodellen](../pim/product-configuration-models.md)

[Lean manufacturing](lean-manufacturing-overview.md)




