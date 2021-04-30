---
title: Maandelijkse journaalposten maken in een batch
description: In dit onderwerp wordt uitgelegd hoe u journaalposten in een batch maakt om de efficiëntie te verhogen wanneer de maandelijkse leasekosten worden vastgelegd.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881199"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Maandelijkse journaalposten maken in een batch

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u journaalposten in een batch maakt om de efficiëntie te verhogen wanneer de maandelijkse leasekosten worden vastgelegd. Batchverwerking kan worden gebruikt om journaalposten te maken op basis van meerdere schema's. Deze journaalposten kunnen bijvoorbeeld leasebetalingen, afschrijvingen van verplichtingen, afschrijving van RoU-activa en administratieve kosten bevatten. U kunt ook batchverwerking gebruiken om de eerste toerekening van meerdere leases tegelijk uit te voeren of om tegelijkertijd overgangscorrecties voor meerdere leases te maken.

Als u een batchtaak wilt instellen of betalingsfacturen, afschrijving of rente voor meerdere leases wilt verwerken, gaat u naar **Activa leasen \> Periodiek \> Batchjournaal maken**. In het dialoogvenster dat wordt weergegeven, kunt u de planning selecteren waaruit de journaalposten moeten worden gemaakt. U kunt ook opgeven of het batchproces moet worden uitgevoerd voor specifieke entiteiten, leasegroepen of leaseboeken.

> [!NOTE]
> Latere transacties, zoals het afschrijvingsschema verplichtingen, betalingen, afschrijving en onkosten, worden pas geboekt nadat de eerste toerekening voor bijbehorende leases is geboekt.
>
> De journaalposten worden gemaakt, maar ze worden pas geboekt wanneer u de opdracht **Uitvoeren** selecteert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
