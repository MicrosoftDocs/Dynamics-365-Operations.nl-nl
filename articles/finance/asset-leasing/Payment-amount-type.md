---
title: Typen betalingsbedragen toevoegen
description: In dit artikel wordt uitgelegd hoe u typen betalingsbedragen instelt in Activa leasen.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03fc903e6cfe78ef2fed7e3a0744a8f809f6892d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891604"
---
# <a name="add-payment-amount-types"></a>Typen betalingsbedragen toevoegen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u typen betalingsbedragen instelt in Activa leasen. Op deze manier kunt u het leasebetalingsbedrag specificeren in plaats van het totale bedrag ineens op de betalingsschemaregels op te geven.

Om typen betalingsbedragen toe te voegen, volgt u deze stappen.

1. Ga naar **Activa leasen \> Instellingen \> Typen betalingsbedragen**.
2. Selecteer **Nieuw**.
3. Voer het nieuwe betalingstype en een omschrijving in.

> [!NOTE]
> Voor herwaardering van IFRS 16-indexen moet u één betalingsbedragtype maken en dit markeren als **Gebruikt voor IRFS 16-indexherwaardering**. Dit type betalingsbedrag wordt gebruikt wanneer het indexherwaarderingsproces wordt uitgevoerd voor het IFRS 16-boek. Er wordt rekening mee gehouden dat er wijzigingen zijn doorgevoerd als gevolg van het indexherwaarderingsproces.
>
> Wanneer de optie **Betaling opsplitsen** in de lease wordt ingesteld op **Ja** als de indexherwaardering voor IFRS 16 wordt uitgevoerd maar er geen betalingstype voor IFRS 16 is, kan het proces niet worden voltooid.

Er kan slechts één record worden gemarkeerd als **Gebruikt voor IFRS 16-indexherwaardering**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
