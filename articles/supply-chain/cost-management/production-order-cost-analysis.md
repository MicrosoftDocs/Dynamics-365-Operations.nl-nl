---
title: Analyse van productieorderkosten
description: Dit artikel bevat informatie over de kostprijsanalyse die u voor voltooide en huidige productieorders kunt uitvoeren. U kunt de geraamde en werkelijke kosten analyseren met de pagina Prijsberekening of het rapport Geraamde kosten en kostprijsberekeningen. U kunt informatie weergeven over de geraamde en werkelijke kosten (en hoeveelheid) voor alle onderdeelartikelen, de routebewerkingen en de indirecte kosten.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage, ProdSetupHistoricalCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12e9446c145752cd74fb71884fcabe9d4bd03c68
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187693"
---
# <a name="production-order-cost-analysis"></a>Analyse van productieorderkosten

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over de kostprijsanalyse die u voor voltooide en huidige productieorders kunt uitvoeren. U kunt de geraamde en werkelijke kosten analyseren met de pagina Prijsberekening of het rapport Geraamde kosten en kostprijsberekeningen. U kunt informatie weergeven over de geraamde en werkelijke kosten (en hoeveelheid) voor alle onderdeelartikelen, de routebewerkingen en de indirecte kosten.

De werkelijke kosten voor een productieorder zijn gebaseerd op het gerapporteerde verbruik van materiaal en routebewerkingen. U kunt op de pagina **Productieboeking** gedetailleerde transacties weergeven voor het gerapporteerde verbruik van materiaal, routebewerkingen en indirecte kosten voor een productieorder.

## <a name="variance-analysis-for-a-completed-production-order"></a>Afwijkingsanalyse voor een afgeronde productieorder
De afwijkingen weerspiegelen een vergelijking tussen de gemelde productieactiviteiten en de berekening van de standaardkostprijs voor het productieartikel. De afwijkingen vertegenwoordigen geen vergelijking voor de geschatte kosten van de productieorder. De productieactiviteiten die worden gemeld omvatten het verbruik van materialen en routebewerkingen, samen met de bijbehorende indirecte kosten en de hoeveelheid die is gereedgemeld. De volgende vier typen afwijkingen worden berekend:

-   Afwijking partijgrootte
-   Afwijking productiehoeveelheid
-   Productieprijsafwijking
-   Afwijking productievervanging

In het volgende diagram worden de vier afwijkingen getoond die voor het verschil tussen de werkelijke kosten van een productieorder en de berekende kosten zorgen binnen het kostenrecord van het artikel wanneer de productieorder wordt beëindigd. 

![Afwijkingen waarbij rekening wordt gehouden met verschillen in een voltooide productieorder](./media/control.jpg) 

U kunt de productieafwijkingen analyseren met behulp van de pagina **Afwijking** of het rapport **Productieafwijking**. Gebruik de weergaveopties om gedetailleerde afwijkingen volgens artikel- en bewerkingsresource of per kostengroep weer te geven. Het beleid voor de verdeling van de kosten in de voorraadparameters bepaalt of de afwijkingen per kostengroep worden bijgehouden. U kunt ook de weergaveopties **enkel**, **meerdere** en **totaal** gebruiken om samengevatte afwijkingen weer te geven. De informatie over gedetailleerde afwijkingen helpt u van de bron van elke afwijking te begrijpen. Als u vóór het beëindigen van een productieorder afwijkingen wilt voorspellen, moet u de gedetailleerde gegevens uit het rapport **Geraamde kosten en kostprijsberekeningen** analyseren.

## <a name="cost-analysis-for-current-production-orders"></a>Kostenanalyse voor huidige productieorders
Er zijn afzonderlijke rapporten beschikbaar met informatie over elk transactietype. Gebruik deze rapporten om kosten te analyseren voor gerapporteerde productieactiviteiten. Er wordt alleen informatie weergegeven voor huidige productieorders met de status **Gestart** of **Gereedgemeld**.

-   **Materialen in bewerking**: dit rapport bevat orderverzamellijsttransacties die voor de huidige productieorders zijn gerapporteerd vanaf een bepaalde transactiedatum. Het rapport geeft de uitgegeven hoeveelheid van een onderdeel aan en de kostprijs voor elke transactie. Gebruik de selectiecriteria voor één onderdeelartikel. U kunt bijvoorbeeld informatie over de uitgegeven hoeveelheid van het onderdeel afdrukken voor relevante productieorders. De uitgegeven hoeveelheid wordt niet bijgewerkt door de gereedgemelde hoeveelheden voor het bovenliggende artikel. Daarom is de huidige hoeveelheid van grondstoffen in bewerking mogelijk te groot.
-   **Onderhanden werk**: dit rapport bevat routetransacties (of taaktransacties) die voor de huidige productieorders zijn gerapporteerd vanaf een bepaalde transactiedatum. Het rapport vermeldt de uren, het bedrag, en de hoeveelheid (zowel goede hoeveelheid als fouthoeveelheid) die voor elke transactie zijn gerapporteerd. Het bevat ook informatie zoals het bewerkingsnummer, de bewerkings-id en de bron voor bedrijfsactiviteiten. In het rapport wordt ook de totale tijd en het totale bedrag voor alle transacties voor de productieorder weergegeven en de hoeveelheid die is gereedgemeld.
-   **Indirecte kosten in verwerking**: dit rapport geeft de indirecte kosten weer die zijn gemaakt voor productieorders. Deze gegevens zijn gebaseerd op gerapporteerd verbruik van routebewerkingen en onderdelen vanaf een bepaalde transactiedatum. Het rapport geeft het type indirecte kosten aan (toeslag of tarief), de kostprijsberekeningscode voor de indirecte kosten en de kostprijs voor elke transactie. Het rapport bevat geen informatie over de routekaart- of orderverzamellijsttransactie waardoor de indirecte kosten zijn gegenereerd.
-   **Onderhanden productiekosten**: dit rapport geeft het gecombineerde verbruik weer van materiaal, routebewerkingen en indirecte kosten voor de productieorders vanaf een bepaalde transactiedatum.
-   **Gerede artikelen in bewerking**: dit rapport geeft huidige productieorders weer, evenals de gereedgemelde transacties vanaf een bepaalde transactiedatum.


## <a name="additional-resources"></a>Aanvullende resources

[Veelvoorkomende oorzaken voor productieafwijkingen analyseren](common-sources-of-production-variances.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]