---
title: Fout bij het opnieuw aan een werkstroom toevoegen van een inkooporder na een wijziging
description: Fout bij het opnieuw aan een werkstroom toevoegen van een inkooporder na een wijziging
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476059"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Fout bij het opnieuw aan een werkstroom toevoegen van een inkooporder na een wijziging


## <a name="symptoms"></a>Symptomen

De volgende fout treedt op in de werkstroom wanneer een inkooporder opnieuw wordt ingediend na een wijziging:

> Gestopt (fout): X++-uitzondering: wijzigingen in inkooporder PO0000569 zijn alleen toegestaan in de status Concept wanneer wijzigingsbeheer is geactiveerd op<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Dit probleem treedt alleen op als de inkooporder de status *Bevestigd* heeft op het moment dat u wijzigingen aanvraagt. Als u wijzigingen aanvraagt terwijl de inkooporder de status *Goedgekeurd* heeft, kan de werkstroom gewoon worden verwerkt.

## <a name="resolution"></a>Oplossing

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

Het probleem wordt opgelost via [dit Microsoft Knowledge Base-artikel (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
