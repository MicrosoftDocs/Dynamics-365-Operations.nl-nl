---
title: Lopende gemiddelde kosten per voorraaddimensie traceren
description: Er wordt aan elk voorraadartikel een voorraaddimensiegroep gekoppeld. Daarom wordt de lopende gemiddelde kostprijs voor een artikel berekend op basis van de geselecteerde voorraaddimensies die financieel worden bijgehouden.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4f5ca047835fcbb2567f0b97347b356e1b594980
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Lopende gemiddelde kosten per voorraaddimensie traceren

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Er wordt aan elk voorraadartikel een voorraaddimensiegroep gekoppeld. Daarom wordt de lopende gemiddelde kostprijs voor een artikel berekend op basis van de geselecteerde voorraaddimensies die financieel worden bijgehouden.

Er zijn drie typen voorraaddimensies: product, opslag en tracering. Productdimensies zijn onder andere configuratie, grootte en kleur. Productdimensies worden altijd financieel bijgehouden. Opslag- en traceringsdimensies zijn onder andere site, magazijn, locatie, voorraadstatus, nummerbord, batchnummer en serienummer. U kunt bepalen welke opslag- en traceringsdimensies financieel worden bijgehouden. 

**Voorbeeld 1** 

Als de opslagdimensiegroep die aan het artikel is gekoppeld, financieel wordt bijgehouden door het magazijn, wordt de lopende, gemiddelde kostprijs per magazijn berekend. De volgende inkooporders zijn gefactureerd:

-   Een inkooporder voor 2 stuks tegen een kostprijs van EUR 10,00 is gefactureerd voor magazijn GW.
-   Een inkooporder voor 3 stuks tegen een kostprijs van EUR 12,00 is gefactureerd voor magazijn GW.
-   Een inkooporder voor 5 stuks tegen een kostprijs van EUR 15,00 is gefactureerd voor magazijn MW.

De lopende gemiddelde kostprijs voor magazijn GW is EUR 11,20 en de lopende gemiddelde kostprijs voor magazijn MW is EUR 15,00. Een verkooporderfactuur wordt geboekt voor magazijn GW. De waarde van de voorraad en van de kosten van de verkochte artikelen (voordat de voorraadafsluiting zonder markering wordt uitgevoerd) is EUR 11,20. Een andere verkooporder wordt geboekt voor magazijn MW. De waarde van de voorraad en van de kosten van de verkochte artikelen (voordat de voorraadafsluiting zonder markering wordt uitgevoerd) is EUR 15,00. 

**Voorbeeld 2** Als de opslagdimensiegroep die aan het artikel is gekoppeld financieel wordt bijgehouden door het magazijn en de traceringsdimensiegroep financieel wordt bijgehouden op batchnummer, wordt de lopende gemiddelde kostprijs berekend voor elke batch. 

**Opmerking:** Wij raden u aan altijd de kostprijs te bekijken voor alle financiële dimensies die worden bijgehouden. De volgende inkooporders zijn gefactureerd:

-   Een inkooporder voor 2 stuks tegen een kostprijs van EUR 10,00 is gefactureerd voor magazijn GW en batch AAA.
-   Een inkooporder voor 3 stuks tegen een kostprijs van EUR 12,00 is gefactureerd voor magazijn GW en batch AAA.
-   Een inkooporder voor 2 stuks tegen een kostprijs van EUR 15,00 is gefactureerd voor magazijn GW en batch BBB.

De lopende gemiddelde kostprijs voor magazijn GW en batch AAA is EUR 11,20 en de lopende gemiddelde kostprijs voor magazijn GW en batch BBB is EUR 15,00.



