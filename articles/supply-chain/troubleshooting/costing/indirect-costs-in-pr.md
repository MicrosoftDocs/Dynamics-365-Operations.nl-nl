---
title: Het rapport Indirecte kosten in verwerking bevat verwijderde productieorders
description: Het rapport Indirecte kosten in verwerking bevat informatie over productieorders die gedeeltelijk zijn verwerkt en later zijn verwijderd.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751764"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Het rapport Indirecte kosten in verwerking bevat verwijderde productieorders

KB-nummer: 4612748

## <a name="symptoms"></a>Symptomen

Het rapport **Indirecte kosten in verwerking** bevat informatie over productieorders die gedeeltelijk zijn verwerkt en later zijn verwijderd.

## <a name="resolution"></a>Oplossing

Wanneer u een productieorder omkeert, worden ook alle transacties van die productieorder omgekeerd. Wanneer u de productieorder verwijdert, behouden de subgrootboektabellen en het grootboek alle transacties die daaraan zijn gerelateerd. In de rapporten zijn de transacties in de subgrootboektabellen te zien. Voor de specifieke productieorder moet de nettowaarde 0,00 zijn.
