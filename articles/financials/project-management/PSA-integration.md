---
title: Project Service Automation
description: Dit onderwerp biedt informatie over de integratieoplossing voor Project Service Automatisering met Finance and Operations. Deze integratieoplossing gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="7d81a-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7d81a-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7d81a-105">De integratieoplossing voor Project Service Automation met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7d81a-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="7d81a-106">De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maakt de stroom van projecten, projectcontracten, projectcontractregels, projectcontractregelmijlpalen, projecttaken, onkostentransactiecategorieën, uurramingen en onkostenramingen van Project Service Automation naar Finance and Operations mogelijk.</span><span class="sxs-lookup"><span data-stu-id="7d81a-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="7d81a-107">Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="7d81a-108">Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="7d81a-109">Als u Finance and Operations 7.3.0 gebruikt, moet u KB 4074835 installeren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="7d81a-110">U kunt dan projecten met vaste prijs integreren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="7d81a-111">Als u gebruikmaakt van Finance and Operations 7.3.0 en u bijzondere-kostentransacties overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten op te nemen in de projectfactuur.</span><span class="sxs-lookup"><span data-stu-id="7d81a-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="7d81a-112">Als u Microsoft Dynamics 365 for Finance and Operations versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7d81a-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="7d81a-113">Als u Microsoft Dynamics 365 for Finance and Operations 8.0.1 of hoger gebruikt, kunt u werkelijke waarden synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="7d81a-114">Voordat u Project Service Automation kunt integreren met Finance and Operations, moet u de integratieparameters van Project Service Automation configureren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="7d81a-115">Zie [Integratieparameters van Project Service Automation](PSA-parameters.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7d81a-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="7d81a-116">Met deze integratieoplossing is directe synchronisatie mogelijk in de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="7d81a-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="7d81a-117">Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-118">Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-119">Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-120">Onderhoud projectcontractregelmijlpalen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-121">Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-122">Onderhoud onkostentransactiecategorieën in Finance and Operations en synchroniseer ze rechtstreeks van Finance and Operations naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7d81a-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="7d81a-123">Maak projectuurramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-124">Maak projectkostenramingen in Project Service Automation en synchroniseer ze rechtstreeks van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="7d81a-125">Maak projecttijd, onkosten en bijzondere kosten werkelijke waarden in Project Service Automation en maak projecttransacties in het integratiejournaal van Project Service Automation zodat deze kunnen worden geboekt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="7d81a-126">Gegevenssynchronisatie</span><span class="sxs-lookup"><span data-stu-id="7d81a-126">Data synchronization</span></span>

<span data-ttu-id="7d81a-127">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d81a-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="7d81a-128">Niet alle sjablonen zijn momenteel beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="7d81a-128">Not all templates are currently available.</span></span> <span data-ttu-id="7d81a-129">Sjablonen wordt vrijgegeven zodra ze gereed zijn.</span><span class="sxs-lookup"><span data-stu-id="7d81a-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="7d81a-130">[![Integratie van Project Service Automation met Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="7d81a-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="7d81a-131">Systeemvereisten voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d81a-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="7d81a-132">Om de integratieoplossing van Project Service Automation naar Finance and Operations te gebruiken moet u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 met platformupdate 12 of hoger installeren.</span><span class="sxs-lookup"><span data-stu-id="7d81a-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="7d81a-133">Systeemvereisten voor Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7d81a-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="7d81a-134">Als u de integratieoplossing van Project Service Automation naar Finance and Operations wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="7d81a-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="7d81a-135">Microsoft Dynamics 365 for Project Service Automation versie 9.0.0.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="7d81a-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="7d81a-136">De oplossing Prospect naar contant geld voor Microsoft Dynamics 365 for Sales, versie 1.14.0.0 (v14) of hoger</span><span class="sxs-lookup"><span data-stu-id="7d81a-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="7d81a-137">Oplossing Project Service Automation naar Finance and Operations voor Microsoft Dynamics 365 for Project Service Automation versie 1.0.0.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="7d81a-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="7d81a-138">De integratieoplossing van Project Service Automation naar Finance and Operations installeren in uw exemplaar van Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7d81a-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="7d81a-139">Download de integratieoplossing Project Service Automation naar Finance and Operations vanuit het [Microsoft Downloadcentrum](https://www.microsoft.com/en-us/download/details.aspx?id=57016) en volg de instructies die zijn meegeleverd met de oplossing.</span><span class="sxs-lookup"><span data-stu-id="7d81a-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
