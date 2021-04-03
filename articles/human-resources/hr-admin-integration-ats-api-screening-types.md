---
title: Screeningtypen
description: In dit onderwerp wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465913"
---
# <a name="screening-types"></a><span data-ttu-id="3cccf-103">Screeningtypen</span><span class="sxs-lookup"><span data-stu-id="3cccf-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3cccf-104">In dit onderwerp wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="3cccf-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3cccf-105">Fysieke naam: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="3cccf-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="3cccf-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3cccf-106">Description</span></span>

<span data-ttu-id="3cccf-107">Deze entiteit beschrijft de screeningtypen die door het bedrijf zijn ingesteld voor lopende screeningprocessen en screeningprocessen voorafgaand aan een dienstverband voor werknemers.</span><span class="sxs-lookup"><span data-stu-id="3cccf-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3cccf-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="3cccf-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="3cccf-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="3cccf-109">Properties</span></span>

| <span data-ttu-id="3cccf-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="3cccf-110">Property</span></span><br><span data-ttu-id="3cccf-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="3cccf-111">**Physical name**</span></span><br><span data-ttu-id="3cccf-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="3cccf-112">**_Type_**</span></span> | <span data-ttu-id="3cccf-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="3cccf-113">Use</span></span> | <span data-ttu-id="3cccf-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3cccf-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3cccf-115">**Entiteits-id Screeningtype**</span><span class="sxs-lookup"><span data-stu-id="3cccf-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="3cccf-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="3cccf-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="3cccf-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3cccf-117">*GUID*</span></span> | <span data-ttu-id="3cccf-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3cccf-118">Read-only</span></span><br><span data-ttu-id="3cccf-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="3cccf-119">Required</span></span><br><span data-ttu-id="3cccf-120">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="3cccf-120">System-generated</span></span> | <span data-ttu-id="3cccf-121">Unieke primaire id voor de screeningtyperecord.</span><span class="sxs-lookup"><span data-stu-id="3cccf-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="3cccf-122">**Screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="3cccf-122">**Screening Type ID**</span></span><br><span data-ttu-id="3cccf-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="3cccf-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="3cccf-124">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3cccf-124">*String*</span></span> | <span data-ttu-id="3cccf-125">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="3cccf-125">Read/write</span></span><br><span data-ttu-id="3cccf-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="3cccf-126">Required</span></span> | <span data-ttu-id="3cccf-127">Door de gebruiker gedefinieerde unieke primaire id voor het screeningtype.</span><span class="sxs-lookup"><span data-stu-id="3cccf-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="3cccf-128">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="3cccf-128">**Description**</span></span><br><span data-ttu-id="3cccf-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3cccf-129">mshr_description</span></span><br><span data-ttu-id="3cccf-130">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3cccf-130">*String*</span></span> | <span data-ttu-id="3cccf-131">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="3cccf-131">Read/write</span></span><br><span data-ttu-id="3cccf-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="3cccf-132">Required</span></span> | <span data-ttu-id="3cccf-133">De omschrijving van het screeningtype.</span><span class="sxs-lookup"><span data-stu-id="3cccf-133">The description of the screening type.</span></span> |
| <span data-ttu-id="3cccf-134">**Frequentie-eenheid**</span><span class="sxs-lookup"><span data-stu-id="3cccf-134">**Frequency Unit**</span></span><br><span data-ttu-id="3cccf-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="3cccf-135">mshr_frequencyunit</span></span><br><span data-ttu-id="3cccf-136">*mshr_hcmfrequencyunit optieset*</span><span class="sxs-lookup"><span data-stu-id="3cccf-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="3cccf-137">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="3cccf-137">Read/write</span></span><br><span data-ttu-id="3cccf-138">Vereist</span><span class="sxs-lookup"><span data-stu-id="3cccf-138">Required</span></span> | <span data-ttu-id="3cccf-139">Beschrijft de frequentie waarmee de screening moet worden uitgevoerd voor de toegewezen persoon.</span><span class="sxs-lookup"><span data-stu-id="3cccf-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="3cccf-140">**Genereren op basis van**</span><span class="sxs-lookup"><span data-stu-id="3cccf-140">**Generate From**</span></span><br><span data-ttu-id="3cccf-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="3cccf-141">mshr_generatefrom</span></span><br><span data-ttu-id="3cccf-142">*mshr_hcmfrequencygeneratefrom optieset*</span><span class="sxs-lookup"><span data-stu-id="3cccf-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="3cccf-143">Lezen-schrijven</span><span class="sxs-lookup"><span data-stu-id="3cccf-143">Read-write</span></span><br><span data-ttu-id="3cccf-144">Vereist</span><span class="sxs-lookup"><span data-stu-id="3cccf-144">Required</span></span> | <span data-ttu-id="3cccf-145">Als de frequentiewaarde een andere waarde is dan 'Eenmalig', bepaalt de waarde GenerateFrom de datum waarop de volgende screeninggebeurtenis wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="3cccf-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="3cccf-146">**Frequentie-interval**</span><span class="sxs-lookup"><span data-stu-id="3cccf-146">**Frequency Interval**</span></span><br><span data-ttu-id="3cccf-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="3cccf-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="3cccf-148">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="3cccf-148">*Integer*</span></span> | <span data-ttu-id="3cccf-149">Lezen-schrijven</span><span class="sxs-lookup"><span data-stu-id="3cccf-149">Read-write</span></span><br><span data-ttu-id="3cccf-150">Vereist</span><span class="sxs-lookup"><span data-stu-id="3cccf-150">Required</span></span> | <span data-ttu-id="3cccf-151">Als de waarde Frequentie een andere waarde is dan 'Eenmalig', moet u een interval definiëren voor de tijdseenheden tussen elke screeninggebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="3cccf-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3cccf-152">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3cccf-152">See also</span></span>

[<span data-ttu-id="3cccf-153">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="3cccf-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3cccf-154">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="3cccf-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]