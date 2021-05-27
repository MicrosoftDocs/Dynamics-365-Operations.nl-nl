---
title: Hoeveelheid op een gestarte quarantaineorder is niet bijgewerkt wanneer de order wordt gesplitst
description: Wanneer u een quarantaineorder maakt en probeert deze te splitsen, wordt de orderhoeveelheid niet bijgewerkt naar de gesplitste resterende hoeveelheid.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026418"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="3e7c7-103">Hoeveelheid op een gestarte quarantaineorder is niet bijgewerkt wanneer de order wordt gesplitst</span><span class="sxs-lookup"><span data-stu-id="3e7c7-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="3e7c7-104">KB-nummer: 4613113</span><span class="sxs-lookup"><span data-stu-id="3e7c7-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="3e7c7-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="3e7c7-105">Symptoms</span></span>

<span data-ttu-id="3e7c7-106">Wanneer u een quarantaineorder maakt en probeert deze te splitsen, wordt de orderhoeveelheid niet bijgewerkt naar de resterende hoeveelheid na het splitsen.</span><span class="sxs-lookup"><span data-stu-id="3e7c7-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="3e7c7-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="3e7c7-107">Resolution</span></span>

<span data-ttu-id="3e7c7-108">De oorspronkelijke hoeveelheid van een quarantaineorder wordt niet gewijzigd om ervoor te zorgen dat u de oorspronkelijke hoeveelheid die voor die quarantaineorder is gemaakt, kunt bijhouden.</span><span class="sxs-lookup"><span data-stu-id="3e7c7-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="3e7c7-109">De hoeveelheid die is opgesplitst van een quarantaineorder, wordt echter wel bij gehouden.</span><span class="sxs-lookup"><span data-stu-id="3e7c7-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="3e7c7-110">Voor deze tracering wordt een databaseveld met de naam `QuantityThatHasSplitIntoOtherQuarantineOrders` gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3e7c7-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="3e7c7-111">Dit veld is echter niet zichtbaar in de gebruikersinterface (UI).</span><span class="sxs-lookup"><span data-stu-id="3e7c7-111">However, this field isn't visible in the user interface (UI).</span></span>
