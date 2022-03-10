---
title: Lopend gemiddelde kostprijs
description: Met het proces voor het afsluiten van voorraden worden uitgiftetransacties vereffend met ontvangsttransacties op basis van de methode voor het waarderen van voorraden die in de artikelmodelgroep van het artikel is geselecteerd. Voordat de voorraadafsluiting wordt uitgevoerd, wordt echter een lopend gemiddelde kostprijs berekend die in de meeste gevallen wordt gebruikt voor het boeken van uitgiftetransacties.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092184"
---
# <a name="running-average-cost-price"></a>Lopend gemiddelde kostprijs

[!include [banner](../includes/banner.md)]

Met het proces voor het afsluiten van voorraden worden uitgiftetransacties vereffend met ontvangsttransacties op basis van de methode voor het waarderen van voorraden die in de artikelmodelgroep van het artikel is geselecteerd. Voordat de voorraadafsluiting wordt uitgevoerd, wordt echter een lopend gemiddelde kostprijs berekend die in de meeste gevallen wordt gebruikt voor het boeken van uitgiftetransacties.

In het systeem wordt deze lopend gemiddelde kostprijs voor een artikel geschat met behulp van de volgende formule:

Geschatte prijs = (fysiek bedrag + financieel bedrag) / (fysieke hoeveelheid + financiële hoeveelheid)

## <a name="default-item-cost"></a>Standaardartikelkosten

De standaardartikelkosten voor een vrijgegeven product kunnen worden geconfigureerd op een van de twee manieren op de pagina **Vrijgegeven productdetails**:

- Maak standaardkosten door **Artikelprijs** te selecteren in de groep **Instellen** op het tabblad **Kosten beheren** van het actievenster. Als u deze methode gebruikt, moet u een kostprijsberekeningsversie van standaardkosten gebruiken en moeten de kosten worden geactiveerd.
- Definieer een standaardartikelkostenprijs voor een vrijgegeven product door een waarde in het veld **Prijs** op het sneltabblad **Kosten beheren** in te voeren.

U kunt niet alleen een prijs invoeren of maken, maar u kunt ook het selectievakje **Meest recente kostprijs gebruiken** op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven productdetails** inschakelen. In dit geval wordt het veld **Prijs** automatisch bijgewerkt wanneer u een financiële update boekt. Als u bijvoorbeeld een inkooporderfactuur boekt, wordt het veld ingesteld op de inkoopprijs van die factuur.

Als u een kostprijs in een actieve kostprijsberekeningsversie hebt en u voert een prijs op het sneltabblad **Kosten beheren** in, wordt de prijs uit de actieve kostprijsberekeningsversie gebruikt voordat de prijs wordt gebruikt die is gedefinieerd op het sneltabblad **Kosten beheren**.

## <a name="using-the-running-average-cost-price"></a>De lopende gemiddelde kostprijs gebruiken

In de volgende tabel wordt aangegeven wanneer voorraadtransacties worden geboekt met behulp van de lopende gemiddelde kostprijs en wanneer in plaats hiervan de kostprijs wordt gebruikt die is gedefinieerd in de hoofdrecord van het artikel.

| Voorwaarde | De geschatte lopende gemiddelde kostprijs wordt gebruikt | De standaardartikelkostprijs wordt gebruikt |
| --- | --- | --- |
| Zowel de teller\* als de noemer\*\* zijn positief. | Ja | Nr. |
| De teller\*, de noemer\*\* of beide zijn negatief. | Nee | Ja |
| De noemer\*\* is 0 (nul). | Nee | Ja |

\* Teller = (fysiek bedrag + financieel bedrag)  
\*\* Noemer = (fysieke hoeveelheid + financiële hoeveelheid)

> [!NOTE]
> Als de optie **Fysieke waarde opnemen** niet is geselecteerd voor een artikel, wordt 0 (nul) gebruikt voor zowel het fysieke bedrag als de fysieke hoeveelheid. Zie voor informatie over deze optie [Fysieke waarde opnemen](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Prijsverhoging voorkomen

In zeldzame gevallen wordt de prijs van verschillende uitgiften bepaald voordat er voldoende ontvangsten zijn om de prijs op te baseren. Dit scenario kan ertoe leiden dat ramingen van de lopende gemiddelde kostprijs te hoog worden. Er zijn echter maatregelen die u kunt nemen om prijsverhoging te voorkomen of om de invloed ervan te reduceren wanneer het voorkomt.

**Scenario:** de volgende transacties vinden plaats voor een artikel waarvoor u de optie **Fysieke waarde opnemen** hebt geselecteerd:

1. U ontvangt financieel een hoeveelheid van 100 tegen EUR 100,00.
2. U geeft financieel een hoeveelheid van 200 uit.
3. U ontvangt fysiek een hoeveelheid van 101 tegen EUR 202,00.

Wanneer u de geschatte lopend gemiddelde kostprijs voor het artikel bestudeert, verwacht u een kostprijs van EUR 1,51. In plaats daarvan vindt u een geschat lopend gemiddelde van USD 102,00 op basis van de volgende formule:

Geschatte prijs = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Dit komt doordat, wanneer er 200 artikelen financieel zijn uitgegeven bij stap 2, een prijs moet worden bepaald voor 100 van de artikelen voordat de bijbehorende ontvangsten binnen zijn. Dit resulteert in een negatieve voorraad. Vervolgens wordt een eenheidsprijs van EUR 1,00 geraamd, zoals verwacht. Echter, wanneer de bijbehorende 100 ontvangsten binnenkomen, hebben ze een eenheidsprijs van EUR 2,00.

> [!NOTE]
> Hoewel de uitgiften een negatieve voorraad veroorzaken, is de voorraad positief op het moment dat de uitgifteprijs wordt berekend. Dat is de reden waarom de lopend gemiddelde kostprijs wordt gebruikt in plaats van de prijs uit de hoofdrecord van het artikel. Op dit moment heeft het systeem een voorraadwaardetegenboeking van USD 100,00. Hoewel die tegenboeking is opgebouwd over 100 stuks, met een eenheidtegenboeking van EUR 1,00 per stuk, is er nu slechts één stuk in voorraad. De tegenboeking van EUR 100,00 wordt daarom toegewezen aan dit ene stuk. Dit resulteert in een te hoge geraamde kostprijs.
>
> Merk ter vergelijking op dat als stap 2 en 3 in het scenario worden omgekeerd, er 200 artikelen worden uitgegeven met een eenheidsprijs van EUR 1,51 en één stuk de eenheidsprijs van EUR 1,51 behoudt. Aangezien dit prijsverhogingsscenario kan optreden wanneer er negatieve voorraad is, is het moeilijk te voorkomen in de volgende gevallen:
>
> - U moet uitgifteprijzen schatten voor de voorhanden waarde en hoeveelheid.
> - U moet de voorhanden waarde en hoeveelheid aanpassen voor uitgiften en ontvangsten.
> - Uw bedrijfsmodel staat het verzenden, of het bepalen van de prijs, van meer stuks dan u hebt toe.
> - U moet elke ontvangstwaarde en -hoeveelheid die naar u wordt verzonden, accepteren.

Als uw bedrijfsmodel echter de volgende procedures toestaat, kunt u deze gebruiken om de negatieve hoeveelheden te voorkomen die het prijsverhogende scenario mogelijk maken:

- Als u de optie **Fysieke waarde opnemen** voor een artikel selecteert, schakelt u het selectievakje **Fysieke negatieve voorraad** uit op de pagina **Artikelmodelgroepen**.
- Als u de optie **Fysieke waarde opnemen** voor een artikel **niet** selecteert, schakelt u het selectievakje **Fysieke negatieve voorraad** op de pagina **Artikelmodelgroepen** uit.

Houd er ook rekening mee dat de maximumtegenboeking in uw fysieke voorraadwaarde wordt beperkt door het aantal fysieke transacties en door het verschil tussen fysieke en financiële prijzen. Zolang alle fysieke transacties uiteindelijk financieel worden bijgewerkt, kan de fysieke waarde niet extreem hoog worden. Bovendien blijft het verhogende effect aanzienlijk beperkt wanneer de cumulatieve tegenboeking wordt verdeeld over een aantal voorhanden eenheden in plaats van deze toe te wijzen aan één eenheid.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Een kostprijs van nul bij uitgiften vermijden

Wanneer de optie **Fysieke waarde opnemen** niet is geselecteerd op de pagina **Artikelmodelgroep**, kan een uitgifte uit de voorraad een kostprijs van nul hebben als er geen financieel bijgewerkte ontvangsten in de voorraad zijn. Om dit te voorkomen, kunt u de volgende opties overwegen:

- Selecteer de optie **Fysieke waarde opnemen** op de pagina **Artikelmodelgroep**. Met deze optie voorkomt u dat een kostprijs van nul op een uitgifte wordt gebaseerd, mits de ontvangst fysiek wordt bijgewerkt. Als u geen negatieve fysieke voorraad toestaat, wordt met uitgiften het lopende gemiddelde berekend op basis van de fysiek bijgewerkte transacties.
- Maak een standaardartikelkostprijs door een kostprijsberekeningsversie met standaardkosten te activeren of voer de prijs op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven productdetails** in. Deze optie is het beste wanneer de optie **Fysieke waarde opnemen** niet is geselecteerd op de pagina **Artikelmodelgroep** omdat het systeem altijd een terugvalprijs te gebruiken heeft.
- Selecteer de optie **Meest recente kostprijs gebruiken** op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven productdetails**. Met deze optie blijft het veld **Prijs** up-to-date gehouden wanneer u een ontvangst financieel bijwerkt. Als u deze optie selecteert, maar u geen standaardprijs invoert of kosten activeert in een standaardkostprijsberekeningsversie, kunt u voor een uitgifte nog steeds kosten van nul hebben.

Als er uitgiftetransacties zonder kosten zijn, corrigeert het proces *Voorraad afsluiten en aanpassen* de kostprijs door een correctie te maken nadat de ontvangsten financieel zijn bijgewerkt. Houd er rekening mee dat de financiële periode waarin deze update plaatsvindt, kan verschillen van de financiële periode waarin de artikelen fysiek zijn ontvangen of uitgegeven.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
