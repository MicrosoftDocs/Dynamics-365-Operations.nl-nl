---
title: Zwevend gemiddelde
description: Zwevend gemiddelde is een permanente kostenmethode, gebaseerd op het gemiddelde, waarbij de kosten van voorraadproblemen niet veranderen wanneer de aankoopkosten veranderen. Het verschil wordt gekapitaliseerd en is gebaseerd op een proportionele berekening. Het overblijvende bedrag zijn onkosten.
author: JennySong-SH
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0be72c8ba3c123300be83513531d2f805dc8f5e3
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676098"
---
# <a name="moving-average"></a>Zwevend gemiddelde

[!include [banner](../includes/banner.md)]

Zwevend gemiddelde is een permanente kostenmethode, gebaseerd op het gemiddelde, waarbij de kosten van voorraadproblemen niet veranderen wanneer de aankoopkosten veranderen. Het verschil wordt gekapitaliseerd en is gebaseerd op een proportionele berekening. Het overblijvende bedrag zijn onkosten.

Als u een zwevend gemiddelde gebruikt, worden voorraadvereffeningen en voorraadmarkering niet ondersteund. Een voorraadsluiting heeft geen invloed op de producten die een zwevend gemiddelde als de voorraadmodelgroep hebben en genereren geen schikkingen tussen de transacties.

De volgende zijn voorwaarden wanneer u gemiddelde kosten als een kostprijsmethode gebruikt.

1. Stel op de pagina **Artikelmodelgroepen** een artikelmodelgroep in waarbij **Zwevend gemiddelde** is geselecteerd in het veld **Voorraadwaarderingsmodel**.

    > [!NOTE]
    > Standaard worden, als **Zwevend gemiddelde** is geselecteerd, ook de velden **Fysieke voorraad boeken** en **Financiële voorraad boeken** geselecteerd.

1. Wijs op de pagina **Boeking** rekeningen toe aan **Prijsverschil voor zwevend gemiddelde**. U gebruikt de rekening **Prijsverschil voor zwevend gemiddelde** wanneer kosten proportioneel moeten worden opgevoerd. Dit gebeurt in de volgende twee scenario's:
    - Er is een verschil in kosten tussen een inkoopontvangst en de inkoopfactuur vanwege een verschil tussen de oorspronkelijke voorraad en de huidige voorraad.
    - De transacties brengen de voorraad van negatief naar nul en er is een verschil tussen de transactiekosten en de huidige zwevend gemiddelde kosten.

1. Wijs op de pagina **Boeking** rekeningen toe aan de rekeningen **Kostenherwaardering voor zwevend gemiddelde** op het tabblad **Voorraad**. U gebruikt de rekening **Kostenherwaardering voor zwevend gemiddelde** wanneer u de zwevend gemiddelde kosten voor een product wilt wijzigen in een nieuwe eenheidsprijs.

1. Wijs op de pagina **Vrijgegeven producten** de zwevend gemiddelde artikelmodelgroep toe aan het product.

    > [!NOTE]
    > Het afsluitproces van de voorraad sluit alleen de boekhoudperiode af. Het heeft geen invloed op producten waar een zwevend gemiddelde aan is toegewezen als artikelmodelgroep.

## <a name="convert-to-the-moving-average-costing-method"></a>Converteren naar de zwevend gemiddelde kostprijsmethode

Producten kunnen worden geconverteerd zodat de gemiddelde voorraadwaarderingsmethode kan gebruikt worden. Dit type conversie gebeurt gewoonlijk op het einde van het jaar nadat de laatste maand van het huidige jaar is afgesloten. Dit gebeurt met behulp van het huidige kostprijsmodel van het product. U kunt de kostprijsmethode van uw voorraad wijzigen van een kostprijsmethode op basis van de gemiddelde kostprijs of een standaardkostprijs naar een methode die is gebaseerd op het zwevend gemiddelde.

Als u de kostprijsmethode van een standaard kostprijsmethode naar een zwevend gemiddeldemethode wijzigt, moet u de volgende taken uitvoeren:

1. Maak aanpassingen om de voorraadhoeveelheden en waarden naar 0 (nul) te brengen.
1. Nadat de voorraadwaarde en de hoeveelheid 0 (nul) zijn, wijzigt u het zwevend gemiddelde in de artikelmodelgroep.
1. Maak aanpassingen om de voorraadhoeveelheden en waarden terug in de voorraad te brengen.

U kunt uw voorraadkostprijsmethode niet wijzigen van een methode voor zwevend gemiddelde naar een FIFO-methode (First In, First Out), een LIFO-methode (Last In, First Out) of een methode voor gewogen gemiddelde.

> [!NOTE]
> Het omschakelen van een standaardkostprijs naar een zwevend gewogen gemiddelde is een handmatig proces.

De volgende voorbeelden illustreren het effect van de zwevend gemiddelde kostprijsmethode. Er zijn vier configuraties:

- Inkooporder en proportioneel opgevoerd kostenverschil
- Aanpassen van zwevend gemiddelde product en voorraad
- Zwevend gemiddelde met productie
- Zwevend gemiddelde met een achterstallige transactie

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Inkooporder en proportioneel opgevoerd kostenverschil

Bij zwevend gemiddelde worden de kosten van het product bepaald door de inkoopontvangst. Wanneer de inkoopfactuur is geboekt en er is een verschil in kosten tussen de inkoopontvangst en de inkoopfactuur, dan wordt het verschil wordt proportioneel aangepast aan de huidige producten in voorraad en wordt een eventueel resterend bedrag als last opgenomen.

In dit voorbeeld wordt een inkooporder gemaakt en ontvangen tegen een kostprijs en wordt de inkoopfactuur geboekt met een andere kostprijs.

1. Maak een inkooporder voor een hoeveelheid van 2 en een eenheidsprijs van 10,00.
1. Maak een inkoopontvangst van het product.
1. Maak een verkooporder voor een hoeveelheid van 1 en een eenheidsprijs van 10,00.
1. Maak een inkoopfactuur voor een hoeveelheid van 2 en een eenheidsprijs van 12,00.

Het verschil in eenheidsprijs, 2,00, wordt geboekt naar de rekening Prijsverschil voor zwevend gemiddelde wanneer de inkoopfactuur is geboekt. De reden hiervoor is dat twee producten zijn gekocht aan een kostprijs van 20,00. Een van de producten is verkocht voor een eenheidsprijs van 10,00. De inkoopfactuur is geboekt tegen een eenheidsprijs van 12,00 met een hoeveelheid van 2. De eenheidsprijs van het product kan niet tegen 14,00 worden geboekt.

## <a name="moving-average-product-and-inventory-adjustment"></a>Aanpassen van zwevend gemiddelde product en voorraad

Als u de zwevend gemiddelde kostprijs van een product wilt aanpassen, zijn voorraadherwaarderingen toegestaan op de huidige datum. U kunt een voorraadaanpassing niet met terugwerkende kracht aanpassen om de zwevend gemiddelde kostprijs van een product te corrigeren. U de kost niet door opeenvolgend transacties laten passeren.

In dit voorbeeld wordt de zwevend gemiddelde kostprijs aangepast voor een product.

1. Selecteer het product waarvoor u de zwevende gemiddelde kosten wilt aanpassen. 

 > [!NOTE]
 > De pagina **Herwaardering voor zwevend gemiddelde** controleert de beschikbare voorraad voor een product. Het geselecteerde product heeft een geboekte hoeveelheid 1, een geboekte een waarde van 12,00, een geboekte kostprijs van 12,00 en een eenheidskost van 12,00.
    
1. Werk het veld **Eenheidskosten** bij naar 16,00. Het systeem berekent de overige velden.
1. De aanpassing is geboekt.

> [!NOTE]
> U kunt alleen de zwevend gemiddelde kosten vanaf de huidige datum aanpassen.

Op de pagina **Vereffeningen voor boekstuk** kunt u zien dat een correctie van 4,00 is geboekt naar de rekening Kostenherwaardering voor zwevend gemiddelde.

## <a name="moving-average-with-production"></a>Zwevend gemiddelde met productie

Zwevend gemiddelde ondersteunt geproduceerde artikelen. Als u van plan bent om zwevend gemiddelde in een productieomgeving te gebruiken, selecteert u **De geschatte kostprijs gebruiken** op de pagina **Parameters van productiecontrole**. Dit betekent dat de kostprijs die wordt berekend tijdens de raming wordt gebruikt in plaats van de werkelijke kostprijs van de stuklijstberekening.

## <a name="moving-average-with-a-backdated-transaction"></a>Zwevend gemiddelde met een achterstallige transactie

Indien backdated transacties worden toegewezen, worden de zwevend gemiddelde kosten en de fysieke hoeveelheid van het product bijgewerkt maar wordt de zwevend gemiddelde kost niet beïnvloed. In dit voorbeeld van zwevend gemiddelde wordt een backdated transactie voor een zwevend gemiddeldeproduct geboekt.

1. Maak een voorraadcorrectie voor het zwevend gemiddeldeproduct voor een hoeveelheid van 1 en de kosten van 20,00.
1. De voorraadtransactiegeschiedenis voor het product zou er als volgt uitzien:
    - Een voorraadtransactie 1, kosten van 16,00, een boekingsdatum 15 januari en de transactiedatum 15 januari.
    - Een voorraadcorrectie van 1, kosten van 20,00, een boekingsdatum 1 januari en de transactiedatum 15 januari.
1. De correctie boeken.

Op de pagina **Voorraadtransacties** ziet u dat 4,00 als kosten zijn opgevoerd aangezien het huidig zwevend gemiddelde voor het product 16,00 is. U kunt boeken in het verleden, maar het verschil in kosten wordt als last opgenomen, waardoor de zwevend gemiddelde kostprijs niet wordt beïnvloed.

## <a name="negative-inventory-balances"></a>Negatieve voorraadsaldi

Transacties worden verschillend afgehandeld, afhankelijk van of de nieuwe voorhanden hoeveelheid na de transactie negatief, nul of positief is.

### <a name="new-balance-is-negative-or-zero"></a>Nieuw saldo is negatief of nul

Als de nieuwe voorhanden hoeveelheid negatief of nul is, wordt de kostprijs van de transactie bij de huidige gemiddelde kosten berekend. Als er een verschil is tussen de inkoopprijs en de huidige gemiddelde kosten, wordt dit geboekt naar **Prijsverschil voor zwevend gemiddelde**.

### <a name="new-balance-is-positive"></a>Nieuw saldo is positief

Als de nieuwe voorhanden voorraad positief is na de transactie, wordt de transactie opgesplitst in twee delen en wordt de kostprijs verschillend berekend, zoals wordt samengevat in de volgende tabel.

| Deel | Beschrijving |
|---|---|
| Hoeveelheid van negatief naar nul | De voorraad gebruikt de huidige zwevend gemiddelde kostprijs van het artikel in plaats van de transactiekosten voor dat gedeelte van de ontvangsthoeveelheid waardoor het saldo van de voorhanden voorraad wordt verhoogd van negatief naar nul. Het verschil is tussen de transactiekosten en de huidige gemiddeld zwevende kostprijs wordt geboekt naar **Prijsverschil voor zwevend gemiddelde**. |
| Hoeveelheid van nul naar positief | De voorraad gebruikt de transactiekosten voor dat gedeelte van de ontvangsthoeveelheid waarmee het saldo van de voorhanden voorraad wordt verhoogd van nul naar positief.                                                  |

## <a name="inventory-value-report"></a>Voorraadwaardenrapport

In dit voorbeeld van zwevend gemiddelde wordt het voorraadwaarderapport afgedrukt ter ondersteuning van de berekening van het huidige zwevend gemiddelde voor een product. Het rapport Voorraadwaarde kan de transacties in chronologische volgorde afdrukken, samen met de kosten ter ondersteuning van de zwevend gemiddelde kostenberekening van een product. Het rapport bevat de zwevend gemiddelde kosten voor het product. In het dialoogvenster **Voorraadwaardenrapporten** kunt u via een datuminterval de **Transactietijd** of de **Boekingsdatum** selecteren om het rapport op te sorteren. Gewoonlijk wordt het rapport afgedrukt via de optie **Boekingsdatum**. De optie **Transactietijd** is de werkelijke datum waarop de transactie wordt gerapporteerd en waarop de zwevend gemiddelde kosten voor het product worden bijgewerkt. U kunt het rapport Voorraadwaarde afdrukken met de sorteeroptie **Transactietijd** als u de gemiddelde kostprijsberekening gedurende een bepaalde tijd wilt bekijken. De volgende tabel geeft de transacties voor het product weer die op het rapport zullen worden afgedrukt indien de sorteeroptie **Transactietijd** wordt gebruikt.

| Transactietijd | Datum         | Transactietype           | De hoeveelheid | Bedrag | Gemiddelde eenheidskosten |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1 oktober    | Openingssaldo          | 0        | 0,00   | 0,00              |
| 8 oktober        | 28 september | Geantedateerde ontvangst          | 1        | 16,00  | 16,00             |
| 3 oktober        | 3 oktober    | Inkoopontvangst           | 2        | 20,00  | 12,00             |
| 5 oktober        | 5 oktober    | Verkooporder                | -1       | -10,00 | 13,00             |
| 7 oktober        | 7 oktober    | Inkoopfactuur           |          | 2,00   | 14,00             |
| 8 oktober        | 8 oktober    | Herwaardering zwevend gemiddelde |          | 4.00   | 16.00             |
|                  | 31 oktober   | Totaal                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> U kunt het grootboek niet op de voorraad afstemmen met de sorteeroptie **Transactietijd**. Het rapport moet worden afgedrukt met behulp van de optie **Boekingsdatum** .


[!INCLUDE[footer-include](../../includes/footer-banner.md)]