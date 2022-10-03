---
title: Het overgeboekte budget bijwerken na kortingen in inkooporders en facturen
description: In dit artikel wordt beschreven hoe u kunt bepalen wat er gebeurt met het overgeboekte budget wanneer inkooporders worden geannuleerd of verlaagd en wanneer facturen worden verlaagd.
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: 790f1e770fd77d5209436c1c89e0f6125aac150f
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573041"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Het overgeboekte budget bijwerken na kortingen in inkooporders en facturen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel wordt beschreven hoe u kunt bepalen wat er gebeurt met het overgeboekte budget wanneer inkooporders worden geannuleerd of verlaagd en wanneer facturen worden verlaagd.

Zie [Inkooporders aan het einde van het jaar verwerken](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end) voor informatie over de manier waarop inkooporders aan het einde van het jaar worden verwerkt.

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Reducties in het overgeboekte budget voor factuurafwijkingen in- of uitschakelen

Het overgeboekte kan altijd worden bijgewerkt wanneer een inkooporder wordt geannuleerd of verlaagd. Als u het overgeboekte budget echter wilt bijwerken wanneer een factuur wordt verlaagd, moet u de functie *Overgeboekt budget reduceren wanneer een factuur voor een inkooporder wordt verminderd met een afwijking* inschakelen. Beheerders kunnen deze functie in- of uitschakelen door hiernaar te zoeken in de werkruimte **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Inkooporderreducties en -annuleringen

Het overgeboekte budget wordt bijgewerkt wanneer een kwalificerende inkooporder wordt geannuleerd of verlaagd, ongeacht of de functie *Overgeboekt budget reduceren wanneer een factuur voor een inkooporder wordt verminderd met een afwijking* is ingeschakeld. U kunt elk grootboekfonds op een van de volgende manieren laten reageren:

- Het overgeboekte budget behouden zoals het is gemaakt.
- Het overgeboekte budget automatisch aanpassen om het geannuleerde of verlaagde bedrag te verwijderen.

Alleen inkooporderregels met distributies die een fonds bevatten, zijn beschikbaar voor automatische budgetcorrectie. De automatische budgetcorrectie wordt uitgevoerd wanneer de inkooporder wordt afgerond of een inkooporderreductie wordt bevestigd.

## <a name="invoice-reductions"></a>Factuurreducties

Wanneer de functie *Overgeboekt budget reduceren wanneer een factuur voor een inkooporder wordt verminderd met een afwijking* is ingeschakeld, kunt u opgeven of elk fonds het overgeboekte budget moet verminderen wanneer een factuur wordt verlaagd of een inkooporder wordt verminderd of geannuleerd. De factuur moet bedoeld zijn voor een inkooporder met een overgeboekt budget. Reducties zijn onder andere prijsafwijkingen, toeslagafwijkingen en belastingafwijkingen. Wanneer een overgeboekte inkooporder wordt verminderd tijdens het factureren, wordt er een afwijking gemaakt. Wanneer de factuur wordt geboekt, wordt de inkoopordervordering verminderd met het bedrag van de afwijking. De functie maakt ook de automatische budgetcorrectie voor het bedrag van de afwijking.

Als *Overgeboekt budget reduceren wanneer een factuur voor een inkooporder wordt verminderd met een afwijking* is uitgeschakeld, wordt het overgeboekte budget niet verminderd in dit scenario. Daarom blijft het resterende overgeboekte voor het bedrag van de afwijking achter.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>De opties voor overgeboekt budget configureren voor elk fonds

Volg deze stappen voor elk grootboekfonds dat overgeboekt budget moet kunnen verminderen wanneer een inkooporder of factuur wordt verminderd.

1. Ga naar **Grootboek \> Rekeningschema \> Fondsen \> Fondsen**.
1. Selecteer het fonds dat u wilt instellen.
1. Zorg dat onder **Jaarultimo-proces inkooporder** de optie **Geselecteerde jaarafsluitingsoptie overschrijven** is ingesteld op *Ja*.
1. Stel onder **Status overgeboekt budget** het veld **Het budget opnieuw invoeren wanneer een getransporteerde inkooporder wordt geannuleerd of verlaagd** naar wens in. De instellingen kunnen enigszins verschillende effecten hebben, afhankelijk van of de functie *Overgeboekt budget reduceren wanneer een factuur voor een inkooporder wordt verminderd met een afwijking* in het systeem is ingeschakeld.

    - Wanneer de functie is uitgeschakeld, reageert het systeem alleen op geannuleerde of verlaagde inkooporders. De optie-instellingen werken als volgt:

        - *Nee*: het systeem maakt een budgetregisterpost voor het resterende saldo van inkooporders die zijn geannuleerd of verlaagd.
        - *Ja*: het systeem staat toe dat inkooporders worden geannuleerd of verlaagd, maar er wordt geen budgetregisterpost gemaakt. Het overgeboekte budget blijft beschikbaar voor verbruik door andere documenten.

    - Wanneer de functie is ingeschakeld, reageert het systeem zowel op factuurafwijkingen als op geannuleerde of verlaagde inkooporders. De optie-instellingen werken als volgt:

        - *Nee*: voor factuurafwijkingen wordt voor het bedrag van de afwijkingsreductie een budgetregisterpost gemaakt voor de inkooporder. Voor geannuleerde of gereduceerde inkooporders heeft deze instelling hetzelfde effect als wanneer de functie is uitgeschakeld.
        - *Ja*: voor factuurafwijkingen staat het systeem de factuurreductie toe, maar wordt er geen budgetregisterpost gemaakt. Het overgeboekte budget blijft beschikbaar voor verbruik door andere documenten. Voor geannuleerde of gereduceerde inkooporders heeft deze instelling hetzelfde effect als wanneer de functie is uitgeschakeld.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Inkooporders aan het einde van het jaar verwerken](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Algemene budgetreserveringen onderhouden](general-budget-reservation-tasks.md)
- [Fondsen in de openbare sector](funds-public-sector.md)
- [Een fonds instellen voor de openbare sector](tasks/set-up-fund-public-sector.md)
