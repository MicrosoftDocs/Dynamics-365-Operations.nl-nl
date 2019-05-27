---
title: Serviceorderfasen
description: Door de fasen voor een serviceorder te definiëren en deze aan werknemers toe te wijzen, controleert u de stroom van een serviceorder met de verschillende taken die mensen in de serviceorganisatie uitvoeren.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b924be95c7e60598879e4d0cfd03193fe888dd7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569700"
---
# <a name="service-order-stages"></a><span data-ttu-id="af541-103">Serviceorderfasen</span><span class="sxs-lookup"><span data-stu-id="af541-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="af541-104">U kunt fasen instellen voor een serviceorder om de taken die moeten worden voltooid, de volgorde waarin ze zijn afgerond, en de werknemers die van de voltooiing van deze verantwoordelijk is te definiëren.</span><span class="sxs-lookup"><span data-stu-id="af541-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="af541-105">Door de fasen voor een serviceorder te definiëren en deze aan werknemers toe te wijzen, kunt u de stroom controleren van een serviceorder met de verschillende taken die mensen in de serviceorganisatie uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="af541-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="af541-106">De volgorde van fasen moet een eerste fase opnemen.</span><span class="sxs-lookup"><span data-stu-id="af541-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="af541-107">U kunt ook definiëren de acties die zijn toegestaan in elke fase.</span><span class="sxs-lookup"><span data-stu-id="af541-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="af541-108">Als u bijvoorbeeld het selectievakje **Boeken** voor alle fasen behalve de laatste uitschakelt, kunnen serviceorders pas worden geboekt als deze de volledige fasereeks hebben doorlopen.</span><span class="sxs-lookup"><span data-stu-id="af541-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="af541-109">De vertakking in serviceorderfasen</span><span class="sxs-lookup"><span data-stu-id="af541-109">Branching in service order stages</span></span>

<span data-ttu-id="af541-110">Wanneer u een servicefase instelt, u meerdere opties, of vertakkingen maken, om uit te selecteren voor de volgende servicefase.</span><span class="sxs-lookup"><span data-stu-id="af541-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="af541-111">Alle vertakkingen die u maakt zijn beschikbaar om uit te kiezen wanneer de eerste fase is voltooid.</span><span class="sxs-lookup"><span data-stu-id="af541-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="af541-112">Bijvoorbeeld, stelt u **Planning** als eerste fase.</span><span class="sxs-lookup"><span data-stu-id="af541-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="af541-113">U maakt twee fasen genaamd **Onderhanden** en **Annuleren**, en selecteer vervolgens **Planning** als deze bovenliggende voor.</span><span class="sxs-lookup"><span data-stu-id="af541-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="af541-114">U kunt de fase **Planning** aan verkooporder toewijzen.</span><span class="sxs-lookup"><span data-stu-id="af541-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="af541-115">Wanneer de planningsfase voor de verkooporder is voltooid, kunt u de fase **Onderhanden** selecteren als de verkooporder gereed is om te werken, of u kunt de fase **Annuleren** selecteren als de verkooporder wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="af541-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="af541-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="af541-116">See also</span></span>

[<span data-ttu-id="af541-117">Serviceorderfasen instellen</span><span class="sxs-lookup"><span data-stu-id="af541-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="af541-118">De fase van de serviceorder wijzigen</span><span class="sxs-lookup"><span data-stu-id="af541-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


