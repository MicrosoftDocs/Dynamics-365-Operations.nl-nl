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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126165"
---
# <a name="screening-types"></a><span data-ttu-id="6455e-103">Screeningtypen</span><span class="sxs-lookup"><span data-stu-id="6455e-103">Screening types</span></span>

<span data-ttu-id="6455e-104">In dit onderwerp wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="6455e-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6455e-105">Fysieke naam: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="6455e-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="6455e-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6455e-106">Description</span></span>

<span data-ttu-id="6455e-107">Deze entiteit beschrijft de screeningtypen die door het bedrijf zijn ingesteld voor lopende screeningprocessen en screeningprocessen voorafgaand aan een dienstverband voor werknemers.</span><span class="sxs-lookup"><span data-stu-id="6455e-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6455e-108">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="6455e-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="6455e-109">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="6455e-109">Properties</span></span>

| <span data-ttu-id="6455e-110">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="6455e-110">Property</span></span><br><span data-ttu-id="6455e-111">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="6455e-111">**Physical name**</span></span><br><span data-ttu-id="6455e-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="6455e-112">**_Type_**</span></span> | <span data-ttu-id="6455e-113">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="6455e-113">Use</span></span> | <span data-ttu-id="6455e-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6455e-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6455e-115">**Entiteits-id Screeningtype**</span><span class="sxs-lookup"><span data-stu-id="6455e-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="6455e-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="6455e-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="6455e-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6455e-117">*GUID*</span></span> | <span data-ttu-id="6455e-118">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="6455e-118">Read-only</span></span><br><span data-ttu-id="6455e-119">Vereist</span><span class="sxs-lookup"><span data-stu-id="6455e-119">Required</span></span><br><span data-ttu-id="6455e-120">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="6455e-120">System-generated</span></span> | <span data-ttu-id="6455e-121">Unieke primaire id voor de screeningtyperecord.</span><span class="sxs-lookup"><span data-stu-id="6455e-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="6455e-122">**Screeningtype-id**</span><span class="sxs-lookup"><span data-stu-id="6455e-122">**Screening Type ID**</span></span><br><span data-ttu-id="6455e-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="6455e-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="6455e-124">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="6455e-124">*String*</span></span> | <span data-ttu-id="6455e-125">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="6455e-125">Read/write</span></span><br><span data-ttu-id="6455e-126">Vereist</span><span class="sxs-lookup"><span data-stu-id="6455e-126">Required</span></span> | <span data-ttu-id="6455e-127">Door de gebruiker gedefinieerde unieke primaire id voor het screeningtype.</span><span class="sxs-lookup"><span data-stu-id="6455e-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="6455e-128">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="6455e-128">**Description**</span></span><br><span data-ttu-id="6455e-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="6455e-129">mshr_description</span></span><br><span data-ttu-id="6455e-130">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="6455e-130">*String*</span></span> | <span data-ttu-id="6455e-131">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="6455e-131">Read/write</span></span><br><span data-ttu-id="6455e-132">Vereist</span><span class="sxs-lookup"><span data-stu-id="6455e-132">Required</span></span> | <span data-ttu-id="6455e-133">De omschrijving van het screeningtype.</span><span class="sxs-lookup"><span data-stu-id="6455e-133">The description of the screening type.</span></span> |
| <span data-ttu-id="6455e-134">**Frequentie-eenheid**</span><span class="sxs-lookup"><span data-stu-id="6455e-134">**Frequency Unit**</span></span><br><span data-ttu-id="6455e-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="6455e-135">mshr_frequencyunit</span></span><br><span data-ttu-id="6455e-136">*mshr_hcmfrequencyunit optieset*</span><span class="sxs-lookup"><span data-stu-id="6455e-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="6455e-137">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="6455e-137">Read/write</span></span><br><span data-ttu-id="6455e-138">Vereist</span><span class="sxs-lookup"><span data-stu-id="6455e-138">Required</span></span> | <span data-ttu-id="6455e-139">Beschrijft de frequentie waarmee de screening moet worden uitgevoerd voor de toegewezen persoon.</span><span class="sxs-lookup"><span data-stu-id="6455e-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="6455e-140">**Genereren op basis van**</span><span class="sxs-lookup"><span data-stu-id="6455e-140">**Generate From**</span></span><br><span data-ttu-id="6455e-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="6455e-141">mshr_generatefrom</span></span><br><span data-ttu-id="6455e-142">*mshr_hcmfrequencygeneratefrom optieset*</span><span class="sxs-lookup"><span data-stu-id="6455e-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="6455e-143">Lezen-schrijven</span><span class="sxs-lookup"><span data-stu-id="6455e-143">Read-write</span></span><br><span data-ttu-id="6455e-144">Vereist</span><span class="sxs-lookup"><span data-stu-id="6455e-144">Required</span></span> | <span data-ttu-id="6455e-145">Als de frequentiewaarde een andere waarde is dan 'Eenmalig', bepaalt de waarde GenerateFrom de datum waarop de volgende screeninggebeurtenis wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="6455e-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="6455e-146">**Frequentie-interval**</span><span class="sxs-lookup"><span data-stu-id="6455e-146">**Frequency Interval**</span></span><br><span data-ttu-id="6455e-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="6455e-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="6455e-148">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="6455e-148">*Integer*</span></span> | <span data-ttu-id="6455e-149">Lezen-schrijven</span><span class="sxs-lookup"><span data-stu-id="6455e-149">Read-write</span></span><br><span data-ttu-id="6455e-150">Vereist</span><span class="sxs-lookup"><span data-stu-id="6455e-150">Required</span></span> | <span data-ttu-id="6455e-151">Als de waarde Frequentie een andere waarde is dan 'Eenmalig', moet u een interval definiëren voor de tijdseenheden tussen elke screeninggebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="6455e-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6455e-152">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6455e-152">See also</span></span>

[<span data-ttu-id="6455e-153">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="6455e-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="6455e-154">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="6455e-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
