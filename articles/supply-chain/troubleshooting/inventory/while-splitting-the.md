---
title: Wanneer een hoeveelheid variabel gewicht wordt opgesplitst, wordt de minimumhoeveelheid gebruikt in plaats van de nominale hoeveelheid
description: Wanneer een catch weight hoeveelheid wordt opgesplitst in batches, gebruikt het veld Verzamelhoeveelheid de minimumhoeveelheid die is ingesteld voor het artikel, en niet de nominale hoeveelheid.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026414"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="7dfb6-103">Wanneer een hoeveelheid variabel gewicht wordt opgesplitst, wordt de minimumhoeveelheid gebruikt in plaats van de nominale hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7dfb6-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="7dfb6-104">KB-nummer: 4612073</span><span class="sxs-lookup"><span data-stu-id="7dfb6-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="7dfb6-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="7dfb6-105">Symptoms</span></span>

<span data-ttu-id="7dfb6-106">Wanneer een catch weight hoeveelheid wordt opgesplitst in batches, gebruikt het veld **Verzamelhoeveelheid** de minimumhoeveelheid die is ingesteld voor het artikel, en niet de nominale hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="7dfb6-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7dfb6-107">Resolution</span></span>

<span data-ttu-id="7dfb6-108">Dit gedrag van het systeem is inherent aan het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-108">The system is behaving as designed.</span></span> <span data-ttu-id="7dfb6-109">De minimumhoeveelheid-instellingen van elk artikel worden gebruikt voor order verzamelen.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-109">The system uses each item's minimum quantity setup for picking.</span></span>
