---
title: Certificaat van persoon
description: In dit onderwerp wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466515"
---
# <a name="person-certificate"></a><span data-ttu-id="40b61-103">Certificaat van persoon</span><span class="sxs-lookup"><span data-stu-id="40b61-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="40b61-104">In dit onderwerp wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="40b61-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="40b61-105">Fysieke naam: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="40b61-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="40b61-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="40b61-106">Description</span></span>

<span data-ttu-id="40b61-107">Deze entiteit beschrijft de professionele certificaten van een kandidaat.</span><span class="sxs-lookup"><span data-stu-id="40b61-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="40b61-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="40b61-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="40b61-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="40b61-109">Properties</span></span>

| <span data-ttu-id="40b61-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="40b61-110">Property</span></span><br><span data-ttu-id="40b61-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="40b61-111">**Physical name**</span></span><br><span data-ttu-id="40b61-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="40b61-112">**_Type_**</span></span> | <span data-ttu-id="40b61-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="40b61-113">Use</span></span> | <span data-ttu-id="40b61-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="40b61-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="40b61-115">**Entiteits-id Certificaat van persoon**</span><span class="sxs-lookup"><span data-stu-id="40b61-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="40b61-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="40b61-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="40b61-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="40b61-117">*GUID*</span></span> | <span data-ttu-id="40b61-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="40b61-118">Read-only</span></span><br><span data-ttu-id="40b61-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-119">Required</span></span> | <span data-ttu-id="40b61-120">Door het systeem gegenereerde unieke id voor de entiteitsrecord van het certificaat van de persoon.</span><span class="sxs-lookup"><span data-stu-id="40b61-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="40b61-121">**Partijnummer**</span><span class="sxs-lookup"><span data-stu-id="40b61-121">**Party Number**</span></span><br><span data-ttu-id="40b61-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="40b61-122">mshr_partynumber</span></span><br><span data-ttu-id="40b61-123">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40b61-123">*String*</span></span> | <span data-ttu-id="40b61-124">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="40b61-124">Read/write</span></span><br><span data-ttu-id="40b61-125">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-125">Required</span></span> | <span data-ttu-id="40b61-126">De partij-id (persoon) van de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="40b61-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="40b61-127">**Waarde persoonlijke id**</span><span class="sxs-lookup"><span data-stu-id="40b61-127">**Person ID Value**</span></span><br><span data-ttu-id="40b61-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="40b61-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="40b61-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="40b61-129">*GUID*</span></span> | <span data-ttu-id="40b61-130">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="40b61-130">Read-only</span></span><br><span data-ttu-id="40b61-131">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-131">Required</span></span><br><span data-ttu-id="40b61-132">Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="40b61-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="40b61-133">De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon).</span><span class="sxs-lookup"><span data-stu-id="40b61-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="40b61-134">**Certificaattype-id**</span><span class="sxs-lookup"><span data-stu-id="40b61-134">**Certificate Type ID**</span></span><br><span data-ttu-id="40b61-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="40b61-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="40b61-136">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40b61-136">*String*</span></span> | <span data-ttu-id="40b61-137">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="40b61-137">Read/write</span></span><br><span data-ttu-id="40b61-138">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-138">Required</span></span> |  <span data-ttu-id="40b61-139">De id van het certificaattype dat is gedefinieerd in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="40b61-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="40b61-140">**Waarde certificaattype-id**</span><span class="sxs-lookup"><span data-stu-id="40b61-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="40b61-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="40b61-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="40b61-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="40b61-142">*GUID*</span></span> | <span data-ttu-id="40b61-143">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="40b61-143">Read-only</span></span><br><span data-ttu-id="40b61-144">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-144">Required</span></span><br><span data-ttu-id="40b61-145">Refererende sleutel: mshr_hcmcertificatetypeentityid van mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="40b61-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="40b61-146">Door het systeem gegenereerde unieke id voor het certificaattype in de gekoppelde entiteit.</span><span class="sxs-lookup"><span data-stu-id="40b61-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="40b61-147">**Begindatum**</span><span class="sxs-lookup"><span data-stu-id="40b61-147">**Start Date**</span></span><br><span data-ttu-id="40b61-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="40b61-148">mshr_startdate</span></span><br><span data-ttu-id="40b61-149">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="40b61-149">*Datetime*</span></span> | <span data-ttu-id="40b61-150">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="40b61-150">Read/write</span></span><br><span data-ttu-id="40b61-151">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-151">Required</span></span> | <span data-ttu-id="40b61-152">De datum waarop het certificaat is uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="40b61-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="40b61-153">**Einddatum**</span><span class="sxs-lookup"><span data-stu-id="40b61-153">**End Date**</span></span><br><span data-ttu-id="40b61-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="40b61-154">mshr_enddate</span></span><br><span data-ttu-id="40b61-155">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="40b61-155">*Datetime*</span></span> | <span data-ttu-id="40b61-156">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="40b61-156">Read/write</span></span><br><span data-ttu-id="40b61-157">Optioneel</span><span class="sxs-lookup"><span data-stu-id="40b61-157">Optional</span></span> | <span data-ttu-id="40b61-158">De datum waarop het certificaat afloopt.</span><span class="sxs-lookup"><span data-stu-id="40b61-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="40b61-159">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="40b61-159">**Notes**</span></span><br><span data-ttu-id="40b61-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="40b61-160">mshr_notes</span></span><br><span data-ttu-id="40b61-161">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40b61-161">*String*</span></span> | <span data-ttu-id="40b61-162">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="40b61-162">Read/write</span></span><br><span data-ttu-id="40b61-163">Optioneel</span><span class="sxs-lookup"><span data-stu-id="40b61-163">Optional</span></span> | <span data-ttu-id="40b61-164">Notities die worden gebruikt door aanstellende managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="40b61-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="40b61-165">**Primair veld**</span><span class="sxs-lookup"><span data-stu-id="40b61-165">**Primary Field**</span></span><br><span data-ttu-id="40b61-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="40b61-166">mshr_primaryfield</span></span><br><span data-ttu-id="40b61-167">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="40b61-167">*String*</span></span> | <span data-ttu-id="40b61-168">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="40b61-168">Read-only</span></span><br><span data-ttu-id="40b61-169">Vereist</span><span class="sxs-lookup"><span data-stu-id="40b61-169">Required</span></span> |  <span data-ttu-id="40b61-170">Het veld dat moet worden gebruikt als id van de entiteitsrecord.</span><span class="sxs-lookup"><span data-stu-id="40b61-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="40b61-171">Combinatie van partijnummer, certificaattype-id en begindatum.</span><span class="sxs-lookup"><span data-stu-id="40b61-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="40b61-172">Zie ook</span><span class="sxs-lookup"><span data-stu-id="40b61-172">See also</span></span>

[<span data-ttu-id="40b61-173">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="40b61-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="40b61-174">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="40b61-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]