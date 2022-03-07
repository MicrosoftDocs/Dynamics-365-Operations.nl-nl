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
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026406"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Het rapport Indirecte kosten in verwerking bevat verwijderde productieorders

KB-nummer: 4612748

## <a name="symptoms"></a>Symptomen

Het rapport **Indirecte kosten in verwerking** bevat informatie over productieorders die gedeeltelijk zijn verwerkt en later zijn verwijderd.

## <a name="resolution"></a>Oplossing

Wanneer u een productieorder omkeert, worden ook alle transacties van die productieorder omgekeerd. Wanneer u de productieorder verwijdert, behouden de subgrootboektabellen en het grootboek alle transacties die daaraan zijn gerelateerd. In de rapporten zijn de transacties in de subgrootboektabellen te zien. Voor de specifieke productieorder moet de nettowaarde 0,00 zijn.
