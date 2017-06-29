---
title: Kostprijsberekeningsbladen
description: Het instellen van het kostenblad heeft twee doelen. Ten eerste definieert u de indeling voor het weergeven van informatie over kosten van verkochte goederen voor een gefabriceerd artikel of een productieorder. De ingedeelde weergave wordt een kostenblad genoemd. Ten tweede definieert u de basis voor het berekenen van de indirecte kosten. Bij het instellen van het kostenblad wordt gebruikgemaakt van de kostengroepfunctie voor het weergeven van informatie en voor de formules voor het berekenen van indirecte kosten. De twee doelen van het instellen van het kostenblad worden in dit artikel beschreven.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostSheetDesigner
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ff9bde25a2e1785d7063f8c69f673d87abbd948b
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="costing-sheets"></a>Kostprijsberekeningsbladen

[!include[banner](../includes/banner.md)]


Het instellen van het kostenblad heeft twee doelen. Ten eerste definieert u de indeling voor het weergeven van informatie over kosten van verkochte goederen voor een gefabriceerd artikel of een productieorder. De ingedeelde weergave wordt een kostenblad genoemd. Ten tweede definieert u de basis voor het berekenen van de indirecte kosten. Bij het instellen van het kostenblad wordt gebruikgemaakt van de kostengroepfunctie voor het weergeven van informatie en voor de formules voor het berekenen van indirecte kosten. De twee doelen van het instellen van het kostenblad worden in dit artikel beschreven. 

Een kostenblad is de opgemaakte weergave van informatie over kosten van verkochte goederen voor een gefabriceerd artikel of een productieorder. Wanneer u een kostenblad instelt, definieert u de indeling voor de informatie en bepaalt u ook de basis voor het berekenen van indirecte kosten. Bij het instellen van het kostenblad wordt gebruikgemaakt van de kostengroepfuncties voor het weergeven van informatie en voor de formules voor het berekenen van indirecte kosten. Hier is meer informatie over de volgende twee doelen van kostenbladinstellingen:
-   **De indeling definiëren van het kostenblad.** Met de door de gebruiker gedefinieerde indeling voor een kostenblad wordt de segmentatie bepaald van de kosten van verkochte goederen voor een gefabriceerd artikel. Bijvoorbeeld: de informatie over de kosten van verkochte goederen voor het artikel kan worden opgesplitst in de segmenten Materiaal, Arbeid en Overhead op basis van kostengroepen. Deze kostengroepen zijn toegewezen aan artikelen, kostencategorieën voor routebewerkingen en formules voor de berekening van de indirecte kosten. Voor de indeling van het kostenblad zijn meestal subtotalen vereist wanneer er meerdere kostengroepen zijn gedefinieerd. Bijvoorbeeld: meerdere kostengroepen die zijn gerelateerd aan materiaal kunnen worden samengevoegd. De definitie van de indeling van het kostenblad is optioneel, maar deze indeling moet wel worden gedefinieerd als u de indirecte kosten wilt berekenen.
-   **De basis definiëren voor het berekenen van de indirecte kosten.** Indirecte kosten staan voor de overheadkosten die zijn gekoppeld aan de productie van een gefabriceerd artikel. Een formule voor de berekening van de indirecte kosten kan worden uitgedrukt als toeslag of als een tarief. Een toeslag vertegenwoordigt een percentage van een waarde, terwijl een tarief een bedrag per uur voor een routebewerking vertegenwoordigt. Met een kostengroep wordt de basis gedefinieerd voor de berekeningsformule, bijvoorbeeld een toeslag van 100 procent voor een arbeidskostengroep of een uurtarief van EUR 50,00 voor een machinekostengroep. Als u een berekeningsformule en de bijbehorende kostengroepbasis wilt definiëren, moet u bij het instellen van het kostenblad de kostengroep die voor de overheadkosten staat identificeren en selecteren of een toeslag- of tariefbenadering wordt gebruikt.

U moet elke berekeningsformule invoeren als een kostenrecord. De kostenrecord bestaat uit een opgegeven kostprijsberekeningsversie, een toeslagpercentage of een tariefbedrag, de kostengroepbasis, een status en een begindatum. Wanneer een kostenrecord wordt ingevoerd, heeft deze de status **In behandeling** en een begindatum. Wanneer u de kostenrecord activeert, wordt de status bijgewerkt zodat de record de huidige actieve record is, en wordt de begindatum gewijzigd in de activeringsdatum. De kostenrecord kan een locatie aanduiden voor een locatiespecifieke berekeningsformule. Als alternatief kunt u het veld **Locatie** leeg laten om aan te geven dat de berekeningsformule een formule voor het hele bedrijf is. De kostenrecord kan eventueel bestaan uit een opgegeven artikel of artikelengroep wanneer de berekeningsformule is gemarkeerd als een formule 'per artikel'. 

De huidige actieve kostenrecords voor berekeningsformules voor indirecte kosten worden gebruikt om productieorderkosten te schatten. Ze worden ook gebruikt voor het berekenen van de werkelijke kosten die gerelateerd zijn aan het werkelijke verbruik van tijd en materiaal. De kostenrecords die in behandeling zijn worden gebruikt in stuklijstberekeningen voor een toekomstige datum. 

Twee blokkeringsbeleidsregels voor een kostprijsberekeningsversie bepalen of kosten die in behandeling zijn, kunnen worden bijgehouden en of deze kunnen worden gestart. Gebruik de blokkeringsbeleidsregels om gegevensonderhoud toe te staan en vervolgens om gegevensonderhoud voor de kostengegevens in een kostprijsberekeningsversie te voorkomen. 

Nadat u de indeling voor het kostenblad en de berekeningen voor de indirecte kosten hebt gedefinieerd, moet u een extra stap uitvoeren om de gegevens te valideren en op te slaan. Het kostenblad is een indeling voor het hele bedrijf die ervoor moet zorgen dat de informatie over de kosten van verkochte goederen consistent wordt weergegeven. 

Het kostenblad wordt weergegeven als onderdeel van de pagina **Artikelkosten berekenen**. Het kostenblad kan worden weergegeven voor de berekende kostenrecord van een gefabriceerd artikel op de pagina **Artikelprijs** of voor een orderspecifieke berekeningsrecord op de pagina **Resultaten stuklijstberekening**. Het kostenblad wordt ook weergegeven als onderdeel van de pagina **Prijsberekening** voor een productieorder.






