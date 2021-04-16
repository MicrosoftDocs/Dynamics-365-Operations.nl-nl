---
title: MyLeaveRequests-overzicht
description: De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803628"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="cea5a-103">MyLeaveRequests-overzicht</span><span class="sxs-lookup"><span data-stu-id="cea5a-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cea5a-104">De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.</span><span class="sxs-lookup"><span data-stu-id="cea5a-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="cea5a-105">Sleutel</span><span class="sxs-lookup"><span data-stu-id="cea5a-105">Key</span></span>

  | <span data-ttu-id="cea5a-106">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="cea5a-106">Property Name</span></span> | <span data-ttu-id="cea5a-107">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="cea5a-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="cea5a-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="cea5a-108">dataAreaId</span></span>    | <span data-ttu-id="cea5a-109">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-109">String</span></span>    |
  | <span data-ttu-id="cea5a-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="cea5a-110">RequestId</span></span>     | <span data-ttu-id="cea5a-111">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-111">String</span></span>    |
  | <span data-ttu-id="cea5a-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="cea5a-112">LeaveType</span></span>     | <span data-ttu-id="cea5a-113">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-113">String</span></span>    |
  | <span data-ttu-id="cea5a-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="cea5a-114">LeaveDate</span></span>     | <span data-ttu-id="cea5a-115">Datum</span><span class="sxs-lookup"><span data-stu-id="cea5a-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="cea5a-116">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="cea5a-116">Properties</span></span>

  | <span data-ttu-id="cea5a-117">Naam van eigenschap</span><span class="sxs-lookup"><span data-stu-id="cea5a-117">Property Name</span></span>     | <span data-ttu-id="cea5a-118">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="cea5a-118">Data Type</span></span> | <span data-ttu-id="cea5a-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="cea5a-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="cea5a-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="cea5a-120">dataAreaId</span></span>        | <span data-ttu-id="cea5a-121">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-121">String</span></span>    | <span data-ttu-id="cea5a-122">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-122">X</span></span>        |
  | <span data-ttu-id="cea5a-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="cea5a-123">RequestId</span></span>         | <span data-ttu-id="cea5a-124">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-124">String</span></span>    | <span data-ttu-id="cea5a-125">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-125">X</span></span>        |
  | <span data-ttu-id="cea5a-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="cea5a-126">LeaveType</span></span>         | <span data-ttu-id="cea5a-127">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-127">String</span></span>    | <span data-ttu-id="cea5a-128">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-128">X</span></span>        |
  | <span data-ttu-id="cea5a-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="cea5a-129">LeaveDate</span></span>         | <span data-ttu-id="cea5a-130">Datum</span><span class="sxs-lookup"><span data-stu-id="cea5a-130">Date</span></span>      | <span data-ttu-id="cea5a-131">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-131">X</span></span>        |
  | <span data-ttu-id="cea5a-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="cea5a-132">ReasonCodeId</span></span>      | <span data-ttu-id="cea5a-133">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-133">String</span></span>    |          |
  | <span data-ttu-id="cea5a-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="cea5a-134">PersonnelNumber</span></span>   | <span data-ttu-id="cea5a-135">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-135">String</span></span>    | <span data-ttu-id="cea5a-136">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-136">X</span></span>        |
  | <span data-ttu-id="cea5a-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="cea5a-137">RequestDate</span></span>       | <span data-ttu-id="cea5a-138">Datum</span><span class="sxs-lookup"><span data-stu-id="cea5a-138">Date</span></span>      | <span data-ttu-id="cea5a-139">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-139">X</span></span>        |
  | <span data-ttu-id="cea5a-140">Opmerking</span><span class="sxs-lookup"><span data-stu-id="cea5a-140">Comment</span></span>           | <span data-ttu-id="cea5a-141">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cea5a-141">String</span></span>    |          |
  | <span data-ttu-id="cea5a-142">Status</span><span class="sxs-lookup"><span data-stu-id="cea5a-142">Status</span></span>            | <span data-ttu-id="cea5a-143">Opsomming</span><span class="sxs-lookup"><span data-stu-id="cea5a-143">Enum</span></span>      | <span data-ttu-id="cea5a-144">X</span><span class="sxs-lookup"><span data-stu-id="cea5a-144">X</span></span>        |
  | <span data-ttu-id="cea5a-145">Bedrag</span><span class="sxs-lookup"><span data-stu-id="cea5a-145">Amount</span></span>            | <span data-ttu-id="cea5a-146">Real-modus</span><span class="sxs-lookup"><span data-stu-id="cea5a-146">Real</span></span>      |          |
  | <span data-ttu-id="cea5a-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="cea5a-147">HalfDayDefinition</span></span> | <span data-ttu-id="cea5a-148">Opsomming</span><span class="sxs-lookup"><span data-stu-id="cea5a-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="cea5a-149">Acties</span><span class="sxs-lookup"><span data-stu-id="cea5a-149">Actions</span></span>

 | <span data-ttu-id="cea5a-150">Naam actie</span><span class="sxs-lookup"><span data-stu-id="cea5a-150">Action Name</span></span>                               | <span data-ttu-id="cea5a-151">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="cea5a-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="cea5a-152">submit</span><span class="sxs-lookup"><span data-stu-id="cea5a-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="cea5a-153">De aanvraag indienen om door de workflow te worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cea5a-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cea5a-154">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cea5a-154">See also</span></span>

- [<span data-ttu-id="cea5a-155">Een verlofverzoek indienen bij een werkstroom</span><span class="sxs-lookup"><span data-stu-id="cea5a-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="cea5a-156">Verificatie</span><span class="sxs-lookup"><span data-stu-id="cea5a-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]