---
title: Een artikel of een grondstof traceren
description: Deze procedure toont aan hoe u artikeltracering kunt gebruiken om te bepalen waar artikelen of grondstoffen zijn of worden gebruikt.
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c4b093af672b2d4e1a2c91cd55470f9072d992c3
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="trace-an-item-or-raw-material"></a>Een artikel of een grondstof traceren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont aan hoe u artikeltracering kunt gebruiken om te bepalen waar artikelen of grondstoffen zijn of worden gebruikt. Met deze procedure kunt u een artikel identificeren, het terug naar de bron traceren en vervolgens voorwaarts door de productie en de verkoop van het eindproduct traceren. Het proces kan worden gebruikt voor het onderzoeken van de beïnvloede klanten, de betrokken verkooporders en meer. Bij deze procedure wordt het demobedrijf USP2 gebruikt.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Een artikel met een bekend batchnummer achterwaarts traceren
1. Ga naar Voorraadbeheer > Query's en rapporten > Traceerdimensies > Artikeltracering.
2. Selecteer P9100 in het veld Artikelnummer.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Selecteer 'Achterwaarts' in het veld Voorwaarts of achterwaarts.
5. Selecteer as-12-344-01 in het veld Batchnummer.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op OK.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Een artikel identificere, achterwaarts traceren en een analyse maken
    * Het bovenste knooppunt van de structuur toont de voorhanden hoeveelheid van het geselecteerde artikel en de geselecteerde batch. U moet de knooppunten van de structuur uitvouwen om het artikel te zoeken waarop de voorwaartse tracering moet worden uitgevoerd.   
1. Vouw in de structuur de hieronder beschreven knooppunten uit en selecteer vervolgens het laatste knooppunt.
    * Vouw het volgende uit: 'P9100 / 1 / 10 / as-12-344-01 ● 2 vaatjes ● 7,00 gal \P9100 ● Verzameld ● Verkooporder 000072 ● 22-12-2015 ● -1 vaatje ● -4,00 gal ● Vestiging=1, Magazijn=10, Batchnummer=as-12-344-01 \P9100 ● Productie B-000050 ● 9-12-2015● 7 vaatjes ● 27,00 gal ● Vestiging=1,Magazijn=10,Batchnummer=as-12-344-01 ● Coproducten: P9101' en selecteer vervolgens dat knooppunt.     
2. Vouw in de structuur het hieronder beschreven knooppunt uit en selecteer vervolgens dat knooppunt.
    * Beginnend met het knooppunt dat u zojuist hebt geselecteerd, vouwt u 'M9103 ● Productieregel B-000050 ● 9-12-2015 ● -160,00 lb ● Grootte=70, Kleur=OK, Vestiging=1, Magazijn=10, Batchnummer=App01' uit en selecteert u vervolgens dat knooppunt.  
3. Klik op Tracering vanaf knooppunt.
4. Klik op Voorwaarts.
5. Klik in het actievenster op Tracering.
    * Er zijn verschillende traceringopties die informatie over de klanten bevatten waarop het artikel dat u traceert van invloed is, en de verkooporders die aan het artikel zijn gerelateerd die niet en wel zijn verzonden.   
6. Klik op Klanten.
7. Sluit de pagina.
8. Klik in het actievenster op Tracering.
9. Klik op Verzonden verkooporders.
10. Sluit de pagina.
