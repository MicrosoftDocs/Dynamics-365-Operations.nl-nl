---
title: Parameters voor het hoofdplan bestaan niet
description: Wanneer u een geplande order probeert te fiatteren, ontvangt u een foutbericht dat er geen parameters voor het hoofdplan bestaan.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294049"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="341d9-103">Parameters voor het hoofdplan bestaan niet</span><span class="sxs-lookup"><span data-stu-id="341d9-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="341d9-104">Foutcode: SYS25368</span><span class="sxs-lookup"><span data-stu-id="341d9-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="341d9-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="341d9-105">Symptoms</span></span>

<span data-ttu-id="341d9-106">Wanneer u een geplande order probeert te fiatteren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="341d9-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="341d9-107">Parameters voor hoofdplan %1 bestaan niet.</span><span class="sxs-lookup"><span data-stu-id="341d9-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="341d9-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="341d9-108">Cause</span></span>

<span data-ttu-id="341d9-109">Vanwege configuratieproblemen kan het systeem de instellingen voor het opgegeven plan niet vinden.</span><span class="sxs-lookup"><span data-stu-id="341d9-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="341d9-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="341d9-110">Resolution</span></span>

- <span data-ttu-id="341d9-111">Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen** en zorg ervoor dat er een plan met de opgegeven naam bestaat.</span><span class="sxs-lookup"><span data-stu-id="341d9-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
