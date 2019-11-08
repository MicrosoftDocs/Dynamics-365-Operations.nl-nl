---
title: Een ER-configuratie vanuit Lifecycle Services importeren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Lifecycle Services (LCS) kan importeren.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184825"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="f8815-103">Een ER-configuratie vanuit Lifecycle Services importeren</span><span class="sxs-lookup"><span data-stu-id="f8815-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8815-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Lifecycle Services (LCS) kan importeren.</span><span class="sxs-lookup"><span data-stu-id="f8815-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="f8815-105">In dit voorbeeld selecteert u de gewenste versie van de ER-configuratie en importeert u deze naar het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="f8815-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="f8815-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een ER-configuratie uploaden naar Lifecycle Services" voltooien.</span><span class="sxs-lookup"><span data-stu-id="f8815-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="f8815-107">Om deze stappen te kunnen uitvoeren is ook toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="f8815-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="f8815-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="f8815-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f8815-109">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="f8815-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="f8815-110">Een gedeelde versie van gegevensmodelconfiguratie verwijderen</span><span class="sxs-lookup"><span data-stu-id="f8815-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="f8815-111">Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f8815-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="f8815-112">De eerste versie van een voorbeeldgegevensmodelconfiguratie is gemaakt en gepubliceerd naar LCS tijdens de procedure "Een ER-configuratie naar Lifecycle Services uploaden".</span><span class="sxs-lookup"><span data-stu-id="f8815-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="f8815-113">In deze procedure verwijdert u deze versie van de ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="f8815-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="f8815-114">Deze versie van een voorbeeldgegevensmodelconfiguratie wordt later geïmporteerd vanuit LCS.</span><span class="sxs-lookup"><span data-stu-id="f8815-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="f8815-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f8815-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f8815-116">Selecteer de versie van deze configuratie die de status ‘Gedeeld’ heeft.</span><span class="sxs-lookup"><span data-stu-id="f8815-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="f8815-117">Deze status geeft aan dat de configuratie is gepubliceerd naar LCS.</span><span class="sxs-lookup"><span data-stu-id="f8815-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="f8815-118">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f8815-118">Click Change status.</span></span>
4. <span data-ttu-id="f8815-119">Klik op Beëindigen.</span><span class="sxs-lookup"><span data-stu-id="f8815-119">Click Discontinue.</span></span>
    * <span data-ttu-id="f8815-120">Wijzig de status van de geselecteerde versie van ‘Gedeeld’ in ‘Beëindigd’ om deze voor verwijdering beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="f8815-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="f8815-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f8815-121">Click OK.</span></span>
6. <span data-ttu-id="f8815-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f8815-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f8815-123">Selecteer de versie van deze configuratie die de status ‘Beëindigd’ heeft.</span><span class="sxs-lookup"><span data-stu-id="f8815-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="f8815-124">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f8815-124">Click Delete.</span></span>
8. <span data-ttu-id="f8815-125">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="f8815-125">Click Yes.</span></span>
    * <span data-ttu-id="f8815-126">De enige conceptversie 2 van de geselecteerde gegevensmodelconfiguratie is beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="f8815-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="f8815-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f8815-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="f8815-128">Een gedeelde versie van gegevensmodelconfiguratie importeren vanuit LCS</span><span class="sxs-lookup"><span data-stu-id="f8815-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="f8815-129">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8815-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f8815-130">Open de lijst met opslagplaatsen voor de configuratieprovider ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="f8815-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="f8815-131">Litware, Inc openen.</span><span class="sxs-lookup"><span data-stu-id="f8815-131">configuration provider.</span></span>  
2. <span data-ttu-id="f8815-132">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="f8815-132">Click Repositories.</span></span>
3. <span data-ttu-id="f8815-133">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="f8815-133">Click Open.</span></span>
    * <span data-ttu-id="f8815-134">Selecteer de LCS-opslagplaats en open deze.</span><span class="sxs-lookup"><span data-stu-id="f8815-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="f8815-135">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8815-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f8815-136">Selecteer de eerste versie van de 'Voorbeeldmodelconfiguratie' in de lijst met versies.</span><span class="sxs-lookup"><span data-stu-id="f8815-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="f8815-137">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="f8815-137">Click Import.</span></span>
6. <span data-ttu-id="f8815-138">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="f8815-138">Click Yes.</span></span>
    * <span data-ttu-id="f8815-139">Bevestig de import van de geselecteerde versie van LCS.</span><span class="sxs-lookup"><span data-stu-id="f8815-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="f8815-140">Het informatiebericht (boven het formulier) bevestigt de voltooiing van de import van de geselecteerde versie.</span><span class="sxs-lookup"><span data-stu-id="f8815-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="f8815-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f8815-141">Close the page.</span></span>
8. <span data-ttu-id="f8815-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f8815-142">Close the page.</span></span>
9. <span data-ttu-id="f8815-143">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="f8815-143">Click Configurations.</span></span>
10. <span data-ttu-id="f8815-144">Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f8815-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="f8815-145">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f8815-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f8815-146">Selecteer de versie van deze configuratie die de status ‘Gedeeld’ heeft.</span><span class="sxs-lookup"><span data-stu-id="f8815-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="f8815-147">De gedeelde versie 1 van de geselecteerde gegevensmodelconfiguratie is nu ook beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="f8815-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  
