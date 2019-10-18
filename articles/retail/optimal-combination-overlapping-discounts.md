---
title: De optimale combinatie van overlappende kortingen bepalen
description: Als kortingen elkaar overlappen, moet u bepalen welke combinatie van overlappende kortingen leidt tot het laagste totaalbedrag voor de transactie of de hoogste totale korting. Wanneer het kortingsbedrag varieert afhankelijk van de prijs van de producten die worden aangeschaft, zoals in de veelgebruikte retailkorting 'koop 1, krijg 1 met X procent korting' (BOGO), wordt dit proces een kwestie van combinatorische optimalisatie.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 555098a7d11cb0b4c0f90357ff260598e80108f5
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017915"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>De optimale combinatie van overlappende kortingen bepalen

[!include [banner](includes/banner.md)]

Als kortingen elkaar overlappen, moet u bepalen welke combinatie van overlappende kortingen leidt tot het laagste totaalbedrag voor de transactie of de hoogste totale korting. Wanneer het kortingsbedrag varieert afhankelijk van de prijs van de producten die worden aangeschaft, zoals in de veelgebruikte retailkorting 'Koop 1, krijg 1 met X procent korting' (BOGO), wordt dit proces een kwestie van combinatorische optimalisatie.

Dit artikel is van toepassing op Microsoft Dynamics AX 2012 R3 met KB 3105973 (uitgebracht op 2 november 2015) of hoger, en op Dynamics 365 Retail. Om de combinatie van overlappende kortingen die u wilt toepassen snel te bepalen, hebben we een methode voor het toepassen van overlappende kortingen ingevoerd. We noemen deze nieuwe methode **marginale-waardeclassificatie**. Marginale-waardeclassificatie wordt gebruikt wanneer de tijd die nodig is om mogelijke combinaties van overlappende kortingen te evalueren een drempel overschrijdt die u kunt configureren op de pagina **Detailhandelparameters**. In de methode voor marginale-waardeclassificatie wordt een waarde berekend voor elke overlappende korting door middel van de waarde van de korting op de gedeelde producten. De overlappende kortingen worden dan toegepast, vanaf de hoogste relatieve waarde tot de laagste relatieve waarde. Zie de sectie 'Marginale waarde' verderop in dit artikel voor meer informatie over de nieuwe methode. Marginale-waardeclassificatie wordt niet gebruikt wanneer de kortingsbedragen voor een product niet worden beïnvloed door een ander product in de transactie. Deze methode wordt bijvoorbeeld niet gebruikt voor twee eenvoudige kortingen of voor een eenvoudige korting en een kwantumkorting voor een enkel product.

## <a name="discount-examples"></a>Kortingsvoorbeelden

U kunt een onbeperkt aantal retailkortingen voor een gemeenschappelijke set van producten maken. Omdat er geen limiet is, kunnen echter prestatieproblemen optreden wanneer u probeert om de kortingen te berekenen die moeten worden gebruikt voor de verschillende producten. In de volgende voorbeelden wordt deze kwestie nader toegelicht. In voorbeeld 1 beginnen we met twee producten en twee overlappende kortingen. Vervolgens wordt in voorbeeld 2 getoond hoe het probleem uitdijt wanneer meer producten worden toegevoegd.

### <a name="example-1-two-products-and-two-discounts"></a>Voorbeeld 1: Twee producten en twee kortingen

In dit voorbeeld zijn twee producten nodig om in aanmerking te komen voor elke korting en de kortingen kunnen niet worden gecombineerd. De kortingen in dit voorbeeld zijn **Beste prijs**-kortingen. Beide producten komen in aanmerking voor beide kortingen. Dit zijn de twee kortingen.

![Voorbeeld van twee Beste prijs-kortingen](./media/overlapping-discount-combo-01.jpg)

Voor elke combinatie van twee producten is de beste van deze twee kortingen afhankelijk van de prijzen van de twee producten. Wanneer de prijs van beide producten bijna gelijk of gelijk is, is korting 1 beter. Wanneer de prijs van een product aanzienlijk lager is dan de prijs van het andere product, is korting 2 beter. Hier volgt de wiskundige regel voor het evalueren van de twee kortingen ten opzichte van elkaar.

![Regel voor het evalueren van de kortingen](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Wanneer de prijs van product 1 gelijk is aan tweederde van de prijs van product 2, zijn de twee kortingen gelijk. In dit voorbeeld varieert het effectieve kortingspercentage voor korting 1 van enkele procenten (wanneer de prijzen van de twee producten ver uit elkaar liggen) tot maximaal 25 procent (wanneer de twee producten dezelfde prijs hebben). Het effectieve kortingspercentage voor korting 2 ligt vast. Dit bedraagt altijd 20 procent. Aangezien het effectieve kortingspercentage voor korting 1 een bereik heeft waarin het hoger of lager kan liggen dan korting 2, is de beste korting afhankelijk van de prijzen van de twee producten waarop de korting wordt toegepast. In dit voorbeeld wordt de berekening is snel voltooid, omdat slechts twee kortingen worden toegepast op slechts twee producten. Er zijn slechts twee mogelijke combinaties: toepassing van korting 1 of toepassing van korting 2. Er zijn geen permutaties die moeten worden berekend. De waarde van elke korting wordt berekend met behulp van beide producten en de beste korting wordt gebruikt.

### <a name="example-2-four-products-and-two-discounts"></a>Voorbeeld 2: Vier producten en twee kortingen

Vervolgens gebruiken we vier producten en dezelfde twee kortingen. Alle vier producten komen in aanmerking voor beide kortingen. Er zijn twaalf mogelijke combinaties. Uiteindelijk worden twee kortingen toegepast op de transactie, in één van drie combinaties: twee toepassingen van korting 1, twee toepassingen van 2 of één toepassing van korting 1 en één toepassing van korting 2. Ter illustratie van de mogelijke combinaties gaan we twee verschillende sets bekijken van vier producten met verschillende prijzen:

- Alle vier producten hebben dezelfde prijs, namelijk € 15.00. In dit geval bestaat de beste combinatie van kortingen uit twee toepassingen van korting 1. Twee producten hebben de volledige prijs en twee producten hebben een korting van 50 procent. De totale korting voor de transactie is € 45 (15 + 15 + 7,50 + 7,50), € 15 (25 procent) lager dan het totaalbedrag zonder korting van € 60. Korting 2 bedraagt slechts € 12 (20 procent).
- Twee producten zijn elk € 20, één product is € 15 en één product is € 5. In dit geval bestaat de beste combinatie van kortingen uit één toepassing van korting 2 en één toepassing van korting 1. In de volgende tabellen ziet u de kortingen uitgespeld.

Om de tabellen te lezen moet u een product uit een rij nemen en een product uit een kolom. In de tabel voor korting 1 krijgt u bijvoorbeeld € 10 korting als u de twee producten van € 20 combineert. In de tabel voor korting 2 krijgt u € 4 korting als u het product van € 15 combineert met het product van € 5.

![Voorbeeld waarin vier producten voor dezelfde twee kortingen worden gebruikt](./media/overlapping-discount-combo-03.jpg)

Allereerst zoeken we de grootste korting die beschikbaar is voor twee willekeurige producten door middel van een van beide kortingen. In de twee tabellen ziet u het kortingsbedrag voor alle combinaties van de twee producten. De gearceerde gedeelten van de tabellen staan voor gevallen waarin een product in combinatie met zichzelf wordt genomen, wat we niet mogen doen, of voor een omgekeerde combinatie van twee producten die hetzelfde kortingsbedrag oplevert en kan worden genegeerd. Als u de tabellen bekijkt, ziet u dat korting 1 voor de twee artikelen van € 20 de grootste korting is die beschikbaar is voor alle kortingen op alle vier producten. Deze korting is groen gemarkeerd in de eerste tabel. Zo blijven twee producten over: dat van € 15 en dat van € 5. Als u opnieuw de twee tabellen bekijkt, ziet u dat voor deze twee producten korting 1 resulteert in een korting van € 2,50, terwijl korting 2 een korting van € 4 oplevert. Daarom selecteren we korting 2. De totale korting bedraagt € 14. Om deze discussie makkelijker te visualiseren, vindt hier u twee extra tabellen die de het effectieve kortingspercentage weergeven voor alle mogelijke combinaties van twee producten voor zowel korting 1 als korting 2. Hierin is slechts de helft van de lijst met combinaties opgenomen, omdat voor deze twee kortingen de volgorde waarin de twee producten worden aangeboden in de korting niet van belang is. De hoogste effectieve korting (25 procent) is groen gemarkeerd. De laagste effectieve korting (10 procent) is rood gemarkeerd.

![Effectieve kortingspercentage voor alle combinaties van twee producten voor beide kortingen](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Wanneer prijzen variëren en twee of meer kortingen concurreren, kan de beste combinatie van kortingen alleen worden gegarandeerd door beide kortingen te evalueren en met elkaar te vergelijken.

## <a name="total-possible-combinations"></a>Totaal aantal mogelijke combinaties

In deze sectie gaan we verder met het voorbeeld uit de vorige sectie. We voegen meer producten en nog een korting toe en zien hoeveel combinaties moeten worden berekend en vergeleken. In de volgende tabel ziet u het aantal mogelijke kortingscombinaties bij een toenemend aantal producten. U ziet hier wat er gebeurt wanneer er twee overlappende kortingen zijn zoals in het vorige voorbeeld, en ok wanneer er drie overlappende kortingen zijn. Het aantal mogelijke kortingscombinaties dat moet worden geëvalueerd neemt snel toe, en zelfs een krachtige computer kan dan de berekening en vergelijking niet snel genoeg uitvoeren om acceptabel zijn voor detailhandeltransacties.

![Aantal mogelijke kortingscombinaties bij een toenemend aantal producten](./media/overlapping-discount-combo-05.jpg)

Wanneer nog grotere hoeveelheden of meer overlappende kortingen worden toegepast, loopt het totale aantal mogelijke kortingscombinaties snel in de miljoenen. De tijd die nodig is om deze te evalueren en de best mogelijke combinatie te selecteren wordt dan snel merkbaar. Enige optimalisatie is doorgevoerd in de retailprijs-engine om het totale aantal combinaties te verlagen dat moet worden geëvalueerd. Omdat het aantal overlappende kortingen en de aantallen in een transactie niet worden beperkt, moet echter altijd een groot aantal combinaties worden geëvalueerd wanneer er overlappende kortingen zijn. Dit is het probleem waarop de de marginale-waardemethode zich richt.

## <a name="marginal-value-method"></a>Marginale-waardemethode

Om het probleem op te lossen van exponentieel toenemende aantallen combinaties die moeten worden geëvalueerd, bestaat een optimalisatie die de waarde berekent per gedeeld product van elke korting op de reeks producten waarop twee of meer kortingen kunnen worden toegepast. Deze waarde noemen we de **marginale waarde** van de korting voor de gedeelde producten. De marginale waarde is de toename van het gemiddelde per product in het totale kortingsbedrag, wanneer de gedeelde producten worden opgenomen in elke korting. De marginale waarde wordt berekend door van het totale kortingsbedrag (DTotal) het kortingsbedrag zonder de gedeelde producten af te trekken (DMinus\\ Shared) en dit verschil te delen door het aantal gedeelde producten (ProductsShared).

![Formule voor het berekenen van de marginale waarde](./media/overlapping-discount-combo-06.jpg)

Nadat de marginale waarde van elke korting voor een gedeelde reeks producten is berekend, worden de kortingen toegepast op de gedeelde producten in de volledige volgorde van de hoogste marginale waarde tot de laagste marginale waarde. Bij deze methode worden niet telkens alle resterende kortingsmogelijkheden vergeleken zodra één exemplaar van een korting is toegepast. In plaats daarvan worden de overlappende kortingen eenmaal vergeleken en vervolgens op volgorde toegepast. Er worden geen extra vergelijkingen uitgevoerd. U kunt de drempel voor overschakelen naar de marginale-waardemethode configureren op het tabblad **Korting** van de pagina **Detailhandelparameters**. Welke tijd acceptabel is voor berekening van de totale korting, verschilt van sector tot sector. Deze tijd ligt echter over het algemeen ergens tussen enkele tientallen milliseconden tot één seconde.
