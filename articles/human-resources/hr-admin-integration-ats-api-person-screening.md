---
title: Persoonscreening
description: In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125372"
---
# <a name="person-screening"></a><span data-ttu-id="f562d-103">Persoonscreening</span><span class="sxs-lookup"><span data-stu-id="f562d-103">Person screening</span></span>

<span data-ttu-id="f562d-104">In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="f562d-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f562d-105">Fsyieke naam: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="f562d-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="f562d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f562d-106">Description</span></span>

<span data-ttu-id="f562d-107">Deze entiteit beschrijft de screenings waarvoor een kandidaat is geslaagd of moet slagen voor een aanstelling.</span><span class="sxs-lookup"><span data-stu-id="f562d-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f562d-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="f562d-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="f562d-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="f562d-109">Properties</span></span>

| <span data-ttu-id="f562d-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="f562d-110">Property</span></span><br><span data-ttu-id="f562d-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="f562d-111">**Physical name**</span></span><br><span data-ttu-id="f562d-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="f562d-112">**_Type_**</span></span> | <span data-ttu-id="f562d-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="f562d-113">Use</span></span> | <span data-ttu-id="f562d-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f562d-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f562d-115">**Entiteits-id Persoonscreening**</span><span class="sxs-lookup"><span data-stu-id="f562d-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="f562d-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="f562d-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="f562d-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f562d-117">*GUID*</span></span> | <span data-ttu-id="f562d-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="f562d-118">Read-only</span></span><br><span data-ttu-id="f562d-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="f562d-119">Required</span></span><br><span data-ttu-id="f562d-120">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="f562d-120">System-generated</span></span> | <span data-ttu-id="f562d-121">Unieke primaire id voor de persoonscreeningrecord.</span><span class="sxs-lookup"><span data-stu-id="f562d-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="f562d-122">**Partijnummer**</span><span class="sxs-lookup"><span data-stu-id="f562d-122">**Party Number**</span></span><br><span data-ttu-id="f562d-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="f562d-123">mshr_partynumber</span></span><br><span data-ttu-id="f562d-124">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f562d-124">*String*</span></span> | <span data-ttu-id="f562d-125">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="f562d-125">Read/write</span></span><br><span data-ttu-id="f562d-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="f562d-126">Required</span></span> | <span data-ttu-id="f562d-127">Het partijnummer (persoon) dat aan de kandidaat is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f562d-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="f562d-128">**Waarde persoonlijke id**</span><span class="sxs-lookup"><span data-stu-id="f562d-128">**Person ID Value**</span></span><br><span data-ttu-id="f562d-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="f562d-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="f562d-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f562d-130">*GUID*</span></span> | <span data-ttu-id="f562d-131">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="f562d-131">Read-only</span></span><br><span data-ttu-id="f562d-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="f562d-132">Required</span></span><br><span data-ttu-id="f562d-133">Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="f562d-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="f562d-134">De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon).</span><span class="sxs-lookup"><span data-stu-id="f562d-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="f562d-135">**Screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="f562d-135">**Screening Type ID**</span></span><br><span data-ttu-id="f562d-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="f562d-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="f562d-137">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f562d-137">*String*</span></span> | <span data-ttu-id="f562d-138">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="f562d-138">Read/write</span></span><br><span data-ttu-id="f562d-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="f562d-139">Required</span></span><br><span data-ttu-id="f562d-140">Refererende sleutel: Screeningtype</span><span class="sxs-lookup"><span data-stu-id="f562d-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="f562d-141">De id van het screeningtype dat is gedefinieerd in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f562d-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="f562d-142">**Waarde screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="f562d-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="f562d-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="f562d-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="f562d-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f562d-144">*GUID*</span></span> | <span data-ttu-id="f562d-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="f562d-145">Read-only</span></span><br><span data-ttu-id="f562d-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="f562d-146">Required</span></span><br><span data-ttu-id="f562d-147">Refererende sleutel: mshr_hcmscreeningtypeentityid van mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="f562d-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="f562d-148">Door het systeem gegenereerde id voor de record van het screeningtype in de gekoppelde entiteit.</span><span class="sxs-lookup"><span data-stu-id="f562d-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="f562d-149">**Vereist door**</span><span class="sxs-lookup"><span data-stu-id="f562d-149">**Required By**</span></span><br><span data-ttu-id="f562d-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="f562d-150">mshr_requiredby</span></span><br><span data-ttu-id="f562d-151">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="f562d-151">*Datetime*</span></span> | <span data-ttu-id="f562d-152">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="f562d-152">Read/write</span></span><br><span data-ttu-id="f562d-153">Optioneel</span><span class="sxs-lookup"><span data-stu-id="f562d-153">Optional</span></span> | <span data-ttu-id="f562d-154">De datum waarop de screening moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="f562d-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="f562d-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="f562d-155">**Status**</span></span><br><span data-ttu-id="f562d-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="f562d-156">mshr_status</span></span><br><span data-ttu-id="f562d-157">*mshr_hcmcompletionstatus option set*</span><span class="sxs-lookup"><span data-stu-id="f562d-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="f562d-158">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="f562d-158">Read/write</span></span><br><span data-ttu-id="f562d-159">Vereist</span><span class="sxs-lookup"><span data-stu-id="f562d-159">Required</span></span> | <span data-ttu-id="f562d-160">De status van de kandidaat voor de screening.</span><span class="sxs-lookup"><span data-stu-id="f562d-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="f562d-161">**Datum van voltooiing**</span><span class="sxs-lookup"><span data-stu-id="f562d-161">**Completed Date**</span></span><br><span data-ttu-id="f562d-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="f562d-162">mshr_completeddate</span></span><br><span data-ttu-id="f562d-163">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="f562d-163">*Datetime*</span></span> | <span data-ttu-id="f562d-164">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="f562d-164">Read/write</span></span><br><span data-ttu-id="f562d-165">Optioneel</span><span class="sxs-lookup"><span data-stu-id="f562d-165">Optional</span></span> | <span data-ttu-id="f562d-166">De datum waarop de screening is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f562d-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="f562d-167">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="f562d-167">**Notes**</span></span><br><span data-ttu-id="f562d-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="f562d-168">mshr_note</span></span><br><span data-ttu-id="f562d-169">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="f562d-169">*String*</span></span> | <span data-ttu-id="f562d-170">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="f562d-170">Read/write</span></span><br><span data-ttu-id="f562d-171">Optioneel</span><span class="sxs-lookup"><span data-stu-id="f562d-171">Optional</span></span> | <span data-ttu-id="f562d-172">Notities die worden gebruikt door aanstellende managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="f562d-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f562d-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f562d-173">See also</span></span>

[<span data-ttu-id="f562d-174">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="f562d-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f562d-175">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="f562d-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

