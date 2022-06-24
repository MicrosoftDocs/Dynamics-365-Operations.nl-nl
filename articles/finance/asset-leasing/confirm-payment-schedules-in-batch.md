---
title: Betalingsschema's voor activaleases in batch bevestigen
description: In dit artikel wordt uitgelegd hoe u meerdere betalingsschema's in een batch kunt bevestigen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895046"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Betalingsschema's voor activaleases in batch bevestigen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u meerdere betalingsschema's in een batch kunt bevestigen. Betalingsschema's worden per lease bevestigd of met het bevestigingsbatchproces. Een journaalboeking kan alleen worden geboekt naar een lease met een bevestigd betalingsschema. De bevestiging van het betalingsschema dient als laatste goedkeuring van de financiële gegevens voor de lease. Alle toekomstige wijzigingen in de financiële informatie voor de lease, zoals betalingen en de leasetermijn, vormen een leasecorrectie en moeten op die manier worden verwerkt.

Voer de volgende stappen uit om meerdere betalingsschema's te bevestigen.

1. Ga naar **Activa leasen \> Periodiek \> Bevestigingsbatch**.
2. Selecteer **Bevestigingsbatch** op de pagina **Bevestigingsbatch**.
3. In het dialoogvenster dat wordt weergegeven, filtert u op de boeken die u wilt bevestigen.

    - Om alle boeken in een specifieke leasegroep te bevestigen, selecteert u de groep in het veld **Leasegroep**.
    - Als u specifieke boeken wilt bevestigen, selecteert u de boeken in het veld **Boek-id**.
    - Schakel de parameter **Voor alle boeken** in om alle boeken te bevestigen.

De informatie voor de nieuw bevestigde boeken wordt weergegeven op de pagina **Bevestigde boeken**. Nadat de betalingsschema's zijn bevestigd, kunnen de journaalposten voor eerste toerekening worden geboekt op basis van de leases.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
