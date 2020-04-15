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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173149"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="ad320-103">Organisatiehiërarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ad320-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="ad320-104">Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ad320-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="ad320-105">Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ad320-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="ad320-106">Hoewel Common Data Service het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst.</span><span class="sxs-lookup"><span data-stu-id="ad320-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="ad320-107">Als onderdeel van de Common Data Service-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ad320-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="ad320-108">Gegevensstroom</span><span class="sxs-lookup"><span data-stu-id="ad320-108">Data flow</span></span>

<span data-ttu-id="ad320-109">Een bedrijfsecosysteem dat bestaat uit Finance and Operations-apps en Common Data Service blijft een organisatiehiërarchie houden.</span><span class="sxs-lookup"><span data-stu-id="ad320-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="ad320-110">Deze organisatiehiërarchie is gebaseerd op Finance and Operations-apps, maar is in Common Data Service beschikbaar voor informatieve en uitbreidbare doeleinden.</span><span class="sxs-lookup"><span data-stu-id="ad320-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="ad320-111">In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Common Data Service worden weergegeven als een eenrichtingsgegevensstroom Finance and Operations-apps naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ad320-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Afbeelding van architectuur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="ad320-113">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="ad320-113">Templates</span></span>

<span data-ttu-id="ad320-114">Entiteitstoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations-apps naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ad320-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="ad320-115">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="ad320-115">Templates</span></span>

<span data-ttu-id="ad320-116">Productinformatie bevat alle informatie die betrekking heeft op het product en de definitie ervan, zoals de productdimensies of de tracerings- en opslagdimensies.</span><span class="sxs-lookup"><span data-stu-id="ad320-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="ad320-117">Zoals in de volgende tabel wordt aangegeven, wordt een verzameling entiteitstoewijzingen gemaakt om producten en gerelateerde informatie te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="ad320-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="ad320-118">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="ad320-118">Finance and Operations apps</span></span> | <span data-ttu-id="ad320-119">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="ad320-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="ad320-120">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="ad320-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="ad320-121">Organisatiehiërarchiedoelstellingen</span><span class="sxs-lookup"><span data-stu-id="ad320-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="ad320-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="ad320-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="ad320-123">Deze sjabloon biedt synchronisatie in één richting van de entiteit Doel van organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ad320-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="ad320-124">Type organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ad320-124">Organization hierarchy type</span></span> | <span data-ttu-id="ad320-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="ad320-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="ad320-126">Deze sjabloon biedt synchronisatie in één richting van de entiteit Type organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ad320-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="ad320-127">Organisatiehiërarchie - gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="ad320-127">Organization hierarchy - published</span></span> | <span data-ttu-id="ad320-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="ad320-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="ad320-129">Deze sjabloon biedt synchronisatie in één richting van de entiteit Gepubliceerde organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ad320-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="ad320-130">Operationele eenheid</span><span class="sxs-lookup"><span data-stu-id="ad320-130">Operating unit</span></span> | <span data-ttu-id="ad320-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ad320-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="ad320-132">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="ad320-132">Legal entities</span></span> | <span data-ttu-id="ad320-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ad320-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="ad320-134">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="ad320-134">Legal entities</span></span> | <span data-ttu-id="ad320-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="ad320-135">cdm_companies</span></span> | <span data-ttu-id="ad320-136">Biedt bidirectionele synchronisatie van gegevens over rechtspersonen (bedrijven).</span><span class="sxs-lookup"><span data-stu-id="ad320-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="ad320-137">Interne organisatie</span><span class="sxs-lookup"><span data-stu-id="ad320-137">Internal Organization</span></span>

<span data-ttu-id="ad320-138">Gegevens over de interne organisatie in Common Data Service zijn afkomstig van twee entiteiten, **operationele eenheid** en **rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="ad320-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

