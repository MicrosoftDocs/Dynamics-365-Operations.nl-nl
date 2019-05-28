---
title: Kostprijsberekening via terugwaarts afboeken
description: In dit onderwerp wordt het concept van kostprijsberekening via terugwaarts afboeken geïntroduceerd dat wordt gebruikt voor Lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 484bac74ccb498f0b006458f5e6d8fb0e9461a8f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556064"
---
# <a name="backflush-costing"></a>Kostprijsberekening via terugwaarts afboeken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt het concept van kostprijsberekening via terugwaarts afboeken geïntroduceerd dat wordt gebruikt voor Lean manufacturing. 

Bij kostprijsberekening voor Lean manufacturing kan de productiestroom gebruikmaken van de kostenaccumulatiemethode die bekend staat als kostprijsberekening via terugwaarts afboeken. Bij de methode van kostprijsberekening via terugwaarts afboeken worden de directe materialen die worden verbruikt bij elkaar opgeteld in de kostenrekening voor onderhanden werk (OHW) van de productiestroom. Er wordt gebruikgemaakt van de voorraadmodelgroep voor standaardkosten. De producten die worden ontvangen van de productiestroom worden afgetrokken van het OHW tegen standaardkostprijs. Het belangrijkste verschil tussen de kostprijsberekening via terugwaarts afboeken en standaardkosten is dat afwijkingen voor kostprijsberekening via terugwaarts afboeken niet worden berekend per kanban of eindproduct. In plaats daarvan worden afwijkingen per productiestroom berekend gedurende een periode. Deze methode introduceert een echt lean concept voor het melden van materiaalverbruik. Specifiek verzamelde hoeveelheid materiaal worden niet aan een kanban of productieorder gerapporteerd. In plaats daarvan worden volledige batches of materiaalverwerkingseenheden klaargezet voor de productiestroom. Nadat de batches of materiaalverwerkingseenheden als leeg zijn geregistreerd, worden zij als verbruikt verklaard. Mogelijk wordt gebruikgemaakt van geavanceerd verbruik, afhankelijk van de [configuratie van de productiestroom](../production-control/lean-manufacturing-modeling-lean-organization.md). Voordat gebruik kan worden gemaakt van geavanceerd verbruik, moeten organisaties zichzelf toestaan dat materiaal kan verdwijnen in het OHW van de productiestroom. De periodieke kostprijsberekening via terugwaarts afboeken bepaalt de effectieve waarde van OHW naar het einde van de periode. Deze bepaling is gebaseerd op de kanban-materiaalverwerkingseenheden en de kanbantaakstatus. Afwijkingen tussen de daadwerkelijke waarden en de werkelijke OHW-waarden per kostengroep en artikel worden verwerkt en weergegeven als afwijkingen.

## <a name="configuring-backflush-costing"></a>Kostprijsberekening via terugwaarts afboeken configureren
U moet de volgende instellingen uitvoeren om kostprijsberekening in te schakelen:

-   **OHW-rekeningen instellen voor de productiegroep en productiestroom.** De OHW-rekeningen voor de productiestroom worden opgegeven in de productiegroep. De productiestroom voor kostprijsberekening via terugwaarts afboeken berekent afwijkingen als het verschil in de OHW-waarde voor- en nadat kostprijsberekening via terugwaarts afboeken is uitgevoerd voor elke productiestroom. Daarom is het raadzaam dat u een OHW-rekening maakt voor elke productiestroom.
-   **Wijs een kostencategorie toe aan de resourcegroep.** U moet een kostencategorie toewijzen aan de uitvoeringstijdcategorie van de werkcel. Om afwijkingen per activiteit te bepalen, moet u een kostencategorie voor elke werkcel maken. De kostencategorieën voor instelling en hoeveelheid worden niet meegenomen in de kostprijsberekening voor lean manufacturing. De OHW-rekeningen per resourcegroep worden genegeerd bij de kostprijsberekening via terugwaarts afboeken. Voor uitbestede activiteiten is geen kostencategorie vereist. In plaats daarvan wordt de kostengroep die is toegewezen aan de actieve service gebruikt.
-   **Wijs kostengroepen toe.** Als u segmentatie van de bijdrage van de kosten in een productiestroom wilt inschakelen, moet u kostengroepen toewijzen per kostengroeptype:
    -   **Directe materiaalkostengroep**: direct materiaal dat is vereist voor een kostengroep die de materiaalcategorie voor kostprijsberekening identificeert. Deze kostengroep maakt een samengevoegde weergave mogelijk van kosten, OHW en afwijkingen per direct materiaal.
    -   **Kostengroep voor directe productie**: de kostengroep voor directe productie legt de bijdrage van de directe kosten van operationele resources aan de productiestroom vast. Deze kostengroep maakt een samengevoegde weergave mogelijk van kosten, OHW en afwijkingen per kosten voor directe productie.
    -   **Indirecte kostengroep**: de groep voor de indirecte kosten is vereist voor het berekenen van de bijdrage van de indirecte kosten aan de productiestroom. Deze kostengroep maakt een samengevoegde weergave mogelijk van kosten, OHW en afwijkingen per indirecte kosten.
    -   **Kostengroep voor rechtstreekse uitbesteding**: de kostengroep voor de services maakt een samengevoegde weergave mogelijk van toegewezen kosten en OHW en bepaalt de kostenafwijkingen van de uitbestede services.
    -   **Kostengroep voor een eindproduct**: eindproducten vereisen een kostengroep voor identificatie van de productcategorie voor kostprijsberekening. Deze kostengroep maakt een samengevoegde weergave mogelijk van kosten, OHW en afwijkingen per productcategorie. De standaardkosten voor producten wordt berekend met behulp van de kostenberekening op basis van de stuklijst en de regels voor productiestroom en kanban of de route.

### <a name="costing-sheet"></a>Kostprijsberekening

Het kostenblad modelleert de kostenstructuur voor het bedrijf en wordt samengesteld door de kostengroepen voor het classificeren van de kosten. Het kostenblad heeft verschillende vormen. Het geeft kostengegevens weer volgens de structuur waarin het is ontworpen. In het kostenblad definieert u ook de formule die wordt gebruikt voor het berekenen van de indirecte kosten. De berekeningsformule kan worden gebaseerd op hoeveelheden, gewicht, volume of waarde.

-   **Definieer een kostprijsberekeningsversie.** In de kostprijsberekeningsversie definieert het bedrijf hoe de kosten moet worden onderhouden. Een kostprijsberekeningsversie kan een set standaardkostenrecords bevatten, of een set geplande kostenrecords, afhankelijk van het kostprijsberekeningstype dat is toegewezen aan de kostprijsberekeningsversie. De kostprijsberekeningsversie die wordt gebruikt voor kostprijsberekening voor Lean manufacturing moet zijn gebaseerd op de standaardkostprijs.
-   **Wijs een voorraadmodelgroep toe voor vrijgegeven producten.** Alle producten die zijn gerelateerd aan de productiestroom moeten worden toegewezen aan een voorraadmodelgroep die gebruikmaakt van de voorraadmodelgroep **Standaardkosten**. De standaardkostprijs wordt onderhouden per locatie en activeringsdatum. Voor productmodellen kan de voorraadmodelgroep worden geselecteerd als de kosten worden onderhouden per variant of productmodel.
-   **Uitbestede services zijn per definitie services die niet uit voorraad worden geleverd.** Uitbestede activiteiten hebben geen voorraadmodelgroep. Als u een correct kostprijs wilt vaststellen voor een uitbestede activiteit, moet u ervoor zorgen dat de serviceactiviteit deel uitmaakt van een voorraadmodelgroep waarvoor het voorraadbeleid is ingesteld op **Product in voorraad = Onwaar**.

Voor uitvoerproducten vereist kostenberekening op basis van de productiestroom dat een standaardkostprijs wordt onderhouden voor de services die zijn gerelateerd aan uitbestede activiteiten. De kostengroep die is toegewezen aan de services wordt gebruikt om afwijkingen in de kosten van de uitbestede activiteit te bepalen.

## <a name="cost-calculation-for-lean-manufacturing"></a>Kostenberekening voor Lean manufacturing
Voor producten die uit een productiestroom zijn geleverd, moet de stuklijstberekening zijn gebaseerd op een routeversie of een productiestroom. Bij de stuklijstberekening worden de kosten berekend van een product en de bijbehorende uitsplitsing naar de resources en materialen die nodig zijn om het product te kunnen maken. De inhouding op de OHW-rekening voor de productiestroom wordt uitgevoerd met behulp van de onderverdeling van een product per artikel en kostengroep.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Berekening die is gebaseerd op de productiestroom

Lean manufacturing voor Microsoft Dynamics 365 for Finance and Operations is niet afhankelijk van routes. De kostenberekening voor producten die worden geleverd vanuit een productiestroom kan worden gebaseerd op de productiestroom zelf. Voordat de berekening kan worden uitgevoerd, moet een kanbanregel worden gemaakt die het product levert vanuit de productiestroom. Als een product op de berekeningsdatum uit meerdere productiestromen op dezelfde locatie kan worden geleverd, kunt u de productiestroom voor de stuklijstberekening selecteren. Op de pagina **Standaardproductiestroom** kunt u een standaardproductiestroom configureren voor elk artikel. Als er meerdere kanbanregels bestaan voor hetzelfde product in dezelfde productiestroom die actief is op de berekeningsdatum, selecteert de berekening de eerste kanbanregel die actief is voor de berekening.

### <a name="calculation-that-is-based-on-the-route"></a>Berekening die is gebaseerd op de route

Berekening die is gebaseerd op een route is net zo geldig als berekening die is gebaseerd op een productiestroom. Berekening die is gebaseerd op een route maakt echter geen gebruik van de kostprijsberekening voor Lean manufacturing-functionaliteit. De route moet gebruikmaken van resourcevereisten voor resourcegroepen. Als u systematische afwijkingen wilt voorkomen, moet tevens gebruik worden gemaakt van dezelfde werkcellen of ten minste dezelfde kostencategorieën. Nogmaals, voorkom kostencategorieën voor instellingen en hoeveelheid. Zij helpen niet de kosten in een meer gedetailleerde vorm te berekenen dan bij het terugwaarts afboeken van kosten voor Lean manufacturing. Om te bepalen welke optie (productiestroom of route) u het beste kunt gebruiken voor het berekenen van de kostprijs, houdt u rekening met de resultaten van de kostenanalyse. De versie die dichter bij de werkelijkheid komt en minder algemene afwijkingen produceert is de beste optie. In een Lean manufacturing-omgeving waarin een product wordt geleverd door een enkele productiestroom en een enkele kanbanregel is de berekening op basis van de productiestroom waarschijnlijk nauwkeuriger. Voor een product dat kan worden geleverd door Lean manufacturing en productieorders op dezelfde locatie of waarbij meerdere productiestromen of meerdere kanbanregels in dezelfde werkstroom mogelijk zijn, is een berekening die is gebaseerd op een routeversie die specifiek is samengesteld voor de kostenberekening en niet voor de productie mogelijk nauwkeuriger. De berekening van de productiestroom moet worden gebruikt voor het berekenen van producten waarbij sprake is van uitbesteding. In Microsoft Dynamics 365 for Finance and Operations maken de kostenmodellen voor uitbesteding via productieorders en uitbesteding in Lean manufacturing gebruik van twee verschillende benaderingen. Lean manufacturing introduceert een nieuwe kostengroeptype, **Directe uitbesteding**, voor het berekenen van uitbestede services.

## <a name="material-consumption"></a>Materiaalverbruik
Wanneer materiaal wordt verbruikt uit voorraad naar OHW, worden de materiaalkosten toegevoegd aan OHW tegen de werkelijke standaardkosten voor een kostengroep. Deze bewerking vindt plaats onder de volgende voorwaarden:

-   Kanbanuitgiften worden geboekt voor kanbanorderverzamelregels die voorraad bijwerken.
-   Overboekingstaken worden voltooid waarbij voorraad wordt bijgewerkt bij orderverzameling, maar niet bij ontvangst (overboeking van materiaal vanuit voorraad naar OHW).

## <a name="receiving-products-from-the-production-flow"></a>Ontvangst van producten vanuit de productiestroom
Producten worden onder de volgende voorwaarden ontvangen vanuit de productiestroom:

-   Procestaken worden voltooid waarvoor **Voorraad bijwerken bij ontvangst** is ingesteld op **Ja**.
-   Overboekingstaken worden voltooid waarbij voorraad wordt bijgewerkt bij ontvangst, maar waarbij **Voorraad bijwerken bij orderverzameling** is ingesteld op **Nee** (overboeken vanuit OHW naar voorraad). Met deze optie kunt u producten uit een productiestroom ontvangen onafhankelijk van de stuklijst en routeconfiguratie. Het proces volgt simpelweg de fysieke stromen. Deze optie is vooral geschikt voor het ontvangen van bijproducten, coproducten of uitval van een productiestroom en voor het dienovereenkomstig corrigeren van het kostensaldo van de productiestroom voor OHW.

Producten die worden ontvangen van de productiestroom worden afgetrokken van het OHW.

## <a name="products-in-wip"></a>Producten in OHW
Met het OHW-model van Lean manufacturing in Microsoft Dynamics 365 for Finance and Operations kunt u de status van de kanban-materiaalverwerkingseenheid gebruiken voor het beheren van het materiaal, de halffabrikaten en de eindproducten die deel uitmaken van OHW.

-   **Toegewezen**: de kanban kan verbruikt materiaal hebben dat wordt verwerkt in OHW.
-   **Ontvangen**: als de kanban naar een laatste activiteit verwijst waarbij **Voorraad bijwerken bij ontvangst** is ingesteld op **Nee**, vertegenwoordigt dit een volledige materiaalverwerkingseenheid van een product of een halffabrikaat dat is niet geregistreerd voor de voorraad.

Houd er rekening mee dat materiaal in OHW niet zichtbaar is in overzichten van de voorhanden voorraad. Het is echter wel zichtbaar in de overzichten van kanbanhoeveelheden.

## <a name="consuming-products-in-wip"></a>Producten verbruiken in OHW
Producten in OHW worden verbruikt wanneer de bijbehorende kanban-materiaalverwerkingseenheden worden leeggemaakt. Een signaal kanban leeg produceert geen actieve transactie in de kostprijsberekening, maar wordt pas van kracht wanneer de volgende kostprijsberekening via terugwaarts afboeken wordt uitgevoerd. Geleegde kanban-materiaalverwerkingseenheden zijn niet langer geboekt als voorhanden en worden daarom als verbruikt berekend binnen de periode.

### <a name="automatic-empty-registration"></a>Automatische leegregistratie

Geplande of gebeurteniskanbans kunnen worden ingesteld op automatische leegregistratie in de kanbanregel:

-   **Wanneer materiaalverwerkingseenheden worden ontvangen**: standaard wordt voor geplande kanbans het materiaal gedeclareerd als verbruikt wanneer de laatste taak van de kanban is voltooid. Bij kanbans met vaste hoeveelheid wordt deze optie alleen aanbevolen voor kanbans van één opslaglocatie, omdat de kaart naar de vraagbron wordt geretourneerd wanneer een kanban wordt ontvangen op de uiteindelijke bestemming.
-   **Wanneer de bronbehoefte is geregistreerd**: deze optie is alleen beschikbaar voor gebeurteniskanbans en is de standaardoptie voor dergelijke kanbans. In verband met OHW is deze optie handig voor het schoonhouden van OHW, omdat kanbans voor onderdelen in OHW automatisch worden geleegd en daarom verbruikt uit OHW wanneer de bovenliggende kanban wordt voorbereid.

Tot slot kunnen kanban-materiaalverwerkingseenheden worden toegewezen (= in uitvoering), ontvangen (= volledig) of geleegd. Er is geen gedeeltelijke lediging. Daarom is het, omwille van een nauwkeurige registratie van verbruik, belangrijk dat u de producthoeveelheden van een kanban beperkt zodat ze kleiner zijn dan het verbruik per periode. Producten die in grote batches naar de werkvloer worden verplaatst en die betrekking hebben op dagen of weken van vraag dienen niet worden verbruikt voor OHW. In plaats daarvan moeten deze producten in de voorraad worden gehouden.

## <a name="backflush-costing"></a>Kostprijsberekening via terugwaarts afboeken
U moet kostprijsberekening via terugwaarts afboeken uitvoeren om periodiek de waarde te bepalen van het OHW en de status aan het einde van een periode te produceren waarbij de afwijkingen van materiaal, arbeid en indirecte kosten worden berekend. De berekende afwijkingen worden geboekt naar de rekeningen van de afwijking. In het proces voor kostprijsberekening via terugwaarts afboeken worden alle productiestromen van de rechtspersoon gebruikt in dezelfde batchverwerking. Wanneer kostprijsberekening via terugwaarts afboeken in een batch wordt uitgevoerd, is het mogelijk dat verwerking plaatsvindt met meerdere threads per productiestroom. De periode voor terugwaarts afboeken wordt gedefinieerd door een einddatum. U kunt nieuwe transacties niet naar een datum boeken waarop een kostprijsberekening via terugwaarts afboeken is uitgevoerd. Voer kostprijsberekening via terugwaarts afboeken voor de huidige datum nooit uit voordat de dag werkelijk is verstreken. Bij kostprijsberekening via terugwaarts afboeken worden de volgende stappen uitgevoerd.

1.  Bepaal de niet-gebruikte hoeveelheden in de productiestroom vanaf de einddatum van de periode. Nadat de kostprijsberekening via terugwaarts afboeken is uitgevoerd, kunt u de niet-gebruikte hoeveelheden weergeven op de datum waarop de kostprijsberekening is uitgevoerd in het dialoogvenster **Niet-gebruikte hoeveelheden**.
2.  Bereken het netto gerealiseerde verbruik van de productiestroom over de periode.
3.  Schakel het OHW uit via het gerealiseerde resourceverbruik en de producten.
4.  Bereken productieafwijkingen van standaardkosten voor de periode. **Voor verbruikte onderdelen voor de periode:**
    -   Werk financieel de netto gerealiseerde hoeveelheid materiaal bij die de productiestroom gedurende de periode heeft verbruikt. Het systeem verwerkt in FIFO-volgorde (first in, first out) de afzonderlijke voorraadtransacties om de fysiek bijgewerkte transacties voor de productiestroom financieel bij te werken totdat de netto gerealiseerde hoeveelheden voor de periode worden bereikt.
    -   Transacties worden financieel gesplitst om de precieze verbruikte hoeveelheden toe te wijzen.
    -   Niet-gebruikte hoeveelheden in de productiestroom OHW blijven in de fysiek bijgewerkte status.

    **Voor hoeveelheden waarvan de productie is voltooid in de periode:**
    -   Werk financieel de voorraadtransacties voor de voltooide hoeveelheid voor de periode bij.

    **Voor de conversiekosten:**
    -   De toegepaste conversiekostentransacties (routetransacties) die zijn geregistreerd voor de periode worden financieel bijgewerkt.
    -   Alle kosten voor directe productie worden financieel bijgewerkt. Alle kanbanprocestaken die tijdens de periode worden voltooid worden bij elkaar opgeteld.
    -   Alle indirecte kosten die zijn berekend voor het verbruikte materiaal binnen de periode wordt berekend en afgetrokken van het OHW. De resterende indirecte kosten worden geboekt als een afwijking.

5.  Bereken de productieafwijkingen van standaardkosten. De afwijking wordt berekend per kostengroep.





