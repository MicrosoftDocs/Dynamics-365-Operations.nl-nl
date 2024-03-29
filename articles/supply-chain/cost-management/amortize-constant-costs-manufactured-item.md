---
title: Constante kosten voor een gefabriceerd artikel afschrijven
description: De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben.
author: JennySong-SH
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: d466395859e19874183691e697c8aca3a774d359
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675398"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Constante kosten voor een gefabriceerd artikel afschrijven

[!include [banner](../includes/banner.md)]

De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben. 

Het concept van de partijgrootte voor kostprijsberekening wordt gebruikt om deze constante kosten af te schrijven via de berekende kosten van een gefabriceerd artikel. Dit concept heeft verschillende synoniemen, waaronder partijgrootte voor boekhouding. Het concept van het afschrijven van constante kosten heeft ook verschillende synoniemen, waaronder proportionele constante kosten.

De hoeveelheid van de partijgrootte voor kostprijsberekening wordt gebruikt in een stuklijstberekening. De hoeveelheid is afhankelijk van de manier waarop u de stuklijstberekening initieert en uitvoert, zoals wordt geïllustreerd door het volgende:

-   Standaardberekeningshoeveelheid in stuklijstberekening van een artikel - De standaardorderhoeveelheid voor voorraad van het artikel fungeert als partijgrootte voor boekhouding, maar de standaardwaarde kan een grotere hoeveelheid zijn om het veelvoud van de orderhoeveelheid van het artikel aan te geven. De standaardorderhoeveelheid en veelvoud van het artikel kunnen in de standaardorderinstellingen of locatiespecifieke orderinstellingen worden opgegeven.
-   Opgegeven berekeningshoeveelheid in de stuklijstberekening van een artikel - De opgegeven berekeningshoeveelheid dient als de partijgrootte voor kostprijsberekening voor het artikel. De berekeningshoeveelheid gebruikt de standaardorderhoeveelheid van het artikel, maar de standaardwaarde kan handmatig worden overschreven. De opgegeven berekeningshoeveelheid representeert de partijgrootte voor kostprijsberekening voor het opgegeven artikel en voor gefabriceerde onderdelen met het stuklijstregeltype Productie. Dat komt omdat ervan wordt uitgegaan dat het onderdeel wordt gefabriceerd in de exacte hoeveelheid. De partijgrootte voor kostprijsberekening voor andere gefabriceerde onderdelen met het stuklijstregeltype Artikel geeft de standaardorderhoeveelheid weer.
-   Opgegeven Maken naar order-berekeningshoeveelheid in de stuklijstberekening van een artikel - De opgegeven berekeningshoeveelheid dient als de partijgrootte voor kostprijsberekening voor het artikel en de bijbehorende gefabriceerde artikelen wanneer stuklijstberekeningen een Maken naar order-explosiemodus gebruiken. Er wordt uitgegaan van de veronderstelling dat de gefabriceerde onderdelen in de exacte hoeveelheid worden gemaakt, net als een gefabriceerd onderdeel met het stuklijstregeltype Productie.
-   Opgegeven berekeningshoeveelheid in een orderspecifieke stuklijstberekening - Een orderspecifieke stuklijstberekening kan worden uitgevoerd voor een regelartikel op een verkooporder, verkoopofferte of serviceorder. De opgegeven berekeningshoeveelheid gebruikt de hoeveelheid van het oorspronkelijke regelartikel, maar de standaardhoeveelheid kan worden overschreven. U kunt selecteren of u wilt dat de orderspecifieke stuklijstberekening een Maken naar order-explosiemodus of een explosiemodus voor meerdere niveaus gebruikt.

Het berekende bedrag van de afgeschreven constante kosten van een gefabriceerd artikel wordt toeslagen genoemd.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]