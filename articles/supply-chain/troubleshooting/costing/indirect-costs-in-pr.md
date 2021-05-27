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
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="369e5-103">Het rapport Indirecte kosten in verwerking bevat verwijderde productieorders</span><span class="sxs-lookup"><span data-stu-id="369e5-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="369e5-104">KB-nummer: 4612748</span><span class="sxs-lookup"><span data-stu-id="369e5-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="369e5-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="369e5-105">Symptoms</span></span>

<span data-ttu-id="369e5-106">Het rapport **Indirecte kosten in verwerking** bevat informatie over productieorders die gedeeltelijk zijn verwerkt en later zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="369e5-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="369e5-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="369e5-107">Resolution</span></span>

<span data-ttu-id="369e5-108">Wanneer u een productieorder omkeert, worden ook alle transacties van die productieorder omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="369e5-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="369e5-109">Wanneer u de productieorder verwijdert, behouden de subgrootboektabellen en het grootboek alle transacties die daaraan zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="369e5-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="369e5-110">In de rapporten zijn de transacties in de subgrootboektabellen te zien.</span><span class="sxs-lookup"><span data-stu-id="369e5-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="369e5-111">Voor de specifieke productieorder moet de nettowaarde 0,00 zijn.</span><span class="sxs-lookup"><span data-stu-id="369e5-111">For the specific production order, the net value should be 0.00.</span></span>
