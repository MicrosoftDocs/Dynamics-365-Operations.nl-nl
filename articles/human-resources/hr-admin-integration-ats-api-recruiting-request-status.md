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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125949"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="ebd32-103">Status wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="ebd32-103">Recruiting request status</span></span>

<span data-ttu-id="ebd32-104">In dit onderwerp wordt de optieset voor Status wervingsaanvraag voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="ebd32-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ebd32-105">Fysieke naam: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="ebd32-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="ebd32-106">Voor deze opsomming wordt de optieset voor de statuswaarden van een wervingsaanvraag ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ebd32-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="ebd32-107">Waarde</span><span class="sxs-lookup"><span data-stu-id="ebd32-107">Value</span></span> | <span data-ttu-id="ebd32-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="ebd32-108">Label</span></span> | <span data-ttu-id="ebd32-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ebd32-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ebd32-110">200000000</span><span class="sxs-lookup"><span data-stu-id="ebd32-110">200000000</span></span> | <span data-ttu-id="ebd32-111">Concept</span><span class="sxs-lookup"><span data-stu-id="ebd32-111">Draft</span></span> | <span data-ttu-id="ebd32-112">De aanvraag is in concept en gereed voor actieve werving.</span><span class="sxs-lookup"><span data-stu-id="ebd32-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="ebd32-113">200000001</span><span class="sxs-lookup"><span data-stu-id="ebd32-113">200000001</span></span> | <span data-ttu-id="ebd32-114">Wordt gecontroleerd</span><span class="sxs-lookup"><span data-stu-id="ebd32-114">In Review</span></span> | <span data-ttu-id="ebd32-115">De aanvraag is ingediend en wordt gerouteerd voor goedkeuring per werkstroom.</span><span class="sxs-lookup"><span data-stu-id="ebd32-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="ebd32-116">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ebd32-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="ebd32-117">200000002</span><span class="sxs-lookup"><span data-stu-id="ebd32-117">200000002</span></span> | <span data-ttu-id="ebd32-118">In behandeling</span><span class="sxs-lookup"><span data-stu-id="ebd32-118">Pending</span></span> | <span data-ttu-id="ebd32-119">De werkstroomactie voor de aanvraag is in behandeling.</span><span class="sxs-lookup"><span data-stu-id="ebd32-119">The request is pending workflow action.</span></span> <span data-ttu-id="ebd32-120">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ebd32-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="ebd32-121">200000003</span><span class="sxs-lookup"><span data-stu-id="ebd32-121">200000003</span></span> | <span data-ttu-id="ebd32-122">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="ebd32-122">Canceled</span></span> | <span data-ttu-id="ebd32-123">Het verzoek is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="ebd32-123">The request has been canceled.</span></span> <span data-ttu-id="ebd32-124">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ebd32-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="ebd32-125">200000004</span><span class="sxs-lookup"><span data-stu-id="ebd32-125">200000004</span></span> | <span data-ttu-id="ebd32-126">Geweigerd</span><span class="sxs-lookup"><span data-stu-id="ebd32-126">Denied</span></span> | <span data-ttu-id="ebd32-127">De aanvraag is afgewezen.</span><span class="sxs-lookup"><span data-stu-id="ebd32-127">The request has been denied.</span></span> <span data-ttu-id="ebd32-128">Alleen beschikbaar als werkstroom is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ebd32-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="ebd32-129">200000005</span><span class="sxs-lookup"><span data-stu-id="ebd32-129">200000005</span></span> | <span data-ttu-id="ebd32-130">Actief</span><span class="sxs-lookup"><span data-stu-id="ebd32-130">Active</span></span> | <span data-ttu-id="ebd32-131">Elke werkstroom is voltooid en goedgekeurd en de aanvraag is klaar voor actieve werving.</span><span class="sxs-lookup"><span data-stu-id="ebd32-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="ebd32-132">200000006</span><span class="sxs-lookup"><span data-stu-id="ebd32-132">200000006</span></span> | <span data-ttu-id="ebd32-133">Afgesloten</span><span class="sxs-lookup"><span data-stu-id="ebd32-133">Closed</span></span> | <span data-ttu-id="ebd32-134">De wervingsaanvraag is gesloten.</span><span class="sxs-lookup"><span data-stu-id="ebd32-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ebd32-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ebd32-135">See also</span></span>

[<span data-ttu-id="ebd32-136">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="ebd32-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ebd32-137">Voorbeeldquery voor wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="ebd32-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
