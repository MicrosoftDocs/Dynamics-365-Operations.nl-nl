---
title: Geannuleerde inkooporders worden weergegeven in de conceptlijst in het werkgebied
description: Geannuleerde inkooporders worden weergegeven in de conceptlijst in het werkgebied Voorbereiding van inkooporder
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476034"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Geannuleerde inkooporders worden weergegeven in de conceptlijst in het werkgebied

## <a name="symptoms"></a>Symptomen

Nadat u inkooporders hebt geannuleerd die de status *Bevestigd* hadden, worden de geannuleerde inkooporders nog steeds weergegeven in de lijst met conceptinkooporders in de werkruimte **Voorbereiding van inkooporder**.

## <a name="resolution"></a>Oplossing

Dit probleem doet zich alleen voor bij inkooporders waarvoor wijzigingsbeheer van toepassing is. Deze gebeurtenis treedt op omdat de annulering wordt beschouwd als een wijziging die moet worden goedgekeurd. De goedkeuring kan automatisch door het systeem worden uitgevoerd. Daarom moet de geannuleerde inkooporder worden ingediend bij de goedkeuringswerkstroom, zodat deze de status *Goedgekeurd* krijgt. Op dat moment wordt de inkooporder niet meer weergegeven in de lijst met conceptinkooporders in de werkruimte **Voorbereiding van inkooporder**.
