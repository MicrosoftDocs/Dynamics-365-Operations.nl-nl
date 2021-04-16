---
title: Een productieorder plannen
description: Deze procedure toont hoe u een productieorder plant.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a52e2ee3bf0c5dadeda375882d16de60b31d658
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831885"
---
# <a name="schedule-a-production-order"></a>Een productieorder plannen

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u een productieorder plant. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de derde procedure van zeven die de productieorderlevenscyclus beschrijven.


## <a name="schedule-a-production-order"></a>Een productieorder plannen
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
    * Selecteer een productieorder met de status Geschat.  
2. Klik in het actievenster op Plannen.
3. Klik op Taken plannen.
    * De parameters voor planning worden ingesteld op deze pagina. U kunt de parameters instellen voor specifieke gebruikers of alle gebruikers.  
4. Selecteer in het veld Planningsrichting de optie 'Verder vanaf vandaag'.
5. Voer in het veld Planningsdatum een datum in.
6. Schakel het selectievakje Eindige capaciteit in of uit.
7. Schakel het selectievakje Eindig materiaal in of uit.
8. Klik op OK.

## <a name="view-the-scheduling-results"></a>De resultaten van planning weergeven
1. Klik in het actievenster op Productieorder.
2. Klik op Alle taken.
    * Deze pagina toont de geplande taken die u zojuist hebt gegenereerd.  
3. Vouw de sectie Planning uit of samen.
    * Op het sneltabblad Planning kunt u de geplande datum en tijd weergeven.  
4. Klik op Query's.
5. Klik op Capaciteitsbelasting.
    * De pagina Capaciteitsbelasting toont de capaciteit die is gereserveerd via taakplanning, het totale aantal uren dat momenteel is gereserveerd voor de resource en het aantal uren dat beschikbaar is voor taakplanning voor de resource.  
6. Sluit de pagina.
7. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]