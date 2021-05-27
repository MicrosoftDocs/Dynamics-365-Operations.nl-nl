---
title: Geplande inkooporder wordt gemaakt wanneer er binnen negatieve dagen een inkoop bestaat
description: Als de behoefteplanningscode Min/max is, wordt via Planningsoptimalisatie een geplande inkooporder gemaakt wanneer er binnen negatieve dagen een inkoop bestaat.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026411"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="9e867-103">Geplande inkooporder wordt gemaakt wanneer er binnen negatieve dagen een inkoop bestaat</span><span class="sxs-lookup"><span data-stu-id="9e867-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="9e867-104">KB-nummer: 4614298</span><span class="sxs-lookup"><span data-stu-id="9e867-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="9e867-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="9e867-105">Symptoms</span></span>

<span data-ttu-id="9e867-106">Als de behoefteplanningscode *Min/max* is, wordt via Planningsoptimalisatie een geplande inkooporder gemaakt wanneer er binnen negatieve dagen een inkoop bestaat.</span><span class="sxs-lookup"><span data-stu-id="9e867-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="9e867-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="9e867-107">Resolution</span></span>

<span data-ttu-id="9e867-108">Bij planningsoptimalisatie worden negatieve dagen niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="9e867-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="9e867-109">Het zorgt er echter altijd voor dat geplande orders niet worden gepland binnen de doorlooptijd ten opzichte van de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="9e867-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="9e867-110">De doorlooptijd van inkoop is bijvoorbeeld 10 dagen en de verwachting is dat een inkooporder acht dagen later dan vandaag binnenkomt.</span><span class="sxs-lookup"><span data-stu-id="9e867-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="9e867-111">In dit geval wordt de inkooporder gebruikt als vraagaanbod van vijf dagen vanaf vandaag.</span><span class="sxs-lookup"><span data-stu-id="9e867-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="9e867-112">Het wordt daarom aangeraden de doorlooptijden aan te passen voor alle (of bijna alle) scenario's.</span><span class="sxs-lookup"><span data-stu-id="9e867-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
