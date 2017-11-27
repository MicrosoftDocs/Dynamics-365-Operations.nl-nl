---
title: Geplande orders onderhouden
description: Dit artikel bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8931908fbf643a8154da70d2ad065ea47d2aa4e6
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="e7c9f-104">Geplande orders onderhouden</span><span class="sxs-lookup"><span data-stu-id="e7c9f-104">Maintain planned orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e7c9f-105">Dit artikel bevat informatie over het beheer van geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="e7c9f-106">Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="e7c9f-107">U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="e7c9f-108">U kunt het veld **Status** gebruiken om uw voortgang bij te houden.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="e7c9f-109">De volgende waarden worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="e7c9f-109">The following values are used:</span></span>

-   <span data-ttu-id="e7c9f-110">Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status **Niet-verwerkt**.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="e7c9f-111">Wanneer u besluit een geplande order niet te fiatteren, kunt u die order de status **Voltooid** geven.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="e7c9f-112">Wanneer u besluit een geplande order te fiatteren, geeft u die order de status **Goedgekeurd**.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="e7c9f-113">Deze status geeft aan dat u ermee akkoord gaat dat de geplande order wordt gefiatteerd, maar de order is nog niet gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="e7c9f-114">**Opmerking:** Een goedgekeurde, geplande order wordt in de huidige status overgeboekt naar de volgende berekening in de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="e7c9f-115">U kunt geplande orders fiatteren door te klikken op **Fiatteren**.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="e7c9f-116">De volgende geplande orders kunnen worden gefiatteerd:</span><span class="sxs-lookup"><span data-stu-id="e7c9f-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="e7c9f-117">De geplande order die is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="e7c9f-118">Meerdere geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="e7c9f-119">Geplande orders die door een explosie vanaf de pagina **Explosie** zijn gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="e7c9f-120">Klik op **Geplande orders**, selecteer de geplande order en klik op **Fiatteren**.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="e7c9f-121">Wanneer een geplande order wordt gefiatteerd, wordt die order naar de ordersectie van de relevante module verplaatst.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="e7c9f-122">**Opmerking:** U kunt met de rechtermuisknop op een geplande order met een bepaalde status klikken en vervolgens op geplande orders met dezelfde status filteren.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="e7c9f-123">Dit is een handige functionaliteit die u kunt gebruiken wanneer u bijvoorbeeld alle geplande orders met de status **Goedgekeurd** wilt filteren zodat u ze kunt fiatteren.</span><span class="sxs-lookup"><span data-stu-id="e7c9f-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="e7c9f-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e7c9f-124">See also</span></span>
--------

[<span data-ttu-id="e7c9f-125">Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="e7c9f-125">Master plans</span></span>](master-plans.md)




