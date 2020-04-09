---
title: Een planning voor een vestiging maken
description: Deze procedure laat zien hoe u productieorders plant die nog niet voor een vestiging zijn gestart.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1273297a7a48da11b1448f153a151c2a7b461d0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148050"
---
# <a name="create-a-schedule-for-a-site"></a>Een planning voor een vestiging maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u productieorders plant die nog niet voor een vestiging zijn gestart.  Het demobedrijf USMF wordt gebruikt om deze procedure te voltooien.


## <a name="identify-production-orders-that-are-not-started"></a>Productieorders identificeren die niet zijn gestart
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Vestiging met een waarde van '1'.
    * 1 staat voor een vestiging in USMF. Als u geen USMF gebruikt, selecteert u een vestiging van uw eigen bedrijf.  
3. Open de kolomfilter Status.
4. Pas een filter op het veld "Status" toe met een waarde van "Gepland" met behulp van de filteroperator "is exact".

## <a name="create-a-schedule"></a>Een planning maken
1. Selecteer of deselecteer alle rijen in de lijst.
2. Klik in het actievenster op Plannen.
3. Klik op Taken plannen.
4. Selecteer in het veld Planningsrichting de optie "Terug vanaf leveringsdatum".
5. Selecteer Nee in het veld Eindige capaciteit.
6. Selecteer Nee in het veld Eindig materiaal.
7. Klik op OK.
    * Dit kan enige tijd duren.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Het resultaat van geplande productieorders weergeven
1. Markeer in de lijst de geselecteerde rij.
    * U kunt elke rij markeren.  
2. Klik in het actievenster op Productieorder.
3. Klik op Alle taken.
    * Op deze pagina kunt u de lijst met taken bekijken. Op het tabblad Planning kunt u de begindatum en de einddatum voor een taak zien.  
4. Klik op Materialen.
    * Op deze pagina kunt u het geschatte materiaalverbruik voor de bewerkingen op de productieorder en de huidige beschikbare voorraad bekijken.  

