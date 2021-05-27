---
title: Later selecteren wordt niet in acht genomen wanneer productieorders via een batchtaak opnieuw worden ingesteld
description: Wanneer u een terugkerende batchtaak gebruikt om de status van een productieorder opnieuw in te stellen, worden latere selecties niet in acht genomen.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026399"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="78d52-103">Later selecteren wordt niet in acht genomen wanneer productieorders via een batchtaak opnieuw worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="78d52-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="78d52-104">KB-nummer: 4614634</span><span class="sxs-lookup"><span data-stu-id="78d52-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="78d52-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="78d52-105">Symptoms</span></span>

<span data-ttu-id="78d52-106">Wanneer u een terugkerende batchtaak gebruikt om de status van een productieorder opnieuw in te stellen, worden latere selecties niet in acht genomen.</span><span class="sxs-lookup"><span data-stu-id="78d52-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="78d52-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="78d52-107">Resolution</span></span>

<span data-ttu-id="78d52-108">Het huidige ontwerp biedt geen ondersteuning voor het gebruik van later selecteren voor het proces *Status opnieuw instellen*.</span><span class="sxs-lookup"><span data-stu-id="78d52-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
