---
title: Type certificaat
description: In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054687"
---
# <a name="certificate-type"></a><span data-ttu-id="49a54-103">Type certificaat</span><span class="sxs-lookup"><span data-stu-id="49a54-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="49a54-104">In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="49a54-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="49a54-105">Fysieke naam: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="49a54-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="49a54-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="49a54-106">Description</span></span>

<span data-ttu-id="49a54-107">Deze entiteit definieert de lijst met typen professionele certificaten die in Human Resources zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="49a54-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="49a54-108">De entiteit is niet specifiek voor een rechtspersoon (bedrijf).</span><span class="sxs-lookup"><span data-stu-id="49a54-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="49a54-109">JSON-weergave</span><span class="sxs-lookup"><span data-stu-id="49a54-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="49a54-110">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="49a54-110">Properties</span></span>

| <span data-ttu-id="49a54-111">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="49a54-111">Property</span></span><br><span data-ttu-id="49a54-112">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="49a54-112">**Physical name**</span></span><br><span data-ttu-id="49a54-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="49a54-113">**_Type_**</span></span> | <span data-ttu-id="49a54-114">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="49a54-114">Use</span></span> | <span data-ttu-id="49a54-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="49a54-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="49a54-116">**Entiteits-id Type certificaat**</span><span class="sxs-lookup"><span data-stu-id="49a54-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="49a54-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="49a54-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="49a54-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="49a54-118">*GUID*</span></span> | <span data-ttu-id="49a54-119">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="49a54-119">Read-only</span></span><br><span data-ttu-id="49a54-120">Vereist</span><span class="sxs-lookup"><span data-stu-id="49a54-120">Required</span></span> 
<span data-ttu-id="49a54-121">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="49a54-121">System-generated</span></span> | <span data-ttu-id="49a54-122">Unieke primaire id voor het certificaattype.</span><span class="sxs-lookup"><span data-stu-id="49a54-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="49a54-123">**Type certificaat**</span><span class="sxs-lookup"><span data-stu-id="49a54-123">**Certificate Type**</span></span><br><span data-ttu-id="49a54-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="49a54-124">mshr_certificatetype</span></span><br><span data-ttu-id="49a54-125">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="49a54-125">*String*</span></span> | <span data-ttu-id="49a54-126">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="49a54-126">Read/write</span></span><br><span data-ttu-id="49a54-127">Vereist</span><span class="sxs-lookup"><span data-stu-id="49a54-127">Required</span></span> | <span data-ttu-id="49a54-128">Unieke door de gebruiker leesbare id voor het certificaattype.</span><span class="sxs-lookup"><span data-stu-id="49a54-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="49a54-129">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="49a54-129">**Description**</span></span><br><span data-ttu-id="49a54-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="49a54-130">mshr_description</span></span><br><span data-ttu-id="49a54-131">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="49a54-131">*String*</span></span> | <span data-ttu-id="49a54-132">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="49a54-132">Read/write</span></span><br><span data-ttu-id="49a54-133">Vereist</span><span class="sxs-lookup"><span data-stu-id="49a54-133">Required</span></span> | <span data-ttu-id="49a54-134">Omschrijving van het certificaattype.</span><span class="sxs-lookup"><span data-stu-id="49a54-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="49a54-135">**Verlenging vereisen**</span><span class="sxs-lookup"><span data-stu-id="49a54-135">**Require Renewal**</span></span><br><span data-ttu-id="49a54-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="49a54-136">mshr_requirerenewal</span></span><br><span data-ttu-id="49a54-137">*mshr_noyes optieset*</span><span class="sxs-lookup"><span data-stu-id="49a54-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="49a54-138">Lezen/schrijven</span><span class="sxs-lookup"><span data-stu-id="49a54-138">Read/write</span></span><br><span data-ttu-id="49a54-139">Optioneel</span><span class="sxs-lookup"><span data-stu-id="49a54-139">Optional</span></span> | <span data-ttu-id="49a54-140">Geeft aan of verlenging is vereist voor het certificaat.</span><span class="sxs-lookup"><span data-stu-id="49a54-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="49a54-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="49a54-141">See also</span></span>

[<span data-ttu-id="49a54-142">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="49a54-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="49a54-143">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="49a54-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]