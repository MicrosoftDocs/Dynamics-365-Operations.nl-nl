---
title: MyLeaveRequests-overzicht
description: De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115531"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="c5639-103">MyLeaveRequests-overzicht</span><span class="sxs-lookup"><span data-stu-id="c5639-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="c5639-104">De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.</span><span class="sxs-lookup"><span data-stu-id="c5639-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="c5639-105">Sleutel</span><span class="sxs-lookup"><span data-stu-id="c5639-105">Key</span></span>

  | <span data-ttu-id="c5639-106">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="c5639-106">Property Name</span></span> | <span data-ttu-id="c5639-107">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="c5639-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="c5639-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="c5639-108">dataAreaId</span></span>    | <span data-ttu-id="c5639-109">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-109">String</span></span>    |
  | <span data-ttu-id="c5639-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="c5639-110">RequestId</span></span>     | <span data-ttu-id="c5639-111">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-111">String</span></span>    |
  | <span data-ttu-id="c5639-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="c5639-112">LeaveType</span></span>     | <span data-ttu-id="c5639-113">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-113">String</span></span>    |
  | <span data-ttu-id="c5639-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="c5639-114">LeaveDate</span></span>     | <span data-ttu-id="c5639-115">Datum</span><span class="sxs-lookup"><span data-stu-id="c5639-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="c5639-116">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="c5639-116">Properties</span></span>

  | <span data-ttu-id="c5639-117">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="c5639-117">Property Name</span></span>     | <span data-ttu-id="c5639-118">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="c5639-118">Data Type</span></span> | <span data-ttu-id="c5639-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="c5639-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="c5639-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="c5639-120">dataAreaId</span></span>        | <span data-ttu-id="c5639-121">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-121">String</span></span>    | <span data-ttu-id="c5639-122">X</span><span class="sxs-lookup"><span data-stu-id="c5639-122">X</span></span>        |
  | <span data-ttu-id="c5639-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="c5639-123">RequestId</span></span>         | <span data-ttu-id="c5639-124">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-124">String</span></span>    | <span data-ttu-id="c5639-125">X</span><span class="sxs-lookup"><span data-stu-id="c5639-125">X</span></span>        |
  | <span data-ttu-id="c5639-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="c5639-126">LeaveType</span></span>         | <span data-ttu-id="c5639-127">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-127">String</span></span>    | <span data-ttu-id="c5639-128">X</span><span class="sxs-lookup"><span data-stu-id="c5639-128">X</span></span>        |
  | <span data-ttu-id="c5639-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="c5639-129">LeaveDate</span></span>         | <span data-ttu-id="c5639-130">Datum</span><span class="sxs-lookup"><span data-stu-id="c5639-130">Date</span></span>      | <span data-ttu-id="c5639-131">X</span><span class="sxs-lookup"><span data-stu-id="c5639-131">X</span></span>        |
  | <span data-ttu-id="c5639-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="c5639-132">ReasonCodeId</span></span>      | <span data-ttu-id="c5639-133">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-133">String</span></span>    |          |
  | <span data-ttu-id="c5639-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="c5639-134">PersonnelNumber</span></span>   | <span data-ttu-id="c5639-135">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-135">String</span></span>    | <span data-ttu-id="c5639-136">X</span><span class="sxs-lookup"><span data-stu-id="c5639-136">X</span></span>        |
  | <span data-ttu-id="c5639-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="c5639-137">RequestDate</span></span>       | <span data-ttu-id="c5639-138">Datum</span><span class="sxs-lookup"><span data-stu-id="c5639-138">Date</span></span>      | <span data-ttu-id="c5639-139">X</span><span class="sxs-lookup"><span data-stu-id="c5639-139">X</span></span>        |
  | <span data-ttu-id="c5639-140">Opmerking</span><span class="sxs-lookup"><span data-stu-id="c5639-140">Comment</span></span>           | <span data-ttu-id="c5639-141">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c5639-141">String</span></span>    |          |
  | <span data-ttu-id="c5639-142">Status</span><span class="sxs-lookup"><span data-stu-id="c5639-142">Status</span></span>            | <span data-ttu-id="c5639-143">Opsomming</span><span class="sxs-lookup"><span data-stu-id="c5639-143">Enum</span></span>      | <span data-ttu-id="c5639-144">X</span><span class="sxs-lookup"><span data-stu-id="c5639-144">X</span></span>        |
  | <span data-ttu-id="c5639-145">Bedrag</span><span class="sxs-lookup"><span data-stu-id="c5639-145">Amount</span></span>            | <span data-ttu-id="c5639-146">Real-modus</span><span class="sxs-lookup"><span data-stu-id="c5639-146">Real</span></span>      |          |
  | <span data-ttu-id="c5639-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="c5639-147">HalfDayDefinition</span></span> | <span data-ttu-id="c5639-148">Opsomming</span><span class="sxs-lookup"><span data-stu-id="c5639-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="c5639-149">Acties</span><span class="sxs-lookup"><span data-stu-id="c5639-149">Actions</span></span>

 | <span data-ttu-id="c5639-150">Naam actie</span><span class="sxs-lookup"><span data-stu-id="c5639-150">Action Name</span></span>                               | <span data-ttu-id="c5639-151">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c5639-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="c5639-152">submit</span><span class="sxs-lookup"><span data-stu-id="c5639-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="c5639-153">De aanvraag indienen om door de workflow te worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c5639-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c5639-154">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c5639-154">See also</span></span>

- [<span data-ttu-id="c5639-155">Een verlofverzoek indienen bij een werkstroom</span><span class="sxs-lookup"><span data-stu-id="c5639-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="c5639-156">Verificatie</span><span class="sxs-lookup"><span data-stu-id="c5639-156">Authentication</span></span>](hr-developer-api-authentication.md)