---
title: Fysiek ontvangen inkooporders worden niet weergegeven in het voorraadafsluitingsrapport
description: Fysiek ontvangen inkooporders worden niet weergegeven in het voorraadafsluitingsrapport Openstaande hoeveelheden controleren.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026405"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="73b89-103">Fysiek ontvangen inkooporders worden niet weergegeven in het voorraadafsluitingsrapport</span><span class="sxs-lookup"><span data-stu-id="73b89-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="73b89-104">KB-nummer: 4612595</span><span class="sxs-lookup"><span data-stu-id="73b89-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="73b89-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="73b89-105">Symptoms</span></span>

<span data-ttu-id="73b89-106">Fysiek ontvangen inkooporders worden niet weergegeven in het voorraadafsluitingsrapport **Openstaande hoeveelheden controleren**.</span><span class="sxs-lookup"><span data-stu-id="73b89-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="73b89-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="73b89-107">Resolution</span></span>

<span data-ttu-id="73b89-108">Het rapport **Openstaande hoeveelheden controleren** geeft uitgiftetransacties weer die niet kunnen worden vereffend met financieel bijgewerkte voorraadontvangstbonnen vanaf de geselecteerde afsluitdatum.</span><span class="sxs-lookup"><span data-stu-id="73b89-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="73b89-109">U kunt fysieke ontvangstbewijzen opnemen in het rapport.</span><span class="sxs-lookup"><span data-stu-id="73b89-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="73b89-110">In dat geval worden fysieke ontvangstbewijzen weergegeven als ze de uitgiftetransacties kunnen dekken die niet kunnen worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="73b89-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="73b89-111">Zie voor meer informatie [Het uitvoeren van de voorraadafsluiting voorbereiden](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="73b89-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
