--- 
title: Een configuratie uploaden naar Lifecycle Services voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken en uploaden.
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
ms.openlocfilehash: 9f5f8c6cb829ee3d761fa4cdba56b7cdc52f4eb4
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="33738-103">Een configuratie uploaden naar Lifecycle Services voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="33738-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33738-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken en uploaden.</span><span class="sxs-lookup"><span data-stu-id="33738-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="33738-105">In dit voorbeeld maakt u een configuratie en uploadt u deze naar LCS voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="33738-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="33738-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="33738-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="33738-107">Om deze stappen te kunnen uitvoeren is ook toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="33738-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="33738-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="33738-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="33738-109">Selecteer ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="33738-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="33738-110">en stel het in als actief.</span><span class="sxs-lookup"><span data-stu-id="33738-110">and set it as active.</span></span>
3. <span data-ttu-id="33738-111">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="33738-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="33738-112">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="33738-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="33738-113">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="33738-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="33738-114">U maakt een configuratie die een voorbeeldgegevensmodel voor elektronische documenten bevat.</span><span class="sxs-lookup"><span data-stu-id="33738-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="33738-115">Deze gegevensmodelconfiguratie wordt later in LCS geüpload.</span><span class="sxs-lookup"><span data-stu-id="33738-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="33738-116">Typ 'Voorbeeldmodelconfiguratie' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33738-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="33738-117">Voorbeeldmodelconfiguratie</span><span class="sxs-lookup"><span data-stu-id="33738-117">Sample model configuration</span></span>  
3. <span data-ttu-id="33738-118">Typ 'Voorbeeldmodelconfiguratie' in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="33738-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="33738-119">Voorbeeldmodelconfiguratie</span><span class="sxs-lookup"><span data-stu-id="33738-119">Sample model configuration</span></span>  
4. <span data-ttu-id="33738-120">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="33738-120">Click Create configuration.</span></span>
5. <span data-ttu-id="33738-121">Klik op Modelontwerper.</span><span class="sxs-lookup"><span data-stu-id="33738-121">Click Model designer.</span></span>
6. <span data-ttu-id="33738-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="33738-122">Click New.</span></span>
7. <span data-ttu-id="33738-123">Typ 'Invoerpunt' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33738-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="33738-124">Invoerpunt</span><span class="sxs-lookup"><span data-stu-id="33738-124">Entry point</span></span>  
8. <span data-ttu-id="33738-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="33738-125">Click Add.</span></span>
9. <span data-ttu-id="33738-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="33738-126">Click Save.</span></span>
10. <span data-ttu-id="33738-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33738-127">Close the page.</span></span>
11. <span data-ttu-id="33738-128">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="33738-128">Click Change status.</span></span>
12. <span data-ttu-id="33738-129">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="33738-129">Click Complete.</span></span>
13. <span data-ttu-id="33738-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33738-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="33738-131">Een nieuwe opslagplaats registreren</span><span class="sxs-lookup"><span data-stu-id="33738-131">Register a new  repository</span></span>
1. <span data-ttu-id="33738-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33738-132">Close the page.</span></span>
2. <span data-ttu-id="33738-133">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="33738-133">Click Repositories.</span></span>
    * <span data-ttu-id="33738-134">Hiermee kunt u de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc openen.</span><span class="sxs-lookup"><span data-stu-id="33738-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="33738-135">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="33738-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="33738-136">Hiermee kunt u een nieuwe opslagplaats toevoegen.</span><span class="sxs-lookup"><span data-stu-id="33738-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="33738-137">Selecteer LCS in het veld Type opslagplaats van configuratie.</span><span class="sxs-lookup"><span data-stu-id="33738-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="33738-138">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="33738-138">Click Create repository.</span></span>
6. <span data-ttu-id="33738-139">Typ of selecteer een waarde in het veld Project.</span><span class="sxs-lookup"><span data-stu-id="33738-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="33738-140">Selecteer het gewenste LCS-project.</span><span class="sxs-lookup"><span data-stu-id="33738-140">Select the desired LCS project.</span></span> <span data-ttu-id="33738-141">U moet toegang tot het project hebben.</span><span class="sxs-lookup"><span data-stu-id="33738-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="33738-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33738-142">Click OK.</span></span>
    * <span data-ttu-id="33738-143">Voer een nieuwe opslagplaats in.</span><span class="sxs-lookup"><span data-stu-id="33738-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="33738-144">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="33738-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="33738-145">Selecteer de LCS-opslagplaatsrecord.</span><span class="sxs-lookup"><span data-stu-id="33738-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="33738-146">Een geregistreerde opslagplaats wordt door de huidige provide gemarkeerd, wat betekent dat de enige configuraties in bezit van die provider in deze opslagplaats kunnen worden geplaatst en daarom naar het geselecteerde LCS-project kunnen worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="33738-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="33738-147">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="33738-147">Click Open.</span></span>
    * <span data-ttu-id="33738-148">Open de opslagplaats om de lijst met ER-configuraties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="33738-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="33738-149">De lijst is leeg als dit project nog niet voor delen van ER-configuraties is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="33738-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="33738-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33738-150">Close the page.</span></span>
11. <span data-ttu-id="33738-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33738-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="33738-152">Configuratie naar LCS uploaden</span><span class="sxs-lookup"><span data-stu-id="33738-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="33738-153">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="33738-153">Click Configurations.</span></span>
2. <span data-ttu-id="33738-154">Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33738-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="33738-155">Selecteer een gemaakte configuratie die al is voltooid.</span><span class="sxs-lookup"><span data-stu-id="33738-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="33738-156">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="33738-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33738-157">Selecteer de versie van de geselecteerde configuratie met de status ‘Voltooid’.</span><span class="sxs-lookup"><span data-stu-id="33738-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="33738-158">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="33738-158">Click Change status.</span></span>
5. <span data-ttu-id="33738-159">Klik op Delen.</span><span class="sxs-lookup"><span data-stu-id="33738-159">Click Share.</span></span>
    * <span data-ttu-id="33738-160">De configuratiestatus wordt gewijzigd van ‘Voltooid’ in ‘Gedeeld’ wanneer deze wordt gepubliceerd in LCS.</span><span class="sxs-lookup"><span data-stu-id="33738-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="33738-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33738-161">Click OK.</span></span>
7. <span data-ttu-id="33738-162">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="33738-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33738-163">Selecteer de configuratieversie met de status ‘Gedeeld’.</span><span class="sxs-lookup"><span data-stu-id="33738-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="33738-164">De status van de geselecteerde versie is gewijzigd van ‘Voltooid’ in ‘Gedeeld’.</span><span class="sxs-lookup"><span data-stu-id="33738-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="33738-165">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33738-165">Close the page.</span></span>
9. <span data-ttu-id="33738-166">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="33738-166">Click Repositories.</span></span>
    * <span data-ttu-id="33738-167">Hiermee kunt u de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc openen.</span><span class="sxs-lookup"><span data-stu-id="33738-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="33738-168">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="33738-168">Click Open.</span></span>
    * <span data-ttu-id="33738-169">Selecteer de LCS-opslagplaats en open deze.</span><span class="sxs-lookup"><span data-stu-id="33738-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="33738-170">De geselecteerde configuratie wordt getoond als een activum van het geselecteerde LCS-project.</span><span class="sxs-lookup"><span data-stu-id="33738-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="33738-171">Open LCS met https://lcs.dynamics.com. Open een project dat eerder is gebruikt voor opslagplaatsregistratie, open de ‘Activabibliotheek’ van dit project en vouw de inhoud van het activumtype ‘GER-configuratie’ uit; de geüploade ER-configuratie is beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="33738-171">Open LCS using https://lcs.dynamics.com. Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="33738-172">De geüploade LCS-configuratie kan naar een ander Microsoft Dynamics 365 for Finance and Operations-exemplaar worden geïmporteerd als providers toegang tot dit LCS-project hebben.</span><span class="sxs-lookup"><span data-stu-id="33738-172">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations instance if providers have access to this LCS project.</span></span>  


