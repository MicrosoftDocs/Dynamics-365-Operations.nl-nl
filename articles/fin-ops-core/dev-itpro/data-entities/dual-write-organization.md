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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182020"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="14f14-103">Organisatiehiërarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="14f14-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="14f14-104">Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="14f14-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="14f14-105">Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="14f14-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="14f14-106">Hoewel Common Data Service het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst.</span><span class="sxs-lookup"><span data-stu-id="14f14-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="14f14-107">Als onderdeel van de Common Data Service-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14f14-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="14f14-108">Gegevensstroom</span><span class="sxs-lookup"><span data-stu-id="14f14-108">Data flow</span></span>

<span data-ttu-id="14f14-109">Een bedrijfsecosysteem dat bestaat uit Finance and Operations-apps en Common Data Service blijft een organisatiehiërarchie houden.</span><span class="sxs-lookup"><span data-stu-id="14f14-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="14f14-110">Deze organisatiehiërarchie is gebaseerd op Finance and Operations-apps, maar is in Common Data Service beschikbaar voor informatieve en uitbreidbare doeleinden.</span><span class="sxs-lookup"><span data-stu-id="14f14-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="14f14-111">In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Common Data Service worden weergegeven als een eenrichtingsgegevensstroom van Finance and Operations-apps naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14f14-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Afbeelding van architectuur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="14f14-113">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="14f14-113">Templates</span></span>

<span data-ttu-id="14f14-114">Entiteitstoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations-apps naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14f14-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="14f14-115">Doel van interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="14f14-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="14f14-116">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Doel van organisatiehiërarchie van Finance and Operations naar andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="14f14-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="14f14-117">Bronveld</span><span class="sxs-lookup"><span data-stu-id="14f14-117">Source field</span></span> | <span data-ttu-id="14f14-118">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="14f14-118">Map type</span></span> | <span data-ttu-id="14f14-119">Doelveld</span><span class="sxs-lookup"><span data-stu-id="14f14-119">Destination field</span></span>
---|---|---
<span data-ttu-id="14f14-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="14f14-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="14f14-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="14f14-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="14f14-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="14f14-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="14f14-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="14f14-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="14f14-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="14f14-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="14f14-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="14f14-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="14f14-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="14f14-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="14f14-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="14f14-127">msdyn\_immutable</span></span>
<span data-ttu-id="14f14-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="14f14-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="14f14-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="14f14-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="14f14-130">Type interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="14f14-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="14f14-131">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Type van organisatiehiërarchie van Finance and Operations naar andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="14f14-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="14f14-132">Bronveld</span><span class="sxs-lookup"><span data-stu-id="14f14-132">Source field</span></span> | <span data-ttu-id="14f14-133">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="14f14-133">Map type</span></span> | <span data-ttu-id="14f14-134">Doelveld</span><span class="sxs-lookup"><span data-stu-id="14f14-134">Destination field</span></span>
---|---|---
<span data-ttu-id="14f14-135">NAAM</span><span class="sxs-lookup"><span data-stu-id="14f14-135">NAME</span></span> | \> | <span data-ttu-id="14f14-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="14f14-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="14f14-137">Interne organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="14f14-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="14f14-138">Deze sjabloon biedt eenrichtingssynchronisatie van de entiteit Gepubliceerde organisatiehiërarchie van Finance and Operations naar andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="14f14-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="14f14-139">Bronveld</span><span class="sxs-lookup"><span data-stu-id="14f14-139">Source field</span></span> | <span data-ttu-id="14f14-140">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="14f14-140">Map type</span></span> | <span data-ttu-id="14f14-141">Doelveld</span><span class="sxs-lookup"><span data-stu-id="14f14-141">Destination field</span></span>
---|---|---
<span data-ttu-id="14f14-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="14f14-142">VALIDTO</span></span> | \> | <span data-ttu-id="14f14-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="14f14-143">msdyn\_validto</span></span>
<span data-ttu-id="14f14-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="14f14-144">VALIDFROM</span></span> | \> | <span data-ttu-id="14f14-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="14f14-145">msdyn\_validfrom</span></span>
<span data-ttu-id="14f14-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="14f14-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="14f14-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="14f14-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="14f14-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="14f14-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="14f14-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="14f14-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="14f14-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="14f14-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="14f14-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="14f14-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="14f14-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="14f14-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="14f14-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="14f14-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="14f14-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="14f14-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="14f14-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="14f14-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="14f14-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="14f14-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="14f14-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="14f14-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="14f14-158">Interne organisatie</span><span class="sxs-lookup"><span data-stu-id="14f14-158">Internal Organization</span></span>

<span data-ttu-id="14f14-159">Gegevens over de interne organisatie in Common Data Service zijn afkomstig van twee entiteiten, **operationele eenheid** en **rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="14f14-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="14f14-160">Operationele eenheid</span><span class="sxs-lookup"><span data-stu-id="14f14-160">Operating unit</span></span>

<span data-ttu-id="14f14-161">Bronveld</span><span class="sxs-lookup"><span data-stu-id="14f14-161">Source field</span></span> | <span data-ttu-id="14f14-162">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="14f14-162">Map type</span></span> | <span data-ttu-id="14f14-163">Doelveld</span><span class="sxs-lookup"><span data-stu-id="14f14-163">Destination field</span></span>
---|---|---
<span data-ttu-id="14f14-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="14f14-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="14f14-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="14f14-165">msdyn\_languageid</span></span>
<span data-ttu-id="14f14-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="14f14-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="14f14-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="14f14-167">msdyn\_namealias</span></span>
<span data-ttu-id="14f14-168">NAAM</span><span class="sxs-lookup"><span data-stu-id="14f14-168">NAME</span></span> | \> | <span data-ttu-id="14f14-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="14f14-169">msdyn\_name</span></span>
<span data-ttu-id="14f14-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="14f14-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="14f14-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="14f14-171">msdyn\_partynumber</span></span>
<span data-ttu-id="14f14-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="14f14-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="14f14-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="14f14-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="14f14-174">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="14f14-174">Legal entity</span></span>

<span data-ttu-id="14f14-175">Bronveld</span><span class="sxs-lookup"><span data-stu-id="14f14-175">Source field</span></span> | <span data-ttu-id="14f14-176">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="14f14-176">Map type</span></span> | <span data-ttu-id="14f14-177">Doelveld</span><span class="sxs-lookup"><span data-stu-id="14f14-177">Destination field</span></span>
---|---|---
<span data-ttu-id="14f14-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="14f14-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="14f14-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="14f14-179">msdyn\_namealias</span></span>
<span data-ttu-id="14f14-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="14f14-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="14f14-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="14f14-181">msdyn\_languageid</span></span>
<span data-ttu-id="14f14-182">NAAM</span><span class="sxs-lookup"><span data-stu-id="14f14-182">NAME</span></span> | \> | <span data-ttu-id="14f14-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="14f14-183">msdyn\_name</span></span>
<span data-ttu-id="14f14-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="14f14-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="14f14-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="14f14-185">msdyn\_partynumber</span></span>
<span data-ttu-id="14f14-186">geen</span><span class="sxs-lookup"><span data-stu-id="14f14-186">none</span></span> | \>\> | <span data-ttu-id="14f14-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="14f14-187">msdyn\_type</span></span>
<span data-ttu-id="14f14-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="14f14-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="14f14-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="14f14-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="14f14-190">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="14f14-190">Company</span></span>

<span data-ttu-id="14f14-191">Biedt bidirectionele synchronisatie van rechtspersoonsgegevens (bedrijfsgegevens) tussen Finance and Operations en andere Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="14f14-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="14f14-192">Bronveld</span><span class="sxs-lookup"><span data-stu-id="14f14-192">Source field</span></span> | <span data-ttu-id="14f14-193">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="14f14-193">Map type</span></span> | <span data-ttu-id="14f14-194">Doelveld</span><span class="sxs-lookup"><span data-stu-id="14f14-194">Destination field</span></span>
---|---|---
<span data-ttu-id="14f14-195">NAAM</span><span class="sxs-lookup"><span data-stu-id="14f14-195">NAME</span></span> | = | <span data-ttu-id="14f14-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="14f14-196">cdm\_name</span></span>
<span data-ttu-id="14f14-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="14f14-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="14f14-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="14f14-198">cdm\_companycode</span></span>
