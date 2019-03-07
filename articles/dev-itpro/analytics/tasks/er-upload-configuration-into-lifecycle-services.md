---
title: Een ER-configuratie naar Lifecycle Services uploaden
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken en uploaden.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "335089"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="55e2c-103">Een ER-configuratie naar Lifecycle Services uploaden</span><span class="sxs-lookup"><span data-stu-id="55e2c-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55e2c-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken en uploaden.</span><span class="sxs-lookup"><span data-stu-id="55e2c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="55e2c-105">In dit voorbeeld maakt u een configuratie en uploadt u deze naar LCS voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="55e2c-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="55e2c-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="55e2c-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="55e2c-107">Om deze stappen te kunnen uitvoeren is ook toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="55e2c-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="55e2c-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="55e2c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="55e2c-109">Selecteer ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="55e2c-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="55e2c-110">en stel het in als actief.</span><span class="sxs-lookup"><span data-stu-id="55e2c-110">and set it as active.</span></span>
3. <span data-ttu-id="55e2c-111">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="55e2c-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="55e2c-112">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="55e2c-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="55e2c-113">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="55e2c-114">U maakt een configuratie die een voorbeeldgegevensmodel voor elektronische documenten bevat.</span><span class="sxs-lookup"><span data-stu-id="55e2c-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="55e2c-115">Deze gegevensmodelconfiguratie wordt later in LCS geüpload.</span><span class="sxs-lookup"><span data-stu-id="55e2c-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="55e2c-116">Typ 'Voorbeeldmodelconfiguratie' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="55e2c-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="55e2c-117">Voorbeeldmodelconfiguratie</span><span class="sxs-lookup"><span data-stu-id="55e2c-117">Sample model configuration</span></span>  
3. <span data-ttu-id="55e2c-118">Typ 'Voorbeeldmodelconfiguratie' in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="55e2c-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="55e2c-119">Voorbeeldmodelconfiguratie</span><span class="sxs-lookup"><span data-stu-id="55e2c-119">Sample model configuration</span></span>  
4. <span data-ttu-id="55e2c-120">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="55e2c-120">Click Create configuration.</span></span>
5. <span data-ttu-id="55e2c-121">Klik op Modelontwerper.</span><span class="sxs-lookup"><span data-stu-id="55e2c-121">Click Model designer.</span></span>
6. <span data-ttu-id="55e2c-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="55e2c-122">Click New.</span></span>
7. <span data-ttu-id="55e2c-123">Typ 'Invoerpunt' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="55e2c-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="55e2c-124">Invoerpunt</span><span class="sxs-lookup"><span data-stu-id="55e2c-124">Entry point</span></span>  
8. <span data-ttu-id="55e2c-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-125">Click Add.</span></span>
9. <span data-ttu-id="55e2c-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="55e2c-126">Click Save.</span></span>
10. <span data-ttu-id="55e2c-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="55e2c-127">Close the page.</span></span>
11. <span data-ttu-id="55e2c-128">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-128">Click Change status.</span></span>
12. <span data-ttu-id="55e2c-129">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="55e2c-129">Click Complete.</span></span>
13. <span data-ttu-id="55e2c-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="55e2c-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="55e2c-131">Een nieuwe opslagplaats registreren</span><span class="sxs-lookup"><span data-stu-id="55e2c-131">Register a new  repository</span></span>
1. <span data-ttu-id="55e2c-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="55e2c-132">Close the page.</span></span>
2. <span data-ttu-id="55e2c-133">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-133">Click Repositories.</span></span>
    * <span data-ttu-id="55e2c-134">Hiermee kunt u de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc openen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="55e2c-135">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="55e2c-136">Hiermee kunt u een nieuwe opslagplaats toevoegen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="55e2c-137">Selecteer LCS in het veld Type opslagplaats van configuratie.</span><span class="sxs-lookup"><span data-stu-id="55e2c-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="55e2c-138">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="55e2c-138">Click Create repository.</span></span>
6. <span data-ttu-id="55e2c-139">Typ of selecteer een waarde in het veld Project.</span><span class="sxs-lookup"><span data-stu-id="55e2c-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="55e2c-140">Selecteer het gewenste LCS-project.</span><span class="sxs-lookup"><span data-stu-id="55e2c-140">Select the desired LCS project.</span></span> <span data-ttu-id="55e2c-141">U moet toegang tot het project hebben.</span><span class="sxs-lookup"><span data-stu-id="55e2c-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="55e2c-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="55e2c-142">Click OK.</span></span>
    * <span data-ttu-id="55e2c-143">Voer een nieuwe opslagplaats in.</span><span class="sxs-lookup"><span data-stu-id="55e2c-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="55e2c-144">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="55e2c-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="55e2c-145">Selecteer de LCS-opslagplaatsrecord.</span><span class="sxs-lookup"><span data-stu-id="55e2c-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="55e2c-146">Een geregistreerde opslagplaats wordt door de huidige provide gemarkeerd, wat betekent dat de enige configuraties in bezit van die provider in deze opslagplaats kunnen worden geplaatst en daarom naar het geselecteerde LCS-project kunnen worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="55e2c-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="55e2c-147">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-147">Click Open.</span></span>
    * <span data-ttu-id="55e2c-148">Open de opslagplaats om de lijst met ER-configuraties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="55e2c-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="55e2c-149">De lijst is leeg als dit project nog niet voor delen van ER-configuraties is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="55e2c-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="55e2c-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="55e2c-150">Close the page.</span></span>
11. <span data-ttu-id="55e2c-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="55e2c-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="55e2c-152">Configuratie naar LCS uploaden</span><span class="sxs-lookup"><span data-stu-id="55e2c-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="55e2c-153">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="55e2c-153">Click Configurations.</span></span>
2. <span data-ttu-id="55e2c-154">Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="55e2c-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="55e2c-155">Selecteer een gemaakte configuratie die al is voltooid.</span><span class="sxs-lookup"><span data-stu-id="55e2c-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="55e2c-156">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="55e2c-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="55e2c-157">Selecteer de versie van de geselecteerde configuratie met de status ‘Voltooid’.</span><span class="sxs-lookup"><span data-stu-id="55e2c-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="55e2c-158">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-158">Click Change status.</span></span>
5. <span data-ttu-id="55e2c-159">Klik op Delen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-159">Click Share.</span></span>
    * <span data-ttu-id="55e2c-160">De configuratiestatus wordt gewijzigd van ‘Voltooid’ in ‘Gedeeld’ wanneer deze wordt gepubliceerd in LCS.</span><span class="sxs-lookup"><span data-stu-id="55e2c-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="55e2c-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="55e2c-161">Click OK.</span></span>
7. <span data-ttu-id="55e2c-162">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="55e2c-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="55e2c-163">Selecteer de configuratieversie met de status ‘Gedeeld’.</span><span class="sxs-lookup"><span data-stu-id="55e2c-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="55e2c-164">De status van de geselecteerde versie is gewijzigd van ‘Voltooid’ in ‘Gedeeld’.</span><span class="sxs-lookup"><span data-stu-id="55e2c-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="55e2c-165">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="55e2c-165">Close the page.</span></span>
9. <span data-ttu-id="55e2c-166">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-166">Click Repositories.</span></span>
    * <span data-ttu-id="55e2c-167">Hiermee kunt u de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc openen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="55e2c-168">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="55e2c-168">Click Open.</span></span>
    * <span data-ttu-id="55e2c-169">Selecteer de LCS-opslagplaats en open deze.</span><span class="sxs-lookup"><span data-stu-id="55e2c-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="55e2c-170">De geselecteerde configuratie wordt getoond als een activum van het geselecteerde LCS-project.</span><span class="sxs-lookup"><span data-stu-id="55e2c-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="55e2c-171">LCS openen met https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="55e2c-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="55e2c-172">Open een project dat eerder is gebruikt voor opslagplaatsregistratie, open de ‘Activabibliotheek’ van dit project en vouw de inhoud van het activumtype ‘GER-configuratie’ uit; de geüploade ER-configuratie is beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="55e2c-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="55e2c-173">De geüploade LCS-configuratie kan naar een ander Microsoft Dynamics 365 for Finance and Operations, Enterprise edition-exemplaar worden geïmporteerd als providers toegang tot dit LCS-project hebben.</span><span class="sxs-lookup"><span data-stu-id="55e2c-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  

