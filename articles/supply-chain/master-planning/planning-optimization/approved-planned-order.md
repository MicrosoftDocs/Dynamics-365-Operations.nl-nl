---
title: Geplande orders weergeven, beheren en goedkeuren
description: Dit onderwerp bevat informatie over het weergeven, beheren en goedkeuren van geplande orders in Planningsoptimalisatie.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304362"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="e73d2-103">Geplande orders weergeven, beheren en goedkeuren</span><span class="sxs-lookup"><span data-stu-id="e73d2-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e73d2-104">Dit onderwerp bevat informatie over het weergeven, beheren en goedkeuren van geplande orders in Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="e73d2-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="e73d2-105">Geplande orders weergeven en beheren</span><span class="sxs-lookup"><span data-stu-id="e73d2-105">View and manage planned orders</span></span>

<span data-ttu-id="e73d2-106">U kunt geplande orders weergeven en beheren op elke lijstpagina met geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e73d2-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="e73d2-107">Ga naar een van de volgende locaties, afhankelijk van het type geplande orders waarmee u wilt werken:</span><span class="sxs-lookup"><span data-stu-id="e73d2-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="e73d2-108">Hoofdplanning \> Werkgebieden \> Hoofdplanning</span><span class="sxs-lookup"><span data-stu-id="e73d2-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="e73d2-109">Hoofdplanning \> Hoofdplanning \> Geplande orders</span><span class="sxs-lookup"><span data-stu-id="e73d2-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="e73d2-110">Productiebeheer \> Productieorders \> Geplande productieorders</span><span class="sxs-lookup"><span data-stu-id="e73d2-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="e73d2-111">Inkoop en sourcing \> Inkooporders \> Geplande inkooporders</span><span class="sxs-lookup"><span data-stu-id="e73d2-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="e73d2-112">Voorraadbeheer \> Inkomende orders \> Geplande overboekingen</span><span class="sxs-lookup"><span data-stu-id="e73d2-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="e73d2-113">Voorraadbeheer \> Uitgaande orders \> Geplande overboekingen</span><span class="sxs-lookup"><span data-stu-id="e73d2-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="e73d2-114">De status van geplande orders weergeven bewerken</span><span class="sxs-lookup"><span data-stu-id="e73d2-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="e73d2-115">Met het veld **Status** van elke geplande order kunt u de voortgang bijhouden of wijzigen hoe een geplande order wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e73d2-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="e73d2-116">De volgende **Status**-waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="e73d2-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="e73d2-117">**Niet-verwerkt**: Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben zij deze status.</span><span class="sxs-lookup"><span data-stu-id="e73d2-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="e73d2-118">Geplande orders met deze status worden verwijderd tijdens de volgende planningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="e73d2-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="e73d2-119">**Voltooid**: Deze status geeft aan dat de geplande order is voltooid.</span><span class="sxs-lookup"><span data-stu-id="e73d2-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="e73d2-120">Wanneer u besluit een geplande order niet te fiatteren, kunt u handmatig de status wijzigen in *Voltooid*.</span><span class="sxs-lookup"><span data-stu-id="e73d2-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="e73d2-121">Merk op dat de statussen *Niet-verwerkt* en *Voltooid* op dezelfde manier worden behandeld in het systeem.</span><span class="sxs-lookup"><span data-stu-id="e73d2-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="e73d2-122">**Goedgekeurd**: Deze status geeft aan dat de geplande order is goedgekeurd voor fiattering.</span><span class="sxs-lookup"><span data-stu-id="e73d2-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="e73d2-123">Als u een geplande order wilt fiatteren, kunt u de status ervan wijzigen in *Goedgekeurd*.</span><span class="sxs-lookup"><span data-stu-id="e73d2-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="e73d2-124">Als u de bewerkingen wilt behouden die zijn gemaakt in een geplande order, of als u een geplande order wilt goedkeuren, wijzigt u de status in *Goedgekeurd*.</span><span class="sxs-lookup"><span data-stu-id="e73d2-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="e73d2-125">Geplande orders met de status *Goedgekeurd* worden als vaststaand en verwachte levering beschouwd door de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e73d2-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="e73d2-126">Ze worden dus niet gewijzigd of verwijderd tijdens een latere hoofdplanningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="e73d2-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="e73d2-127">Om dit gedrag te bereiken, kopieert de planningslogica de geplande orders met de status *Goedgekeurd* van de oude planversie naar de nieuwe planversie tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e73d2-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="e73d2-128">Merk op dat geplande orders met de status *Goedgekeurd* alleen als levering worden beschouwd in het specifieke hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="e73d2-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="e73d2-129">Als u de status van een enkele geplande order wilt wijzigen, [opent u een lijstpagina met geplande orders](#view-planned-orders). Vervolgens opent u de order en volgt u een van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="e73d2-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="e73d2-130">Wijzig op het sneltabblad **Algemeen** de waarde van het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="e73d2-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="e73d2-131">Selecteer vervolgens in het actievenster op het tabblad **Geplande order** in de groep **Verwerken** de optie **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e73d2-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="e73d2-132">Selecteer in het actievenster de optie **Goedkeuren** om de order te markeren als goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e73d2-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="e73d2-133">Als u de status van meerdere geplande orders tegelijk wilt wijzigen, [opent u een lijstpagina met geplande orders](#view-planned-orders). Vervolgens schakelt u het selectievakje in voor alle orders die u wilt wijzigen en volgt u een van de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="e73d2-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="e73d2-134">Selecteer vervolgens in het actievenster op het tabblad **Geplande order** in de groep **Verwerken** de optie **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e73d2-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="e73d2-135">Selecteer in het actievenster de optie **Goedkeuren** om de orders te markeren als goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e73d2-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="e73d2-136">Geplande orders goedkeuren</span><span class="sxs-lookup"><span data-stu-id="e73d2-136">Approve planned orders</span></span>

<span data-ttu-id="e73d2-137">Goedkeuring van geplande orders is een optionele stap in het proces om een gefiatteerde order te maken op basis van een geplande order.</span><span class="sxs-lookup"><span data-stu-id="e73d2-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="e73d2-138">In de volgende afbeelding ziet u hoe u de **Status**-waarde die aan elke geplande order is toegewezen, kunt gebruiken om een goedkeuringsworkflow te implementeren.</span><span class="sxs-lookup"><span data-stu-id="e73d2-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="e73d2-139">Als u een goedkeuringsproces wilt implementeren, past u de **Status**-waarde voor elke geplande order handmatig aan, zoals beschreven in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="e73d2-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Stroom geplande orders](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="e73d2-141">Het wordt aangeraden alle gewijzigde geplande orders goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="e73d2-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="e73d2-142">Als u dit niet doet, worden de bewerkingen genegeerd en overschreven bij de volgende planningsbewerking.</span><span class="sxs-lookup"><span data-stu-id="e73d2-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e73d2-143">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e73d2-143">Additional resources</span></span>

- [<span data-ttu-id="e73d2-144">Vast geplande orders</span><span class="sxs-lookup"><span data-stu-id="e73d2-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
