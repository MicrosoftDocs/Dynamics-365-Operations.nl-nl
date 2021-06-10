---
title: Salarisdetails voor posities
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056775"
---
# <a name="payroll-position"></a><span data-ttu-id="610ab-103">Salarispositie</span><span class="sxs-lookup"><span data-stu-id="610ab-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="610ab-104">Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="610ab-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="610ab-105">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="610ab-105">Properties</span></span>

| <span data-ttu-id="610ab-106">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="610ab-106">Property</span></span><br><span data-ttu-id="610ab-107">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="610ab-107">**Physical name**</span></span><br><span data-ttu-id="610ab-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="610ab-108">**_Type_**</span></span> | <span data-ttu-id="610ab-109">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="610ab-109">Use</span></span> | <span data-ttu-id="610ab-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="610ab-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="610ab-111">**Jaarlijkse normale uren**</span><span class="sxs-lookup"><span data-stu-id="610ab-111">**Annual regular hours**</span></span><br><span data-ttu-id="610ab-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="610ab-112">annualregularhours</span></span><br><span data-ttu-id="610ab-113">*Decimaal*</span><span class="sxs-lookup"><span data-stu-id="610ab-113">*Decimal*</span></span> | <span data-ttu-id="610ab-114">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-114">Read-only</span></span><br><span data-ttu-id="610ab-115">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-115">Required</span></span> | <span data-ttu-id="610ab-116">Jaarlijkse normale uren die voor de positie zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="610ab-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="610ab-117">**Entiteit-id Salarisdetails voor posities**</span><span class="sxs-lookup"><span data-stu-id="610ab-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="610ab-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="610ab-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="610ab-119">*GUID*</span><span class="sxs-lookup"><span data-stu-id="610ab-119">*Guid*</span></span> | <span data-ttu-id="610ab-120">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-120">Required</span></span><br><span data-ttu-id="610ab-121">Door systeem gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="610ab-121">System generated.</span></span> | <span data-ttu-id="610ab-122">Een door het systeem gegenereerde GUID-waarde als unieke id van de positie.</span><span class="sxs-lookup"><span data-stu-id="610ab-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="610ab-123">**Primair veld**</span><span class="sxs-lookup"><span data-stu-id="610ab-123">**Primary field**</span></span><br><span data-ttu-id="610ab-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="610ab-124">mshr_primaryfield</span></span><br><span data-ttu-id="610ab-125">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="610ab-125">*String*</span></span> | <span data-ttu-id="610ab-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-126">Required</span></span><br><span data-ttu-id="610ab-127">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="610ab-127">System generated</span></span> |  |
| <span data-ttu-id="610ab-128">**Waarde positiefunctie-id**</span><span class="sxs-lookup"><span data-stu-id="610ab-128">**Position job ID value**</span></span><br><span data-ttu-id="610ab-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="610ab-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="610ab-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="610ab-130">*GUID*</span></span> | <span data-ttu-id="610ab-131">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-131">Read-only</span></span><br><span data-ttu-id="610ab-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-132">Required</span></span><br><span data-ttu-id="610ab-133">Refererende sleutel: mshr_PayrollPositionJobEntity van de mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="610ab-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="610ab-134">Id van de taak die aan de geselecteerde positie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="610ab-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="610ab-135">**Waarde vaste compensatieplan-id**</span><span class="sxs-lookup"><span data-stu-id="610ab-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="610ab-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="610ab-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="610ab-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="610ab-137">*GUID*</span></span> | <span data-ttu-id="610ab-138">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-138">Read-only</span></span><br><span data-ttu-id="610ab-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-139">Required</span></span><br><span data-ttu-id="610ab-140">Refererende sleutel: mshr_FixedCompPlan_id van mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="610ab-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="610ab-141">Id van het vaste compensatieplan dat aan de positie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="610ab-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="610ab-142">**Betalingscyclus-id**</span><span class="sxs-lookup"><span data-stu-id="610ab-142">**Pay cycle ID**</span></span><br><span data-ttu-id="610ab-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="610ab-143">mshr_primaryfield</span></span><br><span data-ttu-id="610ab-144">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="610ab-144">*String*</span></span> | <span data-ttu-id="610ab-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-145">Read-only</span></span><br><span data-ttu-id="610ab-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-146">Required</span></span> | <span data-ttu-id="610ab-147">De salariscyclus die voor de positie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="610ab-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="610ab-148">**Betaald door rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="610ab-148">**Paid by legal entity**</span></span><br><span data-ttu-id="610ab-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="610ab-149">paidbylegalentity</span></span><br><span data-ttu-id="610ab-150">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="610ab-150">*String*</span></span> | <span data-ttu-id="610ab-151">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-151">Read-only</span></span><br><span data-ttu-id="610ab-152">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-152">Required</span></span> | <span data-ttu-id="610ab-153">De rechtspersoon die is gedefinieerd in de positie die verantwoordelijk is voor de uitgifte van de betaling.</span><span class="sxs-lookup"><span data-stu-id="610ab-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="610ab-154">**Positie-id**</span><span class="sxs-lookup"><span data-stu-id="610ab-154">**Position ID**</span></span><br><span data-ttu-id="610ab-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="610ab-155">mshr_positionid</span></span><br><span data-ttu-id="610ab-156">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="610ab-156">*String*</span></span> | <span data-ttu-id="610ab-157">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-157">Read-only</span></span><br><span data-ttu-id="610ab-158">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-158">Required</span></span> | <span data-ttu-id="610ab-159">De id van de positie.</span><span class="sxs-lookup"><span data-stu-id="610ab-159">The ID of the position.</span></span> |
| <span data-ttu-id="610ab-160">**Geldig tot**</span><span class="sxs-lookup"><span data-stu-id="610ab-160">**Valid to**</span></span><br><span data-ttu-id="610ab-161">validto</span><span class="sxs-lookup"><span data-stu-id="610ab-161">validto</span></span><br><span data-ttu-id="610ab-162">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="610ab-162">*Date Time Offset*</span></span> | <span data-ttu-id="610ab-163">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-163">Read-only</span></span><br><span data-ttu-id="610ab-164">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-164">Required</span></span> |<span data-ttu-id="610ab-165">De datum waarop de positiedetails geldig worden.</span><span class="sxs-lookup"><span data-stu-id="610ab-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="610ab-166">**Geldig vanaf**</span><span class="sxs-lookup"><span data-stu-id="610ab-166">**Valid from**</span></span><br><span data-ttu-id="610ab-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="610ab-167">validfrom</span></span><br><span data-ttu-id="610ab-168">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="610ab-168">*Date Time Offset*</span></span> | <span data-ttu-id="610ab-169">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="610ab-169">Read-only</span></span><br><span data-ttu-id="610ab-170">Vereist</span><span class="sxs-lookup"><span data-stu-id="610ab-170">Required</span></span> |<span data-ttu-id="610ab-171">De datum tot wanneer de positiedetails geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="610ab-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="610ab-172">**Query**</span><span class="sxs-lookup"><span data-stu-id="610ab-172">**Query**</span></span>

<span data-ttu-id="610ab-173">**Aanvragen**</span><span class="sxs-lookup"><span data-stu-id="610ab-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="610ab-174">**Respons**</span><span class="sxs-lookup"><span data-stu-id="610ab-174">**Response**</span></span>

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
