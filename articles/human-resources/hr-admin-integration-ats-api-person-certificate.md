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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125348"
---
# <a name="person-certificate"></a><span data-ttu-id="63c91-103">Certificaat van persoon</span><span class="sxs-lookup"><span data-stu-id="63c91-103">Person certificate</span></span>

<span data-ttu-id="63c91-104">In dit onderwerp wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="63c91-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="63c91-105">Fysieke naam: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="63c91-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="63c91-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="63c91-106">Description</span></span>

<span data-ttu-id="63c91-107">Deze entiteit beschrijft de professionele certificaten van een kandidaat.</span><span class="sxs-lookup"><span data-stu-id="63c91-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="63c91-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="63c91-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="63c91-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="63c91-109">Properties</span></span>

| <span data-ttu-id="63c91-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="63c91-110">Property</span></span><br><span data-ttu-id="63c91-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="63c91-111">**Physical name**</span></span><br><span data-ttu-id="63c91-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="63c91-112">**_Type_**</span></span> | <span data-ttu-id="63c91-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="63c91-113">Use</span></span> | <span data-ttu-id="63c91-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="63c91-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="63c91-115">**Entiteits-id Certificaat van persoon**</span><span class="sxs-lookup"><span data-stu-id="63c91-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="63c91-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="63c91-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="63c91-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="63c91-117">*GUID*</span></span> | <span data-ttu-id="63c91-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="63c91-118">Read-only</span></span><br><span data-ttu-id="63c91-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-119">Required</span></span> | <span data-ttu-id="63c91-120">Door het systeem gegenereerde unieke id voor de entiteitsrecord van het certificaat van de persoon.</span><span class="sxs-lookup"><span data-stu-id="63c91-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="63c91-121">**Partijnummer**</span><span class="sxs-lookup"><span data-stu-id="63c91-121">**Party Number**</span></span><br><span data-ttu-id="63c91-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="63c91-122">mshr_partynumber</span></span><br><span data-ttu-id="63c91-123">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="63c91-123">*String*</span></span> | <span data-ttu-id="63c91-124">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="63c91-124">Read/write</span></span><br><span data-ttu-id="63c91-125">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-125">Required</span></span> | <span data-ttu-id="63c91-126">De partij-id (persoon) van de kandidaat.</span><span class="sxs-lookup"><span data-stu-id="63c91-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="63c91-127">**Waarde persoonlijke id**</span><span class="sxs-lookup"><span data-stu-id="63c91-127">**Person ID Value**</span></span><br><span data-ttu-id="63c91-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="63c91-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="63c91-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="63c91-129">*GUID*</span></span> | <span data-ttu-id="63c91-130">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="63c91-130">Read-only</span></span><br><span data-ttu-id="63c91-131">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-131">Required</span></span><br><span data-ttu-id="63c91-132">Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="63c91-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="63c91-133">De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon).</span><span class="sxs-lookup"><span data-stu-id="63c91-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="63c91-134">**Certificaattype-id**</span><span class="sxs-lookup"><span data-stu-id="63c91-134">**Certificate Type ID**</span></span><br><span data-ttu-id="63c91-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="63c91-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="63c91-136">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="63c91-136">*String*</span></span> | <span data-ttu-id="63c91-137">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="63c91-137">Read/write</span></span><br><span data-ttu-id="63c91-138">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-138">Required</span></span> |  <span data-ttu-id="63c91-139">De id van het certificaattype dat is gedefinieerd in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63c91-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="63c91-140">**Waarde certificaattype-id**</span><span class="sxs-lookup"><span data-stu-id="63c91-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="63c91-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="63c91-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="63c91-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="63c91-142">*GUID*</span></span> | <span data-ttu-id="63c91-143">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="63c91-143">Read-only</span></span><br><span data-ttu-id="63c91-144">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-144">Required</span></span><br><span data-ttu-id="63c91-145">Refererende sleutel: mshr_hcmcertificatetypeentityid van mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="63c91-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="63c91-146">Door het systeem gegenereerde unieke id voor het certificaattype in de gekoppelde entiteit.</span><span class="sxs-lookup"><span data-stu-id="63c91-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="63c91-147">**Begindatum**</span><span class="sxs-lookup"><span data-stu-id="63c91-147">**Start Date**</span></span><br><span data-ttu-id="63c91-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="63c91-148">mshr_startdate</span></span><br><span data-ttu-id="63c91-149">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="63c91-149">*Datetime*</span></span> | <span data-ttu-id="63c91-150">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="63c91-150">Read/write</span></span><br><span data-ttu-id="63c91-151">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-151">Required</span></span> | <span data-ttu-id="63c91-152">De datum waarop het certificaat is uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="63c91-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="63c91-153">**Einddatum**</span><span class="sxs-lookup"><span data-stu-id="63c91-153">**End Date**</span></span><br><span data-ttu-id="63c91-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="63c91-154">mshr_enddate</span></span><br><span data-ttu-id="63c91-155">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="63c91-155">*Datetime*</span></span> | <span data-ttu-id="63c91-156">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="63c91-156">Read/write</span></span><br><span data-ttu-id="63c91-157">Optioneel</span><span class="sxs-lookup"><span data-stu-id="63c91-157">Optional</span></span> | <span data-ttu-id="63c91-158">De datum waarop het certificaat afloopt.</span><span class="sxs-lookup"><span data-stu-id="63c91-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="63c91-159">**Opmerkingen**</span><span class="sxs-lookup"><span data-stu-id="63c91-159">**Notes**</span></span><br><span data-ttu-id="63c91-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="63c91-160">mshr_notes</span></span><br><span data-ttu-id="63c91-161">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="63c91-161">*String*</span></span> | <span data-ttu-id="63c91-162">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="63c91-162">Read/write</span></span><br><span data-ttu-id="63c91-163">Optioneel</span><span class="sxs-lookup"><span data-stu-id="63c91-163">Optional</span></span> | <span data-ttu-id="63c91-164">Notities die worden gebruikt door aanstellende managers en wervers.</span><span class="sxs-lookup"><span data-stu-id="63c91-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="63c91-165">**Primair veld**</span><span class="sxs-lookup"><span data-stu-id="63c91-165">**Primary Field**</span></span><br><span data-ttu-id="63c91-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="63c91-166">mshr_primaryfield</span></span><br><span data-ttu-id="63c91-167">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="63c91-167">*String*</span></span> | <span data-ttu-id="63c91-168">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="63c91-168">Read-only</span></span><br><span data-ttu-id="63c91-169">Vereist</span><span class="sxs-lookup"><span data-stu-id="63c91-169">Required</span></span> |  <span data-ttu-id="63c91-170">Het veld dat moet worden gebruikt als id van de entiteitsrecord.</span><span class="sxs-lookup"><span data-stu-id="63c91-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="63c91-171">Combinatie van partijnummer, certificaattype-id en begindatum.</span><span class="sxs-lookup"><span data-stu-id="63c91-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="63c91-172">Zie ook</span><span class="sxs-lookup"><span data-stu-id="63c91-172">See also</span></span>

[<span data-ttu-id="63c91-173">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="63c91-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="63c91-174">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="63c91-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

