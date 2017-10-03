---
title: Vrachttransportroutes met meerdere tussenstops plannen
description: Dit artikel beschrijft de verschillende elementen die u kunt gebruiken voor het plannen van transportroutes in Microsoft Dynamics 365 for Finance and Operations.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: e7965c094f91bcbcad21ecfa599f133a6e84f4f7
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Vrachttransportroutes met meerdere tussenstops plannen

[!include[banner](../includes/banner.md)]


Dit artikel beschrijft de verschillende elementen die u kunt gebruiken voor het plannen van transportroutes in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

U kunt routeplannen en routerichtlijnen gebruiken voor complexe transportroutes met meerdere tussenstops. Als dezelfde route regelmatig wordt gebruikt, kunt u een geplande route instellen.

## <a name="route-plans"></a>Routeplannen
Een routeplan bevat routesegmenten die informatie bieden over dee tussenstops die worden gemaakt op de route en de vervoerders die worden gebruikt voor elk segment. U moet de tussenstops op de route definiëren als hubs. Een hub is een leverancier, een magazijn, een klant of zelfs gewoon een herlaadlocatie waar u van vervoerder wisselt. U kunt voor elk segment "plaatstarieven" voor diverse toeslagen definiëren. Hieronder vindt u enkele voorbeelden:

-   Toeslagen voor reizen naar de opgegeven segmenten
-   Toeslagen voor het oppikken van de goederen
-   Toeslagen voor het afleveren van de goederen

Elk routeplan moet worden gekoppeld aan een routerichtlijn.

## <a name="route-guides"></a>Routerichtlijnen
Een routerichtlijn definieert de criteria voor het afstemmen van een laden op een specifiek routeplan. U kunt bijvoorbeeld een oorspronghub en een bestemmingshub opgeven, alsmede limieten voor het containervolume of -gewicht en een vervoerder, service of groep. Routerichtlijnen zijn beschikbaar op de pagina **Workbench tariefroute**, waarbij ladingen handmatig of automatisch kunnen worden afgestemd op routes. Als de routerichtlijn bestemd is voor een geplande route, is deze ook beschikbaar op de pagina **Workbench voor ladingopbouw**.

## <a name="scheduled-routes"></a>Geplande routes
Een geplande route is een vooraf gedefinieerd routeplan met een planning voor de verzenddatums. Geplande routes en niet-geplande routes verschillen in de manier waarop ladingen eraan worden toegewezen. Als u een niet-geplande route toewijst via de tariefroute-workbench, worden alleen de lading en de routerichtlijn gevalideerd. Als u een geplande route toewijst, worden de datums en adressen van de orders en de hubs, en de datum op het routerouterichtlijn eveneens in overweging genomen. U hoeft geen gebruik van de tariefroute-workbench te maken om handmatig ladingen toe te wijzen aan een geplande route. In plaats daarvan kunt u de workbench voor ladingopbouw gebruiken om te suggereren dat ladingen worden opgebouwd op basis van de klantadressen en de leveringsdatums van verkooporders voor een bepaalde geplande route. Bij geplande routes heeft het routeplan vaste oorsprong- en bestemmingshubs. Meestal zijn de vervoerder en de service gelijk voor alle segmenten, maar deze kunnen verschillen. De bestemmingshubs worden gemaakt met behulp van de postcodes van de klanten die op de route worden bezocht. Verschillende routeschema's kunnen worden gedefinieerd voor één routeplan. Het routeplan moet worden gekoppeld aan een routerichtlijn. Bij geplande routes kan het plan echter worden gekoppeld aan slechts één routerichtlijn. Het routeschema wordt alleen gebruikt om de werkelijke routes te maken op de pagina **Routeplanning**. Kunt u de standaardladingsjabloon gebruiken bij het voorstellen van ladingen in de workbench voor ladingopbouw.

## <a name="load-building-workbench"></a>Workbench voor ladingopbouw
De workbench voor ladingopbouw maakt gebruik van de adressen van klanten en de leveringsdatums van verkooporders en de geplande routes die beschikbaar zijn om een lading voor te stellen. Standaard worden de waarden van de route ingevoerd in de workbench. U kunt echter een 'van'-datum selecteren die eerder valt dan de 'van'-datum op de route. Wanneer een lading wordt voorgesteld, worden het afleveradres en de leveringsdatum van alle openstaande verkooporders gecontroleerd. Als de postcode van het afleveradres overeenkomt met de postcode van een hub in het routeplan, en de leveringsdatum binnen het bereik ligt dat is geselecteerd in de criteria, wordt de verkooporder voorgesteld voor de lading. Ook wordt rekening gehouden met de capaciteit van de ladingsjabloon. Er wordt telkens slechts één lading tegelijk voorgesteld. Als u een verkooporder hebt die niet is opgenomen, is het mogelijk dat u een andere ladingsjabloon gebruikt (bijvoorbeeld een ladingsjabloon voor een grotere vrachtwagen of container) of een extra levering plant.




