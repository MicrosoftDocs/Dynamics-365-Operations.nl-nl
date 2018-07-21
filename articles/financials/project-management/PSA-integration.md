---
title: Project Service Automation
description: Deze oplossing gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via de Common Data Service (CDS).
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="12e53-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="12e53-103">Project Service Automation</span></span>

<span data-ttu-id="12e53-104">De oplossing Project Service Automation-integratie gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via de Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="12e53-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="12e53-105">De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maakt de stroom van projecten, projectcontracten, projectcontractregels, projectcontractregelmijlpalen, projecttaken, onkostentransactiecategorieën, uurramingen en onkostenramingen van Project Service Automation naar Finance and Operations mogelijk.</span><span class="sxs-lookup"><span data-stu-id="12e53-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="12e53-106">Als u werkt met Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0, moet u KB 4074835 installeren.</span><span class="sxs-lookup"><span data-stu-id="12e53-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="12e53-107">Hierdoor kunt u vaste-prijsprojecten integreren.</span><span class="sxs-lookup"><span data-stu-id="12e53-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="12e53-108">Als u Dynamics 365 for Finance and Operations versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling gebruiken.</span><span class="sxs-lookup"><span data-stu-id="12e53-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="12e53-109">Als u Dynamics 365 for Finance and Operations 8.0.1 gebruikt, kunt u werkelijke waarden synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="12e53-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="12e53-110">Als u Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="12e53-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="12e53-111">Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="12e53-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="12e53-112">Voordat u Project Service Automation kunt integreren met Finance and Operations, moet u de integratieparameters van Project Service Automation configureren.</span><span class="sxs-lookup"><span data-stu-id="12e53-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="12e53-113">Zie Integratieparameters van Project Service Automation voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="12e53-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="12e53-114">Met deze integratieoplossing is directe synchronisatie mogelijk in de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="12e53-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="12e53-115">Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="12e53-116">Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="12e53-117">Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="12e53-118">Onderhoud projectcontractregelmijlpalen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="12e53-119">Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="12e53-120">Onderhoud onkostentransactiecategorieën in Finance and Operations en synchroniseer ze rechtstreeks van Finance and Operations naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="12e53-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="12e53-121">Maak projectuurramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="12e53-122">Maak projectkostenramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="12e53-123">Gegevenssynchronisatie</span><span class="sxs-lookup"><span data-stu-id="12e53-123">Data synchronization</span></span>
<span data-ttu-id="12e53-124">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12e53-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="12e53-125">Niet alle sjablonen zijn momenteel beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="12e53-125">Not all templates are currently available.</span></span> <span data-ttu-id="12e53-126">Sjablonen wordt vrijgegeven zodra ze gereed zijn.</span><span class="sxs-lookup"><span data-stu-id="12e53-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="12e53-127">[![Integratie van Project Service Automation met Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="12e53-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="12e53-128">Systeemvereisten voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="12e53-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="12e53-129">Om de integratieoplossing van Project Service Automation naar Finance and Operations te gebruiken moet u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 met platformupdate 12 of hoger installeren.</span><span class="sxs-lookup"><span data-stu-id="12e53-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="12e53-130">Systeemvereisten voor Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="12e53-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="12e53-131">Als u de integratieoplossing van Project Service Automation naar Finance and Operations wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="12e53-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="12e53-132">Microsoft Dynamics 365 for Project Service Automation versie 9.0.0.0 of hoger.</span><span class="sxs-lookup"><span data-stu-id="12e53-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="12e53-133">De oplossing Prospect naar contant geld voor Dynamics 365 for Sales, versie 1.14.0.0 (v14) of hoger.</span><span class="sxs-lookup"><span data-stu-id="12e53-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="12e53-134">Oplossing Project Service Automation naar Operations voor Dynamics 365 for Project Service Automation versie 1.0.0.0 of hoger.</span><span class="sxs-lookup"><span data-stu-id="12e53-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="12e53-135">De integratieoplossing van Project Service Automation naar Finance and Operations installeren in uw exemplaar van Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="12e53-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



