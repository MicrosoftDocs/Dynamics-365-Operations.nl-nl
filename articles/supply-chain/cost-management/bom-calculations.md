---
title: Berekening van de vrije voorraad (BOM)
description: De kostenaggregatie- en verkoopprijsberekeningen worden stuklijstberekeningen genoemd en u start ze vanaf de pagina Berekeningen. Dit onderwerp biedt informatie over stuklijstberekeningen.
author: AndersGirke
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: a718a2e825630ccfaa54ff9dece1d3d19d59018c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425647"
---
# <a name="bom-calculations"></a>Berekening van de vrije voorraad (BOM)

[!include [banner](../includes/banner.md)]

De kostenaggregatie- en verkoopprijsberekeningen worden stuklijstberekeningen genoemd en u start ze vanaf de pagina Berekeningen. Dit onderwerp biedt informatie over stuklijstberekeningen.

De kostenaggregatie- en verkoopprijsberekeningen worden stuklijstberekeningen genoemd en u start ze vanaf de pagina **Berekeningen**. Gebruik de pagina **Berekeningen** om de volgende taken uit te voeren:

-   De kosten berekenen van een gefabriceerd artikel en een bijbehorende record voor de kosten van het artikel genereren binnen een kostprijsberekeningsversie.
-   De verkoopprijs van een gefabriceerd artikel berekenen en een bijbehorende record met de verkoopprijs van het artikel genereren binnen een kostprijsberekeningsversie.

De manier waarop u de pagina **Berekeningen** gebruikt, verschilt iets, afhankelijk van hoe u de stuklijstberekeningen start. De manier waarop u de pagina **Berekeningen** gebruikt hangt ook af van het feit of er bij de stuklijstberekeningen sprake is van een kostprijsberekeningsversie voor standaardkosten of geplande kosten, en van de diverse beleidsregels die zijn gedefinieerd in de kostprijsberekeningsversie die bij de stuklijstberekeningen wordt gebruikt. **Opmerking:** een variatie van de pagina **Berekeningen** wordt gebruikt in de context van een verkooporder, verkoopofferte of serviceorderregelitem. Deze berekeningen worden orderspecifieke stuklijstberekeningen genoemd. Een orderspecifieke stuklijstberekening genereert geen artikelkostenrecord binnen een kostprijsberekeningsversie. In plaats daarvan wordt een berekeningsrecord gegenereerd die wordt weergegeven op de pagina **Details van stuklijstberekening**. In de berekeningsrecord staan de berekende kosten en de berekende verkoopprijs. De pagina **Berekeningen** kan worden geopend voor een enkele kostprijsberekeningsversie of voor een enkel geproduceerd artikel.

-   U kunt kosten voor een enkele gefabriceerd artikel berekenen door stuklijstberekeningen te starten vanaf de pagina **Artikelprijs**. De pagina **Berekeningen** neemt de id van het artikel over. De kostprijsberekeningsversie, stuklijstversie, routeversie, berekeningshoeveelheid, berekeningsdatum en site moeten worden opgegeven.
    -   Standaard worden de stuklijstversie en routeversie ingesteld op de actieve versies voor artikel, locatie, datum en berekeningshoeveelheid. U kunt echter de standaardwaarden overschrijven met goedgekeurde versies.
    -   Standaard wordt de berekeningshoeveelheid ingesteld op de standaardorderhoeveelheid van het artikel. U kunt de standaardwaarde echter overschrijven.
    -   De berekeningsdatum of site kan door de kostprijsberekeningsversie zijn voorgeschreven of er kunnen door gebruikers opgegeven waarden worden ingesteld wanneer de datum of site niet in de kostprijsberekeningsversie is voorgeschreven. Een aanstaande berekeningsdatum bepaalt hoe in behandeling zijnde kostenrecords worden gebruikt. Bij stuklijstberekeningen wordt een in behandeling zijnde kostenrecord gebruikt waarvan de dichtstbijzijnde begindatum op of vóór de berekeningsdatum valt.
-   Als u kosten wilt berekenen voor alle gefabriceerde artikelen of geselecteerde artikelen of als u artikelen wilt bijwerken op basis van de gebruikslocatie, start u stuklijstberekeningen vanaf de pagina **Instellingen kostprijsberekeningsversie** of de pagina **Onderhoud kostprijsberekeningsversie**. De pagina **Berekeningen** neemt de kostprijsberekeningsversie over.
    -   Bij de berekeningen wordt ervan uitgegaan dat de actieve stuklijstversie en routeversie worden gebruikt voor een gefabriceerd artikel (en voor de gerelateerde site, datum en hoeveelheid), tenzij er voor een gefabriceerd onderdeel een opgegeven substuklijst of subroute is.
    -   Voor de berekeningen wordt ervan uitgegaan dat de standaardorderhoeveelheid wordt gebruikt voor gefabriceerde artikelen. De standaardorderhoeveelheid biedt de basis voor het berekenen van de aantallen onderdelen, het bepalen van de relevante stuklijst- en routeversies (wanneer de aantallen die u gebruikt, afhangen van de stuklijsten en routes) en het afschrijven van de constante kosten. Wanneer echter een gefabriceerd onderdeel een stuklijstregeltype **Productie** of **Leverancier** heeft of wanneer u een explosiemodus 'maken naar order' gebruikt voor de stuklijstberekeningen, geldt deze veronderstelling niet omdat de hoeveelheden de opgegeven hoeveelheid berekening weergeven.
    -   De berekeningsdatum of site kan door de kostprijsberekeningsversie zijn voorgeschreven of er kunnen door gebruikers opgegeven waarden worden ingesteld wanneer de datum of site niet in de kostprijsberekeningsversie is voorgeschreven.

Andere varianten in stuklijstberekeningen geven het kostentype en de beperkingen van de kostprijsberekeningsversie weer:

-   Stuklijstberekeningen die standaardkosten gebruiken moeten worden beperkt door het beleid voor kostprijsberekeningsversie omdat de beperkingen helpen garanderen dat standaardprincipes voor kostprijsberekeningen worden gebruikt. Voor standaardprincipes voor kostprijsberekeningen moeten de beperkingen over het gebruik van de standaardkosten van ingekochte artikelen, een explosiemodus met een enkel niveau en de opname van diverse toeslagen in eenheidskosten worden afgedwongen.
-   Stuklijstberekeningen die geplande kosten gebruiken hoeven zich daarentegen niet aan de standaardprincipes voor kostprijsberekeningen te houden. Bij deze stuklijstberekeningen worden verschillende explosiemodi, alternatieve bronnen met kosten voor ingekochte artikelen en de eventuele uitvoering van de beperkingen binnen de kostprijsberekeningsversie gebruikt.

### <a name="bom-calculations-that-use-standard-costs"></a>Stuklijstberekeningen die standaardkosten gebruiken

Beleidsregels in de kostprijsberekeningsversie (voor standaardkosten) kunnen het uitvoeren van vijf beleidsregels van stuklijstberekeningen dwingend uitvoeren. In de kostprijsberekeningsversie bepaalt de optie **Registratiebeperking** een van deze beleidsregels, waarbij diverse toeslagen in de eenheidsprijs moeten worden opgenomen. De diverse toeslagen voor ingekochte artikelen kunnen handmatig worden ingevoerd, terwijl diverse toeslagen voor gefabriceerde artikelen de berekende afschrijving van de constante kosten weergeven. In de kostprijsberekeningsversie bepaalt de optie **Berekeningsbeperking** de andere vier beleidsregels voor stuklijstberekening:

-   De bron van kostenbijdragen voor ingekochte artikelen moet op standaardkosten zijn gebaseerd. Met andere woorden, bij stuklijstberekeningen moeten de artikelkostenrecords worden gebruikt binnen de opgegeven kostprijsberekeningsversie of binnen de terugval die de standaardkosten bevat.
-   Om een nauwkeurige en consistene berekening van standaardkosten te helpen garanderen, moet de explosiemodus een modus met een enkel niveau zijn.
-   Om consistente resultaten te helpen garanderen bij het berekenen van de verkoopprijs van artikelen, moet de winstinstelling worden voorgeschreven. Er kan alleen gebruik worden gemaakt van de winstinstelling en de records met verkoopprijzen van artikelen kunnen alleen worden gegenereerd als bij de kostprijsberekeningsversie de inhoud van verkoopprijzen kan worden gebruikt.
-   Het terugvalprincipe moet worden voorgeschreven en kan worden ingesteld op **Geen**, **Actief** (voor actieve kostenrecords) of **Kostprijsberekeningsversie** (voor een opgegeven kostprijsberekeningsversie).

### <a name="bom-calculations-that-use-planned-costs"></a>Stuklijstberekeningen die geplande kosten gebruiken

Beleidsregels in de kostprijsberekeningsversie (voor geplande kosten) kunnen desgewenst het uitvoeren van vijf beleidsregels van stuklijstberekeningen dwingend uitvoeren. Het beleid kan ook alleen standaardwaarden verstrekken. In de kostprijsberekeningsversie bepaalt de optie **Registratiebeperking** of het beleid voor de stuklijstberekening over diverse toeslagen wordt voorgeschreven of als standaardwaarde zal fungeren. Diverse toeslagen kunnen eventueel in de eenheidsprijs worden opgenomen. In de kostprijsberekeningsversie bepaalt de optie **Berekeningsbeperking** of de andere vier beleidsregels voor stuklijstberekening worden voorgeschreven of als standaardwaarden zullen fungeren:

-   De bron van kostenbijdragen voor een ingekocht artikel kunnen de artikelkostenrecords binnen een kostprijsberekeningsversie zijn. De bron kan ook worden gedefinieerd door de stuklijstberekeningsgroep die aan het artikel is toegewezen. De stuklijstberekeningsgroep kan bijvoorbeeld een handelsovereenkomst over een inkoopprijs als de bron van de kostenbijdragegegevens definiëren.
-   De explosiemodus kan een modus met een enkel niveau of met meerdere niveaus zijn, de modus 'maken naar order' zijn of zijn gebaseerd op het stuklijstregelartikel. In de explosiemodus voor het stuklijstregelartikel wordt de kostenberekeningslogica voor ramingen van de productieorder gerepliceerd.
-   De winstinstelling kan zijn voorgeschreven of kan een standaardwaarde zijn. Er kan alleen gebruik worden gemaakt van de winstinstelling en de records met verkoopprijzen van artikelen kunnen alleen worden gegenereerd als bij de kostprijsberekeningsversie de inhoud van verkoopprijzen kan worden gebruikt.
-   Het terugvalprincipe kan zijn voorgeschreven of kan een standaardwaarde zijn. Het terugvalprincipe kan worden ingesteld op **Geen**, **Actief** (voor actieve kostenrecords) of **Kostprijsberekeningsversie** (voor een opgegeven kostprijsberekeningsversie).

Bij het berekenen van stuklijsten worden waarschuwingsberichten en andere typen berichten gegenereerd. De typen berichten worden bepaald door diverse beleidsregels voor stuklijstberekening. De waarschuwingsvoorwaarden worden gedefinieerd in de stuklijstberekeningsgroep die is toegewezen aan artikelen. U kunt deze waarschuwingsvoorwaarden echter overschrijven wanneer u een stuklijstberekening start. Als het terugvalprincipe wordt gebruikt, is het vaak nuttig als de terugval wordt weergegeven als informatiebericht. Wanneer u probeert berekende kosten voor artikelen met ontbrekende kostenrecords bij te werken, kan het ook handig zijn als het informatiebericht artikelen identificeert die niet zijn bijgewerkt.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Stuklijstberekeningen met behulp van het terugvalprincipe
De volgende situaties illustreren twee gebruikstoepassingen van het terugvalprincipe:

-   **Methode met twee versies voor standaardkostenupdates** - Een kostprijsberekeningsversie kan de incrementele wijzigingen voor standaardkosten bevatten, zoals in behandeling zijnde kostenrecords die nieuwe artikelen of kostenwijzigingen vertegenwoordigen. In deze situatie kan het terugvalprincipe het gebruik van de actieve standaardkosten aanduiden die bij andere kostprijsberekeningsversies horen.
-   **Simulatie van het effect van kostenwijzigingen via het gebruik van geplande kosten** - Een kostprijsberekeningsversie voor geplande kosten kan incrementele wijzigingen voor simulatiedoeleinden bevatten. Deze kostprijsberekeningsversie bevat in behandeling zijnde kostenrecords die de gesimuleerde kostenwijzigingen voor artikelen, onkostencategorieën en berekeningsformules voor indirecte kosten vertegenwoordigen. In deze situatie kan het terugvalprincipe het gebruik van de actieve standaardkosten aanduiden die bij andere kostprijsberekeningsversies horen.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Stuklijstberekening van een voorgestelde verkoopprijs
Als u de kostprijs-plus-verhoging-benadering gebruikt, weerspiegelt de berekende verkoopprijs voor een artikel de set winstinstellingspercentages die voor de stuklijstberekening is opgegeven en de kosten die zijn gekoppeld aan de onderdeelartikelen, routebewerkingen en van toepassing zijnde productieoverheadkosten van het artikel. De opslag staat voor de winstinstellingspercentages die zijn toegewezen aan kostengroepen en voor de kostengroepen die zijn toegewezen aan artikelen, kostencategorieën voor routebewerkingen en de indirecte-kostenformules voor het berekenen van de productieoverheadkosten. De verschillende sets winstinstellingspercentages zijn: **Standaard**, **Winst 1**, **Winst 2** en **Winst 3**. In de set Winst 1 kan bijvoorbeeld een winstinstellingspercentage van 50 procent worden gedefinieerd voor een kostengroep die is toegewezen aan ingekocht materiaal, en een winstinstellingspercentage van 80 procent voor een kostengroep die is toegewezen aan kostencategorieën voor routebewerkingen. De context van de stuklijstberekening bepaalt hoe de resultaten van een berekende verkoopprijs worden verwerkt:

-   **Stuklijstberekening voor een artikel en opgegeven kostprijsberekeningsversie** - de stuklijstberekening genereert een verkoopprijsrecord die in behandeling is, binnen de kostprijsberekeningsversie. Deze verkoopprijsrecord vormt het beginpunt voor de weergave van de berekeningsdetails (bijvoorbeeld op de pagina **Artikelkosten berekenen**). De verkoopprijsrecord dient hoofdzakelijk als referentie en wordt niet gebruikt als basis voor een verkoopprijs op verkooporders.
-   **Orderspecifieke stuklijstberekening** - een variant van de pagina **Stuklijstberekening** wordt gebruikt in de context van een verkooporder, verkoopofferte of serviceorderregelartikel. Met een orderspecifieke stuklijstberekening wordt geen kostprijsrecord in een kostprijsberekeningsversie gegenereerd. In plaats daarvan wordt een berekeningsrecord gegenereerd die wordt weergegeven op de pagina **Resultaten stuklijstberekening**. Deze berekeningsrecord vormt het beginpunt voor de weergave van de berekeningsdetails (bijvoorbeeld op de pagina **Artikelkosten berekenen**). Informatie over een geselecteerde berekeningsrecord kan naar het oorspronkelijke regelartikel worden overgeboekt. De berekende verkoopprijs kan bijvoorbeeld worden overgeboekt naar een verkooporderregelartikel.

## <a name="order-specific-bom-calculations"></a>Orderspecifieke stuklijstberekeningen
Een orderspecifieke stuklijstberekening is een variatie op een stuklijstberekening voor een gefabriceerd artikel. De orderspecifieke stuklijstberekening wordt uitgevoerd in de context van een verkooporder, verkoopofferte of serviceorderregelartikel. Een orderspecifieke stuklijstberekening genereert een berekeningsrecord die wordt weergegeven op de pagina **Resultaten stuklijstberekening**. De berekeningsrecord bevat het berekende gewicht, de berekende kosten die op actieve kostenrecords zijn gebaseerd, en de berekende verkoopprijs. De berekeningsrecord die door elke orderspecifieke stukgoedberekening wordt gegenereerd voor een artikel op de pagina **Resultaten van formuleberekening** wordt uniek geïdentificeerd door een berekeningsnummer. Het resultaat van een berekeningsrecord kan desgewenst worden overgeboekt naar het oorspronkelijke regelartikel. Een orderspecifieke stuklijstberekening verschilt op twee manieren van een stuklijstberekening voor een gefabriceerd artikel:

-   Een orderspecifieke stuklijstberekening genereert geen artikelkostenrecord binnen een kostprijsberekeningsversie. Daarom worden de beleidsregels voor stuklijstberekening niet toegepast bij het maken van een artikelkostenrecord of bij het overschrijven van een kostenrecord.
-   Een orderspecifieke stuklijstberekening maakt altijd gebruik van de actieve kostenrecords voor onderdelen, kostencategorieën en berekeningsformules voor indirecte kosten.





