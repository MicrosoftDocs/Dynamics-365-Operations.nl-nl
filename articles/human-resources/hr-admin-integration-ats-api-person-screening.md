---
title: Persoonscreening
description: In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798028"
---
# <a name="person-screening"></a><span data-ttu-id="2c1b2-103">Persoonscreening</span><span class="sxs-lookup"><span data-stu-id="2c1b2-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2c1b2-104">In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="2c1b2-105">Fsyieke naam: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="2c1b2-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="2c1b2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2c1b2-106">Description</span></span>

<span data-ttu-id="2c1b2-107">Deze entiteit beschrijft de screenings waarvoor een kandidaat is geslaagd of moet slagen voor een aanstelling.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2c1b2-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="2c1b2-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="2c1b2-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="2c1b2-109">Properties</span></span>

| <span data-ttu-id="2c1b2-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="2c1b2-110">Property</span></span><br><span data-ttu-id="2c1b2-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-111">**Physical name**</span></span><br><span data-ttu-id="2c1b2-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-112">**_Type_**</span></span> | <span data-ttu-id="2c1b2-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="2c1b2-113">Use</span></span> | <span data-ttu-id="2c1b2-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2c1b2-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2c1b2-115">**Entiteits-id Persoonscreening**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="2c1b2-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="2c1b2-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="2c1b2-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-117">*GUID*</span></span> | <span data-ttu-id="2c1b2-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="2c1b2-118">Read-only</span></span><br><span data-ttu-id="2c1b2-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="2c1b2-119">Required</span></span><br><span data-ttu-id="2c1b2-120">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="2c1b2-120">System-generated</span></span> | <span data-ttu-id="2c1b2-121">Unieke primaire id voor de persoonscreeningrecord.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="2c1b2-122">**Partijnummer**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-122">**Party Number**</span></span><br><span data-ttu-id="2c1b2-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="2c1b2-123">mshr_partynumber</span></span><br><span data-ttu-id="2c1b2-124">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-124">*String*</span></span> | <span data-ttu-id="2c1b2-125">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="2c1b2-125">Read/write</span></span><br><span data-ttu-id="2c1b2-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="2c1b2-126">Required</span></span> | <span data-ttu-id="2c1b2-127">Het partijnummer (persoon) dat aan de kandidaat is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="2c1b2-128">**Waarde persoonlijke id**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-128">**Person ID Value**</span></span><br><span data-ttu-id="2c1b2-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="2c1b2-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="2c1b2-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-130">*GUID*</span></span> | <span data-ttu-id="2c1b2-131">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="2c1b2-131">Read-only</span></span><br><span data-ttu-id="2c1b2-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="2c1b2-132">Required</span></span><br><span data-ttu-id="2c1b2-133">Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="2c1b2-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="2c1b2-134">De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon).</span><span class="sxs-lookup"><span data-stu-id="2c1b2-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="2c1b2-135">**Screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-135">**Screening Type ID**</span></span><br><span data-ttu-id="2c1b2-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="2c1b2-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="2c1b2-137">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-137">*String*</span></span> | <span data-ttu-id="2c1b2-138">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="2c1b2-138">Read/write</span></span><br><span data-ttu-id="2c1b2-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="2c1b2-139">Required</span></span><br><span data-ttu-id="2c1b2-140">Refererende sleutel: Screeningtype</span><span class="sxs-lookup"><span data-stu-id="2c1b2-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="2c1b2-141">De id van het screeningtype dat is gedefinieerd in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="2c1b2-142">**Waarde screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="2c1b2-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="2c1b2-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="2c1b2-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-144">*GUID*</span></span> | <span data-ttu-id="2c1b2-145">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="2c1b2-145">Read-only</span></span><br><span data-ttu-id="2c1b2-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="2c1b2-146">Required</span></span><br><span data-ttu-id="2c1b2-147">Refererende sleutel: mshr_hcmscreeningtypeentityid van mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="2c1b2-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="2c1b2-148">Door het systeem gegenereerde id voor de record van het screeningtype in de gekoppelde entiteit.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="2c1b2-149">**Vereist door**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-149">**Required By**</span></span><br><span data-ttu-id="2c1b2-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="2c1b2-150">mshr_requiredby</span></span><br><span data-ttu-id="2c1b2-151">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-151">*Datetime*</span></span> | <span data-ttu-id="2c1b2-152">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="2c1b2-152">Read/write</span></span><br><span data-ttu-id="2c1b2-153">Optioneel</span><span class="sxs-lookup"><span data-stu-id="2c1b2-153">Optional</span></span> | <span data-ttu-id="2c1b2-154">De datum waarop de screening moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="2c1b2-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-155">**Status**</span></span><br><span data-ttu-id="2c1b2-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="2c1b2-156">mshr_status</span></span><br><span data-ttu-id="2c1b2-157">*mshr_hcmcompletionstatus option set*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="2c1b2-158">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="2c1b2-158">Read/write</span></span><br><span data-ttu-id="2c1b2-159">Vereist</span><span class="sxs-lookup"><span data-stu-id="2c1b2-159">Required</span></span> | <span data-ttu-id="2c1b2-160">De status van de kandidaat voor de screening.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="2c1b2-161">**Datum van voltooiing**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-161">**Completed Date**</span></span><br><span data-ttu-id="2c1b2-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="2c1b2-162">mshr_completeddate</span></span><br><span data-ttu-id="2c1b2-163">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-163">*Datetime*</span></span> | <span data-ttu-id="2c1b2-164">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="2c1b2-164">Read/write</span></span><br><span data-ttu-id="2c1b2-165">Optioneel</span><span class="sxs-lookup"><span data-stu-id="2c1b2-165">Optional</span></span> | <span data-ttu-id="2c1b2-166">De datum waarop de screening is voltooid.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="2c1b2-167">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="2c1b2-167">**Notes**</span></span><br><span data-ttu-id="2c1b2-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="2c1b2-168">mshr_note</span></span><br><span data-ttu-id="2c1b2-169">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="2c1b2-169">*String*</span></span> | <span data-ttu-id="2c1b2-170">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="2c1b2-170">Read/write</span></span><br><span data-ttu-id="2c1b2-171">Optioneel</span><span class="sxs-lookup"><span data-stu-id="2c1b2-171">Optional</span></span> | <span data-ttu-id="2c1b2-172">Notities die worden gebruikt door aanstellende managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="2c1b2-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="2c1b2-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2c1b2-173">See also</span></span>

[<span data-ttu-id="2c1b2-174">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="2c1b2-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="2c1b2-175">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="2c1b2-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]