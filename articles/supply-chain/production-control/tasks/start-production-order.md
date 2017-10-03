--- 
title: Een productieorder starten
description: Deze procedure toont hoe u een productieorder start op de werkvloer.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: a88968072b28ab468af97a875bd76d4d6abecfde
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="start-a-production-order"></a>Een productieorder starten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een productieorder start op de werkvloer. Tijd- en materiaalverbruik worden in dit proces gerapporteerd. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de vijfde procedure van zeven waarin de levenscyclus van de productieorder wordt uitgelegd.


## <a name="start-a-production-order"></a>Een productieorder starten
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
    * Selecteer een productieorder met de status Vrijgegeven.  
2. Klik in het actievenster op Productieorder.
3. Klik op Start.
    * Op deze pagina kunt u de start van de productieorder bevestigen.  
4. Klik op het tabblad Algemeen.
5. Voer in het veld Van Nr. '10' in.
6. Selecteer 'Altijd' in het veld Automatisch routeverbruik.
7. Klik op het selectievakje Routekaart nu boeken.
8. Selecteer 'Altijd' in het veld Automatisch stuklijstverbruik.
9. Klik op het selectievakje Orderverzamellijst nu boeken.
10. Klik op het selectievakje Orderverzamellijst afdrukken.
11. Klik op OK.
    * Dit is de afgedrukte orderverzamellijst die de materialen bevat die worden gebruikt voor de productieorder.  
12. Sluit de pagina.

## <a name="validate-the-picking-list"></a>De orderverzamellijst valideren
1. Klik in het actievenster op Weergeven.
2. Klik op Orderverzamellijst.
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op Bewerken.
6. Voer een getal in het veld Verbruik in.
7. Klik op Boeken.
8. Klik op OK.
    * In het orderverzamellijstjournaal worden de materialen geboekt die worden verbruikt door de productieorder. Voordat u het journaal boekt, kunt u correcties aanbrengen als er een verschil is tussen de geschatte hoeveelheid en de werkelijke verbruikte hoeveelheid.  
9. Klik op het tabblad Rasterdeelvenster.
10. Sluit de pagina.

## <a name="verify-the-route-card-journal"></a>Het routekaartjournaal verifiëren
1. Klik in het actievenster op Weergeven.
2. Klik op Routekaart.
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op Bewerken.
6. Voer een getal in het veld Uren in.
7. Klik op Boeken.
8. Klik op OK.
    * In het routekaartjournaal wordt de bestede tijd voor de afzonderlijke bewerkingen vastgelegd. Goede en foutieve hoeveelheid kan ook worden gerapporteerd.  


