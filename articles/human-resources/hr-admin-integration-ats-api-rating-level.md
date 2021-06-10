---
title: Beoordelingsniveau
description: In dit onderwerp wordt de entiteit Beoordelingsniveau voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054831"
---
# <a name="rating-level"></a><span data-ttu-id="c2809-103">Beoordelingsniveau</span><span class="sxs-lookup"><span data-stu-id="c2809-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c2809-104">In dit onderwerp wordt de entiteit Beoordelingsniveau voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="c2809-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c2809-105">Fysieke naam: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="c2809-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="c2809-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c2809-106">Description</span></span>

<span data-ttu-id="c2809-107">Deze entiteit voorziet in de beschikbare beoordelingsniveaus voor vaardigheden.</span><span class="sxs-lookup"><span data-stu-id="c2809-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="c2809-108">Beoordelingsniveaus gelden voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="c2809-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c2809-109">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="c2809-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="c2809-110">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="c2809-110">Properties</span></span>

| <span data-ttu-id="c2809-111">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="c2809-111">Property</span></span><br><span data-ttu-id="c2809-112">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="c2809-112">**Physical name**</span></span><br><span data-ttu-id="c2809-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="c2809-113">**_Type_**</span></span> | <span data-ttu-id="c2809-114">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="c2809-114">Use</span></span> | <span data-ttu-id="c2809-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c2809-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c2809-116">**Entiteits-id Beoordelingsniveau**</span><span class="sxs-lookup"><span data-stu-id="c2809-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="c2809-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="c2809-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="c2809-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c2809-118">*GUID*</span></span> | <span data-ttu-id="c2809-119">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c2809-119">Read-only</span></span><br><span data-ttu-id="c2809-120">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-120">Required</span></span><br><span data-ttu-id="c2809-121">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="c2809-121">System-generated</span></span> | <span data-ttu-id="c2809-122">De door het systeem gegenereerde unieke id voor het niveau.</span><span class="sxs-lookup"><span data-stu-id="c2809-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="c2809-123">**Beoordelingsniveau-id**</span><span class="sxs-lookup"><span data-stu-id="c2809-123">**Rating Level ID**</span></span><br><span data-ttu-id="c2809-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="c2809-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="c2809-125">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2809-125">*String*</span></span> | <span data-ttu-id="c2809-126">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="c2809-126">Read/write</span></span><br><span data-ttu-id="c2809-127">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-127">Required</span></span> | <span data-ttu-id="c2809-128">Door de gebruiker leesbare unieke id voor het niveau.</span><span class="sxs-lookup"><span data-stu-id="c2809-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="c2809-129">**Beoordelingsmodel-id**</span><span class="sxs-lookup"><span data-stu-id="c2809-129">**Rating Model ID**</span></span><br><span data-ttu-id="c2809-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="c2809-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="c2809-131">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2809-131">*String*</span></span> | <span data-ttu-id="c2809-132">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="c2809-132">Read/write</span></span><br><span data-ttu-id="c2809-133">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-133">Required</span></span> | <span data-ttu-id="c2809-134">Het beoordelingsmodel waarbij het beoordelingsniveau hoort.</span><span class="sxs-lookup"><span data-stu-id="c2809-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="c2809-135">**Entiteits-id Beoordelingsmodel**</span><span class="sxs-lookup"><span data-stu-id="c2809-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="c2809-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="c2809-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="c2809-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c2809-137">*GUID*</span></span> | <span data-ttu-id="c2809-138">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c2809-138">Read-only</span></span><br><span data-ttu-id="c2809-139">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-139">Required</span></span><br><span data-ttu-id="c2809-140">Refererende sleutel: mshr_hcmratingmodelentityid van mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="c2809-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="c2809-141">De door het systeem gegenereerde id voor het beoordelingsmodel waarbij het beoordelingsniveau hoort.</span><span class="sxs-lookup"><span data-stu-id="c2809-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="c2809-142">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="c2809-142">**Description**</span></span><br><span data-ttu-id="c2809-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="c2809-143">mshr_description</span></span><br><span data-ttu-id="c2809-144">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2809-144">*String*</span></span> | <span data-ttu-id="c2809-145">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="c2809-145">Read/write</span></span><br><span data-ttu-id="c2809-146">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-146">Required</span></span> | <span data-ttu-id="c2809-147">De omschrijving van het beoordelingsniveau.</span><span class="sxs-lookup"><span data-stu-id="c2809-147">The description of the rating level.</span></span> |
| <span data-ttu-id="c2809-148">**Factor**</span><span class="sxs-lookup"><span data-stu-id="c2809-148">**Factor**</span></span><br><span data-ttu-id="c2809-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="c2809-149">mshr_factor</span></span><br><span data-ttu-id="c2809-150">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="c2809-150">*Integer*</span></span> | <span data-ttu-id="c2809-151">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="c2809-151">Read/write</span></span><br><span data-ttu-id="c2809-152">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-152">Required</span></span> | <span data-ttu-id="c2809-153">De factor in voor het beoordelingsniveau.</span><span class="sxs-lookup"><span data-stu-id="c2809-153">The factor for the rating level.</span></span> <span data-ttu-id="c2809-154">Wanneer u items vergelijkt met een ander aantal beoordelingsniveaus, wordt deze factor gebruikt om de scores te standaardiseren.</span><span class="sxs-lookup"><span data-stu-id="c2809-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="c2809-155">De waarde moet een geheel getal tussen 0 en 9 zijn.</span><span class="sxs-lookup"><span data-stu-id="c2809-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="c2809-156">**Opmerking**</span><span class="sxs-lookup"><span data-stu-id="c2809-156">**Note**</span></span><br><span data-ttu-id="c2809-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="c2809-157">mshr_note</span></span><br><span data-ttu-id="c2809-158">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2809-158">*String*</span></span> | <span data-ttu-id="c2809-159">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="c2809-159">Read/write</span></span><br><span data-ttu-id="c2809-160">Optioneel</span><span class="sxs-lookup"><span data-stu-id="c2809-160">Optional</span></span> | <span data-ttu-id="c2809-161">Eventuele notities die zijn gekoppeld aan het beoordelingsniveau.</span><span class="sxs-lookup"><span data-stu-id="c2809-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="c2809-162">**Primair veld**</span><span class="sxs-lookup"><span data-stu-id="c2809-162">**Primary Field**</span></span><br><span data-ttu-id="c2809-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="c2809-163">mshr_primaryfield</span></span><br><span data-ttu-id="c2809-164">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="c2809-164">*String*</span></span> | <span data-ttu-id="c2809-165">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="c2809-165">Read-only</span></span><br><span data-ttu-id="c2809-166">Vereist</span><span class="sxs-lookup"><span data-stu-id="c2809-166">Required</span></span> | <span data-ttu-id="c2809-167">Het veld dat moet worden gebruikt als id van de entiteitsrecord.</span><span class="sxs-lookup"><span data-stu-id="c2809-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="c2809-168">Combinatie van beoordelingsniveau-id en beoordelingsmodel-id.</span><span class="sxs-lookup"><span data-stu-id="c2809-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c2809-169">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c2809-169">See also</span></span>

[<span data-ttu-id="c2809-170">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="c2809-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c2809-171">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="c2809-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]