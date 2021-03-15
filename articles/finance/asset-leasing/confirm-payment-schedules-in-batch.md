---
title: Betalingsschema's voor activaleases in batch bevestigen
description: In dit onderwerp wordt uitgelegd hoe u meerdere betalingsschema's in een batch kunt bevestigen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971373"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Betalingsschema's voor activaleases in batch bevestigen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u meerdere betalingsschema's in een batch kunt bevestigen. Betalingsschema's worden per lease bevestigd of met het bevestigingsbatchproces. Een journaalboeking kan alleen worden geboekt naar een lease met een bevestigd betalingsschema. De bevestiging van het betalingsschema dient als laatste goedkeuring van de financiële gegevens voor de lease. Alle toekomstige wijzigingen in de financiële informatie voor de lease, zoals betalingen en de leasetermijn, vormen een leasecorrectie en moeten op die manier worden verwerkt.

Voer de volgende stappen uit om meerdere betalingsschema's te bevestigen.

1. Ga naar **Activa leasen \> Periodiek \> Bevestigingsbatch**.
2. Selecteer **Bevestigingsbatch** op de pagina **Bevestigingsbatch**.
3. In het dialoogvenster dat wordt weergegeven, filtert u op de boeken die u wilt bevestigen.

    - Om alle boeken in een specifieke leasegroep te bevestigen, selecteert u de groep in het veld **Leasegroep**.
    - Als u specifieke boeken wilt bevestigen, selecteert u de boeken in het veld **Boek-id**.
    - Schakel de parameter **Voor alle boeken** in om alle boeken te bevestigen.

De informatie voor de nieuw bevestigde boeken wordt weergegeven op de pagina **Bevestigde boeken**. Nadat de betalingsschema's zijn bevestigd, kunnen de journaalposten voor eerste toerekening worden geboekt op basis van de leases.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]