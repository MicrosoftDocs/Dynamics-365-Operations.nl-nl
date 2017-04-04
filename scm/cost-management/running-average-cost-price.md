---
title: Lopend gemiddelde kostprijs
description: Het voorraadafsluitingsproces vereffent uitgiftetransacties naar ontvangsttransacties op basis van de voorraadwaarderingsmethode die is geselecteerd in de artikelmodelgroep van het artikel. Voordat de voorraadafsluiting wordt uitgevoerd, berekent het systeem een lopend gemiddelde kostprijs die meestal gebruikt wordt bij het boeken van uitgiftetransacties.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Lopend gemiddelde kostprijs

Het voorraadafsluitingsproces vereffent uitgiftetransacties naar ontvangsttransacties op basis van de voorraadwaarderingsmethode die is geselecteerd in de artikelmodelgroep van het artikel. Voordat de voorraadafsluiting wordt uitgevoerd, berekent het systeem een lopend gemiddelde kostprijs die meestal gebruikt wordt bij het boeken van uitgiftetransacties.

Het systeem maakt een schatting van deze lopend gemiddelde kostprijs voor een artikel met behulp van de volgende formule: geschatte prijs = (fysiek bedrag + financieel bedrag) ÷ (fysieke hoeveelheid + financiële hoeveelheid)

## <a name="using-the-running-average-cost-price"></a>De lopende gemiddelde kostprijs gebruiken
De volgende tabel ziet wanneer het systeem voorraadtransacties met behulp van de lopende, gemiddelde kostprijs geboekt en wanneer de kostprijs die is gedefinieerd in de hoofdrecord van het artikel in plaats daarvan wordt gebruikt.

| Voorwaarde                                               | Het systeem gebruikt de geschatte lopend gemiddelde kostprijs | De kostprijs die is gedefinieerd in de hoofdrecord van het artikel wordt gebruikt |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Beide teller\* en een noemer\*\* positief zijn.  | Ja                                                      | Nee                                                                |
| De teller\*, noemer\*\*, of beide negatief zijn. | Nee                                                       | Ja                                                               |
| De noemer\*\* 0 (nul).                        | Nee                                                       | Ja                                                               |

\*Teller = (fysiek bedrag + financieel bedrag) \*\*noemer = (fysieke hoeveelheid + financiële hoeveelheid) **opmerking:** als de **de optie fysieke waarde opnemen** voor een artikel niet is geselecteerd, wordt 0 (nul) gebruikt voor zowel het fysieke bedrag als de fysieke hoeveelheid. Zie voor informatie over deze optie [Fysieke waarde opnemen](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Prijsverhoging voorkomen
In zeldzame gevallen kan prijs het systeem van verschillende uitgiften voordat voldoende ontvangsten wilt baseren, de prijs. Dit scenario kan ertoe leiden dat ramingen van de lopende gemiddelde kostprijs te hoog worden. Er zijn echter maatregelen die u kunt nemen om prijsverhoging te voorkomen of om de invloed ervan te reduceren wanneer het voorkomt. **Scenario** De volgende transacties treden op voor een artikel waarvoor u de optie **Fysieke waarde opnemen** hebt geselecteerd:

1.  U ontvangt financieel een hoeveelheid van 100 tegen EUR 100,00.
2.  U geeft financieel een hoeveelheid van 200 uit.
3.  U ontvangt fysiek een hoeveelheid van 101 tegen EUR 202,00.

Wanneer u de geschatte lopend gemiddelde kostprijs voor het artikel bestudeert, verwacht u een kostprijs van EUR 1,51. U vindt in plaats daarvan een geschatte lopend gemiddelde van USD 102.00, die is gebaseerd op de volgende formule: geschatte prijs = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 deze prijzen prijsverhogende komt doordat, wanneer er 200 artikelen financieel zijn uitgegeven bij stap 2, het systeem moet prijs met 100 van de artikelen voordat de bijbehorende ontvangsten. Dit resulteert in een negatieve voorraad. Het systeem vervolgens maakt een schatting van een eenheidsprijs van USD 1.00, zoals te verwachten. Echter, wanneer de bijbehorende 100 ontvangsten binnenkomen, hebben ze een eenheidsprijs van EUR 2,00. **Opmerking:** hoewel de uitgiften een negatieve voorraad veroorzaken, is de voorraad positief op het moment dat de uitgifteprijs wordt berekend. Dat is de reden waarom de lopend gemiddelde kostprijs wordt gebruikt in plaats van de prijs uit de hoofdrecord van het artikel. Op dit moment is een voorraadwaardetegenboeking van USD 100.00. Hoewel die tegenboeking is opgebouwd over 100 stuks, met een eenheidtegenboeking van EUR 1,00 per stuk, is er nu slechts één stuk in voorraad. De tegenboeking van EUR 100,00 wordt daarom toegewezen aan dit ene stuk. Dit resulteert in een te hoge geraamde kostprijs. **Opmerking:** merk ter vergelijking op dat als stap 2 en 3 in het scenario worden omgekeerd, er 200 artikelen worden uitgegeven met een eenheidsprijs van EUR 1,51 en één stuk de eenheidsprijs van EUR 1,51 behoudt. Aangezien dit prijsverhogingsscenario kan optreden wanneer er negatieve voorraad is, is het moeilijk te voorkomen in de volgende gevallen:

-   U moet uitgifteprijzen schatten voor de voorhanden waarde en hoeveelheid.
-   U moet de voorhanden waarde en hoeveelheid aanpassen voor uitgiften en ontvangsten.
-   Uw bedrijfsmodel staat het verzenden, of het bepalen van de prijs, van meer stuks dan u hebt toe.
-   U moet elke ontvangstwaarde en -hoeveelheid die naar u wordt verzonden, accepteren.

Als uw bedrijfsmodel echter de volgende procedures toestaat, kunt u deze gebruiken om de negatieve hoeveelheden te voorkomen die het prijsverhogende scenario mogelijk maken:

-   Als u de optie **Fysieke waarde opnemen** voor een artikel selecteert, schakelt u het selectievakje **Fysieke negatieve voorraad** uit op de pagina **Artikelmodelgroepen**.
-   Als u de optie **Fysieke waarde opnemen** voor een artikel *niet* selecteert, schakelt u het selectievakje **Fysieke negatieve voorraad** op de pagina **Artikelmodelgroepen** uit.

Houd er ook rekening mee dat de maximumtegenboeking in uw fysieke voorraadwaarde wordt beperkt door het aantal fysieke transacties en door het verschil tussen fysieke en financiële prijzen. Zolang alle fysieke transacties uiteindelijk financieel worden bijgewerkt, kan de fysieke waarde niet extreem hoog worden. Bovendien blijft het verhogende effect aanzienlijk beperkt wanneer de cumulatieve tegenboeking wordt verdeeld over een aantal voorhanden eenheden in plaats van deze toe te wijzen aan één eenheid.


