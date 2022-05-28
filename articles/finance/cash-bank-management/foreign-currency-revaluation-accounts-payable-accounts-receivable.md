---
title: Herwaardering van valuta voor Leveranciers en Klanten
description: Dit onderwerp bevat informatie over de herwaardering van vreemde valuta die u kunt uitvoeren om de waarde van openstaande transacties in Leveranciers en Klanten bij te werken.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: kfend
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32a31df1d56740d803b97d65829b1b1d31eb17
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713919"
---
# <a name="currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Herwaardering van valuta voor Leveranciers en Klanten

[!include [banner](../includes/banner.md)]

Schommelingen in wisselkoersen leiden ertoe dat de theoretische waarde (boekwaarde) van openstaande transacties in vreemde valuta in de loop van de tijd variëren. Dit onderwerp bevat informatie over de herwaardering van vreemde valuta die u kunt uitvoeren om de waarde van openstaande transacties in Leveranciers en Klanten bij te werken. 

De theoretische waarde, of boekwaarde, van openstaande transacties in vreemde valuta varieert in de loop van de tijd vanwege schommelingen in wisselkoersen. U kunt de waarde van openstaande transacties bijwerken in Leveranciers en Klant door het herwaarderingsproces voor vreemde valuta uit te voeren. Herwaardering van vreemde valuta kan worden uitgevoerd voor zowel Leveranciers als Klanten. Voor het proces wordt een nieuwe wisselkoers gehanteerd voor het herwaarderen van openstaande of niet-vereffende bedragen op een opgegeven datum. De verschillen tussen de oorspronkelijke geboekte bedragen en de geherwaardeerde bedragen veroorzaken een niet-gerealiseerde winst of niet-gerealiseerd verlies voor elke openstaande transactie. De subjournalen voor leveranciers en klanten worden vervolgens bijgewerkt, zodat de niet-gerealiseerde winst of het niet-gerealiseerde verlies en een boeking naar het grootboek worden geboekt.

## <a name="simulate-a-foreign-currency-revaluation"></a>Een herwaardering van vreemde valuta simuleren
Voordat u bedragen in vreemde valuta op openstaande transacties herwaardeert, kunt u een simulatierapport van de herwaardering van vreemde valuta uitvoeren voor dezelfde datum en methode. U kunt het simulatierapport uitvoeren door op de pagina, **Herwaardering van vreemde valuta** op de knop **Simulatie** te klikken. Het rapport bevat een voorbeeld van het niet-gerealiseerde winst- of verliesbedrag, op basis van de parameters die zijn gedefinieerd voor de simulatie.

## <a name="process-a-foreign-currency-revaluation"></a>Een herwaardering van vreemde valuta verwerken
Gebruik de pagina **Herwaardering van vreemde valuta** onder **Periodieke taken** om openstaande transacties te herwaarderen. U kunt het proces in realtime uitvoeren of inplannen om het in batch uit te voeren. Wanneer u de instellingen voor het herwaarderingsproces definieert, moet u bedenken of u een rapport met de resultaten wilt afdrukken. Het herwaarderingsrapport kan niet opnieuw worden afgedrukt nadat het proces is voltooid. Als u het herwaarderingsrapport voor vreemde valuta genereert, worden de verschillende saldi op het leveranciers-/klantniveau en het valutaniveau weergegeven:

-   De saldi van klanten of leveranciers met transacties in vreemde valuta hebben een herwaardering ondergaan. De volgende saldi worden weergegeven:
    -   Het totale oorspronkelijke saldo in de vreemde valuta.
    -   Het totale bedrag in vreemde valuta in de valuta voor boekhouding, volgens de vorige herwaardering.
    -   Het totale bedrag in vreemde valuta in de valuta voor boekhouding, volgens de huidige herwaardering.
    -   Het verschil tussen de vorige en huidige herwaardering. Dit verschil is het extra niet-gerealiseerde winst- of verliesbedrag.
-   Het totale niet-gerealiseerde winst- of verliesbedrag voor elke valuta.

Telkens wanneer u een herwaardering van vreemde valuta uitvoert, wordt een registratie bijgehouden. Selecteer vanuit de record op de pagina **Herwaardering van vreemde valuta** de optie **Transacties** om een gedetailleerde lijst met transacties weer te geven die vanwege de herwaardering zijn gemaakt. Elke boekstuktransactie staat voor de openstaande transactie die is geherwaardeerd. Als een openstaande transactie meer dan één keer is geherwaardeerd, ziet u twee records die hetzelfde boekstuk gebruiken. Eén record is bestemd voor de omkering van de vorige niet-gerealiseerde winst of niet-gerealiseerd verlies en de andere record is bestemd voor de nieuwe niet-gerealiseerde winst of niet-gerealiseerd verlies. U kunt het herwaarderingsproces uitvoeren door op de knop **Herwaardering van vreemde valuta** te klikken. Definieer geschikte instellingen voor de volgende parameters:

-   **Methode** – De methode die wordt gebruikt voor de geselecteerde herwaarderingstaak voor vreemde valuta's:
    -   **Standaard** – Herwaarderingstaken van vreemde valuta worden geboekt, ongeacht of deze in winst of verlies resulteren.
    -   **Minimum** – Herwaarderingstaken van vreemde valuta's worden alleen geboekt als deze in verlies resulteren.
    -   **Factuurdatum** – Bij herwaarderingstaken van vreemde valuta wordt de oorspronkelijke wisselkoers van de transacties gebruikt, die wordt teruggezet naar de oorspronkelijke waarde in de valuta voor boekhouding. Het effect van eventuele eerdere herwaarderingen van vreemde valuta's wordt geannuleerd.
-   **Onderhavige datum** – De datum waarop u alle transacties vindt met bedragen die op die datum open staan (niet zijn vereffend). De bedragen voor vreemde valuta's worden geherwaardeerd met de wisselkoersen die zijn ingevoerd op de pagina **Valutawisselkoersen** voor de onderhavige datum. Wanneer bedragen in een vreemde valuta worden geherwaardeerd op een onderhavige datum, wordt deze datum de laatste herwaarderingsdatum voor vreemde valuta's voor de transacties die worden gecorrigeerd. Als u een herwaardering van vreemde valuta uitvoert voor een onderhavige datum die valt voor de datum van de laatste herwaardering van vreemde valuta van reeds gecorrigeerde transacties, worden transacties die openstaan op de eerdere onderhavige datum maar een recentere datum van de laatste herwaardering van vreemde valuta hebben, niet gecorrigeerd met de periodieke taak.
-   **Datum van koers** – De datum waarop de wisselkoers wordt bepaald die wordt gebruikt in de herwaardering voor vreemde valuta's.
-   **Boekingsprofiel gebruiken van** Het boekingsprofiel dat wordt gebruikt om de standaardhoofdrekening voor Klanten of Leveranciers in te voeren voor de journaalregels van de herwaarderingstransacties van vreemde valuta's:
    -   **Boeking** – Het boekingsprofiel van de klanttransactie wordt gebruikt.
    -   **Selecteren** – Voer het boekingsprofiel in het veld **Boekingsprofiel** in.
-   **Boekingsprofiel** – Als **Selecteren** is geselecteerd in het veld **Boekingsprofiel gebruiken van**, wordt het boekingsprofiel van de herwaarderingstransacties voor vreemde valuta's bepaald door het boekingsprofiel in dit veld.
-   **Financiële dimensies**: de financiële dimensies die worden geboekt op de journaalregels van de herwaarderingstransacties voor vreemde valuta's. De financiële dimensies worden niet gevalideerd tegen de regels voor de rekeningstructuur. De rekeningstructuur die aanwezig was op het moment dat de facturen werden geboekt, was mogelijk niet gelijk aan de regels die golden toen de herwaardering werd voltooid. Er is geen optie om specifieke financiële dimensies te selecteren in het herwaarderingsproces, daarom wordt de validatie van de rekeningstructuur overgeslagen.  
    -   **Geen** – Er worden geen financiële dimensies geboekt. Als u een verplichte financiële dimensie hebt in uw rekeningstructuur, wordt het herwaarderingsproces nog steeds uitgevoerd en worden boekhoudvermeldingen gemaakt die geen financiële dimensies hebben. U ontvangt eerst een waarschuwingsbericht, zodat u de herwaardering kunt annuleren.
    -   **Tabel** – De financiële dimensies van de klantrekening of leveranciersrekening worden geboekt op de herwaarderingstransacties voor vreemde valuta's.
    -   **Boeking** – De financiële dimensies van de geherwaardeerde transactie wordt geboekt op de herwaarderingstransacties voor vreemde valuta's. Standaard worden de financiële dimensies van de klant- of leveranciersgrootboekrekening van de oorspronkelijke transactie gebruikt voor de klant-/leveranciershoofdrekening van de herwaarderingtransactie, en worden de financiële dimensies van de grootboekrekening voor onkosten/activa/opbrengsten van de oorspronkelijke transactie gebruikt voor de hoofdrekening voor niet-gerealiseerde winst/niet-gerealiseerd verlies.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
