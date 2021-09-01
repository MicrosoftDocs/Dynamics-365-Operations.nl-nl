---
title: Problemen met werkstromen voor inkoopbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met werkstromen voor inkoopbeheer.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cda9da1a084bf3c04aef6911516ebee0facf1be61e94bfc1abab95e9dee75475
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729454"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Problemen met werkstromen voor inkoopbeheer oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met werkstromen voor inkoopbeheer.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Fout bij het opnieuw indienen van een inkooporder bij de werkstroom na een wijziging: "Wijzigingen in inkooporder X zijn alleen toegestaan in een conceptstatus als wijzigingsbeheer is geactiveerd"

Dit probleem treedt alleen op als de inkooporder de status *Bevestigd* heeft op het moment dat u wijzigingen aanvraagt. Als u wijzigingen aanvraagt terwijl de inkooporder de status *Goedgekeurd* heeft, kan de werkstroom gewoon worden verwerkt.

### <a name="error-description"></a>Foutomschrijving

De volgende fout treedt op in de werkstroom wanneer een inkooporder opnieuw wordt ingediend na een wijziging:

> Gestopt (fout): X++-uitzondering: wijzigingen in inkooporder PO0000569 zijn alleen toegestaan in de status Concept wanneer wijzigingsbeheer is geactiveerd op<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

Het probleem wordt opgelost via [dit Microsoft Knowledge Base-artikel (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Een of meer boekhoudingsverdelingen is te veel of te weinig verdeeld.

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Als een restant van een levering wordt geannuleerd op een inkooporder waarvoor wijzigingsbeheer is ingeschakeld, krijgt de inkooporder weer de status Bevestigd.

### <a name="issue-description"></a>Probleembeschrijving

Als een inkooporder is onderworpen aan wijzigingsbeheer en de enige wijziging die wordt aangevraagd, de annulering van een leveringsrestant op een of meer van de regels is, krijgt de inkooporder weer direct de status *Bevestigd* bevestigd wanneer deze wordt goedgekeurd en wordt er geen journaal gemaakt.

### <a name="issue-resolution"></a>Probleemoplossing

Annulering van een restant van de levering heeft geen invloed op de inhoud van het bevestigingsjournaal. Deze functionaliteit moet worden gebruikt wanneer de regel gedeeltelijk is ontvangen en de resterende kwaliteit in de processtap moet worden geannuleerd nadat de inkooporder met de leverancier is bevestigd.

Als dit op de bevestiging van de inkoopordermoet worden weergegeven, moet de hoeveelheid op de inkooporderregel zo worden gecorrigeerd dat de bevestiging is vereist. Als er niets op de regel is ontvangen, kan de hoeveelheid worden verwijderd. In dit geval is herbevestiging vereist.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Geannuleerde inkooporders worden weergegeven in de conceptlijst in de werkruimte Voorbereiding van inkooporder.

### <a name="issue-description"></a>Probleembeschrijving

Nadat u inkooporders hebt geannuleerd die de status *Bevestigd* hadden, worden de geannuleerde inkooporders nog steeds weergegeven in de lijst met conceptinkooporders in de werkruimte **Voorbereiding van inkooporder**.

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem doet zich alleen voor bij inkooporders waarvoor wijzigingsbeheer van toepassing is. Deze gebeurtenis treedt op omdat de annulering wordt beschouwd als een wijziging die moet worden goedgekeurd. De goedkeuring kan automatisch door het systeem worden uitgevoerd. Daarom moet de geannuleerde inkooporder worden ingediend bij de goedkeuringswerkstroom, zodat deze de status *Goedgekeurd* krijgt. Op dat moment wordt de inkooporder niet meer weergegeven in de lijst met conceptinkooporders in de werkruimte **Voorbereiding van inkooporder**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]