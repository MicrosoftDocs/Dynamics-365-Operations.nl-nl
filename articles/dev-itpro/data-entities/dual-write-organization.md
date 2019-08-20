---
title: Organisatiehiërarchie in Common Data Service
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen Finance and Operations en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789173"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="ca299-103">Organisatiehiërarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ca299-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="ca299-104">Omdat Microsoft Dynamics 365 for Finance and Operations een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ca299-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="ca299-105">Bedrijfsfinanciën en -bewerkingen kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ca299-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="ca299-106">Hoewel Common Data Service het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst.</span><span class="sxs-lookup"><span data-stu-id="ca299-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="ca299-107">Als onderdeel van de Common Data Service-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ca299-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="ca299-108">Gegevensstroom</span><span class="sxs-lookup"><span data-stu-id="ca299-108">Data flow</span></span>

<span data-ttu-id="ca299-109">Een bedrijfsecosysteem dat bestaat uit Finance and Operations en Common Data Service blijft een organisatiehiërarchie houden.</span><span class="sxs-lookup"><span data-stu-id="ca299-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="ca299-110">Deze organisatiehiërarchie is gebaseerd op Finance and Operations, maar is in Common Data Service beschikbaar voor informatieve en uitbreidbare doeleinden.</span><span class="sxs-lookup"><span data-stu-id="ca299-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="ca299-111">In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Common Data Service worden weergegeven als een eenrichtingsgegevensstroom van Finance and Operations naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ca299-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Afbeelding van architectuur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="ca299-113">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="ca299-113">Templates</span></span>

<span data-ttu-id="ca299-114">Entiteitstoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ca299-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="ca299-115">Doel van interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ca299-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="ca299-116">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Doel van organisatiehiërarchie van Finance and Operations naar Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ca299-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="ca299-117">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ca299-117">Source field</span></span> | <span data-ttu-id="ca299-118">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ca299-118">Map type</span></span> | <span data-ttu-id="ca299-119">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ca299-119">Destination field</span></span>
---|---|---
<span data-ttu-id="ca299-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ca299-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ca299-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="ca299-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="ca299-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ca299-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ca299-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ca299-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="ca299-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="ca299-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="ca299-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="ca299-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="ca299-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="ca299-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="ca299-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="ca299-127">msdyn\_immutable</span></span>
<span data-ttu-id="ca299-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="ca299-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="ca299-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="ca299-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="ca299-130">Type interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ca299-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="ca299-131">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Type organisatiehiërarchie van Finance and Operations naar Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ca299-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="ca299-132">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ca299-132">Source field</span></span> | <span data-ttu-id="ca299-133">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ca299-133">Map type</span></span> | <span data-ttu-id="ca299-134">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ca299-134">Destination field</span></span>
---|---|---
<span data-ttu-id="ca299-135">NAAM</span><span class="sxs-lookup"><span data-stu-id="ca299-135">NAME</span></span> | \> | <span data-ttu-id="ca299-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ca299-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="ca299-137">Interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ca299-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="ca299-138">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Gepubliceerde organisatiehiërarchie van Finance and Operations naar Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ca299-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="ca299-139">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ca299-139">Source field</span></span> | <span data-ttu-id="ca299-140">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ca299-140">Map type</span></span> | <span data-ttu-id="ca299-141">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ca299-141">Destination field</span></span>
---|---|---
<span data-ttu-id="ca299-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="ca299-142">VALIDTO</span></span> | \> | <span data-ttu-id="ca299-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="ca299-143">msdyn\_validto</span></span>
<span data-ttu-id="ca299-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="ca299-144">VALIDFROM</span></span> | \> | <span data-ttu-id="ca299-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="ca299-145">msdyn\_validfrom</span></span>
<span data-ttu-id="ca299-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ca299-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ca299-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="ca299-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="ca299-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ca299-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ca299-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="ca299-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="ca299-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ca299-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ca299-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="ca299-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="ca299-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ca299-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ca299-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ca299-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="ca299-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ca299-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ca299-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ca299-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="ca299-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ca299-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ca299-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ca299-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="ca299-158">Interne organisatie</span><span class="sxs-lookup"><span data-stu-id="ca299-158">Internal Organization</span></span>

<span data-ttu-id="ca299-159">Gegevens over de interne organisatie in Common Data Service zijn afkomstig van twee Finance and Operations-entiteiten, **operationele eenheid** en **rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="ca299-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="ca299-160">Operationele eenheid</span><span class="sxs-lookup"><span data-stu-id="ca299-160">Operating unit</span></span>

<span data-ttu-id="ca299-161">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ca299-161">Source field</span></span> | <span data-ttu-id="ca299-162">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ca299-162">Map type</span></span> | <span data-ttu-id="ca299-163">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ca299-163">Destination field</span></span>
---|---|---
<span data-ttu-id="ca299-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="ca299-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="ca299-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="ca299-165">msdyn\_languageid</span></span>
<span data-ttu-id="ca299-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="ca299-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="ca299-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="ca299-167">msdyn\_namealias</span></span>
<span data-ttu-id="ca299-168">NAAM</span><span class="sxs-lookup"><span data-stu-id="ca299-168">NAME</span></span> | \> | <span data-ttu-id="ca299-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ca299-169">msdyn\_name</span></span>
<span data-ttu-id="ca299-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ca299-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="ca299-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ca299-171">msdyn\_partynumber</span></span>
<span data-ttu-id="ca299-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="ca299-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="ca299-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="ca299-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="ca299-174">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="ca299-174">Legal entity</span></span>

<span data-ttu-id="ca299-175">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ca299-175">Source field</span></span> | <span data-ttu-id="ca299-176">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ca299-176">Map type</span></span> | <span data-ttu-id="ca299-177">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ca299-177">Destination field</span></span>
---|---|---
<span data-ttu-id="ca299-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="ca299-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="ca299-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="ca299-179">msdyn\_namealias</span></span>
<span data-ttu-id="ca299-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="ca299-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="ca299-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="ca299-181">msdyn\_languageid</span></span>
<span data-ttu-id="ca299-182">NAAM</span><span class="sxs-lookup"><span data-stu-id="ca299-182">NAME</span></span> | \> | <span data-ttu-id="ca299-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ca299-183">msdyn\_name</span></span>
<span data-ttu-id="ca299-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ca299-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="ca299-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ca299-185">msdyn\_partynumber</span></span>
<span data-ttu-id="ca299-186">geen</span><span class="sxs-lookup"><span data-stu-id="ca299-186">none</span></span> | \>\> | <span data-ttu-id="ca299-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="ca299-187">msdyn\_type</span></span>
<span data-ttu-id="ca299-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="ca299-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="ca299-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="ca299-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="ca299-190">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="ca299-190">Company</span></span>

<span data-ttu-id="ca299-191">Biedt bidirectionele synchronisatie van rechtspersoonsgegevens (bedrijfsgegevens) tussen Finance and Operations en Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ca299-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="ca299-192">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ca299-192">Source field</span></span> | <span data-ttu-id="ca299-193">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ca299-193">Map type</span></span> | <span data-ttu-id="ca299-194">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ca299-194">Destination field</span></span>
---|---|---
<span data-ttu-id="ca299-195">NAAM</span><span class="sxs-lookup"><span data-stu-id="ca299-195">NAME</span></span> | = | <span data-ttu-id="ca299-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="ca299-196">cdm\_name</span></span>
<span data-ttu-id="ca299-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="ca299-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="ca299-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="ca299-198">cdm\_companycode</span></span>
