---
title: Salarisdetails voor posities
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019317"
---
# <a name="payroll-position"></a><span data-ttu-id="c12cc-103">Salarispositie</span><span class="sxs-lookup"><span data-stu-id="c12cc-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c12cc-104">Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c12cc-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="c12cc-105">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="c12cc-105">Properties</span></span>

| <span data-ttu-id="c12cc-106">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="c12cc-106">Property</span></span><br><span data-ttu-id="c12cc-107">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="c12cc-107">**Physical name**</span></span><br><span data-ttu-id="c12cc-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="c12cc-108">**_Type_**</span></span> | <span data-ttu-id="c12cc-109">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="c12cc-109">Use</span></span> | <span data-ttu-id="c12cc-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c12cc-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c12cc-111">**Jaarlijkse normale uren**</span><span class="sxs-lookup"><span data-stu-id="c12cc-111">**Annual regular hours**</span></span><br><span data-ttu-id="c12cc-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="c12cc-112">annualregularhours</span></span><br><span data-ttu-id="c12cc-113">*Decimaal*</span><span class="sxs-lookup"><span data-stu-id="c12cc-113">*Decimal*</span></span> | <span data-ttu-id="c12cc-114">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-114">Read-only</span></span><br><span data-ttu-id="c12cc-115">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-115">Required</span></span> | <span data-ttu-id="c12cc-116">Jaarlijkse normale uren die voor de positie zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c12cc-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="c12cc-117">**Entiteit-id Salarisdetails voor posities**</span><span class="sxs-lookup"><span data-stu-id="c12cc-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="c12cc-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="c12cc-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="c12cc-119">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c12cc-119">*Guid*</span></span> | <span data-ttu-id="c12cc-120">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-120">Required</span></span><br><span data-ttu-id="c12cc-121">Door systeem gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c12cc-121">System generated.</span></span> | <span data-ttu-id="c12cc-122">Een door het systeem gegenereerde GUID-waarde als unieke id van de positie.</span><span class="sxs-lookup"><span data-stu-id="c12cc-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="c12cc-123">**Primair veld**</span><span class="sxs-lookup"><span data-stu-id="c12cc-123">**Primary field**</span></span><br><span data-ttu-id="c12cc-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="c12cc-124">mshr_primaryfield</span></span><br><span data-ttu-id="c12cc-125">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c12cc-125">*String*</span></span> | <span data-ttu-id="c12cc-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-126">Required</span></span><br><span data-ttu-id="c12cc-127">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="c12cc-127">System generated</span></span> |  |
| <span data-ttu-id="c12cc-128">**Waarde positiefunctie-id**</span><span class="sxs-lookup"><span data-stu-id="c12cc-128">**Position job ID value**</span></span><br><span data-ttu-id="c12cc-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="c12cc-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="c12cc-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c12cc-130">*GUID*</span></span> | <span data-ttu-id="c12cc-131">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-131">Read-only</span></span><br><span data-ttu-id="c12cc-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-132">Required</span></span><br><span data-ttu-id="c12cc-133">Refererende sleutel: mshr_PayrollPositionJobEntity van de mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="c12cc-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="c12cc-134">Id van de taak die aan de geselecteerde positie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c12cc-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="c12cc-135">**Waarde vaste compensatieplan-id**</span><span class="sxs-lookup"><span data-stu-id="c12cc-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="c12cc-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="c12cc-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="c12cc-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c12cc-137">*GUID*</span></span> | <span data-ttu-id="c12cc-138">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-138">Read-only</span></span><br><span data-ttu-id="c12cc-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-139">Required</span></span><br><span data-ttu-id="c12cc-140">Refererende sleutel: mshr_FixedCompPlan_id van mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="c12cc-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="c12cc-141">Id van het vaste compensatieplan dat aan de positie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c12cc-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="c12cc-142">**Betalingscyclus-id**</span><span class="sxs-lookup"><span data-stu-id="c12cc-142">**Pay cycle ID**</span></span><br><span data-ttu-id="c12cc-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="c12cc-143">mshr_primaryfield</span></span><br><span data-ttu-id="c12cc-144">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c12cc-144">*String*</span></span> | <span data-ttu-id="c12cc-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-145">Read-only</span></span><br><span data-ttu-id="c12cc-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-146">Required</span></span> | <span data-ttu-id="c12cc-147">De salariscyclus die voor de positie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c12cc-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="c12cc-148">**Betaald door rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="c12cc-148">**Paid by legal entity**</span></span><br><span data-ttu-id="c12cc-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="c12cc-149">paidbylegalentity</span></span><br><span data-ttu-id="c12cc-150">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c12cc-150">*String*</span></span> | <span data-ttu-id="c12cc-151">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-151">Read-only</span></span><br><span data-ttu-id="c12cc-152">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-152">Required</span></span> | <span data-ttu-id="c12cc-153">De rechtspersoon die is gedefinieerd in de positie die verantwoordelijk is voor de uitgifte van de betaling.</span><span class="sxs-lookup"><span data-stu-id="c12cc-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="c12cc-154">**Positie-id**</span><span class="sxs-lookup"><span data-stu-id="c12cc-154">**Position ID**</span></span><br><span data-ttu-id="c12cc-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="c12cc-155">mshr_positionid</span></span><br><span data-ttu-id="c12cc-156">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c12cc-156">*String*</span></span> | <span data-ttu-id="c12cc-157">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-157">Read-only</span></span><br><span data-ttu-id="c12cc-158">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-158">Required</span></span> | <span data-ttu-id="c12cc-159">De id van de positie.</span><span class="sxs-lookup"><span data-stu-id="c12cc-159">The ID of the position.</span></span> |
| <span data-ttu-id="c12cc-160">**Geldig tot**</span><span class="sxs-lookup"><span data-stu-id="c12cc-160">**Valid to**</span></span><br><span data-ttu-id="c12cc-161">validto</span><span class="sxs-lookup"><span data-stu-id="c12cc-161">validto</span></span><br><span data-ttu-id="c12cc-162">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="c12cc-162">*Date Time Offset*</span></span> | <span data-ttu-id="c12cc-163">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-163">Read-only</span></span><br><span data-ttu-id="c12cc-164">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-164">Required</span></span> |<span data-ttu-id="c12cc-165">De datum waarop de positiedetails geldig worden.</span><span class="sxs-lookup"><span data-stu-id="c12cc-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="c12cc-166">**Geldig vanaf**</span><span class="sxs-lookup"><span data-stu-id="c12cc-166">**Valid from**</span></span><br><span data-ttu-id="c12cc-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="c12cc-167">validfrom</span></span><br><span data-ttu-id="c12cc-168">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="c12cc-168">*Date Time Offset*</span></span> | <span data-ttu-id="c12cc-169">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c12cc-169">Read-only</span></span><br><span data-ttu-id="c12cc-170">Vereist</span><span class="sxs-lookup"><span data-stu-id="c12cc-170">Required</span></span> |<span data-ttu-id="c12cc-171">De datum tot wanneer de positiedetails geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="c12cc-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="c12cc-172">**Query**</span><span class="sxs-lookup"><span data-stu-id="c12cc-172">**Query**</span></span>

<span data-ttu-id="c12cc-173">**Aanvragen**</span><span class="sxs-lookup"><span data-stu-id="c12cc-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="c12cc-174">**Respons**</span><span class="sxs-lookup"><span data-stu-id="c12cc-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
