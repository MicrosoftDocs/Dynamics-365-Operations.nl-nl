---
title: Parameters instellen om een intercompany-order te boeken
description: In dit artikel wordt uitgelegd hoe u parameters instelt om een intercompany-order te boeken
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 97ea0061d57beede6350eecfd497c12dd37aea31
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900791"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Parameters instellen om een intercompany-order te boeken

[!include [banner](../../includes/banner.md)]

Wanneer er een intercompany-klantfactuur wordt geboekt, kunt u deze zo instellen dat de intercompany-inkooporder en de oorspronkelijke klantfactuur automatisch worden geboekt.

> [!NOTE]
> Stel, voordat u deze procedure uitvoert, het afdrukbeheer in uw organisatie in op de juiste factuurprinter. Zo zorgt u ervoor dat de factuur voor de oorspronkelijke verkooporder op de juiste printer wordt afgedrukt.

U moet de volgende parameters instellen:

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**. Selecteer de verkooporder waarmee u wilt werken.
1. Selecteer in de verkooporder in het actievenster de optie **Kopweergave** en selecteer vervolgens het sneltabblad **Intercompany-instellingen** en open deze.
1. Ga naar het actievenster op het tabblad **Verkooporder** en selecteer **Bewerken**.
1. Ga terug naar het sneltabblad **Intercompany-instellingen** en selecteer **Rechtstreekse levering** om rechtstreekse levering in de intercompany-keten (alle orders) in te schakelen.
1. Selecteer **Opslaan** om de verkooporder met de nieuwe instelling op te slaan. Selecteer vervolgens **Sluiten** om de verkooporder te sluiten.
1. Ga naar **Inkoop en sourcing \> Leveranciers \> Alle leveranciers**. Selecteer op het tabblad **Algemeen** de optie **Intercompany**.
1. Selecteer op de pagina **Intercompany** de koppeling **Inkooporderbeleid**. Selecteer in de veldgroep **Intercompany-inkooporder (rechtstreekse levering)** de optie **Factuur automatisch boeken** en schakel het selectievakje **Factuur automatisch afdrukken** uit.
1. Selecteer in de veldgroep **Oorspronkelijke inkooporder (rechtstreekse levering)** het veld **Factuur automatisch boeken** en het veld **Factuur automatisch afdrukken**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
