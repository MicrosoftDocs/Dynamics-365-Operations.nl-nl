---
title: Lopend gemiddelde kostprijs
description: Met het proces voor het afsluiten van voorraden worden uitgiftetransacties vereffend met ontvangsttransacties op basis van de methode voor het waarderen van voorraden die in de artikelmodelgroep van het artikel is geselecteerd. Voordat de voorraadafsluiting wordt uitgevoerd, wordt echter een lopend gemiddelde kostprijs berekend die in de meeste gevallen wordt gebruikt voor het boeken van uitgiftetransacties.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 53690038068d7a2cae43585fd2eb896d662ee3e4
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="running-average-cost-price"></a>Lopend gemiddelde kostprijs

[!include[banner](../includes/banner.md)]


Met het proces voor het afsluiten van voorraden worden uitgiftetransacties vereffend met ontvangsttransacties op basis van de methode voor het waarderen van voorraden die in de artikelmodelgroep van het artikel is geselecteerd. Voordat de voorraadafsluiting wordt uitgevoerd, wordt echter een lopend gemiddelde kostprijs berekend die in de meeste gevallen wordt gebruikt voor het boeken van uitgiftetransacties.

In het systeem wordt deze lopend gemiddelde kostprijs voor een artikel geschat met behulp van de volgende formule: 

Geschatte prijs = (fysiek bedrag + financieel bedrag) / (fysieke hoeveelheid + financiële hoeveelheid)

## <a name="using-the-running-average-cost-price"></a>De lopende gemiddelde kostprijs gebruiken
In de volgende tabel wordt aangegeven wanneer voorraadtransacties worden geboekt met behulp van de lopende gemiddelde kostprijs en wanneer in plaats hiervan de kostprijs wordt gebruikt die is gedefinieerd in de hoofdrecord van het artikel.

| Voorwaarde                                               | De geschatte lopende gemiddelde kostprijs wordt gebruikt | De kostprijs die is gedefinieerd in de hoofdrecord van het artikel wordt gebruikt |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Zowel de teller\* als de noemer\*\* zijn positief.  | Ja                                                      | Nee                                                                |
| De teller\*, de noemer\*\* of beide zijn negatief. | Nee                                                       | Ja                                                               |
| De noemer\*\* is 0 (nul).                        | Nee                                                       | Ja                                                               |

\* Teller = (fysiek bedrag + financieel bedragt) \*\* noemer = (fysieke hoeveelheid + financiële hoeveelheid) 

**Opmerking:** als de optie **Fysieke waarde opnemen** niet is geselecteerd voor een artikel, wordt in 0 (nul) gebruikt voor zowel het fysieke bedrag als de fysieke hoeveelheid. Zie voor informatie over deze optie [Fysieke waarde opnemen](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Prijsverhoging voorkomen
In zeldzame gevallen wordt de prijs van verschillende uitgiften bepaald voordat er voldoende ontvangsten zijn om de prijs op te baseren. Dit scenario kan ertoe leiden dat ramingen van de lopende gemiddelde kostprijs te hoog worden. Er zijn echter maatregelen die u kunt nemen om prijsverhoging te voorkomen of om de invloed ervan te reduceren wanneer het voorkomt. **Scenario** De volgende transacties treden op voor een artikel waarvoor u de optie **Fysieke waarde opnemen** hebt geselecteerd:

1.  U ontvangt financieel een hoeveelheid van 100 tegen EUR 100,00.
2.  U geeft financieel een hoeveelheid van 200 uit.
3.  U ontvangt fysiek een hoeveelheid van 101 tegen EUR 202,00.

Wanneer u de geschatte lopend gemiddelde kostprijs voor het artikel bestudeert, verwacht u een kostprijs van EUR 1,51. In plaats daarvan constateert u een geschat lopend gemiddelde van EUR 102,00, dat op de volgende formule is gebaseerd: Geschatte prijs = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102. Deze prijsverhoging treedt op omdat, wanneer er 200 artikelen financieel zijn uitgegeven bij stap 2, de prijs van 100 van de artikelen moet worden bepaald voordat er corresponderende ontvangsten zijn. Dit resulteert in een negatieve voorraad. Vervolgens wordt een eenheidsprijs van EUR 1,00 geraamd, zoals verwacht. Echter, wanneer de bijbehorende 100 ontvangsten binnenkomen, hebben ze een eenheidsprijs van EUR 2,00. 

**Opmerking:** hoewel de uitgiften een negatieve voorraad veroorzaken, is de voorraad positief op het moment dat de uitgifteprijs wordt berekend. Dat is de reden waarom de lopend gemiddelde kostprijs wordt gebruikt in plaats van de prijs uit de hoofdrecord van het artikel. Op dit moment heeft het systeem een voorraadwaardetegenboeking van USD 100,00. Hoewel die tegenboeking is opgebouwd over 100 stuks, met een eenheidtegenboeking van EUR 1,00 per stuk, is er nu slechts één stuk in voorraad. De tegenboeking van EUR 100,00 wordt daarom toegewezen aan dit ene stuk. Dit resulteert in een te hoge geraamde kostprijs. 

**Opmerking:** merk ter vergelijking op dat als stap 2 en 3 in het scenario worden omgekeerd, er 200 artikelen worden uitgegeven met een eenheidsprijs van EUR 1,51 en één stuk de eenheidsprijs van EUR 1,51 behoudt. Aangezien dit prijsverhogingsscenario kan optreden wanneer er negatieve voorraad is, is het moeilijk te voorkomen in de volgende gevallen:

-   U moet uitgifteprijzen schatten voor de voorhanden waarde en hoeveelheid.
-   U moet de voorhanden waarde en hoeveelheid aanpassen voor uitgiften en ontvangsten.
-   Uw bedrijfsmodel staat het verzenden, of het bepalen van de prijs, van meer stuks dan u hebt toe.
-   U moet elke ontvangstwaarde en -hoeveelheid die naar u wordt verzonden, accepteren.

Als uw bedrijfsmodel echter de volgende procedures toestaat, kunt u deze gebruiken om de negatieve hoeveelheden te voorkomen die het prijsverhogende scenario mogelijk maken:

-   Als u de optie **Fysieke waarde opnemen** voor een artikel selecteert, schakelt u het selectievakje **Fysieke negatieve voorraad** uit op de pagina **Artikelmodelgroepen**.
-   Als u de optie **Fysieke waarde opnemen** voor een artikel *niet* selecteert, schakelt u het selectievakje **Fysieke negatieve voorraad** op de pagina **Artikelmodelgroepen** uit.

Houd er ook rekening mee dat de maximumtegenboeking in uw fysieke voorraadwaarde wordt beperkt door het aantal fysieke transacties en door het verschil tussen fysieke en financiële prijzen. Zolang alle fysieke transacties uiteindelijk financieel worden bijgewerkt, kan de fysieke waarde niet extreem hoog worden. Bovendien blijft het verhogende effect aanzienlijk beperkt wanneer de cumulatieve tegenboeking wordt verdeeld over een aantal voorhanden eenheden in plaats van deze toe te wijzen aan één eenheid.




