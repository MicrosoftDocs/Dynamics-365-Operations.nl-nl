---
title: Vereffeningsoverzicht voor gecentraliseerde betalingen
description: Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door een rechtspersoon te gebruiken die alle betalingen verwerkt. Hierdoor hoeft u dezelfde transactie niet voor meerdere rechtspersonen in te voeren en bespaart u tijd doordat het betalingsvoorstelproces, het vereffeningsproces, en het bewerken van openstaande en gesloten transacties voor gecentraliseerde betalingen worden gestroomlijnd.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b76b141531acfc2d1d7553a3e7a13f165373921b
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="settlement-overview-for-centralized-payments"></a>Vereffeningsoverzicht voor gecentraliseerde betalingen

[!INCLUDE [banner](../includes/banner.md)]

Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door een rechtspersoon te gebruiken die alle betalingen verwerkt. Hierdoor hoeft u dezelfde transactie niet voor meerdere rechtspersonen in te voeren en bespaart u tijd doordat het betalingsvoorstelproces, het vereffeningsproces, en het bewerken van openstaande en gesloten transacties voor gecentraliseerde betalingen worden gestroomlijnd. 

Als betaling door een klant of leverancier wordt ingevoerd in een rechtspersoon en is vereffend met een factuur die in een andere rechtspersoon is ingevoerd, worden voor elke rechtspersoon automatisch de toepasbare vereffening, aan- en van-transacties gegenereerd voor elke rechtspersoon. Er wordt een vereffeningsrecord gemaakt voor elke combinatie van factuur en betaling in de transactie. Aan elk vereffeningsrecord wordt een nieuw boekstuknummer toegewezen, gebaseerd op de nummervolgordereeks voor betalingsboekstukken die is opgegeven op de pagina **Klantparameters** voor klanten en op de pagina **Leverancierparameters** voor leveranciers. 

Als extra vereffeningsrecords worden gegenereerd voor contantkortingen, aanpassingen voor buitenlandse valuta, afrondingen, over- of onderbetalingen, krijgen deze de latere datum toegewezen van de betalings- of factuurtransactie. Als vereffening plaatsvindt na het boeken van de betaling, wordt voor de vereffeningsrecords de boekingsdatum van de vereffeningsrecords gebruikt die is opgegeven op de pagina **Openstaande transacties vereffenen**.
Soorten boekingen, soorten transacties, en standaardbeschrijvingen
----------------------------------------------------------

De boekstuktransacties voor intercompany-vereffening gebruiken het boekingstype voor intercompany-vereffening, intercompany-klantvereffening en transactietypen voor intercompany-leveranciervereffening. U kunt informatie voor het transactietype instellen op de pagina **Standaardomschrijvingen**. 

De volgende transactietypen zijn beschikbaar voor gebruik in vereffeningen voor een of meer bedrijven:

-   Vereffening
-   Contantkorting
-   aanpassingen voor buitenlandse valuta (waaronder uitgevoerde en niet-uitgevoerde aanpassingen voor buitenlandse valuta)
-   Afronding
-   Overbetaling/onderbetaling

U kunt ook standaardbeschrijvingen definiëren voor intercompany-vereffeningsboekstukken.

<a name="currency-exchange-gains-or-losses"></a>Winst of verlies bij valutawissel
---------------------------------

De wisselkoers die wordt gebruikt voor klant- of leveranciertransacties, wordt opgeslagen bij de transactie. Gerealiseerde winsten of verliezen voor valutaomrekening worden geboekt voor de rechtspersoon van de factuur of voor de rechtspersoon van de betaling, afhankelijk van de optie die is geselecteerd voor het veld **Winst of verlies bij valutawissel boeken** op de pagina **Intercompany-boekhouding** voor de rechtspersoon van de betaling. In de volgende voorbeelden worden deze valuta's gebruikt:
-   Boekhoudvaluta betaling: EUR
-   Boekhoudvaluta factuur: USD
-   Valuta betalingstransactie: DKK
-   Valuta factuurtransactie: CAD

#### <a name="currency-calculations"></a>Valutaberekeningen

Bij het vereffenen van een factuur die is ingevoerd in een rechtspersoon met een betaling die is ingevoerd in een andere rechtspersoon, wordt de transactievaluta van de betaling (DKK) in drie stappen geconverteerd:
1.  Geconverteerd naar de boekhoudvaluta voor de betaling (EUR), waarbij de valutakoers van de rechtspersoon van de betaling gebruikt wordt.
2.  Geconverteerd naar de boekhoudvaluta van de factuur (USD).
3.  Geconverteerd naar de transactievaluta van de factuur (CAD), waarbij de valutakoers van de rechtspersoon van de factuur gebruikt wordt.

Bij het conversieproces worden de wisselkoersen gebruikt vanaf de betalingsdatum. Als het resulterende betalingsbedrag in de transactievaluta van de factuur (CAD) gelijk is aan het factuurbedrag (CAD), wordt de factuur beschouwd als volledig betaald. 

Wanneer de pagina **Openstaande transacties vereffenen** is geopend vanuit een betalingsjournaal waarin het betalingsbedrag niet is ingevoerd, wordt het te vereffenen bedrag berekend op basis van de facturen die zijn geselecteerd voor vereffening op de pagina **Openstaande transacties vereffenen**. Het te vereffenen bedrag wordt in drie stappen geconverteerd:
1.  Geconverteerd naar de transactievaluta van de factuur (USD), waarbij de valutakoers van de rechtspersoon van de factuur per de betalingsdatum gebruikt wordt.
2.  Geconverteerd naar de boekhoudvaluta voor de betaling (EUR), waarbij de valutakoers van de rechtspersoon van de factuur per de betalingsdatum gebruikt wordt.
3.  Geconverteerd naar de transactievaluta van de betaling (DKK).

Het resulterende betalingsbedrag wordt overgeboekt naar de betalingsjournaalregel wanneer u de pagina **Openstaande transacties vereffenen** sluit.

#### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Voor winst of verlies boeken als gevolg van verschillende boekhoudvaluta

Als sprake is van winst of verlies bij valutawissel, wordt deze geboekt voor de rechtspersoon die is opgegeven voor het veld **Winst of verlies bij valutawissel boeken** op de pagina **Intercompany-boekhouding** voor de rechtspersoon van de betaling. Het verlies- of winstbedrag bij valutawissel wordt geconverteerd naar de boekhoudvaluta van de rechtspersoon waar het verlies- of winstbedrag is geboekt, met de valutakoers die voor die rechtspersoon is gedefinieerd.

<a name="cash-discounts"></a>Contantkortingen
--------------

Contantkortingen die tijdens het cross-company vereffeningsproces worden gegenereerd, worden geboekt voor de rechtspersoon van de factuur of voor de rechtspersoon van de betaling, afhankelijk van de optie die is geselecteerd voor het veld **Contantkorting boeken** op de pagina **Intercompany-boekhouding** voor de rechtspersoon van de betaling. Een bijbehorende vereffeningstransactie wordt in de rechtspersoon van de factuur geboekt.

<a name="overpayments-and-underpayments"></a>Overbetalingen en onderbetalingen
------------------------------

Toleranties voor overbetaling, onderbetaling en afrondingsverschillen worden bepaald aan de hand van de rechtspersoon van de betaling voor overbetalingen en de rechtspersoon van de factuur voor onderbetalingen. Welke boekingsrekening wordt gebruikt, wordt bepaald door de instelling in het veld **Administratie voor contantkorting** op de  pagin **Klantparameters** voor klanten en het veld **Administratie voor contantkorting** op de pagina **Leverancierparameters** voor leveranciers.

-   Als de instelling voor beheer van contantkortingen Specifiek is, of als de instelling Flexibel is en de van toepassing zijnde contantkorting is geboekt op een andere rechtspersoon dan voor de overbetaling, wordt de automatische rekening voor Contantkorting van klant, Contantkorting van leverancier of Afronding in valuta voor boekhouding gebruikt. U kunt deze rekeningen opgeven op de pagina **Rekeningen voor automatische transacties**.
-   Als de instelling voor het beheer van contantkortingen Flexibel is en de contantkorting is geboekt in dezelfde rechtspersoon als de overbetaling (de rechtspersoon van de betaling en de rechtspersoon van de factuur zijn gelijk), wordt de rekening voor de contantkorting aangepast. Als een factuur voor 100,00 met een beschikbare contantkorting van 3,00 bijvoorbeeld wordt vereffend met een betaling van 98,00, wordt het contantkortingsbedrag gecorrigeerd met 1,00. Het nettokortingsbedrag is 2,00.
-   Als de instelling voor het beheer van contantkortingen Flexibel is, wordt de contantkorting geboekt in dezelfde rechtspersoon als de overbetaling en wordt de over- of onderbetaling vereffend met meerder facturen met contantkortingen, dan wordt de rekening voor contantkorting voor de laatste factuur aangepast.

Als voor de administratie voor contactkorting Flexibel is geselecteerd, zijn alleen in de volgende situaties niet-specifieke betalingsvereffeningsregels van toepassing:
-   Er is sprake van overbetaling.
-   De overbetaling wordt vereffend met een of meer facturen met een contantkorting.
-   De contantkorting wordt geboekd in dezelfde rechtspersoon als de overbetaling.

In alle andere gevallen worden over- of onderbetalingen geboekt naar de automatische rekening voor Contantkorting van klant, Contantkorting van leverancier of Afronding in valuta voor boekhouding.

## <a name="sales-tax"></a>Btw
BTW-transacties blijven in de rechtspersoon waar ze oorspronkelijk geboekd zijn. 

Als BTW is geboekt voor een vooruitbetaling, draait de cross-company vereffening de btw op de vooruitbetaling in de rechtspersoon van de vooruitbetaling terug. De belastingen in de rechtspersoon van de factuur blijven in de rechtspersoon van de factuur.

## <a name="financial-dimensions"></a>Financiële dimensies
Voor klantenbetalingen gebruiken de transacties bestemd voor en afkomstig van in de rechtspersoon van de betaling de financiële dimensies die zijn gespecificeerd voor de klantenverzamelrekening van de betaling die wordt vereffend. In de rechtspersoon van de factuur gebruiken transacties bestemd voor en afkomstig van de financiële dimensies die zijn opgegeven voor de klantenverzamelrekening van de factuur die vereffend wordt. 

Voor betalingen aan leveranciers gebruiken de transacties bestemd voor en afkomstig van in de rechtspersoon van de betaling de financiële dimensies die zijn gespecificeerd voor de klantenverzamelrekening van de betaling die wordt vereffend. In de rechtspersoon van de factuur gebruiken bestemd voor en afkomstig van transacties de financiële dimensies die zijn gespecificeerd voor de klantenverzamelrekening van de factuur die vereffend wordt.

## <a name="withholding-tax"></a>Bronbelasting
De leveranciersrekening die aan de factuur is gekoppeld, wordt gebruikt om te bepalen of de bronbelasting berekend moet worden. Als bronbelasting van toepassing is, wordt deze berekend in de rechtspersoon die aan de factuur is gekoppeld. Als de rechtspersonen verschillende valuta gebruiken, wordt de wisselkoers gebruikt van de rechtspersoon die aan de factuur is gekoppeld.






