---
title: Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd
description: Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd die de status Wordt gecontroleerd heeft.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026413"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="4b3b7-103">Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd</span><span class="sxs-lookup"><span data-stu-id="4b3b7-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="4b3b7-104">KB-nummer: 4612450</span><span class="sxs-lookup"><span data-stu-id="4b3b7-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="4b3b7-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="4b3b7-105">Symptoms</span></span>

<span data-ttu-id="4b3b7-106">Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd die de status *Wordt gecontroleerd* heeft.</span><span class="sxs-lookup"><span data-stu-id="4b3b7-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="4b3b7-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4b3b7-107">Resolution</span></span>

<span data-ttu-id="4b3b7-108">Wanneer wijzigingen bijhouden is ingeschakeld, wordt de status *Wordt gecontroleerd* toegewezen aan gefiatteerde afgeleide orders (uitbestede inkooporders).</span><span class="sxs-lookup"><span data-stu-id="4b3b7-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="4b3b7-109">Als een inkooporder wordt afgeleid (dan is het een uitbestede inkooporder), wordt deze dus alleen naar een werkstroom verzonden.</span><span class="sxs-lookup"><span data-stu-id="4b3b7-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="4b3b7-110">Als een inkooporder een gefiatteerde geplande inkooporder is, is deze automatisch goedgekeurd om ervoor te zorgen dat de planningsengine geen nieuwe geplande orders maakt terwijl de inkooporder nog steeds de status *Concept* heeft.</span><span class="sxs-lookup"><span data-stu-id="4b3b7-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
