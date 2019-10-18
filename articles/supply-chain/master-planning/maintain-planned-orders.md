---
title: Geplande orders onderhouden
description: Dit onderwerp bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993435"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="a6a41-104">Geplande orders onderhouden</span><span class="sxs-lookup"><span data-stu-id="a6a41-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6a41-105">Dit onderwerp bevat informatie over het beheer van geplande orders.</span><span class="sxs-lookup"><span data-stu-id="a6a41-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="a6a41-106">Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.</span><span class="sxs-lookup"><span data-stu-id="a6a41-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="a6a41-107">U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren.</span><span class="sxs-lookup"><span data-stu-id="a6a41-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="a6a41-108">Status van geplande order</span><span class="sxs-lookup"><span data-stu-id="a6a41-108">Planned order status</span></span>
<span data-ttu-id="a6a41-109">U kunt het veld **Status** gebruiken om uw voortgang bij te houden.</span><span class="sxs-lookup"><span data-stu-id="a6a41-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="a6a41-110">De volgende waarden worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="a6a41-110">The following values are used:</span></span>

-   <span data-ttu-id="a6a41-111">Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status **Niet-verwerkt**.</span><span class="sxs-lookup"><span data-stu-id="a6a41-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="a6a41-112">Wanneer u besluit een geplande order niet te fiatteren, kunt u die order de status **Voltooid** geven.</span><span class="sxs-lookup"><span data-stu-id="a6a41-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="a6a41-113">Als u een geplande order wilt fiatteren, kunt u de status wijzigen in **Goedgekeurd**.</span><span class="sxs-lookup"><span data-stu-id="a6a41-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="a6a41-114">Geplande orders met de status **Goedgekeurd** worden geëerbiedigd door de hoofdplanning. Ze worden dus niet gewijzigd of verwijderd.</span><span class="sxs-lookup"><span data-stu-id="a6a41-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="a6a41-115">Geplande orders fiatteren</span><span class="sxs-lookup"><span data-stu-id="a6a41-115">Firming planned orders</span></span> 
<span data-ttu-id="a6a41-116">Door geplande orders te fiatteren, worden echte orders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a6a41-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="a6a41-117">Dit worden ook wel *vrijgegeven* of *openstaande orders* genoemd.</span><span class="sxs-lookup"><span data-stu-id="a6a41-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="a6a41-118">Wanneer een geplande order wordt gefiatteerd, wordt die order naar de ordersectie van de relevante module verplaatst.</span><span class="sxs-lookup"><span data-stu-id="a6a41-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="a6a41-119">Op de pagina **Geplande orders** kunt u twee opties voor fiatteren selecteren:</span><span class="sxs-lookup"><span data-stu-id="a6a41-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="a6a41-120">**Fiatteren**: hiermee kunt u een of meer geselecteerde geplande orders fiatteren.</span><span class="sxs-lookup"><span data-stu-id="a6a41-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="a6a41-121">**Alles fiatteren**: hiermee kunt u alle geplande orders in het filter fiatteren.</span><span class="sxs-lookup"><span data-stu-id="a6a41-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="a6a41-122">Als u **Alles fiatteren** gebruikt, hoeft u de geplande order niet te selecteren. Alle geplande orders in het filter worden gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="a6a41-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="a6a41-123">Deze optie kan handig zijn als u een groot aantal geplande orders wilt fiatteren.</span><span class="sxs-lookup"><span data-stu-id="a6a41-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="a6a41-124">U kunt een gefiatteerde geplande order volgen via **Fiatteringshistorie** onder **formulier Geplande orders > Weergeven > Fiatteringshistorie**.</span><span class="sxs-lookup"><span data-stu-id="a6a41-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="a6a41-125">Fiattering parallel uitvoeren</span><span class="sxs-lookup"><span data-stu-id="a6a41-125">Parallelize firming</span></span>
<span data-ttu-id="a6a41-126">Als u meerdere orders tegelijk wilt fiatteren, kunt u de uitvoeringstijd of prestaties verbeteren door de uitvoering parallel te laten verlopen.</span><span class="sxs-lookup"><span data-stu-id="a6a41-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="a6a41-127">Deze optie is beschikbaar wanneer u meerdere geplande orders fiatteert met **Fiatteren** of **Alles fiatteren**.</span><span class="sxs-lookup"><span data-stu-id="a6a41-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="a6a41-128">De volgende parameters zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="a6a41-128">The following parameters are available:</span></span>

-   <span data-ttu-id="a6a41-129">**Parallel fiatteren**: als **Ja** is ingesteld, wordt het fiatteringsproces uitgevoerd parallel met het aantal threads dat is gedefinieerd in **Aantal threads**.</span><span class="sxs-lookup"><span data-stu-id="a6a41-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="a6a41-130">**Aantal threads** : hiermee bepaalt u het aantal threads waarmee het fiatterinigsproces parallel moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a6a41-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="a6a41-131">De parameter wordt alleen weergegeven als **Parallel fiatteren** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6a41-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="a6a41-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a6a41-132">Additional resources</span></span>
--------

[<span data-ttu-id="a6a41-133">Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="a6a41-133">Master plans</span></span>](master-plans.md)



