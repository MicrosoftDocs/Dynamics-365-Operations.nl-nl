---
title: Status wervingsaanvraag
description: In dit onderwerp wordt de optieset voor Status wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464641"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="51e2a-103">Status wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="51e2a-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="51e2a-104">In dit onderwerp wordt de optieset voor Status wervingsaanvraag voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="51e2a-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="51e2a-105">Fysieke naam: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="51e2a-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="51e2a-106">Voor deze opsomming wordt de optieset voor de statuswaarden van een wervingsaanvraag ingesteld.</span><span class="sxs-lookup"><span data-stu-id="51e2a-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="51e2a-107">Waarde</span><span class="sxs-lookup"><span data-stu-id="51e2a-107">Value</span></span> | <span data-ttu-id="51e2a-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="51e2a-108">Label</span></span> | <span data-ttu-id="51e2a-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51e2a-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="51e2a-110">200000000</span><span class="sxs-lookup"><span data-stu-id="51e2a-110">200000000</span></span> | <span data-ttu-id="51e2a-111">Concept</span><span class="sxs-lookup"><span data-stu-id="51e2a-111">Draft</span></span> | <span data-ttu-id="51e2a-112">De aanvraag is in concept en gereed voor actieve werving.</span><span class="sxs-lookup"><span data-stu-id="51e2a-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="51e2a-113">200000001</span><span class="sxs-lookup"><span data-stu-id="51e2a-113">200000001</span></span> | <span data-ttu-id="51e2a-114">Wordt gecontroleerd</span><span class="sxs-lookup"><span data-stu-id="51e2a-114">In Review</span></span> | <span data-ttu-id="51e2a-115">De aanvraag is ingediend en wordt gerouteerd voor goedkeuring per werkstroom.</span><span class="sxs-lookup"><span data-stu-id="51e2a-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="51e2a-116">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="51e2a-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="51e2a-117">200000002</span><span class="sxs-lookup"><span data-stu-id="51e2a-117">200000002</span></span> | <span data-ttu-id="51e2a-118">In behandeling</span><span class="sxs-lookup"><span data-stu-id="51e2a-118">Pending</span></span> | <span data-ttu-id="51e2a-119">De werkstroomactie voor de aanvraag is in behandeling.</span><span class="sxs-lookup"><span data-stu-id="51e2a-119">The request is pending workflow action.</span></span> <span data-ttu-id="51e2a-120">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="51e2a-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="51e2a-121">200000003</span><span class="sxs-lookup"><span data-stu-id="51e2a-121">200000003</span></span> | <span data-ttu-id="51e2a-122">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="51e2a-122">Canceled</span></span> | <span data-ttu-id="51e2a-123">Het verzoek is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="51e2a-123">The request has been canceled.</span></span> <span data-ttu-id="51e2a-124">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="51e2a-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="51e2a-125">200000004</span><span class="sxs-lookup"><span data-stu-id="51e2a-125">200000004</span></span> | <span data-ttu-id="51e2a-126">Geweigerd</span><span class="sxs-lookup"><span data-stu-id="51e2a-126">Denied</span></span> | <span data-ttu-id="51e2a-127">De aanvraag is afgewezen.</span><span class="sxs-lookup"><span data-stu-id="51e2a-127">The request has been denied.</span></span> <span data-ttu-id="51e2a-128">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="51e2a-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="51e2a-129">200000005</span><span class="sxs-lookup"><span data-stu-id="51e2a-129">200000005</span></span> | <span data-ttu-id="51e2a-130">Actief</span><span class="sxs-lookup"><span data-stu-id="51e2a-130">Active</span></span> | <span data-ttu-id="51e2a-131">Elke werkstroom is voltooid en goedgekeurd en de aanvraag is klaar voor actieve werving.</span><span class="sxs-lookup"><span data-stu-id="51e2a-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="51e2a-132">200000006</span><span class="sxs-lookup"><span data-stu-id="51e2a-132">200000006</span></span> | <span data-ttu-id="51e2a-133">Afgesloten</span><span class="sxs-lookup"><span data-stu-id="51e2a-133">Closed</span></span> | <span data-ttu-id="51e2a-134">De wervingsaanvraag is gesloten.</span><span class="sxs-lookup"><span data-stu-id="51e2a-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="51e2a-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="51e2a-135">See also</span></span>

[<span data-ttu-id="51e2a-136">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="51e2a-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="51e2a-137">Voorbeeldquery voor wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="51e2a-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]