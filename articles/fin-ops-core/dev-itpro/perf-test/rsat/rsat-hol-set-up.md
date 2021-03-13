---
title: Zelfstudie over het instellen en installeren van Regression Suite Automation Tool
description: Dit onderwerp is een zelfstudie waarin wordt beschreven hoe u RSAT (Regression Suite Automation Tool) instelt en installeert.
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 46115dc4a46be951517265197f76637ad3e63b78
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036704"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="04e52-103">Zelfstudie over het instellen en installeren van Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="04e52-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="04e52-104">Dit onderwerp is een zelfstudie waarmee u RSAT en de bijbehorende hulpprogramma's kunt instellen en gebruiken.</span><span class="sxs-lookup"><span data-stu-id="04e52-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="04e52-105">Gebruik uw internetbrowser om deze pagina als PDF-bestand te downloaden en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="04e52-106">Belangrijke concepten</span><span class="sxs-lookup"><span data-stu-id="04e52-106">Key concepts</span></span>

- <span data-ttu-id="04e52-107">Begrijp de installatie en de vereiste instellingen voor de verschillende toepassingen die ondersteuning bieden voor RSAT (Regression Suite Automation Tool).</span><span class="sxs-lookup"><span data-stu-id="04e52-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="04e52-108">Begrijp hoe u met de functie Taakregistratie, samen met Microsoft Dynamics Lifecycle Services (LCS) en Microsoft Azure DevOps testcases kunt maken, configureren, uitvoeren, onderzoeken en hiervan rapporten kunt maken.</span><span class="sxs-lookup"><span data-stu-id="04e52-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="04e52-109">Stel functionele gebruikers in staat om zakelijke taken vast te leggen met Taakregistratie en de taakregistraties vervolgens om te zetten in een reeks geautomatiseerde tests zonder broncode te hoeven schrijven.</span><span class="sxs-lookup"><span data-stu-id="04e52-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="04e52-110">Voordat u begint</span><span class="sxs-lookup"><span data-stu-id="04e52-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="04e52-111">Vereisten</span><span class="sxs-lookup"><span data-stu-id="04e52-111">Prerequisites</span></span>

- <span data-ttu-id="04e52-112">Voor deze zelfstudie is een omgeving met Microsoft Dynamics 365 for Finance and Operations 10.0 (april 2019) of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="04e52-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="04e52-113">Voor klanten die Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 gebruiken, wordt Platformupdate 20 (PU20) of hoger ook ondersteund.</span><span class="sxs-lookup"><span data-stu-id="04e52-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="04e52-114">De gebruiker moet over beheerdersrechten voor de omgeving beschikken.</span><span class="sxs-lookup"><span data-stu-id="04e52-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="04e52-115">U moet toegang hebben tot de LCS en Azure DevOps (voorheen Microsoft Visual Studio Team Services \[VSTS\]) van de klanttenant.</span><span class="sxs-lookup"><span data-stu-id="04e52-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="04e52-116">De gebruiker die testsuites maakt en beheert, moet een licentie voor Azure DevOps Test Plans of Test Manager hebben.</span><span class="sxs-lookup"><span data-stu-id="04e52-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="04e52-117">Ook de volgende licenties bieden u toegang tot testplannen:</span><span class="sxs-lookup"><span data-stu-id="04e52-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="04e52-118">Visual Studio Enterprise-licentie</span><span class="sxs-lookup"><span data-stu-id="04e52-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="04e52-119">Visual Studio Test Professional-licentie</span><span class="sxs-lookup"><span data-stu-id="04e52-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="04e52-120">Abonnementslicentie voor MSDN-platforms</span><span class="sxs-lookup"><span data-stu-id="04e52-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="04e52-121">RSAT moet via een webbrowser toegang hebben tot de testomgeving.</span><span class="sxs-lookup"><span data-stu-id="04e52-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="04e52-122">U kunt alleen testparameters genereren en bewerken als u Microsoft Excel hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="04e52-123">Azure DevOps configureren</span><span class="sxs-lookup"><span data-stu-id="04e52-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="04e52-124">Geschiktheid van gebruikers</span><span class="sxs-lookup"><span data-stu-id="04e52-124">User eligibility</span></span>

<span data-ttu-id="04e52-125">Controleer of de gebruiker is gemaakt in Azure DevOps en een abonnementsniveau heeft dat toegang biedt tot Azure Test Plans.</span><span class="sxs-lookup"><span data-stu-id="04e52-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="04e52-126">Een Azure DevOps Test Plans-licentie is alleen vereist als de gebruiker testcases maakt en beheert (dus niet alle RSAT-gebruikers hebben deze licentie nodig).</span><span class="sxs-lookup"><span data-stu-id="04e52-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="04e52-127">Zie [Licentievereisten](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements) voor informatie over de licentievereisten.</span><span class="sxs-lookup"><span data-stu-id="04e52-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="04e52-128">Een nieuw Azure DevOps-project maken</span><span class="sxs-lookup"><span data-stu-id="04e52-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="04e52-129">RSAT gebruikt Azure Devops voor het beheer van testcases en testsuites, rapportage en het onderzoeken van resultaten van testuitvoeringen.</span><span class="sxs-lookup"><span data-stu-id="04e52-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-130">U kunt een bestaand Azure DevOps-project gebruiken.</span><span class="sxs-lookup"><span data-stu-id="04e52-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="04e52-131">Als het bestaande Azure DevOps-project echter zo is ingesteld dat een aangepaste sjabloon wordt gebruikt, wordt het foutbericht Fouten bij VSTS-synchronisatie weergegeven wanneer u testcases vanuit Modelleertool bedrijfsprocessen synchroniseert naar Azure DevOps (zie het gedeelte [De synchronisatie van BPM naar Azure DevOps testen](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="04e52-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="04e52-132">Als de volgende aanbevelingen zijn opgevolgd voor de aangepaste sjabloon, kunt u de testcases synchroniseren naar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="04e52-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="04e52-133">(Deze aanbevolen procedures worden vermeld in het foutbericht.)</span><span class="sxs-lookup"><span data-stu-id="04e52-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="04e52-134">Verwijder geen werkitemtypen of out-of-the-box-velden.</span><span class="sxs-lookup"><span data-stu-id="04e52-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="04e52-135">Verwijder geen status van een werkitemtype.</span><span class="sxs-lookup"><span data-stu-id="04e52-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="04e52-136">Voeg geen vereiste velden toe aan een werkitemtype.</span><span class="sxs-lookup"><span data-stu-id="04e52-136">Do not add any required fields to a work item type.</span></span>

![Foutbericht met een lijst met aanbevolen procedures](./media/setup_rsa_tool_02.png)

<span data-ttu-id="04e52-138">Anders raden we u voor deze zelfstudie aan om een nieuw Azure DevOps-project te maken.</span><span class="sxs-lookup"><span data-stu-id="04e52-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="04e52-139">Zie [Problemen bij synchronisatie naar Modelleertool bedrijfsprocessen met een aangepaste Azure DevOps-processjabloon (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="04e52-140">Open de URL van Azure DevOps (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="04e52-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="04e52-141">Selecteer **Project maken** in de rechterbovenhoek van de Azure DevOps-pagina.</span><span class="sxs-lookup"><span data-stu-id="04e52-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![De knop Project maken](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="04e52-143">Vul de volgende velden in en selecteer **Maken**:</span><span class="sxs-lookup"><span data-stu-id="04e52-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="04e52-144">**Projectnaam**</span><span class="sxs-lookup"><span data-stu-id="04e52-144">**Project name**</span></span>
    - <span data-ttu-id="04e52-145">**Versiebeheer**: selecteer **Team Foundation Version Control**.</span><span class="sxs-lookup"><span data-stu-id="04e52-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="04e52-146">De standaardoptie, **Git**, wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="04e52-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="04e52-147">**Werkitemproces**</span><span class="sxs-lookup"><span data-stu-id="04e52-147">**Work item process**</span></span>

    ![Het dialoogvenster Nieuw project maken](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="04e52-149">Een persoonlijke toegangstoken maken</span><span class="sxs-lookup"><span data-stu-id="04e52-149">Create a personal access token</span></span>

<span data-ttu-id="04e52-150">In deze zelfstudie gebruikt u de LCS-oplossing BPM (Modelleertool bedrijfsprocessen) om een testcase-bibliotheek te maken en uw testcases met Azure DevOps te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="04e52-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="04e52-151">U hebt een persoonlijk toegangstoken nodig om BPM met Azure DevOps te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="04e52-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="04e52-152">Selecteer het profielpictogram in de rechterbovenhoek van de pagina voor uw Azure DevOps-project en selecteer **Beveiliging**.</span><span class="sxs-lookup"><span data-stu-id="04e52-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![De opdracht Beveiliging](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="04e52-154">Selecteer in het linkerdeelvenster onder **Beveiliging** de optie **Persoonlijke toegangstokens**.</span><span class="sxs-lookup"><span data-stu-id="04e52-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="04e52-155">Selecteer vervolgens **Nieuwe token**.</span><span class="sxs-lookup"><span data-stu-id="04e52-155">Then select **New Token**.</span></span>

    ![De knop Nieuwe token op het tabblad Persoonlijke toegangstokens in Gebruikersinstellingen](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="04e52-157">Vul de volgende velden in en selecteer **Maken**:</span><span class="sxs-lookup"><span data-stu-id="04e52-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="04e52-158">**Naam**</span><span class="sxs-lookup"><span data-stu-id="04e52-158">**Name**</span></span>
    - <span data-ttu-id="04e52-159">**Verval (UTC)**: selecteer **Aangepast** en gebruik vervolgens de datumkiezer om de laatste beschikbare datum te selecteren.</span><span class="sxs-lookup"><span data-stu-id="04e52-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="04e52-160">**Bereiken**: selecteer de optie **Volledige toegang**.</span><span class="sxs-lookup"><span data-stu-id="04e52-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Het dialoogvenster Een nieuwe persoonlijke toegangstoken maken](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="04e52-162">Noteer de gemaakte persoonlijke toegangstoken.</span><span class="sxs-lookup"><span data-stu-id="04e52-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="04e52-163">U hebt deze later nodig wanneer u de RSAT-configuratie instelt.</span><span class="sxs-lookup"><span data-stu-id="04e52-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Persoonlijke toegangstoken](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="04e52-165">Het LCS-project configureren</span><span class="sxs-lookup"><span data-stu-id="04e52-165">Configure the LCS project</span></span>

<span data-ttu-id="04e52-166">U hebt een LCS-project (Lifecycle Services) nodig voor de hoofdtestbibliotheek.</span><span class="sxs-lookup"><span data-stu-id="04e52-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="04e52-167">LCS BPM wordt gebruikt als de hoofdbibliotheek voor uw testcases.</span><span class="sxs-lookup"><span data-stu-id="04e52-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="04e52-168">BPM wordt gebruikt om test bibliotheken te beheren en te distribueren voor LCS-projecten.</span><span class="sxs-lookup"><span data-stu-id="04e52-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="04e52-169">Een Microsoft-partner of onafhankelijke softwareleverancier (ISV) die testbibliotheken maakt, brengt testcases in de vorm van BPM-bibliotheken uit.</span><span class="sxs-lookup"><span data-stu-id="04e52-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="04e52-170">In BPM worden testcases ingedeeld op bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04e52-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="04e52-171">In BPM wordt de uitvoeringsvolgorde of -frequentie van uw testdoorloop niet bepaald.</span><span class="sxs-lookup"><span data-stu-id="04e52-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="04e52-172">Deze details worden beheerd in Azure DevOps, zoals later in dit onderwerp wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="04e52-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="04e52-173">Voor uw LCS-project kunt u bestaande klantimplementaties of partnerprojecten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="04e52-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="04e52-174">De CSL-taal bijwerken</span><span class="sxs-lookup"><span data-stu-id="04e52-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-175">Bedrijfsprocessen wordt correct weergegeven in de gebruikersinterface als de LCS-voorkeurstaal is ingesteld op **Engels (Verenigde Staten)**.</span><span class="sxs-lookup"><span data-stu-id="04e52-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="04e52-176">Ga naar het LCS-implementatieproject.</span><span class="sxs-lookup"><span data-stu-id="04e52-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="04e52-177">Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Taalvoorkeur**.</span><span class="sxs-lookup"><span data-stu-id="04e52-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Taalvoorkeur bijwerken](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="04e52-179">Selecteer in het veld **Voorkeurstaal** de optie **Engels (Verenigde Staten)** en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="04e52-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Het tabblad Voorkeurstaal in Gebruikersinstellingen](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="04e52-181">LCS configureren om verbinding te maken met het Azure DevOps-project</span><span class="sxs-lookup"><span data-stu-id="04e52-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="04e52-182">Als u eerder een nieuw Azure DevOps-project hebt gemaakt, configureert u het LCS-project om hiermee verbinding te maken.</span><span class="sxs-lookup"><span data-stu-id="04e52-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="04e52-183">Als uw LCS-project al is verbonden met uw Azure DevOps-project, kunt u doorgaan met het volgende gedeelte.</span><span class="sxs-lookup"><span data-stu-id="04e52-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="04e52-184">Ga naar het LCS-implementatieproject.</span><span class="sxs-lookup"><span data-stu-id="04e52-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="04e52-185">Selecteer de knop **Menu** en vervolgens **Project settings**.</span><span class="sxs-lookup"><span data-stu-id="04e52-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![De opdracht Project settings](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="04e52-187">Selecteer **Visual Studio Team Services** in het linkerdeelvenster en selecteer vervolgens **Setup Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="04e52-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Het tabblad Visual Studio Team Services in Project settings](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="04e52-189">Geef in het veld **Azure DevOps site URL** de URL van de Azure DevOps-site op.</span><span class="sxs-lookup"><span data-stu-id="04e52-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="04e52-190">Voer in het veld **Personal access token** de persoonlijke toegangstoken in die eerder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04e52-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-191">Hoewel VSTS nu bekend staat als Azure DevOps, gebruikt u de oude URL om uw Azure DevOps-project te maken.</span><span class="sxs-lookup"><span data-stu-id="04e52-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="04e52-192">De URL voor Azure DevOps die in deze zelfstudie wordt gebruikt, is bijvoorbeeld `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="04e52-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="04e52-193">In de volgende afbeelding wordt deze echter ingevoerd als `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="04e52-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Stap 1 in Setup Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="04e52-195">Selecteer **Continue**.</span><span class="sxs-lookup"><span data-stu-id="04e52-195">Select **Continue**.</span></span>
6. <span data-ttu-id="04e52-196">Selecteer in het veld **Visual Studio Team Services project** het VSTS-project op de geselecteerde site die moet worden gekoppeld aan het LCS-project.</span><span class="sxs-lookup"><span data-stu-id="04e52-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="04e52-197">Het veld **Process template** is standaard ingesteld op **Agile**.</span><span class="sxs-lookup"><span data-stu-id="04e52-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="04e52-198">Neem voor een aangepaste sjabloon de richtlijn voor de aanbevolen procedure in [Een nieuw Azure DevOps-project maken](#create-a-new-azure-devops-project) door.</span><span class="sxs-lookup"><span data-stu-id="04e52-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="04e52-199">Selecteer vervolgens **Continue**.</span><span class="sxs-lookup"><span data-stu-id="04e52-199">Then select **Continue**.</span></span>

    ![Stap 2 in Setup Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="04e52-201">Controleer de instellingen en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="04e52-201">Review your settings, and then select **Save**.</span></span>

    ![Stap 3 in Setup Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="04e52-203">Selecteer **Authorize** om LCS te autoriseren om namens u toegang tot de geconfigureerde Azure DevOps-site te krijgen en functies in te schakelen die worden geïntegreerd met VSTS.</span><span class="sxs-lookup"><span data-stu-id="04e52-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![De knop Authorize](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="04e52-205">Er wordt een berichtvenster weergegeven waarin wordt aangegeven dat u naar een externe site wordt omgeleid om LCS te autoriseren om namens u verbinding met Visual Studio Team Services te maken.</span><span class="sxs-lookup"><span data-stu-id="04e52-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="04e52-206">Daarnaast wordt gevraagd of u wilt doorgaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-206">Proceed?"</span></span> <span data-ttu-id="04e52-207">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="04e52-207">Select **Yes**.</span></span>

    ![Berichtvenster](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="04e52-209">Selecteer **Accepteren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-209">Select **Accept**.</span></span>

    ![Toegang verlenen](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="04e52-211">Als u geautoriseerd bent als gebruiker, moet u door de UI worden omgeleid naar de pagina met LCS-projectinstellingen.</span><span class="sxs-lookup"><span data-stu-id="04e52-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Geautoriseerde gebruiker](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="04e52-213">Een nieuwe BPM-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="04e52-213">Create a new BPM library</span></span>

1. <span data-ttu-id="04e52-214">Ga naar het LCS-implementatieproject.</span><span class="sxs-lookup"><span data-stu-id="04e52-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="04e52-215">Selecteer de knop **Menu** en vervolgens **Business process modeler**.</span><span class="sxs-lookup"><span data-stu-id="04e52-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![De opdracht Business process modeler](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="04e52-217">Selecteer **New library**.</span><span class="sxs-lookup"><span data-stu-id="04e52-217">Select **New library**.</span></span>

    ![De knop New library](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="04e52-219">Voer in het veld **Library name** een naam in en selecteer **Create**.</span><span class="sxs-lookup"><span data-stu-id="04e52-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="04e52-220">Geef de BPM-bibliotheek voor deze zelfstudie de naam **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="04e52-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Het dialoogvenster Create new library](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="04e52-222">Open de nieuwe BPM-bibliotheek **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="04e52-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="04e52-223">Selecteer het proces **Sample Core Business Process** en selecteer vervolgens **Edit mode** rechts.</span><span class="sxs-lookup"><span data-stu-id="04e52-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![De knop Edit mode](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="04e52-225">Wijzig de waarde van de velden **Name** en **Description** in **Een product maken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="04e52-226">Selecteer **Save**.</span><span class="sxs-lookup"><span data-stu-id="04e52-226">Then select **Save**.</span></span>

    ![De velden Name en Description](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="04e52-228">Omgeving</span><span class="sxs-lookup"><span data-stu-id="04e52-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="04e52-229">Versievereiste</span><span class="sxs-lookup"><span data-stu-id="04e52-229">Version requirement</span></span>

<span data-ttu-id="04e52-230">Een test- of sandbox-omgeving met versie 10 is vereist.</span><span class="sxs-lookup"><span data-stu-id="04e52-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="04e52-231">Voor klanten die versie 7.3 gebruiken, wordt Platformupdate 20 of hoger ook ondersteund.</span><span class="sxs-lookup"><span data-stu-id="04e52-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-232">RSAT moet via een webbrowser toegang hebben tot uw testomgeving.</span><span class="sxs-lookup"><span data-stu-id="04e52-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="04e52-233">Gebruikerscriteria</span><span class="sxs-lookup"><span data-stu-id="04e52-233">User criteria</span></span>

<span data-ttu-id="04e52-234">De gebruiker moet over beheerdersrechten voor deze omgeving beschikken.</span><span class="sxs-lookup"><span data-stu-id="04e52-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="04e52-235">Help-instellingen configureren om verbinding te maken met LCS</span><span class="sxs-lookup"><span data-stu-id="04e52-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="04e52-236">Deze stap is vereist om verbinding te maken met LCS zodat taakregistraties kunnen worden opgeslagen in de juiste BPM-bibliotheek in LCS via de client.</span><span class="sxs-lookup"><span data-stu-id="04e52-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="04e52-237">Open de client.</span><span class="sxs-lookup"><span data-stu-id="04e52-237">Open the client.</span></span>
2. <span data-ttu-id="04e52-238">Ga naar **Systeembeheer \> Instellen \> Systeemparameters**.</span><span class="sxs-lookup"><span data-stu-id="04e52-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="04e52-239">Selecteer op het tabblad **Help** in het veld **Help-configuratie van Lifecycle Services** het betreffende LCS-project (**RSAT** voor deze zelfstudie).</span><span class="sxs-lookup"><span data-stu-id="04e52-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Het veld Help-configuratie van Lifecycle Services op het tabblad Help](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="04e52-241">BPM-bibliotheken worden ingevuld onder het desbetreffende LCS-project.</span><span class="sxs-lookup"><span data-stu-id="04e52-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="04e52-242">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="04e52-242">Select **Save**.</span></span>
5. <span data-ttu-id="04e52-243">Mogelijk moet u de browser vernieuwen om de bijgewerkte Help-inhoud weer te geven.</span><span class="sxs-lookup"><span data-stu-id="04e52-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Melding over het vernieuwen van de browser](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="04e52-245">Taakregistraties</span><span class="sxs-lookup"><span data-stu-id="04e52-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-246">Controleer of al uw taakregistraties starten op het hoofddashboard.</span><span class="sxs-lookup"><span data-stu-id="04e52-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="04e52-247">Houd afzonderlijke opnamen kort en concentreer u op één bedrijfstaak, zoals het maken van een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="04e52-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="04e52-248">Een taakregistratie maken en opslaan in de BPM-bibliotheek</span><span class="sxs-lookup"><span data-stu-id="04e52-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="04e52-249">Maak een bijbehorende taakregistratie die u kunt koppelen aan het eenvoudige bedrijfsproces dat in de nieuwe BPM-bibliotheek is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04e52-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="04e52-250">Open de client.</span><span class="sxs-lookup"><span data-stu-id="04e52-250">Open the client.</span></span>
2. <span data-ttu-id="04e52-251">Selecteer op het hoofddashboard de knop **Instellingen** (het tandwielsymbool) en selecteer **Taakregistratie**.</span><span class="sxs-lookup"><span data-stu-id="04e52-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Taakrecorder selecteren in het menu Instellingen](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="04e52-253">Selecteer **Registratie maken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-253">Select **Create recording**.</span></span>

    ![De knop Registratie maken](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="04e52-255">Vul de velden **Naam van registratie** en **Omschrijving van registratie** in en selecteer **Starten**.</span><span class="sxs-lookup"><span data-stu-id="04e52-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![De velden Naam van registratie en Omschrijving van registratie](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="04e52-257">Registreer de stappen voor het maken van een product.</span><span class="sxs-lookup"><span data-stu-id="04e52-257">Record the steps for creating a product.</span></span> <span data-ttu-id="04e52-258">Wanneer u klaar bent, selecteert u **Stoppen** om de registratie te stoppen.</span><span class="sxs-lookup"><span data-stu-id="04e52-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Stappen voor het maken van een product](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="04e52-260">Selecteer **Opslaan in Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="04e52-260">Select **Save to Lifecycle Services**.</span></span>

    ![Taakregistratie opslaan in Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="04e52-262">Bibliotheekgegevens worden vanuit LCS geladen.</span><span class="sxs-lookup"><span data-stu-id="04e52-262">Library information is loaded from LCS.</span></span>

    ![Bibliotheekgegevens laden](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="04e52-264">Selecteer de BPM-bibliotheek waaraan u de taakregistratie wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="04e52-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="04e52-265">Selecteer voor deze zelfstudie de BPM-bibliotheek **RSAT** die eerder is gemaakt en het bedrijfsproces **Een product maken** daaronder.</span><span class="sxs-lookup"><span data-stu-id="04e52-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="04e52-266">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e52-266">Then select **OK**.</span></span>

    ![De taakregistratie koppelen aan een BPM-bibliotheek en een bedrijfsproces](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="04e52-268">Het bericht Opgeslagen naar Lifecycle Services wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04e52-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Bericht over de opslag naar LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="04e52-270">Voer de volgende stappen uit als u de taakregistratie lokaal wilt opslaan en vervolgens wilt uploaden naar BPM via LCS:</span><span class="sxs-lookup"><span data-stu-id="04e52-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="04e52-271">Als de registratie is voltooid, selecteert u **Opslaan op deze pc**.</span><span class="sxs-lookup"><span data-stu-id="04e52-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Opslaan op deze pc](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="04e52-273">Selecteer in de meldingsbalk van de browser de optie **Opslaan** of **Opslaan als** om het bestand op uw lokale computer op te slaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Meldingsbalk](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="04e52-275">Ga naar de BPM-bibliotheek **RSAT** en selecteer het bedrijfsproces waarvoor u de taakregistratie wilt opslaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="04e52-276">Selecteer op het tabblad **Overzicht** de optie **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="04e52-276">On the **Overview** tab, select **Upload**.</span></span>

        ![De knop Uploaden](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="04e52-278">Selecteer **Bladeren** en selecteer het AXTR-bestand dat u eerder hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="04e52-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="04e52-279">Selecteer vervolgens **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="04e52-279">Then select **Upload**.</span></span>

        ![Het AXTR-bestand selecteren om te uploaden](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="04e52-281">De synchronisatie van BPM naar Azure DevOps testen</span><span class="sxs-lookup"><span data-stu-id="04e52-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="04e52-282">Nu een taakregistratie aan het bedrijfsproces is gekoppeld, moet u controleren of het bedrijfs proces en de gekoppelde taakregistratie naar Azure DevOps kunnen worden gesynchroniseerd als een functie en een testcase (respectievelijk) met behulp van de VSTS-synchronisatiefunctie in LCS.</span><span class="sxs-lookup"><span data-stu-id="04e52-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-283">Welk bijbehorend type werkitem in Azure DevOps wordt gemaakt, is afhankelijk van de processjabloon die u hebt geselecteerd toen u het LCS-project configureerde met Azure DevOps, zoals wordt beschreven in het gedeelte [Een nieuw Azure DevOps-project maken](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="04e52-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="04e52-284">Ga naar de BPM-bibliotheek en open de bibliotheek **RSAT** die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04e52-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="04e52-285">Selecteer de knop met het weglatingsteken (**...**) en selecteer **VSTS synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![De opdracht VSTS synchroniseren](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="04e52-287">Als de VSTS-synchronisatie is voltooid, wordt het tabblad **Vereisten** links weergegeven met het bijbehorende Azure DevOps-werkitem.</span><span class="sxs-lookup"><span data-stu-id="04e52-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-288">Het werkitem dat in Azure DevOps wordt gemaakt, heeft de BPM-bibliotheeknaam als titelvoorvoegsel.</span><span class="sxs-lookup"><span data-stu-id="04e52-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Het tabblad Vereisten](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="04e52-290">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="04e52-290">Refresh the page.</span></span>
4. <span data-ttu-id="04e52-291">Selecteer de knop met het weglatingsteken (**...**). De extra optie **Testcases synchroniseren** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04e52-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="04e52-292">Selecteer deze optie.</span><span class="sxs-lookup"><span data-stu-id="04e52-292">Select this option.</span></span>

    ![De opdracht Testcases synchroniseren](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="04e52-294">Als de optie **Testcases synchroniseren** niet beschikbaar is als u de pagina hebt vernieuwd, gaat u naar de hoofdpagina voor BPM en selecteert u **Testcases synchroniseren** voor de hele bibliotheek zelf.</span><span class="sxs-lookup"><span data-stu-id="04e52-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="04e52-295">Op deze manier dwingt u op effectieve wijze een synchronisatie af voor de hele bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="04e52-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Testcases synchroniseren selecteren voor de hele bibliotheek](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="04e52-297">Als de synchronisatie van testcases is voltooid, wordt een nieuwe testcase gemaakt op het tabblad **Vereisten**.</span><span class="sxs-lookup"><span data-stu-id="04e52-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Nieuwe testcase op het tabblad Vereisten](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="04e52-299">Ga naar uw Azure DevOps-project en selecteer **Borden \> Werkitems**.</span><span class="sxs-lookup"><span data-stu-id="04e52-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![De opdracht Werkitems onder Borden](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="04e52-301">Controleer of het werkitem en de testcase die u via BPM-synchronisatie hebt gemaakt, bestaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Werkitem en testcase](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="04e52-303">RSAT installeren en configureren</span><span class="sxs-lookup"><span data-stu-id="04e52-303">Install and Configure RSAT</span></span>

<span data-ttu-id="04e52-304">RSAT kan worden geïnstalleerd op elke computer waarop Windows 10 wordt uitgevoerd en waarmee verbinding kan worden gemaakt met de omgeving via een webbrowser (Internet Explorer of Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="04e52-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-305">Voordat u een nieuwe versie van het hulpprogramma installeert, is het raadzaam om de vorige versie te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="04e52-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="04e52-306">Een verificatiecertificaat installeren</span><span class="sxs-lookup"><span data-stu-id="04e52-306">Install an authentication certificate</span></span>

<span data-ttu-id="04e52-307">Als u verificatie wilt inschakelen, moet u een certificaat genereren en installeren op de computer waarop RSAT wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="04e52-308">Een certificaat genereren</span><span class="sxs-lookup"><span data-stu-id="04e52-308">Generate a certificate</span></span>

1. <span data-ttu-id="04e52-309">Als u een certificaatbestand wilt genereren, opent u een Microsoft Windows PowerShell-venster als beheerder en voert u de volgende opdracht uit.</span><span class="sxs-lookup"><span data-stu-id="04e52-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="04e52-310">Open certificaatbeheer door **certlm.msc** in te voeren in het dialoogvenster **Uitvoeren** en controleer of het certificaat **D365 Automated testing certificate** is gemaakt onder **Persoonlijk \> Certificaten**.</span><span class="sxs-lookup"><span data-stu-id="04e52-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-311">Voer **certlm.msc** in en niet **certmgr.msc**, aangezien de certificaten zijn opgeslagen op de lokale computer.</span><span class="sxs-lookup"><span data-stu-id="04e52-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Het certificaat D365 Automated testing certificate](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="04e52-313">Klik met de rechtermuisknop op het certificaat en selecteer **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="04e52-314">Ga naar **Vertrouwde basiscertificeringsinstanties \> Certificaten**.</span><span class="sxs-lookup"><span data-stu-id="04e52-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![De map Certificaten onder de map Vertrouwde basiscertificeringsinstanties](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="04e52-316">Selecteer in het menu **Actie** de optie **Plakken** om het certificaat naar de locatie **Vertrouwde basiscertificeringsinstanties** te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="04e52-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![De opdracht Plakken in het menu Actie](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="04e52-318">Om de vingerafdruk van het geïnstalleerde certificaat op te halen, zonder spaties of speciale tekens, opent u een Windows PowerShell-venster als beheerder en voert u de volgende opdrachten uit.</span><span class="sxs-lookup"><span data-stu-id="04e52-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="04e52-319">Sla de vingerafdruk op omdat u deze later nodig hebt wanneer u de WIF-bestanden voor AOS (Application Object Server) bijwerkt en de RSAT-configuratie instelt.</span><span class="sxs-lookup"><span data-stu-id="04e52-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="04e52-320">De AOS-computer configureren om de verbinding te vertrouwen</span><span class="sxs-lookup"><span data-stu-id="04e52-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="04e52-321">Als de omgeving een Tier 2+-omgeving is, moet de vingerafdruk van het certificaat in het bestand wif.config worden bijgewerkt voor **alle** AOS-computers voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="04e52-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="04e52-322">Breng een RDP-verbinding (Remote Desktop Protocol) tot stand met de AOS-computer.</span><span class="sxs-lookup"><span data-stu-id="04e52-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="04e52-323">Details voor aanmelden zijn beschikbaar op de pagina met omgevingsdetails in LCS.</span><span class="sxs-lookup"><span data-stu-id="04e52-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="04e52-324">Open Microsoft Internet Information Services (IIS) en vind **AOSService** in de lijst met sites.</span><span class="sxs-lookup"><span data-stu-id="04e52-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService in de lijst met sites](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="04e52-326">Klik met de rechtermuisknop op **Verkennen** om de map **\<Drive\>: \\AosService\\WebRoot** te openen.</span><span class="sxs-lookup"><span data-stu-id="04e52-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="04e52-327">Zoek het bestand **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="04e52-327">Find the **wif.config** file.</span></span>

    ![Wif.config-bestand in de map WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="04e52-329">Werk het bestand **wif.config** bij door een nieuwe instantievermelding en -naam toe te voegen voor uw certificaat, zoals in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="04e52-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="04e52-330">Als meerdere gebruikers dezelfde toepassing gebruiken, moet iedere gebruiker afzonderlijke vingerafdrukken genereren en moeten alle vingerafdrukken worden toegevoegd aan de sectie **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="04e52-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="04e52-331">Als er meer dan één AOS-computer is, herhaalt u stap 3 en 4 voor elke extra computer.</span><span class="sxs-lookup"><span data-stu-id="04e52-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-332">In tegenstelling tot oudere Tier 2-omgevingen worden nieuwe Tier 2-omgevingen geïmplementeerd met twee AOS-exemplaren.</span><span class="sxs-lookup"><span data-stu-id="04e52-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="04e52-333">Voer **iisreset** uit op alle AOS-computers.</span><span class="sxs-lookup"><span data-stu-id="04e52-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-334">Als u niet beschikt over beheerdersrechten om **iisreset** uit te voeren op een Tier 1-computer, selecteert u op de pagina Omgevingsdetails in LCS de optie Onderhouden > Services opnieuw starten.</span><span class="sxs-lookup"><span data-stu-id="04e52-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="04e52-335">Tier 2+-omgeving</span><span class="sxs-lookup"><span data-stu-id="04e52-335">Tier 2+ environment</span></span>

<span data-ttu-id="04e52-336">Als een Tier 2+-omgeving (standaardacceptatietest voor sandbox of hoger) wordt gebruikt, verifieert of configureert u de volgende registerinstelling op de computer waarop RSAT is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="04e52-337">Deze stap is vereist omdat u zo verificatie- of RSAT-verbindingsfouten kunt voorkomen.</span><span class="sxs-lookup"><span data-stu-id="04e52-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="04e52-338">RSAT installeren</span><span class="sxs-lookup"><span data-stu-id="04e52-338">Install RSAT</span></span>

1. <span data-ttu-id="04e52-339">Ga naar <https://www.microsoft.com/download/details.aspx?id=57357> en selecteer **Downloaden**.</span><span class="sxs-lookup"><span data-stu-id="04e52-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="04e52-340">Selecteer alle bestanden en vervolgens **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="04e52-340">Select all the files, and then select **Next**.</span></span>

    ![Alle bestanden selecteren](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="04e52-342">Dubbelklik op het MSI-pakket om het installatieprogramma uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="04e52-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="04e52-343">Nadat de installatie is voltooid, selecteert u **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="04e52-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT-installatiebestand](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="04e52-345">Selenium- en browserstuurprogramma's installeren</span><span class="sxs-lookup"><span data-stu-id="04e52-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="04e52-346">In oudere versies van RSAT moest u Selenium- en browserstuurprogramma's installeren.</span><span class="sxs-lookup"><span data-stu-id="04e52-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="04e52-347">U hoeft deze stuurprogramma's niet meer te installeren omdat deze automatisch worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="04e52-348">De eerste keer dat u RSAT opent, wordt u gevraagd Selenium automatisch te downloaden en te installeren.</span><span class="sxs-lookup"><span data-stu-id="04e52-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="04e52-349">Zie het gedeelte [RSAT configureren](#configure-rsat) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="04e52-350">Voordat u een testcase kunt uitvoeren, wordt u gevraagd om automatisch het browserstuurprogramma te downloaden en te installeren dat hoort bij de standaardbrowser die is geselecteerd in de RSAT-configuratie.</span><span class="sxs-lookup"><span data-stu-id="04e52-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="04e52-351">Zie het gedeelte [Testcases laden en uitvoeren](#load-and-run-test-cases) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="04e52-352">Aan de slag met RSAT</span><span class="sxs-lookup"><span data-stu-id="04e52-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="04e52-353">Een testplan en testsuites maken</span><span class="sxs-lookup"><span data-stu-id="04e52-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="04e52-354">Ga naar het Azure DevOps-project en selecteer **Testplannen**.</span><span class="sxs-lookup"><span data-stu-id="04e52-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![De opdracht Testplannen](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="04e52-356">Selecteer **Nieuw testplan**.</span><span class="sxs-lookup"><span data-stu-id="04e52-356">Select **New Test Plan**.</span></span>

    ![De knop Nieuw testplan](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="04e52-358">Vul het veld **Naam** in en selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="04e52-359">Geef het testplan voor deze zelfstudie de naam **RSAT-testplan**.</span><span class="sxs-lookup"><span data-stu-id="04e52-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Het dialoogvenster Nieuw testplan](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="04e52-361">Selecteer het plusteken (**+**) en selecteer **Statische suite** om een statische suite te maken onder het nieuwe testplan.</span><span class="sxs-lookup"><span data-stu-id="04e52-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="04e52-362">Geef de nieuwe testsuite de naam **T01 – Maken naar voorraad**.</span><span class="sxs-lookup"><span data-stu-id="04e52-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-363">U kunt ook een suite op basis van query's maken, als u wilt dat de nieuwe testcases vanuit BPM automatisch in de RSAT-testsuite worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="04e52-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Een statische suite maken](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="04e52-365">Testcases koppelen aan testsuites</span><span class="sxs-lookup"><span data-stu-id="04e52-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="04e52-366">Selecteer **Bestaande toevoegen** rechts om bestaande testcases toe te voegen aan de testsuite.</span><span class="sxs-lookup"><span data-stu-id="04e52-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![De knop Bestaande toevoegen](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="04e52-368">Selecteer op de pagina **Testcases toevoegen aan suite** de optie **Query uitvoeren** en selecteer de testcase die u wilt toevoegen aan de testsuite.</span><span class="sxs-lookup"><span data-stu-id="04e52-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="04e52-369">Selecteer voor deze zelfstudie de testcase **Een nieuw product maken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="04e52-370">Selecteer **Testcases toevoegen** in de rechterbenedenhoek van de pagina (deze knop wordt niet weergegeven in de volgende afbeelding).</span><span class="sxs-lookup"><span data-stu-id="04e52-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![De knop Query uitvoeren](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="04e52-372">De testcase wordt toegevoegd aan de testsuite **T01-Maken naar voorraad**.</span><span class="sxs-lookup"><span data-stu-id="04e52-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testcase toegevoegd aan de testsuite](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="04e52-374">RSAT configureren</span><span class="sxs-lookup"><span data-stu-id="04e52-374">Configure RSAT</span></span>

1. <span data-ttu-id="04e52-375">Open RSAT.</span><span class="sxs-lookup"><span data-stu-id="04e52-375">Open RSAT.</span></span>

    ![RSAT-pictogram](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="04e52-377">Er wordt een waarschuwingsbericht weergegeven dat Selenium vereist is voor Regression Suite Automation Tool en u wordt gevraagd of u Selenium automatisch wilt downloaden en installeren.</span><span class="sxs-lookup"><span data-stu-id="04e52-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="04e52-378">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="04e52-378">Select **Yes**.</span></span>

    ![Waarschuwingsbericht dat voor Regression Suite Automation Tool Selenium is vereist](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="04e52-380">Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en vul in het dialoogvenster dat wordt weergegeven de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="04e52-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="04e52-381">**Azure DevOps Url** – Voer de URL van uw Azure DevOps-project in, bijvoorbeeld `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="04e52-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="04e52-382">**Toegangstoken** – Voer de toegangstoken in op basis waarvan door het hulpprogramma verbinding kan orden gemaakt met Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="04e52-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="04e52-383">Gebruik de persoonlijke toegangstoken die u eerder in deze zelfstudie hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04e52-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="04e52-384">Zie [Toegang verifiëren met persoonlijke toegangstokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="04e52-385">**Projectnaam**: selecteer de naam van uw Azure DevOps-project.</span><span class="sxs-lookup"><span data-stu-id="04e52-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="04e52-386">**Testplan**: selecteer het Azure DevOps-testplan dat uw testcases bevat.</span><span class="sxs-lookup"><span data-stu-id="04e52-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="04e52-387">Zie [Testplannen en testsuites maken](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="04e52-388">Nadat u een testplan hebt geselecteerd, selecteert u **Verbinding testen** om de verbinding met Azure DevOps te testen.</span><span class="sxs-lookup"><span data-stu-id="04e52-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="04e52-389">**Hostnaam**: voer de hostnaam in van de testomgeving, zoals **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="04e52-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="04e52-390">Neem het voorvoegsel **https://** of **http://** niet op.</span><span class="sxs-lookup"><span data-stu-id="04e52-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="04e52-391">**SOAP-hostnaam**: voer de naam van de SOAP-host van de testomgeving in.</span><span class="sxs-lookup"><span data-stu-id="04e52-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="04e52-392">Meestal komt de SOAP-hostnaam overeen met de hostnaam, maar heeft deze het achtervoegsel **soap**.</span><span class="sxs-lookup"><span data-stu-id="04e52-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="04e52-393">Hier is een voorbeeld: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="04e52-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="04e52-394">Neem het voorvoegsel **https://** of **http://** niet op.</span><span class="sxs-lookup"><span data-stu-id="04e52-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="04e52-395">Als u de hostnaam en de SOAP-hostnaam wilt vinden, opent u IIS Manager, klikt u met de rechtermuisknop op **Sites \> AOSService** en selecteert u **Bindingen bewerken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="04e52-396">De kolom **Hostnaam** bevat de hostnaam en SOAP-hostnaam (de SOAP-hostnaam bevat het achtervoegsel **soap** in de URL).</span><span class="sxs-lookup"><span data-stu-id="04e52-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Hostnaam en SOAP-hostnaam in de kolom Hostnaam](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="04e52-398">**Gebruikersnaam beheerder**: voer het e-mailadres van een beheerder in de testomgeving in.</span><span class="sxs-lookup"><span data-stu-id="04e52-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="04e52-399">**Vingerafdruk**: voer de vingerafdruk van het verificatiecertificaat in, zoals eerder in deze zelfstudie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="04e52-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="04e52-400">**Werkmap**: geef de maplocatie voor het opslaan van testautomatiseringsbestanden op, zoals Excel-testgegevensbestanden.</span><span class="sxs-lookup"><span data-stu-id="04e52-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="04e52-401">U kunt bijvoorbeeld **C:\\Temp\\RegressionTool** invoeren of selecteren.</span><span class="sxs-lookup"><span data-stu-id="04e52-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="04e52-402">Als de naam van de map spaties bevat, mislukt de uitvoering omdat de map in dat geval niet wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="04e52-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="04e52-403">Dit is een bekend probleem dat moet worden opgelost in de nieuwste versie van het hulpprogramma.</span><span class="sxs-lookup"><span data-stu-id="04e52-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="04e52-404">**Standaardbrowser**: selecteer **Internet Explorer** of **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="04e52-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="04e52-405">Zorg dat de juiste browserstuurprogramma's zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="04e52-406">**Time-out testuitvoering**: geef de time-outperiode in minuten op voor testuitvoeringen.</span><span class="sxs-lookup"><span data-stu-id="04e52-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="04e52-407">Wanneer de time-outperiode is verstreken, worden alle actieve vensters gesloten en mislukken lopende testcases.</span><span class="sxs-lookup"><span data-stu-id="04e52-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="04e52-408">**Time-out van testactie**: in dit veld wordt de time-outperiode in minuten voor serveraanvragen in de Finance and Operation-omgeving beheerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="04e52-409">Meestal volstaat de standaardwaarde (2 minuten).</span><span class="sxs-lookup"><span data-stu-id="04e52-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="04e52-410">Voor langzamere omgevingen kunt u echter de waarde verhogen als er fouten optreden die betrekking hebben op time-outs.</span><span class="sxs-lookup"><span data-stu-id="04e52-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="04e52-411">**Bedrijfsnaam**: voer de bedrijfsnaam in die moet worden gebruikt als uw standaardbedrijf wanneer Excel-parameterbestanden worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04e52-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="04e52-412">U kunt het bedrijf later wijzigen door het Excel-parameterbestand te bewerken.</span><span class="sxs-lookup"><span data-stu-id="04e52-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Het dialoogvenster Instellingen](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="04e52-414">Selecteer **Toepassen** om de instellingen toe te passen en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="04e52-415">Als u de huidige instellingen wilt opslaan in een configuratiebestand op uw computer, selecteert u **Opslaan als**.</span><span class="sxs-lookup"><span data-stu-id="04e52-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="04e52-416">Als u uw huidige instellingen wilt herstellen op basis van een configuratiebestand op uw computer, selecteert u **Openen**.</span><span class="sxs-lookup"><span data-stu-id="04e52-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="04e52-417">Selecteer **Sluiten** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="04e52-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="04e52-418">Testcases laden en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="04e52-418">Load and run test cases</span></span>

1. <span data-ttu-id="04e52-419">Selecteer **Laden** om het **RSAT-testplan** te laden vanuit het Azure DevOps-project.</span><span class="sxs-lookup"><span data-stu-id="04e52-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![De knop Laden](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="04e52-421">Selecteer de testcase **Een nieuw product laden** vanuit de testsuite en selecteer vervolgens **Nieuw \> Testuitvoering en parameterbestanden genereren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![De opdracht Testuitvoering en parameterbestanden genereren in het menu Nieuw](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="04e52-423">Het Excel-parameterbestand wordt gemaakt in de lokale map die u hebt opgegeven in de RSAT-configuratie (bijvoorbeeld **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="04e52-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Het gemaakte Excel-parameterbestand](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="04e52-425">Selecteer **Uploaden** als u de parameterbestanden wilt opslaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="04e52-426">Testautomatiseringsbestanden van alle geselecteerde testcases worden voor toekomstig gebruik naar Azure DevOps geüpload.</span><span class="sxs-lookup"><span data-stu-id="04e52-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="04e52-427">(Deze bestanden omvatten Excel-testparameterbestanden.)</span><span class="sxs-lookup"><span data-stu-id="04e52-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="04e52-428">Op deze manier kunt u **Laden** selecteren om de parameterbestanden (en automatiseringsbestanden) van de testcase direct vanuit Azure DevOps te laden.</span><span class="sxs-lookup"><span data-stu-id="04e52-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="04e52-429">U hoeft de parameterbestanden niet opnieuw te genereren.</span><span class="sxs-lookup"><span data-stu-id="04e52-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="04e52-430">Deze benadering wordt later belangrijk, wanneer u de wijzigingen in het parameterbestand wilt behouden en niet wilt dat ze worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="04e52-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="04e52-431">Als u wilt controleren of de automatiseringsbestanden en parameterbestanden in Azure DevOps zijn opgeslagen, gaat u naar het Azure DevOps-project, selecteert u **Borden \> WerkItems** en selecteert u vervolgens **Een nieuw product maken** .</span><span class="sxs-lookup"><span data-stu-id="04e52-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="04e52-432">Op het tabblad **Bijlagen** ziet u vier bestanden:</span><span class="sxs-lookup"><span data-stu-id="04e52-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="04e52-433">**.cs** – C\#-automatiseringsbestand</span><span class="sxs-lookup"><span data-stu-id="04e52-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="04e52-434">**.dll** – Gecompileerd automatiseringsbestand als een assembly</span><span class="sxs-lookup"><span data-stu-id="04e52-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="04e52-435">**.xlsx** – Excel-parameterbestand</span><span class="sxs-lookup"><span data-stu-id="04e52-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="04e52-436">**.xml** – Registratiebestand</span><span class="sxs-lookup"><span data-stu-id="04e52-436">**.xml** – Recording file</span></span>

    ![Bestanden op het tabblad Bijlagen](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="04e52-438">Selecteer de testcase die u wilt uitvoeren en selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-439">Als u Internet Explorer gebruikt, moet u er voordat u testcases uitvoert voor zorgen dat de bureaubladresolutie is ingesteld op **100%** in **Windows-beeldscherminstellingen \> Schaal en lay-out**.</span><span class="sxs-lookup"><span data-stu-id="04e52-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="04e52-440">Als u deze instelling niet kunt wijzigen op een virtuele machine (VM), wijzigt u deze op de client (laptop) waarvan u de VM wilt openen.</span><span class="sxs-lookup"><span data-stu-id="04e52-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="04e52-441">De resolutie-instellingen worden vervolgens overgenomen door de beeldscherminstellingen van de VM.</span><span class="sxs-lookup"><span data-stu-id="04e52-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Bureaubladresolutie ingesteld op 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="04e52-443">Als de browserstuurprogramma's niet op het systeem zijn geïnstalleerd, wordt er een waarschuwingsbericht weergegeven dat u voor deze bewerking stuurprogramma \<browser name\> nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="04e52-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="04e52-444">Daarnaast wordt u gevraagd of u het automatisch nu wilt downloaden en installeren?</span><span class="sxs-lookup"><span data-stu-id="04e52-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="04e52-445">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="04e52-445">Select **Yes**.</span></span>

    ![Waarschuwingsbericht voor Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Waarschuwingsbericht voor Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="04e52-448">Als u Chrome als browser gebruikt en er een foutbericht wordt weergegeven waarin wordt aangegeven dat de sessie niet is gemaakt omdat de Chrome-versie niet juist is, downloadt u de meest recente versie van <http://chromedriver.chromium.org/downloads> naar de map **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="04e52-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Foutbericht voor Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="04e52-450">De testcase wordt uitgevoerd en het veld **Resultaat** wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="04e52-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Bijgewerkt resultaatveld](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="04e52-452">Als u deze zelfstudie hebt gevolgd zoals deze is geschreven, mislukt de testcase **Een nieuw product maken** omdat met de taakregistratie voor het maken van een product de productnaam is opgeslagen als een hard gecodeerde waarde.</span><span class="sxs-lookup"><span data-stu-id="04e52-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="04e52-453">Als u dezelfde testcase opnieuw uitvoert, wordt er een foutbericht weergegeven omdat het product al bestaat.</span><span class="sxs-lookup"><span data-stu-id="04e52-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Het veld Resultaat ingesteld op Mislukt](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="04e52-455">De testresultaten weergeven</span><span class="sxs-lookup"><span data-stu-id="04e52-455">View the test results</span></span>

1. <span data-ttu-id="04e52-456">Dubbelklik op de mislukte testcase.</span><span class="sxs-lookup"><span data-stu-id="04e52-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="04e52-457">U ontvangt een foutbericht.</span><span class="sxs-lookup"><span data-stu-id="04e52-457">You receive an error message.</span></span>

    ![Foutmelding](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="04e52-459">Selecteer **Details** om het volledige foutbericht weer te geven.</span><span class="sxs-lookup"><span data-stu-id="04e52-459">Select **Details** to view the whole error message.</span></span>

    ![Volledige foutbericht](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="04e52-461">Als u een gedetailleerde versie van het fout bericht in Azure DevOps wilt weergeven, selecteert u **Openen in Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="04e52-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="04e52-462">In Azure DevOps kunt u de status van de testcase en het gedetailleerde foutbericht bekijken.</span><span class="sxs-lookup"><span data-stu-id="04e52-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Gedetailleerd foutbericht in Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="04e52-464">Als u de testresultaten rechtstreeks in het Azure DevOps-project wilt weergeven, gaat u naar **Testplannen \> Testplannen \> Uitvoeringen**.</span><span class="sxs-lookup"><span data-stu-id="04e52-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="04e52-465">Dubbelklik op de testuitvoering waarover u meer details wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="04e52-465">Double-click the test run that you want to see more details for.</span></span>

    ![Lijst met testuitvoeringen in Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="04e52-467">Op het tabblad **Uitvoeringsoverzicht** wordt aangegeven dat de testcase is mislukt, maar het werkelijke foutbericht wordt niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04e52-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="04e52-468">Als u het gedetailleerde foutbericht wilt weergeven, selecteert u het tabblad **Testresultaten**.</span><span class="sxs-lookup"><span data-stu-id="04e52-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Het tabblad Uitvoeringsoverzicht](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="04e52-470">Het tabblad **Testresultaten** bevat informatie over de testcase, het resultaat en het foutbericht.</span><span class="sxs-lookup"><span data-stu-id="04e52-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Het tabblad Testresultaten](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="04e52-472">Dubbelklik op de relevante record om het gedetailleerde foutbericht weer te geven.</span><span class="sxs-lookup"><span data-stu-id="04e52-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Gedetailleerd foutbericht](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="04e52-474">Alle foutberichten zijn ook lokaal beschikbaar in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="04e52-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="04e52-475">U kunt de resultaten van de testuitvoering ook exporteren vanuit het niveau van het testplan door **Exporteren** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="04e52-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Een testplan exporteren](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="04e52-477">Het Excel-parameterbestand wijzigen</span><span class="sxs-lookup"><span data-stu-id="04e52-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="04e52-478">Open RSAT.</span><span class="sxs-lookup"><span data-stu-id="04e52-478">Open RSAT.</span></span>
2. <span data-ttu-id="04e52-479">Selecteer de testcase en selecteer vervolgens **Bewerken** om het Excel-parameterbestand te openen.</span><span class="sxs-lookup"><span data-stu-id="04e52-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="04e52-480">In het blad **EcoResProductCreate** is de waarde van het veld **Productnummer** hard gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="04e52-481">U moet dit veld bijwerken naar een nieuw productnummer voordat u de testcase opnieuw uitvoert.</span><span class="sxs-lookup"><span data-stu-id="04e52-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="04e52-482">Als u een uniek productnummer voor elke uitvoering wilt genereren zonder elke keer het Excel-parameterbestand opnieuw te hoeven openen en het productnummer handmatig te hoeven bijwerken, gebruikt u de volgende Excel-formule.</span><span class="sxs-lookup"><span data-stu-id="04e52-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="04e52-483">Naast het tabblad **Algemeen** bevat het Excel-parameterbestand een gegevenstabblad voor elke formulierpagina die de testcase bezoekt.</span><span class="sxs-lookup"><span data-stu-id="04e52-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Het veld Productnummer](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="04e52-485">Selecteer **Opslaan** en sluit de Excel-werkmap.</span><span class="sxs-lookup"><span data-stu-id="04e52-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="04e52-486">Selecteer **Uploaden** om het Excel-parameterbestand naar Azure DevOps op te slaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Bericht over geslaagde upload](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="04e52-488">Als u testcases in een specifieke gebruikerscontext wilt uitvoeren, typt u de e-mail-id van de gebruiker in het veld **Gebruiker testen** op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="04e52-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="04e52-489">In de meest recente versie van RSAT is de indeling van de velden in het Excel-parameterbestand bijgewerkt, maar het concept blijft hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="04e52-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Het veld Gebruiker testen](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="04e52-491">De resultaten valideren</span><span class="sxs-lookup"><span data-stu-id="04e52-491">Validate the results</span></span>

- <span data-ttu-id="04e52-492">Selecteer **Uitvoeren** om de testcase opnieuw uit te voeren en controleer of de testcase is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="04e52-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="04e52-493">U kunt de testresultaten weergeven op de wijze die wordt beschreven in de sectie [De testresultaten weergeven](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="04e52-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Het veld Resultaat ingesteld op Geslaagd](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="04e52-495">Koppelen van testcases</span><span class="sxs-lookup"><span data-stu-id="04e52-495">Chaining of test cases</span></span>

<span data-ttu-id="04e52-496">Eén belangrijke functie van RSAT is dat testcases kunnen worden aaneengeschakeld (waarden kunnen worden doorgegeven aan andere tests).</span><span class="sxs-lookup"><span data-stu-id="04e52-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="04e52-497">Testcases worden uitgevoerd volgens de gedefinieerde volgorde in het Azure DevOps-testplan.</span><span class="sxs-lookup"><span data-stu-id="04e52-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="04e52-498">(Deze volgorde kan ook worden bijgewerkt in het testprogramma zelf.) Als u variabelen wilt doorgeven van de ene testcase naar de andere, is het daarom zeer belangrijk dat de tests de juiste volgorde hebben.</span><span class="sxs-lookup"><span data-stu-id="04e52-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="04e52-499">In deze sectie maakt u een opgeslagen variabele in de eerste testcase, maakt u een tweede testcase en geeft u de opgeslagen variabele uit de eerste testcase door aan de tweede testcase.</span><span class="sxs-lookup"><span data-stu-id="04e52-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="04e52-500">Vervolgens voert u de testcases uit als een aangeschakelde testcase in RSAT.</span><span class="sxs-lookup"><span data-stu-id="04e52-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="04e52-501">Een bestaande taakregistratie wijzigen om een opgeslagen variabele te maken</span><span class="sxs-lookup"><span data-stu-id="04e52-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="04e52-502">Open de client.</span><span class="sxs-lookup"><span data-stu-id="04e52-502">Open the client.</span></span>
2. <span data-ttu-id="04e52-503">Selecteer de knop **Instellingen** (het tandwielsymbool) en selecteer **Taakregistratie**.</span><span class="sxs-lookup"><span data-stu-id="04e52-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="04e52-504">Selecteer **Opname bewerken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-504">Select **Edit Recording**.</span></span>

    ![De knop Opname bewerken](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="04e52-506">Selecteer **Openen vanuit Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="04e52-506">Select **Open from Lifecycle Services**.</span></span>

    ![De knop Openen vanuit Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="04e52-508">Selecteer **Selecteer de Lifecycle Services-bibliotheek**.</span><span class="sxs-lookup"><span data-stu-id="04e52-508">Select **Select the Lifecycle Services library**.</span></span>

    ![De knop Selecteer de Lifecycle Services-bibliotheek](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="04e52-510">BPM-bibliotheken worden geladen uit LCS.</span><span class="sxs-lookup"><span data-stu-id="04e52-510">BPM libraries are loaded from LCS.</span></span>

    ![BPM-bibliotheken laden](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="04e52-512">Nadat de BPM-bibliotheken vanuit LCS zijn geladen, selecteert u de BPM-bibliotheek **RSAT** en het bedrijfsproces **Een nieuw product maken** waaraan de taakregistratie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="04e52-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="04e52-513">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e52-513">Then select **OK**.</span></span>

    ![Een BMP-bibliotheek en een bedrijfsproces selecteren](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="04e52-515">De naam van de betreffende taakregistratie wordt ingevoerd in het veld **Naam van registratie**.</span><span class="sxs-lookup"><span data-stu-id="04e52-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="04e52-516">Selecteer **Starten**.</span><span class="sxs-lookup"><span data-stu-id="04e52-516">Select **Start**.</span></span>

    ![Naam van de taakregistratie in het veld Naam van registratie](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="04e52-518">Ga naar **Productgegevensbeheer \> Producten** en selecteer **Nieuw** om de pagina te openen waarop de oorspronkelijke taakregistratie **Een product maken** is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="04e52-519">Selecteer **Stap invoegen**.</span><span class="sxs-lookup"><span data-stu-id="04e52-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-520">De nieuwe stap wordt ingevoegd **na** de stap die u in het deelvenster hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="04e52-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![De knop Stap invoegen](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="04e52-522">Klik met de rechtermuisknop in het veld **Productnummer** en selecteer vervolgens **Taakregistratie \> Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![De opdracht Kopiëren](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="04e52-524">Er wordt een nieuwe stap toegevoegd in het deelvenster.</span><span class="sxs-lookup"><span data-stu-id="04e52-524">A new step is added in the pane.</span></span> <span data-ttu-id="04e52-525">Noteer de waarde in het veld **Productnummer**. U hebt deze later nog nodig.</span><span class="sxs-lookup"><span data-stu-id="04e52-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Nieuwe stap toegevoegd](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="04e52-527">Selecteer **Klaar met bewerken**.</span><span class="sxs-lookup"><span data-stu-id="04e52-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="04e52-528">Selecteer **Opslaan in Lifecycle Services** en koppel de nieuwe taakregistratie aan dezelfde BPM-bibliotheek en hetzelfde bedrijfsproces als de oorspronkelijke taakregistratie.</span><span class="sxs-lookup"><span data-stu-id="04e52-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="04e52-529">Zie de sectie [Een taakregistratie maken en opslaan in de BPM-bibliotheek](#create-a-task-recording-and-save-it-to-the-bpm-library) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="04e52-530">Ga naar de BPM-bibliotheek en selecteer **Testcases synchroniseren** om de taakregistratie te overschrijven die aan de testcase is gekoppeld in Azure DevOps, zoals wordt beschreven in [De synchronisatie van BPM naar Azure DevOps testen](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="04e52-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="04e52-531">Open RSAT en selecteer **Laden** om alle testcases opnieuw in de testsuite te laden.</span><span class="sxs-lookup"><span data-stu-id="04e52-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="04e52-532">U moet de automatiserings- en parameterbestanden voor de betreffende testcase opnieuw genereren door de testcase te selecteren en vervolgens **Nieuw \> Testuitvoering en parameterbestanden genereren** te selecteren, zoals wordt beschreven in de [Testcases laden en uitvoeren](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="04e52-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-533">Als het Excel-parameter bestand geopend was, mislukt de nieuwe generatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="04e52-534">Zorg er daarom voor dat het Excel-parameterbestand voor de testcase is gesloten voordat u het nieuwe Excel-parameterbestand genereert.</span><span class="sxs-lookup"><span data-stu-id="04e52-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="04e52-535">Selecteer **Bewerken** om het nieuwe Excel-parameterbestand te openen.</span><span class="sxs-lookup"><span data-stu-id="04e52-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="04e52-536">De nieuwe invoer **Opgeslagen variabele** wordt weergegeven op regel 9.</span><span class="sxs-lookup"><span data-stu-id="04e52-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="04e52-537">Deze variabele, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, wordt opgeslagen in het XML-bestand van de taakregistratie en kan in volgende tests worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="04e52-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Het item Opgeslagen variabele](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="04e52-539">Een nieuwe testcase maken</span><span class="sxs-lookup"><span data-stu-id="04e52-539">Create a new test case</span></span>

1. <span data-ttu-id="04e52-540">Ga naar de BPM-bibliotheek **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="04e52-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="04e52-541">Selecteer het proces **Sample Support Business Process** en selecteer vervolgens **Edit mode** rechts.</span><span class="sxs-lookup"><span data-stu-id="04e52-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="04e52-542">Wijzig de waarde van de velden **Name** en **Description** in **Een product vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="04e52-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="04e52-543">Selecteer **Save**.</span><span class="sxs-lookup"><span data-stu-id="04e52-543">Then select **Save**.</span></span>

    ![Naam en omschrijving gewijzigd in Een product vrijgeven](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="04e52-545">Een nieuwe taakregistratie maken met een functie Valideren</span><span class="sxs-lookup"><span data-stu-id="04e52-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="04e52-546">Maak een taakregistratie om het eerder gemaakte product vrij te geven aan de rechtspersoon USRT.</span><span class="sxs-lookup"><span data-stu-id="04e52-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="04e52-547">Zie de sectie [Een taakregistratie maken en opslaan in de BPM-bibliotheek](#create-a-task-recording-and-save-it-to-the-bpm-library) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04e52-548">Voor aangeschakelde testcases raden wij u aan altijd de benodigde record te zoeken of te filteren door de *waarde van het veld handmatig in te voeren*.</span><span class="sxs-lookup"><span data-stu-id="04e52-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="04e52-549">Op die manier kan worden bepaald voor welke record de actie moet worden uitgevoerd in de volgende testcase.</span><span class="sxs-lookup"><span data-stu-id="04e52-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Nieuwe taakregistratie met een functie Valideren](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="04e52-551">Zoals u in de vorige afbeelding kunt zien, kunt u, nadat u het product hebt gevonden met het snelfilter, voordat u **Producten vrijgeven** selecteert de waarde van het veld **Productnummer** valideren om er zeker van te zijn dat de product-id de product-id is die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04e52-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="04e52-552">Als u de waarde wilt valideren, klikt u met de rechtermuisknop in het veld **Productnummer** en selecteert u **Taakregistratie \> Valideren \> Huidige waarde**.</span><span class="sxs-lookup"><span data-stu-id="04e52-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![De huidige waarde valideren](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="04e52-554">De taakregistratie opslaan in BPM</span><span class="sxs-lookup"><span data-stu-id="04e52-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="04e52-555">Als de taakregistratie is voltooid, selecteert u **Opslaan in Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="04e52-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Voltooide taakregistratie opslaan in Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="04e52-557">Bibliotheekgegevens worden vanuit LCS geladen.</span><span class="sxs-lookup"><span data-stu-id="04e52-557">Library information is loaded from LCS.</span></span>

    ![Bibliotheekgegevens laden vanuit LCS](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="04e52-559">Selecteer de BPM-bibliotheek waaraan u de taakregistratie wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="04e52-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="04e52-560">Selecteer voor deze zelfstudie de BPM-bibliotheek **RSAT** die eerder is gemaakt en het bedrijfsproces **Een product vrijgeven** daaronder.</span><span class="sxs-lookup"><span data-stu-id="04e52-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="04e52-561">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e52-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="04e52-562">BPM synchroniseren naar Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="04e52-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="04e52-563">Ga naar de BPM-bibliotheek en open de bibliotheek **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="04e52-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="04e52-564">Selecteer **VSTS synchroniseren** en vervolgens **Testcases synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="04e52-565">Zie de sectie [De synchronisatie van BPM naar Azure DevOps testen](#test-the-synchronization-from-bpm-to-azure-devops) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="04e52-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="04e52-566">Als de synchronisatie is voltooid, worden het nieuwe werkitem en de bijbehorende testcase voor het bedrijfsproces **Een product vrijgeven** weergegeven in Azure DevOps in **Borden \> Werkitems**.</span><span class="sxs-lookup"><span data-stu-id="04e52-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="04e52-567">De nieuwe testcase toevoegen aan de bestaande testsuite</span><span class="sxs-lookup"><span data-stu-id="04e52-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="04e52-568">Ga naar **Testplannen \> Testplannen** en selecteer het plan **RSAT-testplan**.</span><span class="sxs-lookup"><span data-stu-id="04e52-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="04e52-569">Selecteer **Bestaande toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="04e52-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="04e52-570">Selecteer **Query uitvoeren** op de pagina **Testcases toevoegen aan suite**.</span><span class="sxs-lookup"><span data-stu-id="04e52-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="04e52-571">Selecteer de nieuwe testcase die voor **Een product vrijgeven** is gemaakt en selecteer vervolgens **Testcases toevoegen** in de rechterbenedenhoek van de pagina (deze knop wordt niet weergegeven in de volgende afbeelding).</span><span class="sxs-lookup"><span data-stu-id="04e52-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![De pagina Testcases toevoegen aan suite](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="04e52-573">De testsuite bevat nu twee testcases.</span><span class="sxs-lookup"><span data-stu-id="04e52-573">The test suite now has two test cases.</span></span>

    ![Twee testcases in de testsuite](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="04e52-575">Testcases in RSAT laden</span><span class="sxs-lookup"><span data-stu-id="04e52-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="04e52-576">Open RSAT en selecteer **Laden**.</span><span class="sxs-lookup"><span data-stu-id="04e52-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="04e52-577">De testcases worden geladen en er wordt een waarschuwing weergegeven om aan te geven dat de actie Excel-testgegevensbestanden overschrijft en lokale wijzigingen verloren gaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="04e52-578">Daarnaast wordt gevraagd of u wilt doorgaan.</span><span class="sxs-lookup"><span data-stu-id="04e52-578">Do you want to proceed?"</span></span> <span data-ttu-id="04e52-579">Selecteer **Ja** als u de Excel-parameterbestanden wilt bijwerken in het lokale systeem, maar niet de Excel-parameterbestanden die zijn geüpload naar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="04e52-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Met deze actie worden Excel-testgegevensbestanden overschreven.](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="04e52-581">Beide testcases worden geladen, samen met het Excel-parameterbestand voor de eerste testcase.</span><span class="sxs-lookup"><span data-stu-id="04e52-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="04e52-582">Omdat u **Uploaden** hebt geselecteerd bij de laatste uitvoering, worden de parameterbestanden opgehaald uit Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="04e52-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Testcases geladen](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="04e52-584">Selecteer alleen de tweede testcase en selecteer vervolgens **Nieuw \> Testuitvoering en parameterbestanden genereren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="04e52-585">Het Excel-parameterbestand bewerken</span><span class="sxs-lookup"><span data-stu-id="04e52-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="04e52-586">Selecteer alleen de tweede testcase en selecteer vervolgens **Bewerken** om het bijbehorende Excel-parameterbestand te openen.</span><span class="sxs-lookup"><span data-stu-id="04e52-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="04e52-587">Kopieer de opgeslagen variabele **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (zie de sectie [Een bestaande taakregistratie wijzigen om een opgeslagen variabele te maken](#modify-an-existing-task-recording-to-create-a-saved-variable)) uit de eerste testcase in alle velden waarin het productnummer wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="04e52-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="04e52-588">In dit geval kopieert u de variabele naar de velden **Productnummer** en **Productnummer valideren** op het blad **EcoResproductListPage**.</span><span class="sxs-lookup"><span data-stu-id="04e52-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![De velden Productnummer en Productnummer valideren](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="04e52-590">Variabelen kunnen alleen tijdens dezelfde testuitvoering worden doorgegeven tussen tests.</span><span class="sxs-lookup"><span data-stu-id="04e52-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="04e52-591">De namen van de variabelen moeten exact overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="04e52-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="04e52-592">Selecteer **Opslaan** en sluit de Excel-werkmap.</span><span class="sxs-lookup"><span data-stu-id="04e52-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="04e52-593">Selecteer **Uploaden** om de wijzigingen op te slaan die u in het Excel-parameterbestand hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="04e52-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="04e52-594">De aaneengeschakelde testcases uitvoeren</span><span class="sxs-lookup"><span data-stu-id="04e52-594">Run the chained test cases</span></span>

1. <span data-ttu-id="04e52-595">Selecteer beide testcases die u wilt uitvoeren en selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="04e52-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="04e52-596">Controleer of de testcases zijn geslaagd.</span><span class="sxs-lookup"><span data-stu-id="04e52-596">Verify that both test cases have passed.</span></span>

    ![Het veld Resultaat ingesteld op Geslaagd voor beide testcases](./media/setup_rsa_tool_105.png)
