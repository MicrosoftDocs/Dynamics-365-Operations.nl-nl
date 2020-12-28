---
title: Geplande orders onderhouden
description: Dit onderwerp bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f62381ca212e711fd61e12c9ec8f066ec124a933
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425683"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="9afb2-104">Geplande orders onderhouden</span><span class="sxs-lookup"><span data-stu-id="9afb2-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9afb2-105">Dit onderwerp bevat informatie over het beheer van geplande orders.</span><span class="sxs-lookup"><span data-stu-id="9afb2-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="9afb2-106">Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.</span><span class="sxs-lookup"><span data-stu-id="9afb2-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="9afb2-107">U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren.</span><span class="sxs-lookup"><span data-stu-id="9afb2-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="9afb2-108">Status van geplande order</span><span class="sxs-lookup"><span data-stu-id="9afb2-108">Planned order status</span></span>
<span data-ttu-id="9afb2-109">U kunt het veld **Status** gebruiken om uw voortgang bij te houden.</span><span class="sxs-lookup"><span data-stu-id="9afb2-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="9afb2-110">De volgende waarden worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="9afb2-110">The following values are used:</span></span>

-   <span data-ttu-id="9afb2-111">Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status **Niet-verwerkt**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="9afb2-112">Wanneer u besluit een geplande order niet te fiatteren, kunt u die order de status **Voltooid** geven.</span><span class="sxs-lookup"><span data-stu-id="9afb2-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="9afb2-113">Als u een geplande order wilt fiatteren, kunt u de status wijzigen in **Goedgekeurd**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="9afb2-114">Geplande orders met de status **Goedgekeurd** worden geëerbiedigd door de hoofdplanning. Ze worden dus niet gewijzigd of verwijderd tijdens een latere hoofdplanningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="9afb2-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="9afb2-115">Om dit te bereiken, kopieert de planningslogica de **goedgekeurde** geplande orders van de oude planversie naar de nieuwe planversie tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="9afb2-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="9afb2-116">Geplande orders fiatteren</span><span class="sxs-lookup"><span data-stu-id="9afb2-116">Firming planned orders</span></span> 
<span data-ttu-id="9afb2-117">Door geplande orders te fiatteren, worden echte orders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9afb2-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="9afb2-118">Dit worden ook wel *vrijgegeven* of *openstaande orders* genoemd.</span><span class="sxs-lookup"><span data-stu-id="9afb2-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="9afb2-119">Wanneer een geplande order wordt gefiatteerd, wordt die order naar de ordersectie van de relevante module verplaatst.</span><span class="sxs-lookup"><span data-stu-id="9afb2-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="9afb2-120">Op de pagina **Geplande orders** kunt u twee opties voor fiatteren selecteren:</span><span class="sxs-lookup"><span data-stu-id="9afb2-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="9afb2-121">**Fiatteren**: hiermee kunt u een of meer geselecteerde geplande orders fiatteren.</span><span class="sxs-lookup"><span data-stu-id="9afb2-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="9afb2-122">**Alles fiatteren**: hiermee kunt u alle geplande orders in het filter fiatteren.</span><span class="sxs-lookup"><span data-stu-id="9afb2-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="9afb2-123">Als u **Alles fiatteren** gebruikt, hoeft u de geplande order niet te selecteren. Alle geplande orders in het filter worden gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="9afb2-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="9afb2-124">Deze optie kan handig zijn als u een groot aantal geplande orders wilt fiatteren.</span><span class="sxs-lookup"><span data-stu-id="9afb2-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="9afb2-125">U kunt een gefiatteerde geplande order volgen via **Fiatteringshistorie** onder **formulier Geplande orders > Weergeven > Fiatteringshistorie**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="9afb2-126">Fiattering parallel uitvoeren</span><span class="sxs-lookup"><span data-stu-id="9afb2-126">Parallelize firming</span></span>
<span data-ttu-id="9afb2-127">Als u meerdere orders tegelijk wilt fiatteren, kunt u de uitvoeringstijd of prestaties verbeteren door de uitvoering parallel te laten verlopen.</span><span class="sxs-lookup"><span data-stu-id="9afb2-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="9afb2-128">Deze optie is beschikbaar wanneer u meerdere geplande orders fiatteert met **Fiatteren** of **Alles fiatteren**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="9afb2-129">De volgende parameters zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="9afb2-129">The following parameters are available:</span></span>

-   <span data-ttu-id="9afb2-130">**Parallel fiatteren**: als **Ja** is ingesteld, wordt het fiatteringsproces uitgevoerd parallel met het aantal threads dat is gedefinieerd in **Aantal threads**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="9afb2-131">**Aantal threads** : hiermee bepaalt u het aantal threads waarmee het fiatterinigsproces parallel moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9afb2-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="9afb2-132">De parameter wordt alleen weergegeven als **Parallel fiatteren** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="9afb2-133">De optie voor **Parallel fiatteren** wordt alleen weergegeven wanneer er meer dan één geplande order is geselecteerd voor fiattering.</span><span class="sxs-lookup"><span data-stu-id="9afb2-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9afb2-134">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9afb2-134">Additional resources</span></span>
--------

[<span data-ttu-id="9afb2-135">Overzicht van Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="9afb2-135">Master plans overview</span></span>](master-plans.md)



