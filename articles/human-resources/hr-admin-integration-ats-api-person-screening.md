---
title: Persoonscreening
description: In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059275"
---
# <a name="person-screening"></a><span data-ttu-id="bac43-103">Persoonscreening</span><span class="sxs-lookup"><span data-stu-id="bac43-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bac43-104">In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="bac43-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bac43-105">Fsyieke naam: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="bac43-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="bac43-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bac43-106">Description</span></span>

<span data-ttu-id="bac43-107">Deze entiteit beschrijft de screenings waarvoor een kandidaat is geslaagd of moet slagen voor een aanstelling.</span><span class="sxs-lookup"><span data-stu-id="bac43-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="bac43-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="bac43-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="bac43-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="bac43-109">Properties</span></span>

| <span data-ttu-id="bac43-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="bac43-110">Property</span></span><br><span data-ttu-id="bac43-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="bac43-111">**Physical name**</span></span><br><span data-ttu-id="bac43-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="bac43-112">**_Type_**</span></span> | <span data-ttu-id="bac43-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="bac43-113">Use</span></span> | <span data-ttu-id="bac43-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bac43-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bac43-115">**Entiteits-id Persoonscreening**</span><span class="sxs-lookup"><span data-stu-id="bac43-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="bac43-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="bac43-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="bac43-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bac43-117">*GUID*</span></span> | <span data-ttu-id="bac43-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="bac43-118">Read-only</span></span><br><span data-ttu-id="bac43-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="bac43-119">Required</span></span><br><span data-ttu-id="bac43-120">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="bac43-120">System-generated</span></span> | <span data-ttu-id="bac43-121">Unieke primaire id voor de persoonscreeningrecord.</span><span class="sxs-lookup"><span data-stu-id="bac43-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="bac43-122">**Partijnummer**</span><span class="sxs-lookup"><span data-stu-id="bac43-122">**Party Number**</span></span><br><span data-ttu-id="bac43-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="bac43-123">mshr_partynumber</span></span><br><span data-ttu-id="bac43-124">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="bac43-124">*String*</span></span> | <span data-ttu-id="bac43-125">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="bac43-125">Read/write</span></span><br><span data-ttu-id="bac43-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="bac43-126">Required</span></span> | <span data-ttu-id="bac43-127">Het partijnummer (persoon) dat aan de kandidaat is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="bac43-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="bac43-128">**Waarde persoonlijke id**</span><span class="sxs-lookup"><span data-stu-id="bac43-128">**Person ID Value**</span></span><br><span data-ttu-id="bac43-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="bac43-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="bac43-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bac43-130">*GUID*</span></span> | <span data-ttu-id="bac43-131">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="bac43-131">Read-only</span></span><br><span data-ttu-id="bac43-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="bac43-132">Required</span></span><br><span data-ttu-id="bac43-133">Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="bac43-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="bac43-134">De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon).</span><span class="sxs-lookup"><span data-stu-id="bac43-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="bac43-135">**Screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="bac43-135">**Screening Type ID**</span></span><br><span data-ttu-id="bac43-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="bac43-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="bac43-137">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="bac43-137">*String*</span></span> | <span data-ttu-id="bac43-138">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="bac43-138">Read/write</span></span><br><span data-ttu-id="bac43-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="bac43-139">Required</span></span><br><span data-ttu-id="bac43-140">Refererende sleutel: Screeningtype</span><span class="sxs-lookup"><span data-stu-id="bac43-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="bac43-141">De id van het screeningtype dat is gedefinieerd in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bac43-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="bac43-142">**Waarde screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="bac43-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="bac43-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="bac43-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="bac43-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bac43-144">*GUID*</span></span> | <span data-ttu-id="bac43-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="bac43-145">Read-only</span></span><br><span data-ttu-id="bac43-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="bac43-146">Required</span></span><br><span data-ttu-id="bac43-147">Refererende sleutel: mshr_hcmscreeningtypeentityid van mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="bac43-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="bac43-148">Door het systeem gegenereerde id voor de record van het screeningtype in de gekoppelde entiteit.</span><span class="sxs-lookup"><span data-stu-id="bac43-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="bac43-149">**Vereist door**</span><span class="sxs-lookup"><span data-stu-id="bac43-149">**Required By**</span></span><br><span data-ttu-id="bac43-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="bac43-150">mshr_requiredby</span></span><br><span data-ttu-id="bac43-151">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="bac43-151">*Datetime*</span></span> | <span data-ttu-id="bac43-152">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="bac43-152">Read/write</span></span><br><span data-ttu-id="bac43-153">Optioneel</span><span class="sxs-lookup"><span data-stu-id="bac43-153">Optional</span></span> | <span data-ttu-id="bac43-154">De datum waarop de screening moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="bac43-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="bac43-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="bac43-155">**Status**</span></span><br><span data-ttu-id="bac43-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="bac43-156">mshr_status</span></span><br><span data-ttu-id="bac43-157">*mshr_hcmcompletionstatus option set*</span><span class="sxs-lookup"><span data-stu-id="bac43-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="bac43-158">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="bac43-158">Read/write</span></span><br><span data-ttu-id="bac43-159">Vereist</span><span class="sxs-lookup"><span data-stu-id="bac43-159">Required</span></span> | <span data-ttu-id="bac43-160">De status van de kandidaat voor de screening.</span><span class="sxs-lookup"><span data-stu-id="bac43-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="bac43-161">**Datum van voltooiing**</span><span class="sxs-lookup"><span data-stu-id="bac43-161">**Completed Date**</span></span><br><span data-ttu-id="bac43-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="bac43-162">mshr_completeddate</span></span><br><span data-ttu-id="bac43-163">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="bac43-163">*Datetime*</span></span> | <span data-ttu-id="bac43-164">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="bac43-164">Read/write</span></span><br><span data-ttu-id="bac43-165">Optioneel</span><span class="sxs-lookup"><span data-stu-id="bac43-165">Optional</span></span> | <span data-ttu-id="bac43-166">De datum waarop de screening is voltooid.</span><span class="sxs-lookup"><span data-stu-id="bac43-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="bac43-167">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="bac43-167">**Notes**</span></span><br><span data-ttu-id="bac43-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="bac43-168">mshr_note</span></span><br><span data-ttu-id="bac43-169">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="bac43-169">*String*</span></span> | <span data-ttu-id="bac43-170">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="bac43-170">Read/write</span></span><br><span data-ttu-id="bac43-171">Optioneel</span><span class="sxs-lookup"><span data-stu-id="bac43-171">Optional</span></span> | <span data-ttu-id="bac43-172">Notities die worden gebruikt door aanstellende managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="bac43-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bac43-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bac43-173">See also</span></span>

[<span data-ttu-id="bac43-174">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="bac43-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bac43-175">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="bac43-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]