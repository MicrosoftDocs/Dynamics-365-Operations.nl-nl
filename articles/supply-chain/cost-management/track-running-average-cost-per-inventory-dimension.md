---
title: Lopende gemiddelde kosten per voorraaddimensie traceren
description: Er wordt aan elk voorraadartikel een voorraaddimensiegroep gekoppeld. Daarom wordt de lopende gemiddelde kostprijs voor een artikel berekend op basis van de geselecteerde voorraaddimensies die financieel worden bijgehouden.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2bf04a42edf09c35e81742b1c60db8944eba2ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252865"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Lopende gemiddelde kosten per voorraaddimensie traceren

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]