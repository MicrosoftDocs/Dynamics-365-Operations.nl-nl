---
title: Fout 'Objectverwijzing niet ingesteld' treedt op tijdens inkooporderbevestiging
description: Fout 'Objectverwijzing niet ingesteld' treedt op tijdens inkooporderbevestiging
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
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476033"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>Fout 'Objectverwijzing niet ingesteld' treedt op tijdens inkooporderbevestiging

## <a name="symptoms"></a>Symptomen

U krijgt de volgende uitzondering bij het bevestigen van een inkooporder:

> Objectverwijzing niet ingesteld

## <a name="cause"></a>Oorzaak

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

## <a name="resolution"></a>Oplossing

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.
