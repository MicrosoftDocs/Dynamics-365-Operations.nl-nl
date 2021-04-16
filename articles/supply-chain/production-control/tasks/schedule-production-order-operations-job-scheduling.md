---
title: Een productieorder plannen met bewerkingen en taakplanning
description: Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841378"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Een productieorder plannen met bewerkingen en taakplanning

[!include [banner](../../includes/banner.md)]

Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning. Er worden geen taken gemaakt met bewerkingsplanning, terwijl er wel taken worden gemaakt met taakplanning. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze procedure is bedoeld voor de productiemanager, productieplanner of werkvloersupervisor in een discrete productie-omgeving.


## <a name="create-a-production-order"></a>Een productieorder maken
1. Ga in het navigatievenster naar **Modules > Productiebeheer > Productieorders > Alle productieorders**.
2. Selecteer **Nieuwe productieorder**.
3. Typ of selecteer een waarde in het veld **Artikelnummer**. Selecteer artikelnummer **D0001**.  
4. Selecteer **Maken**.

## <a name="schedule-operations-for-the-production-order"></a>Bewerkingen plannen voor de productieorder.
1. Markeer de nieuwe rij.      
2. Selecteer in het actievenster de optie **Planning**.
3. Selecteert **Bewerkingen plannen**.
4. Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.
5. Voer in het veld **Planningsdatum** een datum in. Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week. Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.  
6. Selecteer **OK**.
7. Markeer in de lijst de geselecteerde rij. Houd er rekening mee dat de status wordt gewijzigd in **Gepland**. 
8. Selecteer **Alle taken**. Houd er rekening mee dat er geen taken worden gemaakt met bewerkingsplanning.  
9. Sluit de pagina.

## <a name="schedule-jobs-for-the-production-order"></a>Taken plannen voor de productieorder.
1. Selecteer in het actievenster de optie **Planning**.
2. Selecteer **Taken plannen**.
3. Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.
4. Voer in het veld **Planningsdatum** een datum in. Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week. Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.  
5. Selecteer **OK**.
6. Selecteer **Productieorder** in het actievenster.
7. Selecteer **Alle taken**. Merk op dat op basis van de actieve route, 5 taken worden gemaakt met taakplanning.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]