--- 
title: Een configuratie importeren vanuit Lifecycle Services voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Lifecycle Services (LCS) kan importeren.
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 011a840994ef61d01a47ac5925674d0a974c2f83
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="fa432-103">Een configuratie importeren vanuit Lifecycle Services voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="fa432-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa432-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Lifecycle Services (LCS) kan importeren.</span><span class="sxs-lookup"><span data-stu-id="fa432-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="fa432-105">In dit voorbeeld selecteert u de gewenste versie van de ER-configuratie en importeert u deze naar het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="fa432-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="fa432-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een ER-configuratie uploaden naar Lifecycle Services" voltooien.</span><span class="sxs-lookup"><span data-stu-id="fa432-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="fa432-107">Om deze stappen te kunnen uitvoeren is ook toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="fa432-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="fa432-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="fa432-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="fa432-109">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="fa432-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="fa432-110">Een gedeelde versie van gegevensmodelconfiguratie verwijderen</span><span class="sxs-lookup"><span data-stu-id="fa432-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="fa432-111">Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="fa432-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="fa432-112">De eerste versie van een voorbeeldgegevensmodelconfiguratie is gemaakt en gepubliceerd naar LCS tijdens de procedure "Een ER-configuratie naar Lifecycle Services uploaden".</span><span class="sxs-lookup"><span data-stu-id="fa432-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="fa432-113">In deze procedure verwijdert u deze versie van de ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="fa432-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="fa432-114">Deze versie van een voorbeeldgegevensmodelconfiguratie wordt later geïmporteerd vanuit LCS.</span><span class="sxs-lookup"><span data-stu-id="fa432-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="fa432-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa432-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fa432-116">Selecteer de versie van deze configuratie die de status ‘Gedeeld’ heeft.</span><span class="sxs-lookup"><span data-stu-id="fa432-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="fa432-117">Deze status geeft aan dat de configuratie is gepubliceerd naar LCS.</span><span class="sxs-lookup"><span data-stu-id="fa432-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="fa432-118">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="fa432-118">Click Change status.</span></span>
4. <span data-ttu-id="fa432-119">Klik op Beëindigen.</span><span class="sxs-lookup"><span data-stu-id="fa432-119">Click Discontinue.</span></span>
    * <span data-ttu-id="fa432-120">Wijzig de status van de geselecteerde versie van ‘Gedeeld’ in ‘Beëindigd’ om deze voor verwijdering beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="fa432-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="fa432-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fa432-121">Click OK.</span></span>
6. <span data-ttu-id="fa432-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa432-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fa432-123">Selecteer de versie van deze configuratie die de status ‘Beëindigd’ heeft.</span><span class="sxs-lookup"><span data-stu-id="fa432-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="fa432-124">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="fa432-124">Click Delete.</span></span>
8. <span data-ttu-id="fa432-125">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="fa432-125">Click Yes.</span></span>
    * <span data-ttu-id="fa432-126">De enige conceptversie 2 van de geselecteerde gegevensmodelconfiguratie is beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="fa432-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="fa432-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fa432-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="fa432-128">Een gedeelde versie van gegevensmodelconfiguratie importeren vanuit LCS</span><span class="sxs-lookup"><span data-stu-id="fa432-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="fa432-129">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fa432-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fa432-130">Open de lijst met opslagplaatsen voor de configuratieprovider ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="fa432-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="fa432-131">Litware, Inc openen.</span><span class="sxs-lookup"><span data-stu-id="fa432-131">configuration provider.</span></span>  
2. <span data-ttu-id="fa432-132">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="fa432-132">Click Repositories.</span></span>
3. <span data-ttu-id="fa432-133">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="fa432-133">Click Open.</span></span>
    * <span data-ttu-id="fa432-134">Selecteer de LCS-opslagplaats en open deze.</span><span class="sxs-lookup"><span data-stu-id="fa432-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="fa432-135">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fa432-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fa432-136">Selecteer de eerste versie van de 'Voorbeeldmodelconfiguratie' in de lijst met versies.</span><span class="sxs-lookup"><span data-stu-id="fa432-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="fa432-137">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="fa432-137">Click Import.</span></span>
6. <span data-ttu-id="fa432-138">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="fa432-138">Click Yes.</span></span>
    * <span data-ttu-id="fa432-139">Bevestig de import van de geselecteerde versie van LCS.</span><span class="sxs-lookup"><span data-stu-id="fa432-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="fa432-140">Het informatiebericht (boven het formulier) bevestigt de voltooiing van de import van de geselecteerde versie.</span><span class="sxs-lookup"><span data-stu-id="fa432-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="fa432-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fa432-141">Close the page.</span></span>
8. <span data-ttu-id="fa432-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fa432-142">Close the page.</span></span>
9. <span data-ttu-id="fa432-143">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="fa432-143">Click Configurations.</span></span>
10. <span data-ttu-id="fa432-144">Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="fa432-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="fa432-145">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa432-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fa432-146">Selecteer de versie van deze configuratie die de status ‘Gedeeld’ heeft.</span><span class="sxs-lookup"><span data-stu-id="fa432-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="fa432-147">De gedeelde versie 1 van de geselecteerde gegevensmodelconfiguratie is nu ook beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="fa432-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


