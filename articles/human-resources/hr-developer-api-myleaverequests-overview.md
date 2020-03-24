---
title: MyLeaveRequests-overzicht
description: De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092032"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="49c9c-103">MyLeaveRequests-overzicht</span><span class="sxs-lookup"><span data-stu-id="49c9c-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="49c9c-104">De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.</span><span class="sxs-lookup"><span data-stu-id="49c9c-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="49c9c-105">Sleutel</span><span class="sxs-lookup"><span data-stu-id="49c9c-105">Key</span></span>

  | <span data-ttu-id="49c9c-106">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="49c9c-106">Property Name</span></span> | <span data-ttu-id="49c9c-107">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="49c9c-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="49c9c-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="49c9c-108">dataAreaId</span></span>    | <span data-ttu-id="49c9c-109">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-109">String</span></span>    |
  | <span data-ttu-id="49c9c-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="49c9c-110">RequestId</span></span>     | <span data-ttu-id="49c9c-111">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-111">String</span></span>    |
  | <span data-ttu-id="49c9c-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="49c9c-112">LeaveType</span></span>     | <span data-ttu-id="49c9c-113">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-113">String</span></span>    |
  | <span data-ttu-id="49c9c-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="49c9c-114">LeaveDate</span></span>     | <span data-ttu-id="49c9c-115">Datum</span><span class="sxs-lookup"><span data-stu-id="49c9c-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="49c9c-116">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="49c9c-116">Properties</span></span>

  | <span data-ttu-id="49c9c-117">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="49c9c-117">Property Name</span></span>     | <span data-ttu-id="49c9c-118">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="49c9c-118">Data Type</span></span> | <span data-ttu-id="49c9c-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="49c9c-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="49c9c-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="49c9c-120">dataAreaId</span></span>        | <span data-ttu-id="49c9c-121">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-121">String</span></span>    | <span data-ttu-id="49c9c-122">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-122">X</span></span>        |
  | <span data-ttu-id="49c9c-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="49c9c-123">RequestId</span></span>         | <span data-ttu-id="49c9c-124">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-124">String</span></span>    | <span data-ttu-id="49c9c-125">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-125">X</span></span>        |
  | <span data-ttu-id="49c9c-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="49c9c-126">LeaveType</span></span>         | <span data-ttu-id="49c9c-127">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-127">String</span></span>    | <span data-ttu-id="49c9c-128">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-128">X</span></span>        |
  | <span data-ttu-id="49c9c-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="49c9c-129">LeaveDate</span></span>         | <span data-ttu-id="49c9c-130">Datum</span><span class="sxs-lookup"><span data-stu-id="49c9c-130">Date</span></span>      | <span data-ttu-id="49c9c-131">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-131">X</span></span>        |
  | <span data-ttu-id="49c9c-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="49c9c-132">ReasonCodeId</span></span>      | <span data-ttu-id="49c9c-133">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-133">String</span></span>    |          |
  | <span data-ttu-id="49c9c-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="49c9c-134">PersonnelNumber</span></span>   | <span data-ttu-id="49c9c-135">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-135">String</span></span>    | <span data-ttu-id="49c9c-136">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-136">X</span></span>        |
  | <span data-ttu-id="49c9c-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="49c9c-137">RequestDate</span></span>       | <span data-ttu-id="49c9c-138">Datum</span><span class="sxs-lookup"><span data-stu-id="49c9c-138">Date</span></span>      | <span data-ttu-id="49c9c-139">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-139">X</span></span>        |
  | <span data-ttu-id="49c9c-140">Opmerking</span><span class="sxs-lookup"><span data-stu-id="49c9c-140">Comment</span></span>           | <span data-ttu-id="49c9c-141">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="49c9c-141">String</span></span>    |          |
  | <span data-ttu-id="49c9c-142">Status</span><span class="sxs-lookup"><span data-stu-id="49c9c-142">Status</span></span>            | <span data-ttu-id="49c9c-143">Opsomming</span><span class="sxs-lookup"><span data-stu-id="49c9c-143">Enum</span></span>      | <span data-ttu-id="49c9c-144">X</span><span class="sxs-lookup"><span data-stu-id="49c9c-144">X</span></span>        |
  | <span data-ttu-id="49c9c-145">Bedrag</span><span class="sxs-lookup"><span data-stu-id="49c9c-145">Amount</span></span>            | <span data-ttu-id="49c9c-146">Real-modus</span><span class="sxs-lookup"><span data-stu-id="49c9c-146">Real</span></span>      |          |
  | <span data-ttu-id="49c9c-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="49c9c-147">HalfDayDefinition</span></span> | <span data-ttu-id="49c9c-148">Opsomming</span><span class="sxs-lookup"><span data-stu-id="49c9c-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="49c9c-149">Acties</span><span class="sxs-lookup"><span data-stu-id="49c9c-149">Actions</span></span>

 | <span data-ttu-id="49c9c-150">Naam actie</span><span class="sxs-lookup"><span data-stu-id="49c9c-150">Action Name</span></span>                               | <span data-ttu-id="49c9c-151">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="49c9c-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="49c9c-152">submit</span><span class="sxs-lookup"><span data-stu-id="49c9c-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="49c9c-153">De aanvraag indienen om door de workflow te worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="49c9c-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="49c9c-154">Zie ook</span><span class="sxs-lookup"><span data-stu-id="49c9c-154">See also</span></span>

- [<span data-ttu-id="49c9c-155">Een verlofverzoek indienen bij een werkstroom</span><span class="sxs-lookup"><span data-stu-id="49c9c-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="49c9c-156">Verificatie</span><span class="sxs-lookup"><span data-stu-id="49c9c-156">Authentication</span></span>](hr-developer-api-authentication.md)