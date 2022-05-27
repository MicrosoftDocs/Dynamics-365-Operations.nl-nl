---
title: Overzicht van Kostprijsberekeningsversies
description: Dit artikel bevat informatie over kostprijsberekeningsversies, hoe u deze onderhoudt en de typen gegevens die u hierin kunt opnemen. Een kostprijsberekeningsversie is primair bedoeld om kostenrecords te bevatten over artikelen, kostencategorieën en berekeningsformules voor indirecte kosten.
author: JennySong-SH
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "54532"
- intro-internal
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f83c35872c769ffd14894aaacc729b031d76504
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670491"
---
# <a name="costing-versions-overview"></a>Overzicht van Kostprijsberekeningsversies

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over kostprijsberekeningsversies, hoe u deze onderhoudt en de typen gegevens die u hierin kunt opnemen. Een kostprijsberekeningsversie is primair bedoeld om kostenrecords te bevatten over artikelen, kostencategorieën en berekeningsformules voor indirecte kosten.

Een kostprijsberekeningsversie kan een of meer functies hebben, afhankelijk van de gegevens die de kostprijsberekeningsversie bevat. Een kostprijsberekeningsversie is primair bedoeld om kostenrecords te bevatten over artikelen, kostencategorieën en berekeningsformules voor indirecte kosten. Een kostprijsberekeningsversie kan een set standaardkostenrecords bevatten, of een set geplande kostenrecords die zijn gebaseerd op het kostprijsberekeningstype dat is toegewezen aan de kostprijsberekeningsversie.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Kostprijsberekeningsversies voor standaardkosten of geplande kosten
### <a name="standard-costs"></a>Standaardkosten

Een kostprijsberekeningsversie kan een standaardkostprijsvoorraadmodel voor artikelen ondersteunen, waarbij de kostprijsberekeningsversie een set standaardkostenrecords over artikelen en productieprocessen bevat. Kostengegevens over productieprocessen worden uitgedrukt in termen van de kostencategorieën voor routeringsbewerkingen en de berekeningsformules voor productieoverhead.

### <a name="planned-costs"></a>Geplande kosten

Een kostprijsberekeningsversie kan een set geplande-kostenrecords bevatten over artikelen en productieprocessen. Een kostprijsberekeningsversie met geplande kosten wordt vaak gebruikt om kostenberekeningsimulaties te ondersteunen, zoals simulaties van het effect van kostenwijzigingen voor ingekocht materiaal of productieprocessen op de berekende kosten van gefabriceerde artikelen. De artikelkostenrecords voor geplande kosten kunnen ook worden gebruikt om een werkelijke-kostenvoorraadmodel te ondersteunen door de beginwaarden op te geven van artikelkosten, waaronder de berekening van geplande kosten voor gefabriceerde artikelen.

## <a name="entering-costs"></a>Kosten invoeren
Bij het gegevensonderhoud van kostenrecords in een kostprijsberekeningsversie hoort het opgeven van kosten voor ingekochte artikelen en voor artikelen die zijn overgeboekt tussen locaties. Bij het extra gegevensonderhoud voor fabrikanten hoort het opgeven van kosten voor kostencategorieën die zijn gekoppeld aan routebewerkingen, het opgeven van berekeningsformules voor de indirecte kosten voor productieoverheads en het berekenen van kosten voor gefabriceerde artikelen. 

De artikelkostengegevens in een kostprijsberekeningsversie bestaan uit een of meer kostenrecords voor elk artikel. Een artikelkostenrecord wordt eerst ingevoerd met de status **In behandeling** en met een gewenste begindatum. Als u de artikelkostenrecord activeert, wordt de status naar **Actief** en de begindatum naar de activeringsdatum bijgewerkt. Verschillende artikelkostenrecords staan mogelijk voor verschillende locaties, begindatums of statusvarianten. Bij het berekenen van de kosten voor gefabriceerde artikelen voor een datum in de toekomst gebruikt de stuklijstberekening kostenrecords met de relevante begindatum, of de status nu **In behandeling** of **Actief** is. De huidige actieve kostenrecord van een artikel wordt gebruikt voor het schatten van de productieorderkosten en het waarderen van de voorraadtransacties onder een standaardmodel voor de kostprijsberekening van de voorraad. Het onderhoud van kostenrecords voor kostencategorieën en indirecte kostenberekeningsformules is vergelijkbaar met het onderhoud van artikelkostenrecords. 

Twee blokkeringsbeleidvarianten voor een kostprijsberekeningsversie bepalen of kosten die in behandeling zijn, kunnen worden bijgehouden en of deze kunnen worden geactiveerd. Gebruik het blokkeringsbeleid om gegevensonderhoud toe te staan en vervolgens het gegevensonderhoud voor kostenrecords in een kostprijsberekeningsversie te voorkomen. 

Een kostprijsberekeningsversie kan ook gegevens bevatten over artikelverkoopprijzen of inkoopprijzen om stuklijsten te kunnen berekenen.

## <a name="item-sales-prices-for-bom-calculations"></a>Artikelverkoopprijzen voor stuklijstberekeningen
De belangrijkste reden voor het opnemen van gegevens over verkoopprijzen is het behouden van de berekende verkoopprijs van een geproduceerd artikel. De berekende verkoopprijs kan dan worden geanalyseerd om te bepalen hoe componenten, routebewerkingen en overhead aan de kost- en verkoopprijs bijdragen. 

Een secundaire reden voor het opnemen van gegevens over verkoopprijzen is het definiëren van de verkoopprijsrecords voor componentartikelen. Deze records kunnen dan worden gebruikt om de verkoopprijs van geproduceerde artikelen berekenen. Eerst definieert u het verkoopprijsmodel dat is ingesloten in de berekeningsgroep van een stuklijst en dan wijst u de berekeningsgroep van de stuklijst toe aan ingekochte artikelen. Selecteer dan, wanneer u stuklijstberekeningen met geplande kosten uitvoert, het kostprijsmodel van de berekeningsgroep van de stuklijst. 

Anders worden de verkoopprijsrecords voor artikelen alleen ter informatie gebruikt, ongeacht of de records handmatig worden ingevoerd of berekend. Door het verkoopprijsrecord van een artikel te activeren, kunt u de basisverkoopprijs van het artikel bijwerken. De basisverkoopprijs is echter niet sitespecifiek en kan handmatig worden overschreven. De basisverkoopprijs van het artikel wordt als standaardverkoopprijs gebruikt op verkooporders en verkoopoffertes.

## <a name="item-purchase-prices-for-bom-calculations"></a>Artikelinkoopprijzen voor stuklijstberekeningen
De belangrijkste reden voor het inschakelen van inkoopprijsgegevens is het definiëren van inkoopprijsrecords voor componentartikelen, zodat deze records kunnen worden gebruikt om de kosten van gefabriceerde artikelen te berekenen. De artikelinkoopprijsrecords moeten handmatig worden ingevoerd. 

Als u inkoopprijsinhoud wilt inschakelen, definieert u eerst een stuklijstberekeningsgroep die een kostprijsmodel voor de inkoopprijs voor het artikel bevat en vervolgens wijst u de stuklijstberekeningsgroep toe aan ingekochte artikelen. Vervolgens gebruikt u een kostprijsmodel voor de stuklijstberekeningsgroep wanneer u stuklijstberekeningen met geplande kosten uitvoert om de verkoopprijs van gefabriceerde artikelen te berekenen. 

De inkoopprijsrecords voor artikelen worden ook gebruikt als verwijzingsinformatie. Door de status van de inkoopprijsrecord van een artikel te wijzigen van **In behandeling** in **Actief**, kunt u de basisinkoopprijs van het artikel bijwerken. De basisinkoopprijs is echter niet sitespecifiek en kan handmatig worden overschreven. De basisinkoopprijs van het artikel wordt gebruikt als standaardinkoopprijs op inkooporders.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]