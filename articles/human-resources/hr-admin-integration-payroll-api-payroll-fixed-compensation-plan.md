---
title: Vast compensatieplan in salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Vast compensatieplan in salarisadministratie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021291"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="e9e60-103">Vast compensatieplan in salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="e9e60-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9e60-104">Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Vast compensatieplan in salarisadministratie in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e9e60-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e9e60-105">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="e9e60-105">Properties</span></span>

| <span data-ttu-id="e9e60-106">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="e9e60-106">Property</span></span><br><span data-ttu-id="e9e60-107">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="e9e60-107">**Physical name**</span></span><br><span data-ttu-id="e9e60-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-108">**_Type_**</span></span> | <span data-ttu-id="e9e60-109">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="e9e60-109">Use</span></span> | <span data-ttu-id="e9e60-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e9e60-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e9e60-111">**Werknemer-id**</span><span class="sxs-lookup"><span data-stu-id="e9e60-111">**Employee ID**</span></span><br><span data-ttu-id="e9e60-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="e9e60-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="e9e60-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9e60-113">*GUID*</span></span> | <span data-ttu-id="e9e60-114">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-114">Read-only</span></span><br><span data-ttu-id="e9e60-115">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-115">Required</span></span><br><span data-ttu-id="e9e60-116">Refererende sleutel: mshr_Employee_id van de entiteit mshr_payrollemployeeentity</span><span class="sxs-lookup"><span data-stu-id="e9e60-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="e9e60-117">Werknemer-id</span><span class="sxs-lookup"><span data-stu-id="e9e60-117">Employee ID</span></span> |
| <span data-ttu-id="e9e60-118">**Loontarief**</span><span class="sxs-lookup"><span data-stu-id="e9e60-118">**Pay rate**</span></span><br><span data-ttu-id="e9e60-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="e9e60-119">mshr_payrate</span></span><br><span data-ttu-id="e9e60-120">*Decimaal*</span><span class="sxs-lookup"><span data-stu-id="e9e60-120">*Decimal*</span></span> | <span data-ttu-id="e9e60-121">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-121">Read-only</span></span><br><span data-ttu-id="e9e60-122">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-122">Required</span></span> | <span data-ttu-id="e9e60-123">Salaristarief dat is gedefinieerd in de vastecompensatieregeling.</span><span class="sxs-lookup"><span data-stu-id="e9e60-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="e9e60-124">**Plan-id**</span><span class="sxs-lookup"><span data-stu-id="e9e60-124">**Plan ID**</span></span><br><span data-ttu-id="e9e60-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="e9e60-125">mshr_planid</span></span><br><span data-ttu-id="e9e60-126">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e9e60-126">*String*</span></span> | <span data-ttu-id="e9e60-127">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-127">Read-only</span></span><br><span data-ttu-id="e9e60-128">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-128">Required</span></span> |<span data-ttu-id="e9e60-129">Geeft het compensatieplan aan</span><span class="sxs-lookup"><span data-stu-id="e9e60-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="e9e60-130">**Geldig vanaf**</span><span class="sxs-lookup"><span data-stu-id="e9e60-130">**Valid from**</span></span><br><span data-ttu-id="e9e60-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="e9e60-131">mshr_validfrom</span></span><br><span data-ttu-id="e9e60-132">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="e9e60-132">*Date Time Offset*</span></span> |  <span data-ttu-id="e9e60-133">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-133">Read-only</span></span><br><span data-ttu-id="e9e60-134">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-134">Required</span></span> |<span data-ttu-id="e9e60-135">De datum vanaf wanneer de vaste compensatie voor de werknemer geldig is.</span><span class="sxs-lookup"><span data-stu-id="e9e60-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="e9e60-136">**Entiteit Vast compensatieplan in salarisadministratie**</span><span class="sxs-lookup"><span data-stu-id="e9e60-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="e9e60-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="e9e60-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="e9e60-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9e60-138">*GUID*</span></span> | <span data-ttu-id="e9e60-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-139">Required</span></span><br><span data-ttu-id="e9e60-140">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="e9e60-140">Sytem generated</span></span> | <span data-ttu-id="e9e60-141">Een door het systeem gegenereerde GUID-waarde als unieke id van het compensatieplan.</span><span class="sxs-lookup"><span data-stu-id="e9e60-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="e9e60-142">**Betalingsfrequentie**</span><span class="sxs-lookup"><span data-stu-id="e9e60-142">**Pay frequency**</span></span><br><span data-ttu-id="e9e60-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="e9e60-143">mshr_payfrequency</span></span><br><span data-ttu-id="e9e60-144">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e9e60-144">*String*</span></span> | <span data-ttu-id="e9e60-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-145">Read-only</span></span><br><span data-ttu-id="e9e60-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-146">Required</span></span> |<span data-ttu-id="e9e60-147">De frequentie waarmee de werknemer wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="e9e60-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="e9e60-148">**Geldig tot**</span><span class="sxs-lookup"><span data-stu-id="e9e60-148">**Valid to**</span></span><br><span data-ttu-id="e9e60-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="e9e60-149">mshr_validto</span></span><br><span data-ttu-id="e9e60-150">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="e9e60-150">*Date Time Offset*</span></span> | <span data-ttu-id="e9e60-151">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-151">Read-only</span></span> <br><span data-ttu-id="e9e60-152">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-152">Required</span></span> | <span data-ttu-id="e9e60-153">De datum tot wanneer de vaste compensatie voor de werknemer geldig is.</span><span class="sxs-lookup"><span data-stu-id="e9e60-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="e9e60-154">**Positie-id**</span><span class="sxs-lookup"><span data-stu-id="e9e60-154">**Position ID**</span></span><br><span data-ttu-id="e9e60-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="e9e60-155">mshr_positionid</span></span><br><span data-ttu-id="e9e60-156">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e9e60-156">*String*</span></span> | <span data-ttu-id="e9e60-157">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-157">Read-only</span></span> <br><span data-ttu-id="e9e60-158">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-158">Required</span></span> | <span data-ttu-id="e9e60-159">De positie-id die is gekoppeld aan de werknemer en de inschrijving voor het vaste compensatieplan.</span><span class="sxs-lookup"><span data-stu-id="e9e60-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="e9e60-160">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="e9e60-160">**Currency**</span></span><br><span data-ttu-id="e9e60-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="e9e60-161">mshr_currency</span></span><br><span data-ttu-id="e9e60-162">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e9e60-162">*String*</span></span> | <span data-ttu-id="e9e60-163">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-163">Read-only</span></span> <br><span data-ttu-id="e9e60-164">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-164">Required</span></span> |<span data-ttu-id="e9e60-165">De valuta die voor het vastecompensatieplan is gedefinieerd</span><span class="sxs-lookup"><span data-stu-id="e9e60-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="e9e60-166">**Personeelsnummer**</span><span class="sxs-lookup"><span data-stu-id="e9e60-166">**Personnel number**</span></span><br><span data-ttu-id="e9e60-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="e9e60-167">mshr_personnelnumber</span></span><br><span data-ttu-id="e9e60-168">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e9e60-168">*String*</span></span> | <span data-ttu-id="e9e60-169">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e9e60-169">Read-only</span></span><br><span data-ttu-id="e9e60-170">Vereist</span><span class="sxs-lookup"><span data-stu-id="e9e60-170">Required</span></span> |<span data-ttu-id="e9e60-171">Het unieke personeelsnummer van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="e9e60-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="e9e60-172">**Query**</span><span class="sxs-lookup"><span data-stu-id="e9e60-172">**Query**</span></span>

<span data-ttu-id="e9e60-173">**Aanvragen**</span><span class="sxs-lookup"><span data-stu-id="e9e60-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="e9e60-174">**Respons**</span><span class="sxs-lookup"><span data-stu-id="e9e60-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
