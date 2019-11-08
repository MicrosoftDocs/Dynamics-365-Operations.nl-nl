---
title: ER-modeltoewijzing in afzonderlijke ER-configuraties beheren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage ER-modeltoewijzingen (Electronic Reporting) kan beheren in aparte ER-configuraties.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcf322973ea5e4afd9c828c3cbd1ebbd9972a964
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182250"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="6f58c-103">ER-modeltoewijzing in afzonderlijke ER-configuraties beheren</span><span class="sxs-lookup"><span data-stu-id="6f58c-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f58c-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage ER-modeltoewijzingen (Electronic Reporting) kan beheren in aparte ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="6f58c-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="6f58c-105">In deze taakbegeleiding maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Voordat u deze taakbegeleiding uitvoert, moet u eerst de stappen uitvoeren in de Taakbegeleiding 'ER Een configuratieprovider maken' en deze als actief markeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="6f58c-106">Omdat ER-configuraties worden gedeeld tussen bedrijven, kunt u deze taakbegeleiding voltooien met behulp van de bedrijfsgegevensset van uw keuze.</span><span class="sxs-lookup"><span data-stu-id="6f58c-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="6f58c-107">De functionaliteit voor deze taakbegeleiding is beschikbaar als u een van de volgende hotfixes hebt geïnstalleerd: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 voor de versie Dynamics AX 7.0 of https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 voor de versie Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="6f58c-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="6f58c-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="6f58c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6f58c-109">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als actief.</span><span class="sxs-lookup"><span data-stu-id="6f58c-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="6f58c-110">Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de taakbegeleiding "Een configuratieprovider maken" en deze als actief markeren uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="6f58c-111">Een nieuwe ER-modelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="6f58c-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="6f58c-112">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="6f58c-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="6f58c-113">Een nieuwe modelconfiguratie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-113">Add a new model configuration.</span></span> <span data-ttu-id="6f58c-114">De naam moet uniek zijn in de structuur van configuraties.</span><span class="sxs-lookup"><span data-stu-id="6f58c-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="6f58c-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6f58c-116">Typ 'Voorbeeldgegevensmodel' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="6f58c-117">Voorbeeldgegevensmodel</span><span class="sxs-lookup"><span data-stu-id="6f58c-117">Sample data model</span></span>  
4. <span data-ttu-id="6f58c-118">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="6f58c-118">Click Create configuration.</span></span>
5. <span data-ttu-id="6f58c-119">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6f58c-119">Click Designer.</span></span>
6. <span data-ttu-id="6f58c-120">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6f58c-121">Typ Basis in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="6f58c-122">Basis</span><span class="sxs-lookup"><span data-stu-id="6f58c-122">Root</span></span>  
8. <span data-ttu-id="6f58c-123">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-123">Click Add.</span></span>
9. <span data-ttu-id="6f58c-124">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="6f58c-125">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6f58c-126">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="6f58c-126">Company</span></span>  
11. <span data-ttu-id="6f58c-127">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-127">Click Add.</span></span>
12. <span data-ttu-id="6f58c-128">Voer in het veld Beschrijving de tekst, omschrijving van de rechtspersoon of het bedrijf in waar een gebruiker tijdens de uitvoering is aangemeld.</span><span class="sxs-lookup"><span data-stu-id="6f58c-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="6f58c-129">Beschrijving van de rechtspersoon of het bedrijf waarin een gebruiker tijdens runtime is aangemeld.</span><span class="sxs-lookup"><span data-stu-id="6f58c-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="6f58c-130">Klik op Basisverwijzing.</span><span class="sxs-lookup"><span data-stu-id="6f58c-130">Click Root reference.</span></span>
14. <span data-ttu-id="6f58c-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-131">Click OK.</span></span>
15. <span data-ttu-id="6f58c-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6f58c-132">Click Save.</span></span>
16. <span data-ttu-id="6f58c-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-133">Close the page.</span></span>
17. <span data-ttu-id="6f58c-134">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-134">Click Change status.</span></span>
18. <span data-ttu-id="6f58c-135">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="6f58c-135">Click Complete.</span></span>
19. <span data-ttu-id="6f58c-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="6f58c-137">Een nieuwe ER-modelgegevensmodelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="6f58c-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="6f58c-138">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6f58c-139">Voer in het veld Nieuw 'Modeltoewijzing gebaseerd op gegevensmodel Voorbeeldgegevensmodel' in.</span><span class="sxs-lookup"><span data-stu-id="6f58c-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="6f58c-140">Typ 'Voorbeeldtoewijzing' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="6f58c-141">Voorbeeldtoewijzing</span><span class="sxs-lookup"><span data-stu-id="6f58c-141">Sample mapping</span></span>  
4. <span data-ttu-id="6f58c-142">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="6f58c-142">Click Create configuration.</span></span>
5. <span data-ttu-id="6f58c-143">Vouw de sectie Vereisten uit.</span><span class="sxs-lookup"><span data-stu-id="6f58c-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="6f58c-144">Houd er rekening mee dat de groep implementatievereisten automatisch is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="6f58c-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="6f58c-145">De groep bevat de vereiste component die verwijst naar de bovenliggende gegevensmodelconfiguratie en is gemarkeerd als Implementatie.</span><span class="sxs-lookup"><span data-stu-id="6f58c-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="6f58c-146">Dit betekent dat deze voorbeeldmodeltoewijzingsconfiguratie wordt beschouwd als de implementatie van het gegevensmodel, Voorbeeldgegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="6f58c-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="6f58c-147">Dit onderdeel dwingt ER daarom de modeltoewijzingsconfiguratie, Voorbeeldtoewijzing, te downloaden uit een ER-opslagplaats wanneer de modelconfiguratie, Voorbeeldgegevensmodel, wordt gedownload.</span><span class="sxs-lookup"><span data-stu-id="6f58c-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="6f58c-148">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6f58c-148">Click Designer.</span></span>
    * <span data-ttu-id="6f58c-149">De gemaakte modeltoewijzingsconfiguratie bevat een nieuwe lege toewijzing met dezelfde naam als de gemaakte configuratie.</span><span class="sxs-lookup"><span data-stu-id="6f58c-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="6f58c-150">Wanneer een geselecteerde bovenliggende modelconfiguratie modeltoewijzingen bevat, worden deze naar een nieuwe modeltoewijzingsconfiguratie gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="6f58c-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="6f58c-151">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6f58c-151">Click Designer.</span></span>
8. <span data-ttu-id="6f58c-152">Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6f58c-153">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-153">Click Add root.</span></span>
10. <span data-ttu-id="6f58c-154">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6f58c-155">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="6f58c-155">Company</span></span>  
11. <span data-ttu-id="6f58c-156">Typ "CompanyInfo" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="6f58c-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6f58c-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6f58c-157">CompanyInfo</span></span>  
12. <span data-ttu-id="6f58c-158">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-158">Click OK.</span></span>
13. <span data-ttu-id="6f58c-159">Vouw in de structuur 'Bedrijf' uit.</span><span class="sxs-lookup"><span data-stu-id="6f58c-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="6f58c-160">Vouw in de structuur 'Bedrijf\find()' uit.</span><span class="sxs-lookup"><span data-stu-id="6f58c-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="6f58c-161">Selecteer in de structuur 'Bedrijf\find()\Naam'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="6f58c-162">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6f58c-162">Click Bind.</span></span>
17. <span data-ttu-id="6f58c-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6f58c-163">Click Save.</span></span>
18. <span data-ttu-id="6f58c-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-164">Close the page.</span></span>
19. <span data-ttu-id="6f58c-165">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-165">Close the page.</span></span>
20. <span data-ttu-id="6f58c-166">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="6f58c-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="6f58c-167">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="6f58c-167">Click User parameters.</span></span>
22. <span data-ttu-id="6f58c-168">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="6f58c-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-169">Click OK.</span></span>
24. <span data-ttu-id="6f58c-170">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="6f58c-170">Click Edit.</span></span>
25. <span data-ttu-id="6f58c-171">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="6f58c-172">Een nieuwe ER-indelingsconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="6f58c-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="6f58c-173">Selecteer in de structuur 'Voorbeeldgegevensmodel'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6f58c-174">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6f58c-175">Voer in het veld Nieuw 'Indeling gebaseerd op gegevensmodel Voorbeeldgegevensmodel' in.</span><span class="sxs-lookup"><span data-stu-id="6f58c-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6f58c-176">Typ 'Voorbeeldindeling' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="6f58c-177">Voorbeeldindeling</span><span class="sxs-lookup"><span data-stu-id="6f58c-177">Sample format</span></span>  
5. <span data-ttu-id="6f58c-178">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="6f58c-178">Click Create configuration.</span></span>
6. <span data-ttu-id="6f58c-179">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6f58c-179">Click Designer.</span></span>
7. <span data-ttu-id="6f58c-180">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="6f58c-181">Selecteer "Text\String" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6f58c-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="6f58c-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-182">Click OK.</span></span>
10. <span data-ttu-id="6f58c-183">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="6f58c-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="6f58c-184">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="6f58c-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="6f58c-185">Selecteer in de structuur 'model\Bedrijf'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="6f58c-186">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6f58c-186">Click Bind.</span></span>
14. <span data-ttu-id="6f58c-187">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6f58c-187">Click Save.</span></span>
15. <span data-ttu-id="6f58c-188">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-188">Close the page.</span></span>
    * <span data-ttu-id="6f58c-189">Voer de conceptversie van de gemaakte indeling uit voor testdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="6f58c-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="6f58c-190">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-190">Click Run.</span></span>
    * <span data-ttu-id="6f58c-191">Klik op het sneltabblad Versies op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="6f58c-192">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-192">Click OK.</span></span>
    * <span data-ttu-id="6f58c-193">Bekijk de uitvoer die de naam bevat van het bedrijf waarin de gebruiker die deze indelingsconfiguratie uitvoert, is aangemeld.</span><span class="sxs-lookup"><span data-stu-id="6f58c-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="6f58c-194">De gemaakte modeltoewijzingsconfiguratie wordt gebruikt door deze indelingsconfiguratie omdat er slechts één configuratie beschikbaar is die vereiste modeltoewijzingen bevat.</span><span class="sxs-lookup"><span data-stu-id="6f58c-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="6f58c-195">Een alternatieve ER-modelgegevensmodelconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="6f58c-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="6f58c-196">Selecteer in de structuur 'Voorbeeldgegevensmodel'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6f58c-197">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6f58c-198">Voer in het veld Nieuw 'Modeltoewijzing gebaseerd op gegevensmodel Voorbeeldgegevensmodel' in.</span><span class="sxs-lookup"><span data-stu-id="6f58c-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6f58c-199">Typ 'Voorbeeldtoewijzing (alternatief)' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="6f58c-200">Voorbeeldtoewijzing (alternatief)</span><span class="sxs-lookup"><span data-stu-id="6f58c-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="6f58c-201">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="6f58c-201">Click Create configuration.</span></span>
6. <span data-ttu-id="6f58c-202">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6f58c-202">Click Designer.</span></span>
7. <span data-ttu-id="6f58c-203">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6f58c-203">Click Designer.</span></span>
8. <span data-ttu-id="6f58c-204">Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6f58c-205">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-205">Click Add root.</span></span>
10. <span data-ttu-id="6f58c-206">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6f58c-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6f58c-207">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="6f58c-207">Company</span></span>  
11. <span data-ttu-id="6f58c-208">Typ "CompanyInfo" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="6f58c-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6f58c-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6f58c-209">CompanyInfo</span></span>  
12. <span data-ttu-id="6f58c-210">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-210">Click OK.</span></span>
13. <span data-ttu-id="6f58c-211">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="6f58c-211">Click Edit.</span></span>
14. <span data-ttu-id="6f58c-212">Selecteer "String\CONCATENATE" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6f58c-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="6f58c-213">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-213">Click Add function.</span></span>
16. <span data-ttu-id="6f58c-214">Vouw in de structuur 'Bedrijf' uit.</span><span class="sxs-lookup"><span data-stu-id="6f58c-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="6f58c-215">Vouw in de structuur 'Bedrijf\find()' uit.</span><span class="sxs-lookup"><span data-stu-id="6f58c-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="6f58c-216">Selecteer in de structuur 'Bedrijf\find()\Naam'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="6f58c-217">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-217">Click Add data source.</span></span>
20. <span data-ttu-id="6f58c-218">Typ een waarde in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="6f58c-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6f58c-219">CONCATENATE(Bedrijf.'find()'.Naam, ";",</span><span class="sxs-lookup"><span data-stu-id="6f58c-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="6f58c-220">Selecteer in de structuur 'Bedrijf\find()\Bedrijf(Gegevensgebied)'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="6f58c-221">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6f58c-221">Click Add data source.</span></span>
23. <span data-ttu-id="6f58c-222">Typ een waarde in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="6f58c-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6f58c-223">CONCATENATE(Company.'find()'. Naam, ';', Bedrijf.'find()'. Gegevensgebied)</span><span class="sxs-lookup"><span data-stu-id="6f58c-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="6f58c-224">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6f58c-224">Click Save.</span></span>
25. <span data-ttu-id="6f58c-225">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-225">Close the page.</span></span>
26. <span data-ttu-id="6f58c-226">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6f58c-226">Click Save.</span></span>
27. <span data-ttu-id="6f58c-227">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-227">Close the page.</span></span>
28. <span data-ttu-id="6f58c-228">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f58c-228">Close the page.</span></span>
29. <span data-ttu-id="6f58c-229">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="6f58c-230">Een bestaande ER-modeltoewijzingsconfiguratie gebruiken</span><span class="sxs-lookup"><span data-stu-id="6f58c-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="6f58c-231">Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldindeling'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="6f58c-232">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-232">Click Run.</span></span>
    * <span data-ttu-id="6f58c-233">Houd er rekening mee dat de geselecteerde conceptversie van de ER-indelingsconfiguratie kan niet worden uitgevoerd omdat er meer dan één modeltoewijzingsconfiguratie beschikbaar is voor het niet-gedefinieerde gegevensmodel dat is geselecteerd als de gegevensbron van de lopende ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="6f58c-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="6f58c-234">Vervolgens definieert u de alternatieve modeltoewijzingsconfiguratie als de configuratie waaruit modeltoewijzingen worden gebruikt als gegevensbronnen voor het uitvoeren van de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="6f58c-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="6f58c-235">Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing (alternatief)'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="6f58c-236">Selecteer in het veld Standaard voor modeltoewijzing de waarde Ja.</span><span class="sxs-lookup"><span data-stu-id="6f58c-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="6f58c-237">Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldindeling'.</span><span class="sxs-lookup"><span data-stu-id="6f58c-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="6f58c-238">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6f58c-238">Click Run.</span></span>
7. <span data-ttu-id="6f58c-239">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6f58c-239">Click OK.</span></span>
    * <span data-ttu-id="6f58c-240">Houd er rekening mee dat de standaardmodeltoewijzingsconfiguratie door deze indelingsconfiguratie wordt gebruikt voor het genereren van het elektronische document (de gemaakte uitvoer bevat de bedrijfscode).</span><span class="sxs-lookup"><span data-stu-id="6f58c-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  
