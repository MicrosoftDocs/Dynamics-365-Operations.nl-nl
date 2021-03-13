---
title: Type certificaat
description: In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125708"
---
# <a name="certificate-type"></a><span data-ttu-id="98ca8-103">Type certificaat</span><span class="sxs-lookup"><span data-stu-id="98ca8-103">Certificate type</span></span>

<span data-ttu-id="98ca8-104">In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="98ca8-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="98ca8-105">Fysieke naam: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="98ca8-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="98ca8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="98ca8-106">Description</span></span>

<span data-ttu-id="98ca8-107">Deze entiteit definieert de lijst met typen professionele certificaten die in Human Resources zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="98ca8-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="98ca8-108">De entiteit is niet specifiek voor een rechtspersoon (bedrijf).</span><span class="sxs-lookup"><span data-stu-id="98ca8-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="98ca8-109">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="98ca8-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="98ca8-110">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="98ca8-110">Properties</span></span>

| <span data-ttu-id="98ca8-111">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="98ca8-111">Property</span></span><br><span data-ttu-id="98ca8-112">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="98ca8-112">**Physical name**</span></span><br><span data-ttu-id="98ca8-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="98ca8-113">**_Type_**</span></span> | <span data-ttu-id="98ca8-114">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="98ca8-114">Use</span></span> | <span data-ttu-id="98ca8-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="98ca8-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="98ca8-116">**Entiteits-id Type certificaat**</span><span class="sxs-lookup"><span data-stu-id="98ca8-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="98ca8-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="98ca8-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="98ca8-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="98ca8-118">*GUID*</span></span> | <span data-ttu-id="98ca8-119">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="98ca8-119">Read-only</span></span><br><span data-ttu-id="98ca8-120">Vereist</span><span class="sxs-lookup"><span data-stu-id="98ca8-120">Required</span></span> 
<span data-ttu-id="98ca8-121">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="98ca8-121">System-generated</span></span> | <span data-ttu-id="98ca8-122">Unieke primaire id voor het certificaattype.</span><span class="sxs-lookup"><span data-stu-id="98ca8-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="98ca8-123">**Type certificaat**</span><span class="sxs-lookup"><span data-stu-id="98ca8-123">**Certificate Type**</span></span><br><span data-ttu-id="98ca8-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="98ca8-124">mshr_certificatetype</span></span><br><span data-ttu-id="98ca8-125">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="98ca8-125">*String*</span></span> | <span data-ttu-id="98ca8-126">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="98ca8-126">Read/write</span></span><br><span data-ttu-id="98ca8-127">Vereist</span><span class="sxs-lookup"><span data-stu-id="98ca8-127">Required</span></span> | <span data-ttu-id="98ca8-128">Unieke door de gebruiker leesbare id voor het certificaattype.</span><span class="sxs-lookup"><span data-stu-id="98ca8-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="98ca8-129">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="98ca8-129">**Description**</span></span><br><span data-ttu-id="98ca8-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="98ca8-130">mshr_description</span></span><br><span data-ttu-id="98ca8-131">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="98ca8-131">*String*</span></span> | <span data-ttu-id="98ca8-132">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="98ca8-132">Read/write</span></span><br><span data-ttu-id="98ca8-133">Vereist</span><span class="sxs-lookup"><span data-stu-id="98ca8-133">Required</span></span> | <span data-ttu-id="98ca8-134">Omschrijving van het certificaattype.</span><span class="sxs-lookup"><span data-stu-id="98ca8-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="98ca8-135">**Verlenging vereisen**</span><span class="sxs-lookup"><span data-stu-id="98ca8-135">**Require Renewal**</span></span><br><span data-ttu-id="98ca8-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="98ca8-136">mshr_requirerenewal</span></span><br><span data-ttu-id="98ca8-137">*mshr_noyes optieset*</span><span class="sxs-lookup"><span data-stu-id="98ca8-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="98ca8-138">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="98ca8-138">Read/write</span></span><br><span data-ttu-id="98ca8-139">Optioneel</span><span class="sxs-lookup"><span data-stu-id="98ca8-139">Optional</span></span> | <span data-ttu-id="98ca8-140">Geeft aan of verlenging is vereist voor het certificaat.</span><span class="sxs-lookup"><span data-stu-id="98ca8-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="98ca8-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="98ca8-141">See also</span></span>

[<span data-ttu-id="98ca8-142">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="98ca8-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="98ca8-143">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="98ca8-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

