--- 
title: Een productieorder plannen met bewerkingen en taakplanning
description: Deze procedure is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Een productieorder plannen met bewerkingen en taakplanning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning. Er worden geen taken gemaakt met bewerkingsplanning, terwijl er wel taken worden gemaakt met taakplanning. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze procedure is bedoeld voor de productiemanager, productieplanner of werkvloersupervisor in een discrete productie-omgeving.


## <a name="create-a-production-order"></a>Een productieorder maken
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
2. Klik op Nieuwe productieorder.
3. Typ of selecteer een waarde in het veld Artikelnummer.
    * Selecteer artikelnummer D0001.  
4. Klik op Maken.

## <a name="schedule-operations-for-the-production-order"></a>Bewerkingen plannen voor de productieorder.
1. Markeer in de lijst de geselecteerde rij.
    * Selecteer de productieorder die u zojuist hebt gemaakt. Deze moet boven aan de lijst staan.      
2. Klik in het actievenster op Plannen.
3. Klik op Bewerkingen plannen.
4. Selecteer in het veld Planningsrichting de optie "Verder vanaf planningsdatum".
5. Voer in het veld Planningsdatum een datum in.
    * Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week. Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.  
6. Klik op OK.
7. Markeer in de lijst de geselecteerde rij.
    * Houd er rekening mee dat de status wordt gewijzigd in Gepland.  
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik op Alle taken.
    * Houd er rekening mee dat er geen taken worden gemaakt met bewerkingsplanning.  
10. Sluit de pagina.

## <a name="schedule-jobs-for-the-production-order"></a>Taken plannen voor de productieorder.
1. Klik in het actievenster op Plannen.
2. Klik op Taken plannen.
3. Selecteer in het veld Planningsrichting de optie "Verder vanaf planningsdatum".
4. Voer in het veld Planningsdatum een datum in.
    * Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week. Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.  
5. Klik op OK.
6. Klik in het actievenster op Productieorder.
7. Klik op Alle taken.
    * Merk op dat op basis van de actieve route, 5 taken worden gemaakt met taakplanning.  


