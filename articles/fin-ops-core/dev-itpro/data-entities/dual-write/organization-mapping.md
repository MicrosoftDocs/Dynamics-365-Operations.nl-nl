---
title: Organisatiehiërarchie in Dataverse
description: In dit onderwerp wordt de integratie van organisatiegegevens tussen Finance and Operations-apps en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750807"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="d9c8a-103">Organisatiehiërarchie in Dataverse</span><span class="sxs-lookup"><span data-stu-id="d9c8a-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d9c8a-104">Omdat Dynamics 365 Finance een financieel systeem is, is *organisatie* een kernconcept en start de systeeminstallatie met de configuratie van een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="d9c8a-105">Bedrijfsfinanciën kunnen vervolgens worden bijgehouden op organisatieniveau en ook op elk niveau in de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="d9c8a-106">Hoewel Dataverse het concept van een organisatiehiërarchie niet heeft, heeft het wel een paar losse concepten, zoals de totale verkoopopbrengst.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="d9c8a-107">Als onderdeel van de Dataverse-integratie wordt de gegevensstructuur van de organisatiehiërarchie toegevoegd aan Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="d9c8a-108">Gegevensstroom</span><span class="sxs-lookup"><span data-stu-id="d9c8a-108">Data flow</span></span>

<span data-ttu-id="d9c8a-109">Een bedrijfsecosysteem dat bestaat uit Finance and Operations-apps en Dataverse blijft een organisatiehiërarchie houden.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="d9c8a-110">Deze organisatiehiërarchie is gebaseerd op Finance and Operations-apps, maar is in Dataverse beschikbaar voor informatieve en uitbreidbare doeleinden.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="d9c8a-111">In de volgende afbeelding ziet u gegevens van de organisatiehiërarchie die in Dataverse worden weergegeven als een eenrichtingsgegevensstroom Finance and Operations-apps naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Afbeelding van architectuur](media/dual-write-data-flow.png)

<span data-ttu-id="d9c8a-113">Tabeltoewijzingen voor organisatiehiërarchie zijn beschikbaar voor eenrichtingssynchronisatie van gegevens uit Finance and Operations-apps naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="d9c8a-114">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="d9c8a-114">Templates</span></span>

<span data-ttu-id="d9c8a-115">Productinformatie bevat alle informatie die betrekking heeft op het product en de definitie ervan, zoals de productdimensies of de tracerings- en opslagdimensies.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="d9c8a-116">Zoals in de volgende tabel wordt aangegeven, wordt een verzameling tabeltoewijzingen gemaakt om producten en gerelateerde informatie te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="d9c8a-117">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="d9c8a-117">Finance and Operations apps</span></span> | <span data-ttu-id="d9c8a-118">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="d9c8a-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d9c8a-119">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d9c8a-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="d9c8a-120">Organisatiehiërarchiedoelstellingen</span><span class="sxs-lookup"><span data-stu-id="d9c8a-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="d9c8a-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="d9c8a-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="d9c8a-122">Deze sjabloon biedt synchronisatie in één richting van de tabel Doel van organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="d9c8a-123">Type organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="d9c8a-123">Organization hierarchy type</span></span> | <span data-ttu-id="d9c8a-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="d9c8a-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="d9c8a-125">Deze sjabloon biedt synchronisatie in één richting van de tabel Type organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="d9c8a-126">Organisatiehiërarchie - gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="d9c8a-126">Organization hierarchy - published</span></span> | <span data-ttu-id="d9c8a-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="d9c8a-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="d9c8a-128">Deze sjabloon biedt synchronisatie in één richting van de tabel Gepubliceerde organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="d9c8a-129">Operationele eenheid</span><span class="sxs-lookup"><span data-stu-id="d9c8a-129">Operating unit</span></span> | <span data-ttu-id="d9c8a-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d9c8a-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d9c8a-131">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="d9c8a-131">Legal entities</span></span> | <span data-ttu-id="d9c8a-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d9c8a-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d9c8a-133">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="d9c8a-133">Legal entities</span></span> | <span data-ttu-id="d9c8a-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="d9c8a-134">cdm_companies</span></span> | <span data-ttu-id="d9c8a-135">Biedt bidirectionele synchronisatie van gegevens over rechtspersonen (bedrijven).</span><span class="sxs-lookup"><span data-stu-id="d9c8a-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="d9c8a-136">Interne organisatie</span><span class="sxs-lookup"><span data-stu-id="d9c8a-136">Internal Organization</span></span>

<span data-ttu-id="d9c8a-137">Gegevens over de interne organisatie in Dataverse zijn afkomstig van twee tabellen, **operationele eenheid** en **rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="d9c8a-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]