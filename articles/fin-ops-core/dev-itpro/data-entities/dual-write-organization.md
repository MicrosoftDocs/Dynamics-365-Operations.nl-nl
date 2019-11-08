---
title: Organisatiehiërarchie in Common Data Service
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen Finance and Operations-apps en Common Data Service beschreven.
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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572444"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="ea49f-103">Organisatiehiërarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ea49f-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="ea49f-104">Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ea49f-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="ea49f-105">Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ea49f-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="ea49f-106">Hoewel Common Data Service het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst.</span><span class="sxs-lookup"><span data-stu-id="ea49f-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="ea49f-107">Als onderdeel van de Common Data Service-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ea49f-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="ea49f-108">Gegevensstroom</span><span class="sxs-lookup"><span data-stu-id="ea49f-108">Data flow</span></span>

<span data-ttu-id="ea49f-109">Een bedrijfsecosysteem dat bestaat uit Finance and Operations-apps en Common Data Service blijft een organisatiehiërarchie houden.</span><span class="sxs-lookup"><span data-stu-id="ea49f-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="ea49f-110">Deze organisatiehiërarchie is gebaseerd op Finance and Operations-apps, maar is in Common Data Service beschikbaar voor informatieve en uitbreidbare doeleinden.</span><span class="sxs-lookup"><span data-stu-id="ea49f-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="ea49f-111">In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Common Data Service worden weergegeven als een eenrichtingsgegevensstroom van Finance and Operations-apps naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ea49f-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Afbeelding van architectuur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="ea49f-113">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="ea49f-113">Templates</span></span>

<span data-ttu-id="ea49f-114">Entiteitstoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations-apps naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ea49f-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="ea49f-115">Doel van interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ea49f-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="ea49f-116">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Doel van organisatiehiërarchie van Finance and Operations naar andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="ea49f-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="ea49f-117">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-117">Source field</span></span> | <span data-ttu-id="ea49f-118">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ea49f-118">Map type</span></span> | <span data-ttu-id="ea49f-119">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-119">Destination field</span></span>
---|---|---
<span data-ttu-id="ea49f-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ea49f-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ea49f-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="ea49f-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="ea49f-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ea49f-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ea49f-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ea49f-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="ea49f-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="ea49f-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="ea49f-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="ea49f-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="ea49f-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="ea49f-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="ea49f-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="ea49f-127">msdyn\_immutable</span></span>
<span data-ttu-id="ea49f-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="ea49f-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="ea49f-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="ea49f-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="ea49f-130">Type interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ea49f-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="ea49f-131">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Type van organisatiehiërarchie van Finance and Operations naar andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="ea49f-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="ea49f-132">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-132">Source field</span></span> | <span data-ttu-id="ea49f-133">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ea49f-133">Map type</span></span> | <span data-ttu-id="ea49f-134">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-134">Destination field</span></span>
---|---|---
<span data-ttu-id="ea49f-135">NAAM</span><span class="sxs-lookup"><span data-stu-id="ea49f-135">NAME</span></span> | \> | <span data-ttu-id="ea49f-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ea49f-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="ea49f-137">Interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ea49f-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="ea49f-138">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Gepubliceerde organisatiehiërarchie van Finance and Operations naar andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="ea49f-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="ea49f-139">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-139">Source field</span></span> | <span data-ttu-id="ea49f-140">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ea49f-140">Map type</span></span> | <span data-ttu-id="ea49f-141">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-141">Destination field</span></span>
---|---|---
<span data-ttu-id="ea49f-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="ea49f-142">VALIDTO</span></span> | \> | <span data-ttu-id="ea49f-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="ea49f-143">msdyn\_validto</span></span>
<span data-ttu-id="ea49f-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="ea49f-144">VALIDFROM</span></span> | \> | <span data-ttu-id="ea49f-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="ea49f-145">msdyn\_validfrom</span></span>
<span data-ttu-id="ea49f-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ea49f-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ea49f-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="ea49f-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="ea49f-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ea49f-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ea49f-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="ea49f-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="ea49f-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ea49f-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ea49f-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="ea49f-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="ea49f-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="ea49f-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="ea49f-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ea49f-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="ea49f-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ea49f-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ea49f-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ea49f-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="ea49f-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ea49f-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="ea49f-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ea49f-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="ea49f-158">Interne organisatie</span><span class="sxs-lookup"><span data-stu-id="ea49f-158">Internal Organization</span></span>

<span data-ttu-id="ea49f-159">Gegevens over de interne organisatie in Common Data Service zijn afkomstig van twee entiteiten, **operationele eenheid** en **rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="ea49f-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="ea49f-160">Operationele eenheid</span><span class="sxs-lookup"><span data-stu-id="ea49f-160">Operating unit</span></span>

<span data-ttu-id="ea49f-161">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-161">Source field</span></span> | <span data-ttu-id="ea49f-162">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ea49f-162">Map type</span></span> | <span data-ttu-id="ea49f-163">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-163">Destination field</span></span>
---|---|---
<span data-ttu-id="ea49f-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="ea49f-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="ea49f-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="ea49f-165">msdyn\_languageid</span></span>
<span data-ttu-id="ea49f-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="ea49f-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="ea49f-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="ea49f-167">msdyn\_namealias</span></span>
<span data-ttu-id="ea49f-168">NAAM</span><span class="sxs-lookup"><span data-stu-id="ea49f-168">NAME</span></span> | \> | <span data-ttu-id="ea49f-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ea49f-169">msdyn\_name</span></span>
<span data-ttu-id="ea49f-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ea49f-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="ea49f-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ea49f-171">msdyn\_partynumber</span></span>
<span data-ttu-id="ea49f-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="ea49f-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="ea49f-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="ea49f-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="ea49f-174">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="ea49f-174">Legal entity</span></span>

<span data-ttu-id="ea49f-175">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-175">Source field</span></span> | <span data-ttu-id="ea49f-176">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ea49f-176">Map type</span></span> | <span data-ttu-id="ea49f-177">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-177">Destination field</span></span>
---|---|---
<span data-ttu-id="ea49f-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="ea49f-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="ea49f-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="ea49f-179">msdyn\_namealias</span></span>
<span data-ttu-id="ea49f-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="ea49f-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="ea49f-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="ea49f-181">msdyn\_languageid</span></span>
<span data-ttu-id="ea49f-182">NAAM</span><span class="sxs-lookup"><span data-stu-id="ea49f-182">NAME</span></span> | \> | <span data-ttu-id="ea49f-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="ea49f-183">msdyn\_name</span></span>
<span data-ttu-id="ea49f-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ea49f-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="ea49f-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="ea49f-185">msdyn\_partynumber</span></span>
<span data-ttu-id="ea49f-186">geen</span><span class="sxs-lookup"><span data-stu-id="ea49f-186">none</span></span> | \>\> | <span data-ttu-id="ea49f-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="ea49f-187">msdyn\_type</span></span>
<span data-ttu-id="ea49f-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="ea49f-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="ea49f-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="ea49f-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="ea49f-190">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="ea49f-190">Company</span></span>

<span data-ttu-id="ea49f-191">Biedt bidirectionele synchronisatie van rechtspersoonsgegevens (bedrijfsgegevens) tussen Finance and Operations en andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="ea49f-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="ea49f-192">Bronveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-192">Source field</span></span> | <span data-ttu-id="ea49f-193">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="ea49f-193">Map type</span></span> | <span data-ttu-id="ea49f-194">Doelveld</span><span class="sxs-lookup"><span data-stu-id="ea49f-194">Destination field</span></span>
---|---|---
<span data-ttu-id="ea49f-195">NAAM</span><span class="sxs-lookup"><span data-stu-id="ea49f-195">NAME</span></span> | = | <span data-ttu-id="ea49f-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="ea49f-196">cdm\_name</span></span>
<span data-ttu-id="ea49f-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="ea49f-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="ea49f-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="ea49f-198">cdm\_companycode</span></span>