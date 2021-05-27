---
title: Adres medewerker salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Adres medewerker salarisadministratie in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020700"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="3852f-103">Adres medewerker salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="3852f-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3852f-104">Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Adres medewerker salarisadministratie in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3852f-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3852f-105">Eigenschappen</span><span class="sxs-lookup"><span data-stu-id="3852f-105">Properties</span></span>

| <span data-ttu-id="3852f-106">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="3852f-106">Property</span></span><br><span data-ttu-id="3852f-107">**Fysieke naam**</span><span class="sxs-lookup"><span data-stu-id="3852f-107">**Physical name**</span></span><br><span data-ttu-id="3852f-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="3852f-108">**_Type_**</span></span> | <span data-ttu-id="3852f-109">Gebruiken</span><span class="sxs-lookup"><span data-stu-id="3852f-109">Use</span></span> | <span data-ttu-id="3852f-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3852f-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3852f-111">**Plaats**</span><span class="sxs-lookup"><span data-stu-id="3852f-111">**City**</span></span><br><span data-ttu-id="3852f-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="3852f-112">mshr_city</span></span><br><span data-ttu-id="3852f-113">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-113">*String*</span></span> | <span data-ttu-id="3852f-114">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-114">Read-only</span></span><br><span data-ttu-id="3852f-115">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-115">Required</span></span> | <span data-ttu-id="3852f-116">De plaats voor het adres</span><span class="sxs-lookup"><span data-stu-id="3852f-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="3852f-117">**Personeelsnummer**</span><span class="sxs-lookup"><span data-stu-id="3852f-117">**Personnel number**</span></span><br><span data-ttu-id="3852f-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="3852f-118">mshr_personnelnumber</span></span><br><span data-ttu-id="3852f-119">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-119">*String*</span></span> | <span data-ttu-id="3852f-120">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-120">Read-only</span></span><br><span data-ttu-id="3852f-121">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-121">Required</span></span> | <span data-ttu-id="3852f-122">Het unieke personeelsnummer van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="3852f-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="3852f-123">**Land/regio**</span><span class="sxs-lookup"><span data-stu-id="3852f-123">**Country region**</span></span><br><span data-ttu-id="3852f-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="3852f-124">mshr_countryregionid</span></span><br><span data-ttu-id="3852f-125">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-125">*String*</span></span> | <span data-ttu-id="3852f-126">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-126">Read-only</span></span><br><span data-ttu-id="3852f-127">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-127">Required</span></span> | <span data-ttu-id="3852f-128">Het land of de regio voor het adres.</span><span class="sxs-lookup"><span data-stu-id="3852f-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="3852f-129">**Geldig vanaf**</span><span class="sxs-lookup"><span data-stu-id="3852f-129">**Valid from**</span></span><br><span data-ttu-id="3852f-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="3852f-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="3852f-131">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="3852f-131">*Date Time Offset*</span></span> | <span data-ttu-id="3852f-132">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-132">Read-only</span></span> <br><span data-ttu-id="3852f-133">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-133">Required</span></span> | <span data-ttu-id="3852f-134">De datum vanaf wanneer het adres geldig is.</span><span class="sxs-lookup"><span data-stu-id="3852f-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="3852f-135">**Gewerkt op adres**</span><span class="sxs-lookup"><span data-stu-id="3852f-135">**Worked in address**</span></span><br><span data-ttu-id="3852f-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="3852f-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="3852f-137">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-137">Read-only</span></span><br><span data-ttu-id="3852f-138">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-138">Required</span></span> | <span data-ttu-id="3852f-139">Geeft aan of dit het adres is waar de werknemer werkt.</span><span class="sxs-lookup"><span data-stu-id="3852f-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="3852f-140">**Land/regio**</span><span class="sxs-lookup"><span data-stu-id="3852f-140">**County**</span></span><br><span data-ttu-id="3852f-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="3852f-141">mshr_county</span></span><br><span data-ttu-id="3852f-142">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-142">*String*</span></span> | <span data-ttu-id="3852f-143">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-143">Read-only</span></span><br><span data-ttu-id="3852f-144">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-144">Required</span></span> | <span data-ttu-id="3852f-145">De land of de regio voor het adres</span><span class="sxs-lookup"><span data-stu-id="3852f-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="3852f-146">**Id medewerker salarisadministratie**</span><span class="sxs-lookup"><span data-stu-id="3852f-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="3852f-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="3852f-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="3852f-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3852f-148">*GUID*</span></span> | <span data-ttu-id="3852f-149">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-149">Required</span></span><br><span data-ttu-id="3852f-150">Door systeem gegenereerd</span><span class="sxs-lookup"><span data-stu-id="3852f-150">System generated</span></span> | <span data-ttu-id="3852f-151">Een door het systeem gegenereerde GUID-waarde als unieke id van het adres.</span><span class="sxs-lookup"><span data-stu-id="3852f-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="3852f-152">**Primair veld**</span><span class="sxs-lookup"><span data-stu-id="3852f-152">**Primary field**</span></span><br><span data-ttu-id="3852f-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3852f-153">mshr_primaryfield</span></span><br><span data-ttu-id="3852f-154">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-154">*String*</span></span> | <span data-ttu-id="3852f-155">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-155">Read-only</span></span><br><span data-ttu-id="3852f-156">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-156">Required</span></span> |  |
| <span data-ttu-id="3852f-157">**Adres**</span><span class="sxs-lookup"><span data-stu-id="3852f-157">**Street**</span></span><br><span data-ttu-id="3852f-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="3852f-158">mshr_street</span></span><br><span data-ttu-id="3852f-159">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-159">*String*</span></span> | <span data-ttu-id="3852f-160">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-160">Read-only</span></span><br><span data-ttu-id="3852f-161">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-161">Required</span></span> | <span data-ttu-id="3852f-162">De straatnaam voor het adres</span><span class="sxs-lookup"><span data-stu-id="3852f-162">The street defined for the address.</span></span> |
| <span data-ttu-id="3852f-163">**Geldig tot**</span><span class="sxs-lookup"><span data-stu-id="3852f-163">**Valid to**</span></span><br><span data-ttu-id="3852f-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="3852f-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="3852f-165">*Verschil datum en tijd*</span><span class="sxs-lookup"><span data-stu-id="3852f-165">*Date Time Offset*</span></span> | <span data-ttu-id="3852f-166">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-166">Read-only</span></span> <br><span data-ttu-id="3852f-167">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-167">Required</span></span> | <span data-ttu-id="3852f-168">De datum tot wanneer het adres geldig is.</span><span class="sxs-lookup"><span data-stu-id="3852f-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="3852f-169">**Locatie-ID**</span><span class="sxs-lookup"><span data-stu-id="3852f-169">**Location ID**</span></span><br><span data-ttu-id="3852f-170">mshr_locationidbr>*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="3852f-171">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-171">Read-only</span></span> <br><span data-ttu-id="3852f-172">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-172">Required</span></span> | <span data-ttu-id="3852f-173">Het id voor het adres.</span><span class="sxs-lookup"><span data-stu-id="3852f-173">The ID for the address.</span></span>  |
| <span data-ttu-id="3852f-174">**Postcode**</span><span class="sxs-lookup"><span data-stu-id="3852f-174">**Postal code**</span></span><br><span data-ttu-id="3852f-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="3852f-175">mshr_zipcode</span></span><br><span data-ttu-id="3852f-176">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-176">*String*</span></span> | <span data-ttu-id="3852f-177">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-177">Read-only</span></span> <br><span data-ttu-id="3852f-178">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-178">Required</span></span> |<span data-ttu-id="3852f-179">Het identificatienummer dat voor de werknemer is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3852f-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="3852f-180">**Gewoond op adres**</span><span class="sxs-lookup"><span data-stu-id="3852f-180">**Lived in address**</span></span><br><span data-ttu-id="3852f-181">mshr_islivedinaddressbr>*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="3852f-182">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-182">Read-only</span></span><br><span data-ttu-id="3852f-183">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-183">Required</span></span> | <span data-ttu-id="3852f-184">Geeft aan of dit het adres is waar de werknemer woont.</span><span class="sxs-lookup"><span data-stu-id="3852f-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="3852f-185">**Staat/provincie**</span><span class="sxs-lookup"><span data-stu-id="3852f-185">**State**</span></span><br><span data-ttu-id="3852f-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="3852f-186">mshr_state</span></span><br><span data-ttu-id="3852f-187">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3852f-187">*String*</span></span> | <span data-ttu-id="3852f-188">Alleen-lezen</span><span class="sxs-lookup"><span data-stu-id="3852f-188">Read-only</span></span><br><span data-ttu-id="3852f-189">Vereist</span><span class="sxs-lookup"><span data-stu-id="3852f-189">Required</span></span> | <span data-ttu-id="3852f-190">De staat/provincie voor het adres</span><span class="sxs-lookup"><span data-stu-id="3852f-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="3852f-191">Voorbeeldquery</span><span class="sxs-lookup"><span data-stu-id="3852f-191">Example query</span></span>

<span data-ttu-id="3852f-192">**Aanvragen**</span><span class="sxs-lookup"><span data-stu-id="3852f-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="3852f-193">**Respons**</span><span class="sxs-lookup"><span data-stu-id="3852f-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
