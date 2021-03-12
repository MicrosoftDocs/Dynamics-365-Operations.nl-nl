---
title: Geplande orders goedkeuren
description: Dit onderwerp beschrijft de goedkeuring van geplande orders die worden ondersteund in Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983564"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="233af-103">Geplande orders goedkeuren</span><span class="sxs-lookup"><span data-stu-id="233af-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="233af-104">Dit onderwerp bevat informatie over het bijwerken van de status van geplande orders in Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="233af-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="233af-105">De goedkeuring van geplande orders is een optionele stap in de procedure om een gefiatteerde order te maken op basis van een geplande order.</span><span class="sxs-lookup"><span data-stu-id="233af-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="233af-106">Het wordt aanbevolen om gewijzigde geplande orders goed te keuren om te voorkomen dat de bewerkingen worden genegeerd en overschreven door de volgende planning.</span><span class="sxs-lookup"><span data-stu-id="233af-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Stroom geplande orders](media/approved-planned-orders-1.png)

<span data-ttu-id="233af-108">Via het veld **Status** kunt u uw voortgang in de gaten houden aan de hand van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="233af-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="233af-109">**Niet-verwerkt:** wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status *Niet-verwerkt*.</span><span class="sxs-lookup"><span data-stu-id="233af-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="233af-110">Geplande orders met deze status worden verwijderd tijdens de volgende planningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="233af-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="233af-111">**Voltooid:** als u besluit een geplande order niet te fiatteren, kunt u de status wijzigen in *Voltooid* om aan te geven dat u de evaluatie van deze geplande order hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="233af-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="233af-112">De statussen *Niet-verwerkt* en *Voltooid* worden op dezelfde manier behandeld in het systeem.</span><span class="sxs-lookup"><span data-stu-id="233af-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="233af-113">**Goedgekeurd:** als u wijzigingen wilt behouden of van plan bent om een geplande order te fiatteren, wijzigt u de status in *Goedgekeurd*.</span><span class="sxs-lookup"><span data-stu-id="233af-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="233af-114">Geplande orders met de status *Goedgekeurd* worden als vaststaand en verwachte levering beschouwd door de hoofdplanning. Ze worden dus niet gewijzigd of verwijderd tijdens een latere hoofdplanningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="233af-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="233af-115">Om dit te bereiken, kopieert de planningslogica de *goedgekeurde* geplande orders van de oude planversie naar de nieuwe planversie tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="233af-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="233af-116">*Goedgekeurde* geplande orders worden alleen als levering beschouwd in het specifieke hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="233af-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="233af-117">U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren.</span><span class="sxs-lookup"><span data-stu-id="233af-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
