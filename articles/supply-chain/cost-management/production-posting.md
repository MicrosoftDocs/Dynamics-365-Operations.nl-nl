---
title: Productieboeking
description: Dit artikel bevat informatie over verschillende typen boekingen in het productieproces.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20a94ed3c64e81013edfa10e060dd32e04d12577
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214476"
---
# <a name="production-posting"></a>Productieboeking

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over verschillende typen boekingen in het productieproces.

Activiteiten die betrekking hebben op productieboekingen, worden uitgevoerd conform de productieprocessen die in de onderstaande secties worden beschreven.

## <a name="material-consumption"></a>Materiaalverbruik
Materialen worden geregistreerd als verbruikt tijdens de productie wanneer de lijst van het productieorderverzamellijstjournaal is geboekt. Dit proces genereert uitgiftetransacties die de voorhanden voorraad aftrekken. In de productieparameters kunt u opgeven of de waarde van grondstoffen die worden uitgevoerd (onderhanden werk \[OHW\]) in het grootboek moeten worden geboekt. De waarde van grondstoffen die worden uitgevoerd (OHW) worden vervolgens geboekt naar een specifieke Orderverzamellijstrekening en een specifieke tegenrekening voor orderverzamellijst.

## <a name="time-consumption"></a>Tijdverbruik
De tijd die de werknemers doorbrengen in productietaken wordt geregistreerd in het routekaartjournaal of het taakkaartjournaal. Wanneer deze journalen worden geboekt, wordt grootboekboeking naar een specifieke rekening voor resources die worden uitgevoerd (OHW) verwerkt. Deze boeking staat voor de waarde van de tijd die is besteed aan de productieorder. Nadat de productieorder als beëindigd is geregistreerd, worden de OHW-rekeningen vereffend.

## <a name="reporting-finished-goods-and-error-quantities"></a>Afgewerkte goederen en fouthoeveelheden rapporteren
Wanneer een productorder is gereedgemeld, wordt de hoeveelheid afgewerkte goederen die zijn voltooid in Voorraadbeheer bijgewerkt via het Gereedmeldingsjournaal. Als u OHW-boekhouding gebruikt, die in de productieparameters kan worden ingesteld, wordt een grootboekjournaal gemaakt om de OHW-rekeningen te verlagen en de voorraad van afgewerkte producten te verhogen. Het journaal gebruikt de standaardkosten die voor het product zijn gedefinieerd.

## <a name="ending-the-production-order"></a>De productieorder beëindigen
Voordat een productieorder wordt beëindigd, worden de werkelijke kosten berekend voor de hoeveelheid die is geproduceerd. Alle geraamde kosten van materiaal, arbeid en overhead worden teruggeboekt en worden vervangen door de werkelijke kosten. De algehele kosten van het afgewerkte artikel worden gedebiteerd op de voorraadontvangstrekening en gecrediteerd op de voorraaduitgifterekening. Als u het selectievakje **Eindtaak** inschakelt bij het uitvoeren van de kostenberekening, wijzigt de status van de productieorder in **Beëindigd**. Deze status wordt voorkomen dat extra kosten onbedoeld op een voltooide productieorder worden geboekt. U kunt opgeven dat de waarde van fouthoeveelheden die tijdens het rapporteren werden gereedgemeld, moeten worden toegewezen aan goede hoeveelheden die zijn gereedgemeld. U kunt ook opgeven dat de waarde van fouthoeveelheden naar een specifieke uitvalrekening moeten worden geboekt.

## <a name="controlling-the-level-of-ledger-posting"></a>Het niveau van het grootboek beheren
In **Parameters van productiecontrole** kunt u het veld **Boeking in grootboek** gebruiken om het niveau van grootboek in te stellen voor productieprocessen. De volgende waarden zijn beschikbaar:

-   **Artikel en resource** - Gebruik de grootboekrekeningen die zijn ingesteld op de artikelengroepen voor grondstoffen en afgewerkte goederen. OHW voor tijdverbruik wordt overgenomen uit resource of resourcegroep van de routebewerkingen.
-   **Artikel en categorie** - Gebruik de grootboekrekeningen die zijn ingesteld op de artikelengroepen voor grondstoffen en afgewerkte goederen. OHW voor tijdverbruik wordt overgenomen van de kostencategorieën die aan de routebewerkingen worden gekoppeld.
-   **Productiegroepen** - Gebruik de grootboekrekeningen die zijn ingesteld op de productiegroepen voor zowel materiaal- als tijdverbruik. De productiegroepen worden gekoppeld aan de vrijgegeven producten en gekopieerd naar de productieorders wanneer deze orders worden gemaakt. Het boeken op de productieorders zal dan de productiegroepen volgen die aan de productieorder zijn gekoppeld.

**Opmerking:** Als de standaardmethode voor het berekenen van de kosten van het afgewerkte artikel werd gebruikt, komt dit terug in de definitieve transacties. Is de werkelijke kosten en de kosten die met de standaardmethode zijn berekend verschillen, wordt het verschil geboekt naar de rekening waarop de winst of het verlies is te zien.



