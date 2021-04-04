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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467236"
---
# <a name="person-screening"></a><span data-ttu-id="e4a63-103">Persoonscreening</span><span class="sxs-lookup"><span data-stu-id="e4a63-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e4a63-104">In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="e4a63-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e4a63-105">Fsyieke naam: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="e4a63-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="e4a63-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e4a63-106">Description</span></span>

<span data-ttu-id="e4a63-107">Deze entiteit beschrijft de screenings waarvoor een kandidaat is geslaagd of moet slagen voor een aanstelling.</span><span class="sxs-lookup"><span data-stu-id="e4a63-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e4a63-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="e4a63-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="e4a63-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="e4a63-109">Properties</span></span>

| <span data-ttu-id="e4a63-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="e4a63-110">Property</span></span><br><span data-ttu-id="e4a63-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="e4a63-111">**Physical name**</span></span><br><span data-ttu-id="e4a63-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="e4a63-112">**_Type_**</span></span> | <span data-ttu-id="e4a63-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="e4a63-113">Use</span></span> | <span data-ttu-id="e4a63-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e4a63-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e4a63-115">**Entiteits-id Persoonscreening**</span><span class="sxs-lookup"><span data-stu-id="e4a63-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="e4a63-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="e4a63-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="e4a63-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4a63-117">*GUID*</span></span> | <span data-ttu-id="e4a63-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e4a63-118">Read-only</span></span><br><span data-ttu-id="e4a63-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="e4a63-119">Required</span></span><br><span data-ttu-id="e4a63-120">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="e4a63-120">System-generated</span></span> | <span data-ttu-id="e4a63-121">Unieke primaire id voor de persoonscreeningrecord.</span><span class="sxs-lookup"><span data-stu-id="e4a63-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="e4a63-122">**Partijnummer**</span><span class="sxs-lookup"><span data-stu-id="e4a63-122">**Party Number**</span></span><br><span data-ttu-id="e4a63-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="e4a63-123">mshr_partynumber</span></span><br><span data-ttu-id="e4a63-124">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e4a63-124">*String*</span></span> | <span data-ttu-id="e4a63-125">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="e4a63-125">Read/write</span></span><br><span data-ttu-id="e4a63-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="e4a63-126">Required</span></span> | <span data-ttu-id="e4a63-127">Het partijnummer (persoon) dat aan de kandidaat is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e4a63-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="e4a63-128">**Waarde persoonlijke id**</span><span class="sxs-lookup"><span data-stu-id="e4a63-128">**Person ID Value**</span></span><br><span data-ttu-id="e4a63-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="e4a63-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="e4a63-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4a63-130">*GUID*</span></span> | <span data-ttu-id="e4a63-131">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e4a63-131">Read-only</span></span><br><span data-ttu-id="e4a63-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="e4a63-132">Required</span></span><br><span data-ttu-id="e4a63-133">Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="e4a63-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="e4a63-134">De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon).</span><span class="sxs-lookup"><span data-stu-id="e4a63-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="e4a63-135">**Screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="e4a63-135">**Screening Type ID**</span></span><br><span data-ttu-id="e4a63-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="e4a63-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="e4a63-137">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e4a63-137">*String*</span></span> | <span data-ttu-id="e4a63-138">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="e4a63-138">Read/write</span></span><br><span data-ttu-id="e4a63-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="e4a63-139">Required</span></span><br><span data-ttu-id="e4a63-140">Refererende sleutel: Screeningtype</span><span class="sxs-lookup"><span data-stu-id="e4a63-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="e4a63-141">De id van het screeningtype dat is gedefinieerd in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e4a63-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="e4a63-142">**Waarde screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="e4a63-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="e4a63-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="e4a63-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="e4a63-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4a63-144">*GUID*</span></span> | <span data-ttu-id="e4a63-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="e4a63-145">Read-only</span></span><br><span data-ttu-id="e4a63-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="e4a63-146">Required</span></span><br><span data-ttu-id="e4a63-147">Refererende sleutel: mshr_hcmscreeningtypeentityid van mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="e4a63-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="e4a63-148">Door het systeem gegenereerde id voor de record van het screeningtype in de gekoppelde entiteit.</span><span class="sxs-lookup"><span data-stu-id="e4a63-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="e4a63-149">**Vereist door**</span><span class="sxs-lookup"><span data-stu-id="e4a63-149">**Required By**</span></span><br><span data-ttu-id="e4a63-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="e4a63-150">mshr_requiredby</span></span><br><span data-ttu-id="e4a63-151">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="e4a63-151">*Datetime*</span></span> | <span data-ttu-id="e4a63-152">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="e4a63-152">Read/write</span></span><br><span data-ttu-id="e4a63-153">Optioneel</span><span class="sxs-lookup"><span data-stu-id="e4a63-153">Optional</span></span> | <span data-ttu-id="e4a63-154">De datum waarop de screening moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="e4a63-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="e4a63-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="e4a63-155">**Status**</span></span><br><span data-ttu-id="e4a63-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="e4a63-156">mshr_status</span></span><br><span data-ttu-id="e4a63-157">*mshr_hcmcompletionstatus option set*</span><span class="sxs-lookup"><span data-stu-id="e4a63-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="e4a63-158">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="e4a63-158">Read/write</span></span><br><span data-ttu-id="e4a63-159">Vereist</span><span class="sxs-lookup"><span data-stu-id="e4a63-159">Required</span></span> | <span data-ttu-id="e4a63-160">De status van de kandidaat voor de screening.</span><span class="sxs-lookup"><span data-stu-id="e4a63-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="e4a63-161">**Datum van voltooiing**</span><span class="sxs-lookup"><span data-stu-id="e4a63-161">**Completed Date**</span></span><br><span data-ttu-id="e4a63-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="e4a63-162">mshr_completeddate</span></span><br><span data-ttu-id="e4a63-163">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="e4a63-163">*Datetime*</span></span> | <span data-ttu-id="e4a63-164">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="e4a63-164">Read/write</span></span><br><span data-ttu-id="e4a63-165">Optioneel</span><span class="sxs-lookup"><span data-stu-id="e4a63-165">Optional</span></span> | <span data-ttu-id="e4a63-166">De datum waarop de screening is voltooid.</span><span class="sxs-lookup"><span data-stu-id="e4a63-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="e4a63-167">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="e4a63-167">**Notes**</span></span><br><span data-ttu-id="e4a63-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="e4a63-168">mshr_note</span></span><br><span data-ttu-id="e4a63-169">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="e4a63-169">*String*</span></span> | <span data-ttu-id="e4a63-170">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="e4a63-170">Read/write</span></span><br><span data-ttu-id="e4a63-171">Optioneel</span><span class="sxs-lookup"><span data-stu-id="e4a63-171">Optional</span></span> | <span data-ttu-id="e4a63-172">Notities die worden gebruikt door aanstellende managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="e4a63-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4a63-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e4a63-173">See also</span></span>

[<span data-ttu-id="e4a63-174">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="e4a63-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e4a63-175">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="e4a63-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]