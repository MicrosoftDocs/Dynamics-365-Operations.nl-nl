--- 
title: Levensduur van batchorder van aanmaakdatum tot startdatum
description: Deze procedure begeleidt u door het eerste gedeelte van de levensduur van een batchorder.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 94f706241545282fd2744c3be4edc253f2998aff
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Levensduur van batchorder van aanmaakdatum tot startdatum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u door het eerste gedeelte van de levensduur van een batchorder.

Vanaf de creatie, de kostenraming en de productietaakplanning tot het werkelijke begin van een batchorder.



Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. 



De vereisten voor het uitvoeren van de procedure met een andere dataset zijn een vrijgegeven product met een actieve formule en routeversie.


## <a name="create-a-batch-order"></a>Een batchorder maken
1. Ga naar Alle productieorders.
2. Klik op Nieuwe batchorder.
3. Typ of selecteer een waarde in het veld Artikelnummer.
4. Klik op Maken.
5. Gebruik het snelfilter om in het veld Productie te filteren met de waarde 'b'.

## <a name="view-production-formula-and-expected-co-products"></a>Productieformule en verwachte co-producten weergeven
1. Klik in het actievenster op Productieorder.
2. Klik op Formule.
3. Sluit de pagina.
4. Klik op Coproducten.
5. Sluit de pagina.

## <a name="estimate-the-batch-order"></a>De batchvolgorde schatten
1. Klik op Raming.
2. Klik op OK.
3. Klik in het actievenster op Kosten beheren.
4. Klik op Berekeningsdetails weergeven.
5. Sluit de pagina.

## <a name="release-the-batch-order"></a>De batchvolgorde vrijgeven
1. Klik in het actievenster op Productieorder.
2. Klik op Vrijgave.
3. Klik op OK.

## <a name="schedule-production-jobs"></a>Productietaken plannen
1. Klik in het actievenster op Plannen.
2. Klik op Taken plannen.
3. Selecteer Nee in het veld Eindige capaciteit.
4. Selecteer Nee in het veld Eindig materiaal.
5. Klik op OK.
6. Klik in het actievenster op Productieorder.
7. Klik op Alle taken.
8. Sluit de pagina.

## <a name="start-the-batch-order"></a>De batchorder starten
1. Klik op Start.
2. Klik op het tabblad Algemeen.
3. Selecteer Nee in het veld Orderverzamellijst nu boeken.
4. Klik op OK.
5. Klik in het actievenster op Weergeven.
6. Klik op Orderverzamellijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Sluit de pagina.
9. Sluit de pagina.
10. Klik op Routekaart.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
12. Sluit de pagina.
13. Sluit de pagina.


