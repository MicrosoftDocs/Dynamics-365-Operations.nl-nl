---
title: MyLeaveRequests-overzicht
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008615"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="0e200-102">MyLeaveRequests-overzicht</span><span class="sxs-lookup"><span data-stu-id="0e200-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="0e200-103">De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.</span><span class="sxs-lookup"><span data-stu-id="0e200-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="0e200-104">Sleutel</span><span class="sxs-lookup"><span data-stu-id="0e200-104">Key</span></span>

  | <span data-ttu-id="0e200-105">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="0e200-105">Property Name</span></span> | <span data-ttu-id="0e200-106">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="0e200-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="0e200-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0e200-107">dataAreaId</span></span>    | <span data-ttu-id="0e200-108">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-108">String</span></span>    |
  | <span data-ttu-id="0e200-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="0e200-109">RequestId</span></span>     | <span data-ttu-id="0e200-110">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-110">String</span></span>    |
  | <span data-ttu-id="0e200-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="0e200-111">LeaveType</span></span>     | <span data-ttu-id="0e200-112">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-112">String</span></span>    |
  | <span data-ttu-id="0e200-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0e200-113">LeaveDate</span></span>     | <span data-ttu-id="0e200-114">Datum</span><span class="sxs-lookup"><span data-stu-id="0e200-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="0e200-115">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="0e200-115">Properties</span></span>

  | <span data-ttu-id="0e200-116">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="0e200-116">Property Name</span></span>     | <span data-ttu-id="0e200-117">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="0e200-117">Data Type</span></span> | <span data-ttu-id="0e200-118">Vereist</span><span class="sxs-lookup"><span data-stu-id="0e200-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="0e200-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0e200-119">dataAreaId</span></span>        | <span data-ttu-id="0e200-120">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-120">String</span></span>    | <span data-ttu-id="0e200-121">X</span><span class="sxs-lookup"><span data-stu-id="0e200-121">X</span></span>        |
  | <span data-ttu-id="0e200-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="0e200-122">RequestId</span></span>         | <span data-ttu-id="0e200-123">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-123">String</span></span>    | <span data-ttu-id="0e200-124">X</span><span class="sxs-lookup"><span data-stu-id="0e200-124">X</span></span>        |
  | <span data-ttu-id="0e200-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="0e200-125">LeaveType</span></span>         | <span data-ttu-id="0e200-126">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-126">String</span></span>    | <span data-ttu-id="0e200-127">X</span><span class="sxs-lookup"><span data-stu-id="0e200-127">X</span></span>        |
  | <span data-ttu-id="0e200-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0e200-128">LeaveDate</span></span>         | <span data-ttu-id="0e200-129">Datum</span><span class="sxs-lookup"><span data-stu-id="0e200-129">Date</span></span>      | <span data-ttu-id="0e200-130">X</span><span class="sxs-lookup"><span data-stu-id="0e200-130">X</span></span>        |
  | <span data-ttu-id="0e200-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="0e200-131">ReasonCodeId</span></span>      | <span data-ttu-id="0e200-132">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-132">String</span></span>    |          |
  | <span data-ttu-id="0e200-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="0e200-133">PersonnelNumber</span></span>   | <span data-ttu-id="0e200-134">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-134">String</span></span>    | <span data-ttu-id="0e200-135">X</span><span class="sxs-lookup"><span data-stu-id="0e200-135">X</span></span>        |
  | <span data-ttu-id="0e200-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="0e200-136">RequestDate</span></span>       | <span data-ttu-id="0e200-137">Datum</span><span class="sxs-lookup"><span data-stu-id="0e200-137">Date</span></span>      | <span data-ttu-id="0e200-138">X</span><span class="sxs-lookup"><span data-stu-id="0e200-138">X</span></span>        |
  | <span data-ttu-id="0e200-139">Opmerking</span><span class="sxs-lookup"><span data-stu-id="0e200-139">Comment</span></span>           | <span data-ttu-id="0e200-140">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="0e200-140">String</span></span>    |          |
  | <span data-ttu-id="0e200-141">Status</span><span class="sxs-lookup"><span data-stu-id="0e200-141">Status</span></span>            | <span data-ttu-id="0e200-142">Opsomming</span><span class="sxs-lookup"><span data-stu-id="0e200-142">Enum</span></span>      | <span data-ttu-id="0e200-143">X</span><span class="sxs-lookup"><span data-stu-id="0e200-143">X</span></span>        |
  | <span data-ttu-id="0e200-144">Bedrag</span><span class="sxs-lookup"><span data-stu-id="0e200-144">Amount</span></span>            | <span data-ttu-id="0e200-145">Real-modus</span><span class="sxs-lookup"><span data-stu-id="0e200-145">Real</span></span>      |          |
  | <span data-ttu-id="0e200-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="0e200-146">HalfDayDefinition</span></span> | <span data-ttu-id="0e200-147">Opsomming</span><span class="sxs-lookup"><span data-stu-id="0e200-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="0e200-148">Acties</span><span class="sxs-lookup"><span data-stu-id="0e200-148">Actions</span></span>

 | <span data-ttu-id="0e200-149">Naam actie</span><span class="sxs-lookup"><span data-stu-id="0e200-149">Action Name</span></span>                               | <span data-ttu-id="0e200-150">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0e200-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="0e200-151">submit</span><span class="sxs-lookup"><span data-stu-id="0e200-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="0e200-152">De aanvraag indienen om door de workflow te worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="0e200-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0e200-153">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0e200-153">See also</span></span>

- [<span data-ttu-id="0e200-154">Een verlofverzoek indienen bij een werkstroom</span><span class="sxs-lookup"><span data-stu-id="0e200-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="0e200-155">Verificatie</span><span class="sxs-lookup"><span data-stu-id="0e200-155">Authentication</span></span>](hr-developer-api-authentication.md)