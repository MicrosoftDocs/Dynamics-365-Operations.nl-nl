---
title: Voorraadhoeveelheden reserveren
description: Dit onderwerp beschrijft de verschillende opties die beschikbaar zijn voor het reserveren van voorraad.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 942a1e9ddcf6e0952da66b239e1884cb83369175
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="reserve-inventory-quantities"></a>Voorraadhoeveelheden reserveren

[!include[banner](../includes/banner.md)]


Dit onderwerp beschrijft de verschillende opties die beschikbaar zijn voor het reserveren van voorraad.

U kunt automatisch voorraadhoeveelheden voor een bepaalde verkooporder reserveren. De consequentie hiervan is, dat gereserveerde voorraad in het magazijn niet voor andere orders kan worden gebruikt, tenzij de reservering van de voorraad in zijn geheel of gedeeltelijk wordt geannuleerd.

Er zijn verschillende redenen voor het reserveren van voorraad:
-   'Wie het eerst komt, het eerst maalt'. Dit betekent dat de klanten de artikelen geleverd krijgen in de volgorde waarop hun bestellingen zijn binnengekomen.
-   Tekort aan artikelen als gevolg van een lange of onbekende leveringstijd van de leverancier. In dat geval is het misschien nodig bepaalde klanten als eerste te leveren wanneer de artikelen weer op voorraad zijn.
-   Bepaalde klanten en bepaalde typen orders moeten het eerst worden verwerkt.
-   Artikelen met serie- of batchnummers. U kunt bepaalde artikelen markeren die voor specifieke orders zijn geleverd of nog moeten worden geleverd.
-   Speciaal bestelde artikelen die voor bepaalde orders zijn gereserveerd.
-   Productieorders. U kunt bijvoorbeeld artikelen markeren die speciaal voor bepaalde orders zijn geproduceerd of aangepast.

Er kan automatisch voorraad worden gereserveerd wanneer een nieuwe orderregel wordt gemaakt, maar de voorraad kan ook handmatig bij elke order afzonderlijk worden gereserveerd. Het is ook mogelijk om voorraad in verschillende fasen in een productieproces te reserveren. Alleen de opgeslagen producten kunnen worden gereserveerd. Services kunnen niet worden gereserveerd omdat er geen voorhanden voorraad is. Zowel de voorhanden als de bestelde maar nog niet ontvangen voorraad kunnen worden gereserveerd. Als er meer is gereserveerd dan er op voorraad is, verschijnt er een bericht dat een dergelijke grote hoeveelheid niet kan worden gereserveerd. U kunt de hoeveelheid toch reserveren of een kleinere hoeveelheid bestellen. De hoeveelheid kan worden gereserveerd of worden gewijzigd. Als er meer artikelen worden gereserveerd dan er op voorraad zijn, wordt het tekort gedekt wanneer er voldoende artikelen op voorraad zijn om te kunnen leveren.

## <a name="inventory-reservation-policies"></a>Reserveringsbeleid van voorraad
Het reserveringsbeleid van de voorraad wordt ingesteld op de pagina **Artikelmodelgroepen**, de pagina **Parameters voor voorraad- en magazijnbeheer** en de pagina **Productieparameters**.
### <a name="policies-on-the-item-model-groups-page"></a>Beleid op de pagina Artikelmodelgroepen

De sectie **Voorraadbeleid** bevat het volgende reserveringsbeleid.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reserveringsbeleid**  | **Omschrijving**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Gecontroleerde FIFO-datum    | Als u de optie **Gecontroleerde FIFO-datum** selecteert, wordt de voorraad volgens een sorteringsdatum gereserveerd door de FIFO-methode (First In First Out) te gebruiken. U kunt batches reserveren op basis van de vroegste ontvangstdatum van artikelen of volgens de FIFO-methode (First In First Out).                                                                                                                                                                                                                                                                       |
| Terug vanaf verzenddatum | Deze optie wordt beschikbaar als u de optie **Gecontroleerde FIFO-datum** hebt geselecteerd. Schakelt u het selectievakje **Terug vanaf verzenddatum** in, dan wordt de voorraad vanaf de gewenste verzenddatum met behulp van de LIFO-methode (Last In First Out) gereserveerd. Als er geen ontvangsten vóór de verzenddatum beschikbaar zijn, wordt er een FIFO-reservering gebruikt.                                                                                                                                                                                                           |
| Artikelverkoopreservering  | Bepaalt of de artikelen automatisch of handmatig worden gereserveerd. Als een reservering automatisch is, reserveert u voorraad wanneer orderregels worden gemaakt. Het is mogelijk om reserveringen voor het artikelnummerniveau voor stuklijsten (optie **Automatisch**) of voor de individuele elementen van een stuklijst (optie **Explosie**) te maken. De standaardwaarde voor **Artikelverkoopreservering** kan van **Klantparameters** zijn overgenomen. Op die pagina wordt de waarde ingesteld in het veld **Reservering** in de sectie **Standaardwaarden verkoop** op het tabblad **Algemeen**. |
| Dezelfde batchselectie    | Met reserveringen uit dezelfde batch kunt u voorraad reserveren voor een verkooporderregel uit één voorraadbatch. Als u deze optie wilt gebruiken, moet u ook de optie **Behoeften consolideren** instellen op **Ja**. Er zijn extra instellingen die voor de traceringsdimensiegroep en de opslagdimensiegroep zijn vereist. Zie voor meer informatie [Dezelfde batch voor een verkooporder reserveren](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Behoeften consolideren | Deze optie is vergelijkbaar met de optie **Dezelfde batchselectie** en hiermee wordt voorraad geconsolideerd die voor verkooporderregels in één behoefte is gereserveerd.                                                                                                                                                                                                                                                                                                                                                                                      |
| Gecontroleerde FEFO-datum    | Met deze optie kunt u batches reserveren die dicht bij hun de vervaldatum of houdbaarheidsdatum zijn. U moet ook het veld **Orderverzamelcriteria** instellen om **Vervaldatum** of **Uiterste houdbaarheidsdatum** te selecteren.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Voorbeeld voor Gecontroleerde FIFO-datum en Terug vanaf verzenddatum

In dit voorbeeld bestaat voorhanden voorraad voor artikelnummer A voor drie verschillende batchnummers.
| artikelnummer | Batchnummer | Hoeveelheid | Datum             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5        | 2 februari 2016 |
| A           | 1001         | 3        | 1 januari 2016  |
| A           | 1002         | 7        | 3 maart 2016    |

Bij een verkooporder die automatisch moet worden gereserveerd en moet worden geleverd op 4 april 2016, wordt de volgende batch gereserveerd:
-   Als zowel het selectievakje **Gecontroleerde FIFO-datum** als het selectievakje **Terug vanaf verzenddatum** is uitgeschakeld, wordt batch 1000 gereserveerd omdat dat de batchis met het laagste nummer.
-   Als het selectievakje **Gecontroleerde FIFO-datum** is ingeschakeld en het selectievakje **Terug vanaf verzenddatum** is uitgeschakeld, wordt batch 1001 gereserveerd omdat dat de batch met de eerste ontvangstdatum is (FIFO).
-   Als zowel het selectievakje **Gecontroleerde FIFO-datum** als het selectievakje **Terug vanaf verzenddatum** is ingeschakeld, wordt batch 1002 gereserveerd omdat dat de batchontvangst is die het dichtst bij de verzenddatum van de verkooporder ligt.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Beleid op de pagina Parameters voor voorraad- en magazijnbeheer

Er zijn twee opties met betrekking tot reserveringen op de pagina de **Parameters voor voorraad- en magazijnbeheer**:
-   Met de optie **Bestelde artikelen reserveren** op het tabblad **Algemeen** kunt u artikelontvangsten reserveren die worden besteld voor artikeluitgiften in Klanten, Projectbeheer en boekhouding en Productiecontrole. Als u deze optie uitschakelt, kunt u alleen artikelen reserveren die fysiek zijn ontvangen. Als een bepaald artikel is ingesteld voor ontvangst van negatieve voorraad, is dit veld niet relevant.
-   De optie **Artikelen automatisch reserveren** optie op het tabblad **Transport** definieert de standaardinstelling als de artikelen automatisch voor transferorders zijn. De standaardinstellingen kunnen op afzonderlijke transferorders worden overschreven.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Het voorraadreserveringsbeleid op de pagina Productieparameters

De waarde van het veld **Reservering** op het tabblad **Algemeen** op de pagina **Productieparameters** bepaalt het standaardpunt in het productieproces waarop de voorraad moet worden gereserveerd. De voorraad kan bijvoorbeeld worden gereserveerd wanneer het werk wordt gepland of wanneer het werk is gestart.




